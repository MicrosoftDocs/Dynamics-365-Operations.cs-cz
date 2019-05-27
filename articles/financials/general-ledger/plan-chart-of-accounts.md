---
title: Plánování účetní osnovy
description: V tomto tématu jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93d5ef19a4b1cb2885c611c8675ac06fd841ac56
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556632"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="dd479-103">Plánování účetní osnovy</span><span class="sxs-lookup"><span data-stu-id="dd479-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd479-104">V tomto tématu jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="dd479-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="dd479-105">Pro sledování a správu finančních informací v organizaci můžete nastavit účtovou osnovu.</span><span class="sxs-lookup"><span data-stu-id="dd479-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="dd479-106">Účtová osnova je sada účtů, které definují finanční rámec.</span><span class="sxs-lookup"><span data-stu-id="dd479-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="dd479-107">Pokud chcete dále sledovat transakce na těchto účtech, můžete přidat segmenty.</span><span class="sxs-lookup"><span data-stu-id="dd479-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="dd479-108">Tyto segmenty se označují jako finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="dd479-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="dd479-109">Účet výdajů může například zahrnovat finanční dimenze s názvem Oddělení, Nákladové středisko a Účel.</span><span class="sxs-lookup"><span data-stu-id="dd479-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="dd479-110">Pravidla definovaná uživatelem určují způsob, jakým se finanční dimenze přiřazují k hlavním účtům a ostatním finančním dimenzím a jakým se zadávají transakce pro účetní strukturu.</span><span class="sxs-lookup"><span data-stu-id="dd479-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="dd479-111">Tato pravidla definovaná uživatelem se nazývají účetní struktury a pokročilá pravidla.</span><span class="sxs-lookup"><span data-stu-id="dd479-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="dd479-112">Účtová osnova představuje strukturovaný seznam účtů hlavní knihy právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="dd479-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="dd479-113">Tento seznam se používá pro přípravu finančního vykazování pro úřady a majitele.</span><span class="sxs-lookup"><span data-stu-id="dd479-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="dd479-114">Účty se nejprve seskupují do typů účtů a obecných kategorií.</span><span class="sxs-lookup"><span data-stu-id="dd479-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="dd479-115">Nejobecnější úroveň účty třídí jako výnosy a náklady (účty provozních nákladů) a aktiva a pasiva (rozvahový účet).</span><span class="sxs-lookup"><span data-stu-id="dd479-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="dd479-116">Účtovou osnovu mohou sdílet a používat všechny právnické osoby v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="dd479-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="dd479-117">Účtové osnovy, které používá právnická osoba, jsou definovány na stránce **Kniha**.</span><span class="sxs-lookup"><span data-stu-id="dd479-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="dd479-118">Zde je několik faktorů, které je třeba brát v potaz při plánování struktury účtové osnovy ve vaší organizaci:</span><span class="sxs-lookup"><span data-stu-id="dd479-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="dd479-119">požadavky na výkazy v zemi nebo oblasti, ve které má společnost sídlo,</span><span class="sxs-lookup"><span data-stu-id="dd479-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="dd479-120">požadavky na výkazy vaší právnické osoby,</span><span class="sxs-lookup"><span data-stu-id="dd479-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="dd479-121">úroveň podrobností, kterou požadují jak externí organizace, tak i vaše společnost.</span><span class="sxs-lookup"><span data-stu-id="dd479-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="dd479-122">Na stránce **Účtová osnova** vytvořte účtovou osnovu.</span><span class="sxs-lookup"><span data-stu-id="dd479-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="dd479-123">Hlavní účty lze vytvořit na stránce **Účtové osnovy** nebo **Hlavní účty**.</span><span class="sxs-lookup"><span data-stu-id="dd479-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="dd479-124">V hlavních účtech nepoužívejte zvláštní znaky, které se používají jako oddělovače účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="dd479-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="dd479-125">V opačném případě může dojít k nestabilitě nebo je třeba vždy použít vyhledávání, resp. při zadávání kombinací účtů a dimenzí.</span><span class="sxs-lookup"><span data-stu-id="dd479-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="dd479-126">Další informace naleznete v tématu [Vytvoření hlavního účtu](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="dd479-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="dd479-127">V aplikaci Microsoft Dynamics for Finance and Operations verze 8.0 (duben 2018) můžete změnit oddělovač účtové osnovy ze stránky **Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="dd479-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="dd479-128">Je vhodné propojit hlavní účty s kategoriemi hlavních účtů, abyste mohli využít výhody výchozích finančních sestav bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="dd479-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="dd479-129">Můžete proto rychleji a snáze navrhovat a spravovat sestavy.</span><span class="sxs-lookup"><span data-stu-id="dd479-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="dd479-130">Pomocí stránky **Konfigurovat účetní struktury** vytvořte účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="dd479-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="dd479-131">Účetní struktury definují platné kombinace.</span><span class="sxs-lookup"><span data-stu-id="dd479-131">Account structures define valid combinations.</span></span> <span data-ttu-id="dd479-132">Tyto kombinace, společně s hlavními účty, tvoří účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="dd479-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="dd479-133">Další informace naleznete v tématu [Vytvoření struktur účtu](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="dd479-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="dd479-134">**Přepisy právnických osob**</span><span class="sxs-lookup"><span data-stu-id="dd479-134">**Legal entity overrides**</span></span>

<span data-ttu-id="dd479-135">Ne všechny hlavní účty platí pro všechny právnické osoby a některé mohou být relevantní pouze pro určité časové období.</span><span class="sxs-lookup"><span data-stu-id="dd479-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="dd479-136">V tomto případě lze pomocí části **Přepisy právnických osob** určit společnosti, u kterých má být použití hlavního účtu pozastaveno, kdo je vlastníkem a období aktivity dimenze.</span><span class="sxs-lookup"><span data-stu-id="dd479-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="dd479-137">Přepisy na sdílené úrovni nemohou být více omezující než přepisy na úrovni právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="dd479-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="dd479-138">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="dd479-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="dd479-139">Finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="dd479-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="dd479-140">Vytvoření a přiřazení struktur rozšířeného pravidla</span><span class="sxs-lookup"><span data-stu-id="dd479-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)
