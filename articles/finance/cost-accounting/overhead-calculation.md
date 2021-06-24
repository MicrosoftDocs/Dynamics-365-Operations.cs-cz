---
title: Výpočet režijních nákladů
description: Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187990"
---
# <a name="overhead-calculation"></a>Výpočet režijních nákladů

[!include [banner](../includes/banner.md)]

Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.

## <a name="term-definition"></a>Definice termínu

Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě. Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk. Následuje několik příkladů režijních nákladů:

-   Renta
-   Elektrické energie
-   Administrativní mzdy

## <a name="overhead-calculation-overview"></a>Přehled výpočtu režijních nákladů
Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí. Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb. Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích. Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování. Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu. ID jedinečné verze se skládá z následujících prvků:

-   Typ verze
-   Datum a čas
-   Hlavní kniha nákladového účetnictví
-   Fiskální rok
-   Fiskální období

Výpočet režijních nákladů se spustí bez ohledu na verzi. Proto lze vypočítat rozpočtovou verzi před skutečnou verzí. Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku. V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku. Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu. Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup. Máte tedy vždy plnou sledovatelnost. 

[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Výpočet a přidělení režijních nákladů za elektřinu
Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální. Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici. V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace. Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení. V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.

<table>
<thead>
<tr>
<th>Datum účtování</th>
<th colspan="2">Nákladové středisko</th>
<th colspan="2">Hlavní účet</th>
<th>Částka v zúčtovací měně</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. ledna 2017</td>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Krok 1: Zpracování výpočtu chování nákladů

Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**. Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.

#### <a name="define-the-cost-behavior-rule"></a>Definice pravidel chování nákladů

V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě. Účty za elektřinu často odpovídají této definici. Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh). Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:

-   Pevná částka 1 000,00
    -   0 &lt;= 1 000,00 = Pevná
    -   1 000,01 &lt; N = Variabilní

##### <a name="journal"></a>Deník

<table>
<thead>
<tr>
<th>Deník</th>
<th>Typ deníku</th>
<th colspan="3">Fiskální kalendářní období</th>
<th>Verze</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Deník výpočtu chování nákladů</td>
<td>Fiskální</td>
<td>2017</td>
<td>Období 1</td>
<td>Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Položky deníku (Položky deníku pro zůstatek objektu nákladů)

<table>
<thead>
<tr>
<th>Datum účtování</th>
<th colspan="2">Objekt nákladů</th>
<th colspan="2">Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Částka</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. ledna 2017</td>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Neklasifikované</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Položky nákladů

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th colspan="2">Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Částka</th>
<th>Datum účtování</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Neklasifikované</td>
<td>10,000.00</td>
<td>3. ledna 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Neklasifikované</td>
<td>-10 000,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>1 000,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>9,000.00</td>
<td>31. ledna 2017</td>
</tr>
</tbody>
</table>

Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)
### <a name="step-2-process-the-cost-distribution-calculation"></a>Krok 2: Zpracování výpočtu distribuce nákladů

Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení. Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.

#### <a name="define-the-cost-distribution-rule"></a>Definice pravidel distribuce nákladů

Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální. V nákladovém účetnictví není tento přístup dostatečně podrobný. Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě. Nejlogičtější základ přidělení je spotřeba elektřiny (kWh). Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba. Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>kWh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1 000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>0</td>
</tr>
</tbody>
</table>

Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Hodnota</th>
<th>Koeficient přidělení</th>
<th>Částka</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1 000</td>
<td>(1 000 ÷ 7 000) × 9 000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>6,000</td>
<td>(6 000 ÷ 7 000) × 9 000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>0</td>
<td>(0 ÷ 7 000) × 9 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu. Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Vzorec</th>
<th>Hodnota</th>
<th>Koeficient přidělení</th>
<th>Částka</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>(1 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>(6 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Deník

<table>
<thead>
<tr>
<th>Deník</th>
<th>Typ deníku</th>
<th colspan="3">Fiskální kalendářní období</th>
<th>Verze</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Deník výpočtu distribuce nákladů</td>
<td>Fiskální</td>
<td>2017</td>
<td>Období 1</td>
<td>Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Položky deníku (Položky deníku pro zůstatek objektu nákladů)

<table>
<thead>
<tr>
<th>Datum účtování</th>
<th colspan="2">Objekt nákladů</th>
<th colspan="2">Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Částka</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. ledna 2017</td>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>1 000,00</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Položky nákladů

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th colspan="2">Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Částka</th>
<th>Datum účtování</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>-1 000,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>500.00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>500.00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Výchozí nákladové středisko</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>-9 000,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>1,285.71</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>7,714.29</td>
<td>31. ledna 2017</td>
</tr>
</tbody>
</table>

Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) 

### <a name="step-3-process-the-overhead-rate-calculation"></a>Krok 3: Zpracování výpočtu režijních nákladů

Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů. Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení. 

#### <a name="define-the-overhead-rate"></a>Definice sazby režijních nákladů

Objekt nákladů CC001 HR přispívá k sadě interních projektů. Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Pracovní doba</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekt 1</td>
<td>3</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekt 2</td>
<td>1</td>
</tr>
</tbody>
</table>

Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Jednotky</th>
<th>Kurz</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Variabilní náklady</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Hodnota</th>
<th>Prvek nákladů</th>
<th>Koeficient přidělení</th>
<th>Částka</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekt 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30.00</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekt 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Deník

<table>
<thead>
<tr>
<th>Deník</th>
<th>Typ deníku</th>
<th colspan="3">Fiskální kalendářní období</th>
<th>Verze</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Deník výpočtu režijních nákladů</td>
<td>Fiskální</td>
<td>2017</td>
<td>Období 1</td>
<td>Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Položky deníku (položky deníku pro výpočet sazby režijních nákladů)

<table>
<thead>
<tr>
<th>Datum účtování</th>
<th colspan="2">Objekt nákladů</th>
<th>Hodnota</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. ledna 2017</td>
<td>Proj 1</td>
<td>Interní projekt 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>Proj 2</td>
<td>Interní projekt 2</td>
<td>1.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Položky nákladů

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th colspan="2">Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Částka</th>
<th>Datum účtování</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>-30,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Proj 1</td>
<td>Interní projekt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>30.00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>-10,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Interní projekt 2</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>10.00</td>
<td>31. ledna 2017</td>
</tr>
</tbody>
</table>

Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).

### <a name="step-4-process-the-cost-allocation-calculation"></a>Krok 4: Zpracování výpočtu přidělení nákladů

Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení. Aplikace Finance podporuje reciproční metodu přidělování. V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů. Systém automaticky určí provádění přidělení ve správném pořadí. Zůstatek objektu nákladů je přidělen jedním základem přidělení. Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů. Pořadí přidělení je řízeno jednotkou řízení nákladů. 

[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Definice přidělení nákladů

Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů. Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů. Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Služby HR</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>10</td>
</tr>
</tbody>
</table>

Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů. Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Finanční služby</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>35</td>
</tr>
</tbody>
</table>

Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů. Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Služby sestavení (v hodinách)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů. Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Služby balení (v hodinách)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje. Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template). V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Hodnota</th>
<th>Koeficient přidělení</th>
<th>Částka</th>
<th>Chování nákladů</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>35</td>
<td>(35 ÷ 100) × 1 245,71</td>
<td>436.00</td>
<td>Variabilní náklady</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>55</td>
<td>(55 ÷ 100) × 1 245,71</td>
<td>685.14</td>
<td>Variabilní náklady</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>10</td>
<td>(10 ÷ 100) × 1 245,71</td>
<td>124.57</td>
<td>Variabilní náklady</td>
</tr>
</tbody>
</table>

V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Hodnota</th>
<th>Koeficient přidělení</th>
<th>Částka</th>
<th>Chování nákladů</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>65</td>
<td>(65 ÷ 100) × (7 714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Variabilní náklady</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>35</td>
<td>(35 ÷ 100) × (7 714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Variabilní náklady</td>
</tr>
</tbody>
</table>

V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Hodnota</th>
<th>Koeficient přidělení</th>
<th>Částka</th>
<th>Chování nákladů</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5 297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Variabilní náklady</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5 297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Variabilní náklady</td>
</tr>
</tbody>
</table>

V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th>Hodnota</th>
<th>Koeficient přidělení</th>
<th>Částka</th>
<th>Chování nákladů</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Pevné náklady</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2 852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Variabilní náklady</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2 852,60 + 124,57)</td>
<td>470.08</td>
<td>Variabilní náklady</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Položky deníku (položky deníku pro zůstatek objektu nákladů)

<table>
<thead>
<tr>
<th>Deník</th>
<th>Typ deníku</th>
<th colspan="3">Fiskální kalendářní období</th>
<th>Verze</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Deník přidělení nákladů</td>
<td>Fiskální</td>
<td>2017</td>
<td>Období 1</td>
<td>Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Řádky deníku

<table>
<thead>
<tr>
<th>Datum účtování</th>
<th colspan="2">Objekt nákladů</th>
<th colspan="2">Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Částka</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. ledna 2017</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>500.00</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>675.00</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>713.75</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC003</td>
<td>Balení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>286.25</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>CC003</td>
<td>Balení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>776.36</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>Prod 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>223.64</td>
</tr>
<tr>
<td>31. ledna 2017</td>
<td>Prod 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Položky nákladů

<table>
<thead>
<tr>
<th colspan="2">Objekt nákladů</th>
<th colspan="2">Prvek nákladů</th>
<th>Chování nákladů</th>
<th>Částka</th>
<th>Datum účtování</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>-500,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>175.00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>275.00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>50,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>-1 245,71</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>436.00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>685.14</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>124.57</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>-675,00</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>438.75</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>236.25</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finance</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>-8 150,29</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>5,297.69</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Balení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>2,852.60</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>-713,75</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>535.31</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>178.44</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>-5 982,83</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>4,487.12</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>1,495.71</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>-286,25</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>241.05</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Pevné náklady</td>
<td>45.20</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Sestavení</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>-2977,17</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>2,507.09</td>
<td>31. ledna 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrické energie</td>
<td>Variabilní náklady</td>
<td>470.08</td>
<td>31. ledna 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Závěr
Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska. Účetní tak budou vědět, že tento náklad musí být přidělen. V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel. Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Prvek nákladů</th>
<th colspan="9">Objekt nákladů</th>
<th rowspan="2">Celkem</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>Proj 1</th>
<th>Proj 2</th>
<th>Prod 1</th>
<th>Prod 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Elektřina</td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30,00</strong></td>
<td style="text-align: right;"><strong>10,00</strong></td>
<td style="text-align: right;"><strong>7.770,57</strong></td>
<td style="text-align: right;"><strong>2.189,43</strong></td>
<td style="text-align: right;"><strong>10.000,00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Neklasifikované</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Pevné náklady</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1.000,00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Variabilní náklady</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30.00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9.000,00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů. Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci. Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady. Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků. Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]