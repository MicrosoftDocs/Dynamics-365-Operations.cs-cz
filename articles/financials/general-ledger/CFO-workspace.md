---
title: "Přidání finančních dimenzí k pracovnímu prostoru CFO"
description: "Toto téma vysvětluje postup při přidání finančních dimenzí do pracovního prostoru CFO tak, aby bylo možné je používat pro hlavní knihu a sestavy rozpočtu."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5faefe5da8c3a64987a38ebef92eb87049ebe874
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="07bec-103">Přidání finančních dimenzí k pracovnímu prostoru CFO</span><span class="sxs-lookup"><span data-stu-id="07bec-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="07bec-104">Toto téma vysvětluje postup při přidání finančních dimenzí do pracovního prostoru CFO (Chief Financial Officer) tak, aby bylo možné je používat pro hlavní knihu a sestavy rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="07bec-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="07bec-105">Pracovní prostor CFO má kartu **Přehled** a kartu **Finanční**. Sestavy na těchto dvou kartách jsou podloženy dvěma měřeními: LedgerActivityMeasure a BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="07bec-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="07bec-106">V aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017) existuje vztah mezi těmito dvěma měřeními a entitou DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="07bec-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="07bec-107">Z tohoto důvodu lze vybrat dimenze.</span><span class="sxs-lookup"><span data-stu-id="07bec-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="07bec-108">V aplikaci Finance and Operations aktualizujte měření **LedgerActivityMeasure** a **BudgetActivityMeasure** na stránce **Úložiště entit**.</span><span class="sxs-lookup"><span data-stu-id="07bec-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="07bec-109">V aplikaci Microsoft Visual Studio otevřete Průzkumníka aplikace a vyhledejte **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="07bec-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="07bec-110">Pod položkou **Zdroje** otevřete **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="07bec-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="07bec-111">Když se zdroj otevře v Microsoft Power BI Desktop, vyberte **Načíst data**, vyberte **Databáze SQL Server** a poté vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="07bec-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="07bec-112">Zadejte název serveru a zadejte **AxDW** jako databázi.</span><span class="sxs-lookup"><span data-stu-id="07bec-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="07bec-113">Vyberte možnost **DirectQuery** a pak zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="07bec-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="07bec-114">Vyhledejte a vyberte **LedgerActivityMeasure\_DimensionCombination** a poté vyberte **Načíst**.</span><span class="sxs-lookup"><span data-stu-id="07bec-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="07bec-115">V seznamu **Pole** přejmenujte tabulku **Finanční dimenze**, aby ji bylo možné snadno identifikovat.</span><span class="sxs-lookup"><span data-stu-id="07bec-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="07bec-116">Vyberte **Spravovat relace** a poté vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="07bec-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="07bec-117">V prvním poli vyberte **Aktivity hlavní knihy** a poté vyberte **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="07bec-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="07bec-118">V druhém poli vyberte **LedgerActivityMeasure\_DimensionCombination** (nebo **Finanční dimenze**, pokud jste přejmenovali tabulku).</span><span class="sxs-lookup"><span data-stu-id="07bec-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="07bec-119">Vyberte záhlaví **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="07bec-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="07bec-120">V poli **Kardinalita** vyberte **N:1**.</span><span class="sxs-lookup"><span data-stu-id="07bec-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="07bec-121">Změňte hodnotu **Směr křížového filtru** na **Jednoduchý**.</span><span class="sxs-lookup"><span data-stu-id="07bec-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="07bec-122">Zvolte **Aktivovat tuto relaci** a **Předpokládat referenční integritu**, vyberte **OK** a poté vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="07bec-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="07bec-123">[![Vytvoření relace](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="07bec-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="07bec-124">V seznamu **Pole** by se měla zobrazit tabulka a dostupné finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="07bec-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="07bec-125">Přetáhněte finanční dimenze, které chcete mít ve filtrech na úrovni sestavy.</span><span class="sxs-lookup"><span data-stu-id="07bec-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="07bec-126">Uložte změny.</span><span class="sxs-lookup"><span data-stu-id="07bec-126">Save your changes.</span></span>
15. <span data-ttu-id="07bec-127">Ve stromu aplikačních objektů (AOT) klikněte pravým tlačítkem myši a poté vyberte **Synchronizovat**.</span><span class="sxs-lookup"><span data-stu-id="07bec-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="07bec-128">Vytvořte svůj projekt a potom otevřete aplikaci pro zobrazení výsledků.</span><span class="sxs-lookup"><span data-stu-id="07bec-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="07bec-129">[![Dokončený pracovní prostor](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="07bec-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

