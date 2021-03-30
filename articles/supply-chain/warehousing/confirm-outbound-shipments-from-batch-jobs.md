---
title: Potvrdit odchozí dodávky z dávkových úloh
description: Toto téma popisuje, jak nastavit dávkovou úlohu, která automaticky potvrzuje odchozí zásilky převodu objednávek pro zatížení připravená k odeslání.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4c4fd5e8cdea9a7fc05ec9cbc7866c44c6f78b2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243960"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="2d03d-103">Potvrdit odchozí dodávky z dávkových úloh</span><span class="sxs-lookup"><span data-stu-id="2d03d-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d03d-104">Toto téma popisuje, jak nastavit dávkovou úlohu, která automaticky potvrzuje odchozí zásilky převodu objednávek pro zatížení připravená k odeslání.</span><span class="sxs-lookup"><span data-stu-id="2d03d-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="2d03d-105">Zde popsaná dávková úloha se vztahuje pouze na přepravu objednávek, nikoli na prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d03d-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="2d03d-106">Povolte funkci Potvrdit odchozí zásilky z dávkových úloh</span><span class="sxs-lookup"><span data-stu-id="2d03d-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="2d03d-107">Než budete moci použít tuto funkci, musíte ji povolit ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="2d03d-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="2d03d-108">Správci mohou pomocí stránky [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="2d03d-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="2d03d-109">Tato funkce je uvedena jako:</span><span class="sxs-lookup"><span data-stu-id="2d03d-109">The feature is listed as:</span></span>

- <span data-ttu-id="2d03d-110">**Modul** - *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="2d03d-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="2d03d-111">**Název funkce** - *Potvrdit odchozí zásilky z dávkových úloh*</span><span class="sxs-lookup"><span data-stu-id="2d03d-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="2d03d-112">Zpracovat odchozí dodávky</span><span class="sxs-lookup"><span data-stu-id="2d03d-112">Process outbound shipments</span></span>

<span data-ttu-id="2d03d-113">Chcete-li nastavit naplánovanou dávkovou úlohu pro spuštění potvrzení odchozí zásilky pro náklady, které jsou připraveny k odeslání:</span><span class="sxs-lookup"><span data-stu-id="2d03d-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="2d03d-114">Přejděte na **Správa skladu \> Periodické úkoly \> Zpracování odchozích zásilek**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="2d03d-115">Otevře se dialogové okno **Potvrďte odeslání**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="2d03d-116">Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="2d03d-117">Otevře se dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="2d03d-117">The query editor dialog box opens.</span></span> <span data-ttu-id="2d03d-118">Na kartě **Oblast** přidejte řádek s následujícími hodnotami:</span><span class="sxs-lookup"><span data-stu-id="2d03d-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="2d03d-119">**Tabulka** - *Náklady*</span><span class="sxs-lookup"><span data-stu-id="2d03d-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="2d03d-120">**Odvozená tabulka** - *Náklady*</span><span class="sxs-lookup"><span data-stu-id="2d03d-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="2d03d-121">**Pole** - *Stav nákladu*</span><span class="sxs-lookup"><span data-stu-id="2d03d-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="2d03d-122">**Kritéria** - *Naloženo*</span><span class="sxs-lookup"><span data-stu-id="2d03d-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="2d03d-123">Vyberte **OK**, chcte-li se vrátit do dialogového okna **Potvrďte odeslání**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="2d03d-124">Na pevné záložce **Spustit na pozadí** nastavte **Dávkové zpracování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="2d03d-125">Na pevné záložce **Spustit na pozadí** vyberte možnost **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="2d03d-126">Otevře se dialogové okno **Definujte opakování**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="2d03d-127">Nastavte plán běhu podle potřeby pro vaše podnikání.</span><span class="sxs-lookup"><span data-stu-id="2d03d-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="2d03d-128">Vyberte **OK**, chcte-li se vrátit do dialogového okna **Potvrďte odeslání**.</span><span class="sxs-lookup"><span data-stu-id="2d03d-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="2d03d-129">Vyberte **OK** v dialogovém okně **Potvrďte odeslání** pro přidání dávkové úlohy do dávkové fronty.</span><span class="sxs-lookup"><span data-stu-id="2d03d-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="2d03d-130">Další informace viz [Přehled dávkového zpracování](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2d03d-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]