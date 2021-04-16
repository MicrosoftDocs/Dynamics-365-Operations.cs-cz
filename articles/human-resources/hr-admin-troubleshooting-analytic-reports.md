---
title: Řešení potíží u analytických sestav
description: Tento článek vysvětluje, jak postupovat, když e nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794966"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="67ab9-103">Řešení potíží u analytických sestav</span><span class="sxs-lookup"><span data-stu-id="67ab9-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="67ab9-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="67ab9-104">**Issue**</span></span>

<span data-ttu-id="67ab9-105">Změny dat odběratele nejsou zobrazeny na kartách **Analytika** v žádném z pracovních prostorů odběratele.</span><span class="sxs-lookup"><span data-stu-id="67ab9-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="67ab9-106">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="67ab9-106">**Cause**</span></span>

<span data-ttu-id="67ab9-107">Ve výchozím nastavení se sestavy Microsoft Power BI aktualizují každé čtyři hodiny, podle plánu dávkové úlohy Nasadit měrný systém.</span><span class="sxs-lookup"><span data-stu-id="67ab9-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="67ab9-108">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="67ab9-108">**Resolution**</span></span>

<span data-ttu-id="67ab9-109">Tento problém může být pouze záležitostí časování.</span><span class="sxs-lookup"><span data-stu-id="67ab9-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="67ab9-110">Tento postup slouží ke spuštění dávkové úlohy a aktualizaci pracovní prostorů analytiky.</span><span class="sxs-lookup"><span data-stu-id="67ab9-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="67ab9-111">Otevřete stránku **Dávkové úlohy** v možnostech **Správa systému \> Odkazy \> Dávkové úlohy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="67ab9-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="67ab9-112">Nebo použijte vyhledávání a zadejte **Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="67ab9-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="67ab9-113">Vyhledejte úlohu **Nasadit měrný systém** v seznamu.</span><span class="sxs-lookup"><span data-stu-id="67ab9-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="67ab9-114">Vyberte **Upravit** v horní části stránky a nastavte naplánované počáteční datum a čas na hodnotu, která bude aktualizovat analytiku blíže aktuálnímu času.</span><span class="sxs-lookup"><span data-stu-id="67ab9-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Dávkové úlohy](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]