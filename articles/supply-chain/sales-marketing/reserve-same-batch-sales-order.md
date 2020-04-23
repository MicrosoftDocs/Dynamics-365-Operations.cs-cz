---
title: Rezervace stejné dávky pro prodejní objednávku
description: Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e101473c5b6958c7e0fb5c5fa80dccd3d9b467
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216015"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="2bdb0-103">Rezervace stejné dávky pro prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="2bdb0-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bdb0-104">Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="2bdb0-105">Rezervace stejné dávky umožňuje rezervovat zásoby pro řádek prodejní objednávky z jediné dávky zásob.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="2bdb0-106">Například zákazník, který si objedná tapetu, může požadovat, aby byla celá objednávka zadána ze stejné dávky nebo šarže, aby se zabránilo nekonzistenci mezi rolemi.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="2bdb0-107">Chcete-li nastavit produkt tak, aby používal rezervaci stejné dávky, musí být aktivní následující nastavení ve skupině modelů zboží, skupině sledovací dimenze a skupině dimenze úložiště, kterou chcete přiřadit k produktu:</span><span class="sxs-lookup"><span data-stu-id="2bdb0-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="2bdb0-108">**Skupiny modelů položek** – Skupina modelů položek musí mít skupinu vybrána pole **Výběr ze stejné dávky** a **Požadavek na konsolidaci** ve skupině polí **Rezervace** pro zásady skladu.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="2bdb0-109">**Skupiny sledovací dimenze** – Skupina sledovací dimenze musí mít vybráno pole **Plán disponibility podle dimenzí** pro číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="2bdb0-110">**Skupiny dimenze úložiště** – Skupina dimenze úložiště musí mít vybráno pole **Plán disponibility podle dimenzí** pro pole **Lokalita** a **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="2bdb0-111">Když rezervujete zásoby pro produkt na řádku prodejní objednávky, který je nastaven pro výběr ze stejné dávky, systém se pokusí rezervovat objednané množství z jediné dávky zásob.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="2bdb0-112">Dále jsou zvažovány jakékoli požadavky atributů dávek.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="2bdb0-113">Pokud nelze množství vyplnit z jedné dávky, zobrazí se strana **Konflikt rezervací stejné dávky**.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="2bdb0-114">Tato stránka popisuje problémy a také akce, které lze provést, chcete-li pokračovat v rezervaci.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="2bdb0-115">Následující podmínky mohou bránit rezervaci dávky:</span><span class="sxs-lookup"><span data-stu-id="2bdb0-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="2bdb0-116">Dispoziční kód dávky má možnost **Blokovat rezervaci** pro prodej označenu jako **Blokováno**.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="2bdb0-117">Platnost dávky vypršela, na základě data vypršení platnosti a všech dnů prodejnosti příslušného odběratele.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="2bdb0-118">Položky lze stále ještě považována za rezervaci, pokud se skupina modelu zboží pro položku „nejdříve končící platnost – nejdříve ze skladu“ (FEFO) – řízenou podle data a pokud je jako kritérium pro výdej vybráno datum doporučené spotřeby.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="2bdb0-119">Dávka neobsahuje dostatek zbývajících dní skladovatelnosti na základě data vypršení platnosti a data doporučené spotřeby, a navíc žádné dny prodejnosti odběratele.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="2bdb0-120">U položek přidružených ke skupině dimenzí úložiště, která má povolenu možnost **Použít procesy řízení skladu**, lze vyhradit specifická čísla dávek pomocí hierarchie rezervací s danou dimenzí zásob čísla dávky definovanou nad dimenzí skladového místa.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="2bdb0-121">Stránka **Rezervace dávky** pro řádky prodejního a převodního příkazu umožňuje také vybrat a rezervovat více řádků na základě dostupných čísel dávek.</span><span class="sxs-lookup"><span data-stu-id="2bdb0-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="2bdb0-122">Další informace, jak postupovat v případě, že používáte hierarchii rezervací s dimenzí čísla dávky pod skladovým místem, naleznete [Flexibilní zásada rezervace dimenze na úrovni skladu](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="2bdb0-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>
