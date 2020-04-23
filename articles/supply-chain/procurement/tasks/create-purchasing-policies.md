---
title: Vytvoření zásad nákupu
description: Totot téma popisuje, jak vytvořit zásady nákupu a srovnat tak obchodní procesy pro nákup.
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e13a9a594e8c4041a586734df53321d57b43586
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204785"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="af363-103">Vytvoření zásad nákupu</span><span class="sxs-lookup"><span data-stu-id="af363-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af363-104">Totot téma popisuje, jak vytvořit zásady nákupu a srovnat tak obchodní procesy pro nákup.</span><span class="sxs-lookup"><span data-stu-id="af363-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="af363-105">Před vytvořením zásady nakupování nastavte parametry zásady nákupu.</span><span class="sxs-lookup"><span data-stu-id="af363-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="af363-106">Je možné vytvořit, upravit a vyřadit zásady nákupu, ale zásady nákupu nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="af363-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="af363-107">Tento proces obvykle provádí manažer nákupu.</span><span class="sxs-lookup"><span data-stu-id="af363-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="af363-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="af363-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="af363-109">Nastavení parametrů zásad</span><span class="sxs-lookup"><span data-stu-id="af363-109">Set up policy parameters</span></span>
1. <span data-ttu-id="af363-110">V navigačním podokně přejděte na **Moduly > Zásobování a nákup > Nastavení > Zásady > Zásady nákupu**.</span><span class="sxs-lookup"><span data-stu-id="af363-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="af363-111">V podokně akcí zvolte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="af363-111">In the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="af363-112">Pravidla priorit zásad se aplikují na různých úrovních ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="af363-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="af363-113">Organizační jednotky, které jsou zobrazeny, závisí na hierarchii v organizaci a na jakých úrovních v hierarchii byl přiřazena účel interní kontroly zásobování.</span><span class="sxs-lookup"><span data-stu-id="af363-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="af363-114">Například vaše organizace může používat právnické osoby, nákladová střediska, oblasti a oddělení, ale je možné, že jen některé z nich mají účel hierarchie Interní kontrola zásobování.</span><span class="sxs-lookup"><span data-stu-id="af363-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="af363-115">Ve výchozím stavu je k dispozici organizace typu Společnost.</span><span class="sxs-lookup"><span data-stu-id="af363-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="af363-116">Vyberte kartu **Parametry typu pravidla zásad**.</span><span class="sxs-lookup"><span data-stu-id="af363-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="af363-117">Ve stromové struktuře přejděte na **Zásady nákupu >Pravidlo kontroly pro nákupní žádanku**.</span><span class="sxs-lookup"><span data-stu-id="af363-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="af363-118">Pořadí zpracování zásad se definuje na úrovni zásad.</span><span class="sxs-lookup"><span data-stu-id="af363-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="af363-119">U některých typů zásad však můžete přepsat pořadí zpracování jednotlivých typů pravidel zásad.</span><span class="sxs-lookup"><span data-stu-id="af363-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="af363-120">Například můžete definovat pořadí zpracování zásad nákupu v tomto pořadí: nákladové centrum, oddělení, společnost.</span><span class="sxs-lookup"><span data-stu-id="af363-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="af363-121">V případě pravidla zásad katalogu můžete chtít upravit pořadí zpracování takto: oddělení, nákladové středisko, společnost.</span><span class="sxs-lookup"><span data-stu-id="af363-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="af363-122">Pořadí zpracování zásad změníte pro pravidlo zásad katalogu.</span><span class="sxs-lookup"><span data-stu-id="af363-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="af363-123">Jakmile zaměstnanec vytvoří požadavek, je určen katalog, který je zobrazen, podle zásad, které jsou přiřazeny k oddělení pracovníka a jeho nákladovému středisku a jeho společnosti.</span><span class="sxs-lookup"><span data-stu-id="af363-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="af363-124">Pokud je na výběr více organizačních úrovní, pomocí šipky nahoru nebo dolů můžete nastavit pořadí priorit pro pravidlo kontroly nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="af363-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="af363-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="af363-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="af363-126">Vytvořit nové zásady</span><span class="sxs-lookup"><span data-stu-id="af363-126">Create a new policy</span></span>
1. <span data-ttu-id="af363-127">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="af363-127">Select **New**.</span></span>
2. <span data-ttu-id="af363-128">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="af363-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="af363-129">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="af363-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="af363-130">Jednu zásadu nákupu lze použít pouze pro jednu organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="af363-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="af363-131">Například může mít jednu hierarchii nazývanou „Geografické“ a jednu „Oddělení“, a používat pro každou jiné zásady nákupu.</span><span class="sxs-lookup"><span data-stu-id="af363-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="af363-132">Vyberte organizaci, pro kterou chcete použít zásady.</span><span class="sxs-lookup"><span data-stu-id="af363-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="af363-133">Výběrem šipky přidejte vybranou organizaci.</span><span class="sxs-lookup"><span data-stu-id="af363-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="af363-134">Tento proces je možné zopakovat a přidat tak další organizace.</span><span class="sxs-lookup"><span data-stu-id="af363-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="af363-135">Přidání pravidla zásad</span><span class="sxs-lookup"><span data-stu-id="af363-135">Add a policy rule</span></span>
1. <span data-ttu-id="af363-136">V seznamu **Typ pravidla zásad** vyberte **pravidlo Účel žádanky**.</span><span class="sxs-lookup"><span data-stu-id="af363-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="af363-137">Vytvoříte pravidlo, které nastaví výchozí účel žádanky jako Spotřeba, ale umožní výběr možnosti Doplnění.</span><span class="sxs-lookup"><span data-stu-id="af363-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="af363-138">Vyberte **Vytvořit pravidlo zásad**.</span><span class="sxs-lookup"><span data-stu-id="af363-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="af363-139">Vyberte možnost **Ano** v poli **Povolit ruční přepsání**.</span><span class="sxs-lookup"><span data-stu-id="af363-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="af363-140">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="af363-140">Select **Close**.</span></span>
- <span data-ttu-id="af363-141">Nyní můžete nastavit jiná pravidla zásad pro zásady nákupu.</span><span class="sxs-lookup"><span data-stu-id="af363-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="af363-142">Všimněte si, že typ pravidel zásad nemůže mít překrývající se pravidla, která jsou aktivní současně v rámci jedné zásady zásobování.</span><span class="sxs-lookup"><span data-stu-id="af363-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  

