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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fba25c900461fbbf4db0cd3b93847d258704ab4e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842874"
---
# <a name="process-interest"></a><span data-ttu-id="07991-103">Zpracování úroků</span><span class="sxs-lookup"><span data-stu-id="07991-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07991-104">Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="07991-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="07991-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="07991-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="07991-106">Nastavte úrok v účetním profilu.</span><span class="sxs-lookup"><span data-stu-id="07991-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="07991-107">Přejděte do nabídky na Kredit a inkasa > Nastavení > Účetní profily odběratele.</span><span class="sxs-lookup"><span data-stu-id="07991-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="07991-108">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="07991-108">Click Edit.</span></span>
    * <span data-ttu-id="07991-109">Vyberte kód úroku z rozevíracího seznamu.</span><span class="sxs-lookup"><span data-stu-id="07991-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="07991-110">Pokud nechcete vypočítat úrok pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="07991-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="07991-111">Karta Omezení tabulky vám umožní změnit způsob, jakým se zpracovává úrok.</span><span class="sxs-lookup"><span data-stu-id="07991-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="07991-112">Je-li toto pole nastaveno na hodnotu Ano, budou u tohoto účetního profilu vypočteny úroky.</span><span class="sxs-lookup"><span data-stu-id="07991-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="07991-113">Vypočítat úroky</span><span class="sxs-lookup"><span data-stu-id="07991-113">Calculate interest</span></span>
1. <span data-ttu-id="07991-114">Přejděte do nabídky Úvěry a inkasa > Úrok > Vytvořit oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="07991-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="07991-115">Musíte vybrat typy transakcí, pro které budete vypočítávat úrok.</span><span class="sxs-lookup"><span data-stu-id="07991-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="07991-116">Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="07991-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="07991-117">Pokud vyberete Úrok, budete počítat úrok z úroku.</span><span class="sxs-lookup"><span data-stu-id="07991-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="07991-118">Je vhodné zkontrolovat zákony upravující výpočet úroku z úroku před jeho zahrnutím do těchto transakcí.</span><span class="sxs-lookup"><span data-stu-id="07991-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="07991-119">Úrok se vypočítá od tohoto data do data "Do data".</span><span class="sxs-lookup"><span data-stu-id="07991-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="07991-120">Pokud neurčíte pole „Od data“, pak všechna nezaúčtovaná oznámení úroků budou zrušena a úroky budou přepočítány od data transakce.</span><span class="sxs-lookup"><span data-stu-id="07991-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="07991-121">Zadejte datum oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="07991-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="07991-122">Existují tři možnosti účetního profilu:  Účet – Použít účetní profil, který je přiřazený k účtu odběratele pro jednotlivá oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="07991-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="07991-123">Vybrat – Použije se účetní profil vybraný v poli Účetní profil.</span><span class="sxs-lookup"><span data-stu-id="07991-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="07991-124">Transakce – Pomocí individuálního účetního profilu z transakcí, na nichž se počítá úrok pro jednotlivá oznámení úroku.</span><span class="sxs-lookup"><span data-stu-id="07991-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="07991-125">Transakce, které nemají přiřazený účetní profil použijí účetní profil, který je uveden v oblasti Hlavní kniha a DPH formuláře Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="07991-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="07991-126">Zde vyberte účetní profil, pokud jste změnili nastavení „Použít účetní profil z“ na možnost „Vybrat“.</span><span class="sxs-lookup"><span data-stu-id="07991-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="07991-127">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="07991-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="07991-128">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="07991-128">Click Filter.</span></span>
5. <span data-ttu-id="07991-129">Do pole Kritéria zadejte ID zákazníka.</span><span class="sxs-lookup"><span data-stu-id="07991-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="07991-130">Například zadejte 'US-001'..</span><span class="sxs-lookup"><span data-stu-id="07991-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="07991-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="07991-131">Click OK.</span></span>
7. <span data-ttu-id="07991-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="07991-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="07991-133">Tisk oznámení úroků</span><span class="sxs-lookup"><span data-stu-id="07991-133">Print interest notes</span></span>
1. <span data-ttu-id="07991-134">Přejděte do nabídky Úvěry a inkasa > Úrok > Zkontrolovat a zpracovat oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="07991-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="07991-135">V poli Stav vyberte možnost „Vytvořeno“.</span><span class="sxs-lookup"><span data-stu-id="07991-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="07991-136">Vyberte volbu Nevytištěno v poli Vytištěno.</span><span class="sxs-lookup"><span data-stu-id="07991-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="07991-137">Klepněte na položku Tisk.</span><span class="sxs-lookup"><span data-stu-id="07991-137">Click Print.</span></span>
5. <span data-ttu-id="07991-138">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="07991-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="07991-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="07991-139">Click OK.</span></span>
7. <span data-ttu-id="07991-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="07991-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="07991-141">Zaúčtování oznámení úroků</span><span class="sxs-lookup"><span data-stu-id="07991-141">Post the interest note</span></span>
1. <span data-ttu-id="07991-142">Vyberte oznámení úroků, které je připraveno k zaúčtování (stav je vytvořen).</span><span class="sxs-lookup"><span data-stu-id="07991-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="07991-143">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="07991-143">Click Post.</span></span>
3. <span data-ttu-id="07991-144">Zadejte datum účtování pro oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="07991-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="07991-145">Chcete-li pro oznámení úroků vytvořit jednu transakci hlavní knihy, vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="07991-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="07991-146">Pokud políčko Ano nevyberete, bude úrok všech oznámení úroků odběrateli kumulován a zaúčtován do hlavní knihy jako jedna transakce.</span><span class="sxs-lookup"><span data-stu-id="07991-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="07991-147">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="07991-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="07991-148">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="07991-148">Click OK.</span></span>
6. <span data-ttu-id="07991-149">V poli Stav vyberte možnost „Zaúčtováno“.</span><span class="sxs-lookup"><span data-stu-id="07991-149">In the Status field, select 'Posted'.</span></span>

