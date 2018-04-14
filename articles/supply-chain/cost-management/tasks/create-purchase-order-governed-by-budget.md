--- 
title: "Vytvoření nákupní objednávky řízené rozpočtem"
description: "Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ddd725df4e06caf36be0e8913b556469421fa1af
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="41404-103">Vytvoření nákupní objednávky řízené rozpočtem</span><span class="sxs-lookup"><span data-stu-id="41404-103">Create a purchase order governed by budget</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41404-104">Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="41404-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="41404-105">Tento záznam používá v ukázkových datech společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="41404-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="41404-106">Zkontrolujte konfiguraci kontroly rozpočtu</span><span class="sxs-lookup"><span data-stu-id="41404-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="41404-107">Přejděte na Rozpočtování > Nastavení > Kontrola rozpočtu > Konfigurace kontroly rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="41404-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="41404-108">Klikněte na kartu Dostupné rozpočtové prostředky.</span><span class="sxs-lookup"><span data-stu-id="41404-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="41404-109">Klepněte na kartu Dokumenty a deníky.</span><span class="sxs-lookup"><span data-stu-id="41404-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="41404-110">Klepněte na kartu Definovat pravidla kontroly rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="41404-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="41404-111">Klepněte na kartu Definovat rozpočtové skupiny.</span><span class="sxs-lookup"><span data-stu-id="41404-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="41404-112">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="41404-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="41404-113">Vytvoření záhlaví nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="41404-113">Create the purchase order header</span></span>
1. <span data-ttu-id="41404-114">Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="41404-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="41404-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="41404-115">Click New.</span></span>
3. <span data-ttu-id="41404-116">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="41404-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="41404-117">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="41404-117">Expand the General section.</span></span>
5. <span data-ttu-id="41404-118">Do pole Datum účtování nastavte datum 2016-01-01.</span><span class="sxs-lookup"><span data-stu-id="41404-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="41404-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="41404-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="41404-120">Přidání řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="41404-120">Add a purchase order line</span></span>
1. <span data-ttu-id="41404-121">V Kategorie zásobování zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="41404-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="41404-122">Nastavte množství na „2“.</span><span class="sxs-lookup"><span data-stu-id="41404-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="41404-123">V poli Jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="41404-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="41404-124">Nastavte jednotkovou cenu na 10000.</span><span class="sxs-lookup"><span data-stu-id="41404-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="41404-125">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="41404-125">Click Financials.</span></span>
6. <span data-ttu-id="41404-126">Klikněte na možnost Distribuovat částky.</span><span class="sxs-lookup"><span data-stu-id="41404-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="41404-127">Do pole Účet hlavní knihy zadejte hodnotu 601300-001-023--.</span><span class="sxs-lookup"><span data-stu-id="41404-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="41404-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="41404-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="41404-129">Provést kontrolu rozpočtu</span><span class="sxs-lookup"><span data-stu-id="41404-129">Perform budget checking</span></span>
1. <span data-ttu-id="41404-130">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="41404-130">Click Financials.</span></span>
2. <span data-ttu-id="41404-131">Klikněte na Provést kontrolu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="41404-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="41404-132">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="41404-132">Click Financials.</span></span>
4. <span data-ttu-id="41404-133">Klikněte na Zobrazit chyby a varování kontroly rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="41404-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="41404-134">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="41404-134">Click Close.</span></span>


