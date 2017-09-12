---
title: "Přidání finančních dimenzí k pracovnímu prostoru CFO"
description: "Toto téma vysvětluje postup při přidání finančních dimenzí do pracovního prostoru CFO tak, aby bylo možné je používat pro hlavní knihu a sestavy rozpočtu."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: cs-cz
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="f8bfe-103">Přidání finančních dimenzí k pracovnímu prostoru CFO</span><span class="sxs-lookup"><span data-stu-id="f8bfe-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f8bfe-104">Toto téma vysvětluje postup při přidání finančních dimenzí do pracovního prostoru CFO (Chief Financial Officer) tak, aby bylo možné je používat pro hlavní knihu a sestavy rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="f8bfe-105">Pracovní prostor CFO má karty **Přehled** kartu a **Finanční**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="f8bfe-106">Sestavy na těchto dvou záložkách jsou podloženy dvěma měřeními: LedgerActivityMeasure a BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="f8bfe-107">V aplikaci Microsoft Dynamics 365 for Finance and Operations, edice Enterprise, v aktualizaci z července 2017, existuje vztah mezi těmito dvěma měřeními a entitou DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="f8bfe-108">Z tohoto důvodu lze vybrat dimenze.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="f8bfe-109">V aplikaci Finance and Operations aktualizujte měření **LedgerActivityMeasure** a **BudgetActivityMeasure** na stránce **Úložiště entit**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="f8bfe-110">V aplikaci Microsoft Visual Studio otevřete Průzkumníka aplikace a vyhledejte **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="f8bfe-111">Pod položkou **Zdroje** otevřete **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="f8bfe-112">Když se zdroj otevře v Microsoft Power BI Desktop, vyberte **Načíst data**, vyberte **Databáze SQL Server** a poté vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="f8bfe-113">Zadejte název serveru a zadejte **AxDW** jako databázi.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="f8bfe-114">Vyberte možnost **DirectQuery** a pak zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="f8bfe-115">Vyhledejte a vyberte **LedgerActivityMeasure\_DimensionCombination** a poté vyberte **Načíst**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="f8bfe-116">V seznamu **Pole** přejmenujte tabulku **Finanční dimenze**, aby ji bylo možné snadno identifikovat.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="f8bfe-117">Vyberte **Spravovat relace** a poté vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="f8bfe-118">V prvním poli vyberte **Aktivity hlavní knihy** a poté vyberte **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="f8bfe-119">V druhém poli vyberte **LedgerActivityMeasure\_DimensionCombination** (nebo **Finanční dimenze**, pokud jste přejmenovali tabulku).</span><span class="sxs-lookup"><span data-stu-id="f8bfe-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="f8bfe-120">Vyberte záhlaví **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="f8bfe-121">V poli **Kardinalita** vyberte **N:1**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="f8bfe-122">Změňte hodnotu **Směr křížového filtru** na **Jednoduchý**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="f8bfe-123">Zvolte **Aktivovat tuto relaci** a **Předpokládat referenční integritu**, vyberte **OK** a poté vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="f8bfe-124">[![Vytvoření relace](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="f8bfe-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="f8bfe-125">V seznamu **Pole** by se měla zobrazit tabulka a dostupné finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="f8bfe-126">Přetáhněte finanční dimenze, které chcete mít ve filtrech na úrovni sestavy.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="f8bfe-127">Uložte změny.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-127">Save your changes.</span></span>
15. <span data-ttu-id="f8bfe-128">Ve stromu aplikačních objektů (AOT) klikněte pravým tlačítkem myši a poté vyberte **Synchronizovat**.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="f8bfe-129">Vytvořte svůj projekt a potom otevřete aplikaci pro zobrazení výsledků.</span><span class="sxs-lookup"><span data-stu-id="f8bfe-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="f8bfe-130">[![Dokončený pracovní prostor](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="f8bfe-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

