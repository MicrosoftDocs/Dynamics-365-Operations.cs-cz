---
title: Nastavení organizačních hierarchií
description: Toto téma popisuje, jak nastavit orhanizační hierarchie v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997768"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="76f29-103">Nastavení organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="76f29-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="76f29-104">Toto téma popisuje, jak nastavit orhanizační hierarchie v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="76f29-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="76f29-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="76f29-105">Overview</span></span>

<span data-ttu-id="76f29-106">Před vytvořením kanálů je nutné zajistit, že byly nastaveny organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="76f29-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="76f29-107">Organizační hierarchii můžete použít k zobrazení a tvorbě sestav vašeho podnikání z různých perspektiv.</span><span class="sxs-lookup"><span data-stu-id="76f29-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="76f29-108">Můžete například nastavit jednu hierarchii pro daňové, právní nebo statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="76f29-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="76f29-109">Potom můžete nastavit jinou hierarchii pro finanční informace sestavy, které nejsou vyžadovány zákonem, ale které se používají pro interní výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="76f29-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="76f29-110">Dříve než vytvoříte organizační hierarchií, musíte vytvořit organizace.</span><span class="sxs-lookup"><span data-stu-id="76f29-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="76f29-111">Další informace naleznete v [Vytvoření právnické osoby](channels-legal-entities.md) nebo [Vytvoření provozní jednotky](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="76f29-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="76f29-112">Další informace naleznete v následujících tématech.</span><span class="sxs-lookup"><span data-stu-id="76f29-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="76f29-113">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="76f29-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="76f29-114">Plánování organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="76f29-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="76f29-115">Vytvoření organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="76f29-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="76f29-116">Vytvoření organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="76f29-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="76f29-117">Následující postup použijte k vytvoření organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="76f29-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="76f29-118">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Organizační hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="76f29-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="76f29-119">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="76f29-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="76f29-120">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="76f29-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="76f29-121">V sekci **Účel** vyberte **Přiřadit účel**.</span><span class="sxs-lookup"><span data-stu-id="76f29-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="76f29-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="76f29-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="76f29-123">Vyberte účel, který chcete přiřadit k hierarchii organizace.</span><span class="sxs-lookup"><span data-stu-id="76f29-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="76f29-124">V sekci **Přiřazené hierarchie** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="76f29-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="76f29-125">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="76f29-125">In the list, mark the selected row.</span></span> <span data-ttu-id="76f29-126">Vyhledejte hierarchii, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="76f29-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="76f29-127">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76f29-127">Select **OK**.</span></span>

<span data-ttu-id="76f29-128">Následující obrázek znázorňuje ukázkovou organizační hierarchii vytvořenou pro fiktivní sadu obchodů "Adventure Works".</span><span class="sxs-lookup"><span data-stu-id="76f29-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Příklad organizační hierarchie](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="76f29-130">Přidání organizací do hierarchie</span><span class="sxs-lookup"><span data-stu-id="76f29-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="76f29-131">Chcete-li přidat organizace do hierachie, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="76f29-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="76f29-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="76f29-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="76f29-133">Vyberte svoji hierarchii.</span><span class="sxs-lookup"><span data-stu-id="76f29-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="76f29-134">V podokně akcí vyberte **Zobrazit**.</span><span class="sxs-lookup"><span data-stu-id="76f29-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="76f29-135">Podle potřeby přidejte organizace.</span><span class="sxs-lookup"><span data-stu-id="76f29-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="76f29-136">Chcete-li přidat organizaci, vyberte **Upravit** a pak vyberte **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="76f29-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="76f29-137">Po dokončení provádění změn můžete uložit návrh a publikovat změny.</span><span class="sxs-lookup"><span data-stu-id="76f29-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="76f29-138">Na následujícím obrázku je znázorněna právnická osoba přidaná v kořenové složce hierarchie se čtyřmi nákladovými středisky přidanými pro kanály "Obchodní centrum", "Outlet", "Online" a "Kontaktní středisko".</span><span class="sxs-lookup"><span data-stu-id="76f29-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="76f29-139">Do každé z nich lze přidat různé maloobchodní a online kanály.</span><span class="sxs-lookup"><span data-stu-id="76f29-139">Various retail, call center and online channels can then be added to each.</span></span>

![Příklad návrháře hierarchie](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="76f29-141">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="76f29-141">Additional resources</span></span>

[<span data-ttu-id="76f29-142">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="76f29-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76f29-143">Plánování organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="76f29-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76f29-144">Vytvořit právnické osoby</span><span class="sxs-lookup"><span data-stu-id="76f29-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="76f29-145">Vytvoření provozních jednotek</span><span class="sxs-lookup"><span data-stu-id="76f29-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76f29-146">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="76f29-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="76f29-147">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="76f29-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
