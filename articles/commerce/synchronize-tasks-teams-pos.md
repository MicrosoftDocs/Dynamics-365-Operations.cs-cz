---
title: Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS
description: Toto téma popisuje, jak synchronizovat správu úloh mezi pokladním místem (POS) Microsoft Teams a Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ca0cb32ac3ee508ddcd5346a895fb9904fa92517
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842629"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="743f6-103">Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="743f6-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="743f6-104">Toto téma popisuje, jak synchronizovat správu úloh mezi pokladním místem (POS) Microsoft Teams a Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="743f6-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="743f6-105">Jedním z hlavních účelů integrace Teams je umožnit synchronizaci správy úkolů mezi aplikací POS a Teams.</span><span class="sxs-lookup"><span data-stu-id="743f6-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="743f6-106">Tímto způsobem mohou zaměstnanci úložiště používat ke správě úkolů buď aplikaci POS nebo Teams, aniž by mezi nimi přepínali.</span><span class="sxs-lookup"><span data-stu-id="743f6-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="743f6-107">Protože Planner se používá jako úložiště pro úkoly v Teams, musí existovat propojení mezi Teams a Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="743f6-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="743f6-108">Tento odkaz je vytvořen pomocí ID konkrétního plánu pro daný tým obchodu.</span><span class="sxs-lookup"><span data-stu-id="743f6-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="743f6-109">Následující postupy ukazují, jak nastavit synchronizaci správy úloh mezi aplikacemi POS a Teams.</span><span class="sxs-lookup"><span data-stu-id="743f6-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="743f6-110">Publikování seznamu testovacích úkolů v Teams</span><span class="sxs-lookup"><span data-stu-id="743f6-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="743f6-111">Následující postup předpokládá, že týmy vašeho obchodu používají integraci správy úkolů Microsoft Teams s Commerce poprvé.</span><span class="sxs-lookup"><span data-stu-id="743f6-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="743f6-112">Chcete-li v Teams publikovat seznam testovacích úkolů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="743f6-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="743f6-113">Přihlaste se k Teams jako manažer komunikace.</span><span class="sxs-lookup"><span data-stu-id="743f6-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="743f6-114">Manažeři komunikace jsou obvykle uživatelé, kteří mají v Commerce roli **Regionální manažer**.</span><span class="sxs-lookup"><span data-stu-id="743f6-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="743f6-115">V levém navigačním podokně vyberte **Úkoly Planner**.</span><span class="sxs-lookup"><span data-stu-id="743f6-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="743f6-116">Na kartě **Publikované seznamy** vyberte **Nový seznam** v levém dolním rohu a pojmenujte nový seznam jako **Seznam testovacích úkolů**.</span><span class="sxs-lookup"><span data-stu-id="743f6-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="743f6-117">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="743f6-117">Select **Create**.</span></span> <span data-ttu-id="743f6-118">Nový seznam se zobrazí v sekci **Koncepty**.</span><span class="sxs-lookup"><span data-stu-id="743f6-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="743f6-119">V sekci **Název úkolu** pojmenujte první úkol jako **Integrace testovacích týmů**.</span><span class="sxs-lookup"><span data-stu-id="743f6-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="743f6-120">Poté stiskněte **Vstup**.</span><span class="sxs-lookup"><span data-stu-id="743f6-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="743f6-121">V seznamu **Koncepty** vyberte seznam úkolů.</span><span class="sxs-lookup"><span data-stu-id="743f6-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="743f6-122">Poté vyberte  **Publikovat**  v pravém horním rohu.</span><span class="sxs-lookup"><span data-stu-id="743f6-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="743f6-123">V dialogovém okně **Vyberte, komu publikovat** vyberte týmy, které by měly obdržet seznam testovacích úkolů.</span><span class="sxs-lookup"><span data-stu-id="743f6-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="743f6-124">Vyberte **Další** a zkontrolujte svůj publikační plán.</span><span class="sxs-lookup"><span data-stu-id="743f6-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="743f6-125">Pokud musíte provést změny, vyberte  **Zpět**.</span><span class="sxs-lookup"><span data-stu-id="743f6-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="743f6-126">Vyberte **Potvrdit a pokračovat** a potom vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="743f6-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="743f6-127">Po dokončení publikování se v horní části karty **Publikované seznamy** zobrazí zpráva se sdělením, zda byl váš seznam úkolů úspěšně doručen.</span><span class="sxs-lookup"><span data-stu-id="743f6-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="743f6-128">Další informace viz [Publikování seznamů úkolů pro vytváření a sledování práce ve vaší organizaci](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="743f6-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="743f6-129">Propojení aplikací POS a Teams pro správu úkolů</span><span class="sxs-lookup"><span data-stu-id="743f6-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="743f6-130">Abyste propojili aplikace POS a Microsoft Teams za účelem správy úkolů v centrále Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="743f6-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="743f6-131">Jděte na **Retail a Commerce \> Správa úkolů \> Integrace úkolů s Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="743f6-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="743f6-132">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="743f6-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="743f6-133">Nastavte možnost **Povolit integraci správy úkolů** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="743f6-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="743f6-134">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="743f6-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="743f6-135">V podokně akcí vyberte **Nastavit správu úkolů**.</span><span class="sxs-lookup"><span data-stu-id="743f6-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="743f6-136">Mělo by se zobrazit oznámení s informací, že se vytváří dávková úloha s názvem **Zřízení Teams**.</span><span class="sxs-lookup"><span data-stu-id="743f6-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="743f6-137">Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy** a vyhledejte nejnovější úlohu s popisem **Zřízení Teams**.</span><span class="sxs-lookup"><span data-stu-id="743f6-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="743f6-138">Počkejte, až se tato úloha dokončí.</span><span class="sxs-lookup"><span data-stu-id="743f6-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="743f6-139">Spusťte **Úloha CDX 1070**, abyste publikovali ID plánu a uložili odkazy na Retail Server.</span><span class="sxs-lookup"><span data-stu-id="743f6-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="743f6-140">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="743f6-140">Additional resources</span></span>

[<span data-ttu-id="743f6-141">Přehled integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="743f6-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="743f6-142">Povolení integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="743f6-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="743f6-143">Zřízení Microsoft Teams z Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="743f6-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="743f6-144">Správa uživatelských rolí v Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="743f6-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="743f6-145">Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy</span><span class="sxs-lookup"><span data-stu-id="743f6-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="743f6-146">Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="743f6-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
