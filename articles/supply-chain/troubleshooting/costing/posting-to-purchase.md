---
title: Přírůstek nákupu, který má nulovou částku, je zaúčtován pro příjem produktu s nulovou hodnotou
description: Když je zaúčtována účtenka produktu, která má nulovou hodnotu, systém vytvoří účtování k nahromadění nákupu, kde je částka 0 (nula).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026353"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="3f84f-103">Přírůstek nákupu, který má nulovou částku, je zaúčtován pro příjem produktu s nulovou hodnotou</span><span class="sxs-lookup"><span data-stu-id="3f84f-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="3f84f-104">Číslo článku znalostní báze: 4612588</span><span class="sxs-lookup"><span data-stu-id="3f84f-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="3f84f-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="3f84f-105">Symptoms</span></span>

<span data-ttu-id="3f84f-106">Když je zaúčtována účtenka produktu, která má nulovou hodnotu, systém vytvoří účtování k nahromadění nákupu, kde je částka 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="3f84f-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="3f84f-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="3f84f-107">Resolution</span></span>

<span data-ttu-id="3f84f-108">Ve výchozím nastavení pro účtování typu hlavní knihy je pole *Nákup, přírůstek* `IsTransferredIndetail` vždy nastaveno na *Souhrn* v transakcích dílčí knihy.</span><span class="sxs-lookup"><span data-stu-id="3f84f-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="3f84f-109">Proto systém vytvoří související položku dokladu, i když je částka 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="3f84f-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="3f84f-110">Chcete-li tento typ účtování přeskočit, když je částka 0 (nula), rozšiřte metodu `subledgerJournalizer.markDoNotTransferEntries` tak, aby zahrnovala `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, jak ukazuje následující příklad.</span><span class="sxs-lookup"><span data-stu-id="3f84f-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
