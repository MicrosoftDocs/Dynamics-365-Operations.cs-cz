---
title: Alternativní dodání
description: Zájemci o prodejní objednávky mohou využívat stránku Alternativy doručení k zjišťování alternativních možností plnění objednávky.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 1fbf8f08322c954a482777abcf041ff0b9d8fb77
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555855"
---
# <a name="delivery-alternatives"></a>Alternativní dodání

[!include [banner](../includes/banner.md)]

Zájemci o prodejní objednávky mohou využívat stránku **Alternativy doručení** k zjišťování alternativních možností plnění objednávky.

Rozložení stránky **Alternativy doručení** poskytuje lepší přehled o všech alternativních možnostech. Umožňuje také zájemcům o objednávky nahlédnout na stávající společnost z hlediska příležitostí plnění. Mají možnost zobrazit mezipodnikové příležitosti a příležitosti od externích dodavatelů. Díky třídění možností podle data dodání mohou zájemci o prodejní objednávky zobrazit inteligentní seznam alternativ doručení. Kromě toho jim parametry pomohou lépe řídit navrhované dodávky. Vzhledem k tomu, že doba přepravy může ovlivnit data dodání, mohou zájemci o prodejní objednávku prozkoumat různé možnosti, které dopravci nabízejí. Vzhledem k tomu, že pro každý návrh se zobrazí podrobné informace, mohou pořizovatelé objednávky činit informovaná rozhodování přímo ze stránky **Alternativní dodání**.

## <a name="open-the-delivery-alternatives-page"></a>Otevření stránky alternativní dodání
Stránku **Alternativní doručení** můžete otevřít z řádku prodejní objednávky.

1.  Klikněte na **Produkty a dodávka** &gt; **Alternativní dodání**.
2.  Klekněte na **Podrobnosti řádku** &gt; **Doručení** &gt; **Alternativní doručení.**

Můžete také otevřít stránku **Alternativní doručení** tak, že otevřete pracovní prostor **Zpracování prodejní objednávky a dotaz** a potom kliknete na **Objednávky a oblíbené položky** &gt; **Řádky zpožděné objednávky** &gt; **Alternativy doručení** **Poznámka:** Stránku **Alternativní doručení** můžete otevřít pouze v případě, že jsou splněny následující podmínky:

-   Jsou vyplněny všechny povinné informace o řádku prodeje.
-   Pole **Řízení data dodání** je nastaveno na jinou hodnotu než **Žádná**.

## <a name="delivery-date-control-methods"></a>Metody řízení data dodání
Metoda řízení data dodání určuje, jak systém stanovuje data dodání, jak se vypočítávají alternativy dodání a jaké informace se zobrazují. Data dodání berou v úvahu kalendáře. Proto následující kalendáře mohou ovlivnit navrhované datum příjmu: kalendář skladu, kalendář dopravy, kalendář dodavatele a kalendář odběratele. V následující tabulce jsou popsány všechny metody řízení data dodání.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Metoda</strong></td>
<td><strong>Popis</strong></td>
</tr>
<tr class="even">
<td><strong>Neomezeno</strong></td>
<td><ul>
<li>Alternativní doručení pro řádky prodeje nejsou podporovány. Tato možnost vypne řízení data dodání.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Doba realizace prodeje</strong></td>
<td><ul>
<li>Alternativní dodání se vypočítá podle předdefinované doby realizace prodeje. Dopravní dny se vypočítávají podle způsobu dodání.</li>
<li>Alternativní dodání zahrnuje sklady, které obsahuje zásoby na skladě a objednávek nabídky a poptávky.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Alternativní doručení se vypočítává na základě logiky Lze slíbit (ATP). Bere se v úvahu aktuální dostupnost a očekávaná budoucí dostupnost. Dopravní dny se vypočítávají podle způsobu dodání.</li>
<li>Alternativní dodání zahrnuje sklady, které obsahuje zásoby na skladě a objednávek nabídky a poptávky.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + rezerva výdeje</strong></td>
<td><ul>
<li>Alternativní dodání se počítá jako pro metodu ATP, ale rezerva výdeje je zahrnuta ve výpočtu.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>Alternativní doručení se vypočítává na základě logiky příslib na základě ověření dostupné kapacity (CTP). Rozpad MRP slouží k určení dostupnosti. Všimněte si, že alespoň CTP vyrovnává data dodání s prodejní dobou realizace. Dopravní dny se vypočítávají podle způsobu dodání.</li>
<li>Alternativy dodání zahrnují návrhy pro tyto sklady:
<ul>
<li>Aktuální sklad</li>
<li>Výchozí sklad</li>
<li>Všechny sklady, které mají k dispozici množství na skladě</li>
<li>Všechny sklady, které mají objednávky dodávky</li>
<li>Všechny sklady, které mají aktivní verze kusovníku (BOM)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Zobrazení informací o alternativním dodání
Tento oddíl popisuje informace o alternativách dodání, které jsou k dispozici na všech kartách stránky **Alternativní dodání**.

### <a name="products"></a>Produkty

Na této kartě se zobrazuje souhrn produktu a podrobnosti o stávajícím řádku prodeje.

### <a name="delivery-alternatives"></a>Alternativní dodání

Tato karta zobrazí seznam alternativních dodání seřazených podle data příjmu. Nad seznamem můžete vybrat možnosti, na kterých budou založeny návrhy. Můžete také vybrat způsob dodání, který určuje dopravní dny. Existují tyto možnosti:

-   **Zahrnout ostatní varianty produktu** – tato možnost je k dispozici pro produkty, které mají varianty produktu. Bude zahrnovat alternativní dodání pro ostatní varianty produktu. Tato možnost není k dispozici pro CTP.
-   **Zahrnout částečné množství** – ve výchozím nastavení jsou zde pouze návrhy, které vyhovují plnému množství na řádku prodeje. Výběrem této možnosti zahrnete návrhy, které splňují pouze částečně řádku objednávky. Tato možnost je užitečná, když odběratel požaduje dřívější datum dodání a akceptuje částečné dodávky.
-   **Zahrnout pozdější data** – ve výchozím nastavení pouze návrhy, které jsou lepší (dřívější) než jsou zobrazená aktuální data na řádku prodeje. Tuto možnost vyberte, chcete-li zahrnout pozdější data. Tato možnost může být užitečná v situacích, kdy mají prioritu jiné parametry než datum. Může být například upřednostňovaný konkrétní dodavatel nebo sklad.
-   **Způsob dodání** - vyberte preferovaný způsob dodání pro optimalizaci dopravního času a nákladů. Ihned uvidíte vliv na alternativní navrhované dodání. Je tedy snadné porovnat alternativy.
-   **Zahrnout zásobování** – Když je vybráno zásobování, mezi navrhované alternativy dodání patří možnosti nákupu od externích dodavatelů a jiných společností v organizaci (mezipodniková). Volba **Zahrnout zásobování** je podporovaná pro ATP a ATP + řízení data dodání marže. Jsou zahrnuty možnosti zásobování od výchozího nákupního dodavatele produktu a všech schválených dodavatelů pro produkt.
-   Pro externí dodavatele platí, že výpočet vychází z doby realizace nákupu.
-   Pro mezipodnikové výpočty se bere v úvahu to, co je k dispozici ze zdrojové společnosti, na základě řízení data dodání ve zdrojové společnosti.
-   **Typ dodávky** (platí pro zásobování)
    -   **Sklad** - produkty se odesílají ze zdrojového skladu pro pracoviště nebo skladu na řádku prodeje. Následně jsou odeslány z tohoto skladu odběrateli.
    -   **Přímá dodávka** - produkty se odesílají přímo ze zdrojového skladu odběrateli.

### <a name="availability-information"></a>Informace o dostupnosti

Informace na této kartě souvisí s vybranou alternativní řádkou dodávky. Zobrazují se následující informace v závislosti na řízení data dodání pro řádku prodeje:

-   **Doba realizace prodeje**
    -   **K dispozici dnes** - zobrazuje aktuální fyzické množství, fyzicky rezervované a dostupné fyzické zásoby.
    -   **Parametry** - zobrazuje skladovou jednotku a dobu realizace prodejů.

-   **ATP a ATP + rezerva výdeje**
    -   **K dispozici dnes** - zobrazuje aktuální fyzické množství, fyzicky rezervované a dostupné fyzické zásoby.
    -   **Parametry** - zobrazuje skladovou jednotku a dobu realizace prodejů.
    -   **Budoucí dostupnost** - zobrazuje grafické znázornění aktuální a budoucí dostupnosti vybraného pracoviště a skladu pod možností **alternativní dodání**. Po kliknutí na sloupce grafu se zobrazí podrobnější informace o budoucí dostupnosti produktu. Posuvník ukazuje seznam relevantních požadavků a objednávek dodávky v rámci ochranné doby ATP.

-   **CTP**
    -   **K dispozici dnes** - zobrazuje aktuální fyzické množství, fyzicky rezervované a dostupné fyzické zásoby.
    -   **Parametry** - zobrazuje skladovou jednotku a dobu realizace prodejů.
    -   **Rozpad** - zobrazuje alternativní rozpad dodávky vybrané dodávky. Můžete vybrat **nastavení** pro změnu polí a dimenzí skladů, které se zobrazují v rozbalení.

### <a name="impact-of-selected-alternative"></a>Dopad vybrané alternativy

Tato karta se podrobněji věnuje dopadu alternativy vybrané dodávky. Pokud klepnete na tlačítko **OK**, řádek prodeje se aktualizuje zvýrazněnými hodnotami ve VYBRANÝCH sloupcích. Všimněte si, že pokud je množství v alternativě pro vybranou dodávku menší než množství na řádku prodeje, vytvoření plánu dodávek a řádku objednávky je rozděleno do dvou řádků: jeden řádek pro vybrané množství a jeden řádek pro zbývající množství. Můžete také aktualizovat obchodních řádek tak, aby odpovídal řádkům plánu a ovlivňoval tvorbu cen.

<a name="additional-resources"></a>Další zdroje
--------

[Příslib objednávky](delivery-dates-available-promise-calculations.md)




