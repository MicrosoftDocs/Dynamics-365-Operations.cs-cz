---
title: Spolupráce s odběrateli interního dodavatelského řetězce
description: Tato procedura ukazuje, jak zobrazit všechny plánované objednávky, které budou splněny mezipodnikovým dodavatelem.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2746534cc808dc61e54aa55c1030422bb37e8984
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148140"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="8247c-103">Spolupráce s odběrateli interního dodavatelského řetězce</span><span class="sxs-lookup"><span data-stu-id="8247c-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8247c-104">Tato procedura ukazuje, jak zobrazit všechny plánované objednávky, které budou splněny mezipodnikovým dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="8247c-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="8247c-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="8247c-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="8247c-106">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="8247c-106">Click Master planning.</span></span>
2. <span data-ttu-id="8247c-107">V poli Plán zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8247c-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="8247c-108">V poli Plán vyberte plán 10.</span><span class="sxs-lookup"><span data-stu-id="8247c-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="8247c-109">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="8247c-109">Click Run.</span></span>
4. <span data-ttu-id="8247c-110">Do pole Počet vláken zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="8247c-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="8247c-111">To představuje počet paralelních podprocesů použitých pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="8247c-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="8247c-112">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8247c-112">Click OK.</span></span>
    * <span data-ttu-id="8247c-113">Tato operace může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="8247c-113">This may take a while.</span></span>  
6. <span data-ttu-id="8247c-114">Klikněte na Plánovaná mezipodniková poptávka.</span><span class="sxs-lookup"><span data-stu-id="8247c-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="8247c-115">Klikněte na Zobrazit výstupní plánovanou mezipodnikovou poptávku.</span><span class="sxs-lookup"><span data-stu-id="8247c-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="8247c-116">Tato stránka obsahuje přehled plánované poptávky, kterou splní dodavatel interního zásobovacího řetězce.</span><span class="sxs-lookup"><span data-stu-id="8247c-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="8247c-117">Rozbalte část Podrobnosti nadřazené poptávky.</span><span class="sxs-lookup"><span data-stu-id="8247c-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="8247c-118">V této části můžete zobrazit podrobnosti o tom, jak bude splněna poptávka.</span><span class="sxs-lookup"><span data-stu-id="8247c-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="8247c-119">Než se zde zobrazí další informace, budete muset počkat na spuštění hlavního plánování v dodavatelské společnosti.</span><span class="sxs-lookup"><span data-stu-id="8247c-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

