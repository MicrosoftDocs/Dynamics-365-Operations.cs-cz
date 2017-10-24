--- 
title: "Spuštění sestavy používající finanční dimenze jako zdroj dat pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: cdecf5fb3f3047a56353ee6d4a8f94957f508e4b
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="e9afc-103">Spuštění sestavy používající finanční dimenze jako zdroj dat pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="e9afc-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9afc-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="e9afc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="e9afc-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="e9afc-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="e9afc-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 3: návrh sestavy").</span><span class="sxs-lookup"><span data-stu-id="e9afc-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="e9afc-107">Na stránce Parametry elektronického výkaznictví musíte také nakonfigurovat výchozí typy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="e9afc-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="e9afc-108">Výchozí typy dokumentů jsou nastaveny také při stahování a importu konfigurace všech elektronických výkazů.</span><span class="sxs-lookup"><span data-stu-id="e9afc-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="e9afc-109">Spuštění sestavy</span><span class="sxs-lookup"><span data-stu-id="e9afc-109">Run report</span></span>
1. <span data-ttu-id="e9afc-110">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="e9afc-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e9afc-111">Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="e9afc-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="e9afc-112">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí\Sestava deníku hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e9afc-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="e9afc-113">Klikněte na Spustit.</span><span class="sxs-lookup"><span data-stu-id="e9afc-113">Click Run.</span></span>
5. <span data-ttu-id="e9afc-114">V poli Název dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e9afc-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="e9afc-115">Chcete-li vybrat všechny dimenze v aktuální společnosti, zadejte následující hodnoty:   BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="e9afc-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="e9afc-116">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="e9afc-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="e9afc-117">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="e9afc-117">Click Filter.</span></span>
8. <span data-ttu-id="e9afc-118">Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="e9afc-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="e9afc-119">Zadejte hodnotu 00057 do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="e9afc-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="e9afc-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e9afc-120">Click OK.</span></span>
11. <span data-ttu-id="e9afc-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e9afc-121">Click OK.</span></span>
    * <span data-ttu-id="e9afc-122">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="e9afc-122">Review the generated output.</span></span> <span data-ttu-id="e9afc-123">Všimněte si, že pro každou transakci vybrané dávky jsou uvedeny finanční dimenze z odpovídající sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="e9afc-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="e9afc-124">Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci Dynamics 365 for Finance and Operations, edice Enterprise.</span><span class="sxs-lookup"><span data-stu-id="e9afc-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


