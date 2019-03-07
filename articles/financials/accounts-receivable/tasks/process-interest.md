---
title: Zpracování úroků
description: Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "359145"
---
# <a name="process-interest"></a><span data-ttu-id="ed558-103">Zpracování úroků</span><span class="sxs-lookup"><span data-stu-id="ed558-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ed558-104">Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="ed558-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="ed558-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="ed558-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="ed558-106">Nastavte úrok v účetním profilu.</span><span class="sxs-lookup"><span data-stu-id="ed558-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="ed558-107">Přejděte do nabídky na Kredit a inkasa > Nastavení > Účetní profily odběratele.</span><span class="sxs-lookup"><span data-stu-id="ed558-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="ed558-108">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="ed558-108">Click Edit.</span></span>
    * <span data-ttu-id="ed558-109">Vyberte kód úroku z rozevíracího seznamu.</span><span class="sxs-lookup"><span data-stu-id="ed558-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="ed558-110">Pokud nechcete vypočítat úrok pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="ed558-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="ed558-111">Karta Omezení tabulky vám umožní změnit způsob, jakým se zpracovává úrok.</span><span class="sxs-lookup"><span data-stu-id="ed558-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="ed558-112">Je-li toto pole nastaveno na hodnotu Ano, budou u tohoto účetního profilu vypočteny úroky.</span><span class="sxs-lookup"><span data-stu-id="ed558-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="ed558-113">Vypočítat úroky</span><span class="sxs-lookup"><span data-stu-id="ed558-113">Calculate interest</span></span>
1. <span data-ttu-id="ed558-114">Přejděte do nabídky Úvěry a inkasa > Úrok > Vytvořit oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="ed558-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="ed558-115">Musíte vybrat typy transakcí, pro které budete vypočítávat úrok.</span><span class="sxs-lookup"><span data-stu-id="ed558-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="ed558-116">Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="ed558-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="ed558-117">Pokud vyberete Úrok, budete počítat úrok z úroku.</span><span class="sxs-lookup"><span data-stu-id="ed558-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="ed558-118">Je vhodné zkontrolovat zákony upravující výpočet úroku z úroku před jeho zahrnutím do těchto transakcí.</span><span class="sxs-lookup"><span data-stu-id="ed558-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="ed558-119">Úrok se vypočítá od tohoto data do data "Do data".</span><span class="sxs-lookup"><span data-stu-id="ed558-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="ed558-120">Pokud neurčíte pole „Od data“, pak všechna nezaúčtovaná oznámení úroků budou zrušena a úroky budou přepočítány od data transakce.</span><span class="sxs-lookup"><span data-stu-id="ed558-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="ed558-121">Zadejte datum oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="ed558-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="ed558-122">Existují tři možnosti účetního profilu:  Účet – Použít účetní profil, který je přiřazený k účtu odběratele pro jednotlivá oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="ed558-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="ed558-123">Vybrat – Použije se účetní profil vybraný v poli Účetní profil.</span><span class="sxs-lookup"><span data-stu-id="ed558-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="ed558-124">Transakce – Pomocí individuálního účetního profilu z transakcí, na nichž se počítá úrok pro jednotlivá oznámení úroku.</span><span class="sxs-lookup"><span data-stu-id="ed558-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="ed558-125">Transakce, které nemají přiřazený účetní profil použijí účetní profil, který je uveden v oblasti Hlavní kniha a DPH formuláře Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="ed558-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="ed558-126">Zde vyberte účetní profil, pokud jste změnili nastavení „Použít účetní profil z“ na možnost „Vybrat“.</span><span class="sxs-lookup"><span data-stu-id="ed558-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="ed558-127">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="ed558-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="ed558-128">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="ed558-128">Click Filter.</span></span>
5. <span data-ttu-id="ed558-129">Do pole Kritéria zadejte ID zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ed558-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="ed558-130">Například zadejte 'US-001'..</span><span class="sxs-lookup"><span data-stu-id="ed558-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="ed558-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ed558-131">Click OK.</span></span>
7. <span data-ttu-id="ed558-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ed558-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="ed558-133">Tisk oznámení úroků</span><span class="sxs-lookup"><span data-stu-id="ed558-133">Print interest notes</span></span>
1. <span data-ttu-id="ed558-134">Přejděte do nabídky Úvěry a inkasa > Úrok > Zkontrolovat a zpracovat oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="ed558-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="ed558-135">V poli Stav vyberte možnost „Vytvořeno“.</span><span class="sxs-lookup"><span data-stu-id="ed558-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="ed558-136">Vyberte volbu Nevytištěno v poli Vytištěno.</span><span class="sxs-lookup"><span data-stu-id="ed558-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="ed558-137">Klepněte na položku Tisk.</span><span class="sxs-lookup"><span data-stu-id="ed558-137">Click Print.</span></span>
5. <span data-ttu-id="ed558-138">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="ed558-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="ed558-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ed558-139">Click OK.</span></span>
7. <span data-ttu-id="ed558-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ed558-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="ed558-141">Zaúčtování oznámení úroků</span><span class="sxs-lookup"><span data-stu-id="ed558-141">Post the interest note</span></span>
1. <span data-ttu-id="ed558-142">Vyberte oznámení úroků, které je připraveno k zaúčtování (stav je vytvořen).</span><span class="sxs-lookup"><span data-stu-id="ed558-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="ed558-143">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="ed558-143">Click Post.</span></span>
3. <span data-ttu-id="ed558-144">Zadejte datum účtování pro oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="ed558-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="ed558-145">Chcete-li pro oznámení úroků vytvořit jednu transakci hlavní knihy, vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="ed558-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="ed558-146">Pokud políčko Ano nevyberete, bude úrok všech oznámení úroků odběrateli kumulován a zaúčtován do hlavní knihy jako jedna transakce.</span><span class="sxs-lookup"><span data-stu-id="ed558-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="ed558-147">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="ed558-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="ed558-148">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ed558-148">Click OK.</span></span>
6. <span data-ttu-id="ed558-149">V poli Stav vyberte možnost „Zaúčtováno“.</span><span class="sxs-lookup"><span data-stu-id="ed558-149">In the Status field, select 'Posted'.</span></span>

