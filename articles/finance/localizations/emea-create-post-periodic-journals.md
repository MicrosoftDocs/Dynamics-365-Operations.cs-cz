---
title: Rozdělení období do periodických deníků
description: Toto téma poskytuje informace o funkci rozdělení období do periodických deníků nebo opakujících se deníků pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšku, Polsku a Rusku.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 976175671ec5ee36f80ba2b2c787a67c18a9b769
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236301"
---
# <a name="split-periods-in-periodic-journals"></a><span data-ttu-id="00226-103">Rozdělení období do periodických deníků</span><span class="sxs-lookup"><span data-stu-id="00226-103">Split periods in periodic journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00226-104">Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="00226-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the journal is posted.</span></span> <span data-ttu-id="00226-105">Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce.</span><span class="sxs-lookup"><span data-stu-id="00226-105">When you create the journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="00226-106">Můžete také určit počet období, pro které bude deník účtován.</span><span class="sxs-lookup"><span data-stu-id="00226-106">You also specify the number of periods for which the journal will be posted.</span></span>

<span data-ttu-id="00226-107">Pro opakované načtení a zaúčtování řádků transakcí můžete použít stránku **Periodické deníky**.</span><span class="sxs-lookup"><span data-stu-id="00226-107">To repeatedly retrieve and post transaction lines, you can use the **Periodic journals** page.</span></span> <span data-ttu-id="00226-108">Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku je stránka **Periodické deníky** rozšířena o funkci rozdělení na období.</span><span class="sxs-lookup"><span data-stu-id="00226-108">For legal entities in Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, and Russia, the **Periodic journals** page is extended by the split for periods functionality.</span></span> <span data-ttu-id="00226-109">Další informace naleznete v tématu [Zaúčtování periodických deníků](../general-ledger/tasks/post-periodic-journals.md)</span><span class="sxs-lookup"><span data-stu-id="00226-109">For more information, see [Post periodic journals](../general-ledger/tasks/post-periodic-journals.md)</span></span>

### <a name="example-split-for-periods-in-periodic-journals"></a><span data-ttu-id="00226-110">Příklad: Rozdělení na období do periodických deníků</span><span class="sxs-lookup"><span data-stu-id="00226-110">Example: Split for periods in periodic journals</span></span>

<span data-ttu-id="00226-111">Pojišťovna nabízí organizaci slevu při předplacení pojistného za celý rok.</span><span class="sxs-lookup"><span data-stu-id="00226-111">An insurance company offers your organization a discount for prepaying the insurance policy for an entire year.</span></span> <span data-ttu-id="00226-112">Platba je zaúčtována do majetkového účtu, například jako předplatné pojistného.</span><span class="sxs-lookup"><span data-stu-id="00226-112">The payment is posted to an asset account such as prepaid insurance.</span></span> <span data-ttu-id="00226-113">Potom umoříte vaše měsíční náklady na pojistné během celého roku vytvořením periodického deníku, který obsahuje kredit na předplaceném účtu pojištění a debet na výdajovém účtu pojištění.</span><span class="sxs-lookup"><span data-stu-id="00226-113">You then amortize your monthly insurance expense throughout the year by creating a periodic journal that contains a credit to the prepaid insurance account and a debit to an insurance expense account.</span></span> <span data-ttu-id="00226-114">V takovém případě můžete použít funkci rozdělení na období.</span><span class="sxs-lookup"><span data-stu-id="00226-114">In this case, you can use the split for periods functionality.</span></span> <span data-ttu-id="00226-115">Klikněte na tlačítko **Rozdělit mezi období** v podokně akcí na stránce **Řádky periodického** **deníku** a potom zadejte následující pole.</span><span class="sxs-lookup"><span data-stu-id="00226-115">Click the **Split for periods** button on the Action Pane on the **Periodic journal** **lines** page, and then specify the following fields.</span></span>


| <span data-ttu-id="00226-116">Pole</span><span class="sxs-lookup"><span data-stu-id="00226-116">Field</span></span>            | <span data-ttu-id="00226-117">Popis</span><span class="sxs-lookup"><span data-stu-id="00226-117">Description</span></span>                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------|
| <span data-ttu-id="00226-118">**Počáteční datum**</span><span class="sxs-lookup"><span data-stu-id="00226-118">**Start date**</span></span>        | <span data-ttu-id="00226-119">Vyberte datum pro první řádek periodického deníku.</span><span class="sxs-lookup"><span data-stu-id="00226-119">Select the date for the first periodic journal line.</span></span>                                                                                                                                                        |
| <span data-ttu-id="00226-120">**Počet období**</span><span class="sxs-lookup"><span data-stu-id="00226-120">**Number of periods**</span></span> | <span data-ttu-id="00226-121">Zadejte počet období, napříč kterými má být řádek deníku rozdělen.</span><span class="sxs-lookup"><span data-stu-id="00226-121">Enter the number of periods across which to split the journal line.</span></span> <span data-ttu-id="00226-122">Tato hodnota určuje, kolik nových transakcí je generováno.</span><span class="sxs-lookup"><span data-stu-id="00226-122">This value determines how many new transactions are generated.</span></span> <span data-ttu-id="00226-123">Částka transakce je rovnoměrně rozložena mezi nové transakce.</span><span class="sxs-lookup"><span data-stu-id="00226-123">The transaction amount is distributed evenly among the new transactions.</span></span> |
| <span data-ttu-id="00226-124">**Jednotka**</span><span class="sxs-lookup"><span data-stu-id="00226-124">**Unit**</span></span>              | <span data-ttu-id="00226-125">Vyberte měrnou jednotku pro dané období.</span><span class="sxs-lookup"><span data-stu-id="00226-125">Select the unit of measure for the period.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="00226-126">**Interval období**</span><span class="sxs-lookup"><span data-stu-id="00226-126">**Period interval**</span></span>   | <span data-ttu-id="00226-127">Určete interval mezi účetními obdobími.</span><span class="sxs-lookup"><span data-stu-id="00226-127">Determine an interval between posting periods.</span></span>                                                                                                                                                              |

<span data-ttu-id="00226-128">Chcete-li například generovat čtvrtletní zaúčtování, zadejte hodnotu **4** do pole **Počet období**, vyberte možnost **Měsíce** v poli **Jednotka** a zadejte hodnotu **3** do pole **Interval období**.</span><span class="sxs-lookup"><span data-stu-id="00226-128">For example, to generate quarterly postings, enter **4** in the **Number of periods** field, select **Months** in the **Unit** field, and enter **3** in the **Period interval** field.</span></span> <span data-ttu-id="00226-129">Systém generuje čtyři řádky deníku, každý pro jednu čtvrtinu částky řádku deníku, který jste zadali ve 3měsíčních intervalech.</span><span class="sxs-lookup"><span data-stu-id="00226-129">The system generates four journal lines, each for one fourth of the journal line amount that you entered, at 3-month intervals.</span></span> <span data-ttu-id="00226-130">Podobná funkce je také k dispozici pro hlavní deník.</span><span class="sxs-lookup"><span data-stu-id="00226-130">Similar functionality is also available for the general journal.</span></span> <span data-ttu-id="00226-131">Při zobrazení řádků hlavního deníku vyberte **Periodický deník**&gt;**Uložit deník**.</span><span class="sxs-lookup"><span data-stu-id="00226-131">When viewing general journal lines, select **Period journal** &gt; **Save journal**.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]