---
title: Úpravy ceny a slevy
description: Tento článek obsahuje informace o úpravách cen a slev v aplikaci Microsoft Dynamics 365 for Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549445"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="dbd60-103">Úpravy ceny a slevy</span><span class="sxs-lookup"><span data-stu-id="dbd60-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dbd60-104">Tento článek obsahuje informace o úpravách cen a slev v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="dbd60-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="dbd60-105">V aplikaci Dynamics 365 for Retail můžete provést úpravy cen produktů a také nastavit slevy, které jsou použity pro položku řádku nebo transakci na pokladním místě (POS), v prodejní objednávce kontaktního střediska nebo v online objednávce.</span><span class="sxs-lookup"><span data-stu-id="dbd60-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="dbd60-106">Úpravy ceny i slevy lze propojit s cenovými skupinami.</span><span class="sxs-lookup"><span data-stu-id="dbd60-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="dbd60-107">Pro úpravy ceny a slevy můžete určit jedno počáteční a koncové datum nebo opakované období, kód slevy a další atributy.</span><span class="sxs-lookup"><span data-stu-id="dbd60-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="dbd60-108">Úpravy ceny a slevy lze použít pro produkty, varianty nebo kategorie.</span><span class="sxs-lookup"><span data-stu-id="dbd60-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="dbd60-109">Pokud je pro produkt platná více než jedna sleva, odběratel může obdržet buď jednu ze slev nebo kombinovanou slevu, a to v závislosti na konfiguraci slevy.</span><span class="sxs-lookup"><span data-stu-id="dbd60-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="dbd60-110">Dynamics 365 for Retail automaticky použije slevu nebo kombinaci slevy, jež nabízí nejlepší cenu pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="dbd60-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="dbd60-111">Při nastavení úpravy ceny nebo slevy je nutné zkontrolovat, zda jsou cenové skupiny přiřazeny pro správné kanály, katalogy, umístění nebo věrnostní programy, u kterých mají být použity slevy.</span><span class="sxs-lookup"><span data-stu-id="dbd60-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="dbd60-112">Dále, pokud potřebujete automaticky vygenerovat ID slevy, můžete před definováním nové slevy nebo úpravy ceny nastavit číselné řady na stránce **Parametry maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="dbd60-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="dbd60-113">Úpravu ceny nebo slevu můžete odstranit.</span><span class="sxs-lookup"><span data-stu-id="dbd60-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="dbd60-114">Dojde však ke ztrátě statistických údajů.</span><span class="sxs-lookup"><span data-stu-id="dbd60-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="dbd60-115">Typy slev</span><span class="sxs-lookup"><span data-stu-id="dbd60-115">Types of discounts</span></span>

<span data-ttu-id="dbd60-116">Existují čtyři typy maloobchodních slev:</span><span class="sxs-lookup"><span data-stu-id="dbd60-116">There are four types of retail discounts:</span></span>

- <span data-ttu-id="dbd60-117">**Jednoduchá sleva** – jedno procento nebo částka.</span><span class="sxs-lookup"><span data-stu-id="dbd60-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="dbd60-118">**Množstevní sleva** – sleva, která se použije při zakoupení dvou nebo více produktů.</span><span class="sxs-lookup"><span data-stu-id="dbd60-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="dbd60-119">**Kombinační sleva** – sleva je uplatněna v případě, že se zakoupí určitá kombinace položek.</span><span class="sxs-lookup"><span data-stu-id="dbd60-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="dbd60-120">**Mezní sleva** – sleva, která se použije, když celková částka transakce je větší než zadaná částka.</span><span class="sxs-lookup"><span data-stu-id="dbd60-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="dbd60-121">Úpravy ceny i slevy lze propojit s cenovými skupinami.</span><span class="sxs-lookup"><span data-stu-id="dbd60-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="dbd60-122">Skupiny cen lze pak přidružit s kanály, katalogy, umístěním a věrnostními programy.</span><span class="sxs-lookup"><span data-stu-id="dbd60-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
