---
title: Skladové objednávky pro jednotky škálování cloudu a hraniční sítě
description: Toto téma poskytuje informace o schopnosti objednávky skladu, která se používá jako součást pracovního vytížení jednotky měřítka skladu.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105696"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="be240-103">Skladové objednávky pro jednotky škálování cloudu a hraniční sítě</span><span class="sxs-lookup"><span data-stu-id="be240-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="be240-104">Ne všechny obchodní funkce jsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže.</span><span class="sxs-lookup"><span data-stu-id="be240-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="be240-105">Pokud používáte jednotky škálování, používejte pouze takové procesy, které toto téma výslovně popisuje jako podporované.</span><span class="sxs-lookup"><span data-stu-id="be240-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="be240-106">Co jsou to skladové objednávky?</span><span class="sxs-lookup"><span data-stu-id="be240-106">What are warehouse orders?</span></span>

<span data-ttu-id="be240-107">*Skladové objednávky* jsou typem objednávky, která byla vytvořena k podpoře nasazení centra podpory a škálování jednotek skladu.</span><span class="sxs-lookup"><span data-stu-id="be240-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="be240-108">Umožní vám přijímat zásoby, když pracujete se zatížením skladu na jednotce škálování.</span><span class="sxs-lookup"><span data-stu-id="be240-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="be240-109">Aktuálně se používají pouze u objednávek.</span><span class="sxs-lookup"><span data-stu-id="be240-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="be240-110">Objednávky skladu se používají jako součást zpracování správy skladu, například když se skladová aplikace používá k registraci fyzických zásob na skladě během zpracování příchozí nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="be240-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="be240-111">Skladové objednávky jsou vytvářeny jako součást procesu *Vydání do skladu*, který je k dispozici pro nákupní objednávky, které určují sklad jednotek měřítka a položky, které mají povoleno používat procesy správy skladu.</span><span class="sxs-lookup"><span data-stu-id="be240-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be240-112">Objednávky skladu jsou k dispozici pouze v nasazeních, která používají [úlohy správy skladu pro cloudové a okrajové jednotky škálování](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="be240-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="be240-113">Vytvoření skladové objednávky</span><span class="sxs-lookup"><span data-stu-id="be240-113">Create a warehouse order</span></span>

<span data-ttu-id="be240-114">Chcete-li vytvořit skladovou objednávku, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="be240-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="be240-115">Přihlaste se k instanci aplikace Microsoft Dynamics 365 Supply Chain Management, která běží v centru.</span><span class="sxs-lookup"><span data-stu-id="be240-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="be240-116">(Musíte zahájit proces *Vydání do skladu*, když jste přihlášeni v centru.)</span><span class="sxs-lookup"><span data-stu-id="be240-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="be240-117">Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="be240-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="be240-118">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="be240-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="be240-119">Chcete-li zobrazit související řádky skladové objednávky, otevřete příslušnou nákupní objednávku a vyberte řádek v části **Řádky nákupní objednávky** a poté na panelu nástrojů vyberte **Sklad \> Skladové řádky**.</span><span class="sxs-lookup"><span data-stu-id="be240-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="be240-120">Chcete-li zobrazit všechny řádky, přejděte na **Řízení skladu \> Dotazy a zprávy \> Skladové řádky**.</span><span class="sxs-lookup"><span data-stu-id="be240-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="be240-121">Zrušení skladové objednávky</span><span class="sxs-lookup"><span data-stu-id="be240-121">Cancel a warehouse order</span></span>

<span data-ttu-id="be240-122">V rámci procesu *Vydání do skladu* jsou skladové transakce nákupních objednávek propojeny se skladovými objednávkami a zablokovány před aktualizací v centru.</span><span class="sxs-lookup"><span data-stu-id="be240-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="be240-123">Pokud jste vydali zboží do skladu omylem nebo pokud máte jiný důvod pro zrušení vytváření řádků skladových objednávek, můžete požádat o zrušení řádků skladových objednávek.</span><span class="sxs-lookup"><span data-stu-id="be240-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="be240-124">Chcete-li zrušit řádky skladové objednávky, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="be240-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="be240-125">Přihlaste se k instanci Supply Chain Management, která běží v centru.</span><span class="sxs-lookup"><span data-stu-id="be240-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="be240-126">Přejděte na **Řízení skladu \> Dotazy a zprávy \> Skladové řádky**.</span><span class="sxs-lookup"><span data-stu-id="be240-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="be240-127">Vyberte příslušný řádek.</span><span class="sxs-lookup"><span data-stu-id="be240-127">Select the relevant line.</span></span>
1. <span data-ttu-id="be240-128">V podokně akcí vyberte **Zrušit řádky skladové objednávky**.</span><span class="sxs-lookup"><span data-stu-id="be240-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="be240-129">Žádost o zrušení řádků bude zamítnuta pro všechny řádky, které již čekají na zrušení nebo které se aktivně zpracovávají ve skladu, na kterém běží jeho pracovní zátěž na jednotce měřítka.</span><span class="sxs-lookup"><span data-stu-id="be240-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="be240-130">Sledování skladové objednávky</span><span class="sxs-lookup"><span data-stu-id="be240-130">Monitor a warehouse order</span></span>

<span data-ttu-id="be240-131">V zobrazení **Skladové řádky** můžete sledovat průběh příchozího příjmu kontrolou hodnot ve sloupci **Zbývající množství k přijetí**.</span><span class="sxs-lookup"><span data-stu-id="be240-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="be240-132">Chcete-li zobrazit podrobnosti, které souvisejí s prací prováděnou pomocí aplikace Sklad, postupujte podle jednoho z těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="be240-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="be240-133">Jděte na **Řízení skladu \> Dotazy a sestavy \> Řádky skladové objednávky** a pomocí filtru najděte řádky, které hledáte.</span><span class="sxs-lookup"><span data-stu-id="be240-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="be240-134">Jděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky** a otevřete příslušnou nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="be240-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="be240-135">V části **Řádky nákupní objednávky** vyberte jeden nebo více řádků a poté na panelu nástrojů vyberte **Sklad \> Záznamy o přijetí do skladu**.</span><span class="sxs-lookup"><span data-stu-id="be240-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
