---
title: Zpoždění
description: Toto téma obsahuje informace o zpožděných datech v hlavním plánování. Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1a8c738fffda76f2a8492c20e2c67a154c68559
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1522282"
---
# <a name="delays"></a><span data-ttu-id="0a180-104">Zpoždění</span><span class="sxs-lookup"><span data-stu-id="0a180-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a180-105">Toto téma obsahuje informace o zpožděných datech v hlavním plánování.</span><span class="sxs-lookup"><span data-stu-id="0a180-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="0a180-106">Zpožděné datum je realistické datum splatnosti přidělené transakci, pokud je nejbližší datum plnění vypočítané hlavním plánováním pozdější než požadované datum.</span><span class="sxs-lookup"><span data-stu-id="0a180-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="0a180-107">Hlavní plánování dokáže vypočítat nejbližší datum plnění transakce na základě doby realizace, dostupnosti materiálu, dostupné kapacity a různých parametrů plánování.</span><span class="sxs-lookup"><span data-stu-id="0a180-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="0a180-108">Pokud hlavní plánování vypočítá datum objednávky, které předchází dnešnímu datu, objednávku nelze splnit včas.</span><span class="sxs-lookup"><span data-stu-id="0a180-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="0a180-109">Objednávka je proto zpožděná.</span><span class="sxs-lookup"><span data-stu-id="0a180-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="0a180-110">V takovém případě hlavní plánování objednávku naplánuje dopředně od dnešního data a zahrne doby realizace.</span><span class="sxs-lookup"><span data-stu-id="0a180-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="0a180-111">Tyto realizace časy zahájení kteroukoliv položkou součásti na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="0a180-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="0a180-112">Objednávce se pak přiřadí datum zpoždění.</span><span class="sxs-lookup"><span data-stu-id="0a180-112">The order then receives a delayed date.</span></span> <span data-ttu-id="0a180-113">Datum zpoždění je realistické datum dodání stanovené podle aktuálního data.</span><span class="sxs-lookup"><span data-stu-id="0a180-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="0a180-114">Hlavní plánování vypočte také počet dnů zpoždění.</span><span class="sxs-lookup"><span data-stu-id="0a180-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="0a180-115">V některých situacích může být vhodnější zpoždění nevypočítávat, například pokud uživatelé vědí, že lze dobu realizace urychlit výběrem alternativních způsobů dodání.</span><span class="sxs-lookup"><span data-stu-id="0a180-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="0a180-116">Způsob výpočtu zpoždění pro skupinu disponibility lze upravit.</span><span class="sxs-lookup"><span data-stu-id="0a180-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="0a180-117">Skupinu disponibility můžete k položce přiřadit později.</span><span class="sxs-lookup"><span data-stu-id="0a180-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="0a180-118">Na stránce **Parametry hlavního plánování** můžete nastavit čas zahájení výpočtu zpoždění.</span><span class="sxs-lookup"><span data-stu-id="0a180-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="0a180-119">Pokud je objednávka splněna po tomto termínu, k datu zpoždění objednávky se přičte jeden den.</span><span class="sxs-lookup"><span data-stu-id="0a180-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="0a180-120">V předchozích verzích se vypočtená zpoždění nazývala *termínové zprávy*, datum zpoždění se nazývalo *datum termínu* a zpožděná transakce se označovala jako *transakce nastavená na budoucí datum*.</span><span class="sxs-lookup"><span data-stu-id="0a180-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="0a180-121">Požadované datum</span><span class="sxs-lookup"><span data-stu-id="0a180-121">Desired date</span></span>

<span data-ttu-id="0a180-122">Na stránce **Plánovaná objednávka** na kartě **Zpoždění** je uvedeno **požadované datum** plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="0a180-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="0a180-123">Požadované datum plánované objednávky je základní datum zpoždění, což je vypočítané datum, které se rovná **požadovanému datu** počítáno od **čistého požadavku**.</span><span class="sxs-lookup"><span data-stu-id="0a180-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="0a180-124">Pokud je plánovaná objednávka řádka kusovníku, výroby nebo řádka kamban, je požadované datum založeno na **datu požadavku** a nebude uvedeno na stránce **Plánovaná objednávka**.</span><span class="sxs-lookup"><span data-stu-id="0a180-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0a180-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0a180-125">Additional resources</span></span>
--------

[<span data-ttu-id="0a180-126">Nastavení distponibility</span><span class="sxs-lookup"><span data-stu-id="0a180-126">Coverage settings</span></span>](coverage-settings.md)
