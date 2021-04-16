---
title: Příklad zpracování upomínek
description: Toto téma prochází příkladem, který ukazuje proces vytváření, tisku a odesílání upomínek.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826340"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="be11c-103">Příklad zpracování upomínek</span><span class="sxs-lookup"><span data-stu-id="be11c-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be11c-104">Toto téma prochází příkladem, který ukazuje proces vytváření, tisku a odesílání upomínek.</span><span class="sxs-lookup"><span data-stu-id="be11c-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="be11c-105">Příklad je založen na možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** v Kredit a výběr.</span><span class="sxs-lookup"><span data-stu-id="be11c-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="be11c-106">Využívá data demo společnosti USMF a nového zákazníka US-045.</span><span class="sxs-lookup"><span data-stu-id="be11c-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="be11c-107">Chcete-li začít, přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci**, vyberte **Nový** a poté zadejte požadované informace k vytvoření zákazníka US-045.</span><span class="sxs-lookup"><span data-stu-id="be11c-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="be11c-108">Po dokončení postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="be11c-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="be11c-109">Přejděte do **Kredit a výběr \> Upomínka \> Nastavit sekvenci upomínky** a nastavte sekvenci upomínky, jak je znázorněno v následující tabulce, která je přiřazena k profilu odesílání zákazníků.</span><span class="sxs-lookup"><span data-stu-id="be11c-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="be11c-110">Kód upomínky</span><span class="sxs-lookup"><span data-stu-id="be11c-110">Collection   letter code</span></span>      |     <span data-ttu-id="be11c-111">popis</span><span class="sxs-lookup"><span data-stu-id="be11c-111">Description</span></span>                           |     <span data-ttu-id="be11c-112">Měna</span><span class="sxs-lookup"><span data-stu-id="be11c-112">Currency</span></span>      |     <span data-ttu-id="be11c-113">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="be11c-113">Main   account</span></span>        |     <span data-ttu-id="be11c-114">Poplatek v měně</span><span class="sxs-lookup"><span data-stu-id="be11c-114">Fee   in currency</span></span>     |     <span data-ttu-id="be11c-115">Minimum přes</span><span class="sxs-lookup"><span data-stu-id="be11c-115">Minimum   over</span></span>        |     <span data-ttu-id="be11c-116">Blok dní</span><span class="sxs-lookup"><span data-stu-id="be11c-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="be11c-117">Upomínka 1</span><span class="sxs-lookup"><span data-stu-id="be11c-117">Collection   letter 1</span></span>         |     <span data-ttu-id="be11c-118">Druhé oznámení s poplatkem</span><span class="sxs-lookup"><span data-stu-id="be11c-118">Second   notification with fee</span></span>        |     <span data-ttu-id="be11c-119">USD</span><span class="sxs-lookup"><span data-stu-id="be11c-119">USD</span></span>           |                           |     <span data-ttu-id="be11c-120">0,00</span><span class="sxs-lookup"><span data-stu-id="be11c-120">0.00</span></span>                  |     <span data-ttu-id="be11c-121">0,00</span><span class="sxs-lookup"><span data-stu-id="be11c-121">0.00</span></span>                  |     <span data-ttu-id="be11c-122">2</span><span class="sxs-lookup"><span data-stu-id="be11c-122">2</span></span>                 |
|     <span data-ttu-id="be11c-123">Upomínka 2</span><span class="sxs-lookup"><span data-stu-id="be11c-123">Collection   letter 2</span></span>         |     <span data-ttu-id="be11c-124">Druhé oznámení s poplatkem</span><span class="sxs-lookup"><span data-stu-id="be11c-124">Second   notification with fee</span></span>        |     <span data-ttu-id="be11c-125">USC</span><span class="sxs-lookup"><span data-stu-id="be11c-125">USC</span></span>           |     <span data-ttu-id="be11c-126">403150</span><span class="sxs-lookup"><span data-stu-id="be11c-126">403150</span></span>                |     <span data-ttu-id="be11c-127">20.00</span><span class="sxs-lookup"><span data-stu-id="be11c-127">20.00</span></span>                 |     <span data-ttu-id="be11c-128">10.00</span><span class="sxs-lookup"><span data-stu-id="be11c-128">10.00</span></span>                 |     <span data-ttu-id="be11c-129">3</span><span class="sxs-lookup"><span data-stu-id="be11c-129">3</span></span>                 |
|     <span data-ttu-id="be11c-130">Kolekce</span><span class="sxs-lookup"><span data-stu-id="be11c-130">Collection</span></span>                    |     <span data-ttu-id="be11c-131">Poslední oznámení s poplatkem</span><span class="sxs-lookup"><span data-stu-id="be11c-131">Final   notification with fee</span></span>         |     <span data-ttu-id="be11c-132">USD</span><span class="sxs-lookup"><span data-stu-id="be11c-132">USD</span></span>           |     <span data-ttu-id="be11c-133">403150</span><span class="sxs-lookup"><span data-stu-id="be11c-133">403150</span></span>                |     <span data-ttu-id="be11c-134">50.00</span><span class="sxs-lookup"><span data-stu-id="be11c-134">50.00</span></span>                 |     <span data-ttu-id="be11c-135">100.00</span><span class="sxs-lookup"><span data-stu-id="be11c-135">100.00</span></span>                |     <span data-ttu-id="be11c-136">15</span><span class="sxs-lookup"><span data-stu-id="be11c-136">15</span></span>                |

<span data-ttu-id="be11c-137">Následující obrázek ukazuje informace, které jsou v tabulce tak, jak by vypadaly na stránce **Upomínky**.</span><span class="sxs-lookup"><span data-stu-id="be11c-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="be11c-138">[![Nastavení pořadí upomínek](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="be11c-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="be11c-139">Nyní musíte nastavit dva parametry požadované pro tento příklad.</span><span class="sxs-lookup"><span data-stu-id="be11c-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="be11c-140">Přejděte na **Kredit a inkasa \> Nastavení \> Parametry závazků** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="be11c-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="be11c-141">Na kartě **Inkasa** nastavte možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be11c-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="be11c-142">Ujistěte se, že pole **Vytvořit upomínku pro** je nastaveno na **Zákazník**.</span><span class="sxs-lookup"><span data-stu-id="be11c-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="be11c-143">[![Nastavení parametrů pohledávek pro inkasa](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="be11c-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="be11c-144">Přejděte do **Pohledávky \> Faktury \> Všechny faktury s volným textem**, vyberte **Nový** a potom postupujte podle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="be11c-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="be11c-145">V poli **Účet odběratele** vyberte **US-045**.</span><span class="sxs-lookup"><span data-stu-id="be11c-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="be11c-146">Do pole **Datum faktury** zadejte **15. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="be11c-147">V poli **Splatnost** zadejte hodnotu **16. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="be11c-148">Na kartě s náhledem **Řádky faktur** v poli **Hlavní účet** zadejte **401100**.</span><span class="sxs-lookup"><span data-stu-id="be11c-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="be11c-149">Do pole **Jednotková cena** zadejte **500.00**.</span><span class="sxs-lookup"><span data-stu-id="be11c-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="be11c-150">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="be11c-150">Select **Post**.</span></span>

    <span data-ttu-id="be11c-151">Nyní musíte zadat dva dobropisy pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="be11c-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="be11c-152">Vyberte **Nový** a postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="be11c-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="be11c-153">V poli **Účet odběratele** vyberte **US-045**.</span><span class="sxs-lookup"><span data-stu-id="be11c-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="be11c-154">Do pole **Datum faktury** zadejte **15. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="be11c-155">V poli **Splatnost** zadejte hodnotu **16. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="be11c-156">Na kartě s náhledem **Řádky faktur** v poli **Hlavní účet** zadejte **401100**.</span><span class="sxs-lookup"><span data-stu-id="be11c-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="be11c-157">Zadejte do pole **Jednotková cena** **−100,00**.</span><span class="sxs-lookup"><span data-stu-id="be11c-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="be11c-158">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="be11c-158">Select **Post**.</span></span>

5. <span data-ttu-id="be11c-159">Opakujte krok 4, ale zadejte **−200,00** do pole **Jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="be11c-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="be11c-160">Přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci** a vyberte zákazníka **US-045**.</span><span class="sxs-lookup"><span data-stu-id="be11c-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="be11c-161">Poté v podokně akcí vyberte **Transakce \> Transakce** a zkontrolujte zákaznické transakce, které jste zaúčtovali dříve.</span><span class="sxs-lookup"><span data-stu-id="be11c-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="be11c-162">[![Kontrola zaúčtovaných transakcí se zákazníkem](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="be11c-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="be11c-163">Nyní musíte vytvořit upomínky pro zákazníka US-045.</span><span class="sxs-lookup"><span data-stu-id="be11c-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="be11c-164">Přejděte na **Kredit a inkasa \> Upomínka \> Vytvořit upomínky** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="be11c-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="be11c-165">Nastavte možnosti **Faktura** a **Dobropis** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be11c-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="be11c-166">Ve výchozím nastavení je pole **Upomínka** nastaveno na **Inkaso na zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="be11c-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="be11c-167">Do pole **Datum upomínky** zadejte **19. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="be11c-168">Na kartě s náhledem **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v poli **Zákaznický účet** přidejte zákazníka **US-045**.</span><span class="sxs-lookup"><span data-stu-id="be11c-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="be11c-169">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="be11c-169">Select **OK**.</span></span>
    5. <span data-ttu-id="be11c-170">Výběrem **OK** vytvoříte upomínky.</span><span class="sxs-lookup"><span data-stu-id="be11c-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="be11c-171">Přejděte na **Kredit a inkasa \> Upomínka \> Zkontrolovat a zpracovat upomínky** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="be11c-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="be11c-172">Všimněte si, že kód upomínky na řádcích záhlaví i transakce je **Upomínka 1**, protože tato upomínka je prvním sběrným dopisem v pořadí.</span><span class="sxs-lookup"><span data-stu-id="be11c-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="be11c-173">(Chcete-li zobrazit řádky transakcí, možná budete muset vybrat kartu s náhledem **Transakce**.)</span><span class="sxs-lookup"><span data-stu-id="be11c-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="be11c-174">[![Ověření, že se v záhlaví a řádcích objeví stejný kód upomínky](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="be11c-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="be11c-175">V podokně akcí zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="be11c-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="be11c-176">Do pole **Datum zaúčtování** zadejte **19. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="be11c-177">Nyní musíte opět vytvořit upomínky pro zákazníka US-045.</span><span class="sxs-lookup"><span data-stu-id="be11c-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="be11c-178">Přejděte na **Kredit a inkasa \> Upomínka \> Vytvořit upomínky** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="be11c-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="be11c-179">Nastavte možnosti **Faktura** a **Dobropis** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be11c-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="be11c-180">Ve výchozím nastavení je pole **Upomínka** nastaveno na **Inkaso na zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="be11c-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="be11c-181">Do pole **Datum upomínky** zadejte **23. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="be11c-182">Na kartě s náhledem **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v poli **Zákaznický účet** přidejte zákazníka **US-045**.</span><span class="sxs-lookup"><span data-stu-id="be11c-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="be11c-183">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="be11c-183">Select **OK**.</span></span>
    5. <span data-ttu-id="be11c-184">Výběrem **OK** vytvoříte upomínky.</span><span class="sxs-lookup"><span data-stu-id="be11c-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="be11c-185">Přejděte na **Kredit a inkasa \> Upomínka \> Zkontrolovat a zpracovat upomínky** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="be11c-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="be11c-186">Všimněte si, že kód upomínky v záhlaví je **Upomínka 1**.</span><span class="sxs-lookup"><span data-stu-id="be11c-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="be11c-187">Kód na řádcích transakce však je **Upomínka 2**.</span><span class="sxs-lookup"><span data-stu-id="be11c-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="be11c-188">[![Ověřuje, že se v záhlaví a řádcích objeví různé kódy upomínky](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="be11c-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="be11c-189">Kódy se liší, protože možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** je na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be11c-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="be11c-190">Nezaúčtovat tuto upomínku.</span><span class="sxs-lookup"><span data-stu-id="be11c-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="be11c-191">Přejděte na **Úvěr a inkasa \> Nastavit \> Parametry pohledávek** a poté na kartě **Inkasa** nastavte **Při výpočtu kódu upomínky ignorovat platby a dobropisy** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="be11c-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="be11c-192">[![Nastavení možnosti Ignorovat platby a dobropisy pro výpočet kódu upomínky na Ne](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="be11c-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="be11c-193">Nyní musíte opět vytvořit upomínky pro zákazníka US-045.</span><span class="sxs-lookup"><span data-stu-id="be11c-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="be11c-194">Přejděte na **Kredit a inkasa \> Upomínka \> Vytvořit upomínky** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="be11c-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="be11c-195">Nastavte možnosti **Faktura** a **Dobropis** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be11c-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="be11c-196">Ve výchozím nastavení je pole **Upomínka** nastaveno na **Inkaso na zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="be11c-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="be11c-197">Do pole **Datum upomínky** zadejte **23. 1. 2021**.</span><span class="sxs-lookup"><span data-stu-id="be11c-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="be11c-198">Na kartě s náhledem **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v poli **Zákaznický účet** přidejte zákazníka **US-045**.</span><span class="sxs-lookup"><span data-stu-id="be11c-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="be11c-199">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="be11c-199">Select **OK**.</span></span>
    5. <span data-ttu-id="be11c-200">Výběrem **OK** vytvoříte upomínky.</span><span class="sxs-lookup"><span data-stu-id="be11c-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="be11c-201">Přejděte na **Kredit a inkasa \> Upomínka \> Zkontrolovat a zpracovat upomínky** a všimněte si, že kód upomínky na řádcích záhlaví i transakce je **Upomínka 2**.</span><span class="sxs-lookup"><span data-stu-id="be11c-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="be11c-202">[![Další zobrazení, že se v záhlaví a řádcích objeví stejný kód upomínky](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="be11c-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="be11c-203">Stejný kód se zobrazuje na obou místech, protože možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** je nyní nastavena na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="be11c-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
