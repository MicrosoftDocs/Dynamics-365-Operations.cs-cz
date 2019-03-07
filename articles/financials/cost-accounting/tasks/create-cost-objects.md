---
title: 'Vytváření objektů nákladů  '
description: Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska Dynamics 365 for Finance and Operations Enterprise edition v nákladovém účetnictví prostřednictvím datového konektoru.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "322667"
---
# <a name="create-cost-objects"></a><span data-ttu-id="34b47-103">Vytváření objektů nákladů  </span><span class="sxs-lookup"><span data-stu-id="34b47-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34b47-104">Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska Dynamics 365 for Finance and Operations Enterprise edition v nákladovém účetnictví prostřednictvím datového konektoru.</span><span class="sxs-lookup"><span data-stu-id="34b47-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="34b47-105">K vytvoření této procedury byla použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="34b47-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="34b47-106">Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="34b47-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="34b47-107">Vytvoření nových objektů nákladů</span><span class="sxs-lookup"><span data-stu-id="34b47-107">Create new cost objects</span></span>
1. <span data-ttu-id="34b47-108">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="34b47-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="34b47-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="34b47-109">Click New.</span></span>
3. <span data-ttu-id="34b47-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="34b47-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="34b47-111">V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34b47-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="34b47-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="34b47-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="34b47-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="34b47-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="34b47-114">Konfigurace datového konektoru</span><span class="sxs-lookup"><span data-stu-id="34b47-114">Configure the data connector</span></span>
1. <span data-ttu-id="34b47-115">Klikněte na Konfigurovat poskytovatele členů dimenzí.</span><span class="sxs-lookup"><span data-stu-id="34b47-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="34b47-116">Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="34b47-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="34b47-117">V poli Název dimenze vyberte Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="34b47-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="34b47-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="34b47-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="34b47-119">Import nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="34b47-119">Import cost centers</span></span>
1. <span data-ttu-id="34b47-120">Klikněte na Importovat členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="34b47-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="34b47-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="34b47-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="34b47-122">Zobrazení importovaných nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="34b47-122">View the imported cost centers</span></span>
1. <span data-ttu-id="34b47-123">Klikněte na Zobrazit členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="34b47-123">Click View dimension members.</span></span>

