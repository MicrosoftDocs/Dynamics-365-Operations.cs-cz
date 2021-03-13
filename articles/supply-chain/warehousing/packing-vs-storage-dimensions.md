---
title: Nastavení různých dimenzí pro balení a skladování
description: Toto téma ukazuje, jak určit, pro který proces (balení, skladování nebo vnořené balení) se použije každá zadaná dimenze.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078242"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="86227-103">Nastavení různých dimenzí pro balení a skladování</span><span class="sxs-lookup"><span data-stu-id="86227-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86227-104">Některé položky jsou zabaleny nebo uloženy takovým způsobem, že budete možná muset sledovat fyzické dimenze odlišně pro každý z několika různých procesů.</span><span class="sxs-lookup"><span data-stu-id="86227-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="86227-105">Funkce *Rozměry balení produktu* umožňuje nastavit jeden nebo několik typů dimenzí pro každý produkt.</span><span class="sxs-lookup"><span data-stu-id="86227-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="86227-106">Každý typ dimenze poskytuje sadu fyzických měření (hmotnost, šířka, hloubka a výška) a zavádí proces, kde platí tyto hodnoty fyzického měření.</span><span class="sxs-lookup"><span data-stu-id="86227-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="86227-107">Když je tato funkce povolena, systém bude podporovat následující typy dimenzí:</span><span class="sxs-lookup"><span data-stu-id="86227-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="86227-108">*Úložiště* - Dimenze úložiště se používají společně s volumetrií umístění k určení, kolik z každé položky lze uložit v různých umístěních skladu.</span><span class="sxs-lookup"><span data-stu-id="86227-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="86227-109">*Balení* - Dimenze balení se používají během kontejnerizace a procesu ručního balení k určení, kolik z každé položky se vejde do různých typů kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="86227-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="86227-110">*Vnořené balení* - Vnořené dimenze balení se používají, když proces balení obsahuje více úrovní.</span><span class="sxs-lookup"><span data-stu-id="86227-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="86227-111">*Dimenze úložiště* jsou podporovány, i když není funkce *Dimenze balení produktu* není povolena.</span><span class="sxs-lookup"><span data-stu-id="86227-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="86227-112">Nastavíte je pomocí stránky **Fyzická dimenze** v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="86227-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="86227-113">Tyto dimenze používají všechny procesy, kde nejsou specifikovány rozměry balení a vnořené rozměry.</span><span class="sxs-lookup"><span data-stu-id="86227-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="86227-114">Dimenze *Balení* a *vnořené balení* se nastavují pomocí stránky **fyzické dimenze produktu**, která se přidá, když povolíte funkci *Dimenze balení produktu*.</span><span class="sxs-lookup"><span data-stu-id="86227-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="86227-115">Toto téma poskytuje scénář, který ukazuje, jak používat tuto funkci.</span><span class="sxs-lookup"><span data-stu-id="86227-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="86227-116">Zapněte funkci dimenzí produktu balení</span><span class="sxs-lookup"><span data-stu-id="86227-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="86227-117">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="86227-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="86227-118">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="86227-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="86227-119">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="86227-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="86227-120">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="86227-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="86227-121">**Název funkce:** *Dimenze produktu balení*</span><span class="sxs-lookup"><span data-stu-id="86227-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="86227-122">Příklad</span><span class="sxs-lookup"><span data-stu-id="86227-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="86227-123">Nastavení scénáře</span><span class="sxs-lookup"><span data-stu-id="86227-123">Set up the scenario</span></span>

<span data-ttu-id="86227-124">Než budete moci spustit ukázkový scénář, musíte připravit systém podle popisu v této části.</span><span class="sxs-lookup"><span data-stu-id="86227-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="86227-125">Povolit ukázková data</span><span class="sxs-lookup"><span data-stu-id="86227-125">Enable demo data</span></span>

<span data-ttu-id="86227-126">Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="86227-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="86227-127">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu *USMF*.</span><span class="sxs-lookup"><span data-stu-id="86227-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="86227-128">Přidání nové fyzické dimenze do produktu</span><span class="sxs-lookup"><span data-stu-id="86227-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="86227-129">Přidejte novou fyzickou dimenzi produktu pomocí následujícího postupu:</span><span class="sxs-lookup"><span data-stu-id="86227-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="86227-130">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="86227-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="86227-131">Vyberte produkt s **číslem položky** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="86227-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="86227-132">V podokně akcí na kartě **Řízení zásob** a ve skupině **Sklad** vyberte **Fyzické rozměry produktu**.</span><span class="sxs-lookup"><span data-stu-id="86227-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="86227-133">Otevře se stránka **Fyzické rozměry produktu**.</span><span class="sxs-lookup"><span data-stu-id="86227-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="86227-134">V podokně akcí vyberte možnost **Nový** pro přidání nové dimenze do mřížky s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="86227-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="86227-135">**Typ fyzické dimenze** - *Balení*</span><span class="sxs-lookup"><span data-stu-id="86227-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="86227-136">**Fyzická jednotka** - *ks*</span><span class="sxs-lookup"><span data-stu-id="86227-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="86227-137">**Váha** - *4*</span><span class="sxs-lookup"><span data-stu-id="86227-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="86227-138">**Hmotnost/jedn.** - *kg*</span><span class="sxs-lookup"><span data-stu-id="86227-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="86227-139">**Hloubka** - *3*</span><span class="sxs-lookup"><span data-stu-id="86227-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="86227-140">**Výška** - *4*</span><span class="sxs-lookup"><span data-stu-id="86227-140">**Height** - *4*</span></span>
    - <span data-ttu-id="86227-141">**Šířka** - *3*</span><span class="sxs-lookup"><span data-stu-id="86227-141">**Width** - *3*</span></span>
    - <span data-ttu-id="86227-142">**Délka** - *cm*</span><span class="sxs-lookup"><span data-stu-id="86227-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="86227-143">**Jednotka objemu** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="86227-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="86227-144">Pole **Objem** se automaticky vypočítá na základě nastavení **Hloubka**, **Výška**, a **Šířka**.</span><span class="sxs-lookup"><span data-stu-id="86227-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="86227-145">Vytvoření nového typu kontejneru</span><span class="sxs-lookup"><span data-stu-id="86227-145">Create a new container type</span></span>

<span data-ttu-id="86227-146">Jděte na **Řízení skladu \> Nastavení \> Kontejnery \> typy kontejnerů** a vytvořte nový záznam s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="86227-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="86227-147">**Typ kontejneru** - *Malá krabice*</span><span class="sxs-lookup"><span data-stu-id="86227-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="86227-148">**Popis** - *Malá krabice*</span><span class="sxs-lookup"><span data-stu-id="86227-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="86227-149">**Maximální čistá hmotnost** - *50*</span><span class="sxs-lookup"><span data-stu-id="86227-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="86227-150">**Objem** - *144*</span><span class="sxs-lookup"><span data-stu-id="86227-150">**Volume** - *144*</span></span>
- <span data-ttu-id="86227-151">**Délka** - *6*</span><span class="sxs-lookup"><span data-stu-id="86227-151">**Length** - *6*</span></span>
- <span data-ttu-id="86227-152">**Šířka** - *6*</span><span class="sxs-lookup"><span data-stu-id="86227-152">**Width** - *6*</span></span>
- <span data-ttu-id="86227-153">**Výška** - *4*</span><span class="sxs-lookup"><span data-stu-id="86227-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="86227-154">Vytvoření skupiny kontejneru</span><span class="sxs-lookup"><span data-stu-id="86227-154">Create a container group</span></span>

<span data-ttu-id="86227-155">Jděte na **Řízení skladu \> Nastavení \> Kontejnery \> skupiny kontejnerů** a vytvořte nový záznam s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="86227-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="86227-156">**ID skupiny kontejnerů** - *Malá krabice*</span><span class="sxs-lookup"><span data-stu-id="86227-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="86227-157">**Popis** - *Malá krabice*</span><span class="sxs-lookup"><span data-stu-id="86227-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="86227-158">Přidejte nový řádek do oddílu **Detaily**.</span><span class="sxs-lookup"><span data-stu-id="86227-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="86227-159">Nastavte **typ kontejneru** na *Malá krabice*.</span><span class="sxs-lookup"><span data-stu-id="86227-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="86227-160">Nastavení šablony sestavení kontejneru</span><span class="sxs-lookup"><span data-stu-id="86227-160">Set up a container build template</span></span>

<span data-ttu-id="86227-161">Jděte na **Řízení skladu \> Nastavení \> Kontejnery \> Šablony sestavení kontejneru** a vyberte **Krabice**.</span><span class="sxs-lookup"><span data-stu-id="86227-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="86227-162">Změňte **ID skupiny kontejnerů** na *Malá krabice*.</span><span class="sxs-lookup"><span data-stu-id="86227-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="86227-163">Spuštění scénáře</span><span class="sxs-lookup"><span data-stu-id="86227-163">Run the scenario</span></span>

<span data-ttu-id="86227-164">Poté, co jste připravili svůj systém podle popisu v předchozí části, jste připraveni spustit scénář podle popisu v následující části.</span><span class="sxs-lookup"><span data-stu-id="86227-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="86227-165">Vytvoření prodejní objednávky a vytvoření zásilky</span><span class="sxs-lookup"><span data-stu-id="86227-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="86227-166">V tomto procesu vytvoříte zásilku na základě dimenzí *balení* položky, u nichž je výška menší než 3.</span><span class="sxs-lookup"><span data-stu-id="86227-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="86227-167">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="86227-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="86227-168">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="86227-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="86227-169">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="86227-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="86227-170">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="86227-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="86227-171">**Sklad:** *63*</span><span class="sxs-lookup"><span data-stu-id="86227-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="86227-172">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="86227-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="86227-173">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="86227-173">The new sales order is opened.</span></span> <span data-ttu-id="86227-174">Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="86227-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="86227-175">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="86227-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="86227-176">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="86227-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="86227-177">**Množství:** *5*</span><span class="sxs-lookup"><span data-stu-id="86227-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="86227-178">Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="86227-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="86227-179">Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.</span><span class="sxs-lookup"><span data-stu-id="86227-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="86227-180">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="86227-180">Close the page.</span></span>
1. <span data-ttu-id="86227-181">V podokně Akce na kartě **Sklad** otevřete možnost **Uvolnit do skladu**. Vytvoří se práce pro sklad.</span><span class="sxs-lookup"><span data-stu-id="86227-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="86227-182">Na záložce s náhledem **Řádky prodejní objednávky** zvolte **Sklad \> Podrobnosti o dodávce**.</span><span class="sxs-lookup"><span data-stu-id="86227-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="86227-183">V podokně akcí otevřete kartu **Doprava** a vyberte **Zobrazit kontejnery**.</span><span class="sxs-lookup"><span data-stu-id="86227-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="86227-184">Potvrďte, že položka byla kontejnerizována do dvou kontejnerů *Malá krabice*.</span><span class="sxs-lookup"><span data-stu-id="86227-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="86227-185">Umístění položky do úložiště</span><span class="sxs-lookup"><span data-stu-id="86227-185">Place an item into storage</span></span>

1. <span data-ttu-id="86227-186">Otevřete mobilní zařízení, přihlaste se do skladu 63 a přejděte na **Inventář \> Upravit**.</span><span class="sxs-lookup"><span data-stu-id="86227-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="86227-187">Zadejte **Loc** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="86227-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="86227-188">Vytvořte novou registrační značku pomocí **Položka** = *A0001* a **Množství** = *1 ks*.</span><span class="sxs-lookup"><span data-stu-id="86227-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="86227-189">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="86227-189">Select **OK**.</span></span> <span data-ttu-id="86227-190">Zobrazí se chyba „Umístění SHORT-01 se nezdařilo, protože položka A0001 se nevejde do zadaných rozměrů umístění.“</span><span class="sxs-lookup"><span data-stu-id="86227-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="86227-191">Důvodem je, že dimenze typu *Úložiště* produktu jsou větší než dimenze určené v profilu umístění.</span><span class="sxs-lookup"><span data-stu-id="86227-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>
