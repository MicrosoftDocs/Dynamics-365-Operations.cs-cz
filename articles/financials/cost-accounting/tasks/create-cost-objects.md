--- 
title: "Vytváření objektů nákladů  "
description: "Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska aplikace Dynamics 365 for Finance and Operations, Enterprise edition v nákladovém účetnictví prostřednictvím datového konektoru."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 52b5fe092048cd7efe7b0a697cd7061ee0f65103
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="f6175-103">Vytváření objektů nákladů  </span><span class="sxs-lookup"><span data-stu-id="f6175-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6175-104">Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska aplikace Dynamics 365 for Finance and Operations, Enterprise edition v nákladovém účetnictví prostřednictvím datového konektoru.</span><span class="sxs-lookup"><span data-stu-id="f6175-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="f6175-105">K vytvoření této procedury byla použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="f6175-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="f6175-106">Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="f6175-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="f6175-107">Vytvoření nových objektů nákladů</span><span class="sxs-lookup"><span data-stu-id="f6175-107">Create new cost objects</span></span>
1. <span data-ttu-id="f6175-108">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="f6175-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="f6175-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f6175-109">Click New.</span></span>
3. <span data-ttu-id="f6175-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="f6175-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f6175-111">V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f6175-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="f6175-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="f6175-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f6175-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f6175-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="f6175-114">Konfigurace datového konektoru</span><span class="sxs-lookup"><span data-stu-id="f6175-114">Configure the data connector</span></span>
1. <span data-ttu-id="f6175-115">Klikněte na Konfigurovat poskytovatele členů dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f6175-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="f6175-116">Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="f6175-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="f6175-117">V poli Název dimenze vyberte Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="f6175-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="f6175-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f6175-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="f6175-119">Import nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="f6175-119">Import cost centers</span></span>
1. <span data-ttu-id="f6175-120">Klikněte na Importovat členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="f6175-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="f6175-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f6175-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="f6175-122">Zobrazení importovaných nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="f6175-122">View the imported cost centers</span></span>
1. <span data-ttu-id="f6175-123">Klikněte na Zobrazit členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="f6175-123">Click View dimension members.</span></span>


