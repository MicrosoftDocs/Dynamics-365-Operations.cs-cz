---
title: Použití mobilního pracovního prostoru správy majetku
description: Toto téma obsahuje informace o mobilním pracovním prostoru Správa majetku.
author: josaw1
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 65b3261367243b747b790c4a9ce5b4189aca85c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260123"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="fef95-103">Použití mobilního pracovního prostoru správy majetku</span><span class="sxs-lookup"><span data-stu-id="fef95-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fef95-104">Toto téma obsahuje informace o mobilním pracovním prostoru **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="fef95-105">Tento pracovní prostor umožňuje uživatelům zobrazovat a vytvářet požadavky na údržbu a pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="fef95-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="fef95-106">Uživatelé mohou také zobrazit přiřazené úlohy pracovního příkazu v kalendáři nebo v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fef95-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="fef95-107">Majetek a funkční místa lze také zobrazit a vyhledat.</span><span class="sxs-lookup"><span data-stu-id="fef95-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="fef95-108">Přehled</span><span class="sxs-lookup"><span data-stu-id="fef95-108">Overview</span></span>

<span data-ttu-id="fef95-109">Správa majetku je rozšířený modul pro správu majetku a úloh pracovních příkazů v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fef95-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fef95-110">Mobilní pracovní prostor **Správa majetku** umožňuje uživatelům rychle zobrazit přiřazené úlohy pracovního příkazu v mobilním zařízení podle svého výběru.</span><span class="sxs-lookup"><span data-stu-id="fef95-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="fef95-111">Uživatelé také mohou vytvářet a spravovat požadavky na údržbu, aktualizovat stav životního cyklu a zobrazovat podrobnosti o zdrojích a funkčních mísech pomocí svého mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="fef95-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="fef95-112">Konkrétně mobilní pracovní prostor **Správa majetku** uživatelům umožňuje provádění těchto úloh:</span><span class="sxs-lookup"><span data-stu-id="fef95-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="fef95-113">Vytvoření, zobrazení a úprava požadavků na údržbu, fotografování nebo připojení existujícího snímku k požadavku na údržbu, měnit stav životního cyklu žádosti o údržbu.</span><span class="sxs-lookup"><span data-stu-id="fef95-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="fef95-114">Vytvoření, zobrazení a úprava pracovních příkazů, fotografování nebo připojení existujícího snímku k pracovnímu příkazu, změna stavu životního cyklu pracovního příkazu, zobrazení úloh pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="fef95-115">Zobrazení přiřazených úloh pracovního příkazu v zobrazení kalendáře.</span><span class="sxs-lookup"><span data-stu-id="fef95-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="fef95-116">Vytvořit, zobrazit a upravit úlohu pracovního příkazu, aktualizovat čítače majetku, zobrazit kontrolní seznam údržby, zobrazit a upravit poznámky k úloze pracovního příkazu, zobrazit nástroje vyžadované pro úlohu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="fef95-117">Zobrazení nebo vyhledání konkrétního majetku nebo funkčního místa.</span><span class="sxs-lookup"><span data-stu-id="fef95-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fef95-118">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="fef95-118">Prerequisites</span></span>

<span data-ttu-id="fef95-119">Než budete moci použít mobilní pracovní prostor **Správa majetku**, musí váš správce nastavit požadované uživatelské a pracovní účty a pracovní prostor publikovat.</span><span class="sxs-lookup"><span data-stu-id="fef95-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="fef95-120">Další informace viz [Nastavení mobilního pracovního prostoru pro správu majetku](set-up-asset-management-mobile.md).</span><span class="sxs-lookup"><span data-stu-id="fef95-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="fef95-121">Stáhněte a nainstalujte mobilní aplikaci</span><span class="sxs-lookup"><span data-stu-id="fef95-121">Download and install the mobile app</span></span>

<span data-ttu-id="fef95-122">Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="fef95-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="fef95-123">Pro telefony Android</span><span class="sxs-lookup"><span data-stu-id="fef95-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="fef95-124">Pro telefony iPhone</span><span class="sxs-lookup"><span data-stu-id="fef95-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="fef95-125">Přihlaste se do mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="fef95-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="fef95-126">Spusťte aplikaci na svém mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="fef95-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="fef95-127">Zadejte adresu URL aplikace Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fef95-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="fef95-128">Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla.</span><span class="sxs-lookup"><span data-stu-id="fef95-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="fef95-129">Zadejte své přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="fef95-129">Enter your credentials.</span></span>

1. <span data-ttu-id="fef95-130">Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="fef95-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="fef95-131">Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="fef95-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="fef95-132">![Výběr pracovního prostoru](media/am-mobile-01.png "Výběr pracovního prostoru")</span><span class="sxs-lookup"><span data-stu-id="fef95-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="fef95-133">Zobrazení přiřazených úloh pracovního příkazu v zobrazení kalendáře</span><span class="sxs-lookup"><span data-stu-id="fef95-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="fef95-134">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-135">Vyberte **Kalendář mých úloh pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="fef95-136">Vyberte datum, pro které chcete zobrazit úlohy pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="fef95-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="fef95-137">V seznamu uvidíte ID majetku a ID funkčního místa pro každou úlohu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="fef95-138">V seznamu vyberte úlohu pracovního příkazu, v níž se zobrazí podrobnosti o úloze: informace o majetku a funkčním umístění a další navigační odkazy pro zobrazení možností **Přílohy**, **Kontrolní seznamy**, **Nástroje**, **Čítače majetku**, **Poznámky**, **Deníky**.</span><span class="sxs-lookup"><span data-stu-id="fef95-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="fef95-139">![Zobrazení přiřazených úloh pracovního příkazu v zobrazení kalendáře](media/am-mobile-02.png "Zobrazení přiřazených úloh pracovního příkazu v zobrazení kalendáře")</span><span class="sxs-lookup"><span data-stu-id="fef95-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="fef95-140">Vytvoření úlohy pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="fef95-140">Create a work order job</span></span>

1. <span data-ttu-id="fef95-141">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-142">Vyberte **Všechny pracovní příkazy údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="fef95-143">Vyberte pacovní příkazu, pro něhož chcete vytvořit novou úlohu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="fef95-144">Vyberte tlačítko **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="fef95-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="fef95-145">Vyberte **Majetek**, pro něhož chcete vytvořit novou úlohu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="fef95-146">Vyberte **Typ práce údržby**, **Variantu typu práce údržby** a **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="fef95-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="fef95-147">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-147">Select **Done**.</span></span>

    <span data-ttu-id="fef95-148">![Obrazovka Přidat řádek](media/am-mobile-03.png "Obrazovka Přidat řádek")</span><span class="sxs-lookup"><span data-stu-id="fef95-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="fef95-149">Přidejte přílohu k úloze pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="fef95-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="fef95-150">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-151">Vyberte **Všechny pracovní příkazy údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="fef95-152">Vyberte pacovní příkaz > úlohu pracovního příkazu, ke které chcete přidat příllohu.</span><span class="sxs-lookup"><span data-stu-id="fef95-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="fef95-153">Případně na domovské stránce vyberete **Kalendář mých úloh pracovního příkaz** nebo **Seznam mých úloh pracovního příkazu** a přejděte na stránku **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="fef95-154">Vyberte **Přílohy** na stránce **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="fef95-155">Na úloze pracovního příkazu uvidíte existující přílohy.</span><span class="sxs-lookup"><span data-stu-id="fef95-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="fef95-156">Vyberte **Přidat přílohu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="fef95-157">Zadejte **Název** a **Poznámky** k příloze.</span><span class="sxs-lookup"><span data-stu-id="fef95-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="fef95-158">Vyberte **Zvolit obrázek**, chcete-li vybrat fotografii z mobilní galerie nebo **Pořídit fotografii**, pokud chete pořídit fotografii.</span><span class="sxs-lookup"><span data-stu-id="fef95-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="fef95-159">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-159">Select **Done**.</span></span>

    <span data-ttu-id="fef95-160">![Zobrazení a přidání příloh k úloze pracovního příkazu](media/am-mobile-04.png "Zobrazení a přidání příloh k úloze pracovního příkazu")</span><span class="sxs-lookup"><span data-stu-id="fef95-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="fef95-161">Zobrazit kontrolní seznam údržby pro úlohu pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="fef95-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="fef95-162">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-163">Vyberte **Všechny pracovní příkazy údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="fef95-164">Vyberte pacovní příkaz > úloha pracovního příkazu, pro kterou chcete zobrazit kontrolní seznam.</span><span class="sxs-lookup"><span data-stu-id="fef95-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="fef95-165">Případně na domovské stránce vyberete **Kalendář mých úloh pracovního příkaz** nebo **Seznam mých úloh pracovního příkazu** a přejděte na stránku **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="fef95-166">Vyberte **Kontrolní seznamy** na stránce **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="fef95-167">Zobrazí se seznam řádků kontrolního seznamu, které souvisejí s úlohou pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="fef95-168">Chcete-li zobrazit **Pokyny** a přidat **Poznámky**, vyberte řádek kontrolního seznamu.</span><span class="sxs-lookup"><span data-stu-id="fef95-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="fef95-169">Chcete-li se vrátit k na předchozí stránku, klikněte na tlačítko Zpět (**<**).</span><span class="sxs-lookup"><span data-stu-id="fef95-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="fef95-170">![Kontrolní seznam údržby a podrobnosti o řádku](media/am-mobile-05.png "Kontrolní seznam údržby a podrobnosti o řádku")</span><span class="sxs-lookup"><span data-stu-id="fef95-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="fef95-171">Zobrazit a aktualizovat čítače majetku na úloze pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="fef95-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="fef95-172">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-173">Vyberte **Všechny pracovní příkazy údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="fef95-174">Vyberte pacovní příkaz > úloha pracovního příkazu, pro kterou chcete zobrazit čítače majetku.</span><span class="sxs-lookup"><span data-stu-id="fef95-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="fef95-175">Případně na domovské stránce vyberete **Kalendář mých úloh pracovního příkaz** nebo **Seznam mých úloh pracovního příkazu** a přejděte na stránku **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="fef95-176">Vyberte **Čítače majetku** na stránce **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="fef95-177">Zobrazí se seznam čítačů majetku, které souvisejí s úlohou pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="fef95-178">Chcete-li aktualizovat hodnotu čítače, vyberte ikonu tužky na řádku čítače majetku.</span><span class="sxs-lookup"><span data-stu-id="fef95-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="fef95-179">Zadejte novou hodnotu čítače a vyberte tlačítko **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="fef95-180">![Zobrazení a aktualizace počítadel majetku](media/am-mobile-06.png "Zobrazení a aktualizace počítadel majetku")</span><span class="sxs-lookup"><span data-stu-id="fef95-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="fef95-181">Registrovat spotřebu pro úlohu pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="fef95-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="fef95-182">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-183">Vyberte **Všechny pracovní příkazy údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="fef95-184">Vyberte pacovní příkaz > úloha pracovního příkazu, pro kterou chcete přidat registraci spotřeby.</span><span class="sxs-lookup"><span data-stu-id="fef95-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="fef95-185">Případně na domovské stránce vyberete **Kalendář mých úloh pracovního příkaz** nebo **Seznam mých úloh pracovního příkazu** a přejděte na stránku **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="fef95-186">Vyberte **Deníky** na stránce **Podrobnosti úlohy pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="fef95-187">Chcete-li vytvořit registrace pracovní doby, vyberte možnost **Přidat hodiny**.</span><span class="sxs-lookup"><span data-stu-id="fef95-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="fef95-188">Vyberte **Kategorii** z vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fef95-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="fef95-189">V poli **Hodiny** zadejte počet pracovních hodin strávených úlohou pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="fef95-190">Zvolte patřičnou **Vlastnost řádku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="fef95-191">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-191">Select **Done**.</span></span>

1. <span data-ttu-id="fef95-192">Chcete-li vytvořit registrace položek, vyberte možnost **Přidat položky**.</span><span class="sxs-lookup"><span data-stu-id="fef95-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="fef95-193">Vyberte **Číslo položky** z vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fef95-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="fef95-194">Vyberte **Pracoviště** z vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fef95-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="fef95-195">Zadejte **Množství** spotřebovaných položek.</span><span class="sxs-lookup"><span data-stu-id="fef95-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="fef95-196">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-196">Select **Done**.</span></span>

1. <span data-ttu-id="fef95-197">Chcete-li vytvořit registrace výdajů, vyberte možnost **Přidat výdaj**.</span><span class="sxs-lookup"><span data-stu-id="fef95-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="fef95-198">Vyberte **Kategorii** z vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fef95-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="fef95-199">Zadejte množství pro registraci výdaje.</span><span class="sxs-lookup"><span data-stu-id="fef95-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="fef95-200">Vybrat **Měnu prodeje** z vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fef95-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="fef95-201">Zadejte **Nákladovou cenu** pro registraci výdaje.</span><span class="sxs-lookup"><span data-stu-id="fef95-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="fef95-202">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-202">Select **Done**.</span></span>

    <span data-ttu-id="fef95-203">![Aktualizace deníku pracovních příkazů](media/am-mobile-07.png "Aktualizace deníku pracovních příkazů")</span><span class="sxs-lookup"><span data-stu-id="fef95-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="fef95-204">Aktualizace stavu životního na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="fef95-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="fef95-205">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-206">Vyberte **Všechny pracovní příkazy údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="fef95-207">Vyberte pracovní příkaz, pro něhož chcete aktualizovat stav životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="fef95-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="fef95-208">V dolní části obrazovky vyberte tlačítko **Ktualizovat stav**.</span><span class="sxs-lookup"><span data-stu-id="fef95-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="fef95-209">Vyberte ze seznamu nový stav životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="fef95-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="fef95-210">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-210">Select **Done**.</span></span>

    <span data-ttu-id="fef95-211">![Aktualizace stavu životního na pracovním příkazu.](media/am-mobile-08.png "Aktualizace stavu životního na pracovním příkazu.")</span><span class="sxs-lookup"><span data-stu-id="fef95-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="fef95-212">Vytvoření požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="fef95-212">Create a maintenance request</span></span>

1. <span data-ttu-id="fef95-213">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-214">Zvolte **Všechny žádosti údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="fef95-215">V části obrazovky vyberte **Akce** a vyberte **Vytvořit požadavek na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="fef95-216">Je-li povolena číselná řada pro požadavky na údržbu v modulu **Správa majetku**, pole **Požadavek na údržbu** je skryté, protože je automaticky vyplněno. Pokud je pole **Požadavek na údržbu** viditelné, vložte ID požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="fef95-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="fef95-217">Zvolte **Typ požadavku na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="fef95-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="fef95-218">Zadejte **Description** pro požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="fef95-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="fef95-219">Vyberte **Majetek**, pro který chcete vytvořit požadavek.</span><span class="sxs-lookup"><span data-stu-id="fef95-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="fef95-220">Vyberte **Úroveň služeb** pro požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="fef95-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="fef95-221">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-221">Select **Done**.</span></span>

    <span data-ttu-id="fef95-222">![Vytvoření požadavku na údržbu](media/am-mobile-09.png "Vytvoření požadavku na údržbu")</span><span class="sxs-lookup"><span data-stu-id="fef95-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="fef95-223">Přidat přílohu k požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="fef95-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="fef95-224">Na svém mobilním zařízení otevřete pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="fef95-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="fef95-225">Zvolte **Všechny žádosti údržby**.</span><span class="sxs-lookup"><span data-stu-id="fef95-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="fef95-226">Vyberte požadavek na údržbu, ke kterému chcete přidat přílohu.</span><span class="sxs-lookup"><span data-stu-id="fef95-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="fef95-227">Výberte **Přílohy** v dolní části obrazovky.</span><span class="sxs-lookup"><span data-stu-id="fef95-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="fef95-228">Vyberte **Přidat přílohy**.</span><span class="sxs-lookup"><span data-stu-id="fef95-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="fef95-229">Zadejte **Název** a **Poznámky** k příloze.</span><span class="sxs-lookup"><span data-stu-id="fef95-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="fef95-230">Vyberte **Zvolit obrázek**, chcete-li vybrat fotografii z mobilní galerie nebo **Pořídit fotografii**, pokud chete pořídit fotografii.</span><span class="sxs-lookup"><span data-stu-id="fef95-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="fef95-231">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="fef95-231">Select **Done**.</span></span>

    <span data-ttu-id="fef95-232">![Přidat přílohu k požadavku na údržbu](media/am-mobile-10.png "Přidat přílohu k požadavku na údržbu")</span><span class="sxs-lookup"><span data-stu-id="fef95-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]