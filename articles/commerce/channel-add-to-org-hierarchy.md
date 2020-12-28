---
title: Přidání kanálu do organizační hierarchie
description: Toto téma popisuje, jak přidat kanál do organizační hierarchie v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 701c90e8e28b4419422cddde698e9c9862a588a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410746"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="a0863-103">Přidání kanálu do organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="a0863-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a0863-104">Toto téma popisuje, jak přidat kanál do organizační hierarchie v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a0863-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a0863-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="a0863-105">Overview</span></span>

<span data-ttu-id="a0863-106">Kanály je nutné přidružit k jedné nebo více organizačním hierarchiím.</span><span class="sxs-lookup"><span data-stu-id="a0863-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="a0863-107">Před vytvořením kanálů je nutné potvrdit, že byly nastaveny vaše organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="a0863-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="a0863-108">Viz [Organizční hierarchie](channels-org-hierarchies.md) pro další podrobnosti o vytváření organizačních hierarchií.</span><span class="sxs-lookup"><span data-stu-id="a0863-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="a0863-109">Vyberte hierarchii</span><span class="sxs-lookup"><span data-stu-id="a0863-109">Select a hierarchy</span></span>

<span data-ttu-id="a0863-110">Chcete-li vybrat hierarchii, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a0863-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="a0863-111">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Organizační hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="a0863-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="a0863-112">Ze seznamu vyberte organizační hierarchii, do které chcete přidat kanál.</span><span class="sxs-lookup"><span data-stu-id="a0863-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="a0863-113">Výběrem možnosti **Zobrazit** v podokně akcí zobrazíte podrobnosti hierarchie.</span><span class="sxs-lookup"><span data-stu-id="a0863-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="a0863-114">Následující obrázek zobrazuje podrobnosti organizační hierarchie pro vybranou hierarchii.</span><span class="sxs-lookup"><span data-stu-id="a0863-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Podrobnosti organizační hierarchie pro vybranou hierarchii](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="a0863-116">Přidání kanálu do uzlu hierachie</span><span class="sxs-lookup"><span data-stu-id="a0863-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="a0863-117">Chcete-li přidat kanál do uzlu hierachie, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a0863-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="a0863-118">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="a0863-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="a0863-119">Vyberte uzel hierachie, do kterého chcete přidat kanál, a poté v rozevíracím seznamu **Vložit** vyberte položku **Maloobchodní kanál**.</span><span class="sxs-lookup"><span data-stu-id="a0863-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="a0863-120">Vyberte kanál, který chcete přidat, a poté vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0863-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="a0863-121">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a0863-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="a0863-122">V podokně akcí vyberte **Publikovat** a zadejte **Datum platnosti** v minulosti, má-li být tato akce provedena okamžitě.</span><span class="sxs-lookup"><span data-stu-id="a0863-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="a0863-123">Následující obrázek ukazuje, jak vybrat kanál, který má být přidán do uzlu hierarchie.</span><span class="sxs-lookup"><span data-stu-id="a0863-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Výběr kanálu pro přidání do uzlu hierarchie](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="a0863-125">Na následujícím obrázku je znázorněna hierarchie s různými kanály.</span><span class="sxs-lookup"><span data-stu-id="a0863-125">The following image shows a hierarchy with various channels added.</span></span>

![Hierarchie s různými přidanými kanály](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="a0863-127">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a0863-127">Additional resources</span></span>

[<span data-ttu-id="a0863-128">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="a0863-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a0863-129">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="a0863-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a0863-130">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="a0863-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="a0863-131">Plánování organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="a0863-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="a0863-132">Organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="a0863-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="a0863-133">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="a0863-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="a0863-134">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="a0863-134">Set up an online channel</span></span>](channel-setup-online.md)
