---
title: Vytvoření měsíčních položek deníku v dávce
description: Toto téma vysvětluje, jak vytvořit položky deníku v dávce, což pomůže zvýšit efektivitu při zaznamenávání měsíčních výdajů na leasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6fd1815620095909e290fd03c404d964baa04a94
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241555"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="98f84-103">Vytvoření měsíčních položek deníku v dávce</span><span class="sxs-lookup"><span data-stu-id="98f84-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98f84-104">Toto téma vysvětluje, jak vytvořit položky deníku v dávce, což pomůže zvýšit efektivitu při zaznamenávání měsíčních výdajů na leasing.</span><span class="sxs-lookup"><span data-stu-id="98f84-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="98f84-105">Dávkové zpracování lze použít k vytvoření položek deníku z více plánů.</span><span class="sxs-lookup"><span data-stu-id="98f84-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="98f84-106">Mezi tyto položky deníku mohou patřit leasingové splátky, amortizace závazků, amortizace používaného majetku a výdaje na zachraňovací náklady.</span><span class="sxs-lookup"><span data-stu-id="98f84-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="98f84-107">Dávkové zpracování můžete také použít k počátečnímu uznání více leasingů najednou nebo k vytvoření přechodových úprav pro více leasingů najednou.</span><span class="sxs-lookup"><span data-stu-id="98f84-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="98f84-108">Chcete-li vytvořit dávkovou úlohu nebo zpracovat platební faktury, odpisy nebo úroky pro více leasingů, přejděte na **Leasing majetku \> Periodicky \> Dávkové vytvoření deníku**.</span><span class="sxs-lookup"><span data-stu-id="98f84-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="98f84-109">V dialogovém okně, které se zobrazí, můžete vybrat plán, ze kterého mají být vytvořeny položky deníku.</span><span class="sxs-lookup"><span data-stu-id="98f84-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="98f84-110">Můžete také určit, zda má být dávkový proces spuštěn pro konkrétní entity, skupiny leasingu nebo leasingové knihy.</span><span class="sxs-lookup"><span data-stu-id="98f84-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="98f84-111">Následné transakce, jako jsou plány amortizace závazků, platby, odpisy a výdaje, budou zaúčtovány až po zaúčtování počátečního uznání u příslušných leasingů.</span><span class="sxs-lookup"><span data-stu-id="98f84-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="98f84-112">Položky deníku jsou vytvořeny, ale nebudou zaúčtovány, dokud nevyberete příkaz **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="98f84-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]