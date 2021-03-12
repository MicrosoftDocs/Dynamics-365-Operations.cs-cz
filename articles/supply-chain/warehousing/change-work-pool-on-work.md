---
title: Změnit fond práce u práce
description: Toto téma vysvětluje, jak můžete pomocí tlačítka Změnit fond práce pro pracovní položky změnit fond práce stávající práce.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001142"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="f396d-103">Změnit fond práce u práce</span><span class="sxs-lookup"><span data-stu-id="f396d-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f396d-104">Fondy práce můžete použít k uspořádání práce do skupin.</span><span class="sxs-lookup"><span data-stu-id="f396d-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="f396d-105">Můžete například vytvořit fond práce pro klasifikaci práce, ke které dochází v určitém skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="f396d-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="f396d-106">Funkce *Změna fondu práce v práci* přidá tlačítko **Změna fondu práce** do podokna akcí pro pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="f396d-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="f396d-107">Proto mohou vedoucí skladu snadno změnit fond práce stávající práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="f396d-108">Tato funkce umožňuje manažerům rychle reagovat na změny ve skladu ve skladu a pomáhá zlepšit jejich schopnost přizpůsobit se měnícím se situacím a potřebě převést práci do jiného pracovního fondu.</span><span class="sxs-lookup"><span data-stu-id="f396d-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="f396d-109">Zapněte funkci Změnit fond práce pro práci</span><span class="sxs-lookup"><span data-stu-id="f396d-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="f396d-110">Než začnete tuto funkci nastavovat nebo používat, musíte se ujistit, že je ve vašem systému k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f396d-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="f396d-111">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="f396d-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f396d-112">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="f396d-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f396d-113">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="f396d-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f396d-114">**Název funkce:** *Změnit fond práce pro práci*</span><span class="sxs-lookup"><span data-stu-id="f396d-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="f396d-115">Nastavte funkci Změnit fond práce pro práci</span><span class="sxs-lookup"><span data-stu-id="f396d-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="f396d-116">Chcete-li tuto funkci používat, musíte mít nastaveny některé fondy práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="f396d-117">Můžete také nastavit své pracovní šablony, aby automaticky přiřadily fond.</span><span class="sxs-lookup"><span data-stu-id="f396d-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="f396d-118">Pokud chcete využít scénář uvedený v tomto tématu jako příklad, nastavte systém podle popisu v této části.</span><span class="sxs-lookup"><span data-stu-id="f396d-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="f396d-119">Nastavení fondů práce</span><span class="sxs-lookup"><span data-stu-id="f396d-119">Set up work pools</span></span>

<span data-ttu-id="f396d-120">Fondy práce umožňují organizovat pracovní položky podle typu.</span><span class="sxs-lookup"><span data-stu-id="f396d-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="f396d-121">Chcete-li pracovat s funkcí *Změna fondu práce pro práci*, musíte mít k dispozici alespoň dva fondy práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="f396d-122">Chcete-li zobrazit a přidat fondy práce, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="f396d-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="f396d-123">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Fondy práce**.</span><span class="sxs-lookup"><span data-stu-id="f396d-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="f396d-124">Pokud pracujete s demo daty společnosti **USMF** a budete pokračovat v příkladu scénáře dále v tomto tématu, přidejte dva fondy práce, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f396d-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="f396d-125">Fond práce 1:</span><span class="sxs-lookup"><span data-stu-id="f396d-125">Work pool 1:</span></span>

        - <span data-ttu-id="f396d-126">**ID fondu práce:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="f396d-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="f396d-127">**Popis:** *Webový obchod*</span><span class="sxs-lookup"><span data-stu-id="f396d-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="f396d-128">Fond práce 2:</span><span class="sxs-lookup"><span data-stu-id="f396d-128">Work pool 2:</span></span>

        - <span data-ttu-id="f396d-129">**ID fondu práce:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="f396d-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="f396d-130">**Popis:** *Kontaktní středisko*</span><span class="sxs-lookup"><span data-stu-id="f396d-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="f396d-131">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f396d-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="f396d-132">Nastavit šablony práce</span><span class="sxs-lookup"><span data-stu-id="f396d-132">Set up work templates</span></span>

<span data-ttu-id="f396d-133">Pro každou ze svých pracovních šablon můžete podle potřeby nastavit výchozí fond práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="f396d-134">Pro každou příslušnou šablonu přiřadíte fond práce ve sloupci **ID fondu práce**.</span><span class="sxs-lookup"><span data-stu-id="f396d-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="f396d-135">V tomto případě všechny pracovní položky, které jsou generovány pomocí dané šablony, automaticky zdědí přiřazený fond práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="f396d-136">Pokud pracujete s demo daty společnosti **USMF** a budete pokračovat v příkladu scénáře dále v tomto tématu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="f396d-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="f396d-137">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="f396d-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="f396d-138">V podokně Akce vyberte možnost **Upravit**, tím přepnete stránku režimu úprav.</span><span class="sxs-lookup"><span data-stu-id="f396d-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="f396d-139">Upravte šablonu nastavením následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="f396d-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="f396d-140">**Pracovní šablona:** *62 výdejů do balení*</span><span class="sxs-lookup"><span data-stu-id="f396d-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="f396d-141">**ID fondu práce:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="f396d-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="f396d-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f396d-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f396d-143">Příklad</span><span class="sxs-lookup"><span data-stu-id="f396d-143">Example scenario</span></span>

<span data-ttu-id="f396d-144">Tento scénář ukazuje, jak změnit tok zpracování pro existující pracovní položku změnou jejího fondu práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="f396d-145">Používá demo data společnosti **USMF** a nastavení, která byla navržena dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="f396d-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="f396d-146">Vytvořte prodejní objednávku a uvolněte ji do skladu</span><span class="sxs-lookup"><span data-stu-id="f396d-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="f396d-147">Potvrďte, že je k dispozici dostatek zásob na skladě pro položky *A0001* a *A0002* ve skladu *62*.</span><span class="sxs-lookup"><span data-stu-id="f396d-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="f396d-148">Přejděte na **Řízení zásob \> Dotazy a sestavy \> Seznam na skladě** a upravte filtry podle obrázku:</span><span class="sxs-lookup"><span data-stu-id="f396d-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="f396d-149">Hodnota **Sklad** začíná na *62*.</span><span class="sxs-lookup"><span data-stu-id="f396d-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="f396d-150">Hodnota **Číslo položky** je buď *A001* nebo *A002*.</span><span class="sxs-lookup"><span data-stu-id="f396d-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="f396d-151">Demo data by měla množství 10.</span><span class="sxs-lookup"><span data-stu-id="f396d-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="f396d-152">Dále musíte vytvořit prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="f396d-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="f396d-153">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f396d-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f396d-154">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f396d-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f396d-155">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="f396d-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f396d-156">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f396d-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f396d-157">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="f396d-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f396d-158">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="f396d-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="f396d-159">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="f396d-159">The new sales order is opened.</span></span> <span data-ttu-id="f396d-160">Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f396d-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f396d-161">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="f396d-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="f396d-162">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f396d-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="f396d-163">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="f396d-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="f396d-164">V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="f396d-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f396d-165">Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.</span><span class="sxs-lookup"><span data-stu-id="f396d-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="f396d-166">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f396d-166">Close the page.</span></span>
1. <span data-ttu-id="f396d-167">Na záložce s náhledem **Řádky prodejní objednávky** možnost **Přidat řádek**. Přidá se další řádek do vaší prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f396d-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="f396d-168">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="f396d-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="f396d-169">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f396d-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="f396d-170">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="f396d-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="f396d-171">V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="f396d-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f396d-172">Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.</span><span class="sxs-lookup"><span data-stu-id="f396d-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="f396d-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f396d-173">Close the page.</span></span>
1. <span data-ttu-id="f396d-174">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="f396d-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f396d-175">Zobrazí se informační zprávy určující ID vlny a ID dodávky, jež byly vytvořeny z uvolnění.</span><span class="sxs-lookup"><span data-stu-id="f396d-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="f396d-176">Poznamenejte si ID vlny.</span><span class="sxs-lookup"><span data-stu-id="f396d-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="f396d-177">Zkontrolujte odchozí vlnu</span><span class="sxs-lookup"><span data-stu-id="f396d-177">Review the outbound wave</span></span>

1. <span data-ttu-id="f396d-178">Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.</span><span class="sxs-lookup"><span data-stu-id="f396d-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="f396d-179">V mřížce vyhledejte ID vlny vytvořené uvolněním prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f396d-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="f396d-180">Chcete-li zobrazit podrobnosti, vyberte ID vlny.</span><span class="sxs-lookup"><span data-stu-id="f396d-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="f396d-181">Na pevné záložce **Řádky vlny** se ujistěte, že se u prodejní objednávky zobrazuje ID zásilky.</span><span class="sxs-lookup"><span data-stu-id="f396d-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="f396d-182">Pokud je možnost **Zpracovat vlnu při uvolnění do skladu** nastavena na *Ne* v nastavení šablony přepravní vlny, musíte vlnu ručně zpracovat výběrem **Zpracovat** na kartě **Vlna** v podokně akcí pro vytvoření práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="f396d-183">Ujistěte se, že vlna byla zpracována.</span><span class="sxs-lookup"><span data-stu-id="f396d-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="f396d-184">Toto zpracování vytvoří požadovanou práci.</span><span class="sxs-lookup"><span data-stu-id="f396d-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="f396d-185">Zobrazit podrobnosti o práci a změnit fond práce</span><span class="sxs-lookup"><span data-stu-id="f396d-185">View work details and change the work pool</span></span>

<span data-ttu-id="f396d-186">Můžete použít stránku **Podrobnosti o práci** pro zobrazení vytvořené práce a pro správu fondu práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="f396d-187">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="f396d-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="f396d-188">Vyberte řádek právě vytvořené práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="f396d-189">Ve sloupci **Číslo objednávky** se zobrazí číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f396d-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="f396d-190">Pole **ID fondu práce** bude nastaveno na ID fondu práce, které bylo nastaveno v pracovní šabloně.</span><span class="sxs-lookup"><span data-stu-id="f396d-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="f396d-191">Pokud nevidíte pole **ID fondu práce**, přidejte sloupec do mřížky a poté stránku obnovte.</span><span class="sxs-lookup"><span data-stu-id="f396d-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="f396d-192">Chcete-li změnit fond práce, který je spojen s ID práce, v podokně akcí na kartě **Práce** vyberte **Změnit ID fondu práce**.</span><span class="sxs-lookup"><span data-stu-id="f396d-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="f396d-193">V dialogovém okně **Změna fondu práce** na pevné záložce **Parametry** v poli **ID fondu práce** vyberte pole *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="f396d-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="f396d-194">Vyberte **OK** pro použití změn.</span><span class="sxs-lookup"><span data-stu-id="f396d-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="f396d-195">Všimněte si, že hodnota pole **ID fondu práce** byla nyní změněna na *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="f396d-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f396d-196">Když se objeví dialogové okno **Změna fondu práce**, pole **ID fondu práce** může být ve výchozím nastavení prázdné.</span><span class="sxs-lookup"><span data-stu-id="f396d-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="f396d-197">Pokud je pole prázdné, když vyberete **OK** pro použití změn, odeberete fond práce úplně z práce.</span><span class="sxs-lookup"><span data-stu-id="f396d-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="f396d-198">Kromě přepínání fondů práce můžete pomocí tohoto postupu přidat fond práce do jakékoli pracovní položky, která ji nemá, nebo odebrat fond práce z jakékoli pracovní položky, která jej nemá.</span><span class="sxs-lookup"><span data-stu-id="f396d-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
