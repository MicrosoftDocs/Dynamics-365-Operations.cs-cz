---
title: Sledování průběžných průměrných nákladů pro dimenzi zboží
description: Každá skladová položka má přiřazenou skupinu dimenzí zásob. Průběžná průměrná nákladová cena položky je tedy vypočtena na základě výběru dimenzí zásob, které jsou finančně sledovány.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8da13a01b28ca09ce9c29ecd3a9342dfb9eaa4bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834306"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="594cf-104">Sledování průběžných průměrných nákladů pro dimenzi zboží</span><span class="sxs-lookup"><span data-stu-id="594cf-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="594cf-105">Každá skladová položka má přiřazenou skupinu dimenzí zásob.</span><span class="sxs-lookup"><span data-stu-id="594cf-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="594cf-106">Průběžná průměrná nákladová cena položky je tedy vypočtena na základě výběru dimenzí zásob, které jsou finančně sledovány.</span><span class="sxs-lookup"><span data-stu-id="594cf-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="594cf-107">Existují tři typy dimenzí zásob: produkty, skladiště a sledování.</span><span class="sxs-lookup"><span data-stu-id="594cf-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="594cf-108">Dimenze produktu zahrnují konfiguraci, velikost a barvu.</span><span class="sxs-lookup"><span data-stu-id="594cf-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="594cf-109">Dimenze produktu jsou vždy finančně sledovány.</span><span class="sxs-lookup"><span data-stu-id="594cf-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="594cf-110">Naproti tomu dimenze uskladnění a sledování zahrnují pracoviště, sklad, umístění, stav zásob, registrační značku, číslo dávky a sériové číslo.</span><span class="sxs-lookup"><span data-stu-id="594cf-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="594cf-111">Můžete vybrat, které dimenze uskladnění a sledování budou finančně sledovány.</span><span class="sxs-lookup"><span data-stu-id="594cf-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="594cf-112">**Příklad 1**</span><span class="sxs-lookup"><span data-stu-id="594cf-112">**Example 1**</span></span> 

<span data-ttu-id="594cf-113">Pokud je u skupiny dimenzí úložiště, která je připojena k položce, finančně sledován sklad, bude průběžná průměrná nákladová cena vypočtena pro každý sklad.</span><span class="sxs-lookup"><span data-stu-id="594cf-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="594cf-114">Byly fakturovány následující nákupní objednávky:</span><span class="sxs-lookup"><span data-stu-id="594cf-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="594cf-115">Nákupní objednávka na 2 kusy v ceně 10,00 USD byla fakturována pro sklad GW.</span><span class="sxs-lookup"><span data-stu-id="594cf-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="594cf-116">Nákupní objednávka na 3 kusy v ceně 12,00 USD byla fakturována pro sklad GW.</span><span class="sxs-lookup"><span data-stu-id="594cf-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="594cf-117">Nákupní objednávka na 5 kusy v ceně 15,00 USD byla fakturována pro sklad MW.</span><span class="sxs-lookup"><span data-stu-id="594cf-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="594cf-118">Průběžná průměrná nákladová cena ve skladu GW činí 11,20 USD a průběžná průměrná nákladová cena ve skladu MW činí 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="594cf-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="594cf-119">K zaúčtování faktury prodejní objednávky dojde pro sklad GW.</span><span class="sxs-lookup"><span data-stu-id="594cf-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="594cf-120">Hodnota zásob a náklady prodaného zboží (před provedením uzávěrky skladu a bez označení) činí 11,20 USD.</span><span class="sxs-lookup"><span data-stu-id="594cf-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="594cf-121">Dojde k zaúčtování faktury další prodejní objednávky pro sklad MW.</span><span class="sxs-lookup"><span data-stu-id="594cf-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="594cf-122">Hodnota zásob a náklady prodaného zboží (před provedením uzávěrky skladu a bez označení) činí 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="594cf-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="594cf-123">**Příklad 2** Jestliže skupina dimenzí úložiště, která je připojena k položce, je finančně sledována podle skladu, a skupina sledovacích dimenzí je finančně sledována podle čísla dávky, bude průběžná průměrná nákladová cena vypočtena pro každou dávku.</span><span class="sxs-lookup"><span data-stu-id="594cf-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="594cf-124">**Poznámka:** Doporučujeme vždy zobrazit nákladovou cenu se všemi finančními dimenzemi, které se u položky sledují.</span><span class="sxs-lookup"><span data-stu-id="594cf-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="594cf-125">Byly fakturovány následující nákupní objednávky:</span><span class="sxs-lookup"><span data-stu-id="594cf-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="594cf-126">Nákupní objednávka na 2 kusy v ceně 10,00 USD byla fakturována pro sklad GW a dávku AAA.</span><span class="sxs-lookup"><span data-stu-id="594cf-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="594cf-127">Nákupní objednávka na 3 kusy v ceně 12,00 USD byla fakturována pro sklad GW a dávku AAA.</span><span class="sxs-lookup"><span data-stu-id="594cf-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="594cf-128">Nákupní objednávka na 2 kusy v ceně 15,00 USD byla fakturována pro sklad GW a dávku BBB.</span><span class="sxs-lookup"><span data-stu-id="594cf-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="594cf-129">Průběžná průměrná nákladová cena ve skladu GW a dávce AAA činí 11,20 USD a průběžná průměrná nákladová cena ve skladu GW a dávce BBB činí 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="594cf-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]