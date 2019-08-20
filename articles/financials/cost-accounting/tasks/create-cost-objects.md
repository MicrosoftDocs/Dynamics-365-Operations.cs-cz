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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f63827977f080aa78fb385c60f757ad6b710005
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841242"
---
# <a name="create-cost-objects"></a><span data-ttu-id="3ebec-103">Vytváření objektů nákladů  </span><span class="sxs-lookup"><span data-stu-id="3ebec-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ebec-104">Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska Dynamics 365 for Finance and Operations Enterprise edition v nákladovém účetnictví prostřednictvím datového konektoru.</span><span class="sxs-lookup"><span data-stu-id="3ebec-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="3ebec-105">K vytvoření této procedury byla použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="3ebec-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="3ebec-106">Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="3ebec-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="3ebec-107">Vytvoření nových objektů nákladů</span><span class="sxs-lookup"><span data-stu-id="3ebec-107">Create new cost objects</span></span>
1. <span data-ttu-id="3ebec-108">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="3ebec-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="3ebec-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="3ebec-109">Click New.</span></span>
3. <span data-ttu-id="3ebec-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="3ebec-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3ebec-111">V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3ebec-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="3ebec-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="3ebec-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3ebec-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="3ebec-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="3ebec-114">Konfigurace datového konektoru</span><span class="sxs-lookup"><span data-stu-id="3ebec-114">Configure the data connector</span></span>
1. <span data-ttu-id="3ebec-115">Klikněte na Konfigurovat poskytovatele členů dimenzí.</span><span class="sxs-lookup"><span data-stu-id="3ebec-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="3ebec-116">Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="3ebec-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="3ebec-117">V poli Název dimenze vyberte Nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="3ebec-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="3ebec-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="3ebec-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="3ebec-119">Import nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="3ebec-119">Import cost centers</span></span>
1. <span data-ttu-id="3ebec-120">Klikněte na Importovat členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="3ebec-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="3ebec-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="3ebec-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="3ebec-122">Zobrazení importovaných nákladových středisek</span><span class="sxs-lookup"><span data-stu-id="3ebec-122">View the imported cost centers</span></span>
1. <span data-ttu-id="3ebec-123">Klikněte na Zobrazit členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="3ebec-123">Click View dimension members.</span></span>

