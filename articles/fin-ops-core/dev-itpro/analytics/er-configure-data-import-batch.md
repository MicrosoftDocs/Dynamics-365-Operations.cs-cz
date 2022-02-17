---
title: Import dat z ručně vybraných souborů v dávkovém režimu
description: Toto téma vysvětluje, jak importovat data z ručně vybraných souborů v dávkovém režimu.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075601"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Import dat z ručně vybraných souborů v dávkovém režimu

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Chcete-li použít rámec [Elektronické vykazování (ER)](general-electronic-reporting.md) pro import dat z ručně vybraných příchozích souborů v dávkovém režimu, nakonfigurujte [formát](er-overview-components.md#format-component) ER, který podporuje import. Poté spusťte [mapování modelu](er-overview-components.md#model-mapping-component) typu **Do cíle**, který používá tento formát jako zdroj dat. Pokud chcete provést import dat, přejděte do souboru, který chcete importovat, a ručně ho vyberte. 

Nová funkce ER, která podporuje import dat v dávkovém režimu umožňuje tento proces konfigurovat jako bezobslužný. Konfigurace ER můžete použít k provedení importu dat naplánováním nové dávkové úlohy z uživatelského rozhraní (UI) ER.

Toto téma vysvětluje, jak importovat data z ručně vybraného souboru v dávkovém režimu. Tyto příklady používají transakcí dodavatele jako obchodní data. Kroky těchto příkladů lze provést ve společnosti **USMF**. Není nutné žádné kódování.

## <a name="prerequisites"></a>Předpoklady

Pro dokončení příkladů v tomto tématu musíte mít následující přístup:

- Jedna z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Konfigurace formátu a modelu ER pro platby 1099

### <a name="create-the-required-er-configurations"></a>Vytvoření požadovaných konfigurací ER

Chcete-li vytvořit požadované konfigurace ER a získat další předpoklady, postupujte podle jednoho z těchto kroků:

- Přehrajte si průvodce záznamem úloh **ER Import dat ze souboru aplikace Microsoft Excel**, které jsou součástí obchodního procesu **7.5.4.3 Acquire/Develop IT service/solution components (10677)**. Tito průvodci záznamem úloh vás provedou procesem navrhování a použití konfigurací ER pro interaktivní import transakcí dodavatele z externích souborů aplikace Microsoft Excel. Další informace naleznete v tématu [analýza příchozích dokumentů do formátu Excel](parse-incoming-documents-excel.md).
- Proveďte příklady v části [Konfigurace importu dat z SharePoint](er-configure-data-import-sharepoint.md). Tyto příklady vás provedou procesem navrhování a použití konfigurací ER pro interaktivní import transakcí dodavatele ze souborů Excel, které jsou uloženy ve složce SharePoint.

### <a name="download-the-required-er-configurations"></a>Stažení požadovaných konfigurací ER

1. Stáhněte a lokálně uložte následující konfigurace ER.

    | Popis obsahu | Soubor |
    |---------------------|------|
    | Konfigurace datového modelu ER **Model platby 1099** | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | Konfigurace formátu ER **Pro import transakcí dodavatelů (Excel)** | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Použijte možnost ER [Načíst ze souboru XML](er-defer-sequence-element.md#import-the-sample-er-configurations) pro import stažených konfigurací ER do vaší instance Dynamics 365 Finance v následujícím pořadí:

    1. Konfigurace datového modelu elektronického výkaznictví
    2. Konfigurace formátu elektronického výkaznictví

### <a name="download-the-required-excel-files"></a>Stažení požadovaných souborů Excel

- Stáhněte si následující ukázkovou datovou sadu a uložte ji místně.

    | Popis obsahu | Soubor |
    |---------------------|------|
    | Příchozí soubor **1099import-data.xlsx**, který obsahuje ukázková data pro import | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Kontrola předpokladů

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** zkontrolujte připravené ER řešení pro import dat v dávkovém režimu.
3. Zkontrolujte konfiguraci formátu **Pro import transakcí dodavatelů (Excel)**.

    - Komponenta formátu této konfigurace je navržena tak, aby analyzovala příchozí soubor aplikace Excel.
    - Komponenta mapování modelu této konfigurace se používá k vyplnění základního datového modelu pomocí dat z analyzovaného souboru Excel.

    ![Konfigurace formátu ER pro import dat v dávkovém režimu z uživatelského rozhraní ER.](./media/er-configure-data-import-batch-configurations-1.png)

4. Zkontrolujte konfiguraci datového modelu ER **Model platby 1099**.

    - Komponenta modelu této konfigurace představuje strukturu datového modelu, který se používá k předávání dat mezi spuštěními komponentami ER.
    - Komponenta mapování modelu této konfigurace se používá k získávání dat z vykonávané komponenty formátu a následné aktualizaci tabulek aplikace.

    ![Konfigurace datového modelu ER pro import dat v dávkovém režimu z uživatelského rozhraní ER.](./media/er-configure-data-import-batch-configurations-2.png)

5. Otevřete soubor **1099import-data.xlsx** v Excelu.

    ![Ukázkový soubor Excel s daty pro import v dávkovém režimu.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Aktivace dávkového importu dat pro ER z uživatelského rozhraní

1. Přejděte do nabídky **Správa systému** \> **Pracovní prostory** \> **Správa funkcí**.
2. V pracovním prostoru **Správa funkcí** vyberte funkci **Spustit import ER ručně nahraných dokumentů v dávce** a poté vyberte **Aktivovat**.

## <a name="import-data-from-manually-selected-excel-files"></a>Import dat z ručně vybraných souborů Excel

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** vyberte konfiguraci datového modelu **Model platby 1099**.
3. Na pevné záložce **Konfigurační komponenty** vyberte odkaz **Pro import ručních transakcí 1099**.
4. Na stránce **Mapování modelu na zdroj dat** je předem vybrané mapování modelu **Pro ruční import transakcí 1099**. Vyberte **Spustit**.
5. Na kartě **Parametry** vyberte **Procházet**. Vyhledejte a vyberte soubor **1099import-data.xlsx** a poté vyberte **OK**.
6. Do pole **Zadat ID dokladu** zadejte **V-00001**.
7. Na kartě **Spustit na pozadí** nastavte možnost **Dávkové zpracování** na **Ano**.

    Všimněte si, že pole **Popis ulohy** je nastaveno na **Spuštění mapování modelu „Pro ruční import transakcí 1099“, konfigurace „Model plateb 1099“**. Tato hodnota označuje, že provedení mapování vybraného modelu bude naplánováno jako nová dávková úloha.

    ![Zadání podrobností o importu dat v dávkovém režimu v dialogovém okně Parametry elektronické zprávy.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Vyberte **OK**. Zpráva vás upozorní, že byla naplánována nová dávková úloha.

    ![Zpráva o nové naplánované dávkové úloze na stránce mapování modelu na zdroj dat.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Zkontrolujte výsledky importu dat na stránce Dávková úloha

1. Přejděte na **Společné** \> **Dotazy** \> **Dávkové úlohy** \> **Moje dávkové úlohy**.
2. Na stránce **Dávková úloha** filtrujte seznam dávkových úloh, abyste našli naplánovanou dávku, a pak ji vyberte.
3. Vyberte **ID úlohy** pro zobrazení údajů o úloze.
4. Na pevné záložce **Dávkové úkoly** vyberte **Protokolovat**.

    ![Tlačítko Protokolovat na stránce Dávková úloha.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Zkontrolujte údaje o spuštění.

    ![Protokol spuštění naplánované dávkové úlohy na stránce Dávková úloha.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Změna parametrů importu dat

Po naplánování vaší dávky a v době, kdy ještě nebyla spuštěna, můžete změnit parametry plánovaného importu dat.

1. Přejděte na **Společné** \> **Dotazy** \> **Dávkové úlohy** \> **Moje dávkové úlohy**.
2. Na stránce **Dávková úloha** filtrujte seznam dávkových úloh, abyste našli naplánovanou dávku, a pak ji vyberte.
3. Vyberte **Změnit stav**.
4. V dialogovém okně **Vybrat nový stav** vyberte **Srážka** a pak vyberte možnost **OK**.
5. Vyberte odkaz **ID úlohy** pro přístup k údajům o úloze.
6. Na pevné záložce **Dávkové úkoly** vyberte **Parametry**.
7. V dialogovém okně **Parametry elektronické sestavy** postupujte následovně:

    1. Vyberte **Procházet** pro výběr alternativního souboru pro import dat.
    2. Vyberte **Zadat ID dokladu** pro změnu čísla dokladu pro import transakcí dodavatele.

        ![Změna parametrů importu dat pro naplánovanou dávkovou úlohu v dialogovém okně Parametry elektronické sestavy.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Vyberte **OK**.

8. Ujistěte se, že je dávka stále vybraná, a poté znovu vyberte **Změnit stav**.
9. V dialogovém okně **Vybrat nový stav** vyberte **Čekání** a pak vyberte možnost **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Zkontrolujte výsledky importu dat na stránce zdroj ER

1. Přejděte na **Správa organizace** \> **Elektronická sestava** \> **Úlohy elektronických sestav**.
2. Vyberte záznam **Pro import transakcí dodavatelů (Excel)**, který byl automaticky vytvořen během importu dat.

    ![Záznam pro konfiguraci Pro import transakcí dodavatelů (Excel) na stránce Zdroj elektronického vykazování.](./media/er-configure-data-import-batch-files-source-1.png)

3. Vyberte **Stavy souboru pro zdroje**.
4. Na pevných záložkách **Soubory** a **Zdrojové protokoly pro formát importu** zkontrolujte podrobnosti importu.
5. Na pevné záložce **Soubory** vyberte záznam. Všimněte si, že importovaný soubor je připojen k tomuto záznamu.

    ![Importovaný soubor připojený k záznamu na stránce Stavy souboru na stránce zdrojů.](./media/er-configure-data-import-batch-files-source-2.png)

6. Vyberte **Přílohy** pro kontrolu importovaného souboru.

    ![Importovaný soubor na stránce zobrazení dokumentu.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > K uchování těchto příloh používá rámec ER typ dokumentu, který je [nastaven](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) pro současnou společnost v poli **Ostatní** parametrů ER.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Zkontrolujte výsledky importu dat na stránce Vyrovnání dodavatele za 1099s

1. Přejděte na **Závazky** \> **Pravidelné úlohy** \> **Daň 1099** \> **Vyrovnání dodavatele pro sestavy 1099**.
2. V poli **Od data** zadejte **12/31/2017** (31. prosinec 2017).
3. Vyberte **Ruční transakce 1099**.

    ![Importované transakce dodavatele na stránce transakcí Daň 1099.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
