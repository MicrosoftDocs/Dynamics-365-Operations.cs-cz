---
title: Delegování pracovních položek ve workflowu
description: Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48d8fd06217d318fa8208e11ffa5624f6be25be1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796699"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="32f0d-103">Delegování položek práce ve workflow</span><span class="sxs-lookup"><span data-stu-id="32f0d-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="32f0d-104">Ručně delegování pracovní položky</span><span class="sxs-lookup"><span data-stu-id="32f0d-104">Manually delegate a work item</span></span>

<span data-ttu-id="32f0d-105">Pokud chcete delegovat oprávnění pro jednotlivé pracovní položky, vyberte možnost **Delegovat** v nabídce **Workflow** a zadejte uživatele k delegování a komentář.</span><span class="sxs-lookup"><span data-stu-id="32f0d-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="32f0d-106">Tím bude pracovní položka znovu přiřazena danému uživateli, aby ji mohl dokončit.</span><span class="sxs-lookup"><span data-stu-id="32f0d-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="32f0d-107">Ruční delegování více pracovních položek</span><span class="sxs-lookup"><span data-stu-id="32f0d-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="32f0d-108">Více pracovních položek lze delegovat najednou na stránce **Pracovní položky přiřazené mně**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="32f0d-109">Pro hromadné delegování jsou způsobilé následující typy pracovních postupů: pracovní postup schvalování kupní smlouvy, pracovní postup nákupní objednávky, kontrola nákupní žádanky a pracovní postup faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="32f0d-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="32f0d-110">Funkce **delegování více pracovních položek** je ve výchozím nastavení zakázána a lze ji povolit v nabídce **Pracovní prostory > Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="32f0d-111">Chcete-li pomoci s povolením této funkce, obraťte se na správce systému.</span><span class="sxs-lookup"><span data-stu-id="32f0d-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="32f0d-112">Přejděte na **Společné > Společné > Pracovní položky > Pracovní položky přiřazené mně**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="32f0d-113">Vyberte pracovní položky, které mají být delegovány.</span><span class="sxs-lookup"><span data-stu-id="32f0d-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="32f0d-114">Klikněte na nabídku **Delegování pracovních položek**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="32f0d-115">V poli **Uživatel** vyberte uživatele, kterému chcete pracovní položku delegovat.</span><span class="sxs-lookup"><span data-stu-id="32f0d-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="32f0d-116">Do pole **Komentář** zadejte komentář s vysvětlením, proč delegujete pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="32f0d-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="32f0d-117">Klikněte na tlačítko **Delegovat pracovní položky**. Tím se delegování pracovní položky provede.</span><span class="sxs-lookup"><span data-stu-id="32f0d-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="32f0d-118">Automatické delegování pracovních položek</span><span class="sxs-lookup"><span data-stu-id="32f0d-118">Automatically delegate work items</span></span>

<span data-ttu-id="32f0d-119">Pokud plánujete absenci v kanceláři nebo nejste jinak schopní u pracovních položek nějakou dobu jednat, můžete automaticky delegovat nové pracovní položky na ostatní uživatele pomocí stránky **Uživatelské možnosti**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="32f0d-120">Nastavení automatického předávání</span><span class="sxs-lookup"><span data-stu-id="32f0d-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="32f0d-121">Přejděte na **Společné > Nastavení > Možnosti uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="32f0d-122">Klikněte na kartu **Workflow**. Zkontrolujte, zda je rozbalen oddíl Delegování.</span><span class="sxs-lookup"><span data-stu-id="32f0d-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="32f0d-123">Chcete-li nakonfigurovat systém tak, aby automaticky delegoval vaše pracovní položky ostatním uživatelům, je nutné vytvořit pravidla delegování, která určí, kdy se budou delegovat určité typy pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="32f0d-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="32f0d-124">Při vytváření pravidla delegování postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="32f0d-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="32f0d-125">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-125">Click **Add**.</span></span>
4. <span data-ttu-id="32f0d-126">Vyberte volbu v poli **Rozsah**:</span><span class="sxs-lookup"><span data-stu-id="32f0d-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="32f0d-127">Vše - Delegování všech pracovních položek, které máte přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="32f0d-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="32f0d-128">Modul – Delegování pouze pracovních položek, které máte přiřazeny pro specifický typ workflowu.</span><span class="sxs-lookup"><span data-stu-id="32f0d-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="32f0d-129">Pokud vyberete tuto možnost, je nutné vybrat typ workflowu v poli **Název**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="32f0d-130">Workflow – Delegování pouze pracovních položek, které máte přiřazeny pro specifický workflow.</span><span class="sxs-lookup"><span data-stu-id="32f0d-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="32f0d-131">Pokud vyberete tuto možnost, je nutné vybrat workflow v poli **Název**.</span><span class="sxs-lookup"><span data-stu-id="32f0d-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="32f0d-132">V poli **Název**:</span><span class="sxs-lookup"><span data-stu-id="32f0d-132">In the **Name** field:</span></span>
    - <span data-ttu-id="32f0d-133">Pro rozsah **Modul** vyberte cílový modul.</span><span class="sxs-lookup"><span data-stu-id="32f0d-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="32f0d-134">Pro rozsah **Workflow** vyberte cílový workflow.</span><span class="sxs-lookup"><span data-stu-id="32f0d-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="32f0d-135">V poli **Delegovat** vyberte uživatele, kterému chcete pracovní položku delegovat.</span><span class="sxs-lookup"><span data-stu-id="32f0d-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="32f0d-136">Použijte pole **Počáteční datum a čas** a **Koncové datum a čas** k určení, kdy mají být pracovní položky automaticky delegovány.</span><span class="sxs-lookup"><span data-stu-id="32f0d-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="32f0d-137">Do pole **Počáteční datum a čas** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="32f0d-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="32f0d-138">Do pole **Koncové datum a čas** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="32f0d-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="32f0d-139">Zaškrtnutím políčka **Povoleno** můžete aktivovat pravidlo delegování.</span><span class="sxs-lookup"><span data-stu-id="32f0d-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="32f0d-140">Do pole **Komentář** zadejte komentář s vysvětlením, proč delegujete pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="32f0d-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
