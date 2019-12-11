---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696754"
---
# <a name="cart-module"></a>Modul košíku

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul košíku je kontejner, který se používá k hostování všech modulů, které jsou nutné k prezentaci položek, které jsou v nákupním košíku. Obsahuje například všechny položky, které byly přidány do nákupního košíku, souhrn objednávky a propagační kódy.

Modul košíku vykresluje data na základě ID košíku. ID košíku je soubor cookie prohlížeče, který je k dispozici v rámci celého webu.

## <a name="cart-module-properties-and-slots"></a>Vlastnosti a pozice modulu košíku

Coby kontejner řídí modul košíku některé základní vlastnosti, jako nadpis a šířka. Nadpis je obvykle text jako **Nákupní taška**, **Váš nákupní košík** nebo **Položky v nákupním košíku**. Nastavení šířky určuje, zda se moduly uvnitř kontejneru musí vejít do tohoto kontejneru nebo zda mohou vyplnit obrazovku.

Stránka košíku je rozdělena do více oblastí: řádky položek v košíku, souhrn objednávky a pokladna a funkce Hledat v obchodě. Každá oblast je mapována na pozici v modulu košíku a každá pozice přijímá předdefinovanou sadu modulů.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduly, které lze použít v modulu košíku

- **Řádky položek v košíku** – Tento modul zobrazuje souhrn všech položek, které byly přidány do nákupního košíku. Tyto informace zahrnují název produktu, vybrané rozměry, cenu, množství a slevy. Tento modul také podporuje akce jako „odebrat z košíku“ a „přidat do seznamu přání“. Pro každou položku na řádku existuje možnost ji expedovat nebo vyzvednout z obchodu. Tato možnost musí být nakonfigurována samostatně v modulu vyzvednutí v obchodě.
- **Souhrn objednávky** – Tento modul zobrazuje souhrn objednávky. Tyto informace zahrnují mezisoučet, expedici, daně a úspory. Pro tento modul lze konfigurovat nadpis.
- **Propagační kód** – Tento modul umožňuje zákazníkům uplatnit propagační kódy. Propagační kód lze použít nebo odebrat.
- **Pokladna** – Tento modul inicializuje akci pokladny a přesměruje uživatele na stránku pokladny. Pro tento modul musí být nakonfigurovány tři odkazy:

    - **Pokladna** – Tento odkaz vynutí, aby se zákazníci přihlásili, nejsou-li již přihlášeni.
    - **Pokladna** hosta – Tento odkaz umožňuje anonymním zákazníkům podat objednávku. Zobrazí se jen tehdy, když nejsou zákazníci přihlášeni.
    - **Zpět k nakupování** – Tento odkaz zákazníkům umožňuje přejít na domovskou stránku nebo nějakou jinou stránku, aby mohli pokračovat v nakupování.

- **Blok s formátovaným obsahem** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku. Zprávy řídí systém správy obsahu (CMS). Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.
- **Vyzvednout v obchodě** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji. Standardně tento modul zobrazuje obchody, které jsou v okruhu 80 km umístění zákazníka. Okruh hledání však můžete upravit v modulu. U každého obchodu se provádí kontrola zásob, je-li zapnuta funkce kontroly zásob a je zobrazena odpovídající zpráva na skladě nebo není na skladě.
- **Hledání obchodů v mapách Bing** – Tento modul lze použít uvnitř modulu vyzvednutí v obchodě. Umožňuje zákazníkům vyhledávat obchody zadáním umístění. Programovací rozhraní (API) pro aplikaci geokódování služby Mapy Bing, které slouží k převodu zákazníkem zadaného umístění na zeměpisnou šířku a délku. Není-li použit tento modul, zobrazí se pouze obchody, které jsou poblíž aktuálního umístění zákazníka, a zákazník nebude moci vyhledat jiné umístění.

## <a name="cart-module-settings"></a>Nastavení modulu košíku

Moduly košíku mají tři nastavení, která lze konfigurovat:

- **Maximální množství** – Maximální počet jednotlivých položek, které lze přidat do nákupního košíku. Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.
- **Kontrola zásob** – Je-li nastavena hodnota **Pravda**, položka se přidá do košíku pouze poté, co se modul buy boxu ověří, že je na skladě. Tato kontrola zásob se provádí pro scénáře, když má být položka expedována, a pro scénáře, kdy má být vyzvednuta v obchodě. Je-li tato hodnota nastavena na hodnotu **Nepravda**, před přidáním položky do nákupního košíku a podání objednávky není provedena kontrola zásob.
- **Zásboník zásob** – Údržba zásob probíhá v reálném čase a když mnoho zákazníků podá objednávku, může být obtížné zajistit přesný počet zásob. Proto lze pro zásoby definovat zásobník. Když je provedena kontrola zásob, pokud je množství na skladu nižší než množství zásobníku, produkt je brán, jakože není na skladu. Pokud se tedy prodej rychle točí prostřednictvím několika kanálů, takže zásoby nejsou plně synchronizovány, existuje menší riziko, že položka, která se nenachází na skladě, je v prodeji.

## <a name="retail-server-interaction"></a>Interakce se serverem maloobchodu

Modul košíku načítá informace o produktu pomocí rozhraní API serveru maloobchodu. ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu ze serveru maloobchodu.

## <a name="add-a-cart-module-to-a-page"></a>Přidání modulu košíku na stránku

Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte fragment s názvem **Fragment košíku** a do něj přidejte modul košíku.
1. V pozici **Řádky položek v košíku** v modulu košíku přidejte modul položky řádků položek v nákupním košíku.
1. V pozici **Souhrn objednávky** přidejte modul souhrnu objednávky.
1. V pozici **Propagační kód** přidejte modul propagačního kódu.
1. V pozici **Pokladna** přidejte modul pokladny.
1. Do pozice **Hledat v obchodě** přidejte modul vyhledání v obchodě.
1. V modulu vyzvednutí v obchodě vyberte pozici **Hledání obchodů** a přidejte modul hledání obchodů v mapách Bing.
1. Vraťte fragment se změnami a publikujte jej.
1. Vytvořte šablonu s názvem **Šablona košíku** a přidejte fragment košíku, který jste právě vytvořili.
1. Uložte šablonu, vraťte ji se změnami a publikujte.
1. Vytvořte stránku, která používá novou šablonu.
1. Uložte stránku a zobrazte náhled.
1. Vraťte stránku se změnami a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
