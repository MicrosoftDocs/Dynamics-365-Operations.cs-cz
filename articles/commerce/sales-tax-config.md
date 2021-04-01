---
title: Konfigurace DPH pro online objednávky
description: Tohle téma poskytuje přehled o výběru skupiny DPH pro různé typy online objednávek v Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254834"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="4d7ef-103">Konfigurace DPH pro online objednávky</span><span class="sxs-lookup"><span data-stu-id="4d7ef-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d7ef-104">Tohle téma poskytuje přehled o výběru skupiny DPH pro různé typy online objednávek.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="4d7ef-105">Pro svůj kanál elektronického obchodování možná bude chtít podporu možností, jako je doručení nebo vyzvednutí online objednávek.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="4d7ef-106">Uplatnění DPH závisí na možnosti vybrané vašimi online uživateli.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="4d7ef-107">Když se zákazník webu rozhodne koupit položku online a odešle ji na adresu, DPH se určí na základě nastavení daňové skupiny pro dodací adresu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="4d7ef-108">Když se zákazník rozhodne vyzvednout si zakoupenou položku v obchodě, DPH se určí na základě nastavení daňové skupiny obchodu pro vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="4d7ef-109">Objednávky odeslané na adresu zákazníka</span><span class="sxs-lookup"><span data-stu-id="4d7ef-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="4d7ef-110">Obecně jsou daně u online objednávek, které jsou dodávány na adresy zákazníků, definovány podle cílového místa.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="4d7ef-111">Každá skupina DPH má konfiguraci daně na základě cílového místa maloobchodu, ve které může vaše firma v hierarchické podobě definovat podrobnosti o cílovém místě, jako je kraj/oblast, stát, kraj a město.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="4d7ef-112">Když je zadána online objednávka, daňový modul Commerce použije dodací adresu každé řádkové položky v objednávce a vyhledá skupiny DPH s odpovídajícími cílovými daňovými kritérii.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="4d7ef-113">Například u online objednávky s dodací adresou řádkové položky do San Franciska v Kalifornii vyhledá daňový modul skupinu DPH a kód DPH pro Kalifornii a poté odpovídajícím způsobem vypočítá daň pro každou řádkovou položku.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="4d7ef-114">Zákaznické daňové skupiny</span><span class="sxs-lookup"><span data-stu-id="4d7ef-114">Customer-based tax groups</span></span>

<span data-ttu-id="4d7ef-115">V centrále Commerce existují dvě místa, kde jsou nakonfigurovány daňové skupiny pro zákazníky:</span><span class="sxs-lookup"><span data-stu-id="4d7ef-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="4d7ef-116">**Profil zákazníka**</span><span class="sxs-lookup"><span data-stu-id="4d7ef-116">**Customer's profile**</span></span>
- <span data-ttu-id="4d7ef-117">**Dodací adresa zákazníka**</span><span class="sxs-lookup"><span data-stu-id="4d7ef-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="4d7ef-118">Když má profil zákazníka nakonfigurovanou daňovou skupinu</span><span class="sxs-lookup"><span data-stu-id="4d7ef-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="4d7ef-119">Záznam profilu zákazníka v centrále může mít nakonfigurovanou skupinu DPH, ale u online objednávek nebude skupinu DPH nakonfigurovanou v profilu zákazníka daňový modul používat.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="4d7ef-120">Když má dodací adresa zákazníka nakonfigurovanou daňovou skupinu</span><span class="sxs-lookup"><span data-stu-id="4d7ef-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="4d7ef-121">Pokud má záznam dodací adresy zákazníka nakonfigurovanou daňovou skupinu a online objednávka (nebo řádková položka) je odeslána na dodací adresu zákazníka, daňová skupina nakonfigurovaná v záznamu adresy zákazníka bude použita daňovým modulem pro výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="4d7ef-122">Konfigurace daňové skupiny pro záznam dodací adresy zákazníka</span><span class="sxs-lookup"><span data-stu-id="4d7ef-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="4d7ef-123">Chcete-li nakonfigurovat daňovou skupinu pro záznam dodací adresy zákazníka v centrále Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4d7ef-124">Jděte na **Všichni zákazníci** a poté vyberte požadovaného zákazníka.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="4d7ef-125">Na záložce s náhledem **Adresy** vyberte požadovanou adresu a poté vyberte **Další možnosti \> Rozšířené**.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="4d7ef-126">Na kartě **Obecné** na stránce **Spravovat adresy** podle potřeby nastavte hodnotu DPH.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="4d7ef-127">Daňová skupina je definována pomocí doručovací adresy řádku objednávky a daně založené na cílovém umístění se konfigurují u samotné daňové skupiny.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="4d7ef-128">Další informace viz [Nastavení daní pro online obchody podle cílového místa](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="4d7ef-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="4d7ef-129">Vyzvednutí objednávky v obchodě</span><span class="sxs-lookup"><span data-stu-id="4d7ef-129">Order pickup in store</span></span>

<span data-ttu-id="4d7ef-130">U řádků objednávky se zadaným vyzvednutím v obchodě nebo pouličním výdejem se použije daňová skupina z vybraného obchodu pro vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="4d7ef-131">Podrobnosti, jak konfigurovat daňovou skupinu pro daný obchod, viz [Nastavení dalších daňových možností pro obchody](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="4d7ef-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="4d7ef-132">Když je řádek objednávky vyzvednut v obchodě, daňový modul bude ignorovat nastavení daně z adresy zákazníka (pokud je nastaveno) a použije se konfigurace daně obchodu pro vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4d7ef-133">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4d7ef-133">Additional resources</span></span>

[<span data-ttu-id="4d7ef-134">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="4d7ef-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="4d7ef-135">Metody výpočtu DPH v poli Zdroj</span><span class="sxs-lookup"><span data-stu-id="4d7ef-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="4d7ef-136"> Přiřazení a přepsání DPH</span><span class="sxs-lookup"><span data-stu-id="4d7ef-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="4d7ef-137">Možnosti výpočtu celé částky a intervalu pro kódy daně z prodeje</span><span class="sxs-lookup"><span data-stu-id="4d7ef-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="4d7ef-138">Výpočet osvobození od daně</span><span class="sxs-lookup"><span data-stu-id="4d7ef-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]