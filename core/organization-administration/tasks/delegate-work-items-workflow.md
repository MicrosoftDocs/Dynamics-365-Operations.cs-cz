--- 
title: "Delegování pracovních položek ve workflowu"
description: "Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6483307ff89ce79a3ef16bb763e3124ac537a5d8
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="55f58-103">Delegování pracovních položek ve workflowu</span><span class="sxs-lookup"><span data-stu-id="55f58-103">Delegate work items in a workflow</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55f58-104">Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="55f58-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="55f58-105">Tento postup umožňuje konfiguraci systému pro automatické delegování vašich pracovních položek jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="55f58-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="55f58-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="55f58-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="55f58-107">Nastavení automatického předávání</span><span class="sxs-lookup"><span data-stu-id="55f58-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="55f58-108">Přejděte na Společné > Nastavení > Možnosti uživatelů.</span><span class="sxs-lookup"><span data-stu-id="55f58-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="55f58-109">Klikněte na kartu Workflow.</span><span class="sxs-lookup"><span data-stu-id="55f58-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="55f58-110">Ujistěte se, že je rozbalená část Delegování.</span><span class="sxs-lookup"><span data-stu-id="55f58-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="55f58-111">Chcete-li nakonfigurovat systém tak, aby automaticky delegoval vaše pracovní položky ostatním uživatelům, je nutné vytvořit pravidla delegování, která určí, kdy se budou delegovat určité typy pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="55f58-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="55f58-112">Při vytváření pravidla delegování postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="55f58-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="55f58-113">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="55f58-113">Click Add.</span></span>
4. <span data-ttu-id="55f58-114">Vyberte volbu v poli Rozsah.</span><span class="sxs-lookup"><span data-stu-id="55f58-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="55f58-115">Vše - Delegování všech pracovních položek, které máte přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="55f58-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="55f58-116">Modul – Delegování pouze pracovních položek, které máte přiřazeny pro specifický typ workflowu.</span><span class="sxs-lookup"><span data-stu-id="55f58-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="55f58-117">Pokud vyberete tuto možnost, je nutné vybrat typ workflowu v poli Název.</span><span class="sxs-lookup"><span data-stu-id="55f58-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="55f58-118">Workflow – Delegování pouze pracovních položek, které máte přiřazeny pro specifický workflow.</span><span class="sxs-lookup"><span data-stu-id="55f58-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="55f58-119">Pokud vyberete tuto možnost, je nutné vybrat workflow v poli Název.</span><span class="sxs-lookup"><span data-stu-id="55f58-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="55f58-120">V poli Delegovat vyberte uživatele, kterému chcete pracovní položku delegovat.</span><span class="sxs-lookup"><span data-stu-id="55f58-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="55f58-121">Použijte pole Počáteční datum a čas a Koncové datum a čas k určení, kdy mají být pracovní položky automaticky delegovány.</span><span class="sxs-lookup"><span data-stu-id="55f58-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="55f58-122">Do pole Počáteční datum a čas zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="55f58-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="55f58-123">Do pole Koncové datum a čas zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="55f58-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="55f58-124">Zaškrtnutím políčka Povoleno můžete aktivovat pravidlo delegování.</span><span class="sxs-lookup"><span data-stu-id="55f58-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="55f58-125">Pokud jste vybrali Modul jako Rozsah, je nutné v poli Název vybrat modul.</span><span class="sxs-lookup"><span data-stu-id="55f58-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="55f58-126">Pokud jste vybrali Workflow jako Rozsah, je nutné v poli Název vybrat specifické workflow k delegování.</span><span class="sxs-lookup"><span data-stu-id="55f58-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="55f58-127">Do pole Komentář zadejte komentář s vysvětlením, proč delegujete pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="55f58-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


