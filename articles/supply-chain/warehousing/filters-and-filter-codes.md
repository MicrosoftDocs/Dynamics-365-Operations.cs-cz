---
title: Konfigurace produktových filtrů pro skladové transakce
description: Toto téma popisuje, jak konfigurovat filtry pro produkty a kódy filtrů ke kategorizaci skladových položek ve skladu. Filtry lze také použít k určení, kteří odběratelé mohou objednat určité zboží a určit zboží, které lze zakoupit od určitého dodavatele.
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 922ff818e069f41c139cc00db9161dc6e113888b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973728"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a><span data-ttu-id="8cb1b-104">Konfigurace produktových filtrů pro skladové transakce</span><span class="sxs-lookup"><span data-stu-id="8cb1b-104">Configure product filters for warehouse transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cb1b-105">Toto téma popisuje, jak konfigurovat filtry pro produkty a kódy filtrů ke kategorizaci skladových položek ve skladu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-105">This topic describes how to configure product filters and filter codes to categorize inventory items in a warehouse.</span></span> <span data-ttu-id="8cb1b-106">Filtry lze také použít k určení, kteří odběratelé mohou objednat určité zboží a určit zboží, které lze zakoupit od určitého dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-106">You can also use filters to specify which customers can order a particular item and which items can be purchased from a particular vendor.</span></span>

<span data-ttu-id="8cb1b-107">Dále můžete nastavit a používat kódy produktů k automatickému uspořádání skladových položek ve skladu a kombinování filtrovaných položek do skupin filtrů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-107">Additionally, you can set up and use product filters to automatically organize inventory items in a warehouse and combine filtered items into filter groups.</span></span> <span data-ttu-id="8cb1b-108">Filtry lze použít k zařazení položek do kategorií pro procesy manipulace, nákupu a prodeje.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-108">Filters can be used to put items into categories for handling, purchasing, and selling processes.</span></span> <span data-ttu-id="8cb1b-109">Možná budete chtít položky seskupit nebo je od sebe oddělit, pokud způsob manipulace s nimi závisí na hmotnosti nebo omezeních manipulace.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-109">You might want to group items together or separate them from each other when the way that they are handled is based on weight or handling restrictions.</span></span> <span data-ttu-id="8cb1b-110">Můžete také určit, od kterých zákazníků nebo prodejců lze položku zakoupit nebo prodat.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-110">You can also specify which customers or vendors an item can be purchased from or sold to.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8cb1b-111">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="8cb1b-111">Prerequisites</span></span>

<span data-ttu-id="8cb1b-112">Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-112">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="8cb1b-113">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="8cb1b-113">Prerequisite</span></span> | <span data-ttu-id="8cb1b-114">Pokyny</span><span class="sxs-lookup"><span data-stu-id="8cb1b-114">Instructions</span></span> |
|---|---|
| <span data-ttu-id="8cb1b-115">Než začnete konfigurovat produkty na stránce **Podrobnosti o uvolněném produktu**, musíte zapnout zpracování skladu pro skupinu dimenzí úložiště produktu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-115">Before you start to configure products on the **Released product details** page, you must turn on warehouse processing for the product's storage dimension group.</span></span> | <span data-ttu-id="8cb1b-116">Jděte na **Správa informací o produkt \> Nastavení \> Skupiny dimenzí a variant \> Skupiny dimenzí úložiště** a vyberte nebo vytvořte skupinu dimenzí úložiště, kde je možnost **Použít procesy řízení skladu** nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-116">Go to **Product information management \> Setup \> Dimension and variant groups \> Storage dimension groups**, and select or create a storage dimension group where the **Use warehouse management processes** option is set to *Yes*.</span></span> |
| <span data-ttu-id="8cb1b-117">Pokud budete používat zákaznické filtry nebo filtry dodavatelů, musíte povolit jejich použití v parametrech řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-117">If you will use customer filters and/or vendor filters, you must enable their use in Warehouse management parameters.</span></span> | <span data-ttu-id="8cb1b-118">Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="8cb1b-119">Na kartě **Filtry produktu** nastavte **Povolit zákaznické filtry** a/nebo **Povolit filtry dodavatele** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-119">On the **Product filters** tab, set the **Enable customer filters** and/or **Enable vendor filters** option  to *Yes*.</span></span> |

## <a name="set-up-product-filters"></a><span data-ttu-id="8cb1b-120">Nastavení filtrů produktu</span><span class="sxs-lookup"><span data-stu-id="8cb1b-120">Set up product filters</span></span>

<span data-ttu-id="8cb1b-121">Filtry produktu poskytují až 10 vlastností **Název filtru**, což jsou hodnoty výčtu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-121">Product filters provide up to 10 **Filter title** characteristics, which are enumeration (enum) values.</span></span> <span data-ttu-id="8cb1b-122">Tyto hodnoty výčtu jsou k dispozici pro výběr při vytváření filtru produktu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-122">These enum values are available for selection when you create a product filter.</span></span> <span data-ttu-id="8cb1b-123">Hodnoty výčtu *Code 1* až *Code 10* jsou definované systémem a představují konkrétní vlastnost nebo atribut položky.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-123">The enum values *Code 1* through *Code 10* are system-defined and represent a specific characteristic or attribute of an item.</span></span> <span data-ttu-id="8cb1b-124">Například *Kód 1* může představovat položky, které mají klasifikaci nebezpečných materiálů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-124">For example, *Code 1* might represent items that have a hazardous material classification.</span></span> <span data-ttu-id="8cb1b-125">*Kód 2* může představovat položky, které si mohou koupit pouze prodejci.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-125">*Code 2* might represent items that only vendors can purchase.</span></span> <span data-ttu-id="8cb1b-126">Filtry produktu pak definují konkrétní hodnotu **Kód filtru** spojenou s hodnotou **Název filtru**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-126">Product filters then define the specific **Filter code** value that is associated with a **Filter title** value.</span></span>

1. <span data-ttu-id="8cb1b-127">Jděte na **Řízení skladu \> Nastavení \> Filtry produktu \> Filtry produktu**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-127">Go to **Warehouse management \> Setup \> Product filters \> Product filters**.</span></span>
1. <span data-ttu-id="8cb1b-128">V podokně Akce vyberte možnost **Nový** pro přidání filtru produktu do mřížky.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-128">On the Action Pane, select **New** to add a product filter to the grid.</span></span>
1. <span data-ttu-id="8cb1b-129">V poli **Název filtru** vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-129">In the **Filter title** field, select a value.</span></span>
1. <span data-ttu-id="8cb1b-130">Zadejte hodnotu do pole **Kód filtru**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-130">In the **Filter code** field, enter a value.</span></span>

    <span data-ttu-id="8cb1b-131">![Nastavení filtru produktu](media/Product_Filters10.png "Nastavení filtru produktu")</span><span class="sxs-lookup"><span data-stu-id="8cb1b-131">![Setting up a product filter](media/Product_Filters10.png "Setting up a product filter")</span></span>

1. <span data-ttu-id="8cb1b-132">Do pole **Popis** zadejte název kódu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-132">In the **Description** field, enter a name for the code.</span></span> <span data-ttu-id="8cb1b-133">Například *Kód 2* může představovat dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-133">For example, *Code 2* might represent vendors.</span></span> <span data-ttu-id="8cb1b-134">Poté můžete vytvořit produktový filtr pro konkrétního dodavatele nebo skupinu dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-134">You can then create a product filter for a specific vendor or group of vendors.</span></span> <span data-ttu-id="8cb1b-135">Více informací naleznete v části [Nastavení kódů filtru dodavatele](#vendor-product-filters) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-135">For more information, see the [Setup vendor filter codes](#vendor-product-filters) section later in this topic.</span></span>

    <span data-ttu-id="8cb1b-136">![Nastavení filtrů produktu](media/Product_Filters.png "Nastavení filtrů produktu")</span><span class="sxs-lookup"><span data-stu-id="8cb1b-136">![Set of product filters](media/Product_Filters.png "Set of product filters")</span></span>

## <a name="set-up-product-filter-groups"></a><span data-ttu-id="8cb1b-137">Nastavení skupin filtru produktu</span><span class="sxs-lookup"><span data-stu-id="8cb1b-137">Set up product filter groups</span></span>

<span data-ttu-id="8cb1b-138">K seskupení kódů filtru můžete použít skupiny filtrů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-138">You can use filter groups to group filter codes.</span></span> <span data-ttu-id="8cb1b-139">Tato schopnost je užitečná, když se skupina používá v dotazu ve směrnici skladového místa, a vy chcete vyhledat skupiny, nikoli série kódů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-139">This capability is helpful when a group is used in a query in a location directive, and you want to search for the group instead of a series of codes.</span></span> <span data-ttu-id="8cb1b-140">Každá skupina filtrů je přidružena ke skupině položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-140">Each filter group is associated with an item group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cb1b-141">Ne všechny skupiny filtrů produktů jsou k dispozici pro kódy filtrů, které jsou vyšší než *Kód 4* (to znamená, *Kód 5* přes *Kód 10*).</span><span class="sxs-lookup"><span data-stu-id="8cb1b-141">Not all product filter groups are available for filter codes that are higher than *Code 4* (that is, *Code 5* through *Code 10*).</span></span> <span data-ttu-id="8cb1b-142">Například u vydaných produktů se sice přidají všechny kódy filtrů produktů, ale seskupení kódů filtrů se neaktualizuje.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-142">For example, for released products, although all the product filter codes will be added, the grouping of filter codes won't be updated.</span></span> <span data-ttu-id="8cb1b-143">Toto chování může být aktualizováno v pozdějších verzích.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-143">This behavior might be updated in later releases.</span></span>

<span data-ttu-id="8cb1b-144">Chcete-li nastavit skupiny filtrů, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-144">To set up filter groups, follow these steps.</span></span>

1. <span data-ttu-id="8cb1b-145">Jděte na **Řízení skladu \> Nastavení \> Filtry produktu \> Skupiny filtrů produktu**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-145">Go to **Warehouse management \> Setup \> Product filters \> Product filter groups**.</span></span>
1. <span data-ttu-id="8cb1b-146">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-146">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8cb1b-147">V poli **Skupina 1** a **Skupina 2** zadejte názvy, které budou použity ke kategorizaci položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-147">In the **Group 1** and **Group 2** fields, enter the names that will be used to categorize items.</span></span>
1. <span data-ttu-id="8cb1b-148">Na záložce s náhledem **Detaily** vytvořte nový řádek stisknutím tlačítka **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-148">On the **Details** FastTab, select **New** to add a line.</span></span>
1. <span data-ttu-id="8cb1b-149">V poli **Počáteční datum / čas** a **Koncové datum / čas** zadejte počáteční a koncové datum pro skupinu filtrů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-149">In the **Start date/time** and **End date/time** fields, enter start and end dates for the filter group.</span></span>
1. <span data-ttu-id="8cb1b-150">V poli **Skupina položek** vyberte skupinu položek, na kterou by se měl filtr produktu vztahovat.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-150">In the **Item group** field, select the item group that the product filter should apply to.</span></span>
1. <span data-ttu-id="8cb1b-151">V poli **Kód 1** až **Kód 10** podle potřeby vyberte kódy filtrů, které chcete do skupiny zahrnout.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-151">In the **Code 1** through **Code 10** fields, select the filter codes to include in the group, as required.</span></span>

    <span data-ttu-id="8cb1b-152">![Sk. položek](media/ProdFilterGroup.png "Sk. položek")</span><span class="sxs-lookup"><span data-stu-id="8cb1b-152">![Item group](media/ProdFilterGroup.png "Item group")</span></span>

> [!NOTE]
> <span data-ttu-id="8cb1b-153">Pokud se při zavření stránky zobrazí chybová zpráva, může chybět nastavení kódu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-153">If you receive an error message when you close the page, a code setup might be missing.</span></span> <span data-ttu-id="8cb1b-154">Na stránce **Skupiny položek** můžete označit kódy jako povinné pro skupinu položek zaškrtnutím políček **Přiřadit kód 1 filtru pro skupinu položek**, **Přiřadit kód 2 filtru pro skupinu položek** atd.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-154">On the **Item groups** page, you can make the codes mandatory for an item group by selecting the **Assign filter code 1 for item group**, **Assign filter code 2 for item group**, and so on, check boxes.</span></span>

## <a name="set-up-filter-codes-on-item-groups"></a><span data-ttu-id="8cb1b-155">Nastavení kódů filtrů ve skupinách zboží</span><span class="sxs-lookup"><span data-stu-id="8cb1b-155">Set up filter codes on item groups</span></span>

<span data-ttu-id="8cb1b-156">Nastavením kódů filtrů pro skupinu zboží můžete vyžadovat kódy, které jsou požadované pro produkty připojené k této skupině zboží.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-156">By setting up filter codes on an item group, you can make the codes that are required for products that are attached to that item group.</span></span>

<span data-ttu-id="8cb1b-157">Chcete-li nastavit kódy filtrů pro skupiny zboží postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-157">To set up filter codes on item groups, follow these steps.</span></span>

1. <span data-ttu-id="8cb1b-158">Jděte na **Řízení zásob \> Nastavení \> Sklady \> Skupiny položek**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-158">Go to **Inventory management \> Setup \> Inventory \> Item groups**.</span></span>
1. <span data-ttu-id="8cb1b-159">V podokně Akce vyberte možnost **Nová** a vytvořte novou skupinu položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-159">On the Action Pane, select **New** to create an item group.</span></span>
1. <span data-ttu-id="8cb1b-160">V poli **Skupina položek** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-160">In the **Item group** field, enter a name.</span></span>
1. <span data-ttu-id="8cb1b-161">Do pole **Název** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-161">In the **Name** field, enter a description.</span></span>
1. <span data-ttu-id="8cb1b-162">Na záložce s náhledem **Sklad** v části **Požadovaný filtr** zaškrtněte příslušná políčka k definování jednoho nebo více kódů filtrů, které musí být určeny pro produkty, které jsou přidružené ke skupině zboží.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-162">On the **Warehouse** FastTab, in the **Filter required** section, select the check boxes for the filter codes that must be specified for products that are associated with the item group.</span></span>

    <span data-ttu-id="8cb1b-163">Chcete-li aktualizovat vydaný produkt, otevřete jeho stránku **Podrobnosti o vydaném produktu** a poté v podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-163">To update a released product, open its **Released product details** page, and then, on the Action Pane, select **Edit**.</span></span> <span data-ttu-id="8cb1b-164">Filtry, které jsou přidruženy ke kódům, budou poté k dispozici na záložce s náhledem **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-164">The filters that are associated with codes then become available on the **Warehouse** FastTab.</span></span>

    <span data-ttu-id="8cb1b-165">![Sk. položek](media/ItemGroup10.png "Sk. položek")</span><span class="sxs-lookup"><span data-stu-id="8cb1b-165">![Item groups](media/ItemGroup10.png "Item groups")</span></span>

1. <span data-ttu-id="8cb1b-166">V části **Filtr skupin položek** zaškrtněte políčka u filtrů, které se musí shodovat, aby skupina filtrů byla výchozí skupinou filtrů pro položku.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-166">In the **Item group filter** section, select the check boxes for the filters that must match for the filter group to be the default filter group for an item.</span></span>

    <span data-ttu-id="8cb1b-167">Například pokud jsou zaškrtnutá políčka **Použít kód 1 filtru** a **Použít kód filtru 2**, kód filtru 1 i 2 pro zboží se bude muset shodovat s nastavením skupiny filtrů pro vybranou skupinu položek před tím, než bude možné vybrat skupinu filtrů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-167">For example, if the **Use filter code 1** and **Use filter code 2** check boxes are selected, both filter code 1 and filter code 2 of the item must match the setup of the filter group for the item group before the filter group can be selected.</span></span> <span data-ttu-id="8cb1b-168">Když vytvoříte novou položku, vybraná skupina filtrů bude výchozí skupinou filtrů **Skupina 1** a **Skupina 2** na záložce s náhledem **Sklad** podokna **Podrobnosti o vydaném produktu**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-168">When you create a new item, the selected filter group will be the default filter group in the **Group 1** and **Group 2** fields on the **Warehouse** FastTab of the **Released product details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cb1b-169">Kódy filtrů produktů jsou povoleny pouze pro položky, které používají pokročilou správu skladu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-169">Product filter codes are enabled only for items that use advanced warehouse management.</span></span>

## <a name="specify-filter-codes-for-released-products"></a><span data-ttu-id="8cb1b-170">Zadání kódů filtrů pro uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="8cb1b-170">Specify filter codes for released products</span></span>

<span data-ttu-id="8cb1b-171">Tento postup slouží k zadání kódů filtrů pro uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-171">Follow these steps to specify filter codes for released products.</span></span> <span data-ttu-id="8cb1b-172">Například můžete použít kódy filtrů ke seskupení nebezpečných produktů, které kupují konkrétní prodejci.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-172">For example, you can use filter codes to group hazardous products that specific vendors purchase.</span></span>

1. <span data-ttu-id="8cb1b-173">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-173">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8cb1b-174">V podokně akcí vyberte možnost **Nový** a vytvořte produkt.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-174">On the Action Pane, select **New** to create a product.</span></span>
1. <span data-ttu-id="8cb1b-175">V dialogovém okně **Nově vydaný produkt** zadejte data, která jsou nutná k vytvoření základny nového produktu, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-175">In the **New released product** dialog box, enter the data that is required to create the base of a new product, and then select **OK**.</span></span>

    <span data-ttu-id="8cb1b-176">Kódy filtrů produktů nejsou povoleny, pokud skupina položek připojená k produktu nebyla nakonfigurována pro kódy filtrů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-176">Product filter codes aren't enabled unless the item group that is attached to the product has been configured for filter codes.</span></span>

    <span data-ttu-id="8cb1b-177">Další informace naleznete v tématu [Vytvoření nového produktu](../pim/tasks/create-new-product.md).</span><span class="sxs-lookup"><span data-stu-id="8cb1b-177">For more information, see [Create a new product](../pim/tasks/create-new-product.md).</span></span>

1. <span data-ttu-id="8cb1b-178">Na kartě s náhledem **Sklad** v části **Kódy filtru produktu** vyberte kódy filtrů pro pole **Kód 1** až **Kód 10**, jak je požadováno k určení kódů filtru pro produkt.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-178">On the **Warehouse** FastTab, in the **Product filter codes** section, select filter codes for the **Code 1** through **Code 10** fields, as required, to specify filter codes for the product.</span></span>

## <a name="set-up-generally-available-items"></a><span data-ttu-id="8cb1b-179">Nastavení obecně dostupných položek</span><span class="sxs-lookup"><span data-stu-id="8cb1b-179">Set up generally available items</span></span>

<span data-ttu-id="8cb1b-180">Můžete zpřístupnit konkrétny skladové položky pouze pro odběratele, dodavatele nebo pro odběratele i dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-180">You can make specific inventory items available only for customers, only for vendors, or for both customers and vendors.</span></span>

> [!NOTE]
> <span data-ttu-id="8cb1b-181">Na všechny položky, které nastavíte jako obecně dostupné, se nevztahují filtry odběratelů ani filtry dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-181">Customer and vendor filters don't apply to any item that is set up as generally available.</span></span>

<span data-ttu-id="8cb1b-182">Chcete-li nastavit obecně dostupné položky postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-182">To set up generally available items, follow these steps.</span></span>

1. <span data-ttu-id="8cb1b-183">Jděte na **Řízení skladu \> Nastavení \> Filtry produktu \> Obecně dostupné produkty**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-183">Go to **Warehouse management \> Setup \> Product filters \> Generally available products**.</span></span>
1. <span data-ttu-id="8cb1b-184">V podokně akcí vyberte možnost **Nový** a vytvořte záznam.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-184">On the Action Pane, select **New** to create a record.</span></span>
1. <span data-ttu-id="8cb1b-185">V poli **Odběratel nebo dodavatel** vyberte *Odběratel*, *Dodavatel* nebo *Vše* ke zpřístupnění položek pro odběratele, dodavatele nebo obojí.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-185">In the **Customer or vendor** field, select *Customer*, *Vendor*, or *All* to make the items available for customers, vendors, or both.</span></span>
1. <span data-ttu-id="8cb1b-186">V poli **Počáteční datum / čas** zadejte datum a čas, kdy bude položka k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-186">In the **Start date/time** field, enter the date and time when the item will become available.</span></span>
1. <span data-ttu-id="8cb1b-187">V poli **Skupina položky** vyberte skupinu zboží.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-187">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="8cb1b-188">V polích **Kód 1** až **Kód 10** vyberte kódy filtrů pro omezení položek, které jsou obecně dostupné.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-188">In the **Code 1** through **Code 10** fields, select the filter codes to limit the items that are generally available.</span></span>

    <span data-ttu-id="8cb1b-189">Při výběru skupiny položek nastavíte tuto skupinu položek veřejně přístupnou.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-189">When you select an item group, you set that group of items as generally available.</span></span> <span data-ttu-id="8cb1b-190">Výběrem kódů filtrů v těchto položkách omezíte obecně dostupné položky.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-190">By selecting filter codes in these fields, you limit the items that are available.</span></span>

## <a name="set-up-customer-product-filters"></a><span data-ttu-id="8cb1b-191">Nastavení filtrů produktů zákazníků</span><span class="sxs-lookup"><span data-stu-id="8cb1b-191">Set up customer product filters</span></span>

<span data-ttu-id="8cb1b-192">Tato volitelná procedura popisuje postup určení zboží, které má být k dispozici pro odběratele navíc ke zboží, které je dostupné prostřednictvím nastavení filtru na stránce **Obecně dostupné zboží**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-192">You can use this optional procedure to specify items that should be available for a customer in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="8cb1b-193">Můžete nastavit více filtrů pro jednoho odběratele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-193">You can set up multiple filters for a single customer.</span></span>

<span data-ttu-id="8cb1b-194">Chcete-li nastavit kódy filtru odběratele, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-194">To set up customer filter codes, follow these steps.</span></span>

1. <span data-ttu-id="8cb1b-195">Přejděte na **Prodej a marketing \> Odběratelé \> Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-195">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="8cb1b-196">Vyberte odběratele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-196">Select a customer.</span></span>
1. <span data-ttu-id="8cb1b-197">V podokně Akce na kartě **Zákazník** ve skupině **Nastavení** zvolte **Filtry produktu**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-197">On the Action Pane, on the **Customer** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="8cb1b-198">Na stránce **Kódy filtrů produktu** v podokně Akce vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-198">On the **Product filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8cb1b-199">V poli **Počáteční datum / čas** a **Koncové datum / čas** zadejte počáteční a koncové datum pro vybranou skupinu položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-199">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="8cb1b-200">V poli **Skupina položky** vyberte skupinu zboží.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-200">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="8cb1b-201">V poli **Kód 1** až **Kód 10** vyberte kódy filtrů, které chcete použít jako kritéria k omezení položek, které jsou k dispozici zákazníkům ve vybrané skupině položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-201">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for customers in the selected item group.</span></span> <span data-ttu-id="8cb1b-202">Musíte provést výběr pro každý kód filtru, který je nastaven pro skupinu položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-202">You must make a selection for every filter code that is set up for the item group.</span></span>

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a><span data-ttu-id="8cb1b-203">Nastavení filtrů produktů dodavatelů</span><span class="sxs-lookup"><span data-stu-id="8cb1b-203">Set up vendor product filters</span></span>

<span data-ttu-id="8cb1b-204">Tato volitelná procedura popisuje postup určení zboží, které má být k dispozici pro dodavatele navíc ke zboží, které je dostupné prostřednictvím nastavení filtru na stránce **Obecně dostupné zboží**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-204">You can use this optional procedure to specify items that should be available for a vendor in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="8cb1b-205">Můžete nastavit více filtrů pro jednoho dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-205">You can set up multiple filters for a single vendor.</span></span>

<span data-ttu-id="8cb1b-206">Chcete-li nastavit kódy filtru dodavatele, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-206">To set up vendor filter codes, follow these steps.</span></span>

1. <span data-ttu-id="8cb1b-207">Přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-207">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="8cb1b-208">Vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-208">Select a vendor.</span></span>
1. <span data-ttu-id="8cb1b-209">V podokně Akce na kartě **Dodavatel** ve skupině **Nastavení** zvolte **Filtry produktu**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-209">On the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="8cb1b-210">Na stránce **Kódy filtrů** v podokně Akce vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-210">On the **Filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8cb1b-211">V poli **Počáteční datum / čas** a **Koncové datum / čas** zadejte počáteční a koncové datum pro vybranou skupinu položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-211">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="8cb1b-212">V poli **Skupina položky** vyberte skupinu zboží.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-212">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="8cb1b-213">V poli **Kód 1** až **Kód 10** vyberte kódy filtrů, které chcete použít jako kritéria k omezení položek, které jsou k dispozici dodavatelům ve vybrané skupině položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-213">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for vendors in the selected item group.</span></span> <span data-ttu-id="8cb1b-214">Musíte provést výběr pro každý kód filtru, který je nastaven pro skupinu položek.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-214">You must make a selection for every filter code that is set up for the item group.</span></span>

> [!NOTE]
> <span data-ttu-id="8cb1b-215">Nastavení filtrů produktů dodavatele se vztahuje na vydané produkty, kde jsou pro příslušnou skupinu dimenzí úložiště povoleny procesy správy skladu.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-215">The setup of vendor product filters applies to released products where warehouse management processes are enabled for the associated storage dimension group.</span></span> <span data-ttu-id="8cb1b-216">Kódy filtru se používají k určení, zda systém umožní uživatelům koupit danou položku od daného dodavatele, když vytvoří řádky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-216">The filter codes are used to determine whether the system will allow users to purchase a given item from a given vendor when they create purchase order lines.</span></span> <span data-ttu-id="8cb1b-217">Microsoft Dynamics 365 Supply Chain Management má dvě metody pro zacházení se schválením dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-217">Microsoft Dynamics 365 Supply Chain Management has two methods for handling vendor approval.</span></span> <span data-ttu-id="8cb1b-218">Pokud existuje jeden nebo více vydaných produktů, kde je pole **Schválená metoda kontroly dodavatele** nastaveno na *Pouze varování* nebo *Nepovoleno*, pro tyto položky lze povolit obě metody schválení dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-218">If one or more released products exist where the **Approved vendor check method** field is set to *Warning only* or *Not allowed*, both vendor approval methods could be enabled for those items.</span></span> <span data-ttu-id="8cb1b-219">Tato situace může způsobit problémy, když uživatelé vytvoří řádky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-219">This situation might cause issues when users create purchase order lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cb1b-220">Viz také</span><span class="sxs-lookup"><span data-stu-id="8cb1b-220">See also</span></span>

[<span data-ttu-id="8cb1b-221">Další informace najdete v příspěvku na blogu WMS-Warehouse Filter Codes</span><span class="sxs-lookup"><span data-stu-id="8cb1b-221">For more information see the blog post WMS-Warehouse Filter Codes</span></span>](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)