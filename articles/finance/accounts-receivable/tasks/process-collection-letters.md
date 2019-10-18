---
title: Zpracování upomínek
description: Toto téma popisuje způsob tvorby, tisku a zaúčtování upomínek.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176827"
---
# <a name="process-collection-letters"></a><span data-ttu-id="1e99a-103">Zpracování upomínek</span><span class="sxs-lookup"><span data-stu-id="1e99a-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e99a-104">Toto téma popisuje způsob tvorby, tisku a zaúčtování upomínek.</span><span class="sxs-lookup"><span data-stu-id="1e99a-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="1e99a-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="1e99a-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="1e99a-106">Nastavení posloupnosti upomínek v účetním profilu</span><span class="sxs-lookup"><span data-stu-id="1e99a-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="1e99a-107">Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Účetní profily odběratele**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="1e99a-108">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-108">Click **Edit**.</span></span>
3. <span data-ttu-id="1e99a-109">Z rozevíracího seznamu vyberte posloupnost upomínek.</span><span class="sxs-lookup"><span data-stu-id="1e99a-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="1e99a-110">Pokud nechcete generovat upomínky pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="1e99a-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="1e99a-111">Rozbalte kartu **Omezení tabulky**, což umožní změnit způsob, jakým se zpracovávají upomínky.</span><span class="sxs-lookup"><span data-stu-id="1e99a-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="1e99a-112">Je-li toto pole nastaveno na hodnotu **Ano**, budou u tohoto účetního profilu vytvářeny upomínky.</span><span class="sxs-lookup"><span data-stu-id="1e99a-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="1e99a-113">Vytvořit upomínky</span><span class="sxs-lookup"><span data-stu-id="1e99a-113">Create collection letters</span></span>
1. <span data-ttu-id="1e99a-114">Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Upomínka > Vytvořit upomínky**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="1e99a-115">Vyberte typy transakcí, pro které budete shromažďovat upomínky.</span><span class="sxs-lookup"><span data-stu-id="1e99a-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="1e99a-116">Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="1e99a-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="1e99a-117">V poli **Upomínka** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="1e99a-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="1e99a-118">Do pole **Datum upomínky** zadejte datum upomínky.</span><span class="sxs-lookup"><span data-stu-id="1e99a-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="1e99a-119">Vyberte účetní profil, pokud jste změnili nastavení **Použít účetní profil z** na možnost **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="1e99a-120">Existují dvě možnosti účetního profilu:</span><span class="sxs-lookup"><span data-stu-id="1e99a-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="1e99a-121">**Účet** – Pro každé oznámení úroku použije účetní profil přiřazený účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="1e99a-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="1e99a-122">**Vybrat** – Použije se účetní profil vybraný v poli **Účetní profil**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="1e99a-123">Rozbalte oddíl **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="1e99a-124">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-124">Select **Filter**.</span></span>
8. <span data-ttu-id="1e99a-125">Do pole **Kritéria** zadejte ID zákazníka.</span><span class="sxs-lookup"><span data-stu-id="1e99a-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="1e99a-126">Například zadejte 'US-001'.</span><span class="sxs-lookup"><span data-stu-id="1e99a-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="1e99a-127">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-127">Select **OK**.</span></span>
10. <span data-ttu-id="1e99a-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="1e99a-129">Tisk upomínek</span><span class="sxs-lookup"><span data-stu-id="1e99a-129">Print collection letters</span></span>
1. <span data-ttu-id="1e99a-130">Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="1e99a-131">V poli **Stav** vyberte možnost **Vytvořeno**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="1e99a-132">Vyberte volbu **Nevytištěno** v poli **Vytištěno**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="1e99a-133">Vyberte **Tisk**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-133">Select **Print**.</span></span>
5. <span data-ttu-id="1e99a-134">Vyberte možnost **Upomínka**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="1e99a-135">V oddílu **Parametry** zadejte datum přerušení pro zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="1e99a-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="1e99a-136">Rozbalte část **Záznamy k zahrnutí** a zadejte podrobnosti o upomínce.</span><span class="sxs-lookup"><span data-stu-id="1e99a-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="1e99a-137">Výběrem **OK** vytiskněte upomínku.</span><span class="sxs-lookup"><span data-stu-id="1e99a-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="1e99a-138">Zaúčtování upomínky.</span><span class="sxs-lookup"><span data-stu-id="1e99a-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="1e99a-139">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-139">Select **Post**.</span></span>
    1. <span data-ttu-id="1e99a-140">Zadejte datum zaúčtování pro upomínku.</span><span class="sxs-lookup"><span data-stu-id="1e99a-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="1e99a-141">Rozbalte oddíl **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="1e99a-142">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-142">Select **OK**.</span></span>
    1. <span data-ttu-id="1e99a-143">V poli **Stav** vyberte možnost **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="1e99a-144">Vyberte volbu v poli **Vytištěno**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="1e99a-145">Ovládací prvek upomínky na úrovni odběratelů</span><span class="sxs-lookup"><span data-stu-id="1e99a-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="1e99a-146">Upomínky lze také nastavit na úrovni odběratele, tak aby byl sledován kód upomínky pro každou transakci, ale zpracování upomínky bylo založeno na jedné úrovni upomínky, která je pro odběratele uložena.</span><span class="sxs-lookup"><span data-stu-id="1e99a-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="1e99a-147">Jedna upomínka bude obsahovat všechny transakce, které jsou pro odběratele po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1e99a-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="1e99a-148">Vzhledem k tomu, že se dny odkladu nyní sledují na úrovni odběratele, nebude další upomínka odeslána, dokud neuplyne počet dní odkladu pro další upomínku v pořadí, a to i přesto, že budou transakce po odeslání poslední upomínky po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1e99a-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="1e99a-149">Tato možnost sníží počet upomínek odeslaných pro každého zákazníka.</span><span class="sxs-lookup"><span data-stu-id="1e99a-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="1e99a-150">Nastavení odběratele na kontrolu upomínek na úrovni odběratelů</span><span class="sxs-lookup"><span data-stu-id="1e99a-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="1e99a-151">Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Parametry závazků** a vyberte kartu **Inkasa**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="1e99a-152">Změňte hodnotu **vytvořit upomínku pro** na **Odběratel**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="1e99a-153">Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="1e99a-154">Vygeneruje se pouze jedna upomínka pro odběratele se všemi transakcemi po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="1e99a-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="1e99a-155">Ignorovat platby a dobropisy pro výpočet kódu upomínky</span><span class="sxs-lookup"><span data-stu-id="1e99a-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="1e99a-156">Pokud zahrnete transakce a upomínky do transakcí, které budou zahrnuty v upomínkách, můžete mít platby nebo dobropisy, které vyvolají upomínku.</span><span class="sxs-lookup"><span data-stu-id="1e99a-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="1e99a-157">Můžete určovat, jak platby a dobropisy určují kód upomínky, změnou hodnoty parametru **Ignorovat platby a dobropisy při výpočtu kódu upomínky**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="1e99a-158">Pokud chcete ignorovat platby a dobropisy pro výpočet kódu upomínky, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="1e99a-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="1e99a-159">Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Parametry závazků** a klikněte na kartu **Inkasa**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="1e99a-160">Změňte hodnotu možnosti **ignorovat platby a dobropisy pro výpočet kódu upomínky na** **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1e99a-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
