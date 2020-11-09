---
title: Zásady práce
description: Toto téma vysvětluje, jak nastavit pracovní zásady.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 08c04caeace7b8ced40915ace1561d817426cba3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017660"
---
# <a name="work-policies"></a><span data-ttu-id="d4e53-103">Zásady práce</span><span class="sxs-lookup"><span data-stu-id="d4e53-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4e53-104">Toto téma vysvětluje, jak nastavit systém a aplikaci skladu tak, aby podporovaly pracovní zásady.</span><span class="sxs-lookup"><span data-stu-id="d4e53-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="d4e53-105">Tuto funkci můžete použít k rychlé registraci zásob bez vytvoření práce odložení, když obdržíte objednávky nákupu nebo převodu nebo když dokončíte výrobní procesy.</span><span class="sxs-lookup"><span data-stu-id="d4e53-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="d4e53-106">Toto téma obsahuje obecné informace.</span><span class="sxs-lookup"><span data-stu-id="d4e53-106">This topic provides general information.</span></span> <span data-ttu-id="d4e53-107">Podrobné informace týkající se přijímání registračních značek viz [Příjem registrační značky prostřednictvím aplikace skladu](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="d4e53-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="d4e53-108">Zásady práce určují, zda je práce ve skladu vytvořena, když je vyrobená položka nahlášena jako dokončená nebo když je zboží přijato pomocí aplikace skladu.</span><span class="sxs-lookup"><span data-stu-id="d4e53-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="d4e53-109">Každé zásady práce nastavíte definováním podmínek, ve kterých platí: typy a procesy pracovní objednávky, umístění zásob a (volitelně) produkty.</span><span class="sxs-lookup"><span data-stu-id="d4e53-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="d4e53-110">Například objednávka produktu *A0001* musí být přijata na místě *RECV* ve skladu *24*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="d4e53-111">Později se produkt spotřebuje v jiném procesu na místě *RECV*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="d4e53-112">V takovém případě můžete nastavit pracovní zásadu, která zabrání tomu, aby v případě, že pracovník ohlásí produkt *A0001* jako přijatý do skladu *RECV* , nebyla vytvořena práce odložení.</span><span class="sxs-lookup"><span data-stu-id="d4e53-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="d4e53-113">Aby byly zásady práce aktivní, musíte pro ně definovat nejméně jedno místo na pevné záložce **Skladovací místa** na stránce **Zásady práce**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="d4e53-114">Nemůžete zadat stejné umístění pro více pracovních zásad.</span><span class="sxs-lookup"><span data-stu-id="d4e53-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="d4e53-115">Možnost **Tisk štítku** pro mobilní zařízení s aplikací Warehousing nevytisknou registrační štítek bez vytvoření práce.</span><span class="sxs-lookup"><span data-stu-id="d4e53-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="d4e53-116">Aktivace funkcí v systému</span><span class="sxs-lookup"><span data-stu-id="d4e53-116">Activate the features in your system</span></span>

<span data-ttu-id="d4e53-117">Chcete-li zpřístupnit všechny funkce popsané v tomto tématu ve vašem systému, zapněte v systému dvě následující funkce [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="d4e53-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="d4e53-118">Rozšíření příjmu registrační značky</span><span class="sxs-lookup"><span data-stu-id="d4e53-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="d4e53-119">Vylepšení zásad práce pro příchozí práci</span><span class="sxs-lookup"><span data-stu-id="d4e53-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="d4e53-120">Stránka Zásady práce</span><span class="sxs-lookup"><span data-stu-id="d4e53-120">The Work policies page</span></span>

<span data-ttu-id="d4e53-121">Chcete-li nastavit zásady práce, přejděte na **Řízení skladu \> Nastavení \> Práce \> Zásady práce**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="d4e53-122">Poté na každé pevné záložce nastavte pole, jak je popsáno v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="d4e53-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="d4e53-123">Pevná záložka Typy pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="d4e53-123">The Work order types FastTab</span></span>

<span data-ttu-id="d4e53-124">Na pevné záložce **Typy pracovních příkazů** přidejte všechny typy pracovních příkazů a související pracovní procesy, na které se pracovní zásady vztahují.</span><span class="sxs-lookup"><span data-stu-id="d4e53-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="d4e53-125">Pro pracovní zásady jsou podporovány následující typy pracovních příkazů a související pracovní procesy.</span><span class="sxs-lookup"><span data-stu-id="d4e53-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="d4e53-126">Typ pořadí pracovních činností</span><span class="sxs-lookup"><span data-stu-id="d4e53-126">Work order type</span></span> | <span data-ttu-id="d4e53-127">Proces práce</span><span class="sxs-lookup"><span data-stu-id="d4e53-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="d4e53-128">Výdej suroviny</span><span class="sxs-lookup"><span data-stu-id="d4e53-128">Raw material picking</span></span>| <span data-ttu-id="d4e53-129">Všechny související procesy</span><span class="sxs-lookup"><span data-stu-id="d4e53-129">All related processes</span></span> |
| <span data-ttu-id="d4e53-130">Vyskladnění vedlejšího produktu</span><span class="sxs-lookup"><span data-stu-id="d4e53-130">Co-product and by-product put away</span></span> | <span data-ttu-id="d4e53-131">Všechny související procesy</span><span class="sxs-lookup"><span data-stu-id="d4e53-131">All related processes</span></span> |
| <span data-ttu-id="d4e53-132">Výdej dokončeného zboží</span><span class="sxs-lookup"><span data-stu-id="d4e53-132">Finished goods putaway</span></span> | <span data-ttu-id="d4e53-133">Všechny související procesy</span><span class="sxs-lookup"><span data-stu-id="d4e53-133">All related processes</span></span> |
| <span data-ttu-id="d4e53-134">Příjem převodu</span><span class="sxs-lookup"><span data-stu-id="d4e53-134">Transfer receipt</span></span> | <span data-ttu-id="d4e53-135">Přijetí (a odložení) registrační značky</span><span class="sxs-lookup"><span data-stu-id="d4e53-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="d4e53-136">Nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="d4e53-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="d4e53-137">Přijetí (a odložení) registrační značky</span><span class="sxs-lookup"><span data-stu-id="d4e53-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="d4e53-138">Přijetí (a odložení) položky nákladu</span><span class="sxs-lookup"><span data-stu-id="d4e53-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="d4e53-139">Přijetí řádku nákupní objednávky (a odložení)</span><span class="sxs-lookup"><span data-stu-id="d4e53-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="d4e53-140">Přijetí zboží nákupní objednávky (a odložení)</span><span class="sxs-lookup"><span data-stu-id="d4e53-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="d4e53-141">Chcete-li nastavit pracovní zásady tak, aby se vztahovaly na několik pracovních procesů stejného typu pracovního příkazu, přidejte do mřížky samostatný řádek pro každý pracovní proces.</span><span class="sxs-lookup"><span data-stu-id="d4e53-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="d4e53-142">Pro každý řádek v mřížce nastavte pole **Metodu tvorby práce** na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="d4e53-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="d4e53-143">**Nikdy** - Tato hodnota značí, že pracovní zásada zabrání vytvoření práce ve skladu pro vybraný typ pracovního příkazu a souvisejícího pracovního procesu.</span><span class="sxs-lookup"><span data-stu-id="d4e53-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="d4e53-144">**Cross docking** - Zásady práce vytvoří křížové dokovací práce pomocí zásady, kterou vyberete v poli **Název zásady cross dockingu**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="d4e53-145">Pevná záložka Umístění zásob</span><span class="sxs-lookup"><span data-stu-id="d4e53-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="d4e53-146">Na pevné záložce **Umístění zásob** přidejte všechna umístění, kde by se měly tyto pracovní zásady použít.</span><span class="sxs-lookup"><span data-stu-id="d4e53-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="d4e53-147">Pokud žádné umístění není přidruženo k zásadám práce, zásady práce se nepoužijí na žádný proces.</span><span class="sxs-lookup"><span data-stu-id="d4e53-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="d4e53-148">Nemůžete zadat stejné umístění pro více pracovních zásad.</span><span class="sxs-lookup"><span data-stu-id="d4e53-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="d4e53-149">Je možné použít umístění skladu, které je přiřazeno k profilu místa, kde není volba **Použít sledování registrační značky** vypnutá.</span><span class="sxs-lookup"><span data-stu-id="d4e53-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="d4e53-150">V takovém případě pracovníci zaregistrují zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="d4e53-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="d4e53-151">Pevná záložka Produkty</span><span class="sxs-lookup"><span data-stu-id="d4e53-151">The Products FastTab</span></span>

<span data-ttu-id="d4e53-152">Na kartě **Produkty** nastavte pole **Výběr produktu** na řízení, na které produkty by se zásady měly vztahovat:</span><span class="sxs-lookup"><span data-stu-id="d4e53-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="d4e53-153">**Vše** - Zásady by se měly vztahovat na všechny produkty.</span><span class="sxs-lookup"><span data-stu-id="d4e53-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="d4e53-154">**Vybrané** - Zásady by se měly vztahovat pouze na produkty, které jsou uvedeny v tabulce.</span><span class="sxs-lookup"><span data-stu-id="d4e53-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="d4e53-155">Použijte panel nástrojů na pevné záložce **Produkty** pro přidání produktů do mřížky nebo jejich odstranění z mřížky.</span><span class="sxs-lookup"><span data-stu-id="d4e53-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="d4e53-156">Výchozí a vlastní umístění „do“</span><span class="sxs-lookup"><span data-stu-id="d4e53-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="d4e53-157">Abyste zpřístupnili funkce popsané v této části ve vašem systému, musíte zapnout funkce *Vylepšení příjmu poznávací značky* a *Vylepšení pracovních zásad pro příchozí práci* v okně [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d4e53-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="d4e53-158">Dříve systém podporoval příjem pouze ve výchozím umístění, které je definováno pro každý sklad.</span><span class="sxs-lookup"><span data-stu-id="d4e53-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="d4e53-159">Položky nabídky mobilního zařízení, které používají následující procesy vytváření práce, však nyní poskytují volbu **Použít výchozí data**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="d4e53-160">Tato možnost umožňuje přiřadit vlastní volbu „do“ místa k jedné nebo více položkám nabídky.</span><span class="sxs-lookup"><span data-stu-id="d4e53-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="d4e53-161">(Tato možnost již byla k dispozici pro některé jiné typy položek nabídky.)</span><span class="sxs-lookup"><span data-stu-id="d4e53-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="d4e53-162">Přijetí (a odložení) registrační značky</span><span class="sxs-lookup"><span data-stu-id="d4e53-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="d4e53-163">Přijetí (a odložení) položky nákladu</span><span class="sxs-lookup"><span data-stu-id="d4e53-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="d4e53-164">Přijetí řádku nákupní objednávky (a odložení)</span><span class="sxs-lookup"><span data-stu-id="d4e53-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="d4e53-165">Přijetí zboží nákupní objednávky (a odložení)</span><span class="sxs-lookup"><span data-stu-id="d4e53-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="d4e53-166">Nastavení **Do místa** pro položku nabídky přepíše výchozí umístění příjmu do skladu, pro všechny objednávky, které jsou zpracovány pomocí této položky nabídky.</span><span class="sxs-lookup"><span data-stu-id="d4e53-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="d4e53-167">Chcete-li nastavit položku nabídky mobilního zařízení na podporu příjmu do vlastního místa, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="d4e53-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="d4e53-168">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d4e53-169">Vyberte nebo vytvořte položku nabídky, která používá jeden z procesů vytváření práce, které jsou uvedeny dříve v této části.</span><span class="sxs-lookup"><span data-stu-id="d4e53-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="d4e53-170">Na pevné záložce **Obecné** nastavte možnost **Použít výchozí data** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="d4e53-171">V podokně akcí vyberte **výchozí data**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="d4e53-172">Na stránce **Výchozí data** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d4e53-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="d4e53-173">**Výchozí datové pole:** Nastavte toto pole na *Do místa*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="d4e53-174">**Sklad:** Vyberte cílový sklad, který chcete použít s touto položkou nabídky.</span><span class="sxs-lookup"><span data-stu-id="d4e53-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="d4e53-175">**Umístění:** Toto pole uvádí všechna ID umístění, která jsou k dispozici pro vybraný sklad.</span><span class="sxs-lookup"><span data-stu-id="d4e53-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="d4e53-176">Nastavení tohoto pole však ve skutečnosti nemá žádný účinek.</span><span class="sxs-lookup"><span data-stu-id="d4e53-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="d4e53-177">Proto je nemůžete nechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="d4e53-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="d4e53-178">Seznam však můžete použít k potvrzení ID, které musíte zadat do pole **Pevně zakódovaná hodnota**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="d4e53-179">**Pevně zakódovaná hodnota:** Zadejte ID místa pro přijímající umístění, které se vztahuje na tuto položku nabídky.</span><span class="sxs-lookup"><span data-stu-id="d4e53-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="d4e53-180">Pracovní zásadu lze použít, pouze pokud jsou všechna místa pro příjem uvedena v příslušném nastavení zásad práce.</span><span class="sxs-lookup"><span data-stu-id="d4e53-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="d4e53-181">Tento požadavek platí bez ohledu na to, zda používáte výchozí umístění pro příjem skladu nebo vlastní umístění „do“.</span><span class="sxs-lookup"><span data-stu-id="d4e53-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="d4e53-182">Příklad scénáře: Příjem skladu</span><span class="sxs-lookup"><span data-stu-id="d4e53-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="d4e53-183">Všechny produkty, které obdrží proces *Přijetí zboží nákupní objednávky (a odložení)* musí být registrován v místě *FL-001* a musí být k dispozici ve skladu *24*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001* , and they must be available in warehouse *24*.</span></span> <span data-ttu-id="d4e53-184">Práce by však neměla být vytvořena.</span><span class="sxs-lookup"><span data-stu-id="d4e53-184">However, work should not be created.</span></span> <span data-ttu-id="d4e53-185">Produkty, které jsou přijímány jakýmkoli jiným procesem (tj. pomocí jiných položek nabídky mobilního zařízení), by měly být zaregistrovány ve výchozím umístění pro příjem skladu ( *RECV* ) a práce by měla být vytvořena jako obvykle.</span><span class="sxs-lookup"><span data-stu-id="d4e53-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location ( *RECV* ), and work should be created as usual.</span></span> <span data-ttu-id="d4e53-186">(Tento scénář nezobrazuje výchozí nastavení příjmu.)</span><span class="sxs-lookup"><span data-stu-id="d4e53-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="d4e53-187">Tento scénář vyžaduje následující prvky:</span><span class="sxs-lookup"><span data-stu-id="d4e53-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="d4e53-188">Zásady práce pro proces *Přijetí zboží nákupní objednávky (a odložení)* v místě *FL-001* , pro všechny produkty</span><span class="sxs-lookup"><span data-stu-id="d4e53-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001* , for all products</span></span>
- <span data-ttu-id="d4e53-189">Položka nabídky mobilního zařízení, která má výchozí data a nastavuje pole **Na místo** na hodnotu *FL-001*</span><span class="sxs-lookup"><span data-stu-id="d4e53-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d4e53-190">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="d4e53-190">Prerequisites</span></span>

<span data-ttu-id="d4e53-191">Abyste zpřístupnili funkce popsané v tomto scénáři ve vašem systému, musíte zapnout funkce *Vylepšení příjmu registrační značky* a *Vylepšení pracovních zásad pro příchozí práci* v okně [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d4e53-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="d4e53-192">Tento scénář používá standardní ukázková data.</span><span class="sxs-lookup"><span data-stu-id="d4e53-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="d4e53-193">Proto, chcete-li s tímto scénářem pracovat pomocí hodnot zde poskytnutých, musíte používat prostředí, ve kterém jsou nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="d4e53-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="d4e53-194">Dále musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="d4e53-195">Nastavení zásady práce</span><span class="sxs-lookup"><span data-stu-id="d4e53-195">Set up a work policy</span></span>

1. <span data-ttu-id="d4e53-196">Přejděte do nabídky **Řízení skladu \> Nastavení \> Práce \> Pracovní zásady**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="d4e53-197">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-197">Select **New**.</span></span>
1. <span data-ttu-id="d4e53-198">Do pole **Název zásady práce** zadejte *Žádná odložená práce nákupní položky*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="d4e53-199">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-199">Select **Save**.</span></span>
1. <span data-ttu-id="d4e53-200">Na pevné záložce **Typy pracovních příkazů** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="d4e53-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="d4e53-201">**Typ pracovního příkazu:** *Nákupní objednávky*</span><span class="sxs-lookup"><span data-stu-id="d4e53-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="d4e53-202">**Proces tvorby práce:** *Příjem (a odložení) řádku nákupní objednávky*</span><span class="sxs-lookup"><span data-stu-id="d4e53-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="d4e53-203">**Metoda tvorby práce:** *Nikdy*</span><span class="sxs-lookup"><span data-stu-id="d4e53-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="d4e53-204">**Název zásad cross dockingu:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="d4e53-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="d4e53-205">Na pevné záložce **Skladová místa** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="d4e53-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="d4e53-206">**Sklad:** *24*</span><span class="sxs-lookup"><span data-stu-id="d4e53-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="d4e53-207">**Umístění:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="d4e53-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="d4e53-208">Na pevné záložce **Produkty** , nastavte pole **Výběr produktu** na *Vše*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="d4e53-209">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="d4e53-210">Nastavení položky nabídky na mobilním zařízení na registraci přijatých položek</span><span class="sxs-lookup"><span data-stu-id="d4e53-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="d4e53-211">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d4e53-212">V levém podokně vyberte existující položku nabídky **Příjem nákupu**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="d4e53-213">Na pevné záložce **Obecné** nastavte možnost **Použít výchozí data** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="d4e53-214">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-214">Select **Save**.</span></span>
1. <span data-ttu-id="d4e53-215">V podokně akcí vyberte **výchozí data**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="d4e53-216">Na pevné záložce **Výchozí data** vyberte **Nový** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="d4e53-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="d4e53-217">**Výchozí datové pole:** *Do místa*</span><span class="sxs-lookup"><span data-stu-id="d4e53-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="d4e53-218">**Sklad:** *24*</span><span class="sxs-lookup"><span data-stu-id="d4e53-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="d4e53-219">**Místo:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="d4e53-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="d4e53-220">**Pevně zakódovaná hodnota:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="d4e53-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="d4e53-221">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="d4e53-222">Příjem nákupní objednávky bez vytvoření práce</span><span class="sxs-lookup"><span data-stu-id="d4e53-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="d4e53-223">Příklad v této části ukazuje, jak přijímat položku objednávky, ale bez vytvoření práce, na místě, které se liší od výchozího přijímacího místa, které je nastaveno na sklad.</span><span class="sxs-lookup"><span data-stu-id="d4e53-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="d4e53-224">Tento příklad používá zásady práce a položku mobilního zařízení, které jste vytvořili dříve v tomto scénáři.</span><span class="sxs-lookup"><span data-stu-id="d4e53-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="d4e53-225">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="d4e53-225">Create a purchase order</span></span>

1. <span data-ttu-id="d4e53-226">Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d4e53-227">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-227">Select **New**.</span></span>
1. <span data-ttu-id="d4e53-228">V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d4e53-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d4e53-229">**Účet dodavatele:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="d4e53-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="d4e53-230">**Lokalita:** *2*</span><span class="sxs-lookup"><span data-stu-id="d4e53-230">**Site:** *2*</span></span>
    - <span data-ttu-id="d4e53-231">**Sklad:** *24*</span><span class="sxs-lookup"><span data-stu-id="d4e53-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="d4e53-232">Vyberte **OK** - nová prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="d4e53-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="d4e53-233">Na pevné záložce **Řádky objednávek** nastavte následující hodnoty pro prázdný řádek:</span><span class="sxs-lookup"><span data-stu-id="d4e53-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="d4e53-234">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d4e53-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d4e53-235">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="d4e53-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="d4e53-236">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-236">Select **Save**.</span></span>
1. <span data-ttu-id="d4e53-237">Poznamenejte si číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d4e53-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="d4e53-238">Příjem nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="d4e53-238">Receive a purchase order</span></span>

1. <span data-ttu-id="d4e53-239">Na mobilním zařízení se přihlaste ke skladu *24* a jako ID uživatele zadejte *24* a jako heslo *1*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="d4e53-240">Vyberte **Příchozí**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="d4e53-241">Vyberte **Příjem nákupu**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-241">Select **Purchase receive**.</span></span> <span data-ttu-id="d4e53-242">Pole **Umístění** by mělo být nastaveno na *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="d4e53-243">Zadejte číslo objednávky pro objednávku, kterou jste vytvořili v předchozím postupu.</span><span class="sxs-lookup"><span data-stu-id="d4e53-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="d4e53-244">V poli **Číslo zboží** zadejte *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="d4e53-245">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-245">Select **OK**.</span></span>
1. <span data-ttu-id="d4e53-246">Do pole **Množství** zadejte *1*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="d4e53-247">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-247">Select **OK**.</span></span>

<span data-ttu-id="d4e53-248">Nákupní objednávka je nyní přijata, ale není s ní spojena žádná práce.</span><span class="sxs-lookup"><span data-stu-id="d4e53-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="d4e53-249">Byl aktualizován soupis zásob a množství *1* položky *A0001* je nyní k dispozici v místě *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="d4e53-250">Příklad scénáře: Výroba</span><span class="sxs-lookup"><span data-stu-id="d4e53-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="d4e53-251">V následujícím příkladu jsou dvě výrobní zakázky, *PROD-001* a *PROD-002*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="d4e53-252">Výrobní zakázka *PROD-001* má operaci s názvem *Sestavení* , kde produkt *SC1* je hlášen jako dokončený v místě *001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-252">Production order *PRD-001* has an operation that is named *Assembly* , where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="d4e53-253">Výrobní zakázka *PROD-002* má operaci, která se nazývá *Lakování* a spotřebovává produkt *SC1* z umístění *001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="d4e53-254">Výrobní zakázka *PROD-002* také spotřebovává suroviny *RM1* 1 z umístění *001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="d4e53-255">Surovina *RM1* je uložena ve skladu *BULK-001* a bude vyskladněno v umístění *001* během práce ve skladu pro výdej surovin.</span><span class="sxs-lookup"><span data-stu-id="d4e53-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="d4e53-256">Pro uvolnění výroby *PROD-002* je generována práce vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="d4e53-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="d4e53-257">[![Zásady práce ve skladu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="d4e53-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="d4e53-258">Při plánování konfigurace zásad práce ve skladu pro tento scénář je třeba zvážit následujících body:</span><span class="sxs-lookup"><span data-stu-id="d4e53-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="d4e53-259">Práce ve skladu pro výdej dokončeného zboží není vyžadována, když vykážete produkt *SC1* jako dokončený z výrobní zakázky *PROD-001* do umístění *001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="d4e53-260">Důvodem je, že operace *Lakování* pro výrobní zakázku *PROD-002* spotřebovává *SC1* na stejném místě.</span><span class="sxs-lookup"><span data-stu-id="d4e53-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="d4e53-261">Práce ve skladu pro vyzvednutí surovin je požadována pro účely přesunutí surovin *RM1* z umístění ve skladu *BULK-001* do umístění *001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="d4e53-262">Toto je příklad zásad práce, které můžete nastavit na základě těchto důvodů:</span><span class="sxs-lookup"><span data-stu-id="d4e53-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="d4e53-263">**Název pracovních zásad:** *Žádná odložená práce*</span><span class="sxs-lookup"><span data-stu-id="d4e53-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="d4e53-264">**Typy pracovních příkazů:** *Výdej dokončeného zboží* a *Vyskladnění vedlejšího produktu*</span><span class="sxs-lookup"><span data-stu-id="d4e53-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="d4e53-265">**Skladová místa:** Sklad *51* a místa *001*</span><span class="sxs-lookup"><span data-stu-id="d4e53-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="d4e53-266">**Produkty:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="d4e53-266">**Products:** *SC1*</span></span>

<span data-ttu-id="d4e53-267">Následující ukázkové scénáře obsahují podrobné pokyny ke způsobu nastavení zásad pracovního skladu pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="d4e53-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="d4e53-268">Ukázkový scénář: Vykázání jako dokončeného v místě, které není řízeno registrační značkou</span><span class="sxs-lookup"><span data-stu-id="d4e53-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="d4e53-269">Tento scénář ukazuje příklad, kdy je výrobní příkaz vykázán jako dokončený v místě, které nemá licenční kód.</span><span class="sxs-lookup"><span data-stu-id="d4e53-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="d4e53-270">Tento scénář používá standardní ukázková data.</span><span class="sxs-lookup"><span data-stu-id="d4e53-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="d4e53-271">Proto, chcete-li s tímto scénářem pracovat pomocí hodnot zde poskytnutých, musíte používat prostředí, ve kterém jsou nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="d4e53-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="d4e53-272">Dále musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="d4e53-273">Nastavení zásady práce ve skladu</span><span class="sxs-lookup"><span data-stu-id="d4e53-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="d4e53-274">Skladové procesy ne vždy zahrnují skladovou práci.</span><span class="sxs-lookup"><span data-stu-id="d4e53-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="d4e53-275">Definováním zásad práce můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.</span><span class="sxs-lookup"><span data-stu-id="d4e53-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="d4e53-276">Přejděte do nabídky **Řízení skladu \> Nastavení \> Práce \> Pracovní zásady**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="d4e53-277">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-277">Select **New**.</span></span>
1. <span data-ttu-id="d4e53-278">Do pole **Název zásady práce** zadejte *Žádná odložená práce*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="d4e53-279">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d4e53-280">Na pevné záložce **Typy pracovních příkazů** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="d4e53-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="d4e53-281">**Typ pracovního příkazu:** *Výdej dokončeného zboží*</span><span class="sxs-lookup"><span data-stu-id="d4e53-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="d4e53-282">**Pracovní proces:** *Všechny související pracovní procesy*</span><span class="sxs-lookup"><span data-stu-id="d4e53-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="d4e53-283">**Metoda tvorby práce:** *Nikdy*</span><span class="sxs-lookup"><span data-stu-id="d4e53-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="d4e53-284">**Název zásad cross dockingu:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="d4e53-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="d4e53-285">Na pevné záložce Skladová místa znovu vyberte **Přidat** pro přidání druhého řádku do mřížky a nastavení následujících hodnot pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="d4e53-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="d4e53-286">V poli **Typ pracovního příkazu:** *Vyskladnění vedlejšího produktu*</span><span class="sxs-lookup"><span data-stu-id="d4e53-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="d4e53-287">**Pracovní proces:** *Všechny související pracovní procesy*</span><span class="sxs-lookup"><span data-stu-id="d4e53-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="d4e53-288">**Metoda tvorby práce:** *Nikdy*</span><span class="sxs-lookup"><span data-stu-id="d4e53-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="d4e53-289">**Název zásad cross dockingu:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="d4e53-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="d4e53-290">Na pevné záložce **Skladová místa** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="d4e53-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="d4e53-291">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="d4e53-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="d4e53-292">**Místo:** *001*</span><span class="sxs-lookup"><span data-stu-id="d4e53-292">**Location:** *001*</span></span>

1. <span data-ttu-id="d4e53-293">Na pevné záložce **Produkty** , nastavte pole **Výběr produktu** na *Vybrané*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="d4e53-294">Na pevné záložce **Produkty** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="d4e53-295">V novém řádku nastavte pole **Číslo položky** na *L0101*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="d4e53-296">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="d4e53-297">Nastavení výstupního umístění</span><span class="sxs-lookup"><span data-stu-id="d4e53-297">Set up an output location</span></span>

1. <span data-ttu-id="d4e53-298">Přejděte na **Správa organizace \> Zdroje \> Skupiny zdrojů.**</span><span class="sxs-lookup"><span data-stu-id="d4e53-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="d4e53-299">V levém podokně vyberte skupinu zdrojů **5102**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="d4e53-300">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d4e53-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d4e53-301">**Výstupní sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="d4e53-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="d4e53-302">**Výstupní umístění:** *001*</span><span class="sxs-lookup"><span data-stu-id="d4e53-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="d4e53-303">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="d4e53-304">Umístění *001* není umístění řízené registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="d4e53-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="d4e53-305">Umístění výstupu, které není řízeno registrační značkou, můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.</span><span class="sxs-lookup"><span data-stu-id="d4e53-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="d4e53-306">Vytvoření výrobní zakázky a její ohlášení jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4e53-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="d4e53-307">Přejděte na **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="d4e53-308">V podokně akcí vyberte možnost **Nová výrobní zakázka**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="d4e53-309">V dialogovém okně **Vytvoření výrobní zakázky** nastavte pole **Číslo položky** na *L0101*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="d4e53-310">Vyberte **Vytvořit** , prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="d4e53-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="d4e53-311">Nová výrobní zakázka je přidána do mřížky na stránce **Všechny výrobní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="d4e53-312">Nechte vybranou novou výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="d4e53-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="d4e53-313">V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Odhad**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="d4e53-314">V dialogovém okně **Odhad** si přečtěte odhad a poté výběrem **OK** zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d4e53-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="d4e53-315">V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Start**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="d4e53-316">V dialogovém okně **Start** na kartě **Obecné** nastavte hodnotu pole **Automatická spotřeba kusovníku** na *Nikdy*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="d4e53-317">Volbou **OK** uložte svá nastavení a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d4e53-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="d4e53-318">V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Vykázat jako dokončené**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="d4e53-319">V dialogovém okně **Vykázat jako dokončené** na kartě **Obecné** nastavte možnost **Chyba přijetí** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="d4e53-320">Volbou **OK** uložte svá nastavení a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d4e53-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="d4e53-321">V podokně akcí na kartě **Sklad** ve skupině **Obecné** vyberte **Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="d4e53-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="d4e53-322">Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena.</span><span class="sxs-lookup"><span data-stu-id="d4e53-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="d4e53-323">K tomuto chování dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt *L0101* ohlášen za dokončený v umístění *001*.</span><span class="sxs-lookup"><span data-stu-id="d4e53-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="d4e53-324">Další informace</span><span class="sxs-lookup"><span data-stu-id="d4e53-324">More information</span></span>

<span data-ttu-id="d4e53-325">Další informace o položkách nabídky mobilního zařízení naleznete v tématu [Nastavení mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d4e53-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="d4e53-326">Další informace týkající se přijímání registračních značek a zásad práce získáte v tématu [Příjem registrační značky prostřednictvím aplikace skladu](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="d4e53-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="d4e53-327">Další informace o správě příchozího vytížení získáte v části [Skladová manipulace s příchozím zatížením pro nákupní objednávky](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="d4e53-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>
