---
title: "Částka pro zaokrouhlení výpočtů odpisů"
description: "Tento článek popisuje pole Zaokrouhlit odpis, které se nachází na stránce Nastavení knihy."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0ad57b076542c38d3c29dba4caacf830de6f7200
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="a3c93-103">Částka pro zaokrouhlení výpočtů odpisů</span><span class="sxs-lookup"><span data-stu-id="a3c93-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a3c93-104">Tento článek popisuje pole Zaokrouhlit odpis, které se nachází na stránce Nastavení knihy.</span><span class="sxs-lookup"><span data-stu-id="a3c93-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="a3c93-105">Celková částka odpisů je stanovena pro každou knihu.</span><span class="sxs-lookup"><span data-stu-id="a3c93-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="a3c93-106">Současné odpisové částky se používají v profilu odpisování dlouhodobého majetku, který ukazuje budoucí odpisy a hodnotu dlouhodobého majetku, a také v návrzích na odpisy.</span><span class="sxs-lookup"><span data-stu-id="a3c93-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="a3c93-107">Zadejte nejnižší částku odpisu povolenou pro tuto knihu.</span><span class="sxs-lookup"><span data-stu-id="a3c93-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="a3c93-108">Bez ohledu na nastavené zaokrouhlování, není částka odpisu v posledním období odpisu zaokrouhlena.</span><span class="sxs-lookup"><span data-stu-id="a3c93-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="a3c93-109">Na konci posledního období odpisu musí být hodnota dlouhodobého majetku 0 (nula) nebo hodnotu odpadu, pokud se používá konečná zůstatková hodnota.</span><span class="sxs-lookup"><span data-stu-id="a3c93-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="a3c93-110">Příklad</span><span class="sxs-lookup"><span data-stu-id="a3c93-110">Example</span></span>

<span data-ttu-id="a3c93-111">Odpis je bez zaokrouhlení vypočítán v částce 2 444,44.</span><span class="sxs-lookup"><span data-stu-id="a3c93-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="a3c93-112">Stejně jako v následující tabulce se částky, které budou nabízeny, liší v závislosti na tom, jak je nastavené zaokrouhlování.</span><span class="sxs-lookup"><span data-stu-id="a3c93-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="a3c93-113">Metoda zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="a3c93-113">Rounding method</span></span> | <span data-ttu-id="a3c93-114">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="a3c93-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="a3c93-115">Zaokrouhlení 0,1</span><span class="sxs-lookup"><span data-stu-id="a3c93-115">Rounding 0.1</span></span>    | <span data-ttu-id="a3c93-116">2 444,40</span><span class="sxs-lookup"><span data-stu-id="a3c93-116">2,444.40</span></span>            |
| <span data-ttu-id="a3c93-117">Zaokrouhlení 1,00</span><span class="sxs-lookup"><span data-stu-id="a3c93-117">Rounding 1.00</span></span>   | <span data-ttu-id="a3c93-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="a3c93-118">2,444.00</span></span>            |
| <span data-ttu-id="a3c93-119">Zaokrouhlení 10,00</span><span class="sxs-lookup"><span data-stu-id="a3c93-119">Rounding 10.00</span></span>  | <span data-ttu-id="a3c93-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="a3c93-120">2,440.00</span></span>            |
| <span data-ttu-id="a3c93-121">Zaokrouhlení 100,00</span><span class="sxs-lookup"><span data-stu-id="a3c93-121">Rounding 100.00</span></span> | <span data-ttu-id="a3c93-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="a3c93-122">2,400.00</span></span>            |






