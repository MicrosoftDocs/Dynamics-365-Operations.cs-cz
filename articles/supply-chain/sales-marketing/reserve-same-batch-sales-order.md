---
title: "Rezervace stejné dávky pro prodejní objednávku"
description: "Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 59d5beb92ed762f57b930c44894f40549024fcc5
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="0f8f2-103">Rezervace stejné dávky pro prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="0f8f2-103">Reserve the same batch for a sales order</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="0f8f2-104">Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="0f8f2-105">Rezervace stejné dávky umožňuje rezervovat zásoby pro řádek prodejní objednávky z jediné dávky zásob.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="0f8f2-106">Například zákazník, který si objedná tapetu, může požadovat, aby byla celá objednávka zadána ze stejné dávky nebo šarže, aby se zabránilo nekonzistenci mezi rolemi.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="0f8f2-107">Chcete-li nastavit produkt tak, aby používal rezervaci stejné dávky, musí být aktivní následující nastavení ve skupině modelů zboží, skupině sledovací dimenze a skupině dimenze úložiště, kterou chcete přiřadit k produktu:</span><span class="sxs-lookup"><span data-stu-id="0f8f2-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="0f8f2-108">**Skupiny modelů položek** – Skupina modelů položek musí mít skupinu vybrána pole **Výběr ze stejné dávky** a **Požadavek na konsolidaci** ve skupině polí **Rezervace** pro zásady skladu.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="0f8f2-109">**Skupiny sledovací dimenze** – Skupina sledovací dimenze musí mít vybráno pole **Plán disponibility podle dimenzí** pro číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="0f8f2-110">**Skupiny dimenze úložiště** – Skupina dimenze úložiště musí mít vybráno pole **Plán disponibility podle dimenzí** pro pole **Lokalita** a **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="0f8f2-111">Když rezervujete zásoby pro produkt na řádku prodejní objednávky, který je nastaven pro výběr ze stejné dávky, aplikace Microsoft Dynamics 365 for Finance and Operations se pokusí rezervovat objednané množství z jediné dávky zásob.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="0f8f2-112">Dále jsou zvažovány jakékoli požadavky atributů dávek.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="0f8f2-113">Pokud nelze množství vyplnit z jedné dávky, zobrazí se strana **Konflikt rezervací stejné dávky**.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="0f8f2-114">Tato stránka popisuje problémy a také akce, které lze provést, chcete-li pokračovat v rezervaci.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="0f8f2-115">Následující podmínky mohou bránit rezervaci dávky:</span><span class="sxs-lookup"><span data-stu-id="0f8f2-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="0f8f2-116">Dispoziční kód dávky má možnost **Blokovat rezervaci** pro prodej označenu jako **Blokováno**.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="0f8f2-117">Platnost dávky vypršela, na základě data vypršení platnosti a všech dnů prodejnosti příslušného odběratele.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="0f8f2-118">Položky lze stále ještě považována za rezervaci, pokud se skupina modelu zboží pro položku „nejdříve končící platnost – nejdříve ze skladu“ (FEFO) – řízenou podle data a pokud je jako kritérium pro výdej vybráno datum doporučené spotřeby.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="0f8f2-119">Dávka neobsahuje dostatek zbývajících dní skladovatelnosti na základě data vypršení platnosti a data doporučené spotřeby, a navíc žádné dny prodejnosti odběratele.</span><span class="sxs-lookup"><span data-stu-id="0f8f2-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





