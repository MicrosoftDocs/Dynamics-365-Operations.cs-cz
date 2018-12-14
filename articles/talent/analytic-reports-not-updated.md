---
title: "Analytické sestavy nejsou aktualizovány"
description: "Toto téma vysvětluje, jak postupovat, když e nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="3bd87-103">Analytické sestavy nejsou aktualizovány</span><span class="sxs-lookup"><span data-stu-id="3bd87-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3bd87-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="3bd87-104">**Issue**</span></span>

<span data-ttu-id="3bd87-105">Změny dat odběratele nejsou zobrazeny na kartách **Analytika** v žádném z pracovních prostorů odběratele.</span><span class="sxs-lookup"><span data-stu-id="3bd87-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="3bd87-106">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="3bd87-106">**Cause**</span></span>

<span data-ttu-id="3bd87-107">Ve výchozím nastavení se sestavy Microsoft Power BI aktualizují každé čtyři hodiny, podle plánu dávkové úlohy Nasadit měrný systém.</span><span class="sxs-lookup"><span data-stu-id="3bd87-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="3bd87-108">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="3bd87-108">**Resolution**</span></span>

<span data-ttu-id="3bd87-109">Tento problém může být pouze záležitostí časování.</span><span class="sxs-lookup"><span data-stu-id="3bd87-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="3bd87-110">Tento postup slouží ke spuštění dávkové úlohy a aktualizaci pracovní prostorů analytiky.</span><span class="sxs-lookup"><span data-stu-id="3bd87-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="3bd87-111">Otevřete stránku **Dávkové úlohy** v možnostech **Správa systému \> Odkazy \> Dávkové úlohy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="3bd87-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="3bd87-112">Nebo použijte vyhledávání a zadejte **Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="3bd87-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="3bd87-113">Vyhledejte úlohu **Nasadit měrný systém** v seznamu.</span><span class="sxs-lookup"><span data-stu-id="3bd87-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="3bd87-114">Vyberte **Upravit** v horní části stránky a nastavte naplánované počáteční datum a čas na hodnotu, která bude aktualizovat analytiku blíže aktuálnímu času.</span><span class="sxs-lookup"><span data-stu-id="3bd87-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Dávkové úlohy](media/batch-jobs.png)

