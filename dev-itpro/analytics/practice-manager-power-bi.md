---
title: "Obsah Power BI pro manažery školení"
description: "Toto téma popisuje, co je součástí obsahu pro manažery školení v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Obsah Power BI pro manažery školení

[!include[banner](../includes/banner.md)]


Toto téma popisuje, co je součástí obsahu pro **manažery školení** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které jsou použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah Power BI pro **manažery školení** je určený pro manažery školení a projektové manažery. Poskytuje klíčové metriky, které se vztahují k projektům, na nichž organizace pracuje. Řídicí panel poskytuje přehled projektů a příslušných odběratelů. Filtr na úrovni sestavy slouží k vykazování pro určité právnické osoby. Tento obsah spotřeby BI získává data z agregovaných měření účetnictví projektu pro aplikaci Microsoft Dynamics 365 for Operations.

Obsah Power BI pro **manažera školení** obsahuje pět stránek sestav: jednu stránku přehledu a čtyři stránky, které uvádějí podrobnosti o nákladech na projekt, výnosech, správě získané hodnoty a metriky hodin, které jsou rozděleny mezi různé dimenze.

Všechny částky v obsahu jsou zobrazeny v měně systému. Systémovou měnu můžete nastavit na stránce **Parametry systému**.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Obsah **Manažera školení** v Power BI naleznete v knihovně sdíleného majetku ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení balíčku obsahu a připojení k datům aplikace Dynamics 365 for Operations naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md).

Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI

Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu Power BI **manažera školení**.

| Stránka sestavy                                          | Metrika               |
|------------------------------------------------------|-----------------------------------------------|
| Řídicí panel  | Vytvořené projekty<br>Odhadované projekty<br>Probíhající projekty<br>Počet projektů podle fáze<br>Počet projektů podle města<br>Skutečný výnos podle odběratele<br>Rozpočet hrubé marže podle projektu<br>Přehled správy získané hodnoty |
| Náklady                                                 | Skutečné vs. rozpočtované náklady podle měsíce<br>Skutečné vs. rozpočtované náklady podle roku<br>Skutečné vs. rozpočtované náklady podle kategorie<br>Skutečné náklady podle typu transakce       |
| Výnosy                                              | Skutečný výnos podle měsíce<br>Skutečný výnos podle PSČ<br>Skutečný vs. rozpočtovaný výnos podle kategorie<br>Skutečný výnos podle odvětví zákazníka        |
| EVM                                                  | Stanovení nákladů a plánování indexu výkonnosti podle projektu                 |
| Pracovní doba                                                | Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpoču vs. hodiny rozpočtu<br>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpoču podle projektu<br>Skutečné fakturovatelné využité hodiny vs. skutečné fakturovatelné hodiny rozpoču podle prostředku<br>Poměr skutečných fakturovatelných hodin podle projektu<br>Poměr skutečných fakturovatelných hodin podle prostředku |

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Můžete také použít základní funkci exportu dat pro export základních dat, jejichž souhrn je uveden ve vizualizaci.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Data aplikace Dynamics 365 for Operations se používají k naplnění stránek sestavy v obsahu **manažera školení** v Power BI. Tato data jsou reprezentována jako měrné systémy agregace, které jsou rozfázovány v úložišti entit, což je databáze Microsoft SQL optimalizována pro analýzy. Další informace naleznete v tématu [Přehled integrace Power BI úložištěm entit](power-bi-integration-entity-store.md).

V následujících oddílech jsou vysvětlena agregační měření, která se používají v každé entitě.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Entita: ProjectAccountingCube_ActualHourUtilization
**Zdroj dat**: ProjEmplTrans

| Klíčové měření agregace                | Pole                                | popis                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Souhrn skutečných fakturovatelných využitých hodin |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Souhrn skutečné míry režie             |

### <a name="entity-projectaccountingcubeactuals"></a>Entita: ProjectAccountingCube_Actuals
**Zdroj dat**: ProjTransPosting

| Klíčové měření agregace                | Pole                                | popis                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Součet zaúčtovaných výnosů pro všechny transakce |   
| ActualCost   |                             Sum(ActualCost)           |    Součet zaúčtovaných nákladů pro všechny typy transakcí    |

### <a name="entity-projectaccountingcubecustomer"></a>Entita: ProjectAccountingCube_Customer
**Zdroj dat**: CustTable

| Klíčové měření agregace                | Pole                                | popis                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Počet projektů        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Počet dostupných projektů    |


### <a name="entity-projectaccountingcubeforecasts"></a>Entita: ProjectAccountingCube_Forecasts
**Zdroj dat**: ProjTransBudget

| Klíčové měření agregace                | Pole                                | popis                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Celkem předpovídaných nákladů pro všechny typy transakcí     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Celkový počet časově rozlišených/fakturovaných výnosů podle prognózy         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Rozdíl mezi součtem celkové prognózy výnosů a součtem celkových prognózovaných nákladů

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Entita: ProjectAccountingCube_ProjectPlanCostsView
**Zdroj dat**: Projekt

| Klíčové měření agregace                | Pole                                | popis                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Celková nákladová cena v odhadech pro všechny typy transakcí projektu s plánovanými úlohami |

### <a name="entity-projectaccountingcubeprojects"></a>Entita: ProjectAccountingCube_Projects
**Zdroj dat**: Projekt

| Klíčové měření agregace                | Pole                                | popis                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Index výkonnosti nákladů  |ProjectAccountingCube_Projects[Získaná hodnota] / ProjectAccountingCube_Projects[Celkové skutečné náklady dokončených úkolů] |     Výpočet celkové hodnoty vydělené celkovými skutečnými náklady|
|  Index plánu výkonnosti |ProjectAccountingCube_Projects[získaná hodnota] / ProjectAccountingCube_Projects[Celkové plánované náklady dokončených úkolů]|Výpočet celkové hodnoty vydělené celkovými plánovanými náklady |
|Procento dokončené práce |Procento dokončené práce = ProjectAccountingCube_Projects[Celkové skutečné náklady na dokončené úkoly] / (ProjectAccountingCube_Projects[Celkové skutečné náklady na dokončené úkoly] + ProjectAccountingCube_Projects[Celkové plánované náklady na projekt] - ProjectAccountingCube_Projects[Celkové plánované náklady na dokončené úkoly])|Celkové procento dokončené práce na základě celkových skutečných nákladů na dokončení úkolu a plánovaných nákladů projektu|
|Poměr skutečných fakturovatelných hodin projektu|ProjectAccountingCube_Projects[Celkové skutečné fakturovatelné využité hodiny projektu] / (ProjectAccountingCube_Projects[Celkové skutečné fakturovatelné využité hodiny projektu] + ProjectAccountingCube_Projects[Celkové skutečné fakturovatelné hodiny režie])|Celkové skutečné fakturovatelných hodin na základě využití + režie|
|Získaná hodnota|ProjectAccountingCube_Projects[Celkové plánované náklady na projekt] * ProjectAccountingCube_Projects[Procento dokončené práce]|Celkové plánované náklady vynásobené procentem dokončené práce|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Entita: ProjectAccountingCube_TotalEstimatedCosts 
**Zdroj dat**: ProjTable

| Klíčové měření agregace                | Pole                                | popis                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Celková nákladová cena v odhadech pro všechny typy transakcí projektu s dokončenými úlohami|

## <a name="additional-resources"></a>Další zdroje

Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

- [Datové entity](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Konfigurace integrace služby Power BI pro pracovní prostory](configure-power-bi-integration.md)

