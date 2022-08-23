---
title: Seskupení záznamů a agregace výpočtů pomocí zdrojů dat GROUPBY
description: Tento článek vysvětluje, jak je možné používat datové zdroje GROUPBY mezi více společnostmi v modulu Elektronické výkaznictví (ER).
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 0e520705d2441ead5a68ec3284db74999b3d90b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277565"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Seskupení záznamů a agregace výpočtů pomocí zdrojů dat GROUPBY

[!include[banner](../includes/banner.md)]

Při konfiguraci mapování nebo formátů služby [elektronického vykazování (ER)](general-electronic-reporting.md) můžete [přidat](#AddMmDataSource2) požadované zdroje dat typu **GroupBy**.

V době návrhu je zdroj dat **GroupBy** nakonfigurován tak, aby identifikoval následující prvky:

- [Základní zdroj dat](#BaseDataSource), který obsahuje záznamy, které budou seskupeny za běhu
- [Pole seskupování](#GroupingFields) základního zdroje dat, který bude použit pro seskupování záznamů za běhu
- [Agregační funkce](#AggregateFunctions), které určují agregované výpočty, které budou provedeny pro každou zjištěnou skupinu za běhu

Za běhu nakonfigurovaný zdroj dat **GroupBy** seskupuje záznamy, které mají stejné hodnoty v polích seskupení, a poté vrátí seznam záznamů. Každý záznam představuje jednu skupinu. Pro každou skupinu zdroj dat zpřístupní hodnoty polí, podle kterých byly seskupeny počáteční záznamy, hodnoty vypočítaných agregačních funkcí a seznam záznamů základního zdroje dat, který patří do skupiny.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Agregační funkce

Za běhu se každý agregovaný výpočet provádí pro každou skupinu záznamů. Tento výpočet se provádí pomocí hodnoty jednoho pole nebo výrazu v záznamech zdroje dat, který byl vybrán pro seskupení v upravitelném zdroji dat typu **GroupBy**. V současné době jsou podporovány následující agregační funkce:

- **AVG** – Tato funkce vrací průměr hodnot ve skupině. Lze jej použít pouze s číselnými poli.
- **POČET** – Tato funkce vrací počet položek, které byly nalezeny ve skupině.
- **Min** – Tato funkce vrací minimální hodnotu mezi hodnotami ve skupině.
- **Max** – Tato funkce vrací maximální hodnotu mezi hodnotami ve skupině.
- **SUM** – Tato funkce vrací součet všech hodnot ve skupině. Lze jej použít pouze s číselnými poli.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Místo provedení

Když upravíte zdroj dat **GroupBy** a zadáte základní datový zdroj, který obsahuje záznamy, které musí být seskupeny, systém automaticky detekuje nejúčinnější [umístění](#ExecutionLocation) pro provedení toho zdroje dat **GroupBy**. Pokud je základní zdroj dat [dotazovatelný](er-functions-list-filter.md#usage-notes) (tj. pokud ji lze spustit na úrovni databáze), je aplikační databáze také určena jako spouštěcí umístění upravitelného zdroje dat **GroupBy**. V opačném případě je jako místo provádění určena paměť aplikačního serveru.

Automaticky zjištěné umístění provádění můžete ručně změnit výběrem umístění, které je použitelné pro nakonfigurovaný zdroj dat. Pokud vybrané místo provádění nelze použít, je v době návrhu vyvolána [chyba ověření](er-components-inspections.md#i5).

> [!TIP]
> Doporučujeme použít umístění databáze k seskupení zdrojů dat, které odhalují velké množství záznamů.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Spotřeba paměti

Ve výchozím nastavení, pokud zdroj dat **GroupBy** běží v paměti, paměť aplikačního serveru se používá k ukládání záznamů o základním datovém zdroji, který patří do každé zjištěné skupiny, jako záznamy jedné skupiny. Chcete-li snížit spotřebu paměti, můžete potlačit ukládání záznamů pro zdroj dat **GroupBy** zdroje dat, pokud byly nakonfigurovány tak, aby počítaly pouze agregované funkce a záznamy jejich skupiny se nepoužívají za běhu. Chcete-li tímto způsobem snížit spotřebu paměti, povolte funkci **Snížit využití paměti v ER, když se seskupování záznamů používá pouze k výpočtu agregací** v pracovním prostoru **Správa funkcí**.

## <a name="alternatives"></a><a name="Alternatives"></a>Alternativy

Podobné agregace lze vypočítat pomocí [odlišných](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) typů zdrojů dat nebo vestavěných funkcí ER.

Chcete-li získat další informace o této funkci, vyplňte následující příklad.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Příklad: Použití zdroje dat GROUPBY pro agregované výpočty a seskupování záznamů

Tento příklad ukazuje, jak může uživatel v roli správce systému nebo funkčního poradce pro elektronické vykazování konfigurovat mapování modelu ER, které má zdroj dat **GROUPBY**, který se používá k výpočtu agregačních funkcí a seskupování a seskupených záznamů. Toto mapování modelu se používá pro tisk kontrolního hlášení při generování výkazu Intrastat. Tato sestava vám umožňuje zkontrolovat vykázané transakce Intrastat.

Postupy v tomto příkladu lze provést ve společnosti **DEMF** v Microsoft Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Příprava ukázkových dat

Ujistěte se, že máte transakce Intrastat pro vykazování ve stránce **Intrastat**. Musíte mít transakce pro různé přepravní kódy, protože budete seskupovat transakce podle pole **Doprava** v tomto příkladu.

![Příprava transakcí Intrastat na stránce Intrastat.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Konfigurace rámce ER

Postupujte podle kroků uvedených v části [Konfigurace architektury ER](er-quick-start2-customize-report.md#ConfigureFramework) a nastavte minimální sadu parametrů ER. Toto nastavení musíte dokončit, než začnete používat architekturu ER k návrhu mapování modelu ER.

### <a name="import-the-standard-er-format-configuration"></a>Import standardní konfigurace formátu ER

Postupujte podle kroků uvedených v části [Import standardní konfigurace formátu ER](er-quick-start2-customize-report.md#ImportERSolution1) a přidejte standardní konfigurace ER do vaší aktuální instance Dynamics 365 Finance. Importujte verzi 1 konfigurace **modelu Intrastat** z úložiště.

### <a name="create-a-custom-data-model-configuration"></a>Vytvoření vlastní konfigurace datového modelu

Postupujte podle kroků v [Přidání vlastní konfigurace datového modelu](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) pro ruční přidání nové konfigurace datového modelu ER **modelu Intrastat (Litware)**, kterou odvodíte z importované konfigurace **modelu Intrastat**.

### <a name="configure-a-custom-data-model-component"></a>Konfigurace vlastní komponenty datového modelu

Chcete-li provést požadované změny v odvozeném datovém modelu **modelu Intrastat (Litware)**, postupujte podle těchto kroků, aby ho bylo možné použít k odhalení transportních kódů, které mají požadované podrobnosti.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Model Intrastat (Litware)**.
3. Vyberte možnost **Návrhář**.
4. Na stránce **Návrhář datového modelu** ve stromu modelů vyberte **Intrastat**.
5. Vyberte **Nový** pro přidání nového vnořeného uzlu pro vybraný uzel **Intrastat**. V rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Do pole **Název** zadejte **Přenos**.
    2. V poli **Typ položky** vyberte **Seznam záznamů**.
    3. Kliknutím na **Přidat** přidáte nový uzel.

6. Vyberte **Nový** pro přidání nového vnořeného uzlu pro uzel **Přenos**, který jste právě přidali. V rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Do pole **Název** zadejte **Kód**.
    2. V poli **Typ položky** vyberte **Řetězec**.
    3. Kliknutím na **Přidat** přidáte nový uzel.

7. Vyberte **Nový** pro přidání dalšího nového vnořeného uzlu pro uzel **Přenos**. V rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Do pole **Název** zadejte **TotalInvoicedAmount**.
    2. V poli **Typ položky** vyberte **Reálný**.
    3. Kliknutím na **Přidat** přidáte nový uzel.

8. Vyberte **Nový** pro přidání dalšího nového vnořeného uzlu pro uzel **Přenos**. V rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Do pole **Název** zadejte **NumberOfTransactions**.
    2. V poli **Typ položky** vyberte **Celé číslo**.
    3. Kliknutím na **Přidat** přidáte nový uzel.

9. Vyberte **Nový** pro přidání dalšího nového vnořeného uzlu pro uzel **Přenos**. V rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Do pole **Název** zadejte **Transaction**.
    2. V poli **Typ položky** vyberte **Seznam záznamů**.
    3. Kliknutím na **Přidat** přidáte nový uzel.

10. Pro uzel **Transakce**, který jste právě přidali, na pevné záložce **Uzel** vyberte **Přepnout odkaz na položku**.
11. V dialogovém okně **Přepnout odkaz na položku** ve stromu datového modelu vyberte **CommodityRecord**. Pak vyberte **OK**.

![Konfigurovaný datový model v návrháři datového modelu ER.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Dokončení návrhu vlastního datového modelu

Postupujte podle kroků v [Dokončení návrhu datového modelu](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) k dokončení návrhu odvozeného datového modelu **Model Intrastat (Litware)**.

### <a name="create-a-new-model-mapping-configuration"></a>Vytvoření nové konfigurace mapování modelu

Postupujte podle kroků v [Vytvoření nové konfigurace modelu](er-quick-start1-new-solution.md#CreateModelMapping) pro ruční přidání nové konfigurace mapování modelu ER **mapování ukázky ER** pro odvozenou konfiguraci **modelu Intrastat (Litware)**.

### <a name="add-a-new-model-mapping-component"></a>Přidání nové komponenty mapování modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací rozbalte konfiguraci **Model Intrastat**.
3. Vyberte konfiguraci **Mapování ukázky Intrastat**.
4. Výběrem možnosti **Návrhář** otevřete seznam mapování.
5. Vyberte **Odstranit** k odstranění stávající komponenty mapování.
6. K přidání nové komponenty mapování klikněte na tlačítko **Nový**.
7. V poli **Definice** zadejte **Intrastat**.
8. Do pole **Název** zadejte **Mapování Intrastat**.
9. Ke konfiguraci nového mapování vyberte možnost **Návrhář**.

### <a name="design-the-added-model-mapping-component"></a>Návrh přidaného komponentu mapování modelu

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Přidání zdroje dat pro přístup k aplikační tabulce

Konfigurace zdroje dat pro přístup k aplikačním tabulkám, které obsahují údaje transakcí Intrastat.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Záznamy tabulky**.
2. V podokně **Zdroj dat** vyberte **Přidat root** pro přidání nového zdroje dat, který bude použit pro přístup k tabulce **Intrastat**. Každý záznam v tabulce **Intrastat** představuje jednu transakci Intrastat.
3. V dialogovém okně **Vlastnosti zdroje dat** v poli **Název** zadejte **Transakce**.
4. Do pole **Tabulka** zadejte **Intrastat**.
5. Vyberte **OK** pro přidání nového zdroje dat.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>Přidání zdroje dat do skupiny transakcí Intrastat

Nakonfigurujte zdroj dat **GroupBy** pro seskupení transakcí Intrastat a výpočet agregačních funkcí.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Funkce\\Seskupit podle**.
2. V podokně **Zdroj dat** vyberte **Přidat root** pro přidání nového zdroje dat, který bude použit k seskupení transakcí Intrastat a vypočtu agregačních funkcí.
3. V dialogovém okně **Vlastnosti zdroje dat** v poli **Název** zadejte **TransportRecord**.
4. Vyberte **Upravit seskupit podle** pro konfiguraci podmínek seskupování.
5. Na stránce **Upravit parametry „Seskupit podle“** v seznamu zdrojů dat v pravém podokně vyberte zdroj dat **Transakce** dat a rozbalte ho.
6. Vyberte **Přidat pole do \> Co seskupit** k určení, že zdroj dat **Transakce** dat je vybrán jako <a name="BaseDataSource">základní zdroj dat</a> pro nakonfigurovaný zdroj dat **GroupBy**. Záznamy o zdroji dat **Transakce** dat budou seskupeny a hodnoty polí tohoto zdroje dat budou použity pro výpočty v agregačních funkcích.
7. Vyberte pole **Transakce\Přenos** a poté vyberte **Přidat pole do \> Seskupené pole** k určení, že pole **Přenos** základního zdroje dat je vybráno jako <a name="GroupingFields">seskupovací kritérium</a> pro nakonfigurovaný zdroj dat **GroupBy**. Jinými slovy, záznamy o zdroji dat **Transakce** budou seskupen na základě hodnoty pole **Přenos**. Každý záznam konfigurovaného zdroje dat **GroupBy** bude představovat jeden transportní kód, který byl nalezen v záznamech základního zdroje dat.
8. Vyberte pole **Transakce\AmountMST** a poté postupujte takto:

    1. Vyberte **Přidat pole do \> Agregovaná pole** k určení, že <a name="AggregateFunctions">agregační funkce</a> bude vypočítána pro toto pole.
    2. V podokně **Agregace** v záznamu, který byl přidán pro vybrané pole **Transakce\AmountMST** v poli **Metoda** vyberte funkci **Součet**.
    3. Do volitelného pole **Název** zadejte **TotalInvoicedAmount**.

    Tato nastavení určují, že pro každou skupinu přenosu bude celková částka pole **Transakce\AmountMST** vypočítána.

9. Vyberte pole **Transakce\RecId** a poté postupujte takto:

    1. Vyberte **Přidat pole do \> Agregovaná pole** k určení, že agregační funkce bude vypočítána pro toto pole.
    2. V podokně **Agregace** v záznamu, který byl přidán pro vybrané pole **Transakce\RecId** v poli **Metoda** vyberte funkci **Počet**.
    3. Do volitelného pole **Název** zadejte **NumberOfTransactions**.

    Tato nastavení určují, že pro každou skupinu přenosu bude vypočten počet transakcí ve skupině.

10. Zvolte možnost **Uložit**.
11. Zkontrolujte parametry <a name="ExecutionLocation">spuštění</a> upravitelného zdroje dat. Všimněte si, že **Automatická detekce** bylo automaticky vybráno v poli **Místo spuštění** a pole **Spuštění v** obsahuje hodnotu **SQL**. Tato nastavení určují, že vybraný základní zdroj dat **Transakce** je aktuálně dotazovatelný a můžete spustit upravitelný zdroj dat **GroupBy** na úrovni databáze.
12. Otevřete vyhledávání pro pole **Místo spuštění** pro zobrazení seznamu dostupných hodnot. Všimněte si, že si můžete vybrat **Dotaz** nebo **V paměti** a vynutit, aby byl tento zdroj dat **GroupBy** spuštěn na úrovni databáze nebo v paměti aplikačního serveru.
13. Vyberte **Uložit** a zavřete stránku **Upravit parametry „Seskupit podle“**.
14. Vyberte **OK** pro dokončení nastavení zdroje dat **GroupBy**.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>Navázání zdroje dat GroupBy na pole zdrojů dat

Konfigurované zdroje dat svažte s poli datového modelu a určete, jak bude datový model vyplněn aplikačními daty za běhu.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** rozbalte uzel **Přenos**.
2. V podolně **Zdroje dat** rozbalte zdroj dat **TransportRecord**.
3. Chcete-li zobrazit seznam nalezených skupin přenosu, přidejte vazbu:

    1. V podokně **Datový model** vyberte položku **Přenos**.
    2. V podolně **Zdroje dat** vyberte zdroj dat **TransportRecord**.
    3. Vyberte možnost **vazba**.

4. Chcete-li zobrazit kód přenosu jednotlivých nalezených skupin přenosu:

    1. Vyberte položku datového modelu **Transport.Code**.
    2. Vyberte seskupené pole **TransportRecord.grouped.TransportMode**.
    3. Vyberte možnost **vazba**.

5. Přidejte vazbu k odhalení hodnot vypočítaných agregačních funkcí pro každou zjištěnou transportní skupinu:

    1. Vyberte položku datového modelu **Transport.NumberOfTransactions**.
    2. Vyberte agregované pole **TransportRecord.agregated.NumberOfTransactions**.
    3. Vyberte možnost **vazba**.
    4. Vyberte položku datového modelu **Transport.TotalInvoicedAmount**.
    5. Vyberte agregované pole **TransportRecord.agregated.TotalInvoicedAmount**.
    6. Vyberte možnost **vazba**.

6. Přidejte vazbu k odhalení záznamů transakcí, které patří do každé zjištěné skupiny přenosu:

    1. Vyberte položku datového modelu **Transport.Transaction**.
    2. Vyberte pole **TransportRecord.lines**.
    3. Vyberte možnost **vazba**.

    Můžete pokračovat v konfiguraci vazeb pro vnořené položky položky datového modelu **ransport.Transaction** a pole zdroje dat **TransportRecord.lines**, abyste za běhu odhalili podrobnosti o transakcích Intrastat, které patří do každé zjištěné skupiny přenosu.

![Konfigurovaný model mapování v návrháři mapového modelu ER.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Ladění přidaného komponentu mapování modelu

Pomocí [ladicího programu zdroje dat ER](er-debug-data-sources.md) otestujte nakonfigurované mapování modelu.

1. Na stránce **vývojáře Mapování modelu** vyberte **Spustit ladění**.
2. Na stránce **Ladění zdrojů dat** v levém podokně vyberte vyberte zdroj dat **TransportRecord** a poté vyberte možnost **Přečíst všechny záznamy**.
3. Rozbalte zdroj dat **TransportRecord** a poté postupujte takto:

    1. Vyberte zdroj dat **TransportRecord.grouped.TransportMode**.
    2. Vyberte **Získat hodnotu**.
    3. Vyberte zdroj dat **TransportRecord.grouped.NumberOfTransactions**.
    4. Vyberte **Získat hodnotu**.
    5. Vyberte zdroj dat **TransportRecord.grouped.TotalInvoicedAmount**.
    6. Vyberte **Získat hodnotu**.

4. V pravém podokně vyberte **Rozbalit vše**.

Zdroj dat **TransportRecord** odhaluje dva záznamy a představuje dva kódy přenosu. Pro každý kód přenosu je vypočítán počet transakcí a celková fakturovaná částka.

> [!NOTE]
> Přístup „líného čtení“ se používá, když se zdroj dat **GroupBy** volá za účelem optimalizace volání databáze. Proto se některé hodnoty polí ve zdroji dat **GroupBy** počítají v ladicím programu zdroje dat ER pouze v případě, že jsou vázány na pole datového modelu.

![Výsledky ladění zdroje dat na stránce Ladění zdrojů dat.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Existuje nějaký způsob, jak vypočítat celkové součty při výpočtu součtů skupiny?

Ano. Chcete-li vypočítat celkové součty, nakonfigurujte další zdroj dat **GroupBy**, kde se používá zdroj dat **GroupBy**, který jste dříve nakonfigurovali, jako základní zdroj dat. Následující obrázek ukazuje zdroj dat **Součty** typu **GroupBy**, který se používá k výpočtu agregační funkce **SOUČET** na základě agregace **SOUČET** zdroje dat **TransportRecord** typu **GroupBy**.

![Zdroj dat Součet v návrháři mapování modelů ER.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Následující obrázek ukazuje výsledky ladění zdroje dat **Součty**.

![Výsledky ladění zdroje dat Součty na stránce Ladění zdrojů dat.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace](er-debug-data-sources.md)
- [Používejte datové zdroje SHROMAŽĎOVÁNÍ DAT ve formátech elektronického hlášení](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
