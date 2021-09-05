---
title: Úprava buněk definice řádku
description: Toto téma popisuje informace, které jsou nutné pro každou buňku v definici řádku ve finanční sestavě, a vysvětluje, jak tyto informace zadat.
author: ShylaThompson
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80df992ce14577ba78587648f8af2c35b382a589
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344878"
---
# <a name="modify-row-definition-cells"></a>Úprava buněk definice řádku

[!include [banner](../includes/banner.md)]

Toto téma popisuje informace, které jsou nutné pro každou buňku v definici řádku ve finanční sestavě, a vysvětluje, jak tyto informace zadat.

## <a name="specify-a-row-code-in-a-row-definition"></a>Určení kódu řádku v definici řádku

V definicích řádku čísla nebo popisky v buňce **Kód řádku** identifikují každý řádek v definici řádku. Kód řádku můžete zadat, jestliže se chcete odkazovat na data ve výpočtech nebo součtech.

### <a name="row-code-requirements"></a>Požadavky na kódy řádků

Kód řádku je vyžadován pro všechny řádky. Můžete kombinovat číselné, alfanumerické a nenastavené (prázdné) kódy řádků v definici řádku. Kód řádku může být kladné číslo (menší než 100 000 000) nebo popisek, který tento řádek identifikuje. Popisný štítek musí být v souladu se těmito pravidly:

- Popisek musí začínat abecedním znakem (a až z nebo A až Z) a může být libovolnou kombinací číslic a písmen do maximálně 16 znaků.

    > [!NOTE]
    > Popisek může zahrnovat znak podtržítka (\_), ale nejsou povoleny žádné jiné speciální znaky.

- Popisek nesmí používat žádné z následujících rezervovaných slov: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO nebo RPO.

Následující příklady jsou platné kódy řádků:

- 320
- TL\_NET\_PŘÍJEM
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Změna kódu řádku v definici řádku

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2. V odpovídajícím řádku zadejte novou hodnotu do buňky ve sloupci **Kód řádku**.

### <a name="reset-numeric-row-codes"></a>Reset číselných kódů řádků

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2. V nabídce **Upravit** klikněte na tlačítko **Přečíslovat řádky**.
3. V dialogovém okně **Přečíslovat řádky** zadejte nové hodnoty pro počáteční kód řádku a přírůstek kódu řádku. Můžete obnovit číselné kódy řádků na rovnoměrně rozložené hodnoty. Návrhář sestav však přečísluje pouze kódy řádků začínající číslicemi (například 130 nebo 246). Nepřečísluje kódy řádků, které začínají písmeny (například INCOME\_93 nebo TP0693)

> [!NOTE]
> Při přečíslování kódů řádků návrhář sestav automaticky aktualizuje odkazy **TOT** and **CAL**. Pokud například řádek **TOT** odkazuje na rozmezí, které začíná kódem řádku 100, a přečíslujete řádky počínaje od 90, počáteční odkaz **TOT** se změní ze 100 na 90.

## <a name="add-a-description"></a>Přidat popis
Buňky s popisem poskytují popis finančních dat v řádku sestavy, například „Výnosy“ nebo „Čistý příjem“. Text v buňce **Popis** se zobrazí v sestavě přesně tak, jak ho zadáte do definice řádku.

> [!NOTE]
> Šířka sloupce popisu v sestavě je nastavena v definici sloupce. Pokud je text ve sloupci **Popis** v definici řádku dlouhý, ověřte šířku sloupce **DESC**. Když používáte dialogové okno **Vložit řádky z dimenzí**, hodnoty ve sloupci **Popis** jsou hodnoty segmentu nebo hodnoty dimenze z finančních dat. Řádky můžete vkládat, pokud chcete přidat popisný text, například záhlaví oddílu nebo součet pro oddíl, nebo když chcete přidat formátování, například řádek před řádkem s celkovým součtem. Pokud sestava obsahuje organizační strom, můžete zahrnout další text definovaný pro organizační jednotky v organizačním stromu. Můžete také omezit další text na konkrétní organizační jednotku.

### <a name="add-the-description-for-a-line-on-a-report"></a>Přidání popisu pro řádek v sestavě

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2. Vyberte buňku **Popis** a poté zadejte název řádku sestavy.
3. Použijte formátování.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Přidání dalšího textu z organizačního stromu do popisu

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2. Zadejte kód doplňkového textu a jakýkoli další text do příslušné buňky **Popis**.
3. Použijte formátování.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Omezení dalšího textu na konkrétní organizační jednotku

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2. Vyhledejte řádek, ve kterém má být vytvořen doplňkový text, a pak dvakrát klikněte na buňku ve sloupci **Související vzorce/řádky/jednotky**.
3. V dialogovém okně **Výběr jednotky výkaznictví** v poli **Strom výkaznictví** vyberte strom výkaznictví.
4. V poli **Vyberte jednotku výkaznictví pro omezení** rozbalte nebo sbalte strom výkaznictví a vyberte jednotku výkaznictví.

## <a name="add-a-format-code"></a>Přidání kódu formátu
Buňka **Kód formátu** nabízí výběr předem naformátovaných voleb pro obsah daného řádku. Pokud je buňka **Kód formátu** prázdná, řádek bude interpretován jako řádek podrobností finančních dat.

> [!NOTE]
> Pokud sestava obsahuje řádky s formátováním bez částky, které souvisejí s řádky s částkami, které byly potlačeny (například z důvodu nulových zůstatků), lze použít sloupec **Související vzorce/řádky/jednotky** k zabránění tisku řádků názvu a formátu.

### <a name="add-a-format-code-to-a-report-row"></a>Přidání kódu formátu k řádku sestavy

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom vyberte definici řádku ke změně.
2. Dvakrát klikněte na buňku **Kód formátu**.
3. Vyberte kód formátu ze seznamu. Následující tabulka popisuje kódy formátů a jejich akce.

    | Kód formátu                   | Interpretace kódu formátu | Akce |
    |-------------------------------|-----------------------------------|--------|
    | (Žádné)                        |                                   | Vymaže buňku **Kód formátu**. |
    | TOT                           | Celkem                             | Identifikuje řádek, který používá matematické operátory ve sloupci **Související vzorce/řádky/jednotky**. Součty obsahují jednoduché operátory, například **+** nebo **-**. |
    | CAL                           | Výpočet                       | Identifikuje řádek, který používá matematické operátory ve sloupci **Související vzorce/řádky/jednotky**. Výpočty obsahují složité operátory, například **+**, **-**, **\**_, _*/**, a příkazy **IF/THEN/ELSE**. |
    | DES                           | popis                       | Identifikuje řádek záhlaví nebo prázdný řádek v sestavě. |
    | LFT RGT CEN                   | Vlevo Na střed Vpravo                 | Zarovná text popisu řádku na stránce sestavy bez ohledu na jeho umístění v definici sloupce. |
    | CBR                           | Změna základního řádku                   | Označuje řádek, který nastavuje základní řádek pro výpočty sloupce. |
    | SLOUPEC                        | Zalomení sloupce                      | Začne nový sloupec v sestavě. |
    | STRANA                          | Konec strany                        | Začne novou stránku v sestavě. |
    | \---                          | Jednoduché podtržení                  | Vloží jednoduchou linku pod všechny sloupce částek v sestavě. |
    | ===                           | Dvojité podtržení                  | Vloží dvojitou linku pod všechny sloupce částek v sestavě. |
    | LINE1                         | Tenká čára                         | Nakreslí přes celou šířku stránky jednu tenkou čáru. |
    | LINE2                         | Tlustá čára                        | Nakreslí přes celou šířku stránky jednu tlustou čáru. |
    | LINE3                         | Tečkovaná čára                       | Nakreslí jednu tečkovanou čáru přes celou šířku stránky. |
    | LINE4                         | Tlustá čára a tenká čára          | Nakreslí přes celou šířku stránky dvojitou čáru. Horní čára je tlustá a spodní čára je tenká. |
    | LINE5                         | Tenká čára a tlustá čára          | Nakreslí přes celou šířku stránky dvojitou čáru. Horní čára je tenká a spodní čára je tlustá. |
    | BXB BXC                       | Řádek v rámečku                         | Vytvoří ohraničení kolem řádků sestavy, které začínají řádkem **BXB** a končí řádkem **BXC**. |
    | REM                           | Poznámka                            | Označuje řádek komentáře, který se nemá tisknout na sestavě. V řádku poznámek se mohou například vysvětlovat vaše metody formátování. |
    | SORT ASORT SORTDESC ASORTDESC | Seřadit                              | Umožňuje seřadit výdaje nebo výnosy, seřadit sestavy odchylek skutečnosti a rozpočtu podle největší odchylky nebo abecedně seřadit popisy řádků. |

## <a name="specify-related-formulasrowsunits"></a>Určit související vzorce/řádky/jednotky
Buňka **Související vzorce/řádky/jednotky** má více účelů. V závislosti na typu řádku může buňka **Související vzorce/řádky/jednotky** provést některou z následujících funkcí:

- definovat řádky, které chcete zahrnout do výpočtu při používání kódu formátu **TOT** nebo **CAL**;
- Propojení řádku formátování na řádek částky, aby se formátování vytisklo pouze v případě, že je vytištěna příslušná částka.
- Omezení řádku na konkrétní organizační jednotku.
- definovat základní řádek pro výpočty při použití kódu formátu **BASEROW**;
- Definujte řádky, které se mají třídit, pokud použijete některý z kódů formátů třídění.

### <a name="use-a-row-total-in-a-row-definition"></a>Použití součtu řádku v definici řádků

Pomocí vzorců součtových řádků můžete sčítat a odečítat částky v jiných řádcích. Vzorec pro vytvoření součtového řádku může zahrnovat operátory + a - pro kombinování jednotlivých kódů řádků a rozsahů. Rozsahy jsou označeny dvojtečkou (:). Vzorec může obsahovat až 1024 znaků. Zde je příklad standardního sčítacího vzorce: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Součásti vzorce součtového řádku

Při vytváření vzorce součtového řádku je nutné pomocí kódů řádků určit, které řádky chcete sečíst nebo odečíst v aktuální definici řádku, a pomocí operátorů určit, jak mají být řádky zkombinovány. Součtové řádky a řádky částek lze používat v jakékoli kombinaci.

> [!NOTE]
> Všechny součtové řádky nacházející se v daném rozsahu jsou vyloučeny. Chcete-li vytvořit celkový součet, můžete zadat rozsah řádků. V případě, že první řádek rozsahu je součtový řádek, bude zahrnut do nového součtu. Následující tabulka popisuje použití operátorů ve vzorcích součtů řádků.

| Operátor | Příklad vzorce | popis                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Přičte částku v řádku 100 k částce v řádku 330.        |
| :        | 100:330         | Sečte součty všech řádků mezi řádkem 100 a řádkem 330.    |
| -        | 100-330         | Odečte částku v řádku 100 od částky v řádku 330. |

### <a name="create-a-row-total"></a>Vytvoření součtového řádku

1. V Návrháři sestav klikněte na položku **Definice řádků** a otevřete definici řádků, kterou chcete změnit.
2. Dvakrát klikněte na buňku **Kód formátu** v definici řádku a vyberte možnost **TOT**.
3. V buňce **Související vzorce/řádky/jednotky** zadejte vzorec součtu.

### <a name="relate-a-format-row-to-an-amount-row"></a>Vztažení řádku formátu k řádku částky

Ve sloupci **Kód formátu** v definici řádku kódy formátu **DES**, **LFT**, **RGT**, **CEN**, **---** a **===** aplikují formátování na řádky bez částek. Chcete-li zabránit tisku tohoto formátování při potlačení souvisejících řádků částky (například protože řádky s částkami obsahují nulové hodnoty nebo nemají žádnou aktivitu v období), musíte spojit řádky formátu s odpovídajícími řádky částek. Tato funkce je užitečná, pokud chcete zabránit tisku záhlaví nebo formátování souvisejícího s mezisoučty, když neexistují žádné podrobnosti k tisku pro dané období.

> [!NOTE]
> Poznámka: Můžete také potlačit tisk řádků podrobných částek, pokud zrušíte zaškrtnutí políčka pro zobrazení řádků bez částek. Tato možnost se nachází na kartě **Nastavení** v definici sestavy. Ve výchozím nastavení jsou v sestavách potlačeny účty podrobností transakcí s nulovým zůstatkem nebo bez jakékoli aktivity v daném období. Zobrazit tyto účty podrobností transakcí můžete zaškrtnutím políčka **Zobrazit řádky bez částek** na kartě **Nastavení** definice sestavy.

### <a name="relate-a-format-row-to-an-amount-row"></a>Spojení řádku formátu s řádkem částky

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom vyberte definici řádku ke změně.
2. Do řádku formátování v buňce **Související vzorce/řádky/jednotky** zadejte kód řádku částky k potlačení.

    > [!NOTE]
    > Chcete-li potlačit částku na řádku, zůstatek na řádku musí být 0 (nula). Částka řádku se zůstatkem není potlačena.

3. V nabídce **Soubor** klikněte na možnost **Uložit**.

### <a name="example-of-preventing-printing-of-rows"></a>Příklad potlačení tisku řádků

V následujícím příkladu chce uživatel zabránit vytištění záhlaví a podtržení v řádku **Hotovost celkem** ve své sestavě, protože nebyla zaznamenána žádná aktivita v žádném z pokladních účtů. Proto uživatel v řádku 220 (který je podle kódu formátu **---** řádkem formátování) v buňce **Související vzorce/řádky/jednotky** zadá **250**, což je kód řádku s částkou, který chce potlačit.

[![RelatedRowsRowDefinition.](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Výběr základního řádku pro výpočet sloupce
V relačním vykazování přiřadíte jeden nebo více základních řádků v definici řádku pomocí kódu formátu **CBR** (změna základního řádku). Na základní řádek se pak odkazují výpočty v definicích sloupců. Zde jsou některé typické příklady výpočtů CBR:

- Procento celkových výnosů ve vztahu k jednotlivým položkám výnosů
- Procento celkových výdajů ve vztahu k jednotlivým položkám výdajů
- Procento hrubé marže ve vztahu k podrobným údajům pro divize nebo oddělení

V definici řádku se definuje jeden nebo více základních řádků a v definicích sloupců se pak určí vztah vůči základnímu řádku, na jehož základě se informace vykazují. Kód, který se používá ve vzorci sloupce, je **BASEROW**. Následující základní matematické operace, které se používají u funkce **BASEROW**: dělení, násobení, sčítání nebo odčítání. Operace, která se používá nejčastěji, je dělení podle funkce **BASEROW**, kde je výsledek zobrazen v procentech. Výpočty sloupců, které používají funkci **BASEROW** ve vzorci, používají definici řádku pro související kódy základních řádků. Řádky **CBR** mají následující charakteristiky:

- řádky **CBR** nejsou vytištěny v dokončené sestavě;
- kód formátu **CBR** a související kód řádku jsou umístěny nad řádkem nebo oddílem zobrazujícím související výpočty.

Typ sloupce **CALC** v definici sloupce udává, že se jedná o sloupec, pro který je v řádku **Vzorec** zadán vzorec. Tento vzorec pracuje s daty tohoto sloupce sestavy a používá klíčové slovo Baserow k založení výpočtů na kódech formátu **CBR** v řádku. V definici řádku definuje kód formátu **CBR** základní řádek pro sloupce, které vypočítávají procento základního řádku nebo násobí základním řádkem pro každý řádek v sestavě. Můžete mít více kódů formátu **CBR** v řádku formátu, například jeden pro čistý prodej, jeden pro hrubý prodej a jeden pro celkové výdaje. Obvykle kód formátu **CBR** slouží k vytvoření procentuální hodnoty pro účty, které jsou porovnány s řádkem součtu. Základní řádek se používá pro všechny výpočty, dokud není definován další základní řádek. Je nutné definovat počáteční kód formátu **CBR** a konečný kód formátu **CBR**. Pokud byste například chtěli vyjádřit výdaje jako procento čistého prodeje, můžete hodnoty v jednotlivých řádcích výdajů vydělit hodnotou v řádku čistého prodeje. V takovém případě je řádek čistého prodeje základním řádkem. Můžete vytvořit definici sloupce, který vykazuje aktuální výsledek a výsledek od začátku roku a pro každý z těchto výsledků zobrazuje také procento základní hodnoty, jak je vidět v následujícím příkladu. Začněte podrobnou výsledovkou.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Výběr základního řádku v definici řádku pro výpočet sloupce

1. V Návrháři sestav, klikněte na tlačítko **Definice sloupce** a potom otevřete definici sloupce pro výkaz zisků.
2. Přidejte nový sloupec do definice sloupce a nastavte typ sloupce na možnost **CALC**.
3. V buňce **Vzorec** nového sloupce zadejte vzorec **X/BASEROW**, kde **X** je typ sloupce **FD** pro zobrazení v procentech.
4. Dvakrát klikněte na buňku **Přepsání formátu/měny**.
5. V dialogovém okně **Přepsání formátu** v seznamu **Kategorie formátu** vyberte možnost **Procento** a klikněte na tlačítko **OK**.
6. V nabídce **Soubor** klikněte na tlačítko **Uložit jako** a uložte definici sloupce pod novým názvem. Připojte kód **CBR** k aktuálnímu názvu souboru (například **CUR\_YTD\_CBR**). Tato definice sloupce je vaše definice sloupce základního řádku.
7. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně použitím výpočtu základního řádku.
8. Vložte nový řádek nad místo, kde by měl začínat výpočet využívající základní řádek.
9. Dvakrát klikněte na buňku **Kód formátu** v definici řádku a vyberte možnost **CBR**.
10. V buňce **Související vzorce/řádky/jednotky** zadejte číslo kódu řádku pro základní řádek.

### <a name="example-of-base-row-calculation"></a>Příklad výpočtu základního řádku

V následujícím příkladu definice řádku ukazuje řádek 100, že základní řádek pro výpočty je řádek 280.

[![Příklad výpočtu základního řádku.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

V následujícím příkladu definice sloupce se použije při výpočtech formát kódu **CBR**. Výpočet ve sloupci C podělí hodnotu ve sloupci B sestavy hodnotou v řádku 280 sloupce B. Díky přepsání formátu ve sloupci B se výsledek výpočtu vytiskne jako procento. Podobně jednotlivé částky ve sloupci E jsou částky ze sloupce D jako procento čistého prodeje.

[![Příklad definice sloupce.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Následující příklad ukazuje sestavu, která může být generováno na základě předchozích výpočtů.

[![Příklad sestavy založené na výpočtech předchozích příkladů.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Výběr kódu třídění pro definici řádků
Kódy řazení slouží k seřazení účtů a hodnot, k seřazení sestavy odchylek skutečnosti a rozpočtu podle největší odchylky nebo k abecednímu seřazení popisů řádků. K dispozici jsou následující kódy řazení:

- **SORT** – seřadí sestavu vzestupně podle hodnot ve vybraném sloupci.
- **ASORT** – seřadí sestavu vzestupně podle absolutní hodnoty hodnot ve vybraném sloupci. Jinými slovy, při řazení hodnot se ignoruje znaménko jednotlivých hodnot. Tento kód formátu seřadí hodnoty podle velikosti odchylky bez ohledu na to, zda je odchylka kladná nebo záporná.
- **SORTDESC** – seřadí sestavu sestupně podle hodnot ve vybraném sloupci.
- **ASORTDESC** – seřadí sestavu sestupně podle absolutní hodnoty hodnot ve vybraném sloupci.

### <a name="select-a-sorting-code"></a>Volba kódu řazení

1. V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.
2. Dvakrát klikněte na buňku **Kód formátu** a vyberte kód třídění.
3. V buňce **Související vzorce/řádky/jednotky** stanovte rozmezí kódů řádků ke třídění. Při zadávání rozsahu zadejte kód prvního řádku, dvojtečku (:) a poté kód posledního řádku. Zadáním například hodnoty **160:490** určete rozmezí od řádku 160 po řádek 490.
4. V buňce **Omezení sloupce** zadejte písmeno sloupce sestavy k použití pro řazení.

    > [!NOTE]
    > Do výpočtu řazení zahrnujte pouze řádky částek.

### <a name="examples-of-ascending-and-descending-column-values"></a>Příklady vzestupných a sestupných hodnot sloupců

V následujícím příkladu budou hodnoty ve sloupci D sestavy seřazeny ve vzestupném pořadí řádků 160 až 490. V následujícím příkladu budou absolutní hodnoty ve sloupci G sestavy seřazeny v sestupném pořadí řádků 610 až 940.

| Kód řádku | Popis                                         | Kód formátu | Související vzorce/řádky/jednotky | Normální rozvaha | Omezení sloupce | Odkaz na finanční dimenze |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Seřazeno vzestupně podle měsíční odchylky       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Prodej                                               |             |                             | C              |                    | 4100                         |
| 190      | Prodejní vratky                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Příjem z úroků                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Seřazeno sestupně podle absolutní odchylky od začátku roku | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Prodej.                                               |             |                             | o              |                    | 4100                         |
| 640      | Prodejní vratky                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Příjem z úroků                                     |             |                             | o              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Určení buňky přepsání formátu
Buňka **Přepsání formátu** určuje formátování použité pro řádek při vytištění sestavy. Toto formátování má přednost před veškerým formátováním, které je určeno v definici sloupce a definici sestavy. Ve výchozím nastavení je formátování určené těmito definicemi měna. Pokud sestava obsahuje v jednom řádku počet aktiv, například počet budov, a v jiném řádku jejich peněžní hodnoty, můžete přepsat formátování měny a zadat pro řádek, který určuje počet budov, číselný formát. Tyto informace můžete zadat v dialogovém okně **Přepsání formátu**. To, jaké možnosti budou dostupné, bude záviset na kategorii formátu, kterou vyberete. Oblast **Ukázka** dialogového okna zobrazuje příklady formátů. Dostupné jsou následující kategorie formátů:

- Formátování měny
- Číselné formátování
- Procentuální formátování
- Vlastní formátování

### <a name="override-cell-formatting"></a>Přepsání formátování buňky

1. V Návrháři sestav otevřete definici řádků, kterou chcete změnit.
2. V řádku pro přepsání formátu dvakrát klikněte na buňku ve sloupci **Přepsání formátu**.
3. V dialogovém okně **Přepsání formátu** vyberte možnosti formátování pro použití v daném řádku v sestavě.
4. Klepněte na tlačítko **OK**.

### <a name="currency-formatting"></a>Měnové formátování

Formátování měny se použije na fiskální hodnotu a obsahuje symbol měny. K dispozici jsou tyto možnosti:

- **Symbol měny** – Symbol měny pro sestavu Tato hodnota přepíše nastavení **Možnosti místního nastavení** pro informace o společnosti.
- **Záporná čísla** – záporná čísla mohou obsahovat záporné znaménko (-), mohou se zobrazovat v závorkách nebo mají trojúhelník (∆).
- **Desetinná místa** – počet číslic, které chcete zobrazit za desetinnou čárkou.
- **Text přepsání nulové hodnoty** – text, který bude zahrnut do sestavy, pokud je částka 0 (nula). Tento text se zobrazí jako poslední řádek oblasti **Ukázka**.

    > [!NOTE]
    > Je-li tisk pro nulové hodnoty potlačen nebo nebyla žádná aktivita v období, tento text bude potlačen.

### <a name="numeric-formatting"></a>Číselné formátování

Formátování čísel platí pro všechny částky a nezahrnuje symbol měny. K dispozici jsou tyto možnosti:

- **Záporná čísla** – záporná čísla mohou obsahovat záporné znaménko (-), mohou se zobrazovat v závorkách nebo mají trojúhelník (∆).
- **Desetinná místa** – počet číslic, které chcete zobrazit za desetinnou čárkou.
- **Text přepsání nulové hodnoty** – text, který bude zahrnut do sestavy, pokud je částka 0 (nula). Tento text se zobrazí jako poslední řádek oblasti **Ukázka**.

    > [!NOTE]
    > Je-li tisk pro nulové hodnoty potlačen nebo nebyla žádná aktivita v období, tento text bude potlačen.

### <a name="percentage-formatting"></a>Procentuální formátování

Formátování jako procenta zahrnuje znak procent (%). K dispozici jsou tyto možnosti:

- **Záporná čísla** – záporná čísla mohou obsahovat záporné znaménko (-), mohou se zobrazovat v závorkách nebo mají trojúhelník (∆).
- **Desetinná místa** – počet číslic, které chcete zobrazit za desetinnou čárkou.
- **Text přepsání nulové hodnoty** – text, který bude zahrnut do sestavy, pokud je částka 0 (nula). Tento text se zobrazí jako poslední řádek oblasti **Ukázka**.

    > [!NOTE]
    > Je-li tisk pro nulové hodnoty potlačen nebo nebyla žádná aktivita v období, tento text bude potlačen.

### <a name="custom-formatting"></a>Vlastní formátování

Pomocí kategorie vlastního formátování můžete nakonfigurovat nastavení pro přepsání vlastním formátem. K dispozici jsou tyto možnosti:

- **Typ** – Vlastní formátování
- **Text přepsání nulové hodnoty** – text, který bude zahrnut do sestavy, pokud je částka 0 (nula). Tento text se zobrazí jako poslední řádek oblasti **Ukázka**.

    > [!NOTE]
    > Je-li tisk pro nulové hodnoty potlačen nebo nebyla žádná aktivita v období, tento text bude potlačen.

Typ by měl představovat jak kladnou, tak i zápornou hodnotu. Obvykle zadáte podobný formát pro rozlišování mezi kladnými a zápornými hodnotami. Pokud chcete například určit, že kladné i záporné hodnoty mají mít dvě desetinná místa, ale záporné hodnoty se zobrazí v závorkách, zadejte hodnotu **0,00;(0,00)**. V následující tabulce jsou uvedeny vlastní formáty, pomocí kterých lze určovat formát hodnot. Všechny příklady začínají z hodnoty 1234,56.

| Formát                         | Kladné   | Záporný     | Nula    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1 235      | (1 235)      | (Prázdné) |
| \#,\#\#0,00;(\#,\#\#0.00);nula | 1 234,56   | (1 234,56)   | nula    |
| 0,00 %;(0,00 %)                  | 123456,00 % | (123456,00%) | 0,00 %   |

## <a name="specify-a-normal-balance-cell"></a>Určit obvyklé saldo buňky
Buňka **Normální zůstatek** v definici řádku řídí znaménka částek v řádku. Chcete-li obrátit znaménko řádku nebo pokud je normální zůstatek účtu na straně Dal, zadejte **C** do buňky **Normální zůstatek** pro daný řádek. Aplikace Návrhář sestav obrátí znaménka na všech rozvahových účtech na straně Dal v daném řádku. Když návrhář sestav převádí tyto účty, odstraní charakteristiky Má dáti / Dal ze všech částek a tím pádem zjednoduší sčítání. Chcete-li například vypočítat čistý příjem, odečtete výdaje od příjmů. Obvykle nejsou sečtené a vypočtené řádky ovlivněny kódem **C**. Ovládací prvek tisku **XCR** v definici sloupce obrátí znaménko jakéhokoli řádku obsahujícího hodnotu **C** ve sloupci **Normální zůstatek**. Toto formátování je zvláště důležité, pokud chcete zobrazit všechny nepříznivé odchylky jako záporné částky. Pokud má sečtené nebo vypočtené číslo nesprávné znaménko, zadáním hodnoty **C** do buňky **Normální zůstatek** pro řádek obrátíte znaménko.

## <a name="specify-a-row-modifier-cell"></a>Určení modifikátoru řádku buňky
Obsah buňky **Modifikátor řádku** v definici řádku přepíše fiskální roky, období a další informace, které jsou určeny v definici sloupce pro daný řádek. Vybraný modifikátor platí pro všechny účty v tomto řádku. Každý řádek je možné upravit pomocí jednoho nebo více následujících typů modifikátorů:

- Modifikátory účtů
- Modifikátory kódů knih
- Atributy účtů a transakcí

### <a name="override-a-column-definition"></a>Přepsání definice sloupce

1. V Návrháři sestav otevřete definici řádků, kterou chcete změnit.
2. V řádku, ve kterém chcete přepsat definici sloupce, klikněte dvakrát na buňku **Modifikátor řádku**.
3. V dialogovém okně **Modifikátor řádku** vyberte jednu z možností v poli **Modifikátor účtu**. Popis možností najdete v tématu „Modifikátory účtů“.
4. V poli **Modifikátory kódu knihy** vyberte kód knihy pro použití v tomto řádku.
5. V části **Atributy** pomocí následujících kroků přidejte záznam pro každý atribut, který má být zahrnut s kódem řádku:

    1. Dvakrát klikněte na buňku **Atribut** a vyberte název atributu.

        > [!IMPORTANT]
        > Nahraďte znak (\#) číselnou hodnotou.

    2. Dvakrát klikněte na buňku **Od** a zadejte první hodnotu rozsahu.
    3. Dvakrát klikněte na buňku **Do** a zadejte poslední hodnotu rozsahu.

6. Klepněte na tlačítko **OK**.

### <a name="account-modifiers"></a>modifikátory účtů,

Vyberete-li určitý účet, návrhář sestav obvykle spojí účet a fiskální roky, období a další informace, které zadáte do definice sloupce. Pro konkrétní řádky ale můžete použít jiné informace, například jiná fiskální období. Následující tabulka ukazuje modifikátory účtů, které jsou k dispozici. Nahraďte křížek (\#) hodnotou, která je menší nebo rovna počtu období ve fiskálním roku.

| Modifikátor účtu | Co bude vytištěno                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Počáteční zůstatek účtu                                                     |
| /\#              | Zůstatek pro určené období                                                     |
| /-\#             | Zůstatek pro období, které zahrnuje \# období před aktuálním obdobím                  |
| /+\#             | Zůstatek pro období, které zahrnuje \# období po aktuálním období                   |
| /C               | Zůstatek pro aktuální období                                                       |
| /C-\#            | Zůstatek pro období, které zahrnuje \# období před aktuálním obdobím                  |
| /C+\#            | Zůstatek pro období, které zahrnuje \# období po aktuálním období                   |
| /Y               | Zůstatek od začátku roku do aktuálního období.                                      |
| /Y-\#            | Zůstatek od začátku roku do období, které zahrnuje \# období před aktuálním obdobím. |
| /Y+\#            | Zůstatek od začátku roku do období, které zahrnuje \# období po aktuálním období.  |

### <a name="book-code-modifiers"></a>modifikátory kódu knihy,

Řádek můžete omezit na existující kód knihy. Definice sloupce musí zahrnovat alespoň jeden sloupec **FD**, který má kód knihy.

> [!NOTE]
> Omezení kódu knihy pro řádek přepíše omezení kódu knihy v definici sloupce pro daný řádek.

### <a name="account-and-transaction-attributes"></a>Atributy účtů a transakcí

Některé účetní systémy podporují atributy účtů a transakcí ve finančních datech. Tyto atributy fungují podobně jako segmenty virtuální účet a mohou obsahovat další informace o vztahu nebo transakce. Tyto doplňkové informace může být účet ID, ID šarže, poštovní směrovací čísla nebo jiné atributy. Pokud váš účetní systém podporuje atributy, můžete atributy účtů nebo transakcí použít jako modifikátory řádku v definici řádku. Pokyny, jak přepsat informace řádku, naleznete v postupu „Přepsání definice sloupce“ v předchozím textu tohoto článku.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Zadání buňky Odkaz na finanční dimenze
Buňka **Odkaz na finanční dimenze** obsahuje odkazy na finanční data, která mají být zahrnuta v každém řádku sestavy. Tato buňka obsahuje hodnoty dimenze. Otevřete dialogové okno **Dimenze** kliknutím dvakrát na buňku **Odkaz na finanční dimenze**.

> [!NOTE]
> Návrhář sestav nemůže vybrat účty, dimenze nebo pole ze systému Microsoft Dynamics ERP, které obsahují kterékoli z následujících vyhrazených znaků: : & \*, \[, \], {, or }. Chcete-li zadat informace pro řádek, který již je v definici řádků, přidejte tyto informace do buňky **Odkaz na finanční dimenze**. Chcete-li přidat nové řádky, které odkazují na finanční data, použijte dialogové okno **Vložit řádky z** pro vytvoření nových řádků v definici sestavy. Název sloupce se změní podle toho, jak je nakonfigurován, jak je znázorněno v následující tabulce.

| Vybraný typ odkazu       | Popis sloupce Odkaz se změní na tento |
|----------------------------------|----------------------------------------------------|
| Finanční dimenze             | Odkaz na finanční dimenze                       |
| List sestavy                 | Sestava finančního výkaznictví                         |

### <a name="specify-a-dimension-or-range"></a>Zadání dimenze nebo rozsahu

1. V Návrháři sestav otevřete definici řádku k úpravě.
2. Dvakrát klikněte na některou buňku ve sloupci **Odkaz na finanční dimenze**.
3. V dialogovém okně **Dimenze** dvakrát klikněte na buňku pod názvem dimenze.
4. V dialogovém okně pro dimenzi vyberte položku **Jednotlivec nebo rozsah**.
5. Do pole **Od** zadejte počáteční dimenzi nebo klikněte na ![Procházet.](media/browse.gif "Procházet") pro vyhledání dostupných dimenzí. Chcete-li zadat rozsah dimenzí, zadejte koncové dimenze do pole **Do**.
6. Kliknutím na tlačítko **OK** zavřete dialogové okno pro dimenzi. Dialogové okno **Dimenze** zobrazuje aktualizovanou dimenzi nebo rozsah.
7. Kliknutím na tlačítko **OK** zavřete dialogové okno **Dimenze**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Zobrazení účtů s nulovým zůstatkem v definici řádku
Ve výchozím nastavení návrhář sestav netiskne řádky, které nemají odpovídající zůstatek ve finančních datech. Můžete proto vytvořit jednu definici řádku zahrnující všechny hodnoty přirozených segmentů nebo všechny hodnoty dimenzí a tuto definici řádku pak používat pro všechna oddělení.

### <a name="modify-zero-balance-settings"></a>Upravit nastavení nulových zůstatků

1. V Návrháři sestav otevřete definici sestavy, kterou chcete změnit.
2. Na kartě **Nastavení** v části **Další formátování** vyberte možnosti pro definici řádku, která se používá v definici sestavy.
3. Chcete-li uložit změny, klikněte v nabídce **Soubor** na tlačítko **Uložit**.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Používání zástupných znaků a rozsahů v definici řádku
Když zadáte přirozenou hodnotu segmentu do dialogového okna **Dimenze** můžete použít zástupný znak (? nebo \*) na jakékoli pozici segmentu. Aplikace Návrhář sestav extrahuje všechny hodnoty definovaných pozic bez zohlednění zástupných znaků. Například definice řádku obsahuje pouze přirozené hodnoty segmentu a přirozené segmenty mají čtyři znaky. Zadáním hodnoty **6???** na řádku dáte Návrháři sestav pokyn k zahrnutí všech účtů, které mají hodnotu přirozeného segmentu začínající 6. Pokud zadáte **6\**_, budou vráceny stejné výsledky, ale výsledky budou obsahovat také hodnoty proměnné šířky, jako je například _* 60** a **600000**. Návrhář sestav nahradí každý zástupný znak (?) úplným rozsahem možných hodnot, které zahrnují písmena a speciální znaky. Například v rozsahu od **12?0** do **12?4** bude zástupný znak v hodnotě **12?0** nahrazen nejnižší hodnotou ve znakové sadě a zástupný znak v hodnotě **12?4** bude nahrazen nejvyšší hodnotou ve znakové sadě.

> [!NOTE]
> Měli byste se vyhnout používání zástupných znaků pro počáteční a koncové účty v rozsazích. Pokud použijete zástupné znaky u počátečního nebo koncového účtu, mohly by být vráceny neočekávané výsledky.

### <a name="single-segment-or-single-dimension-ranges"></a>Rozsahy s jedním segmentem nebo jednou dimenzí

Můžete zadat rozsah hodnot segmentů nebo dimenzí. Výhodou zadání rozsahu je, že nemusíte aktualizovat definici řádku pokaždé, když je přidána nová hodnota segmentu nebo hodnota dimenze do finančních dat. Například rozsah **+Účet=\[6100:6900\]** získá hodnoty z účtů 6100 až 6900 do částky řádku. Když rozsah zahrnuje zástupný znak (?), nebude návrhář sestav hodnotit rozsah znak po znaku. Místo toho určí dolní a horní konec rozsahu a potom zahrne koncové hodnoty a veškeré hodnoty mezi nimi.

> [!NOTE]
> Návrhář sestav nemůže vybrat účty, dimenze nebo pole ze systému Microsoft Dynamics ERP, které obsahují kterékoli z následujících vyhrazených znaků: : & \*, \[, \], {, or }. Můžete přidat ampersand (&) pouze při automatickém vytváření definic řádku pomocí dialogového okna **Vložit řádky z dimenzí**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Rozsahy s více segmenty nebo dimenzemi

Při zadání rozsahu kombinací více hodnot dimenzí se provádí porovnání rozsahu na základě ..\\financial-dimensions\\dimension-by-dimension basis. Porovnání rozsahu nelze provést po znacích nebo částečných segmentech. Například rozsah **+Účet=\[5000:6000\], Oddělení=\[1000:2000\], Nákladové středisko=\[00\]** zahrnuje pouze účty, které odpovídají každému segmentu. V tomto případě první dimenze musí být v rozmezí od 5000 až 6000, druhá dimenze musí být v rozmezí 1000 až 2000 a poslední dimenze musí být 00. Například **+ účet =\[5100\], oddělení =\[1100\], nákladové středisko =\[01\]** není zahrnuto v sestavě, protože poslední segment je mimo zadaný rozsah. Pokud hodnota segmentu zahrnuje mezery, vložte ji do hranatých závorek (\[ \]). Následující hodnoty jsou platné pro čtyřmístný segment: **\[ 234\], \[123 \], \[1 34\]**. Hodnoty dimenze mají být zadávány do hranatých závorek (\[ \]) a návrhář sestav tyto závorky přidá za vás. Pokud rozsah segmentu více nebo více dimenzí obsahuje zástupné znaky (? nebo \*), bude určen horní a dolní konec celého násobného segmentu a potom budou zahrnuty koncové hodnoty a veškeré hodnoty mezi nimi. Pokud máte velký rozsah, například celý rozsah účtů od 40000 do 99999, zadejte platný počáteční účet a koncový účet, kdykoli je to možné.

> [!NOTE] 
> Návrhář sestav nemůže vybrat účty, dimenze nebo pole ze systému Microsoft Dynamics ERP, které obsahují kterékoli z následujících vyhrazených znaků: : & \*, \[, \], {, or }. Můžete přidat ampersand (&) pouze při automatickém vytváření definic řádku pomocí dialogového okna **Vložit řádky z dimenzí**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Sčítání nebo odečítání z jiných účtů v definici řádku
Chcete-li přičítat nebo odečítat peněžní částky jednoho účtu od peněžních částek jiného účtu, můžete použít znaménko plus (+) a znaménko minus (-) v buňce **Odkaz na finanční dimenze**. Následující tabulka zobrazuje přípustné formáty pro přičítání odkazů k finančním datům a pro jejich odečítání.

| Operace                                                                               | Použijte tento formát                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Součet dvou plně kvalifikovaných účtů                                                       | +Divize=\[000\], Účet=\[1205\], Oddělení=\[00\]+Divize=\[100\], Účet=\[1205\], Oddělení=\[00\] |
| Součet dvou hodnot segmentů                                                                 | +Účet=\[1205\]+Účet=\[1210\]                                                                           |
| Součet hodnot segmentů obsahujících zástupné znaky.                                    | +Účet=\[120?+Účet=\[11??\]                                                                             |
| Součet rozsahu plně kvalifikovaných účtů                                                | +Divize=\[000:100\], Účet=\[1205\], Oddělení=\[00\]                                                   |
| Součet rozsahu hodnot segmentů                                                          | +Účet=\[1200:1205\]                                                                                       |
| Součet rozsahu hodnot segmentů obsahujících zástupné znaky.                         | +Účet=\[120?:130?\]                                                                                       |
| Odečtení jednoho plně kvalifikovaného účtu od jiného plně kvalifikovaného účtu              | +Divize=\[000\], Účet=\[1205\], Oddělení=\[00\]-Divize=\[100\], Účet=\[1205\], Oddělení=\[00\] |
| Odečtení jedné hodnoty segmentu od jiné hodnoty segmentu.                                  | +Účet=\[1205\]-Účet=\[1210\]                                                                           |
| Odečtení hodnoty segmentu, která obsahuje zástupný znak, od jiné hodnoty segmentu. | +Účet=\[1200\]-Účet=\[11??\]                                                                           |
| Odečtení rozsahu plně kvalifikovaných účtů                                           | -Divize=\[000:100\], Účet=\[1200:1205\], Oddělení=\[00:01\]                                           |
| Odečtení rozsahu hodnot segmentů                                                     | -Účet=\[1200:1205\]                                                                                       |
| Odečtení rozsahu hodnot segmentů obsahujících zástupné znaky.                    | -Účet=\[120?:130?\]                                                                                       |

Ačkoli můžete upravovat účty přímo, můžete použít také dialogové okno **Dimenze** k aplikaci správného formátování na vaše odkazy na finanční údaje. Všechny hodnoty mohou obsahovat zástupné znaky (? nebo \*). Návrhář sestav však nemůže vybrat účty, dimenze nebo pole ze systému Microsoft Dynamics ERP, které obsahují kterékoli z následujících vyhrazených znaků: : & \*, \[, \], {, or }.

> [!NOTE]
> Chcete-li odečítat hodnoty, je nutné uzavřít tyto hodnoty do závorek. Zadáte-li například hodnotu **450?-(4509)**, bude zobrazena jako **+Účet==\[4509\]-Účet=\[450?\]** a říká návrháři sestav, aby odečetl částku segmentu účtu 4509 od částky jakéhokoli segmentu účtu, který má na začátku 450.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Přičítání nebo odečítání účtů od jiných účtů

1. V Návrháři sestav otevřete definici řádku k úpravě.
2. V odpovídajícím řádku klikněte dvakrát na buňku ve sloupci **Odkaz na finanční dimenze**.
3. V prvním řádku dialogového okna **Dimenze** proveďte tyto kroky:

    1. V prvním poli vyberte všechny dimenze (výchozí) nebo kliknutím otevřete dialogové okno **Správa sad dimenzí**, kde můžete vytvořit, upravit, kopírovat nebo odstranit sadu.
    2. Klikněte dvakrát na buňku **Operátor +/-** a vyberte znaménko plus (**+**) nebo mínus (**-**), které platí pro jednu nebo více hodnot nebo sad dimenzí v řádku.
    3. Ve sloupci hodnoty příslušné dimenze kliknutím dvakrát na buňku otevřete dialogové okno **Dimenze** a vyberte, zda je tato hodnota dimenze pro jednotlivce nebo rozsah, sadu hodnot dimenze nebo účty součtů. Popisy polí v dialogovém okně **Dimenze** naleznete v části „Popis dialogového okna Dimenze“.
    4. Zadejte hodnoty segmentů do sloupců **Od** a **Do**.

4. Opakováním kroků 2 až 3 přidejte další operace.

> [!NOTE]
> Operátor platí pro všechny dimenze v řádku.

## <a name="description-of-the-dimensions-dialog-box"></a>Popis dialogového okna Dimenze
Pole dialogového okna **Dimenze** jsou popsána v následující tabulce.

| Položka                | Popis |
|---------------------|-------------|
| Jednotlivě nebo jako rozsah | Do pole **Od** zadejte název účtu nebo klikněte na tlačítko **Procházet** ![Procházet](media/browse.gif "Procházet") k vyhledání účtu. K výběru rozsahu zadejte nebo vyhledejte hodnotu pro pole **Do**. |
| Sada hodnot dimenzí | Do pole **Název** zadejte název sady hodnot dimenze. Chcete-li vytvořit, upravit, kopírovat nebo odstranit sadu, klikněte na tlačítko **Správa sad hodnot dimenzí**. Pole **Vzorec** je vyplněno vzorcem z buňky **Odkaz na finanční dimenze** pro tuto sadu hodnot dimenze v definici řádku. |
| Sčítání na účtech   | V poli **Název** zadejte nebo vyhledejte dimenzi účtů součtů. Pole **Vzorec** je vyplněno vzorcem z buňky **Odkaz na finanční dimenze** pro tento účet součtů v definici řádku. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Přidání sad hodnot dimenzí do definice řádku
Sada hodnot dimenze je pojmenovaná skupina hodnot dimenze. Sada hodnot dimenze může obsahovat hodnoty v jedné dimenzi, ale můžete použít sadu hodnot dimenze ve více definicích řádku, definicích sloupce, definicích stromu výkaznictví a definicích sestav. Také můžete kombinovat sady hodnot dimenzí v definici sestavy. Pokud změna finančních dat vyžaduje, abyste změnili sadu hodnot dimenze, můžete aktualizovat definici sady hodnot dimenze. Tato aktualizace se projeví ve všech oblastech, kde se tato sada hodnot dimenze používá. Pokud například často vyznačujete rozsah hodnot, které mají odkazovat na finanční data (například hodnoty od 5100 do 5600), můžete tento rozsah přiřadit sadě účtů s názvem Prodej. Po vytvoření sady hodnot dimenze můžete tuto sadu vybrat jako odkaz na finanční data. Jiný příklad: Pokud máte rozsah hodnot 5100 až 5600 přiřazený k prodeji a hodnotu 4175 ke slevám, můžete celkový prodej určit odečtením slev od prodeje. Tato operace je označena jako **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Vytvoření sady hodnot dimenze

1. V Návrháři sestav otevřete definici řádku, sloupce nebo stromu k úpravě.
2. V nabídce **Upravit** klikněte na tlačítko **Správa sad hodnot dimenzí**.
3. V dialogovém okně **Správa sad hodnot dimenzí** v poli **Dimenze** vyberte typ sady hodnot dimenze k vytvoření a klikněte na tlačítko **Nová**.
4. V dialogovém okně **Nová** zadejte název a popis sady.
5. Ve sloupci **Od** klikněte dvakrát na buňku.
6. V dialogovém okně **Účet** vyberte v seznamu název účtu nebo vyhledejte položku v poli **Hledat**. Poté klikněte na tlačítko **OK**.
7. Opakováním kroků 5 až 6 ve sloupci **Do** navrhněte vzorec pro daný operátor.
8. Po dokončení vzorce klikněte na tlačítko **OK**.
9. V dialogovém okně **Spravovat sady dimenzí** klikněte na tlačítko **Zavřít**.

### <a name="update-a-set-of-dimension-values"></a>Aktualizace sady hodnot dimenze

1. V Návrháři sestav otevřete definici řádků, sloupců nebo stromu, kterou chcete změnit.
2. V nabídce **Upravit** klikněte na tlačítko **Správa sad hodnot dimenzí**.
3. V dialogovém okně **Správa sad hodnot dimenzí** v poli **Dimenze** vyberte typ dimenze.
4. V seznamu vyberte sadu hodnot dimenze k aktualizaci a poté klikněte na tlačítko **Upravit**.
5. V dialogovém okně **Upravit** upravte hodnoty vzorce k zahrnutí do sady.

    > [!NOTE]
    > Pokud přidáte nové účty nebo dimenze, nezapomeňte upravit existující sady hodnot dimenzí tak, aby změny zohledňovaly.

6. Klikněte dvakrát na buňku a vyberte odpovídající operátor, účet **Od** a účet **Do**.
7. Kliknutím na tlačítko **OK** zavřete dialogové okno **Upravit** a uložte změny.

### <a name="copy-a-dimension-set"></a>Kopírování sady dimenzí

1. V Návrháři sestav otevřete definici řádků, sloupců nebo stromu, kterou chcete změnit.
2. V nabídce **Upravit** klikněte na tlačítko **Správa sad hodnot dimenzí**.
3. V dialogovém okně **Správa sad hodnot dimenzí** v poli **Dimenze** vyberte typ dimenze.
4. V seznamu vyberte sadu ke zkopírování a poté klikněte na tlačítko **Uložit jako**.
5. Zadejte nový název zkopírované sady a klikněte na tlačítko **OK**.

### <a name="delete-a-dimension-set"></a>Odstranění sady dimenzí

1. V Návrháři sestav otevřete definici řádků, sloupců nebo stromu, kterou chcete změnit.
2. V nabídce **Upravit** klikněte na tlačítko **Správa sad hodnot dimenzí**.
3. V dialogovém okně **Správa sad hodnot dimenzí** v poli **Dimenze** vyberte typ dimenze.
4. Vyberte sadu, kterou chcete odstranit, a klikněte na příkaz **Odstranit**. Kliknutím na tlačítko **Ano** se tato sada hodnot dimenze trvale odstraní.

## <a name="additional-resources"></a>Další prostředky

[Finanční výkaznictví](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
