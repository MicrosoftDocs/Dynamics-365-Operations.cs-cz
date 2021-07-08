---
title: Nejčastější dotazy k finančnímu výkaznictví
description: Toto téma poskytuje odpovědi na nejčastější dotazy týkající se finančního výkaznictví.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266626"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="8516e-103">Nejčastější dotazy k finančnímu výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8516e-103">Financial reporting FAQ</span></span>

<span data-ttu-id="8516e-104">Toto téma poskytuje odpovědi na nejčastější dotazy týkající se finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8516e-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="8516e-105">Jak omezím přístup k sestavě pomocí zabezpečení stromu?</span><span class="sxs-lookup"><span data-stu-id="8516e-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="8516e-106">Následující příklad ukazuje, jak omezit přístup k sestavě pomocí zabezpečení stromu.</span><span class="sxs-lookup"><span data-stu-id="8516e-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="8516e-107">Ukázková společnost USMF má sestavu **rozvahy**, ke které by neměli mít přístup všichni uživatelé finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8516e-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="8516e-108">Zabezpečení stromu můžete použít k omezení přístupu k jedné sestavě, aby k ní měl přístup pouze konkrétní uživatel.</span><span class="sxs-lookup"><span data-stu-id="8516e-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="8516e-109">Přihlaste se do Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="8516e-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="8516e-110">Vyberte **Soubor \> Nový \> Definice stromu** pro vytvoření definice nového stromu.</span><span class="sxs-lookup"><span data-stu-id="8516e-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="8516e-111">Dvakrát klikněte (nebo dvakrát klepněte) na řádek **Souhrn** ve sloupci **Zabezpečení jednotky**.</span><span class="sxs-lookup"><span data-stu-id="8516e-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="8516e-112">Zvolte **Uživatelé a skupiny**.</span><span class="sxs-lookup"><span data-stu-id="8516e-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="8516e-113">Vyberte uživatele nebo skupiny vyžadující přístup k této sestavě.</span><span class="sxs-lookup"><span data-stu-id="8516e-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="8516e-114">Zvolte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8516e-114">Select **Save**.</span></span>
7. <span data-ttu-id="8516e-115">V definici sestavy přidejte svou novou definici stromu.</span><span class="sxs-lookup"><span data-stu-id="8516e-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="8516e-116">V definici stromu vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8516e-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="8516e-117">Poté v možnosti **Výběr organizační jednotky** vyberte **Zahrnout všechny jednotky**.</span><span class="sxs-lookup"><span data-stu-id="8516e-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="8516e-118">Jak zjistím, které účty neodpovídají mým zůstatkům?</span><span class="sxs-lookup"><span data-stu-id="8516e-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="8516e-119">Pokud máte sestavu, který nemá odpovídající zůstatky, použijte k identifikaci každého účtu a odchylky následující postupy.</span><span class="sxs-lookup"><span data-stu-id="8516e-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="8516e-120">V Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="8516e-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="8516e-121">Vytvořte novou definici řádku.</span><span class="sxs-lookup"><span data-stu-id="8516e-121">Create a new row definition.</span></span>
2. <span data-ttu-id="8516e-122">Zvolte **Upravit \> Vložit řádky z dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="8516e-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="8516e-123">Vyberte **Hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="8516e-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="8516e-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8516e-124">Select **OK**.</span></span>
5. <span data-ttu-id="8516e-125">Uložte definici řádku.</span><span class="sxs-lookup"><span data-stu-id="8516e-125">Save the row definition.</span></span>
6. <span data-ttu-id="8516e-126">Vytvořte novou definici sloupce.</span><span class="sxs-lookup"><span data-stu-id="8516e-126">Create a new column definition.</span></span>
7. <span data-ttu-id="8516e-127">Vytvořte novou definici sestavy.</span><span class="sxs-lookup"><span data-stu-id="8516e-127">Create a new report definition.</span></span>
8. <span data-ttu-id="8516e-128">Vyberte **Nastavení** a zrušte označení této možnosti.</span><span class="sxs-lookup"><span data-stu-id="8516e-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="8516e-129">Vygenerujte sestavu.</span><span class="sxs-lookup"><span data-stu-id="8516e-129">Generate the report.</span></span> 
10. <span data-ttu-id="8516e-130">Exportujte sestavu do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8516e-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="8516e-131">V Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8516e-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="8516e-132">Přejděte na **Hlavní kniha \> Dotazy a sestavy \> Předvaha**.</span><span class="sxs-lookup"><span data-stu-id="8516e-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="8516e-133">Nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="8516e-133">Set the following fields:</span></span>

    - <span data-ttu-id="8516e-134">**Od data** – Zadejte počáteční datum fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="8516e-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="8516e-135">**Do data** – Zadejte datum, pro které generujete sestavu.</span><span class="sxs-lookup"><span data-stu-id="8516e-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="8516e-136">**Finanční dimenze** – Nastavte toto pole na **Hlavní účet nastaven**.</span><span class="sxs-lookup"><span data-stu-id="8516e-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="8516e-137">Vyberte **Vypočítat**.</span><span class="sxs-lookup"><span data-stu-id="8516e-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="8516e-138">Exportujte sestavu do aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="8516e-138">Export the report to Excel.</span></span>

<span data-ttu-id="8516e-139">Nyní byste měli být schopni zkopírovat data ze sestavy Excelu Financial Reporter do sestavy **Předvahy** a porovnat sloupce **Konečný zůstatek**.</span><span class="sxs-lookup"><span data-stu-id="8516e-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="8516e-140">Když navrhuji sestavu v aplikaci Report Designer nebo když generuji finanční sestavu, obdržel jsem následující zprávu: „Operaci nelze dokončit kvůli problému v rámci poskytovatele dat.“</span><span class="sxs-lookup"><span data-stu-id="8516e-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="8516e-141">Jak mám reagovat?</span><span class="sxs-lookup"><span data-stu-id="8516e-141">How should I respond?</span></span>

<span data-ttu-id="8516e-142">Zpráva označuje, že došlo k problému, když se systém pokusil načíst finanční metadata z datového tržiště během vašeho používání finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8516e-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="8516e-143">Na tento problém lze odpovědět dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="8516e-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="8516e-144">Zkontrolujte stav integrace dat přechodem na **Nástroje \> Stav integrace** v aplikaci Report Designer.</span><span class="sxs-lookup"><span data-stu-id="8516e-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="8516e-145">Pokud je integrace neúplná, počkejte na její dokončení.</span><span class="sxs-lookup"><span data-stu-id="8516e-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="8516e-146">Až dostanete zprávu, vraťte se ke své předchozí činnosti.</span><span class="sxs-lookup"><span data-stu-id="8516e-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="8516e-147">Kontaktujte podporu, abyste problém identifikovali a vyřešili ho.</span><span class="sxs-lookup"><span data-stu-id="8516e-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="8516e-148">V systému mohou být nekonzistentní data.</span><span class="sxs-lookup"><span data-stu-id="8516e-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="8516e-149">Technici podpory vám mohou pomoci identifikovat tento problém na serveru a najít konkrétní data, která mohou vyžadovat aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="8516e-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
