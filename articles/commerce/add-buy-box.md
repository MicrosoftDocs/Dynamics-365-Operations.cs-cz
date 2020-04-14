---
title: Modul buy boxu
description: Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 3417156cbf3cb20a5190e5e51b61b3423816895a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154056"
---
# <a name="buy-box-module"></a>Modul buy boxu


[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Termín *buy box* se obvykle vztahuje k oblasti stránky s podrobnostmi o produktu, která se nachází „above the fold“ a která je hostitelem nejdůležitějších informací vyžadovaných k provedení nákupu produktu. (Oblast „above the fold“ je viditelná po prvním načtení stránky, takže uživatelé nemusejí posouvat zobrazení směrem dolů, aby ji viděli.)

Modul buy boxu je speciální kontejner, který slouží k hostování všech modulů, které jsou zobrazeny v oblasti buy boxu na stránce podrobností produktu.

Adresa URL stránky s podrobnostmi o produktu obsahuje ID produktu. Všechny informace, které jsou požadovány pro vygenerování modulu buy boxu, jsou odvozeny z tohoto ID produktu. Není-li zadáno ID produktu, nebude modul buy boxu na stránce správně vykreslen. Modul buy boxu lze proto použít pouze na stránkách, které mají kontext produktu. Chcete-li použít položku na stránce, která nemá kontext produktu (například domovskou stránku nebo marketingovou stránku), je nutné provést další úpravy.

## <a name="buy-box-module-properties-and-slots"></a>Vlastnosti a pozice modulu buy boxu 

Na stránce s podrobnostmi o produktu je buy box rozdělen na dvě oblasti: oblast médií v levé části a oblast obsahu vpravo. Ve výchozím nastavení je poměr šířky sloupce oblasti médií k šířce sloupce oblast obsahu 2:1. Na mobilních zařízeních obě oblasti navrstveny, takže se jedna oblast zobrazí pod druhou oblastí. Motivy lze použít k přizpůsobení šířky sloupců a rozměru pro skládání.

Modul buy boxu vykreslí název, popis, cenu a hodnocení produktu. Dále odběratelům vybírá varianty produktu, které mají různé atributy produktu, například velikost, styl a barvu. Je-li vybrána varianta produktu, budou další vlastnosti v buy boxu (například popis a obrázky produktu) aktualizovány tak, aby odrážely informace o variantách. 

Výběr množství je k dispozici, takže zákazníci mohou určit množství položek, které mají být zakoupeny. Maximální množství, které lze koupit, lze definovat v nastavení pracoviště.
 
Z buy boxu mohou zákazníci také provádět akce, jako je přidání produktu do nákupního košíku, přidání produktu do svého seznamu přání a výběr místa výdeje. Tyto akce lze provést u produktu nebo varianty produktu. Chcete-li přidat produkt do seznamu přání, je nutné, aby byl přihlášen zákazník.

Pomocí motivů lze odebrat nebo změnit pořadí vlastností produktu a ovládacích prvků akcí pro buy box. 

## <a name="module-properties"></a>Vlastnosti modulu

- **Značka záhlaví** – Tato vlastnost definuje značku nadpisu produktu. Je-li buy box v horní části stránky, měla by být tato vlastnost nastavena na **H1**, aby vyhovovala standardům usnadnění. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduly, které lze použít v modulu buy boxu

- **Galerie médií** – Tento modul slouží k předvedení obrázků produktu na stránce s podrobnostmi o produktu. Může podporovat jeden nebo mnoho obrázků. Podporuje také obrázky miniatur. Obrázky miniatur lze uspořádat vodorovně (jako řádek pod obrázkem) nebo svisle (jako sloupec vedle obrázku). Modul galerie médií lze přidat do pozice **Média** v modulu buy boxu. V současné době podporuje pouze obrázky. 
- **Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji. Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí. Další informace o tomto modulu naleznete v tématu [Modul Volič obchodů](store-selector.md).

## <a name="buy-box-module-settings"></a>Nastavení modulu buy boxu

Moduly buy boxu mají tři nastavení, která lze konfigurovat na **Nastavení webu \> Rozšíření**:

- **Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku. Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.
- **Kontrola zásob** – Je-li nastavena hodnota **Pravda**, položka se přidá do košíku pouze poté, co se modul buy boxu ověří, že je na skladě. Tato kontrola zásob se provádí pro scénáře, když má být položka expedována, a pro scénáře, kdy má být vyzvednuta v obchodě. Je-li tato hodnota nastavena na hodnotu **Nepravda**, před přidáním položky do nákupního košíku a podání objednávky není provedena kontrola zásob.
- **Zásboník zásob** – Tato vlastnost se používá k určení čísla zásobníku pro zásoby. Údržba zásob probíhá v reálném čase a když mnoho zákazníků podá objednávku, může být obtížné zajistit přesný počet zásob. Když je provedena kontrola zásob, pokud je množství na skladu nižší než množství zásobníku, produkt je brán, jakože není na skladu. Pokud se tedy prodej rychle točí prostřednictvím několika kanálů a zásoby nejsou plně synchronizovány, existuje menší riziko, že položka, která se nenachází na skladě, je v prodeji.

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Modul buy boxu načítá informace o produktu pomocí rozhraní API Commerce Scale Unit. ID produktu ze stránky s podrobnostmi o produktu slouží k načtení všech informací.

## <a name="add-a-buy-box-module-to-a-page"></a>Přidání modulu buy boxu na stránku

Chcete-li přidat modul buy boxu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte fragment s názvem **Fragment buy boxu** a do něj přidejte modul buy boxu.
1. Do pozice **Média** modulu buy boxu přidejte modul galerie médií.
1. Do slotu **Výběr obchodu** v modulu buy boxu přidejte modul Selektor obchodu.
1. Vraťte stránku se změnami a publikujte ji.
1. Vytvořte šablonu pro stránku s podrobnostmi o produktu a pojmenujte ji **Šablona POP**.
1. Přidejte výchozí stránku.
1. V pozici **Hlavní** na výchozí stránce přidejte fragment buy boxu.
1. Uložte šablonu, dokončete úpravy a publikujte ji.
1. Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka POP**.
1. V pozici **Hlavní** nové stránky přidejte fragment buy boxu.
1. Uložte stránku a zobrazte náhled. Do adresy URL stránky náhledu přidejte parametr řetězce dotazu **?productid=&lt;id produktu&gt;**. Tímto způsobem se pro načtení a vykreslení stránky náhledu použije kontext produktu.
1. Uložte stránku, dokončete úpravy a publikujte ji. Na stránce s podrobnostmi o produktu by se měl zobrazit buy box.

## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul Volič obchodů](store-selector.md)

[Modul kontejneru](add-container-module.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
