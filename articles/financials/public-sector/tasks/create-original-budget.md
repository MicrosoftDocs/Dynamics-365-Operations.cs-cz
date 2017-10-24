--- 
title: "Vytvoření původního rozpočtu a stornování předběžných položek rozpočtu ve veřejném sektoru"
description: "Pokud vytvoříte původní položku rozpočtu a použijete hodnoty rozpočtových modelů a dimenzí, které obsahují předběžné částky rozpočtu, předběžné částky rozpočtu lze stornovat."
author: twheeloc
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2f50cc6bf8ec533db677d290c52dbd711d7a1de8
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-original-budget-and-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="7cf72-103">Vytvoření původního rozpočtu a stornování předběžných položek rozpočtu ve veřejném sektoru</span><span class="sxs-lookup"><span data-stu-id="7cf72-103">Create an original budget and reverse preliminary budget entries in the public sector</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7cf72-104">Pokud vytvoříte původní položku rozpočtu a použijete hodnoty rozpočtových modelů a dimenzí, které obsahují předběžné částky rozpočtu, předběžné částky rozpočtu lze stornovat.</span><span class="sxs-lookup"><span data-stu-id="7cf72-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="7cf72-105">Tato procedura byla vytvořena pomocí ukázkových dat společnosti PSUS v oddílu veřejného sektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf72-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="7cf72-106">Přejděte na Rozpočtování > Položky registru rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="7cf72-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="7cf72-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7cf72-107">Click New.</span></span>
3. <span data-ttu-id="7cf72-108">V poli Rozpočtový model kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7cf72-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7cf72-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7cf72-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7cf72-110">V poli Kód rozpočtu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7cf72-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7cf72-111">Klikněte na možnost Původní rozpočet na seznamu.</span><span class="sxs-lookup"><span data-stu-id="7cf72-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="7cf72-112">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="7cf72-112">Click Save.</span></span>
8. <span data-ttu-id="7cf72-113">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="7cf72-113">Click Add line.</span></span>
9. <span data-ttu-id="7cf72-114">Volitelné: Pokud chcete změnit datum na jiné, než je datum v záhlaví, zadejte nové datum.</span><span class="sxs-lookup"><span data-stu-id="7cf72-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="7cf72-115">Toto datum určuje fiskální období, pro které je zaznamenán rozpočet.</span><span class="sxs-lookup"><span data-stu-id="7cf72-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="7cf72-116">V poli Účetní struktura klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7cf72-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7cf72-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7cf72-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7cf72-118">Zadejte požadované hodnoty do pole Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="7cf72-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="7cf72-119">Zadejte číslo do pole Částka.</span><span class="sxs-lookup"><span data-stu-id="7cf72-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="7cf72-120">V poli Měna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7cf72-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="7cf72-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7cf72-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="7cf72-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7cf72-122">Click Save.</span></span>
17. <span data-ttu-id="7cf72-123">Klikněte na možnost Aktualizovat zůstatky rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="7cf72-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="7cf72-124">Volitelné: Můžete vybrat možnost Stornovat předběžný rozpočet.</span><span class="sxs-lookup"><span data-stu-id="7cf72-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="7cf72-125">Poznámka: Stornovat můžete všechny předběžné položky rozpočtu, nebo pouze předběžné položky rozpočtu, které mají vámi zadaný kód rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="7cf72-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="7cf72-126">Chcete-li provádět volitelné výběry, klikněte na ikonu Odemknout v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="7cf72-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="7cf72-127">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="7cf72-127">Click Update.</span></span>


