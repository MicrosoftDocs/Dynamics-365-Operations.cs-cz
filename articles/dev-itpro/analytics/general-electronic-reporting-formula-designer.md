---
title: "Návrhář receptur v elektronickém výkaznictví"
description: "Toto téma popisuje, jak lze používat návrháře receptur v elektronickém výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: adbbb36da2bc1e9a2211c703823370571105ecab
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="formula-designer-in-electronic-reporting"></a>Návrhář vzorců v elektronickém výkaznictví

[!INCLUDE [banner](../includes/banner.md)]

Toto téma popisuje, jak lze používat návrháře receptur v elektronickém výkaznictví. Při vytváření formátu pro určitý elektronický dokument pro elektronické výkaznictví můžete použít vzorce k převodu dat za účelem plnění požadavků na plnění a formátování daného dokumentu. Tyto vzorce připomínají vzorce aplikace Microsoft Excel. Ve vzorcích jsou podporovány různé typy funkcí: text, datum a čas, matematika, logika, informace, převod datových typů a další (funkce specifické pro danou obchodní doménu).

## <a name="formula-designer-overview"></a>Přehled návrháře vzorců

Elektronické výkaznictví podporuje návrháře receptur. Proto můžete během návrhu konfigurovat výrazy, které lze použít pro následující úkoly za běhu:

- Transformace dat přijatých z databáze Microsoft Dynamics 365 for Finance and Operations, která mají být zadána v datovém modelu elektronického výkaznictví, který je určený jako zdroj dat pro formáty elektronického výkaznictví. (Tyto transformace mohou například zahrnovat filtrování, seskupení a převod typů dat.)
- Formátování dat, která musí být odeslána do generovaného elektronické dokument v souladu s rozvržením a podmínkami konkrétního formátu elektronického výkaznictví. (Formátování může být například provedeno v souladu s požadovaným jazykem, jazykovou verzí nebo kódováním).
- Kontrola procesu vytváření elektronických dokumentů. (Například výrazy mohou povolit nebo zakázat výstup konkrétních prvků formátu, v závislosti na zpracování dat. Mohou rovněž přerušit proces vytváření dokumentu nebo odesílat zprávy uživateli.)

Můžete otevřít stránku **Návrhář receptur** po provedení některé z následujících akcí:

- vazba položek zdroje dat na součásti datového modelu,
- vazba položek zdroje dat na součásti formátu,
- kompletní údržba vypočtených polí, která jsou součástí datových zdrojů.
- definování podmínek viditelnosti pro vstupní parametry uživatele,
- návrh transformací formátu,
- definování povolení podmínek pro součásti formátu,
- definování názvů souborů pro součásti souboru formátu,
- definování podmínek pro ověření kontroly procesu,
- definování textu zpráv pro ověření kontroly procesu.

## <a name="designing-er-formulas"></a>Vytvoření vzorců elektronického výkaznictví

### <a name="data-binding"></a>Datová vazba

Návrháře receptur elektronického výkaznictví lze použít k definování výrazu, který převádí data přijatá ze zdrojů dat, aby tato data bylo možné zadat v příjemci dat za běhu:

- ze zdrojů dat aplikace Finance and Operations a parametrů spuštění do datového modelu elektronického výkaznictví,
- z datového modelu elektronického výkaznictví do formátu elektronického výkaznictví,
- ze zdrojů dat aplikace Finance and Operations a parametrů spuštění do formátu elektronického výkaznictví.

Následující obrázek znázorňuje návrh výraz tohoto typu. V tomto příkladu výraz zaokrouhluje hodnotu pole **Intrastat.AmountMST** tabulky Intrastat aplikace Finance and Operations na dvě desetinná místa a vrací zaokrouhlenou hodnotu.

[![Datová vazba](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Je možné použít následující obrázek, který znázorňuje návrh výrazu tohoto typu. V tomto příkladu je výsledek navrženého výrazu zadán do komponenty **Transaction.InvoicedAmount** datového modelu **Vykazování daně**.

[![Používané datové vazby](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Navržený vzorec **ROUND (Intrastat.AmountMST 2)**, zaokrouhluje za běhu hodnot pole **AmountMST** pro každý záznam v tabulce Intrastat na dvě desetinná místa. Poté zadá zaokrouhlenou hodnotu do komponenty **Transaction.InvoicedAmount** datového modelu **Vykazování daně**.

### <a name="data-formatting"></a>Formátování dat

Návrháře receptur elektronického výkaznictví lze použít k definování výrazu, který naformátuje data přijatá ze zdrojů dat, aby tato data bylo možné odeslat jako součást generovaného elektronického dokumentu: Můžete mít formátování, které je třeba použít jako typické pravidlo, které by mělo být znovu použito pro formát. V takovém případě můžete uvést toto formátování jednou v konfiguraci formátu jako pojmenovanou transformaci, která má výraz formátování. Tuto pojmenovanou transformaci lze potom propojit s mnoha komponentami formátu, kde výstup musí být formátován podle vytvořeného výrazu formátování.

Následující obrázek znázorňuje návrh transformace tohoto typu. V tomto příkladu ořeže transformace **TrimmedString** vstupní data typu dat **Řetězec** odstraněním počáteční a koncové mezery. Itd vrátí hodnotu oříznutého řetězce.

[![Transformace](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Je možné použít následující obrázek, který znázorňuje návrh transformace tohoto typu. V tomto příkladu více součástí formátu odesílá text jako výstup do generovaného elektrického dokumentu za běhu. Všechny tyto součásti formátu odkazují na transofmraci **TrimmedString** podle názvu.

[![Použitá transformace](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Když součásti formátu, jako je například součást **partyName** na předchozím obrázku, odkazují na transformaci **TrimmedString**, transformace odešle text jako výstup generovaného elektronického dokumentu. Tento text nezahrnuje počáteční a koncové mezery.

Pokud máte formátování, které je nutné použít jednotlivě, můžete toto formátování použít jako jednotlivý výraz vazby konkrétní součásti formátu. Následující obrázek znázorňuje výraz tohoto typu. V tomto příkladu je součást formátu **partyType** vázána na zdroj dat pomocí výrazu, který převede příchozí data z pole **Model.Company.RegistrationType** ve zdroji dat na text s velkými písmeny. Výraz pak odešle tento text jako výstup do elektronického dokumentu.

[![Použití formátování na jednotlivou součást](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Kontrola procesního toku

Návrháře receptur elektronického výkaznictví lze použít k definování výrazů, které se používají k řízení toku procesu generovaných elektronických dokumentů. K dispozici jsou tyto úlohy:

- Definujte podmínky určující, kdy musí být zastaven proces vytvoření dokumentu.
- Zadejte výrazy, které vytvoří zprávy pro uživatele o zastaveném procesu nebo vyvolají spuštění zpráv protokolu o pokračujícím procesu generování sestav.
- Zadejte názvy souborů generovaných elektronických dokumentů a řiďte podmínky jejich vytvoření.

Každé pravidlo procesu řízení toku je navržen jako jednotlivé ověření. Následující obrázek znázorňuje ověření tohoto typu. Zde je vysvětlení konfigurace v tomto příkladu:

- Ověření je vyhodnoceno, když je uzel **INSTAT** vytvořen během generování souboru XML.
- Pokud je seznam transakcí prázdný, ověření zastaví proces spouštění a vrátí hodnotu **FALSE**.
- Ověření vrátí chybovou zpráva, která obsahuje textu Finance and Operations popisku SYS70894 v upřednostňovaném jazyce uživatele.

[![Ověření](./media/picture-validation.jpg)](./media/picture-validation.jpg)

Návrhář receptur elektronického výkaznictví lze také použít k vygenerování názvu souboru pro generovaný elektronický dokument a kontrolu procesu vytvoření souboru. Následující obrázek znázorňuje návrh kontroly procesního toku tohoto typu. Zde je vysvětlení konfigurace v tomto příkladu:

- Seznam záznamů z datového zdroje **model.Intrastat** je rozdělen do dávek. Každá dávka obsahuje až 1 000 záznamů.
- Výstup vytvoří soubor ZIP, který obsahuje jeden soubor ve formátu XML pro každou dávku, která byla vytvořena.
- Výraz vrátí název souboru pro generované elektronické dokumenty zřetězením názvu a přípony souboru. Pro druhou dávku a všechny následné dávky obsahuje název souboru ID dávky jako příponu.
- Výraz umožňuje (vrácením hodnoty **TRUE**) proces vytváření souborů pro dávky, které obsahují alespoň jeden záznam.

[![Kontrola souboru](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Základní syntaxe

Výrazy elektronické výkaznictví mohou obsahovat jakékoli nebo všechny následující prvky:

- Konstanty
- Operátory
- Odkazy
- Cesty
- Funkce

#### <a name="constants"></a>Konstanty

Při návrhu výrazů lze použít text a numerické konstanty (hodnoty, které nejsou vypočteny). Například výraz **VALUE ("100") + 20** používá číselnou konstantu **20** a řetězcovou konstantu **"100"** a vrátí číselnou hodnotu **120**. Návrhář receptur elektronického výkaznictví podporuje řídicí sekvence. Můžete tedy určit řetězec výrazu, se kterým má být zacházeno jinak. Například výraz **"Lev Tolstoj ""Vojna a mir"" Svazek 1"** vrátí textový řetězec **Lev Tolstoj "Vojna a mir" Svazek 1**.

#### <a name="operators"></a>Operátory

Následující tabulka ukazuje aritmetické operátory, které lze používat k provádění základních matematických operací, například sčítání, odčítání, dělení a násobení.

| Operátor | Význam               | Příklad |
|----------|-----------------------|---------|
| +        | Dodatek              | 1+2     |
| -        | Odečítání, negace | 5-2, -1 |
| \*       | Násobení        | 7\*8    |
| /        | Divize              | 9/3     |

Následující tabulka ukazuje operátory porovnávání, které jsou podporovány. Tyto operátory slouží k porovnání dvou hodnot.

| Operátor | Význam                  | Příklad    |
|----------|--------------------------|------------|
| =        | Rovno                    | X=Y        |
| &gt;     | Je větší než             | X&gt;Y     |
| &lt;     | Je menší než                | X&lt;Y     |
| &gt;=    | Větší než nebo rovno | X&gt;=Y    |
| &lt;=    | Menší než nebo rovno    | X&lt;=Y    |
| &lt;&gt; | Není rovno             | X&lt;&gt;Y |

Kromě toho můžete použít znak & jako operátor ke zřetězení textu. Tímto způsobem můžete spojit nebo zřetězit jeden nebo více řetězců do jednoho textu.

| Operátor | Význam     | Příklad                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Sloučit | "Nic k tisku" & ":&nbsp;" & "nebyly nalezeny žádné záznamy" |

##### <a name="operator-precedence"></a>Priorita operátorů

Pořadí, v jakém jsou části složeného výrazu vyhodnoceny, je důležité. Například výsledek výrazu **1 + 4 / 2** se liší v závislosti na tom, zda se provádí nejprve sčítání nebo dělení. Pomocí závorek lze explicitně definovat způsob vyhodnocení výrazu. Chcete-li například uvést, že se sčítání musí provést jako první, můžete upravit předchozí výraz na **(1 + 4) / 2**. Pokud pořadí operací ve výrazu, není explicitně definováno, pořadí vychází z výchozí priority přiřazené k podporovaným operátorům. V následující tabulce je priorita, která je přiřazena ke každému operátoru. Operátory, které mají vyšší prioritu (například 7), jsou vyhodnoceny dříve než operátory s nižší prioritou (například 1).

| Priorita | Operátory      | Syntaxe                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Seskupení       | ( … )                                                                   |
| 6          | Přístup členů  | … . …                                                                   |
| 5          | Volání funkce  | … ( … )                                                                 |
| 4          | Multiplikativní | … \* …<br>… / …                                                         |
| 3          | Přídavné       | … + …<br>… - …                                                          |
| 2          | Porovnání     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Dělení     | … , …                                                                   |

Pokud výraz obsahuje několik po sobě jdoucích operátorů, které mají stejnou prioritu, vyhodnocují se tyto operátory zleva doprava. Například výraz **1 + 6 / 2 \* 3 &gt; 5** vrátí hodnotu **true**. Doporučujeme vám pomocí závorek explicitně určit požadované pořadí operátorů ve výrazech, usnadní se tím čtení a správa výrazů.

#### <a name="references"></a>Odkazy

Všechny zdroje dat aktuální součásti elektronického výkaznictví, které jsou k dispozici během návrhu výrazu, lze použít jako pojmenované odkazy. (Aktuální součást elektronického výkaznictví může být model nebo formát.) Aktuální datový model model elektronického výkaznictví obsahuje například datový zdroj **ReportingDate** a tento datový zdroj vrací hodnotu typu dat **DATETIME**. Abyste tuto hodnotu v generování dokumentu správně zformátovali, můžete odkazovat na zdroj dat ve výrazu jako je **DATETIMEFORMAT (ReportingDate, "dd-MM-rrrr")**.

Všechny znaky v názvu referenčního datového zdroje, které nepředstavují písmeno abecedy, musí předcházet jednoduchá uvozovka ('). Pokud název odkazujícího zdroje dat obsahuje alespoň jeden znak, který nepředstavuje písmeno abecedy, musí být název v jednoduchých uvozovkách. (Těmito nealfabetickými symboly mohou být například interpunkční znaménka nebo jiné psané symboly.) Zde je několik příkladů:

- Datový zdroj **Dnešní datum a čas** je nutné odkazovat ve výrazu elektronického výkaznictví jako **Dnešní datum a čas**.
- Na metodu **name()** zdroje dat **Odběratelé** musí být odkazováno ve výrazu elektronického výkaznictví jako **Odběratelé.'name()'**

Pokud mají metody aplikace Finance and Operations datové zdroje s parametry, používá se pro volání těchto metod následující syntaxe:

- Pokud má metoda **isLanguageRTL** datového zdroje **Systém** parametr **EN-US** datového typu **Řetězec**, musí být odkazována ve výrazu elektronického výkaznictví jako **System.'isLanguageRTL'("EN-US")**.
- Pokud název metody obsahuje pouze alfanumerické znaky, nejsou uvozovky vyžadovány. U metod tabulky, jejichž název obsahuje závorky, jsou však povinné.

Při přidání datového zdroje **Systém** do mapování elektronického výkaznictví, které odkazuje na třídu aplikace Finance and Operations **Globální**, výraz vrátí logickou hodnotu **FALSE**. Upravený výraz **System.' isLanguageRTL'("AR")** vrátí logickou hodnotu **TRUE**.

Je možné omezit způsob, jakým jsou hodnoty předány do parametrů tohoto typu metody:

- Lze předat pouze konstanty do metod tohoto typu. Hodnoty konstant jsou definovány v době návrhu.
- Podporovány jsou pouze jednoduché (základní) datové typy pro parametry tohoto typu. (Jednoduché datové typy jsou celé číslo, reálné, logická hodnota, řetězec atd).

#### <a name="paths"></a>Cesty

Pokud výraz odkazuje na strukturovaný zdroj dat, můžete použít definici cesty k volbě určitého primitivního prvku daného zdroje dat. Znak tečky (.) se používá k oddělení jednotlivých prvků strukturovaného zdroje dat. Například aktuální datový model elektronického výkaznictví obsahuje zdroj dat **InvoiceTransactions** a ten vrátí seznam záznamů. Struktura záznamu **InvoiceTransactions** obsahuje pole **AmountDebit** a **AmountCredit** a obě tato pole vrací číselné hodnoty. Proto můžete vytvořit následující výraz pro výpočet fakturované částky: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Funkce

Další část popisuje funkce, které lze použít ve výrazech elektronického výkaznictví. Všechny zdroje dat kontextu výrazu (aktuální datový model nebo formát elektronického výkaznictví) mohou sloužit jako parametry funkcí volání, v souladu se seznamem argumentů pro funkce volání. Konstanty lze také použít jako parametry funkcí volání. Například aktuální datový model elektronického výkaznictví obsahuje zdroj dat **InvoiceTransactions** a ten vrátí seznam záznamů. Struktura záznamu **InvoiceTransactions** obsahuje pole **AmountDebit** a **AmountCredit** a obě tato pole vrací číselné hodnoty. Takže pokud chcete vypočítat částku, můžete vytvořit následující výraz využívající integrovanou funkci zaokrouhlování pro použití v elektronickém výkaznictví: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Podporované funkce

V následující tabulce jsou popsány funkce pro manipulaci s daty, které lze použít k vytváření datových modelů a sestav elektronického výkaznictví. Seznam funkcí není pevný. Vývojáři ho mohou rozšířit. Chcete-li zobrazit seznam funkcí, které můžete použít, otevřete podokno funkcí v návrháři receptur elektronického výkaznictví.

### <a name="date-and-time-functions"></a>Funkce data a času

| Funkce | Popis | Příklad |
|----------|-------------|---------|
| ADDDAYS (datum a čas, dny) | Přidá zadaný počet dní k zadané hodnotě data a času. | **ADDDAYS (NOW(), 7)** vrátí datum a čas sedm dní v budoucnosti. |
| DATETODATETIME (datum) | Převede zadanou hodnotu data na hodnotu data a času. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** vrátí datum aktuální relace aplikace Finance and Operations, např. 24. prosince 2015, jako **12/24/2015 12:00:00 AM**. V tomto příkladu **CompInfo** představuje zdroj dat elektronického výkaznictví typu **Finance and Operations/Table** a odkazuje na tabulku CompanyInfo. |
| NOW () | Vrátí aktuální datum a čas relace aplikačního serveru Finance and Operations jako hodnotu data a času. | |
| TODAY () | Vrátí aktuální datum relace aplikačního serveru Finance and Operations jako hodnotu data. | |
| NULLDATE () | Vrátí hodnotu data **null**. | |
| NULLDATETIME () | Vrátí hodnotu data a času **null**. | |
| DATETIMEFORMAT (datum a čas, formát) | Převede zadanou hodnotu data a času na řetězec v zadaném formátu. (Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** vrátí aktuální datum aplikačního serveru Finance and Operations, například 24. prosince 2015 jako **"24-12-2015"** na základě zadaného vlastního formátu. |
| DATETIMEFORMAT (datum a čas, jazyková verze) | Převede zadanou hodnotu data a času na řetězec v zadaném formátu a [jazykové verzi](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informace o podporovaných formátech viz [standardní](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** vrátí aktuální datum aplikačního serveru Finance and Operations, například 24. prosince 2015, jako **"24.12.2015"**, na základě vybraného německého prostředí. |
| SESSIONTODAY () | Vrátí aktuální datum relace aplikace Finance and Operations jako hodnotu data. | |
| SESSIONNOW () | Vrátí aktuální datum a čas relace aplikace Finance and Operations jako hodnotu data a času. | |
| DATEFORMAT (datum, formát) | Vrátí znázornění řetězce zadaného data v zadaném formátu. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")**  vrátí aktuální datum aplikace Finance and Operations, například 24. prosince 2015 jako **"24-12-2015"** na základě zadaného vlastního formátu. |
| DATEFORMAT (datum, formát, jazyková verze) | Převede zadanou hodnotu data na řetězec v zadaném formátu [jazykové verzi](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informace o podporovaných formátech viz [standardní](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** vrátí aktuální datum aplikace Finance and Operations, například 24. prosince 2015, jako **"24.12.2015"**, na základě vybraného německého prostředí. |
| DAYOFYEAR (datum) | Vrátí celočíselnou reprezentaci počtu dní mezi 1. lednem a zadaným datem. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** vrátí **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** vrátí **1**. |
| DAYS (datum 1, datum 2) | Vrátí počet dní mezi prvním a druhým určeným datem. Vrátí kladnou hodnotu, pokud je první datum pozdější než druhé datum, vrátí **0** (nulu), když se první datum shoduje s druhým datem, nebo vrátí zápor nou hodnotu v opačném případě. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** vrátí **-1**. |

### <a name="data-conversion-functions"></a>Funkce převodu dat

| Funkce | popis | Příklad |
|----------|-------------|---------|
| DATETODATETIME (datum) | Převede zadanou hodnotu data na hodnotu data a času. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** vrátí datum aktuální relace aplikace Finance and Operations, např. 24. prosince 2015, jako **12/24/2015 12:00:00 AM**. V tomto příkladu **CompInfo** představuje zdroj dat elektronického výkaznictví typu **Finance and Operations/Table** a odkazuje na tabulku CompanyInfo. |
| DATEVALUE (řetězec, formát) | Vrátí znázornění data zadaného řetězce v zadaném formátu. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** vrátí datum 21. prosince 2016 na základě zadaného vlastního formátu a výchozí jazykové verze aplikace **EN-US**. |
| DATEVALUE (řetězec, formát, prostředí) | Vrátí znázornění data zadaného řetězce v zadaném formátu a jazykové verzi. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** vrátí datum 21. ledna 2016 na základě zadaného vlastního formátu a jazykové verze. Nicméně **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** zobrazí výjimku za účelem informování uživatele, že zadaný řetězec nebyl rozpoznán jako platné datum. |
| DATETIMEVALUE (řetězec, formát) | Vrátí znázornění data a času zadaného řetězce v zadaném formátu. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** vrátí 2:55:00 21. prosince 2016 na základě zadaného vlastní formátu a výchozí jazykové verze aplikace **EN-US**. |
| DATETIMEVALUE (řetězec, formát, prostředí) | Vrátí znázornění data a času zadaného řetězce v zadaném formátu a jazykové verzi. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** vrátí 2:55:00 21. prosince 2016 na základě zadaného vlastní formátu a výchozí jazykové verze aplikace EN-US. Nicméně **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** zobrazí výjimku za účelem informování uživatele, že zadaný řetězec nebyl rozpoznán jako platné datum. |

### <a name="list-functions"></a>Funkce seznamu

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkce</th>
<th>popis</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (vstup, délka)</td>
<td>Rozdělí zadaný vstupní řetězec na dílčí řetězce, přičemž každý bude mít zadanou délku. Vrátí výsledek jako nový seznam.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> vrátí nový seznam obsahující dva záznamy, které mají pole <strong>STRING</strong>. Pole v prvním záznamu obsahuje text <strong>&quot;abc&quot;</strong> a pole v druhém záznamu obsahuje text <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (seznam, počet)</td>
<td>Rozdělí zadaný seznam na dávky, přičemž každá z nich obsahuje zadaný počet záznamů. Vrátí výsledek jako nový seznam dávek, který obsahuje následující prvky:
<ul>
<li>Dávky jako běžné seznamy (součást <strong>Value</strong>)</li>
<li>Číslo aktuální dávky (součást <strong>BatchNumber</strong>)</li>
</ul></td>
<td>V následujícím příkladu je datový zdroj <strong>Řádky</strong> vytvořen jako seznam záznamů ze tři záznamů. Tento seznam je rozdělen do dávek, z nichž každá obsahuje až dva záznamy.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Následující obrázek znázorňuje navržené rozvržení formátu. V tomto rozvržení formátu jsou vytvořeny vazby na datový zdroj <strong>Řádky</strong> za účelem vygenerování výstupu ve formátu XML. Tento výstup představuje jednotlivé uzly pro každou dávku a záznamy v ní.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (záznam 1 [, záznam 2, …])</td>
<td>Vrátí nový seznam, který je vytvořený na základě zadaných argumentů.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> vrátí prázdný záznam, kde seznam polí obsahuje všechna pole seznamů záznamů <strong>MainData</strong> a <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (seznam 1, seznam 2, …)</td>
<td>Vrátí spojený seznam, který je vytvořený ze seznamů zadaných argumentů.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> vrátí seznam šesti záznamů, kde jedno pole datového typu <strong>STRING</strong> obsahuje jednotlivá písmena.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (seznam)</td>
<td>Vrátí hodnotu <strong>TRUE</strong>, pokud zadaný seznam neobsahuje žádné prvky. V opačném případě vrátí hodnotu <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (seznam)</td>
<td>Vrátí prázdný seznam pomocí zadaného seznamu jako zdroje pro strukturu seznamu.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> vrátí nový prázdný seznam, který má stejnou strukturu jako seznam vrácený funkcí <strong>SPLIT</strong>.</td>
</tr>
<tr class="odd">
<td>FIRST (seznam)</td>
<td>Vrátí první záznam zadaného seznamu, pokud tento záznam není prázdný. V opačném bude vyvolána výjimka.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (seznam)</td>
<td>Vrátí první záznam zadaného seznamu, pokud tento záznam není prázdný. V opačném vrátí záznam <strong>null</strong>.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (seznam)</td>
<td>Vrátí seznam obsahující pouze první položku zadaného seznamu.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (cesta)</td>
<td>Vrátí nový plochý seznam, který obsahuje všechny položky odpovídající zadané cestě. Cesta musí být definována jako platná cesta zdroje dat k prvku zdroje dat typu dat seznamu záznamů. Datové prvky, jako je cesta k řetězci, datum atd. by měly zobrazit chybu v době návrhu v tvůrci výrazů elektronického výkaznictví.</td>
<td>Zadáte-li <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> jako zdroj dat (DS), <strong>COUNT( ALLITEMS (DS.Value))</strong> vrátí <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (seznam [, výraz 1, výraz 2…])</td>
<td>Vrátí zadaný seznam po seřazení podle zadaných argumentů. Tyto argumenty lze definovat jako výrazy.</td>
<td>Jestliže je položka <strong>Vendor</strong> konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, <strong>ORDERBY (Vendors, Vendors.&#39;name()&#39;)</strong> vrátí seznam dodavatelů seřazených podle názvu ve vzestupném pořadí.</td>
</tr>
<tr class="even">
<td>REVERSE (seznam)</td>
<td>Vrátí zadaný seznam v obráceném pořadí.</td>
<td>Jestliže je položka <strong>Vendor</strong> konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, <strong>REVERSE (ORDERBY (Vendors, Vendors.'nam.&#39;name()&#39;)) )</strong> vrátí seznam dodavatelů seřazených podle názvu v sestupném pořadí.</td>
</tr>
<tr class="odd">
<td>WHERE (seznam, podmínka)</td>
<td>Vrátí zadaný seznam po vyfiltrování podle zadané podmínky. Zadaná podmínka se použije na seznam v paměti. Tímto způsobem se funkce <strong>WHERE</strong> liší od funkce <strong>FILTER</strong>.</td>
<td>Jestliže je položka <strong>Dodavatel</strong> konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> vrátí pouze seznam dodavatelů patřících do skupiny dodavatelů č. 40.</td>
</tr>
<tr class="even">
<td>ENUMERATE (seznam)</td>
<td>Vrátí nový seznam, který se skládá z výčtových záznamů zadaného seznamu a poskytne následující prvky:
<ul>
<li>Zadané záznamy seznamu jako běžné seznamy (součást <strong>hodnota</strong>)</li>
<li>Aktuální index záznamů (součást <strong>číslo</strong>)</li>
</ul></td>
<td>Na následujícím obrázku je zdroj dat <strong>Enumerated</strong> vytvořen jako výčtový seznam záznamů dodavatelů ze zdroje dat <strong>Vendors</strong>, který odkazuje na tabulku VendTable.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Následující obrázek znázorňuje formát. V tomto formátu jsou vytvořeny vazby za účelem vygenerování výstupu ve formátu XML. Tento výstup představuje jednotlivé dodavatel jako výčtové uzly.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (seznam)</td>
<td>Vrátí počet záznamů v zadaném seznamu, pokud tento seznam není prázdný. V opačném případě vrátí hodnotu <strong>0</strong> (nula).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> vrátí <strong>2</strong>, protože funkce <strong>SPLIT</strong> vytvoří seznam, který se skládá ze dvou záznamů.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (cesta)</td>
<td>Vrátí seznam záznamů vytvořený z argumentu jednoho z následujících typů:
<ul>
<li>Výčet modelu</li>
<li>Výčet formátu</li>
<li>Kontejner</li>
</ul>
<p>Vytvořený seznam obsahuje záznamy, které mají následující pole:</p>
<ul>
<li>Jméno</li>
<li>Štítek</li>
<li>popis</li>
</ul>
Při běhu vrátí pole <strong>Popisek</strong> a <strong>Popis</strong> hodnoty založené na jazykovém nastavení formátu.</td>
<td>Na následujícím obrázku je výčet uveden v datovém modelu.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Následující obrázek znázorňuje tyto podrobnosti:</p>
<ul>
<li>Výčet modelů je vložen do sestavy jako zdroj dat.</li>
<li>Výraz elektronického výkaznictví používá výčet modelů jako parametr funkce <strong>LISTOFFIELDS</strong>.</li>
<li>Zdroj dat typu seznamu záznamů je vložen do sestavy pomocí vytvořeného výrazu elektronického výkaznictví.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Následující příklad uvádí prvky formátu ER, které jsou vázané na zdroj dat typu seznamu záznamů, který byl vytvořen pomocí funkce <strong>LISTOFFIELDS</strong>.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE]<br>
Přeložený text popisků a popisů je zadáván do výstupu formátu elektronického výkaznictví na základě nastavení jazyka nadřazených prvků formátu FILE a FOLDER.</blockquote></td>
</tr>
<tr class="odd">
<td>LISTOFFIELDS (cesta, jazyk)</td>
<td>Vrátí seznam záznamů vytvořený z argumentu, jako například výčet modelů, výčet formátů nebo kontejner. Vytvořený seznam obsahuje záznamy, které mají následující pole:
<ul>
<li>Jméno</li>
<li>Štítek</li>
<li>popis</li>
<li>Je přeloženo</li>
</ul>
<p>Při běhu vrátí pole <strong>Popisek</strong> a <strong>Popis</strong> hodnoty založené na jazykovém nastavení formátu a zadaném jazyku. Pole <strong>Je přeloženo</strong> označuje, že pole <strong>Popisek</strong> je přeloženo do určeného jazyka.</td>
<td>Například použijete typ datového zdroje <strong>Vypočítané pole</strong> ke konfiguraci datových zdrojů <strong>enumType_de</strong> a <strong>enumType_deCH</strong> pro výčet datových modelů <strong>enumType</strong>:
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
V takovém případě můžete použít následující výraz k získání popisku hodnoty výčtu ve švýcarské němčině, pokud je tento překlad k dispozici. Není-li překlad do švýcarské němčiny k dispozici, je popisek v němčině: <strong>IF (není (enumType_deCH.IsTranslated) enumType_de. Popisek, enumType_deCH.Label)</strong>.</td>
</tr>
<tr class="even">
<td>STRINGJOIN (seznam, název pole, oddělovač)</td>
<td>Vrátí řetězec, který se skládá ze zřetězených hodnot zadaného pole ze zadaného seznamu. Hodnoty jsou odděleny určeným oddělovačem.</td>

<td>Pokud zadáte <strong>SPLIT(&quot;abc&quot; , 1)</strong> jako zdroj dat (DS), výraz <strong>STRINGJOIN (DS, DS.Value, &quot;:&quot;)</strong> vrátí <strong>&quot;a</strong><strong>:b</strong><strong>:c&quot;</strong>.</td>

</tr>
<tr class="odd">
<td>SPLITLISTBYLIMIT (seznamu, hodnota limitu, zdroj limitu)</td>
<td>Rozdělí zadaný seznam na nový seznam podřízených seznamů a vrátí výsledek v obsahu seznamu záznamů. Parametr hodnoty limitu určuje hodnotu limitu k rozdělení původního seznamu. Parametr zdroje limitu určuje krok, o který se celkový součet zvýší. Limit nebude použito na jednu položku z původního seznamu, když zdrojový limit překročí definovaný limit.</td>
<td>Následující obrázek zobrazuje formát a zdroje dat, které se pro něj používají. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Následující obrázek znázorňuje výsledek při spuštění formátu. V takovém případě je výstup prostý seznam položek komodit.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Následující obrázek uvádí stejný formát, který byl upraven tak, aby obsahoval seznam položek komodit v dávkách, kdy musí jedna dávka zahrnovat komodity a celková hmotnost nesmí překračovat limit 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Následující obrázek znázorňuje výsledek při spuštění upraveného formátu.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE]<br>
Limit není použit na poslední položku v původním seznamu, protože hodnota (11) zdroje limitu (hmotnost) překračuje definovaný limit (9). Použijte funkci <strong>WHERE</strong> nebo výraz <strong>Enabled</strong> odpovídajícího prvku formátu k ignorování (přeskočení) dílčích seznamů během generování sestavy podle potřeby.</blockquote></td>
</tr>
<tr class="even">
<td>FILTER (seznam, podmínka)</td>
<td>Vrátí zadaný seznam po úpravě dotazu k filtrování podle zadané podmínky. Tato funkce se liší od funkce <strong>WHERE</strong>, protože zadaná podmínka je použita u jakéhokoli zdroje dat elektronického výkaznictví typu <strong>Záznamy tabulky</strong> na úrovni databáze. Seznam a podmínku lze definovat pomocí tabulek a relací.</td>
  <td>Jestliže je položka <strong>Dodavatel</strong> konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, <strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> vrátí pouze seznam dodavatelů patřících do skupiny dodavatelů č. 40. Pokud je <strong>Vendor</strong> nakonfigurován jako zdroj dat elektronického výkaznictví, který se vztahuje k tabulce <strong>VendTable</strong> a <strong>parmVendorBankGroup</strong> nakonfigurovaný jako zdroj elektronického výkaznictví vrací hodnotu v datovém typu řetězce, <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong>  vrací seznam pouze těch dodavatelských účtů, které patří ke konkrétní bankovní skupině.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logické funkce

| Funkce | popis | Příklad |
|----------|-------------|---------|
| CASE (výraz, možnost 1, výsledek 1 \[, možnost 2, výsledek\] … \[, výchozí výsledek\]) | Vyhodnotí zadanou hodnotu výrazu s ohledem na zadané alternativní možnosti. Vrací výsledek možnosti, která je rovna hodnotě výrazu. V opačném případě vrací volitelný výchozí výsledek, pokud je zadán výchozí výsledek. (Výchozí výsledek je poslední parametr, který nepředchází žádná možnost). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** vrátí řetězec **"WINTER"**, jestliže je aktuální datum relace aplikace Finance and Operations mezi říjnem a prosincem. Jinak bude vrácen prázdný řetězec. |
| IF (podmínka, hodnota 1, hodnota 2) | Při splnění dané podmínky bude vrácena první zadaná hodnota. V opačném případě vrací druhou zadanou hodnotu. Pokud hodnoty 1 a 2 jsou záznamy nebo seznamy záznamů, má výsledek pouze pole, která existují v obou seznamech. | **IF (1=2, "podmínka je splněna", "podmínka není splněna")** vrátí řetězec **"podmínka není splněna"**. |
| NOT (podmínka) | Vrátí obrácenou logickou hodnotu zadané podmínky. | **NOT (TRUE)** vrátí **FALSE**. |
| AND (podmínka 1\[, podmínka 2, …\]) | Vrátí **TRUE**, pokud jsou *všechny* zadané podmínky pravda. V opačném případě vrátí hodnotu **FALSE**. | **AND (1=1, "a"="a")** vrátí **TRUE**. **AND (1=2, "a"="a")** vrátí **FALSE**. |
| OR (podmínka 1\[, podmínka 2, …\]) | Vrátí **FALSE**, pokud jsou *všechny* zadané podmínky nepravda. Vrátí **TRUE**, pokud je *jakákoli* zadaná podmínka pravda. | **OR (1=2, "a"="a")** vrátí **TRUE**. |

### <a name="mathematical-functions"></a>Matematické funkce

| Funkce | Popis | Příklad |
|----------|-------------|---------|
| ABS (číslo) | Vrací absolutní hodnotu zadaného čísla. (Jinými slovy, vrací číslo bez znaménka). | **ABS (-1)** vrátí hodnotu **1**. |
| POWER (číslo, mocnina) | Vrátí výsledek umocnění zadaného kladného čísla pomocí zadané mocniny. | **POWER (10, 2)** vrátí hodnotu **100**. |
| NUMBERVALUE (řetězec, oddělovač desetinných míst, oddělovač skupin číslic) | Převede zadaný řetězec na číslo. Zadaný oddělovač desetinných míst se použije mezi celým číslem a zlomkovou částí desetinného čísla. Zadaný oddělovač skupin číslic se použije jako oddělovač tisíců. | **NUMBERVALUE("1 234,56", ",", " ")** vrátí hodnotu **1234.56**. |
| VALUE (řetězec) | Převede zadaný řetězec na číslo. Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní spojovník (-) se používá jako záporné znaménko. Pokud jsou v zadaném řetězci obsaženy jiné než číselné znaky, bude vyvolána výjimka. | **VALUE ("1 234,56")** vyvolá výjimku. |
| ROUND (číslo, desetinná čísla) | Vrátí zadané číslo, poté, co je zaokrouhleno na zadaný počet desetinných míst:<ul><li>Pokud je hodnota parametru desetinných míst vyšší než 0 (nula), zadané číslo je zaokrouhleno na tento počet desetinných míst.</li><li>Pokud je hodnota parametru desetinných míst **0** (nula), zadané číslo je zaokrouhleno na nejbližší celé číslo.</li><li>Pokud je hodnota parametru desetinných míst nižší než 0 (nula), zadané číslo je zaokrouhleno vlevo od oddělovače desetinných míst.</li></ul> | **ROUND (1200.767, 2)** zaokrouhlí na dvě desetinná místa a vrátí hodnotu **1200.77**. **ROUND (1200.767, -3)** zaokrouhlí na nejbližší násobek 1 000 a vrátí hodnotu **1000**. |
| ROUNDDOWN (číslo, desetinná čísla) | Vrátí zadané číslo, poté, co je zaokrouhleno dolů na zadaný počet desetinných míst.<blockquote>[!NOTE]<br>Tato funkce se chová jako <strong>ROUND</strong>, ale vždy zaokrouhluje zadané číslo směrem dolů (směrem k nule).</blockquote> | **ROUNDDOWN (1200.767, 2)** zaokrouhlí směrem dolů na dvě desetinná místa a vrátí hodnotu **1200.76**. **ROUNDDOWN (1700.767, -3)** zaokrouhlí směrem dolů na nejbližší násobek 1 000 a vrátí hodnotu **1000**. |
| ROUNDUP (číslo, desetinná čísla) | Vrátí zadané číslo, poté, co je zaokrouhleno nahoru na zadaný počet desetinných míst.<blockquote>[!NOTE]<br>Tato funkce se chová jako <strong>ROUND</strong>, ale vždy zaokrouhluje zadané číslo směrem nahoru (směrem od nuly).</blockquote> | **ROUNDUP (1200.763, 2)** zaokrouhlí směrem nahoru na dvě desetinná místa a vrátí hodnotu **1200.77**. **ROUNDUP (1200.767, -3)** zaokrouhlí směrem nahoru na nejbližší násobek 1 000 a vrátí hodnotu **2000**. |

### <a name="data-conversion-functions"></a>Funkce převodu dat

| Funkce | popis | Příklad |
|----------|-------------|---------|
| VALUE (řetězec) | Převede zadaný řetězec na číslo. Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní spojovník (-) se používá jako záporné znaménko. Pokud jsou v zadaném řetězci obsaženy jiné než číselné znaky, bude vyvolána výjimka. | **VALUE ("1 234,56")** vyvolá výjimku. |
| NUMBERVALUE (řetězec, oddělovač desetinných míst, oddělovač skupin číslic) | Převede zadaný řetězec na číslo. Zadaný oddělovač desetinných míst se použije mezi celým číslem a zlomkovou částí desetinného čísla. Zadaný oddělovač skupin číslic se použije jako oddělovač tisíců. | **NUMBERVALUE("1 234,56", ",", " ")** vrátí **1234.56**. |
| INTVALUE (řetězec) | Vrátí reprezentaci celého čísla zadaného řetězce. Desetinná místa jsou oříznuta. | **INTVALUE ("100.77")** vrátí **100**. |
| INTVALUE (číslo) | Vrátí reprezentaci celého čísla zadaného čísla. Desetinná místa jsou oříznuta. | **INTVALUE (-100.77)** vrátí hodnotu **-100**. |
| INT64VALUE (řetězec) | Vrátí reprezentaci int64 zadaného řetězce. Desetinná místa jsou oříznuta. | **INT64VALUE ("22565422744")** vrátí **22565422744**. |
| INT64VALUE (číslo) | Vrátí reprezentaci int64 zadaného čísla. Desetinná místa jsou oříznuta. | **INT64VALUE (22565422744.00)** vrátí hodnotu **22565422744**. |

### <a name="record-functions"></a>Funkce záznamu

| Funkce | popis | Příklad |
|----------|-------------|---------|
| NULLCONTAINER (seznam) | Vrátí záznam **null**, který má stejnou strukturu jako zadaný seznam záznamů nebo záznam.<blockquote>[!NOTE]<br>Tato funkce je zastaralá. Místo toho použijte <strong>EMPTYRECORD</strong>.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí **SPLIT**. |
| EMPTYRECORD (záznam) | Vrátí záznam **null**, který má stejnou strukturu jako zadaný seznam záznamů nebo záznam.<blockquote>[!NOTE]<br>Záznam <strong>null</strong> je záznam, kde všechna pole mají prázdnou hodnotu. Prázdná hodnota je <strong>0</strong> (nula) pro čísla, prázdný řetězec pro řetězce atd.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí **SPLIT**. |

### <a name="text-functions"></a>Textové funkce

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkce</th>
<th>popis</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (řetězec)</td>
<td>Vrátí zadaný řetězec po převedení na velká písmena.</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> vrátí <strong>&quot;SAMPLE&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (řetězec)</td>
<td>Vrátí zadaný řetězec po převedení na malá písmena.</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> vrátí <strong>&quot;sample&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (řetězec, počet znaků)</td>
<td>Vrátí zadaný počet znaků od začátku zadaného řetězce.</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> vrátí <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (řetězec, počet znaků)</td>
<td>Vrátí zadaný počet znaků od konce zadaného řetězce.</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> vrátí <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (řetězec, počáteční pozice, počet znaků)</td>
<td>Vrátí zadaný počet znaků ze zadaného řetězce, počínaje od zadané pozice.</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> vrátí <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (řetězec)</td>
<td>Vrátí počet znaků v zadaném řetězci.</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> vrátí <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (číslo)</td>
<td>Vrátí řetězec znaků, na který odkazuje zadané číslo ve znakové sadě Unicode.</td>
<td><strong>CHAR (255)</strong> vrátí <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE]<br>
Řetězec, který vrací tato funkce, závisí na kódování, které je vybráno v nadřazeném prvku formátu SOUBORU. Více informací o seznamu podporovaných kódování naleznete v tématu <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Třída kódování</a>.</blockquote>
</td>
</tr>
<tr class="even">
<td>CONCATENATE (řetězec 1 [, řetězec 2…])</td>
<td>Vrátí všechny zadané textové řetězce po jejich spojení do jednoho řetězce.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> vrátí <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE]<br>
Výraz <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> vrátí též <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr class="odd">
<td>TRANSLATE (řetězec, vzor, náhrada)</td>
<td>Vrátí zadaný řetězec po nahrazení všech výskytů znaků v zadaném řetězci vzoru za znaky na odpovídající pozici zadaného řetězce sloužícího jako náhrada.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> nahradí vzorec <strong>&quot;cd&quot;</strong> řetězcem <strong>&quot;GH&quot;</strong> a vrátí <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (řetězec, vzor, náhrada, příznak regulérního výrazu)</td>
<td>Pokud je zadaný příznak regulérního výrazu <strong>true</strong>, vrátí zadaný po úpravě použitím regulárního výrazu zadaného jako argument vzoru pro tuto funkci. Tento výraz slouží k vyhledání znaků, které je třeba nahradit. Znaky zadaného argumentu-náhrady jsou použity k nahrazení vyhledaných znaků. Pokud je zadaný příznak regulérního výrazu <strong>false</strong>, tato funkce se chová jako <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> použije regulární výraz, ktreý odebere všechny nečíselné symboly a vrátí <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> nahradí vzorec <strong>&quot;cd&quot;</strong> řetězcem <strong>&quot;GH&quot;</strong> a vrátí <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (vstup)</td>
<td>Vrátí zadaný vstup po převedení na textový řetězec naformátovaný podle nastavení národního prostředí serveru aktuální instance aplikace Finance and Operations. Co se týká hodnot typu <strong>real</strong>, převod řetězce je omezen na dvě desetinná místa.</td>
<td>Jestliže je národní prostředí serveru Finance and Operations definováno jako <strong>EN-US</strong>, <strong>TEXT (NOW ())</strong> vrátí aktuální datum relace aplikace Finance and Operations, například 17. prosince 2015, jako textový řetězec <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> vrátí <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (řetězec 1 řetězce 2[, řetězec 3 ...])</td>
<td>Vrátí zadaný řetězec po zformátování nahrazením všech výskytů <strong>%N</strong> <em>n-tým</em> argumentem. Argumenty jsou řetězce. Pokud pro parametr není zadán argument, parametr je vrácen jako <strong>&quot;%N&quot;</strong> v řetězci. Co se týká hodnot typu <strong>real</strong>, převod řetězce je omezen na dvě desetinná místa.</td>
<td>Ná následujícím obrázku vrátí zdroj dat <strong>PaymentModel</strong> seznam záznamů odběratelů prostřednictvím součásti <strong>Customer</strong> a datum zpracování prostřednictvím pole <strong>ProcessingDate</strong>.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>Ve formátu elektronického výkaznictví, který je určený ke generování elektronického souboru pro vybrané odběratele, je vybrán řetězec <strong>PaymentModel</strong> jako zdroj dat, který řídí procesní tok. Jestliže je vybraný odběratel zastaven u data zpracování sestavy, je vyvolána výjimka pro informování uživatele. Vzorec, který je určen pro tento typ ovládacího prvku pro zpracování, může využít následující zdroje:</p>
<ul>
<li>Popisek aplikace Finance and Operations SYS70894, který má následující text:
<ul>
<li><strong>Pro jazyk EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Pro jazyk CS:</strong> &quot;Nic k vytištění&quot;</li>
</ul></li>
<li>Popisek aplikace Finance and Operations SYS18389, který má následující text:
<ul>
<li><strong>Pro jazyk EN-US:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Němčina: </strong> &quot;Debitor &#39;%1&#39; wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Zde je vzorec, který lze vytvořit:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Pokud je sestava zpracovávána pro odběratele <strong>Litware Retail</strong> 17. prosince 2015, v národním prostředí <strong>EN-US</strong> a jazyce <strong>EN-US</strong>, tento vzorec vrátí následující text, který může být uživateli nabídnut ve formě zprávy výjimky:</p>
<p>&quot;Nic k tisku. Customer Litware Retail is stopped for 12/17/2015.&quot;</p>
<p>Jestliže je stejná sestava zpracována pro odběratele <strong>Litware Retail</strong> 17. prosince 2015 v jazykové verzi <strong>DE</strong> a jazyce <strong>DE</strong>, tento vzorec vrátí následující text, který používá jiný formát data:</p>
<p>&quot;Nichts zu drucken. Debitor &#39;Litware Retail&#39; wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE]<br>
Následující syntaxe je použita ve vzorcích elektronického výkaznictví pro popisky:
<ul>
<li><strong>Popisky ze zdrojů aplikace Finance and Operations:</strong> <strong>@&quot;X&quot;</strong>, kde X je ID popisku ve stromu aplikačních objektů (AOT)</li>
<li><strong>Popisky, které se nachází v konfiguracích elektronického výkaznictví:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, kde X je ID popisku v konfiguraci elektronického výkaznictví.</li>
</ul></blockquote></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (číslo, formát)</td>
<td>Vrátí znázornění řetězce zadaného čísla v zadaném formátu. (Informace o podporovaných formátech naleznete v tématu <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standardní</a> a <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">vlastní</a>.) Spuštění této funkce v rámci určuje jazykovou verzi, která je použita k formátování čísla.</td>
<td>Pro jazykovou verzi EN-US vrátí <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> hodnotu <strong>&quot;45,00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> vrátí hodnotu <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (číslo jazyk, měna, příznak názvu měny pro tisk, desetinná místa)</td>
<td>Vrátí zadané číslo po vyslovení (převedení) na textové řetězce v zadaném jazyce. Kód jazyka je volitelný. Pokud je definován jako prázdný řetězec, použije se místo něj kód jazyka pro aktuální kontext. (Kód jazyka aktuálního kontext je definován pro generovaný soubor nebo složku). Kód měny je také volitelný. Pokud je definován jako prázdný řetězec, je použita měna společnosti.
<blockquote>[!NOTE]<br>
Příznak název měny pro tisk a parametry desetinných míst jsou analyzovány pouze pro následující jazykové kódy: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, and <strong>RU</strong>. Dále je příznak názvu měny pro tisk analyzován pouze pro společnosti používající aplikaci Finance and Operations s kontextem země nebo oblasti, který podporuje skloňování názvů měn.</blockquote></td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> returns <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> vrátí <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> vrátí <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>PADLEFT (řetězec, délka, odsazovací znaky)</td>
<td>Vrátí řetězec určené délky, ve kterém je začátek určeného řetězce odsazen určenými znaky.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> vrátí řetězec <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr class="even">
<td>TRIM (řetězec)</td>
<td>Vrátí určený textový řetězec po příznutí počátečních a koncových mezer a po odebrání více mezer mezi slovy.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ukázkový&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> vrátí <strong>&quot;Ukázkový text&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>GETENUMVALUEBYNAME (cesta zdroje dat výčtu, text popisku hodnoty výčtu)</td>
<td>Vrátí hodnotu zadaného zdroje dat výčtu podle zadaného textu popisku výčtu.</td>
<td>Na následujícím obrázku je výčet <strong>ReportDirection</strong> uveden v datovém modelu. Pro hodnoty výčtu jsou definovány popisky.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Následující obrázek znázorňuje tyto podrobnosti:</p>
<ul>
<li>Výčet modelů <strong>ReportDirection</strong> je vložený do sestavy jako zdroj dat <strong>$Direction</strong>.</li>
<li>Výraz elektronického výkaznictví <strong>$IsArrivals</strong> je určený k použití výčtu modelů jako parametr této funkce. Hodnota tohoto výrazu je <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Funkce převodu dat

| Funkce | popis | Příklad |
|----------|-------------|---------|
| TEXT (vstup) | Vrátí zadaný vstup po převedení na textový řetězec naformátovaný podle nastavení národního prostředí serveru aktuální instance aplikace Finance and Operations. Co se týká hodnot typu **real**, převod řetězce je omezen na dvě desetinná místa. | Jestliže je národní prostředí serveru Finance and Operations definováno jako **EN-US**, **TEXT (NOW ())** vrátí aktuální datum relace aplikace Finance and Operations, například 17. prosince 2015, jako textový řetězec **"12/17/2015 07:59:23 AM"**. **TEXT (1/3)** vrátí **"0.33"**. |
| QRCODE (řetězec) | Vrátí obrázek QR kódu v binárním formátu base64 pro zadaný řetězec. | **QRCODE (“Ukázkový text”)** vrátí hodnotu **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Funkce shromažďování dat

| Funkce | popis | Příklad |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Vrátí název prvku aktuálního formátu. Vrátí prázdný řetězec, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut. | Další informace o použití těchto funkcí najdete v průvodci záznamem úloh **Elektronické výkaznictví - zdroj dat formát výstupu pro inventuru a souhrn**, část obchodního procesu **Získání/vývoj komponent služby/řešení**. |
| SUMIFS (key string for summing, criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | Vrátí součet hodnot XML uzlů (s názvem definovaným jako klíč), získaný během provedení tohoto formátu, který splňuje zadané podmínky (dvojice rozsahů a hodnot). Vrací hodnotu **0** (nula), když je příznak  **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut. | |
| SUMIF (řetězec klíče pro sčítání, řetězec kritéria rozsahu, řetězec kritéria hodnoty) | Vrátí součet hodnot XML uzlů (s názvem definovaným jako klíč), získaný během provedení tohoto formátu, který splňuje zadanou podmínku (rozsah a hodnota). Vrací hodnotu **0** (nula), když je příznak  **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut. | |
| COUNTIFS (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | Vrátí počet XML uzlů získaný během provedení tohoto formátu, který splňuje zadané podmínky (dvojice rozsahů a hodnot). Vrací hodnotu **0** (nula), když je příznak  **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut. | |
| COUNTIF (řetězec rozsahu kritérií, řetězec hodnoty kritérií) | Vrátí počet XML uzlů získaný během provedení formátu, který splňuje zadanou podmínku (rozsah a hodnota). Vrací hodnotu **0** (nula), když je příznak  **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut. | |
| COLLECTEDLIST (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | Vrátí seznam hodnot XML uzlů získaný během provedení tohoto formátu, který splňuje zadané podmínky (rozsah a hodnota). Vrátí prázdný seznam, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut. | |

### <a name="other-business-domainspecific-functions"></a>Další funkce (konkrétní pro obchodní domény)

| Funkce | popis | Příklad |
|----------|-------------|---------|
| CONVERTCURRENCY (částka, zdrojová měna, cílová měna, datum, společnost) | Převede zadanou peněžní částku ze zadané měny na zadanou měnu za použití nastavení zadané společnosti v aplikaci Finance and Operations k zadanému datu. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** vrátí ekvivalent jednoho eura v amerických dolarech v aktuální den relace podle nastavení společnosti DEMF. |
| ROUNDAMOUNT (číslo, desetinná místa, pravidlo zaokrouhlování) | Zaokrouhlí zadanou částku na zadaný počet bdesetinných míst podle zadaného pravidla zaokrouhlování.<blockquote>[!NOTE]<br>Pravidlo zaokrouhlování musí být zadáno jako hodnota výčtu <strong>RoundOffType</strong> aplikace Finance and Operations.</blockquote> | Pokud je parametr **model.RoundOff** nastaven na **Downward**, **3ROUNDAMOUNT (1000.787, 2, model.RoundOff)** vrátí hodnotu **1000.78**. Pokud je parametr **model.RoundOff** nastaven na hodnotu **Normal** nebo **Rounding-up**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** vrátí hodnotu **1000.79**. |
| CURCredRef (číslice) | Vrátí referenční údaj věřitele na základě číslic zadaného čísla faktury. | **CURCredRef ("VEND-200002")** vrátí hodnotu **"2200002"**. |
| MOD\_97 (číslice) | Vrátí referenční údaj věřitele jako výraz MOD97 na základě číslic zadaného čísla faktury. | **MOD\_97 ("VEND-200002")** vrátí **"20000285"**. |
| ISOCredRef (číslice) | Vrátí ISO údaj věřitele na základě číslic a abecedních symbolů zadaného čísla faktury.<blockquote>[!NOTE]<br>Chcete-li vyloučit z abecedy symboly, které jsou v souladu se standardem ISO, vstupní parametr musí být přeložen před jeho předáním této funkci.</blockquote> | **ISOCredRef ("VEND-200002")** vrátí hodnotu **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (řetězec, číslo) | Získá ID další finanční dimenze. Dimenze jsou reprezentovány v tomto řetězci jako ID oddělená čárkou. V tomto řetězci čísla definují kód číselné řady požadované dimenze. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** vrací **"CC"**. |
| GetCurrentCompany () | Vrací textovou reprezentaci kódu právnické osoby (společnosti), ke které je uživatel momentálně přihlášen. | **GETCURRENTCOMPANY ()** vrátí hodnotu **USMF** u uživatele přihlášeného v aplikaci Finance and Operations ke společnosti **Contoso Entertainment System USA**. |
| CH\_BANK\_MOD\_10 (číslice) | Vrátí odkaz věřitele jako výraz MOD10 na základě číslic zadaného čísla faktury. | **CH\_BANK\_MOD\_10 ("VEND-200002")** vrátí **3**. |
| FA\_SUM (kód dlouhodobého majetku, kód modelu hodnoty, počáteční datum, koncové datum) | Vrátí připravený datový kontejner částky dlouhodobého majetku za období. | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** vrátí připravený datový kontejner dlouhodobého majetku **"COMP-000001"** s modelem hodnoty **"Current"** za období mezi **Date1** a **Date2**. |
| FA\_BALANCE (kód dlouhodobého majetku, kód oceňovacího modelu, vykazovaný rok, datum sestavy) | Vrátí připravený datový kontejner zůstatku dlouhodobého majetku. Rok vykazování je nutné zadat jako hodnotu výčtu aplikace Finance and Operations **AssetYear**. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** vrátí připravený datový kontejner zůstatků pro dlouhodobý majetek **"COMP-000001"** s modelem hodnoty **"Current"** k aktuálnímu datu relace aplikace 365 for Finance and Operations. |
| TABLENAME2ID (řetězec) | Vrací reprezentaci celého čísla ID tabulky pro daný název tabulky. | **TABLENAME2ID ("Intrastat")** vrátí hodnotu **1510**. |
| ISVALIDCHARACTERISO7064 (řetězec) | Vrátí logickou hodnotu **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN). V opačném případě vrátí logickou hodnotu **FALSE**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** vrátí hodnotu **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** vrátí hodnotu **FALSE**. |

### <a name="functions-list-extension"></a>Rozšíření seznamu funkcí

Elektronické výkaznictví umožňuje rozšířit seznam funkcí, které se používají ve výrazech elektronického výkaznictví. Je však vyžadováno určité technické úsilí. Další informace naleznete v tématu [Rozšíření seznamu funkcí elektronického vykazování](general-electronic-reporting-formulas-list-extension.md).

## <a name="see-also"></a>Viz také

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Rozšíření seznamu funkcí elektronického vykazování](general-electronic-reporting-formulas-list-extension.md)

