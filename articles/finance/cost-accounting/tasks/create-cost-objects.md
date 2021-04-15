---
title: 'Vytváření objektů nákladů  '
description: Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810047"
---
# <a name="create-cost-objects"></a><span data-ttu-id="09ca1-103">Vytváření objektů nákladů  </span><span class="sxs-lookup"><span data-stu-id="09ca1-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09ca1-104">Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru.</span><span class="sxs-lookup"><span data-stu-id="09ca1-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="09ca1-105">K vytvoření této procedury byla použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="09ca1-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="09ca1-106">Vytvoření nových objektů nákladů</span><span class="sxs-lookup"><span data-stu-id="09ca1-106">Create new cost objects</span></span>
1. <span data-ttu-id="09ca1-107">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="09ca1-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="09ca1-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="09ca1-108">Click New.</span></span>
3. <span data-ttu-id="09ca1-109">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="09ca1-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="09ca1-110">V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="09ca1-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="09ca1-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="09ca1-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="09ca1-112">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="09ca1-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="09ca1-113">Konfigurace datového konektoru</span><span class="sxs-lookup"><span data-stu-id="09ca1-113">Configure the data connector</span></span>
1. <span data-ttu-id="09ca1-114">Klikněte na Konfigurovat poskytovatele členů dimenzí.</span><span class="sxs-lookup"><span data-stu-id="09ca1-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="09ca1-115">Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="09ca1-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="09ca1-116">V poli Název dimenze vyberte Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="09ca1-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="09ca1-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="09ca1-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="09ca1-118">Import nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="09ca1-118">Import cost centers</span></span>
1. <span data-ttu-id="09ca1-119">Klikněte na Importovat členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="09ca1-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="09ca1-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="09ca1-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="09ca1-121">Zobrazení importovaných nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="09ca1-121">View the imported cost centers</span></span>
1. <span data-ttu-id="09ca1-122">Klikněte na Zobrazit členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="09ca1-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]