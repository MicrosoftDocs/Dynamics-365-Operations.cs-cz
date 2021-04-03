---
title: Automatizace procesů
description: Toto téma uvádí podrobnosti o automatizace procesů, jež umožňuje jednoduše plánovat procesy, které budou spouštěny dávkovým serverem.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: e3babed18caefff16105f70a0b15b8b8cf0f08eb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568203"
---
# <a name="process-automation"></a><span data-ttu-id="1200c-103">Automatizace procesů</span><span class="sxs-lookup"><span data-stu-id="1200c-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1200c-104">Automatizace procesů umožňuje jednoduše plánovat procesy, které budou spouštěny dávkovým serverem.</span><span class="sxs-lookup"><span data-stu-id="1200c-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="1200c-105">Aktualizované kalendářové zobrazení naplánované práce umožňuje koncovým uživatelům prohlížet plánované a dokončené práce a provádět ve vztahu k nim různé akce.</span><span class="sxs-lookup"><span data-stu-id="1200c-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="1200c-106">Správa</span><span class="sxs-lookup"><span data-stu-id="1200c-106">Administration</span></span>

<span data-ttu-id="1200c-107">Centrální administrační stránka pro veškerou automatizaci procesů se nachází v modulu správy systému v nabídce **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="1200c-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="1200c-108">Na této stránce najdete všechny automatizované procesy (řady), které jsou v systému nastaveny.</span><span class="sxs-lookup"><span data-stu-id="1200c-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="1200c-109">Přímo z této stránky je též možné přidávat nové automatizace procesů.</span><span class="sxs-lookup"><span data-stu-id="1200c-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="1200c-110">Po nastavení řady můžete z tohoto seznamu každou jednotlivou řadu spravovat.</span><span class="sxs-lookup"><span data-stu-id="1200c-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="1200c-111">Můžete upravit celou řadu, smazat ji, zobrazit všechny výskyty jako seznam nebo řadu zakázat, chcete-li plánovanou práci na určitou dobu pozastavit.</span><span class="sxs-lookup"><span data-stu-id="1200c-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="1200c-112">Všechny procesy, které jsou zakázány ve správě prvků, se po deaktivaci funkce nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="1200c-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="1200c-113">Navíc plánovací modul automatizace procesů nebude plánovat žádné události ani procesy na pozadí pro zakázanou funkci.</span><span class="sxs-lookup"><span data-stu-id="1200c-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="1200c-114">Opětovné povolení funkce způsobí okamžité spuštění všech minulých naplánovaných událostí nebo procesů na pozadí.</span><span class="sxs-lookup"><span data-stu-id="1200c-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="1200c-115">Kalendářové zobrazení</span><span class="sxs-lookup"><span data-stu-id="1200c-115">Calendar view</span></span>

<span data-ttu-id="1200c-116">Jednou z klíčových výhod automatizace procesů je možnost vidět plánovanou práci v jednoduchém kalendářovém zobrazení.</span><span class="sxs-lookup"><span data-stu-id="1200c-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="1200c-117">Toto zobrazení umožňuje zobrazit najednou práci na období jednoho týdne.</span><span class="sxs-lookup"><span data-stu-id="1200c-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="1200c-118">Toto zobrazení uvidíte na pravé straně na stránce **Automatizace procesů**.</span><span class="sxs-lookup"><span data-stu-id="1200c-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="1200c-119">Bude naplněno naplánovanou prací pro vybranou řadu.</span><span class="sxs-lookup"><span data-stu-id="1200c-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="1200c-120">[![Kalendář automatizace procesů](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="1200c-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="1200c-121">Změny výskytů</span><span class="sxs-lookup"><span data-stu-id="1200c-121">Occurrence changes</span></span>

<span data-ttu-id="1200c-122">Každý výskyt lze upravit, aniž by to mělo vliv na jiné výskyty definované řadou, z níž daný výskyt pochází.</span><span class="sxs-lookup"><span data-stu-id="1200c-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="1200c-123">Výskyt plánované práce lze upravit v kalendářovém zobrazení stiskem tlačítka **Zobrazit/upravit** a výběrem možnosti **Výskyt**.</span><span class="sxs-lookup"><span data-stu-id="1200c-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="1200c-124">Získáte tak přístup ke všem nastavením původně zobrazeným v průvodci nastavením řady. Můžete provést jednorázovou změnu vybraného výskytu.</span><span class="sxs-lookup"><span data-stu-id="1200c-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="1200c-125">Výskyt plánované práce lze také vypnout v kalendářovém zobrazení výběrem možnosti **Zakázat**.</span><span class="sxs-lookup"><span data-stu-id="1200c-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="1200c-126">Dokumentace pro vývojáře</span><span class="sxs-lookup"><span data-stu-id="1200c-126">Developer documentation</span></span>

<span data-ttu-id="1200c-127">Rámec automatizace procesů umožňuje vývojářům rozšířit rámec automatizace procesů.</span><span class="sxs-lookup"><span data-stu-id="1200c-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="1200c-128">Dokumentace k [rámci automatizace procesu](../process-automation/process-automation-framework.md) poskytuje informace o tom, jak vytvářet vlastní procesy, jež mají být spouštěny dávkovým serverem, jak je plánovat pomocí průvodce automatizací procesů a automaticky zobrazovat v kalendářovém zobrazení.</span><span class="sxs-lookup"><span data-stu-id="1200c-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]