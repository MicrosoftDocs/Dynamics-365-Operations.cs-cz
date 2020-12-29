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
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7052aeb4154cefe30a1935dfdca53085a035deb6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687604"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="d651f-103">Vytvoření pravidel pro poradce při optimalizaci</span><span class="sxs-lookup"><span data-stu-id="d651f-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d651f-104">Toto téma vysvětluje postup vytvoření nových pravidel pro **Poradce při optimalizaci**.</span><span class="sxs-lookup"><span data-stu-id="d651f-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="d651f-105">Můžete například vytvořit nové pravidlo, které identifikuje, jaké případy požadavků na nabídku mají prázdný název.</span><span class="sxs-lookup"><span data-stu-id="d651f-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="d651f-106">Použití názvů u případů je činí snadno identifikovatelné a vyhledávatelné.</span><span class="sxs-lookup"><span data-stu-id="d651f-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="d651f-107">I když je to docela snadncě, tento příklad ukazuje, čeho lze s pravidly optimalizace dosáhnout.</span><span class="sxs-lookup"><span data-stu-id="d651f-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="d651f-108">*Pravidlo* je kontrola na datech aplikace.</span><span class="sxs-lookup"><span data-stu-id="d651f-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="d651f-109">Pokud je splněna podmínka, kterou pravidlo vyhodnocuje, vytvoří se příležitosti k optimalizaci procesů nebo vylepšení dat.</span><span class="sxs-lookup"><span data-stu-id="d651f-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="d651f-110">Na příležitosti lze reagovat a v případě potřeby můžete měřit dopad akce.</span><span class="sxs-lookup"><span data-stu-id="d651f-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="d651f-111">Chcete-li vytvořit nové pravidlo pro **Poradce při optimalizaci**, přidejte novou třídu, která rozšiřuje abstraktní třídy **SelfHealingRule**, implementuje rozhraní **IDiagnosticsRule** a bude vyplněna atributem **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="d651f-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="d651f-112">Třída musí mít také metodu vyplněnou atributem **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d651f-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="d651f-113">To se děje na metodě **opportunityTitle**, která bude diskutována dále.</span><span class="sxs-lookup"><span data-stu-id="d651f-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="d651f-114">Tuto novou třídu lze přidat do vlastního modelu se závislostí na modelu **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="d651f-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="d651f-115">V následujícím příkladu se implementované pravidlo nazývá **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="d651f-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="d651f-116">Abstraktní třída **SelfHealingRule** má abstraktní metody, které musí být implementovány ve zděděných třídách.</span><span class="sxs-lookup"><span data-stu-id="d651f-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="d651f-117">Základem je metoda **evaluate**, která vrací seznam příležitostí identifikovaných pravidlem.</span><span class="sxs-lookup"><span data-stu-id="d651f-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="d651f-118">Příležitosti mohou být podle právnické osoby nebo je lze použít na celý systém.</span><span class="sxs-lookup"><span data-stu-id="d651f-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```xpp
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

<span data-ttu-id="d651f-119">Metoda zobrazená výše provádí smyčky nad společnostmi a vybere případy požadavku na nabídku s prázdné názvy v metodě **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="d651f-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="d651f-120">Pokud je nalezen nejméně jeden takový případ, vytvoří se příležitost specifická pro firmu s metodou **getOpportunityForCompany**.</span><span class="sxs-lookup"><span data-stu-id="d651f-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="d651f-121">Všimněte si, že pole **Data** v tabulce **SelfHealingOpportunity** je typu **Kontejner**, a proto může obsahovat jakákoli data relevantní pro logiku specifickou pro toto pravidlo.</span><span class="sxs-lookup"><span data-stu-id="d651f-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="d651f-122">Nastavení **OpportunityDate** s aktuálním časovým razítkem registruje čas posledního vyhodnocení příležitosti.</span><span class="sxs-lookup"><span data-stu-id="d651f-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="d651f-123">Příležitosti mohou být také mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="d651f-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="d651f-124">V takovém případě smyčka nad společnostmi není potřebná a je potřeba vytvořit příležitost s metodou **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="d651f-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="d651f-125">Následující kód zobrazí metodu **findRFQCasesWithEmptyTitle**, která vrátí ID případů požadavku na nabídku, které mají prázdné názvy.</span><span class="sxs-lookup"><span data-stu-id="d651f-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```xpp
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

<span data-ttu-id="d651f-126">Dvě další metody, které musí být implementovány, jsou **opportunityTitle** a **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="d651f-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="d651f-127">První vrátí stručný název pro příležitost, druhá vrátí podrobný popis příležitosti, která může také zahrnovat data.</span><span class="sxs-lookup"><span data-stu-id="d651f-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="d651f-128">Název vrácený metodou **opportunityTitle** se zobrazí pod sloupcem **Příležitost optimalizace** v pracovním prostoru **Poradce při optimalizaci**.</span><span class="sxs-lookup"><span data-stu-id="d651f-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="d651f-129">Zobrazí se také jako záhlaví postranního podokna s více informacemi o příležitosti.</span><span class="sxs-lookup"><span data-stu-id="d651f-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="d651f-130">Tato metoda je vyplněna atributem **DiagnosticRuleSubscription**, který má následující argumenty:</span><span class="sxs-lookup"><span data-stu-id="d651f-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="d651f-131">**Diagnostická oblast** – Výčet typu **DiagnosticArea**, který popisuje, k jaké oblasti aplikace pravidlo patří, jako je například **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="d651f-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="d651f-132">**Název pravidla** – Řetězec s názvem pravidla.</span><span class="sxs-lookup"><span data-stu-id="d651f-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="d651f-133">Zobrazí se pod sloupcem **Název pravidla** ve formuláři **Pravidlo ověření diagnostiky** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="d651f-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="d651f-134">**Spustit frekvenci** – Výčet typu **DiagnosticRunFrequency**, který popisuje, jak často má být pravidlo spuštěno, jako je například **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="d651f-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="d651f-135">**Popis pravidla** – Řetězec s podrobnějším popisem pravidla.</span><span class="sxs-lookup"><span data-stu-id="d651f-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="d651f-136">Zobrazí se pod sloupcem **Popis pravidla** ve formuláři **Pravidlo ověření diagnostiky** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="d651f-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="d651f-137">Atribut **DiagnosticRuleSubscription** je požadován, aby toto pravidlo fungovalo.</span><span class="sxs-lookup"><span data-stu-id="d651f-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="d651f-138">Obvykle se používá v **opportunityTitle**, ale může vyplnit jakoukoli metodu třídy.</span><span class="sxs-lookup"><span data-stu-id="d651f-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="d651f-139">Následuje příklad implementace.</span><span class="sxs-lookup"><span data-stu-id="d651f-139">The following is an example implementation.</span></span> <span data-ttu-id="d651f-140">Neupravené řetězce se používají pro zjednodušení, ale správná implementace vyžaduje popisky.</span><span class="sxs-lookup"><span data-stu-id="d651f-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="d651f-141">Popis vrácený **opportunityDetails** se zobrazí na postranním podokně zobrazující další informace o příležitosti.</span><span class="sxs-lookup"><span data-stu-id="d651f-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="d651f-142">Vezme argument **SelfHealingOpportunity**, kterým je pole **Data**, které lze použít k poskytnutí více podrobností o příležitosti.</span><span class="sxs-lookup"><span data-stu-id="d651f-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="d651f-143">V tomto příkladu metoda vrátí ID případy požadavku na nabídku s prázdným názvem.</span><span class="sxs-lookup"><span data-stu-id="d651f-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```xpp
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

<span data-ttu-id="d651f-144">Dvě zbývající abstraktní metody k implementaci jsou **provideHealingAction** a **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="d651f-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="d651f-145">**provideHealingAction** vrací hodnotu true, pokud je poskytnuta opravná akce, vrátí false.</span><span class="sxs-lookup"><span data-stu-id="d651f-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="d651f-146">Pokud je vrácena hodnota true, metoda **performAction** musí být implementována, nebo dojde ke zobrazení chyby.</span><span class="sxs-lookup"><span data-stu-id="d651f-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="d651f-147">Metoda **PerformAction** vezme argument **SelfHealingOpportunity**, ve které lze použít data pro danou akci.</span><span class="sxs-lookup"><span data-stu-id="d651f-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="d651f-148">V tomto příkladu akce otevře **PurchRFQCaseTableListPage** pro ruční opravu.</span><span class="sxs-lookup"><span data-stu-id="d651f-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="d651f-149">V závislosti na specifikách pravidla, je možné provést automatickou akci pomocí dat příležitosti.</span><span class="sxs-lookup"><span data-stu-id="d651f-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="d651f-150">V tomto příkladu by systém mohl vygenerovat názvy pro případy požadavku na nabídku automaticky.</span><span class="sxs-lookup"><span data-stu-id="d651f-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="d651f-151">**securityMenuItem** vrátí název položky nabídky akcí tak, aby pravidlo bylo viditelné pro uživatele, kteří mají přístup k položce nabídky akcí.</span><span class="sxs-lookup"><span data-stu-id="d651f-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="d651f-152">Zabezpečení může vyžadovat, aby konkrétní pravidla a příležitosti byly přístupné pouze pro oprávněné uživatele.</span><span class="sxs-lookup"><span data-stu-id="d651f-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="d651f-153">V tomto příkladu pouze uživatelé s přístupem **PurchRFQCaseTitleAction** mohou zobrazit příležitost.</span><span class="sxs-lookup"><span data-stu-id="d651f-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="d651f-154">Všimněte si, že tato položka nabídky akcí byla vytvořena pro tento příklad a byla přidána jako vstupní bod pro oprávnění zabezpečení **PurchRFQCaseTableMaintain**.</span><span class="sxs-lookup"><span data-stu-id="d651f-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="d651f-155">Položka nabídky musí být položka nabídky akcí, aby zabezpečení pracovalo správně.</span><span class="sxs-lookup"><span data-stu-id="d651f-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="d651f-156">Ostatní typy položky nabídky, jako například **Položky nabídky zobrazení**, nebudou fungovat správně.</span><span class="sxs-lookup"><span data-stu-id="d651f-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="d651f-157">Po kompilaci pravidla spusťte následující úlohu, aby se zobrazilo v uživatelském rozhraní.</span><span class="sxs-lookup"><span data-stu-id="d651f-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```xpp
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

<span data-ttu-id="d651f-158">Pravidlo se zobrazí ve formuláři **Pravidlo ověření diagnostiky**, dostupné z **Správa systému** > **Periodické úlohy** > **Udržovat pravidlo ověření diagnostiky**.</span><span class="sxs-lookup"><span data-stu-id="d651f-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="d651f-159">Pokud ho chcete mít vyhodnocené, přejděte na **Správa systému** > **Periodické úlohy** > **Naplánovat pravidlo ověření diagnostiky**, vyberte četnost pravidla, jako je například **Denně**.</span><span class="sxs-lookup"><span data-stu-id="d651f-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="d651f-160">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d651f-160">Click **OK**.</span></span> <span data-ttu-id="d651f-161">Přejděte na **Správa systému** > **Poradce při optimalizaci** pro zobrazení nové příležitosti.</span><span class="sxs-lookup"><span data-stu-id="d651f-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="d651f-162">V následujícím příkladu je fragment kódu s kostrou pravidla, včetně všech požadovaných metod a atributů.</span><span class="sxs-lookup"><span data-stu-id="d651f-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="d651f-163">Pomůže vám to při zahájení psaní nových pravidel.</span><span class="sxs-lookup"><span data-stu-id="d651f-163">It helps you get started with writing new rules.</span></span> <span data-ttu-id="d651f-164">Popisky a položky nabídky akcí, které se používají v uvedeném příkladu, slouží pouze pro demonstrační účel.</span><span class="sxs-lookup"><span data-stu-id="d651f-164">The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```xpp
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

<span data-ttu-id="d651f-165">Další informace naleznete v krátkém videu YouTube: [Poradce při optimalizaci v Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="d651f-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
