---
title: Vytvoření předběžného rozpočtu pro veřejný sektor
description: Můžete vytvořit předběžné položky registru rozpočtu pro určitý rozpočtový model a hodnoty dimenze.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40371809f3855e57db4bc12f5466f7cef5cec600
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235549"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="02619-103">Vytvoření předběžného rozpočtu pro veřejný sektor</span><span class="sxs-lookup"><span data-stu-id="02619-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02619-104">Můžete vytvořit předběžné položky registru rozpočtu pro určitý rozpočtový model a hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="02619-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="02619-105">Po schválení aktuálního rozpočtu můžete vytvořit původní položky registru rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="02619-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="02619-106">Tato procedura byla vytvořena pomocí ukázkových dat společnosti PSUS v oddílu veřejného sektoru.</span><span class="sxs-lookup"><span data-stu-id="02619-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="02619-107">Přejděte na Rozpočtování > Položky registru rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="02619-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="02619-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="02619-108">Click New.</span></span>
3. <span data-ttu-id="02619-109">V poli Rozpočtový model kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="02619-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="02619-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="02619-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="02619-111">V poli Kód rozpočtu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="02619-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="02619-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="02619-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="02619-113">V poli Kód důvodu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="02619-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="02619-114">Klikněte na seznamu na tlačítko požadovaných záznamů.</span><span class="sxs-lookup"><span data-stu-id="02619-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="02619-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="02619-115">Click Save.</span></span>
10. <span data-ttu-id="02619-116">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="02619-116">Click Add line.</span></span>
    * <span data-ttu-id="02619-117">Volitelné: Pokud chcete změnit datum na jiné, než je datum v záhlaví, zadejte nové datum.</span><span class="sxs-lookup"><span data-stu-id="02619-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="02619-118">Toto datum určuje fiskální období, pro které je zaznamenán rozpočet.</span><span class="sxs-lookup"><span data-stu-id="02619-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="02619-119">Pokud při zobrazování úloh průvodce chcete vyplnit ostatní pole, klikněte v horní části stránky na položku Odemknout.</span><span class="sxs-lookup"><span data-stu-id="02619-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="02619-120">V poli Účetní struktura klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="02619-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="02619-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="02619-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="02619-122">Zadejte požadované hodnoty do pole Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="02619-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="02619-123">Zadejte číslo do pole Částka.</span><span class="sxs-lookup"><span data-stu-id="02619-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="02619-124">Můžete také zadat typ částky.</span><span class="sxs-lookup"><span data-stu-id="02619-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="02619-125">V poli Měna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="02619-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="02619-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="02619-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="02619-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="02619-127">Click Save.</span></span>
18. <span data-ttu-id="02619-128">Klikněte na možnost Aktualizovat zůstatky rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="02619-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="02619-129">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="02619-129">Click Update.</span></span>
    * <span data-ttu-id="02619-130">Výsledky aktualizace zobrazíte kliknutím na možnost Podrobnosti zprávy na modrém panelu.</span><span class="sxs-lookup"><span data-stu-id="02619-130">To see the results of the update, click Message details on the blue bar.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]