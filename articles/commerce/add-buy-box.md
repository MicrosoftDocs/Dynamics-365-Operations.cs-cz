---
title: Modul buy boxu
description: Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811134"
---
# <a name="buy-box-module"></a>Modul buy boxu

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Termín *buy box* se obvykle vztahuje k oblasti stránky s podrobnostmi o produktu, která se nachází „above the fold“ a která je hostitelem nejdůležitějších informací vyžadovaných k provedení nákupu produktu. (Oblast „above the fold“ je viditelná po prvním načtení stránky, takže uživatelé nemusejí posouvat zobrazení směrem dolů, aby ji viděli.)

Modul buy boxu je speciální kontejner, který slouží k hostování všech modulů, které jsou zobrazeny v oblasti buy boxu na stránce podrobností produktu.

Adresa URL stránky s podrobnostmi o produktu obsahuje ID produktu. Všechny informace, které jsou požadovány pro vygenerování modulu buy boxu, jsou odvozeny z tohoto ID produktu. Není-li zadáno ID produktu, nebude modul buy boxu na stránce správně vykreslen. Proto nelze použít modul buy boxu na žádné stránce, která nemá kontext produktu (například domovská stránka nebo marketingová stránka).

## <a name="buy-box-module-properties-and-slots"></a>Vlastnosti a pozice modulu buy boxu 

Coby kontejner řídí modul buy boxu některé základní vlastnosti, jako je například šířka. Nastavení šířky určuje, zda se moduly uvnitř kontejneru musí vejít do tohoto kontejneru nebo zda mohou vyplnit obrazovku.

Na stránce s podrobnostmi o produktu je buy box rozdělen na dvě oblasti: oblast médií v levé části a oblast obsahu vpravo. Tyto dvě oblasti jsou reprezentovány pozicemi v modulu buy boxu. Každá pozice je předem nakonfigurována tak, aby přijímala pouze určité moduly, které jsou v pozici podporovány. Například pozice **Média** podporuje pouze modul galerie médií.

Standardně je poměr šířek sloupců pro oblast médií a oblast obsahu 2:1. Šířku sloupců však může být přepsána motivem. Kromě toho jsou na mobilních zařízeních obě oblasti navrstveny, takže se jedna oblast zobrazí pod druhou oblastí.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduly, které lze použít v modulu buy boxu

- **Galerie médií** – Tento modul slouží k předvedení obrázků produktu na stránce s podrobnostmi o produktu. Může podporovat jeden nebo mnoho obrázků. Podporuje také obrázky miniatur. Obrázky miniatur lze uspořádat vodorovně (jako řádek pod obrázkem) nebo svisle (jako sloupec vedle obrázku). Modul galerie médií lze přidat do pozice **Média** v modulu buy boxu. V současné době podporuje pouze obrázky a videa.
- **Název produktu** – Tento modul zobrazuje název produktu na stránce podrobností produktu. Standardně je použita značka nadpisu **H1**, ale značku nadpisu lze podle potřeby změnit.
- **Hodnocení produktu** – Tento modul zobrazuje hodnocení pomocí hvězdiček na základě zákaznického hodnocení produktu. Modul buy boxu načte hodnocení produktu pro jednotlivé produkty ze služby hodnocení.
- **Cena produktu** – Tento modul zobrazuje cenu produktu. Cena zahrnuje přeškrtnuté ceny a slevy.
- **Popis produktu** – Tento modul zobrazuje popis produktu.
- **Konfigurace produktu** – Tento modul zobrazuje velikost, styl a rozměry produktu. Selektory rozměrů lze skládat svisle nebo je možné je zobrazit vedle sebe. Je-li vybrána varianta produktu, budou další vlastnosti v buy boxu (například popis a obrázky produktu) aktualizovány tak, aby odrážely informace o variantách.
- **Množství produktu** – Tento modul se používá ke konfiguraci množství produktu. Nastavení omezuje množství produktu nebo varianty, které lze přidat do nákupního košíku.
- **Přidat do nákupního košíku** – Tento modul slouží k provedení akce „Přidat do košíku“. Do nákupního košíku lze přidat pouze produkt nebo variantu. Jinými slovy, hlavní produkt nelze přidat do košíku. Modul obsahuje vlastnost **Přejít do nákupního košíku**, kterou může nastavit autor webu. Je-li tato vlastnost nastavena na hodnotu **Pravda**, uživatel je přesměrován na stránku nákupního košíku vždy, když je aktivována akce „Přidat do košíku“. Je-li nastavena na hodnotu **Nepravda**, může zákazník pokračovat v procházení stránky s podrobnostmi o produktu po přidání položek do nákupního košíku.
- **Přidat do seznamu přání** – Tento modul slouží k přidání položky do seznamu přání odběratele. Do seznamu přání lze přidat pouze produkt nebo variantu. Dále je nutné, aby byl zákazník přihlášen k danému webu. Modul zahrnuje logiku zpracování chyb, aby bylo zajištěno, že obě tyto podmínky budou splněny.
- **Hledat v obchodě** – Tento modul aktivuje tok „koupit online, vyzvednout v obchodě“.
- **Vyzvednout v obchodě** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji. Standardně tento modul zobrazuje obchody, které jsou v okruhu 80 km umístění zákazníka. Okruh hledání však můžete upravit v modulu. U každého obchodu se provádí kontrola zásob, je-li zapnuta funkce kontroly zásob a je zobrazena odpovídající zpráva na skladě nebo není na skladě.
- **Hledání obchodů v mapách Bing** – Tento modul lze použít uvnitř modulu vyzvednutí v obchodě. Umožňuje zákazníkům vyhledávat obchody zadáním umístění. Programovací rozhraní (API) pro aplikaci geokódování služby Mapy Bing, které slouží k převodu zadaného umístění na zeměpisnou šířku a délku. Je-li použit tento modul, zobrazí se pouze obchody, které jsou poblíž aktuálního umístění zákazníka, a zákazník nebude moci vyhledat jiné umístění.
- **Blok s formátovaným obsahem** – Tento modul může zobrazit zprávu, kterou autor webu nebo prodejce chce umístit do buy boxu, například „Při problémech s objednávkou volejte 123 456 789“ nebo „Poštovné zdarma při objednávce nad 1000 Kč“. Zprávy řídí systém správy obsahu (CMS).

## <a name="buy-box-module-settings"></a>Nastavení modulu buy boxu

Moduly buy boxu mají tři nastavení, která lze konfigurovat:

- **Maximální množství** – Maximální počet jednotlivých položek, které lze přidat do nákupního košíku. Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.
- **Kontrola zásob** – Je-li nastavena hodnota **Pravda**, položka se přidá do košíku pouze poté, co se modul buy boxu ověří, že je na skladě. Tato kontrola zásob se provádí pro scénáře, když má být položka expedována, a pro scénáře, kdy má být vyzvednuta v obchodě. Je-li tato hodnota nastavena na hodnotu **Nepravda**, před přidáním položky do nákupního košíku a podání objednávky není provedena kontrola zásob.
- **Zásboník zásob** – Údržba zásob probíhá v reálném čase a když mnoho zákazníků podá objednávku, může být obtížné zajistit přesný počet zásob. Proto lze pro zásoby definovat zásobník. Když je provedena kontrola zásob, pokud je množství na skladu nižší než množství zásobníku, produkt je brán, jakože není na skladu. Pokud se tedy prodej rychle točí prostřednictvím několika kanálů, takže zásoby nejsou plně synchronizovány, existuje menší riziko, že položka, která se nenachází na skladě, je v prodeji.

## <a name="retail-server-interaction"></a>Interakce se serverem maloobchodu

Modul buy boxu načítá informace o produktu pomocí rozhraní API serveru maloobchodu. ID produktu ze stránky s podrobnostmi o produktu slouží k načtení všech informací.

## <a name="add-a-buy-box-module-to-a-page"></a>Přidání modulu buy boxu na stránku

Chcete-li přidat modul buy boxu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte fragment s názvem **Fragment buy boxu** a do něj přidejte modul buy boxu.
1. Do pozice **Média** modulu buy boxu přidejte modul galerie médií.
1. Do pozice **Obsah** modulu buy boxu přidejte následující moduly: název produktu, hodnocení produktu, cena produktu, popis produktu, konfigurace produktu, přidat do košíku, přidat do seznamu přání a hledat v obchodě. Rozložení modulů v pozici **Obsah** můžete dle libosti změnit.
1. Vyberte modul pro vyhledání v obchodě. V pozici uvnitř tohoto modulu přidejte modul pro vyzvednutí v obchodě.
1. V pozici uvnitř modulu vyzvednutí v obchodě přidejte modul hledání obchodů v mapách Bing.
1. Vraťte stránku se změnami a publikujte ji.
1. Vytvořte šablonu pro stránku s podrobnostmi o produktu a pojmenujte ji **Šablona POP**.
1. Přidejte výchozí stránku.
1. V pozici **Hlavní** na výchozí stránce přidejte fragment buy boxu.
1. Uložte šablonu, vraťte ji se změnami a publikujte.
1. Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka POP**.
1. V pozici **Hlavní** nové stránky přidejte fragment buy boxu.
1. Uložte stránku a zobrazte náhled. Do adresy URL stránky náhledu přidejte parametr řetězce dotazu **?productid=&lt;id produktu&gt;**. Tímto způsobem se pro načtení a vykreslení stránky náhledu použije kontext produktu.
1. Vraťte stránku se změnami a publikujte ji. Na stránce s podrobnostmi o produktu by se měl zobrazit buy box.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
