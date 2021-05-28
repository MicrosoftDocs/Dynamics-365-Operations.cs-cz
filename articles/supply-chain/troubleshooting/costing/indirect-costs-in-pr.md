---
title: Sestava Nepřímé náklady v procesu zahrnuje odstraněné výrobní zakázky
description: Zpráva Nepřímé náklady v procesu obsahuje informace o výrobních zakázkách, které byly částečně zpracovány a později odstraněny.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026338"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="729ae-103">Sestava Nepřímé náklady v procesu zahrnuje odstraněné výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="729ae-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="729ae-104">Číslo článku znalostní báze: 4612748</span><span class="sxs-lookup"><span data-stu-id="729ae-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="729ae-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="729ae-105">Symptoms</span></span>

<span data-ttu-id="729ae-106">Zpráva **Nepřímé náklady** v procesu obsahuje informace o výrobních zakázkách, které byly částečně zpracovány a později odstraněny.</span><span class="sxs-lookup"><span data-stu-id="729ae-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="729ae-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="729ae-107">Resolution</span></span>

<span data-ttu-id="729ae-108">Když stornujete výrobní zakázku, stornujete také všechny transakce dané výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="729ae-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="729ae-109">Když odstraníte výrobní zakázku, tabulky vedlejší knihy a hlavní knihy přetrvají přes všechny transakce, které s ní souvisí.</span><span class="sxs-lookup"><span data-stu-id="729ae-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="729ae-110">Sestavy budou zobrazovat transakce v tabulkách podřízené knihy.</span><span class="sxs-lookup"><span data-stu-id="729ae-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="729ae-111">U konkrétní výrobní zakázky by čistá hodnota měla být 0,00.</span><span class="sxs-lookup"><span data-stu-id="729ae-111">For the specific production order, the net value should be 0.00.</span></span>
