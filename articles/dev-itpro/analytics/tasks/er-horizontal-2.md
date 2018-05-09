--- 
title: "Spuštění formátu používajícího vodorovně rozbalovací oblasti k dynamickému přidání sloupců v sestavách aplikace Excel"
description: "Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c4538bd9f8c71108e7ec8fd9da2c2b914d76f13
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="62e0d-103">Spuštění formátu používajícího vodorovně rozbalovací oblasti k dynamickému přidání sloupců v sestavách aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="62e0d-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62e0d-104">Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy.</span><span class="sxs-lookup"><span data-stu-id="62e0d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="62e0d-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="62e0d-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="62e0d-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel (část 1: formát návrhu).</span><span class="sxs-lookup"><span data-stu-id="62e0d-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="62e0d-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="62e0d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="62e0d-108">Vyhledání vytvořeného formátu</span><span class="sxs-lookup"><span data-stu-id="62e0d-108">Find created format</span></span>
1. <span data-ttu-id="62e0d-109">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="62e0d-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="62e0d-110">Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="62e0d-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="62e0d-111">Ve stromové struktuře vyberte 'Vzorový model finančních dimenzí\Vzorová sestava s vodorovně rozbalitelnými rozsahy'.</span><span class="sxs-lookup"><span data-stu-id="62e0d-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="62e0d-112">Spuštění formátu k vytvoření výstupu v Excelu</span><span class="sxs-lookup"><span data-stu-id="62e0d-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="62e0d-113">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="62e0d-113">Click Run.</span></span>
2. <span data-ttu-id="62e0d-114">Do pole Název dimenze zadejte 'BusinessUnit;CostCenter;Department'.</span><span class="sxs-lookup"><span data-stu-id="62e0d-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="62e0d-115">V poli Název dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="62e0d-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="62e0d-116">Chcete-li vybrat všechny dimenze pro aktuální společnost, zadejte následující hodnoty:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="62e0d-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="62e0d-117">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="62e0d-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="62e0d-118">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="62e0d-118">Click Filter.</span></span>
5. <span data-ttu-id="62e0d-119">Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="62e0d-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="62e0d-120">Zadejte hodnotu '00057..00058' do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="62e0d-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="62e0d-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="62e0d-121">00057..00058</span></span>  
7. <span data-ttu-id="62e0d-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="62e0d-122">Click OK.</span></span>
8. <span data-ttu-id="62e0d-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="62e0d-123">Click OK.</span></span>
    * <span data-ttu-id="62e0d-124">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="62e0d-124">Review the generated output.</span></span> <span data-ttu-id="62e0d-125">Všimněte si, že nově vytvořený soubor aplikace Excel obsahuje stejný počet sloupců, které byly vybrány pro finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="62e0d-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="62e0d-126">Záhlaví sestavy v těchto sloupcích představuje názvy finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="62e0d-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="62e0d-127">Řádky transakce v těchto sloupcích představují finančních dimenze.</span><span class="sxs-lookup"><span data-stu-id="62e0d-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="62e0d-128">Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava nezávisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="62e0d-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


