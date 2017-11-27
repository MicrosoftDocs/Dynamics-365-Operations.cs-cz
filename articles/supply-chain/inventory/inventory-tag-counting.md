---
title: "Inventura zásob podle štítků"
description: "Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0687058bc76c3ed0dad57b76d54ad57c00987f42
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-tag-counting"></a><span data-ttu-id="52062-103">Inventura zásob podle štítků</span><span class="sxs-lookup"><span data-stu-id="52062-103">Inventory tag counting</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="52062-104">Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě.</span><span class="sxs-lookup"><span data-stu-id="52062-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="52062-105">Vytvořením řádků na stránce **Inventura podle štítků** přidáte číslo štítku ke každé skladové položce, například číslo od 1 do 500.</span><span class="sxs-lookup"><span data-stu-id="52062-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="52062-106">Během inventury zadejte číslo položky a množství na příslušném štítku.</span><span class="sxs-lookup"><span data-stu-id="52062-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="52062-107">Tento štítek pak slouží jako základ pro vstup do deníku inventur podle štítků.</span><span class="sxs-lookup"><span data-stu-id="52062-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="52062-108">Po zaúčtování deníku inventur štítků se na stránce **Inventura** vytvoří nový deník inventur.</span><span class="sxs-lookup"><span data-stu-id="52062-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="52062-109">Nový deník vychází z řádků v deníku inventur podle štítků, které jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="52062-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="52062-110">Pro inventuru položek podle určité skladové dimenze vyberte dimenzi na stránce **Zobrazení dimenzí**, která se zobrazí při vytvoření deníku inventur podle štítků.</span><span class="sxs-lookup"><span data-stu-id="52062-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="52062-111">Například k provedení inventury položek v konkrétním skladu zaškrtněte políčko **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="52062-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="52062-112">Pokud je vybraný posuvník **Uzamknout položky během inventury** na stránce **Parametry modulu Řízení zásob a skladu**, položky nelze během inventury fyzicky aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="52062-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="52062-113">Položky v denících inventur však během inventury nejsou uzamknuty.</span><span class="sxs-lookup"><span data-stu-id="52062-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="52062-114">Skladové transakce se nevytvoří, dokud se řádky inventur štítků nezaúčtují a nepřenesou do deníku inventur.</span><span class="sxs-lookup"><span data-stu-id="52062-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="52062-115">Pokud jsou štítky vloženy náhodně a vy chcete určit chybějící štítky, klikněte na záhlaví sloupce **Štítek** a seřaďte řádky podle štítků.</span><span class="sxs-lookup"><span data-stu-id="52062-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="see-also"></a><span data-ttu-id="52062-116">Viz také</span><span class="sxs-lookup"><span data-stu-id="52062-116">See also</span></span>
--------

[<span data-ttu-id="52062-117">Cyklická inventura</span><span class="sxs-lookup"><span data-stu-id="52062-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)

