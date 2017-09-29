---
title: "Rozdělení období do periodických deníků"
description: "Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku. Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce. Můžete také určit počet období, pro které bude deník účtován."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9b07d2c274d3e4818ffd917a730aeba3e5dff76c
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="split-periods-in-periodic-journals"></a><span data-ttu-id="97a77-105">Rozdělení období do periodických deníků</span><span class="sxs-lookup"><span data-stu-id="97a77-105">Split periods in periodic journals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="97a77-106">Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="97a77-106">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the journal is posted.</span></span> <span data-ttu-id="97a77-107">Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce.</span><span class="sxs-lookup"><span data-stu-id="97a77-107">When you create the journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="97a77-108">Můžete také určit počet období, pro které bude deník účtován.</span><span class="sxs-lookup"><span data-stu-id="97a77-108">You also specify the number of periods for which the journal will be posted.</span></span>

<span data-ttu-id="97a77-109">Pro opakované načtení a zaúčtování řádků transakcí můžete použít stránku **Periodické deníky**.</span><span class="sxs-lookup"><span data-stu-id="97a77-109">To repeatedly retrieve and post transaction lines, you can use the **Periodic journals** page.</span></span> <span data-ttu-id="97a77-110">Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku je stránka **Periodické deníky** rozšířena o funkci rozdělení na období.</span><span class="sxs-lookup"><span data-stu-id="97a77-110">For legal entities in Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, and Russia, the **Periodic journals** page is extended by the split for periods functionality.</span></span> <span data-ttu-id="97a77-111">Další informace naleznete v tématu [Zaúčtování periodického deníku](/dynamics365/unified-operations/financials/general-ledger/tasks/post-periodic-journals)</span><span class="sxs-lookup"><span data-stu-id="97a77-111">For more information, see [Post a periodic journal](/dynamics365/unified-operations/financials/general-ledger/tasks/post-periodic-journals)</span></span>

### <a name="example-split-for-periods-in-periodic-journals"></a><span data-ttu-id="97a77-112">Příklad: Rozdělení na období do periodických deníků</span><span class="sxs-lookup"><span data-stu-id="97a77-112">Example: Split for periods in periodic journals</span></span>

<span data-ttu-id="97a77-113">Pojišťovna nabízí organizaci slevu při předplacení pojistného za celý rok.</span><span class="sxs-lookup"><span data-stu-id="97a77-113">An insurance company offers your organization a discount for prepaying the insurance policy for an entire year.</span></span> <span data-ttu-id="97a77-114">Platba je zaúčtována do majetkového účtu, například jako předplatné pojistného.</span><span class="sxs-lookup"><span data-stu-id="97a77-114">The payment is posted to an asset account such as prepaid insurance.</span></span> <span data-ttu-id="97a77-115">Potom umoříte vaše měsíční náklady na pojistné během celého roku vytvořením periodického deníku, který obsahuje kredit na předplaceném účtu pojištění a debet na výdajovém účtu pojištění.</span><span class="sxs-lookup"><span data-stu-id="97a77-115">You then amortize your monthly insurance expense throughout the year by creating a periodic journal that contains a credit to the prepaid insurance account and a debit to an insurance expense account.</span></span> <span data-ttu-id="97a77-116">V takovém případě můžete použít funkci rozdělení na období.</span><span class="sxs-lookup"><span data-stu-id="97a77-116">In this case, you can use the split for periods functionality.</span></span> <span data-ttu-id="97a77-117">Klikněte na tlačítko **Rozdělit mezi období** v podokně akcí na stránce **Řádky periodického****deníku** a potom zadejte následující pole.</span><span class="sxs-lookup"><span data-stu-id="97a77-117">Click the **Split for periods** button on the Action Pane on the **Periodic journal** **lines** page, and then specify the following fields.</span></span>

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a77-118">**Pole**</span><span class="sxs-lookup"><span data-stu-id="97a77-118">**Field**</span></span>             | <span data-ttu-id="97a77-119">**Popis**</span><span class="sxs-lookup"><span data-stu-id="97a77-119">**Description**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="97a77-120">**Počáteční datum**</span><span class="sxs-lookup"><span data-stu-id="97a77-120">**Start date**</span></span>        | <span data-ttu-id="97a77-121">Vyberte datum pro první řádek periodického deníku.</span><span class="sxs-lookup"><span data-stu-id="97a77-121">Select the date for the first periodic journal line.</span></span>                                                                                                                                                        |
| <span data-ttu-id="97a77-122">**Počet období**</span><span class="sxs-lookup"><span data-stu-id="97a77-122">**Number of periods**</span></span> | <span data-ttu-id="97a77-123">Zadejte počet období, napříč kterými má být řádek deníku rozdělen.</span><span class="sxs-lookup"><span data-stu-id="97a77-123">Enter the number of periods across which to split the journal line.</span></span> <span data-ttu-id="97a77-124">Tato hodnota určuje, kolik nových transakcí je generováno.</span><span class="sxs-lookup"><span data-stu-id="97a77-124">This value determines how many new transactions are generated.</span></span> <span data-ttu-id="97a77-125">Částka transakce je rovnoměrně rozložena mezi nové transakce.</span><span class="sxs-lookup"><span data-stu-id="97a77-125">The transaction amount is distributed evenly among the new transactions.</span></span> |
| <span data-ttu-id="97a77-126">**Jednotka**</span><span class="sxs-lookup"><span data-stu-id="97a77-126">**Unit**</span></span>              | <span data-ttu-id="97a77-127">Vyberte měrnou jednotku pro dané období.</span><span class="sxs-lookup"><span data-stu-id="97a77-127">Select the unit of measure for the period.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="97a77-128">**Interval období**</span><span class="sxs-lookup"><span data-stu-id="97a77-128">**Period interval**</span></span>   | <span data-ttu-id="97a77-129">Určete interval mezi účetními obdobími.</span><span class="sxs-lookup"><span data-stu-id="97a77-129">Determine an interval between posting periods.</span></span>                                                                                                                                                              |

<span data-ttu-id="97a77-130">Chcete-li například generovat čtvrtletní zaúčtování, zadejte hodnotu **4** do pole **Počet období**, vyberte možnost **Měsíce** v poli **Jednotka** a zadejte hodnotu **3** do pole **Interval období**.</span><span class="sxs-lookup"><span data-stu-id="97a77-130">For example, to generate quarterly postings, enter **4** in the **Number of periods** field, select **Months** in the **Unit** field, and enter **3** in the **Period interval** field.</span></span> <span data-ttu-id="97a77-131">Systém generuje čtyři řádky deníku, každý pro jednu čtvrtinu částky řádku deníku, který jste zadali ve 3měsíčních intervalech.</span><span class="sxs-lookup"><span data-stu-id="97a77-131">The system generates four journal lines, each for one fourth of the journal line amount that you entered, at 3-month intervals.</span></span> <span data-ttu-id="97a77-132">Podobná funkce je také k dispozici pro hlavní deník.</span><span class="sxs-lookup"><span data-stu-id="97a77-132">Similar functionality is also available for the general journal.</span></span> <span data-ttu-id="97a77-133">Při zobrazení řádků hlavního deníku vyberte **Periodický deník**&gt;**Uložit deník**.</span><span class="sxs-lookup"><span data-stu-id="97a77-133">When viewing general journal lines, select **Period journal** &gt; **Save journal**.</span></span>




