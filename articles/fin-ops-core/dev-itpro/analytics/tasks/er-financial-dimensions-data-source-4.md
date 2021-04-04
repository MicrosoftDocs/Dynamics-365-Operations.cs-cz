---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)
description: Toto téma popisuje, jak nakonfigurovat model elektronického výkaznictví (ER) tak, aby používal finanční dimenze jako zdroj dat pro zprávy ER. (část 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7cc1a60234ef09b80950cbf0c7f18b0d65709d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565207"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="674f3-104">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)</span><span class="sxs-lookup"><span data-stu-id="674f3-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="674f3-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="674f3-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="674f3-106">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="674f3-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="674f3-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 3: návrh sestavy").</span><span class="sxs-lookup"><span data-stu-id="674f3-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="674f3-108">Na stránce Parametry elektronického výkaznictví musíte také nakonfigurovat výchozí typy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="674f3-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="674f3-109">Výchozí typy dokumentů jsou nastaveny také při stahování a importu konfigurace všech elektronických výkazů.</span><span class="sxs-lookup"><span data-stu-id="674f3-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="674f3-110">Spuštění sestavy</span><span class="sxs-lookup"><span data-stu-id="674f3-110">Run report</span></span>
1. <span data-ttu-id="674f3-111">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="674f3-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="674f3-112">Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="674f3-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="674f3-113">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí\Sestava deníku hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="674f3-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="674f3-114">Klikněte na Spustit.</span><span class="sxs-lookup"><span data-stu-id="674f3-114">Click Run.</span></span>
<span data-ttu-id="674f3-115">![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="674f3-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="674f3-116">V poli Název dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="674f3-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="674f3-117">Chcete-li vybrat všechny dimenze v aktuální společnosti, zadejte následující informace: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="674f3-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="674f3-119">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="674f3-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="674f3-120">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="674f3-120">Click Filter.</span></span>
8. <span data-ttu-id="674f3-121">Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="674f3-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="674f3-122">Zadejte hodnotu 00057 do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="674f3-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="674f3-123">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="674f3-123">Click OK.</span></span>
11. <span data-ttu-id="674f3-124">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="674f3-124">Click OK.</span></span>
<span data-ttu-id="674f3-125">![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="674f3-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="674f3-126">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="674f3-126">Review the generated output.</span></span> <span data-ttu-id="674f3-127">Pro každou transakci vybrané dávky jsou uvedeny finanční dimenze z odpovídající sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="674f3-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="674f3-128">Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci.</span><span class="sxs-lookup"><span data-stu-id="674f3-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]