---
title: Nastavit sklad
description: Toto téma popisuje, jak nastavit sklad, který má být použit s novým kanálem v Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800488"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="c8408-103">Nastavit sklad</span><span class="sxs-lookup"><span data-stu-id="c8408-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8408-104">Toto téma popisuje, jak nastavit sklad, který má být použit s novým kanálem v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c8408-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c8408-105">Ke každému obchodnímu kanálu je nutné přidružit konfigurovaný sklad.</span><span class="sxs-lookup"><span data-stu-id="c8408-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="c8408-106">Následující postupy poskytují minimální konfiguraci nutnou k nastavení skladu pro obchodní kanál.</span><span class="sxs-lookup"><span data-stu-id="c8408-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="c8408-107">Další informace týkající se nastavení skladu naleznete v [Přehledu řízení skladu](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c8408-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="c8408-108">Konfigurace místa skladu</span><span class="sxs-lookup"><span data-stu-id="c8408-108">Configure a warehouse site</span></span>

<span data-ttu-id="c8408-109">Před nastavením skladu je nutné nakonfigurovat místo skladu.</span><span class="sxs-lookup"><span data-stu-id="c8408-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="c8408-110">Chcete-li konfigurovat místo skladu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="c8408-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="c8408-111">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Místa**.</span><span class="sxs-lookup"><span data-stu-id="c8408-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="c8408-112">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c8408-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8408-113">Zadejte hodnotu do pole **Místo**.</span><span class="sxs-lookup"><span data-stu-id="c8408-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="c8408-114">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="c8408-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="c8408-115">V části **Obecné** nastavte příslušné **Časové pásmo**.</span><span class="sxs-lookup"><span data-stu-id="c8408-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="c8408-116">Do sekce **Addresy** zadejte adresu.</span><span class="sxs-lookup"><span data-stu-id="c8408-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="c8408-117">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8408-118">Následující obrázek znázorňuje příklad místa skladu.</span><span class="sxs-lookup"><span data-stu-id="c8408-118">The following image shows an example warehouse site.</span></span>

![Příklad místa skladu](media/warehouse-site.png)

## <a name="set-up-a-warehouse&quot;></a><span data-ttu-id=&quot;c8408-120&quot;>Nastavit sklad</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-120&quot;>Set up a warehouse</span></span>

<span data-ttu-id=&quot;c8408-121&quot;>Chcete-li nastavit sklad, postupujte následujícím způsobem.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-121&quot;>To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id=&quot;c8408-122&quot;>V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-122&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id=&quot;c8408-123&quot;>V podokně akcí zvolte **Nový**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-123&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;c8408-124&quot;>V poli **Sklad** zadejte hodnotu.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-124&quot;>In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id=&quot;c8408-125&quot;>Pokud se jedná o mapování 1:1 na obchod, zvažte použití názvu obchodu nebo názvu místního distribučního střediska.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-125&quot;>If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id=&quot;c8408-126&quot;>Zadejte hodnotu do pole **Název**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-126&quot;>In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id=&quot;c8408-127&quot;>V rozevíracím seznamu **Místo** vyberte místo skladu, které bylo vytvořeno dříve.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-127&quot;>In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id=&quot;c8408-128&quot;>V poli **Typ** vyberte **Výchozí**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-128&quot;>In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id=&quot;c8408-129&quot;>Chcete-li nastavit **Karanténní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Karanténa**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-129&quot;>If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id=&quot;c8408-130&quot;>Chcete-li nastavit **Tranzitní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Tranzitní**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-130&quot;>If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id=&quot;c8408-131&quot;>V podokně akcí vyberte **Uložit**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-131&quot;>On the action pane, select **Save**.</span></span>

## <a name=&quot;set-up-inventory-aisles&quot;></a><span data-ttu-id=&quot;c8408-132&quot;>Nastavit skladové uličky</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-132&quot;>Set up inventory aisles</span></span>

<span data-ttu-id=&quot;c8408-133&quot;>Chcete-li nastavit skladové uličky, postupujte následujícím způsobem.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-133&quot;>To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id=&quot;c8408-134&quot;>V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Nastavení umístění \> Skladové uličky**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-134&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id=&quot;c8408-135&quot;>V podokně akcí zvolte **Nový**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-135&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;c8408-136&quot;>V rozevíracím seznamu **Sklad** vyberte místo skladu, které bylo vytvořeno dříve.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c8408-136&quot;>In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id=&quot;c8408-137&quot;>Do pole **Ulička** zadejte název (například &quot;def").</span><span class="sxs-lookup"><span data-stu-id="c8408-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="c8408-138">Do pole **Název** zadejte název (například "Výchozí ulička").</span><span class="sxs-lookup"><span data-stu-id="c8408-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="c8408-139">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="c8408-140">Nastavit skladová místa ve skladu</span><span class="sxs-lookup"><span data-stu-id="c8408-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="c8408-141">Chcete-li nastavit umístění skladových zásob pro standardní, poškozené a vrácené zásoby, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="c8408-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="c8408-142">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="c8408-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="c8408-143">Vyberte dříve vytvořený sklad.</span><span class="sxs-lookup"><span data-stu-id="c8408-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="c8408-144">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="c8408-145">V podokně akcí vyberte **Sklad** a pak vyberte **Skladové místo**.</span><span class="sxs-lookup"><span data-stu-id="c8408-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="c8408-146">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c8408-146">On the action pane, select **New**.</span></span> <span data-ttu-id="c8408-147">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="c8408-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="c8408-148">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="c8408-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="c8408-149">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="c8408-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="c8408-150">Do pole **Umístění** zadejte název skladu.</span><span class="sxs-lookup"><span data-stu-id="c8408-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="c8408-151">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="c8408-152">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c8408-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="c8408-153">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="c8408-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="c8408-154">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="c8408-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="c8408-155">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="c8408-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="c8408-156">V poli **Umístění** zadejte "Poškozeno".</span><span class="sxs-lookup"><span data-stu-id="c8408-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="c8408-157">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="c8408-158">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c8408-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="c8408-159">Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.</span><span class="sxs-lookup"><span data-stu-id="c8408-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="c8408-160">Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="c8408-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="c8408-161">Nastavte **Ruční aktualizaci** na **Ano**</span><span class="sxs-lookup"><span data-stu-id="c8408-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="c8408-162">V poli **Umístění** zadejte "Vrácené".</span><span class="sxs-lookup"><span data-stu-id="c8408-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="c8408-163">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="c8408-164">Na následujícím obrázku je znázorněno nastavení skladového místa San Francisco.</span><span class="sxs-lookup"><span data-stu-id="c8408-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Příklad nastavení skladového místa](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="c8408-166">Dokončené nastavení skladu</span><span class="sxs-lookup"><span data-stu-id="c8408-166">Complete warehouse setup</span></span>

<span data-ttu-id="c8408-167">Abyste dokončili nastavení skladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c8408-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="c8408-168">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.</span><span class="sxs-lookup"><span data-stu-id="c8408-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="c8408-169">Vyberte dříve vytvořený sklad.</span><span class="sxs-lookup"><span data-stu-id="c8408-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="c8408-170">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="c8408-171">V **Řízení zásob a skladu**:</span><span class="sxs-lookup"><span data-stu-id="c8408-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="c8408-172">Nastavte **Výchozí umístění příjemky** na výchozí místo, které bylo vytvořeno výše.</span><span class="sxs-lookup"><span data-stu-id="c8408-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="c8408-173">Vyberte **Výchozí skladové místo výdejů** na výchozí místo, které bylo vytvořeno výše.</span><span class="sxs-lookup"><span data-stu-id="c8408-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="c8408-174">V části **Adresy** zadejte adresu skladu.</span><span class="sxs-lookup"><span data-stu-id="c8408-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="c8408-175">V části **Maloobchod**:</span><span class="sxs-lookup"><span data-stu-id="c8408-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="c8408-176">Do pole **Výchozí místo vrácení** zadejte umístění vrácení, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="c8408-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="c8408-177">Nastavit **Obchod** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="c8408-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="c8408-178">Nastavte **Hmotnost** na **1.00**.</span><span class="sxs-lookup"><span data-stu-id="c8408-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="c8408-179">Do pole **Dimenze úložiště** zadejte výchozí umístění, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="c8408-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="c8408-180">V části **Sklad** nastavte **Záporný fyzický sklad** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="c8408-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="c8408-181">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c8408-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8408-182">Následující obrázek ukazuje podrobnosti pro konfigurovaný sklad.</span><span class="sxs-lookup"><span data-stu-id="c8408-182">The following image shows details for a configured warehouse.</span></span>

![Příklad nakonfigurovaného skladu](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="c8408-184">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c8408-184">Additional resources</span></span>

[<span data-ttu-id="c8408-185">Přehled řízení skladu</span><span class="sxs-lookup"><span data-stu-id="c8408-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c8408-186">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="c8408-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c8408-187">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="c8408-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="c8408-188">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="c8408-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="c8408-189">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="c8408-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="c8408-190">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="c8408-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
