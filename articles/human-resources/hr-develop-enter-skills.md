---
title: Zadejte dovednosti
description: Práce a manažeři mohou zadávat dovednosti v Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193970"
---
# <a name="enter-skills"></a><span data-ttu-id="8d861-103">Zadejte dovednosti</span><span class="sxs-lookup"><span data-stu-id="8d861-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8d861-104">Můžete zadat cílové dovednosti, nebo skutečné dovedností zaměstnanců, uchazečů nebo kontaktů v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8d861-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8d861-105">Cílové dovednosti jsou dovednosti, kterých se osoba chystá dosáhnout.</span><span class="sxs-lookup"><span data-stu-id="8d861-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="8d861-106">Skutečná dovednost je dovednost, kterou pracovník aktuálně disponuje.</span><span class="sxs-lookup"><span data-stu-id="8d861-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="8d861-107">Vytvořte pracovní postup pro automatické schvalování dovedností</span><span class="sxs-lookup"><span data-stu-id="8d861-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="8d861-108">Chcete-li zadat dovednosti bez nutnosti schválení, musíte vytvořit pracovní tok, který dovednosti automaticky schválí.</span><span class="sxs-lookup"><span data-stu-id="8d861-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="8d861-109">Dovednosti zadávané pracovníky vždy vyžadují souhlas vedoucího.</span><span class="sxs-lookup"><span data-stu-id="8d861-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="8d861-110">Tento pracovní postup pouze automaticky schvaluje dovednosti zadané manažery jménem jejich pracovníků.</span><span class="sxs-lookup"><span data-stu-id="8d861-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="8d861-111">V pracovním prostoru **Správa zaměstnanců** vyberte kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="8d861-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="8d861-112">V části **Nastavení** vyberte **Workflowy lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="8d861-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="8d861-113">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8d861-113">Select **New**.</span></span>

4. <span data-ttu-id="8d861-114">V podokně **Vytvořit pracovní postup** vyberte **Dovednosti pracovníků**.</span><span class="sxs-lookup"><span data-stu-id="8d861-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="8d861-115">[![Vyberte pracovní postup Dovednosti pracovníků](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="8d861-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="8d861-116">V dialogovém okně **Otevřít tento soubor?** vyberte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="8d861-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="8d861-117">Po výzvě zadejte své přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="8d861-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="8d861-118">V editoru pracovního postupu vyberte prvek pracovního toku **Schvánit dovednosti** a přetáhněte jej na plátno.</span><span class="sxs-lookup"><span data-stu-id="8d861-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="8d861-119">[![Vyberte prvek pracovního postupu Schválit dovednosti](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="8d861-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="8d861-120">Připojte prvek **Start** k prvku **Schválit dovednosti 1** a poté připojte prvek **Schválit dovednosti 1** k prvku **Konec**.</span><span class="sxs-lookup"><span data-stu-id="8d861-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="8d861-121">Možná se budete muset posunout dolů, abyste viděli prvek **Konec**.</span><span class="sxs-lookup"><span data-stu-id="8d861-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="8d861-122">Můžete jej přetáhnout blíže k ostatním prvkům.</span><span class="sxs-lookup"><span data-stu-id="8d861-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="8d861-123">[![Prvky propojit pracovní postupy](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="8d861-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="8d861-124">Poklepejte na prvek pracovního postupu **Schválit dovednosti 1** a poté klepněte pravým tlačítkem na prvek **Krok 1**.</span><span class="sxs-lookup"><span data-stu-id="8d861-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="8d861-125">Klepněte pravým tlačítkem na prvek **Krok 1** a poté vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="8d861-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="8d861-126">V okně **Vlastnosti** vyberte **Podmínka** na levé navigační liště.</span><span class="sxs-lookup"><span data-stu-id="8d861-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="8d861-127">Vyberte **Provést tento krok pouze v případě, že je splněna následující podmínka**.</span><span class="sxs-lookup"><span data-stu-id="8d861-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="8d861-128">Vyberte **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="8d861-128">Select **Add condition**.</span></span> <span data-ttu-id="8d861-129">Po **Kde** vyberte **Dovednosti v samoobsluze zaměstnanců** a potom vyberte **Dovednosti samoobsluhy zaměstnanců. Osoba**.</span><span class="sxs-lookup"><span data-stu-id="8d861-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="8d861-130">Po **je** vyberte **pole** a potom vyberte **Vztah mezi uživatelem a osobou**.</span><span class="sxs-lookup"><span data-stu-id="8d861-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="8d861-131">[![Uveďte podmínku](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="8d861-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="8d861-132">Vyberte **Úkol** na levé navigační liště.</span><span class="sxs-lookup"><span data-stu-id="8d861-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="8d861-133">Na kartě **Typ přiřazení** vyberte **Hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="8d861-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="8d861-134">Na kartě **Výběr hierarchie** v poli **Typ hierarchie:** vyberte **Manažerská hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="8d861-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="8d861-135">[![Určete manažerskou hierarchii](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="8d861-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="8d861-136">Vyberte **Zavřít**, vyberte **Pracovní postup** v popisu cesty k plátnu a poté vyberte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="8d861-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="8d861-137">Další informace o vytváření pracovních postupů naleznete v tématu [Přehled systému workflow](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json)</span><span class="sxs-lookup"><span data-stu-id="8d861-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="8d861-138">Zadejte dovednosti pro pracovníka</span><span class="sxs-lookup"><span data-stu-id="8d861-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="8d861-139">Vyberte pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8d861-139">Select a worker.</span></span>

2. <span data-ttu-id="8d861-140">Na panelu akcí na stránce **Pracovník** vyberte **Osoba** a potom vyberte **Dovednosti**.</span><span class="sxs-lookup"><span data-stu-id="8d861-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="8d861-141">Na stránce **Dovednosti** vyplňte následující pole pro každou dovednost:</span><span class="sxs-lookup"><span data-stu-id="8d861-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="8d861-142">**Dovednost**: Vyberte dovednost.</span><span class="sxs-lookup"><span data-stu-id="8d861-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="8d861-143">**Typ úrovně**: Vyberte **Aktuální** pro dovednost, kterou pracovník již má, nebo vyberte **Cílová** pro dovednost, na které pracovník pracuje.</span><span class="sxs-lookup"><span data-stu-id="8d861-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="8d861-144">**Úroveň**: Vyberte úroveň pro dovednosti pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8d861-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="8d861-145">**Datum dovednosti**: vyberte datum v nástroji kalendář.</span><span class="sxs-lookup"><span data-stu-id="8d861-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="8d861-146">**Zkoušející**: Je-li to vhodné, vyberte zkoušejícího ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="8d861-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="8d861-147">Můžete filtrovat vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8d861-147">You can filter your search.</span></span>
   - <span data-ttu-id="8d861-148">**Roky zkušeností**: Zadejte roky zkušeností.</span><span class="sxs-lookup"><span data-stu-id="8d861-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="8d861-149">**Ověřeno**: Pokud je dovednost ověřena, zaškrtněte políčko.</span><span class="sxs-lookup"><span data-stu-id="8d861-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="8d861-150">**Ověřil**: Zadejte název ověřovatele.</span><span class="sxs-lookup"><span data-stu-id="8d861-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="8d861-151">Až zadáte dovednosti, vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8d861-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d861-152">Viz také</span><span class="sxs-lookup"><span data-stu-id="8d861-152">See also</span></span>

[<span data-ttu-id="8d861-153">Nakonfigurujte dovednosti</span><span class="sxs-lookup"><span data-stu-id="8d861-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="8d861-154">Mapové dovednosti</span><span class="sxs-lookup"><span data-stu-id="8d861-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]