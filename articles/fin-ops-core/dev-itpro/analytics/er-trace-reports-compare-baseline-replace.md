---
title: Vylepšení sledování výsledků vygenerovaných sestav elektronického výkaznictví pro porovnání se základními hodnotami
description: Tento článek popisuje vylepšení funkce základní úrovně ER v Microsoft Dynamics 365 Finance verze 10.0.3 (červen 2019).
author: NickSelin
ms.date: 06/19/2019
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
ms.openlocfilehash: bb2e76492ac9f6feb71811d0fbfd25919b59ac4d
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109135"
---
# <a name="improve-tracing-the-results-of-generated-er-reports-to-compare-with-baseline-values"></a>Vylepšení sledování výsledků vygenerovaných sestav elektronického výkaznictví pro porovnání se základními hodnotami

[!include[banner](../includes/banner.md)]

V tomto článku je popsána první sada vylepšení, která byla provedena ve funkci směrného plánu systému elektronického výkaznictví (ER). Tato vylepšení jsou k dispozici v aplikaci Microsoft Dynamics 365 Finance verze 10.0.3 (červen 2019) a novějších.

## <a name="automate-the-setting-of-baseline-rules"></a>Automatizace nastavení pravidel směrného plánu

Článek [Sledování generovaných výsledků sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md) vysvětluje, jak konfigurovat rámec ER na shromažďování informací o spouštění formátu ER a vyhodnotit výsledky těchto spuštění. Příklad v tomto článku obsahuje kroky, které je nutné provést.

Tady jsou některé kroky:

- Chcete-li generovat odchozí soubor, spusťte formát ER a soubor uložte lokálně.
- Přidejte lokálně uložený soubor jako přílohu směrného plánu, který byl přidán do formátu ER.
- Nakonfigurujte pravidlo směrného plánu pro přidaný směrný plán. Tato konfigurace zahrnuje následující kroky:

    - Určete formátovací prvek ER, který slouží k vygenerování odchozího souboru.
    - Vyberte přílohu, která odkazuje na generovaný výstupní soubor.

> [!NOTE]
> Tyto kroky je nutné provést ručně, přestože nové schopnosti ER umožňují jejich automatizované provedení. Chcete-li získat další informace o této funkci, vyplňte následující příklad.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Příklad: Automatizace nastavení pravidel směrného plánu

Chcete-li dokončit kroky v tomto příkladu, musíte nejprve dokončit kroky v příkladu v článku [Sledování generovaných výsledků sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md), a to až do části Přidání nového směrného plánu pro navržený formát ER.

### <a name="review-added-baseline"></a>Kontrola přidaného směrného plánu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Vyberte **Směrné plány**.

    > [!NOTE]
    > Tlačítko **Směrný plán** v podokně akcí je k dispozici pouze v případě že je pro aktuální společnost zapnutý parametr ER **Spustit v režimu ladění**.

Směrný plán byl přidán k vybranému **Formátu pro osvojení si směrných plánů**, ale pravidla směrného plánu pro tento směrný plán ještě nebyla přidána.

![Stránka směrného plánu elektronického výkaznictví, zatím žádná pravidla.](media/GER-BaselineSample-AddBaseline2.PNG "Obrazovka stránky se směrným plánem formátu elektronického výkaznictví")

### <a name="make-a-new-baseline-rule"></a>Vtvoření nového pravidla směrného plánu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Ve stromové struktuře rozbalte **Model pro učení směrných plánů ER**.
3. Ve stromové struktuře vyberte **Model pro učení směrných plánů ER\\Formát pro učení směrných plánů ER**.
4. Na pevné záložce **Verze** vyberte **Spustit**.
5. Do pole **Zadat ID** zadejte **1**.
6. Nastavte volbu **vytvořit soubory směrného plánu** na **Ano**.
7. Vyberte **OK**.
8. Vyberte **Směrné plány**.

    ![Stránka se směrným plánem formátu elektronického výkaznictví, vybrané základní plány.](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Obrazovka stránky se směrným plánem formátu elektronického výkaznictví")

    Generovaný výstupní soubor byl automaticky připojen ke směrnému plánu provedeného formátu ER. Do tohoto směrného plánu bylo automaticky přidáno pravidlo směrného plánu, které obsahuje také odkaz na připojený soubor.

9. Do pole **Název** zadejte **Směrný plán 1**.
10. Do pole **Maska názvu souboru** zadejte **.xml**.
11. Zvolte **Uložit**.

### <a name="run-the-format"></a>Spuštění formátu

Nyní můžete dokončit zbývající kroky v příkladu v článku [Sledování generovaných výsledků sestavy a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md), počínaje částí Spuštění navrženého formátu ER a kontrola protokolu k analýze výsledků.

> [!NOTE]
> Odstraníte-li automaticky přidané pravidlo směrného plánu na pevné záložce **Směrné plány**, odkazovaná příloha nebude automaticky odstraněna.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Konfigurace směrného plánu tak, aby ignoroval neustále se měnící části výstupu ER

Pokud byl formát ER navržen tak, aby obsahoval informace, které se změní při spuštění formátu, musí být formát vyžadován pro použití funkce směrného plánu pro porovnání generovaných výsledků s hodnotami podle směrného plánu. Informace mohou být například datum a čas zpracování nebo jedinečný identifikátor vygenerovaného dokumentu v různých formátech (globálně jedinečný identifikátor \[GUID\] atd.). Nové možnosti ER umožňují konfigurovat pravidlo směrného plánu tak, aby při spuštění formátu s cílem porovnání hodnot podle směrného plánu s výsledky provádění formátu ignorovalo změny ve formátu ER. Chcete-li získat další informace o této funkci, vyplňte následující příklad.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Příklad: Konfigurace směrného plánu tak, aby ignoroval neustále se měnící části výstupu ER

Chcete-li dokončit kroky v tomto příkladu, musíte nejprve dokončit kroky v příkladu v článku [Sledování generovaných výsledků sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md).

### <a name="modify-a-configured-er-format"></a>Úprava konfigurovaného formátu ER

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Ve stromové struktuře rozbalte **Model pro učení směrných plánů ER**.
3. Ve stromové struktuře vyberte **Model pro učení směrných plánů ER\\Formát pro učení směrných plánů ER**.
4. Vyberte možnost **Návrhář**.
5. Ve stromovém zobrazení vyberte **Výstup\\Dokument**.
6. Vyberte **přidat**.
7. V rozevíracím dialogovém okně ve stromu vyberte **XML\\Atribut**.
8. Do pole **Název** zadejte **ProcessingDateTime**.
9. Vyberte **OK**.
10. Na kartě **mapování** ve stromové struktuře vyberte **Output\\Document\\ProcessingDateTime.**
11. Vyberte možnost **Upravit vzorec**.
12. Do pole **Vzorec** zadejte následující výraz: **DATETIMEFORMAT(NOW(), "O")**
13. Vyberte **Uložit** a potom **Test**.
14. Pokud chcete znovu otestovat konfigurovaný výraz, znovu vyberte **Test**.

    ![Stránka Návrhář receptur.](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Snímek obrazovky stránky Návrhář receptur")

    > [!NOTE]
    > Na kartě **Výsledek** testu se zobrazuje, že konfigurovaný výraz vrací při každém volání jinou hodnotu data a času.

15. Vyberte stránku **Návrhář vzorců** a potom **Uložit**.

    ![Stránka návrháře formátu.](media/GER-BaselineSample-FormatMappingDesign2.PNG "Snímek obrazovky stránky Návrhář formátu")

16. Zavřete stránku **Návrhář formátu**.

### <a name="remove-an-existing-baseline-rule"></a>Odebrání existujícího pravidla směrného plánu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Vyberte **Směrné plány**.
3. V seznamu směrných plánů vyberte směrný plán, který je nakonfigurován pro **Formát pro učení směrných plánů**.
4. Na pevné záložce **Směrné plány** vyberte **Odstranit** k odebrání dříve vytvořeného pravidla směrného plánu.

![Stránka směrného plánu elektronického výkaznictví, odstraněná.](media/GER-BaselineSample-AddBaseline3.PNG "Obrazovka stránky se směrným plánem formátu elektronického výkaznictví")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Definování náhrad pro vazby navrženého formátu ER

1. Na stránce **Konfigurace** na pevné záložce **Náhrady** vyberte **Vybrat komponenty**.
2. Ve stromu komponent formátu rozbalte **Výstup**, rozbalte **Výstup\\Dokument** a zaškrtněte políčko **Výstup\\Dokument\\ProcessingDateTime**.
3. Vyberte **OK**.

![Stránka směrného plánu elektronického výkaznictví, komponenty.](media/GER-BaselineSample-AddBaseline4.PNG "Obrazovka stránky se směrným plánem formátu elektronického výkaznictví")

Vybraná koponenta formátu ER byla přidána do seznamu komponent na pevné záložce **Náhrady**. Při spuštění základního formátu ER v režimu ladění bude vazba formátu pro každou součást nahrazena vazbou, která je zobrazena ve sloupci **vazba**. Chcete-li změnit výchozí vazbu pro komponentu, která je uvedena na pevné záložce **Náhrady**, vyberte **Upravit**.

### <a name="make-a-new-baseline-rule"></a>Vtvoření nového pravidla směrného plánu

Postupujte podle kroků v části Příklad: automatizace nastavení pravidel směrného plánu dříve v tomto článku. Zobrazí se upozornění, že výstupní soubor byl vygenerován pomocí nastavení směrného plánu a že došlo k vynucenému nahrazení vazeb formátu.

![Oznámení na stránce Konfigurace.](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Snímek obrazovky oznámení na stránce Konfigurace")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Potlačení upozornění na náhradní vazby formátu

Nastavením specifických parametrů ER můžete potlačit upozornění na nahrazení formátovacích vazeb. Toto potlačení může být užitečné, pokud jsou formátovací vazby nahrazeny bezobslužným režimem pomocí Regression Suite Automation Tool. V tomto případě může být upozornění považováno za selhání testovacího případu, který běží.

1. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** vyberte **Parametry uživatelů**.
2. Nastavte volbu **potlačit upozornění** podle směrného plánu na hodnotu **Ano** a pak klikněte na tlačítko **OK**.

### <a name="review-the-generated-baseline-file"></a>Kontrola generovaného souboru směrného plánu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Vyberte **Směrné plány**.
3. Vyberte **Přílohy**.
    > [!NOTE]
    > Vygenerovaný soubor obsahuje text data a času zpracování (**"#"**) z vazby, která byla nakonfigurována v přidaném základním pravidlu, ne z vazby formátu.
    
4. Zavřete stránku **Přílohy**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Spuštění navrženého formát ER a kontrola protokolu pro analýzu výsledků

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Ve stromové struktuře rozbalte **Model pro učení směrných plánů ER**.
3. Ve stromové struktuře vyberte **Model pro učení směrných plánů ER\\Formát pro učení směrných plánů ER**.
4. Na pevné záložce **Verze** vyberte **Spustit**.
5. Do pole **Zadat ID** zadejte **1**.
6. Vyberte **OK**.
7. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurovat protokoly ladění**.

Protokol spuštění obsahuje informace o výsledcích porovnání generovaného souboru s nakonfigurovaným směrným plánem. Protokol označuje, že vygenerovaný soubor a směrný plán jsou stejné, přestože spuštěný formát obsahuje vazbu k zadání neustále se měnící hodnoty data a času v odchozím souboru.

> [!NOTE]
> Přestože byl výstupní soubor vygenerován pomocí nastavení směrného plánu, které vynutí nahrazení vazeb formátu, neobdržíte žádná upozornění o náhradě.

## <a name="exchange-baseline-settings-between-environments"></a>Výměna nastavení směrného plánu mezi prostředími

### <a name="export-baseline-settings"></a>Export nastavení směrného plánu

Nové možnosti ER umožňují exportovat nastavení směrného plánu pro vybraný formát ER z aktuálního prostředí a uložit je jako soubory XML. 

Pokud chcete exportovat nastavení směrného plánu, na stránce **Směrné plány formátu elektrického výkaznictví** vyberte **Export**.

### <a name="import-baseline-settings"></a>Importovat základní nastavení

Exportované nastavení směrného plánu lze importovat do prostředí. Prostředí musí být nejprve importováno jako formát ER. Poté můžete importovat nastavení směrného plánu.

Pokud chcete importovat nastavení směrného plánu z lokálně uloženého souboru XML, na stránce **Směrné plány formátu elektronického výkaznictví** vyberte **Import** a potom po kliknutí na **Procházet** vyberte soubor XML.

![Dialogové okno Importovat základní nastavení.](media/GER-BaselineSample-ImportBaseline1.PNG "Snímek obrazovky dialogového okna Import nastavení směrného plánu")

Chcete-li importovat nastavení směrného plánu ze souboru XML, který je uložen na serveru SharePoint společnosti Microsoft na základě aktuálního nastavení správy dokumentů a vybraného typu dokumentu, na stránce **Směrné plány formátu elektronického výkaznictví** vyberte možnost **Importovat ze zdroje**. Pak vyberte typ dokumentu a soubor XML. Požadovaný typ dokumentu pro přístup do složky SharePoint musí být nakonfigurován předem.

![Dialogové okno Importovat ze zdroje.](media/GER-BaselineSample-ImportBaseline2.PNG "Snímek obrazovky dialogového okna Import ze zdroje")

> [!NOTE]
> Pomocí záznamníku úkolů můžete zaznamenat postup pro výběr požadovaného typu dokumentu a název souboru v dialogovém okně **Importovat ze zdroje**. Tímto způsobem můžete ponechat požadované nastavení směrného plánu na serveru SharePoint a poté je automaticky importovat přehráním záznamu úkolu při spuštění automatizovaných testů pomocí nástroje Regression Suite Automation Tool.

## <a name="additional-resources"></a>Další zdroje

- [Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami](er-trace-reports-compare-baseline.md)
- [Zdroje záznamníku úloh](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

