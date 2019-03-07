---
title: Analytické sestavy nejsou aktualizovány
description: Toto téma vysvětluje, jak postupovat, když e nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303543"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="de7e1-103">Analytické sestavy nejsou aktualizovány</span><span class="sxs-lookup"><span data-stu-id="de7e1-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de7e1-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="de7e1-104">**Issue**</span></span>

<span data-ttu-id="de7e1-105">Změny dat odběratele nejsou zobrazeny na kartách **Analytika** v žádném z pracovních prostorů odběratele.</span><span class="sxs-lookup"><span data-stu-id="de7e1-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="de7e1-106">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="de7e1-106">**Cause**</span></span>

<span data-ttu-id="de7e1-107">Ve výchozím nastavení se sestavy Microsoft Power BI aktualizují každé čtyři hodiny, podle plánu dávkové úlohy Nasadit měrný systém.</span><span class="sxs-lookup"><span data-stu-id="de7e1-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="de7e1-108">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="de7e1-108">**Resolution**</span></span>

<span data-ttu-id="de7e1-109">Tento problém může být pouze záležitostí časování.</span><span class="sxs-lookup"><span data-stu-id="de7e1-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="de7e1-110">Tento postup slouží ke spuštění dávkové úlohy a aktualizaci pracovní prostorů analytiky.</span><span class="sxs-lookup"><span data-stu-id="de7e1-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="de7e1-111">Otevřete stránku **Dávkové úlohy** v možnostech **Správa systému \> Odkazy \> Dávkové úlohy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="de7e1-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="de7e1-112">Nebo použijte vyhledávání a zadejte **Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="de7e1-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="de7e1-113">Vyhledejte úlohu **Nasadit měrný systém** v seznamu.</span><span class="sxs-lookup"><span data-stu-id="de7e1-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="de7e1-114">Vyberte **Upravit** v horní části stránky a nastavte naplánované počáteční datum a čas na hodnotu, která bude aktualizovat analytiku blíže aktuálnímu času.</span><span class="sxs-lookup"><span data-stu-id="de7e1-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Dávkové úlohy](media/batch-jobs.png)
