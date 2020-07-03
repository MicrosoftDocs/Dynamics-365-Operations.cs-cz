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
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443865"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="a4e78-103">Dostupnost zásob v dvojitém zápisu</span><span class="sxs-lookup"><span data-stu-id="a4e78-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4e78-104">Pomocí dostupnosti zásob můžete zkontrolovat své zásoby před přidáním produktu do formulářů **Nabídky**, **Objednávky** nebo **Faktury** v modelem řízených aplikacích v Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="a4e78-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="a4e78-105">Například kontrolujete zásoby a určíte, že jednou z klíčových úloh ve [zpeněžení potenciálního zákazníka](dual-write-prospect-to-cash.md) je určení data plnění.</span><span class="sxs-lookup"><span data-stu-id="a4e78-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="a4e78-106">Pokud nemáte dostatek zásob, můžete odhadnout datum dodání na základě předpokládaných příjmů a problémů se zásobami.</span><span class="sxs-lookup"><span data-stu-id="a4e78-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="a4e78-107">Můžete také zkontrolovat dostupné informace o produktu Lze slíbit (ATP), kde najdete množství ATP v předem definované ochranné době.</span><span class="sxs-lookup"><span data-stu-id="a4e78-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="a4e78-108">Zásoby na skladě</span><span class="sxs-lookup"><span data-stu-id="a4e78-108">On-hand inventory</span></span>

<span data-ttu-id="a4e78-109">V Dynamics 365 Sales bylo přidáno nové tlačítko **Zásoby na skladě** do záhlaví stránek **Nabídky**, **Objednávky** a **Faktury**.</span><span class="sxs-lookup"><span data-stu-id="a4e78-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a4e78-110">Po výběru tohoto tlačítka se zobrazí dialogové okno, kde můžete určit společnost a produkt, u kterého chcete zkontrolovat zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="a4e78-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="a4e78-111">Toto dialogové okno zobrazuje stejné informace jako [Zásoby na skladě](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="a4e78-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="a4e78-112">Dialogové okno vrací informace o zásobách z Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4e78-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a4e78-113">Tato informace obsahuje následující množství:</span><span class="sxs-lookup"><span data-stu-id="a4e78-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="a4e78-114">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="a4e78-114">On-hand quantity</span></span>
- <span data-ttu-id="a4e78-115">Rezervované množství na skladě</span><span class="sxs-lookup"><span data-stu-id="a4e78-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="a4e78-116">Dostupné množství na skladě</span><span class="sxs-lookup"><span data-stu-id="a4e78-116">Available on-hand quantity</span></span>
- <span data-ttu-id="a4e78-117">Objednané množství</span><span class="sxs-lookup"><span data-stu-id="a4e78-117">Ordered quantity</span></span>
- <span data-ttu-id="a4e78-118">Množství na objednávce</span><span class="sxs-lookup"><span data-stu-id="a4e78-118">On-order quantity</span></span>
- <span data-ttu-id="a4e78-119">Rezervované objednané množství</span><span class="sxs-lookup"><span data-stu-id="a4e78-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="a4e78-120">Celkové dostupné množství</span><span class="sxs-lookup"><span data-stu-id="a4e78-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="a4e78-121">Informace ATP</span><span class="sxs-lookup"><span data-stu-id="a4e78-121">ATP information</span></span>

<span data-ttu-id="a4e78-122">Do aplikace Sales bylo přidáno nové tlačítko **Informace ATP** k položkám řádku na stránkách **Nabídky**, **Objednávky** a **Faktury**.</span><span class="sxs-lookup"><span data-stu-id="a4e78-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a4e78-123">Po výběru tlačítka se zobrazí dialogové okno, kde můžete určit společnost, produkt, skladové pracoviště, sklad zásob a množství na objednávce.</span><span class="sxs-lookup"><span data-stu-id="a4e78-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="a4e78-124">Toto dialogové okno má stejná nastavení, jaká jsou popsána v části [Příslib objednávky](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="a4e78-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="a4e78-125">Dialogové okno vrací informace ATP ze Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4e78-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="a4e78-126">Tato informace obsahuje následující množství:</span><span class="sxs-lookup"><span data-stu-id="a4e78-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="a4e78-127">Množství ATP</span><span class="sxs-lookup"><span data-stu-id="a4e78-127">ATP quantity</span></span>
- <span data-ttu-id="a4e78-128">Množství příjmu</span><span class="sxs-lookup"><span data-stu-id="a4e78-128">Receipt quantity</span></span>
- <span data-ttu-id="a4e78-129">Množství výdeje</span><span class="sxs-lookup"><span data-stu-id="a4e78-129">Issue quantity</span></span>
- <span data-ttu-id="a4e78-130">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="a4e78-130">On-hand quantity</span></span>
