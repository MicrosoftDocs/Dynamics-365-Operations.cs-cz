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
ms.openlocfilehash: 65a0f72f8d97bda36bacd691d545807c413f8825
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967651"
---
# <a name="cost-objects"></a><span data-ttu-id="3d096-105">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="3d096-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d096-106">Tento článek poskytuje informace o nákladových objektech a vysvětluje, jakým způsobem se kumulují náklady a množství.</span><span class="sxs-lookup"><span data-stu-id="3d096-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="3d096-107">Nákladový objekt je entita, pro kterou se kumulují náklady a množství.</span><span class="sxs-lookup"><span data-stu-id="3d096-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="3d096-108">Entita nákladového objektu může být produkt a varianty produktu, například varianty pro styl a barvu.</span><span class="sxs-lookup"><span data-stu-id="3d096-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="3d096-109">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="3d096-109">Cost objects</span></span>

<span data-ttu-id="3d096-110">Stránka **Nákladové objekty** obsahuje všechny nákladové objekty, které jsou registrovány v produktu.</span><span class="sxs-lookup"><span data-stu-id="3d096-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="3d096-111">Nákladové objekty jsou definovány dle údajů z následujících zdrojů:</span><span class="sxs-lookup"><span data-stu-id="3d096-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="3d096-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="3d096-112">Product</span></span>
-   <span data-ttu-id="3d096-113">Skupina dimenzí produktů</span><span class="sxs-lookup"><span data-stu-id="3d096-113">Product dimension group</span></span>
-   <span data-ttu-id="3d096-114">Skupina dimenze úložiště</span><span class="sxs-lookup"><span data-stu-id="3d096-114">Storage dimension group</span></span>
-   <span data-ttu-id="3d096-115">Skupina sledovací dimenze</span><span class="sxs-lookup"><span data-stu-id="3d096-115">Tracking dimension group</span></span>

<span data-ttu-id="3d096-116">**Poznámka:** Nákladový objekt představuje nákladový prvek pouze typu **Přímý materiál**.</span><span class="sxs-lookup"><span data-stu-id="3d096-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="3d096-117">Nákladový objekt a objektu zásob se liší způsobem, že nákladový objekt je definován podle dimenzí zásob, které jsou vybrány pro finanční zásoby.</span><span class="sxs-lookup"><span data-stu-id="3d096-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="3d096-118">Například zboží má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="3d096-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="3d096-119">**Web:** Fyzické zásoby = Ano, Finanční zásoby = Ano</span><span class="sxs-lookup"><span data-stu-id="3d096-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="3d096-120">**Sklad:** Fyzické zásoby = Ano, Finanční zásoby = Ne</span><span class="sxs-lookup"><span data-stu-id="3d096-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="3d096-121">**Č. dávky:** Fyzické zásoby = Ano, Finanční zásoby = Ne</span><span class="sxs-lookup"><span data-stu-id="3d096-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="3d096-122">Následující tabulka zobrazuje, co je nákladový objekt a co je objekt zásob.</span><span class="sxs-lookup"><span data-stu-id="3d096-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="3d096-123">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="3d096-123">Object type</span></span>      | <span data-ttu-id="3d096-124">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="3d096-124">Item number</span></span> | <span data-ttu-id="3d096-125">Lokalita</span><span class="sxs-lookup"><span data-stu-id="3d096-125">Site</span></span> | <span data-ttu-id="3d096-126">Sklad</span><span class="sxs-lookup"><span data-stu-id="3d096-126">Warehouse</span></span> | <span data-ttu-id="3d096-127">Č. dávky</span><span class="sxs-lookup"><span data-stu-id="3d096-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="3d096-128">Nákladový objekt</span><span class="sxs-lookup"><span data-stu-id="3d096-128">Cost object</span></span>      | <span data-ttu-id="3d096-129"> linka</span><span class="sxs-lookup"><span data-stu-id="3d096-129">x</span></span>           | <span data-ttu-id="3d096-130"> linka</span><span class="sxs-lookup"><span data-stu-id="3d096-130">x</span></span>    |           |           |
| <span data-ttu-id="3d096-131">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="3d096-131">Inventory object</span></span> | <span data-ttu-id="3d096-132"> linka</span><span class="sxs-lookup"><span data-stu-id="3d096-132">x</span></span>           | <span data-ttu-id="3d096-133"> linka</span><span class="sxs-lookup"><span data-stu-id="3d096-133">x</span></span>    |  <span data-ttu-id="3d096-134"> linka</span><span class="sxs-lookup"><span data-stu-id="3d096-134">x</span></span>        | <span data-ttu-id="3d096-135"> linka</span><span class="sxs-lookup"><span data-stu-id="3d096-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="3d096-136">Kumulace nákladů a množství</span><span class="sxs-lookup"><span data-stu-id="3d096-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="3d096-137">Hodnota v poli **Hodnota** je součet následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="3d096-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="3d096-138">Fyzická částka nákladů</span><span class="sxs-lookup"><span data-stu-id="3d096-138">Physical cost amount</span></span>
    -   <span data-ttu-id="3d096-139">Částka finančních nákladů</span><span class="sxs-lookup"><span data-stu-id="3d096-139">Financial cost amount</span></span>
    -   <span data-ttu-id="3d096-140">Množství úprav</span><span class="sxs-lookup"><span data-stu-id="3d096-140">Adjustments</span></span>
-   <span data-ttu-id="3d096-141">Hodnota v poli **Množství** je součet následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="3d096-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="3d096-142">Přijato</span><span class="sxs-lookup"><span data-stu-id="3d096-142">Received</span></span>
    -   <span data-ttu-id="3d096-143">Odečteno</span><span class="sxs-lookup"><span data-stu-id="3d096-143">Deducted</span></span>
    -   <span data-ttu-id="3d096-144">Zaúčtované mn.</span><span class="sxs-lookup"><span data-stu-id="3d096-144">Posted quantity</span></span>
-   <span data-ttu-id="3d096-145">Pole **Průměrné náklady na jednotku** je vypočítané.</span><span class="sxs-lookup"><span data-stu-id="3d096-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="3d096-146">Hodnota se vypočítá jako podíl hodnoty pole **Hodnota** a hodnoty pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="3d096-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="3d096-147">**Poznámka:** Parametr **Zahrnovat fyzickou hodnotu** nemá žádný vliv na předchozí výpočty.</span><span class="sxs-lookup"><span data-stu-id="3d096-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="3d096-148">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3d096-148">Additional resources</span></span>
--------

[<span data-ttu-id="3d096-149">Skupina dimenzí produktů</span><span class="sxs-lookup"><span data-stu-id="3d096-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="3d096-150">Skupina dimenze úložiště</span><span class="sxs-lookup"><span data-stu-id="3d096-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="3d096-151">Skupina sledovací dimenze</span><span class="sxs-lookup"><span data-stu-id="3d096-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="3d096-152">Co je nového a co se změnilo</span><span class="sxs-lookup"><span data-stu-id="3d096-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="3d096-153">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="3d096-153">Cost entries</span></span>](cost-entries.md)



