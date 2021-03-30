---
title: Zpracování úroků
description: Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4f1ed6d0199235e946d55dfa904246c109acba42
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220124"
---
# <a name="process-interest"></a><span data-ttu-id="3cae5-103">Zpracování úroků</span><span class="sxs-lookup"><span data-stu-id="3cae5-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cae5-104">Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="3cae5-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="3cae5-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="3cae5-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="3cae5-106">Nastavte úrok v účetním profilu.</span><span class="sxs-lookup"><span data-stu-id="3cae5-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="3cae5-107">V **Navigačním podokně** přejděte na **Moduly > Kredit a inkasa > Nastavení > Účetní profily odběratele**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="3cae5-108">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-108">Click **Edit**.</span></span>
3. <span data-ttu-id="3cae5-109">Na pevné záložce **Nastavení** v poli **Kód úroku** vyberte kód úroku z rozevíracího seznamu.</span><span class="sxs-lookup"><span data-stu-id="3cae5-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="3cae5-110">Pokud nechcete vypočítat úrok pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="3cae5-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="3cae5-111">Pevná záložka **Omezení tabulky** vám umožní změnit způsob, jakým se zpracovává úrok.</span><span class="sxs-lookup"><span data-stu-id="3cae5-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="3cae5-112">Je-li toto pole nastaveno na hodnotu Ano, budou u tohoto účetního profilu vypočteny úroky.</span><span class="sxs-lookup"><span data-stu-id="3cae5-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="3cae5-113">Vypočítat úroky</span><span class="sxs-lookup"><span data-stu-id="3cae5-113">Calculate interest</span></span>
1. <span data-ttu-id="3cae5-114">V **Navigačním podokně** přejděte na **Moduly > Kredit a inkasa > Úrok > Vytvořit oznámení úroků**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="3cae5-115">Musíte vybrat typy transakcí, pro které budete vypočítávat úrok.</span><span class="sxs-lookup"><span data-stu-id="3cae5-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="3cae5-116">Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="3cae5-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="3cae5-117">Pokud nastavíte **Úrok** na ‚Ano‘, budete počítat úrok z úroku.</span><span class="sxs-lookup"><span data-stu-id="3cae5-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="3cae5-118">Je vhodné zkontrolovat zákony upravující výpočet úroku z úroku před jeho zahrnutím do těchto transakcí.</span><span class="sxs-lookup"><span data-stu-id="3cae5-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="3cae5-119">V poli **Od data** zadejte datum, od kterého se bude úrok počítat.</span><span class="sxs-lookup"><span data-stu-id="3cae5-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="3cae5-120">Pokud neurčíte pole **Od data**, pak všechna nezaúčtovaná oznámení úroků budou zrušena a úroky budou přepočítány od data transakce.</span><span class="sxs-lookup"><span data-stu-id="3cae5-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="3cae5-121">V poli **Do data** zadejte datum, do kterého se bude úrok počítat.</span><span class="sxs-lookup"><span data-stu-id="3cae5-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="3cae5-122">V poli **Použít účetní profil od** je nutné vybrat nějakou možnost.</span><span class="sxs-lookup"><span data-stu-id="3cae5-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="3cae5-123">Existují tři možnosti účetního profilu:</span><span class="sxs-lookup"><span data-stu-id="3cae5-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="3cae5-124">Účet – Pro každé oznámení úroku použije účetní profil přiřazený účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="3cae5-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="3cae5-125">Vybrat – Použije se účetní profil vybraný v poli Účetní profil.</span><span class="sxs-lookup"><span data-stu-id="3cae5-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="3cae5-126">Transakce – Pomocí individuálního účetního profilu z transakcí, na nichž se počítá úrok pro jednotlivá oznámení úroku.</span><span class="sxs-lookup"><span data-stu-id="3cae5-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="3cae5-127">Transakce, které nemají přiřazený účetní profil použijí účetní profil, který je uveden v oblasti Hlavní kniha a DPH formuláře Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="3cae5-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="3cae5-128">Rozbalte pevnou záložku **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="3cae5-129">Klikněte na tlačítko **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-129">Click **Filter**.</span></span>
9. <span data-ttu-id="3cae5-130">Do pole **Kritéria** zadejte ID zákazníka.</span><span class="sxs-lookup"><span data-stu-id="3cae5-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="3cae5-131">Například zadejte 'US-001'.</span><span class="sxs-lookup"><span data-stu-id="3cae5-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="3cae5-132">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-132">Click **OK**.</span></span>
7. <span data-ttu-id="3cae5-133">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="3cae5-134">Tisk oznámení úroků</span><span class="sxs-lookup"><span data-stu-id="3cae5-134">Print interest notes</span></span>
1. <span data-ttu-id="3cae5-135">V **Navigačním podokně** přejděte na **Moduly > Kredit a inkasa > Úrok > Zkontrolovat a zpracovat oznámení úroků**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="3cae5-136">V poli **Stav** vyberte možnost „Vytvořeno“.</span><span class="sxs-lookup"><span data-stu-id="3cae5-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="3cae5-137">V poli **Vytištěno** vyberte volbu ‚Nevytištěno‘.</span><span class="sxs-lookup"><span data-stu-id="3cae5-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="3cae5-138">Klepněte na položku **Tisk**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-138">Click **Print**.</span></span>
5. <span data-ttu-id="3cae5-139">Rozbalte pevnou záložku **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="3cae5-140">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-140">Click **OK**.</span></span>
7. <span data-ttu-id="3cae5-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3cae5-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="3cae5-142">Zaúčtování oznámení úroků</span><span class="sxs-lookup"><span data-stu-id="3cae5-142">Post the interest note</span></span>
1. <span data-ttu-id="3cae5-143">Vyberte oznámení úroků, které je připraveno k zaúčtování (stav je vytvořen).</span><span class="sxs-lookup"><span data-stu-id="3cae5-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="3cae5-144">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-144">Click **Post**.</span></span>
3. <span data-ttu-id="3cae5-145">Zadejte datum účtování pro oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="3cae5-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="3cae5-146">Chcete-li pro oznámení úroků vytvořit jednu transakci hlavní knihy, vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="3cae5-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="3cae5-147">Pokud políčko Ano nevyberete, bude úrok všech oznámení úroků odběrateli kumulován a zaúčtován do hlavní knihy jako jedna transakce.</span><span class="sxs-lookup"><span data-stu-id="3cae5-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="3cae5-148">Rozbalte pevnou záložku **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="3cae5-149">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cae5-149">Click **OK**.</span></span>
6. <span data-ttu-id="3cae5-150">V poli **Stav** vyberte možnost „Zaúčtováno“.</span><span class="sxs-lookup"><span data-stu-id="3cae5-150">In the **Status** field, select 'Posted'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]