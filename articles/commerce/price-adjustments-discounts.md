---
title: Úpravy ceny a slevy
description: Tento článek obsahuje informace o úpravách cen a slev v aplikaci Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240935"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="6c5cb-103">Úpravy ceny a slevy</span><span class="sxs-lookup"><span data-stu-id="6c5cb-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c5cb-104">Tento článek obsahuje informace o úpravách cen a slev v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6c5cb-105">V aplikaci Commerce můžete provést úpravy cen produktů a také nastavit slevy, které jsou použity pro položku řádku nebo transakci na pokladním místě (POS), v prodejní objednávce kontaktního střediska nebo v online objednávce.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="6c5cb-106">Úpravy ceny i slevy lze propojit s cenovými skupinami.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="6c5cb-107">Pro úpravy ceny a slevy můžete určit jedno počáteční a koncové datum nebo opakované období, kód slevy a další atributy.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="6c5cb-108">Úpravy ceny a slevy lze použít pro produkty, varianty nebo kategorie.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="6c5cb-109">Pokud je pro produkt platná více než jedna sleva, odběratel může obdržet buď jednu ze slev nebo kombinovanou slevu, a to v závislosti na konfiguraci slevy.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="6c5cb-110">Commerce automaticky použije slevu nebo kombinaci slevy, jež nabízí nejlepší cenu pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="6c5cb-111">Při nastavení úpravy ceny nebo slevy je nutné zkontrolovat, zda jsou cenové skupiny přiřazeny pro správné kanály, katalogy, umístění nebo věrnostní programy, u kterých mají být použity slevy.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="6c5cb-112">Dále, pokud potřebujete automaticky vygenerovat ID slevy, můžete před definováním nové slevy nebo úpravy ceny nastavit číselné řady na stránce **Parametry obchodu**.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="6c5cb-113">Úpravu ceny nebo slevu můžete odstranit.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="6c5cb-114">Dojde však ke ztrátě statistických údajů.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="6c5cb-115">Typy slev</span><span class="sxs-lookup"><span data-stu-id="6c5cb-115">Types of discounts</span></span>

<span data-ttu-id="6c5cb-116">Existují mnoho typů slev:</span><span class="sxs-lookup"><span data-stu-id="6c5cb-116">There are many types of discounts:</span></span>

- <span data-ttu-id="6c5cb-117">**Jednoduchá sleva** – jedno procento nebo částka.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="6c5cb-118">**Množstevní sleva** – sleva, která se použije při zakoupení dvou nebo více produktů.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="6c5cb-119">**Kombinační sleva** – sleva je uplatněna v případě, že se zakoupí určitá kombinace položek.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="6c5cb-120">**Mezní sleva** – sleva, která se použije, když celková částka transakce je větší než zadaná částka.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="6c5cb-121">**Slevy založené na úhradě** – Sleva, která se použije, když celková částka transakce přesáhne stanovenou částku a pro platbu se použije určitý typ platby (například hotovost, kreditní nebo debetní karta).</span><span class="sxs-lookup"><span data-stu-id="6c5cb-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="6c5cb-122">**Přepravní sleva** – Sleva, která se použije, když celková částka transakce přesáhne zadanou částku a na objednávku se použije určitý způsob doručení (například dvoudenní nebo noční přeprava).</span><span class="sxs-lookup"><span data-stu-id="6c5cb-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="6c5cb-123">Úpravy ceny i slevy lze propojit s cenovými skupinami.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="6c5cb-124">Skupiny cen lze pak přidružit s kanály, katalogy, umístěním a věrnostními programy.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="6c5cb-125">Kombinační sleva a mezní sleva mají vlastnosti s názvem „Započítat produkty bez slevy“ a „Započítat produkty bez slevy do mezní hodnoty“.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="6c5cb-126">Pokud jsou tyto vlastnosti povoleny, položka, která nemá nárok na žádnou slevu, může stále pomoci kvalifikovat transakci k udělení slevy, ale nezpůsobilá položka slevu nezíská.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="6c5cb-127">Například pokud vytvoříte kombinační slevu se dvěma řádky A a B, kde by měl zákazník získat slevu 10% na obě položky, ale položka A má zaškrtnutou konfiguraci „Zabránit všem slevám“, pak by obvykle položka A do slevy zahrnuta nebyla.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="6c5cb-128">Pokud je však povolena vlastnost „Započítat produkty bez slevy“, lze položku A použít k získání kombinační slevy, ale 10% sleva se použije pouze na položku B. Podobná logika platí i pro mezní slevu.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="6c5cb-129">Vlastnost „Započítat produkty bez slevy do mezní hodnoty“ má však ve srovnání s vlastností „Započítat produkty bez slevy“ kombinační slevy další schopnost.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="6c5cb-130">Pokud je povolena mezní sleva a pokud existuje položka, která má existující slevu, která by bránila položce v jakýchkoli jiných slevách, pak by cena zaplacená za tuto položku způsobila splnění mezní hodnoty, ale tato položka nedostane další slevu.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
