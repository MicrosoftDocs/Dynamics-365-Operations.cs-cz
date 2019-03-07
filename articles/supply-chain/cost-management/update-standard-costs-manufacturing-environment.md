---
title: Aktualizace standardních nákladů ve výrobním prostředí
description: V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady ve výrobním prostředí.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fccfcec3d74bd13aa1b6511ebd37ee1454d1b47b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "332350"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="af440-103">Aktualizace standardních nákladů ve výrobním prostředí</span><span class="sxs-lookup"><span data-stu-id="af440-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af440-104">V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady ve výrobním prostředí.</span><span class="sxs-lookup"><span data-stu-id="af440-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="af440-105">Aktualizace mohou odrážet nové položky, kategorie nákladů nebo vzorce nepřímého výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="af440-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="af440-106">Můžete také odrážet opravy a změny nákladů.</span><span class="sxs-lookup"><span data-stu-id="af440-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="af440-107">Typ aktualizace má vliv na kroky, které je nutno provést k aktualizaci standardních nákladů, jak je uvedeno v následujících příkladech:</span><span class="sxs-lookup"><span data-stu-id="af440-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="af440-108">Určete očekávané standardní změny nákladů pro zakoupené položky a poté pro příslušné datum změňte stav záznamů o nákladech na položku na hodnotu **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="af440-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="af440-109">Neprovádějte však přepočítání nákladů na vyrobené položky, které používají zakoupené položky.</span><span class="sxs-lookup"><span data-stu-id="af440-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="af440-110">Určete standardní náklady na nově zakoupenou položku, avšak neprovádějte přepočítání nákladů vyrobených položek s verzemi kusovníku, které jako komponentu obsahuje nově zakoupenou položku.</span><span class="sxs-lookup"><span data-stu-id="af440-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="af440-111">Opravte nebo změňte náklady na zakoupenou položku nebo změňte nákladovou skupinu přiřazenou k zakoupené položce a vypočtěte náklady pro všechny vyrobené položky s verzí kusovníku, která jako součást obsahuje zakoupenou položku.</span><span class="sxs-lookup"><span data-stu-id="af440-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="af440-112">Změňte náklady pro kategorii nákladů a vypočtěte náklady pro všechny vypočtené položky s verzí postupu, která obsahuje operace postupu používající danou kategorii nákladů.</span><span class="sxs-lookup"><span data-stu-id="af440-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="af440-113">Změňte kategorie nákladů, které jsou přiřazeny k operacím postupů, nebo nákladovou skupinu, která je přiřazena k nákladovým kategoriím.</span><span class="sxs-lookup"><span data-stu-id="af440-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="af440-114">Potom vypočtěte náklady pro všechny vyrobené položky s verzí postupu, která obsahuje operace postupu používající danou kategorii nákladů.</span><span class="sxs-lookup"><span data-stu-id="af440-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="af440-115">Změňte vzorec nepřímého výpočtu nákladů a vypočtěte náklady pro všechny vyráběné položky, na které bude mít uvedená změna vliv.</span><span class="sxs-lookup"><span data-stu-id="af440-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="af440-116">Pro vyráběnou položku změňte nebo přidejte výrobní pracoviště a vypočtěte výrobní náklady položky pro dané pracoviště.</span><span class="sxs-lookup"><span data-stu-id="af440-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="af440-117">Vypočítejte nebo přepočítejte náklady na vyráběnou položku a přepočítejte náklady pro všechny vyráběné položky s verzí kusovníku, která obsahuje vyráběnou položku jako součást.</span><span class="sxs-lookup"><span data-stu-id="af440-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="af440-118">Vypočtěte náklady pro nově vyráběnou položku na základě údajů definovaného, schváleného a aktivního kusovníku a postupu.</span><span class="sxs-lookup"><span data-stu-id="af440-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="af440-119">Každý případ vyžaduje pečlivé zvážení způsobu aktualizace standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="af440-119">Each case requires careful consideration about how to update standard costs.</span></span>



