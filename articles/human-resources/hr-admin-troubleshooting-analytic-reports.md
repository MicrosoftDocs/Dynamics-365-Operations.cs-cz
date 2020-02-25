---
title: Řešení potíží u analytických sestav
description: Tento článek vysvětluje, jak postupovat, když e nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008303"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="3fe17-103">Řešení potíží u analytických sestav</span><span class="sxs-lookup"><span data-stu-id="3fe17-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="3fe17-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="3fe17-104">**Issue**</span></span>

<span data-ttu-id="3fe17-105">Změny dat odběratele nejsou zobrazeny na kartách **Analytika** v žádném z pracovních prostorů odběratele.</span><span class="sxs-lookup"><span data-stu-id="3fe17-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="3fe17-106">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="3fe17-106">**Cause**</span></span>

<span data-ttu-id="3fe17-107">Ve výchozím nastavení se sestavy Microsoft Power BI aktualizují každé čtyři hodiny, podle plánu dávkové úlohy Nasadit měrný systém.</span><span class="sxs-lookup"><span data-stu-id="3fe17-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="3fe17-108">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="3fe17-108">**Resolution**</span></span>

<span data-ttu-id="3fe17-109">Tento problém může být pouze záležitostí časování.</span><span class="sxs-lookup"><span data-stu-id="3fe17-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="3fe17-110">Tento postup slouží ke spuštění dávkové úlohy a aktualizaci pracovní prostorů analytiky.</span><span class="sxs-lookup"><span data-stu-id="3fe17-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="3fe17-111">Otevřete stránku **Dávkové úlohy** v možnostech **Správa systému \> Odkazy \> Dávkové úlohy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="3fe17-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="3fe17-112">Nebo použijte vyhledávání a zadejte **Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="3fe17-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="3fe17-113">Vyhledejte úlohu **Nasadit měrný systém** v seznamu.</span><span class="sxs-lookup"><span data-stu-id="3fe17-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="3fe17-114">Vyberte **Upravit** v horní části stránky a nastavte naplánované počáteční datum a čas na hodnotu, která bude aktualizovat analytiku blíže aktuálnímu času.</span><span class="sxs-lookup"><span data-stu-id="3fe17-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Dávkové úlohy](media/batch-jobs.png)
