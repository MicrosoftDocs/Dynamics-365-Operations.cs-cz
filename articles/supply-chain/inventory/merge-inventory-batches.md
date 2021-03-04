---
title: Sloučit dávky skladových zásob
description: Tento článek obsahuje informace o způsobu sloučení dvou nebo více skladových dávek na sloučenou dávku.
author: pjacobse
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa571fb7392f6f7154f7f1bfd908e11e1bebd3a6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423983"
---
# <a name="merge-inventory-batches"></a>Sloučit dávky skladových zásob

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o způsobu sloučení dvou nebo více skladových dávek na sloučenou dávku.

Při slučování dávek mohou výpočty pomoci optimalizovat charakteristiku a atributy dávky ve sloučené dávce. Po výběru zdrojových dávek lze sloučenou dávku zkontrolovat a před zaúčtováním změnit. Sloučení dávky také můžete přenést do skladového deníku ke schválení. Zásoby lze poté rezervovat nebo zaúčtovat přímo ze skladového deníku. Při zaúčtování sloučené dávky jsou zásoby upraveny pro zdrojové dávky a pro sloučenou dávku.

## <a name="are-there-any-prerequisites"></a>Jsou nějaké požadavky?
Ano, jsou některé záležitosti, které je nutné nastavit před použitím nástrojů sloučení dávky. Následující tabulka obsahuje popis předpokladů.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Stránka</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Názvy deníků, Sklad</td>
<td>Je nutné vytvořit název deníku typu kusovníku, který bude použit jako výchozí při zaúčtování sloučení dávek v denících zásob. Volitelně, přestože se doporučuje, můžete určit automatické rezervace, které se provedou při převodu sloučení dávek do deníku zásob. V ostatních případech je nebezpečí, že změna je provedená na straně zásob poté, co jsou nastaveny podrobnosti sloučení dávek a deník je zaúčtován. Chcete-li povolit automatické rezervace pro název deníku, vyberte hodnotu <strong>Automaticky</strong> v poli <strong><strong>Rezervace</strong></strong>.</td>
</tr>
<tr class="even">
<td>Parametry modulu Řízení zásob a skladu</td>
<td>Je nutné specifikovat výchozí název deníku pro skladový deník.</td>
</tr>
<tr class="odd">
<td>Uvolněné produkty</td>
<td>Uvádíme doporučená nastavení pro položku:
<ul>
<li>Pokud chcete automaticky vygenerovat čísla dávky pro sloučené dávky, je nutné přiřadit uvolněný produkt ke skupině čísel dávek. Číslo dávky lze také zadat ručně při vytváření sloučené dávky, nebo vybrat číslo existující dávky. Pokud vyberete číslo existující dávky, ujistěte se, že vybraná dávka není zahrnuta v žádných skladových transakcích.</li>
<li>Pokud použijete skladovatelnost a spotřebu před datem pro uvolněný produkt, data pro sloučenou dávku budou vypočtena na základě výběru v poli <strong>Výpočet data sloučení dávky</strong>. Existují tyto možnosti:
<ul>
<li><strong>Nejdřívější</strong>: Výpočet je založen na nejdřívějším datu, které je určeno pro zdrojovou dávku, která je vybrána pro sloučení dávky.</li>
<li><strong>Nejnovější</strong>: Výpočet je založen na nejnovějším datu, které je určeno pro zdrojovou dávku, která je vybrána pro sloučení dávky.</li>
<li><strong>Ručně</strong>: Nebyla provedena žádná kalkulace. Pokud je datum stejné u všech zdrojových dávek, bude navrženo datum. Toto datum lze změnit. Neshoduje-li se datum s datem zdrojových dávek, lze jej ručně zadat.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Skupina čísel dávek</td>
<td>Volitelně: Pokud chcete vygenerovat čísla dávky při vytvoření sloučené dávky, je nutné přiřadit skupinu čísel dávek k uvolněnému produktu. Číslo dávky v opačném případě lze zadat ručně.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Kdy chci sloučit dávky zásob?
Následující příklady situací, kdy je užitečné slučování dávek:

-   Sammy prochází svým skladem a zjistí, že několik dávek stejné položky má nízké množství. Očekává příjem několika nových dodávek a uvědomí si, že může uvolnit nějaké místo na zemi sloučením zbývajícího množství do nové dávky.
-   Sammy přijímá zásoby a chce sloučit nové dávky s jednou, kterou již přijal, aby tak zlepšil hodnotu atributu dávky existující dávky. Tímto způsobem vytvoříte novou dávku.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Mohu sloučit dávky mezi pracovišti a právnickými osobami?
Ne, můžete pouze sloučit dávky stejného pracoviště a dimenze úložiště skladu v jedné právnické osobě. Můžete však zadat různá umístění a ID palety pro sloučenou dávku.

## <a name="can-i-merge-partial-quantities"></a>Je možné sloučit částečné množství?
Ne, sloučit lze pouze celé množství dávky. Funkce pro dávkové sloučení je určena jako funkce pro zásoby, nikoliv jako funkce pro výrobu.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Co když mají dávky odlišné hodnoty atributů dávky?
Vyberete-li zdrojové dávky ke sloučení ve sloučené dávce, aplikace Supply Chain Management ověří, zda mají všechny dávky vlastnosti nebo hodnoty atributů. Pokud hodnota atributu je stejná, bude navržena hodnota pro sloučenou dávku. Tuto hodnotu lze změnit. Hodnoty atributů, které se neshodují, jsou ponechány prázdné pro sloučenou dávku a lze tyto hodnoty zadat ručně. Pokud je typ atributu dávky pro hodnotu atributu celé číslo nebo zlomek a hodnoty nejsou shodné pro všechny zdrojové dávky, hodnota se vypočítá s použitím výpočtu váženého průměru. Vypočtená hodnota je zaokrouhlena nahoru nebo dolů na nejbližší přírůstek. Je-li tato hodnota je prázdná pro zdrojovou dávku, dávka a její množství nejsou zahrnuty do výpočtu. **Příklad** Následující příklad znázorňuje výpočet váženého průměru pro sloučenou dávku. Dvě zdrojové dávky mají prázdné hodnoty pro typ atributů dávky, který je celé číslo. Následující atributy jsou přiřazeny zdrojovým dávkám.

| Atribut | Minimum | Přírůstek | Maximum |
|-----------|---------|-----------|---------|
| Třída     | 3       | 3         | 30      |

Zdrojové dávky mají následující hodnoty atributů pro atribut **Dávka třídy**.

| Dávka | Množství | Atribut | Hodnota atributu |
|-------|----------|-----------|-----------------|
| B1    | 10       | Třída     | Prázdné           |
| B2    | 15       | Třída     | 15              |
| B3    | 20       | Třída     | 20              |
| B4    | 25       | Třída     | Prázdné           |
| B5    | 30       | Třída     | 25              |

Přidáte-li tyto dávky jako zdrojové dávky, sloučená dávka je přiřazena následujícím hodnotám.

| Dávka | Množství | Atribut | Hodnota atributu |
|-------|----------|-----------|-----------------|
| B6    | 100      | Třída     | 21              |

Hodnoty a množství pro dávky B1 a B4 nejsou zahrnuty ve výpočtu váženého průměru. Proto se hodnoty pro sloučenou dávku vypočítávají následujícím způsobem.

| Hodnota | Množství (hmotnost)                              | Relativní hmotnost | Relativní hmotnost x Hodnota                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0,230769231     | 3,461538462                                                           |
| 20    | 20                                             | 0,307692308     | 6,153846154                                                           |
| 25    | 30                                             | 0,461538462     | 11,53846154                                                           |
|       | **Celkem:** 65, tj. celkový počet hmotnosti |                 | **Celkem:** 21,5384615, zaokrouhleno na 21, což je nejbližší přírůstek. |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Co když mají dávky odlišná data dávky?
Pokud mají dávky jiná data dávky, některá data se vypočítají na základě hodnot ve skupině **Data dávky** na pevné záložce **Sloučené dávky** na stránce **Sloučení dávky**. Systém vypočítá hodnoty polí ve skupině **Data dávky**. Mezi tyto hodnoty patří datum výroby, datum vypršení platnosti, datum doporučené doby skladování a datum doporučené spotřeby. Data se vypočítají na základě nastavení pro položky ve skupině polí **Data položky** na stránce **Podrobnosti o uvolněném produktu**. V případě potřeby můžete změnit hodnoty nebo je vkládat ručně. Pro další data nebyl proveden žádný výpočet. Stejný princip se používá pro hodnoty atributů dávky. Je-li datum je stejné pro všechny dávky zdroje, toto datum bude navrženo pro sloučenou dávku. Pokud datum není stejné pro všechny zdrojové dávky, je datum sloučené dávky prázdné a můžete jej zadat ručně.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Jak postupovat v případě, že se dimenze liší v dávkách, které chci sloučit?
Dimenze produktu, sledovací dimenze a dimenze uskladnění jsou zpracovávány následujícím způsobem:

-   **Dimenze produktu**: Všechny dimenze produktu pro vybranou položku musí být stejné. Nelze sloučit dávky napříč dimenzemi produktu.
-   **Sledovací dimenze**: Nové číslo dávky je generováno automaticky, pokud je pro položku zadána skupina čísel dávek. Pokud skupina čísel dávek není přiřazena k položce, můžete vybrat existující dávku nebo toto číslo zadejte ručně. Sériová čísla jsou převedena ze zdrojové dávky do řádků skladového deníku pro sloučenou dávku.
-   **Dimenze úložiště**: Dimenze úložiště pracoviště a skladu musí být shodné pro všechny zdrojové dávky a pro sloučenou dávku. Můžete však zadat nová umístění a ID palety pro sloučenou dávku.

## <a name="how-does-posting-work"></a>Jak funguje zaúčtování?
Zaúčtování funguje dvěma způsoby v závislosti na tom, zda používáte proces schvalování deníků. Lze použít akce **Převod do deníku** a **Zaúčtovat sloučení dávky** pro přesun sloučených dávek do deníku, kde je lze ověřit a zaúčtovat, nebo lze sloučení dávky přímo zaúčtovat. Zásadní rozdíl mezi dvěma akcemi je, že převod do deníku nezaúčtuje sloučení dávky. Obě akce vytvoří novou dávku, pokud není vybrána existující dávka, aktualizuje všechny podrobnosti o dávkách a hodnotách atributu a vytvoří deník zásob.

-   **Převod do deníku**: Přenese podrobnosti o sloučení dávky do nového deníku zásob. Pokud jste nastavili automatické rezervace, jsou rezervována množství ve zdrojových dávkách. Podrobné informace o sloučení dávky nelze změnit. Pokud musíte upravit sloučení dávky, je nutné odstranit deník. Deník lze použít jako úkol, který jiný zaměstnanec provede později. Rezervace množství dávky na řádku deníku je zabezpečena. Toto přidělení umožňuje plánovači kvality nebo manažerovi skladu vytvoření úkolů pro jeho zaměstnance.
-   **Zaúčtovat sloučení dávky**: Zaúčtuje sloučení dávky přímo. Tuto akci můžete provést až po fyzickém slučování.

Můžete schválit deník zásob pro sloučení dávky ze stránky se seznamem **Všechna sloučení dávek**. Klikněte na **Deník** &gt; **Zaúčtovat**. Podrobnosti ve sloučené dávce nelze změnit po zaúčtování deníku. Po přenesení sloučení dávky do deníku zásob můžete změnit údaje pouze v případě, že dojde k odstranění deníku.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Poté, co byly sloučeny položky se skutečnou hmotností, proč nejsou zobrazeny údaje o skutečné hmotnosti v deníku zásob?
Lze sloučit dávky položek se skutečnou hmotností stejně jako všech ostatních položek. Údaje o skutečné hmotnosti však nejsou zobrazeny v deníku zásob. Doporučujeme ověřit údaje o skutečné hmotnosti před přenesením sloučení dávky do deníku zásob.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]