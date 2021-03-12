---
title: Stornování zaúčtování deníků
description: V tomto tématu jsou popsány funkce, které umožňují stornovat doklady ze seznamu transakcí dokladu nebo z finančních deníků.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 697ca7557b26026783626e843ee1e5d1fd27db9a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990257"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="29332-103">Stornování zaúčtování deníků</span><span class="sxs-lookup"><span data-stu-id="29332-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29332-104">Toto téma popisuje funkce schopnosti Microsoft Dynamics 365 Finance, které umožňují stornovat celý deník nebo jeden nebo více dokladů ze seznamu transakcí dokladu bez ohledu na jejich původ.</span><span class="sxs-lookup"><span data-stu-id="29332-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="29332-105">Storno deníků</span><span class="sxs-lookup"><span data-stu-id="29332-105">Reversing journals</span></span>

<span data-ttu-id="29332-106">Řádky deníku můžete stornovat jednotlivě.</span><span class="sxs-lookup"><span data-stu-id="29332-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="29332-107">Při zaúčtování storna deníku můžete také stornovat celý finanční deník.</span><span class="sxs-lookup"><span data-stu-id="29332-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="29332-108">Postup stornování deníku:</span><span class="sxs-lookup"><span data-stu-id="29332-108">To reverse a journal:</span></span> 

- <span data-ttu-id="29332-109">Otevřete finanční deník a filtrujte podle zaúčtovaných deníků.</span><span class="sxs-lookup"><span data-stu-id="29332-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="29332-110">Vyberte na nabídku **Stornovat** v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="29332-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="29332-111">Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.</span><span class="sxs-lookup"><span data-stu-id="29332-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="29332-112">Vyberte možnost **Ano**, chcete-li použít existující data transakcí nebo hodnotu **Ne** a zadat novou.</span><span class="sxs-lookup"><span data-stu-id="29332-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="29332-113">V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.</span><span class="sxs-lookup"><span data-stu-id="29332-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="29332-114">Pokud vyberete možnost **Ne**, zadejte datum transakce pro stornování.</span><span class="sxs-lookup"><span data-stu-id="29332-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="29332-115">Zadejte poznámku, kterou chcete přidat k transakci storna.</span><span class="sxs-lookup"><span data-stu-id="29332-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="29332-116">Zvolte tlačítko **Stornovat**.</span><span class="sxs-lookup"><span data-stu-id="29332-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="29332-117">Transakce budou stornovány.</span><span class="sxs-lookup"><span data-stu-id="29332-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="29332-118">Pokud počet řádků dokladu obsahuje více než 100 řádků, bude proces storna proveden pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="29332-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="29332-119">Výsledky můžete zkontrolovat zobrazením komentářů v dávkové úloze.</span><span class="sxs-lookup"><span data-stu-id="29332-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="29332-120">Všechny transakce, u nichž nelze provést stornování, budou uvedeny v historii dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="29332-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="29332-121">Pokud doklad obsahuje 100 nebo méně řádků, bude proces storna spuštěn okamžitě.</span><span class="sxs-lookup"><span data-stu-id="29332-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="29332-122">Výsledky budou uvedeny v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat.</span><span class="sxs-lookup"><span data-stu-id="29332-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="29332-123">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29332-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="29332-124">Stornování dokladů ze seznamu transakcí dokladu.</span><span class="sxs-lookup"><span data-stu-id="29332-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="29332-125">Můžete také stornovat doklady ze **seznamu transakcí dokladu** ve všech dílčích knihách.</span><span class="sxs-lookup"><span data-stu-id="29332-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="29332-126">Kromě toho lze najednou stornovat více dokladů.</span><span class="sxs-lookup"><span data-stu-id="29332-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="29332-127">Chcete-li stornovat jeden nebo více dokladů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="29332-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="29332-128">Vyberte na nabídku **Stornovat** v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="29332-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="29332-129">Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.</span><span class="sxs-lookup"><span data-stu-id="29332-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="29332-130">Vyberte možnost **Ano**, chcete-li použít existující data transakcí nebo hodnotu **Ne** a zadat novou.</span><span class="sxs-lookup"><span data-stu-id="29332-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="29332-131">V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.</span><span class="sxs-lookup"><span data-stu-id="29332-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="29332-132">Pokud vyberete možnost **Ne**, zadejte datum transakce pro stornování.</span><span class="sxs-lookup"><span data-stu-id="29332-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="29332-133">Zadejte komentář popisující transakci stornování.</span><span class="sxs-lookup"><span data-stu-id="29332-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="29332-134">Zvolte tlačítko **Stornovat**.</span><span class="sxs-lookup"><span data-stu-id="29332-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="29332-135">Transakce budou stornovány.</span><span class="sxs-lookup"><span data-stu-id="29332-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="29332-136">Pokud počet řádků dokladu obsahuje více než 100 řádků dokladu, bude proces storna proveden pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="29332-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="29332-137">Výsledky můžete zkontrolovat zobrazením komentářů v dávkové úloze.</span><span class="sxs-lookup"><span data-stu-id="29332-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="29332-138">Všechny transakce, u nichž nelze provést stornování, budou uvedeny v historii dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="29332-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="29332-139">Pokud je počet řádků dokladu 100 nebo méně, bude proces storna spuštěn okamžitě.</span><span class="sxs-lookup"><span data-stu-id="29332-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="29332-140">Výsledky se zobrazí v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat.</span><span class="sxs-lookup"><span data-stu-id="29332-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="29332-141">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29332-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="29332-142">Transakce lze stornovat pouze v případě, že vyhovují obchodním pravidlům pro jejich stornování.</span><span class="sxs-lookup"><span data-stu-id="29332-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="29332-143">Platby dodavatele nelze stornovat pomocí možnosti popsané v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="29332-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="29332-144">Platby dodavatelů je nutné stornovat podle kroků uvedených v části [Stornování platby dodavatele](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="29332-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

