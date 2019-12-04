---
title: Automatizace testování s elektronickým výkaznictvím
description: V tomto tématu je vysvětleno, jak můžete pomocí funkce směrného plánu elektronického výkaznictví (ER) automatizovat testování některých funkcí.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: be641e1b2f90f4d19f7ed15e47413c0aa43d5073
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771437"
---
# <a name="automate-testing-with-electronic-reporting"></a>Automatizace testování s elektronickým výkaznictvím

[!include[banner](../includes/banner.md)]

V tomto tématu je vysvětleno, jak můžete pomocí systému elektronického výkaznictví (ER) automatizovat testování některých funkcí. Příklad v tomto tématu ukazuje, jak automatizovat testování zpracování platby dodavatele.

Aplikace používá systém ER ke generování platebních souborů a odpovídajících dokumentů během zpracování plateb dodavatele. Systém ER se skládá z datového modelu, mapování modelu a formátovacích součástí, které podporují zpracování plateb pro různé typy plateb a generování dokumentů v různých formátech. Tyto komponenty lze stáhnout ze služby Microsoft Dynamics Lifecycle Services (LCS) a importovat do instance.

Můžete také upravit každou komponentu Microsoft a použít ji jako základ pro vlastní komponentu. Vytvořením vlastní verze můžete provést změny, které podporují konkrétní požadavky. Můžete například upravit datový model ER a mapování modelu ER pro přístup k datům aplikací specifickým pro odběratele, nebo můžete změnit formát ER pro úpravu rozvržení vygenerovaného dokumentu.

Můžete použít vlastní formáty ER pro zpracování souborů plateb, které generují platby dodavatelů, a také ke zpracování kontrolních sestav. V komponentách ER je podporováno vytváření verzí. Z tohoto důvodu může společnost Microsoft poskytnout aktualizované verze řešení ER pro zpracování plateb dodavatele a automaticky sloučit aktualizovanou verzi s přizpůsobenou komponentou tím, že ji znovu vytvoří. Je však nutné otestovat znovu vytvořenou verzi, abyste se ujistili, že funguje očekávaným způsobem.

Datové modely ER a mapování modelů ER jsou společné pro mnoho formátů ER, které se používají ke zpracování plateb různých typů a ke generování platebních dokumentů pro konkrétní zemi nebo oblast. Proto je důrazně doporučeno automatizovat přijímání uživatelů a testování integrace, takže je automaticky prováděno ve více společnostech, ale bere v úvahu kontext země/oblasti pro každou cílovou společnost za použití různých datových sad, atd.

Další informace o tom, jak vytvořit vlastní verzi formátu, která je založena na formátu přijatém od poskytovatele konfigurace, naleznete v tématu [ER Upgrade formátu přijetím nové základní verze tohoto formátu](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Klíčové koncepty

Funkční členové skupiny Power Users mohou vytvářet přijímání uživatelů a testování integrace bez nutnosti vytvářet zdrojový kód.

- Pomocí funkce směrného plánu ER můžete porovnat generované dokumenty s hlavními kopiemi. Více informací získáte v tématu [Sledování výsledků vygenerovaných sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md).
- Pomocí záznamníku úloh můžete zaznamenávat testovací případy a zahrnovat hodnocení směrného plánu. Více informací viz [Zdroje záznamníku úloh](../user-interface/task-recorder.md).
- Seskupte testovací případy pro požadované scénáře testování. Další informace naleznete v tématu [Vytvoření a automatizace testů](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - K vytvoření knihoven pro testy přijetí uživatelů použijte modelování podnikových procesů v LCS.
    - Pomocí testovacích knihoven BPM vytvořte testovací plán a testovací sady ve službě Microsoft Azure DevOps Services (Azure DevOps).

Funkční členové skupiny Power Users mohou spustit testy přijetí a integrace s uživatelem.

- Pomocí nástroje RSAT (Regression Suite Automation Tool) spusťte testovací případy požadované sady testů.
- Oznamte výsledky testování do aplikace Azure DevOps a pomocí této služby prozkoumejte tyto výsledky.

## <a name="prerequisites"></a>Předpoklady

Před provedením úkolů v tomto tématu je třeba splnit následující předpoklady:

- Nasaďte topologii, která podporuje automatizaci testování. Musíte mít přístup do instance této topologie pro roli **Správce systému**. Tato topologie musí obsahovat ukázková data, která budou použita v tomto příkladu. Další informace naleznete v tématu [Nasazení a použití prostředí, které podporuje automatizaci průběžného sestavení a testů](../perf-test/continuous-build-test-automation.md).
- Chcete-li automaticky spustit testy přijetí a integrace s uživatelem, je nutné nainstalovat RSAT do používané topologie a odpovídajícím způsobem ji nakonfigurovat. Informace o tom, jak instalovat RSAT pro práci s aplikacemi Finance and Operations a Azure DevOps, získáte v tématu [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Věnujte pozornost předpokladům pro používání nástroje. Následující obrázek znázorňuje příklad nastavení RSAT. Modrý obdélník ohraničuje parametry, které určují přístup do Azure DevOps. Zelený obdélník označuje parametry, které určují přístup k instanci.

    ![Nastavení RSAT](media/GER-Configure.png "Snímek obrazovky dialogového okna Nastavení RSAT")

- K uspořádání testovacích případů v sadách za účelem zajištění správného pořadí provádění, aby bylo možné shromáždit protokoly provádění testů pro další hlášení a vyšetřování, musíte mít přístup Azure DevOps z nasazené topologie.
- Chcete-li dokončit příklad v tomto tématu, doporučujeme vám stáhnout [použití ER pro testy RSAT](https://go.microsoft.com/fwlink/?linkid=874684) Tento soubor zip obsahuje následující průvodce úkoly:

    | Obsah                                           | Název a umístění souboru |
    |---------------------------------------------------|------------------------|
    | Ukázkový záznam úloh pro přípravu dat k testování | Příprava\\záznam XML |
    | Ukázkový záznam úlohy zpracování platby dodavatele   | Proces\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Příprava modulu Závazky pro zpracování plateb dodavatele

1. Přihlaste se k instanci.
2. Stáhněte si následující konfigurace elektronického výkaznictví z úložiště LCS. Pokyny viz [Import konfigurace ze služby Lifecycle Services pro elektronické výkaznictví](./tasks/er-import-configuration-lifecycle-services.md).

    - **Model platby** Konfogurace modelu ER
    - **Mapování modelu platby 1611** Konfigurace mapování modelu ER
    - **BACS (UK)** Konfigurace formátu ER

    ![Konfigurace elektronického výkaznictví](media/GER-Configurations.png "Snímek obrazovky stránky se směrným plánem v elektronickém výkaznictví")

3. Vyberte ukázkovou datovou společnost **GBSI**, která má kontext země/oblasti ve Velké Británii.
4. Konfigurace parametrů závazků:

    1. Přejděte do nabídky **Závazky \> Nastavení \> Metody platby**.
    2. Vyberte **Elektronický** způsob platby.
    3. Konfigurovat vybranou metodu platby tak, aby používala dříve stažený formát ER systému **BACS (UK)** ke zpracování plateb dodavatele:

        1. Na pevné záložce **Formáty souboru** nastavte volbu **Obecný formát elektronického exportu** na **Ano**.
        2. V poli **Exportovat konfiguraci formátu** vyberte **BACS (UK)**.

    ![Stránka Metody platby](media/GER-APParameters.png "Snímek obrazovky stránky platebních metod")

    > [!NOTE]
    > Pokud používáte odvozenou verzi tohoto formátu ER, která byla vytvořena pro podporu vlastního nastavení, můžete tuto konfiguraci vybrat v **elektronické** metodě platby.

5. Vytvoření ukázkové platby dodavatele:

    1. Přejděte na **Závazky \> Platby \> Deník plateb**.
    2. Ujistěte se, že jste deník plateb nezaúčtovali.

        ![Stránka Deník plateb](media/GER-APJournal.png "Snímek obrazovky stránky deníku platby")

    3. Vyberte **Řádky** a zadejte řádek, který obsahuje následující informace.

        | Pole               | Ukázková hodnota   |
        |---------------------|-----------------|
        | Název dodavatele         | GB\_SI\_000001  |
        | Má Dáti               | 1,000.00        |
        | Měna            | GBP             |
        | Typ protiúčtu | Banka            |
        | Protiúčet      | GBSI OPER       |
        | Metoda platby   | Elektronicky      |

    ![Stránka Platby dodavatelů](media/GER-APJournalLines.png "Snímek obrazovky stránky Platby dodavatele")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Příprava architektury ER pro testování zpracování plateb dodavatele

### <a name="configure-er-parameters"></a>Konfigurace parametrů ER

1. Přejděte do nabídky **Správa organizace \> Elektronické výkaznictví \> Parametry elektronického výkaznictví**.
2. Na kartě **přílohy** vyberte v poli **směrný plán** možnost **soubor** jako typ dokumentu, který používá systém správy dokumentů (DM) pro uchovávání dokumentů souvisejících se základní funkcí jako přílohy DM.

    ![Stránka parametrů elektronického výkaznictví](media/GER-ERParameters.png "Snímek obrazovky stránky Parametry elektronického výkaznictví")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Generování kopií směrného plánu pro dokumenty související s platbami dodavatele

1. Přejděte na **Závazky \> Platby \> Deník plateb**.
2. Vybrat **řádky**.
3. Vyberte **Generovat platby**.
4. Vyberte **Elektronický** způsob platby.
5. Vyberte bankovní účet **GBSI OPER**.
6. Nastavte možnost **Vytisknout kontrolní sestavu** na **Ano**.
7. Stáhněte vygenerovaný výstup jako soubor zip.
8. Otevřete stažený soubor.
9. Extrahujte následující soubory ze staženého souboru:

    - **Soubor** soubor platby v textovém formátu
    - Soubor kontrolní sestavy **ERVendOutPaymControlReport** ve formátu XLSX

    ![Extrahované soubory](media/GER-APJournalProcessed.png "Snímek obrazovky názvů extrahovaných souborů v Průzkumníkovi Windows")

### <a name="turn-on-the-er-baseline-feature"></a>Zapnutí funkce směrného plánu ER

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. V podokně akcí na kartě **Konfigurace** zvolte **Parametry uživatele**.
3. Nastavte možnost **Spustit v režimu ladění** na **Ano**.

Zapnutím parametru **spustit v režimu ladění** vynutíte, aby architektura ER prováděla následující akce po spuštění libovolného formátu ER generujícího odchozí dokumenty:

1. Určuje, zda byl směrný plán konfigurován pro některou ze součástí provedeného formátu ER.
2. Určete, zda se každý nakonfigurovaný směrný plán použije za aktuálních podmínek (kód společnosti pro přihlášenou společnost, název souboru a příponu názvu souboru generovaného výstupu atd.).
3. Pro každý použitelný směrný plán proveďte následující akce:

    1. Porovnejte výstup, který je generován při provádění formátu ER, s odpovídajícím směrným plánem.
    2. Výsledky porovnání uložte do protokolu ladění konfigurací ER.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Konfigurace směrných plánů ER pro zpracování plateb dodavatele

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. Vyberte **Směrné plány**.
3. Zvolte **Nové**.
4. V poli **Reference** vyberte formát **BACS (UK)**.
5. Vyberte **Přílohy**.
6. Přidání nového směrného plánu souboru platby dodavatele:

    1. Zvolte **Nové**.
    2. V poli **Typ** vyberte **Soubor** Typ dokumentu DM, který jste nakonfigurovali v parametrech ER za účelem uložení artefaktů směrného plánu.
    3. Přejděte k výběru místně uloženého **souboru** platby souboru v textovém formátu.
    4. Do pole **Popis** zadejte **Soubor TXT platby**.

7. Přidání nového směrného plánu pro sestavu řízení platby dodavatele:

    1. Zvolte **Nové**.
    2. V poli **Typ** vyberte **Soubor** Typ dokumentu DM, který jste nakonfigurovali v parametrech ER za účelem uložení artefaktů směrného plánu.
    3. Přejděte k výběru místně uloženého kontrolního souboru sestavy **ERVendOutPaymControlReport** ve formátu XLSX.
    4. Do pole **Popis** zadejte **Kontrolní sestava XLS platby**.

    ![Směrné plány pro soubor a řídicí sestavu platby dodavatele](media/GER-BaselineAttachments.png "Snímek obrazovky se stránkou konfigurace s vybranou sestavou platebního modulu XLSX")

8. Zavřete stránku.
9. Na pevné záložce **Směrné plány** vyberte **Nový** ke konfiguraci směrného plánu pro soubor platby:

    1. Pojmenujte **Nastavení směrného plánu pro soubor platby**.
    2. V poli **název součásti souboru** vyberte možnost **soubor**, chcete-li použít tento směrný plán ve formátu výstupu ER, který generuje soubor platby v textovém formátu souboru BACS (UK).
    3. V poli **Společnosti** vyberte **GBSI**, chcete-li použít tento základní směrný plán při spuštění formátu ER **BACS (UK)** ve společnosti GBSI.
    4. V poli **Maska názvu souboru** zadejte **\*.TXT** pro použití tohoto směrného plánu pouze pro výstupy formátu **souboru** s příponou **.txt**.
    5. V poli **směrný plán** vyberte **soubor txt platby**, aby se tento směrný plán používal pro porovnání s generovaným výstupem.

10. Vyberte **Nový** a nakonfigurujte směrný plán pro sestavu ovládacího prvku:

    1. Pojmenujte řádek **Nastavení směrného plánu pro kontrolní sestavu**.
    2. V poli **Název součásti souboru** vyberte možnost **ERVendOutPaymControlReport**, chcete-li použít tento směrný plán ve formátu výstupu ER, který generuje kontrolní sestavu.
    3. V poli **Společnosti** vyberte **GBSI**, chcete-li použít tento základní směrný plán při spuštění formátu ER **BACS (UK)** ve společnosti GBSI.
    4. V poli **Maska názvu souboru** zadejte **\*.XLSX** pro použití tohoto směrného plánu pouze pro výstupy formátu **ERVendOutPaymControlReport** s příponou **.xslx**.
    5. V poli **směrný plán** vyberte **kontrolní sestava XLS platby**, aby se tento směrný plán používal pro porovnání s generovaným výstupem.

    ![Pevná záložka Směrné plány na stránce Konfigurace](media/GER-BaselineRules.png "Snímek obrazovky pevné záložky Směrné plány na stránce Konfigurace")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Záznam testů pro ověření zpracování plateb dodavatele

Jako funkční uživatel Power User můžete zaznamenat vlastní kroky a otestovat tak zpracování plateb dodavatelů. Doporučujeme vám přehrát (a podle potřeby upravit) záznam úloh **Prepare\\Recording.xml**, který jste stáhli dříve. Tento záznam slouží k nastavení všech testovacích dat do správného stavu. Tento krok je vyžadován, protože testování může být provedeno mnohokrát a každý test musí používat data, která jsou ve stejném stavu.

### <a name="reset-user-settings"></a>Obnovit nastavení uživatele

1. Otevřete výchozí řídicí panel.
2. Vyberte tlačítko **Nastavení** (symbol ozubeného kola).
3. Vyberte **Možnosti uživatele**.
4. Vyberte **Údaje o využití**.
5. Vyberte **Obnovit**.
6. Vyberte **Ano** pro potvrzení, že chcete resetovat údaje o použití.
7. Zavřete stránku.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Záznam kroků pro přípravu dat pro testování

1. Vyberte tlačítko **Nastavení** (symbol ozubeného kola).
2. Vyberte **Záznamník úloh**.
3. Vyberte **Záznam přehrávání**.
4. Vyberte **Otevřít z tohoto počítače**.
5. Vyberte **Procházet** a vyberte místně uložený soubor **Prepare\\Recording.xml**.
6. Vyberte **Spustit**.
7. Vybírejte možnost **Přehrát další čekající krok**, dokud se nepřehrají všechny kroky v nahrávce.

Tento záznam úloh provádí následující akce:

1. Nastavte stav zpracovaného řádku platby na hodnotu **Žádný**.

    ![Záznam úkolu kroky 3 až 4](media/GER-Recording1Review1.png "Snímek obrazovky záznamu úkolu kroky 3 až 4")

2. Zapněte parametr uživatele ER **Spustit v režimu ladění**.

    ![Záznam úkolu kroky 9 až 10](media/GER-Recording1Review2.png "Snímek obrazovky záznamu úkolu kroky 9 až 10")

3. Vyčistěte protokol ladění ER, který obsahuje výsledky porovnání vygenerovaných souborů do směrných plánů.

    ![Záznam úkolu kroky 13 až 15](media/GER-Recording1Review3.png "Snímek obrazovky záznamu úkolu kroky 13 až 15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Zaznamenejte kroky k testování zpracování plateb dodavatele

Doporučujeme vám přehrát (a podle potřeby upravit) záznam úloh **Process\\Recording.xml**, který jste stáhli dříve. Tento záznam se používá ke zpracování plateb dodavateli a k ověření výsledků porovnání vygenerovaných dokumentů s odpovídajícími směrnými plány.

1. Vyberte tlačítko **Nastavení** (symbol ozubeného kola).
2. Vyberte **Záznamník úloh**.
3. Vyberte **Záznam přehrávání**.
4. Vyberte **Otevřít z tohoto počítače**.
5. Vyberte **Procházet** a vyberte místně uložený soubor **Process\\Recording.xml**.
6. Vyberte **Spustit**.
7. Vybírejte možnost **Přehrát další čekající krok**, dokud se nepřehrají všechny kroky v nahrávce.

Tento záznam úloh provádí následující akce:

1. Spusťte zpracování platby dodavateli.
2. Vyberte správné parametry modulu runtime a zapněte generování kontrolní sestavy.

    ![Záznam úkolu kroky 3 až 8](media/GER-Recording2Review1.png "Snímek obrazovky záznamu úkolu kroky 3 až 8")

3. Přejděte k protokolu ladění ER pro zaznamenání výsledků porovnání vygenerovaných výstupů do odpovídajících směrných plánů.

    V protokolu ladění ER se výsledky porovnání zobrazí v poli **Generovaný text**. Pole **Komponenta formátu** a **Cesta formátu, která způsobila záznam do protokolu**, odkazují na komponentu souboru, pro kterou byl vygenerovaný výstup porovnán se směrným plánem.

    ![Položky na stránce Protokoly spuštění elektronického výkaznictví](media/GER-ERDebugLog.png "Snímek položek na stránce Protokoly spuštění Parametry elektronického výkaznictví")

4. Porovnání aktuálního výstupu se směrným plánem je zaznamenáno pomocí možnosti **Ověřit** záznamník úloh a výběrem možnosti **Aktuální hodnota**.

    ![Použití možnosti ověření pro porovnání s aktuální hodnotou](media/GER-TRRecordValidation.png "Snímek obrazovky použití možnosti ověření pro porovnání s aktuální hodnotou")

    Následující obrázek ukazuje, jak vypadají zaznamenané kroky ověření v záznamu úloh.

    ![Záznam úkolu kroky 13 a 15](media/GER-Recording2Review2.png "Snímek obrazovky záznamu úkolu kroky 13 a 15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Přidání zaznamenaných testů do Azure DevOps

1. Otevřete prostředí Azure DevOps.
2. Vyberte projekt, který jste definovali v parametrech RSAT, [při konfiguraci nástroje](#prerequisites).
3. Vyberte zkušební plán, který jste definovali v parametrech RSAT, [při konfiguraci nástroje](#prerequisites).
4. Vytvořit nový testovací případ pro vybraný zkušební plán:

    1. Pojmenujte testovací případ **Příprava dat pro testování elektronické platby dodavatele**.
    2. Připojte soubor **Record. XML** ze složky **Připravit**, kterou jste stáhli dříve.

5. Vytvořit nový testovací případ pro vybraný zkušební plán:

    1. Pojmenujte testovací případ **Zkušební zpracování plateb dodavatelů pomocí formátu systému BACS (UK)**.
    2. Připojte soubor **Record. XML** ze složky **Proces**, kterou jste stáhli dříve.

    ![Nové testovací případy pro vybraný zkušební plán](media/GER-RSAT-DevOps-Tests-Passed.png "Snímek obrazovky Nové testovací případy pro vybraný zkušební plán")

> [!NOTE]
> Věnujte pozornost správnému pořadí provedení přidaných testů.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Příprava RSAT pro spuštění zaznamenaných testů

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Nahrání testů z Azure DevOps do RSAT

1. Otevřete v aktuální topologii místní aplikaci RSAT.
2. Vyberte možnost **Load** k načtení testů, které se aktuálně nacházejí v aplikaci Azure DevOps, do RSAT.

    ![Testy načtené na RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Snímek obrazovky testů načtených na RSAT")

### <a name="create-automation-and-parameters-files"></a>Vytvoření souborů automatizace a parametrů

1. V RSAT vyberte testy, které jste načetli z Azure DevOps.
2. Vyberte **Nový** k vytvoření souborů automatizace a parametrů RSAT.

    ![Automatizace RSAT a soubory parametrů vytvořené v RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Snímek obrazovky Automatizace RSAT a soubory parametrů vytvořené v RSAT")

### <a name="modify-the-parameters-files"></a>Změna souborů parametrů

1. V RSAT vyberte testovací případ **Příprava dat pro testování elektronické platby dodavatele**.
2. Vyberte možnost **Upravit**.
3. V sešitu Microsoft Excel, který je otevřen, změňte v listu **obecné** kód společnosti na **GBSI**, protože tato společnost bude použita k provedení testu.
4. V RSAT vyberte testovací případ **Zkušební zpracování plateb dodavatelů pomocí formátu systému BACS (UK)**.
5. Vyberte možnost **Upravit**.
6. V sešitu aplikace Excel, který je otevřen, změňte na listu **Obecné** kód společnosti na **GBSI.**
7. V listu **ERFormatMappingRunLogTable** si povšimněte, že buňky A:3 a C:3 obsahují text polí v tabulce protokolu ladění ER, která slouží k ověření výsledků porovnání výstupu se směrným plánem. Tyto texty budou použity k vyhodnocení záznamů protokolů ladění ER, které jsou vytvářeny při provádění testu.

    ![List ERFormatMappingRunLogTable](media/GER-RSAT-RSAT-ExcelParameters.png "Snímek obrazovky listu ERFormatMappingRunLogTable")

## <a name="run-the-tests-and-analyze-the-results"></a>Spuštění testů a analýza výsledků

### <a name="run-the-tests-in-rsat"></a>Spuštění testů v RSAT

1. V RSAT vyberte načtené testy.
2. Vyberte **Spustit**.

Všimněte si, že testovací případy jsou automaticky spuštěny v aplikaci pomocí webového prohlížeče.

### <a name="analyze-the-results-of-test-execution"></a>Analýza výsledků spuštění testu

Výsledky testu se ukládají na RSAT. Povšimněte si, že byly oba testy předány.

![Testy předané v RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Snímek obrazovky testů, které byly předány v RSAT")

Všimněte si, že výsledky spuštění testu jsou také odesílány do Azure DevOps, aby bylo možné provádět další analýzu.

![Výsledky spuštění testu v Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Obrazovka výsledků spuštění testu v Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Simulace situace, kdy se testy nedaří

Tato sada testů musí selhat, pokud alespoň jeden z generovaných výstupů neodpovídá odpovídajícímu směrnému plánu. Chcete-li této situace dosáhnout, můžete použít odvozenou verzi formátu **BACS (UK)**, který bude generovat soubor platby s jiným obsahem než odpovídajícím směrným plánem. Chcete-li tuto situaci simulovat, můžete použít stejný formát **BACS (UK)**, ale změnit částku platby na řádku zpracované platby.

1. Otevřete aplikaci a přejděte na **Závazky \> Platby \> Deník plateb**.
2. Vybrat **řádky**.
3. Vyberte řádek platby a poté vyberte **stav platby \> Žádný**.
4. V poli **Debet** dáti změňte hodnotu z **1 000,00** na **2 000,00**.
5. Klepnutím na tlačítko **Uložit** uložte změny.

### <a name="run-the-tests-in-rsat"></a>Spuštění testů v RSAT

1. V RSAT vyberte načtené testy.
2. Vyberte **Spustit**.

Všimněte si, že testovací případy jsou automaticky spuštěny v aplikaci pomocí webového prohlížeče.

### <a name="analyze-the-results-of-test-execution"></a>Analýza výsledků spuštění testu

Výsledky testu se ukládají na RSAT. Všimněte si, že druhý test selhal při druhém spuštění.

![Neúspěšné výsledky testů v RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Snímek obrazovky neúspěšných výsledků testů v RSAT")

Všimněte si, že výsledky spuštění testu jsou také odesílány do Azure DevOps, aby bylo možné provádět další analýzu.

![Neúspěšné výsledky testů v RSAT Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Snímek obrazovky neúspěšných výsledků testů v Azure DevOps")

Můžete mít přístup ke stavu každého testu. K protokolu spuštění můžete také přistupovat, abyste analyzovali důvody selhání. Na následujícím obrázku protokol spuštění ukazuje, že k chybě došlo kvůli rozdílu v obsahu mezi vygenerovaným souborem platby a jeho směrným plánem.

![Protokol provádění pro analýzu chyb v Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Snímek obrazovky protokolu provádění s analýzou chyby v Azure DevOps")

Proto, jak jste viděli, lze fungování formátu ER vyhodnotit automaticky pomocí RSAT jako testovací platformy a pomocí testovacích případů na základě záznamníku úloh, které používají funkci ER.

## <a name="additional-resources"></a>Další zdroje

- [Zdroje záznamníku úloh](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Vytvoření a automatizace akceptačních testování uživatele](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Nasazení a používání prostředí podporujícího průběžné sestavování a automatizace testování](../perf-test/continuous-build-test-automation.md)
- [Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami](er-trace-reports-compare-baseline.md)
- [Elektronické výkaznictví - Upgrade formátu přijetím nové základní verze tohoto formátu](tasks/er-upgrade-format.md)
- [Import konfigurace ER ze služby Lifecycle Services](tasks/er-import-configuration-lifecycle-services.md)
