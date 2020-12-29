---
title: Zobrazení výstupní plánované mezipodnikové poptávky
description: Tato procedura ukazuje, jak zobrazit všechny plánované objednávky, které budou splněny mezipodnikovým dodavatelem.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 259ce229c18466b7d29fd231dc3f0be8a6906c6b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423588"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="ad6de-103">Zobrazení výstupní plánované mezipodnikové poptávky</span><span class="sxs-lookup"><span data-stu-id="ad6de-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad6de-104">Tato procedura ukazuje, jak zobrazit všechny plánované objednávky, které budou splněny mezipodnikovým dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="ad6de-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="ad6de-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="ad6de-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="ad6de-106">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="ad6de-106">Click Master planning.</span></span>
2. <span data-ttu-id="ad6de-107">V poli Plán zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ad6de-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="ad6de-108">V poli Plán vyberte plán 10.</span><span class="sxs-lookup"><span data-stu-id="ad6de-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="ad6de-109">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="ad6de-109">Click Run.</span></span>
4. <span data-ttu-id="ad6de-110">Do pole Počet vláken zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ad6de-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="ad6de-111">To představuje počet paralelních podprocesů použitých pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="ad6de-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="ad6de-112">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ad6de-112">Click OK.</span></span>
    * <span data-ttu-id="ad6de-113">Tato operace může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="ad6de-113">This may take a while.</span></span>  
6. <span data-ttu-id="ad6de-114">Klikněte na Plánovaná mezipodniková poptávka.</span><span class="sxs-lookup"><span data-stu-id="ad6de-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="ad6de-115">Klikněte na Zobrazit výstupní plánovanou mezipodnikovou poptávku.</span><span class="sxs-lookup"><span data-stu-id="ad6de-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="ad6de-116">Tato stránka obsahuje přehled plánované poptávky, kterou splní dodavatel interního zásobovacího řetězce.</span><span class="sxs-lookup"><span data-stu-id="ad6de-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="ad6de-117">Rozbalte část Podrobnosti nadřazené poptávky.</span><span class="sxs-lookup"><span data-stu-id="ad6de-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="ad6de-118">V této části můžete zobrazit podrobnosti o tom, jak bude splněna poptávka.</span><span class="sxs-lookup"><span data-stu-id="ad6de-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="ad6de-119">Než se zde zobrazí další informace, budete muset počkat na spuštění hlavního plánování v dodavatelské společnosti.</span><span class="sxs-lookup"><span data-stu-id="ad6de-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

