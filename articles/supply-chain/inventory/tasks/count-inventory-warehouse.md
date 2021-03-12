---
title: Inventura zásob ve skladu
description: Toto téma popisuje proces vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7f85cb91f36004a6bd6da714e7baa460a83a66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000081"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="f24c2-103">Inventura zásob ve skladu</span><span class="sxs-lookup"><span data-stu-id="f24c2-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f24c2-104">Toto téma popisuje proces vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu.</span><span class="sxs-lookup"><span data-stu-id="f24c2-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="f24c2-105">Tento postup lze použít pro funkce „základního uskladnění“, dostupného v modulu Řízení zásob, ne pro funkce uskladnění, které jsou k dispozici v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="f24c2-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="f24c2-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="f24c2-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="f24c2-107">Používáte-li vlastní data, ujistěte se, že máte nastaveny produkty a umístění a že jste vytvořili název deníku zásob pro deníky inventury.</span><span class="sxs-lookup"><span data-stu-id="f24c2-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="f24c2-108">Inventuru skladu běžně provádí zaměstnanec skladu.</span><span class="sxs-lookup"><span data-stu-id="f24c2-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="f24c2-109">Vytvořte deník inventur zásob</span><span class="sxs-lookup"><span data-stu-id="f24c2-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="f24c2-110">Přejděte na **Navigační podokno > Moduly > Správa zásob > Deníkové položky > Počet položek > Inventury**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="f24c2-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-111">Select **New**.</span></span>
3. <span data-ttu-id="f24c2-112">V poli **Název** vyberte z rozevíracího seznamu název deníku inventur zásob, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="f24c2-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="f24c2-113">Některá další pole budou vyplněna na základě nastavení názvu deníku inventur zásob, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="f24c2-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="f24c2-114">V poli **Pracovník** klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f24c2-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f24c2-115">Ze seznamu **vyberte** pracovníka, kterého chcete použít.</span><span class="sxs-lookup"><span data-stu-id="f24c2-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="f24c2-116">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="f24c2-117">Vytvořit řádky deníku</span><span class="sxs-lookup"><span data-stu-id="f24c2-117">Create journal lines</span></span>
1. <span data-ttu-id="f24c2-118">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-118">Select **New**.</span></span>
2. <span data-ttu-id="f24c2-119">V poli **Číslo položky** vyberte z rozevíracího seznamu požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="f24c2-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f24c2-120">Používáte-li ukázková data společnosti USMF vyberte hodnotu **A0001**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="f24c2-121">V poli **Pracoviště** vyberte z rozevíracího seznamu požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="f24c2-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f24c2-122">Používáte-li ukázková data společnosti USMF, vyberte pracoviště **2**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="f24c2-123">V poli **Sklad** vyberte z rozevíracího seznamu požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="f24c2-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f24c2-124">Používáte-li ukázková data společnosti USMF, vyberte sklad **24**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="f24c2-125">V poli **Umístění** vyberte z rozevíracího seznamu požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="f24c2-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f24c2-126">Používáte-li ukázková data společnosti USMF, vyberte umístění **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="f24c2-127">Zadejte číslo do pole Spočteno.</span><span class="sxs-lookup"><span data-stu-id="f24c2-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="f24c2-128">Pokud zadáte číslo inventury, které se liší od čísla uvedeného v poli **Na skladě**, pole **množství** se aktualizuje a zobrazí odchylku.</span><span class="sxs-lookup"><span data-stu-id="f24c2-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="f24c2-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="f24c2-130">Zaúčtujte deník inventury zásob</span><span class="sxs-lookup"><span data-stu-id="f24c2-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="f24c2-131">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-131">Select **Post**.</span></span> <span data-ttu-id="f24c2-132">Když tento deník inventury skladu zaúčtujete, a zaúčtovaná částka se bude lišit od částky nahlášené v poli **Na skladě**, zaúčtuje se příjem nebo výdej zásob, změní se úroveň a hodnota zásob a vygeneruje se transakce hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f24c2-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="f24c2-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="f24c2-134">Zobrazit skladové transakce</span><span class="sxs-lookup"><span data-stu-id="f24c2-134">View inventory transactions</span></span>
1. <span data-ttu-id="f24c2-135">Vyberte **skladový model**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="f24c2-136">Vyberte **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="f24c2-136">Select **Transactions**.</span></span> <span data-ttu-id="f24c2-137">V tomto poli se zobrazí všechny související transakce vytvořené při zaúčtování deníku inventury zásob.</span><span class="sxs-lookup"><span data-stu-id="f24c2-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

