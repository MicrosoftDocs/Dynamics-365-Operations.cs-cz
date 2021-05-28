---
title: Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy
description: Toto téma popisuje, jak mapovat obchody a odpovídající týmy v Dynamics 365 Commerce Headquarters, pokud vaše organizace již vytvořila týmy v Microsoft Teams před integrací s Commerce.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ccc2cbf11e405facf310d93e5458cfe12a43146d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020212"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="2062f-103">Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy</span><span class="sxs-lookup"><span data-stu-id="2062f-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2062f-104">Toto téma popisuje, jak mapovat obchody a odpovídající týmy v Dynamics 365 Commerce Headquarters, pokud vaše organizace již vytvořila týmy v Microsoft Teams před integrací s Commerce.</span><span class="sxs-lookup"><span data-stu-id="2062f-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="2062f-105">Před integrací Dynamics 365 Commerce a Microsoft Teams může vaše organizace mít vytvořené týmy pro některé nebo všechny vaše obchody.</span><span class="sxs-lookup"><span data-stu-id="2062f-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="2062f-106">Pokud tomu tak je, musíte poskytnout mapování obchodů a odpovídající tým v Commerce Headquarters, pokud chcete vytvořit synchronizaci úkolů mezi Commerce POS a Microsoft Teams .</span><span class="sxs-lookup"><span data-stu-id="2062f-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="2062f-107">Mapování obchodů a odpovídajících týmů v Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="2062f-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="2062f-108">Pro mapování obchodů a odpovídajících týmů v Commerce Headquarters postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="2062f-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2062f-109">Přejděte do **Správa systému \> Pracovní prostor \> Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="2062f-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="2062f-110">Vyberte **Export**.</span><span class="sxs-lookup"><span data-stu-id="2062f-110">Select **Export**.</span></span> 
1. <span data-ttu-id="2062f-111">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="2062f-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2062f-112">V možnosti **Název skupiny** zadejte „Exportovat mapování Teams“.</span><span class="sxs-lookup"><span data-stu-id="2062f-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="2062f-113">Na záložce s náhledem **Vybrané entity** vyberte **Přidat entitu**.</span><span class="sxs-lookup"><span data-stu-id="2062f-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="2062f-114">Zobrazí se dialogové okno **Přidat entitu**.</span><span class="sxs-lookup"><span data-stu-id="2062f-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="2062f-115">Z rozevíracího seznamu **Název entity** vyberte **Mapování Teams mezi zdrojem a týmem**.</span><span class="sxs-lookup"><span data-stu-id="2062f-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="2062f-116">V rozevíracím seznamu **Formát cílových dat** vyberte **CSV**.</span><span class="sxs-lookup"><span data-stu-id="2062f-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="2062f-117">Vyberte **Přidat** a potom vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="2062f-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="2062f-118">Vlevo nahoře pod podoknem akcí vyberte **Exportovat nyní**.</span><span class="sxs-lookup"><span data-stu-id="2062f-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="2062f-119">V možnosti **Stav zpracování entity** vyberte **Stáhnout soubor**.</span><span class="sxs-lookup"><span data-stu-id="2062f-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="2062f-120">V exportovaném souboru CSV zadejte hodnoty pro **SOURCETYPE**, **SOURCEID** a **TEAMID** následně:</span><span class="sxs-lookup"><span data-stu-id="2062f-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="2062f-121">Pro **SOURCETYPE** zadejte „RetailStore“.</span><span class="sxs-lookup"><span data-stu-id="2062f-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="2062f-122">Pro **SOURCEID** zadejte číslo obchodu (například „000135“ pro obchod v San Francisku).</span><span class="sxs-lookup"><span data-stu-id="2062f-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="2062f-123">Čísla obchodů najdete v možnostech **Retail a Commerce \> Kanály \> Obchody**.</span><span class="sxs-lookup"><span data-stu-id="2062f-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="2062f-124">Pro **TEAMID** zadejte odpovídající ID týmu z Microsoft Teams (například, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span><span class="sxs-lookup"><span data-stu-id="2062f-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="2062f-125">Informace o ID týmu najdete na [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2062f-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="2062f-126">Uložte soubor CSV do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="2062f-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="2062f-127">Přejděte do **Správa systému \> Pracovní prostor \> Správa dat a poté zvolte** **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="2062f-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="2062f-128">Na záložce s náhledem **Vybrané entity** vyberte **Přidat soubor**.</span><span class="sxs-lookup"><span data-stu-id="2062f-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="2062f-129">Zobrazí se dialogové okno **Přidat soubor**.</span><span class="sxs-lookup"><span data-stu-id="2062f-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="2062f-130">Z rozevíracího seznamu **Název entity** vyberte **Mapování Teams mezi zdrojem a týmem**.</span><span class="sxs-lookup"><span data-stu-id="2062f-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="2062f-131">V rozevíracím seznamu **Formát zdrojových dat** vyberte **CSV**.</span><span class="sxs-lookup"><span data-stu-id="2062f-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="2062f-132">Vyberte **Nahrát a přidat**, vyberte soubor CSV, který jste dříve uložili, a poté vyberte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="2062f-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="2062f-133">V dialogovém okně **Přidat soubor** vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="2062f-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="2062f-134">V podokně akcí vyberte **Uložit** a potom vyberte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="2062f-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="2062f-135">Následující příkladový obrázek ukazuje skupinu **Exportovat mapování Teams** v Commerce s prvky **Přidat entitu** a zvýrazněnými záhlavími exportovaného souboru CSV.</span><span class="sxs-lookup"><span data-stu-id="2062f-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Export mapování Teams v Commerce s prvky přidání entity a zvýrazněnými záhlavími exportovaného souboru CSV](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="2062f-137">Po dokončení předchozích kroků postupujte podle pokynů v části [Synchronizace správy úkolů mezi Microsoft Teams a POS](synchronize-tasks-teams-pos.md) pro synchronizaci správy úkolů.</span><span class="sxs-lookup"><span data-stu-id="2062f-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2062f-138">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="2062f-138">Additional resources</span></span>

[<span data-ttu-id="2062f-139">Přehled integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2062f-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="2062f-140">Povolení integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2062f-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="2062f-141">Zřízení Microsoft Teams z Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2062f-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="2062f-142">Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="2062f-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="2062f-143">Správa uživatelských rolí v Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2062f-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="2062f-144">Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2062f-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
