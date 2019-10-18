---
title: Stornování zaúčtování deníků
description: V tomto tématu jsou popsány funkce, které umožňují stornovat doklady ze seznamu transakcí dokladu nebo z finančních deníků.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248578"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="b0a2b-103">Stornování zaúčtování deníků</span><span class="sxs-lookup"><span data-stu-id="b0a2b-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0a2b-104">Toto téma popisuje funkce schopnosti Microsoft Dynamics 365 Finance, které umožňují stornovat celý deník nebo stornovat jeden nebo více dokladů ze seznamu transakcí dokladu bez ohledu na jejich původ.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="b0a2b-105">Storno deníků</span><span class="sxs-lookup"><span data-stu-id="b0a2b-105">Reversing journals</span></span>

<span data-ttu-id="b0a2b-106">Řádky deníku můžete stornovat jednotlivě.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="b0a2b-107">Při zaúčtování storna deníku můžete také stornovat celý finanční deník.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="b0a2b-108">Postup stornování deníku:</span><span class="sxs-lookup"><span data-stu-id="b0a2b-108">To reverse a journal:</span></span> 
- <span data-ttu-id="b0a2b-109">Otevření finančního deníku a filtrování podle zaúčtovaných deníků</span><span class="sxs-lookup"><span data-stu-id="b0a2b-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="b0a2b-110">Klikněte na nabídku Stornovat v horní části stránky</span><span class="sxs-lookup"><span data-stu-id="b0a2b-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="b0a2b-111">Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b0a2b-112">Vyberte možnost Ano, chcete-li použít existující data transakcí nebo hodnotu Ne a zadat novou.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="b0a2b-113">V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b0a2b-114">Pokud jste vybrali možnost Ne, zadejte datum transakce pro stornování.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b0a2b-115">Zadejte poznámku, kterou chcete přidat k transakci storna.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="b0a2b-116">Klikněte na tlačítko Stornovat.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-116">Click the Reverse button</span></span>

<span data-ttu-id="b0a2b-117">Transakce budou stornovány.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="b0a2b-118">Pokud počet řádků dokladu překročí 100 řádků, bude proces storna proveden pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="b0a2b-119">Výsledky stornování můžete zkontrolovat zobrazením komentářů v dávkové úloze, která byla spuštěna.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="b0a2b-120">Všechny chyby budou zaznamenány v historii dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="b0a2b-121">Pokud je počet řádků dokladu 100 nebo méně, bude proces storna spuštěn okamžitě.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="b0a2b-122">Výsledky budou uvedeny v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="b0a2b-123">Kliknutím na tlačítko OK dialogové okno zavřete.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="b0a2b-124">Stornování dokladů ze seznamu transakcí dokladu.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="b0a2b-125">Můžete také stornovat doklady ze **seznamu transakcí dokladu** ve všech dílčích knihách.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="b0a2b-126">Kromě toho lze najednou stornovat více dokladů.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="b0a2b-127">Chcete-li stornovat jeden nebo více dokladů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="b0a2b-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="b0a2b-128">Klikněte na nabídku Stornovat v horní části stránky</span><span class="sxs-lookup"><span data-stu-id="b0a2b-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="b0a2b-129">Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b0a2b-130">Vyberte možnost Ano, chcete-li použít existující data transakcí nebo hodnotu Ne a zadat novou.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="b0a2b-131">V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b0a2b-132">Pokud jste vybrali možnost Ne, zadejte datum transakce pro stornování.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b0a2b-133">Zadejte poznámku, kterou chcete přidat k transakci storna.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="b0a2b-134">Klikněte na tlačítko Stornovat.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-134">Click the Reverse button</span></span>

<span data-ttu-id="b0a2b-135">Transakce budou stornovány.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="b0a2b-136">Pokud počet řádků dokladu překročí 100 řádků, bude proces storna proveden pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="b0a2b-137">Výsledky stornování můžete zkontrolovat zobrazením komentářů v dávkové úloze, která byla spuštěna.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="b0a2b-138">Všechny chyby budou zaznamenány v historii dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="b0a2b-139">Pokud je počet řádků dokladu 100 nebo méně, bude proces storna spuštěn okamžitě.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="b0a2b-140">Výsledky budou uvedeny v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="b0a2b-141">Kliknutím na tlačítko OK dialogové okno zavřete.</span><span class="sxs-lookup"><span data-stu-id="b0a2b-141">Click on Ok to close the dialog.</span></span>

