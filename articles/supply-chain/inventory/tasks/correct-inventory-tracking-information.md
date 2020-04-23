---
title: Oprava informací o sledování zásob
description: Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob, za účelem opravit informace o sledování zásob.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204187"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="1c2e2-103">Oprava informací o sledování zásob</span><span class="sxs-lookup"><span data-stu-id="1c2e2-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c2e2-104">Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob, za účelem opravit informace o sledování zásob.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="1c2e2-105">V tomto příkladu aktualizujeme informace o položky řízené dávkou pomocí změny nesprávně registrované dávky na jinou dávku.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="1c2e2-106">Tento proces můžete projít pomocí ukázkových dat společnosti USPI nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="1c2e2-107">Při použití vlastních dat musí mít zboží, pro které je povolena dávka a nesmí být řízeno na základě umístění.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="1c2e2-108">Rovněž je třeba mít nastaven název deníku zásob pro převody zásob.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="1c2e2-109">Tyto úkoly obvykle provádějí zaměstnanci skladu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="1c2e2-110">Vytvořit deník převodu zásob</span><span class="sxs-lookup"><span data-stu-id="1c2e2-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="1c2e2-111">Přejít do převodu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-111">Go to Transfer.</span></span>
2. <span data-ttu-id="1c2e2-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-112">Click New.</span></span>
3. <span data-ttu-id="1c2e2-113">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="1c2e2-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="1c2e2-115">Vytvoření řádků deníku</span><span class="sxs-lookup"><span data-stu-id="1c2e2-115">Create journal lines</span></span>
1. <span data-ttu-id="1c2e2-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-116">Click New.</span></span>
2. <span data-ttu-id="1c2e2-117">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="1c2e2-118">Pokud používáte USPI, vyberte položku M5003.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="1c2e2-119">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="1c2e2-120">Klepněte na kartu Dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="1c2e2-121">V poli Číslo dávky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="1c2e2-122">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="1c2e2-123">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="1c2e2-124">V poli Číslo dávky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="1c2e2-125">Zaúčtovat deník</span><span class="sxs-lookup"><span data-stu-id="1c2e2-125">Post the journal</span></span>
1. <span data-ttu-id="1c2e2-126">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-126">Click Post.</span></span>
2. <span data-ttu-id="1c2e2-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="1c2e2-128">Kontrola informací o trase</span><span class="sxs-lookup"><span data-stu-id="1c2e2-128">Check tracing information</span></span>
1. <span data-ttu-id="1c2e2-129">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-129">Click Inventory.</span></span>
2. <span data-ttu-id="1c2e2-130">Klikněte na Trasa.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-130">Click Trace.</span></span>
3. <span data-ttu-id="1c2e2-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-131">Click OK.</span></span>
    * <span data-ttu-id="1c2e2-132">Pomocí těchto informací trasování lze zpětně sledovat, ze které dávky jste opravili skladové položky.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="1c2e2-133">Můžete také použít stránku Sledování položky pro tyto informace.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="1c2e2-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="1c2e2-135">Kontrola transakcí zásob</span><span class="sxs-lookup"><span data-stu-id="1c2e2-135">Check inventory transactions</span></span>
1. <span data-ttu-id="1c2e2-136">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-136">Click Inventory.</span></span>
2. <span data-ttu-id="1c2e2-137">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-137">Click Transactions.</span></span>
    * <span data-ttu-id="1c2e2-138">V tomto poli se zobrazí transakce, které byly vytvořeny při zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="1c2e2-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

