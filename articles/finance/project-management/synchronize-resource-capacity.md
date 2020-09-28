---
title: Synchronizace kapacity prostředku
description: Toto téma poskytuje informace o tom, jak synchronizovat kapacitu prostředku napříč kalendáři a projekty.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760492"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="567d8-103">Synchronizace kapacity prostředku</span><span class="sxs-lookup"><span data-stu-id="567d8-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="567d8-104">Procesy pro synchronizaci prostředků pomáhají zajistit, aby informace pro kalendář a základní kalendář přešly dále do plánování prostředků pro projekt.</span><span class="sxs-lookup"><span data-stu-id="567d8-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="567d8-105">Pokud dojde ke změně kalendáře, procesy provedou požadované aktualizace v plánování zdrojů pro projekt.</span><span class="sxs-lookup"><span data-stu-id="567d8-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="567d8-106">Procesy také pomáhají zvýšit výkonnost, protože informace o zdrojích kalendáře jsou synchronizovány v předstihu.</span><span class="sxs-lookup"><span data-stu-id="567d8-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="567d8-107">Aktualizace informací o plánování zdrojů se děje tudíž rychleji.</span><span class="sxs-lookup"><span data-stu-id="567d8-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="567d8-108">Doporučujeme naplánovat procesy jako dávku namísto postupného zpracování.</span><span class="sxs-lookup"><span data-stu-id="567d8-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="567d8-109">V opačném případě je riziko, že někdo zapomene inkluzivní datum, kdy byly informace naposled synchronizovány.</span><span class="sxs-lookup"><span data-stu-id="567d8-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="567d8-110">Pokud inkluzivní data nejsou použity, mohou vzniknout mezery v synchronizaci dat.</span><span class="sxs-lookup"><span data-stu-id="567d8-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synchronizace kalendáře](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="567d8-112">Synchronizace shrnutí kapacity pro prostředek</span><span class="sxs-lookup"><span data-stu-id="567d8-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="567d8-113">Proces synchronizace umožňuje synchronizovat všechny informace v kalendáři prostředku.</span><span class="sxs-lookup"><span data-stu-id="567d8-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="567d8-114">Tyto informace zahrnují základní informace z kalendáře o všech změnách v tabulce kapacity kalendáře prostředků projektu.</span><span class="sxs-lookup"><span data-stu-id="567d8-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="567d8-115">Pokud jsou do projektu přidány nové prostředky, synchronizace pomáhá zajistit, že jsou aktualizované informace k dispozici.</span><span class="sxs-lookup"><span data-stu-id="567d8-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="567d8-116">Tuto synchronizaci lze provádět kdykoliv.</span><span class="sxs-lookup"><span data-stu-id="567d8-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="567d8-117">Doporučujeme používat dávky.</span><span class="sxs-lookup"><span data-stu-id="567d8-117">We recommend that you use a batch.</span></span> <span data-ttu-id="567d8-118">Možnosti jsou dostupné při synchronizaci rezervací kapacity.</span><span class="sxs-lookup"><span data-stu-id="567d8-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="567d8-119">Zvolte **Řízení a účetnictví projektů** &gt; **Periodicky** &gt; **Synchronizace kapacity** &gt; **Synchronizace shrnutí kapacity pro prostředek**.</span><span class="sxs-lookup"><span data-stu-id="567d8-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="567d8-120">Nastavte možnosti v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="567d8-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="567d8-121">Parametr</span><span class="sxs-lookup"><span data-stu-id="567d8-121">Option</span></span>      | <span data-ttu-id="567d8-122">popis</span><span class="sxs-lookup"><span data-stu-id="567d8-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="567d8-123">Kód období</span><span class="sxs-lookup"><span data-stu-id="567d8-123">Period code</span></span> | <span data-ttu-id="567d8-124">Volitelně vyberte kód datového intervalu hlavní knihy k nastavení počátečního a koncového data pro synchronizaci procesu pro shrnutí kapacity zdrojů.</span><span class="sxs-lookup"><span data-stu-id="567d8-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="567d8-125">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="567d8-125">Start date</span></span>  | <span data-ttu-id="567d8-126">Zadejte počáteční datum pro proces synchronizace pro shrnutí kapacity zdrojů.</span><span class="sxs-lookup"><span data-stu-id="567d8-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="567d8-127">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="567d8-127">End date</span></span>    | <span data-ttu-id="567d8-128">Zadejte koncové datum pro proces synchronizace pro shrnutí kapacity zdrojů.</span><span class="sxs-lookup"><span data-stu-id="567d8-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="567d8-129">[![Proces synchronizace](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="567d8-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
