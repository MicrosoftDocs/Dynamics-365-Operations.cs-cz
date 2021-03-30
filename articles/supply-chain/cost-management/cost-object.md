---
title: Nákladové objekty
description: Tento článek poskytuje informace o nákladových objektech a vysvětluje, jakým způsobem se kumulují náklady a množství. Nákladový objekt je entita, pro kterou se kumulují náklady a množství. Entita nákladového objektu může být produkt a varianty produktu, například varianty pro styl a barvu.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee7c170d5a330c0080931a67c1548eb0d3522bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232391"
---
# <a name="cost-objects"></a><span data-ttu-id="7cd7d-105">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="7cd7d-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cd7d-106">Tento článek poskytuje informace o nákladových objektech a vysvětluje, jakým způsobem se kumulují náklady a množství.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="7cd7d-107">Nákladový objekt je entita, pro kterou se kumulují náklady a množství.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="7cd7d-108">Entita nákladového objektu může být produkt a varianty produktu, například varianty pro styl a barvu.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="7cd7d-109">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="7cd7d-109">Cost objects</span></span>

<span data-ttu-id="7cd7d-110">Stránka **Nákladové objekty** obsahuje všechny nákladové objekty, které jsou registrovány v produktu.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="7cd7d-111">Nákladové objekty jsou definovány dle údajů z následujících zdrojů:</span><span class="sxs-lookup"><span data-stu-id="7cd7d-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="7cd7d-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="7cd7d-112">Product</span></span>
-   <span data-ttu-id="7cd7d-113">Skupina dimenzí produktů</span><span class="sxs-lookup"><span data-stu-id="7cd7d-113">Product dimension group</span></span>
-   <span data-ttu-id="7cd7d-114">Skupina dimenze úložiště</span><span class="sxs-lookup"><span data-stu-id="7cd7d-114">Storage dimension group</span></span>
-   <span data-ttu-id="7cd7d-115">Skupina sledovací dimenze</span><span class="sxs-lookup"><span data-stu-id="7cd7d-115">Tracking dimension group</span></span>

<span data-ttu-id="7cd7d-116">**Poznámka:** Nákladový objekt představuje nákladový prvek pouze typu **Přímý materiál**.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="7cd7d-117">Nákladový objekt a objektu zásob se liší způsobem, že nákladový objekt je definován podle dimenzí zásob, které jsou vybrány pro finanční zásoby.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="7cd7d-118">Například zboží má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="7cd7d-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="7cd7d-119">**Web:** Fyzické zásoby = Ano, Finanční zásoby = Ano</span><span class="sxs-lookup"><span data-stu-id="7cd7d-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="7cd7d-120">**Sklad:** Fyzické zásoby = Ano, Finanční zásoby = Ne</span><span class="sxs-lookup"><span data-stu-id="7cd7d-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="7cd7d-121">**Č. dávky:** Fyzické zásoby = Ano, Finanční zásoby = Ne</span><span class="sxs-lookup"><span data-stu-id="7cd7d-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="7cd7d-122">Následující tabulka zobrazuje, co je nákladový objekt a co je objekt zásob.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="7cd7d-123">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="7cd7d-123">Object type</span></span>      | <span data-ttu-id="7cd7d-124">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="7cd7d-124">Item number</span></span> | <span data-ttu-id="7cd7d-125">Lokalita</span><span class="sxs-lookup"><span data-stu-id="7cd7d-125">Site</span></span> | <span data-ttu-id="7cd7d-126">Sklad</span><span class="sxs-lookup"><span data-stu-id="7cd7d-126">Warehouse</span></span> | <span data-ttu-id="7cd7d-127">Č. dávky</span><span class="sxs-lookup"><span data-stu-id="7cd7d-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="7cd7d-128">Nákladový objekt</span><span class="sxs-lookup"><span data-stu-id="7cd7d-128">Cost object</span></span>      | <span data-ttu-id="7cd7d-129"> linka</span><span class="sxs-lookup"><span data-stu-id="7cd7d-129">x</span></span>           | <span data-ttu-id="7cd7d-130"> linka</span><span class="sxs-lookup"><span data-stu-id="7cd7d-130">x</span></span>    |           |           |
| <span data-ttu-id="7cd7d-131">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="7cd7d-131">Inventory object</span></span> | <span data-ttu-id="7cd7d-132"> linka</span><span class="sxs-lookup"><span data-stu-id="7cd7d-132">x</span></span>           | <span data-ttu-id="7cd7d-133"> linka</span><span class="sxs-lookup"><span data-stu-id="7cd7d-133">x</span></span>    |  <span data-ttu-id="7cd7d-134"> linka</span><span class="sxs-lookup"><span data-stu-id="7cd7d-134">x</span></span>        | <span data-ttu-id="7cd7d-135"> linka</span><span class="sxs-lookup"><span data-stu-id="7cd7d-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="7cd7d-136">Kumulace nákladů a množství</span><span class="sxs-lookup"><span data-stu-id="7cd7d-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="7cd7d-137">Hodnota v poli **Hodnota** je součet následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="7cd7d-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="7cd7d-138">Fyzická částka nákladů</span><span class="sxs-lookup"><span data-stu-id="7cd7d-138">Physical cost amount</span></span>
    -   <span data-ttu-id="7cd7d-139">Částka finančních nákladů</span><span class="sxs-lookup"><span data-stu-id="7cd7d-139">Financial cost amount</span></span>
    -   <span data-ttu-id="7cd7d-140">Množství úprav</span><span class="sxs-lookup"><span data-stu-id="7cd7d-140">Adjustments</span></span>
-   <span data-ttu-id="7cd7d-141">Hodnota v poli **Množství** je součet následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="7cd7d-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="7cd7d-142">Přijato</span><span class="sxs-lookup"><span data-stu-id="7cd7d-142">Received</span></span>
    -   <span data-ttu-id="7cd7d-143">Odečteno</span><span class="sxs-lookup"><span data-stu-id="7cd7d-143">Deducted</span></span>
    -   <span data-ttu-id="7cd7d-144">Zaúčtované mn.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-144">Posted quantity</span></span>
-   <span data-ttu-id="7cd7d-145">Pole **Průměrné náklady na jednotku** je vypočítané.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="7cd7d-146">Hodnota se vypočítá jako podíl hodnoty pole **Hodnota** a hodnoty pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="7cd7d-147">**Poznámka:** Parametr **Zahrnovat fyzickou hodnotu** nemá žádný vliv na předchozí výpočty.</span><span class="sxs-lookup"><span data-stu-id="7cd7d-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="7cd7d-148">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7cd7d-148">Additional resources</span></span>
--------

[<span data-ttu-id="7cd7d-149">Skupina dimenzí produktů</span><span class="sxs-lookup"><span data-stu-id="7cd7d-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="7cd7d-150">Skupina dimenze úložiště</span><span class="sxs-lookup"><span data-stu-id="7cd7d-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="7cd7d-151">Skupina sledovací dimenze</span><span class="sxs-lookup"><span data-stu-id="7cd7d-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="7cd7d-152">Co je nového a co se změnilo</span><span class="sxs-lookup"><span data-stu-id="7cd7d-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="7cd7d-153">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="7cd7d-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]