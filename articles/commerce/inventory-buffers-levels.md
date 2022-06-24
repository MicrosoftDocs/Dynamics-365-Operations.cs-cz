---
title: Konfigurace rezervních zásob a úrovní zásob
description: Tento článek vysvětluje, jak konfigurovat rezervní zásoby a úrovně zásob, které určují zasílání zpráv o dostupnosti zásob na weby Microsoft Dynamics 365 Commerce.
author: boycezhu
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: acfe71f7fb55f1bc701297bb3949e91d6450d9e9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853786"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Konfigurace rezervních zásob a úrovní zásob

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak konfigurovat rezervní zásoby a úrovně zásob, které určují zasílání zpráv o dostupnosti zásob na weby Microsoft Dynamics 365 Commerce.

Centrála Dynamics 365 Commerce uchovává údaje o zásobách a různé kanály, jako jsou aplikace v místě prodeje (POS), poutače e-Commerce a další vlastní integrované aplikace, které řídí oběh zásob asynchronním způsobem. Dostupné hodnoty inventáře, které se získají prostřednictvím stránky inventáře v centrále Commerte, prostřednictvím uživatelského rozhraní POS (UI) a prostřednictvím rozhraní API pro dostupnost zásob elektronického obchodování, tedy nejsou vždy v reálném čase vždy stoprocentně přesné.

Namísto zobrazování skutečných hodnot zásob v poutačích elektronického obchodu mnoho prodejců upřednostňuje pouze zobrazování zpráv o stavu dostupnosti zásob (například „Dostupné“ nebo „Vyprodáno“), aby informovalo zákazníky o tom, zda je položka k dispozici ke koupi nebo potenciálně vyprodána. Pro tento přístup musí být zpřístupněny a nakonfigurovány rezervní zásoby a úrovně zásob, které určují zprávy o dostupnosti zásob.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Předpoklad: Zapněte funkce rezervních zásob a úrovní zásob

Funkce pro rezervní zásoby a úrovně zásob je řízena pomocí správy funkcí v centrále Commerce. Chcete-li funkci zapnout, postupujte následujícím způsobem.

1. Přejděte do nabídky **Správa systému** \> **Pracovní prostory** \> **Správa funkcí**.
1. Vyhledejte **Povolit rezervní zásoby a úrovně zásob**, vyberte jeho řádek a poté vyberte **Povolit hned**.

Po zapnutí funkce najdete úrovně zásob na **Retail a Commerce \> Řízení zásob**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Vytvořte a nakonfigurujte profil úrovně zásob

*Profil úrovně zásob* určuje, zda je daný stav množství produktu považován na skladě, vyprodán nebo v jiném vlastním stavu. Můžete vytvořit a konfigurovat více profilů úrovně zásob na právnickou osobu. Každý profil se skládá ze sady úrovní zásob a každá úroveň je definována pomocí *rozsahu*, *kódu* a *popisku*.

- **Rozsah** - Každý rozsah je definován a *počátečním množstvím* a *konečným množstvím*. Hodnota množství spadá do rozsahu, pokud je větší než počáteční množství tohoto rozsahu a ne více než konečné množství.
- **Kód** - Kód je vnitřní zkratka, která představuje úroveň. Zákazníci, kteří se přímo integrují s rozhraními API pro zásoby, mohou pomocí kódů vytvořit další logiku pro danou úroveň zásob. Například mohou vypnout funkci nákupu produktu, když je jeho kód úrovně zásob **OOS** ("vyprodáno").
- **Popisek** - Popisek je smysluplná zpráva zaměřená na zákazníka, která zákazníkům zprostředkovává úroveň inventáře na webu elektronického obchodu.

### <a name="create-an-inventory-level-profile"></a>Vytvořte profil úrovně zásob

Chcete-li vytvořit profil úrovně zásob, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce** \> **Řízení zásob** \> **Úrovně zásob**.
1. Na podokně Akce vyberte **Nový** a poté zadejte hodnoty do polí **ID profilu** a **Popis**.
1. Na pevné záložce **Rozsahy** vyberte **Přidat** a přidejte novou úroveň a poté zadejte hodnoty do slouců **Počáteční množství**, **Konečné množství**, **Kód** a **Popisek** pro tuto úroveň. Zopakujte tento krok, chcete-li přidat další úrovně. Podle potřeby můžete upravit hodnoty v datové mřížce, nebo můžete vybrat **Odstranit** a odstranit úroveň.
1. V podokně akcí vyberte **Uložit**.

Po vytvoření nového profilu se automaticky inicializují dvě úrovně zásob:

- **OOS** - úroveň „vyprodáno“, kde dolní mez rozsahu je záporné nekonečno. Počáteční množství a kód nelze pro tuto úroveň upravit.
- **AVAIL** - "dostupná" úroveň, kde horní hranice rozsahu je nekonečno. Koncové množství a kód nelze pro tuto úroveň upravit.

> [!NOTE]
> V definici profilu nemohou být mezery ani překrývání mezi rozsahy.

Můžete použít tlačítko **Překlady** v podokně Akce pro konfiguraci lokalizovaných řetězců pro zprávu se štítkem. Poté musíte spustit distribuční rozvrhovací úlohu **1110** (**Globální konfigurace**) pro synchronizaci lokalizovaných řetězců s kanály.

### <a name="configure-an-inventory-level-profile"></a>Konfigurujte profil úrovně zásob

Profil úrovně zásob můžete nakonfigurovat buď na úrovni kategorie produktu, nebo na úrovni jednotlivých produktů. Když je pro produkt nakonfigurován profil úrovně zásob, je úroveň zásob stanovena na základě rozsahů definovaných v propojeném profilu. V opačném případě se úroveň zásob „dostupná“ nebo „vyprodaná“ stanoví na základě toho, zda má produkt kladné množství na skladě.

Chcete-li konfigurovat profil úrovně zásob pro kategorii, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce** \> **Produkty a kategorie** \> **Hierarchie produktů Commerce**.
1. Chcete-li konfigurovat profil úrovně zásob pro kategorii, vyberte kategorii.
1. Na pevné záložce **Vlastnosti prodávaného produktu** vyberte právnickou osobu.
1. V sekci **Zásoby Commerte** v poli **Profil úrovně zásob** vyberte jeden z předdefinovaných profilů úrovně zásob.

Můžete použít tlačítko **Aktualizovat produkty** v podokně akcí, chcete-li rozšířit hodnotu profilu na úrovni kategorie do produktů, na které se daná kategorie vztahuje. Další informace viz [Správa kategorií produktů a produktů](category-management-product-creation.md).

Chcete-li konfigurovat profil úrovně zásob pro uvolněný produkt, postupujte následujícím způsobem.

1. Přejděte do nabídky **Retail a Commerce** \> **Produkty a kategorie** \> **Uvolněné produkty podle kategorie**.
1. Vyberte produkt a poté otevřete stránku s podrobnostmi o produktu.
1. Na pevné záložce **Prodej**, v sekci **Zásoby Commerce** v poli **Profil úrovně zásob** vyberte jeden z předdefinovaných profilů úrovně zásob.

Když je vytvořen nový produkt, pole **Profil úrovně zásob**, stejně jako mnoho dalších atributů na úrovni produktu, bude nastaveno na hodnotu nakonfigurovanou pro kategorii, ke které je produkt přidružen.

> [!NOTE]
> Profil úrovně zásob je atribut specifický pro právnickou osobu. U stejné kategorie nebo produktu se hodnota profilu úrovně zásob může u právnických osob lišit.

Chcete-li synchronizovat konfigurace profilů úrovně zásob s kanály, postupujte takto.

1. Přejděte na **Retail a Commerce** \> **IT pro Retail a Commerce** \> **Plán distribuce**.
1. Spusťte plán distribuce **1040** (**Produkt**).

## <a name="configure-an-inventory-buffer"></a>Nakonfigurujte rezervní zásoby

*rezervní zásoby* je uživatelem definovaná hodnota, která odečte dodatečné množství položky od původního množství pro výpočet odhadovaného množství. Toto odhadované množství poskytuje maloobchodníkům bezpečnou rezervu, aby neprodali produkt tím, že by prodali více, než jsou jeho skutečné zásoby na skladě. Rezervní zásoby můžete nakonfigurovat buď na úrovni kategorie produktu, nebo na úrovni jednotlivých produktů. Nejsou-li zadány žádné rezervní zásoby, použije se výchozí hodnota **0** (nula).

Chcete-li konfigurovat rezervní zásoby pro kategorii, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce** \> **Produkty a kategorie** \> **Hierarchie produktů Commerce**.
1. Chcete-li konfigurovat rezervní zásoby pro kategorii, vyberte kategorii.
1. Na pevné záložce **Vlastnosti prodávaného produktu** vyberte právnickou osobu.
1. V sekci **Zásoby Commerce** v poli **Rezervní zásoby** zadejte kladnou hodnotu.

Můžete použít tlačítko **Aktualizovat produkty** v podokně akcí, chcete-li rozšířit hodnotu rezervy na úrovni kategorie do produktů, na které se daná kategorie vztahuje. Další informace viz [Správa kategorií produktů a produktů](category-management-product-creation.md).

Chcete-li konfigurovat rezervní zásoby pro uvolněný produkt, postupujte následujícím způsobem.

1. Přejděte do nabídky **Retail a Commerce** \> **Produkty a kategorie** \> **Uvolněné produkty podle kategorie**.
1. Vyberte produkt a poté otevřete stránku s podrobnostmi o produktu.
1. Na pevné záložce **Prodej**, v sekci **Zásoby Commerce** v poli **Rezervní zásoby** zadejte kladnou hodnotu.

Když je vytvořen nový produkt, pole **Rezervní zásoby** bude nastaveno na hodnotu nakonfigurovanou pro kategorii, ke které je produkt přidružen.

> [!NOTE]
> Pokud jsou pro produkt nakonfigurovány jak rezervní zásoby, tak i úrovně zásob, odhadované množství produktu (tj. původní množství minus hodnota rezervy) bude použito pro výpočet rozsahu k určení úrovně zásob.

Chcete-li synchronizovat konfigurace rezervních zásob s kanály, postupujte takto.

1. Přejděte na **Retail a Commerce** \> **IT pro Retail a Commerce** \> **Plán distribuce**.
1. Spusťte plán distribuce **1040** (**Produkt**).

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Použijte rezervní zásoby a úrovně zásob ve scénáři elektronického obchodování

Tvůrce webu Commerce používá funkce rezervních zásob a úrovně zásob v centrále Commerce k určování zpráv o dostupnosti zásob na webech elektronického obchodování. Další informace [Použít nastavení zásob](inventory-settings.md).

Pokud se integrujete s řešením elektronického obchodování třetí strany, můžete použít rozhraní API **GetEstimatedAvailability** a **GetEstimatedProductWarehouseAvailability** pro zobrazení dostupnosti zásob pro produkt ve scénáři elektronického obchodování. Další informace o těchto API najdete na stránce [Vypočítat dostupnost zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md).

Zavedení rezerv zásob a úrovní zásob umožňuje těmto API vrátit kódy úrovně zásob a zprávy popisků, které jsou určeny na základě celkových dostupných a dostupných fyzických hodnot. API lze dále konfigurovat, aby určily, zda je množství zásob vráceno společně se zprávou a zda je dostupné množství sníženo o hodnotu rezervy zásob.

Chcete-li nakonfigurovat odpověď API dostupnosti produktu, postupujte takto.

1. Přejděte na možnost **Retail a Commerce** \> **Nastavení centrály** \> **Parametry** \> **Parametry obchodu**.
1. V sekci **Zásoby vy skladu** na kartě **Zásoby** v poli **Rozhraní API pro dostupnost produktů pro elektronický obchod** vyberte hodnotu.
1. Chcete-li použít nastavení na kanály, spusťte úlohu distribučního plánu **1110** (**Globální konfigurace**).

## <a name="additional-resources"></a>Další prostředky

[Správa kategorií produktů a produktů](category-management-product-creation.md)

[Použití nastavení zásob](inventory-settings.md)

[Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
