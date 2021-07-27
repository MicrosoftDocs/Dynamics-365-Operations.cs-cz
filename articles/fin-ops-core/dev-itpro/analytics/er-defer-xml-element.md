---
title: Odložení provádění prvků XML ve formátech elektronického výkaznictví
description: V tomto tématu je vysvětleno, jak odložit provádění prvku XML ve formátu elektronického výkaznictví.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f89c671ae012907a4c3e07c09bdc867c1d67a101
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348062"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>Odložení provádění prvků XML ve formátech elektronického výkaznictví

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

Můžete použít návrháře operací rámce [elektronického výkaznictví](general-electronic-reporting.md) pro [konfiguraci](./tasks/er-format-configuration-2016-11.md) [komponenty formátu](general-electronic-reporting.md#FormatComponentOutbound) řešení elektronického výkaznictví, které se používá ke generování odchozích dokumentů ve formátu XML. Hierarchická struktura konfigurované součásti formátu sestává z prvků formátu různých typů. Tyto prvky formátu se používají k vyplňování vygenerovaných dokumentů s požadovanými informacemi za běhu. Při spuštění formátu elektronického výkaznictví jsou ve výchozím nastavení prvky formátu spouštěny ve stejném pořadí, v jakém jsou uvedeny v hierarchii formátu: jeden po druhém, shora dolů. Avšak v době návrhu můžete změnit pořadí provádění pro libovolné prvky XML v konfigurované součásti formátu.

Zapnutím možnosti <a name="DeferredXmlElementExecution"></a>**odloženého provedení** pro prvek XML v konfigurovaném formátu můžete odložit (pozdržet) provedení tohoto prvku. V tomto případě se prvek nespustí, dokud nejsou spuštěny všechny ostatní prvky nadřazené položky.

Chcete-li získat další informace o této funkci, vyplňte příklad tomto tématu.

## <a name="limitations"></a>Omezení

Možnost **odloženého provedení** je podporována pouze u prvků XML, které jsou nakonfigurovány pro formát elektronického výkaznictví, který slouží ke generování **odchozích** dokumentů ve formátu XML.

Možnost **odloženého provedení** je podporována pouze u prvků XML, které se nacházejí pouze v jednom dalším prvku XML. Proto není použitelné pro prvky XML, které se nacházejí v jiných typech prvků formátu (například v prvku **posloupnost XML**).

Možnost **odloženého provedení** není podporována u prvků XML, které se nacházejí v prvku formátu **Common\\File**, pokud je možnost **Rozdělit soubor** nastavena na **Ano**. Informace o rozdělení souborů XML naleznete v části [Rozdělení generovaných souborů XML na základě velikosti souboru a množství obsahu](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Příklad: Odložení provádění prvku XML ve formátu elektronického výkaznictví

Následující postup vysvětluje, jak může uživatel v [roli](../sysadmin/tasks/assign-users-security-roles.md) správce systému nebo funkčního konzultanta elektronického výkaznictví konfigurovat formát elektronického výkaznictví, který obsahuje prvek XML, kde se pořadí provádění liší od pořadí v hierarchii formátu.

Tyto kroky lze provést ve společnosti **USMF** v aplikaci Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Předpoklady

K dokončení tohoto příkladu v tomto tématu musíte mít přístup ke společnosti **USMF** v aplikaci Finance pro některou z následujících rolí:

- Funkční konzultant elektronického výkaznictví
- Správce systému

Pokud jste ještě nedokončili příklad v části [Odložení provádění prvků posloupnosti ve formátech elektronického výkaznictví](er-defer-sequence-element.md#Example), stáhněte si následující [konfigurace](general-electronic-reporting.md#Configuration) ukázkového řešení elektronického výkaznictví.

| Popis obsahu            | Název souboru |
|--------------------------------|-----------|
| Konfigurace datového modelu elektronického výkaznictví    | [Model to learn deferred elements.version.1.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| Konfigurace mapování modelu elektronického výkaznictví | [Mapping to learn deferred elements.version.1.1.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Než začnete, musíte také stáhnout a uložit následující konfiguraci ukázkového řešení elektronického výkaznictví do svého místního počítače.

| Popis obsahu     | Název souboru |
|-------------------------|-----------|
| Konfigurace formátu elektronického výkaznictví | [Format to learn deferred XML elements.version.1.1.xml](https://download.microsoft.com/download/4/7/8/478fa846-22e9-4fa0-89b1-d3aeae660067/FormattolearndeferredXMLelements.version.1.1.xml) |

### <a name="import-the-sample-er-configurations"></a>Import ukázkových konfigurací elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Na stránce **Konfigurace**, pokud **Model to learn deferred elements** není ve stromu konfigurací k dispozici, importujte konfiguraci datového modelu elektronického výkaznictví:

    1. Vyberte **Exchange** a poté vyberte **Načíst ze souboru XML**.
    2. Vyberte **Procházet** najděte a vyberte soubor **Model to learn deferred elements.1.xml** a poté vyberte **OK**.

4. Pokud konfigurace **Mapping to learn deferred elements** není ve stromu konfigurací k dispozici, importujte konfiguraci datového modelu elektronického výkaznictví:

    1. Vyberte **Exchange** a poté vyberte **Načíst ze souboru XML**.
    2. Vyberte **Procházet** najděte a vyberte soubor **Mapping to learn deferred elements.1.xml** a poté vyberte **OK**.

5. Import konfigurace formátu elektronického výkaznictví:

    1. Vyberte **Exchange** a poté vyberte **Načíst ze souboru XML**.
    2. Vyberte **Procházet** najděte a vyberte soubor **Format to learn deferred XML elements.1.1.xml** a poté vyberte **OK**.

6. Ve stromu konfigurace rozbalte **Model to learn deferred elements**.
7. Zkontrolujte seznam importovaných konfigurací elektronického výkaznictví ve stromu konfigurace.

    ![Importované konfigurace elektronického výkaznictví na stránce konfigurace.](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Aktivace poskytovatele konfigurace

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurace** ověřte, že je uveden [poskytovatel konfigurace](general-electronic-reporting.md#Provider) ukázkové společnosti Litware, Inc. (`http://www.litware.com`) a že je označen jako aktivní. Není-li tento poskytovatel konfigurace uveden v seznamu nebo není-li označen jako aktivní, postupujte podle kroků v tématu [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Ukázková společnost Litware, Inc. na stránce konfigurace lokalizace.](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Kontrola importovaného mapování modelu

Zkontrolujte nastavení součásti mapování modelu elektronického výkaznictví, která je nakonfigurována pro přístup k daňovým transakcím a vystavení přístupových dat na vyžádání.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Na stránce **Konfigurace** ve stromu konfigurací rozbalte **Model to learn deferred elements**.
4. Vyberte konfiguraci **Mapping to learn deferred elements**.
5. Výběrem možnosti **Návrhář** otevřete seznam mapování.
6. Chcete-li zkontrolovat podrobnosti mapování, vyberte možnost **Návrhář**.
7. Vyberte **Zobrazit podrobnosti**.
8. Zkontrolujte zdroje dat, které jsou nakonfigurovány pro přístup k daňovým transakcím:

    - Datový zdroj **Transakce** typu *Záznam tabulky* je nakonfigurován pro přístup k záznamům tabulky aplikace **TaxTrans**.
    - Datový zdroj **Doklady** typu *Vypočítané pole* je nakonfigurován tak, aby vracel požadované kódy dokladů (**INV-10000349** a **INV-10000350**) jako seznam záznamů.
    - Datový zdroj **Filtrovaný** typu *Vypočítané pole* je nakonfigurován tak, aby ze zdroje dat **Transakce** vybral pouze daňové transakce požadovaných dokladů.
    - Pole **\$TaxAmount** typu *Vypočítané pole* je přidáno do datového zdroje **Filtrované** za účelem vystavení hodnoty daně s opačným znaménkem.
    - Datový zdroj **Seskupený** typu *Seskupit podle* je nakonfigurován tak, aby seskupoval filtrované daňové transakce datového zdroje **Filtrované**.
    - Pole agregace **TotalSum** datového zdroje **Seskupený** je nakonfigurováno tak, aby shrnoval hodnoty pole **\$TaxAmount** datového zdroje **Filtrované** pro všechny filtrované daňové transakce zdroje dat.

        ![Pole agregace TotalSum na stránce Úpravy parametrů GroupBy.](./media/ER-DeferredXml-GroupByParameters.png)

9. Zkontrolujte, jakým způsobem jsou nakonfigurované zdroje dat navázány na datový model a jakým způsobem vystavují data přístupu k jejich zpřístupnění ve formátu elektronického výkaznictví:

    - Datový zdroj **Filtrovaný** je navázán na pole **Data.List** datového modelu.
    - Pole **\$TaxAmount** datového zdroje **Filtrovaný** je navázán na pole **Data.List.Value** datového modelu.
    - Pole **TotalSum** datového zdroje **Seskupený** je navázán na pole **Data.Summary.Total** datového modelu.

    ![Stránka návrháře mapování modelu.](./media/ER-DeferredXml-ModelMapping.png)

10. Zavřete stránky **Návrhář mapování modelu** a **Mapování modelu**.

### <a name="review-the-imported-format"></a>Kontrola importovaného formátu

1. Na stránce **Konfigurace** ve stromu konfigurace vyberte konfiguraci **Format to learn deferred XML elements**.
2. Chcete-li zkontrolovat podrobnosti formátu, vyberte možnost **Návrhář**.
3. Vyberte **Zobrazit podrobnosti**.
4. Zkontrolujte nastavení součástí formátu elektronického výkaznictví, které jsou nakonfigurovány pro generování odchozího dokumentu ve formátu XML, který obsahuje podrobnosti o daňových transakcích:

    - Prvek XML **Report\\Message** je nakonfigurován tak, aby vyplnil odchozí dokument jedním uzlem, který obsahuje vnořené prvky XML (**Záhlaví**, **Záznam** a **Souhrn**).
    - Prvek fXML **Report\\Message\\Header** je nakonfigurován tak, aby vyplnil odchozí dokument jedním uzlem záhlaví, který zobrazuje datum a čas zahájení zpracování.
    - Prvek XML **Report \\Message\\Record** je nakonfigurován tak, aby vyplnil odchozí dokument jedním uzlem záznamu, který zobrazuje podrobnosti jednotlivé daňové transakce.
    - Prvek XML **Report\\Message\\Summary** je nakonfigurován tak, aby vyplnil odchozí dokument jedním uzlem souhrnu, který zahrnuje souhrn hodnot daně ze zpracovaných daňových transakcí.

    ![Prvek XML zprávy a vnořené prvky XML na stránce Návrhář formátu.](./media/ER-DeferredXml-Format.png)

5. Na kartě **Mapování** zkontrolujte následující podrobnosti:

    - Prvek **Report\\Message\\Header** nemusí být vázán na zdroj pro generování jednoho uzlu v odchozím dokumentu.
    - Atribut **ExecutionDateTime** generuje datum a čas (včetně milisekund), kdy je přidán uzel záhlaví.
    - Prvek **Report\\Message\\Record** je vázán na seznam **model.Data.List** pro generování jednoho uzlu záznamu pro každý záznam z vázaného seznamu.
    - Atribut **TaxAmount** je vázán na **model.Data.List.Value** (který je zobrazen jako **\@.Value** v zobrazení relativní cesty) pro generování hodnoty daně aktuální daňové transakce.
    - Atribut **RunningTotal** je zástupný symbol pro mezisoučet hodnot daně. V současné době nemá tento atribut žádný výstup, protože pro něj není nakonfigurována ani vazba ani výchozí hodnota.
    - Atribut **ExecutionDateTime** generuje datum a čas (včetně milisekund), kdy je v této sestavě zpracována aktuální transakce.
    - Prvek **Report\\Message\\Summary** nemusí být vázán na datový zdroj pro generování jednoho uzlu v odchozím dokumentu.
    - Atribut **TotalTaxAmount** je vázán na **model. Data.Summary.Total** pro vygenerování součtu hodnot daně zpracovaných daňových transakcí.
    - Atribut **ExecutionDateTime** generuje datum a čas (včetně milisekund), kdy je přidán uzel souhrnu.

    ![Karta mapování na stránce Návrhář formátu.](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Spuštění importovaného formátu

1. Na stránce **Návrhář formátu** zvolte **Spustit**.
2. Stáhněte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Stažený soubor importovaného formátu.](./media/ER-DeferredXml-Run.png)

Povšimněte si, že souhrnný uzel představuje součet hodnot daně pro zpracované transakce. Vzhledem k tomu, že formát je konfigurován pro použití vazby **model.Data.Summary.Total** pro vrácení tohoto souhrnu, vypočte se součet voláním agregace **TotalSum** datového zdroje **Seskupený** typu *GroupBy* v mapování modelu. Pro výpočet této agregace prochází mapování modelů všechny transakce, které byly vybrány ve zdroji dat **Filtrované**. Porovnáním dob provádění na souhrnném uzlu a v posledním uzlu záznamu můžete určit, že výpočet součtu trvá 12 milisekund (MS). Porovnáním dob provádění prvního a posledního uzlu záznamu můžete určit, že generování všech uzlů záznamu trvalo 9 ms. Z tohoto důvodu je nutné celkem 21 ms.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Upravte formát tak, aby výpočet byl založen na generovaném výstupu.

Pokud je objem transakce mnohem větší než objem v aktuálním příkladu, může se čas výpočtu zvýšit a způsobit problémy s výkonem. Změnou nastavení formátu můžete předejít těmto problémům s výkonem. Protože přistupujete k hodnotám daně, které mají být zahrnuty do generované sestavy, můžete tyto informace znovu použít k výpočtu hodnot daně. Další informace naleznete v tématu [Konfigurace formátu počítání a sčítání](./tasks/er-format-counting-summing-1.md).

1. Na stránce **Návrhář formátu** na kartě **Formát** vyberte ve stromu formátu prvek souboru **Sestava**.
2. Nastavte možnost **Podrobnosti výstupu shromažďování** na **Ano**. Nyní můžete tento formát konfigurovat použitím obsahu vygenerované sestavy jako zdroje dat, ke kterému lze získat přístup pomocí vestavěných funkcí elektronického výkaznictví v kategorii [shromažďování dat](er-functions-category-data-collection.md).
3. Na kartě **Mapování** vyberte prvek XML **Report\\Message\\Record**.
4. Konfigurujte výraz **Název klíče shromážděných dat** jako `WsColumn`.
5. Konfigurujte výraz **Hodnota klíče shromážděných dat** jako `WsRow`.

    ![Prvek XML záznamu na stránce Návrhář formátu.](./media/ER-DeferredXml-Format3.png)

6. Vyberte atribut **Report\\Message\\Record\\TaxAmount**.
7. Konfigurujte výraz **Název klíče shromážděných dat** jako `SummingAmountKey`.

    ![Atribut TaxAmount na stránce Návrhář formátu.](./media/ER-DeferredXml-Format4.png)

    Toto nastavení je možné vzít v úvahu při plnění virtuálního listu, kde je hodnota buňky A1 připojena k hodnotě částky daně z každé zpracované daňové transakce.

8. Vyberte atribut **Report\\Message\\Record\\RunningTotal** a poté zvolte **Upravit vzorec**.
9. Nakonfigurujte výraz `SUMIF(SummingAmountKey, WsColumn, WsRow)` pomocí vestavěné funkce elektronického výkaznictví [SUMIF](er-functions-datacollection-sumif.md) a poté zvolte **Uložit**.

    ![Výraz SUMIF.](./media/ER-DeferredXml-FormulaDesigner.png)

10. Zavřete stránku **Návrhář vzorce**.
11. Vyberte **Uložit** a potom **Spustit**.
12. Stáhněte a zkontrolujte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Generovaný seznam hodnoty daně s průběžným součtem.](./media/ER-DeferredXml-Run1.png)

    Poslední uzel záznamu obsahuje mezisoučet hodnot daně, který se vypočítává pro všechny zpracované transakce s použitím generovaného výstupu jako zdroje dat. Tento zdroj dat začíná od začátku sestavy a pokračuje k poslední daňové transakci. Uzel souhrnu obsahuje součet hodnot daně ze všech zpracovaných transakcí, které jsou vypočteny v mapování modelu pomocí zdroje dat typu *GroupBy*. Všimněte si, že tyto hodnoty jsou stejné. Z tohoto důvodu lze použít souhrn založený na výstupu namísto **GroupBy**. Porovnáním dob provádění prvního uzlu záznamu a uzlu souhrnu můžete určit, že generování všech uzlů záznamu a součtu trvalo 11 ms. Proto, pokud jde o generování uzlů řádku a sčítání daňových hodnot, je upravený formát přibližně dvakrát rychlejší než původní formát.

13. Vyberte atribut **Report\\Message\\Summary\\TotalTaxAmount** a poté zvolte **Upravit vzorec**.
14. Zadejte výraz `SUMIF(SummingAmountKey, WsColumn, WsRow)` namísto existujícího výrazu.
15. Vyberte **Uložit** a potom **Spustit**.
16. Stáhněte a zkontrolujte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Generovaný seznam daňových hodnot pomocí upraveného vzorce.](./media/ER-DeferredXml-Run2.png)

    Povšimněte si, že mezisoučet daňových hodnot v posledním uzlu záznamu se nyní rovná součtu v uzlu souhrnu.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Vložení hodnot součtu založeného na výstupu v záhlaví sestavy

Je-li například nutné v záhlaví sestavy zobrazit součet daňových hodnot, můžete formát upravit.

1. Na stránce **Návrhář formátu** na kartě **Formát** vyberte prvek XML **Report\\Message\\Summary**.
2. Vyberte **Přesunout nahoru**.
3. Vyberte **Uložit** a potom **Spustit**.
4. Stáhněte a zkontrolujte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Stažený soubor daňových hodnot pro záhlaví sestavy.](./media/ER-DeferredXml-Run3.png)

    Všimněte si, že součet hodnot daně v uzlu souhrnu se nyní rovná 0 (nula), protože tento součet je nyní vypočten na základě generovaného výstupu. Je-li generován první uzel záznamu, vygenerovaný výstup dosud neobsahuje uzly záznamu s podrobnostmi transakce. Tento formát lze nakonfigurovat tak, aby odložil provádění prvku **Report\\Message\\Summary**, dokud prvek **Report\\Message\\Record** nebyl spuštěn pro všechny daňové transakce.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Odložení provedení prvku XML tak, aby byl použit vypočtený součet

1. Na stránce **Návrhář formátu** na kartě **Formát** vyberte prvek XML **Report\\Message\\Summary**.
2. Nastavte možnost **Odložené provedení** na **Ano**.

    ![Možnost odloženého provedení prvku XML souhrnu na stránce Návrhář formátu.](./media/ER-DeferredXml-Format5.png)

3. Vyberte **Uložit** a potom **Spustit**.
4. Stáhněte a zkontrolujte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Stažený soubor odloženého provedení.](./media/ER-DeferredXml-Run4.png)

    Prvek **Report\\Message\\Summary** je nyní spuštěn pouze po spuštění všech ostatních položek, které jsou vnořeny pod svým nadřazeným prvkem **Report\\Message**. Proto je spuštěn po spuštění prvku **Report\\Message\\Record** pro všechny daňové transakce datového zdroje **model.Data.List**. Doba provádění prvního a posledního uzlu záznamu a uzlů záhlaví a souhrnu, odhalí tuto skutečnost.

## <a name="additional-resources"></a>Další zdroje

- [Konfigurace formátu počítání a sčítání](./tasks/er-format-counting-summing-1.md)
- [Sledování provádění formátu elektronického výkaznictví za účelem řešení potíží s výkonem](trace-execution-er-troubleshoot-perf.md)
- [Odložení provádění prvků posloupnosti ve formátech elektronického výkaznictví](er-defer-sequence-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
