---
title: Nejčastější dotazy k finančnímu výkaznictví
description: Toto téma se zabývá dotazy uživatelů ohledně finančního výkaznictví.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249294"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="2a88d-103">Nejčastější dotazy k finančnímu výkaznictví</span><span class="sxs-lookup"><span data-stu-id="2a88d-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="2a88d-104">Toto téma se zabývá dotazy uživatelů ohledně finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="2a88d-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="2a88d-105">Jak omezím přístup k sestavě pomocí zabezpečení stromu?</span><span class="sxs-lookup"><span data-stu-id="2a88d-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="2a88d-106">Scénář: Ukázková společnost USMF má sestavu rozvahy, která není určena všem uživatelům finančního výkaznictví v D365.</span><span class="sxs-lookup"><span data-stu-id="2a88d-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="2a88d-107">Řešení: Pomocí zabezpečení stromu můžete omezit přístup některých uživatelů k sestavě.</span><span class="sxs-lookup"><span data-stu-id="2a88d-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="2a88d-108">Přihlášení do návrháře finančních sestav</span><span class="sxs-lookup"><span data-stu-id="2a88d-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="2a88d-109">Vytvořte novou definici stromu (Soubor | Nový | Definice stromu). a.</span><span class="sxs-lookup"><span data-stu-id="2a88d-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="2a88d-110">Ve sloupci **Zabezpečení jednotky** poklepejte na řádek **Souhrn**.</span><span class="sxs-lookup"><span data-stu-id="2a88d-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="2a88d-111">i.</span><span class="sxs-lookup"><span data-stu-id="2a88d-111">i.</span></span>    <span data-ttu-id="2a88d-112">Klikněte na možnost Uživatelé a skupiny.</span><span class="sxs-lookup"><span data-stu-id="2a88d-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="2a88d-113">1.    Vyberte uživatele nebo skupinu, která má mít přístup k této sestavě.</span><span class="sxs-lookup"><span data-stu-id="2a88d-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="2a88d-114">[![obrazovka uživatele](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="2a88d-115">[![obrazovka zabezpečení](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="2a88d-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="2a88d-116">b.</span><span class="sxs-lookup"><span data-stu-id="2a88d-116">b.</span></span>    <span data-ttu-id="2a88d-117">Klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2a88d-117">Click **Save**.</span></span>
  
<span data-ttu-id="2a88d-118">[![tlačítko uložit](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="2a88d-119">Do definice sestavy přidejte novou definici stromu.</span><span class="sxs-lookup"><span data-stu-id="2a88d-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="2a88d-120">[![formulář definice stromu](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="2a88d-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="2a88d-121">A.</span><span class="sxs-lookup"><span data-stu-id="2a88d-121">A.</span></span>  <span data-ttu-id="2a88d-122">V definici stromu klikněte na Nastavení a v části „Výběr organizační jednotky“ zaškrtněte „Zahrnout všechny jednotky“.</span><span class="sxs-lookup"><span data-stu-id="2a88d-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="2a88d-123">[![formulář pro výběr organizační jednotky](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="2a88d-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="2a88d-124">**Před:** [![před screenshotem](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="2a88d-125">**Po:** [![po screenshotu](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="2a88d-126">Poznámka: Výše uvedená zpráva se zobrazila, protože po použití zabezpečení jednotky nemá váš uživatel přístup k této sestavě.</span><span class="sxs-lookup"><span data-stu-id="2a88d-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="2a88d-127">Jak zjistím, které účty neodpovídají mým zůstatkům v D365?</span><span class="sxs-lookup"><span data-stu-id="2a88d-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="2a88d-128">Pokud sestava v D365 neodpovídá vašim očekáváním, zde je několik kroků, kterými můžete identifikovat tyto účty a odchylky.</span><span class="sxs-lookup"><span data-stu-id="2a88d-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="2a88d-129">V návrháři finančních sestav:</span><span class="sxs-lookup"><span data-stu-id="2a88d-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="2a88d-130">Vytvořte novou definici řádků. a.</span><span class="sxs-lookup"><span data-stu-id="2a88d-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="2a88d-131">Klikněte na položku Upravit | Vložit řádky z dimenzí. i.</span><span class="sxs-lookup"><span data-stu-id="2a88d-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="2a88d-132">Vyberte Hlavní účet [![Výběr hlavní obrazovky](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="2a88d-133">ii.</span><span class="sxs-lookup"><span data-stu-id="2a88d-133">ii.</span></span> <span data-ttu-id="2a88d-134">Klikněte na tlačítko OK. b.</span><span class="sxs-lookup"><span data-stu-id="2a88d-134">Click Ok b.</span></span>    <span data-ttu-id="2a88d-135">Uložte definici řádku.</span><span class="sxs-lookup"><span data-stu-id="2a88d-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="2a88d-136">Vytvořte novou definici sloupce.     [![Vytvoření nové definice sloupce](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="2a88d-137">Vytvořte novou definici sestavy. a.</span><span class="sxs-lookup"><span data-stu-id="2a88d-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="2a88d-138">Klikněte na Nastavení a zrušte zaškrtnutí. [![Formulář Nastavení](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="2a88d-139">Vygenerujte sestavu.</span><span class="sxs-lookup"><span data-stu-id="2a88d-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="2a88d-140">Exportujte sestavu do aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="2a88d-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="2a88d-141">V D365:</span><span class="sxs-lookup"><span data-stu-id="2a88d-141">In D365:</span></span> 
1.  <span data-ttu-id="2a88d-142">Klikněte na položky Hlavní kniha | Dotazy a sestavy | Předvaha. a.</span><span class="sxs-lookup"><span data-stu-id="2a88d-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="2a88d-143">Parametry: i.</span><span class="sxs-lookup"><span data-stu-id="2a88d-143">Parameters i.</span></span>  <span data-ttu-id="2a88d-144">Od data: Začátek fiskálního roku. ii.</span><span class="sxs-lookup"><span data-stu-id="2a88d-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="2a88d-145">Do data: Datum, pro které jste vygenerovali sestavu. iii.</span><span class="sxs-lookup"><span data-stu-id="2a88d-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="2a88d-146">Sada finančních dimenzí nastavená jako „Sada hlavního účtu“. [![Formulář hlavního účtu](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="2a88d-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="2a88d-147">b.</span><span class="sxs-lookup"><span data-stu-id="2a88d-147">b.</span></span>    <span data-ttu-id="2a88d-148">Klikněte na tlačítko Vypočítat.</span><span class="sxs-lookup"><span data-stu-id="2a88d-148">Click Calculate</span></span>

2.  <span data-ttu-id="2a88d-149">Exportujte sestavu do aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="2a88d-149">Export the report to Excel</span></span>

<span data-ttu-id="2a88d-150">Nyní byste měli být schopni zkopírovat data ze sestavy finančního výkaznictví Excel a do sestavy předvahy D365 a porovnat sloupce „Konečný zůstatek“.</span><span class="sxs-lookup"><span data-stu-id="2a88d-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]