---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025429"
---
# <a name="cart-module"></a>Modul košíku


[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul košíku se používá k zobrazení položek, které byly přidány do košíku, než odběratel pokračuje v rezervaci. Obsahuje například všechny položky, které byly přidány do nákupního košíku a souhrn objednávky. Dále umožňuje odběrateli použití nebo odebrání propagačních kódů.

Modul košíku podporuje přihlášené uživatele i hosty. Také podporuje odkaz **Zpět na nákupy**. Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.

Modul košíku vykresluje data na základě ID košíku. ID košíku je soubor cookie prohlížeče, který je k dispozici v rámci celého webu.

## <a name="cart-module-properties-and-slots"></a>Vlastnosti a pozice modulu košíku

Modul košíku má vlastnost **Záhlaví**, kterou lze nastavit na hodnoty, jako je **Nákupní taška** a **Položky v košíku**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduly, které lze použít v modulu košíku

- **Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku. Zprávy řídí systém správy obsahu (CMS). Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.
- **Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji. Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí. Modul volby obchodu je integrovaný s API geokódování služby Mapy Bing, které slouží k převodu umístění na zeměpisnou šířku a délku. Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky sdílené parametry pro Retail v aplikaci Dynamics 365 Retail. Tento modul podporuje dvě vlastnosti, **Okruh hledání** a **Odkaz na podmínky služby**. Vlastnost **Okruh hledání** definuje poloměr vyhledávání pro obchody v mílích. Není-li zadána žádná hodnota, použije se výchozí poloměr vyhledávání 50 mil. Pokud se používají mapy Bing nebo některá externí služba, vlastnost **Odkaz na podmínky služby** se používá k získání odkazu na podmínky služby. Pro službu Bing Maps je vyžadován odkaz na podmínky služby. 

## <a name="cart-module-settings"></a>Nastavení modulu košíku

Moduly košíku mají následující nastavení, která lze konfigurovat na **Nastavení webu \> Rozšíření**:

- **Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku. Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.
- **Kontrola zásob** – Je-li nastavena hodnota **Pravda**, položka se přidá do košíku pouze poté, co se modul buy boxu ověří, že je na skladě. Tato kontrola zásob se provádí pro scénáře, když má být položka expedována, a pro scénáře, kdy má být vyzvednuta v obchodě. Je-li tato hodnota nastavena na hodnotu **Nepravda**, před přidáním položky do nákupního košíku a podání objednávky není provedena kontrola zásob.
- **Zásboník zásob** – Tato vlastnost se používá k určení čísla zásobníku pro zásoby. Údržba zásob probíhá v reálném čase a když mnoho zákazníků podá objednávku, může být obtížné zajistit přesný počet zásob. Když je provedena kontrola zásob, pokud je množství na skladu nižší než množství zásobníku, produkt je brán, jakože není na skladu. Pokud se tedy prodej rychle točí prostřednictvím několika kanálů a zásoby nejsou plně synchronizovány, existuje menší riziko, že položka, která se nenachází na skladě, je v prodeji.
- **Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**. Tento postup lze konfigurovat na úrovni pracoviště. Tuto konfiguraci maloobchodní prodejci používají pro nasměrování zákazníků zpět na domovskou stránku nebo jakoukoli jinou stránku na webu.

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit. ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Přidání modulu košíku na stránku

Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte fragment s názvem **Fragment košíku** a do něj přidejte modul košíku.
1. Přidejte do modulu košíku nadpis.
1. Přidejte modul Selector obchodu do modulu vozík.
1. Uložte fragment, dokončete úpravy a publikujte ji.
1. Vytvořte šablonu s názvem **Šablona košíku** a přidejte fragment košíku, který jste právě vytvořili.
1. Uložte šablonu, dokončete úpravy a publikujte ji.
1. Vytvořte stránku, která používá novou šablonu.
1. Uložte stránku a zobrazte náhled.
1. Dokončete úpravy stránky a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
