---
title: Vytvoření pravidel pro poradce při optimalizaci
description: Toto téma popisuje postup přidání nových pravidel do poradce při optimalizaci.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: ca73120a5a0da4dc348c2d16dca8e7654876af5d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "354154"
---
# <a name="create-rules-for-optimization-advisor"></a>Vytvoření pravidel pro poradce při optimalizaci

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje postup vytvoření nových pravidel pro **Poradce při optimalizaci**. Můžete například vytvořit nové pravidlo, které identifikuje, jaké případy požadavků na nabídku mají prázdný název. Použití názvů u případů je činí snadno identifikovatelné a vyhledávatelné. I když je to docela snadncě, tento příklad ukazuje, čeho lze s pravidly optimalizace dosáhnout. 

*Pravidlo* je kontrola na datech aplikace. Pokud je splněna podmínka, kterou pravidlo vyhodnocuje, vytvoří se příležitosti k optimalizaci procesů nebo vylepšení dat. Na příležitosti lze reagovat a v případě potřeby můžete měřit dopad akce. 

Chcete-li vytvořit nové pravidlo pro **Poradce při optimalizaci**, přidejte novou třídu, která rozšiřuje abstraktní třídy **SelfHealingRule**, implementuje rozhraní **IDiagnosticsRule** a bude vyplněna atributem **DiagnosticRule**. Třída musí mít také metodu vyplněnou atributem **DiagnosticsRuleSubscription**. To se děje na metodě **opportunityTitle**, která bude diskutována dále. Tuto novou třídu lze přidat do vlastního modelu se závislostí na modelu **SelfHealingRules**. V následujícím příkladu se implementované pravidlo nazývá **RFQTitleSelfHealingRule**.

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

Abstraktní třída **SelfHealingRule** má abstraktní metody, které musí být implementovány ve zděděných třídách. Základem je metoda **evaluate**, která vrací seznam příležitostí identifikovaných pravidlem. Příležitosti mohou být podle právnické osoby nebo je lze použít na celý systém.

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

Metoda zobrazená výše provádí smyčky nad společnostmi a vybere případy požadavku na nabídku s prázdné názvy v metodě **findRFQCasesWithEmptyTitle**. Pokud je nalezen nejméně jeden takový případ, vytvoří se příležitost specifická pro firmu s metodou **getOpportunityForCompany**. Všimněte si, že pole **Data** v tabulce **SelfHealingOpportunity** je typu **Kontejner**, a proto může obsahovat jakákoli data relevantní pro logiku specifickou pro toto pravidlo. Nastavení **OpportunityDate** s aktuálním časovým razítkem registruje čas posledního vyhodnocení příležitosti.  

Příležitosti mohou být také mezi společnostmi. V takovém případě smyčka nad společnostmi není potřebná a je potřeba vytvořit příležitost s metodou **getOpportunityAcrossCompanies**. 

Následující kód zobrazí metodu **findRFQCasesWithEmptyTitle**, která vrátí ID případů požadavku na nabídku, které mají prázdné názvy.

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

Dvě další metody, které musí být implementovány, jsou **opportunityTitle** a **opportunityDetails**. První vrátí stručný název pro příležitost, druhá vrátí podrobný popis příležitosti, která může také zahrnovat data.

Název vrácený metodou **opportunityTitle** se zobrazí pod sloupcem **Příležitost optimalizace** v pracovním prostoru **Poradce při optimalizaci**. Zobrazí se také jako záhlaví postranního podokna s více informacemi o příležitosti. Tato metoda je vyplněna atributem **DiagnosticRuleSubscription**, který má následující argumenty: 

* **Diagnostická oblast** – Výčet typu **DiagnosticArea**, který popisuje, k jaké oblasti aplikace pravidlo patří, jako je například **DiagnosticArea::SCM**. 

* **Název pravidla** – Řetězec s názvem pravidla. Zobrazí se pod sloupcem **Název pravidla** ve formuláři **Pravidlo ověření diagnostiky** (**DiagnosticsValidationRuleMaintain**). 

* **Spustit frekvenci** – Výčet typu **DiagnosticRunFrequency**, který popisuje, jak často má být pravidlo spuštěno, jako je například **DiagnosticRunFrequency::Daily**. 

* **Popis pravidla** – Řetězec s podrobnějším popisem pravidla. Zobrazí se pod sloupcem **Popis pravidla** ve formuláři **Pravidlo ověření diagnostiky** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Atribut **DiagnosticRuleSubscription** je požadován, aby toto pravidlo fungovalo. Obvykle se používá v **opportunityTitle**, ale může vyplnit jakoukoli metodu třídy.

Následuje příklad implementace. Neupravené řetězce se používají pro zjednodušení, ale správná implementace vyžaduje popisky. 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

Popis vrácený **opportunityDetails** se zobrazí na postranním podokně zobrazující další informace o příležitosti. Vezme argument **SelfHealingOpportunity**, kterým je pole **Data**, které lze použít k poskytnutí více podrobností o příležitosti. V tomto příkladu metoda vrátí ID případy požadavku na nabídku s prázdným názvem. 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

Dvě zbývající abstraktní metody k implementaci jsou **provideHealingAction** a **securityMenuItem**. 

**provideHealingAction** vrací hodnotu true, pokud je poskytnuta opravná akce, vrátí false. Pokud je vrácena hodnota true, metoda **performAction** musí být implementována, nebo dojde ke zobrazení chyby. Metoda **PerformAction** vezme argument **SelfHealingOpportunity**, ve které lze použít data pro danou akci. V tomto příkladu akce otevře **PurchRFQCaseTableListPage** pro ruční opravu. 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

V závislosti na specifikách pravidla, je možné provést automatickou akci pomocí dat příležitosti. V tomto příkladu by systém mohl vygenerovat názvy pro případy požadavku na nabídku automaticky. 

**securityMenuItem** vrátí název položky nabídky akcí tak, aby pravidlo bylo viditelné pro uživatele, kteří mají přístup k položce nabídky akcí. Zabezpečení může vyžadovat, aby konkrétní pravidla a příležitosti byly přístupné pouze pro oprávněné uživatele. V tomto příkladu pouze uživatelé s přístupem **PurchRFQCaseTitleAction** mohou zobrazit příležitost. Všimněte si, že tato položka nabídky akcí byla vytvořena pro tento příklad a byla přidána jako vstupní bod pro oprávnění zabezpečení **PurchRFQCaseTableMaintain**. 

> [!NOTE]
> Položka nabídky musí být položka nabídky akcí, aby zabezpečení pracovalo správně. Ostatní typy položky nabídky, jako například **Položky nabídky zobrazení**, nebudou fungovat správně.

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Po kompilaci pravidla spusťte následující úlohu, aby se zobrazilo v uživatelském rozhraní.

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

Pravidlo se zobrazí ve formuláři **Pravidlo ověření diagnostiky**, dostupné z **Správa systému** > **Periodické úlohy** > **Udržovat pravidlo ověření diagnostiky**. Pokud ho chcete mít vyhodnocené, přejděte na **Správa systému** > **Periodické úlohy** > **Naplánovat pravidlo ověření diagnostiky**, vyberte četnost pravidla, jako je například **Denně**. Klikněte na tlačítko **OK**. Přejděte na **Správa systému** > **Poradce při optimalizaci** pro zobrazení nové příležitosti. 

V následujícím příkladu je fragment kódu s kostrou pravidla, včetně všech požadovaných metod a atributů. Pomůže vám to při zahájení psaní nových pravidel. Popisky a položky nabídky akcí, které se používají v uvedeném příkladu, slouží pouze pro demonstrační účel.

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

Další informace naleznete v krátkém videu YouTube: [Poradce při optimalizaci v Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
