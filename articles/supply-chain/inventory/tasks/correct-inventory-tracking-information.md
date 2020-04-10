---
title: Oprava informací o sledování zásob
description: Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob, za účelem opravit informace o sledování zásob.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5155ada23fe4f559c79964e6bd10d86712009d1d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145757"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="0024a-103">Oprava informací o sledování zásob</span><span class="sxs-lookup"><span data-stu-id="0024a-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0024a-104">Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob, za účelem opravit informace o sledování zásob.</span><span class="sxs-lookup"><span data-stu-id="0024a-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="0024a-105">V tomto příkladu aktualizujeme informace o položky řízené dávkou pomocí změny nesprávně registrované dávky na jinou dávku.</span><span class="sxs-lookup"><span data-stu-id="0024a-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="0024a-106">Tento proces můžete projít pomocí ukázkových dat společnosti USPI nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="0024a-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="0024a-107">Při použití vlastních dat musí mít zboží, pro které je povolena dávka a nesmí být řízeno na základě umístění.</span><span class="sxs-lookup"><span data-stu-id="0024a-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="0024a-108">Rovněž je třeba mít nastaven název deníku zásob pro převody zásob.</span><span class="sxs-lookup"><span data-stu-id="0024a-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="0024a-109">Tyto úkoly obvykle provádějí zaměstnanci skladu.</span><span class="sxs-lookup"><span data-stu-id="0024a-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="0024a-110">Vytvořit deník převodu zásob</span><span class="sxs-lookup"><span data-stu-id="0024a-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="0024a-111">Přejít do převodu.</span><span class="sxs-lookup"><span data-stu-id="0024a-111">Go to Transfer.</span></span>
2. <span data-ttu-id="0024a-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0024a-112">Click New.</span></span>
3. <span data-ttu-id="0024a-113">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0024a-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="0024a-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0024a-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="0024a-115">Vytvoření řádků deníku</span><span class="sxs-lookup"><span data-stu-id="0024a-115">Create journal lines</span></span>
1. <span data-ttu-id="0024a-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0024a-116">Click New.</span></span>
2. <span data-ttu-id="0024a-117">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0024a-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="0024a-118">Pokud používáte USPI, vyberte položku M5003.</span><span class="sxs-lookup"><span data-stu-id="0024a-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="0024a-119">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="0024a-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="0024a-120">Klepněte na kartu Dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="0024a-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="0024a-121">V poli Číslo dávky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0024a-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="0024a-122">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0024a-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="0024a-123">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0024a-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="0024a-124">V poli Číslo dávky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0024a-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="0024a-125">Zaúčtovat deník</span><span class="sxs-lookup"><span data-stu-id="0024a-125">Post the journal</span></span>
1. <span data-ttu-id="0024a-126">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="0024a-126">Click Post.</span></span>
2. <span data-ttu-id="0024a-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0024a-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="0024a-128">Kontrola informací o trase</span><span class="sxs-lookup"><span data-stu-id="0024a-128">Check tracing information</span></span>
1. <span data-ttu-id="0024a-129">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="0024a-129">Click Inventory.</span></span>
2. <span data-ttu-id="0024a-130">Klikněte na Trasa.</span><span class="sxs-lookup"><span data-stu-id="0024a-130">Click Trace.</span></span>
3. <span data-ttu-id="0024a-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0024a-131">Click OK.</span></span>
    * <span data-ttu-id="0024a-132">Pomocí těchto informací trasování lze zpětně sledovat, ze které dávky jste opravili skladové položky.</span><span class="sxs-lookup"><span data-stu-id="0024a-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="0024a-133">Můžete také použít stránku Sledování položky pro tyto informace.</span><span class="sxs-lookup"><span data-stu-id="0024a-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="0024a-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0024a-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="0024a-135">Kontrola transakcí zásob</span><span class="sxs-lookup"><span data-stu-id="0024a-135">Check inventory transactions</span></span>
1. <span data-ttu-id="0024a-136">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="0024a-136">Click Inventory.</span></span>
2. <span data-ttu-id="0024a-137">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="0024a-137">Click Transactions.</span></span>
    * <span data-ttu-id="0024a-138">V tomto poli se zobrazí transakce, které byly vytvořeny při zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="0024a-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

