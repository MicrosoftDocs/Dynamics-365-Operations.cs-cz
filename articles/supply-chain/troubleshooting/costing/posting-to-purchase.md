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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Přírůstek nákupu, který má nulovou částku, je zaúčtován pro příjem produktu s nulovou hodnotou

Číslo článku znalostní báze: 4612588

## <a name="symptoms"></a>Příznaky

Když je zaúčtována účtenka produktu, která má nulovou hodnotu, systém vytvoří účtování k nahromadění nákupu, kde je částka 0 (nula).

## <a name="resolution"></a>Rozlišení

Ve výchozím nastavení pro účtování typu hlavní knihy je pole *Nákup, přírůstek* `IsTransferredIndetail` vždy nastaveno na *Souhrn* v transakcích dílčí knihy. Proto systém vytvoří související položku dokladu, i když je částka 0 (nula).

Chcete-li tento typ účtování přeskočit, když je částka 0 (nula), rozšiřte metodu `subledgerJournalizer.markDoNotTransferEntries` tak, aby zahrnovala `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, jak ukazuje následující příklad.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
