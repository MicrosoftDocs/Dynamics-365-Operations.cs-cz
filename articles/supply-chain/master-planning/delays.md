---
title: Zpoždění
description: Toto téma obsahuje informace o zpožděných datech v hlavním plánování. Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dcb11b3665c5d2f296f1ba2ce4708c4eff241b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977981"
---
# <a name="delays"></a><span data-ttu-id="f0707-104">Zpoždění</span><span class="sxs-lookup"><span data-stu-id="f0707-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0707-105">Toto téma obsahuje informace o zpožděných datech v hlavním plánování.</span><span class="sxs-lookup"><span data-stu-id="f0707-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="f0707-106">Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum.</span><span class="sxs-lookup"><span data-stu-id="f0707-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="f0707-107">Hlavní plánování dokáže vypočítat nejbližší datum plnění transakce na základě doby realizace, dostupnosti materiálu, dostupné kapacity a různých parametrů plánování.</span><span class="sxs-lookup"><span data-stu-id="f0707-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="f0707-108">Pokud hlavní plánování vypočítá datum objednávky, které předchází dnešnímu datu, objednávku nelze splnit včas.</span><span class="sxs-lookup"><span data-stu-id="f0707-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="f0707-109">Objednávka je proto zpožděná.</span><span class="sxs-lookup"><span data-stu-id="f0707-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="f0707-110">V takovém případě hlavní plánování objednávku naplánuje dopředně od dnešního data a zahrne doby realizace.</span><span class="sxs-lookup"><span data-stu-id="f0707-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="f0707-111">Tyto realizace časy zahájení kteroukoliv položkou součásti na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="f0707-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="f0707-112">Objednávce se pak přiřadí datum zpoždění.</span><span class="sxs-lookup"><span data-stu-id="f0707-112">The order then receives a delayed date.</span></span> <span data-ttu-id="f0707-113">Datum zpoždění je realistické datum dodání stanovené podle aktuálního data.</span><span class="sxs-lookup"><span data-stu-id="f0707-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="f0707-114">Hlavní plánování vypočte také počet dnů zpoždění.</span><span class="sxs-lookup"><span data-stu-id="f0707-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="f0707-115">V některých situacích může být vhodnější zpoždění nevypočítávat, například pokud uživatelé vědí, že lze dobu realizace urychlit výběrem alternativních způsobů dodání.</span><span class="sxs-lookup"><span data-stu-id="f0707-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="f0707-116">Způsob výpočtu zpoždění pro skupinu disponibility lze upravit.</span><span class="sxs-lookup"><span data-stu-id="f0707-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="f0707-117">Skupinu disponibility můžete k položce přiřadit později.</span><span class="sxs-lookup"><span data-stu-id="f0707-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="f0707-118">Na stránce **Parametry hlavního plánování** můžete nastavit čas zahájení výpočtu zpoždění.</span><span class="sxs-lookup"><span data-stu-id="f0707-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="f0707-119">Pokud je objednávka splněna po tomto termínu, k datu zpoždění objednávky se přičte jeden den.</span><span class="sxs-lookup"><span data-stu-id="f0707-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="f0707-120">V předchozích verzích se vypočtená zpoždění nazývala *termínové zprávy*, datum zpoždění se nazývalo *datum termínu* a zpožděná transakce se označovala jako *transakce nastavená na budoucí datum*.</span><span class="sxs-lookup"><span data-stu-id="f0707-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="f0707-121">Omezené zpoždění při nastavení výroby s více úrovněmi kusovníku</span><span class="sxs-lookup"><span data-stu-id="f0707-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="f0707-122">Pokud pracujete se zpožděními v nastavení výroby, které má více úrovní kusovníku, je důležité poznamenat, že pouze položky, které způsobují zpoždění, přímo nad položkou (ve struktuře kusovníku), budou při spuštění hlavního plánování aktualizovány s prodlením.</span><span class="sxs-lookup"><span data-stu-id="f0707-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="f0707-123">Ostatní položky ve struktuře kusovníku nebudou při schválení nebo potvrzení plánované objednávky pro nejvyšší úroveň použity zpoždění použité do prvního hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="f0707-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="f0707-124">Chcete-li toto známé omezení obejít, je možné schválit výrobní zakázky na vrcholu struktury kusovníku se zpožděními (nebo pevně) před dalším spuštěním hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="f0707-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="f0707-125">Tímto způsobem se zachovají zpoždění z opožděné schválené plánované výrobní zakázky a všechny podřízené komponenty budou odpovídajícím způsobem aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="f0707-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="f0707-126">Zprávy akce lze rovněž použít k identifikaci plánovaných objednávek, které lze přesunout do pozdějšího data z důvodu jiných zpoždění ve struktuře kusovníku.</span><span class="sxs-lookup"><span data-stu-id="f0707-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="f0707-127">Požadované datum</span><span class="sxs-lookup"><span data-stu-id="f0707-127">Desired date</span></span>

<span data-ttu-id="f0707-128">Na stránce **Plánovaná objednávka** na kartě **Zpoždění** je uvedeno **požadované datum** plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0707-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="f0707-129">Požadované datum plánované objednávky je základní datum zpoždění, což je vypočítané datum, které se rovná **požadovanému datu** počítáno od **čistého požadavku**.</span><span class="sxs-lookup"><span data-stu-id="f0707-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="f0707-130">Pokud je plánovaná objednávka řádka kusovníku, výroby nebo řádka kamban, je požadované datum založeno na **datu požadavku** a nebude uvedeno na stránce **Plánovaná objednávka**.</span><span class="sxs-lookup"><span data-stu-id="f0707-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f0707-131">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f0707-131">Additional resources</span></span>
--------

[<span data-ttu-id="f0707-132">Nastavení distponibility</span><span class="sxs-lookup"><span data-stu-id="f0707-132">Coverage settings</span></span>](coverage-settings.md)
