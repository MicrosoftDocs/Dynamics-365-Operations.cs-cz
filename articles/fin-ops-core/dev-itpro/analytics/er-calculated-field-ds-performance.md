---
title: Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE
description: Tohle téma popisuje, jak můžete zlepšit výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4ee5a074c5c6d2e2144181e39917b1cc42dfc015
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944823"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE

[!include [banner](../includes/banner.md)]

Tohle téma popisuje, jak můžete použít informace ze spuštěných [sledování výkonu](trace-execution-er-troubleshoot-perf.md) z formátů [elektronického výkaznictví](general-electronic-reporting.md) ke zlepšení výkonu prostřednictvím parametrizovaných zdrojů dat typu **Počítané pole**.

V rámci procesu vytváření konfigurací elektronického výkaznictví pro generování obchodních dokumentů definujete metodu, která se používá k načtení dat z aplikace a jejich zadávání do generovaného výstupu. Návrhem parametrizovaného zdroje dat elektronického výkaznictví typu **Počítané pole** můžete snížit počet volání databáze a výrazně snížit čas a náklady spojené se shromažďováním podrobností při spuštění formátu elektronického výkaznictví.

## <a name="prerequisites"></a>Předpoklady

- Abyste mohli dokončit příklady v tomto tématu, musíte mít přístup k některé z následujících [rolí](../sysadmin/tasks/assign-users-security-roles.md):

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Společnost musí být nastavena na **DEMF**.
- Podle pokynů v [příloze 1](#appendix1) tohoto tématu si stáhněte součásti ukázkového řešení elektronického výkaznictví společnosti Microsoft, které jsou potřeba k provedení příkladů v tomto tématu.
- Podle pokynů v [příloze 2](#appendix2) v tomto tématu můžete nakonfigurovat minimální sadu parametrů elektronického výkaznictví, které jsou potřeba k použití architektury elektronického výkaznictví k zlepšení výkonu ukázkového řešení elektronického výkaznictví společnosti Microsoft.

## <a name="import-the-sample-er-solution"></a>Import ukázkového řešení elektronického výkaznictví

Představte si, že musíte navrhnout nové řešení elektronického výkaznictví pro generování nové sestavy, která obsahuje transakce dodavatele. Momentálně můžete najít transakce pro zvoleného dodavatele na stránce **Transakce dodavatele** (přejděte na **Závazky** \> **Dodavatelé** \> **Všichni dodavatelé**, zvolte dodavatele a potom v podokně akcí na kartě **Dodavatel** ve skupině **Transakce** zvolte **Transakce**). Chcete však mít všechny transakce dodavatele současně v jednom elektronickém dokumentu ve formátu XML. Toto řešení bude obsahovat několik konfigurací elektronického výkaznictví, které obsahují požadovaný datový model, mapování modelu a součásti formátu.

Prvním krokem je import ukázkového řešení elektronického výkaznictví k vygenerování sestavy transakcí dodavatele.

1. Přihlaste se k instanci Microsoft Dynamics 365 Finance, která je zřízena pro vaši společnost.
2. V tomto tématu vytvoříte a upravíte konfigurace pro vzorovou společnost **Litware, Inc.**. Ujistěte se, že tento poskytovatel konfigurace byl přidán do instance Finance a je označen jako aktivní. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** importujte konfigurace elektronického výkaznictví, které jste stáhli jako nezbytný požadavek do Finance, v následujícím pořadí: datový model, mapování modelu, formát. Pro každou konfiguraci postupujte takto:

    1. V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.
    2. Zvolte **Procházet** a vyberte příslušný soubor pro konfiguraci elektronického výkaznictví ve formátu XML.
    3. Vyberte **OK**.

![Importované konfigurace na stránce Konfigurace](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Kontrola ukázkového řešení elektronického výkaznictví

### <a name="review-the-model-mapping"></a>Kontrola mapování modelu

1. Na stránce **Konfigurace** ve stromu konfigurací položku **Model zlepšení výkonu** a vyberte možnost **Mapování zlepšení výkonu**.
2. V podokně akcí zvolte **Návrhář**.
3. Na stránce **Mapování modelu na zdroj dat** v podokně Akce vyberte možnost **Návrhář**.

    Toto mapování modelu elektronického výkaznictví je navrženo k následujícím akcím:

    - Načtěte seznam transakcí dodavatele, které jsou uloženy v tabulce VendTrans (zdroj dat **Trans**).
    - Pro každou transakci načtěte z tabulky VendTable záznam dodavatele, pro kterého byla transakce zaúčtována (zdroj dat **\#Vend**).

    > [!NOTE]
    > Zdroj dat **\#Vend** je nakonfigurován tak, aby načetl odpovídající záznam dodavatele pomocí existujícího vztahu N:1 **\@'\>Relations'.VendTable\_AccountNum**.

    Mapování modelu v této konfiguraci implementuje základní datový model pro všechny formáty elektronického výkaznictví vytvořené pro tento model a spuštěné ve Finance. V důsledku toho je obsah zdroje dat **Trans** vystaven pro formáty elektronického výkaznictví, jako jsou například abstraktní zdroje dat **modelu**.

    ![Zdroj dat Trans na stránce návrháře mapování modelů](media/er-calculated-field-ds-performance-mapping-1.png)

4. Zavřete stránku **Návrhář mapování modelu**.
5. Zavřete stránku **Mapování modelu na zdroj dat**.

### <a name="review-format"></a>Zkontrolovat formát

1. Na stránce **Konfigurace** ve stromu konfigurací položku **Model zlepšení výkonu** a vyberte možnost **Formát zlepšení výkonu**.
2. V podokně akcí zvolte **Návrhář**.
3. Na stránce **Návrhář formátu** na kartě **Mapování** vyberte **Rozbalit/sbalit**.
4. Rozbalte položky **Model**, **Data** a **Transakce**.

    Tento formát elektronického výkaznictví je navržen tak, aby generoval zprávu o transakcích dodavatele ve formátu XML.

    ![Formátování zdroje dat a konfigurovaných vazeb prvků formátu na stránce Návrhář formátu](media/er-calculated-field-ds-performance-format.png)

5. Zavřete stránku **Návrhář formátu**.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Spuštění ukázkového řešení elektronického výkaznictví pro sledování provádění

Představte si, že jste dokončili návrh první verze řešení elektronického výkaznictví. Nyní chcete řešení vyzkoušet v instanci Finance a analyzovat výkon při jeho provádění.

### <a name="turn-on-the-er-performance-trace"></a>Zapnutí sledování výkonu elektronického výkaznictví

1. Vyberte společnost **DEMF**.
2. Podle pokynů v části [Zapnutí sledování výkonu elektronického výkaznictví](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) vygenerujte sledování výkonu, když je spuštěn formát elektronického výkaznictví.

    ![Dialogové okno Parametry uživatele](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>Spuštění formátu elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Formát zlepšení výkonu**.
3. V podokně akcí zvolte **Spustit**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Použití sledování výkonu k analýze výkonu mapování modelů

1. Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování zlepšení výkonu**.
2. V podokně akcí zvolte **Návrhář**.
3. Na stránce **Mapování modelu** v podokně Akce vyberte možnost **Návrhář**.
4. Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.
5. Vyberte nejnovější sledování, které bylo vygenerováno, a poté vyberte **OK**.

Nyní jsou dostupné nové informace pro některé položky zdroje dat aktuálního mapování modelu:

- Skutečný čas strávený získáváním dat pomocí zdroje dat
- Stejný čas vyjádřený jako procento z celkového času stráveného spouštěním celého mapování modelu

![Podrobnosti o době provedení na stránce návrháře mapování modelů](./media/er-calculated-field-ds-performance-mapping-2.png)

Mřížka **Statistiky výkonu** ukazuje, že zdroj dat **Trans** jednou volá tabulku VendTrans. Hodnota **\[265\]\[Q:265\]** ze zdroje dat **Trans** udává, že 265 transakcí dodavatele bylo načteno z tabulky aplikace a vráceno do datového modelu.

Mřížka **Statistiky výkonu** také ukazuje, že aktuální model mapování duplikuje databázové požadavky, zatímco je spuštěn zdroj dat **\#Vend**. Tato duplikace se vyskytuje z následujících důvodů:

- Tabulka dodavatele je volána dvakrát pro každou z 265 iterovaných transakcí dodavatele, celkem tedy 530 volání:

    - Jedním voláním se zadá číslo účtu dodavatele.
    - Jedním voláním se zadá název dodavatele.

- Tabulka dodavatelů je volána pro každou iterovanou transakci dodavatele, přestože načtené transakce byly zaúčtovány pouze pro pět dodavatelů. Z 530 hovorů je 525 duplikátů. Následující obrázek ukazuje zprávu, kterou obdržíte o duplicitních voláních (databázové požadavky).

![Zpráva o duplicitních žádostech databáze na stránce návrháře mapování modelu](./media/er-calculated-field-ds-performance-mapping-2a.png)

Z celkové doby provedení mapování modelu (přibližně osm sekund) si všimněte, že více než 80 procent (přibližně šest sekund) bylo vynaloženo na načtení hodnot z tabulky aplikace VendTable. Toto procento je příliš vysoké pro dva atributy pěti dodavatelů ve srovnání s objemem informací z tabulky aplikace VendTrans.

Chcete-li snížit počet volání, abyste získali podrobnosti o dodavateli pro každou transakci a zlepšili výkon mapování modelu, můžete použít ukládání do mezipaměti pro zdroj dat **\#Vend**.

> [!NOTE]
> Zdroj dat **Trans\\\#Vend** bude uložen do mezipaměti v rozsahu aktuální transakce zdroje dat **Trans** za běhu.

Uložením zdroje dat **\#Vend** do mezipaměti snížíte počet duplicitních hovorů z 525 na 260, ale duplikaci zcela neodstraníte. Chcete-li zcela vyloučit duplikaci, můžete nakonfigurovat nový parametrizovaný zdroj dat typu **Počítané pole**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Vylepšení mapování modelu na základě informací ze sledování provádění

### <a name="change-the-logic-of-the-model-mapping"></a>Změna logiky mapování modelu

Pomocí těchto kroků můžete použít ukládání zdroje dat typu **Počítané pole** do mezipaměti, aby se zabránilo duplicitním voláním do databáze.

1. Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování zlepšení výkonu**.
2. V podokně akcí zvolte **Návrhář**.
3. Na stránce **Mapování modelu** v podokně Akce vyberte možnost **Návrhář**.
4. Na stránce **Návrhář mapování modelů** postupujte podle těchto kroků, abyste přidali zdroj dat typu **Záznamy tabulky** pro přístup k záznamům v tabulce aplikace VendTable:

    1. V podokně **Typy zdrojů dat** rozbalte **Dynamics 365 for Operations** a vyberte **Záznamy tabulky**.
    2. Vyberte **Přidat kořen**.
    3. V dialogovém okně do pole **Název** zadejte **Vend**.
    4. Do pole **Tabulka** zadejte **VendTable**.
    5. Vyberte **OK**.

5. Můžete parametrizovat volání zdrojů dat typu **Počítané pole**, pouze pokud jsou tyto zdroje dat umístěny v kontejneru. Proto podle těchto pokynů přidejte zdroj dat typu **Prázdný kontejner** pro uchování nového parametrizovaného zdroje dat typu **Počítané pole**:

    1. V podokně **Typy zdrojů dat** rozbalte **Obecné** a vyberte **Prázdný kontejner**.
    2. Vyberte **Přidat kořen**.
    3. V dialogovém okně do pole **Název** zadejte **Box**.
    3. Vyberte **OK**.

    ![Zdroj dat Box na stránce návrháře mapování modelů](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Pomocí těchto kroků přidáte parametrizovaný zdroj dat typu **Počítané pole**:

    1. V podokně **Zdroje dat** vyberte **Box**.
    2. V podokně **Typy zdrojů dat** rozbalte **Funkce** a vyberte **Počítané pole**.
    3. Vyberte **přidat**.
    4. V dialogovém okně do pole **Název** zadejte **Vend**.
    5. Vyberte možnost **Upravit vzorec**.
    6. Na stránce **Návrhář vzorců** vyberte **Parametry** k určení parametrů, které je nutné zadat při volání tohoto zdroje dat.
    7. V dialogovém okně **Parametry** vyberte **Nový**.
    8. Do pole **Název** zadejte **parmVendAccNumber**.
    9. V poli **Typ** vyberte **Řetězec**.
    10. Vyberte **OK**.
    11. V poli **Vzorec** zadejte **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.
    13. Vyberte **OK** pro přidání nového zdroje dat.

7. Chcete-li během provádění označit přidaný zdroj dat, že je v mezipaměti, postupujte takto:

    1. V podokně **Zdroje dat** vyberte **Box\\Vend**.
    2. Vyberte **Mezipaměť**.

    > [!NOTE]
    > Zdroj dat **Box\\Vend** bude uložen do mezipaměti v rozsahu všech transakcí dodavatele zdroje dat **Trans** za běhu.

8. Podle těchto pokynů aktualizujte vnořený zdroj dat **Trans\\\#Vend** tak, že používá zdroj dat **Box\\Vend**:

    1. V podokně **Zdroje dat** rozbalte **Trans**.
    2. Vyberte zdroj dat **Trans\\\#Vend** a poté vyberte **Upravit** \> **Upravit vzorec**.
    3. Na stránce **Návrhář vzorců** v poli **Vzorec** zadejte **Box.Vend(\@.AccountNum)**.
    4. Vyberte **Uložit** a poté zavřete stránku **Návrhář vzorců**.
    5. Tlačítkem **OK** dokončíte změny ve vybraném zdroji dat.

9. Zvolte **Uložit**.

    ![Zdroj dat Vend na stránce návrháře mapování modelů](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Zavřete stránku **Návrhář mapování modelu**.
11. Zavřete stránku **Mapování modelu**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Dokončení upravené verze mapování modelu elektronického výkaznictví

1. Na stránce **Konfigurace** na záložce s náhledem **Verze** vyberte verzi **1.2** konfigurace **Mapování zlepšení výkonu**.
2. Vyberte **Změnit stav** \> **Dokončit** a poté vyberte **OK**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Spuštění upraveného řešení elektronického výkaznictví pro sledování provádění

Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Použití sledování výkonu k analýze úprav mapování modelů 

1. Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování zlepšení výkonu**.
2. V podokně akcí zvolte **Návrhář**.
3. Na stránce **Mapování modelu** v podokně Akce vyberte možnost **Návrhář**.
4. Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.
5. Vyberte nejnovější sledování, které bylo vygenerováno, a poté vyberte **OK**.

Všimněte si, že úpravy provedené v mapování modelu odstranily duplicitní dotazy do databáze. Počet volání databázových tabulek a zdrojů dat pro toto mapování modelu byl snížen.

![Informace o sledování na stránce Návrhář mapování modelů 1](./media/er-calculated-field-ds-performance-mapping-5.png)

Celková doba provedení byla snížena přibližně 20krát (z přibližně 8 sekund na přibližně 400 milisekund). Z toho vyplývá zvýšení výkonu celého řešení elektronického výkaznictví.

![Informace o sledování na stránce Návrhář mapování modelů 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Příloha 1: Stáhněte si součásti ukázkového řešení elektronického výkaznictví Microsoft

Je nutné stáhnout a místně uložit následující soubory.

| Soubor                                        | Obsah |
|---------------------------------------------|---------|
| Performance improvement model.version.1     | [Vzorová konfigurace datového modelu elektronického výkaznictví](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Performance improvement mapping.version.1.1 | [Vzorová konfigurace mapování elektronického výkaznictví](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Performance improvement format.version.1.1  | [Vzorová konfigurace formátu elektronického výkaznictví](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Příloha 2: Konfigurace architektury elektronického výkaznictví

Než začnete používat architekturu elektronického výkaznictví ke zlepšení výkonu ukázkového řešení elektronického výkaznictví Microsoft, musíte nakonfigurovat minimální sadu parametrů elektronického výkaznictví.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurace parametrů elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** vyberte v části **Související odkazy** možnost **Parametry elektronického výkaznictví**.
3. Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.
4. Na kartě **Přílohy** natavte následující parametry:

    - V poli **Konfigurace** vyberte pro společnost **DEMF** typ **Soubor**.
    - V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.

Další informace o parametrech elektronického výkaznictví najdete v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivace poskytovatele konfigurace elektronického výkaznictví

U každé přidané konfigurace elektronického výkaznictví je vyznačen jako vlastník poskytovatel konfigurace elektronického výkaznictví. Pro tyto účely se používá poskytovatel konfigurace elektronického výkaznictví, který je aktivován v pracovním prostoru **Elektronické výkaznictví**. Než začnete přidávat nebo upravovat konfigurace elektronického výkaznictví, musíte proto aktivovat poskytovatele konfigurace elektronického výkaznictví v pracovním prostoru **Elektronické výkaznictví**.

> [!NOTE]
> Pouze vlastník konfigurace elektronického výkaznictví může konfiguraci upravovat. Konfiguraci elektronického výkaznictví proto můžete upravovat teprve poté, co je příslušná konfigurace elektronického výkaznictví aktivována v pracovním prostoru **Elektronické výkaznictví**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Kontrola seznamu poskytovatelů konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Tabulka poskytovatelů konfigurací** má záznam každého poskytovatele jedinečný název a adresu URL. Zkontrolujte obsah této stránky. Pokud již existuje záznam **Litware, Inc.**, další postup, [Přidání nového poskytovatele konfigurace elektronického výkaznictví](#ActivateProvider), přeskočte.

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Přidání nového poskytovatele konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.
4. Do pole **Název** zadejte **Litware, Inc.**
5. Do pole **Internetová adresa** zadejte `https://www.litware.com`.
6. Zvolte **Uložit**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivace poskytovatele konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** klikněte v části **Poskytovatelé konfigurací** na dlaždici **Litware, Inc.** a poté vyberte možnost **Nastavit jako aktivní**.

Další informace o poskytovatelích konfigurací elektronického výkaznictví naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md)
- [Podpora parametrizovaných volání zdrojů dat elektronického výkaznictví typu vypočítaného pole](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
