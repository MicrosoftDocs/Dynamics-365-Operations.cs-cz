---
title: Kurz pro Regression Suite Automation Tool
description: Tento článek ukazuje, jak používat Regression Suite Automation Tool (RSAT). Popisuje různé funkce a poskytuje příklady, které používají pokročilé skriptování.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277397"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Kurz pro nástroj Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Pomocí nástrojů internetového prohlížeče můžete tuto stránku stáhnout a uložit ve formátu PDF.

Tento kurz prochází některými rozšířenými funkcemi nástroje Regression Suite Automation Tool (RSAT), zahrnuje přiřazení ukázky a popisuje strategii a klíčové body učení.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Významné funkce RSAT a Záznamník úloh

### <a name="validate-a-field-value"></a>Ověření hodnoty pole

Nástroje RSAT umožňují do testovacího případu zahrnout kroky ověření pro ověření očekávaných hodnot. Další informace o této funkci naleznete v článku [Ověření očekávaných hodnot](rsat-validate-expected.md).

V následujícím příkladu je ukázáno, jak lze pomocí této funkce ověřit, zda je množství na skladě větší než 0 (nula).

1. V ukázkových datech společnosti **USMF** vytvořte záznam úloh, který má následující kroky:

    1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
    2. Použijte rychlý filtr pro hledání záznamů. Například filtrujte na hodnotě **1000** pole **Číslo položky**.
    3. Vyberte **Zásoby na skladě**.
    4. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat na hodnotě **1** pro pole **Pracoviště**.
    5. Označte na seznamu vybraný řádek.
    6. Ověřte, zda hodnota pole **Celkem k dispozici** je **411.0000000000000000**.

2. Uložte záznam úlohy jako **nahrávku vývojáře** a připojte jej k testovacímu případu v Azure DevOps.
3. Přidejte testovací případ do testovacího plánu a načtěte testovací případ do RSAT.
4. Otevřete soubor parametrů Excel a přejděte na kartu **Kroky TestCase**.
5. Pro ověření, zda bude množství na skladě vždy vyšší než **0**, přejděte na krok **Ověřit dostupný celkový počet** a změňte jeho hodnotu z **411** na **0**. Změňte hodnotu pole **Operátor** ze znaku rovná se (**=**) na znak je větší než (**\>**).
6. Uložte a zavřete soubor parametrů aplikace Excel.
7. Vyberte **Odeslat** pro uložení provedených změn souboru parametrů aplikace Excel do Azure DevOps.

Nyní, pokud je hodnota pole **Celkem k dispozici** pro určitou položku ve skladu větší než 0 (nula), testy budou úspěšné, bez ohledu na skutečnou hodnotu zásob na skladě.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Uložené proměnné a zřetězení testovacích případů

Jednou z klíčových funkcí nástroje RSAT je zřetězení testovacích případů, tj. schopnost testu předat hodnoty jiným testům. Další informace naleznete v článku [Kopie proměnných pro zřetězení testovacích případů](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Odvozený testovací případ

RSAT umožňuje používat stejný Záznam úloh s více testovacími případy, který umožňuje spuštění úlohy s různými konfiguracemi dat. Další informace naleznete v článku [Odvozené testovací případy](rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Ověřit oznámení a zprávy

Tuto funkci lze použít k ověření, zda došlo k akci. Je-li například vytvořena, odhadnuta a následně zahájena výrobní zakázka, aplikace zobrazí zprávu „Výroba - Zahájení“ a upozorní vás, že výrobní zakázka byla zahájena.

![Oznámení Výroba – Zahájení.](./media/use_rsa_tool_05.png)

Tuto zprávu můžete ověřit prostřednictvím RSAT zadáním textu zprávy na kartě **Ověření zprávy** souboru parametrů aplikace Excel pro příslušný záznam.

![Karta Ověření zprávy.](./media/use_rsa_tool_06.png)

Po spuštění testovacího případu se zpráva v souboru parametrů aplikace Excel porovná se zprávou zobrazenou. Pokud se zprávy neshodují, testovací případ se nezdaří.

> [!NOTE]
> Na kartě **Ověření zprávy** v souboru parametrů aplikace Excel můžete zadat více než jednu zprávu. Zprávy mohou být také chybové nebo varovné namísto informačních zpráv.

### <a name="snapshot"></a>Snímek

Tato funkce pořídí snímky obrazovek kroků, které byly provedeny při záznamu úloh. Je užitečný pro účely auditu nebo ladění.

- Chcete-li použít tuto funkci v době, kdy je spuštěno RSAT s uživatelským rozhraním, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Chcete-li použít tuto funkci v době, kdy je spuštěno RSAT prostřednictvím příkazového řádku (například Azure DevOps), otevřete soubor **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Když spustíte testovací případy, RSAT generuje snímky (obrázky) kroků a uloží je ve složce přehrávání v testovacích případech v pracovním adresáři. Ve složce pro přehrávání je vytvořena samostatná podsložka s názvem **StepSnapshots**. Tato složka obsahuje snímky pro spuštěné testovací případy.

## <a name="assignment"></a>Přiřazení

### <a name="scenario"></a>Scénář

1. Návrhář produktu vytvoří nový uvolněný produkt.
2. Vedoucí výroby iniciuje výrobní zakázku za účelem zvýšení zásob na dva kusy.
3. Výroba zahájí a ukončí výrobní zakázku a ověří, že množství na skladě jsou dva kusy.
4. Prodejní tým obdrží objednávku na čtyři kusy nového produktu. Prodejní tým proto aktualizuje čisté požadavky prostřednictvím dynamického plánu. Vzhledem k tomu, že žádná další kapacita není k dispozici, je výchozí zásada objednávky nastavena na hodnotu „koupit místo vyrobit“. Proto se vytvoří plánovaná nákupní objednávka.
5. Kupující přidá dodavatele, podepíše plánovanou nákupní objednávku a poté potvrdí nákupní objednávku.
6. Po doručení zakoupeného zboží do skladu vyhledá operátor skladu související nákupní objednávku a přijme zboží. Vzhledem k tomu, že objednávka je nyní dokončena, lze zboží vydat a zabalit proti prodejní objednávce.
7. Finance zaúčtují nákupní fakturu a prodejní fakturu.

Následující ilustrace znázorňuje tok pro tento scénář.

![Tok ukázkového scénáře.](./media/use_rsa_tool_14.png)

Na následujícím obrázku je znázorněna hierarchie obchodních procesů pro tento scénář v modulu pro Modelování obchodních procesů LCS.

![Obchodní procesy pro ukázkový scénář.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategie – klíčové učení

### <a name="data"></a>Údaje

- Ujistěte se, že máte reprezentativní datové objemy (kopie dat produkční/zlaté konfigurace a přenesená data).
- Když generujete nová data pomocí záznamníku úloh, vytvořte názvy testů, které nekolidují s existujícími názvy (například použijte předponu **RSATxxx**).
- Použijte obnovení k určitému bodu v čase Azure- pro opětovné spuštění testů v prostředích, které nejsou v úrovni 1.
- Ačkoli můžete použít funkce Excelu **RANDOM** a **NOW** k vygenerování jedinečné kombinace, úsilí je poměrně vysoké. Následuje příklad.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Záznamník úkolů

- Definujte scénáře před zahájením záznamu. Dobře spravovaný projekt má předdefinované scénáře testování. Chcete-li vytvořit testovací případ, zvažte, jak předvídatelné výsledky těchto testů jsou.
- Záznamy rozdělte, pokud je provedete různými rolemi, nebo pokud se před dalším krokem vyskytl čas čekání nebo externí událost.
- Vyhněte se výběru hodnot v seznamech. Místo toho použijte textové formáty, jako například **FIFO**, **AudioRM** a **SiteWH**. Vyberete-li možnost v seznamu, bude zaznamenána pozice hodnoty v seznamu, nikoli hodnota samotná. Pokud jsou do seznamu přidány položky, bude možné změnit pozici hodnoty. Proto bude nahrávka používat jiný parametr a může to mít vliv na zbytek scénáře.
- Zamyslete se nad chováním více uživatelů. Nepředpokládejte například, že nově vytvořená prodejní objednávka bude vždy vybrána automaticky. Místo toho vždy použijte ke zjištění správné objednávky filtr.
- Použijte funkci kopírování v záznamníku úloh pro uložení názvu nově vytvořeného produktu, aby jej bylo možné použít ve zřetězených testovacích případech.
- Použijte funkci ověření v záznamníku úloh pro nastavení kontrolních bodů, které ověřují, zda byly provedeny správné kroky.

### <a name="rsat"></a>RSAT

- Chcete-li spustit test v jiné společnosti, můžete změnit společnost na kartě **Obecné** v souboru parametrů aplikace Excel. Zkontrolujte, zda jsou v nově vybrané společnosti k dispozici nastavení a data.
- Testovacího uživatele můžete změnit na kartě **Obecné** v souboru parametrů aplikace Excel. Zadejte ID e-mailu uživatele, který spustí testovací případ. Tímto způsobem lze testovací případ spustit pomocí oprávnění zabezpečení zadaného uživatele.
- Chcete-li počkat před zahájením testu, můžete na kartě **Obecné** v souboru parametrů aplikace Excel definovat pauzu. Toto pozastavení lze použít v dávkové úloze (například v případě, že je nutné spustit workflow ještě před provedením dalšího kroku).

## <a name="advanced-scripting"></a>Pokročilé skriptování

### <a name="cli"></a>CLI

RSAT lze volat z okna **Příkazového řádku** nebo **PowerShell**.

> [!NOTE]
> Ověřte, zda je proměnná prostředí **TestRoot** nastavena na cestu instalace RSAT. (V Microsoft Windows otevřete **Ovládací panel**, vyberte **Systém a zabezpečení \> Systém \> Pokročilá nastavení systému** a pak zvolte **Proměnné prostředí**.)

1. Otevřete okno **příkazového řádku** nebo **PowerShell** jako správce.
2. Přejděte do instalačního adresáře RSAT.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Vyvolejte seznam všech příkazů.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Zobrazí seznam všech příkazů nebo zobrazí nápovědu pro konkrétní příkaz spolu s dostupnými parametry.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Volitelné parametry

`command`: Část ``[command]`` je jedním z příkazů v předchozím seznamu.

#### <a name="about"></a>about

Zobrazí verzi instalovaného RSAT.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Vymaže obrazovku.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>download

Stáhne přílohy (soubory nahrávek, provádění a parametrů) pro zadaný testovací případ z Azure DevOps do výstupního adresáře. Příkazem ``list`` získáte všechny dostupné testovací případy a libovolnou hodnotu z prvního sloupce pak můžete použít jako parametr **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces stahování počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.

##### <a name="download-required-parameters"></a>download: požadované parametry

+ `test_case_id`: Představuje ID testovacího případu.

##### <a name="download-optional-parameters"></a>download: volitelné parametry

+ `output_dir`: Představuje výstupní pracovní adresář. Adresář musí existovat. Pokud tento parametr není zadán, použije se pracovní adresář z nastavení.

##### <a name="download-examples"></a>download: příklady

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Stáhne přílohy (soubory nahrávek, provádění a parametrů) pro všechny testovací případy v zadané testovací sadě z Azure DevOps do výstupního adresáře. Příkazem ``listtestsuitenames`` získáte všechny dostupné testovací sady a libovolnou hodnotu pak můžete použít jako parametr **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces stahování počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/byid`: Tento přepínač označuje, že požadovaná testovací sada je identifikována pomocí ID Azure DevOps, nikoli názvem testovací sady.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: požadované parametry

+ `test_suite_name`: Představuje název testovací sady. Tento parametr je povinný, pokud přepínač /byid **není** zadán. Tento název je názvem testovací sady Azure DevOps.
+ `test_suite_id`: Představuje ID testovací sady. Tento parametr je povinný, pokud přepínač /byid **je** zadán. Toto ID je ID testovací sady Azure DevOps.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: volitelné parametry

+ `output_dir`: Představuje výstupní pracovní adresář. Adresář musí existovat. Pokud tento parametr není zadán, použije se pracovní adresář z nastavení.

##### <a name="downloadsuite-examples"></a>downloadsuite: příklady

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>edit

Umožňuje otevřít soubor parametrů v aplikaci Excel a upravit jej.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: povinné parametry

+ `excel_file`: Musí obsahovat úplnou cestu k existujícímu souboru aplikace Excel.

##### <a name="edit-examples"></a>edit: příklady

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Generuje spuštění testu a soubory parametrů pro zadaný testovací případ v výstupním adresáři. Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy. Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces generování počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/dllonly`: Generovat pouze spouštěcí soubory testu. Soubor Excelu s parametry znovu negeneruje.
+ `/keepcustomexcel`: Aktualizace existujícího souboru parametrů. Také znovu generuje spouštěcí soubory.

##### <a name="generate-required-parameters"></a>generate: požadované parametry

+ `test_case_id`: Představuje ID testovacího případu.

##### <a name="generate-optional-parameters"></a>generate: volitelné parametry

+ `output_dir`: Představuje výstupní pracovní adresář. Adresář musí existovat. Pokud tento parametr není zadán, použije se pracovní adresář z nastavení.

##### <a name="generate-examples"></a>generate: příklady

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Generuje nový odvozený (podřízený) testovací případ zadaného testovacího případu. Nový testovací případ se také přidá do zadané testovací sady. Příkazem ``list`` získáte všechny dostupné testovací případy a libovolnou hodnotu z prvního sloupce pak můžete použít jako parametr **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces generování počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.

##### <a name="generatederived-required-parameters"></a>generatederived: požadované parametry

+ `parent_test_case_id`: Představuje ID nadřazeného testovacího případu.
+ `test_plan_id`: Představuje ID testovacího plánu.
+ `test_suite_id`: Představuje ID testovací sady.

##### <a name="generatederived-examples"></a>generatederived: příklady

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Generuje pouze spouštěcí soubory testu pro zadaný testovací případ. Negeneruje znovu soubor Excelu s parametry. Soubory jsou generovány v určeném výstupním adresáři. Příkazem ``list`` získáte všechny dostupné testovací případy a libovolnou hodnotu z prvního sloupce pak můžete použít jako parametr **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces generování počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: požadované parametry

+ `test_case_id`: Představuje ID testovacího případu.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: volitelné parametry

+ `output_dir`: Představuje výstupní pracovní adresář. Adresář musí existovat. Pokud tento parametr není zadán, použije se pracovní adresář z nastavení.

##### <a name="generatetestonly-examples"></a>generatetestonly: příklady

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Generuje všechny soubory pro automatizaci testů pro všechny testovací případy v zadané testovací sadě. Příkazem ``listtestsuitenames`` získáte všechny dostupné testovací sady a libovolnou hodnotu pak můžete použít jako parametr **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces generování počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/dllonly`: Generovat pouze spouštěcí soubory testu. Soubor Excelu s parametry znovu negeneruje.
+ `/keepcustomexcel`: Aktualizace existujícího souboru parametrů. Také znovu generuje spouštěcí soubory.
+ `/byid`: Tento přepínač označuje, že požadovaná testovací sada je identifikována pomocí ID Azure DevOps, nikoli názvem testovací sady.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: požadované parametry

+ `test_suite_name`: Představuje název testovací sady. Tento parametr je povinný, pokud přepínač /byid **není** zadán. Tento název je názvem testovací sady Azure DevOps.
+ `test_suite_id`: Představuje ID testovací sady. Tento parametr je povinný, pokud přepínač /byid **je** zadán. Toto ID je ID testovací sady Azure DevOps.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: volitelné parametry

+ `output_dir`: Představuje výstupní pracovní adresář. Adresář musí existovat. Pokud tento parametr není zadán, použije se pracovní adresář z nastavení.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: příklady

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>help

Totožný s [?](#section) příkaz.

#### <a name="list"></a>list

Vypíše seznam všech dostupných testovacích případů v aktuálním plánu testování.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Obsahuje seznam všech dostupných testovacích plánů.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Uvádí seznam testovacích případů pro zadanou testovací sadu. Příkazem ``listtestsuitenames`` získáte všechny dostupné testovací sady a libovolnou hodnotu ze seznamu pak můžete použít jako parametr **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: požadované parametry

+ `test_suite_name`: Název požadované sady.

##### <a name="listtestsuite-examples"></a>listtestsuite: příklady

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Uvádí seznam testovacích případů pro zadanou testovací sadu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: požadované parametry

+ `test_suite_id`: ID požadované sady.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: příklady

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Vypíše seznam všech dostupných testovacích sad v aktuálním plánu testování.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Přehraje testovací případ, který je přidružen k zadanému souboru parametrů aplikace Excel. Tento příkaz používá existující místní soubory automatizace a nestahuje soubory z Azure DevOps. Tento příkaz není podporován u testovacích případů pokladního místa POS.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces přehrávání počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/comments[="comment"]`: Zadejte vlastní informační řetězec, který bude přidán do pole **Komentáře** na stránkách souhrnu a výsledků testu pro spuštění testovacích případů Azure DevOps.

##### <a name="playback-required-parameters"></a>playback: požadované parametry

+ `excel_parameter_file`: Úplná cesta k souboru parametrů aplikace Excel. Soubor musí existovat.

##### <a name="playback-examples"></a>playback: příklady

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Přehrává se více testovacích případů najednou. Testovací případy jsou identifikovány podle jejich ID. Tento příkaz stáhne soubory z Azure DevOps. Příkazem ``list`` získáte všechny dostupné testovací případy a libovolnou hodnotu z prvního sloupce pak můžete použít jako parametr **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces přehrávání počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/comments[="comment"]`: Zadejte vlastní informační řetězec, který bude přidán do pole **Komentáře** na stránkách souhrnu a výsledků testu pro spuštění testovacích případů Azure DevOps.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: požadované parametry

+ `test_case_id1`: ID existujícího testovacího případu.
+ `test_case_id2`: ID existujícího testovacího případu.
+ `test_case_idN`: ID existujícího testovacího případu.

##### <a name="playbackbyid-examples"></a>playbackbyid: příklady

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Přehrává se více testovacích případů najednou. Testovací případy jsou identifikovány podle souborů parametrů aplikace Excel. Tento příkaz používá existující místní soubory automatizace a nestahuje soubory z Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces přehrávání počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/comments[="comment"]`: Zadejte vlastní informační řetězec, který bude přidán do pole **Komentáře** na stránkách souhrnu a výsledků testu pro spuštění testovacích případů Azure DevOps.

##### <a name="playbackmany-required-parameters"></a>playbackmany: požadované parametry

+ `excel_parameter_file1`: Úplná cesta k souboru parametrů aplikace Excel. Soubor musí existovat.
+ `excel_parameter_file2`: Úplná cesta k souboru parametrů aplikace Excel. Soubor musí existovat.
+ `excel_parameter_fileN`: Úplná cesta k souboru parametrů aplikace Excel. Soubor musí existovat.

##### <a name="playbackmany-examples"></a>playbackmany: příklady

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Přehraje všechny testovací případy z jedné či více zadaných testovacích sad. Pokud je zadán přepínač /local, budou pro přehrávání použity místní přílohy. V opačném případě budou přílohy staženy z Azure DevOps. Příkazem ``listtestsuitenames`` získáte všechny dostupné testovací sady a libovolnou hodnotu z prvního sloupce pak můžete použít jako parametr **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: volitelné přepínače

+ `/updatedriver`: Je-li zadán tento přepínač, bude webový ovladač internetového prohlížeče podle potřeby aktualizován před spuštěním procesu přehrávání.
+ `/local`: Tento přepínač označuje, že pro přehrávání by se měly používat místní přílohy místo stahování souborů z Azure DevOps.
+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces přehrávání počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/comments[="comment"]`: Zadejte vlastní informační řetězec, který bude přidán do pole **Komentáře** na stránkách souhrnu a výsledků testu pro spuštění testovacích případů Azure DevOps.
+ `/byid`: Tento přepínač označuje, že požadovaná testovací sada je identifikována pomocí ID Azure DevOps, nikoli názvem testovací sady.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: požadované parametry

+ `test_suite_name1`: Představuje název testovací sady. Tento parametr je povinný, pokud přepínač /byid **není** zadán. Tento název je názvem testovací sady Azure DevOps.
+ `test_suite_nameN`: Představuje název testovací sady. Tento parametr je povinný, pokud přepínač /byid **není** zadán. Tento název je názvem testovací sady Azure DevOps.
+ `test_suite_id1`: Představuje ID testovací sady. Tento parametr je povinný, pokud přepínač /byid **je** zadán. Toto ID je ID testovací sady Azure DevOps.
+ `test_suite_idN`: Představuje ID testovací sady. Tento parametr je povinný, pokud přepínač /byid **je** zadán. Toto ID je ID testovací sady Azure DevOps.

##### <a name="playbacksuite-examples"></a>playbacksuite: příklady

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Spustí všechny testovací případy v zadané sadě testů Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: volitelné přepínače

+ `/retry[=seconds]`: Pokud je zadán tento přepínač a testovací případy jsou blokovány jinými instancemi RSAT, proces přehrávání počká zadaný počet sekund a poté to zkusí ještě jednou. Výchozí hodnota přepínače \[seconds\] je 120 sekund. Bez tohoto přepínače bude proces okamžitě zrušen, pokud jsou testovací případy zablokovány.
+ `/comments[="comment"]`: Zadejte vlastní informační řetězec, který bude přidán do pole **Komentáře** na stránkách souhrnu a výsledků testu pro spuštění testovacích případů Azure DevOps.
+ `/byid`: Tento přepínač označuje, že požadovaná testovací sada je identifikována pomocí ID Azure DevOps, nikoli názvem testovací sady.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: požadované parametry

+ `test_suite_id`: Představuje ID testovací sady tak, jak existuje v Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: příklady

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

Zavře aplikaci. Tento příkaz je užitečný pouze v případě, že aplikace běží v interaktivním režimu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: příklady

`quit`

#### <a name="upload"></a>upload

Nahrává soubory příloh (soubory nahrávek, provádění a parametrů), které patří do určené testovací sady nebo testovacích případů, do Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: požadované parametry

+ `test_suite_name`: Odeslány budou všechny soubory patřící do zadané testovací sady.
+ `test_case_id1`: Představuje ID prvního testovacího případu, který by měl být nahrán. Tento parametr použijte pouze v případě, že nebyl zadán žádný název testovací sady.
+ `test_case_idN`: Představuje ID posledního testovacího případu, který by měl být nahrán. Tento parametr použijte pouze v případě, že nebyl zadán žádný název testovací sady.

##### <a name="upload-examples"></a>upload: příklady

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Nahraje do Azure DevOps pouze soubor nahrávky, který patří do jedné či více zadaných testovacích případů.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: požadované parametry

+ `test_case_id1`: Představuje ID prvního testovacího případu nahrávky, který by měl být nahrán do Azure DevOps.
+ `test_case_idN`: Představuje ID posledního testovacího případu nahrávky, který by měl být nahrán do Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: příklady

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Zobrazuje tři režimy použití této aplikace.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Interaktivní spuštění aplikace:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Spuštění aplikace zadáním příkazu:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Spuštění aplikace poskytnutím souboru nastavení:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>Příklad Windows PowerShell

#### <a name="run-a-test-case-in-a-loop"></a>Spuštění testovacího případu ve smyčce

Máte testovací skript, který vytvoří nového odběratele. Pomocí skriptování lze tento testovací případ spustit ve smyčce tak, že před spuštěním každé iterace náhodně použijete následující data:

- ID odběratele
- Jméno zákazníka
- Adresa odběratele

ID zákazníka bude mít formát *ATCUS\<number\>*, kde \<number\> je hodnota mezi **000000001** a **999999999**.

V následujícím příkladu je použit jeden parametr **start** pro definování prvního použitého čísla. Aplikace používá k definování počtu odběratelů, které je nutné vytvořit, druhý parametr **nr**. Parametry v souboru parametrů aplikace Excel jsou pro každou iteraci změněny pomocí funkce UpdateCustomer. Poté bude příkazový řádek RSAT volán ve funkci RunTestCase.

Otevřete Microsoft Windows PowerShell Integrated Scripting Environment (ISE) v režimu správy a vložte následující kód do okna s názvem **Untitled1. ps1.**

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Spuštění skriptu, který závisí na datech v Microsoft Dynamics 365

V následujícím příkladu je pomocí volání OData (Open Data Protocol) nalezen stav nákupní objednávky. Pokud není stav **fakturován**, můžete například volat testovací případ RSAT, který zaúčtuje fakturu.

```powershell
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
