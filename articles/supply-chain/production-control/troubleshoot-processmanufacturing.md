---
title: Řešení potíží s procesní výrobou
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s procesní výrobou.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966173"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="a3fb7-103">Řešení potíží s procesní výrobou</span><span class="sxs-lookup"><span data-stu-id="a3fb7-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="a3fb7-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s procesní výrobou.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="a3fb7-105">Když použiji zařízení úkolového lístku k nahlášení částečného množství na posledním úkolu ve výrobní zakázce, automaticky se ukončí všechny předchozí úkoly na této zakázce, které mají stav Probíhá.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="a3fb7-106">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-106">This behavior is by design.</span></span> <span data-ttu-id="a3fb7-107">Na stránce **Výchozí hodnoty výrobní zakázky** na kartě **Nahlásit jako dokončené** je možnost s názvem **Ukončení tech. postupu**.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="a3fb7-108">Pokud je toto téma nastaveno na *Ano*, deník karet postupů se zaúčtuje, když pracovník použije zařízení úkolového lístku nebo terminál úkolového lístku k nahlášení poslední operace.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="a3fb7-109">Tento deník označuje všechny operace jako dokončené a ukončí všechny produkční úlohy.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="a3fb7-110">Když je možnost **Ukončení tech. postupu** nastavena na *Ano*, systém nezohledňuje stav úlohy, který pracovník vybral, když ohlásil poslední operaci.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="a3fb7-111">Systém také nezvažuje, zda pracovník hlásí úplné nebo částečné množství.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="a3fb7-112">Když se pokusím o uzavření skladu, zobrazí se následující varovná zpráva: „Žádné provedení výpočtu zpětného účtování nákladů s datem konce odpovídajícího období %1 nebylo zaregistrováno."</span><span class="sxs-lookup"><span data-stu-id="a3fb7-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="a3fb7-113">Ve verzích před vydáním 10.0.13, pokud nepoužíváte tok výpočtu nákladů štíhlé výroby, zobrazí se během uzávěrky skladu následující chybová varovná zpráva:</span><span class="sxs-lookup"><span data-stu-id="a3fb7-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="a3fb7-114">Chystáte se provést uzávěrku skladu s datem %1.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="a3fb7-115">Žádné provedení výpočtu zpětného účtování nákladů s datem konce odpovídajícího období %1 nebylo zaregistrováno.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="a3fb7-116">Nezapomeňte spustit výpočet zpětného účtování nákladů s datem konce odpovídajícího období %1.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="a3fb7-117">Ocenění zásob, náklady prodaného zboží a odchylky nemusí být správné v dílčí knize nebo hlavní knize, dokud to nebude provedeno.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="a3fb7-118">Tento problém byl opraven ve verzi 10.0.13 a novější.</span><span class="sxs-lookup"><span data-stu-id="a3fb7-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="a3fb7-119">Další informace naleznete v [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="a3fb7-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
