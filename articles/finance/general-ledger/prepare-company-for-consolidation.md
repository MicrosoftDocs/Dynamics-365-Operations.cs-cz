---
title: Připravit právnickou osobu pro proces konsolidace
description: Při konsolidaci shromáždíte transakce z několika sad účtů právnické osoby do jediné sady účtů právnické osoby. Toto téma vysvětluje, jak připravit právnickou osobu na konsolidaci.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990290"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="1b1a2-104">Připravit právnickou osobu pro proces konsolidace</span><span class="sxs-lookup"><span data-stu-id="1b1a2-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b1a2-105">Při konsolidaci shromáždíte transakce z několika sad účtů právnické osoby do jediné sady účtů právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="1b1a2-106">Toto téma vysvětluje, jak připravit právnickou osobu na konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="1b1a2-107">Doporučujeme použít Management Reporter pro Microsoft Dynamics 365 Finance, chcete-li kombinovat finanční výsledky pro více právnických osob v konsolidovaném formátu.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="1b1a2-108">Management Reporter vám umožňuje vytvářet konsolidované finanční výkazy napříč právnickými osobami, používat Excel k importu konsolidačních dat z jiných zdrojů a převádět částky do libovolného počtu měn vykazování, aniž byste museli spouštět proces konsolidace v Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="1b1a2-109">Lze vytisknout sestavy, například finanční výkazy, z konsolidované právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="1b1a2-110">Konsolidovanou právnickou osobu však nelze použít pro denní transakce.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="1b1a2-111">Můžete konsolidovat data z právnické osoby, která používá jiné databáze než konsolidovaná právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="1b1a2-112">Tento proces konsolidace je označován jako *konsolidace importu*.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="1b1a2-113">Právnické osoby mohou rovněž používat stejnou databázi jako konsolidovaná právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="1b1a2-114">Tento proces konsolidace je označován jako *online konsolidace.*</span><span class="sxs-lookup"><span data-stu-id="1b1a2-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="1b1a2-115">Konsolidovaná právnická osoba shromažďuje výsledky a zůstatky dceřiných společností.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="1b1a2-116">Při přípravě konsolidované právnické osoby ke konsolidaci je nutné postupovat takto.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="1b1a2-117">Přejděte do části **Hlavní knika \> Nastavení \> Organizace \> Právnické osoby**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="1b1a2-118">Vyberte **Nová** a vytvořte právnickou osobu, která bude konsolidovanou právnickou osobou.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="1b1a2-119">Zaškrtněte políčko **Použijte pro proces finanční konsolidace** a poté zadejte informace o konsolidované právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="1b1a2-120">Zadejte tento údaj přesně tak, jak se má zobrazovat na finančních výpisech konsolidované právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="1b1a2-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-121">Close the page.</span></span>
5. <span data-ttu-id="1b1a2-122">Vyberte konsolidovanou právnickou osobu v poli v pravém horním rohu stránky a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="1b1a2-123">Přejděte do části **Hlavní kniha \> Nastavení \> Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="1b1a2-124">Vyberte účtovou osnovu, fiskální kalendář, zúčtovací měnu, volitelnou měnu vykazování a výchozí typ směnného kurzu pro konsolidovanou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="1b1a2-125">Přejděte do části **Hlavní kniha \> Nastavení \> Měna \> Směnné kurzy**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="1b1a2-126">Nastavte směnné kurzy měny v relevantních obdobích pro měny dceřiných právnických osob.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="1b1a2-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-127">Close the page.</span></span>
11. <span data-ttu-id="1b1a2-128">Má-li konsolidovaná právnická osoba dceřiné společnosti, které používají cizí měny, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="1b1a2-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="1b1a2-129">Přejděte do části **Hlavní kniha \> Nastavení \> Účtování \> Účty pro automatické transakce**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="1b1a2-130">V poli **Typ zaúčtování** vyberte příslušný účet:</span><span class="sxs-lookup"><span data-stu-id="1b1a2-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="1b1a2-131">Pokud má právnická osoba zahraniční dceřiné společnosti, které jsou finančně nebo provozně závislé na mateřské právnické osobě, vyberte vhodný účet pro typ zaúčtování **Účet zisku a ztráty pro konsolidační rozdíly**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="1b1a2-132">Jestliže konsolidujete dceřinou společnost, která nezávisí finančně ani provozně na nadřazené právnické osobě, nebo právnickou osobu obsahující výsledky několika dceřiných společností, které nezávisí finančně ani provozně na nadřazené právnické osobě, a pokud používáte metody převodu ke konsolidaci dat, vyberte odpovídající účet pro typ zaúčtování **Protiúčet pro konsolidační rozdíly**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="1b1a2-133">V poli **Hlavní účet** vyberte hlavní účty, které by se měly použít pro úpravy přecenění cizí měny.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="1b1a2-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-134">Close the page.</span></span>

    <span data-ttu-id="1b1a2-135">Pokud vytvoříte konsolidovanou právnickou osobu na začátku období, je možné přecenit částky v cizí měně tak, jak se budou během období konsolidace měnit směnné kurzy.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="1b1a2-136">Konsolidovaná právnická osoba je nyní nastavena pro periodickou úlohu **Konsolidace**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="1b1a2-137">Můžete provést konsolidaci importu nebo konsolidaci online.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="1b1a2-138">Chcete-li provést konsolidaci importu, přejděte na **Hlavní kniha \> Periodické \> Konsolidace \> Konsolidace \[Importovat z\]**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="1b1a2-139">Chcete-li provést online konsolidaci, přejděte na **Hlavní kniha \> Periodické \> Konsolidace \> Konsolidace \[Online\]**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="1b1a2-140">Před zpracováním konsolidace musíte připravit právnické osoby dceřiné společnosti na konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="1b1a2-141">Další informace viz [Založení dceřiné právnické osoby ke konsolidaci](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="1b1a2-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>
