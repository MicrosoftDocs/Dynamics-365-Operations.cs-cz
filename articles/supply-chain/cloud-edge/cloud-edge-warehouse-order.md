---
title: Skladové objednávky pro jednotky škálování cloudu a hraniční sítě
description: Toto téma poskytuje informace o schopnosti objednávky skladu, která se používá jako součást pracovního vytížení jednotky měřítka skladu.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f2401102ab44f5c24f5cd6f545f30438db0a36cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836679"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="96d0e-103">Skladové objednávky pro jednotky škálování cloudu a hraniční sítě</span><span class="sxs-lookup"><span data-stu-id="96d0e-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="96d0e-104">Ne všechny obchodní funkce jsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže.</span><span class="sxs-lookup"><span data-stu-id="96d0e-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="96d0e-105">Pokud používáte jednotky škálování, používejte pouze takové procesy, které toto téma výslovně popisuje jako podporované.</span><span class="sxs-lookup"><span data-stu-id="96d0e-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="96d0e-106">Co jsou to skladové objednávky?</span><span class="sxs-lookup"><span data-stu-id="96d0e-106">What are warehouse orders?</span></span>

<span data-ttu-id="96d0e-107">*Skladové objednávky* jsou typem objednávky, která byla vytvořena k podpoře nasazení centra podpory a škálování jednotek skladu.</span><span class="sxs-lookup"><span data-stu-id="96d0e-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="96d0e-108">Umožní vám přijímat zásoby, když pracujete se zatížením skladu na jednotce škálování.</span><span class="sxs-lookup"><span data-stu-id="96d0e-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="96d0e-109">Aktuálně se používají pouze u objednávek.</span><span class="sxs-lookup"><span data-stu-id="96d0e-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="96d0e-110">Objednávky skladu se používají jako součást zpracování správy skladu, například když se mobilní aplikace Řízení skladu používá k registraci fyzických zásob na skladě během zpracování příchozí nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="96d0e-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="96d0e-111">Skladové objednávky jsou vytvářeny jako součást procesu *Vydání do skladu*, který je k dispozici pro nákupní objednávky, které určují sklad jednotek měřítka a položky, které mají povoleno používat procesy správy skladu.</span><span class="sxs-lookup"><span data-stu-id="96d0e-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96d0e-112">Objednávky skladu jsou k dispozici pouze v nasazeních, která používají [úlohy správy skladu pro cloudové a okrajové jednotky škálování](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="96d0e-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="96d0e-113">Vytvoření skladové objednávky</span><span class="sxs-lookup"><span data-stu-id="96d0e-113">Create a warehouse order</span></span>

<span data-ttu-id="96d0e-114">Chcete-li vytvořit skladovou objednávku, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="96d0e-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="96d0e-115">Přihlaste se k instanci aplikace Microsoft Dynamics 365 Supply Chain Management, která běží v centru.</span><span class="sxs-lookup"><span data-stu-id="96d0e-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="96d0e-116">(Musíte zahájit proces *Vydání do skladu*, když jste přihlášeni v centru.)</span><span class="sxs-lookup"><span data-stu-id="96d0e-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="96d0e-117">Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="96d0e-118">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="96d0e-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="96d0e-119">Chcete-li zobrazit související řádky skladové objednávky, otevřete příslušnou nákupní objednávku a vyberte řádek v části **Řádky nákupní objednávky** a poté na panelu nástrojů vyberte **Sklad \> Skladové řádky**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="96d0e-120">Chcete-li zobrazit všechny řádky, přejděte na **Řízení skladu \> Dotazy a zprávy \> Skladové řádky**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="96d0e-121">Proces *Uvolnění do skladu* můžete také spustit z dávkové úlohy, a to přechodem do nabídky **Správa skladu > Uvolnění do skladu > Automatické uvolnění nákupních objednávek**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="96d0e-122">Při nastavování dávkové úlohy můžete vybrat konkrétní řádky nákupní objednávky na základě dotazu.</span><span class="sxs-lookup"><span data-stu-id="96d0e-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="96d0e-123">Typickým scénářem by bylo nastavení opakované dávkové úlohy, která uvolní všechny potvrzené řádky nákupní objednávky, které se očekávají příští den.</span><span class="sxs-lookup"><span data-stu-id="96d0e-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="96d0e-124">Zrušení skladové objednávky</span><span class="sxs-lookup"><span data-stu-id="96d0e-124">Cancel a warehouse order</span></span>

<span data-ttu-id="96d0e-125">V rámci procesu *Vydání do skladu* jsou skladové transakce nákupních objednávek propojeny se skladovými objednávkami a zablokovány před aktualizací v centru.</span><span class="sxs-lookup"><span data-stu-id="96d0e-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="96d0e-126">Pokud jste vydali zboží do skladu omylem nebo pokud máte jiný důvod pro zrušení vytváření řádků skladových objednávek, můžete požádat o zrušení řádků skladových objednávek.</span><span class="sxs-lookup"><span data-stu-id="96d0e-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="96d0e-127">Chcete-li zrušit řádky skladové objednávky, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="96d0e-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="96d0e-128">Přihlaste se k instanci Supply Chain Management, která běží v centru.</span><span class="sxs-lookup"><span data-stu-id="96d0e-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="96d0e-129">Přejděte na **Řízení skladu \> Dotazy a zprávy \> Skladové řádky**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="96d0e-130">Vyberte příslušný řádek.</span><span class="sxs-lookup"><span data-stu-id="96d0e-130">Select the relevant line.</span></span>
1. <span data-ttu-id="96d0e-131">V podokně akcí vyberte **Zrušit řádky skladové objednávky**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="96d0e-132">Žádost o zrušení řádků bude zamítnuta pro všechny řádky, které již čekají na zrušení nebo které se aktivně zpracovávají ve skladu, na kterém běží jeho pracovní zátěž na jednotce měřítka.</span><span class="sxs-lookup"><span data-stu-id="96d0e-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="96d0e-133">Sledování skladové objednávky</span><span class="sxs-lookup"><span data-stu-id="96d0e-133">Monitor a warehouse order</span></span>

<span data-ttu-id="96d0e-134">V zobrazení **Skladové řádky** můžete sledovat průběh příchozího příjmu kontrolou hodnot ve sloupci **Zbývající množství k přijetí**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="96d0e-135">Chcete-li zobrazit podrobnosti, které souvisejí s prací prováděnou pomocí mobilní aplikace Řízení skladu, postupujte podle jednoho z těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="96d0e-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="96d0e-136">Jděte na **Řízení skladu \> Dotazy a sestavy \> Řádky skladové objednávky** a pomocí filtru najděte řádky, které hledáte.</span><span class="sxs-lookup"><span data-stu-id="96d0e-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="96d0e-137">Jděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky** a otevřete příslušnou nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="96d0e-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="96d0e-138">V části **Řádky nákupní objednávky** vyberte jeden nebo více řádků a poté na panelu nástrojů vyberte **Sklad \> Záznamy o přijetí do skladu**.</span><span class="sxs-lookup"><span data-stu-id="96d0e-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]