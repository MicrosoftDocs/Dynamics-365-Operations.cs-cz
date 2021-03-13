---
title: Převedení fyzických zásob ve skladu
description: Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c00b6d18b036482cd96e2287119ddb7fd80bfa2d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011440"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="e8a4c-103">Převedení fyzických zásob ve skladu</span><span class="sxs-lookup"><span data-stu-id="e8a4c-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8a4c-104">Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="e8a4c-105">Předtím, než začnete, je třeba mít nastaven název deníku zásob pro převody zásob.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="e8a4c-106">Tento postup můžete projít v ukázkových datech společnosti USMF pomocí příkladových hodnot, které jsou zobrazeny, nebo můžete použít vlastní data, pokud máte produkty a nastavená umístění.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="e8a4c-107">Tyto úkoly obvykle provádějí zaměstnanci skladu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="e8a4c-108">Vytvořit deník převodu zásob</span><span class="sxs-lookup"><span data-stu-id="e8a4c-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="e8a4c-109">V **Navigačním podokně** přejděte na **Řízení zásob > Položky deníku > Položky > Převod**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="e8a4c-110">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-110">Click **New**.</span></span>
3. <span data-ttu-id="e8a4c-111">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="e8a4c-112">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-112">Click **OK**.</span></span> <span data-ttu-id="e8a4c-113">Pro každý řádek deníku je možné zadat hodnotu dimenzí „od“ a „do“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="e8a4c-114">Ty jsou pro tento typ deníku nezbytné.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-114">These are essential for this journal type.</span></span> <span data-ttu-id="e8a4c-115">Položky můžete převést do umístění pomocí různých pravidel.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="e8a4c-116">V tomto příkladu přeneseme položku v rámci stejného skladu, z umístění řízeného registrační značkou do umístění, která není řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="e8a4c-117">Vytvořit řádky deníku</span><span class="sxs-lookup"><span data-stu-id="e8a4c-117">Create journal lines</span></span>
1. <span data-ttu-id="e8a4c-118">Na pevné záložce **Řádky deníku** klikněte klepněte na položku **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="e8a4c-119">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-120">Pokud používáte data USMF, můžete vybrat položku „A0001“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="e8a4c-121">V poli **Zdrojové pracoviště** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-122">Pokud používáte data USMF, můžete vybrat položku „2“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="e8a4c-123">V poli **Cílové pracoviště** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-124">Pokud používáte data USMF, můžete vybrat položku „2“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="e8a4c-125">V poli **Ze skladu zadejte** nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-126">Pokud používáte data USMF, můžete vybrat „24“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="e8a4c-127">V poli **Do skladu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-128">Pokud používáte data USMF, můžete vybrat „24“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="e8a4c-129">V poli **Ze skladového místa** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-130">Pokud používáte data USMF, můžete vybrat „FL-001“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="e8a4c-131">V poli **Do skladového místa** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-132">Pokud používáte data USMF, můžete vybrat „BULK-001“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="e8a4c-133">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="e8a4c-134">Na pevné záložce **Podrobnosti řádku** klikněte na kartu **Dimenze zásob**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="e8a4c-135">V možnosti **Z dimenzí zásob** v poli **Registrační značka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="e8a4c-136">Pokud používáte data USMF, můžete vybrat „24“.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="e8a4c-137">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="e8a4c-138">Zaúčtovat deník převodu zásob</span><span class="sxs-lookup"><span data-stu-id="e8a4c-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="e8a4c-139">V **podokně akcí** klikněte na **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="e8a4c-140">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="e8a4c-141">Zobrazit skladové transakce</span><span class="sxs-lookup"><span data-stu-id="e8a4c-141">View inventory transactions</span></span>
1. <span data-ttu-id="e8a4c-142">Klikněte na položku **Zásoby**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="e8a4c-143">Klikněte **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-143">Click **Transactions**.</span></span> <span data-ttu-id="e8a4c-144">V tomto poli se zobrazí transakce, které byly vytvořeny při zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="e8a4c-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

