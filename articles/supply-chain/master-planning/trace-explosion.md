---
title: Použití sledování pro rozpad
description: V tomto článku je vysvětleno použití sledování k prozkoumání příčin výsledku rozpadu objednávky.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e777d69c9da8a19c186bca3ca591e59af232f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423587"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="7a6f2-103">Použití sledování pro rozpad</span><span class="sxs-lookup"><span data-stu-id="7a6f2-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a6f2-104">V tomto článku je vysvětleno použití sledování k prozkoumání příčin výsledku rozpadu objednávky.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="7a6f2-105">Po povolení sledování můžete zobrazit informace o činitelích, které tvoří výsledek rozpadu určité objednávky.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="7a6f2-106">Na následujícím příkladu je znázorněno, jak lze použít informace o sledování:</span><span class="sxs-lookup"><span data-stu-id="7a6f2-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="7a6f2-107">Zobrazit vztahy mezi akcemi na plánovaných objednávkách za účelem optimalizace dodavatelského řetězce a skladových rezervací.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="7a6f2-108">Zobrazit vztahy k objednávkám, které již byly schváleny.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="7a6f2-109">Můžete se zaměřit na automatické potvrzování odvozených požadavků a přesněji stanovit prioritu objednávky.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="7a6f2-110">Simulovat výsledky plánování a určit, zda jsou parametry plánování optimální.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="7a6f2-111">Určit způsob, jakým byly pro objednávku určovány informace, jako například data výroby, množství a priority.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="7a6f2-112">Můžete zobrazit podrobnosti o termínech a akcích pro vybranou objednávku.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="7a6f2-113">Na stránce **Rozpad** jsou na kartě **Vysvětlení** v horním podokně k dispozici informace o sledování.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="7a6f2-114">K sledování dochází, když rozložíte objednávku.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="7a6f2-115">Sledování objednávky zahájíte kliknutím na možnost **Aktualizace** a následným označením zaškrtávacího políčka **Povolit sledování**.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="7a6f2-116">Při vyhledávání konkrétních informací v protokolu můžete použít pole **Najít text**.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="7a6f2-117">Výsledky hledání jsou zvýrazněny ve stromové struktuře.</span><span class="sxs-lookup"><span data-stu-id="7a6f2-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="7a6f2-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7a6f2-118">Additional resources</span></span>
--------

[<span data-ttu-id="7a6f2-119">Přehled hlavních plánů</span><span class="sxs-lookup"><span data-stu-id="7a6f2-119">Master plans overview</span></span>](master-plans.md)



