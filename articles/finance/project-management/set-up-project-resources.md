---
title: Nastavení prostředků projektu
description: Tohle téma poskytuje informace o nastavení nebo požadování prostředků projektu.
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760498"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="954f4-103">Nastavení prostředků projektu</span><span class="sxs-lookup"><span data-stu-id="954f4-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="954f4-104">Musíte nastavit kalendář a přidružit jej se zaměstnancem nebo pracovníkem.</span><span class="sxs-lookup"><span data-stu-id="954f4-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="954f4-105">Kalendář lze použít pro naplánování projektu a pracovní doby zdrojů, které jsou na projekt rezervovány.</span><span class="sxs-lookup"><span data-stu-id="954f4-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="954f4-106">Během nastavení kalendáře může projektový manažer provádět vyrovnání zdrojů v rámci optimalizace zdrojů.</span><span class="sxs-lookup"><span data-stu-id="954f4-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="954f4-107">Na základě plánu kalendáře lze na zdroje uvalit omezení.</span><span class="sxs-lookup"><span data-stu-id="954f4-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="954f4-108">Můžete nastavit kalendář na stránce **Kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="954f4-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="954f4-109">Pokud nastavíte pracovníka jako projektový zdroj, můžete se vybrat z pracovníků, kteří pracují ve společnosti, pro kterou nastavujete zdroje.</span><span class="sxs-lookup"><span data-stu-id="954f4-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="954f4-110">Případně můžete vybrat pracovníky z ostatních společností ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="954f4-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="954f4-111">Tito pracovníci se označují jako mezipodnikové zdroje.</span><span class="sxs-lookup"><span data-stu-id="954f4-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="954f4-112">Následující postupy vysvětlují, jak nastavit pracovníka jako zdroj projektu v rámci společnosti a jak nastavit mezipodnikový zdroj projektu.</span><span class="sxs-lookup"><span data-stu-id="954f4-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="954f4-113">Nastavení pracovníka jako prostředek projektu</span><span class="sxs-lookup"><span data-stu-id="954f4-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="954f4-114">Na stránce **Pracovníci** v seznamu **Pracovníci** vyberte pracovníka, kterého chcete přidat jako prostředek projektu, a otevřete záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="954f4-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="954f4-115">V podokně akcí zvolte na **Projekt** &gt; **Nastavení** &gt; **Nastavení projektu**.</span><span class="sxs-lookup"><span data-stu-id="954f4-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="954f4-116">Vyberte kalendář a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="954f4-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="954f4-117">Můžete také určit výchozí projekty pro prostředky jako typ předběžného přiřazení.</span><span class="sxs-lookup"><span data-stu-id="954f4-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="954f4-118">Předběžné přiřazení lze použít, pokud manažer prostředků nebo projektu dopředu ví, na kterých projektech budou prostředky pracovat.</span><span class="sxs-lookup"><span data-stu-id="954f4-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="954f4-119">Předběžné přiřazení může být založeno také na žádosti investora projektu nebo odběratele.</span><span class="sxs-lookup"><span data-stu-id="954f4-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="954f4-120">Pokud chcete předběžně přiřadit projekt, na stránce **Přiřadit projekty** na kartě **Projekty** v seznamu **Zbývající projekty** vyberte příslušný projekt.</span><span class="sxs-lookup"><span data-stu-id="954f4-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="954f4-121">Nastavení mezipodnikového zdroje</span><span class="sxs-lookup"><span data-stu-id="954f4-121">Set up an intercompany resource</span></span>

<span data-ttu-id="954f4-122">Při nastavování pracovníka jako mezipodnikového zdroje je nutné dokončit nastavení ve společnosti poskytující půjčku a společnosti, která zažádala o půjčku.</span><span class="sxs-lookup"><span data-stu-id="954f4-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="954f4-123">Ve společnosti poskytující půjčku</span><span class="sxs-lookup"><span data-stu-id="954f4-123">In the lending company</span></span>

1. <span data-ttu-id="954f4-124">V aplikaci Finance ověřte, zda je vybrána společnost poskytující půjčku, a pak dokončete postup uvedený v předchozí části s názvem Nastavení pracovníka jako zdroje projektu.</span><span class="sxs-lookup"><span data-stu-id="954f4-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="954f4-125">Na stránce **Mezipodnikového účetnictví** vyberte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="954f4-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="954f4-126">V poli **ID právnické osoby** vyberte společnost poskytující půjčku.</span><span class="sxs-lookup"><span data-stu-id="954f4-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="954f4-127">Podle potřeby vyplňte zbývající pole a potom zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="954f4-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="954f4-128">Na stránce **Mezipodniková cena** vyberte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="954f4-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="954f4-129">V poli **Právnická osoba, která si půjčuje** vyberte příslušnou společnost.</span><span class="sxs-lookup"><span data-stu-id="954f4-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="954f4-130">Pokud si chcete od společnosti poskytující půjčku pouze vypůjčit zdroj, který jste vytvořili na začátku této části, v poli **Zdroj**, vyberte název zdroje, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="954f4-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="954f4-131">Pokud chcete zpřístupnit všechny zdroje společnosti poskytující půjčku společnosti, která si půjčuje, ponechte pole **Zdroj** prázdné.</span><span class="sxs-lookup"><span data-stu-id="954f4-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="954f4-132">Na stránce **Parametry modulu Řízení a účetnictví projektu** na kartě **Mezipodnikové** nastavte možnost **Povolit mezipodnikové plánování prostředků a časové rozvrhy** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="954f4-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="954f4-133">Ve společnosti, která zažádala o půjčku </span><span class="sxs-lookup"><span data-stu-id="954f4-133">In the borrowing company</span></span>

- <span data-ttu-id="954f4-134">Na stránce **Seznam zdrojů** ve filtru vyhledávání zadejte název zdroje, který jste vytvořili v předchozím postupu pro společnost poskytující půjčku, a ověřte, že název je zahrnut v seznamu zdrojů pro společnost, která žádá o půjčku.</span><span class="sxs-lookup"><span data-stu-id="954f4-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="954f4-135">Žádost o prostředky projektu</span><span class="sxs-lookup"><span data-stu-id="954f4-135">Request project resources</span></span>
<span data-ttu-id="954f4-136">Funkce pro plánování projektových zdrojů umožní pouze správcům zdrojů distribuovat personální zdroje na aktivity nebo projekty.</span><span class="sxs-lookup"><span data-stu-id="954f4-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="954f4-137">Chcete-li povolit tuto funkci, proveďte následující úlohy nebo ověřte, že byly dokončeny:</span><span class="sxs-lookup"><span data-stu-id="954f4-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="954f4-138">Nastavte číselné řady.</span><span class="sxs-lookup"><span data-stu-id="954f4-138">Set up number sequences.</span></span>
- <span data-ttu-id="954f4-139">Nastavte workflowy pro řízení a účetnictví projektu.</span><span class="sxs-lookup"><span data-stu-id="954f4-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="954f4-140">Povolit workflowy žádosti o prostředek.</span><span class="sxs-lookup"><span data-stu-id="954f4-140">Enable resource request workflows.</span></span>

<span data-ttu-id="954f4-141">Po dokončení předcházejících úkolů můžete provést následující úkoly podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="954f4-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="954f4-142">Vytvořte požadavek na prostředek z předběžně definovaných personálních prostředků.</span><span class="sxs-lookup"><span data-stu-id="954f4-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="954f4-143">Monitorujte požadavky na prostředky.</span><span class="sxs-lookup"><span data-stu-id="954f4-143">Monitor resource requests.</span></span>
- <span data-ttu-id="954f4-144">Naplňte požadavky na prostředky</span><span class="sxs-lookup"><span data-stu-id="954f4-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="954f4-145">Požádejte o personální prostředek z WBS.</span><span class="sxs-lookup"><span data-stu-id="954f4-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="954f4-146">Zarezervujte si zdroje na projektu bez požadavku na personální prostředek.</span><span class="sxs-lookup"><span data-stu-id="954f4-146">Book resources to a project without having a request for a staffed resource.</span></span>
