---
title: Běžné zdroje výrobních odchylek
description: Tento článek vysvětluje různé obvyklé zdroje každého typu výrobní odchylky.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f36e482595cad49d1149873f8bcdd6a05a3287d5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229272"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="11918-103">Běžné zdroje výrobních odchylek</span><span class="sxs-lookup"><span data-stu-id="11918-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11918-104">Tento článek vysvětluje různé obvyklé zdroje každého typu výrobní odchylky.</span><span class="sxs-lookup"><span data-stu-id="11918-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="11918-105">Zde jsou některé typické zdroje odchylek ve **velikosti šarže**:</span><span class="sxs-lookup"><span data-stu-id="11918-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="11918-106">Množství zboží pro výrobní zakázku se liší od množství pro výpočet používané ve standardním výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="11918-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="11918-107">Toto množství poskytuje základ pro amortizaci konstantních nákladů.</span><span class="sxs-lookup"><span data-stu-id="11918-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="11918-108">Hodnota konstantních nákladů ve výrobní zakázce se liší od konstantních nákladů používaných ve standardním výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="11918-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="11918-109">Konstantní náklady ve výrobní zakázce se mohou lišit z několika důvodů.</span><span class="sxs-lookup"><span data-stu-id="11918-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="11918-110">Konstantní náklady mohou například odrážet následující faktory:</span><span class="sxs-lookup"><span data-stu-id="11918-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="11918-111">ruční změny ve výrobním kusovníku, kusovníku nebo postupu;</span><span class="sxs-lookup"><span data-stu-id="11918-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="11918-112">výběr jiné verze kusovníku nebo verze postupu při vytváření výrobní zakázky;</span><span class="sxs-lookup"><span data-stu-id="11918-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="11918-113">plánované technické změny verze kusovníku nebo verze postupu, která je přiřazena k položce.</span><span class="sxs-lookup"><span data-stu-id="11918-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="11918-114">Zde jsou některé typické zdroje odchylek ve **výrobní ceně**:</span><span class="sxs-lookup"><span data-stu-id="11918-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="11918-115">Kategorie nákladů (a cena kategorie nákladů) vykazované spotřeby operace postupu se liší od kategorie nákladů používané ve standardním výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="11918-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="11918-116">Aktivní náklad ceny kategorie nákladů se liší od ceny kategorie nákladů používané ve standardním výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="11918-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="11918-117">Zde jsou některé typické zdroje odchylek ve **výrobním množství**:</span><span class="sxs-lookup"><span data-stu-id="11918-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="11918-118">nadměrný příjem materiálové komponenty nebo nedostatečný příjem materiálové komponenty;</span><span class="sxs-lookup"><span data-stu-id="11918-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="11918-119">nadměrný nebo nedostatečný čas sestavy pro operace postupu;</span><span class="sxs-lookup"><span data-stu-id="11918-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="11918-120">nadměrný nebo nedostatečný příjem množství zboží nadřazené položky, ve vztahu k množství objednávky.</span><span class="sxs-lookup"><span data-stu-id="11918-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="11918-121">Avšak vydáte komponenty a plně vykážete operace na základě objednaného množství ve výrobní zakázce.</span><span class="sxs-lookup"><span data-stu-id="11918-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="11918-122">Zde jsou některé typické zdroje odchylek v **nahrazení výroby**:</span><span class="sxs-lookup"><span data-stu-id="11918-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="11918-123">výdej materiálové komponenty, která se nenachází ve výrobním kusovníku;</span><span class="sxs-lookup"><span data-stu-id="11918-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="11918-124">ruční přidání komponenty do výrobního kusovníku a vykázání této komponenty jako spotřebované;</span><span class="sxs-lookup"><span data-stu-id="11918-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="11918-125">vykázání položky jako spotřebované, avšak bez ručního přidání této položky do výrobního kusovníku;</span><span class="sxs-lookup"><span data-stu-id="11918-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="11918-126">ruční přidání operace do výrobního postupu a vykázání této operace jako spotřebované;</span><span class="sxs-lookup"><span data-stu-id="11918-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="11918-127">při vytváření výrobní zakázky vyberete verzi kusovníku, která se liší od verze kusovníku používané ve standardním výpočtu nákladů;</span><span class="sxs-lookup"><span data-stu-id="11918-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="11918-128">při vytváření výrobní zakázky vyberete verzi postupu, která se liší od verze postupu používané ve standardním výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="11918-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]