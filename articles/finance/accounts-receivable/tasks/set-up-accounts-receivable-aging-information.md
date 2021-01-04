---
title: Nastavení a generování informací o splatnosti pohledávek
description: Tento průvodce vám pomůže nastavit definici sledování splatnosti, splatné zůstatky odběratelů a zobrazit zůstatky v seznamu Splatný zůstatek a na stránce Kolekce.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439be64a864056cc19fd156f664a4b90601be040
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441176"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="4758f-103">Nastavení a generování informací o splatnosti pohledávek</span><span class="sxs-lookup"><span data-stu-id="4758f-103">Set up and generate accounts receivable aging information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4758f-104">Tento průvodce vám pomůže nastavit definici sledování splatnosti, splatné zůstatky odběratelů a zobrazit zůstatky v seznamu Splatný zůstatek a na stránce Kolekce.</span><span class="sxs-lookup"><span data-stu-id="4758f-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="4758f-105">Tento záznam používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="4758f-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="4758f-106">Vytvoření definice období pro sledování splatnosti</span><span class="sxs-lookup"><span data-stu-id="4758f-106">Create an aging period definition</span></span>
1. <span data-ttu-id="4758f-107">Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Definice období pro sledování splatnosti**.</span><span class="sxs-lookup"><span data-stu-id="4758f-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="4758f-108">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4758f-108">Click **New**.</span></span>
3. <span data-ttu-id="4758f-109">Zadejte hodnotu do pole **Období pro sledování splatnosti**.</span><span class="sxs-lookup"><span data-stu-id="4758f-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="4758f-110">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="4758f-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="4758f-111">Klepnutím na položku **Přidat níže** vložte nové období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="4758f-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="4758f-112">V poli **Období** zadejte popis, který se zobrazí v sestavách pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="4758f-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="4758f-113">Do pole **Jednotka** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4758f-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="4758f-114">Vyberte volbu v poli **Interval**.</span><span class="sxs-lookup"><span data-stu-id="4758f-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="4758f-115">Období hlavní knihy odpovídá období kalendáře hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="4758f-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="4758f-116">Den, týden, měsíc, čtvrtletí a roky definují velikost intervalu podle typu data.</span><span class="sxs-lookup"><span data-stu-id="4758f-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="4758f-117">Hodnota Neomezeno vybere všechny transakce před nebo po předchozím období v závislosti na tom, zda se jedná o první nebo poslední období.</span><span class="sxs-lookup"><span data-stu-id="4758f-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="4758f-118">Vyberte volbu v poli **Indikátor sledování splatnosti**.</span><span class="sxs-lookup"><span data-stu-id="4758f-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="4758f-119">Vyberte období v horní části mřížky.</span><span class="sxs-lookup"><span data-stu-id="4758f-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="4758f-120">Aktualizace popisu popisujícího nejstarší období v definici období pro sledování splatnosti</span><span class="sxs-lookup"><span data-stu-id="4758f-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="4758f-121">V poli **Období** zadejte nový popis pro období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="4758f-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="4758f-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4758f-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="4758f-123">Splatnost zůstatku</span><span class="sxs-lookup"><span data-stu-id="4758f-123">Age the balances</span></span>
1. <span data-ttu-id="4758f-124">Přejděte na **Kredit a inkasa > Pravidelné úlohy > Splatné zůstatky odběratelů**.</span><span class="sxs-lookup"><span data-stu-id="4758f-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="4758f-125">V poli **Definice období pro sledování splatnosti** vyberte definici období pro sledování splatnosti, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="4758f-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="4758f-126">Lze nastavit jeden aktivní snímek pro každou definici období pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="4758f-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="4758f-127">Ve výchozím nastavení se zpracují všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="4758f-127">All customers are processed by default.</span></span> <span data-ttu-id="4758f-128">Tento výběr můžete použít pro výpočet jednoho inkasního fondu zákazníků.</span><span class="sxs-lookup"><span data-stu-id="4758f-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="4758f-129">Vyberte datum z transakce, kterou chcete použít pro sledování splatnosti.</span><span class="sxs-lookup"><span data-stu-id="4758f-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="4758f-130">Vyberte pro sledování splatnosti možnost „k datu“.</span><span class="sxs-lookup"><span data-stu-id="4758f-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="4758f-131">Výchozí hodnota je dnešní, ale při změně tohoto pole na Vybrané datum bude možné vybrat požadované datum.</span><span class="sxs-lookup"><span data-stu-id="4758f-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="4758f-132">Pro dávkové zpracování použijte Dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="4758f-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="4758f-133">Rozbalte rozsah **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="4758f-133">Expand the **Company** range.</span></span> <span data-ttu-id="4758f-134">Můžete vybrat společnosti, které budou zahrnuty do snímku.</span><span class="sxs-lookup"><span data-stu-id="4758f-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="4758f-135">Standardně je vybraná aktuální společnost.</span><span class="sxs-lookup"><span data-stu-id="4758f-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="4758f-136">Klepnutím na tlačítko **Ok** spustíte zpracování snímku.</span><span class="sxs-lookup"><span data-stu-id="4758f-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="4758f-137">Akce bude chvíli trvat. Počkejte, než zmizí posuvník, a zkontrolujte centrum zpráv, zda se vám nedoručila zpráva.</span><span class="sxs-lookup"><span data-stu-id="4758f-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="4758f-138">Prohlédnutí zůstatků na stránce se seznamem Splatné zůstatky a Kolekce</span><span class="sxs-lookup"><span data-stu-id="4758f-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="4758f-139">Přejděte do nabídky **Kredit a inkasa > Inkasa > Splatné zůstatky**.</span><span class="sxs-lookup"><span data-stu-id="4758f-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="4758f-140">Stránka seznamu zobrazí zůstatky pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="4758f-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="4758f-141">Ikona sledování splatnosti zobrazuje období pro sledování splatnosti nejstarší transakce.</span><span class="sxs-lookup"><span data-stu-id="4758f-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="4758f-142">Vyberte odběratele se zůstatkem.</span><span class="sxs-lookup"><span data-stu-id="4758f-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="4758f-143">Rozbalte oblast okna s fakty **Sledování splatnosti** a prohlédněte si splatné zůstatky.</span><span class="sxs-lookup"><span data-stu-id="4758f-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="4758f-144">Definice období pro sledování splatnosti pro okno s fakty je převzata z výchozí definice období pro sledování splatnosti stanovené v parametrech.</span><span class="sxs-lookup"><span data-stu-id="4758f-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="4758f-145">Její změna je možná pomocí nabídky Shromažďovat.</span><span class="sxs-lookup"><span data-stu-id="4758f-145">You can change it using the Collect menu.</span></span>  

