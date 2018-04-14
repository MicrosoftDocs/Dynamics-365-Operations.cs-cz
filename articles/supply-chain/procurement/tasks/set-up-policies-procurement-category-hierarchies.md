--- 
title: "Nastavení zásad pro hierarchie kategorií zásobování"
description: "Tento postup použijte k nastavení pravidel pro objednávání produktů v kategorii."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a773675b858a196e795ad54cc534ef5eb98ef484
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="8f481-103">Nastavení zásad pro hierarchie kategorií zásobování</span><span class="sxs-lookup"><span data-stu-id="8f481-103">Set up policies for procurement category hierarchies</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f481-104">Tento postup použijte k nastavení pravidel pro objednávání produktů v kategorii.</span><span class="sxs-lookup"><span data-stu-id="8f481-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="8f481-105">Pravidla jsou definována pro určitou zásadu nákupu.</span><span class="sxs-lookup"><span data-stu-id="8f481-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="8f481-106">Pravidlo zásad přístupu ke kategorii určuje, ke kterým kategoriím zásobování mají uživatelé přístup při vytváření žádanky.</span><span class="sxs-lookup"><span data-stu-id="8f481-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="8f481-107">Při vytvoření žádanky jsou zásada nákupu a pravidla přístupu ke kategoriím určená k použití určena na základě právního subjektu a provozní jednotky, do které zaměstnanec patří.</span><span class="sxs-lookup"><span data-stu-id="8f481-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="8f481-108">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="8f481-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="8f481-109">Tento úkol obvykle provádí manažer nákupu.</span><span class="sxs-lookup"><span data-stu-id="8f481-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="8f481-110">Vyhledejte zásady zásobování</span><span class="sxs-lookup"><span data-stu-id="8f481-110">Find the procurement policy</span></span>
1. <span data-ttu-id="8f481-111">Přejděte na Zásobování a zdroje > Nastavení > Zásady > Zásady nákupu.</span><span class="sxs-lookup"><span data-stu-id="8f481-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="8f481-112">Klepněte na odkaz u USMF – zásady zásobování.</span><span class="sxs-lookup"><span data-stu-id="8f481-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="8f481-113">Toto je zásada, ke které přidáte pravidlo.</span><span class="sxs-lookup"><span data-stu-id="8f481-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="8f481-114">Musí být aktivní zásadou.</span><span class="sxs-lookup"><span data-stu-id="8f481-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="8f481-115">Vytvořit pravidlo přístupu ke kategorii</span><span class="sxs-lookup"><span data-stu-id="8f481-115">Create a category access rule</span></span>
1. <span data-ttu-id="8f481-116">Vyberte pravidlo zásad přístupu ke kategorii.</span><span class="sxs-lookup"><span data-stu-id="8f481-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="8f481-117">Pokud je tlačítko Vytvořit pravidlo zobrazeno šedě, je to proto, že již existuje aktivní pravidlo zásad pro přístup ke kategorii.</span><span class="sxs-lookup"><span data-stu-id="8f481-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="8f481-118">Zkontrolujte pole Účinné datum a Datum vypršení platnosti, určete, které z nich to je, vyberte je a klepněte na tlačítko Vyřadit pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="8f481-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="8f481-119">Pokud je tlačítko Vytvořit pravidlo zásad k dispozici, nemusíte provádět žádné změny.</span><span class="sxs-lookup"><span data-stu-id="8f481-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="8f481-120">Klikněte na Vytvořit pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="8f481-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="8f481-121">Do pole Datum platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="8f481-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="8f481-122">Čas se nesmí překrývat s dalším pravidlem, které je již aktivní.</span><span class="sxs-lookup"><span data-stu-id="8f481-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="8f481-123">Vyberte kategorii, pro kterou bude pravidlo platit.</span><span class="sxs-lookup"><span data-stu-id="8f481-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="8f481-124">Poznamenejte si, o jakou kategorii se jedná – budete ji potřebovat později.</span><span class="sxs-lookup"><span data-stu-id="8f481-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="8f481-125">Při výběru kategorie se do vybraného seznamu kategorií přidají její kategorie nebo nadřazené kategorie.</span><span class="sxs-lookup"><span data-stu-id="8f481-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="8f481-126">Vyberte možnost Zahrnout podkategorie, chcete-li pravidlo použít na všechny podkategorie vybrané kategorie.</span><span class="sxs-lookup"><span data-stu-id="8f481-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="8f481-127">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="8f481-127">Click Add.</span></span>
    * <span data-ttu-id="8f481-128">Pokud nastavíte možnost Zahrnout nadřazené pravidlo na Ano, pravidlo zásad, které definujete pro nadřazené kategorie, bude také přiřazeno podřízeným kategoriím, pokud nebylo žádné pravidlo zásad definováno pro podřízené kategorie.</span><span class="sxs-lookup"><span data-stu-id="8f481-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="8f481-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8f481-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="8f481-130">Vytvořit pravidlo zásad kategorie</span><span class="sxs-lookup"><span data-stu-id="8f481-130">Create a category policy rule</span></span>
1. <span data-ttu-id="8f481-131">Vyberte pravidlo zásad kategorie</span><span class="sxs-lookup"><span data-stu-id="8f481-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="8f481-132">Pokud je tlačítko Vytvořit pravidlo zásad zobrazeno šedě, vyberte aktivní pravidlo zásad a klepněte na tlačítko Vyřadit pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="8f481-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="8f481-133">Klikněte na Vytvořit pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="8f481-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="8f481-134">Do pole Datum platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="8f481-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="8f481-135">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="8f481-135">Click Add.</span></span>
5. <span data-ttu-id="8f481-136">Vyberte stejnou kategorii, která je použita pro pravidlo přístupu ke kategorii.</span><span class="sxs-lookup"><span data-stu-id="8f481-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="8f481-137">Vyberte možnost v poli Výběr dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8f481-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="8f481-138">Vyberte pravidlo, které určuje, jaký typ dodavatelů lze vybrat pro kategorii při vytváření žádanky.</span><span class="sxs-lookup"><span data-stu-id="8f481-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="8f481-139">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="8f481-139">Click Close.</span></span>
    * <span data-ttu-id="8f481-140">Vámi definovaná pravidla zásad, byla pro žádanky typu Spotřeba.</span><span class="sxs-lookup"><span data-stu-id="8f481-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="8f481-141">Pokud chcete definovat zásady pro žádanky typu Doplnění, vytvořte pravidlo pro typ pravidla zásad s názvem „Pravidlo zásad přístupu ke kategorii doplnění“.</span><span class="sxs-lookup"><span data-stu-id="8f481-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


