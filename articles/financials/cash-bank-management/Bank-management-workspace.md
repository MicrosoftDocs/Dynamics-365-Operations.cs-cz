---
title: Pracovní prostor správy banky
description: Toto téma poskytuje informace o pracovním prostoru Správa banky. Tento pracovní prostor zobrazuje Informace, které se vztahují k bankovním účtům společnosti a obsahují souhrnné zobrazení a stránku analýzy. Souhrnné zobrazení ukazuje souhrnné dlaždice, informace o bankovním účtu, graf zůstatku a související informace. Na stránce analýzy se používají funkce Microsoft Power BI k zobrazení vizuálů, které se vztahují k zůstatkům na bankovním účtu.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 20847ea4651b816fc95135ca03667ae297cde5be
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842730"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="dc0c2-106">Pracovní prostor správy banky</span><span class="sxs-lookup"><span data-stu-id="dc0c2-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc0c2-107">Pracovní prostor **Správa banky** zobrazuje informace, které se vztahují k bankovním účtům společnosti.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="dc0c2-108">Tento pracovní prostor obsahuje zobrazení **Souhrn** a stránku **Analýzy**.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="dc0c2-109">Zobrazení **Souhrn** ukazuje souhrnné dlaždice, informace o bankovním účtu, graf zůstatku a související informace.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="dc0c2-110">Na stránce **Analýzy** se používají funkce Microsoft Power BI k zobrazení vizuálů, které se vztahují k zůstatkům na bankovním účtu.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="dc0c2-111">Souhrnné zobrazení</span><span class="sxs-lookup"><span data-stu-id="dc0c2-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="dc0c2-112">Souhrn</span><span class="sxs-lookup"><span data-stu-id="dc0c2-112">Summary</span></span>

<span data-ttu-id="dc0c2-113">Dlaždice v části **Souhrn** poskytují přehled o bankovních účtech a umožňují rychlý přístup ke stránkám, které musíte používat nejčastěji.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="dc0c2-114">Informace o odsouhlasení banky je specifická vůči funkci rozšířeného odsouhlasení banky.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="dc0c2-115">Informace jsou zahrnuty pouze pro ty bankovní účty, které mají možnost **Rozšířené odsouhlasení banky** nastaveno na **Ano** na stránce **Bankovní účet**.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="dc0c2-116">Z části **Souhrn** můžete importovat elektronické bankovní soubory pro bankovní účty napříč všemi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="dc0c2-117">Bankovní účty</span><span class="sxs-lookup"><span data-stu-id="dc0c2-117">Bank accounts</span></span>

<span data-ttu-id="dc0c2-118">Každý bankovní účet v právnické osobě je představován kartou v části **Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="dc0c2-119">Je zobrazen aktuální zůstatek a vy můžete procházet podrobnosti transakcí, které tvoří souhrnnou částku zůstatku.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="dc0c2-120">Částka **Překlenovací transakce** také umožňuje přejít k podrobnostem transakcí, které tvoří souhrnnou částku.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="dc0c2-121">Překlenovací transakce jsou všechny čekající transakce, které byly zaúčtovány pomocí překlenovací funkce, ale které nebyly dosud byly proplaceny.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="dc0c2-122">Částka **Čekající zůstatek** je aktuální zůstatek minus překlenovací, nebo čekající, transakce.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="dc0c2-123">Karta rovněž zobrazuje, kdy byl naposledy bankovní účet odsouhlasen.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="dc0c2-124">Tyto informace se zobrazí pouze tehdy, pokud je povoleno Rozšířené odsouhlasení banky pro bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="dc0c2-125">Rozvaha</span><span class="sxs-lookup"><span data-stu-id="dc0c2-125">Balance</span></span>

<span data-ttu-id="dc0c2-126">Graf **Zůstatek** zobrazuje buď historické informace o zůstatku pro účet zvolený v části **Bankovní účty**, nebo souhrn historických informací o zůstatku pro všechny bankovní účty právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="dc0c2-127">Tyto informace jsou k dispozici pro různá období: aktuální týden, aktuální měsíc, aktuální rok, posledních pět let a všechna období (úplná historie bankovního účtu).</span><span class="sxs-lookup"><span data-stu-id="dc0c2-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="dc0c2-128">Pokud zobrazíte graf **Zůstatek** pro jeden bankovní účet, historické zůstatky jsou zobrazeny v měně bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="dc0c2-129">Pokud zobrazíte graf pro všechny bankovní účty právnické osoby, historické zůstatky jsou zobrazeny v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="dc0c2-130">Informace o poslední aktualizaci dat se zobrazí v horní části grafu.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="dc0c2-131">Můžete data aktualizovat podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="dc0c2-132">Související informace</span><span class="sxs-lookup"><span data-stu-id="dc0c2-132">Related information</span></span>

<span data-ttu-id="dc0c2-133">Z části **Související informace** je možné otevřít stránku **Hlavní deníku** pro dokončení bankovních převodů.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="dc0c2-134">Můžete otevřít rychle také stránky **Bankovní transakce** a **Překlenovací transakce**.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="dc0c2-135">Zobrazení analýzy</span><span class="sxs-lookup"><span data-stu-id="dc0c2-135">Analytics view</span></span>

<span data-ttu-id="dc0c2-136">Stránka **Analýza** poskytuje důležité metriky o bankovních účtech v aktuální společnosti.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="dc0c2-137">Na stránce jsou k dispozici následující vizualizace:</span><span class="sxs-lookup"><span data-stu-id="dc0c2-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="dc0c2-138">Celkový bankovní zůstatek v měně systému</span><span class="sxs-lookup"><span data-stu-id="dc0c2-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="dc0c2-139">Zůstatek podle právnické osoby</span><span class="sxs-lookup"><span data-stu-id="dc0c2-139">Balance by legal entity</span></span>
-   <span data-ttu-id="dc0c2-140">Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="dc0c2-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="dc0c2-141">Zůstatek podle bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="dc0c2-141">Balance by bank account</span></span>
-   <span data-ttu-id="dc0c2-142">Zůstatek podle měny</span><span class="sxs-lookup"><span data-stu-id="dc0c2-142">Balance by currency</span></span>

<span data-ttu-id="dc0c2-143">Zobrazit bankovní analýzu napříč všemi společnostmi můžete z pracovního prostoru **Přehled hotovosti – všechny společnosti**.</span><span class="sxs-lookup"><span data-stu-id="dc0c2-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span>
