---
title: Vytvoření projektového týmu
description: Tohle téma obsahuje informace, jak vytvořit a spravovat projektové týmy.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760494"
---
# <a name="create-a-project-team"></a><span data-ttu-id="9f784-103">Vytvoření projektového týmu</span><span class="sxs-lookup"><span data-stu-id="9f784-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f784-104">Pokud chcete použít role, které byly dříve nastaveny, v projektu, projektový manažer musí přiřadit role k projektu.</span><span class="sxs-lookup"><span data-stu-id="9f784-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="9f784-105">Projektu může být přiřazeno více rolí.</span><span class="sxs-lookup"><span data-stu-id="9f784-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="9f784-106">Aby se zabránilo nejasnostem, aplikace automaticky označuje tyto role během rezervace.</span><span class="sxs-lookup"><span data-stu-id="9f784-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="9f784-107">Například pokud manažer projektu požaduje tři softwarové techniky, automaticky se vygenerují tři role softwarový technik, které jsou pojmenovány jako **Softwarový technik 1**, **Softwarový technik 2** a **Softwarový technik 3**.</span><span class="sxs-lookup"><span data-stu-id="9f784-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="9f784-108">Pokud byly dříve pro roli nastaveny charakteristiky role, jsou použity jako filtr při hledání zdroje.</span><span class="sxs-lookup"><span data-stu-id="9f784-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="9f784-109">Pro další upřesnění hledání lze volitelně přidat další charakteristiky.</span><span class="sxs-lookup"><span data-stu-id="9f784-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="9f784-110">Možnost Zobrazit nastavení lze také upravit tak, aby poskytovala lepší pohled na dostupnost prostředků.</span><span class="sxs-lookup"><span data-stu-id="9f784-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="9f784-111">K dispozici je možnost zobrazit dostupnost hodinově, denně, týdně, měsíčně, čtvrtletně a ročně.</span><span class="sxs-lookup"><span data-stu-id="9f784-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="9f784-112">Existuje také možnost zobrazit dostupnou a zbývající kapacitu prostředků.</span><span class="sxs-lookup"><span data-stu-id="9f784-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="9f784-113">Tato možnost je užitečná pro časovou správu, pokud odhadujete dostupný čas pro aktivity nebo dostupnost prostředku.</span><span class="sxs-lookup"><span data-stu-id="9f784-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="9f784-114">Manažer projektu může vybrat roli na stránce a poté, je-li dostupný prostředek, který odpovídá požadavkům, může vybrat a rezervovat prostředek pro obsazení role.</span><span class="sxs-lookup"><span data-stu-id="9f784-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="9f784-115">Mějte na paměti, že zdroje nemusí být v této fázi plánování rezervovány.</span><span class="sxs-lookup"><span data-stu-id="9f784-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="9f784-116">Při vytváření struktury WBS můžete nahradit role skutečnými personálními prostředky pro daný projekt.</span><span class="sxs-lookup"><span data-stu-id="9f784-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="9f784-117">Pokud role budou nahrazeny skutečnými zaměstnanci ve struktuře WBS, nastavení prostředků automaticky aktualizuje výpis a plánování projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="9f784-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="9f784-118">[![Seznam týmů projektu, který obsahuje role a skutečné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="9f784-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="9f784-119">Vedoucí projektu má řadu možností pro rezervaci zdroje na projekt, například **Zbývající kapacita**, **Plná kapacita**, **Procento kapacity** a **Zadání hodin**.</span><span class="sxs-lookup"><span data-stu-id="9f784-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="9f784-120">Tyto možnosti rezervace lze kdykoli zrušit v případě, že se změní přiřazení prostředků.</span><span class="sxs-lookup"><span data-stu-id="9f784-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="9f784-121">Podporovány jsou dva typy rezervace:</span><span class="sxs-lookup"><span data-stu-id="9f784-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="9f784-122">**Závazná rezervace** – Rezervace prostředku byla schválena a práce na projektu byla po určenou dobu trvání potvrzena.</span><span class="sxs-lookup"><span data-stu-id="9f784-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="9f784-123">**Předběžná rezervace** – rezervace prostředku a účast na projektu po určenou dobu trvání je nezávazně schválena.</span><span class="sxs-lookup"><span data-stu-id="9f784-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="9f784-124">Při vytváření projektového týmu postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="9f784-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="9f784-125">Vytvoření projektového týmu</span><span class="sxs-lookup"><span data-stu-id="9f784-125">Create a project team</span></span>

1. <span data-ttu-id="9f784-126">Na stránce se seznamem **Všechny projekty** vyberte projekt a pak vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9f784-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="9f784-127">Na kartě **Projektový tým a plánování** v poli **Naplánovat koncové datum** zadejte datum zahájení plánu posunuté o jeden měsíc.</span><span class="sxs-lookup"><span data-stu-id="9f784-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="9f784-128">Je-li datum zahájení plánu například 24. června 2017 (24/06/2017), zadejte **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="9f784-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="9f784-129">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="9f784-129">Select **Add**.</span></span>
4. <span data-ttu-id="9f784-130">V podokně **Přidat role do projektu** v poli **Role** vyberte **Vrchní manažer projektu**.</span><span class="sxs-lookup"><span data-stu-id="9f784-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="9f784-131">Vyberte **Požadované kompetence**.</span><span class="sxs-lookup"><span data-stu-id="9f784-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="9f784-132">Na stránce **Vybrat charakteristiky** jsou standardně zvoleny charakteristiky, které jste dříve nastavili pro roli Vrchní manažer projektu.</span><span class="sxs-lookup"><span data-stu-id="9f784-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="9f784-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f784-133">Select **OK**.</span></span>
7. <span data-ttu-id="9f784-134">Na stránce **Přidat role do projektu** v poli **Počet prostředků** zadejte **1**.</span><span class="sxs-lookup"><span data-stu-id="9f784-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="9f784-135">V poli **Prostředek** vyhledávání zobrazí všechny zdroje, které mají požadované kompetence.</span><span class="sxs-lookup"><span data-stu-id="9f784-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="9f784-136">Vyberte **Daniel Goldschmidt** a vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="9f784-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="9f784-137">Na stránce **Projekt** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="9f784-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="9f784-138">V podokně **Přidat role do projektu** v poli **Role** vyberte **Člen týmu**.</span><span class="sxs-lookup"><span data-stu-id="9f784-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="9f784-139">V poli **Počet prostředků** zadejte hodnotu **5**.</span><span class="sxs-lookup"><span data-stu-id="9f784-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="9f784-140">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="9f784-140">Select **Create**.</span></span>
12. <span data-ttu-id="9f784-141">Na stránce **Projekty** vyberte **Splnit prostředek**.</span><span class="sxs-lookup"><span data-stu-id="9f784-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="9f784-142">Monitorování projektových týmů</span><span class="sxs-lookup"><span data-stu-id="9f784-142">Monitor project teams</span></span>
1. <span data-ttu-id="9f784-143">Na stránce **Všechny projekty** vyberte odkaz **ID projektu** pro projekt **Upgrade XYZ fáze 2**.</span><span class="sxs-lookup"><span data-stu-id="9f784-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="9f784-144">Na pevné záložce **Projektový tým a plánování** ověřte správnost uvedených prostředků.</span><span class="sxs-lookup"><span data-stu-id="9f784-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
