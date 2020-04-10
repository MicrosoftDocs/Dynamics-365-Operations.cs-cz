---
title: Delegování pracovních položek ve workflowu
description: Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140575"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="ddd05-103">Delegování položek práce ve workflow</span><span class="sxs-lookup"><span data-stu-id="ddd05-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="ddd05-104">Ručně delegování pracovní položky</span><span class="sxs-lookup"><span data-stu-id="ddd05-104">Manually delegate a work item</span></span>

<span data-ttu-id="ddd05-105">Pokud chcete delegovat oprávnění pro jednotlivé pracovní položky, vyberte možnost **Delegovat** v nabídce **Workflow** a zadejte uživatele k delegování a komentář.</span><span class="sxs-lookup"><span data-stu-id="ddd05-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="ddd05-106">Tím bude pracovní položka znovu přiřazena danému uživateli, aby ji mohl dokončit.</span><span class="sxs-lookup"><span data-stu-id="ddd05-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="ddd05-107">Automatické delegování pracovních položek</span><span class="sxs-lookup"><span data-stu-id="ddd05-107">Automatically delegate work items</span></span>

<span data-ttu-id="ddd05-108">Pokud plánujete absenci v kanceláři nebo nejste jinak schopní u pracovních položek nějakou dobu jednat, můžete automaticky delegovat nové pracovní položky na ostatní uživatele pomocí stránky **Uživatelské možnosti**.</span><span class="sxs-lookup"><span data-stu-id="ddd05-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="ddd05-109">Nastavení automatického předávání</span><span class="sxs-lookup"><span data-stu-id="ddd05-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="ddd05-110">Přejděte na **Společné > Nastavení > Možnosti uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="ddd05-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="ddd05-111">Klikněte na kartu **Workflow**. Zkontrolujte, zda je rozbalen oddíl Delegování.</span><span class="sxs-lookup"><span data-stu-id="ddd05-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="ddd05-112">Chcete-li nakonfigurovat systém tak, aby automaticky delegoval vaše pracovní položky ostatním uživatelům, je nutné vytvořit pravidla delegování, která určí, kdy se budou delegovat určité typy pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="ddd05-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="ddd05-113">Při vytváření pravidla delegování postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ddd05-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="ddd05-114">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ddd05-114">Click **Add**.</span></span>
4. <span data-ttu-id="ddd05-115">Vyberte volbu v poli **Rozsah**.</span><span class="sxs-lookup"><span data-stu-id="ddd05-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="ddd05-116">Vše - Delegování všech pracovních položek, které máte přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="ddd05-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="ddd05-117">Modul – Delegování pouze pracovních položek, které máte přiřazeny pro specifický typ workflowu.</span><span class="sxs-lookup"><span data-stu-id="ddd05-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="ddd05-118">Pokud vyberete tuto možnost, je nutné vybrat typ workflowu v poli Název.</span><span class="sxs-lookup"><span data-stu-id="ddd05-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="ddd05-119">Workflow – Delegování pouze pracovních položek, které máte přiřazeny pro specifický workflow.</span><span class="sxs-lookup"><span data-stu-id="ddd05-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="ddd05-120">Pokud vyberete tuto možnost, je nutné vybrat workflow v poli Název.</span><span class="sxs-lookup"><span data-stu-id="ddd05-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="ddd05-121">V poli **Delegovat** vyberte uživatele, kterému chcete pracovní položku delegovat.</span><span class="sxs-lookup"><span data-stu-id="ddd05-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="ddd05-122">Použijte pole Počáteční datum a čas a Koncové datum a čas k určení, kdy mají být pracovní položky automaticky delegovány.</span><span class="sxs-lookup"><span data-stu-id="ddd05-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="ddd05-123">Do pole **Počáteční datum a čas** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="ddd05-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="ddd05-124">Do pole **Koncové datum a čas** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="ddd05-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="ddd05-125">Zaškrtnutím políčka **Povoleno** můžete aktivovat pravidlo delegování.</span><span class="sxs-lookup"><span data-stu-id="ddd05-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="ddd05-126">Pokud jste vybrali **Modul** jako Rozsah, je nutné v poli Název vybrat modul.</span><span class="sxs-lookup"><span data-stu-id="ddd05-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="ddd05-127">Pokud jste vybrali **Workflow** jako Rozsah, je nutné v poli Název vybrat specifické workflow k delegování.</span><span class="sxs-lookup"><span data-stu-id="ddd05-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="ddd05-128">Do pole **Komentář** zadejte komentář s vysvětlením, proč delegujete pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="ddd05-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

