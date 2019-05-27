---
title: Auditní porušení zásad a případy
description: Tento článek popisuje, jak jsou generovány případy auditu z porušení pravidel zásad auditu. Dále zahrnuje informace o různých způsobech použití rozsahu dat pro výběr dokumentu v zásadách auditu.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3ed72f829ca4060fe0a4c03b6d4a47a98cdebd6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568817"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="ad811-104">Auditní porušení zásad a případy</span><span class="sxs-lookup"><span data-stu-id="ad811-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad811-105">Tento článek popisuje, jak jsou generovány případy auditu z porušení pravidel zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="ad811-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="ad811-106">Dále zahrnuje informace o různých způsobech použití rozsahu dat pro výběr dokumentu v zásadách auditu.</span><span class="sxs-lookup"><span data-stu-id="ad811-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="ad811-107">Způsob generování případů auditu</span><span class="sxs-lookup"><span data-stu-id="ad811-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="ad811-108">Zásady auditu slouží k identifikaci výkazy výdajů, nákupních objednávek a faktur dodavatele, které nejsou v souladu s obchodními pravidly, která se definují a nakonfigurují jako pravidla zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="ad811-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="ad811-109">Zásady auditu se spouští v dávkovém režimu.</span><span class="sxs-lookup"><span data-stu-id="ad811-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="ad811-110">Při spuštění zásad auditu se všechna pravidla zásad, které jsou součástí zásady, spustí současně.</span><span class="sxs-lookup"><span data-stu-id="ad811-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="ad811-111">Každé pravidlo zásad vyhodnocuje sadu dokumentů.</span><span class="sxs-lookup"><span data-stu-id="ad811-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="ad811-112">Pravidlo zásad vybere dokumenty, které se nacházejí v rozsahu dat pro výběr dokumentu, a přiřadí zadaná kritériím.</span><span class="sxs-lookup"><span data-stu-id="ad811-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="ad811-113">Například jedno pravidlo zásad může vybrat výkazy výdajů, které mají stravování překračující 50,00.</span><span class="sxs-lookup"><span data-stu-id="ad811-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="ad811-114">Jiné pravidlo zásad může vybrat dodavatelské faktury, které jsou splatné určitému dodavateli.</span><span class="sxs-lookup"><span data-stu-id="ad811-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="ad811-115">Pro každý dokument, který je vybrán v sadě, se generuje porušení.</span><span class="sxs-lookup"><span data-stu-id="ad811-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="ad811-116">Toto porušení je záznam, že určitý dokument, jako je například faktura 12345, nesplňuje pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="ad811-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="ad811-117">Vícenásobné záznamy o porušení auditu seskupeny a přidruženy k auditním případům.</span><span class="sxs-lookup"><span data-stu-id="ad811-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="ad811-118">Ve výchozím nastavení se případy pro každou zásadu auditu seskupí podle pravidla zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="ad811-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="ad811-119">V případě potřeby můžete vybrat další kritéria pro seskupování pomocí stránky **Kritéria seskupování případu**.</span><span class="sxs-lookup"><span data-stu-id="ad811-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="ad811-120">Můžete například seskupit záhlaví výdajů podle ID projektu a faktury dodavatele podle účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ad811-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="ad811-121">V takovém případě se všechna porušení záhlaví výdajů se stejným ID projektu seskupí do stejného případu a všechny faktury dodavatele, které mají stejný účet dodavatele, se seskupí do stejného případu.</span><span class="sxs-lookup"><span data-stu-id="ad811-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="ad811-122">U pravidel zásad auditu, která jsou založena na dotazu typu **Duplicitní**, se porušení neseskupují podle pravidla zásad nebo kritérií zadaných na stránce **Kritéria seskupování případu**.</span><span class="sxs-lookup"><span data-stu-id="ad811-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="ad811-123">Místo toho se seskupují podle kritérií, která jsou součástí pravidla zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="ad811-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="ad811-124">Pokud například pravidlo zásad vyhodnocuje ve výkazech výdajů duplicitní výdaje se stelnou částkou, ID obchodníka a datem, všechny výdaje, které mají stejné hodnoty v těchto polích, budou jeden případ.</span><span class="sxs-lookup"><span data-stu-id="ad811-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="ad811-125">Veškeré výdaje, které mají různé hodnoty, budou samostatný případ.</span><span class="sxs-lookup"><span data-stu-id="ad811-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="ad811-126">Auditní případy se po vygenerování zpracují pomocí typických procesů správy případů.</span><span class="sxs-lookup"><span data-stu-id="ad811-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="ad811-127">Časová rozmezí pro výběr dokumentů</span><span class="sxs-lookup"><span data-stu-id="ad811-127">Document selection date ranges</span></span>
<span data-ttu-id="ad811-128">Po spuštění zásad auditu vybere každé pravidlo zásad dokumenty zadaného typu, které mají datum v rámci rozsahu dat pro výběr dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ad811-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="ad811-129">Rozsah dat pro výběr dokumentu je zadán na stránce **Další možnosti**.</span><span class="sxs-lookup"><span data-stu-id="ad811-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="ad811-130">Mnoho dokumentů má přidruženo více než jedno datum.</span><span class="sxs-lookup"><span data-stu-id="ad811-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="ad811-131">Pole data, která pravidlo zásad auditu používá, je zadáno na stránce **Typ pravidla zásad**.</span><span class="sxs-lookup"><span data-stu-id="ad811-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="ad811-132">Zde je několik dalších způsobů, které zásady auditu používají u rozsahu dat pro výběr dokumentu:</span><span class="sxs-lookup"><span data-stu-id="ad811-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="ad811-133">Zásady použijí verzi pravidla zásad, která je platná k poslednímu dni rozsahu dat pro výběr dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ad811-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="ad811-134">Data účinnosti můžete pro každé pravidlo zásad zobrazit na stránce se seznamem **Zásady auditu**.</span><span class="sxs-lookup"><span data-stu-id="ad811-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="ad811-135">Zásady používají organizační uzly, které jsou přidruženy k zásadám v poslední den rozsahu dat pro výběr dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ad811-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="ad811-136">Pouze organizační uzly, které jsou aktuálně přidruženy k zásadám, se zobrazují na stránce se seznamem **Zásady auditu**.</span><span class="sxs-lookup"><span data-stu-id="ad811-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="ad811-137">Pro pravidla zásad, která jsou založena na typu dotazu **Vyhledávání seznamu**, pravidla vyhodnocují v dokumentech sledované entity, které jsou účinné v poslední den rozsahu dat pro výběr dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ad811-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="ad811-138">Další informace naleznete v tématu [Pravidla zásad auditu](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="ad811-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>



