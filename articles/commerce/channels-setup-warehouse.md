---
title: Nastavit sklad
description: Toto téma popisuje, jak nastavit sklad, který má být použit s novým kanálem v Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993646"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="77f0c-103">Nastavit sklad</span><span class="sxs-lookup"><span data-stu-id="77f0c-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="77f0c-104">Toto téma popisuje, jak nastavit sklad, který má být použit s novým kanálem v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="77f0c-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="77f0c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="77f0c-105">Overview</span></span>

<span data-ttu-id="77f0c-106">Ke každému obchodnímu kanálu je nutné přidružit konfigurovaný sklad.</span><span class="sxs-lookup"><span data-stu-id="77f0c-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="77f0c-107">Následující postupy poskytují minimální konfiguraci nutnou k nastavení skladu pro obchodní kanál.</span><span class="sxs-lookup"><span data-stu-id="77f0c-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="77f0c-108">Další informace týkající se nastavení skladu naleznete v [Přehledu řízení skladu](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="77f0c-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="77f0c-109">Konfigurace místa skladu</span><span class="sxs-lookup"><span data-stu-id="77f0c-109">Configure a warehouse site</span></span>

<span data-ttu-id="77f0c-110">Před nastavením skladu je nutné nakonfigurovat místo skladu.</span><span class="sxs-lookup"><span data-stu-id="77f0c-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="77f0c-111">Chcete-li konfigurovat místo skladu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="77f0c-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="77f0c-112">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Místa**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="77f0c-113">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="77f0c-114">Zadejte hodnotu do pole **Místo**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="77f0c-115">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="77f0c-116">V části **Obecné** nastavte příslušné **Časové pásmo**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="77f0c-117">Do sekce **Addresy** zadejte adresu.</span><span class="sxs-lookup"><span data-stu-id="77f0c-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="77f0c-118">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="77f0c-119">Následující obrázek znázorňuje příklad místa skladu.</span><span class="sxs-lookup"><span data-stu-id="77f0c-119">The following image shows an example warehouse site.</span></span>

![Příklad místa skladu](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="77f0c-121">Nastavit sklad</span><span class="sxs-lookup"><span data-stu-id="77f0c-121">Set up a warehouse</span></span>

<span data-ttu-id="77f0c-122">Chcete-li nastavit sklad, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="77f0c-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="77f0c-123">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="77f0c-124">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="77f0c-125">V poli **Sklad** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="77f0c-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="77f0c-126">Pokud se jedná o mapování 1:1 na obchod, zvažte použití názvu obchodu nebo názvu místního distribučního střediska.</span><span class="sxs-lookup"><span data-stu-id="77f0c-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="77f0c-127">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="77f0c-128">V rozevíracím seznamu **Místo** vyberte místo skladu, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="77f0c-129">V poli **Typ** vyberte **Výchozí**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="77f0c-130">Chcete-li nastavit **Karanténní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Karanténa**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="77f0c-131">Chcete-li nastavit **Tranzitní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Tranzitní**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="77f0c-132">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="77f0c-133">Nastavit skladové uličky</span><span class="sxs-lookup"><span data-stu-id="77f0c-133">Set up inventory aisles</span></span>

<span data-ttu-id="77f0c-134">Chcete-li nastavit skladové uličky, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="77f0c-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="77f0c-135">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Nastavení umístění \> Skladové uličky**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="77f0c-136">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="77f0c-137">V rozevíracím seznamu **Sklad** vyberte místo skladu, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="77f0c-138">Do pole **Ulička** zadejte název (například "def").</span><span class="sxs-lookup"><span data-stu-id="77f0c-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="77f0c-139">Do pole **Název** zadejte název (například "Výchozí ulička").</span><span class="sxs-lookup"><span data-stu-id="77f0c-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="77f0c-140">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="77f0c-141">Nastavit skladová místa ve skladu</span><span class="sxs-lookup"><span data-stu-id="77f0c-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="77f0c-142">Chcete-li nastavit umístění skladových zásob pro standardní, poškozené a vrácené zásoby, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="77f0c-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="77f0c-143">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="77f0c-144">Vyberte dříve vytvořený sklad.</span><span class="sxs-lookup"><span data-stu-id="77f0c-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="77f0c-145">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="77f0c-146">V podokně akcí vyberte **Sklad** a pak vyberte **Skladové místo**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="77f0c-147">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-147">On the action pane, select **New**.</span></span> <span data-ttu-id="77f0c-148">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="77f0c-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="77f0c-149">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="77f0c-150">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="77f0c-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="77f0c-151">Do pole **Umístění** zadejte název skladu.</span><span class="sxs-lookup"><span data-stu-id="77f0c-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="77f0c-152">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="77f0c-153">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="77f0c-154">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="77f0c-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="77f0c-155">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="77f0c-156">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="77f0c-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="77f0c-157">V poli **Umístění** zadejte "Poškozeno".</span><span class="sxs-lookup"><span data-stu-id="77f0c-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="77f0c-158">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="77f0c-159">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="77f0c-160">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="77f0c-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="77f0c-161">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="77f0c-162">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="77f0c-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="77f0c-163">V poli **Umístění** zadejte "Vrácené".</span><span class="sxs-lookup"><span data-stu-id="77f0c-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="77f0c-164">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="77f0c-165">Na následujícím obrázku je znázorněno nastavení skladového místa San Francisco.</span><span class="sxs-lookup"><span data-stu-id="77f0c-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Příklad nastavení skladového místa](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="77f0c-167">Dokončené nastavení skladu</span><span class="sxs-lookup"><span data-stu-id="77f0c-167">Complete warehouse setup</span></span>

<span data-ttu-id="77f0c-168">Abyste dokončili nastavení skladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="77f0c-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="77f0c-169">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="77f0c-170">Vyberte dříve vytvořený sklad.</span><span class="sxs-lookup"><span data-stu-id="77f0c-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="77f0c-171">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="77f0c-172">V **Řízení zásob a skladu**:</span><span class="sxs-lookup"><span data-stu-id="77f0c-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="77f0c-173">Nastavte **Výchozí umístění příjemky** na výchozí místo, které bylo vytvořeno výše.</span><span class="sxs-lookup"><span data-stu-id="77f0c-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="77f0c-174">Vyberte **Výchozí skladové místo výdejů** na výchozí místo, které bylo vytvořeno výše.</span><span class="sxs-lookup"><span data-stu-id="77f0c-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="77f0c-175">V části **Adresy** zadejte adresu skladu.</span><span class="sxs-lookup"><span data-stu-id="77f0c-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="77f0c-176">V části **Maloobchod**:</span><span class="sxs-lookup"><span data-stu-id="77f0c-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="77f0c-177">Do pole **Výchozí místo vrácení** zadejte umístění vrácení, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="77f0c-178">Nastavit **Obchod** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="77f0c-179">Nastavte **Hmotnost** na **1.00**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="77f0c-180">Do pole **Dimenze úložiště** zadejte výchozí umístění, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="77f0c-181">V části **Sklad** nastavte **Záporný fyzický sklad** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="77f0c-182">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="77f0c-183">Následující obrázek ukazuje podrobnosti pro konfigurovaný sklad.</span><span class="sxs-lookup"><span data-stu-id="77f0c-183">The following image shows details for a configured warehouse.</span></span>

![Příklad nakonfigurovaného skladu](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="77f0c-185">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="77f0c-185">Additional resources</span></span>

[<span data-ttu-id="77f0c-186">Přehled řízení skladu</span><span class="sxs-lookup"><span data-stu-id="77f0c-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="77f0c-187">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="77f0c-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="77f0c-188">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="77f0c-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="77f0c-189">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="77f0c-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="77f0c-190">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="77f0c-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="77f0c-191">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="77f0c-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





