---
title: Kontrola kvality zboží
description: Toto téma popisuje, jak zpracovat objednávky kvality.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956127"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="049c8-103">Kontrola kvality zboží</span><span class="sxs-lookup"><span data-stu-id="049c8-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="049c8-104">Toto téma popisuje, jak zpracovat objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="049c8-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="049c8-105">Kontroly kvality obvykle provádějí pracovníci pro kontrolu kvality.</span><span class="sxs-lookup"><span data-stu-id="049c8-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="049c8-106">Pokud jsou nainstalována standardní ukázková data, můžete je použít k provedení postupů v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="049c8-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="049c8-107">K použití ukázkových dat vyberte právnickou osobu *USMF*.</span><span class="sxs-lookup"><span data-stu-id="049c8-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="049c8-108">Poté musíte potvrdit nákupní objednávku *000016* a zaúčtovat příjemku produktu.</span><span class="sxs-lookup"><span data-stu-id="049c8-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="049c8-109">Objednávka kvality je generována automaticky.</span><span class="sxs-lookup"><span data-stu-id="049c8-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="049c8-110">Krok 1: Vyberte objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="049c8-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="049c8-111">Pokud chcete vybrat objednávku kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="049c8-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="049c8-112">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.</span><span class="sxs-lookup"><span data-stu-id="049c8-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="049c8-113">Vyberte objednávku kvality, která byla vygenerována před zahájením tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="049c8-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="049c8-114">Krok 2: Záznam výsledků testu</span><span class="sxs-lookup"><span data-stu-id="049c8-114">Step 2: Record test results</span></span>

<span data-ttu-id="049c8-115">Chcete-li zaznamenat výsledky testu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="049c8-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="049c8-116">Vyberte **Výsledky**</span><span class="sxs-lookup"><span data-stu-id="049c8-116">Select **Results**.</span></span>
1. <span data-ttu-id="049c8-117">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="049c8-117">Select **Edit**.</span></span>
1. <span data-ttu-id="049c8-118">V poli **Výsledné množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="049c8-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="049c8-119">V poli **Výsledek** zvolte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="049c8-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="049c8-120">V tomto příkladu vychází výsledek z předem definovaného výsledku.</span><span class="sxs-lookup"><span data-stu-id="049c8-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="049c8-121">Obvykle vytvoříte záznam s mnohem přesnějšími výsledky, jako například s velikostí nebo jinou dimenzí.</span><span class="sxs-lookup"><span data-stu-id="049c8-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="049c8-122">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="049c8-122">Select **Save**.</span></span>
1. <span data-ttu-id="049c8-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="049c8-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="049c8-124">Krok 3: Ověřit objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="049c8-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="049c8-125">Pokud chcete objednávku kvality ověřit, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="049c8-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="049c8-126">Vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="049c8-126">Select **Validate**.</span></span>
1. <span data-ttu-id="049c8-127">V poli **Potvrdil(a)** vyberte uživatele, který provádí kontrolu.</span><span class="sxs-lookup"><span data-stu-id="049c8-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="049c8-128">Zvolte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="049c8-128">Select **Select**.</span></span>
1. <span data-ttu-id="049c8-129">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="049c8-129">Select **OK**.</span></span>
1. <span data-ttu-id="049c8-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="049c8-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
