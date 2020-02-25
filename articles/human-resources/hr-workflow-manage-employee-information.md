---
title: Použití workflow ke správě informací o zaměstnanci
description: Tento článek vysvětluje, jak můžete použít funkci workflowu pro lidské zdroje ke správě informací o zaměstnancích. Například můžete přidružit workflow k pozici a konfigurovat workflow pro schválení, který se zahájí, když zaměstnanec změní svůj záznam.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a159f5fd811ee80c0ac45ca1b582f2f46fcb2c61
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008316"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="a825a-104">Použití workflow ke správě informací o zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="a825a-104">Use workflows to manage employee information</span></span>

<span data-ttu-id="a825a-105">Tento článek vysvětluje, jak můžete použít funkci workflowu pro lidské zdroje ke správě informací o zaměstnancích.</span><span class="sxs-lookup"><span data-stu-id="a825a-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="a825a-106">Například můžete přidružit workflow k pozici a konfigurovat workflow pro schválení, který se zahájí, když zaměstnanec změní svůj záznam.</span><span class="sxs-lookup"><span data-stu-id="a825a-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="a825a-107">Funkce workflowu pro lidské zdroje obsahuje velký počet workflowů pro správu aktivit lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="a825a-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="a825a-108">Navíc jsou k dispozici četné možnosti, abyste mohli upravit konkrétní workflowy a přidružit je k hierarchii vykazování.</span><span class="sxs-lookup"><span data-stu-id="a825a-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="a825a-109">Workflowy pomáhají při správě změn ve více standardních typech informací o zaměstnancích.</span><span class="sxs-lookup"><span data-stu-id="a825a-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="a825a-110">Workflow je možné přidružit k pozici.</span><span class="sxs-lookup"><span data-stu-id="a825a-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="a825a-111">Pokud poté zaměstnanci změní svůj záznam zaměstnance, zahájí se workflow, který vyžaduje schválení před uložením nových informací.</span><span class="sxs-lookup"><span data-stu-id="a825a-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="a825a-112">Workflowy jsou předem definované pro následující typy informací, které vám pomohou efektivně spravovat změny a zachovat přesnost dat zaměstnanců:</span><span class="sxs-lookup"><span data-stu-id="a825a-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="a825a-113">Identifikační čísla</span><span class="sxs-lookup"><span data-stu-id="a825a-113">Identification numbers</span></span>
-   <span data-ttu-id="a825a-114">Kurzy</span><span class="sxs-lookup"><span data-stu-id="a825a-114">Courses</span></span>
-   <span data-ttu-id="a825a-115">Vzdělání</span><span class="sxs-lookup"><span data-stu-id="a825a-115">Education</span></span>
-   <span data-ttu-id="a825a-116">Obrázek</span><span class="sxs-lookup"><span data-stu-id="a825a-116">Image</span></span>
-   <span data-ttu-id="a825a-117">Zapůjčené položky</span><span class="sxs-lookup"><span data-stu-id="a825a-117">Loaned items</span></span>
-   <span data-ttu-id="a825a-118">Odborné zkušenosti</span><span class="sxs-lookup"><span data-stu-id="a825a-118">Professional experience</span></span>
-   <span data-ttu-id="a825a-119">Zkušenost z projektu</span><span class="sxs-lookup"><span data-stu-id="a825a-119">Project experience</span></span>
-   <span data-ttu-id="a825a-120">Dovednosti</span><span class="sxs-lookup"><span data-stu-id="a825a-120">Skills</span></span>
-   <span data-ttu-id="a825a-121">Pozice důvěry</span><span class="sxs-lookup"><span data-stu-id="a825a-121">Positions of trust</span></span>
-   <span data-ttu-id="a825a-122">Akce lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="a825a-122">Human resources actions</span></span>
-   <span data-ttu-id="a825a-123">Registrace do kurzu</span><span class="sxs-lookup"><span data-stu-id="a825a-123">Course registration</span></span>

<span data-ttu-id="a825a-124">Když jsou zaměstnanci přijati, převedeni nebo ukončeni, workflow může zahrnovat proces přezkoumání.</span><span class="sxs-lookup"><span data-stu-id="a825a-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="a825a-125">Tímto způsobem může být přezkoumán dokument nebo lze definovat podmínky akce jako součást workflowu.</span><span class="sxs-lookup"><span data-stu-id="a825a-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="a825a-126">Po dokončení procesu přezkoumání se dokončí dokument nebo akce a workflow přejde ke kroku pro konečné schválení.</span><span class="sxs-lookup"><span data-stu-id="a825a-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="a825a-127">Přidružení workflowu k hierarchii pozic</span><span class="sxs-lookup"><span data-stu-id="a825a-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="a825a-128">Workflow lze přidružit k jakékoli hierarchii, kterou konfigurujete.</span><span class="sxs-lookup"><span data-stu-id="a825a-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="a825a-129">Pokud je například pozice přidružena k hierarchii vykazování matice, můžete nakonfigurovat workflow, který směruje výdaje pro konkrétní projekt na vedoucího projektu místo vedoucího zaměstnance, který je přidružen k této pozici.</span><span class="sxs-lookup"><span data-stu-id="a825a-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="a825a-130">Chcete-li vytvořit nový workflow nebo změnit existující workflow, na stránce **Workflowy lidských zdrojů** klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a825a-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="a825a-131">Vyberte workflow v seznamu, čímž spustíte Návrháře workflowů.</span><span class="sxs-lookup"><span data-stu-id="a825a-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="a825a-132">Návrháře můžete použít k vytvoření nového workflowu nebo změně kroků existujícího workflowu.</span><span class="sxs-lookup"><span data-stu-id="a825a-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="a825a-133">Když změníte existující workflow, změny jsou uloženy do nové verze.</span><span class="sxs-lookup"><span data-stu-id="a825a-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="a825a-134">Proto se můžete vždy vrátit zpět k předchozí verzi, pokud bude třeba.</span><span class="sxs-lookup"><span data-stu-id="a825a-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="a825a-135">Konfigurace workflowu lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="a825a-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="a825a-136">Chcete-li konfigurovat základní workflow, který je spuštěn, když zaměstnanci požadují změny v jejich osobní identifikaci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a825a-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="a825a-137">Na stránce **Workflowy lidských zdrojů** klikněte na tlačítko **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a825a-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="a825a-138">V seznamu dostupných workflowů vyberte **Identifikační čísla**.</span><span class="sxs-lookup"><span data-stu-id="a825a-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="a825a-139">Klikněte na tlačítko **Spustit** a spusťte Návrháře workflowů. Potom na výzvu zadejte uživatelské jméno a heslo.</span><span class="sxs-lookup"><span data-stu-id="a825a-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="a825a-140">Přetáhněte prvek **Schválit identifikační číslo** ze seznamu prvků workflowu na plátno návrháře.</span><span class="sxs-lookup"><span data-stu-id="a825a-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="a825a-141">Připojte prvek schválení k položkám **Začátek** a **Konec**.</span><span class="sxs-lookup"><span data-stu-id="a825a-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="a825a-142">Dvakrát klikněte na **Schválit prvek**a potom klikněte pravým tlačítkem myši a vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="a825a-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="a825a-143">Postupujte podle těchto kroků a přidejte pokyny pro pracovní položku:</span><span class="sxs-lookup"><span data-stu-id="a825a-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="a825a-144">Vyberte **Přiřazení**a potom vyberte **Hierarchie** pro typ přiřazení.</span><span class="sxs-lookup"><span data-stu-id="a825a-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="a825a-145">Pod výběrem **Hierarchie** vyberte **Konfigurovatelná hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="a825a-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="a825a-146">Přidejte podmínku ukončení a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a825a-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="a825a-147">Dokončete všechny další pokyny (neměly by existovat žádná další upozornění).</span><span class="sxs-lookup"><span data-stu-id="a825a-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="a825a-148">Klikněte na možnost **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="a825a-148">Click **Save and close**.</span></span> <span data-ttu-id="a825a-149">Aktivujte nový workflow, když se otevře dialogové okno, a vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="a825a-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="a825a-150">Přejděte to nabídky **Lidské zdroje** &gt; **Pozice** &gt; **Typy hierarchií pozic**.</span><span class="sxs-lookup"><span data-stu-id="a825a-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="a825a-151">Vyberte **Matice**.</span><span class="sxs-lookup"><span data-stu-id="a825a-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="a825a-152">Přidejte na seznam položku **Identifikační číslo pracovníka**.</span><span class="sxs-lookup"><span data-stu-id="a825a-152">Add the **Worker identification number** workflow to the list.</span></span>




