---
title: Používání programů trvání
description: Tento postup vás provede prodejem programu trvání a zpracováním souvisejících prodejních objednávek.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b641fb6ba5edf359a2f1f2de7b5095d73b497cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003621"
---
# <a name="using-continuity-program"></a><span data-ttu-id="180e3-103">Používání programů trvání</span><span class="sxs-lookup"><span data-stu-id="180e3-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="180e3-104">Tento postup vás provede prodejem programu trvání a zpracováním souvisejících prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="180e3-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="180e3-105">Aby bylo možné tuto proceduru dokončit, musí být uživatel nastaven jako uživatel kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="180e3-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="180e3-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="180e3-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="180e3-107">Přejděte na Maloobchodní a velkoobchodní prodej > Odběratelé > Služby odběratele.</span><span class="sxs-lookup"><span data-stu-id="180e3-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="180e3-108">Do pole SearchText zadejte Karen a pak stiskněte klávesu Tab.</span><span class="sxs-lookup"><span data-stu-id="180e3-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="180e3-109">Mělo by se otevřít překryvné dialogové okno Rozšířené hledání.</span><span class="sxs-lookup"><span data-stu-id="180e3-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="180e3-110">Pokud tomu tak není, klepněte na tlačítko Hledat vpravo od tohoto pole.</span><span class="sxs-lookup"><span data-stu-id="180e3-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="180e3-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="180e3-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="180e3-112">Měla by existovat pouze jeden řádek se zobrazením Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="180e3-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="180e3-113">Vyberte řádek klepnutím na znak zaškrtnutí zcela vlevo v mřížce.</span><span class="sxs-lookup"><span data-stu-id="180e3-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="180e3-114">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="180e3-114">Click Select.</span></span>
5. <span data-ttu-id="180e3-115">Klepněte na položky Nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="180e3-115">Click New sales order.</span></span>
    * <span data-ttu-id="180e3-116">Je vhodné poznamenat si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="180e3-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="180e3-117">Budete je potřebovat později v této proceduře.</span><span class="sxs-lookup"><span data-stu-id="180e3-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="180e3-118">Do pole Číslo položky zadejte '88000' a pak stiskněte klávesu Tab.</span><span class="sxs-lookup"><span data-stu-id="180e3-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="180e3-119">Toto je trvalé zboží v demo datech USRT.</span><span class="sxs-lookup"><span data-stu-id="180e3-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="180e3-120">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="180e3-120">Click Complete.</span></span>
8. <span data-ttu-id="180e3-121">Do pole Způsob platby zadejte 'Visa'.</span><span class="sxs-lookup"><span data-stu-id="180e3-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="180e3-122">Klikněte na Přidat kreditní kartu.</span><span class="sxs-lookup"><span data-stu-id="180e3-122">Click Add credit card.</span></span>
    * <span data-ttu-id="180e3-123">Na této stránce zadejte požadované informace o platební kartě.</span><span class="sxs-lookup"><span data-stu-id="180e3-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="180e3-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="180e3-124">Click OK.</span></span>
11. <span data-ttu-id="180e3-125">Rozbalte sekci Platba.</span><span class="sxs-lookup"><span data-stu-id="180e3-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="180e3-126">Pro objednávku musí být zadány platby, aby bylo možné odeslat objednávku do kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="180e3-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="180e3-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="180e3-127">Click OK.</span></span>
13. <span data-ttu-id="180e3-128">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="180e3-128">Click Submit.</span></span>
    * <span data-ttu-id="180e3-129">Teď máte vytvořenou novou trvalou objednávku.</span><span class="sxs-lookup"><span data-stu-id="180e3-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="180e3-130">Potom spustíte dvě výrobní dávky, které slouží ke zpracování trvalých objednávek.</span><span class="sxs-lookup"><span data-stu-id="180e3-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="180e3-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="180e3-131">Close the page.</span></span>
15. <span data-ttu-id="180e3-132">Přejděte na Maloobchodní a velkoobchodní prodej > Trvání > Zpracovat trvalé platby.</span><span class="sxs-lookup"><span data-stu-id="180e3-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="180e3-133">V poli Položka trvání zadejte "88000" a potom stiskněte klávesu Tab.</span><span class="sxs-lookup"><span data-stu-id="180e3-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="180e3-134">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="180e3-134">Click OK.</span></span>
18. <span data-ttu-id="180e3-135">Přejděte na Maloobchodní a velkoobchodní prodej > Trvání > Vytvořit trvalé podřízené objednávky.</span><span class="sxs-lookup"><span data-stu-id="180e3-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="180e3-136">Tento proces vytvoří nové prodejní objednávky na základě nastavení programů trvání.</span><span class="sxs-lookup"><span data-stu-id="180e3-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="180e3-137">V poli Položka trvání zadejte "88000" a potom stiskněte klávesu Tab.</span><span class="sxs-lookup"><span data-stu-id="180e3-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="180e3-138">Zboží '88000 je trvalé zboží v ukázkových datech USRT.</span><span class="sxs-lookup"><span data-stu-id="180e3-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="180e3-139">V poli Prodejní objednávka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="180e3-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="180e3-140">Zadejte číslo prodejní objednávky, které jste si poznamenali dříve v proceduře.</span><span class="sxs-lookup"><span data-stu-id="180e3-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="180e3-141">Tím zachováte dobu zpracování pro tuto proceduru jako minimální.</span><span class="sxs-lookup"><span data-stu-id="180e3-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="180e3-142">Pole Prodejní objednávka je volitelné – můžete zpracovat všechny objednávky pro jakýkoli program.</span><span class="sxs-lookup"><span data-stu-id="180e3-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="180e3-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="180e3-143">Click OK.</span></span>

