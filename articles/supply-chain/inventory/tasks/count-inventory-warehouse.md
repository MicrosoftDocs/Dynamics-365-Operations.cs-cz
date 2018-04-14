---
title: "Inventura zásob ve skladu"
description: "Tento postup vás provede procesem vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 9832a60ee703878701927b66b0b4b63cb7efb985
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="b8a26-103">Inventura zásob ve skladu</span><span class="sxs-lookup"><span data-stu-id="b8a26-103">Count inventory in a warehouse</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8a26-104">Tento postup vás provede procesem vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu.</span><span class="sxs-lookup"><span data-stu-id="b8a26-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="b8a26-105">Tento postup lze použít pro funkce „základního uskladnění“, dostupného v modulu Řízení zásob, ne pro funkce uskladnění, které jsou k dispozici v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="b8a26-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="b8a26-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="b8a26-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="b8a26-107">Používáte-li vlastní data, ujistěte se, že máte nastaveny produkty a umístění a že jste vytvořili název deníku zásob pro deníky inventury.</span><span class="sxs-lookup"><span data-stu-id="b8a26-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="b8a26-108">Inventuru skladu běžně provádí zaměstnanec skladu.</span><span class="sxs-lookup"><span data-stu-id="b8a26-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="b8a26-109">Vytvořte deník inventur zásob</span><span class="sxs-lookup"><span data-stu-id="b8a26-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="b8a26-110">Přejděte do Řízení zásob > Položky deníku > Inventura zboží > Inventura.</span><span class="sxs-lookup"><span data-stu-id="b8a26-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="b8a26-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b8a26-111">Click New.</span></span>
3. <span data-ttu-id="b8a26-112">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b8a26-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b8a26-113">V seznamu klepněte na název deníku inventury skladu, který chcete použít</span><span class="sxs-lookup"><span data-stu-id="b8a26-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="b8a26-114">Některá další pole budou vyplněna na základě nastavení názvu deníku inventur zásob, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="b8a26-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="b8a26-115">V poli Pracovník klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b8a26-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b8a26-116">Ze seznamu vyberte pracovníka, kterého chcete použít.</span><span class="sxs-lookup"><span data-stu-id="b8a26-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="b8a26-117">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="b8a26-117">Click Select.</span></span>
8. <span data-ttu-id="b8a26-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b8a26-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="b8a26-119">Vytvoření řádků deníku</span><span class="sxs-lookup"><span data-stu-id="b8a26-119">Create journal lines</span></span>
1. <span data-ttu-id="b8a26-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b8a26-120">Click New.</span></span>
2. <span data-ttu-id="b8a26-121">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b8a26-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b8a26-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b8a26-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8a26-123">Používáte-li ukázková data společnosti USMF, vyberte hodnotu „A0001“.</span><span class="sxs-lookup"><span data-stu-id="b8a26-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="b8a26-124">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b8a26-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b8a26-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b8a26-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8a26-126">Používáte-li ukázková data společnosti USMF, vyberte web „2“.</span><span class="sxs-lookup"><span data-stu-id="b8a26-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="b8a26-127">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b8a26-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b8a26-128">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b8a26-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8a26-129">Používáte-li ukázková data společnosti USMF, vyberte sklad „24“.</span><span class="sxs-lookup"><span data-stu-id="b8a26-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="b8a26-130">V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b8a26-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b8a26-131">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b8a26-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8a26-132">Používáte-li ukázková data společnosti USMF, vyberte umístění „BULK-001“.</span><span class="sxs-lookup"><span data-stu-id="b8a26-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="b8a26-133">Zadejte číslo do pole Spočteno.</span><span class="sxs-lookup"><span data-stu-id="b8a26-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="b8a26-134">Pokud zadáte číslo inventury, které se liší od čísla uvedeného v poli Na skladě, pole množství se aktualizuje a zobrazí odchylku.</span><span class="sxs-lookup"><span data-stu-id="b8a26-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="b8a26-135">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b8a26-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="b8a26-136">Zaúčtujte deník inventury zásob</span><span class="sxs-lookup"><span data-stu-id="b8a26-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="b8a26-137">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="b8a26-137">Click Post.</span></span>
    * <span data-ttu-id="b8a26-138">Když tento deník inventury skladu zaúčtujete, a zaúčtovaná částka se bude lišit od částky nahlášené v poli Na skladě, zaúčtuje se příjem nebo výdej zásob, změní se úroveň a hodnota zásob a vygeneruje se transakce hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b8a26-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="b8a26-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b8a26-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="b8a26-140">Zobrazit skladové transakce</span><span class="sxs-lookup"><span data-stu-id="b8a26-140">View inventory transactions</span></span>
1. <span data-ttu-id="b8a26-141">Klepněte na položku Zásoby.</span><span class="sxs-lookup"><span data-stu-id="b8a26-141">Click Inventory.</span></span>
2. <span data-ttu-id="b8a26-142">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="b8a26-142">Click Transactions.</span></span>
    * <span data-ttu-id="b8a26-143">V tomto poli se zobrazí všechny související transakce vytvořené při zaúčtování deníku inventury zásob.</span><span class="sxs-lookup"><span data-stu-id="b8a26-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

