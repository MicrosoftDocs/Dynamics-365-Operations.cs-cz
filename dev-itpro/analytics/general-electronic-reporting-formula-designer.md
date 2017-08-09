---
title: "Návrhář receptur v elektronickém výkaznictví"
description: "Toto téma popisuje, jak lze používat návrháře receptur v elektronickém výkaznictví. Při vytváření formátu pro určitý elektronický dokument pro elektronické výkaznictví můžete použít vzorce podobné vzorcům aplikace Microsoft Excel pro transformaci dat za účelem plnění požadavků na plnění a formátování daného dokumentu. Jsou podporovány různé typy funkcí – text, datum a čas, matematická logika, informace, převod datových typů a další (funkce specifické pro danou obchodní doménu)."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2c04bbccf22ab830404206cd54b4cb8e97b6a822
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="formula-designer-in-electronic-reporting"></a>Návrhář receptur v elektronickém výkaznictví

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak lze používat návrháře receptur v elektronickém výkaznictví. Při vytváření formátu pro určitý elektronický dokument pro elektronické výkaznictví můžete použít vzorce podobné vzorcům aplikace Microsoft Excel pro transformaci dat za účelem plnění požadavků na plnění a formátování daného dokumentu. Jsou podporovány různé typy funkcí – text, datum a čas, matematika, logika, informace, převod datových typů a další (funkce specifické pro danou obchodní doménu).

<a name="formula-designer-overview"></a>Přehled návrháře vzorců
-------------------------

Elektronické výkaznictví podporuje návrháře receptur. Proto můžete během návrhu konfigurovat výrazy, které lze použít pro následující úkoly za běhu:

-   transformace dat, která jsou přijímána z databáze Microsoft Dynamics 365 for Finance and Operations a která mají být vyplněna v datovém modelu elektronického výkaznictví, který je určený jako zdroj dat pro formáty elektronického výkaznictví (filtrování, seskupení, převod typů dat a podobně.);
-   formátování dat, která musí být odeslána to generovaného elektronického dokumentu podle rozvržení a pravidel určitého formátu elektronického výkaznictví (podle požadovaného jazyka nebo jazykové verze, kódování atd.);
-   Řízení procesu generování elektronického dokumentu (povolení a zakázání výstupu určitých prvků formátu podle zpracování dat, přerušení vytváření dokumentu, vyvolávání zpráv pro koncové uživatele atd.).

Proto lze otevřít stránku Návrhář receptur po provedení některé z následujících akcí:

-   vazba položek zdroje dat na součásti datového modelu,
-   vazba položek zdroje dat na součásti formátu,
-   kompletní údržba vypočtených polí v rámci zdrojů dat,
-   definování podmínek viditelnosti pro vstupní parametry uživatele,
-   návrh transformací formátu,
-   definování povolení podmínek pro součásti formátu,
-   definování názvů souborů pro součásti souboru formátu,
-   definování podmínek pro ověření kontroly procesu,
-   definování textu zpráv pro ověření kontroly procesu.

## <a name="designing-er-formulas"></a>Vytvoření vzorců elektronického výkaznictví
### <a name="data-binding"></a>Datová vazba

Návrháře receptur elektronického výkaznictví lze použít k definování výrazu, který převádí data přijatá ze zdrojů dat, aby tato data bylo možné vyplnit v příjemci dat za běhu:

-   ze zdrojů dat aplikace Finance and Operations a parametrů spuštění do datového modelu elektronického výkaznictví,
-   z datového modelu elektronického výkaznictví do formátu elektronického výkaznictví,
-   ze zdrojů dat aplikace Finance and Operations a parametrů spuštění do formátu elektronického výkaznictví.

Následující obrázek znázorňuje návrh výraz tohoto typu. V tomto příkladu výraz vrací hodnotu pole **Intrastat.AmountMST** tabulky aplikace Finance and Operations **Intrastat** po zaokrouhlení hodnoty na dvě desetinná místa. [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) Následující obrázek ukazuje, jak lze použít výraz tohoto typu. V tomto příkladu je výsledek navrženého výrazu zadán do komponenty **Transaction.InvoicedAmount** datového modelu **Model vykazování daně**. [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) Při spuštění zaokrouhlí vytvořený vzorec **ROUND (Intrastat.AmountMST, 2)** hodnotu pole **AmountMST** pro každý záznam tabulky **Intrastat** na dvě desetinná místa a vyplní zaokrouhlenou hodnotu v součásti **Transaction.InvoicedAmount** datového modelu **Vykazování daně**.

### <a name="data-formatting"></a>Formátování dat

Návrháře receptur elektronického výkaznictví lze použít k definování výrazu, který naformátuje data přijatá ze zdrojů dat, aby tato data bylo možné odeslat jako součást generovaného elektronického dokumentu: Pokud máte formátování, které je třeba použít jako typické pravidlo, které by mělo být znovu využito pro formát, můžete použít toto formátování jednou v konfiguraci formátu jako pojmenovanou transformaci, která má výraz formátování. Tuto pojmenovanou transformaci lze potom propojit s mnoha komponentami formátu, jejichž výstup musí být formátován podle vytvořeného výrazu. Následující obrázek znázorňuje návrh transformace tohoto typu. V tomto příkladu přijme transformace **TrimmedString** vstupní data typu dat **řetězec** a ořeže počáteční a koncové mezery při vrácení hodnoty řetězce. [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) Následující obrázek znázorňuje, jak lze použít návrh transformace tohoto typu. V tomto příkladu několik součástí formátu, které v době spuštění odeslaly text jako výstup do generovaného elektronického dokumentu, odkazuje na transformaci **TrimmedString** názvem. [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Když komponenty formátu odkazují na transformaci **TrimmedString** (například) **partyName** na předchozím obrázku), odešle se text jako výstup generovaného dokumentu. Text nezahrnuje počáteční a koncové mezery. Pokud máte formátování, které je nutné použít jednotlivě, můžete toto formátování použít jako jednotlivý výraz vazby konkrétní součásti formátu. Následující obrázek znázorňuje výraz tohoto typu. V tomto příkladu je součást formátu **partyType** vázána na zdroj dat pomocí výrazu, který převede příchozí data z pole **Model.Company.RegistrationType** ve zdroji dat na text s velkými písmeny a odešle tento text jako výstup do elektronického dokumentu. [![picture-binding-with-formula](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Kontrola procesního toku

Návrháře receptur elektronického výkaznictví lze použít k definování výrazů, které se používají k řízení toku procesu generovaných dokumentů. Můžete provádět následující akce:

-   Definujte podmínky určující, kdy musí být zastaven proces vytvoření dokumentu.
-   Zadejte výrazy, které vytvoří zprávy pro koncového uživatele o zastaveném procesu nebo vyvolají spuštění zpráv protokolu o pokračujícím procesu generování sestav.
-   Zadejte názvy souborů generovaných dokumentů a řiďte podmínky jejich vytvoření.

Každé pravidlo procesu řízení toku je navržen jako jednotlivé ověření. Následující obrázek znázorňuje ověření tohoto typu. Zde je vysvětlení konfigurace v tomto příkladu:

-   Ověření je vyhodnoceno, když je uzel **INSTAT** vytvořen v generovaném souboru XML.
-   Pokud je seznam transakcí prázdný, ověření zastaví proces spouštění a vrátí hodnotu **FALSE**.
-   Ověření vrátí chybovou zpráva, která obsahuje textu popisku 70894 v upřednostňovaném jazyce uživatele.

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg) Příklad ověření Návrhář receptur elektronického výkaznictví lze také použít k určení názvu soubor pro generovaný elektronický dokument a kontrolu procesu vytvoření souboru. Následující obrázek znázorňuje návrh kontroly procesního toku tohoto typu. Zde je vysvětlení konfigurace v tomto příkladu:

-   Seznam záznamů ze zdroje dat **model.Intrastat** je rozdělen na dávky, z nichž každá obsahuje až 1 000 záznamů.
-   Výstup vytvoří soubor ZIP, který obsahuje jeden soubor ve formátu XML pro každou dávku, která byla vytvořena.
-   Výraz vrátí název souboru pro generování elektronických dokumentů zřetězením názvu a přípony souboru. Pro druhou dávku a všechny následné dávky obsahuje název souboru ID dávky jako příponu.
-   Výraz umožňuje (vrácením hodnoty **TRUE**) proces vytváření souborů pro dávky, které obsahují alespoň jeden záznam.

[![picture-file-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Základní syntaxe

Výrazy elektronické výkaznictví mohou obsahovat jakékoli nebo všechny následující prvky:

-   Konstanty
-   Operátory
-   Odkazy
-   Cesty
-   Funkce

#### <a name="constants"></a>Konstanty

Text a numerické konstanty (hodnoty, které nejsou vypočteny) lze použít při tvorbě výrazů. Například výraz **VALUE ("100") + 20**používá číselnou konstantu 20 a řetězcovou konstantu 100 a vrátí číselnou hodnotu **120**. Návrhář receptur elektronického výkaznictví podporuje řídicí sekvence, které tak můžete zadat jako část řetězce výrazu, s níž by se mělo zacházet jinak. Například výraz **"Lev Tolstoj ""Vojna a mir"" Svazek 1"** vrátí textový řetězec **Lev Tolstoj "Vojna a mir" Svazek 1**.

#### <a name="operators"></a>Operátory

Následující tabulka obsahuje aritmetické operátory, které lze používat k provádění základních matematických operací, například sčítání, odčítání, dělení a násobení.

| Operátor | Význam              | Příklad |
|----------|----------------------|---------|
| +        | Dodatek             | 1+2     |
| -        | Odečítání/negace | 5-2 -1  |
| \*       | Násobení       | 7\*8    |
| /        | Divize             | 9/3     |

Následující tabulka zobrazuje operátory porovnávání, které jsou také podporovány a lze používat k porovnávání dvou hodnot.

| Operátor | Význam                  | Příklad    |
|----------|--------------------------|------------|
| =        | Rovno                    | X=Y        |
| &gt;     | Je větší než             | X&gt;Y     |
| &lt;     | Je menší než                | X&lt;Y     |
| &gt;=    | Větší než nebo rovno | X&gt;=Y    |
| &lt;=    | Menší než nebo rovno    | X&lt;=Y    |
| &lt;&gt; | Není rovno             | X&lt;&gt;Y |

Kromě toho můžete použít ampersand (&) jako operátor ke zřetězení textu pro spojení, neboli zřetězení, jednoho nebo více textových řetězců do jednoho textového celku.

| Operátor | Význam     | Příklad                                        |
|----------|-------------|------------------------------------------------|
| &        | Sloučit | "Nic k tisku" & ": " & "nebyly nalezeny žádné záznamy" |

#### <a name="operator-precedence"></a>Priorita operátorů

Pořadí, v jakém jsou části složeného výrazu vyhodnoceny, je důležité. Například výsledek výrazu **1 + 4 / 2** se liší v závislosti na tom, zda se provádí nejprve sčítání nebo dělení. Pomocí závorek lze explicitně definovat způsob vyhodnocení výrazu. Chcete-li například uvést, že se sčítání musí provést jako první, můžete upravit předchozí výraz na **(1 + 4) / 2**. Pokud pořadí operací, které musí být provedeny ve výrazu, není explicitně definováno, pořadí vychází z výchozí priority přiřazené k podporovaným operátorům. V následující tabulce jsou operátory a priorita, která je k nim přiřazená. Operátory, které mají vyšší prioritu (například 7), jsou vyhodnoceny dříve než operátory s nižší prioritou (například 1).

| Priorita | Operátory      | Syntaxe                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Seskupení       | ( … )                                                    |
| 6          | Přístup členů  | … . …                                                    |
| 5          | Volání funkce  | … ( … )                                                  |
| 4          | Multiplikativní | … \* … … / …                                             |
| 3          | Přídavné       | … + … … - …                                              |
| 2          | Porovnání     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Dělení     | … , …                                                    |

Operátory na stejném řádku mají stejnou prioritu. Pokud výraz obsahuje více těchto operátorů, bude vyhodnocen zleva doprava. Například výraz **1 + 6 / 2 \* 3 &gt; 5** vrátí hodnotu **true**. Doporučujeme vám pomocí závorek explicitně určit požadované pořadí vyhodnocení výrazů, usnadní se tím čtení a správa výrazů.

#### <a name="references"></a>Odkazy

Všechny zdroje dat aktuální součásti elektronického výkaznictví (model nebo formát), které jsou k dispozici během návrhu výrazu, lze použít jako pojmenované odkazy. Například aktuální datový model elektronického výkaznictví obsahuje zdroj dat **ReportingDate**, který vrací hodnotu datového typu **DATETIME**. Pro správné formátování této hodnoty v generovaném dokumentu můžete odkazovat na zdroj dat následujícím způsobem: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")** Všechny znaky názvu odkazujícího zdroje dat, které nepředstavují písmeno abecedy, musí mít jako úvodní symbol jednoduchou uvozovku. Pokud název odkazujícího zdroje dat, který obsahuje alespoň jeden znak, který nepředstavuje písmeno abecedy (například interpunkční znaménka nebo jiné psané symboly), musí být v jednoduchých uvozovkách. Několik příkladů:

-   Na zdroj dat **Dnešní datum a čas** je nutné odkazovat ve výrazu elektronického výkaznictví následujícím způsobem: **'Dnešní datum a čas'**
-   Na metodu **name()** zdroje dat **Odběratelé** musí být odkazováno ve výrazu elektronického výkaznictví následujícím způsobem: **Odběratelé.'name()'**

Následující syntaxe se používá k volání metod datových zdrojů aplikace Dynamics 365 for Operations s parametry:

- Odkaz na metodu isLanguageRTL datového zdroje systému s parametrem datového typu řetězce EN-US musí být obsažen ve výrazu elektronického výkaznictví, a to takto: System.’isLanguageRTL’(“EN-US”).
- Pokud název metody obsahuje pouze alfanumerické znaky, nejsou uvozovky povinné. U metod tabulky, jejichž název obsahuje závorky, jsou uvozovky povinné.

Při přidání systémového datového zdroje do mapování elektronického výkaznictví, které odkazuje na globální třídu aplikace Dynamics 365 for Operations, výraz vrátí logickou hodnotu FALSE. Upravený výraz System.’ isLanguageRTL’(“AR”) vrátí logickou hodnotu TRUE.

Předávání parametrů těmto metodám lze definovat s následujícími omezeními:

- Těmto metodám lze předávat pouze konstanty, jejichž hodnota se určí v době návrhu.
- U těchto parametrů jsou podporovány pouze primitivní (základní) typy dat (celé číslo, reálné číslo, logická hodnota, řetězec a podobně).

#### <a name="path"></a>Cesta

Pokud výraz odkazuje na strukturovaný zdroj dat, můžete použít definici cesty k volbě určitého primitivního prvku daného zdroje dat. Znak tečky (.) se používá k oddělení jednotlivých prvků strukturovaného zdroje dat. Například aktuální datový model elektronického výkaznictví obsahuje zdroj dat **InvoiceTransactions**, který vrátí seznam záznamů. Struktura záznamu **InvoiceTransactions** obsahuje pole **AmountDebit** a **AmountCredit**, která vrací číselné hodnoty. Proto můžete vytvořit následující výraz pro výpočet fakturované částky: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funkce

Další část popisuje funkce, které lze použít ve výrazech elektronického výkaznictví. Všechny zdroje dat kontextu výrazu (aktuální datový model nebo formát elektronického výkaznictví) a také konstanty mohou sloužit jako parametry funkcí volání podle seznamu argumentů funkcí volání. Například aktuální datový model elektronického výkaznictví obsahuje zdroj dat **InvoiceTransactions**, který vrátí seznam záznamů. Struktura záznamu **InvoiceTransactions** obsahuje pole **AmountDebit** a **AmountCredit**, která vrací číselné hodnoty. Takže pokud chcete vypočítat částku, můžete vytvořit následující výraz využívající integrovanou funkci zaokrouhlování pro použití v elektronickém výkaznictví: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Podporované funkce
V následující tabulce jsou popsány funkce pro manipulaci s daty, které lze použít k vytváření datových modelů a sestav elektronického výkaznictví. Seznam funkcí není finální a může být vývojáři rozšířen. Chcete-li zobrazit seznam funkcí, které můžete použít, otevřete podokno funkcí v návrháři receptur elektronického výkaznictví.

### <a name="date-and-time-functions"></a>Funkce data a času

| Funkce                                   | Popis                                                                                                                                                                                                                                                                                                                                                      | Příklad                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (datum a čas, dny)                   | Přidá zadaný počet dní k zadané hodnotě data a času.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** vrátí datum a čas sedm dní v budoucnosti.                                                                                                                                                                                                                            |
| DATETODATETIME (datum)                      | Převede zadanou hodnotu data na hodnotu data a času.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. 'getCurrentDate()')** vrátí datum aktuální relace aplikace Finance and Operations, např. 24. 12. 2015, jako **12/24/2015 12:00:00 AM**. V tomto příkladu **CompInfo** představuje zdroj dat elektronického výkaznictví typu **Finance and Operations/Table**, který odkazuje na tabulku CompanyInfo. |
| NOW ()                                     | Vrátí aktuální datum a čas relace aplikačního serveru Finance and Operations jako hodnotu data a času.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Vrátí aktuální datum relace aplikačního serveru Finance and Operations jako hodnotu data.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Vrátí hodnotu data **null**.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Vrátí hodnotu data a času **null**.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (datum a čas, formát)          | Převede zadanou hodnotu data a času na řetězec v zadaném formátu. (Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** vrátí aktuální datum aplikačního serveru Finance and Operations, například 24. 12. 2015 jako **"24-12-2015"** podle zadaného vlastního formátu.                                                                                                          |
| DATETIMEFORMAT (datum a čas, jazyková verze) | Převede zadanou hodnotu data a času na řetězec v zadaném formátu [jazykové verzi](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informace o podporovaných formátech viz [standardní](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** vrátí aktuální datum aplikačního serveru Finance and Operations, například 24. 12. 2015, jako **"24.12.2015"**, podle vybraného německého prostředí.                                                                                                             |
| SESSIONTODAY ()                            | Vrátí aktuální datum relace aplikace Dynamics 365 for Finance and Operations jako hodnotu data.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Vrátí aktuální datum a čas relace aplikace Dynamics 365 for Finance and Operations jako hodnotu data a času.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (datum, formát)                  | Vrátí řetězcovou reprezentaci data v zadaném formátu.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** vrátí aktuální datum relace aplikace Dynamics 365 for Finance and Operations, například 24. 12. 2015, jako **"24-12-2015"** podle zadaného vlastního formátu.                                                                                                                      |
| DATEFORMAT (datum, formát, jazyková verze)         | Převede zadanou hodnotu data na řetězec v zadaném formátu [jazykové verzi](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informace o podporovaných formátech viz [standardní](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** vrátí aktuální datum relace aplikace Finance and Operations, například 24. 12. 2015, jako **"24.12.2015"**, podle vybraného německého prostředí.                                                                                                                       |
| DAYOFYEAR (datum)              | Vrátí celočíselnou reprezentaci počtu dní mezi 1. lednem a zadaným datem.       | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** vrátí **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** vrátí **1**. 
                                                                                                                      |

**Funkce převodu dat**

| Funkce                                   | popis                                                                                                                                                                                                                                                                                                                                                      | Příklad                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATETODATETIME (datum)                 | Převede zadanou hodnotu data na hodnotu data a času.           | **DATETODATETIME (CompInfo. 'getCurrentDate()')** vrátí datum aktuální relace aplikace Finance and Operations, např. 24. 12. 2015, jako **12/24/2015 12:00:00 AM**. V tomto příkladu **CompInfo** představuje zdroj dat elektronického výkaznictví typu **Finance and Operations/Table**, který odkazuje na tabulku **CompanyInfo**.                                                                                                                       |
| DATEVALUE (řetězec, formát)              | Vrátí reprezentaci data řetězce v zadaném formátu.       | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** vrátí datu, 21. 12. 2016 podle zadaného vlastního formátu a výchozího jazykového prostředí aplikace **EN-US**.                                                                                                                       |
| DATEVALUE (řetězec, formát, prostředí)              | Vrátí reprezentaci data řetězce v zadaném formátu a jazykové verzi.       | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", “IT”)** vrátí datum 21. 1. 2016 podle zadaného vlastního formátu a jazykové verze. Při volání této funkce **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", “EN-US”)** vznikne výjimka informující o tom, že zadaný řetězec není platným datem.                                                                                                                       |
| DATETIMEVALUE (řetězec, formát)              | Vrátí reprezentaci hodnoty data a času řetězce v zadaném formátu.       | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** vrátí čas 2:55:00 a datum 21. 12. 2016 podle zadaného vlastního formátu a výchozí jazykové verze aplikace **EN-US**.                                                                                                                       |
| DATETIMEVALUE (řetězec, formát, prostředí)              | Vrátí reprezentaci data a času řetězce v zadaném formátu a jazykové verzi.       | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", “IT”)** vrátí čas 2:55:00 a datum 21. 12. 2016 podle zadaného vlastního formátu a jazykové verze. Při volání této funkce **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", “EN-US”)** vznikne výjimka informující o tom, že zadaný řetězec není platným datem a časem.                                                                                                                       |
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
<td>V následujícím příkladu je zdroj dat <strong>Lines</strong> vytvořen jako seznamu tří záznamů, který je rozdělený na dávky, z nichž každá obsahuje až dva záznamy. 
<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> 

Zde je navržené rozvržení formátu, kde jsou vazby na zdroj dat <strong>Řádky</strong> vytvořeny s cílem vygenerovat výstup ve formátu XML, který poskytuje jednotlivé uzly pro každou dávku a obsažené záznamy. 
<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> 

Následuje výsledek spuštění navrženého formátu. 
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (záznam 1 [, záznam 2, ...])</td>
<td>Vrátí nový seznam, který je vytvořený na základě zadaných argumentů.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> vrátí prázdný záznam, kde seznam polí obsahuje všechna pole seznamů záznamů <strong>MainData</strong> a <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (seznam 1, seznam 2...)</td>
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
<td>Vrátí nový plochý seznam, který obsahuje všechny položky odpovídající zadané cestě. Cesta musí být definována jako platná cesta zdroje dat k prvku zdroje dat typu dat seznamu záznamů. Cesta k řetězci, datu atd. Datové prvky by měly zvýšit chybu v době návrhu v záznamu výrazů ER.</td>
<td>Zadáte-li <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> jako zdroj dat (DS), <strong>COUNT( ALLITEMS (DS.Value))</strong> vrátí <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (seznam [, výraz 1, výraz 2…])</td>
<td>Vrátí zadaný seznam seřazený podle zadaných argumentů, které lze definovat jako výrazy.</td>
<td>Jestliže je položka <strong>Vendor</strong> konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, <strong>ORDERBY (Vendors, Vendors.'name()')</strong> vrátí seznamu dodavatelů seřazených podle názvu ve vzestupném pořadí.</td>
</tr>
<tr class="even">
<td>REVERSE (seznam)</td>
<td>Vrátí zadaný seznam v obráceném pořadí.</td>
<td>Jestliže je položka <strong>Vendor</strong> konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> vrátí seznamu dodavatelů seřazených podle názvu v sestupném pořadí.</td>
</tr>
<tr class="odd">
<td>WHERE (seznam, podmínka)</td>
<td>Vrátí zadaný seznam, který je filtrován podle zadané podmínky. Na rozdíl od funkce <strong>FILTR</strong> je zadaná podmínka použita v seznamu v paměti.</td>
<td>Jestliže je položka <strong>Vendor</strong> konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> vrátí seznamu dodavatelů patřících do skupiny dodavatelů č. 40.</td>
</tr>
<tr class="even">
<td>ENUMERATE (seznam)</td>
<td>Vrátí nový seznam, který se skládá z výčtových záznamů zadaného seznamu a poskytne následující prvky:
<ul>
<li>Zadané záznamy seznamu jako běžné seznamy (součást <strong>hodnota</strong>)</li>
<li>Aktuální index záznamů (součást <strong>číslo</strong>)</li>
</ul></td>
<td>V následujícím příkladu je zdroj dat <strong>Enumerated</strong> vytvořen jako výčtový seznam záznamů dodavatelů ze zdroje dat <strong>Vendors</strong>, který odkazuje na tabulku <strong>VendTable</strong>. 
<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a> 

Zde je formát, kde jsou vazby dat vytvořeny k vygenerování výstupu ve formátu XML, který obsahuje jednotlivé dodavatele jako výčtové uzly. 
<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> 

Následuje výsledek spuštění navrženého formátu. 
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (seznam)</td>
<td>Vrátí počet záznamů v zadaném seznamu, pokud tento seznam není prázdný. V opačném případě vrátí hodnotu <strong>0</strong> (nula).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> vrátí <strong>2</strong>, protože funkce <strong>SPLIT</strong> vytvoří seznam, který se skládá ze dvou záznamů.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (cesta)</td>
<td>Zobrazí seznam záznamů vytvořený z argumentu jednoho z následujících typů:
<ul>
<li>Výčet modelu</li>
<li>Výčet formátu</li>
<li>Kontejner</li>
</ul>
Vytvořený seznam bude obsahovat záznamy s následujícími poli:
<ul>
<li>Jméno</li>
<li>Štítek</li>
<li>popis</li>
</ul>
Pole Popisek a Popis se vrátí hodnoty runtime založené na jazykovém nastavení formátu.</td>
<td>Následující příklad ukazuje výčet zavedený v datovém modelu. 
<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Následující příklad ukazuje:
<ul>
<li>Vyčíslení modelu vložené do sestavy jako zdroj dat.</li>
<li>Výraz ER určený k použití vyčíslení modelu jako parametr této funkce.</li>
<li>Zdroj dat typu záznamu vložený do sestavy pomocí vytvořeného výrazu elektronického výkaznictví.</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> 

Následující příklad uvádí prvky formátu ER, které jsou vázané na zdroj dat typu seznamu záznamů, který byl vytvořen pomocí funkce LISTOFFIELDS.
<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Toto je výsledek spuštění navrženého formátu.
<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>

Poznámka:</strong> Přeložený text štítků a popisy je zadáván do výstupu formátu ER v souladu s jazykovým nastavením nakonfigurovaným pro nadřízené prvky formátu FILE a FOLDER.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (seznam, název pole, oddělovač)</td>
<td>Vrátí řetězec zřetězených hodnot pole ze seznamu odděleném vybraným oddělovačem.</td>
<td>Pokud jste jako zdroj dat DS zadali výraz SPLIT(“abc” , 1), vrátí výraz STRINGJOIN (DS, DS.Value, “:”) hodnotu “a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (seznamu, hodnota limitu, zdroj limitu)</td>
<td>Rozdělí daný seznam na nový seznam podřízených seznamů a vrátí výsledek v obsahu seznamu záznamů. Parametr Hodnota limitu určuje hodnotu limitu k rozdělení seznamu původu. Parametr zdroje limitu určuje krok, o který se celkový součet zvýší. Limit nebude použito na jednu položku z daného seznamu, když zdrojový limit překročí definovaný limit.</td>
<td>V následujícím příkladu je uveden vzorový formát použití datových zdrojů. 
<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

To je výsledné provedení formátu, které představuje plošný seznam položek komodit.
<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Následující příklad uvádí stejný formát, který byl upraven tak, aby obsahoval seznam položek komodit v dávkách, kdy musí jedna dávka zahrnovat komodity s celkovou hmotností nepřekračující limit 9.
<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Toto je výsledek spuštění upraveného formátu. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

<strong>Poznámka:</strong> Limit není použit na poslední zboží v seznamu původu, protože hodnota (11) zdroje limitu (hmotnost) překračuje definovaný limit (9). Použijte funkci <strong>WHERE</strong> nebo výraz <strong>Enabled</strong> odpovídajícího prvku formátu k ignorování (přeskočení) dílčích seznamů během generování sestavy (pokud je třeba).</td>
</tr>
<tr class="odd">
<td>FILTER (seznam, podmínka)</td>
<td>Vrátí daný seznam filtrovaný pro zadanou podmínku změnou dotazu. Na rozdíl od funkce <strong>WHERE</strong> je zadaná podmínka použita na úrovni databáze u jakéhokoli zdroje dat elektronického výkaznictví u typů záznamy Tabulka.</td>
<td>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;) vrátí seznam pouze těch dodavatelů, kteří patří do skupiny dodavatelů “40”, když je <strong>dodavatel</strong> nakonfigurovaný jako zdroj dat elektronického výkaznictví odkazující na tabulku <strong>VendTable</strong>.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logické funkce

| Funkce                                                                                | popis                                                                                                                                                                                                                                                                     | Příklad                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (výraz, možnost 1, výsledek 1 \[, možnost 2, výsledek 2\] ... \[, výchozí výsledek\]) | Vyhodnotí zadanou hodnotu výrazu s ohledem na zadané alternativní možnosti. Vrátí se výsledek možnosti, která je rovna hodnotě výrazu. V opačném případě se vrátí volitelně zadaný výchozí výsledek (poslední parametr, který nepředchází dané možnosti). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** vrátí řetězec **"WINTER"**, jestliže je aktuální datum relace aplikace Finance and Operations mezi říjnem a prosincem. Jinak bude vrácen prázdný řetězec. |
| IF (podmínka, hodnota 1, hodnota 2)                                                        | Při splnění dané podmínky bude vrácena zadaná hodnota 1. V opačném případě vrátí hodnotu 2. Pokud hodnoty 1 a 2 jsou záznamy nebo seznamy záznamů, bude mít výsledek pouze pole, která existují v obou seznamech.                                                                     | **IF (1=2, "podmínka je splněna", "podmínka není splněna")** vrátí řetězec **"podmínka není splněna"**.                                                                                                                                                      |
| NOT (podmínka)                                                                         | Vrátí obrácenou logickou hodnotu zadané podmínky.                                                                                                                                                                                                                   | **NOT (TRUE)** vrátí **FALSE**.                                                                                                                                                                                                                            |
| AND (podmínka 1\[, podmínka 2, ...\])                                                 | Vrátí **TRUE**, pokud jsou *všechny* zadané podmínky pravda. V opačném případě vrátí hodnotu **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** vrátí **TRUE**. **AND (1=2, "a"="a")** vrátí **FALSE**.                                                                                                                                                                           |
| OR (podmínka 1\[, podmínka 2, ...\])                                                  | Vrátí **FALSE**, pokud jsou *všechny* zadané podmínky nepravda. Vrátí **TRUE**, pokud je *jakákoli* zadaná podmínka pravda.                                                                                                                                                                 | **OR (1=2, "a"="a")** vrátí **TRUE**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matematické funkce

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkce</th>
<th>Popis</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (číslo)</td>
<td>Vrátí absolutní hodnotu zadaného čísla (číslo bez znaménka).</td>
<td><strong>ABS (-1)</strong> vrátí hodnotu <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (číslo, mocnina)</td>
<td>Vrátí výsledek umocnění zadaného kladného čísla pomocí zadané mocniny.</td>
<td><strong>POWER (10, 2)</strong> vrátí hodnotu <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (řetězec, oddělovač desetinných míst, oddělovač skupin číslic)</td>
<td>Převede zadaný řetězec na číslo. Zadaný symbol se použije k oddělení celého čísla a zlomkových částí desetinného čísla a také se použije zadaný oddělovač tisíců.</td>
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot;, &quot; &quot;)</strong> vrátí hodnotu <strong>1234,56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (řetězec)</td>
<td>Převede zadaný řetězec na číslo. Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní pomlčka (-) se používá jako záporné znaménko. Pokud jsou v zadaném řetězci zjištěny jiné než číselné znaky, bude vyvolána výjimka.</td>
<td><strong>VALUE (&quot;1 234,56&quot;)</strong> vyvolá výjimku.</td>
</tr>
<tr class="odd">
<td>ROUND (číslo, desetinná čísla)</td>
<td>Vrátí zadané číslo, které je zaokrouhleno na zadaný počet desetinných míst:
<ul>
<li>Pokud je zadaná hodnota desetinných míst vyšší než 0 (nula), zadané číslo je zaokrouhleno na zadaný počet desetinných míst.</li>
<li>Pokud je zadaná hodnota desetinných míst 0 (nula), zadané číslo je zaokrouhleno na nejbližší celé číslo.</li>
<li>Pokud je zadaná hodnota desetinných míst nižší než 0 (nula), zadané číslo je zaokrouhleno vlevo od oddělovače desetinných míst.</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> zaokrouhlí na dvě desetinná místa a vrátí hodnotu <strong>1200.77</strong>. <strong>ROUND (1200.767, -3)</strong> zaokrouhlí na nejbližší násobek 1 000 a vrátí hodnotu <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (číslo, desetinná čísla)</td>
<td>Vrátí zadané číslo, které je zaokrouhleno dolů (směrem k nule) na zadaný počet desetinných míst. <strong>Poznámka:</strong> Tato funkce se chová jako <strong>ROUND</strong>, ale vždy zaokrouhluje na zadané číslo směrem dolů.</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> zaokrouhlí směrem dolů na dvě desetinná místa a vrátí hodnotu <strong>1200.76</strong>. <strong>ROUNDDOWN (1700.767, -3)</strong> zaokrouhlí směrem dolů na nejbližší násobek 1 000 a vrátí hodnotu <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (číslo, desetinná čísla)</td>
<td>Vrátí zadané číslo, které je zaokrouhleno nahoru (směrem od nuly) na zadaný počet desetinných míst. <strong>Poznámka:</strong> Tato funkce se chová jako <strong>ROUND</strong>, ale vždy zaokrouhluje na zadané číslo směrem nahoru.</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> zaokrouhlí směrem nahoru na dvě desetinná místa a vrátí hodnotu <strong>1200.77</strong>. <strong>ROUNDUP (1200.767, -3)</strong> zaokrouhlí směrem nahoru na nejbližší násobek 1 000 a vrátí hodnotu <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

**Funkce převodu dat**

| Funkce             | popis                                                                                                                                                                                                                                     | Příklad                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| VALUE (řetězec) | Převede zadaný řetězec na číslo. Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní spojovník (-) se používá jako záporné znaménko. Pokud jsou v zadaném řetězci zjištěny jiné než číselné znaky, dojde k chybě.                                                                                  | **VALUE ("1 234,56")** vyvolá výjimku.   |
| NUMBERVALUE (řetězec, oddělovač desetinných míst, oddělovač skupin číslic) | Převede zadaný řetězec na číslo. Zadaný symbol se použije k oddělení celého čísla a zlomkových částí desetinného čísla a také se použije zadaný oddělovač tisíců.                                                                                  | **NUMBERVALUE("1 234,56", ",", " ")** vrátí hodnotu **1234.56**.    |
| INTVALUE (řetězec) | Vrátí celočíselnou reprezentaci řetězce. Případné desetinné části budou zkráceny.                                                                                  | **INTVALUE ("100.77")** vrátí hodnotu **100**. |
| INTVALUE (číslo) | Vrátí celočíselnou reprezentaci čísla. Případné desetinné části budou zkráceny.                                                                                  | **INTVALUE (-100.77)** vrátí hodnotu **-100**. |
| INT64VALUE (řetězec) | Vrátí reprezentaci řetězce ve formátu int64. Případné desetinné části budou zkráceny.                                                                                  | **INT64VALUE (“22565422744”)** vrátí hodnotu **22565422744**. |
| INT64VALUE (číslo) | Vrátí reprezentaci čísla ve formátu int64. Případné desetinné části budou zkráceny.                                                                                  | **INT64VALUE (22565422744.00)** vrátí hodnotu **22565422744**. |



### <a name="record-functions"></a>Funkce záznamu

| Funkce             | popis                                                                                                                                                                                                                                     | Příklad                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (seznam) | Vrátí záznam **null**, který má stejnou strukturu jako zadaný seznam záznamů nebo záznam. **Poznámka:** Tato funkce je zastaralá. Místo toho použijte **EMPTYRECORD**.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí **SPLIT**. |
| EMPTYRECORD (záznam) | Vrátí záznam **null**, který má stejnou strukturu jako zadaný seznam záznamů nebo záznam. **Poznámka:** Záznam **null** je záznam, ve kterém mají všechna pole prázdnou hodnotu (**0** \[nula\] pro čísla, prázdný řetězec pro řetězce atd.). | **EMPTYRECORD (SPLIT ("abc", 1))** vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí **SPLIT**.   |

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
<th>Popis</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (řetězec)</td>
<td>Vrátí zadaný řetězec, který je převeden na velká písmena.</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> vrátí <strong>&quot;SAMPLE&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (řetězec)</td>
<td>Vrátí zadaný řetězec, který je převeden na malá písmena.</td>
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
<td><strong>CHAR (255)</strong> vrátí <strong>&quot;ÿ&quot;</strong>. <strong>Poznámka:</strong> vrácený řetězec závisí na kódování, které je vybráno v nadřazeném prvku formátu SOUBORU. Seznam podporovaných kódování lze najít v tématu <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Třída kódování</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (řetězec 1 [, řetězec 2…])</td>
<td>Vrátí všechny zadané textové řetězce, které jsou spojeny do jednoho řetězce.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> vrátí <strong>&quot;abcdef&quot;</strong>. <strong>Poznámka:</strong> Výraz <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> také vrátí <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (řetězec, vzor, náhrada)</td>
<td>Vrátí zadaný řetězec, v němž všechny výskyty znaků v zadaném řetězci vzoru jsou nahrazeny znaky na odpovídající pozici zadaného řetězce sloužícího jako náhrada.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> nahradí vzorec <strong>&quot;cd&quot;</strong> řetězcem <strong>&quot;GH&quot;</strong> a vrátí <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (řetězec, vzor, náhrada, příznak regulérního výrazu)</td>
<td>Pokud je zadaný příznak regulérního výrazu <strong>true</strong>, vrátí zadaní řetězec, který je upraven použitím regulárního výrazu zadaného jako argument vzoru pro tuto funkci. Tento výraz slouží k vyhledání znaků, které je třeba nahradit. Znaky zadaného argumentu-náhrady jsou použity k nahrazení vyhledaných znaků. Pokud je zadaný příznak regulérního výrazu <strong>false</strong>, tato funkce se chová jako <strong>TRANSLATE</strong>.</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> použije regulární výraz, ktreý odebere všechny nečíselné symboly a vrátí <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> nahradí vzorec <strong>&quot;cd&quot;</strong> řetězcem <strong>&quot;GH&quot;</strong> a vrátí <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (vstup)</td>
<td>Vrátí zadaný vstup, který je převeden na textový řetězec naformátovaný podle nastavení národního prostředí serveru aktuální instance aplikace Finance and Operations. Co se týká hodnot typu <strong>real</strong>, převod řetězce je omezen na dvě desetinná místa.</td>
<td>Jestliže je národní prostředí serveru Finance and Operations definováno jako <strong>EN-US</strong>, <strong>TEXT (NOW ())</strong> vrátí aktuální datum relace aplikace Finance and Operations, například 17. 12. 2015, jako textový řetězec <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> vrátí <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (řetězec 1 řetězce 2[, řetězec 3...])</td>
<td>Vrátí zadaný řetězec, který je formátován nahrazením všech výskytů <strong>%N</strong> <em>n</em>. argumentem. Argumenty jsou řetězce. Pokud pro parametr není zadán argument, parametr je vrácen jako <strong>&quot;%N&quot;</strong> v řetězci. Co se týká hodnot typu <strong>real</strong>, převod řetězce je omezen na dvě desetinná místa.</td>
<td>V tomto příkladu vrátí zdroj dat <strong>PaymentModel</strong> seznam záznamů odběratelů prostřednictvím součásti <strong>Customer</strong> a datum zpracování prostřednictvím pole <strong>ProcessingDate</strong>. 
<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> 

Ve formátu elektronického výkaznictví, který je určený ke generování elektronického souboru pro vybrané odběratele, je vybrán řetězec <strong>PaymentModel</strong> jako zdroj dat, který řídí procesní tok. Jestliže je vybraný odběratel zastaven u data zpracování sestavy, je vyvolána výjimka pro koncové uživatele. Vzorec, který je určen pro tento typ ovládacího prvku pro zpracování, může využít následující zdroje:
<ul>
<li>Popisek aplikace Finance and Operations SYS70894, který má následující text:
<ul>
<li><strong>Pro jazyk EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Pro jazyk CS:</strong> &quot;Nic k vytištění&quot;</li>
</ul></li>
<li>Popisek aplikace Finance and Operations SYS18389, který má následující text:
<ul>
<li><strong>Pro jazyk EN-US:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Pro jazyk DE:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Zde je vzorec, který lze vytvořit: FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)) Pokud je sestava zpracovávána pro <strong>maloobchodního odběratele Litware</strong> 17. prosince 2015 v národním prostředí <strong>EN-US</strong> a jazyce <strong>EN-US</strong> tento vzorec vrátí následující text, který může být koncovému uživateli nabídnut ve formě zprávy výjimky: &quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot; Jestliže je stejná sestava zpracována pro <strong>maloobchodního odběratele Litware</strong> 17. 12. 2015 v jazykové verzi <strong>DE</strong> a jazyce <strong>DE</strong>, tento vzorec vrátí následující text, který používá jiný formát data: &quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Poznámka:</strong> Následující syntaxe se ve vzorcích ER používá pro popisky:
<ul>
<li><strong>Popisky ze zdrojů aplikace Finance and Operations:</strong> <strong>@&quot;X&quot;</strong>, kde X je ID popisku ve stromu aplikačních objektů (AOT)</li>
<li><strong>Popisky, které se nachází v konfiguracích elektronického výkaznictví:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, kde X je ID popisku v konfiguraci elektronického výkaznictví.</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (číslo, formát)</td>
<td>Vrátí znázornění řetězce zadaného čísla v zadaném formátu. (Informace o podporovaných formátech naleznete v tématu <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standardní</a> a <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">vlastní</a>.) Spuštění této funkce v rámci určuje jazykovou verzi, která je použita k formátování čísla.</td>
<td>Pro jazykovou verzi EN-US vrátí <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> hodnotu <strong>&quot;45,00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> vrátí hodnotu <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (číslo jazyk, měna, příznak názvu měny pro tisk, desetinná místa)</td>
<td>Vrátí vyslovené číslo převedené na textové řetězců definovaného jazyka. Kód jazyka je volitelný: Pokud je definován jako prázdný řetězec, bude použit spuštěný kód jazyka kontextu (definovaný pro generování souboru nebo složky). Zadaný kód měny je volitelný. Pokud je definován jako prázdný řetězec, je převzata měna společnosti. Všimněte si, že parametr <strong>Název měny pro tisk</strong> a parametr <strong>Desetinná místa</strong> jsou analyzovány pouze pro tyto kódy jazyka: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Parametr <strong>Název měny pro tisk</strong> je analyzován pouze pro společnosti používající aplikaci Finance and Operations s kontextem země, který podporuje kolísání měny.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2) vrátí “One Thousand Two Hundred Thirty Four and 56” NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) vrátí “Sto dwadzieścia” NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) returns “Сто двадцать евро 21 евроцент”</td>
</tr>
<tr class="odd">
<td>PADLEFT (řetězec, délka, odsazovací znaky)</td>
<td>Vrátí řetězec určené délky, ve kterém je začátek aktuálního řetězce odsazen určenými znaky.</td>
<td>PADLEFT (“1234”, 10, “ “) vrátí textový řetězec “      1234”</td>
</tr>
<tr class="even">
<td>TRIM (řetězec)</td>
<td>Vrátí daný text po zkrácení o mezery na začátku a na konci a po odstranění vícenásobných mezer mezi slovy na jednu mezeru. </td>
<td><strong>TRIM ("     Ukázkový     text     ")</strong> vrátí hodnotu <strong>"Ukázkový text".</strong></td>
</tr>
<tr class="odd">
<td>GETENUMVALUEBYNAME (cesta zdroje dat výčtu, text popisku hodnoty výčtu)</td>
<td>Vrátí hodnotu zadaného zdroje dat výčtu podle zadaného textu tohoto popisku výčtu.</td>
<td>Následující příklad ukazuje výčet ReportDirection zavedený v datovém modelu. Pro hodnoty výčtu jsou definovány popisky.
Následující příklady ukazují:
<ul><li>Výčet modelu <strong>ReportDirection</strong> vložený do sestavy jako zdroj dat <strong>$Direction</strong>.</li>
<li>Výraz elektronického výkaznictví <strong>$IsArrivals</strong> nastavený na použití výčtu modelu jako parametru této funkce. Hodnota tohoto výrazu je <strong>TRUE</strong>.</li></ul></td>
</tr>
</tbody>
</table>

**Funkce převodu dat**

| Funkce             | popis                                                                                                                                                                                                                                     | Příklad                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| TEXT (vstup) | Vrátí zadaný vstup, který je převeden na textový řetězec naformátovaný podle nastavení národního prostředí serveru aktuální instance aplikace Finance and Operations.
Co se týká hodnot typu real, převod řetězce je omezen na dvě desetinná místa.| Jestliže je národní prostředí serveru Finance and Operations definováno jako **EN-US, TEXT (NOW ())**, vrátí se aktuální datum relace aplikace Finance and Operations, například 17. 12. 2015, jako textový řetězec **"12/17/2015 07:59:23 AM"**.
**TEXT (1/3) vrátí hodnotu "0.33"**. |
| QRCODE (řetězec) | Vrací obrázek QR kódu v binárním formátu base64 pro daný řetězec. | **QRCODE (“Ukázkový text”)** vrátí hodnotu **U2FtcGxlIHRleHQ=**.   |

### <a name="data-collection-functions"></a>Funkce shromažďování dat

| Funkce             | popis                                                                                                                                                                                                                                     | Příklad                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATELEMENTNAME () | Vrátí název elementu aktuálního formátu. Vrací prázdný řetězec, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut.| Další informace o použití těchto funkcí najdete v části **Elektronické výkaznictví - zdroj dat formát výstupu pro inventuru a souhrn** (část obchodního procesu **Získání/vývoj komponent služby/řešení** Průvodce záznamem úloh. |
| SUMIFS (key string for summing, criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) |Vrátí součet hodnot uzlů (s názvem definovaným jako klíčem) XML získaným během provedení tohoto formátu, který splňuje zadané podmínky (dvojice rozsah a hodnota). Vrací nulovou hodnotu, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut. |            |
| SUMIF (řetězec klíče pro sčítání, řetězec kritéria rozsahu, řetězec kritéria hodnoty) | Vrátí součet hodnot uzlů (s názvem definovaným jako klíčem) XML získaným během provedení tohoto formátu, který splňuje zadanou podmínku (rozsah a hodnota). Vrací nulovou hodnotu, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut.|           |
| COUNTIFS (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | Vrátí počet uzlů (s názvem definovaným jako klíčem) XML získaným během provedení tohoto formátu, který splňuje zadané podmínky. Vrací nulovou hodnotu, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut.|     |
| COUNTIF (řetězec rozsahu kritérií, řetězec hodnoty kritérií) | Vrátí počet uzlů XML získaný během provedení tohoto formátu, který splňuje zadanou podmínku (rozsah a hodnota). Vrací nulovou hodnotu, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut.|          |
| COLLECTEDLIST (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | Vrátí počet hodnot uzlů XML získaný během provedení tohoto formátu, který splňuje zadané podmínky. Vrací prázdný seznam, když je příznak **Podrobnosti výstupu shromažďování** aktuálních souborů vypnut.|               |   




### <a name="other-business-domainspecific-functions"></a>Další funkce (konkrétní pro obchodní domény)

| Funkce                                                                         | popis                                                                                                                                                                                                                                                        | Příklad                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (částka, zdrojová měna, cílová měna, datum, společnost)        | Převede zadanou peněžní částku ze zdrojové měny na cílovou měnu za použití nastavení zadané společnosti v aplikaci Finance and Operations k zadanému datu.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** vrátí ekvivalent jednoho eura v amerických dolarech v aktuální den relace podle nastavení společnosti DEMF.                                                                                                                                  |
| ROUNDAMOUNT (číslo, desetinná místa, pravidlo zaokrouhlování)                                       | Zaokrouhlí zadanou částku podle zadaného pravidla zaokrouhlování a zadaného počtu desetinných míst. **Poznámka:** Pravidlo zaokrouhlování musí být zadáno jako hodnota výčtu **RoundOffType** aplikace Finance and Operations.                          | Pokud je parametr **model.RoundOff** nastaven na ****Downward****, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** vrátí hodnotu **1000.78**. Pokud je parametr **model.RoundOff** nastaven na hodnotu **Normal** nebo **Rounding-up**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** vrátí hodnotu **1000.79**. |
| CURCredRef (číslice)                                                              | Vrátí referenční údaj věřitele na základě číslic zadaného čísla faktury.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** vrátí hodnotu **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (číslice)                                                                 | Vrátí referenční údaj věřitele jako výraz MOD97 na základě číslic zadaného čísla faktury.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** vrátí **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (číslice)                                                              | Vrátí referenční údaj ISO věřitele na základě číslic a abecedních symbolů zadaného čísla faktury. **Poznámka:** Chcete-li vyloučit z abecedy symboly, které jsou v souladu se standardem ISO, vstupní parametr musí být přeložen před jeho předáním této funkci. | **ISOCredRef ("VEND-200002")** vrátí hodnotu **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (řetězec, číslo)                                  | Získá ID další finanční dimenze. Dimenze reprezentují v tomto řetězci ID oddělená čárkou. Čísla definují požadovaný kód číselné řady dimenze v tomto řetězci.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) vrátí “CC”                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Vrací textovou reprezentaci kódu právnické osoby (společnosti), ke které je uživatel momentálně přihlášen.                                                                                                                                                                                                                    | **GETCURRENTCOMPANY ()** vrátí hodnotu **USMF** u uživatele přihlášeného v aplikaci Finance and Operations ke společnosti **Contoso Entertainment System USA**.                                                                                                                                                                                                                                                                                                              |
| CH\_BANK\_MOD\_10 (číslice)                                                       | Vrátí referenční údaj věřitele jako výraz MOD10 na základě číslic daného čísla faktury.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") vrátí 3                                                                                                                                                                                                                                                                   |
| FA\_SUM (kód dlouhodobého majetku, kód modelu hodnoty, počáteční datum, koncové datum)               | Vrátí připravený datový kontejner částek dlouhodobého majetku za období.                                                                                                                                                                                         | FA\_SUM ("COMP-000001", “Current”, Date1, Date2) vrátí připravený datový kontejner dlouhodobého majetku "COMP-000001" s modelem hodnoty “Current” pro období mezi Date1 a Date2.                                                                                                                        |
| FA\_BALANCE (kód dlouhodobého majetku, kód oceňovacího modelu, vykazovaný rok, datum sestavy) | Vrátí připravený datový kontejner zůstatků dlouhodobého majetku. Rok vykazování je nutné zadat jako hodnotu výčtu aplikace Finance and Operations **AssetYear**.                                                                                           | FA\_SUM ("COMP-000001", “Current”, AxEnumAssetYear.ThisYear, SESSIONTODAY ()) vrátí připravený datový kontejner zůstatků pro dlouhodobý majetek "COMP-000001" s modelem hodnoty “Current” k aktuálnímu datu relace aplikace 365 for Finance and Operations.                                                                |
| TABLENAME2ID (řetězec)                                                       | Vrací reprezentaci celého čísla ID tabulky pro daný název tabulky.                                                                                                                                                                      | **TABLENAME2ID ("Intrastat")** vrátí hodnotu **1510**.                                                                                                                                                                                                                                                                   |
| ISVALIDCHARACTERISO7064 (řetězec)                                                       | Vrátí logickou hodnotu **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN). Jinak vrátí logickou hodnotu **FALSE**.                                                                                                                                                                      | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** vrátí hodnotu **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** vrátí hodnotu **FALSE**.                                                                                                                                                                                                                                                                   |

### <a name="functions-list-extension"></a>Rozšíření seznamu funkcí

Elektronické výkaznictví umožňuje rozšířit seznam funkcí, které se používají ve výrazech elektronického výkaznictví. Je však vyžadována určitá technická zdatnost. Další informace naleznete v tématu [Rozšíření seznamu funkcí elektronického vykazování](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Viz také
--------

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Rozšíření seznamu funkcí elektronického vykazování](general-electronic-reporting-formulas-list-extension.md)




