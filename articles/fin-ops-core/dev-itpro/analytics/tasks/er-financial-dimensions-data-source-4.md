---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9a6f07d6c665097fabab4d3ec6d7fa5ba80b65d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406467"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="cd2a3-103">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)</span><span class="sxs-lookup"><span data-stu-id="cd2a3-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd2a3-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="cd2a3-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="cd2a3-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 3: návrh sestavy").</span><span class="sxs-lookup"><span data-stu-id="cd2a3-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="cd2a3-107">Na stránce Parametry elektronického výkaznictví musíte také nakonfigurovat výchozí typy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="cd2a3-108">Výchozí typy dokumentů jsou nastaveny také při stahování a importu konfigurace všech elektronických výkazů.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="cd2a3-109">Spuštění sestavy</span><span class="sxs-lookup"><span data-stu-id="cd2a3-109">Run report</span></span>
1. <span data-ttu-id="cd2a3-110">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="cd2a3-111">Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="cd2a3-112">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí\Sestava deníku hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="cd2a3-113">Klikněte na Spustit.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-113">Click Run.</span></span>
<span data-ttu-id="cd2a3-114">![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="cd2a3-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="cd2a3-115">V poli Název dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="cd2a3-116">Chcete-li vybrat všechny dimenze v aktuální společnosti, zadejte následující informace: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="cd2a3-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="cd2a3-118">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="cd2a3-119">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-119">Click Filter.</span></span>
8. <span data-ttu-id="cd2a3-120">Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="cd2a3-121">Zadejte hodnotu 00057 do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="cd2a3-122">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-122">Click OK.</span></span>
11. <span data-ttu-id="cd2a3-123">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-123">Click OK.</span></span>
<span data-ttu-id="cd2a3-124">![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="cd2a3-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="cd2a3-125">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-125">Review the generated output.</span></span> <span data-ttu-id="cd2a3-126">Pro každou transakci vybrané dávky jsou uvedeny finanční dimenze z odpovídající sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="cd2a3-127">Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Stránka konfigurací elektronického výkaznictví](../media/er-financial-dimensions-guides-run4.png)
