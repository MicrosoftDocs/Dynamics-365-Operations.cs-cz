---
title: Události aplikace skladu
description: Toto téma popisuje zpracování událostí aplikace skladu používané ke zpracování zpráv o událostech aplikace skladu jako součást dávkové úlohy.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0bafcbd5306860cb80d6e813aabf83853a9011c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248636"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="ef5b0-103">Zpracování události aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="ef5b0-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef5b0-104">Dávkové úlohy spuštěné v produktu Supply Chain Management mohou používat data z fronty pro zpracování událostí vydaných aplikací skladu, aby podle potřeby reagovaly na signalizované události.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="ef5b0-105">Tato funkce přidává do fronty relevantní události v reakci na určité typy akcí prováděné pracovníky používajícími tuto aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="ef5b0-106">Příkladem je, že při použití funkce **Vytvářet a zpracovat převodní příkazy z aplikace skladu** se záhlaví a řádky převodního příkazu vytvoří a aktualizují v back-endu, když v systému běží dávková úloha **Zpracovat události aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="ef5b0-107">Povolení funkce Zpracovat události aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="ef5b0-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="ef5b0-108">Než budete moci použít tuto funkci, musíte ji povolit ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="ef5b0-109">Správci mohou pomocí stránky [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="ef5b0-110">Funkce Zpracovat události aplikace skladu je uvedena takto:</span><span class="sxs-lookup"><span data-stu-id="ef5b0-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="ef5b0-111">**Modul** - Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="ef5b0-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="ef5b0-112">**Název funkce** – Zpracovat události aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="ef5b0-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="ef5b0-113">Nastavit dávkovou úlohu pro zpracování událostí aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="ef5b0-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="ef5b0-114">Zpracovat události aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="ef5b0-114">Process warehouse app events</span></span>

<span data-ttu-id="ef5b0-115">Nastavte naplánovanou dávkovou úlohu pro zpracování událostí aplikace skladu pro vytvoření převodních příkazů a aktualizací řádků.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="ef5b0-116">Přejděte na **Správa skladu \> Periodické úkoly \> Zpracovat události aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="ef5b0-117">Otevře se dialogové okno Zpracovat události aplikace skladu.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="ef5b0-118">Rozbalte záložku s náhledem **Spustit na pozadí** a nastavte **Dávkové zpracování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="ef5b0-119">Na pevné záložce **Spustit na pozadí** vyberte možnost **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="ef5b0-120">Otevře se dialogové okno **Definujte opakování**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="ef5b0-121">Nastavte plán běhu podle potřeby pro vaše podnikání.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="ef5b0-122">Volbou **OK** se vraťte do dialogového okna **Zpracovat události aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="ef5b0-123">Vyberte **OK** v dialogovém okně **Zpracovat události aplikace skladu** pro přidání dávkové úlohy do dávkové fronty.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="ef5b0-124">Dotazy na události aplikace skladu</span><span class="sxs-lookup"><span data-stu-id="ef5b0-124">Query warehouse app events</span></span>

<span data-ttu-id="ef5b0-125">Frontu událostí a zprávy o událostech generované aplikací skladu si můžete zobrazit přechodem na **Řízení skladu \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Události aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="ef5b0-126">Standardní proces fronty událostí</span><span class="sxs-lookup"><span data-stu-id="ef5b0-126">The standard event queue process</span></span>

<span data-ttu-id="ef5b0-127">Fronta událostí skladových aplikací se obvykle používá s následujícím popsaným tokem:</span><span class="sxs-lookup"><span data-stu-id="ef5b0-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="ef5b0-128">Událost bude přidána do fronty se zprávou o události.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="ef5b0-129">Nová zpráva má zpočátku stav události **Čekání**, což znamená, že dávková úloha **Zpracovat události aplikace skladu** tuto zprávu nevyzvedne a nezpracuje.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="ef5b0-130">Jakmile je stav zprávy aktualizován na **Ve frontě**, dávková úloha **Zpracovat události aplikace skladu** událost vyzvedne a zpracuje.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="ef5b0-131">Dávková úloha aktualizuje stavy události buď na **Dokončeno**, nebo **Selhalo**, a to podle toho, zda byl požadovaný proces možný.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="ef5b0-132">Když jsou všechny související zprávy o událostech **Dokončeno**, událost se odstraní z fronty.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="ef5b0-133">Podrobný příklad viz [Vytvoření převodního příkazu z procesu aplikace skladu](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="ef5b0-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="ef5b0-134">Zpracování chyb událostí</span><span class="sxs-lookup"><span data-stu-id="ef5b0-134">Handle event errors</span></span>

<span data-ttu-id="ef5b0-135">Je možné, že v rámci zpracování události skladu nebude aktivita požadované zprávy přijímat procesy z dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="ef5b0-136">V takovém případě se zpráva události změní na **Selhalo**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="ef5b0-137">Můžete použít informace **Dávkový protokol**, abyste se dozvěděli proč a mohli podniknout kroky potřebné k nápravě případných problémů.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="ef5b0-138">Podrobný příklad viz [Vytvoření převodního příkazu z aplikace skladu](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="ef5b0-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="ef5b0-139">Resetování zprávy „Selhalo“ o události aplikace:</span><span class="sxs-lookup"><span data-stu-id="ef5b0-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="ef5b0-140">Přejděte na **Řízení skladu \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Události aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="ef5b0-141">Na záložce s náhledem **Zprávy o událostech aplikace skladu** vyhledejte a vyberte relevantní událost, která se zobrazuje se stavem **Selhalo** ve sloupci **Stav události**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="ef5b0-142">Vyberte **Resetovat** z panelu nástrojů **Zprávy o událostech aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="ef5b0-143">Pokračujte v práci, dokud se neresetují všechny relevantní zprávy.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="ef5b0-144">Zprávu o události **Selhalo** můžete také odebrat pomocí možnosti **Odstranit** na panelu nástrojů **Zprávy o událostech aplikace skladu**.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]