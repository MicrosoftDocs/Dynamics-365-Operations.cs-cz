---
title: 'Vytváření prvků nákladů  '
description: Existuje několik způsobů, jak vytvořit prvky nákladů v nákladovém účetnictví.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87f93fd7c1c42045274d6b89847b27e93614d9a4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441293"
---
# <a name="create-cost-elements"></a><span data-ttu-id="f8e87-103">Vytváření prvků nákladů  </span><span class="sxs-lookup"><span data-stu-id="f8e87-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8e87-104">Existuje několik způsobů, jak vytvořit prvky nákladů v nákladovém účetnictví.</span><span class="sxs-lookup"><span data-stu-id="f8e87-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="f8e87-105">Tato procedura popisuje, jak vytvořit nákladové prvky importováním hlavních účtů prostřednictvím datového konektoru.</span><span class="sxs-lookup"><span data-stu-id="f8e87-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="f8e87-106">K vytvoření této procedury byla použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="f8e87-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="f8e87-107">Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="f8e87-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="f8e87-108">Vytvoření nových prvků nákladů</span><span class="sxs-lookup"><span data-stu-id="f8e87-108">Create new cost elements</span></span>
1. <span data-ttu-id="f8e87-109">Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8e87-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="f8e87-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f8e87-110">Click New.</span></span>
3. <span data-ttu-id="f8e87-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="f8e87-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f8e87-112">V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f8e87-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="f8e87-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="f8e87-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f8e87-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f8e87-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="f8e87-115">Konfigurace datového konektoru</span><span class="sxs-lookup"><span data-stu-id="f8e87-115">Configure the data connector</span></span>
1. <span data-ttu-id="f8e87-116">Klikněte na Konfigurovat poskytovatele členů dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f8e87-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="f8e87-117">V poli Účtová osnova zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f8e87-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="f8e87-118">Vyberte Sdílené pro použití sdílené účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="f8e87-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="f8e87-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f8e87-119">Click New.</span></span>
4. <span data-ttu-id="f8e87-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f8e87-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f8e87-121">Můžete použít filtry u účtů, které splňují vaše kritéria.</span><span class="sxs-lookup"><span data-stu-id="f8e87-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="f8e87-122">V poli Z hlavního účtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f8e87-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="f8e87-123">V poli Na hlavní účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f8e87-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="f8e87-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f8e87-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="f8e87-125">Importovat hlavní účty</span><span class="sxs-lookup"><span data-stu-id="f8e87-125">Import main accounts</span></span>
1. <span data-ttu-id="f8e87-126">Klikněte na Importovat členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="f8e87-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="f8e87-127">Hlavní účty budou importovány do nákladového účetnictví a použity jako nákladové prvky.</span><span class="sxs-lookup"><span data-stu-id="f8e87-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="f8e87-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f8e87-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="f8e87-129">Zobrazení importovaných účtů jako prvků nákladů</span><span class="sxs-lookup"><span data-stu-id="f8e87-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="f8e87-130">Klikněte na Zobrazit členy dimenze.</span><span class="sxs-lookup"><span data-stu-id="f8e87-130">Click View dimension members.</span></span>
    * <span data-ttu-id="f8e87-131">Zobrazte importované účty hlavní knihy jako nákladové prvky ve vaší firmě, do které mohou být evidovány náklady.</span><span class="sxs-lookup"><span data-stu-id="f8e87-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

