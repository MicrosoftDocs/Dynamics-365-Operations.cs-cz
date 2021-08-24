---
title: Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami
description: Toto téma vysvětluje, jak porovnat výsledky generovaných sestav elektronického výkaznictví (ER) s hodnotami sestavy směrného plánu.
author: NickSelin
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: ecca65508c048e2946d912f2bf0292d811fb4eabac9602a35f1ce26f4ebe1da6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769917"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami

[!include[banner](../includes/banner.md)]

Můžete sledovat výsledky formátů elektronického výkaznictví (ER), které generují odchozí elektronické dokumenty. Když je zapnuté generování trasování (pomocí parametru uživatele ER **Spustit v režimu ladění**), nový záznam sledování je generován v protokolu spuštění formátu pokaždé, když je spuštěna sestava ER. Následující údaje jsou uloženy v každém trasování, které je generováno:

- Všechny výstrahy, které byly vytvořeny pravidly ověření
- Všechny chyby, které byly vytvořeny pravidly ověření
- Všechny vytvořené soubory, které jsou uloženy jako přílohy záznamu sledování

Jednotlivé základní soubory aplikací můžete uložit pro libovolný formát ER. Soubory jsou považovány za základní, když popisují očekávané výsledky sestavy, které jsou spuštěny. Pokud je k dispozici základní soubor pro formát ER, který byl spuštěný při zapnutí generování sledování, sledování kromě dříve zmíněných detailů uloží výsledky porovnání generovaného elektronického dokumentu do základního souboru. Stačí jediné kliknutí a můžete získat také generovaný elektronický dokument a jeho základní soubor v jednom souboru ZIP. Pak můžete provést detailní srovnání pomocí externího nástroje, například WinDiff.

Můžete vyhodnotit sledování k analýze, zda elektronické dokumenty, které jsou generovány, obsahují očekávaný obsah. Toto hodnocení můžete provést v prostředí testování přijetí uživatelem (UAT), když byl změněn základní kód (například při migraci na novou instanci aplikace, nainstalované balíčky oprav hotfix nebo změn nasazeného kódu). Tímto způsobem zajistíte, že hodnocení neovlivní provádění sestav ER sestavy, které se používají. U spousty sestav ER může probíhat hodnocení probíhat v bezobslužném režimu.

Další informace o této funkci získáte přehráním průvodců záznamů úloh **Generování sestav ER a porovnání jejich výsledků (část 1)** a **Generování sestav ER a porovnání výsledků (část 2)**, které jsou součástí obchodního procesu **7.5.4.3 Test IT services/solutions (10679)** a které se dají stáhnout ve [službě stažení softwaru Microsoft](https://go.microsoft.com/fwlink/?linkid=874684). Tito průvodci záznamů úloh vás provedou procesem konfigurace rozhraní ER na používání základních souborů pro posouzení generovaných elektronických dokumentů.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Příklad: Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami

Tento postup vysvětluje, jak konfigurovat architekturu ER tak, aby byly shromažďovány informace o provádění formátu ER, a poté vyhodnotit výsledky těchto provedení. Jako součást tohoto vyhodnocení budou vygenerované dokumenty porovnány se svými soubory směrného plánu. V tomto příkladu vytvoříte požadované konfigurace ER pro vzorovou společnost Litware, Inc. Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití libovolné datové sady.

K provedení kroků z tohoto příkladu musíte nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurace** ověřte, že je uveden poskytovatel konfigurace ukázkové společnosti Litware, Inc. a že je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, proveďte kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Konfigurujte parametry správy dokumentů

1. Přejděte na **Správa organizace** \> **Správa dokumentů** \> **Typy dokumentů** a vtvořte nový typ dokumentu pro uložení souborů směrného plánu.
2. V poli **Třída** zadejte **Připojit soubor**.
3. V poli **Skupina** zadejte **Soubor**.

![Stránka typu dokumentu.](media/GER-BaselineSample-SetupDocumentType.PNG "Snímek obrazovky stránky Typy dokumentů")

> [!NOTE]
> Pro každou sadu dat, ve které plánujete použít funkci směrného plánu ER, je nutné nakonfigurovat nový typ dokumentu se stejným názvem.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Konfigurace parametrů ER tak, aby začaly používat funkci směrného plánu

1. V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Parametry elektronického výkaznictví**.

    ![Pracovní prostor elektronického vykazování.](media/GER-BaselineSample-ERWorkspace.PNG "Obrazovka pracovního prostoru Elektronické výkaznictví")

2. Na kartě **Přílohy** zadejte do pole **Směrný plán** typ dokumentu, který jste právě vytvořili, nebo ho vyberte.

    ![Karta přílohy na stránce parametry elektronického výkaznictví.](media/GER-BaselineSample-ERParameters.PNG "Snímek obrazovky Parametry elektronického výkaznictví")

3. Vyberte **Uložit** a zavřete stránku **Parametry elektronického výkaznictví**.

### <a name="add-a-new-er-model-configuration"></a>Přidání nové konfigurace ER modelu

1. V pracovním prostoru **Elektronické výkaznictví** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
2. V podokně akcí vyberte **Vytvořit konfiguraci**.
3. V rozevíracím dialogovém okně v poli **Název** zadejte **Model pro učení směrných plánů ER**.
4. Vyberte **Vytvořit konfiguraci** pro potvrzení vytvoření nové položky datového modelu ER.

![Dialogové okno Vytvořit konfiguraci – rozevírací seznam.](media/GER-BaselineSample-ModelAdd.PNG "Snímek obrazovky dialogového okna Vytvořit konfiguraci s rozevíracím seznamem")

### <a name="design-a-data-model"></a>Navržení datového modelu

1. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Návrhář**.
2. Zvolte **Nové**.
3. V rozevíracím dialogovém okně do pole **Název** zadejte **Kořen**.
4. Vyberte **přidat**.
5. Vyberte **Kořenová reference**.
6. Vyberte **OK** a potom **Uložit**.
7. Zavřete stránku **Návrhář modelu**.
8. Vyberte **Změnit stav**.
9. Vyberte **Dokončit** a potom **OK**.

![Stránka konfigurace.](media/GER-BaselineSample-ModelComplete.PNG "Snímek obrazovky stránky Konfigurace")

### <a name="add-a-new-er-format-configuration"></a>Přidání nové konfigurace formátu ER

1. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Vytvořit konfiguraci**.
2. V rozevíracím dialogovém okně ve skupině polí **Nový** vyberte možnost **Formát založený na datovém modelu pro učení ER**.
3. Do pole **Název** zadejte **Formát pro učení směrných plánů ER**.
4. Vyberte **Vytvořit konfiguraci** pro potvrzení vytvoření nové položky formátu ER.

![Dialogové okno Vytvořit konfiguraci – rozevírací seznam.](media/GER-BaselineSample-FormatAdd.PNG "Snímek obrazovky dialogového okna Vytvořit konfiguraci s rozevíracím seznamem")

### <a name="design-a-format"></a>Návrh formátu

V tomto příkladu vytvoříte jednoduchý formát ER pro generování dokumentů XML.

1. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Návrhář**.
2. Vyberte **Přidat kořen**.
2. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve stromovém zobrazení vyberte **Společné\\Soubor**.
    2. Do pole **Název** zadejte **Výstup**.
    3. Vyberte **OK**.

3. Vyberte **přidat**.
4. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve stromovém zobrazení vyberte **XML\\Element**.
    2. Do pole **Název** zadejte **Dokument**.
    3. Vyberte **OK**.

5. Ve stromovém zobrazení vyberte **Výstup\\Dokument**.
6. Vyberte **přidat**.
7. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve stromovém zobrazení vyberte **XML\\Attribute**.
    2. Do pole **Název** zadejte **ID**.
    3. Vyberte **OK**.

    ![Stránka návrháře formátu.](media/GER-BaselineSample-FormatLayoutDesign.PNG "Snímek obrazovky stránky Návrhář formátu")

8. Na kartě **Mapování** vyberte **Odstranit**.
9. Vyberte **Přidat kořen**.
10. V rozevíracím dialogovém okně ve stromové struktuře vyberte možnost **Obecný\\vstupní parametr uživatele** a potom postupujte následujícím způsobem:

    1. Do pole **Název** zadejte **ID**.
    2. Do pole **Popisek** zadejte **Zadat ID**.
    3. Vyberte **OK**.

11. Ve stromovém zobrazení vyberte **Výstup\\Dokument\\Id**.
12. Vyberte **Vazba** a potom **Uložit**.

![Stránka návrháře formátu.](media/GER-BaselineSample-FormatMappingDesign.PNG "Snímek obrazovky stránky Návrhář formátu")

Na základě navržené struktury vygeneruje konfigurovaný formát soubor XML. Tento sobor XML obsahuje prvek **Kořen** s atributem **ID** nastaveným na hodnotu, kterou uživatel zadá do dialogového okna ER runtime.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Generování nového směrného plánu pro navržený formát ER

1. Na stránce **Konfigurace** na pevné záložce **Verze** vyberte **Spustit**.
2. Do pole **Zadat ID** zadejte **1**.
3. Vyberte **OK**.

    ![Dialogové okno parametrů elektronického výkaznictví.](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Snímek obrazovky dialogového okna Parametry elektronického výkaznictví")

4. Uloží místní kopii souboru **out.Admin.xml**, který je vygenerován, aby jej bylo možné použít později jako základ pro tento formát ER.

    ![Upozornění na vygenerovaný soubor na stránce Konfigurace.](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Snímek obrazovky upozornění na vygenerovaný soubor na stránce Konfigurace")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Konfigurace parametrů ER tak, aby začaly používat funkci směrného plánu

1. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** vyberte **Parametry uživatelů**.
2. Nastavte možnost **Spustit v režimu ladění** na **Ano**.
3. Vyberte **OK**.

![Dialogové okno Parametry uživatele.](media/GER-BaselineSample-ERUserParameters.PNG "Snímek obrazovky dialogového okna Parametry uživatele")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Přidání nového směrného plánu pro navržený formát ER

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. V podokně akcí zvolte **Směrné plány**.

    ![Tlačítko Směrné plány na stránce Konfigurace.](media/GER-BaselineSample-OpenBaselinePage.PNG "Snímek obrazovky tlačítka Směrné plány na stránce Konfigurace")

3. V podokně akcí zvolte **Nový**.
4. Vyberte dříve navržený formát ER **Formát pro učení směrných plánů ER**.
5. Zvolte možnost **Uložit**.

![Stránka směrného plánu elektronického výkaznictví.](media/GER-BaselineSample-AddBaseline.PNG "Obrazovka stránky se směrným plánem formátu elektronického výkaznictví")

Je přidán směrný plán pro formát **Formát pro učení směrných plánů ER**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Nakonfigurujte pravidlo směrného plánu pro přidaný směrný plán.

1. Na stránce **Směrné plány formátu elektronického výkaznictví** v podokně akcí vyberte tlačítko **Přílohy** (symbol papírové spony).
2. V podokně akcí zvolte **Nový** \> **Soubor**. V parametrech ER měl dříve vybrán **Soubor** jako typ dokumentu, který se používá k ukládání základních souborů, který byl použit k uložení souborů směrného plánu.
3. Vyberte **Procházet** a pak vyberte soubor **out.Admin.xml**, který byl vygenerován při spuštění dříve konfigurovaného formátu ER.

    ![Stránka Přílohy.](media/GER-BaselineSample-UploadBaselineFile.PNG "Snímek obrazovky stránky Přílohy")

4. Zavřete stránku **Přílohy**.
5. Na pevné záložce **Směrné plány** vyberte **Nový**.
6. Do pole **Název** zadejte **Směrný plán 1**.
7. V poli **Název součásti souboru** zadejte nebo vyberte **Výstup**. Tato hodnota označuje, že konfigurovaný směrný plán bude porovnán se souborem, který je generován pomocí prvku formátu **výstup**.
8. Do pole **Maska názvu souboru** zadejte **\*.xml**.

    > [!NOTE]
    > Můžete definovat masku názvu souboru. Je-li definována maska názvu souboru, bude záznam podle směrného plánu použit k vyhodnocení generovaného výstupu pouze v případě, že název výstupního souboru, který je generován, odpovídá této masce.

9. Pokud má být konfigurovaný směrný plán použit pouze v případě, že uživatelé kteří jsou přihlášeni k určitým společnostem, spustili **Formát k učení směrných plánů ER**, vyberte tyto společnosti v poli **Společnosti**.
10. V poli **Směrný plán** zadejte nebo vyberte přílohu **out.Admin**.
11. Zvolte možnost **Uložit**.

![Stránka směrného plánu elektronického výkaznictví.](media/GER-BaselineSample-SetupBaselineLine.PNG "Obrazovka stránky se směrným plánem formátu elektronického výkaznictví")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Spuštění navrženého formát ER a kontrola protokolu pro analýzu výsledků

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Ve stromové struktuře rozbalte **Model k učení směrných plánů** a vyberte **Model k učení směrných plánů\\Formát k učení směrných plánů ER**.
3. Na pevné záložce **Verze** vyberte **Spustit**.
4. Do pole **Zadat ID** zadejte **1**.
5. Vyberte **OK**.
6. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurovat protokoly ladění**.

    ![Stránka protokolů spouštění elektronického výkaznictví.](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Snímek obrazovky stránky protokolů spuštění Parametry elektronického výkaznictví")

    > [!NOTE]
    > Protokol spuštění obsahuje informace o výsledcích porovnání generovaného souboru s nakonfigurovaným směrným plánem. V tomto příkladu protokol udává, že vygenerovaný soubor a směrný plán jsou stejné.

7. Vyberte **Odstranit vše**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Spuštění navrženého formát ER a kontrola protokolu pro analýzu výsledků

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Ve stromové struktuře rozbalte **Model k učení směrných plánů** a vyberte **Model k učení směrných plánů\\Formát k učení směrných plánů ER**.
3. Na pevné záložce **Verze** vyberte **Spustit**.
4. Do pole **Zadat ID** zadejte **2**.
5. Vyberte **OK**.
6. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurovat protokoly ladění**.

    ![Stránka protokolů spouštění elektronického výkaznictví.](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Snímek obrazovky stránky protokolů spuštění Parametry elektronického výkaznictví")

    > [!NOTE]
    > Protokol spuštění obsahuje informace o výsledcích porovnání generovaného souboru s nakonfigurovaným směrným plánem. V tomto příkladu protokol udává, že vygenerovaný soubor a směrný plán nejsou stejné.

7. Vyberte **Porovnat**.

> [!NOTE]
> Vygenerovaný soubor a soubor směrného plánu jsou nabízeny jako soubory zip. Chcete-li porovnat soubory a zkontrolovat rozdíly, můžete použít externí nástroje pro porovnání, jako například WinDiff.

## <a name="additional-resources"></a>Další zdroje

- [Konfigurace architektury elektronického výkaznictví (ER)](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]