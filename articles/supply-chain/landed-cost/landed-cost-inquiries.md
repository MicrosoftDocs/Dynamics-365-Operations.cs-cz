---
title: Dotazy týkající se nákladů za doručení
description: Toto téma popisuje, jak vyhledat a použít různé typy dotazů, které jsou k dispozici pro modul Náklady za doručení.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 22a2e76780adb43b053b6cf7fd08411a4a60aeac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823354"
---
# <a name="landed-cost-inquiries"></a>Dotazy týkající se nákladů za doručení

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Dotazy na řádek cesty

Dotaz **Řádky cesty** ukazuje všechny řádky cesty, které se vztahují k zásobám. Tento dotaz lze použít jako filtr, který vám pomůže najít položku, nákupní objednávku nebo jinou užitečnou informaci. Lze jej také použít k identifikaci očekávaného data dodání položky, která by mohla být na jedné nebo více cestách. Tímto způsobem vám může pomoci při správě očekávaného příjmu zásob.

Chcete-li otevřít tento dotaz, přejděte na **Náklady za doručení \> Dotazy \> Řádky cesty**.

### <a name="overview-tab"></a>Karta Přehled

Karta **Přehled** stránky dotazu **Řádky cesty** obsahuje mřížku, která zobrazuje základní informace o každém příslušném řádku cesty. Následující tabulka popisuje sloupce v mřížce.

| Sloupec | Popis |
|---|---|
| **Číslo položky** | Položka pro řádek cesty. |
| **Odkaz** | Typ objednávky (nákupní objednávka nebo převodní příkaz). |
| **Počet** | Číslo nákupní objednávky nebo převodního příkazu. |
| **Folio** | Folio, které je přiřazeno řádku cesty. |
| **Přepravní kontejner** | Přepravní kontejner, který je přiřazen řádku cesty. |
| **Cesta** | Cesta, která je přiřazena řádku cesty. |
| **Množství** | Množství položky na řádku cesty. |
| (Jiné dimenze) | Podle potřeby můžete zobrazit sloupce pro další dimenze. Mezi tyto dimenze patří číslo šarže, stav zásob a sklad. V podokně akcí výběrem příkazu **Zásoby \> Zobrazit dimenze** otevřete dialogové okno, kde můžete vybrat použité dimenze. |

### <a name="general-tab"></a>Karta Obecné

Vyberte kartu **Obecné**, chcete-li vidět více informací o řádku, který je aktuálně vybrán na kartě **Přehled**.

### <a name="dimensions-tab"></a>Karta Dimenze

Vyberte kartu **Dimenze**, chcete-li vidět hodnoty pro všechny dostupné dimenze řádku, který je aktuálně vybrán na kartě **Přehled**, a to bez ohledu na dimenze, které jste vybrali, aby se na kartě zobrazily.

## <a name="cost-estimate-inquiries"></a>Dotazy týkající se odhadu nákladů

Pokaždé, když vygenerujete odhad nákladů, odhad se přidá do stránky dotazu **Odhady nákladů**. Úplné podrobnosti o tom, jak generovat, prohlížet a pracovat s odhady nákladů (včetně odhadů na stránce dotazu), najdete v tématu [Odhad a správa nákladů za doručení](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Sledování položky

Stránku **Sledování položek** použijte k zobrazení otevřených řádků nákupních objednávek a jejich aktuálního stavu. Řádky nemusí být spojeny s cestou, aby se zde zobrazily. Pokud je však položka spojena s cestou, řádek záznamu sledování položky zobrazuje ID cesty.

Chcete-li otevřít tuto stránku, přejděte na **Náklady za doručení \> Dotazy \> Sledování \> Sledování položek**.

Protože váš systém pravděpodobně obsahuje velmi velký počet řádků nákupní objednávky, stránka **Sledování položek** zpočátku nezobrazuje žádné záznamy. Začněte tím, že pomocí polí filtru v horní části stránky definujete sadu řádků nákupní objednávky, které hledáte. Poté vyberte příkaz **Aktualizovat** v podoknu akcí a vygenerujte seznam. V libovolném poli filtru můžete použít hvězdičku (\*) jako zástupný znak. Chcete-li například vyhledat všechny řádky nákupní objednávky pro položky, které mají v názvu slovo „DVD“, nastavte pole **Typ** na **Název výrobku** a zadejte *\*DVD\** v poli **Hodnota pole**.

> [!NOTE]
> V současné době doobjednávky zahrnují pouze prodejní objednávky. Prodejní nabídky nejsou zobrazeny ani považovány za doobjednávky.

Následující tabulka popisuje sloupce v mřížce na stránce **Sledování položek**.

| Sloupcový | popis |
|---|---|
| **Cílový přístav** | Konečný cíl. |
| **Potvrzeno** | Potvrzené datum řádku nákupní objednávky. |
| **Datum dodání** | Datum dodání řádku nákupní objednávky. |
| **Cesta** | ID cesty, když je řádek spojen s cestou. |
| **Přepravní kontejner** | ID kontejneru, když je řádek připojen k přepravnímu kontejneru. |
| **Přepravní přístav** | Aktuální přístav, založený na prvním úseku ve sledovacím formuláři, kde není nastaveno žádné skutečné datum pro přepravní kontejner, který je přidružen k řádku nákupní objednávky. |
| **Aktivita** | Aktuální aktivita, založená na prvním úseku ve sledovacím formuláři, kde není nastaveno žádné skutečné datum pro přepravní kontejner, který je přidružen k řádku nákupní objednávky. |
| **Odhadované datum ukončení** | Datum, kdy se očekává přijetí cesty v cílovém skladu. |
| **Jméno** | Název dodavatele Toto jméno je vytištěné na dokumentech odesílaných dodavateli, jako jsou např. |
| **Stav cesty** | Stav dodávky, která je připojena k řádku nákupní objednávky. |
| **Číslo položky** | Číslo položky pro řádek nákupní objednávky. |
| **Externí** | Název položky dodavatele. |
| **Název produktu** | Název položky pro řádek nákupní objednávky. |
| **Množství** | Množství řádku nákupní objednávky pro řádek nákupní objednávky. |
| **Jednotka** | Měrná jednotka pro řádek nákupní objednávky. |
| **Odkaz** | Typ objednávky (nákupní objednávka nebo převodní příkaz) |
| **Odkaz na číslo** | Číslo nákupní objednávky nebo převodního příkazu. |
| **Doobjednávka** | Symbol označuje, že u položky existují doobjednávky. |
| (Jiné dimenze) | Podle potřeby můžete zobrazit sloupce pro další dimenze. Mezi tyto dimenze patří číslo šarže, stav zásob a sklad. V podokně akcí výběrem příkazu **Zobrazit dimenze** otevřete dialogové okno, kde můžete vybrat použité dimenze. |

### <a name="related-information-about-backorders"></a>Související informace o doobjednávkách

Chcete-li zobrazit více informací o doobjednávkách, vyberte kartu **Související informace** na pravé straně stránky a poté vyberte **Doobjednávky**. Chcete-li zobrazit ještě více informací o konkrétní doobjednávce, vyberte její řádek a poté vyberte odkaz **Více**.

## <a name="individual-shipping-container-tracking"></a>Sledování jednotlivého přepravního kontejneru

Dotaz **Sledování jednotlivého přepravního kontejneru** poskytuje filtr, který vám umožní najít přepravní kontejner a poté identifikovat všechny řádky cesty v tomto kontejneru.

Chcete-li otevřít tento dotaz, přejděte na **Náklady za doručení \> Dotazy \> Sledování \> Sledování jednotlivého přepravního kontejneru**.

## <a name="multiple-shipping-container-tracking"></a>Sledování více přepravních kontejnerů

Dotaz **Sledování více přepravních kontejnerů** poskytuje filtr, který vám umožní najít kolekci přepravních kontejnerů a poté identifikovat všechny řádky cesty v těchto kontejnerech.

Chcete-li otevřít tento dotaz, přejděte na **Náklady za doručení \> Dotazy \> Sledování \> Sledování více přepravních kontejnerů**.
