--- 
title: "Zpracování upomínek"
description: "Tato procedura popisuje způsob tvorby, tisku a zaúčtování upomínek."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6ef5916f16cec8e536523192f2d0d234f75de277
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="7ec57-103">Zpracování upomínek</span><span class="sxs-lookup"><span data-stu-id="7ec57-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ec57-104">Tato procedura popisuje způsob tvorby, tisku a zaúčtování upomínek.</span><span class="sxs-lookup"><span data-stu-id="7ec57-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="7ec57-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="7ec57-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="7ec57-106">Nastavení posloupnosti upomínek v účetním profilu</span><span class="sxs-lookup"><span data-stu-id="7ec57-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="7ec57-107">Přejděte do nabídky na Kredit a inkasa > Nastavení > Účetní profily odběratele.</span><span class="sxs-lookup"><span data-stu-id="7ec57-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="7ec57-108">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="7ec57-108">Click Edit.</span></span>
    * <span data-ttu-id="7ec57-109">Z rozevíracího seznamu vyberte posloupnost upomínek.</span><span class="sxs-lookup"><span data-stu-id="7ec57-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="7ec57-110">Pokud nechcete generovat upomínky pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="7ec57-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="7ec57-111">Karta omezení tabulky vám umožní změnit způsob, jakým se zpracovávají upomínky.</span><span class="sxs-lookup"><span data-stu-id="7ec57-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="7ec57-112">Je-li toto pole nastaveno na hodnotu Ano, budou u tohoto účetního profilu vytvářeny upomínky.</span><span class="sxs-lookup"><span data-stu-id="7ec57-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="7ec57-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7ec57-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="7ec57-114">Vytvořit upomínky</span><span class="sxs-lookup"><span data-stu-id="7ec57-114">Create collection letters</span></span>
1. <span data-ttu-id="7ec57-115">Přejděte na Úvěry a inkasa > Upomínka > Vytvořit upomínky.</span><span class="sxs-lookup"><span data-stu-id="7ec57-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="7ec57-116">Musíte vybrat typy transakcí, pro které budete shromažďovat upomínky.</span><span class="sxs-lookup"><span data-stu-id="7ec57-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="7ec57-117">Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="7ec57-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="7ec57-118">V poli Upomínka vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="7ec57-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="7ec57-119">Zadejte datum upomínky.</span><span class="sxs-lookup"><span data-stu-id="7ec57-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="7ec57-120">Existují dvě možnosti účetního profilu:  Účet – Použít účetní profil, který je přiřazený k účtu odběratele pro jednotlivá oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="7ec57-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="7ec57-121">Vybrat – Použije se účetní profil vybraný v poli Účetní profil.</span><span class="sxs-lookup"><span data-stu-id="7ec57-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="7ec57-122">Vyberte účetní profil, pokud jste změnili nastavení „Použít účetní profil z“ na možnost „Vybrat“.</span><span class="sxs-lookup"><span data-stu-id="7ec57-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="7ec57-123">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="7ec57-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="7ec57-124">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="7ec57-124">Click Filter.</span></span>
6. <span data-ttu-id="7ec57-125">Do pole Kritéria v poli Kritéria, zadejte ID zákazníka.</span><span class="sxs-lookup"><span data-stu-id="7ec57-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="7ec57-126">Například zadejte 'US-001'..</span><span class="sxs-lookup"><span data-stu-id="7ec57-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="7ec57-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ec57-127">Click OK.</span></span>
8. <span data-ttu-id="7ec57-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ec57-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="7ec57-129">Tisk upomínek</span><span class="sxs-lookup"><span data-stu-id="7ec57-129">Print collection letters</span></span>
1. <span data-ttu-id="7ec57-130">Přejděte na Úvěry a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky.</span><span class="sxs-lookup"><span data-stu-id="7ec57-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="7ec57-131">V poli Stav vyberte možnost „Vytvořeno“.</span><span class="sxs-lookup"><span data-stu-id="7ec57-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="7ec57-132">Vyberte volbu Nevytištěno v poli Vytištěno.</span><span class="sxs-lookup"><span data-stu-id="7ec57-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="7ec57-133">Klepněte na položku Tisk.</span><span class="sxs-lookup"><span data-stu-id="7ec57-133">Click Print.</span></span>
5. <span data-ttu-id="7ec57-134">Klikněte na možnost Upomínka.</span><span class="sxs-lookup"><span data-stu-id="7ec57-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="7ec57-135">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="7ec57-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="7ec57-136">Vložení data přerušení pro zaúčtování</span><span class="sxs-lookup"><span data-stu-id="7ec57-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="7ec57-137">Kliknutím na OK vytiskněte upomínku.</span><span class="sxs-lookup"><span data-stu-id="7ec57-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="7ec57-138">Zaúčtování upomínky</span><span class="sxs-lookup"><span data-stu-id="7ec57-138">Post the collection letter</span></span>
1. <span data-ttu-id="7ec57-139">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="7ec57-139">Click Post.</span></span>
2. <span data-ttu-id="7ec57-140">Zadejte datum zaúčtování pro upomínku.</span><span class="sxs-lookup"><span data-stu-id="7ec57-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="7ec57-141">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="7ec57-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="7ec57-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ec57-142">Click OK.</span></span>
5. <span data-ttu-id="7ec57-143">V poli Stav vyberte možnost „Zaúčtováno“.</span><span class="sxs-lookup"><span data-stu-id="7ec57-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="7ec57-144">Vyberte volbu v poli Vytištěno.</span><span class="sxs-lookup"><span data-stu-id="7ec57-144">In the Printed field, select an option.</span></span>


