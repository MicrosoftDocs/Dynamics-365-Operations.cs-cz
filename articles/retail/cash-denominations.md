---
title: Konfigurace nominálních hodnot hotovosti pro pokladní místo (POS)
description: Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a34ae8084c0ad55221f4ab93eb8c6481fa8c4771
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606749"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="a100b-103">Konfigurace nominálních hodnot hotovosti pro pokladní místo (POS)</span><span class="sxs-lookup"><span data-stu-id="a100b-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a100b-104">Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS.</span><span class="sxs-lookup"><span data-stu-id="a100b-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="a100b-105">Tyto nominální hodnoty lze použít pro pomoc při inventuře hotovosti pro výkazy úhrad na konci dne nebo pro rychlé úhrady prodeje.</span><span class="sxs-lookup"><span data-stu-id="a100b-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="a100b-106">Definování nominálních hodnot</span><span class="sxs-lookup"><span data-stu-id="a100b-106">Define denominations</span></span>

<span data-ttu-id="a100b-107">Nominální hodnoty se nastavují na úrovni obchodu v možnosti **Nastavit** \> **Výkaz hotovosti** ze stránky vlastnosti obchodu.</span><span class="sxs-lookup"><span data-stu-id="a100b-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![Možnost výkazu hotovosti](./media/image1-denomination.png)

<span data-ttu-id="a100b-109">Jak definovat nominální hodnotu:</span><span class="sxs-lookup"><span data-stu-id="a100b-109">To define a denomination:</span></span>

1. <span data-ttu-id="a100b-110">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a100b-110">Click **New**.</span></span>
1. <span data-ttu-id="a100b-111">Zadejte typ (mince nebo bankovka).</span><span class="sxs-lookup"><span data-stu-id="a100b-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="a100b-112">Zadejte částku (hodnota).</span><span class="sxs-lookup"><span data-stu-id="a100b-112">Specify the amount (value).</span></span>

![Stránka nominální hodnoty výkazu hotovosti](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="a100b-114">Konfigurace funkčního profilu</span><span class="sxs-lookup"><span data-stu-id="a100b-114">Configure the functionality profile</span></span>

<span data-ttu-id="a100b-115">Při platbě hotovosti v POS může uživatel použít nominální hodnoty k rychlému zadání částky placené odběratelem.</span><span class="sxs-lookup"><span data-stu-id="a100b-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="a100b-116">Ve funkčním profilu můžete nakonfigurovat dvě možnosti pro zobrazení nominálních hodnot v POS.</span><span class="sxs-lookup"><span data-stu-id="a100b-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="a100b-117">**Větší nebo rovno splatné částce** - Ve výchozím nastavení POS zobrazí pouze nominálních hodnoty, které jsou větší než splatná částka, což umožňuje úhradu jedním dotykem.</span><span class="sxs-lookup"><span data-stu-id="a100b-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="a100b-118">Pokud je například dlužná částka 7,5 USD, POS zobrazí následující nominální hodnoty: 10 USD, 20 USD, 50 USD a 100 USD.</span><span class="sxs-lookup"><span data-stu-id="a100b-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="a100b-119">Dotyk jedné z těchto částek automaticky uhradí prodej za tuto částku.</span><span class="sxs-lookup"><span data-stu-id="a100b-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="a100b-120">Bankovky 1 USD a 5 USD se nezobrazují, protože tyto částky jsou menší než částka k zaplacení.</span><span class="sxs-lookup"><span data-stu-id="a100b-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="a100b-121">**Všechny nominální hodnoty** - Zvolte tuto možnost, aby se vždy zobrazily všechny nominální hodnoty v POS, bez ohledu částku k úhradě.</span><span class="sxs-lookup"><span data-stu-id="a100b-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="a100b-122">To znamená, že uživatel může použít kombinaci bankovek k dosažení splatné částky.</span><span class="sxs-lookup"><span data-stu-id="a100b-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="a100b-123">Například pokud je dlužná částka 25,00 USD, uživatel si může zvolit 20 USD a 5 USD k dokončení prodeje.</span><span class="sxs-lookup"><span data-stu-id="a100b-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>
