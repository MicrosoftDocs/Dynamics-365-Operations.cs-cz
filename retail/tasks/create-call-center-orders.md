--- 
title: " Vytváření objednávek v kontaktním středisku"
description: "Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 62f88cc2e28405a9d2eb43819fb09d83a64658b6
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="ff942-103"> Vytváření objednávek v kontaktním středisku</span><span class="sxs-lookup"><span data-stu-id="ff942-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ff942-104">Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele.</span><span class="sxs-lookup"><span data-stu-id="ff942-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="ff942-105">Tato procedura používá ukázková data USRT společnosti a je určena pro úředníka prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ff942-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="ff942-106">Předpoklady: Uživatelé provádějící proceduru jsou nastaveni jako uživatelé kontaktního střediska a pololetní katalog společnosti Fabrikam je publikovaném s alespoň jedním zdrojovým kódem.</span><span class="sxs-lookup"><span data-stu-id="ff942-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="ff942-107">Přejděte na Maloobchodní a velkoobchodní prodej > Odběratelé > Služby odběratele.</span><span class="sxs-lookup"><span data-stu-id="ff942-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="ff942-108">V poli SearchText zadejte kritéria vyhledávání pro vyhledávání odběratele.</span><span class="sxs-lookup"><span data-stu-id="ff942-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="ff942-109">Pro tuto vzorovou proceduru zadejte text „karen“ a stiskněte tabulátor.</span><span class="sxs-lookup"><span data-stu-id="ff942-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="ff942-110">Klikněte na Hledat.</span><span class="sxs-lookup"><span data-stu-id="ff942-110">Click Search.</span></span>
    * <span data-ttu-id="ff942-111">Jelikož v ukázkových datech existuje pouze jeden odběratel se jménem Karen, bude výběr proveden automaticky.</span><span class="sxs-lookup"><span data-stu-id="ff942-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="ff942-112">Klepněte na položky Nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="ff942-112">Click New sales order.</span></span>
5. <span data-ttu-id="ff942-113">Rozbalte nebo sbalte oddíl Záhlaví prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ff942-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="ff942-114">Vyberte typ zdrojového kódu pro katalog.</span><span class="sxs-lookup"><span data-stu-id="ff942-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="ff942-115">Pokud neexistují žádné aktivní zdrojové kódy, můžete zavřít pole Zdroj a tento krok vynechat.</span><span class="sxs-lookup"><span data-stu-id="ff942-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="ff942-116">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="ff942-116">Click Add line.</span></span>
8. <span data-ttu-id="ff942-117">Do pole Číslo položky zadejte hledaný výraz položky.</span><span class="sxs-lookup"><span data-stu-id="ff942-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="ff942-118">U této vzorové procedury zadejte číslo dílčí položky „8111“ a stiskněte tabulátor.</span><span class="sxs-lookup"><span data-stu-id="ff942-118">For this sample procedure enter a partial item number of '8111' and press tab.</span></span> <span data-ttu-id="ff942-119">Objeví se místní okno hledání položky.</span><span class="sxs-lookup"><span data-stu-id="ff942-119">This will pop up the item search window.</span></span>  
9. <span data-ttu-id="ff942-120">Vyberte produkt, který chcete přidat do prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="ff942-120">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="ff942-121">Zadejte prodejní množství.</span><span class="sxs-lookup"><span data-stu-id="ff942-121">Enter the sales quantity.</span></span>
11. <span data-ttu-id="ff942-122">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="ff942-122">Click Create.</span></span>
12. <span data-ttu-id="ff942-123">Kliknutím na tlačítko Dokončit zachytíte platbu odběratele.</span><span class="sxs-lookup"><span data-stu-id="ff942-123">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="ff942-124">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="ff942-124">Click Add.</span></span>
    * <span data-ttu-id="ff942-125">Odkaz Přidat se nachází na kartě Platby.</span><span class="sxs-lookup"><span data-stu-id="ff942-125">The Add link is in the Payments tab.</span></span> <span data-ttu-id="ff942-126">Pokud je sbalena karta Platby, rozbalte ji.</span><span class="sxs-lookup"><span data-stu-id="ff942-126">Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="ff942-127">Vyberte způsob platby.</span><span class="sxs-lookup"><span data-stu-id="ff942-127">Select the payment method.</span></span>
    * <span data-ttu-id="ff942-128">V této proceduře vyberte hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="ff942-128">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="ff942-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ff942-129">Close the page.</span></span>
16. <span data-ttu-id="ff942-130">Zadejte částku.</span><span class="sxs-lookup"><span data-stu-id="ff942-130">Enter the amount.</span></span>
    * <span data-ttu-id="ff942-131">V této proceduře zadejte částku odpovídající výši zůstatku objednávky, který lze zobrazit na stránce Souhrn prodejní objednávky vlevo od pole Částka.</span><span class="sxs-lookup"><span data-stu-id="ff942-131">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="ff942-132">Díky tomu budete moci ukončit objednávku jako plně zaplacenou.</span><span class="sxs-lookup"><span data-stu-id="ff942-132">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="ff942-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ff942-133">Click OK.</span></span>
18. <span data-ttu-id="ff942-134">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="ff942-134">Click Submit.</span></span>


