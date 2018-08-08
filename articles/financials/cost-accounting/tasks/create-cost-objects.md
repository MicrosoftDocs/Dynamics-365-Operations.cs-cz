--- 
title: "Vytváření objektů nákladů  "
description: "Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska aplikace Dynamics 365 for Finance and Operations, v nákladovém účetnictví prostřednictvím datového konektoru."
author: ShylaThompson
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 571406164236c7c079e059367e5d757cc4cefb1f
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="b4bee-103">Vytváření objektů nákladů  </span><span class="sxs-lookup"><span data-stu-id="b4bee-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4bee-104">Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska aplikace Dynamics 365 for Finance and Operations, v nákladovém účetnictví prostřednictvím datového konektoru.</span><span class="sxs-lookup"><span data-stu-id="b4bee-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="b4bee-105">K vytvoření této procedury byla použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="b4bee-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="b4bee-106">Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="b4bee-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="b4bee-107">Vytvoření nových objektů nákladů</span><span class="sxs-lookup"><span data-stu-id="b4bee-107">Create new cost objects</span></span>
1. <span data-ttu-id="b4bee-108">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="b4bee-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="b4bee-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b4bee-109">Click New.</span></span>
3. <span data-ttu-id="b4bee-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b4bee-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b4bee-111">V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b4bee-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b4bee-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b4bee-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b4bee-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b4bee-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b4bee-114">Konfigurace datového konektoru</span><span class="sxs-lookup"><span data-stu-id="b4bee-114">Configure the data connector</span></span>
1. <span data-ttu-id="b4bee-115">Klikněte na Konfigurovat poskytovatele členů dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b4bee-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="b4bee-116">Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="b4bee-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="b4bee-117">V poli Název dimenze vyberte Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="b4bee-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="b4bee-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b4bee-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="b4bee-119">Import nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="b4bee-119">Import cost centers</span></span>
1. <span data-ttu-id="b4bee-120">Klikněte na Importovat členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="b4bee-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="b4bee-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b4bee-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="b4bee-122">Zobrazení importovaných nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="b4bee-122">View the imported cost centers</span></span>
1. <span data-ttu-id="b4bee-123">Klikněte na Zobrazit členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="b4bee-123">Click View dimension members.</span></span>


