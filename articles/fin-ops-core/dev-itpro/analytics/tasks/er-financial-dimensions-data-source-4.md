---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 7ae9f72df5d6ff6add4eb97836cf32509aebd511
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141954"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="71a48-103">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)</span><span class="sxs-lookup"><span data-stu-id="71a48-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71a48-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="71a48-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="71a48-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="71a48-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="71a48-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 3: návrh sestavy").</span><span class="sxs-lookup"><span data-stu-id="71a48-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="71a48-107">Na stránce Parametry elektronického výkaznictví musíte také nakonfigurovat výchozí typy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="71a48-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="71a48-108">Výchozí typy dokumentů jsou nastaveny také při stahování a importu konfigurace všech elektronických výkazů.</span><span class="sxs-lookup"><span data-stu-id="71a48-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="71a48-109">Spuštění sestavy</span><span class="sxs-lookup"><span data-stu-id="71a48-109">Run report</span></span>
1. <span data-ttu-id="71a48-110">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="71a48-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="71a48-111">Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="71a48-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="71a48-112">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí\Sestava deníku hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="71a48-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="71a48-113">Klikněte na Spustit.</span><span class="sxs-lookup"><span data-stu-id="71a48-113">Click Run.</span></span>
5. <span data-ttu-id="71a48-114">V poli Název dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="71a48-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="71a48-115">Chcete-li vybrat všechny dimenze v aktuální společnosti, zadejte následující hodnoty:   BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="71a48-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="71a48-116">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="71a48-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="71a48-117">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="71a48-117">Click Filter.</span></span>
8. <span data-ttu-id="71a48-118">Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="71a48-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="71a48-119">Zadejte hodnotu 00057 do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="71a48-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="71a48-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="71a48-120">Click OK.</span></span>
11. <span data-ttu-id="71a48-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="71a48-121">Click OK.</span></span>
    * <span data-ttu-id="71a48-122">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="71a48-122">Review the generated output.</span></span> <span data-ttu-id="71a48-123">Všimněte si, že pro každou transakci vybrané dávky jsou uvedeny finanční dimenze z odpovídající sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="71a48-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="71a48-124">Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci.</span><span class="sxs-lookup"><span data-stu-id="71a48-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

