---
title: Používejte datové zdroje SHROMAŽĎOVÁNÍ DAT ve formátech elektronického hlášení
description: Tento článek vysvětluje, jak je možné používat datové zdroje SHROMAŽĎOVÁNÍ DAT ve formátech Elektronického výkaznictví (ER).
author: NickSelin
ms.date: 08/23/2021
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
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 7591bed5d01ce2c2f434f0e7c81e441eda98483e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883839"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>Používejte datové zdroje SHROMAŽĎOVÁNÍ DAT ve formátech elektronického hlášení

[!include [banner](../includes/banner.md)]

Můžete použít návrháře operací architektury [Elektronického výkaznictví (ER)](general-electronic-reporting.md) pro konfiguraci komponenty formátu řešení elektronického výkaznictví, které se používá ke generování odchozích dokumentů v různých formátech. Hierarchická struktura konfigurované součásti formátu sestává z prvků formátu různých typů. Tyto prvky formátu se používají k vyplňování vygenerovaných dokumentů s požadovanými informacemi za běhu. Při spuštění formátu elektronického výkaznictví jsou ve výchozím nastavení prvky formátu spouštěny ve stejném pořadí, v jakém jsou uvedeny v hierarchii formátu: jeden po druhém, shora dolů.

Když ER spustí element formátu, který obsahuje vazbu, spustí se vzorec této vazby a element formátu přidá hodnotu do generovaného dokumentu. Vazba může například předat hodnotu a pole datový model na prvek formátu. Zdroj dat SHROMAŽĎOVÁNÍ DAT můžete nakonfigurovat tak, aby sbíral hodnoty polí datového modelu za běhu, prováděl sčítání hodnot a generovaný dokument vyplnil shromážděnými hodnotami. Chcete-li použít tento přístup, změňte počáteční vazbu, aby se konfigurovaný zdroj dat SHROMAŽĎOVÁNÍ DAT použil k předání hodnoty pole datového modelu prvku formátu. Předáním hodnot prostřednictvím zdroje dat SHROMAŽĎOVÁNÍ DAT můžete shromažďovat požadované podrobnosti pro další použití.

Při konfiguraci zdroje dat SHROMAŽĎOVÁNÍ DAT zadejte typ hodnoty, který bude spravován ve zdroji dat. Následující [typy dat](er-formula-supported-data-types-primitive.md) jsou aktuálně podporovány pro shromažďování hodnot:

- Logická
- Datum
- Datum/čas
- GUID
- Int64
- Celé číslo
- Reálný
- Řetězec
- Čas

Můžete použít metodu `Collect(Value)` zdroje dat SHROMAŽĎOVÁNÍ DAT k předání hodnoty zdroji dat ke sběru. V této metodě je argument `Value` buď konstanta, nebo platná cesta pole zdroje dat příslušného datového typu.

Použijte vlastnost `Result` zdroje dat SHROMAŽĎOVÁNÍ DAT pro přístup k seznamu shromážděných hodnot. Tato vlastnost vrací [seznam záznamů](er-formula-supported-data-types-composite.md#record-list). Záznamy v seznamu záznamů obsahují pole `Value`, které můžete použít pro přístup ke shromážděným hodnotám.

Ve výchozím nastavení shromažďuje zdroj dat SHROMAŽĎOVÁNÍ DAT pouze jedinečné hodnoty.

Chcete-li shromáždit všechny hodnoty, nastavte **Shromáždit všechny hodnoty** nakonfigurovaného zdroje dat SHROMAŽĎOVÁNÍ DAT na **Ano**. Když je pole **Shromáždit všechny hodnoty** nastaveno na **Ano**, parametrizovaná vlastnost `Sum(Flag)` bude k dispozici. Tuto vlastnost můžete použít k získání celkového množství všech aktuálně shromážděných hodnot. U tohoto majetku je argument `Flag` je [Logická](er-formula-supported-data-types-primitive.md#boolean) hodnota, která se používá k označení, zda je nutné resetovat celkovou hodnotu.

- Když je poskytnuta hodnota **False**, sčítání pokračuje z dříve vybrané částky.
- V případě hodnoty **True**, spustí se nové sčítání.

Následující typy dat jsou aktuálně podporovány pro sčítání:

- Int64
- Celé číslo
- Reálný

Chcete-li získat další informace o této funkci, vyplňte následující příklad.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Příklad: Nakonfigurujte formát ER tak, aby prováděl počítání a sčítání pomocí zdroje dat SHROMAŽĎOVÁNÍ DAT

Tento příklad ukazuje, jak může uživatel v roli správce systému nebo funkčního poradce pro elektronické vykazování konfigurovat formát ER, který má zdroj dat SHROMAŽĎOVÁNÍ DAT, který se používá k výpočtu běžících součtů a shromažďování součtových hodnot.

Postupy v tomto příkladu lze provést ve společnosti USMF v Microsoft Dynamics 365 Finance.

### <a name="upload-and-use-the-provided-er-solution"></a>Nahrajte a použijte poskytnuté řešení ER

1. [Import ukázkových konfigurací elektronického výkaznictví](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Aktivace poskytovatele konfigurace](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Kontrola importovaného mapování modelu](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Kontrola importovaného formátu](er-defer-sequence-element.md#review-the-imported-format).
5. [Spuštění importovaného formátu](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Spusťte formát poskytovaného řešení ER

1. Na stránce **Návrhář formátu** zvolte **Spustit**.
2. V dialogovém okně **Parametry elektronické sestavy** vyberte **OK**.
3. Stáhněte a zkontrolujte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Stažený soubor, který obsahuje výsledky původního spuštění formátu](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Upravte formát řešení ER tak, aby se vypočítal součet běžící daně

Pokud je objem transakcí mnohem větší než objem v aktuálním příkladu, může se čas sčítání zvýšit a způsobit problémy s výkonem. Změnou nastavení formátu můžete předejít těmto problémům s výkonem. Protože přistupujete k hodnotám daně, které mají být zahrnuty do generované sestavy, můžete tyto informace znovu použít k sčítání hodnot daně.

1. Na stránce **Návrhář formátu** na kartě **Mapování** vyberte **Přidat kořen**.
2. V dialogovém okně **Přidat zdroj dat** vyberte **Funkce** \> **Sběr dat**.
3. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** postupujte takto:

    1. Do pole **Název** zadejte **CollectedTaxValues**.
    2. V poli **Typ položky** vyberte **Reálný**.
    3. Vyberte možnost **Ano** v poli **Zahrnout vše**.
    4. Vyberte **OK**.

4. Vyberte číselný prvek formátu **Report\\Lines\\Record\\TaxAmount**.

    > [!NOTE]
    > V současné době je nakonfigurována vazba `@.Value` pro tento prvek. Vygenerovaný dokument je tedy naplněn daňovými hodnotami z pole `model.Data.List.Value`.

5. Vyberte možnost **Upravit vzorec**.
6. Na stránce **Návrhář vzorců** proveďte následující kroky:

    1. V poli **Vzorec** nahraďte `@.Value` za `CollectedTaxValues.Collect(@.Value)`.
    2. Uložte změny a zavřete stránku.

    > [!NOTE]
    > Nová vazba předá do vygenerovaného dokumentu stejné daňové hodnoty. Tyto hodnoty však budou také shromážděny ve zdroji dat **CollectedTaxValues**.

7. Vyberte číselný prvek formátu **Report\\Lines\\Record\\RunningTotal**.
8. Vyberte možnost **Upravit vzorec**.
9. Na stránce **Návrhář vzorců** proveďte následující kroky:

    1. Do pole **Vzorec** zdejte `CollectedTaxValues.Sum(false)`
    2. Uložte změny a zavřete stránku.

    > [!NOTE]
    > Nová vazba předá generovanému dokumentu celkovou částku daňových hodnot, které již byly zadány.

    ![Numerické prvky, které mají aktualizované vazby na stránce Návrhář formátu](./media/er-data-collection-data-sources-02.png)

10. Vyberte **Uložit** a potom **Spustit**.
11. V dialogovém okně **Parametry elektronické sestavy** vyberte **OK**.
12. Stáhněte a zkontrolujte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Stažený soubor, který obsahuje výsledky upraveného spuštění formátu](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Upravte formát tak, aby vyhodnotil seznam vybraných daní

1. Na stránce **Návrhář formátu** na kartě **Formát** vyberte prvek číselného formátu **Report\\Lines\\Record\\RunningTotal** a poté postupujte takto:

    1. V poli **Číselný typ** změňte hodnotu z **Reálné číslo** na **Celé číslo**.
    2. V poli **Číselný formát** změňte hodnotu z **F2** na **F0**.

3. Na kartě **Mapování** vyberte **Upravit vzorec**.
4. Na stránce **Návrhář vzorců** proveďte následující kroky:

    1. Do pole **Vzorec** zdejte `COUNT(CollectedTaxValues.Result)`
    2. Uložte změny a zavřete stránku.

    > [!NOTE]
    > Nová vazba předá generovanému dokumentu počet záznamů v seznamu, kde jsou shromažďovány hodnoty daně.

5. Vyberte **Uložit** a potom **Spustit**.
6. V dialogovém okně **Parametry elektronické sestavy** vyberte **OK**.
7. Stáhněte a zkontrolujte soubor, který webový prohlížeč nabízí, a otevřete jej k revizi.

    ![Stažený soubor, který obsahuje výsledky dalšího upraveného spuštění formátu](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Pokud mám vypočítat průběžné součty a sbírat data, jaký je rozdíl mezi použitím zdroje dat SHROMAŽĎOVÁNÍ DAT a vestavěnými funkcemi SHROMAŽĎOVÁNÍ DAT?

Zdroj dat SHROMAŽĎOVÁNÍ DAT a vestavěné funkce [SHROMAŽĎOVÁNÍ DAT](er-functions-category-data-collection.md) lze použít pro sběr dat, sčítání a počítání na základě informací předávaných do generovaného odchozího dokumentu. Když se však rozhodujete, jakou techniku použít, musíte vzít v úvahu následující body.

| Zdroj dat | Vestavěné funkce |
|-------------| ------------------ |
| Shromažďují se pouze hodnoty. | <p>Shromažďují se pojmenované hodnoty. Proto lze součty vypočítat pro oddělené skupiny hodnot.</p><p>Skupiny lze navíc extrahovat jako seznam.</p><p>Lze také sbírat textové hodnoty.</p> |
| Jedinečné hodnoty se shromažďují automaticky. | K extrahování seznamu jedinečných hodnot ze shromážděných hodnot je zapotřebí další nastavení. |
| Výkon závisí na objemu shromážděných hodnot. | V praxi výkon nezávisí na objemu shromážděných hodnot. |
| Tato technika funguje pro všechny typy odchozích dokumentů. | Tato technika funguje pouze pro textové a XML dokumenty. |

## <a name="additional-resources"></a>Další prostředky

- [Konfigurace formátu počítání a sčítání](./tasks/er-format-counting-summing-1.md)
- [Odložení provádění prvků posloupnosti ve formátech elektronického výkaznictví](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
