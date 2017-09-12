--- 
title: "Schválení modelu konfigurace produktu"
description: "Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa4548d3017246cbe49e2613f8990df6ea1c368b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="4cf7d-103">Schválení modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="4cf7d-103">Approve a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cf7d-104">Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="4cf7d-105">Tento postup využívá model špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="4cf7d-106">Všimněte si, že tento model již byl schválen, ale postup vás provede celým procesem.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="4cf7d-107">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="4cf7d-108">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="4cf7d-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4cf7d-110">Pro tuto proceduru vyberte model špičkového reproduktoru.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="4cf7d-111">Klepněte na Verze.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-111">Click Versions.</span></span>
5. <span data-ttu-id="4cf7d-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-112">Click New.</span></span>
6. <span data-ttu-id="4cf7d-113">V poli Číslo produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="4cf7d-114">Odkaz na produkt představuje verzi modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="4cf7d-115">V seznamu se zobrazí pouze základní produkty, které mají technologii konfigurace založenou na omezeních.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="4cf7d-116">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4cf7d-117">Vyberte, kdy bude verze modelu produktu k dispozici.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="4cf7d-118">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="4cf7d-119">Vyberte koncové datum, kdy této verzi modelu produktu vyprší platnost, nebo vyberte Nikdy.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="4cf7d-120">Klepnutím na možnost Schválit otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="4cf7d-121">V poli Schválil(a) zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="4cf7d-122">Vyberte osobu, která je odpovědná za schválení modelů produktu pro použití v operacích.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="4cf7d-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-123">Click OK.</span></span>
12. <span data-ttu-id="4cf7d-124">Vyberte možnost v poli Metoda cenových kalkulací.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="4cf7d-125">Aktivujte verzi modelu výrobku.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-125">Activate the product model version.</span></span> <span data-ttu-id="4cf7d-126">Pro jeden model produktu je možné současně mít aktivní pouze jeden produkt.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="4cf7d-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4cf7d-127">Close the page.</span></span>


