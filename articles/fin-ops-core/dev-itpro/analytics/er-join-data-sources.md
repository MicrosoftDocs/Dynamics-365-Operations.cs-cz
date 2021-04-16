---
title: Použití zdrojů dat JOIN v mapování modelu ER k získání dat z více aplikačních tabulek
description: Toto téma vysvětluje, jak je možné používat datové zdroje JOIN mezi více společnostmi v modulu Elektronické výkaznictví (ER).
author: NickSelin
ms.date: 05/04/2020
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
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: d42016b914d7992b6f4ae1c573eb8f867ba87e22
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743970"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Použití zdrojů dat JOIN v mapování modelu elektrického vykazování (ER) k získání dat z více aplikačních tabulek

[!include[banner](../includes/banner.md)]

Při konfiguraci mapování nebo formátů služby elektronického vykazování (ER) můžete [přidat](#review) požadované zdroje dat typu **Join**. V době návrhu je zdroj dat **Join** konfigurován jako sada několika datových zdrojů, z nichž každá vrací seznam záznamů. U každého zdroje dat s výjimkou prvního je nutné definovat nezbytné podmínky pro spojení se záznamy o aktuálních a předchozích zdrojích dat. V době běhu konfigurovaný zdroj dat typu **Join** [vrátí](#executeERformat) jediný sloučený seznam záznamů, který obsahuje pole ze záznamů vnořených datových zdrojů.

V současné době jsou podporovány následující typy spojení:

- Vnější (levé) spojení:
    - Spojte všechny záznamy prvního (nejvíce vlevo) zdroje dat a pak všechny požadavky v souladu s konfigurovanými záznamy druhého (nejvíce vpravo) zdroje dat.
- Vnitřní (pravé) spojení:
    - Spojte pouze záznamy prvního (nejvíce vlevo) zdroje dat a pak pouze záznamy druhého (pravého) zdroje dat vzájemně si odpovídající podle konfigurovaných podmínek.

V konfigurovaném zdroji dat **připojení**, když jsou všechny zdroje dat typu **Záznamy tabulky**, lze spuštění zdroje dat Připojení [provést na úrovni databáze](#analyze) pomocí jediného příkazu SQL. Tento příkaz snižuje počet volání databáze, což zlepšuje výkon mapování modelu. V opačném případě se spuštění zdroje **propojení dat** provádí v paměti.

> [!NOTE]
> Použití funkce **VALUEIN** ve výrazech ER, které určují podmínky pro spojení záznamů ve zdrojích dat typu spojení ještě není podporováno. Pro více podrobností o této funkci navštivte stránku [Návrhář receptury v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md).

Chcete-li získat další informace o této funkci, vyplňte příklad tomto tématu.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Příklad: použití zdrojů dat JOIN v mapování modelu ER

Následující postup vysvětluje, jak může správce systému nebo vývojář elektronického vykazování konfigurovat mapování modelu elektronického vykazování (ER) tak, aby získal data z více aplikačních tabulek najednou pomocí datových zdrojů typu **JOIN** k vylepšení výkonu přístupu k datům. Tyto kroky lze provádět pro jakoukoliv společnost Dynamics 365 Finance nebo službu Regulatory Configuration Services (RCS).

### <a name="prerequisites"></a>Předpoklady

Chcete-li provést příklady uvedené v tomto tématu, musíte mít přístup k jednomu z následujících postupů v závislosti na tom, která služba je používána pro dokončení těchto kroků:

**Přístup k Finance pro některou z následujících rolí:**

- Návrhář elektronického výkaznictví
- Funkční konzultant elektronického výkaznictví
- Správce systému

**Přístup k RCS pro některou z následujících rolí:**

- Návrhář elektronického výkaznictví
- Funkční konzultant elektronického výkaznictví
- Správce systému

K provedení těchto kroků musíte také nejprve dokončit jednotlivé kroky v proceduře [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Předem je nutné také stáhnout ze [služby Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) a místně uložit následující ukázkové konfigurační soubory ER:

| **Popis obsahu**  | **Název souboru**   |
|--------------------------|-----------------|
| Ukázkový konfigurační soubor **datového modelu ER**, který se používá jako zdroj dat pro příklady.| [Model k učení se JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Ukázkový konfigurační soubor **mapování modelu ER**, který implementuje model dat ER pro příklady. | [Mapování k učení se JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Ukázkový konfigurační soubor **formátu ER**. V tomto souboru jsou popsána data pro naplnění součásti formátu ER pro příklady. | [Formát k učení se JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>Aktivace zprostředkovatele konfigurací

1. Přístup k financím nebo RCS v první relaci vašeho webového prohlížeče.
2. Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.
3. Na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurace** ověřte, že je uveden poskytovatel konfigurace ukázkové společnosti [Litware, Inc.](http://www.litware.com) a že je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, proveďte kroky v proceduře [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Pracovní prostor elektronického vykazování](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Import ukázkových konfiguračních souborů ER

1. Vyberte **Konfigurace vykazování**.
2. Importujte konfigurační soubor datového modelu ER.
    1. Vyberte **Exchange**.
    2. Vyberte **Načíst ze souboru XML**.
    3. Vyberte **Procházet** a najděte soubor **Model to learn JOIN data sources.version.1.1.xml**.
    4. Vyberte **OK**.
3. Importujte konfigurační soubor mapování modelu ER.
    1. Vyberte **Exchange**.
    2. Vyberte **Načíst ze souboru XML**.
    3. Vyberte **Procházet** a najděte soubor **Mapping to learn JOIN data sources.version.1.1.xml**.
    4. Vyberte **OK**.
4. Importujte soubor konfigurace formátu ER.
    1. Vyberte **Exchange**.
    2. Vyberte **Načíst ze souboru XML**.
    3. Vyberte **Procházet** a najděte soubor **Format to learn JOIN data sources.version.1.1.xml**.
    4. Vyberte **OK**.
5. Ve stromu konfigurací rozbalte položku **Model k učení zdrojů dat JOIN** item další položky modelu (když jsou k dispozici).
6. Sledujte seznam konfigurací ER ve stromové struktuře a podrobnosti o verzi na pevné záložce **Verze** – budou použity jako zdroj dat pro ukázkovou sestavu.

    ![Stránka Konfigurace elektronického výkaznictví](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Zapnutí možností sledování spuštění

1. Vyberte **KONFIGURACE**.
2. Vyberte **Uživatelské parametry**.
3. Nastavte parametry sledování spuštění, jak je uvedeno na snímku obrazovky dole.

    ![Stránka parametrů uživatele elektronického výkaznictví](./media/GER-JoinDS-Parameters.PNG)

    Jsou-li tyto parametry zapnuty, bude pro každou realizaci importovaného souboru ER vygenerováno sledování spouštění. Pomocí podrobností o generovaném trasování provedení můžete analyzovat provádění komponent formátu ER a mapování modelu ER. Další informace o funkci sledování spouštění nástroje ER naleznete na stránce [Sledování provedení formátu ER k řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md).

### <a name="review-er-model-mapping-part-1"></a>Kontrola mapování modelu ER (část 1)

Zkontrolujte nastavení komponenty mapování modelu ER. Komponenta je nakonfigurována pro přístup k informacím o verzích konfigurací ER, podrobnostech konfigurace a poskytovatelů konfigurace bez použití datových zdrojů typu **Join**.

1. Vyberte konfiguraci **Mapování k učení se zdrojů dat JOIN**.
2. Výběrem možnosti **Návrhář** otevřete seznam mapování.
3. Chcete-li zkontrolovat podrobnosti mapování, vyberte možnost **Návrhář**.
4. Vyberte **Zobrazit podrobnosti**.
5. Ve stromu konfigurací rozbalte položky datového modelu **Set1** a **Set1. Details**:

    1. Vázba **Details: Record list = Versions** označuje, že položka **Set1.Details** je vázaná na zdroj dat **Versions** vracející záznamy tabulky **ERSolutionVersionTable**. Každý záznam této tabulky představuje jedinou verzi konfigurace ER. Obsah této tabulky je zobrazen na pevné záložce **Verze** na stránce **Konfigurace**.
    2. Vazba **ConfigurationVersion: String = @.PublicVersionNumber**  znamená, že hodnota veřejné verze jednotlivých konfigurací ER je provedena z pole **PublicVersionNumber** tabulky **ERSolutionVersionTable** a umístěna do položky **ConfigurationVersion**.
    3. Vazba **ConfigurationTitle: String = @.'>Relations'.Solution.Name** označuje, že se název konfigurace ER vybírá z pole **Název** tabulky **ERSolutionTable**, do které se přistupuje pomocí vztahu N:1 (**'>Relations'**) mezi tabulkami **ERSolutionVersionTable** a **ERSolutionTable**. Názvy konfigurací ER pro aktuální instanci aplikace jsou uvedeny ve stromu konfigurací na stránce **Konfigurace**.
    4. Vazba **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** znamená, že se název poskytovatele konfigurace, který vlastní současnou konfiguraci, odvozuje z pole **Název** tabulky **ERVendorTable**, ke které lze získat přístup pomocí vztahu n:1 mezi tabulkami **ERSolutionTable** a **ERVendorTable**. Názvy poskytovatelů konfigurací ER pro každou konfiguraci jsou uvedeny ve stromu konfigurací na stránce **Konfigurace**. Úplný seznam poskytovatelů konfigurace ER lze nalézt na stránce tabulky **Správa organzace \> Elekronické výkaznictví \> Poskytovatel konfigurace**.

    ![Stránka Návrhář mapování modelu ER](./media/GER-JoinDS-Set1Review.PNG)

6. Ve stromu konfigurací rozbalte položky datového modelu **Set1.Summary**:

    1. Vazba **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** označuje, že položka **Set1.Summary.VersionsNumber** je vázaná na souhrnné pole **VersionsNumber** zdroje dat **VersionsSummary** typu **GroupBy**, který byl konfigurován na vracení počtu záznamů tabulky **ERSolutionVersionTable** prostřednictvím zdroje dat **Versions**.

    ![Stránka parametrů zdroje dat GROUPBY](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. Zavřete stránku.

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a> Kontrola mapování modelu ER (část 2)

Zkontrolujte nastavení komponenty mapování modelu ER. Komponenta je nakonfigurována pro přístup k informacím o verzích konfigurací ER, podrobnostech konfigurace a poskytovatelů konfigurace s použitím datových zdrojů typu **Join**.

1. Ve stromu konfigurací rozbalte položky datového modelu **Set2** a **Set2. Details**. Vazba **Details: Record list = Details** naznačuje, že je položka **Set2.Details** vázaná na zdroj dat **Details** konfigurovaný jako zdroj dat typu **Join**.

    ![Stránka Návrhář mapování modelu ER](./media/GER-JoinDS-Set2Review.PNG)

    Zdroj dat **Join** lze přidat výběrem zdroje dat **Functions\Join**:

    ![Stránka Návrhář mapování modelu ER](./media/GER-JoinDS-AddJoinDS.PNG)

2. Vyberte zdroj dat **Detail** s.
3. V podokně **Zdroje dat** vyberte **Upravit**.
4. Vyberte možnost **Upravit spojení**.
5. Vyberte **Zobrazit podrobnosti**.

    ![Stránka parametrů zdroje dat JOIN](./media/GER-JoinDS-JoinDSEditor.PNG)

    Tato stránka slouží k navrhování požadovaného zdroje dat **typu Join**. Při spuštění tento zdroj dat vytvoří jediný sloučený seznam záznamů ze zdrojů dat v mřížce **Připojený seznam**. Spojování záznamů začíná u zdroje dat **ConfigurationProviders**, který je v mřížce jako první (sloupec **Typ** je pro ně prázdný). Záznamy o každém dalším zdroji dat budou následně připojeny k záznamům nadřazeného zdroje dat na základě jeho pořadí v této mřížce. Každý připojující se zdroj dat musí být nakonfigurován jako zdroj dat vnořený pod cílovým zdrojem dat (zdroj dat `1Versions` je vnořený pod zdrojem dat `1Configurations`; zdroj dat `1Configurations` je vnořený pod zdrojem **ConfigurationProviders**). Každý nakonfigurovaný zdroj dat musí obsahovat podmínky pro spojení. Ve zdroji dat pro toto konkrétní **spojení** jsou definována následující spojení:

    - Každý záznam ve zdroji dat **ConfigurationProviders** (odkazovaný na tabulku **ERVendorTable**) je propojen pouze se záznamy **1Configurations** (odkazovanými v tabulce **ERSolutionTable**) se stejnou hodnotou v polích **SolutionVendor** a **RecId**. Typ **Vnitřní spojení** se používá pro toto spojení i pro následující podmínky párování záznamů:

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Každý záznam ve zdroji dat **Configurations** (odkazovaný na tabulku **ERSolutionTable**) je propojen pouze se záznamy **1Versions** (odkazovanými v tabulce **ERSolutionVersionTable**) se stejnou hodnotou v polích **Solution** a **RecId**. Typ **Vnitřní spojení** se používá pro toto spojení i pro následující podmínky párování záznamů:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - Možnost **Spustit** je konfigurována jako **dotaz** v tom smyslu, že tento spojený zdroj dat bude proveden v době běhu na úrovni databáze jako přímé volání SQL.

    Při spojování záznamů zdrojů dat představujících aplikační tabulky můžete určit podmínky spojení použitím párů jiných polí, než jsou ty, které popisují existující v relacích AOT mezi těmito tabulkami. Tento typ spojení lze nakonfigurovat také na úrovni databáze.

6. Zavřete stránku.
7. Vyberte možnost **Zrušit**.
8. Ve stromu konfigurací rozbalte položky datového modelu **Set2.Summary**:

    - Vazba **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** označuje, že položka **Set2.Summary.VersionsNumber** je vázaná na souhrnné pole **VersionsNumber** zdroje dat **DetailsSummary** typu **GroupBy**, který byl konfigurován na vracení počtu spojených záznamů zdroje dat **Details** typu **Join**.
    - Možnost umístění **Spustit** je konfigurována jako **dotaz** v tom smyslu, že tento zdroj dat  **GroupBy** bude proveden v době běhu na úrovni databáze jako přímé volání SQL. Toto chování je možné, protože základní zdroj dat **Details** typu **Join** je konfigurován jako spuštěný na úrovni databáze.

    ![Stránka parametrů zdroje dat GROUPBY](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. Zavřete stránku.
10. Vyberte možnost **Zrušit**.

### <a name="execute-er-format"></a><a name="executeERformat"></a> Provést formát ER

1. Ve druhé relaci webového prohlížeče se přistupuje k financím nebo RCS pomocí stejných přihlašovacích údajů a společnosti jako při první relaci.
2. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
3. Rozbalte konfiguraci **Mapování k učení se zdrojů dat JOIN**.
4. Vyberte konfiguraci **Formát k učení se zdrojů dat JOIN**.
5. Vyberte možnost **Návrhář**.
6. Vyberte **Zobrazit podrobnosti**.
7. Vyberte **Mapování**.
8. Vyberte **Rozbalit/sbalit**.

    Tento formát je určen k naplnění vygenerovaného textového souboru s použitím nového řádku pro každou verzi konfigurace ER (sekvence **Verze**). Každý generovaný řádek bude obsahovat název poskytovatele konfigurace, který vlastní aktuální konfiguraci, název konfigurace a verzi konfigurace oddělené středníkem. Poslední řádek generovaného souboru bude obsahovat počet zjištěných verzí konfigurací ER (**souhrnná** sekvence).

    ![Stránka návrháře formátu ER](./media/GER-JoinDS-FormatReview.PNG)

    Zdroje dat **Data** a **Souhrn** slouží k naplnění podrobností o verzi konfigurace do generovaného souboru:

    - Informace z datového modelu **Set1** jsou použity při výběru volby **Ne** pro zdroj dat **Selektor** v době běhu na stránce uživatelského dialogového okna při spuštění formátu ER.
    - Informace z datového modelu **Set2** jsou použity při výběru volby **Ano** pro zdroj dat **Selektor** v době běhu na stránce uživatelského dialogového okna při spuštění formátu ER.

    ![Stránka návrháře formátu ER](./media/GER-JoinDS-FormatMappingReview.PNG)

9. Vyberte **Spustit**.
10. Na stránce dialogového okna vyberte **Ne** v poli **Použít zdroj dat JOIN**.
11. Vyberte **OK**.
12. Zkontrolujte vygenerovaný soubor.

    ![Stránka dialogového okna uživatele ER](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>Analýza sledování spouštění formátu ER

1. V první relaci Finance nebo RCS vyberte **Návrhář**.
2. Vyberte **Sledování výkonu**.
3. V mřížce **sledování výkonu** vyberte nejvyšší záznam posledního spuštění sledování formátu ER, který použil aktuální součást mapování modelu.
4. Vyberte **OK**.

    Statistika provedení informuje o zdvojených voláních tabulek aplikací:

    - **ERSolutionTable** byla volána tolikrát, kolikrát máte v tabulce **ERSolutionVersionTable** záznamy o konfiguraci verze, zatímco počet takových volání může být v některých případech snížen pro zlepšení výkonu.
    - **ERVendorTable** byla volána dvakrát pro každý záznam verze konfigurace, který byl zjištěn v tabulce **ERSolutionVersionTable**, zatímco počet takových volání může být v některých případech rovněž snížen.

    ![Stránka Návrhář mapování modelu ER](./media/GER-JoinDS-Set1Run2.PNG)

5. Zavřete stránku.

### <a name="execute-er-format"></a>Provést formát ER

1. Přepněte na kartu webového prohlížeče s druhou relací modulu finance nebo RCS.
2. Vyberte **Spustit**.
3. Na stránce dialogového okna vyberte **Ano** v poli **Použít zdroj dat JOIN**.
4. Vyberte **OK**.
5. Zkontrolujte vygenerovaný soubor.

    ![Stránka dialogového okna uživatele ER](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a> Analýza sledování spouštění formátu ER

1. V první relaci Finance nebo RCS vyberte **Návrhář**.
2. Vyberte **Sledování výkonu**.
3. V mřížce **sledování výkonu** vyberte nejvyšší záznam reprezentující poslední spuštění sledování formátu ER, který použil aktuální součást mapování modelu.
4. Vyberte **OK**.

    Statistiky vás informují o následujících faktech:

    - Aplikační databáze byla volána jednou za účelem získání záznamů z tabulek **ERVendorTable**, **ERSolutionTable**, a **ERSolutionVersionTable** pro přístup k požadovaným polím.

    ![Stránka Návrhář mapování modelu ER](./media/GER-JoinDS-Set2Run2.PNG)

    - Aplikační databáze byla volána jednou za účelem výpočtu počtu konfiguračních verzí pomocí spojení, která byla nakonfigurována ve zdroji dat **Podrobnosti**.

    ![Stránka Návrhář mapování modelu ER](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a>Omezení

Jak můžete vidět z příkladu v tomto tématu, **PROPOJENÝ** zdroj dat lze sestavit z několika zdrojů dat, které popisují jednotlivé datové sady záznamů, které musí být nakonec spojeny. Tyto zdroje dat můžete nakonfigurovat pomocí vestavěné funkce ER [FILTR](er-functions-list-filter.md). Když nakonfigurujete zdroj dat tak, aby byl volán i mimo **PROPOJENÝ** zdroj dat, můžete použít firemní rozsahy jako součást podmínky pro výběr dat. První implementace **PROPOJENÉHO** zdroje dat nepodporuje zdroje dat tohoto typu. Například když voláte zdroj dat založený na [FILTRU](er-functions-list-filter.md) v rámci rozsahu provedení zdroje dat **PROPOJIT**, platí, že pokud volaný zdroj dat obsahuje rozsahy společnosti v rámci podmínky výběru dat, dojde k výjimce.

V Microsoft Dynamics 365 Finance verze 10.0.12 (srpen 2020) můžete použít firemní rozsahy jako součást podmínky pro výběr dat ve zdrojích dat založených na funkci [FILTR](er-functions-list-filter.md), které jsou vyvolány v rámci provedení **PROPOJENÉHO** zdroje dat. Z důvodu omezení tvůrce [dotazů](../dev-ref/xpp-library-objects.md#query-object-model) aplikace jsou rozsahy společnosti podporovány pouze pro první zdroj dat **PROPOJENÉHO** zdroje dat.

### <a name="example"></a>Příklad

Například musíte provést jediné volání do databáze aplikací, abyste získali seznam transakcí zahraničního obchodu více společností a podrobnosti o položce inventáře, na kterou se v těchto transakcích odkazuje.

V tomto případě nakonfigurujete v mapování modelu ER následující artefakty:

- Kořenový zdroj dat **Intrastat**, který představuje tabulku **Intrastat**.
- Kořenový zdroj dat **Položky**, který představuje tabulku **InventTable**.
- Kořenový zdroj dat **Společnosti**, který vrací seznam společností (v tomto příkladu **DEMF** a **GBSI**), kde je nutné přistupovat k transakcím. Kód společnosti je k dispozici v poli **Companies.Code**.
- **X1** kořenový zdroj dat, který má výraz `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))`. Jako součást podmínky pro výběr dat obsahuje tento výraz definici podnikových rozsahů `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.
- **X2** zdroj dat jako vnořená položka zdroje dat **X1**. Zahrnuje výraz `FILTER (Items, Items.ItemId = X1.ItemId)`.

Nakonec můžete nakonfigurovat a **PŘIPOJIT** zdroj dat, kde **X1** je první zdroj dat a **X2** je druhý zdroj dat. Můžete zadat **Dotaz** jako možnost **Provést** pro vynucení spuštění zdroje dat na úrovni databázi v ER jako přímého volání SQL.

Když je nakonfigurovaný zdroj dat spuštěn, zatímco je provádění ER [sledováno](trace-execution-er-troubleshoot-perf.md), je v návrháři mapování modelu ER jako součást sledování výkonu ER zobrazen následující návrh.

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> Pokud spustíte **PROPOJENý** zdroj dat, který byl nakonfigurován tak, aby obsahoval podmínky výběru dat, které mají rozsahy společností pro další zdroje dat prováděného **PROPOJENéHO** zdroje dat, dojde k chybě.

## <a name="additional-resources"></a>Další prostředky

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Sledování provádění formátu elektronického výkaznictví za účelem řešení potíží s výkonem](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]