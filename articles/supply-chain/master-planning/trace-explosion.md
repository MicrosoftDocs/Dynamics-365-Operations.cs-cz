---
title: Použití sledování pro rozpad
description: V tomto článku je vysvětleno použití sledování k prozkoumání příčin výsledku rozpadu objednávky.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a6123d7443cce51e95aa6d1fdb1fdc19d001d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557841"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="e03da-103">Použití sledování pro rozpad</span><span class="sxs-lookup"><span data-stu-id="e03da-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e03da-104">V tomto článku je vysvětleno použití sledování k prozkoumání příčin výsledku rozpadu objednávky.</span><span class="sxs-lookup"><span data-stu-id="e03da-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="e03da-105">Po povolení sledování můžete zobrazit informace o činitelích, které tvoří výsledek rozpadu určité objednávky.</span><span class="sxs-lookup"><span data-stu-id="e03da-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="e03da-106">Na následujícím příkladu je znázorněno, jak lze použít informace o sledování:</span><span class="sxs-lookup"><span data-stu-id="e03da-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="e03da-107">Zobrazit vztahy mezi akcemi na plánovaných objednávkách za účelem optimalizace dodavatelského řetězce a skladových rezervací.</span><span class="sxs-lookup"><span data-stu-id="e03da-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="e03da-108">Zobrazit vztahy k objednávkám, které již byly schváleny.</span><span class="sxs-lookup"><span data-stu-id="e03da-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="e03da-109">Můžete se zaměřit na automatické potvrzování odvozených požadavků a přesněji stanovit prioritu objednávky.</span><span class="sxs-lookup"><span data-stu-id="e03da-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="e03da-110">Simulovat výsledky plánování a určit, zda jsou parametry plánování optimální.</span><span class="sxs-lookup"><span data-stu-id="e03da-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="e03da-111">Určit způsob, jakým byly pro objednávku určovány informace, jako například data výroby, množství a priority.</span><span class="sxs-lookup"><span data-stu-id="e03da-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="e03da-112">Můžete zobrazit podrobnosti o termínech a akcích pro vybranou objednávku.</span><span class="sxs-lookup"><span data-stu-id="e03da-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="e03da-113">Na stránce **Rozpad** jsou na kartě **Vysvětlení** v horním podokně k dispozici informace o sledování.</span><span class="sxs-lookup"><span data-stu-id="e03da-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="e03da-114">K sledování dochází, když rozložíte objednávku.</span><span class="sxs-lookup"><span data-stu-id="e03da-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="e03da-115">Sledování objednávky zahájíte kliknutím na možnost **Aktualizace**a následným označením zaškrtávacího políčka **Povolit sledování**.</span><span class="sxs-lookup"><span data-stu-id="e03da-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="e03da-116">Při vyhledávání konkrétních informací v protokolu můžete použít pole **Najít text**.</span><span class="sxs-lookup"><span data-stu-id="e03da-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="e03da-117">Výsledky hledání jsou zvýrazněny ve stromové struktuře.</span><span class="sxs-lookup"><span data-stu-id="e03da-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="e03da-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e03da-118">Additional resources</span></span>
--------

[<span data-ttu-id="e03da-119">Hlavní plány</span><span class="sxs-lookup"><span data-stu-id="e03da-119">Master plans</span></span>](master-plans.md)



