---
title: Dostupnost zásob v dvojitém zápisu
description: Toto téma obsahuje informace o kontrole dostupnosti zásob ve dvojím zapisování.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426975"
---
# <a name="inventory-availability"></a><span data-ttu-id="5f684-103">Dostupnost zásob</span><span class="sxs-lookup"><span data-stu-id="5f684-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5f684-104">Pomocí dostupnosti zásob můžete zkontrolovat své zásoby před přidáním produktu do formulářů **Nabídky**, **Objednávky** nebo **Faktury** v modelem řízených aplikacích v Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5f684-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="5f684-105">Například kontrola zásob a určení data plnění je klíčovým úkolem v procesu [zpeněžení potenciálního zákazníka](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="5f684-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="5f684-106">Pokud nemáte dostatek zásob, můžete odhadnout datum dodání na základě předpokládaných příjmů a problémů se zásobami.</span><span class="sxs-lookup"><span data-stu-id="5f684-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="5f684-107">Můžete také zkontrolovat dostupné informace o produktu Lze slíbit (ATP), kde najdete množství ATP v předem definované ochranné době.</span><span class="sxs-lookup"><span data-stu-id="5f684-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="5f684-108">Zásoby na skladě</span><span class="sxs-lookup"><span data-stu-id="5f684-108">On-hand Inventory</span></span> 

<span data-ttu-id="5f684-109">V záhlaví formulářů **Nabídky**, **Objednávky** nebo **Faktury** v Dynamics 365 Sales je přidáno nové tlačítko **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="5f684-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="5f684-110">Po kliknutí na tlačítko se zobrazí dialogové okno a můžete určit společnost a produkt, u kterého chcete zkontrolovat zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="5f684-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="5f684-111">Vrací informace o zásobách z Dynamics 365 Supply Chain Management a zobrazuje stejné informace jako [Zásoby na skladě](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="5f684-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="5f684-112">Informace zahrnují tato množství:</span><span class="sxs-lookup"><span data-stu-id="5f684-112">The information includes these quantities:</span></span>

- <span data-ttu-id="5f684-113">**Množství na skladě**</span><span class="sxs-lookup"><span data-stu-id="5f684-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="5f684-114">**Rezervované množství na skladě**</span><span class="sxs-lookup"><span data-stu-id="5f684-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="5f684-115">**Dostupné množství na skladě**</span><span class="sxs-lookup"><span data-stu-id="5f684-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="5f684-116">**Množství objednávky**</span><span class="sxs-lookup"><span data-stu-id="5f684-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="5f684-117">**Množství na objednávce.**</span><span class="sxs-lookup"><span data-stu-id="5f684-117">**On-order Quantity**</span></span>
- <span data-ttu-id="5f684-118">**Rezervované objednané množství**</span><span class="sxs-lookup"><span data-stu-id="5f684-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="5f684-119">**Celkové dostupné množství**</span><span class="sxs-lookup"><span data-stu-id="5f684-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="5f684-120">Informace ATP</span><span class="sxs-lookup"><span data-stu-id="5f684-120">ATP information</span></span>

<span data-ttu-id="5f684-121">Položkám na řádcích formulářů **Nabídky**, **Objednávky** nebo **Faktury** v Dynamics 365 Sales je přidáno nové tlačítko **Informace ATP**.</span><span class="sxs-lookup"><span data-stu-id="5f684-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="5f684-122">Po kliknutí na tlačítko se zobrazí dialogové okno a můžete určit společnost a produkt, Skladové pracoviště, sklad zásob a množství na objednávce.</span><span class="sxs-lookup"><span data-stu-id="5f684-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="5f684-123">Vrací **Informace ATP** ze Supply Chain Management a zobrazuje nastavení popsaná v [Příslibu objednávky](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="5f684-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="5f684-124">Tyto informace zahrnují **Množství ATP**, **Přijaté množství**, **Vydané množství**, a **Množství na skladě**.</span><span class="sxs-lookup"><span data-stu-id="5f684-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
