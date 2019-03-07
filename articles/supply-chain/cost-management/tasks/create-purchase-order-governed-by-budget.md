---
title: Vytvoření nákupní objednávky řízené rozpočtem
description: Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82e40d67547f5932a4805f2580e8c9f58def284
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "366528"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="c1c6a-103">Vytvoření nákupní objednávky řízené rozpočtem</span><span class="sxs-lookup"><span data-stu-id="c1c6a-103">Create a purchase order governed by budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1c6a-104">Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="c1c6a-105">Tento záznam používá v ukázkových datech společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="c1c6a-106">Zkontrolujte konfiguraci kontroly rozpočtu</span><span class="sxs-lookup"><span data-stu-id="c1c6a-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="c1c6a-107">Přejděte na Rozpočtování > Nastavení > Kontrola rozpočtu > Konfigurace kontroly rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="c1c6a-108">Klikněte na kartu Dostupné rozpočtové prostředky.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="c1c6a-109">Klepněte na kartu Dokumenty a deníky.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="c1c6a-110">Klepněte na kartu Definovat pravidla kontroly rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="c1c6a-111">Klepněte na kartu Definovat rozpočtové skupiny.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="c1c6a-112">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="c1c6a-113">Vytvoření záhlaví nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="c1c6a-113">Create the purchase order header</span></span>
1. <span data-ttu-id="c1c6a-114">Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c1c6a-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-115">Click New.</span></span>
3. <span data-ttu-id="c1c6a-116">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="c1c6a-117">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-117">Expand the General section.</span></span>
5. <span data-ttu-id="c1c6a-118">Do pole Datum účtování nastavte datum 2016-01-01.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="c1c6a-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="c1c6a-120">Přidání řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="c1c6a-120">Add a purchase order line</span></span>
1. <span data-ttu-id="c1c6a-121">V Kategorie zásobování zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="c1c6a-122">Nastavte množství na „2“.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="c1c6a-123">V poli Jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="c1c6a-124">Nastavte jednotkovou cenu na 10000.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="c1c6a-125">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-125">Click Financials.</span></span>
6. <span data-ttu-id="c1c6a-126">Klikněte na možnost Distribuovat částky.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="c1c6a-127">Do pole Účet hlavní knihy zadejte hodnotu 601300-001-023--.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="c1c6a-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="c1c6a-129">Provést kontrolu rozpočtu</span><span class="sxs-lookup"><span data-stu-id="c1c6a-129">Perform budget checking</span></span>
1. <span data-ttu-id="c1c6a-130">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-130">Click Financials.</span></span>
2. <span data-ttu-id="c1c6a-131">Klikněte na Provést kontrolu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="c1c6a-132">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-132">Click Financials.</span></span>
4. <span data-ttu-id="c1c6a-133">Klikněte na Zobrazit chyby a varování kontroly rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="c1c6a-134">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="c1c6a-134">Click Close.</span></span>

