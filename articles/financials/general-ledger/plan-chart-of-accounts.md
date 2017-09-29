---
title: "Plánování účtové osnovy"
description: "V tomto článku jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="3e81b-103">Plánování účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="3e81b-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3e81b-104">V tomto článku jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="3e81b-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="3e81b-105">Pro sledování a správu finančních informací v organizaci můžete nastavit účtovou osnovu.</span><span class="sxs-lookup"><span data-stu-id="3e81b-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="3e81b-106">Účtová osnova je sada účtů, které definují finanční rámec.</span><span class="sxs-lookup"><span data-stu-id="3e81b-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="3e81b-107">Pokud chcete dále sledovat transakce v těchto účtech, můžete přidat segmenty označované jako finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="3e81b-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="3e81b-108">Účet výdajů může například zahrnovat finanční dimenze s názvem Oddělení, Nákladové středisko a Účel.</span><span class="sxs-lookup"><span data-stu-id="3e81b-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="3e81b-109">Pravidla definovaná uživatelem, která se označují jako účetní struktury a rozšířená pravidla, určují způsob, jakým se finanční dimenze přiřazují k hlavním účtům a ostatním finančním dimenzím a jakým se zadávají transakce pro účetní strukturu.</span><span class="sxs-lookup"><span data-stu-id="3e81b-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="3e81b-110">Účtová osnova představuje strukturovaný seznam účtů hlavní knihy právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="3e81b-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="3e81b-111">Tento seznam se používá pro přípravu finančního vykazování pro úřady a majitele.</span><span class="sxs-lookup"><span data-stu-id="3e81b-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="3e81b-112">Účty se seskupují do typů účtů a obecných kategorií.</span><span class="sxs-lookup"><span data-stu-id="3e81b-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="3e81b-113">Nejobecnější úroveň účty třídí jako výnosy a náklady (účty provozních nákladů) a aktiva a pasiva (rozvahový účet).</span><span class="sxs-lookup"><span data-stu-id="3e81b-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="3e81b-114">Účtovou osnovu mohou sdílet a používat všechny právnické osoby v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="3e81b-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="3e81b-115">Účtové osnovy, které používá právnická osoba, jsou definovány na stránce **Kniha**.</span><span class="sxs-lookup"><span data-stu-id="3e81b-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="3e81b-116">Zde je několik faktorů, které je třeba brát v potaz při plánování struktury účtové osnovy ve vaší organizaci:</span><span class="sxs-lookup"><span data-stu-id="3e81b-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="3e81b-117">požadavky na výkazy v zemi nebo oblasti, ve které má společnost sídlo,</span><span class="sxs-lookup"><span data-stu-id="3e81b-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="3e81b-118">požadavky na výkazy vaší právnické osoby,</span><span class="sxs-lookup"><span data-stu-id="3e81b-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="3e81b-119">úroveň podrobností, kterou požadují jak externí organizace, tak i vaše společnost.</span><span class="sxs-lookup"><span data-stu-id="3e81b-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="3e81b-120">Na stránce **Účtová osnova** vytvořte účtovou osnovu.</span><span class="sxs-lookup"><span data-stu-id="3e81b-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="3e81b-121">Hlavní účty lze vytvořit na stránce **Účtové osnovy** nebo **Hlavní účty**.</span><span class="sxs-lookup"><span data-stu-id="3e81b-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="3e81b-122">V hlavních účtech nepoužívejte zvláštní znaky, které se používají jako oddělovače účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="3e81b-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="3e81b-123">Pokud použijete zvláštní znak, který se shoduje s oddělovačem účtové osnovy, můžete zaznamenat nestabilitu nebo nutnost používat vyhledávání či plovoucí panel pokaždé, když zadáváte kombinací účtů a dimenzí.</span><span class="sxs-lookup"><span data-stu-id="3e81b-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="3e81b-124">Další informace naleznete v tématu [Vytvoření hlavního účtu](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="3e81b-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="3e81b-125">Je vhodné propojit hlavní účty s kategoriemi hlavních účtů, abyste mohli využít výhody výchozích finančních sestav bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="3e81b-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="3e81b-126">Můžete proto rychleji a snáze navrhovat a spravovat sestavy.</span><span class="sxs-lookup"><span data-stu-id="3e81b-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="3e81b-127">Pomocí stránky **Konfigurovat účetní struktury** vytvořte účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="3e81b-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="3e81b-128">Účetní struktury definují platné kombinace.</span><span class="sxs-lookup"><span data-stu-id="3e81b-128">Account structures define valid combinations.</span></span> <span data-ttu-id="3e81b-129">Kombinace, společně s hlavními účty, tvoří účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="3e81b-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="3e81b-130">Další informace naleznete v tématu [Vytvoření struktur účtu](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="3e81b-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="3e81b-131">**Přepisy právnických osob**</span><span class="sxs-lookup"><span data-stu-id="3e81b-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="3e81b-132">Ne všechny hlavní účty platí pro všechny právnické osoby a některé mohou být relevantní pouze pro určité časové období.</span><span class="sxs-lookup"><span data-stu-id="3e81b-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="3e81b-133">V tomto případě lze část Přepisy právnických osob použít k určení, u kterých společností by mělo být použití hlavního účtu pozastaveno, kdo je vlastníkem a časové období aktivity dimenze.</span><span class="sxs-lookup"><span data-stu-id="3e81b-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="3e81b-134">Přepisy na sdílené úrovni nemohou být více omezující než přepisy na úrovni právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="3e81b-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="3e81b-135">Další informace naleznete v následujících tématech: [Finanční dimenze](financial-dimensions.md)
[Vytvoření a přiřazení rozšířené struktury pravidel](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="3e81b-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




