---
title: "Konfigurace nominálních hodnot hotovosti pro POS"
description: "Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e70765c43b93e9d8abab5fbb9de1d67a739a74
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="d3505-103">Konfigurace nominálních hodnot hotovosti pro POS</span><span class="sxs-lookup"><span data-stu-id="d3505-103">Configure cash denominations for POS</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="d3505-104">Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS.</span><span class="sxs-lookup"><span data-stu-id="d3505-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="d3505-105">Tyto nominální hodnoty lze použít pro pomoc při inventuře hotovosti pro výkazy úhrad na konci dne nebo pro rychlé úhrady prodeje.</span><span class="sxs-lookup"><span data-stu-id="d3505-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="d3505-106">Definování nominálních hodnot</span><span class="sxs-lookup"><span data-stu-id="d3505-106">Define denominations</span></span>
<span data-ttu-id="d3505-107">Nominální hodnoty se nastavují na úrovni obchodu na stránce **Nastavit** > **Možnost výkazu hotovosti z vlastnosti obchodu**.</span><span class="sxs-lookup"><span data-stu-id="d3505-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![nominální hodnoty hotovosti](./media/image1-denomination.png)

<span data-ttu-id="d3505-109">Jak definovat nominální hodnotu:</span><span class="sxs-lookup"><span data-stu-id="d3505-109">To define a denomination:</span></span>
1. <span data-ttu-id="d3505-110">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d3505-110">Click **New**.</span></span>
1. <span data-ttu-id="d3505-111">Zadejte typ (mince nebo bankovka).</span><span class="sxs-lookup"><span data-stu-id="d3505-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="d3505-112">Zadejte částku (hodnota).</span><span class="sxs-lookup"><span data-stu-id="d3505-112">Specify the amount (value).</span></span>

![nominální hodnoty hotovosti](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="d3505-114">Konfigurace funkčního profilu</span><span class="sxs-lookup"><span data-stu-id="d3505-114">Configure the functionality profile</span></span>
<span data-ttu-id="d3505-115">Při platbě hotovosti v POS může uživatel použít nominální hodnoty k rychlému zadání částky placené odběratelem.</span><span class="sxs-lookup"><span data-stu-id="d3505-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="d3505-116">Ve funkčním profilu můžete nakonfigurovat dvě možnosti pro zobrazení nominálních hodnot v POS.</span><span class="sxs-lookup"><span data-stu-id="d3505-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="d3505-117">**Větší nebo rovno splatné částce**: Ve výchozím nastavení POS zobrazí pouze nominálních hodnoty, které jsou větší než splatná částka, což umožňuje úhradu jedním dotykem.</span><span class="sxs-lookup"><span data-stu-id="d3505-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="d3505-118">Pokud je například dlužná částka 7,5 USD, POS zobrazí následující nominální hodnoty: 10 USD, 20 USD, 50 USD a 100 USD.</span><span class="sxs-lookup"><span data-stu-id="d3505-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="d3505-119">Dotyk jedné z těchto částek automaticky uhradí prodej za tuto částku.</span><span class="sxs-lookup"><span data-stu-id="d3505-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="d3505-120">Bankovky 1 USD a 5 USD se nezobrazují, protože tyto částky jsou menší než částka k zaplacení.</span><span class="sxs-lookup"><span data-stu-id="d3505-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="d3505-121">**Všechny nominální hodnoty**: Zvolte tuto možnost, aby se vždy zobrazily všechny nominální hodnoty v POS, bez ohledu částku k úhradě.</span><span class="sxs-lookup"><span data-stu-id="d3505-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="d3505-122">To znamená, že uživatel může použít kombinaci bankovek k dosažení splatné částky.</span><span class="sxs-lookup"><span data-stu-id="d3505-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="d3505-123">Například pokud je dlužná částka 25,00 USD, uživatel si může zvolit 20 USD a 5 USD k dokončení prodeje.</span><span class="sxs-lookup"><span data-stu-id="d3505-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>

