---
title: Vytvoření skupiny variant
description: V tomto tématu je popsán postup při vytvoření skupiny variant velikosti, stylu nebo barev pro produkt v Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001868"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="66238-103">Vytvoření skupiny variant</span><span class="sxs-lookup"><span data-stu-id="66238-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="66238-104">V tomto tématu je popsán postup při vytvoření skupiny variant velikosti, stylu nebo barev pro produkt v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="66238-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="66238-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="66238-105">Overview</span></span>

<span data-ttu-id="66238-106">Dynamics 365 Commerce podporuje více variant produktů.</span><span class="sxs-lookup"><span data-stu-id="66238-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="66238-107">Je ideální pro nastavení skupin variant pro různé kategorie produktů.</span><span class="sxs-lookup"><span data-stu-id="66238-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="66238-108">Skupinu velikostí lze například vytvořit pro trička s velikostí extra small, small, medium, large, and extra large nebo může být vytvořena skupina barev, která obsahuje všechny dostupné barvy produktu.</span><span class="sxs-lookup"><span data-stu-id="66238-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="66238-109">Před přidáním produktů je třeba přidat skupiny variant.</span><span class="sxs-lookup"><span data-stu-id="66238-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="66238-110">V tomto tématu bude vytvořena a konfigurována skupina velikostí.</span><span class="sxs-lookup"><span data-stu-id="66238-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="66238-111">Podobné postupy lze použít pro přidání a konfiguraci skupin stylů a skupin barev.</span><span class="sxs-lookup"><span data-stu-id="66238-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="66238-112">Vytvoření skupiny velikostí</span><span class="sxs-lookup"><span data-stu-id="66238-112">Create a size group</span></span>

<span data-ttu-id="66238-113">Pokud chcete vytvořit skupinu velikostí, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="66238-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="66238-114">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Skupiny variant \> Skupiny velikostí**.</span><span class="sxs-lookup"><span data-stu-id="66238-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="66238-115">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="66238-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="66238-116">Do pole **Skupiny velikostí** zadejte jedinečný název skupiny velikostí.</span><span class="sxs-lookup"><span data-stu-id="66238-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="66238-117">Je-li to nutné, zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="66238-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="66238-118">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="66238-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="66238-119">Přidání atributů do skupiny velikostí</span><span class="sxs-lookup"><span data-stu-id="66238-119">Add attributes to the size group</span></span>

<span data-ttu-id="66238-120">Chcete-li přidat atributy ke skupině velikostí, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="66238-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="66238-121">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Skupiny variant \> Skupiny velikostí**</span><span class="sxs-lookup"><span data-stu-id="66238-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="66238-122">V navigačním podokně vyberte skupinu velikostí.</span><span class="sxs-lookup"><span data-stu-id="66238-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="66238-123">V položce **Řádky skupiny velikostí** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="66238-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="66238-124">Do pole **Velikost** zadejte řetězec přestavující velikost (např. "XL").</span><span class="sxs-lookup"><span data-stu-id="66238-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="66238-125">Do pole **Název velikosti** zadejte název velikosti (například "Extra Large").</span><span class="sxs-lookup"><span data-stu-id="66238-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="66238-126">Do pole **Hmotnost doplnění** zadejte číslo představující hmotnost doplnění.</span><span class="sxs-lookup"><span data-stu-id="66238-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="66238-127">Do pole **číslo v čárovém kódu** zadejte číslo představující čárový kód.</span><span class="sxs-lookup"><span data-stu-id="66238-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="66238-128">V poli **Pořadí zobrazení** zadejte číslo pořadí zobrazení.</span><span class="sxs-lookup"><span data-stu-id="66238-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="66238-129">Po dokončení přidávání velikostí vyberte možnost **Uložit** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="66238-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="66238-130">Následující obrázek znázorňuje příklad skupiny velikostí pro "velikosti volnočasových košil".</span><span class="sxs-lookup"><span data-stu-id="66238-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Vytvoření skupiny velikostí](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="66238-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="66238-132">Additional resources</span></span>

[<span data-ttu-id="66238-133">Přehled informací o produktech</span><span class="sxs-lookup"><span data-stu-id="66238-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="66238-134">Nastavení maloobchodních produktů</span><span class="sxs-lookup"><span data-stu-id="66238-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="66238-135">Dimenze produktu</span><span class="sxs-lookup"><span data-stu-id="66238-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
