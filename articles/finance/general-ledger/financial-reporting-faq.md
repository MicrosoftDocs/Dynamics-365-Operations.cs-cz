---
title: Nejčastější dotazy k finančnímu výkaznictví
description: Toto téma se zabývá dotazy uživatelů ohledně finančního výkaznictví.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923018"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="8968e-103">Nejčastější dotazy k finančnímu výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8968e-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="8968e-104">Toto téma poskytuje odpovědi na nejčastější dotazy týkající se finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8968e-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="8968e-105">Jak omezím přístup k sestavě pomocí zabezpečení stromu?</span><span class="sxs-lookup"><span data-stu-id="8968e-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="8968e-106">Následující příklad ukazuje, jak omezit přístup k sestavě pomocí zabezpečení stromu.</span><span class="sxs-lookup"><span data-stu-id="8968e-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="8968e-107">Ukázková společnost USMF má sestavu rozvahy, ke které by neměli mít přístup všichni uživatelé finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8968e-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="8968e-108">Pro omezení přístupu můžete pomocí zabezpečení stromu omezit přístup některých uživatelů k sestavě.</span><span class="sxs-lookup"><span data-stu-id="8968e-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="8968e-109">Chcete-li omezit přístup, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8968e-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="8968e-110">Přihlaste se do aplikace Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="8968e-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="8968e-111">Vytvořte novou definici stromu.</span><span class="sxs-lookup"><span data-stu-id="8968e-111">Create a new tree definition.</span></span> <span data-ttu-id="8968e-112">Přejděte na **Soubor > Nový > Definice stromu**.</span><span class="sxs-lookup"><span data-stu-id="8968e-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="8968e-113">Ve sloupci **Zabezpečení jednotky** poklepejte na řádek **Souhrn**.</span><span class="sxs-lookup"><span data-stu-id="8968e-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="8968e-114">Zvolte **Uživatelé a skupiny**.</span><span class="sxs-lookup"><span data-stu-id="8968e-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="8968e-115">Vyberte uživatele nebo skupiny, které mají mít přístup k této sestavě.</span><span class="sxs-lookup"><span data-stu-id="8968e-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="8968e-116">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8968e-116">Select **Save**.</span></span>
7. <span data-ttu-id="8968e-117">V definici sestavy přidejte svou novou definici stromu.</span><span class="sxs-lookup"><span data-stu-id="8968e-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="8968e-118">V definici stromu vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8968e-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="8968e-119">V možnosti **Výběr organizační jednotky** vyberte **Zahrnout všechny jednotky**.</span><span class="sxs-lookup"><span data-stu-id="8968e-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="8968e-120">Jak zjistím, které účty neodpovídají mým zůstatkům?</span><span class="sxs-lookup"><span data-stu-id="8968e-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="8968e-121">Pokud máte sestavu, který nemá odpovídající zůstatky, je zde několik kroků, které můžete podniknout k identifikaci každého z účtů a odchylek.</span><span class="sxs-lookup"><span data-stu-id="8968e-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="8968e-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="8968e-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="8968e-123">V aplikaci Financial Reporter Report Designer vytvořte novou definici řádku.</span><span class="sxs-lookup"><span data-stu-id="8968e-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="8968e-124">Zvolte **Upravit > Vložit řádky z dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="8968e-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="8968e-125">Vyberte **Hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="8968e-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="8968e-126">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8968e-126">Select **OK**.</span></span>
5. <span data-ttu-id="8968e-127">Uložte definici řádku.</span><span class="sxs-lookup"><span data-stu-id="8968e-127">Save the row definition.</span></span>
6. <span data-ttu-id="8968e-128">Vytvoření nové definice sloupce</span><span class="sxs-lookup"><span data-stu-id="8968e-128">Create a new column definition</span></span>
7. <span data-ttu-id="8968e-129">Vytvořte novou definici sestavy.</span><span class="sxs-lookup"><span data-stu-id="8968e-129">Create a new report definition.</span></span>
8. <span data-ttu-id="8968e-130">Vyberte **Nastavení** a zrušte označení této možnosti.</span><span class="sxs-lookup"><span data-stu-id="8968e-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="8968e-131">Vygenerujte sestavu.</span><span class="sxs-lookup"><span data-stu-id="8968e-131">Generate the report.</span></span> 
10. <span data-ttu-id="8968e-132">Exportujte sestavu do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8968e-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="8968e-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="8968e-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="8968e-134">V Dynamics 365 Finance, přejděte na **Hlavní kniha > Dotazy a sestavy > Předvaha**.</span><span class="sxs-lookup"><span data-stu-id="8968e-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="8968e-135">Nastavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="8968e-135">Set the following parameters:</span></span>
   - <span data-ttu-id="8968e-136">**Od data** - Zadejte začátek fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="8968e-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="8968e-137">**Do data** - Zadejte datum, pro které generujete sestavu.</span><span class="sxs-lookup"><span data-stu-id="8968e-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="8968e-138">**Finanční dimenze** - Nastavte toto pole na **Hlavní účet nastaven**.</span><span class="sxs-lookup"><span data-stu-id="8968e-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="8968e-139">Vyberte **Vypočítat**.</span><span class="sxs-lookup"><span data-stu-id="8968e-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="8968e-140">Exportujte sestavu do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8968e-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="8968e-141">Nyní byste měli být schopni zkopírovat data ze sestavy finančního výkaznictví v Excelu a do sestavy předvahy a porovnat sloupce **Konečný zůstatek**.</span><span class="sxs-lookup"><span data-stu-id="8968e-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]