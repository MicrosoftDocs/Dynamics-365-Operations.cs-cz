---
title: Použití kurzu pro nástroj Regression Suite Automation Tool
description: Toto téma ukazuje, jak používat Regression Suite Automation Tool (RSAT). Popisuje různé funkce a poskytuje příklady, které používají pokročilé skriptování.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 9afa98156c58d10c19454430769a3d60343661dc
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550950"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Použití kurzu pro Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Pomocí nástrojů internetového prohlížeče můžete tuto stránku stáhnout a uložit ve formátu PDF. 

Tento kurz prochází některými rozšířenými funkcemi nástroje Regression Suite Automation Tool (RSAT), zahrnuje přiřazení ukázky a popisuje strategii a klíčové body učení.

## <a name="features-of-rsattask-recorder"></a>Funkce nástroje RSAT/Záznamník úloh

### <a name="validate-a-field-value"></a>Ověření hodnoty pole

Další informace o této funkci naleznete v tématu [Vytvoření nového záznamu úkolu, který má funkci ověření](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Uložená proměnná

Další informace o této funkci naleznete v tématu [Úprava existujícího záznamu úkolu pro vytvoření uložené proměnné](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Odvozený testovací případ

1. Spusťte Regression Suite Automation Tool (RSAT) a vyberte oba testovací případy, které jste vytvořili v [Nastavení a instalace nístroje Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).
2. Vyberte **Nový \> Odložit testovací případ**.

    ![Vytvoření příkazu odvozeného testovacího případu v nabídce Nový](./media/use_rsa_tool_01.png)

3. Zobrazí se zpráva oznamující, že pro každý vybraný testovací případ v aktuální sadě testů bude vytvořen odvozený testovací případ a že každý odvozený testovací případ bude mít svou vlastní kopii souboru parametrů aplikace Excel. Vyberte **OK**.

    > [!NOTE]
    > Spustíte-li odvozený testovací případ, použije se záznam úloh jeho nadřazeného testovacího případu a jeho vlastní kopie souboru parametrů aplikace Excel. Tímto způsobem lze spustit stejný test s jinými parametry, aniž by bylo nutné udržovat více než jeden záznam úloh. Odvozený testovací případ nemusí být součástí stejné sady testů jako nadřazený testovací případ.

    ![Okno se zprávou](./media/use_rsa_tool_02.png)

    Jsou vytvořeny dva další odvozené testovací případy a je pro ně zaškrtnuto políčko **Odvozený?**.

    ![Vytvořené odvozené testovací případy](./media/use_rsa_tool_03.png)

    Odvozený testovací případ je automaticky vytvořen v Azure DevOps. Jedná se o podřízenou položku testovacího případu **Vytvoření nového produktu** a je označen speciálním klíčovým slovem: **RSAT:DerivedTestSteps**. Tyto testovací případy se také automaticky přidají do plánu testování v Azure DevOps.

    ![Klíčové slovo RSAT: DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Pokud z jakéhokoliv důvodu nejsou vytvořené odvozené testovací případy ve správném pořadí, přejděte do Azure DevOps a přeuspořádejte testovací případy v sadě testů, aby je mohl RSAT spustit ve správném pořadí.

4. Vyberte odvozené testovací případy a poté výběrem možnosti **Upravit** otevřete odpovídající soubory parametrů aplikace Excel.
5. Upravte tyto soubory parametrů aplikace Excel stejným způsobem, jakým jste upravili nadřazené soubory. Jinými slovy, ujistěte se, že je ID produktu nastaveno tak, aby bylo automaticky vygenerováno. Rovněž se ujistěte, že uložená proměnná je zkopírována do příslušných polí.
6. Na kartě **Obecné** v obou souborech parametrů aplikace Excel aktualizujte hodnotu pole **Společnost** na **USSI**, takže odvozené testovací případy se spustí proti jiné právnické osobě, než je nadřazený testovací případ. Chcete-li testovací případy spustit proti konkrétnímu uživateli (nebo s rolí přidruženou k určitému uživateli), můžete aktualizovat hodnotu pole **Testovací uživatel**.
7. Vyberte **Spustit** a ověřte, že je produkt vytvořen v právnické osobě USMF i v právnické osobě USSI.

### <a name="validate-notifications"></a>Ověření oznámení

Tuto funkci lze použít k ověření, zda došlo k akci. Je-li například vytvořena, odhadnuta a následně zahájena výrobní zakázka, aplikace zobrazí zprávu „Výroba - Zahájení“ a upozorní vás, že výrobní zakázka byla zahájena.

![Oznámení Výroba - Zahájení](./media/use_rsa_tool_05.png)

Tuto zprávu můžete ověřit prostřednictvím RSAT zadáním textu zprávy na kartě **Ověření zprávy** souboru parametrů aplikace Excel pro příslušný záznam.

![Karta Ověření zprávy](./media/use_rsa_tool_06.png)

Po spuštění testovacího případu se zpráva v souboru parametrů aplikace Excel porovná se zprávou zobrazenou. Pokud se zprávy neshodují, testovací případ se nezdaří.

> [!NOTE]
> Na kartě **Ověření zprávy** v souboru parametrů aplikace Excel můžete zadat více než jednu zprávu. Zprávy mohou být také chybové nebo varovné namísto informačních zpráv.

### <a name="validate-values-by-using-operators"></a>Ověření hodnot pomocí operátorů

V předchozích verzích RSAT bylo možné ověřit hodnoty pouze v případě, že se kontrolní hodnota rovnala očekávané hodnotě. Nová funkce umožňuje ověřit, že proměnná není rovna, je menší než nebo je větší než zadaná hodnota.

- Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    V souboru parametrů aplikace Excel se zobrazí nový **Operátor**.

    > [!NOTE]
    > Pokud používáte starší verzi nástrojů RSAT, musíte vygenerovat nové soubory parametrů aplikace Excel.

    ![Pole Operátor](./media/use_rsa_tool_07.png)

V následujícím příkladu je ukázáno, jak lze pomocí této funkce ověřit, zda je množství na skladě větší než 0 (nula).

1. V ukázkových datech společnosti **USMF** vytvořte záznam úloh, který má následující kroky:

    1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
    2. Použijte rychlý filtr pro hledání záznamů. Například filtrujte na hodnotě **1000** pole **Číslo položky**.
    3. Vyberte **Zásoby na skladě**.
    4. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat na hodnotě **1** pro pole **Pracoviště**.
    5. Označte na seznamu vybraný řádek.
    6. Ověřte, zda hodnota pole **Celkem k dispozici** je **411.0000000000000000**.

2. Uložte záznam úloh do knihovny BPM v LCS a synchronizujte ho do Azure DevOps.
3. Přidejte testovací případ do testovacího plánu a načtěte testovací případ do RSAT.
4. Otevřete soubor parametrů aplikace Excel. Na kartě **InventOnhandItem** se zobrazí část **Ověřit InventOnhandItem**, která obsahuje pole **Operátor**.

    ![Pole Operátor](./media/use_rsa_tool_08.png)

5. Chcete-li ověřit, zda bude množství na skladě vždy větší než 0, změňte hodnotu pole **Hodnota** z **411** na **0** a hodnotu pole **Operátor** od znaménka rovná se (**=**). na znaménko větší než (**\>**).

    ![Hodnoty polí Hodnota a Operátor byly změněny.](./media/use_rsa_tool_09.png)

6. Uložte a zavřete soubor parametrů aplikace Excel.
7. Vyberte **Odeslat** pro uložení provedených změn souboru parametrů aplikace Excel do Azure DevOps.

Nyní, pokud je hodnota pole **Celkem k dispozici** pro určitou položku ve skladu větší než 0 (nula), testy budou úspěšné, bez ohledu na skutečnou hodnotu zásob na skladě.

### <a name="generator-logs"></a>Protokoly generátoru

Tato funkce vytvoří složku obsahující protokoly testovacích případů, které byly spuštěny.

- Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.

    ```
    <add key="LogGeneration" value="false" />
    ```

Po spuštění testovacích případů můžete vyhledat soubory protokolů ve složce **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![Složka GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Pokud existovaly testovací případy před změnou hodnoty v souboru. config, nebudou protokoly generovány pro tyto testovací případy, dokud nevytvoříte nové soubory spuštění testu.
> 
> ![Příkaz Generovat pouze soubory spuštění testu v nabídce Nový](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Snímek

Tato funkce pořídí snímky obrazovek kroků, které byly provedeny při záznamu úloh.

- Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu následujícího prvku z **false** na **true**.

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Pro každý spuštěný testovací případ se vytvoří samostatná složka pod Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**.

![Složka snímku pro testovací případ](./media/use_rsa_tool_12.png)

V každé z těchto složek můžete vyhledat snímky kroků, které byly provedeny při spuštění testovacích případů.

![Soubory snímků](./media/use_rsa_tool_13.png)

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

![Tok ukázkového scénáře](./media/use_rsa_tool_14.png)

Následující ilustrace znázorňuje obchodní procesy pro tento scénář v RSAT.

![Obchodní procesy pro ukázkový scénář](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategie – klíčové učení

### <a name="data"></a>Údaje

- Ujistěte se, že máte reprezentativní datové objemy (kopie dat produkční/zlaté konfigurace a přenesená data).
- Když generujete nová data pomocí záznamníku úloh, vytvořte názvy testů, které nekolidují s existujícími názvy (například použijte předponu **RSATxxx**).
- Použijte obnovení k určitému bodu v čase Azure- pro opětovné spuštění testů v prostředích, které nejsou v úrovni 1.
- Ačkoli můžete použít funkce Excelu **RANDOM** a **NOW** k vygenerování jedinečné kombinace, úsilí je poměrně vysoké. Následuje příklad.

    ```
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

### <a name="command-line"></a>Příkazový řádek

RSAT lze volat z okna **příkazového řádku**.

> [!NOTE]
> Ověřte, zda je proměnná prostředí **TestRoot** nastavena na cestu instalace RSAT. (V Microsoft Windows otevřete **Ovládací panel**, vyberte **Systém a zabezpečení \> Systém \> Pokročilá nastavení systému** a pak zvolte **Proměnné prostředí**.)

1. Otevřete okno **příkazového řádku** jako správce.
2. Spusťte nástroj z instalačního adresáře.

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Vyvolejte seznam všech příkazů.

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Příklad Windows PowerShell

#### <a name="run-a-test-case-in-a-loop"></a>Spuštění testovacího případu ve smyčce

Máte testovací skript, který vytvoří nového odběratele. Pomocí skriptování lze tento testovací případ spustit ve smyčce tak, že před spuštěním každé iterace náhodně použijete následující data:

- ID odběratele
- Jméno zákazníka
- Adresa odběratele

ID zákazníka bude mít formát *ATCUS\<číslo\>*, kde \<číslo\> je hodnota mezi **000000001** a **999999999**.

V následujícím příkladu je použit jeden parametr **start** pro definování prvního použitého čísla. Aplikace používá k definování počtu odběratelů, které je nutné vytvořit, druhý parametr **nr**. Parametry v souboru parametrů aplikace Excel jsou pro každou iteraci změněny pomocí funkce UpdateCustomer. Poté bude příkazový řádek RSAT volán ve funkci RunTestCase.

Otevřete Microsoft Windows PowerShell Integrated Scripting Environment (ISE) v režimu správy a vložte následující kód do okna s názvem **Untitled1. ps1.**

```
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
$excelFilename = "full path to excel file parameter file"
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

```
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