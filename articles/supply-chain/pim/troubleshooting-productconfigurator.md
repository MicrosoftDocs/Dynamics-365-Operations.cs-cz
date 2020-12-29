---
title: Řešení potíží s konfigurátorem produktu
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s konfigurátorem produktu.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dacc7205eaf2084f6fbd3be9d8ac0572f9e1bcde
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516743"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="2ebea-103">Řešení potíží s konfigurátorem produktu</span><span class="sxs-lookup"><span data-stu-id="2ebea-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="2ebea-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s konfigurátorem produktu.</span><span class="sxs-lookup"><span data-stu-id="2ebea-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="2ebea-105">Text položky je přepsán, když konfiguruji produkt na řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2ebea-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ebea-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="2ebea-106">Issue description</span></span>

<span data-ttu-id="2ebea-107">K tomuto problému dochází, když vytvoříte řádek prodejní objednávky pro konfigurovatelnou položku a poté upravíte text položky.</span><span class="sxs-lookup"><span data-stu-id="2ebea-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="2ebea-108">Když položku konfigurujete a poté vyberete **OK**, text je přepsán standardním textem.</span><span class="sxs-lookup"><span data-stu-id="2ebea-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2ebea-109">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="2ebea-109">Issue resolution</span></span>

<span data-ttu-id="2ebea-110">Toto chování se očekává.</span><span class="sxs-lookup"><span data-stu-id="2ebea-110">This behavior is expected.</span></span> <span data-ttu-id="2ebea-111">Textové pole obsahuje název varianty, který se vyplní až po konfiguraci řádku.</span><span class="sxs-lookup"><span data-stu-id="2ebea-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="2ebea-112">Proto musíte změnit text po nakonfigurování řádku, ne dříve.</span><span class="sxs-lookup"><span data-stu-id="2ebea-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="2ebea-113">Atributy celého čísla jsou při výpočtu konfiguračních modelů produktu nesprávně zaokrouhleny.</span><span class="sxs-lookup"><span data-stu-id="2ebea-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ebea-114">Popis problému</span><span class="sxs-lookup"><span data-stu-id="2ebea-114">Issue description</span></span>

<span data-ttu-id="2ebea-115">K tomuto problému může dojít, když provedete následující řadu akcí:</span><span class="sxs-lookup"><span data-stu-id="2ebea-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="2ebea-116">Na produkčním konfiguračním modelu nastavte následující atributy:</span><span class="sxs-lookup"><span data-stu-id="2ebea-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="2ebea-117">Vstup (celé číslo)</span><span class="sxs-lookup"><span data-stu-id="2ebea-117">Input (integer)</span></span>
    - <span data-ttu-id="2ebea-118">Procento (desetinné)</span><span class="sxs-lookup"><span data-stu-id="2ebea-118">Percent (decimal)</span></span>
    - <span data-ttu-id="2ebea-119">Výsledek (celé číslo)</span><span class="sxs-lookup"><span data-stu-id="2ebea-119">Result (integer)</span></span>

2. <span data-ttu-id="2ebea-120">Vytvořte výpočet, který má následující výraz:</span><span class="sxs-lookup"><span data-stu-id="2ebea-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="2ebea-121">*Výsledek* = *Vstup* × *Procento* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="2ebea-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="2ebea-122">V takovém případě není výsledek celého čísla vždy správně zaokrouhlený.</span><span class="sxs-lookup"><span data-stu-id="2ebea-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="2ebea-123">Například vstup je 1 000 a procento je 2,40.</span><span class="sxs-lookup"><span data-stu-id="2ebea-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="2ebea-124">Proto očekáváte, že celočíselný výsledek bude 24, protože 2,40 procent z 1 000 je 24 (nebo 24,00 v desetinné formě).</span><span class="sxs-lookup"><span data-stu-id="2ebea-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="2ebea-125">Místo toho je výsledek zobrazen jako 23.</span><span class="sxs-lookup"><span data-stu-id="2ebea-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="2ebea-126">Když je však procento 2,39, výpočet se zaokrouhlí na 24 místo 23.</span><span class="sxs-lookup"><span data-stu-id="2ebea-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="2ebea-127">Když je procento 2,5 výpočet se zaokrouhlí na 25 podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="2ebea-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2ebea-128">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="2ebea-128">Issue resolution</span></span>

<span data-ttu-id="2ebea-129">K tomuto problému dochází kvůli způsobu, jakým Microsoft Solver Foundation interně představuje čísla pomocí zlomků.</span><span class="sxs-lookup"><span data-stu-id="2ebea-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="2ebea-130">V předchozím příkladu je výsledek výpočtu, kde je procento 2,40, reprezentován jako 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="2ebea-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="2ebea-131">Když .NET převede tuto hodnotu na celé číslo, vrátí 23.</span><span class="sxs-lookup"><span data-stu-id="2ebea-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="2ebea-132">Toto chování se nezmění, protože na něm závisí jiné scénáře.</span><span class="sxs-lookup"><span data-stu-id="2ebea-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="2ebea-133">V předchozím příkladu můžete problém vyřešit zavedením dalšího desetinného atributu a výpočtu.</span><span class="sxs-lookup"><span data-stu-id="2ebea-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="2ebea-134">Například můžete nastavit na produkčním konfiguračním modelu následující atributy:</span><span class="sxs-lookup"><span data-stu-id="2ebea-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="2ebea-135">Vstup (celé číslo)</span><span class="sxs-lookup"><span data-stu-id="2ebea-135">Input (integer)</span></span>
- <span data-ttu-id="2ebea-136">Procento (desetinné)</span><span class="sxs-lookup"><span data-stu-id="2ebea-136">Percent (decimal)</span></span>
- <span data-ttu-id="2ebea-137">ResultDecimal (desetinné)</span><span class="sxs-lookup"><span data-stu-id="2ebea-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="2ebea-138">ResultInteger (celé číslo)</span><span class="sxs-lookup"><span data-stu-id="2ebea-138">ResultInteger (integer)</span></span>

<span data-ttu-id="2ebea-139">Poté můžete přidat následující výpočty:</span><span class="sxs-lookup"><span data-stu-id="2ebea-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="2ebea-140">*ResultDecimal* = *Vstup* × *Procento* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="2ebea-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="2ebea-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="2ebea-141">*ResultInteger* = *ResultDecimal*</span></span>
