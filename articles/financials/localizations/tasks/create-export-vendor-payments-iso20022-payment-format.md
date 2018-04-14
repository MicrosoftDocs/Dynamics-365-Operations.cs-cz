--- 
title: "Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022"
description: "Tento postup ukazuje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5787edc4a041e4b571c7ab6f056f4bd0a17cf2d7
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="4988c-103">Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022</span><span class="sxs-lookup"><span data-stu-id="4988c-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4988c-104">Tento postup ukazuje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022.</span><span class="sxs-lookup"><span data-stu-id="4988c-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="4988c-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="4988c-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="4988c-106">Toto je pátý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4988c-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="4988c-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="4988c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="4988c-108">Vytvoření řádků platby</span><span class="sxs-lookup"><span data-stu-id="4988c-108">Create payment lines</span></span>
1. <span data-ttu-id="4988c-109">Přejděte na Závazky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="4988c-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="4988c-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4988c-110">Click New.</span></span>
3. <span data-ttu-id="4988c-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4988c-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4988c-112">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4988c-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="4988c-113">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="4988c-113">Click Lines.</span></span>
6. <span data-ttu-id="4988c-114">Klikněte na Návrh platby.</span><span class="sxs-lookup"><span data-stu-id="4988c-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="4988c-115">Klikněte na Vytvořit návrh plateb.</span><span class="sxs-lookup"><span data-stu-id="4988c-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="4988c-116">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="4988c-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="4988c-117">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="4988c-117">Click Filter.</span></span>
10. <span data-ttu-id="4988c-118">V seznamu vyberte řádek pro tabulku dodavatelů a pole Účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4988c-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="4988c-119">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4988c-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="4988c-120">Můžete použít všechna kritéria pro výběr transakcí dodavatele k zaplacení. Pro tento příklad použijte DE-001 jako účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4988c-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="4988c-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4988c-121">Click OK.</span></span>
13. <span data-ttu-id="4988c-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4988c-122">Click OK.</span></span>
14. <span data-ttu-id="4988c-123">Klikněte na Vytvořit platby.</span><span class="sxs-lookup"><span data-stu-id="4988c-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="4988c-124">Vygenerování souboru platby ISO20022</span><span class="sxs-lookup"><span data-stu-id="4988c-124">Generate an ISO20022 payment file</span></span>


