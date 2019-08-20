---
title: Úprava úrovně zásob ve skladu (základní správa skladu)
description: Tento postup vás provede procesem vytvoření a zaúčtování deníku úpravy zásob za účelem úpravy úrovně zásob produktu ve skladu.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 450e95d8a4d5a216b84a3c944c6c63b4a8ad10c5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838816"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="51e65-103">Úprava úrovně zásob ve skladu (základní správa skladu)</span><span class="sxs-lookup"><span data-stu-id="51e65-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51e65-104">Tento postup vás provede procesem vytvoření a zaúčtování deníku úpravy zásob za účelem úpravy úrovně zásob produktu ve skladu.</span><span class="sxs-lookup"><span data-stu-id="51e65-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="51e65-105">Předtím, než začnete, je třeba mít nastaven název deníku zásob pro úpravy zásob.</span><span class="sxs-lookup"><span data-stu-id="51e65-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="51e65-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="51e65-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="51e65-107">Tyto úkoly obvykle provádějí zaměstnanci skladu.</span><span class="sxs-lookup"><span data-stu-id="51e65-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="51e65-108">Vytvoření deníku úprav zásob</span><span class="sxs-lookup"><span data-stu-id="51e65-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="51e65-109">Přejděte do Řízení zásob > Položky deníku > Zboží > Úprava zásob.</span><span class="sxs-lookup"><span data-stu-id="51e65-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="51e65-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="51e65-110">Click New.</span></span>
3. <span data-ttu-id="51e65-111">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="51e65-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="51e65-112">V seznamu klepněte na název deníku úpravy skladu, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="51e65-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="51e65-113">Některá další pole budou vyplněna na základě nastavení názvu deníku úprav zásob, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="51e65-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="51e65-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="51e65-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="51e65-115">Vytvoření řádků deníku</span><span class="sxs-lookup"><span data-stu-id="51e65-115">Create journal lines</span></span>
1. <span data-ttu-id="51e65-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="51e65-116">Click New.</span></span>
2. <span data-ttu-id="51e65-117">V seznamu označte pole čísla položky.</span><span class="sxs-lookup"><span data-stu-id="51e65-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="51e65-118">V poli Číslo položky vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="51e65-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="51e65-119">Používáte-li ukázková data společnosti USMF, zadejte hodnotu „D0001“.</span><span class="sxs-lookup"><span data-stu-id="51e65-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="51e65-120">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="51e65-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="51e65-121">V seznamu vyberte web.</span><span class="sxs-lookup"><span data-stu-id="51e65-121">In the list, select a site.</span></span>
6. <span data-ttu-id="51e65-122">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="51e65-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="51e65-123">V seznamu vyberte sklad.</span><span class="sxs-lookup"><span data-stu-id="51e65-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="51e65-124">Pokud jste vybrali položku se skladovým místem jako povinnou dimenzi, je zde třeba určit umístění.</span><span class="sxs-lookup"><span data-stu-id="51e65-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="51e65-125">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="51e65-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="51e65-126">Pole nákladové ceny určuje náklady za jednotku za příjmy na sklad.</span><span class="sxs-lookup"><span data-stu-id="51e65-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="51e65-127">Pokud náklady nejsou pro číslo položky specifikovány nebo pokud je chcete určit ručně, lze to udělat zde.</span><span class="sxs-lookup"><span data-stu-id="51e65-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="51e65-128">Proveďte ověření a zaúčtování deníku úprav zásob.</span><span class="sxs-lookup"><span data-stu-id="51e65-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="51e65-129">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="51e65-129">Click Validate.</span></span>
2. <span data-ttu-id="51e65-130">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="51e65-130">Click OK.</span></span>
3. <span data-ttu-id="51e65-131">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="51e65-131">Click Post.</span></span>
    * <span data-ttu-id="51e65-132">Když tento typ deníku zaúčtujete, zaúčtuje se příjem nebo výdej zásoby, změní se úroveň a hodnota zásob a vygeneruje se transakce hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="51e65-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="51e65-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="51e65-133">Click OK.</span></span>
5. <span data-ttu-id="51e65-134">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="51e65-134">Close the form.</span></span>
6. <span data-ttu-id="51e65-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="51e65-135">Close the page.</span></span>

