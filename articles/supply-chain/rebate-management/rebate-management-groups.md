---
title: Skupiny správy rabatu
description: Toto téma popisuje, jak nastavit data pro skupiny správy rabatu. Skupiny správy rabatu lze použít při výpočtech rabatu a lze je připojit k hlavnímu záznamu.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271070"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="70b72-104">Skupiny správy rabatu</span><span class="sxs-lookup"><span data-stu-id="70b72-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70b72-105">Výpočty správy rabatů mohou být řízeny skupinami.</span><span class="sxs-lookup"><span data-stu-id="70b72-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="70b72-106">Pro zákazníky, dodavatele a položky lze vytvořit skupiny správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="70b72-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="70b72-107">Mohou být připojeny k hlavnímu záznamu.</span><span class="sxs-lookup"><span data-stu-id="70b72-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="70b72-108">Skupiny zákazníka správy rabatu</span><span class="sxs-lookup"><span data-stu-id="70b72-108">Rebate management customer groups</span></span>

<span data-ttu-id="70b72-109">Výpočet pro skupinu zákazníků se často vytváří pro řetězec společností, jako je řetězec supermarketů nebo franšízová společnost.</span><span class="sxs-lookup"><span data-stu-id="70b72-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="70b72-110">Tento typ výpočtu obvykle souvisí s rabatem.</span><span class="sxs-lookup"><span data-stu-id="70b72-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="70b72-111">Odpočet se často počítá bez ohledu na to, komu byla kvalifikovaná objednávka prodána.</span><span class="sxs-lookup"><span data-stu-id="70b72-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="70b72-112">Existuje však několik výjimek.</span><span class="sxs-lookup"><span data-stu-id="70b72-112">However, there are exceptions.</span></span> <span data-ttu-id="70b72-113">Nabyvatel licence může například vytvořit schéma odpočtu, kde skupina zákazníků A obdrží 4 procenta, ale skupina zákazníků B obdrží pouze 3 procenta.</span><span class="sxs-lookup"><span data-stu-id="70b72-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="70b72-114">Nastavit skupiny odběratelů</span><span class="sxs-lookup"><span data-stu-id="70b72-114">Set up customer groups</span></span>

<span data-ttu-id="70b72-115">Chcete-li pracovat se skupinami zákazníků správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny zákazníků**.</span><span class="sxs-lookup"><span data-stu-id="70b72-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="70b72-116">Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="70b72-117">U každé skupiny je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="70b72-118">**Skupina správy rabatů** – Zadejte jedinečný název skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="70b72-119">**Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.</span><span class="sxs-lookup"><span data-stu-id="70b72-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="70b72-120">Správa přiřazení skupin zákazníků</span><span class="sxs-lookup"><span data-stu-id="70b72-120">Manage customer group assignments</span></span>

<span data-ttu-id="70b72-121">Každý zákazník může patřit do libovolného počtu skupin správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="70b72-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="70b72-122">Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu zákazníků.</span><span class="sxs-lookup"><span data-stu-id="70b72-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="70b72-123">Chcete-li zobrazit, přidat nebo odebrat zákazníky pro vybranou skupinu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70b72-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="70b72-124">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny zákazníků**.</span><span class="sxs-lookup"><span data-stu-id="70b72-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="70b72-125">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="70b72-125">Select the group to manage.</span></span>
1. <span data-ttu-id="70b72-126">V podokně akcí vyberte **Zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="70b72-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="70b72-127">Zobrazí se stránka **Skupiny správy rabatů** se seznamem zákazníků, kteří jsou již členy vybrané skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="70b72-128">Chcete-li do skupiny přidat nového zákazníka, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="70b72-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="70b72-129">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="70b72-130">**Účet zákazníka** - Vyberte ID účtu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="70b72-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="70b72-131">Chcete-li odebrat zákazníka ze skupiny, vyberte zákazníka a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="70b72-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="70b72-132">Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybraného zákazníka, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70b72-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="70b72-133">Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="70b72-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="70b72-134">Vyberte zákazníka, se kterým chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="70b72-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="70b72-135">V podokně akcí na kartě **Zákazník** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**.</span><span class="sxs-lookup"><span data-stu-id="70b72-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="70b72-136">Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraný zákazník patří.</span><span class="sxs-lookup"><span data-stu-id="70b72-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="70b72-137">Chcete-li do nové skupiny přidat zákazníka, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="70b72-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="70b72-138">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="70b72-139">**Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat zákazníka.</span><span class="sxs-lookup"><span data-stu-id="70b72-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="70b72-140">Chcete-li odebrat zákazníka ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="70b72-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="70b72-141">Skupiny dodavatelů správy rabatů</span><span class="sxs-lookup"><span data-stu-id="70b72-141">Rebate management vendor groups</span></span>

<span data-ttu-id="70b72-142">Výpočet pro skupinu dodavatelů se často vytváří pro skupinu míst dodání.</span><span class="sxs-lookup"><span data-stu-id="70b72-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="70b72-143">Tento typ výpočtu obvykle souvisí s rabatem.</span><span class="sxs-lookup"><span data-stu-id="70b72-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="70b72-144">Nastavení skupin dodavatele</span><span class="sxs-lookup"><span data-stu-id="70b72-144">Set up vendor groups</span></span>

<span data-ttu-id="70b72-145">Chcete-li pracovat se skupinami dodavatelů správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny dodavatelů**.</span><span class="sxs-lookup"><span data-stu-id="70b72-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="70b72-146">Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="70b72-147">U každé skupiny je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="70b72-148">**Skupina správy rabatů** – Zadejte jedinečný název skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="70b72-149">**Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.</span><span class="sxs-lookup"><span data-stu-id="70b72-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="70b72-150">Správa přiřazení skupin dodavatelů</span><span class="sxs-lookup"><span data-stu-id="70b72-150">Manage vendor group assignments</span></span>

<span data-ttu-id="70b72-151">Každý dodavatel může patřit do libovolného počtu skupin správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="70b72-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="70b72-152">Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="70b72-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="70b72-153">Chcete-li zobrazit, přidat nebo odebrat dodavatele pro vybranou skupinu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70b72-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="70b72-154">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny dodavatelů**.</span><span class="sxs-lookup"><span data-stu-id="70b72-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="70b72-155">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="70b72-155">Select the group to manage.</span></span>
1. <span data-ttu-id="70b72-156">V podokně akcí vyberte možnost **Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="70b72-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="70b72-157">Zobrazí se stránka **Skupiny správy rabatů** se seznamem dodavatelů, kteří jsou již členy vybrané skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="70b72-158">Chcete-li do skupiny přidat nového dodavatele, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="70b72-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="70b72-159">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="70b72-160">**Účet dodavatele** - Vyberte ID účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="70b72-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="70b72-161">Chcete-li odebrat dodavatele ze skupiny, vyberte dodavatele a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="70b72-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="70b72-162">Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybraného dodavatele, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70b72-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="70b72-163">Přejděte do části **Pohledávky \> Dodavatelé \> Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="70b72-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="70b72-164">Vyberte dodavatele, se kterým chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="70b72-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="70b72-165">V podokně akcí na kartě **Dodavatel** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**.</span><span class="sxs-lookup"><span data-stu-id="70b72-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="70b72-166">Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraný dodavatel patří.</span><span class="sxs-lookup"><span data-stu-id="70b72-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="70b72-167">Chcete-li do nové skupiny přidat dodavatele, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="70b72-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="70b72-168">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="70b72-169">**Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat dodavatele.</span><span class="sxs-lookup"><span data-stu-id="70b72-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="70b72-170">Chcete-li odebrat dodavatele ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="70b72-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="70b72-171">Skupiny rabatu pro položky</span><span class="sxs-lookup"><span data-stu-id="70b72-171">Item rebate groups</span></span>

<span data-ttu-id="70b72-172">Seskupením položek získáte větší flexibilitu při výpočtu rabatů a odpočtů.</span><span class="sxs-lookup"><span data-stu-id="70b72-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="70b72-173">Tento přístup je často efektivnějším způsobem, jak nastavit rabaty a odpočty pro zákazníky a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="70b72-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="70b72-174">Nastavit skupiny položek</span><span class="sxs-lookup"><span data-stu-id="70b72-174">Set up item groups</span></span>

<span data-ttu-id="70b72-175">Chcete-li pracovat se skupinami položek správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.</span><span class="sxs-lookup"><span data-stu-id="70b72-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="70b72-176">Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="70b72-177">U každé skupiny je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="70b72-178">**Skupina správy rabatů** – Zadejte jedinečný název skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="70b72-179">**Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.</span><span class="sxs-lookup"><span data-stu-id="70b72-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="70b72-180">Správa přiřazení skupin položek</span><span class="sxs-lookup"><span data-stu-id="70b72-180">Manage item group assignments</span></span>

<span data-ttu-id="70b72-181">Každá položka může patřit do libovolného počtu skupin správy rabatů.</span><span class="sxs-lookup"><span data-stu-id="70b72-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="70b72-182">Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu položek.</span><span class="sxs-lookup"><span data-stu-id="70b72-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="70b72-183">Můžete také přidat položky na základě vaší hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="70b72-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="70b72-184">Chcete-li zobrazit, přidat nebo odebrat položky pro vybranou skupinu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70b72-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="70b72-185">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.</span><span class="sxs-lookup"><span data-stu-id="70b72-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="70b72-186">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="70b72-186">Select the group to manage.</span></span>
1. <span data-ttu-id="70b72-187">V podokně akcí zvolte **Položky**.</span><span class="sxs-lookup"><span data-stu-id="70b72-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="70b72-188">Zobrazí se stránka **Skupiny správy rabatů** se seznamem položek, kteří jsou již členy vybrané skupiny.</span><span class="sxs-lookup"><span data-stu-id="70b72-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="70b72-189">Chcete-li do skupiny přidat novou položku, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="70b72-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="70b72-190">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="70b72-191">**Účet položky** - Vyberte ID účtu položky.</span><span class="sxs-lookup"><span data-stu-id="70b72-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="70b72-192">Chcete-li odebrat položku ze skupiny, vyberte položku a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="70b72-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="70b72-193">Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybranéou položku, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70b72-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="70b72-194">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="70b72-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="70b72-195">Vyberte položku, se kterou chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="70b72-195">Select the item to work with.</span></span>
1. <span data-ttu-id="70b72-196">V podokně akcí na kartě **Produkt** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**.</span><span class="sxs-lookup"><span data-stu-id="70b72-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="70b72-197">Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraná položka patří.</span><span class="sxs-lookup"><span data-stu-id="70b72-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="70b72-198">Chcete-li do nové skupiny přidat položku, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="70b72-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="70b72-199">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="70b72-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="70b72-200">**Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat položku.</span><span class="sxs-lookup"><span data-stu-id="70b72-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="70b72-201">Chcete-li odebrat položku ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="70b72-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="70b72-202">Chcete-li přidat položky do skupiny na základě vaší hierarchie kategorií, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70b72-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="70b72-203">Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.</span><span class="sxs-lookup"><span data-stu-id="70b72-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="70b72-204">Vyberte skupinu, kterou chcete spravovat.</span><span class="sxs-lookup"><span data-stu-id="70b72-204">Select the group to manage.</span></span>
1. <span data-ttu-id="70b72-205">V podokně akcí zvolte **Přidat položky**.</span><span class="sxs-lookup"><span data-stu-id="70b72-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="70b72-206">V dialogovém okně **Přidat položky** v poli **Hierarchie kategorií** vyberte kategorii nejvyšší úrovně.</span><span class="sxs-lookup"><span data-stu-id="70b72-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="70b72-207">V levém podokně se otevře hierarchie položek.</span><span class="sxs-lookup"><span data-stu-id="70b72-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="70b72-208">Vyberte úroveň hierarchie, kterou hledáte.</span><span class="sxs-lookup"><span data-stu-id="70b72-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="70b72-209">Položky z vybrané hierarchie a úrovně hierarchie jsou nyní uvedeny v pravém podokně.</span><span class="sxs-lookup"><span data-stu-id="70b72-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="70b72-210">Při práci s podoknem postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="70b72-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="70b72-211">Zaškrtněte políčko pro každou položku, kterou chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="70b72-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="70b72-212">Zaškrtnutím políčka v záhlaví mřížky vyberte všechny uvedené položky.</span><span class="sxs-lookup"><span data-stu-id="70b72-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="70b72-213">Vyberte tlačítko **Zobrazit vybrané** pro filtrování mřížky tak, aby zobrazovala pouze položky, které jste dosud vybrali.</span><span class="sxs-lookup"><span data-stu-id="70b72-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="70b72-214">Opětovným stisknutím tlačítka se vrátíte na úplný seznam.</span><span class="sxs-lookup"><span data-stu-id="70b72-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="70b72-215">Vyberte **OK** a použijte výběr položek na vybranou skupinu.</span><span class="sxs-lookup"><span data-stu-id="70b72-215">Select **OK** to apply your item selection to the selected group.</span></span>
