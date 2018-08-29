---
title: "Vyhledávání zásob v pokladním místě (POS)"
description: "V tomto tématu jsou popsány možnosti, které jsou k dispozici pro zobrazení informací o zásobách v pokladním místě."
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: e40c558e03ef230fee6726994bc94979d40493c2
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="e82ca-103">Vyhledávání zásob v pokladním místě (POS)</span><span class="sxs-lookup"><span data-stu-id="e82ca-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e82ca-104">Vyhledávání zásob v pokladním místě pomáhá maloobchodním prodejcům dosáhnout provozní kvality v reálném čase a získat přehledy připojením obchodů, pokladního místa a účetního systému.</span><span class="sxs-lookup"><span data-stu-id="e82ca-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="e82ca-105">Tato funkce poskytuje přesné zobrazení zásob produktu v reálném čase napříč obchody a distribučními centry.</span><span class="sxs-lookup"><span data-stu-id="e82ca-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="e82ca-106">Rovněž pomáhá maloobchodním prodejcům využít další efektivní možnosti a úspory nákladů díky zlepšenému plánování zásob v reálném čase.</span><span class="sxs-lookup"><span data-stu-id="e82ca-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="e82ca-107">Přesné zobrazení zásob v reálném čase napříč organizací pomáhá zaměstnacům obchodu poskytovat včasný a vynikající zákaznický servis.</span><span class="sxs-lookup"><span data-stu-id="e82ca-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="e82ca-108">Nejdůležitějším okamžikem je okamžik, kdy je zákazník připraven k rozhodnutí o koupi.</span><span class="sxs-lookup"><span data-stu-id="e82ca-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="e82ca-109">Je důležité, aby pokladníci v obchodě měli k dispozici informace o zásobách v reálném čase, aby mohli přesně zaručit dodání a vyzvednutí produktu.</span><span class="sxs-lookup"><span data-stu-id="e82ca-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="e82ca-110">Stránku **Vyhledávání zásob** můžete otevřít z pracovních prostorů **Retail Modern POS** nebo **Retail Cloud POS**.</span><span class="sxs-lookup"><span data-stu-id="e82ca-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Dlaždice vyhledávání zásob na domovské stránce pokladního místa](media/POSHomepage.png)

<span data-ttu-id="e82ca-112">Na stránce **Vyhledávání zásob** můžete použít číselnou klávesnici pro zadání čísla produktu.</span><span class="sxs-lookup"><span data-stu-id="e82ca-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="e82ca-113">Poté můžete zobrazit množství na skladě pro více obchodů a skladů.</span><span class="sxs-lookup"><span data-stu-id="e82ca-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standardní stránka vyhledávání zásob](media/InventoryLookUp.png)

<span data-ttu-id="e82ca-115">Pro každé skladové místo se rovněž zobrazují **Rezervovaná** a **Objednaná** množství.</span><span class="sxs-lookup"><span data-stu-id="e82ca-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="e82ca-116">**Rezervované** – Toto množství se vztahuje k hodnotě **Fyzicky rezervováno** z účetního systému pro zadané číslo produktu na daném skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="e82ca-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="e82ca-117">**Objednané** – Toto množství se vztahuje k hodnotě **Objednáno celkem** z účetního systému pro zadané číslo produktu na daném skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="e82ca-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="e82ca-118">Skladová místa, pro která se zobrazují informace o dostupnosti zásob</span><span class="sxs-lookup"><span data-stu-id="e82ca-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="e82ca-119">Seznam skladových míst obsahuje dva typy entit:</span><span class="sxs-lookup"><span data-stu-id="e82ca-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="e82ca-120">**Maloobchody** – Seznam zobrazuje obchody, které jsou nakonfigurovány pomocí skupiny lokátoru obchodů pro aktuální obchod v modulu Retail headquarters.</span><span class="sxs-lookup"><span data-stu-id="e82ca-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span> 
- <span data-ttu-id="e82ca-121">**Distribučních centra** – Různé typy distribučních center (například sklady) lze konfigurovat v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e82ca-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="e82ca-122">Seznam však zobrazuje informace o dostupnosti zásob pouze pro distribuční centra výchozího typu **Standardní**.</span><span class="sxs-lookup"><span data-stu-id="e82ca-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e82ca-123">Informace o dostupnosti zásob se nezobrazuje pro sklady typu **Tranzit**, **Karanténa** a **Zboží v postupu** pro pokladní místo.</span><span class="sxs-lookup"><span data-stu-id="e82ca-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="e82ca-124">Na stránce **Vyhledávání zásob** je možné zobrazit kromě aktuálního množství na skladě, rezervovaného množství a objednaného množství i množství dostupné pro slíbení pro každý obchod.</span><span class="sxs-lookup"><span data-stu-id="e82ca-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="e82ca-125">Vyberte obchod, pro který chcete zobrazit informace o množství dostupném pro slíbení, a pak vyberte **Zobrazit dostupnost obchodu**.</span><span class="sxs-lookup"><span data-stu-id="e82ca-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![Množství ATP](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="e82ca-127">Otevření zobrazení matice založené na dimenzi pro zobrazení všech variant</span><span class="sxs-lookup"><span data-stu-id="e82ca-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="e82ca-128">Na stránce **Podrobnosti produktu** základního produktu nebo na stránce **Vyhledávání zásob** vyberte **Zobrazit všechny varianty** z panelu aplikací dolní části stránky.</span><span class="sxs-lookup"><span data-stu-id="e82ca-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="e82ca-129">Zobrazení **Matice založená na dimenzi** pro počáteční spuštění z těchto stránkách zobrazuje informace o dostupnosti zásob pro všechny varianty produktu pro aktuální obchod.</span><span class="sxs-lookup"><span data-stu-id="e82ca-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="e82ca-130">Tlačítko **Zobrazit všechny varianty** je k dispozici pouze pro základní produkty položky, které mají varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="e82ca-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="e82ca-131">Není k dispozici pro samostatné produkty nebo sady.</span><span class="sxs-lookup"><span data-stu-id="e82ca-131">It isn't available for standalone products or kits.</span></span>

![Tlačítko Zobrazit všechny varianty na stránce vyhledávání zásob](media/StandardToMatrix.png)

<span data-ttu-id="e82ca-133">Vyberte **Zobrazit všechny varianty** na stránce **Podrobnosti produktu** základního produktu nebo na stránce **Vyhledávání zásob** bez výběru skladového místa, přejděte na zobrazení **Matice založená na dimenzi** pro zobrazení informací o dostupnosti zásob pro všechny varianty produktu pro aktuální obchod.</span><span class="sxs-lookup"><span data-stu-id="e82ca-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Zobrazení Matice založená na dimenzi pro stránku Vyhledávání zásob](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="e82ca-135">Na předchozím obrázku je pořadí zobrazení dimenzí abecední, vzhledem k tomu, že pro vybraný produkt nebylo nakonfigurováno pořadí zobrazení dimenzí.</span><span class="sxs-lookup"><span data-stu-id="e82ca-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="e82ca-136">V zobrazení **Matice založená na dimenzi** zahrnují buňky pro varianty produktu hodnotu zásob na skladě v pravém dolním rohu.</span><span class="sxs-lookup"><span data-stu-id="e82ca-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="e82ca-137">Následující tabulka vysvětluje význam různých hodnot.</span><span class="sxs-lookup"><span data-stu-id="e82ca-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="e82ca-138">Hodnota položek na skladě</span><span class="sxs-lookup"><span data-stu-id="e82ca-138">On-hand value</span></span>                            | <span data-ttu-id="e82ca-139">popis</span><span class="sxs-lookup"><span data-stu-id="e82ca-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="e82ca-140">Číselná hodnota větší než 0 (nula)</span><span class="sxs-lookup"><span data-stu-id="e82ca-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="e82ca-141">Varianta byla uvolněna do vybraného skladového místa a můžete provést další akce v buňce.</span><span class="sxs-lookup"><span data-stu-id="e82ca-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="e82ca-142">(Tyto akce jsou popsány podrobněji dále v tomto tématu.)</span><span class="sxs-lookup"><span data-stu-id="e82ca-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="e82ca-143">**0** (nula)</span><span class="sxs-lookup"><span data-stu-id="e82ca-143">**0** (zero)</span></span>                             | <span data-ttu-id="e82ca-144">Varianta byla uvolněna do vybraného skladového místa, ale položka není k dispozici ve vybraném skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="e82ca-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="e82ca-145">Lze však provést další akce v buňce.</span><span class="sxs-lookup"><span data-stu-id="e82ca-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="e82ca-146">(Tyto akce jsou popsány podrobněji dále v tomto tématu.)</span><span class="sxs-lookup"><span data-stu-id="e82ca-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="e82ca-147">**není k dispozici** nebo neaktivní buňka</span><span class="sxs-lookup"><span data-stu-id="e82ca-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="e82ca-148">Varianta nebyla uvolněna do vybraného skladového místa a nemůžete provést další akce v buňce.</span><span class="sxs-lookup"><span data-stu-id="e82ca-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="e82ca-149">Výběrem nové dimenze, kterou chcete použít, můžete také změnit pivot pro dimenze.</span><span class="sxs-lookup"><span data-stu-id="e82ca-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span> 

![Změna pivotu](media/ChangePivot.png)

![Pivot změněn](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="e82ca-152">Na předchozím obrázku je vlastní (neabecední) pořadí zobrazení dimenzí pro vybraný produkt.</span><span class="sxs-lookup"><span data-stu-id="e82ca-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="e82ca-153">Je založeno na pořadí zobrazení dimenzí nastaveném v účetním systému.</span><span class="sxs-lookup"><span data-stu-id="e82ca-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="e82ca-154">Dále lze provést v zobrazení **Matice založená na dimenzi** další akce pro zlepšení produktivity zaměstnance obchodu.</span><span class="sxs-lookup"><span data-stu-id="e82ca-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="e82ca-155">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="e82ca-155">Here are some examples:</span></span>

- <span data-ttu-id="e82ca-156">Změňte umístění obchodu pro vyhledání skladové dostupnosti všech variant produktu na jiných skladových místech.</span><span class="sxs-lookup"><span data-stu-id="e82ca-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="e82ca-157">Tato umístění zahrnují jiné obchody ve skupině lokátorů obchodů a distribučních centrech výchozího typu **Standardní**.</span><span class="sxs-lookup"><span data-stu-id="e82ca-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="e82ca-158">Prodejte jednotlivou variantu produktu odběrateli pomocí velkoobchodního prodeje za hotové, vyzvednutí v obchodě nebo expedice na adresu.</span><span class="sxs-lookup"><span data-stu-id="e82ca-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="e82ca-159">Poskytněte odběrateli informace o dostupných položkách pro slíbení jednotlivých variant produktu v konkrétním místě.</span><span class="sxs-lookup"><span data-stu-id="e82ca-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Další akce na dlaždicích variant](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="e82ca-161">Na předchozím obrázku je pořadí zobrazení dimenzí abecední, vzhledem k tomu, že pro vybraný produkt nebylo nakonfigurováno pořadí zobrazení dimenzí.</span><span class="sxs-lookup"><span data-stu-id="e82ca-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="e82ca-162">Následující tabulka uvádí více informací o dalších dostupných akcích.</span><span class="sxs-lookup"><span data-stu-id="e82ca-162">The following table provides more information about the additional actions that are available.</span></span>


|        <span data-ttu-id="e82ca-163">Akce</span><span class="sxs-lookup"><span data-stu-id="e82ca-163">Action</span></span>        |                                                                                                                    <span data-ttu-id="e82ca-164">popis</span><span class="sxs-lookup"><span data-stu-id="e82ca-164">Description</span></span>                                                                                                                    |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       <span data-ttu-id="e82ca-165">Prodat nyní</span><span class="sxs-lookup"><span data-stu-id="e82ca-165">Sell now</span></span>       |                               <span data-ttu-id="e82ca-166">Přidejte vybranou položka varianty k transakci a přesměrujte uživatele na obrazovku transakce.</span><span class="sxs-lookup"><span data-stu-id="e82ca-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="e82ca-167">(Tato akce není k dispozici, když je zvoleným místem distribuční centrum.)</span><span class="sxs-lookup"><span data-stu-id="e82ca-167">(This action isn't available when the selected location is a distribution center.)</span></span>                               |
|   <span data-ttu-id="e82ca-168">Vyzvednout z obchodu</span><span class="sxs-lookup"><span data-stu-id="e82ca-168">Pick up in store</span></span>   |      <span data-ttu-id="e82ca-169">Vytvořte objednávku odběratele pro variantu produktu, která bude vyzvednuta z vybraného umístění, a přesměrujte uživatele na obrazovku transakce.</span><span class="sxs-lookup"><span data-stu-id="e82ca-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="e82ca-170">(Tato akce není k dispozici, když je zvoleným místem distribuční centrum.)</span><span class="sxs-lookup"><span data-stu-id="e82ca-170">(This action isn't available when the selected location is a distribution center.)</span></span>       |
|     <span data-ttu-id="e82ca-171">Dodat produkt</span><span class="sxs-lookup"><span data-stu-id="e82ca-171">Ship product</span></span>     |                                                 <span data-ttu-id="e82ca-172">Vytvořte objednávku odběratele pro variantu produktu, která bude expedována z vybraného umístění, a přesměrujte uživatele na obrazovku transakce.</span><span class="sxs-lookup"><span data-stu-id="e82ca-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span>                                                 |
|     <span data-ttu-id="e82ca-173">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="e82ca-173">Availability</span></span>     |                                                                             <span data-ttu-id="e82ca-174">Zobrazte informace o položkách dostupných pro slíbení pro vybranou kombinaci variant pro vybrané umístění.</span><span class="sxs-lookup"><span data-stu-id="e82ca-174">Show the ATP information for the selected variant combination for the selected location.</span></span>                                                                              |
|  <span data-ttu-id="e82ca-175">Zobrazit všechna místa</span><span class="sxs-lookup"><span data-stu-id="e82ca-175">Show all locations</span></span>  | <span data-ttu-id="e82ca-176">Přepněte na standardní zobrazení vyhledávání zásob a zvýrazněte informace o dostupnosti zásob pro variantu položky napříč všemi obchody ve skupině lokátorů obchodů a distribučních centrech typu <strong>Standardní/Výchozí</strong>.</span><span class="sxs-lookup"><span data-stu-id="e82ca-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the <strong>Standard/Default</strong> type.</span></span> |
| <span data-ttu-id="e82ca-177">Zobrazit podrobnosti produktu</span><span class="sxs-lookup"><span data-stu-id="e82ca-177">View product details</span></span> |                                                                         <span data-ttu-id="e82ca-178">Přesměrujte uživatele na stránku <strong>Podrobnosti produktu</strong> přidruženého základního produktu.</span><span class="sxs-lookup"><span data-stu-id="e82ca-178">Redirect the user to the <strong>Product details</strong> page of the associated product master.</span></span>                                                                          |


