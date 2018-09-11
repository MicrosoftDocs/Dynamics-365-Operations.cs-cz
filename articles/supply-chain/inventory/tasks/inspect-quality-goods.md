--- 
title: "Kontrola kvality zboží"
description: "Tato procedura popisuje způsob zpracování objednávky kvality."
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c2313ba26eac8abf6e603f0230f06103802536c4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="0393f-103">Kontrola kvality zboží</span><span class="sxs-lookup"><span data-stu-id="0393f-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0393f-104">Tato procedura popisuje způsob zpracování objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="0393f-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="0393f-105">Tohoto průvodce můžete použít s ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0393f-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="0393f-106">Před zahájením tohoto vzorového postupu je nutné potvrdit nákupní objednávku "000016" a zaúčtovat příjemku produktu.</span><span class="sxs-lookup"><span data-stu-id="0393f-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="0393f-107">To způsobí automatické vytvoření objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="0393f-107">This will automatically create a quality order.</span></span> <span data-ttu-id="0393f-108">Kontroly kvality obvykle provádějí pracovníci pro kontrolu kvality.</span><span class="sxs-lookup"><span data-stu-id="0393f-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="0393f-109">Vyberte objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="0393f-109">Select a quality order</span></span>
1. <span data-ttu-id="0393f-110">Přejděte na Řízení zásob > Periodické úlohy > Správa kvality > Objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="0393f-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="0393f-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="0393f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0393f-112">Vyberte objednávku kvality, která byla vytvořena před zahájením tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="0393f-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="0393f-113">Záznam výsledků testu</span><span class="sxs-lookup"><span data-stu-id="0393f-113">Record test results</span></span>
1. <span data-ttu-id="0393f-114">Klikněte na možnost Výsledky.</span><span class="sxs-lookup"><span data-stu-id="0393f-114">Click Results.</span></span>
2. <span data-ttu-id="0393f-115">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="0393f-115">Click Edit.</span></span>
3. <span data-ttu-id="0393f-116">V poli Výsledné množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0393f-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="0393f-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="0393f-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="0393f-118">V poli Výsledek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0393f-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0393f-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0393f-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0393f-120">V tomto příkladu vychází výsledek z předem definovaného výsledku.</span><span class="sxs-lookup"><span data-stu-id="0393f-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="0393f-121">Běžně byste vytvořili záznam s mnohem přesnějšími výsledky, jako například s velikostí nebo jinou dimenzí.</span><span class="sxs-lookup"><span data-stu-id="0393f-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="0393f-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0393f-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0393f-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0393f-123">Click Save.</span></span>
9. <span data-ttu-id="0393f-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0393f-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="0393f-125">Ověřit objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="0393f-125">Validate the quality order</span></span>
1. <span data-ttu-id="0393f-126">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="0393f-126">Click Validate.</span></span>
2. <span data-ttu-id="0393f-127">V poli Ověřil(a) kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0393f-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0393f-128">Vyberte uživatele provádějícího kontrolu.</span><span class="sxs-lookup"><span data-stu-id="0393f-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="0393f-129">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0393f-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0393f-130">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="0393f-130">Click Select.</span></span>
5. <span data-ttu-id="0393f-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0393f-131">Click OK.</span></span>
6. <span data-ttu-id="0393f-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0393f-132">Close the page.</span></span>


