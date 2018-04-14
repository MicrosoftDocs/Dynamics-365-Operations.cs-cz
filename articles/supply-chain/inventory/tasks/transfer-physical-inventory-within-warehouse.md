---
title: "Převedení fyzických zásob ve skladu"
description: "Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 442a608d2f7c7923ec50654d3d96cc429d205537
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="b96fc-103">Převedení fyzických zásob ve skladu</span><span class="sxs-lookup"><span data-stu-id="b96fc-103">Transfer physical inventory within the warehouse</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b96fc-104">Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého.</span><span class="sxs-lookup"><span data-stu-id="b96fc-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="b96fc-105">Předtím, než začnete, je třeba mít nastaven název deníku zásob pro převody zásob.</span><span class="sxs-lookup"><span data-stu-id="b96fc-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="b96fc-106">Tento postup můžete projít v ukázkových datech společnosti USMF pomocí příkladových hodnot, které jsou zobrazeny, nebo můžete použít vlastní data, pokud máte produkty a nastavená umístění.</span><span class="sxs-lookup"><span data-stu-id="b96fc-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="b96fc-107">Tyto úkoly obvykle provádějí zaměstnanci skladu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="b96fc-108">Vytvořit deník převodu zásob</span><span class="sxs-lookup"><span data-stu-id="b96fc-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="b96fc-109">Přejít do převodu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-109">Go to Transfer.</span></span>
2. <span data-ttu-id="b96fc-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b96fc-110">Click New.</span></span>
3. <span data-ttu-id="b96fc-111">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="b96fc-112">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b96fc-112">Click OK.</span></span>
    * <span data-ttu-id="b96fc-113">Pro každý řádek deníku je možné zadat hodnotu dimenzí „od“ a „do“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="b96fc-114">Ty jsou pro tento typ deníku nezbytné.</span><span class="sxs-lookup"><span data-stu-id="b96fc-114">These are essential for this journal type.</span></span> <span data-ttu-id="b96fc-115">Položky můžete převést do umístění pomocí různých pravidel.</span><span class="sxs-lookup"><span data-stu-id="b96fc-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="b96fc-116">V tomto příkladu přeneseme položku v rámci stejného skladu, z umístění řízeného registrační značkou do umístění, která není řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="b96fc-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="b96fc-117">Vytvoření řádků deníku</span><span class="sxs-lookup"><span data-stu-id="b96fc-117">Create journal lines</span></span>
1. <span data-ttu-id="b96fc-118">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b96fc-118">Click New.</span></span>
2. <span data-ttu-id="b96fc-119">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-120">Pokud používáte data USMF, můžete vybrat položku „A0001“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="b96fc-121">V poli Zdrojové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-122">Pokud používáte data USMF, můžete vybrat položku „2“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="b96fc-123">V poli Cílové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-124">Pokud používáte data USMF, můžete vybrat položku „2“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="b96fc-125">V poli Ze skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-126">Pokud používáte data USMF, můžete vybrat „24“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="b96fc-127">V poli Do skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-128">Pokud používáte data USMF, můžete vybrat „24“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="b96fc-129">V poli Ze skladového místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-130">Pokud používáte data USMF, můžete vybrat „FL-001“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="b96fc-131">V poli Do skladového místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-132">Pokud používáte data USMF, můžete vybrat „BULK-001“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="b96fc-133">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="b96fc-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="b96fc-134">Klepněte na kartu Dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="b96fc-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="b96fc-135">V poli Registrační značka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b96fc-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="b96fc-136">Pokud používáte data USMF, můžete vybrat „24“.</span><span class="sxs-lookup"><span data-stu-id="b96fc-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="b96fc-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b96fc-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="b96fc-138">Zaúčtovat deník převodu zásob</span><span class="sxs-lookup"><span data-stu-id="b96fc-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="b96fc-139">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="b96fc-139">Click Post.</span></span>
2. <span data-ttu-id="b96fc-140">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b96fc-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="b96fc-141">Zobrazit skladové transakce</span><span class="sxs-lookup"><span data-stu-id="b96fc-141">View inventory transactions</span></span>
1. <span data-ttu-id="b96fc-142">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="b96fc-142">Click Inventory.</span></span>
2. <span data-ttu-id="b96fc-143">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="b96fc-143">Click Transactions.</span></span>
    * <span data-ttu-id="b96fc-144">V tomto poli se zobrazí transakce, které byly vytvořeny při zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="b96fc-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

