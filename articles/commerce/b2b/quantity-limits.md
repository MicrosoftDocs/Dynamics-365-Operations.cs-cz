---
title: Nastavte limity množství produktů pro weby B2B elektronického obchodování
description: Toto téma popisuje, jak nastavit limity množství produktu pro weby elektronického obchodování typu business-to-business (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211170"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="45644-103">Nastavte limity množství produktů pro weby B2B elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="45644-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45644-104">Toto téma popisuje, jak nastavit limity množství produktu pro weby elektronického obchodování typu business-to-business (B2B).</span><span class="sxs-lookup"><span data-stu-id="45644-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="45644-105">Většina produktů má měrnou jednotku, která definuje jejich seskupení.</span><span class="sxs-lookup"><span data-stu-id="45644-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="45644-106">Seskupení ovlivňuje způsob prodeje produktů.</span><span class="sxs-lookup"><span data-stu-id="45644-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="45644-107">Některé produkty mohou mít další seskupení pro množství.</span><span class="sxs-lookup"><span data-stu-id="45644-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="45644-108">Toto seskupení určuje, zda lze produkty prodávat jako jednotlivé jednotky nebo násobky a zda existuje minimální nebo maximální limit množství objednávky, který je třeba dodržet.</span><span class="sxs-lookup"><span data-stu-id="45644-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="45644-109">Funkce omezení množství zajišťuje, že minimální, maximální, vícenásobné a standardní množství je nakonfigurováno v Microsoft Dynamics 365 Commerce (ve výchozím nastavení objednávky nebo nastavení webu konfigurátoru webu Commerce) se použijí na objednávky zákazníků, které jsou umístěny na webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="45644-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="45644-110">Omezení množství produktů nejsou aktuálně podporována pro pokladní místa (POS) a kontaktní střediska.</span><span class="sxs-lookup"><span data-stu-id="45644-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="45644-111">Celá řada maloobchodních prodejců poskytuje možnost objednávek odběratele (neboli speciálních objednávek), aby splnili různé požadavky týkající se produktu a plnění.</span><span class="sxs-lookup"><span data-stu-id="45644-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="45644-112">Zde jsou některé typické scénáře:</span><span class="sxs-lookup"><span data-stu-id="45644-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="45644-113">Zákazník chce, aby se produkty konkrétních variant prodávaly ve velkém množství.</span><span class="sxs-lookup"><span data-stu-id="45644-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="45644-114">Zákazník chce vyzvednout výrobky ve skladu nebo z místa, které se liší od skladu nebo místa, kde zákazník tyto produkty zakoupil.</span><span class="sxs-lookup"><span data-stu-id="45644-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="45644-115">Standardy balení pro obchody se však liší od standardů balení pro distribuci online prodeje.</span><span class="sxs-lookup"><span data-stu-id="45644-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="45644-116">Zákazník chce koupit limitovaný produkt, který má maximální limit množství pro položky, které lze zakoupit.</span><span class="sxs-lookup"><span data-stu-id="45644-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="45644-117">V centrále Commerce zapněte funkci výchozího nastavení objednávky</span><span class="sxs-lookup"><span data-stu-id="45644-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="45644-118">Než budete moci nastavit limity množství produktu, musí být v centrále Commerce zapnuta funkce výchozího nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="45644-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="45644-119">Pomocí následujících kroků zapněte funkci výchozího nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="45644-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="45644-120">Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="45644-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="45644-121">Najděte a vyberte funkci **Podpora nastavení webu a výchozího nastavení v objednávce zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="45644-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="45644-122">V dolní části pravého podokna vyberte **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="45644-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="45644-123">Definujte nastavení množství</span><span class="sxs-lookup"><span data-stu-id="45644-123">Define quantity settings</span></span> 

<span data-ttu-id="45644-124">Výchozí množství můžete definovat na stránce **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="45644-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="45644-125">Chcete-li definovat nastavení množství, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="45644-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="45644-126">Přejděte do nabídky **Retail a Commerce \> Produkty a kategorie \> Uvolněné produkty podle kategorie**.</span><span class="sxs-lookup"><span data-stu-id="45644-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="45644-127">Vyberte uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="45644-127">Select a released product.</span></span>
1. <span data-ttu-id="45644-128">V podokně akcí, na kartě **Spravovat sklad**, ve skupině **Nastavení objednávky**, vyberte **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="45644-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="45644-129">Na stránce **Výchozí nastavení objednávky**, na pevné záložce **Prodejní objednávka**, v sekci **Množství prodeje** nastavte množství prodeje produktu:</span><span class="sxs-lookup"><span data-stu-id="45644-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="45644-130">**Násobek** - Množství, ve kterém lze produkt zakoupit v násobcích.</span><span class="sxs-lookup"><span data-stu-id="45644-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="45644-131">**Minimální množství pro objednání** - Minimální počet produktů, které je třeba zakoupit.</span><span class="sxs-lookup"><span data-stu-id="45644-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="45644-132">**Maximální množství pro objednání** - Maximální počet produktů, které je možné zakoupit.</span><span class="sxs-lookup"><span data-stu-id="45644-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="45644-133">**Standardní objednané množství** - Výchozí množství, které se automaticky zadá při výběru produktu.</span><span class="sxs-lookup"><span data-stu-id="45644-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="45644-134">Zapněte funkci omezení počtu objednávek B2B v konfigurátoru webů Commerce</span><span class="sxs-lookup"><span data-stu-id="45644-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="45644-135">Chcete-li zapnout funkci omezení počtu objednávek B2B v konfigurátoru webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="45644-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="45644-136">Přejděte na **Nastavení webu \> Rozšíření**</span><span class="sxs-lookup"><span data-stu-id="45644-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="45644-137">V **Povolit limity množství objednávky** vyberte **Povoleno pro zákazníky B2B** v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="45644-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="45644-138">Aktualizované nastavení konfigurátoru webu se projeví až po aktualizaci souboru app.settings.json.</span><span class="sxs-lookup"><span data-stu-id="45644-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="45644-139">Další informace viz [Aktualizace knihoven SDK a modulů](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="45644-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45644-140">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="45644-140">Additional resources</span></span>

[<span data-ttu-id="45644-141">Nastavení webu elektronického obchodování B2B</span><span class="sxs-lookup"><span data-stu-id="45644-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="45644-142">Vytvářejte hierarchie modelování org pro organizace B2B</span><span class="sxs-lookup"><span data-stu-id="45644-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="45644-143">Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B</span><span class="sxs-lookup"><span data-stu-id="45644-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="45644-144">Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B</span><span class="sxs-lookup"><span data-stu-id="45644-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]