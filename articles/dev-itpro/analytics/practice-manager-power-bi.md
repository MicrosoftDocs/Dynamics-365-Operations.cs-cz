---
title: "Obsah Power BI pro manažery školení"
description: "Toto téma popisuje, co je součástí obsahu pro manažery školení v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 836997f9f5b146ff48252c3f06153791ec1aabed
ms.contentlocale: cs-cz
ms.lasthandoff: 12/01/2017

---

# <a name="practice-manager-power-bi-content"></a>Obsah Power BI pro manažery školení

[!include[banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu pro **manažery školení** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které jsou použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah Power BI pro **manažery školení** je určený pro manažery školení a projektové manažery. Poskytuje klíčové metriky, které se vztahují k projektům, na nichž organizace pracuje. Řídicí panel poskytuje přehled projektů a příslušných odběratelů. Filtr na úrovni sestavy slouží k vykazování pro určité právnické osoby. Tento obsah Power BI získává data z agregovaných měření účetnictví projektu.

Obsah Power BI pro **Manažera školení** obsahuje pět stránek sestav: jednu stránku přehledu a čtyři stránky, které uvádějí podrobnosti o nákladech na projekt, výnosech, správě získané hodnoty a metrikách hodin, které jsou rozděleny mezi různé dimenze.

Všechny částky v obsahu jsou zobrazeny v měně systému. Systémovou měnu můžete nastavit na stránce **Parametry systému**.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah Power BI **Manažer školení** se zobrazí v pracovním prostoru **Manažer školení**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI

Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu Power BI **manažera školení**.

| Stránka sestavy       | Metrika |
|-------------------|---------|
| Přehled projektů | <ul><li>Vytvořené projekty</li><li>Odhadované projekty</li><li>Probíhající projekty</li><li>Počet projektů podle fáze</li><li>Počet projektů podle města</li><li>Skutečný výnos podle odběratele</li><li>Rozpočet hrubé marže podle projektu</li><li>Přehled správy získané hodnoty</li></ul> |
| Náklady              | <ul><li>Skutečné vs. rozpočtované náklady podle měsíce</li><li>Skutečné vs. rozpočtované náklady podle roku</li><li>Skutečné vs. rozpočtované náklady podle kategorie</li><li>Skutečné náklady podle typu transakce</li></ul> |
| Výnosy           | <ul><li>Skutečný výnos podle měsíce</li><li>Skutečný výnos podle PSČ</li><li>Skutečný vs. rozpočtovaný výnos podle kategorie</li><li>Skutečný výnos podle odvětví zákazníka</li></ul> |
| EVM               | Stanovení nákladů a plánování indexu výkonnosti podle projektu |
| Pracovní doba             | <ul><li>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpočtu vs. hodiny rozpočtu</li><li>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpočtu podle projektu</li><li>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpočtu podle prostředku</li><li>Poměr skutečných fakturovatelných hodin podle projektu</li><li>Poměr skutečných fakturovatelných hodin podle prostředku</li></ul> |

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Můžete také použít základní funkci exportu dat pro export základních dat, jejichž souhrn je uveden ve vizualizaci.

## <a name="extending-the-power-bi-content"></a>Rozšíření obsahu v Power BI
Pomocí balíčků obsahu, které jsou k dispozici ve službě Microsoft Dynamics Lifecycle Services (LCS) můžete poskytovat skvělou analýzu osobám, které nejsou přihlášeny k aplikaci Microsoft Dynamics 365. Tyto balíčky obsahu můžete upravit tak, aby zahrnovaly jiné sestavy nebo vizuály, a potom je publikovat na svého klienta Power BI.com pro analýzu. 

Obsah **Manažer školení** v Power BI najdete v knihovně sdíleného majetku ve službě LCS. Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

Nezapomeňte si stáhnout obsah **Manažer školení**, který se vztahuje k vámi používané verzi aplikace Dynamics 365.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Následující data se používají k naplnění stránek sestavy v obsahu **Manažer školení** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Přehled integrace Power BI úložištěm entit](power-bi-integration-entity-store.md).

V následujících oddílech jsou popsána agregační měření, která se používají v každé entitě.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Entita: ProjectAccountingCube_ActualHourUtilization
**Zdroj dat:** ProjEmplTrans

| Klíčové měření agregace      | Pole                              | popis | 
|--------------------------------|------------------------------------|-------------|
| Skutečné fakturovatelné využité hodiny | Sum(ActualUtilizationBillableRate) | Součet skutečných fakturovatelných využitých hodin |
| Skutečné fakturovatelné hodiny režie   | Sum(ActualBurdenBillableRate)      | Součet skutečné míry režie |

### <a name="entity-projectaccountingcubeactuals"></a>Entita: ProjectAccountingCube_Actuals
**Zdroj dat:** ProjTransPosting

| Klíčové měření agregace | Pole              | popis | 
|---------------------------|--------------------|-------------|
| Skutečné výnosy            | Sum(ActualRevenue) | Součet zaúčtovaných výnosů pro všechny transakce. |   
| Skutečné náklady               | Sum(ActualCost)    | Součet zaúčtovaných nákladů pro všechny typy transakcí. |

### <a name="entity-projectaccountingcubecustomer"></a>Entita: ProjectAccountingCube_Customer
**Zdroj dat:** CustTable

| Klíčové měření agregace | Pole                                            | popis | 
|---------------------------|--------------------------------------------------|-------------|
| Počet projektů        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Počet dostupných projektů. |


### <a name="entity-projectaccountingcubeforecasts"></a>Entita: ProjectAccountingCube_Forecasts
**Zdroj dat:** ProjTransBudget

| Klíčové měření agregace | Pole                  | popis | 
|---------------------------|------------------------|-------------|
| Rozpočtové náklady               | Sum(BudgetCost)        | Součet předpovídaných nákladů pro všechny typy transakcí. |
| Rozpočtové výnosy            | Sum(BudgetRevenue)     | Celkový počet časově rozlišených/fakturovaných výnosů podle prognózy.  |
| Rozpočtová hrubá marže       | Sum(BudgetGrossMargin) | Rozdíl mezi součtem celkové prognózy výnosů a součtem celkových prognózovaných nákladů. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Entita: ProjectAccountingCube_ProjectPlanCostsView
**Zdroj dat:** Project

| Klíčové měření agregace | Pole                    | popis | 
|---------------------------|--------------------------|-------------|
| Plánované náklady              | Sum(SumOfTotalCostPrice) | Celková nákladová cena v odhadech pro všechny typy transakcí projektu s plánovanými úlohami. |

### <a name="entity-projectaccountingcubeprojects"></a>Entita: ProjectAccountingCube_Projects
**Zdroj dat:** Project

| Klíčové měření agregace    | Pole | popis | 
|------------------------------|-------|-------------|
| Index výkonnosti nákladů       | ProjectAccountingCube_Projects[Získaná hodnota] / ProjectAccountingCube_Projects[Celkové skutečné náklady dokončených úkolů] | Výpočet celkové hodnoty vydělené celkovými skutečnými náklady. |
| Index plánu výkonnosti   | ProjectAccountingCube_Projects[získaná hodnota] / ProjectAccountingCube_Projects[Celkové plánované náklady dokončených úkolů] | Výpočet celkové hodnoty vydělené celkovými skutečnými plánovanými náklady. |
| Procento dokončené práce | Procento dokončené práce = ProjectAccountingCube_Projects[Celkové skutečné náklady na dokončené úkoly] / (ProjectAccountingCube_Projects[Celkové skutečné náklady na dokončené úkoly] + ProjectAccountingCube_Projects[Celkové plánované náklady na projekt] - ProjectAccountingCube_Projects[Celkové plánované náklady na dokončené úkoly]) | Celkové procento dokončené práce na základě celkových skutečných nákladů na dokončení úkolu a plánovaných nákladů projektu. |
| Skutečný poměr fakturovatelných hodin  | ProjectAccountingCube_Projects[Celkové skutečné fakturovatelné využité hodiny projektu] / (ProjectAccountingCube_Projects[Celkové skutečné fakturovatelné využité hodiny projektu] + ProjectAccountingCube_Projects[Celkové skutečné fakturovatelné hodiny režie]) | Celkové skutečné fakturovatelné hodiny na základě využitých hodin a hodin režie. |
| Získaná hodnota                 | ProjectAccountingCube_Projects[Celkové plánované náklady na projekt] * ProjectAccountingCube_Projects[Procento dokončené práce] | Celkové plánované náklady vydělené procentem dokončené práce. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Entita: ProjectAccountingCube_TotalEstimatedCosts 
**Zdroj dat:** ProjTable

| Klíčové měření agregace       | Pole               | popis | 
|---------------------------------|---------------------|-------------|
| Plánované náklady dokončené aktivity | Sum(TotalCostPrice) | Celková nákladová cena v odhadech pro všechny typy transakcí projektu s dokončenými úlohami. |

