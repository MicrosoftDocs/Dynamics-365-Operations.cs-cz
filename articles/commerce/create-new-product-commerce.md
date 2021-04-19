---
title: Vytvoření nového produktu v Commerce
description: Toto téma popisuje, jak vytvořit nový produkt v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 44a58da0be280b06d96cdeae6929042bb50ed4a6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795708"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="9e385-103">Vytvoření nového produktu v Commerce</span><span class="sxs-lookup"><span data-stu-id="9e385-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9e385-104">Toto téma popisuje, jak vytvořit nový produkt v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9e385-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9e385-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="9e385-105">Overview</span></span>

<span data-ttu-id="9e385-106">Produkt je definován především číslem, názvem a popisem.</span><span class="sxs-lookup"><span data-stu-id="9e385-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="9e385-107">Jsou však požadována také další data za účelem popisu produktu nebo služby:</span><span class="sxs-lookup"><span data-stu-id="9e385-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="9e385-108">Vytvoření nového produktu</span><span class="sxs-lookup"><span data-stu-id="9e385-108">Create a new product</span></span>

1. <span data-ttu-id="9e385-109">V navigačním podokně přejděte na **Moduly \> Retail and Commerce \> Produkty a kategorie \> Produkty dle kategorie**.</span><span class="sxs-lookup"><span data-stu-id="9e385-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="9e385-110">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="9e385-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9e385-111">V rozevíracím seznamu **Typ produktu** vyberte **položku** nebo **službu**.</span><span class="sxs-lookup"><span data-stu-id="9e385-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="9e385-112">V rozevíracím seznamu **Podtyp produktu** vyberte možnost **Produkt** (pokud produkt nebude mít žádné varianty) nebo **Základní produkt** (pokud produkt bude mít varianty).</span><span class="sxs-lookup"><span data-stu-id="9e385-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="9e385-113">Do pole **Číslo produktu** zadejte číslo produktu, pokud ještě není předem vyplněno.</span><span class="sxs-lookup"><span data-stu-id="9e385-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="9e385-114">Do pole **Název produktu** zadejte název produktu.</span><span class="sxs-lookup"><span data-stu-id="9e385-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="9e385-115">V poli **Vyhledat název** zadejte název pro vyhledání.</span><span class="sxs-lookup"><span data-stu-id="9e385-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="9e385-116">V rozevíracím seznamu **Maloobchodní kategorie** vyberte příslušnou kategorii.</span><span class="sxs-lookup"><span data-stu-id="9e385-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="9e385-117">Je-li produkt sadou, vyberte **Ano** pro **Produktovou sadu**.</span><span class="sxs-lookup"><span data-stu-id="9e385-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="9e385-118">Je-li dílčím typem produktu základní produkt, nastavte **Skupinu dimenzí produktu** tak, aby zahrnovala podporované varianty.</span><span class="sxs-lookup"><span data-stu-id="9e385-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="9e385-119">Mezi možnosti patří **Barva**, **Vylikost**, **Styl** a **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="9e385-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="9e385-120">V případě potřeby bude pravděpodobně nutné vytvořit další skupiny dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="9e385-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="9e385-121">V rozevíracím seznamu **Techologie konfigurace** vyberte příslušnou možnost.</span><span class="sxs-lookup"><span data-stu-id="9e385-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="9e385-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e385-122">Select **OK**.</span></span>

<span data-ttu-id="9e385-123">Následující obrázek znázorňuje příklad přidaného produktu.</span><span class="sxs-lookup"><span data-stu-id="9e385-123">The following image shows an example product being added.</span></span>

![Vytvoření produktu](media/create-new-product.png)

<span data-ttu-id="9e385-125">Po přidání produktu lze pro něj nastavit další data, například **Popis produktu**, **Skupiny variant**, **Skupiny dimenzí**, **Atributy produktu** a **Související produkty**.</span><span class="sxs-lookup"><span data-stu-id="9e385-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="9e385-126">Následující obrázek znázorňuje další podrobnosti o produktu.</span><span class="sxs-lookup"><span data-stu-id="9e385-126">The following image shows a product's additional details.</span></span>

![Podrobnosti produktu](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="9e385-128">Vytvořit varianty produktů</span><span class="sxs-lookup"><span data-stu-id="9e385-128">Create product variants</span></span>

<span data-ttu-id="9e385-129">Je-li dílčím typem produktu **Základní produkt**, bude nutné vytvořit specifické varianty.</span><span class="sxs-lookup"><span data-stu-id="9e385-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="9e385-130">Při vytváření produktových variant postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9e385-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="9e385-131">V podokně akcí vyberte **Varianty produktu**.</span><span class="sxs-lookup"><span data-stu-id="9e385-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="9e385-132">Pokud byly v podokně akcí vybrány skupiny variant, vyberte možnost \**Návrhy variant*.</span><span class="sxs-lookup"><span data-stu-id="9e385-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="9e385-133">Vyberte varianty, které chcete pro produkt podporovat.</span><span class="sxs-lookup"><span data-stu-id="9e385-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="9e385-134">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="9e385-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="9e385-135">Uvolnění produktu</span><span class="sxs-lookup"><span data-stu-id="9e385-135">Release a product</span></span>

<span data-ttu-id="9e385-136">Při prodeji produktu musí být nejprve uvolněn právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="9e385-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="9e385-137">Na stránce produkt vyberte možnost **Uvolnit produkty**.</span><span class="sxs-lookup"><span data-stu-id="9e385-137">From the product page, select **Release products**.</span></span>

    ![Uvolnit produkt](media/create-new-product-3.png)

1. <span data-ttu-id="9e385-139">Vyberte produkt k uvolnění a pak klikněte na tlačítko **Další**.</span><span class="sxs-lookup"><span data-stu-id="9e385-139">Select the product to release, and then select **Next**.</span></span>

    ![Vyberte produkt k uvolnění](media/create-new-product-4.png)

1. <span data-ttu-id="9e385-141">Vyberte sadu variant produktu k uvolnění a pak klikněte na tlačítko **Další**.</span><span class="sxs-lookup"><span data-stu-id="9e385-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Vyberte varianty k uvolnění](media/create-new-product-5.png)

1. <span data-ttu-id="9e385-143">Vyberte právnickou osobu a poté vyberte možnost **Další**.</span><span class="sxs-lookup"><span data-stu-id="9e385-143">Select the legal entity, and then select **Next**.</span></span>

    ![Zvolte právnickou osobu](media/create-new-product-6.png)

1. <span data-ttu-id="9e385-145">Vyberte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="9e385-145">Select **Finish**.</span></span>

    ![Dokončit uvolnění produktu](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="9e385-147">Konfigurovat uvolněný produkt</span><span class="sxs-lookup"><span data-stu-id="9e385-147">Configure a released product</span></span>

<span data-ttu-id="9e385-148">Jakmile je produkt uvolněn, bude vyžadovat další konfiguraci, která zahrnuje přidání ceny k produktu.</span><span class="sxs-lookup"><span data-stu-id="9e385-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="9e385-149">V navigačním okně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Uvolněné produkty podle kategorie**.</span><span class="sxs-lookup"><span data-stu-id="9e385-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="9e385-150">Vyberte uzel kategorie produktu, který byl uvolněn, a pak vyberte produkt ze seznamu produktů.</span><span class="sxs-lookup"><span data-stu-id="9e385-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="9e385-151">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9e385-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="9e385-152">V části **Nákup** nakonfigurujte všechny požadované vlastnosti včetně **jednotek**, **ceny** a **množství**.</span><span class="sxs-lookup"><span data-stu-id="9e385-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="9e385-153">V podokně akcí vyberte možnost **Ověřit** a zajistěte, aby pro chybějící pole nebyly hlášeny žádné chyby.</span><span class="sxs-lookup"><span data-stu-id="9e385-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="9e385-154">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9e385-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9e385-155">Následující obrázek znázorňuje příklad konfigurace pro uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="9e385-155">The following image shows an example configuration for a released product.</span></span>

![Konfigurovat uvolněný produkt](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="9e385-157">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9e385-157">Additional resources</span></span>

[<span data-ttu-id="9e385-158">Vytvořit právnické osoby</span><span class="sxs-lookup"><span data-stu-id="9e385-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="9e385-159">Vytvoření skupiny variant</span><span class="sxs-lookup"><span data-stu-id="9e385-159">Create a variant group</span></span>](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]