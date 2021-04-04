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
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3d249809f15b50c59620d69a901a427dc3ecb2f0
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477577"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="8ccc0-103">Přiřazení seznamů úkolů k obchodům nebo zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="8ccc0-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ccc0-104">Toto téma popisuje, jak přiřadit seznamy úkolů k obchodům nebo zaměstnancům v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8ccc0-105">Správa úkolů v Dynamics 365 Commerce umožňuje přiřadit seznam úkolů několika obchodům nebo zaměstnancům nebo kombinaci obchodů a zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="8ccc0-106">Například regionální manažer 20 obchodů bude chtít přiřadit seznam úkolů **Příprava na letní sezónu** ke všem 20 obchodům.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="8ccc0-107">Spuštění procesu přiřazení seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="8ccc0-107">Start the task list assignment process</span></span>

<span data-ttu-id="8ccc0-108">Chcete-li spustit proces přiřazování seznamu úkolů, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="8ccc0-109">Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="8ccc0-110">Vyberte seznam úkolů, který chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="8ccc0-111">Vyberte možnost **Spustit proces**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-111">Select **Start process**.</span></span>
1. <span data-ttu-id="8ccc0-112">V dialogovém okně **Spuštění procesu** na kartě **Obecné** zadejete do pole **Název procesu** jeho název (například **Obchody ve východní oblasti**).</span><span class="sxs-lookup"><span data-stu-id="8ccc0-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="8ccc0-113">Do pole **Cílové datum** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="8ccc0-114">Chcete-li přiřadit seznam úkolů k obchodům, na kartě **Obchody** pomocí filtru **Organizační hierarchie** vyhledejte a vyberte obchody.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="8ccc0-115">Chcete-li přiřadit seznam úkolů zaměstnancům, na kartě **Pracovníci** vyhledejte a vyberte zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="8ccc0-116">Tlačítkem **OK** spustíte proces.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-116">Select **OK** to start the process.</span></span> <span data-ttu-id="8ccc0-117">Seznam úkolů je přiřazen k vybraným obchodům nebo zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="8ccc0-118">Následující ilustrace znázorňuje příklad, jak najít a vybrat obchody v dialogovém okně **Spuštění procesu**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Vyhledání a výběr obchodů v dialogovém okně Spuštění procesu](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="8ccc0-120">Opakované přiřazování seznamů úkolů</span><span class="sxs-lookup"><span data-stu-id="8ccc0-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="8ccc0-121">Maloobchodní prodejce má někdy opakující se úkoly, například „Úkoly pro čtvrteční uzávěrku“ nebo „Úkoly pro první den v měsíci“.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="8ccc0-122">Pro ty by se mu hodila možnost pravidelného přiřazování seznamu úkolů.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="8ccc0-123">Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="8ccc0-124">Vyberte seznam úkolů, který chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="8ccc0-125">Vyberte možnost **Spustit proces**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-125">Select **Start process**.</span></span>
1. <span data-ttu-id="8ccc0-126">V dialogovém okně **Spuštění procesu** na kartě **Obecné** zadejete do pole **Název procesu** jeho název.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="8ccc0-127">Nastavte možnost **Opakování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="8ccc0-128">Do pole **Opakovaný posun cílového data ve dnech** zadejte počet dní.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="8ccc0-129">Zadáte -li například hodnotu **4**, cílové datum bude datem opakování plus čtyři dny.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="8ccc0-130">Na kartě **Spustit na pozadí** a vyberte možnost **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="8ccc0-131">V dialogovém okně **Definovat opakování** zadejte kritéria četnosti a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="8ccc0-132">Na následujícím obrázku je znázorněn příklad postupu při zadávání kritérií četnosti v dialogovém okně **Definovat opakování**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Zadání kritérií četnosti v dialogovém okně Definovat opakování](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="8ccc0-134">Sledování stavu seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="8ccc0-134">Track task list status</span></span>

<span data-ttu-id="8ccc0-135">Jste-li regilnální manažer nebo manažer obchodu, budete pravděpodobně chtít sledovat stav seznamů úkolů, které byly přiřazeny více obchodům nebo zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="8ccc0-136">Poté můžete sledovat obchody nebo pracovníky, kteří nedokončili přiřazené úkoly včas.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="8ccc0-137">Administrativa Commerce umožňuje zobrazit stav seznamů úkolů, přeřadit úkoly nebo změnit stav úkolu.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="8ccc0-138">Chcete-li sledovat stav seznamu úkolů pro všechny úkoly, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="8ccc0-139">Přejděte na **Retail a Commerce \> Správa úkolů \> Procesy správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="8ccc0-140">Chcete- li zobrazit stav všech seznamů úkolů, které jsou přiřazeny k různým obchodům, vyberte kartu **Všechny seznamy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="8ccc0-141">Chcete-li sledovat stav seznamu úkolů pro všechny úkoly, které vám jsou přiřazeny, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="8ccc0-142">Přejděte na **Retail a Commerce \> Správa úkolů \> Procesy správy úkolů**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="8ccc0-143">Chcete- li zobrazit nebo aktualizovat stav úkolů, které jsou vám přiřazeny, vyberte kartu **Moje úkoly** nebo **Všechny úkoly**.</span><span class="sxs-lookup"><span data-stu-id="8ccc0-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ccc0-144">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8ccc0-144">Additional resources</span></span>

[<span data-ttu-id="8ccc0-145">Přehled správy úkolů</span><span class="sxs-lookup"><span data-stu-id="8ccc0-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="8ccc0-146">Konfigurace správy úkolů</span><span class="sxs-lookup"><span data-stu-id="8ccc0-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="8ccc0-147">Vytvoření seznamů úkolů a přidání úkolů</span><span class="sxs-lookup"><span data-stu-id="8ccc0-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="8ccc0-148">Správa úkolů v POS</span><span class="sxs-lookup"><span data-stu-id="8ccc0-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
