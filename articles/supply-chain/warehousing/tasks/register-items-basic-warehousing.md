---
title: Registrace položek pro položky umožňující základní uskladnění pomocí deníku se záznamem doručení položek
description: Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete "základní funkce skladu" v modulu Řízení zásob.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3e8ffa6cee7742de1cd98c9c83d134b6d5e4a89
ms.sourcegitcommit: 529763612e8af315d588e85ba807a5c849df57bf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/25/2019
ms.locfileid: "894671"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="32cf0-103">Registrace položek pro položky umožňující základní uskladnění pomocí deníku se záznamem doručení položek</span><span class="sxs-lookup"><span data-stu-id="32cf0-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32cf0-104">Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete "základní funkce skladu" v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="32cf0-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="32cf0-105">To obvykle provádí přijímající pracovník.</span><span class="sxs-lookup"><span data-stu-id="32cf0-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="32cf0-106">Tento postup můžete spustit s ukázkovými daty společnosti USMF s ukázkovými hodnotami, které jsou zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="32cf0-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="32cf0-107">Pokud nepoužíváte USMF, musíte mít před zahájením tohoto průvodce potvrzenou nákupní objednávku s otevřeným řádkem nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="32cf0-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="32cf0-108">Položka na řádku musí být na skladě.</span><span class="sxs-lookup"><span data-stu-id="32cf0-108">The item on the line must be stocked.</span></span> <span data-ttu-id="32cf0-109">Položka zároveň musí být přidružena ke skupině dimenzí úložiště, kde jsou aktivní pracoviště a sklad.</span><span class="sxs-lookup"><span data-stu-id="32cf0-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="32cf0-110">Vytvoření záhlaví deníku pro doručení položky</span><span class="sxs-lookup"><span data-stu-id="32cf0-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="32cf0-111">Přejděte do Řízení zásob > Položky deníku > Doručení položky > Doručení položky.</span><span class="sxs-lookup"><span data-stu-id="32cf0-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="32cf0-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="32cf0-112">Click New.</span></span>
3. <span data-ttu-id="32cf0-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="32cf0-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="32cf0-114">Pokud používáte data USMF, můžete zadat „WHS“.</span><span class="sxs-lookup"><span data-stu-id="32cf0-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="32cf0-115">Pokud používáte jiná data, deník s názvem, který zvolíte, musí mít následující vlastnosti: místo výdeje šeku musí být nastaveno na hodnotu Ne a u Řízení karantény musí být nastavena hodnota Ne.</span><span class="sxs-lookup"><span data-stu-id="32cf0-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="32cf0-116">Zadejte hodnotu do pole Dodací list.</span><span class="sxs-lookup"><span data-stu-id="32cf0-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="32cf0-117">Jedná se o ID dodacího listu z dodacího listu vydaného dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="32cf0-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="32cf0-118">Přidejte jedinečné číslo.</span><span class="sxs-lookup"><span data-stu-id="32cf0-118">Add a unique number.</span></span>  
5. <span data-ttu-id="32cf0-119">V poli Číslo vyberte nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="32cf0-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="32cf0-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32cf0-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="32cf0-121">Přidání řádků do deníku doručení zboží</span><span class="sxs-lookup"><span data-stu-id="32cf0-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="32cf0-122">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="32cf0-122">Click Functions.</span></span>
2. <span data-ttu-id="32cf0-123">Klikněte na Vytvořit řádky.</span><span class="sxs-lookup"><span data-stu-id="32cf0-123">Click Create lines.</span></span>
    * <span data-ttu-id="32cf0-124">Řádky lze zadat ručně do tohoto deníku, nebo je vytvořit automaticky.</span><span class="sxs-lookup"><span data-stu-id="32cf0-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="32cf0-125">Tím se zobrazí, jak lze vytvoření provést automaticky.</span><span class="sxs-lookup"><span data-stu-id="32cf0-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="32cf0-126">Zaškrtněte nebo zrušte zaškrtnutí políčka Inicializovat množství.</span><span class="sxs-lookup"><span data-stu-id="32cf0-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="32cf0-127">To zahájí sledování množství na řádcích deníku, u kterých není množství zaregistrováno z řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="32cf0-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="32cf0-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32cf0-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="32cf0-129">Zaúčtovat deník</span><span class="sxs-lookup"><span data-stu-id="32cf0-129">Post the journal</span></span>
1. <span data-ttu-id="32cf0-130">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="32cf0-130">Click Post.</span></span>
2. <span data-ttu-id="32cf0-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32cf0-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="32cf0-132">Generování příjemky produktu</span><span class="sxs-lookup"><span data-stu-id="32cf0-132">Generate the product receipt</span></span>
1. <span data-ttu-id="32cf0-133">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="32cf0-133">Click Functions.</span></span>
2. <span data-ttu-id="32cf0-134">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="32cf0-134">Click Product receipt.</span></span>
3. <span data-ttu-id="32cf0-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32cf0-135">Click OK.</span></span>

