---
title: Správa sortimentů (listopad 2016)
description: Tato procedura ukazuje, jak vytvářet a publikovat nový sortiment produktů a používá ukázkovou datovou firmu USRT.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailCategoryAndProductWorkspace, RetailCategoryAndProductAssortment, RetailAssortmentDetails, RetailOperatingUnitPicker, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96c79558c3248406a1b5988f9c9dc9783db4406
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564338"
---
# <a name="manage-assortments-november-2016"></a><span data-ttu-id="35caa-103">Správa sortimentů (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="35caa-103">Manage assortments (November 2016)</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="35caa-104">Tato procedura ukazuje, jak vytvářet a publikovat nový sortiment produktů a používá ukázkovou datovou firmu USRT.</span><span class="sxs-lookup"><span data-stu-id="35caa-104">This procedure demonstrates how to create and publish a new product assortment and uses the demo data company USRT.</span></span> <span data-ttu-id="35caa-105">Tato procedura vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější a platformu Dynamics AX 7.1.</span><span class="sxs-lookup"><span data-stu-id="35caa-105">This procedure requires Dynamics AX application 7.0.1 or later, and Dynamics AX platform 7.1.</span></span>  

1. <span data-ttu-id="35caa-106">Klikněte na Správa kategorií a produktů.</span><span class="sxs-lookup"><span data-stu-id="35caa-106">Click Category and product management.</span></span>

## <a name="create-an-assortment"></a><span data-ttu-id="35caa-107">Vytvoření sortimentu</span><span class="sxs-lookup"><span data-stu-id="35caa-107">Create an assortment</span></span>
1. <span data-ttu-id="35caa-108">Klikněte na kartu Sortimenty.</span><span class="sxs-lookup"><span data-stu-id="35caa-108">Click the Assortments tab.</span></span>
2. <span data-ttu-id="35caa-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="35caa-109">Click New.</span></span>
3. <span data-ttu-id="35caa-110">Klikněte na tlačítko Sortiment.</span><span class="sxs-lookup"><span data-stu-id="35caa-110">Click Assortment.</span></span>
    * <span data-ttu-id="35caa-111">ID sortimentu je požadováno a musí mít jedinečnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="35caa-111">The Assortment ID is required and must be a unique value.</span></span>  
4. <span data-ttu-id="35caa-112">Do pole Název sortimentu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="35caa-112">In the Assortment name field, type a value.</span></span>
5. <span data-ttu-id="35caa-113">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="35caa-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="35caa-114">Do pole Datum vypršení platnosti zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="35caa-114">In the Expiration date field, enter a date.</span></span>
7. <span data-ttu-id="35caa-115">Rozbalte část Maloobchodní sítě.</span><span class="sxs-lookup"><span data-stu-id="35caa-115">Expand the Retail channels section.</span></span>
8. <span data-ttu-id="35caa-116">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="35caa-116">Click Add line.</span></span>
9. <span data-ttu-id="35caa-117">Ve stromovém zobrazení vyberte „Contoso Retail\Electronics\Boston“.</span><span class="sxs-lookup"><span data-stu-id="35caa-117">In the tree, select 'Contoso Retail\Electronics\Boston'.</span></span>
10. <span data-ttu-id="35caa-118">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="35caa-118">Click Add.</span></span>
11. <span data-ttu-id="35caa-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="35caa-119">Click OK.</span></span>
12. <span data-ttu-id="35caa-120">Rozbalte část Produkty.</span><span class="sxs-lookup"><span data-stu-id="35caa-120">Expand the Products section.</span></span>
13. <span data-ttu-id="35caa-121">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="35caa-121">Click Add line.</span></span>
14. <span data-ttu-id="35caa-122">V poli Kategorie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="35caa-122">In the Category field, enter or select a value.</span></span>
15. <span data-ttu-id="35caa-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="35caa-123">Click Save.</span></span>

## <a name="publish-an-assortment"></a><span data-ttu-id="35caa-124">Publikování sortimentu</span><span class="sxs-lookup"><span data-stu-id="35caa-124">Publish an assortment</span></span>
1. <span data-ttu-id="35caa-125">Klikněte na tlačítko Publikovat.</span><span class="sxs-lookup"><span data-stu-id="35caa-125">Click Publish.</span></span>
2. <span data-ttu-id="35caa-126">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="35caa-126">Click Yes.</span></span>

