---
title: Částka pro zaokrouhlení výpočtů odpisů
description: Tento článek popisuje pole Zaokrouhlit odpis, které se nachází na stránce Nastavení knihy.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40fd019b1b5900fbd15866d9d3c32ed6d88147b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441213"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="466f8-103">Částka pro zaokrouhlení výpočtů odpisů</span><span class="sxs-lookup"><span data-stu-id="466f8-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="466f8-104">Tento článek popisuje pole Zaokrouhlit odpis, které se nachází na stránce Nastavení knihy.</span><span class="sxs-lookup"><span data-stu-id="466f8-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="466f8-105">Celková částka odpisů je stanovena pro každou knihu.</span><span class="sxs-lookup"><span data-stu-id="466f8-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="466f8-106">Současné odpisové částky se používají v profilu odpisování dlouhodobého majetku, který ukazuje budoucí odpisy a hodnotu dlouhodobého majetku, a také v návrzích na odpisy.</span><span class="sxs-lookup"><span data-stu-id="466f8-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="466f8-107">Zadejte nejnižší částku odpisu povolenou pro tuto knihu.</span><span class="sxs-lookup"><span data-stu-id="466f8-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="466f8-108">Bez ohledu na nastavené zaokrouhlování, není částka odpisu v posledním období odpisu zaokrouhlena.</span><span class="sxs-lookup"><span data-stu-id="466f8-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="466f8-109">Na konci posledního období odpisu musí být hodnota dlouhodobého majetku 0 (nula) nebo hodnotu odpadu, pokud se používá konečná zůstatková hodnota.</span><span class="sxs-lookup"><span data-stu-id="466f8-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="466f8-110">Příklad</span><span class="sxs-lookup"><span data-stu-id="466f8-110">Example</span></span>

<span data-ttu-id="466f8-111">Odpis je bez zaokrouhlení vypočítán v částce 2 444,44.</span><span class="sxs-lookup"><span data-stu-id="466f8-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="466f8-112">Stejně jako v následující tabulce se částky, které budou nabízeny, liší v závislosti na tom, jak je nastavené zaokrouhlování.</span><span class="sxs-lookup"><span data-stu-id="466f8-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="466f8-113">Metoda zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="466f8-113">Rounding method</span></span> | <span data-ttu-id="466f8-114">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="466f8-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="466f8-115">Zaokrouhlení 0,1</span><span class="sxs-lookup"><span data-stu-id="466f8-115">Rounding 0.1</span></span>    | <span data-ttu-id="466f8-116">2 444,40</span><span class="sxs-lookup"><span data-stu-id="466f8-116">2,444.40</span></span>            |
| <span data-ttu-id="466f8-117">Zaokrouhlení 1,00</span><span class="sxs-lookup"><span data-stu-id="466f8-117">Rounding 1.00</span></span>   | <span data-ttu-id="466f8-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="466f8-118">2,444.00</span></span>            |
| <span data-ttu-id="466f8-119">Zaokrouhlení 10,00</span><span class="sxs-lookup"><span data-stu-id="466f8-119">Rounding 10.00</span></span>  | <span data-ttu-id="466f8-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="466f8-120">2,440.00</span></span>            |
| <span data-ttu-id="466f8-121">Zaokrouhlení 100,00</span><span class="sxs-lookup"><span data-stu-id="466f8-121">Rounding 100.00</span></span> | <span data-ttu-id="466f8-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="466f8-122">2,400.00</span></span>            |





