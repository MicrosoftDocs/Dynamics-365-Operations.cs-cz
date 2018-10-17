--- 
title: "Správa sortimentů (listopad 2016)"
description: "Tato procedura ukazuje, jak vytvářet a publikovat nový sortiment produktů a používá ukázkovou datovou firmu USRT."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, RetailCategoryAndProductWorkspace, RetailCategoryAndProductAssortment, RetailAssortmentDetails, RetailOperatingUnitPicker, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f96c79558c3248406a1b5988f9c9dc9783db4406
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="manage-assortments-november-2016"></a><span data-ttu-id="ec03d-103">Správa sortimentů (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="ec03d-103">Manage assortments (November 2016)</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ec03d-104">Tato procedura ukazuje, jak vytvářet a publikovat nový sortiment produktů a používá ukázkovou datovou firmu USRT.</span><span class="sxs-lookup"><span data-stu-id="ec03d-104">This procedure demonstrates how to create and publish a new product assortment and uses the demo data company USRT.</span></span> <span data-ttu-id="ec03d-105">Tato procedura vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější a platformu Dynamics AX 7.1.</span><span class="sxs-lookup"><span data-stu-id="ec03d-105">This procedure requires Dynamics AX application 7.0.1 or later, and Dynamics AX platform 7.1.</span></span>  

1. <span data-ttu-id="ec03d-106">Klikněte na Správa kategorií a produktů.</span><span class="sxs-lookup"><span data-stu-id="ec03d-106">Click Category and product management.</span></span>

## <a name="create-an-assortment"></a><span data-ttu-id="ec03d-107">Vytvoření sortimentu</span><span class="sxs-lookup"><span data-stu-id="ec03d-107">Create an assortment</span></span>
1. <span data-ttu-id="ec03d-108">Klikněte na kartu Sortimenty.</span><span class="sxs-lookup"><span data-stu-id="ec03d-108">Click the Assortments tab.</span></span>
2. <span data-ttu-id="ec03d-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ec03d-109">Click New.</span></span>
3. <span data-ttu-id="ec03d-110">Klikněte na tlačítko Sortiment.</span><span class="sxs-lookup"><span data-stu-id="ec03d-110">Click Assortment.</span></span>
    * <span data-ttu-id="ec03d-111">ID sortimentu je požadováno a musí mít jedinečnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ec03d-111">The Assortment ID is required and must be a unique value.</span></span>  
4. <span data-ttu-id="ec03d-112">Do pole Název sortimentu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ec03d-112">In the Assortment name field, type a value.</span></span>
5. <span data-ttu-id="ec03d-113">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="ec03d-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="ec03d-114">Do pole Datum vypršení platnosti zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="ec03d-114">In the Expiration date field, enter a date.</span></span>
7. <span data-ttu-id="ec03d-115">Rozbalte část Maloobchodní sítě.</span><span class="sxs-lookup"><span data-stu-id="ec03d-115">Expand the Retail channels section.</span></span>
8. <span data-ttu-id="ec03d-116">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="ec03d-116">Click Add line.</span></span>
9. <span data-ttu-id="ec03d-117">Ve stromovém zobrazení vyberte „Contoso Retail\Electronics\Boston“.</span><span class="sxs-lookup"><span data-stu-id="ec03d-117">In the tree, select 'Contoso Retail\Electronics\Boston'.</span></span>
10. <span data-ttu-id="ec03d-118">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="ec03d-118">Click Add.</span></span>
11. <span data-ttu-id="ec03d-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ec03d-119">Click OK.</span></span>
12. <span data-ttu-id="ec03d-120">Rozbalte část Produkty.</span><span class="sxs-lookup"><span data-stu-id="ec03d-120">Expand the Products section.</span></span>
13. <span data-ttu-id="ec03d-121">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="ec03d-121">Click Add line.</span></span>
14. <span data-ttu-id="ec03d-122">V poli Kategorie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ec03d-122">In the Category field, enter or select a value.</span></span>
15. <span data-ttu-id="ec03d-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ec03d-123">Click Save.</span></span>

## <a name="publish-an-assortment"></a><span data-ttu-id="ec03d-124">Publikování sortimentu</span><span class="sxs-lookup"><span data-stu-id="ec03d-124">Publish an assortment</span></span>
1. <span data-ttu-id="ec03d-125">Klikněte na tlačítko Publikovat.</span><span class="sxs-lookup"><span data-stu-id="ec03d-125">Click Publish.</span></span>
2. <span data-ttu-id="ec03d-126">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="ec03d-126">Click Yes.</span></span>


