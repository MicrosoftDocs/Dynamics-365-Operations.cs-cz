---
title: Použití nastavení zásob
description: Toto téma se týká nastavení zásob a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fc81c190806a0bdb50569f526589cfa1808ce0c
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417431"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="60807-103">Použití nastavení zásob</span><span class="sxs-lookup"><span data-stu-id="60807-103">Apply inventory settings</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="60807-104">Toto téma se týká nastavení zásob a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="60807-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="60807-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="60807-105">Overview</span></span>

<span data-ttu-id="60807-106">Nastavení zásob určuje, zda se mají zásoby zkontrolovat před přidáním produktů do košíku.</span><span class="sxs-lookup"><span data-stu-id="60807-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="60807-107">Rovněž definují zprávy související se zásobami, například „Na skladě“ a „Zbývá jen několik“.</span><span class="sxs-lookup"><span data-stu-id="60807-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="60807-108">Toto nastavení zajišťuje, že produkt nelze zakoupit, pokud není na skladě.</span><span class="sxs-lookup"><span data-stu-id="60807-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="60807-109">Dynamics 365 Commerce poskytuje odhady dostupnosti produktů na skladě.</span><span class="sxs-lookup"><span data-stu-id="60807-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="60807-110">Informace o tom, jak se vypočítává odhadovaná dostupnost na skladě, viz [Vypočítat dostupnost zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="60807-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="60807-111">V tvůrci webů Commerce lze definovat prahové hodnoty a rozsahy zásob pro produkt nebo kategorii.</span><span class="sxs-lookup"><span data-stu-id="60807-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="60807-112">Určují, zda lze zásoby klasifikovat jako zásoby, nízké zásoby nebo vyprodané.</span><span class="sxs-lookup"><span data-stu-id="60807-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="60807-113">Podrobnosti najdete v tématu [Konfigurace rezervních zásob a úrovní zásob](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="60807-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="60807-114">Nastavení zásob</span><span class="sxs-lookup"><span data-stu-id="60807-114">Inventory settings</span></span>

<span data-ttu-id="60807-115">V Commerce jsou nastavení zásob definována v **Nastavení webu \> Rozšíření \> Řízení zásob** ve tvůrci webu.</span><span class="sxs-lookup"><span data-stu-id="60807-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="60807-116">Existují čtyři nastavení zásob, z nichž jedno je zastaralé:</span><span class="sxs-lookup"><span data-stu-id="60807-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="60807-117">**Povolit kontrolu zásob v aplikaci** - Toto nastavení zapne kontrolu zásob produktu.</span><span class="sxs-lookup"><span data-stu-id="60807-117">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="60807-118">Buy box, nákupní košík a vyzvednutí v modulech obchod pak zkontrolují zásoby produktu a umožní přidání produktu do košíku, pouze pokud je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="60807-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="60807-119">**Úroveň zásob na základě** - Toto nastavení definuje způsob výpočtu úrovní zásob.</span><span class="sxs-lookup"><span data-stu-id="60807-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="60807-120">Dostupné hodnoty jsou **Celkem k dispozici**, **Fyzicky k dispozici** a **Prahová hodnota pro vyprodáno**.</span><span class="sxs-lookup"><span data-stu-id="60807-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="60807-121">V Commerce lze definovat prahové hodnoty a rozsahy zásob pro každý produkt a kategorii.</span><span class="sxs-lookup"><span data-stu-id="60807-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="60807-122">Rozhraní API zásob vracejí informace o zásobách produktů pro majetek **Celkem k dispozici** a **Fyzicky k dispozici**.</span><span class="sxs-lookup"><span data-stu-id="60807-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="60807-123">Prodejce rozhodne, zda hodnota **Celkem k dispozici** nebo **Fyzicky k dispozici** by měla být použita k určení počtu zásob a odpovídajících rozsahů pro stavy na skladě a vyprodáno.</span><span class="sxs-lookup"><span data-stu-id="60807-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="60807-124">Hodnota **Prahová hodnota vyprodáno** nastavení **Úroveň zásob na základě** je zastaralá hodnota.</span><span class="sxs-lookup"><span data-stu-id="60807-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="60807-125">Pokud je vybrána, počet zásob je určen z výsledků hodnoty **Celkem k dispozici**, ale prahová hodnota je definována pomocí numerického nastavení **Prahová hodnota pro vyprodáno**, které je popsáno dále.</span><span class="sxs-lookup"><span data-stu-id="60807-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="60807-126">Toto nastavení prahové hodnoty se vztahuje na všechny produkty na webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="60807-126">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="60807-127">Pokud jsou zásoby pod prahovým číslem, produkt se považuje za vyprodaný.</span><span class="sxs-lookup"><span data-stu-id="60807-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="60807-128">Jinak se to považuje za skladem.</span><span class="sxs-lookup"><span data-stu-id="60807-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="60807-129">Možnosti hodnoty **Prahová hodnota pro vyprodáno** jsou omezené a nedoporučujeme je používat ve verzi 10.0.12 a novější.</span><span class="sxs-lookup"><span data-stu-id="60807-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="60807-130">**Rozsahy zásob** - Toto nastavení definuje rozsahy zásob, pro které se zpráva zobrazuje na modulech webu.</span><span class="sxs-lookup"><span data-stu-id="60807-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="60807-131">Je to použitelné, pouze pokud je vybrána hodnota **Celkem k dispozici** nebo **Fyzicky k dispozici** pro nastavení **Úroveň zásob na základě**.</span><span class="sxs-lookup"><span data-stu-id="60807-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="60807-132">Dostupné hodnoty jsou **Všechno**, **Nízké a vyprodané** a **Vyprodáno**.</span><span class="sxs-lookup"><span data-stu-id="60807-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="60807-133">Je-li vybráno **Všechno**, zobrazí se zprávy pro všechny rozsahy zásob, od skladem (zpráva „Dostupné“) po vyprodáno (zpráva „Není skladem“).</span><span class="sxs-lookup"><span data-stu-id="60807-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="60807-134">Je-li vybráno **Nízké a vyprodané**, zobrazí se zprávy pro všechny rozsahy zásob, kromě skladem (zpráva „Dostupné“).</span><span class="sxs-lookup"><span data-stu-id="60807-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="60807-135">Je-li vybráno **Vyprodáno**, zobrazí se pouze zpráva „Není na skladě“.</span><span class="sxs-lookup"><span data-stu-id="60807-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="60807-136">**Prahová hodnota pro vyprodáno** - Toto staré číselné nastavení se projeví, pouze pokud je vybrána hodnota **Prahová hodnota pro vyprodáno** pro nastavení **Úroveň zásob na základě**.</span><span class="sxs-lookup"><span data-stu-id="60807-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="60807-137">Moduly, které používají nastavení zásob</span><span class="sxs-lookup"><span data-stu-id="60807-137">Modules that use inventory settings</span></span>

<span data-ttu-id="60807-138">Moduly Buy box, seznam přání, volby obchodu, košík a ikona košíku používají nastavení zásob k zobrazení rozsahů zásob a zpráv.</span><span class="sxs-lookup"><span data-stu-id="60807-138">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="60807-139">Následující obrázek ukazuje příklad stránky s podrobnostmi o produktu (PDP), která zobrazuje zprávu na skladě („Dostupné“).</span><span class="sxs-lookup"><span data-stu-id="60807-139">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Příklad modulu PDP, který obsahuje zprávu na skladě](./media/pdp-InStock.png)

<span data-ttu-id="60807-141">Následující obrázek ukazuje příklad stránky s podrobnostmi o produktu (PDP), která zobrazuje zprávu "Vyprodáno".</span><span class="sxs-lookup"><span data-stu-id="60807-141">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Příklad modulu PDP, který obsahuje zprávu vyprodáno](./media/pdp-outofstock.png)

<span data-ttu-id="60807-143">Následující obrázek ukazuje příklad stránky s podrobnostmi o košíku, která zobrazuje zprávu Na skladě ("Dostupné").</span><span class="sxs-lookup"><span data-stu-id="60807-143">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Příklad modulu košíku, který obsahuje zprávu na skladě](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="60807-145">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="60807-145">Additional resources</span></span>

[<span data-ttu-id="60807-146">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="60807-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="60807-147">Konfigurace rezervních zásob a úrovní zásob</span><span class="sxs-lookup"><span data-stu-id="60807-147">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="60807-148">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="60807-148">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="60807-149">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="60807-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="60807-150">Moduly a stránky správy obchodního vztahu</span><span class="sxs-lookup"><span data-stu-id="60807-150">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="60807-151">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="60807-151">Store selector module</span></span>](store-selector.md)