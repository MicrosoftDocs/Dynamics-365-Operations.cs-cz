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
ms.openlocfilehash: 772c7584549b30a34e371a7911131edc01214ed8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477627"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="89ff4-103">Nastavit sklad</span><span class="sxs-lookup"><span data-stu-id="89ff4-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="89ff4-104">Toto téma popisuje, jak nastavit sklad, který má být použit s novým kanálem v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="89ff4-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="89ff4-105">Ke každému obchodnímu kanálu je nutné přidružit konfigurovaný sklad.</span><span class="sxs-lookup"><span data-stu-id="89ff4-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="89ff4-106">Následující postupy poskytují minimální konfiguraci nutnou k nastavení skladu pro obchodní kanál.</span><span class="sxs-lookup"><span data-stu-id="89ff4-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="89ff4-107">Další informace týkající se nastavení skladu naleznete v [Přehledu řízení skladu](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="89ff4-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="89ff4-108">Konfigurace místa skladu</span><span class="sxs-lookup"><span data-stu-id="89ff4-108">Configure a warehouse site</span></span>

<span data-ttu-id="89ff4-109">Před nastavením skladu je nutné nakonfigurovat místo skladu.</span><span class="sxs-lookup"><span data-stu-id="89ff4-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="89ff4-110">Chcete-li konfigurovat místo skladu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="89ff4-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="89ff4-111">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Místa**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="89ff4-112">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="89ff4-113">Zadejte hodnotu do pole **Místo**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="89ff4-114">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="89ff4-115">V části **Obecné** nastavte příslušné **Časové pásmo**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="89ff4-116">Do sekce **Addresy** zadejte adresu.</span><span class="sxs-lookup"><span data-stu-id="89ff4-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="89ff4-117">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="89ff4-118">Následující obrázek znázorňuje příklad místa skladu.</span><span class="sxs-lookup"><span data-stu-id="89ff4-118">The following image shows an example warehouse site.</span></span>

![Příklad místa skladu](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="89ff4-120">Nastavit sklad</span><span class="sxs-lookup"><span data-stu-id="89ff4-120">Set up a warehouse</span></span>

<span data-ttu-id="89ff4-121">Chcete-li nastavit sklad, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="89ff4-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="89ff4-122">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="89ff4-123">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="89ff4-124">V poli **Sklad** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="89ff4-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="89ff4-125">Pokud se jedná o mapování 1:1 na obchod, zvažte použití názvu obchodu nebo názvu místního distribučního střediska.</span><span class="sxs-lookup"><span data-stu-id="89ff4-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="89ff4-126">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="89ff4-127">V rozevíracím seznamu **Místo** vyberte místo skladu, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="89ff4-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="89ff4-128">V poli **Typ** vyberte **Výchozí**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="89ff4-129">Chcete-li nastavit **Karanténní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Karanténa**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="89ff4-130">Chcete-li nastavit **Tranzitní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Tranzitní**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="89ff4-131">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="89ff4-132">Nastavit skladové uličky</span><span class="sxs-lookup"><span data-stu-id="89ff4-132">Set up inventory aisles</span></span>

<span data-ttu-id="89ff4-133">Chcete-li nastavit skladové uličky, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="89ff4-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="89ff4-134">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Nastavení umístění \> Skladové uličky**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="89ff4-135">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="89ff4-136">V rozevíracím seznamu **Sklad** vyberte místo skladu, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="89ff4-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="89ff4-137">Do pole **Ulička** zadejte název (například "def").</span><span class="sxs-lookup"><span data-stu-id="89ff4-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="89ff4-138">Do pole **Název** zadejte název (například "Výchozí ulička").</span><span class="sxs-lookup"><span data-stu-id="89ff4-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="89ff4-139">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="89ff4-140">Nastavit skladová místa ve skladu</span><span class="sxs-lookup"><span data-stu-id="89ff4-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="89ff4-141">Chcete-li nastavit umístění skladových zásob pro standardní, poškozené a vrácené zásoby, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="89ff4-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="89ff4-142">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="89ff4-143">Vyberte dříve vytvořený sklad.</span><span class="sxs-lookup"><span data-stu-id="89ff4-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="89ff4-144">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="89ff4-145">V podokně akcí vyberte **Sklad** a pak vyberte **Skladové místo**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="89ff4-146">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-146">On the action pane, select **New**.</span></span> <span data-ttu-id="89ff4-147">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="89ff4-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="89ff4-148">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="89ff4-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="89ff4-149">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="89ff4-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="89ff4-150">Do pole **Umístění** zadejte název skladu.</span><span class="sxs-lookup"><span data-stu-id="89ff4-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="89ff4-151">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="89ff4-152">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="89ff4-153">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="89ff4-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="89ff4-154">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="89ff4-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="89ff4-155">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="89ff4-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="89ff4-156">V poli **Umístění** zadejte "Poškozeno".</span><span class="sxs-lookup"><span data-stu-id="89ff4-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="89ff4-157">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="89ff4-158">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="89ff4-159">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="89ff4-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="89ff4-160">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="89ff4-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="89ff4-161">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="89ff4-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="89ff4-162">V poli **Umístění** zadejte "Vrácené".</span><span class="sxs-lookup"><span data-stu-id="89ff4-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="89ff4-163">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="89ff4-164">Na následujícím obrázku je znázorněno nastavení skladového místa San Francisco.</span><span class="sxs-lookup"><span data-stu-id="89ff4-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Příklad nastavení skladového místa](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="89ff4-166">Dokončené nastavení skladu</span><span class="sxs-lookup"><span data-stu-id="89ff4-166">Complete warehouse setup</span></span>

<span data-ttu-id="89ff4-167">Abyste dokončili nastavení skladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="89ff4-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="89ff4-168">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="89ff4-169">Vyberte dříve vytvořený sklad.</span><span class="sxs-lookup"><span data-stu-id="89ff4-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="89ff4-170">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="89ff4-171">V **Řízení zásob a skladu**:</span><span class="sxs-lookup"><span data-stu-id="89ff4-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="89ff4-172">Nastavte **Výchozí umístění příjemky** na výchozí místo, které bylo vytvořeno výše.</span><span class="sxs-lookup"><span data-stu-id="89ff4-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="89ff4-173">Vyberte **Výchozí skladové místo výdejů** na výchozí místo, které bylo vytvořeno výše.</span><span class="sxs-lookup"><span data-stu-id="89ff4-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="89ff4-174">V části **Adresy** zadejte adresu skladu.</span><span class="sxs-lookup"><span data-stu-id="89ff4-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="89ff4-175">V části **Maloobchod**:</span><span class="sxs-lookup"><span data-stu-id="89ff4-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="89ff4-176">Do pole **Výchozí místo vrácení** zadejte umístění vrácení, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="89ff4-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="89ff4-177">Nastavit **Obchod** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="89ff4-178">Nastavte **Hmotnost** na **1.00**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="89ff4-179">Do pole **Dimenze úložiště** zadejte výchozí umístění, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="89ff4-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="89ff4-180">V části **Sklad** nastavte **Záporný fyzický sklad** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="89ff4-181">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89ff4-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="89ff4-182">Následující obrázek ukazuje podrobnosti pro konfigurovaný sklad.</span><span class="sxs-lookup"><span data-stu-id="89ff4-182">The following image shows details for a configured warehouse.</span></span>

![Příklad nakonfigurovaného skladu](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="89ff4-184">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="89ff4-184">Additional resources</span></span>

[<span data-ttu-id="89ff4-185">Přehled řízení skladu</span><span class="sxs-lookup"><span data-stu-id="89ff4-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="89ff4-186">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="89ff4-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="89ff4-187">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="89ff4-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="89ff4-188">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="89ff4-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="89ff4-189">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="89ff4-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="89ff4-190">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="89ff4-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
