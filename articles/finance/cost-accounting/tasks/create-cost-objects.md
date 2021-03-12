---
title: 'Vytváření objektů nákladů  '
description: Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990760"
---
# <a name="create-cost-objects"></a><span data-ttu-id="b088f-103">Vytváření objektů nákladů  </span><span class="sxs-lookup"><span data-stu-id="b088f-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b088f-104">Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru.</span><span class="sxs-lookup"><span data-stu-id="b088f-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="b088f-105">K vytvoření této procedury byla použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="b088f-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="b088f-106">Vytvoření nových objektů nákladů</span><span class="sxs-lookup"><span data-stu-id="b088f-106">Create new cost objects</span></span>
1. <span data-ttu-id="b088f-107">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="b088f-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="b088f-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b088f-108">Click New.</span></span>
3. <span data-ttu-id="b088f-109">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b088f-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b088f-110">V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b088f-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b088f-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b088f-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b088f-112">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b088f-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b088f-113">Konfigurace datového konektoru</span><span class="sxs-lookup"><span data-stu-id="b088f-113">Configure the data connector</span></span>
1. <span data-ttu-id="b088f-114">Klikněte na Konfigurovat poskytovatele členů dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b088f-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="b088f-115">Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="b088f-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="b088f-116">V poli Název dimenze vyberte Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="b088f-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="b088f-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b088f-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="b088f-118">Import nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="b088f-118">Import cost centers</span></span>
1. <span data-ttu-id="b088f-119">Klikněte na Importovat členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="b088f-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="b088f-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b088f-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="b088f-121">Zobrazení importovaných nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="b088f-121">View the imported cost centers</span></span>
1. <span data-ttu-id="b088f-122">Klikněte na Zobrazit členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="b088f-122">Click View dimension members.</span></span>

