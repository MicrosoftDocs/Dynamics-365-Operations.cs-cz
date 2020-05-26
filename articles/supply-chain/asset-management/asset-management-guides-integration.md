---
title: Integrace Dynamics 365 Supply Chain Management (správa majetku) s Dynamics 365 Guides
description: Toto téma vysvětluje, jak integrovat modul správy majetku do produktu Microsoft Dynamics 365 Supply Chain Management s Dynamics 365 Guides, aby bylo možné využít příručky smíšené reality ve vašich každodenních pracovních a servisních pracovních postupech.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f9ee7f1af8e88f56589c84bfaa063ea005aa353a
ms.sourcegitcommit: 88b4a9d19d16b0ef6543adf7c378a08bf0e07b3a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2020
ms.locfileid: "3311774"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="953a4-103">Integrace Dynamics 365 Supply Chain Management (správa majetku) s Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="953a4-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="953a4-104">Toto téma vysvětluje, jak integrovat modul **Správa majetku** do produktu Microsoft Dynamics 365 Supply Chain Management s Dynamics 365 Guides, aby bylo možné využít příručky smíšené reality ve vašich každodenních pracovních a servisních pracovních postupech.</span><span class="sxs-lookup"><span data-stu-id="953a4-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="953a4-105">Pokud je průvodce přiřazen k pracovnímu příkazu Správa majetku, pracovník, který otevře kontrolní seznam údržby objednávky v mobilní aplikaci Supply Chain Management (Dynamics 365), uvidí, že je průvodce k dispozici.</span><span class="sxs-lookup"><span data-stu-id="953a4-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="953a4-106">Pracovník pak může průvodce najít a otevřít v aplikaci Dynamics 365 Guides HoloLens.</span><span class="sxs-lookup"><span data-stu-id="953a4-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="953a4-107">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="953a4-107">Prerequisites</span></span>

<span data-ttu-id="953a4-108">Před připojením průvodců k pracovním příkazům správy aktiv musíte splnit tyto předpoklady:</span><span class="sxs-lookup"><span data-stu-id="953a4-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="953a4-109">[Nastavení Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) verze 10.0.9 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="953a4-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="953a4-110">[Zapnutí duálního zápisu pro aplikace Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="953a4-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="953a4-111">[Zapnutí testovací verze](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) pro funkci **MRGuidesFeature**.</span><span class="sxs-lookup"><span data-stu-id="953a4-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="953a4-112">(Pro produkční prostředí musíte nejprve odeslat lístek na podporu, aby byl váš klient přidán do skupiny testovací verze.)</span><span class="sxs-lookup"><span data-stu-id="953a4-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="953a4-113">[Zapněte následující konfigurační klíče](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) na stránce **Konfigurace licence**:</span><span class="sxs-lookup"><span data-stu-id="953a4-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="953a4-114">Správa majetku \> Smíšená realita správy majetku</span><span class="sxs-lookup"><span data-stu-id="953a4-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="953a4-115">Smíšená realita \> Průvodce smíšenou realitou</span><span class="sxs-lookup"><span data-stu-id="953a4-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="953a4-116">[Nastavení Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) verze 200.0.0.96 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="953a4-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="953a4-117">Použití Dynamics 365 Guides se správou majetku</span><span class="sxs-lookup"><span data-stu-id="953a4-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="953a4-118">Chcete-li průvodce přiřadit, použijte řádek kontrolního seznamu údržby ve správě aktiv.</span><span class="sxs-lookup"><span data-stu-id="953a4-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="953a4-119">Přidružení můžete vytvořit pomocí šablony kontrolního seznamu údržby, typu úlohy údržby nebo pracovní objednávky, protože všechny tři obsahují řádky kontrolního seznamu údržby.</span><span class="sxs-lookup"><span data-stu-id="953a4-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="953a4-120">Můžete ušetřit čas pomocí šablony, protože šablona může být spojena se všemi typy úloh údržby, které ji používají.</span><span class="sxs-lookup"><span data-stu-id="953a4-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="953a4-121">Například průvodce, který je spojen s typem úlohy údržby, je automaticky spojen se všemi pracovními příkazy, které specifikují daný typ úlohy.</span><span class="sxs-lookup"><span data-stu-id="953a4-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="953a4-122">Na druhé straně průvodce, který je přímo spojen s pracovním příkazem, existuje pouze pro tento pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="953a4-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="953a4-123">Přiřazení průvodce šabloně kontrolního seznamu údržby</span><span class="sxs-lookup"><span data-stu-id="953a4-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="953a4-124">Chcete-li přiřadit průvodce k šabloně kontrolního seznamu údržby, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="953a4-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="953a4-125">Vytvořte průvodce pomocí aplikací Dynamics 365 Guides PC a HoloLens.</span><span class="sxs-lookup"><span data-stu-id="953a4-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="953a4-126">Další informace o vytvoření průvodce naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="953a4-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="953a4-127">Vytvoření průvodce pomocí aplikace PC</span><span class="sxs-lookup"><span data-stu-id="953a4-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="953a4-128">Umístění hologramů pomocí aplikace HoloLens</span><span class="sxs-lookup"><span data-stu-id="953a4-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="953a4-129">V aplikaci Supply Chain Management [vytvořte šablonu kontrolního seznamu údržby](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="953a4-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="953a4-130">Přiřaďte průvodce, kterého jste vytvořili, k řádce kontrolního seznamu údržby v nové šabloně kontrolního seznamu údržby:</span><span class="sxs-lookup"><span data-stu-id="953a4-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="953a4-131">Na pevné záložce **Řádky kontrolního seznamu údržby** vyberte řádek, se kterým chcete průvodce spojit.</span><span class="sxs-lookup"><span data-stu-id="953a4-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="953a4-132">Na pevné záložce **Přidružení průvodci** vyberte **Přidat průvodce**.</span><span class="sxs-lookup"><span data-stu-id="953a4-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="953a4-133">![Přiřazení průvodce řádku kontrolního seznamu údržby](media/am-guides-integration-add-guide.png "Přiřazení průvodce řádku kontrolního seznamu údržby")</span><span class="sxs-lookup"><span data-stu-id="953a4-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="953a4-134">V poli **Název** vyberte průvodce a poté vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="953a4-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="953a4-135">![Výběr průvodce v poli Název](media/am-guides-integration-select-guide.png "Výběr průvodce v poli Název")</span><span class="sxs-lookup"><span data-stu-id="953a4-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="953a4-136">Přidružení šablony kontrolního seznamu údržby typu úlohy:</span><span class="sxs-lookup"><span data-stu-id="953a4-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="953a4-137">[Vytvořte typ úlohy údržby](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) nebo vyberte existující typ úlohy údržby.</span><span class="sxs-lookup"><span data-stu-id="953a4-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="953a4-138">V podokně akcí vyberte **Výchozí typ úlohy údržby**.</span><span class="sxs-lookup"><span data-stu-id="953a4-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="953a4-139">![Tlačítko Výchozí hodnoty typu práce údržby](media/am-guides-integration-job-defaults.png "Tlačítko Výchozí hodnoty typu práce údržby")</span><span class="sxs-lookup"><span data-stu-id="953a4-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="953a4-140">Vytvořte řádek a vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="953a4-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="953a4-141">![Vytvoření řádku](media/am-guides-integration-add-line.png "Vytvoření řádku")</span><span class="sxs-lookup"><span data-stu-id="953a4-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="953a4-142">V podokně akcí klikněte na možnost **Kontrolní seznam údržby**.</span><span class="sxs-lookup"><span data-stu-id="953a4-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="953a4-143">![Tlačítko Kontrolní seznamy údržby](media/am-guides-integration-maintenance-checklist.png "Tlačítko Kontrolní seznamy údržby")</span><span class="sxs-lookup"><span data-stu-id="953a4-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="953a4-144">Na pevné záložce **Řádky kontrolního seznamu údržby** přidejte řádek a poté změňte hodnotu pole **Typ** na **Šablona**.</span><span class="sxs-lookup"><span data-stu-id="953a4-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="953a4-145">![Změna hodnoty typu](media/am-guides-integration-checklist-lines.png "Změna hodnoty typu")</span><span class="sxs-lookup"><span data-stu-id="953a4-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="953a4-146">Na pevné záložce **Podrobnosti řádku** v poli **Šablona** vyberte šablonu, s níž jste průvodce spojili, a vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="953a4-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="953a4-147">![Výběr šablony](media/am-guides-integration-checklist-line-details.png "Výběr šablony")</span><span class="sxs-lookup"><span data-stu-id="953a4-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="953a4-148">[Vytvořte pracovní příkaz](work-orders/manually-created-workorders.md#create-work-order) a poté vyberte typ úlohy údržby, který používá šablonu kontrolního seznamu údržby, s níž jste průvodce spojili.</span><span class="sxs-lookup"><span data-stu-id="953a4-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="953a4-149">Průvodce je automaticky přiřazen k pracovnímu příkazu.</span><span class="sxs-lookup"><span data-stu-id="953a4-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="953a4-150">![Výběr typu úlohy údržby](media/am-guides-integration-create-work-order.png "Výběr typu úlohy údržby")</span><span class="sxs-lookup"><span data-stu-id="953a4-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="953a4-151">Podívejte se na průvodce, který je spojen s pracovním příkazem a zaměstnanci:</span><span class="sxs-lookup"><span data-stu-id="953a4-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="953a4-152">Otevřete [Mobilní pracovní prostor Správa majetku](asset-management-mobile-workspace.md) pro přístup k pracovnímu příkazu.</span><span class="sxs-lookup"><span data-stu-id="953a4-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="953a4-153">[Otevřete kontrolní seznam údržby](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) pro pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="953a4-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="953a4-154">Vyberte řádek kontrolního seznamu k zobrazení souvisejícího průvodce.</span><span class="sxs-lookup"><span data-stu-id="953a4-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="953a4-155">![Průvodce spojený s řádkem kontrolního seznamu](media/am-guides-integration-show-guide.png "Průvodce spojený s řádkem kontrolního seznamu")</span><span class="sxs-lookup"><span data-stu-id="953a4-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="953a4-156">Otevřete průvodce v aplikaci HoloLens.</span><span class="sxs-lookup"><span data-stu-id="953a4-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="953a4-157">![Otevřete průvodce v aplikaci HoloLens](media/am-guides-integration-hololens-select.png "Otevření průvodce v aplikaci HoloLens")</span><span class="sxs-lookup"><span data-stu-id="953a4-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="953a4-158">Průvodce můžete také přiřadit přímo do kontrolního seznamu údržby pracovního příkazu nebo typu úlohy.</span><span class="sxs-lookup"><span data-stu-id="953a4-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="953a4-159">Existuje známý problém, že když přiřadíte šablonu kontrolního seznamu údržby k výchozímu typu úlohy údržby, průvodce, který je propojen se šablonou, se nezobrazí na pevné záložce **Přidružení průvodci** stránky **Výchozí typ úlohy údržby**.</span><span class="sxs-lookup"><span data-stu-id="953a4-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="953a4-160">Průvodce se však zobrazí poté, co se daný typ úlohy použije na pracovní příkaz na pevné záložce **Přidružení průvodci**.</span><span class="sxs-lookup"><span data-stu-id="953a4-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="953a4-161">Viz také</span><span class="sxs-lookup"><span data-stu-id="953a4-161">See also</span></span>

- [<span data-ttu-id="953a4-162">Přehled dvojitého zápisu</span><span class="sxs-lookup"><span data-stu-id="953a4-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="953a4-163">Přehled správy majetku</span><span class="sxs-lookup"><span data-stu-id="953a4-163">Asset management overview</span></span>](index.md)