---
title: " Definování plánů trvání"
description: Toto téma vás provede nastavením programu trvání (označovaném také jako opakované objednávky).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06fd1e23ad84fdc5e94e309717d5a96fbff45035
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410828"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="b225d-103"> Definování plánů trvání</span><span class="sxs-lookup"><span data-stu-id="b225d-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b225d-104">Toto téma vás provede nastavením programu trvání (označovaném také jako opakované objednávky).</span><span class="sxs-lookup"><span data-stu-id="b225d-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="b225d-105">Toto téma používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="b225d-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="b225d-106">Vytvoření programu trvání</span><span class="sxs-lookup"><span data-stu-id="b225d-106">Create continuity program</span></span>
1. <span data-ttu-id="b225d-107">Přejděte na Retail and Commerce > Trvání > Programy trvání.</span><span class="sxs-lookup"><span data-stu-id="b225d-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="b225d-108">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="b225d-108">Click New.</span></span>
3. <span data-ttu-id="b225d-109">V poli ID plánu zadejte ID plánu trvání</span><span class="sxs-lookup"><span data-stu-id="b225d-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="b225d-110">V poli zahájení objednávky vyberte "První událost".</span><span class="sxs-lookup"><span data-stu-id="b225d-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="b225d-111">Jestliže odběratel zadá novou objednávku pro program kontinuity, existují dvě možnosti, pro které bude výrobek expedován: 1.</span><span class="sxs-lookup"><span data-stu-id="b225d-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="b225d-112">První událost: první produkt v programu kontinuity bude expedován.</span><span class="sxs-lookup"><span data-stu-id="b225d-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="b225d-113">2.</span><span class="sxs-lookup"><span data-stu-id="b225d-113">2.</span></span> <span data-ttu-id="b225d-114">Aktuální událost: bude expedován aktuální produkt.</span><span class="sxs-lookup"><span data-stu-id="b225d-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="b225d-115">Například</span><span class="sxs-lookup"><span data-stu-id="b225d-115">For example.</span></span> <span data-ttu-id="b225d-116">tři měsíce do programu, zákazník obdrží třetí produkt v programu.</span><span class="sxs-lookup"><span data-stu-id="b225d-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="b225d-117">Vyberte možnost "Ano" u výzvy k zadání počátečního data objednávky.</span><span class="sxs-lookup"><span data-stu-id="b225d-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="b225d-118">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="b225d-118">Click Add line.</span></span>
7. <span data-ttu-id="b225d-119">V poli Číslo zboží zadejte číslo zboží pro první produkt (0013).</span><span class="sxs-lookup"><span data-stu-id="b225d-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="b225d-120">Napište "CP".</span><span class="sxs-lookup"><span data-stu-id="b225d-120">Type 'CP'.</span></span>
9. <span data-ttu-id="b225d-121">Zadejte datum, kdy bude možné první produkt objednat.</span><span class="sxs-lookup"><span data-stu-id="b225d-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="b225d-122">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="b225d-122">Click Add line.</span></span>
11. <span data-ttu-id="b225d-123">Do pole Číslo zboží zadejte „0014“.</span><span class="sxs-lookup"><span data-stu-id="b225d-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="b225d-124">V poli kód intervalu data vymažte hodnotu, aby bylo prázdné.</span><span class="sxs-lookup"><span data-stu-id="b225d-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="b225d-125">Vymažte pro tuto proceduru datový interval.</span><span class="sxs-lookup"><span data-stu-id="b225d-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="b225d-126">Datum bude postupně narůstat od počátečního data první položky.</span><span class="sxs-lookup"><span data-stu-id="b225d-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="b225d-127">Sem zadáte interval, ve kterém budou dodávány produkty.</span><span class="sxs-lookup"><span data-stu-id="b225d-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="b225d-128">Napište 30.</span><span class="sxs-lookup"><span data-stu-id="b225d-128">Type '30'.</span></span>
    * <span data-ttu-id="b225d-129">Pro měsíční program zadejte interval 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="b225d-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="b225d-130">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="b225d-130">Click Add line.</span></span>
15. <span data-ttu-id="b225d-131">Do pole Číslo zboží zadejte „0015“.</span><span class="sxs-lookup"><span data-stu-id="b225d-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="b225d-132">Napište 'Konec'.</span><span class="sxs-lookup"><span data-stu-id="b225d-132">Type 'End'.</span></span>
17. <span data-ttu-id="b225d-133">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b225d-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="b225d-134">Přiřazení k trvalému zboží</span><span class="sxs-lookup"><span data-stu-id="b225d-134">Assign to continuity item</span></span>
1. <span data-ttu-id="b225d-135">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="b225d-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b225d-136">Vyberte zboží '0016'.</span><span class="sxs-lookup"><span data-stu-id="b225d-136">Select item '0016'.</span></span>
    * <span data-ttu-id="b225d-137">Pro tuto proceduru vyberte číslo položky 0016.</span><span class="sxs-lookup"><span data-stu-id="b225d-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="b225d-138">Za normálních okolností budete mít vytvořený uvolněný produkt, který má aplikovanou další trvalou obchodní logiku při umístění do prodejní objednávky v kontaktním středisku.</span><span class="sxs-lookup"><span data-stu-id="b225d-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="b225d-139">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b225d-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b225d-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="b225d-140">Click Edit.</span></span>
5. <span data-ttu-id="b225d-141">Rozbalte nebo sbalte oddíl Prodej.</span><span class="sxs-lookup"><span data-stu-id="b225d-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="b225d-142">Sem zadejte program trvání, který tato položka představuje.</span><span class="sxs-lookup"><span data-stu-id="b225d-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="b225d-143">Zadejte kód plánu, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="b225d-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="b225d-144">Když je prostřednictvím kontaktního střediska prodáno zboží, z vybraného programu trvání se aplikuje další obchodní logika.</span><span class="sxs-lookup"><span data-stu-id="b225d-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="b225d-145">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b225d-145">Click Save.</span></span>

