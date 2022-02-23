---
title: Obsah manažera školení v Power BI
description: Toto téma popisuje, co je součástí obsahu pro manažery školení v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 17a68e5aedb8b085c85d1ed7b6ad87f3eaecfc25
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685698"
---
# <a name="practice-manager-power-bi-content"></a>Obsah manažera školení v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **manažera školení** v Microsoft Power BI Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **manažer školení** v Power BI je určený pro manažery školení a projektové manažery. Poskytuje klíčové metriky, které se vztahují k projektům, na nichž organizace pracuje. Řídicí panel poskytuje přehled projektů a příslušných odběratelů. Filtr na úrovni sestavy slouží k vykazování pro určité právnické osoby. Tento obsah Power BI získává data z agregovaných měření účetnictví projektu.

Obsah **Manažer školení** v Power BI obsahuje pět stránek sestav: jednu stránku přehledu a čtyři stránky, které uvádějí podrobnosti o nákladech na projekt, výnosech, správě získané hodnoty a metrikách hodin, které jsou rozděleny mezi různé dimenze.

Všechny částky v obsahu jsou zobrazeny v měně systému. Systémovou měnu můžete nastavit na stránce **Parametry systému**.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Obsah **Manažer školení** v Power BI se zobrazí v pracovním prostoru **Správa projektu**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI

Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu **manažera školení** v Power BI.

| Stránka sestavy       | Metrika |
|-------------------|---------|
| Přehled projektů | <ul><li>Vytvořené projekty</li><li>Odhadované projekty</li><li>Probíhající projekty</li><li>Skutečný výnos podle odběratele</li><li>Rozpočet hrubé marže podle projektu</li><li>Přehled správy získané hodnoty</li></ul> |
| Náklady              | <ul><li>Skutečné vs. rozpočtované náklady podle měsíce</li><li>Skutečné vs. rozpočtované náklady podle roku</li><li>Skutečné vs. rozpočtované náklady podle kategorie</li><li>Skutečné náklady podle typu transakce</li></ul> |
| Výnosy           | <ul><li>Skutečný výnos podle měsíce</li><li>Skutečný výnos podle PSČ</li><li>Skutečný vs. rozpočtovaný výnos podle kategorie</li><li>Skutečný výnos podle odvětví zákazníka</li></ul> |
| EVM               | Stanovení nákladů a plánování indexu výkonnosti podle projektu |
| Pracovní doba             | <ul><li>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpočtu vs. hodiny rozpočtu</li><li>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpočtu podle projektu</li><li>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpočtu podle prostředku</li><li>Poměr skutečných fakturovatelných hodin podle projektu</li><li>Poměr skutečných fakturovatelných hodin podle prostředku</li></ul> |

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Můžete také použít základní funkci exportu dat pro export základních dat, jejichž souhrn je uveden ve vizualizaci.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Následující data se používají k naplnění stránek sestavy v obsahu **Manažer školení** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).

V následujících oddílech jsou popsána agregační měření, která se používají v každé entitě.

### <a name="entity-projectaccountingcube_actualhourutilization"></a>Entita: ProjectAccountingCube\_ActualHourUtilization
**Zdroj dat:** ProjEmplTrans

| Klíčové měření agregace      | Pole                              | popis |
|--------------------------------|------------------------------------|-------------|
| Skutečné fakturovatelné využité hodiny | Sum(ActualUtilizationBillableRate) | Součet skutečných fakturovatelných využitých hodin |
| Skutečné fakturovatelné hodiny režie   | Sum(ActualBurdenBillableRate)      | Součet skutečné míry režie |

### <a name="entity-projectaccountingcube_actuals"></a>Entita: ProjectAccountingCube\_Actuals
**Zdroj dat:** ProjTransPosting

| Klíčové měření agregace | Pole              | popis |
|---------------------------|--------------------|-------------|
| Skutečné výnosy            | Sum(ActualRevenue) | Součet zaúčtovaných výnosů pro všechny transakce. |
| Skutečné náklady               | Sum(ActualCost)    | Součet zaúčtovaných nákladů pro všechny typy transakcí. |

### <a name="entity-projectaccountingcube_customer"></a>Entita: ProjectAccountingCube\_Customer
**Zdroj dat:** CustTable

| Klíčové měření agregace | Pole                                             | popis |
|---------------------------|---------------------------------------------------|-------------|
| Počet projektů        | COUNTA(ProjectAccountingCube\_Projects\[PROJECTS\]) | Počet dostupných projektů. |

### <a name="entity-projectaccountingcube_forecasts"></a>Entita: ProjectAccountingCube\_Forecasts
**Zdroj dat:** ProjTransBudget

| Klíčové měření agregace | Pole                  | popis |
|---------------------------|------------------------|-------------|
| Rozpočtové náklady               | Sum(BudgetCost)        | Součet předpovídaných nákladů pro všechny typy transakcí. |
| Rozpočtové výnosy            | Sum(BudgetRevenue)     | Celkový počet časově rozlišených/fakturovaných výnosů podle prognózy. |
| Rozpočtová hrubá marže       | Sum(BudgetGrossMargin) | Rozdíl mezi součtem celkové prognózy výnosů a součtem celkových prognózovaných nákladů. |

### <a name="entity-projectaccountingcube_projectplancostsview"></a>Entita: ProjectAccountingCube\_ProjectPlanCostsView
**Zdroj dat:** Project

| Klíčové měření agregace | Pole                    | popis |
|---------------------------|--------------------------|-------------|
| Plánované náklady              | Sum(SumOfTotalCostPrice) | Celková nákladová cena v odhadech pro všechny typy transakcí projektu s plánovanými úlohami. |

### <a name="entity-projectaccountingcube_projects"></a>Entita: ProjectAccountingCube\_Projects
**Zdroj dat:** Project

| Klíčové měření agregace    | Pole | popis |
|------------------------------|-------|-------------|
| Index výkonnosti nákladů       | ProjectAccountingCube\_Projekty\[Získaná hodnota\] ÷ ProjectAccountingCube\_Projekty\[Celkové skutečné náklady dokončených úkolů\] | Výpočet celkové hodnoty vydělené celkovými skutečnými náklady. |
| Index plánu výkonnosti   | ProjectAccountingCube\_Projekty\[Získaná hodnota\] ÷ ProjectAccountingCube\_Projekty\[Celkové plánované náklady dokončených úkolů\] | Výpočet celkové hodnoty vydělené celkovými skutečnými plánovanými náklady. |
| Procento dokončené práce | Procento dokončené práce = ProjectAccountingCube\_Projekty\[Celkové skutečné náklady na dokončené úkoly\] ÷ (ProjectAccountingCube\_Projects\[Celkové skutečné náklady na dokončené úkoly\] + ProjectAccountingCube\_Projekty\[Celkové plánované náklady na projekt\] - ProjectAccountingCube\_Projekty\[Celkové plánované náklady na dokončené úkoly\]) | Celkové procento dokončené práce na základě celkových skutečných nákladů na dokončení úkolu a plánovaných nákladů projektu. |
| Skutečný poměr fakturovatelných hodin  | ProjectAccountingCube\_Projekty\[Celkové skutečné fakturovatelné využité hodiny projektu\] ÷ (ProjectAccountingCube\_Projekty\[Celkové skutečné fakturovatelné využité hodiny projektu\] + ProjectAccountingCube\_Projekty\[Celkové skutečné fakturovatelné hodiny režie\]) | Celkové skutečné fakturovatelné hodiny na základě využitých hodin a hodin režie. |
| Získaná hodnota                 | ProjectAccountingCube\_Projekty\[Celkové plánované náklady na projekt\] * ProjectAccountingCube\_Projekty\[Procento dokončené práce\] | Celkové plánované náklady vydělené procentem dokončené práce. |

### <a name="entity-projectaccountingcube_totalestimatedcosts"></a>Entita: ProjectAccountingCube\_TotalEstimatedCosts 
**Zdroj dat:** ProjTable

| Klíčové měření agregace       | Pole               | popis |
|---------------------------------|---------------------|-------------|
| Plánované náklady dokončené aktivity | Sum(TotalCostPrice) | Celková nákladová cena v odhadech pro všechny typy transakcí projektu s dokončenými úlohami. |
