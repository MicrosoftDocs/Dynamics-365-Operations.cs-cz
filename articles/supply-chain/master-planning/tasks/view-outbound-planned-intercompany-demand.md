--- 
title: "Zobrazení výstupní plánované mezipodnikové poptávky"
description: "Tato procedura ukazuje, jak zobrazit všechny plánované objednávky, které budou splněny mezipodnikovým dodavatelem."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 183bbba80351c19d2218c577020b1e852ab45ac4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="f6139-103">Zobrazení výstupní plánované mezipodnikové poptávky</span><span class="sxs-lookup"><span data-stu-id="f6139-103">View outbound planned intercompany demand</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6139-104">Tato procedura ukazuje, jak zobrazit všechny plánované objednávky, které budou splněny mezipodnikovým dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="f6139-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="f6139-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="f6139-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="f6139-106">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f6139-106">Click Master planning.</span></span>
2. <span data-ttu-id="f6139-107">V poli Plán zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f6139-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="f6139-108">V poli Plán vyberte plán 10.</span><span class="sxs-lookup"><span data-stu-id="f6139-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="f6139-109">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="f6139-109">Click Run.</span></span>
4. <span data-ttu-id="f6139-110">Do pole Počet vláken zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="f6139-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="f6139-111">To představuje počet paralelních podprocesů použitých pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f6139-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="f6139-112">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f6139-112">Click OK.</span></span>
    * <span data-ttu-id="f6139-113">Tato operace může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="f6139-113">This may take a while.</span></span>  
6. <span data-ttu-id="f6139-114">Klikněte na Plánovaná mezipodniková poptávka.</span><span class="sxs-lookup"><span data-stu-id="f6139-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="f6139-115">Klikněte na Zobrazit výstupní plánovanou mezipodnikovou poptávku.</span><span class="sxs-lookup"><span data-stu-id="f6139-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="f6139-116">Tato stránka obsahuje přehled plánované poptávky, kterou splní dodavatel interního zásobovacího řetězce.</span><span class="sxs-lookup"><span data-stu-id="f6139-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="f6139-117">Rozbalte část Podrobnosti nadřazené poptávky.</span><span class="sxs-lookup"><span data-stu-id="f6139-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="f6139-118">V této části můžete zobrazit podrobnosti o tom, jak bude splněna poptávka.</span><span class="sxs-lookup"><span data-stu-id="f6139-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="f6139-119">Než se zde zobrazí další informace, budete muset počkat na spuštění hlavního plánování v dodavatelské společnosti.</span><span class="sxs-lookup"><span data-stu-id="f6139-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  


