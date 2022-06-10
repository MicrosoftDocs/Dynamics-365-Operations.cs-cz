---
title: Zlepšete výkon řešení ER snížením počtu polí tabulky, která jsou načítána za běhu
description: Toto téma pojednává o tom, jak zlepšit výkon řešení ER snížením počtu polí tabulky, která jsou načítána za běhu.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd192a7718ac4fd8bcb636ede6c005ca29ee5f08
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811951"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Zlepšete výkon řešení ER snížením počtu polí tabulky, která jsou načítána za běhu

[!include[banner](../includes/banner.md)]

[Formáty](er-overview-components.md#format-components-for-outgoing-electronic-documents) v modulu [Elektronické výkaznictví](general-electronic-reporting.md) (ER) můžete navrhovat pro generování odchozích dokumentů v různých formátech. Při generování dokumentu formát ER volá zdroje dat, které byly nakonfigurovány v odpovídajícím [mapování modelu](er-overview-components.md#model-mapping-component) ER. Aby bylo možné nakonfigurovat přístup k tabulkám, dotazům nebo entitám aplikace pro načtení záznamu, můžete použít zdroje dat ER typu *záznamy tabulky*. Ve výchozím nastavení zdroj dat typu *Záznamy tabulky* načte hodnoty všech polí v požadovaných záznamech. Tento typ zdroje dat však můžete nakonfigurovat tak, aby načítal pouze hodnoty polí, které jsou vyžadovány pro spouštění formátu ER. Tato konfigurace pomáhá snížit spotřebu paměti aplikačního serveru, který provádí načítání dat a další ukládání záznamů do mezipaměti.

Chcete-li se dozvědět více o tom, jak omezit seznam načtených polí zdrojů dat typu *Záznamy tabulky*, doplňte příklad v tomto tématu.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Příklad: Snižte počet polí tabulky, která se načítají za běhu

Následující postupy ukazují, jak může uživatel v roli správce systému nebo vývojář elektronických sestav konfigurovat mapování modelu ER tak, aby načítalo pouze pole, která jsou vyžadována ke spuštění formátu ER, aby se snížila spotřeba paměti aplikačního serveru.

Tyto postupy lze provést v rámci společnosti **USMF** v Microsoft Dynamics 365 Finance. Není nutné žádné kódování.

K dokončení tohoto příkladu v tomto tématu musíte mít přístup ke společnosti **USMF** pro některou z následujících rolí:

- Funkční konzultant elektronického výkaznictví
- Správce systému

V tomto příkladu použijete [konfigurace](general-electronic-reporting.md#Configuration) ER, které jsou poskytnuty pro vzorovou společnost **Litware, Inc**. Ověřte, že je dostupný poskytovatel konfigurace ukázkové společnosti **Litware, Inc.** (`http://www.litware.com`) uveden pro rámec ER a že označen jako **Aktivní**. Není-li tento poskytovatel konfigurace uveden v seznamu nebo není-li označen jako **Aktivní**, postupujte podle kroků v tématu [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>Konfigurace rámce ER

Postupujte podle kroků uvedených v části [Konfigurace architektury ER](er-quick-start2-customize-report.md#ConfigureFramework) a nastavte minimální sadu parametrů ER. Toto nastavení musíte dokončit, než začnete používat architekturu ER k úpravě datových zdrojů poskytnutého řešení ER.

### <a name="import-the-sample-er-configurations"></a>Import ukázkových konfigurací elektronického výkaznictví

Pokud jste ještě nedokončili příklad v tématu [Navrhněte nové řešení ER pro tisk vlastní sestavy](er-quick-start1-new-solution.md), stáhněte a lokálně uložte soubory XML pro následující konfigurace poskytovaného řešení ER.

| Popis obsahu            | Název souboru |
|--------------------------------|-----------|
| Konfigurace datového modelu elektronického výkaznictví    | [Dotazník model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| Konfigurace mapování modelu elektronického výkaznictví | [Dotazník mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| Konfigurace formátu elektronického výkaznictví        | [Dotazník format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Poté postupujte podle těchto kroků a nahrajte konfigurace poskytnutého řešení ER do vaší instance Finance.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Na stránce **Konfigurace** importujte konfiguraci datového modelu ER.

    1. Vyberte **Exchange** a poté vyberte **Načíst ze souboru XML**.
    2. Vyberte **Procházet**, najděte a vyberte soubor **Questionnaires model.version.1.xml** a pak vyberte **OK**.

4. Importujte konfiguraci mapování modelu ER.

    1. Vyberte **Exchange** a poté vyberte **Načíst ze souboru XML**.
    2. Vyberte **Procházet**, najděte a vyberte soubor **Questionnaires mapping.1.1.xml** a vyberte **OK**.

5. Import konfigurace formátu elektronického výkaznictví.

    1. Vyberte **Exchange** a poté vyberte **Načíst ze souboru XML**.
    2. Vyberte **Procházet**, najděte a vyberte soubor **Questionnaires format.1.1.xml** a vyberte **OK**.

6. Ve stromu konfigurace rozbalte **Model dotazníků**.
7. Zkontrolujte seznam importovaných konfigurací elektronického výkaznictví ve stromu konfigurace.

    ![Kontrola seznamu importovaných konfigurací ER na stránce Konfigurace.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Kontrola poskytnutého mapování modelu ER

1. Na stránce **Konfigurace** zvolte **Mapování dotazníků**.
2. V podokně akcí zvolte **Návrhář**.
3. Na stránce **Mapování modelu k datovým zdrojům** vyberte **Designer**.
4. Na stránce **Designer mapování modelů** vyberte v podokně akcí **Skupinové zobrazení** a zapněte **Skupinové** zobrazení.
5. V podokně **Datový model** rozbalte **Dotazník**.

    Všimněte si, že pro přístup k aplikační tabulce `KMCollection`, byl nakonfigurován zdroj dat **Dotazník**.

6. V podokně **Zdroje dat** rozbalte **Záznamy tabulky** \> **Dotazník** \> **Pole**.

    Všimněte si, kolik polí z aplikační tabulky `KMCollection` jsou vystaveny zdrojem dat **Dotazník** typu *Záznamy tabulky*.

    ![Kontrola poskytnutého mapování modelu na stránce Designer mapování modelu, když je zapnuté skupinové zobrazení.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. V podokně akcí opět vyberte **Skupinové zobrazení** a vypněte **Skupinové** zobrazení, poté vyberte **Ukázat vše** \> **Zobrazit pouze namapované**.

    Všimněte si, že několik polí aplikační tabulky `KMCollection` slouží k vyplnění seznamu záznamů **Dotazník** v datovém modelu ER:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Kontrola poskytnutého mapování modelu na stránce Designer mapování modelu, když je vypnuté skupinové zobrazení.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>Zapnutí sledování výkonu elektronického výkaznictví

Postupujte podle kroků v [Zapněte trasování výkonu ER](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) pro nastavení uživatelských parametrů ER, které umožňují sledování provádění komponent ER.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Spusťte poskytnutý formát ER pomocí dodaného mapování modelu

Postupujte podle kroků v [Spusťte navržený formát z ER](er-quick-start1-new-solution.md#RunFormatFromER), chcete-li spustit poskytnutý formát ER pro jeden dotazník ze stránky **Konfigurace**.

### <a name="review-the-execution-trace-of-the-first-run"></a>Kontrola sledování spuštění prvního spuštění.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví \> Konfigurace**.
2. Na stránce **Konfigurace** rozbalte **Model dotazníků** a vyberte **Mapování dotazníků**.

    > [!NOTE]
    > Podrobnosti na pevné záložce **Verze** označuje, že jste vybrali verzi konceptu konfigurace **Mapování dotazníků**. Proto můžete upravit obsah tohoto mapování modelu.

3. V podokně akcí zvolte **Návrhář**.
4. Na stránce **Mapování modelu k datovým zdrojům** vyberte **Designer**.
5. Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.
6. V dialogovém okně **Nastavení výsledků sledování výkonu** vyberte trasování, které bylo vygenerováno během posledního spuštění formátování.

    ![Výběr trasování v dialogovém okně Nastavení výsledků trasování výkonu.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Vyberte **OK**. 
8. Na pevné záložce **Podrobnosti** filtrujte cestu **Dotazník**, která ukazuje na zdroj dat **Dotazník**.
9. Zkontrolujte podrobnosti databázového dotazu, který byl vygenerován, když byl volán zdroj dat **Dotazník**.

    Všimněte si, že všechna pole aplikační tabulky `KMCollection` byly načteny za běhu, když byl volán zdroj dat **Dotazník**.

    ![Kontrola podrobností databázového dotazu na stránce Designer mapování modelu.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Úprava poskytnutého mapování modelu ER

1. Na stránce **Návrhář mapování modelu** v podokně **Datové zdroje** zvolte zdroj dat **Dotazník**.
2. V podokně **Zdroje dat** vyberte **Upravit**.
3. V dialogovém okně **Vlastnosti zdroje dat** vyberte **Výběr polí**, chcete-li specifikovat seznam polí odkazované aplikační tabulky `KMCollection`, která bude načtena za běhu, když je volán upravitelný zdroj dat **Dotazník**.

    ![V dialogovém okně Vlastnosti zdroje dat vyberte Výběr polí, chcete-li začít upravovat seznam polí , které budou načteny z aplikační tabulky za použití upravitelného zdroje dat.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Na stránce **Výběr polí** vyberte **Automaticky vyplnit**.

    Seznam **Vybraná pole** je automaticky vyplněn na základě předem nakonfigurovaných artefaktů mapování modelu. Do seznamu se přidají všechna pole a vztahy odkazované tabulky, které jsou uvedeny v jakékoli vazbě, vzorci nebo zdroji dat mapování modelu.

    ![Konfigurace seznamu polí, která budou načtena z tabulky aplikace na stránce Výběr polí.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Vyberte **Uložit** a zavřete stránku **Výběr polí**.
6. Vyberte **OK** pro uložení změn, které jste provedli v nastavení zdroje dat.
7. V podokně akcí zvolte **Zobrazit vše**.

    Všimněte si, že zdroj dat **Dotazník** nyní zobrazuje text **\<Fields are filtered\>**. Tento text označuje, že zdroj dat byl nakonfigurován tak, aby načítal omezený počet polí z tabulky odkazované aplikace.

    ![Kontrola aktualizovaného mapování modelu na stránce Designer mapování modelu.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Vyberte **Uložit** pro uložení změn, které jste provedli v upravitelném mapování modelu.

    > [!NOTE]
    > Za běhu ER analyzuje přidané vztahy a přidá všechna pole, která se v nich používají, do databázového dotazu, i když tato pole nebyla explicitně přidána do seznamu načtených polí v době návrhu.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Spusťte poskytnutý formát ER pomocí aktualizovaného mapování modelu

Postupujte podle kroků v [Spusťte navržený formát z ER](er-quick-start1-new-solution.md#RunFormatFromER), chcete-li spustit poskytnutý formát ER pro jeden dotazník ze stránky **Konfigurace**.

### <a name="review-the-execution-trace-of-the-second-run"></a>Kontrola sledování spuštění druhého spuštění

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** rozbalte **Model dotazníků** a vyberte **Mapování dotazníků**.
3. V podokně akcí zvolte **Návrhář**.
4. Na stránce **Mapování modelu k datovým zdrojům** vyberte **Designer**.
5. Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.
6. V dialogovém okně **Nastavení výsledků sledování výkonu** vyberte trasování, které bylo vygenerováno během posledního spuštění formátování.
7. Vyberte **OK**.
8. Na pevné záložce **Podrobnosti** filtrujte cestu **Dotazník**, která ukazuje na zdroj dat **Dotazník**.
9. Zkontrolujte podrobnosti databázového dotazu, který byl vygenerován, když byl volán zdroj dat **Dotazník**.

    Všimněte si, že pouze pole, která jsou vyžadována k vyplnění zdroje dat, byla za běhu načtena z aplikační tabulky `KMCollection`, když byl volán zdroj dat **Dotazník**.

    > [!NOTE]
    > Některá pole, jako jsou pole pro ID oddílu, ID datové oblasti a ID záznamu, jsou automaticky přidána rámcem Správy dat aplikace Finance.

    ![Kontrola podrobností databázového dotazu pro mapování aktualizovaého modelu na stránce Designer mapování modelu.](./media/er-reduce-fetched-fields-number-query2.png)

Tuto techniku můžete použít ke snížení počtu načtených záznamů, když musíte snížit spotřebu paměti běžícím mapováním modelu ER a formátem ER.

## <a name="limitations"></a>Omezení

Když omezíte počet načtených polí pro zdroj dat typu *Záznamy tabulky*, nemůžete použít metody tabulky aplikace, na kterou odkazuje zdroj dat, protože metadata aplikace neposkytují informace o polích tabulky, která jsou nutná k volání těchto metod.

## <a name="usage-notes"></a>Poznámky k použití

Ačkoliv příkaz **Automatické vyplňování** automaticky přidá pole, automaticky neodstraní dříve přidaná pole, i když se již nepoužívají ve vazbách, vzorcích a zdrojích dat upravitelného mapování modelu.

Když vyberete **Automatické vyplňování**, ER analyzuje vazby, vzorce a zdroje dat, které mělo mapování upravitelného modelu, když jste jej otevřeli pro úpravy. Pokud změníte vazby, vzorce a zdroje dat upravitelného mapování modelu a chcete použít příkaz **Automatické vyplňování**, zavřete návrhář mapování modelu a poté jej znovu otevřete, abyste mohli upravit mapování modelu. 

## <a name="additional-resources"></a>Další prostředky

- [Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md)
- [Odstraňování problémů s výkonem v konfiguracích ER](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
