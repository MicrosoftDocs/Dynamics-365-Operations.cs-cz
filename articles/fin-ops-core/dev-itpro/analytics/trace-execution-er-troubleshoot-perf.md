---
title: Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem
description: Toto téma obsahuje informace o způsobu použití funkce sledování výkonu v elektronickém výkaznictví pro řešení potíží s výkonem.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6585e44701160bf31c107c07226f992b12cf035e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550641"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>Sledování provádění formátů elektronického výkaznictví za účelem řešení potíží s výkonem

[!include[banner](../includes/banner.md)]

V rámci procesu navrhování konfigurací elektronického výkaznictví pro generování elektronických dokumentů definujete metodu, která se používá k získání dat z aplikace a jejich zadávání do generovaného výstupu. Funkce sledování výkonu elektronického výkaznictví pomáhá významně snižovat čas a náklady, které jsou spojeny se shromažďováním podrobností o provedení formátu elektronického výkaznictví a jejich použití k řešení potíží s výkonem. Tento kurz poskytuje pokyny k interpretaci sledování výkonu pro provedené formáty elektronického výkaznictví a způsob použití informací z těchto sledování k vylepšení výkonu.

## <a name="prerequisites"></a>Předpoklady

Pro dokončení příkladů v tomto kurzu musíte mít následující přístup:

- Přejděte k některé z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Přístup k instanci služeb Regulatory Configuration Services (RCS), který byl zřízen pro stejného klienta jako aplikace, pro jednu z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

Je také nutné stáhnout a lokálně uložit následující soubory.

| Soubor                                  | Obsah                               |
|---------------------------------------|---------------------------------------|
| Model sledování výkonu - verze 1     | [Vzorová konfigurace datového modelu elektronického výkaznictví](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| Metadata sledování výkonu - verze 1  | [Vzorová konfigurace metadat elektronického výkaznictví](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| Mapování sledování výkonu - verze 1.1 | [Vzorová konfigurace mapování elektronického výkaznictví](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Formát sledování výkonu - verze 1.1  | [Vzorová konfigurace formátu elektronického výkaznictví](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>Konfigurace parametrů ER

Každé sledování výkonu elektronického výkaznictví, které je generováno v aplikaci, je uloženo jako příloha záznamu protokolu provádění. Pro správu těchto příloh se používá architektura správy dokumentů (DM). Parametry elektronického výkaznictví je nutné nakonfigurovat s předstihem, aby bylo možné určit typ dokumentu ve správě dokumentů, který se má použít pro připojení sledování výkonu. V pracovním prostoru **Elektronické sestavy** vyberte **Parametry elektronického vykazování**. Poté na stránce **Parametry elektronického výkaznictví** na kartě **Přílohy** v poli **Jiné** vyberte dokument správy dokumentů pro použití sledování výkonů.

![Stránka parametrů elektronického výkaznictví](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Aby byl k dispozici ve vyhledávacím poli **Jiné**, musí být typ dokumentu typu správy dokumentů nakonfigurován následujícím způsobem na stránce **Typy dokumentů** (**Správa organizace \> Správa dokumentů \> Typy dokumentů**):

- **Třída:** Připojit soubor
- **Skupina:** Soubor

![Stránka typu dokumentu](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Vybraný typ dokumentu musí být k dispozici ve všech společnostech aktuální instance, protože přílohy správy dokumentů jsou specifické pro konkrétní společnost.

### <a name="configure-rcs-parameters"></a>Konfigurace parametrů RCS

Sledování výkonu elektronického výkaznictví, která jsou generována, budou importována do RCS pro analýzu pomocí návrháře formátu elektronického výkaznictví a návrháře mapování elektronického výkaznictví. Vzhledem k tomu, že sledování výkonu elektronického výkaznictví jsou uložena jako přílohy záznamu protokolu spouštění, který souvisí s formátem elektronického výkaznictví, je nutné předem nakonfigurovat parametry RCS, aby bylo možné určit typ dokumentu správy dokumentů, který se má použít pro připojení sledování výkonu. V instanci RCS zřízené pro vaši společnost vyberte v pracovním prostoru **Elektronické výkaznictví** možnost **Parametry elektronického výkaznictví**. Poté na stránce **Parametry elektronického výkaznictví** na kartě **Přílohy** v poli **Jiné** vyberte dokument správy dokumentů pro použití sledování výkonů.

![Stránka parametrů elektronického výkaznictví v RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Aby byl k dispozici ve vyhledávacím poli **Jiné**, musí být typ dokumentu typu správy dokumentů nakonfigurován následujícím způsobem na stránce **Typy dokumentů** (**Správa organizace \> Správa dokumentů \> Typy dokumentů**):

- **Třída:** Připojit soubor
- **Skupina:** Soubor

## <a name="design-an-er-solution"></a>Návrh řešení elektronického výkaznictví

Předpokládejme, že jste začali navrhovat nové řešení elektronického výkaznictví pro generování nové sestavy, která představuje transakce dodavatele. Momentálně můžete najít transakce pro zvoleného dodavatele na stránce **Transakce dodavatele** (přejděte na **Závazky \> Dodavatelé \> Všichni dodavatelé**, zvolte dodavatele a potom v podokně akcí na kartě **Dodavatel** ve skupině **Transakce** zvolte **Transakce**). Chcete však mít všechny transakce dodavatele současně v jednom elektronickém dokumentu ve formátu XML. Toto řešení bude obsahovat několik konfigurací elektronického výkaznictví, které obsahují požadovaný datový model, metadata, mapování modelu a součásti formátu.

1. Přihlaste se k instanci RCS, která byla pro vaši společnost zřízena.
2. V tomto kurzu vytvoříte a upravíte konfigurace pro vzorovou společnost **Litware, Inc.**. Proto se ujistěte, že tento poskytovatel konfigurace byl přidán do RCS a vybrán jako aktivní. Pokyny naleznete v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** importujte konfigurace elektronického výkaznictví, které jste stáhli jako nezbytný požadavek do RCS, v následujícím pořadí: datový model, metadata, mapování modelu, formát. Pro každou konfiguraci postupujte takto:

    1. V podokně akcí vyberte **Exchange \> Načíst ze souboru XML**.
    2. Zvolte **Procházet** a vyberte příslušný soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.
    3. Vyberte **OK**.

    ![Stránka konfigurace v RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>Spuštění řešení elektronického výkaznictví pro sledování provádění

Předpokládejme, že jste dokončili návrh první verze řešení elektronického výkaznictví. Nyní ji chcete vyzkoušet ve své instanci a analyzovat výkon provedení.

### <a id='import-configuration'></a>Import konfigurace elektronického výkaznictví z RCS do Finance and Operations

1. Přihlaste se k instanci aplikace.
2. V tomto kurzu naimportujete konfigurace z vaší instance RCS (kde navrhujete komponenty elektronického výkaznictví) do své instance (kde je otestujete a nakonec je použijete). Proto je nutné zajistit, aby byly připraveny všechny požadované artefakty. Další pokyny získáte v postupu [Import konfigurací elektronického výkaznictví ze služby RCS (Regulatory Configuration Services)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).
3. Pomocí následujícího postupu importujte konfigurace z RCS do aplikace:

    1. V pracovním prostoru **Elektronické výkaznictví** na dlaždici pro poskytovatele konfigurace **Litware, Inc** . vyberte **Úložiště**.
    2. Na stránce **Úložiště konfigurací** vyberte úložiště typu **RCS** a poté zvolte **Otevřít**.
    3. Na záložce s náhledem **Konfigurace** vyberte konfiguraci **Formát sledování výkonu**.
    4. Na záložce s náhledem **Verze** zvolte verzi **1.1** zvolené konfigurace a poté zvolte **Importovat**.

    ![Stránka úložiště konfigurace](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Odpovídající verze konfigurací datových modelů a mapování modelů jsou automaticky importovány jako předpoklady pro importovanou konfiguraci formátu elektronického výkaznictví.

### <a name="turn-on-the-er-performance-trace"></a>Zapnutí sledování výkonu elektronického výkaznictví

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** postupujte takto:

    1. V poli **Formát sledování provádění** zvolte **Ladit formát sledování** pro spuštění shromažďování podrobností o provádění formátu elektronického výkaznictví. Je-li vybrána tato hodnota, sledování výkonu bude shromažďovat informace o době strávené na následujících akcích:

        - Spuštění každého zdroje dat v mapování modelu, které je voláno za účelem získání dat
        - Zpracování jednotlivých položek formátu za účelem zadání dat ve výstupu, který je generován

        Pole **Formát sledování provádění** použijte k upřesnění formátu generovaného sledování výkonu, ve kterém jsou uloženy podrobnosti o provádění pro formát elektronického výkaznictví a prvky mapování. Volbou možnosti **adit formát sledování** budete moci analyzovat obsah sledování v návrháři operací elektronického výkaznictví a zobrazit formát elektronického výkaznictví nebo prvky mapování, které jsou uvedeny ve sledování.

    2. Chcete-li shromažďovat konkrétní podrobnosti o provádění mapování modelu elektronického výkaznictví a součástech formátu elektronického výkaznictví, nastavte následující možnosti na hodnotu **Ano**:

        - **Shromáždit statistiky dotazů** – Pokud je tato možnost zapnuta, bude sledování výkonu bude shromažďovat následující informace:

            - Počet volání databáze, která byla provedena zdroji dat.
            - Počet duplicitních volání do databáze
            - Podrobnosti o příkazech SQL, které byly použity k vytvoření databázových volání

        - **Sledovat přístup ukládání do mezipaměti** - Je-li tato možnost zapnuta, bude sledování výkonu shromažďovat informace o využití mezipaměti mapování modelu elektronického výkaznictví.
        - **Přístup k datům sledování** – Pokud je tato možnost zapnuta, sledování výkonu bude shromažďovat informace o počtu volání do databáze pro provedené zdroje dat typu seznamu záznamů.
        - **Výčet seznamu sledování** – Pokud je tato možnost zapnuta, sledování výkonu bude shromažďovat informace o počtu záznamů vyžadovaných od zdrojů dat typu seznamu záznamů.

    > [!NOTE]
    > Parametry v dialogovém okně **Parametry uživatelů** jsou specifické pro uživatele a aktuální společnost.

    ![Dialogové okno Parametry uživatele](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a>Spuštění formátu elektronického výkaznictví

1. Vyberte společnost **DEMF**.
2. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
3. Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Formát sledování výkonu**.
4. V podokně akcí zvolte **Spustit**.

Povšimněte si, že vygenerovaný soubor uvádí informace o 265 transakcích pro šest dodavatelů.

## <a name="review-the-execution-trace"></a>Kontrola sledování provádění

### <a id='export-trace'></a>Export generovaného trasovacího programu z aplikace

Sledování výkonu je odděleno od zdrojového formátu elektronického výkaznictví a lze ho serializovat do externího souboru ZIP.

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurovat protokoly ladění**.
2. Na stránce **Protokoly spuštění elektronického výkaznictví** v levém podokně v poli **Název konfigurace** vyberte **Formát sledování výkonu** pro vyhledání záznamů protokolů, které byly vygenerovány provedením konfigurace **Formát sledování výkonu**.
3. Vyberte tlačítko **Přílohy** (ikona kancelářské sponky) v pravém horním rohu stránky, nebo stiskněte **Ctrl+Shift+A**.

    ![Tlačítko Přílohy na stránce Protokoly spuštění elektronického výkaznictví](./media/GER-PerfTrace-GER-DebugLog.png)

4. Na stránce **Přílohy pro protokoly spuštění elektronického výkaznictví** v podokně akcí zvolte **Otevřít** pro získání sledování výkonu jako souboru ZIP, a lokálně ho uložte.

    ![Přílohy pro protokoly spuštění elektronických sestav](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Vygenerovaní sledování má odkaz na zdrojovou sestavu elektronického výkaznictví prostřednictvím jedinečného identifikátoru sestavy pouze ve formátu **GUID**. Číslování verzí formátu není zvažováno.

Všimněte si, že přidružení mezi sledováním výkonu, které bylo vygenerováno pro spuštěný formát elektronického výkaznictví, a mapováním modelu elektronického výkaznictví, je založeno na použitém kořenovém popisovači a na společném datovém modelu. Číslování verzí formátu a mapování modelu není zvažováno. Nastavení příznaku **Výchozí pro mapování modelu** pro mapování modelu se také nebere v úvahu.

### <a id='import-trace'></a>Import generovaného sledování do RCS

1. V RCS v pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
2. Na stránce **Konfigurace** ve stromové struktuře konfigurací rozbalte položku **Model sledování výkonu** a vyberte položku **Formát sledování výkonu**.
3. V podokně akcí zvolte **Návrhář**.
4. Na stránce **Návrhář formátu** v podokně akcí vyberte **Sledování výkonu**.
5. V dialogovém okně **Nastavení výsledků sledování výkonu** vyberte možnost **Importovat sledování výkonu**.
6. Vyberte **Procházet** a vyberte soubor zip, který jste předtím exportovali.
7. Vyberte **OK**.

    ![Dialogové okno nastavení výsledků sledování výkonu v RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Použití sledování výkonu pro analýzu v RCS – provádění formátu

1. V RCS na stránce **Návrhář formátu** vyberte možnost **Rozbalit/sbalit** a rozbalte obsah všech položek formátu.

    Všimněte si, že pro některé položky aktuálního formátu jsou zobrazeny další informace:

    - Skutečný čas strávený zadáváním dat ve vygenerovaném výstupu s použitím položky formátu
    - Stejný čas vyjádřený jako procento z celkového času stráveného generováním celého výstupu

    ![Stránka návrháře formátu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Zavřete stránku **návrháře formátu**.

### <a id='use-trace'></a>Použití sledování výkonu pro analýzu v RCS – mapování modelu

1. V RCS na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování sledování výkonu**.
2. V podokně akcí zvolte **Návrhář**.
3. Vyberte možnost **Návrhář**.
4. Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.
5. Vyberte sledování, které jste importovali dříve.
6. Vyberte **OK**.

Povšimněte si, že nové informace budou k dispozici pro některé položky zdroje dat aktuálního mapování modelu:

- Skutečný čas strávený získáváním dat pomocí zdroje dat
- Stejný čas vyjádřený jako procento z celkového času stráveného spouštěním celého mapování modelu

Všimněte si, že elektronické výkaznictví vás informuje, že aktuální mapování modelu duplikuje databázové požadavky, zatímco je spuštěn zdroj dat VendTable/\<Relations/VendTrans.VendTable\_AccountNum. Tato duplicita nastane, protože seznam transakcí dodavatele se pro každý opakovaný záznam dodavatele volá dvakrát.

- Jedno volání se provádí pro zadání podrobností o každé transakci v datovém modelu na základě konfigurovaných vazeb.
- Druhé volání se provádí k zadání vypočítaného počtu transakcí pro dodavatele v datovém modelu.

![Zpráva o duplicitních žádostech databáze na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Hodnota **\[Q:530\]** označuje, že tabulka VendTrans byla volána 530krát, aby vracela záznam z této tabulky do datové zdroje VendTable/\<Relations/VendTrans.VendTable\_AccountNum. Hodnota **\[530\]** označuje, že zdroj dat VendTable/\<Relations/VendTrans.VendTable\_AccountNum byl volán 530krát, aby vracel záznam z tohoto zdroje dat a zadal z něj podrobnosti do datového modelu.

Doporučujeme použít ukládání do mezipaměti pro datový zdroj VendTable/\<Relations/VendTrans.VendTable\_AccountNum ke snížení počtu volání, která jsou prováděna za účelem získání podrobností o 265 transakcích 265 a zlepšení výkonu mapování modelu.

Je také užitečné omezit počet volání, která jsou provedena na zdroj dat LedgerTransTypeList. Tento zdroj dat slouží k přidružení každé hodnoty výčtu **LedgerTransType** k jeho popisku. Pomocí tohoto zdroje dat můžete vyhledat příslušný popisek a zadat ho do datového modelu pro každou transakci dodavatele. Aktuální počet volání tohoto zdroje dat (9 027) je poměrně vysoký pro 265 transakcí.

![Stránka návrháře mapování modelu v RCS, zobrazující 9 027 volání zdroje dat.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Vylepšení mapování modelu na základě informací ze sledování provádění

### <a name="modify-the-logic-of-the-model-mapping"></a>Úprava logiky mapování modelu

1. Chcete-li zabránit duplicitním voláním do databáze, postupujte podle následujících kroků pro použití ukládání do mezipaměti:

    1. V RCS na stránce **Návrhář mapování modelu** v podokně **Datové zdroje** zvolte položku **VendTable**.
    2. Vyberte **Mezipaměť**.
    3. Rozbalte položku **VendTable**, rozbalte seznam relací 1:N pro zdroj dat VendTable (položka **\<Vztahy**) a vyberte položku **VendTrans. VendTable\_AccountNum**.
    4. Vyberte **Mezipaměť**.

    ![Nastavení ukládání do mezipaměti za účelem předcházení duplicitním voláním](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Chcete-li do rozsahu datového zdroje VendTable přenést zdroj dat LedgerTransTypeList, postupujte podle následujících kroků:

    1. V podokně **Typy zdrojů dat** rozbalte položku **Funkce** a vyberte položku **Vypočítané pole**.
    2. V podokně **Datové zdroje** vyberte položku **VendTable**.
    3. Vyberte **přidat**.
    4. Do pole **Název** zadejte řetězec **\$TransType**.
    5. Vyberte možnost **Upravit vzorec**.
    6. Do pole **Vzorec** zadejte **LedgerTransTypeList**.
    7. Zvolte **Uložit**.
    8. Zavřete stránku **Editor vzorců**.
    9. Klikněte na tlačítko **OK**.

3. Chcete-li provést ukládání do mezipaměti pole **\$TransType**, postupujte podle následujících kroků:

    1. Vyberte položku **LedgerTransTypeList**.
    2. Vyberte **Mezipaměť**.
    3. Vyberte položku **VendTable.\$TransType**.
    4. Vyberte **Mezipaměť**.

    ![Nastavení ukládání do mezipaměti pro pole $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Chcete-li změnit **\$TransTypeRecord** tak, aby začalo používat pole **\$TransType** uložené v mezipaměti, použijte následující postup:

    1. V podokně **Datové zdroje** rozbalte položku **VendTable**, rozbalte položku **\<Relations**, rozbalte položku **VendTrans.VendTable\_AccountNum** a vyberte položku **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.
    2. Vyberte možnost **Upravit**.
    3. Vyberte možnost **Upravit vzorec**.
    4. V poli **Vzorec** vyhledejte následující výraz:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. V poli **Vzorec** zadejte následující výraz:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Zvolte **Uložit**.
    7. Zavřete stránku **Editor vzorců**.
    8. Vyberte **OK**.

5. Zvolte **Uložit**.
6. Zavřete stránku **Návrhář mapování modelu**.
7. Zavřete stránku **Mapování modelu**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Dokončení upravené verze mapování modelu elektronického výkaznictví

1. V RCS na stránce **Konfigurace** na záložce s náhledem **Verze** vyberte verzi **1.2** konfigurace **Mapování sledování výkonu**.
2. Vyberte **Změnit stav**.
3. Zvolte **Dokončit**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Import upravené konfigurace mapování modelu elektronického výkaznictví z RCS do aplikace

Opakujte kroky z části [Import konfigurace elektronického výkaznictví z RCS do Finance and Operations](#import-configuration) dříve v tomto tématu pro import verze 1.2 konfigurace **Mapování sledování výkonu**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Spuštění upraveného řešení elektronického výkaznictví pro sledování provádění

### <a name="run-the-er-format"></a>Spuštění formátu elektronického výkaznictví

Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.

## <a name="review-the-execution-trace"></a>Kontrola sledování provádění

### <a name="export-the-generated-trace-from-the-application"></a>Export generovaného trasovacího programu z aplikace

Zopakujte kroky v části [Exportování vygenerovaného sledování z aplikace](#export-trace) výše v tomto tématu pro místní uložení nového sledování výkonu.

### <a name="import-the-generated-trace-into-rcs"></a>Import generovaného sledování do RCS

Opakujte kroky v části [Import generovaného sledování do RCS](#import-trace) výše v tomto tématu pro import nového sledování výkonu do RCS.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Použití sledování výkonu pro analýzu v RCS – mapování modelu

Opakujte kroky v části [Použití sledování výkonu pro analýzu v RCS – mapování modelu](#use-trace) výše v tomto tématu pro analýzu nejnovějšího sledování výkonu.

Všimněte si, že úpravy provedené v mapování modelu odstranily duplicitní dotazy do databáze. Počet volání databázových tabulek a zdrojů dat pro toto mapování modelu byl také snížen. Z toho vyplývá zvýšení výkonu celého řešení elektronického výkaznictví.

![Sledování informací pro datový zdroj VendTable na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

Hodnota **\[12\]** pro zdroj dat VendTable v informacích o sledování označuje, že tento zdroj dat byl volán 12krát. Hodnota **\[Q:6\]** označuje, že šest volání bylo přeloženo do volání databáze do tabulky VendTable. Hodnota **\[C:6\]** označuje, že záznamy načtené z databáze byly uloženy do mezipaměti a šest dalších volání bylo zpracováno pomocí mezipaměti.

Všimněte si, že počet volání zdroje dat LedgerTransTypeList byl snížen z 9 027 na 240.

![Sledování informací pro datový zdroj LedgerTransTypeList na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Kontrola sledování spuštění v aplikaci

Kromě RCS mohou některé verze nabídnout možnosti pro rozhraní návrháře architektury elektronického výkaznictví. Tyto verze mají možnost **Povolit režim návrhu**, kterou lze zapnout. Tuto možnost naleznete na kartě **Obecné** na stránce **Parametry elektronického výkaznictví**, kterou lze otevřít v pracovním prostoru **elektronického výkaznictví**.

![Povolení možnosti režimu návrhu na stránce parametry elektronického vykazování](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Pokud používáte některou z těchto verzí můžete analyzovat podrobnosti generovaných sledováních výkonu přímo v aplikaci. Nemusíte je exportovat z aplikace a importovat do RCS.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Kontrola sledování provádění pomocí externích nástrojů

### <a name="configure-user-parameters"></a>Konfigurace parametrů uživatele

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** v poli **Formát sledování provádění** vyberte **PerfView XML**.

### <a name="run-the-er-format"></a>Spuštění formátu elektronického výkaznictví

Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.

Povšimněte si, že webový prohlížeč nabízí soubor zip ke stažení. Tento soubor obsahuje sledování výkonu ve formátu PerfView. Poté můžete pomocí nástroje analýzy výkonu PerfView analyzovat podrobnosti provádění formátu elektronického výkaznictví.

![Informace o sledování pro spuštěný formát elektronického výkaznictví v PerfView](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Použití externích nástrojů ke kontrole sledování provádění, které obsahuje databázové dotazy

Z důvodu vylepšení, které bylo provedeno v rámci architektury elektronického výkaznictví, nabízí sledování výkonu generované ve formátu PerfView nyní více podrobnostmi o provádění formátu elektronického výkaznictví. V aplikaci Microsoft Dynamics 365 for Finance and Operations verze 10.0.4 (červenec 2019) může toto sledování také zahrnovat podrobnosti o provedených dotazech SQL do aplikační databáze.

### <a name="configure-user-parameters"></a>Konfigurace parametrů uživatele

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** nastavte následující parametry:

    - V poli **Formát sledování provádění** vyberte **PerfView XML**.
    - Nastavte možnost **Shromáždit statistiky dotazů** na **Ano**.
    - Nastavte možnost **Dotaz na sledování** na **Ano**.

    ![Dialogové okno Parametry uživatele](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>Spuštění formátu elektronického výkaznictví

Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.

Povšimněte si, že webový prohlížeč nabízí soubor zip ke stažení. Tento soubor obsahuje sledování výkonu ve formátu PerfView. Poté můžete pomocí nástroje analýzy výkonu PerfView analyzovat podrobnosti provádění formátu elektronického výkaznictví. Sledování nyní zahrnuje podrobné informace o přístupu k databázi SQL během provádění formátu elektronického výkaznictví.

![Informace o sledování pro spuštěný formát elektronického výkaznictví v PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)