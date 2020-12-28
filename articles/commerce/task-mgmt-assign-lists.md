---
title: Přiřazení seznamů úkolů k obchodům nebo zaměstnancům
description: Toto téma popisuje, jak přiřadit seznamy úkolů k obchodům nebo zaměstnancům v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410849"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="b67b3-103">Přiřazení seznamů úkolů k obchodům nebo zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="b67b3-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b67b3-104">Toto téma popisuje, jak přiřadit seznamy úkolů k obchodům nebo zaměstnancům v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b67b3-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b67b3-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b67b3-105">Overview</span></span>

<span data-ttu-id="b67b3-106">Správa úkolů v Dynamics 365 Commerce umožňuje přiřadit seznam úkolů několika obchodům nebo zaměstnancům nebo kombinaci obchodů a zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="b67b3-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="b67b3-107">Například regionální manažer 20 obchodů bude chtít přiřadit seznam úkolů **Příprava na letní sezónu** ke všem 20 obchodům.</span><span class="sxs-lookup"><span data-stu-id="b67b3-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="b67b3-108">Spuštění procesu přiřazení seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="b67b3-108">Start the task list assignment process</span></span>

<span data-ttu-id="b67b3-109">Chcete-li spustit proces přiřazování seznamu úkolů, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b67b3-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="b67b3-110">Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="b67b3-111">Vyberte seznam úkolů, který chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="b67b3-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="b67b3-112">Vyberte možnost **Spustit proces**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-112">Select **Start process**.</span></span>
1. <span data-ttu-id="b67b3-113">V dialogovém okně **Spuštění procesu** na kartě **Obecné** zadejete do pole **Název procesu** jeho název (například **Obchody ve východní oblasti**).</span><span class="sxs-lookup"><span data-stu-id="b67b3-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="b67b3-114">Do pole **Cílové datum** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="b67b3-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="b67b3-115">Chcete-li přiřadit seznam úkolů k obchodům, na kartě **Obchody** pomocí filtru **Organizační hierarchie** vyhledejte a vyberte obchody.</span><span class="sxs-lookup"><span data-stu-id="b67b3-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="b67b3-116">Chcete-li přiřadit seznam úkolů zaměstnancům, na kartě **Pracovníci** vyhledejte a vyberte zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="b67b3-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="b67b3-117">Tlačítkem **OK** spustíte proces.</span><span class="sxs-lookup"><span data-stu-id="b67b3-117">Select **OK** to start the process.</span></span> <span data-ttu-id="b67b3-118">Seznam úkolů je přiřazen k vybraným obchodům nebo zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="b67b3-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="b67b3-119">Následující ilustrace znázorňuje příklad, jak najít a vybrat obchody v dialogovém okně **Spuštění procesu**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Vyhledání a výběr obchodů v dialogovém okně Spuštění procesu](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="b67b3-121">Opakované přiřazování seznamů úkolů</span><span class="sxs-lookup"><span data-stu-id="b67b3-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="b67b3-122">Maloobchodní prodejce má někdy opakující se úkoly, například „Úkoly pro čtvrteční uzávěrku“ nebo „Úkoly pro první den v měsíci“.</span><span class="sxs-lookup"><span data-stu-id="b67b3-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="b67b3-123">Pro ty by se mu hodila možnost pravidelného přiřazování seznamu úkolů.</span><span class="sxs-lookup"><span data-stu-id="b67b3-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="b67b3-124">Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="b67b3-125">Vyberte seznam úkolů, který chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="b67b3-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="b67b3-126">Vyberte možnost **Spustit proces**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-126">Select **Start process**.</span></span>
1. <span data-ttu-id="b67b3-127">V dialogovém okně **Spuštění procesu** na kartě **Obecné** zadejete do pole **Název procesu** jeho název.</span><span class="sxs-lookup"><span data-stu-id="b67b3-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="b67b3-128">Nastavte možnost **Opakování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="b67b3-129">Do pole **Opakovaný posun cílového data ve dnech** zadejte počet dní.</span><span class="sxs-lookup"><span data-stu-id="b67b3-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="b67b3-130">Zadáte -li například hodnotu **4**, cílové datum bude datem opakování plus čtyři dny.</span><span class="sxs-lookup"><span data-stu-id="b67b3-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="b67b3-131">Na kartě **Spustit na pozadí** a vyberte možnost **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="b67b3-132">V dialogovém okně **Definovat opakování** zadejte kritéria četnosti a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="b67b3-133">Na následujícím obrázku je znázorněn příklad postupu při zadávání kritérií četnosti v dialogovém okně **Definovat opakování**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Zadání kritérií četnosti v dialogovém okně Definovat opakování](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="b67b3-135">Sledování stavu seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="b67b3-135">Track task list status</span></span>

<span data-ttu-id="b67b3-136">Jste-li regilnální manažer nebo manažer obchodu, budete pravděpodobně chtít sledovat stav seznamů úkolů, které byly přiřazeny více obchodům nebo zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="b67b3-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="b67b3-137">Poté můžete sledovat obchody nebo pracovníky, kteří nedokončili přiřazené úkoly včas.</span><span class="sxs-lookup"><span data-stu-id="b67b3-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="b67b3-138">Administrativa Commerce umožňuje zobrazit stav seznamů úkolů, přeřadit úkoly nebo změnit stav úkolu.</span><span class="sxs-lookup"><span data-stu-id="b67b3-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="b67b3-139">Chcete-li sledovat stav seznamu úkolů pro všechny úkoly, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="b67b3-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="b67b3-140">Přejděte na **Retail a Commerce \> Správa úkolů \> Procesy správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="b67b3-141">Chcete- li zobrazit stav všech seznamů úkolů, které jsou přiřazeny k různým obchodům, vyberte kartu **Všechny seznamy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="b67b3-142">Chcete-li sledovat stav seznamu úkolů pro všechny úkoly, které vám jsou přiřazeny, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="b67b3-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="b67b3-143">Přejděte na **Retail a Commerce \> Správa úkolů \> Procesy správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="b67b3-144">Chcete- li zobrazit nebo aktualizovat stav úkolů, které jsou vám přiřazeny, vyberte kartu **Moje úkoly** nebo **Všechny úkoly**.</span><span class="sxs-lookup"><span data-stu-id="b67b3-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b67b3-145">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b67b3-145">Additional resources</span></span>

[<span data-ttu-id="b67b3-146">Přehled správy úkolů</span><span class="sxs-lookup"><span data-stu-id="b67b3-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="b67b3-147">Konfigurace správy úkolů</span><span class="sxs-lookup"><span data-stu-id="b67b3-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="b67b3-148">Vytvoření seznamů úkolů a přidání úkolů</span><span class="sxs-lookup"><span data-stu-id="b67b3-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="b67b3-149">Správa úkolů v POS</span><span class="sxs-lookup"><span data-stu-id="b67b3-149">Task management in POS</span></span>](task-mgmt-POS.md)
