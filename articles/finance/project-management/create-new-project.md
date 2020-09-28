---
title: Vytvořit nový projekt
description: Tohle téma obsahuje informace, jak vytvořit nový projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760493"
---
# <a name="create-a-new-project"></a><span data-ttu-id="c326d-103">Vytvořit nový projekt</span><span class="sxs-lookup"><span data-stu-id="c326d-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c326d-104">Pomocí následujících kroků vytvoříte nový projekt.</span><span class="sxs-lookup"><span data-stu-id="c326d-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="c326d-105">Na stránce **Správa projektu** vyberte **Nový projekt** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c326d-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="c326d-106">**Typ projektu:** Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="c326d-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="c326d-107">**Název projektu:** Upgrade XYZ fáze 2</span><span class="sxs-lookup"><span data-stu-id="c326d-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="c326d-108">**Skupina projektu:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="c326d-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="c326d-109">**ID projektové smlouvy:** 00000002</span><span class="sxs-lookup"><span data-stu-id="c326d-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="c326d-110">Zvolte **Vytvořit projekt**.</span><span class="sxs-lookup"><span data-stu-id="c326d-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="c326d-111">Přiřazení prostředku k projektu</span><span class="sxs-lookup"><span data-stu-id="c326d-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="c326d-112">Na stránce **Pracovníci** v seznamu **Pracovníci** vyberte záznam o zaměstnanci, pro kterého jste dříve nastavili kompetence, a otevřete záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="c326d-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="c326d-113">V podokně akcí na kartě **Projekt** ve skupině **Nastavení** zvolte **Přiřadit projekty**.</span><span class="sxs-lookup"><span data-stu-id="c326d-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="c326d-114">Na stránce **Přiřazení projektů ověření prostředku** na kartě **Projekty** v poli **Přidat projekt do vybraných projektů** pole filtrujte na projektu **Upgrade XYZ fáze 2**.</span><span class="sxs-lookup"><span data-stu-id="c326d-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="c326d-115">V podokně **Zbývající projekty** vyberte projekt, zvolte tlačítko šipky a přidejte ho do podokna **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="c326d-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="c326d-116">Podle potřeby můžete také přiřadit kategorie ke zdroji.</span><span class="sxs-lookup"><span data-stu-id="c326d-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="c326d-117">Typ kategorie jsou buď **Náklady** nebo **Výnosy**.</span><span class="sxs-lookup"><span data-stu-id="c326d-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="c326d-118">Typ kategorie je určen vaší organizací.</span><span class="sxs-lookup"><span data-stu-id="c326d-118">The category type is determined by your organization.</span></span> <span data-ttu-id="c326d-119">Pokud neexistují žádné přiřazené kategorie pro zdroj, aplikace Finance vyhledává výchozí kategorii pro hodinové ceny pro náklady a výnosy.</span><span class="sxs-lookup"><span data-stu-id="c326d-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="c326d-120">Nastavení vlastností prostředků a role projektu</span><span class="sxs-lookup"><span data-stu-id="c326d-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="c326d-121">Manažer projektu může použít funkci přidělení prostředků k projektu pro vytvoření rolí potřebných pro daný projekt.</span><span class="sxs-lookup"><span data-stu-id="c326d-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="c326d-122">Role lze použít, pokud potvrzené zdroje jsou během rezervace zdroje zatím neznámé.</span><span class="sxs-lookup"><span data-stu-id="c326d-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="c326d-123">Role lze použít pro dočasné rezervování jako plánovaných zdrojů, abyste mohli pokračovat ve fázi plánování projektu.</span><span class="sxs-lookup"><span data-stu-id="c326d-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="c326d-124">[![Příklad role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="c326d-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="c326d-125">**Scénář:** Společnost Contoso byla najata na dokončení projektu Čas a materiál, který má schválené stanovy projektu.</span><span class="sxs-lookup"><span data-stu-id="c326d-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="c326d-126">Nižší manažer projektu stále dokončuje rozsah projektu.</span><span class="sxs-lookup"><span data-stu-id="c326d-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="c326d-127">Manažer prostředků aktuálně identifikuje konkrétní zdroje, které budou rezervovány k práci na novém projektu.</span><span class="sxs-lookup"><span data-stu-id="c326d-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="c326d-128">S ohledem na kritickou povahu projektu investor projektu požaduje, aby jedna z rolí byla vrchní vedoucí projektu.</span><span class="sxs-lookup"><span data-stu-id="c326d-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="c326d-129">Správce zdrojů musí získat nový zdroj a rozhodne se, že určí roli v systému pro případ, že nižší manažer projektu bude potřebovat informace o zdroji během plánování projektu.</span><span class="sxs-lookup"><span data-stu-id="c326d-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="c326d-130">Následující pokyny popisují, jak může manažer prostředků nastavit roli Vrchní vedoucí projektu a přidružit k ní vlastnosti prostředků.</span><span class="sxs-lookup"><span data-stu-id="c326d-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="c326d-131">Později slouží role k vyhledání dostupných zdrojů, které odpovídají požadovaným kompetencím prostředku.</span><span class="sxs-lookup"><span data-stu-id="c326d-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="c326d-132">Na stránce **Nastavení role** vyberte **Nová** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c326d-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="c326d-133">**ID role:** vrchní manažer projektu</span><span class="sxs-lookup"><span data-stu-id="c326d-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="c326d-134">**Popis:** vrchní manažer projektu</span><span class="sxs-lookup"><span data-stu-id="c326d-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="c326d-135">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="c326d-135">Select **Create**.</span></span>
3. <span data-ttu-id="c326d-136">Vyberte roli **Vrchní manažer projektu** a zvolte **Konfigurace vlastností**.</span><span class="sxs-lookup"><span data-stu-id="c326d-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="c326d-137">V poli **Typ charakteristik** vyberte **Dovednost**.</span><span class="sxs-lookup"><span data-stu-id="c326d-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="c326d-138">V poli **Dostupné charakteristiky** zadejte hledanou dovednost.</span><span class="sxs-lookup"><span data-stu-id="c326d-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="c326d-139">V poli **Typ charakteristiky** vyberte **Certifikát**.</span><span class="sxs-lookup"><span data-stu-id="c326d-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="c326d-140">V poli **Dostupné charakteristiky** zadejte hledaný typ certifikátu.</span><span class="sxs-lookup"><span data-stu-id="c326d-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="c326d-141">Přiřazení prostředku projektu k projektu</span><span class="sxs-lookup"><span data-stu-id="c326d-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="c326d-142">Na stránce **Všechny projekty** vyberte projekt **Upgrade XYZ fáze 2**.</span><span class="sxs-lookup"><span data-stu-id="c326d-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="c326d-143">Na kartě **Projektový tým a plánování** zvolte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="c326d-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="c326d-144">V poli **Role** vyberte **Člen týmu**.</span><span class="sxs-lookup"><span data-stu-id="c326d-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="c326d-145">Zvolte **Rezervovat z kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="c326d-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="c326d-146">Na stránce **Dostupnost prostředku** zvolte **Zobrazit nastavení**.</span><span class="sxs-lookup"><span data-stu-id="c326d-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="c326d-147">Na stránce **Upravit nastavení zobrazení** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c326d-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="c326d-148">**Formát pro zobrazení rozsahu dat:** den</span><span class="sxs-lookup"><span data-stu-id="c326d-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="c326d-149">**Zobrazit popisy dostupnosti:** ano</span><span class="sxs-lookup"><span data-stu-id="c326d-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="c326d-150">**Zobrazit zbývající kapacitu:** ano</span><span class="sxs-lookup"><span data-stu-id="c326d-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="c326d-151">V seznamu zdrojů vyberte prostředek.</span><span class="sxs-lookup"><span data-stu-id="c326d-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="c326d-152">Vyberte **Závazná rezervace** a **Plná kapacita**.</span><span class="sxs-lookup"><span data-stu-id="c326d-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="c326d-153">Přiřazení prostředku k jiné roli</span><span class="sxs-lookup"><span data-stu-id="c326d-153">Assign a resource to a default role</span></span>

<span data-ttu-id="c326d-154">Pokud chcete usnadnit práci manažerům projektu nebo zdrojů, můžete přejít hlouběji do podrobností zdrojů, které lze pro projekt rezervovat.</span><span class="sxs-lookup"><span data-stu-id="c326d-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="c326d-155">Můžete přiřadit výchozí roli k existujícímu prostředku nebo nově získanému prostředku.</span><span class="sxs-lookup"><span data-stu-id="c326d-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="c326d-156">Například když byl přijat Daniel, měl zkušenosti a schopnosti plnit roli obchodního analytika.</span><span class="sxs-lookup"><span data-stu-id="c326d-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="c326d-157">Správce prostředků přiřadil tuto roli Danielovi jako výchozí.</span><span class="sxs-lookup"><span data-stu-id="c326d-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="c326d-158">Proto správce prostředků přidal Daniela do fondu obchodních analytiků, kteří jsou k dispozici pro práci na projektech.</span><span class="sxs-lookup"><span data-stu-id="c326d-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="c326d-159">Během rezervování zdrojů mohou projektoví manažeři filtrovat zdroje v roli, které jsou k dispozici pro práci na projektech.</span><span class="sxs-lookup"><span data-stu-id="c326d-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="c326d-160">Tyto údaje lze použít jako jednu z kritérií při provádění analýzy rozhodnutí s více kritérii během plnění prostředků.</span><span class="sxs-lookup"><span data-stu-id="c326d-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="c326d-161">Mohou také přidat další charakteristiky prostředků do filtru a vyhledat zdroje, které mají určité dovednosti, vzdělání a zkušenosti s daným projektem.</span><span class="sxs-lookup"><span data-stu-id="c326d-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="c326d-162">**Situace:** začal schválený projekt a role Hlavní manažer projektu byla během fáze plánování projektu rezervována jako plánovaný zdroj.</span><span class="sxs-lookup"><span data-stu-id="c326d-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="c326d-163">Manažer prostředků získá prostředek pro naplnění role Hlavní manažer projektu.</span><span class="sxs-lookup"><span data-stu-id="c326d-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="c326d-164">Na stránce **Seznam prostředků** vyberte **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="c326d-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="c326d-165">Na stránce **Role prostředku** vyberte **Nový** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c326d-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="c326d-166">**Platnost:** Zadejte aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="c326d-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="c326d-167">**Vypršení platnosti:** Zadejte **Nikdy**.</span><span class="sxs-lookup"><span data-stu-id="c326d-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="c326d-168">**Role:** Zadejte **Vrchní manažer projektu**.</span><span class="sxs-lookup"><span data-stu-id="c326d-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="c326d-169">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c326d-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="c326d-170">Na kartě **Kompetence** přidejte dovednost **ProjectMgmt** a certifikát **PMP**.</span><span class="sxs-lookup"><span data-stu-id="c326d-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
