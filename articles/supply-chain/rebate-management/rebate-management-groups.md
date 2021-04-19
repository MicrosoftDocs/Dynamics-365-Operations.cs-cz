---
title: Skupiny správy rabatu
description: Toto téma popisuje, jak nastavit data pro skupiny správy rabatu. Skupiny správy rabatu lze použít při výpočtech rabatu a lze je připojit k hlavnímu záznamu.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 2d1f8ed9def03afc97c0b4c5ea86430ff089aac6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819225"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="5d18e-104">Skupiny správy rabatu</span><span class="sxs-lookup"><span data-stu-id="5d18e-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5d18e-105">Výpočty rabatů a odpočtů mohou být řízeny skupinami.</span><span class="sxs-lookup"><span data-stu-id="5d18e-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="5d18e-106">Pro zákazníky, dodavatele a položky lze vytvořit skupiny správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="5d18e-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="5d18e-107">Mohou být připojeny k hlavnímu záznamu.</span><span class="sxs-lookup"><span data-stu-id="5d18e-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="5d18e-108">Skupiny zákazníka správy rabatu</span><span class="sxs-lookup"><span data-stu-id="5d18e-108">Rebate management customer groups</span></span>

<span data-ttu-id="5d18e-109">Výpočet pro skupinu zákazníků se často vytváří pro řetězec společností, jako je řetězec supermarketů nebo franšízová společnost.</span><span class="sxs-lookup"><span data-stu-id="5d18e-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="5d18e-110">Tento typ výpočtu obvykle souvisí s rabatem.</span><span class="sxs-lookup"><span data-stu-id="5d18e-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="5d18e-111">Odpočet se často počítá bez ohledu na to, komu byla kvalifikovaná objednávka prodána.</span><span class="sxs-lookup"><span data-stu-id="5d18e-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="5d18e-112">Existuje však několik výjimek.</span><span class="sxs-lookup"><span data-stu-id="5d18e-112">However, there are exceptions.</span></span> <span data-ttu-id="5d18e-113">Nabyvatel licence může například vytvořit schéma odpočtu, kde skupina zákazníků A obdrží 4 procenta, ale skupina zákazníků B obdrží pouze 3 procenta.</span><span class="sxs-lookup"><span data-stu-id="5d18e-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="5d18e-114">Nastavit skupiny odběratelů</span><span class="sxs-lookup"><span data-stu-id="5d18e-114">Set up customer groups</span></span>

<span data-ttu-id="5d18e-115">Chcete-li pracovat se skupinami zákazníků správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny zákazníků**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="5d18e-116">Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5d18e-117">U každé skupiny je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="5d18e-118">**Skupina správy rabatů** – Zadejte jedinečný název skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5d18e-119">**Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.</span><span class="sxs-lookup"><span data-stu-id="5d18e-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="5d18e-120">Správa přiřazení skupin zákazníků</span><span class="sxs-lookup"><span data-stu-id="5d18e-120">Manage customer group assignments</span></span>

<span data-ttu-id="5d18e-121">Každý zákazník může patřit do libovolného počtu skupin správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="5d18e-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5d18e-122">Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu zákazníků.</span><span class="sxs-lookup"><span data-stu-id="5d18e-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="5d18e-123">Chcete-li zobrazit, přidat nebo odebrat zákazníky pro vybranou skupinu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5d18e-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5d18e-124">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny zákazníků**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="5d18e-125">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-125">Select the group to manage.</span></span>
1. <span data-ttu-id="5d18e-126">V podokně akcí vyberte **Zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="5d18e-127">Zobrazí se stránka **Skupiny správy rabatů** se seznamem zákazníků, kteří jsou již členy vybrané skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="5d18e-128">Chcete-li do skupiny přidat nového zákazníka, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5d18e-129">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5d18e-130">**Účet zákazníka** - Vyberte ID účtu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="5d18e-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="5d18e-131">**Název** - Zadejte název anebo popis zákazníka.</span><span class="sxs-lookup"><span data-stu-id="5d18e-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="5d18e-132">Chcete-li odebrat zákazníka ze skupiny, vyberte zákazníka a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="5d18e-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5d18e-133">Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybraného zákazníka, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5d18e-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="5d18e-134">Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="5d18e-135">Vyberte zákazníka, se kterým chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="5d18e-136">V podokně akcí na kartě **Zákazník** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5d18e-137">Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraný zákazník patří.</span><span class="sxs-lookup"><span data-stu-id="5d18e-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="5d18e-138">Chcete-li do nové skupiny přidat zákazníka, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5d18e-139">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5d18e-140">**Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat zákazníka.</span><span class="sxs-lookup"><span data-stu-id="5d18e-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="5d18e-141">**Popis** - Zadejte popis skupiny (například pro vysvětlení, proč je zákazník jejím členem).</span><span class="sxs-lookup"><span data-stu-id="5d18e-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="5d18e-142">Chcete-li odebrat zákazníka ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="5d18e-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="5d18e-143">Skupiny dodavatelů správy rabatů</span><span class="sxs-lookup"><span data-stu-id="5d18e-143">Rebate management vendor groups</span></span>

<span data-ttu-id="5d18e-144">Výpočet pro skupinu dodavatelů se často vytváří pro skupinu míst dodání.</span><span class="sxs-lookup"><span data-stu-id="5d18e-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="5d18e-145">Tento typ výpočtu obvykle souvisí s rabatem.</span><span class="sxs-lookup"><span data-stu-id="5d18e-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="5d18e-146">Nastavení skupin dodavatele</span><span class="sxs-lookup"><span data-stu-id="5d18e-146">Set up vendor groups</span></span>

<span data-ttu-id="5d18e-147">Chcete-li pracovat se skupinami dodavatelů správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny dodavatelů**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="5d18e-148">Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5d18e-149">U každé skupiny je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="5d18e-150">**Skupina správy rabatů** – Zadejte jedinečný název skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5d18e-151">**Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.</span><span class="sxs-lookup"><span data-stu-id="5d18e-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="5d18e-152">Správa přiřazení skupin dodavatelů</span><span class="sxs-lookup"><span data-stu-id="5d18e-152">Manage vendor group assignments</span></span>

<span data-ttu-id="5d18e-153">Každý dodavatel může patřit do libovolného počtu skupin správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="5d18e-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5d18e-154">Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="5d18e-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="5d18e-155">Chcete-li zobrazit, přidat nebo odebrat dodavatele pro vybranou skupinu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5d18e-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5d18e-156">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny dodavatelů**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="5d18e-157">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-157">Select the group to manage.</span></span>
1. <span data-ttu-id="5d18e-158">V podokně akcí vyberte možnost **Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="5d18e-159">Zobrazí se stránka **Skupiny správy rabatů** se seznamem dodavatelů, kteří jsou již členy vybrané skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="5d18e-160">Chcete-li do skupiny přidat nového dodavatele, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5d18e-161">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5d18e-162">**Účet dodavatele** - Vyberte ID účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="5d18e-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="5d18e-163">**Název** - Zadejte název anebo popis dodavatele.</span><span class="sxs-lookup"><span data-stu-id="5d18e-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="5d18e-164">Chcete-li odebrat dodavatele ze skupiny, vyberte dodavatele a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="5d18e-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5d18e-165">Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybraného dodavatele, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5d18e-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="5d18e-166">Přejděte do části **Pohledávky \> Dodavatelé \> Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="5d18e-167">Vyberte dodavatele, se kterým chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="5d18e-168">V podokně akcí na kartě **Dodavatel** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5d18e-169">Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraný dodavatel patří.</span><span class="sxs-lookup"><span data-stu-id="5d18e-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="5d18e-170">Chcete-li do nové skupiny přidat dodavatele, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5d18e-171">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5d18e-172">**Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat dodavatele.</span><span class="sxs-lookup"><span data-stu-id="5d18e-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="5d18e-173">**Popis** - Zadejte popis skupiny (například pro vysvětlení, proč je dodavatel jejím členem).</span><span class="sxs-lookup"><span data-stu-id="5d18e-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="5d18e-174">Chcete-li odebrat dodavatele ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="5d18e-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="5d18e-175">Skupiny rabatu pro položky</span><span class="sxs-lookup"><span data-stu-id="5d18e-175">Item rebate groups</span></span>

<span data-ttu-id="5d18e-176">Seskupením položek získáte větší flexibilitu při výpočtu rabatů a odpočtů.</span><span class="sxs-lookup"><span data-stu-id="5d18e-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="5d18e-177">Tento přístup je často efektivnějším způsobem, jak nastavit rabaty a odpočty pro zákazníky a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="5d18e-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="5d18e-178">Nastavit skupiny položek</span><span class="sxs-lookup"><span data-stu-id="5d18e-178">Set up item groups</span></span>

<span data-ttu-id="5d18e-179">Chcete-li pracovat se skupinami položek správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="5d18e-180">Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5d18e-181">U každé skupiny je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="5d18e-182">**Skupina správy rabatů** – Zadejte jedinečný název skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5d18e-183">**Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.</span><span class="sxs-lookup"><span data-stu-id="5d18e-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="5d18e-184">Správa přiřazení skupin položek</span><span class="sxs-lookup"><span data-stu-id="5d18e-184">Manage item group assignments</span></span>

<span data-ttu-id="5d18e-185">Každá položka může patřit do libovolného počtu skupin správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="5d18e-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5d18e-186">Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu položek.</span><span class="sxs-lookup"><span data-stu-id="5d18e-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="5d18e-187">Můžete také přidat položky na základě vaší hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="5d18e-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="5d18e-188">Chcete-li zobrazit, přidat nebo odebrat položky pro vybranou skupinu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5d18e-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5d18e-189">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="5d18e-190">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-190">Select the group to manage.</span></span>
1. <span data-ttu-id="5d18e-191">V podokně akcí zvolte **Položky**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="5d18e-192">Zobrazí se stránka **Skupiny správy rabatů** se seznamem položek, kteří jsou již členy vybrané skupiny.</span><span class="sxs-lookup"><span data-stu-id="5d18e-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="5d18e-193">Chcete-li do skupiny přidat novou položku, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5d18e-194">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5d18e-195">**Účet položky** - Vyberte ID účtu položky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="5d18e-196">**Název produktu** - Zadejte název anebo popis položky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="5d18e-197">Chcete-li odebrat položku ze skupiny, vyberte položku a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="5d18e-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5d18e-198">Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybranéou položku, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5d18e-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="5d18e-199">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5d18e-200">Vyberte položku, se kterou chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-200">Select the item to work with.</span></span>
1. <span data-ttu-id="5d18e-201">V podokně akcí na kartě **Produkt** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5d18e-202">Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraná položka patří.</span><span class="sxs-lookup"><span data-stu-id="5d18e-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="5d18e-203">Chcete-li do nové skupiny přidat položku, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5d18e-204">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="5d18e-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5d18e-205">**Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat položku.</span><span class="sxs-lookup"><span data-stu-id="5d18e-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="5d18e-206">**Popis** - Zadejte popis skupiny (například pro vysvětlení, proč je položka jejím členem).</span><span class="sxs-lookup"><span data-stu-id="5d18e-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="5d18e-207">Chcete-li odebrat položku ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="5d18e-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5d18e-208">Chcete-li přidat položky do skupiny na základě vaší hierarchie kategorií, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5d18e-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5d18e-209">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="5d18e-210">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-210">Select the group to manage.</span></span>
1. <span data-ttu-id="5d18e-211">V podokně akcí zvolte **Přidat položky**.</span><span class="sxs-lookup"><span data-stu-id="5d18e-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="5d18e-212">V dialogovém okně **Přidat položky** v poli **Hierarchie kategorií** vyberte kategorii nejvyšší úrovně.</span><span class="sxs-lookup"><span data-stu-id="5d18e-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="5d18e-213">V levém podokně se otevře hierarchie položek.</span><span class="sxs-lookup"><span data-stu-id="5d18e-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="5d18e-214">Vyberte úroveň hierarchie, kterou hledáte.</span><span class="sxs-lookup"><span data-stu-id="5d18e-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="5d18e-215">Položky z vybrané hierarchie a úrovně hierarchie jsou nyní uvedeny v pravém podokně.</span><span class="sxs-lookup"><span data-stu-id="5d18e-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="5d18e-216">Při práci s podoknem postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="5d18e-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="5d18e-217">Zaškrtněte políčko pro každou položku, kterou chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="5d18e-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="5d18e-218">Zaškrtnutím políčka v záhlaví mřížky vyberte všechny uvedené položky.</span><span class="sxs-lookup"><span data-stu-id="5d18e-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="5d18e-219">Vyberte tlačítko **Zobrazit vybrané** pro filtrování mřížky tak, aby zobrazovala pouze položky, které jste dosud vybrali.</span><span class="sxs-lookup"><span data-stu-id="5d18e-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="5d18e-220">Opětovným stisknutím tlačítka se vrátíte na úplný seznam.</span><span class="sxs-lookup"><span data-stu-id="5d18e-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="5d18e-221">Vyberte **OK** a použijte výběr položek na vybranou skupinu.</span><span class="sxs-lookup"><span data-stu-id="5d18e-221">Select **OK** to apply your item selection to the selected group.</span></span>
