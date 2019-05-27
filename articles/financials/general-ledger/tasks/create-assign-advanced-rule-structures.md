---
title: Vytvoření a přiřazení struktur rozšířeného pravidla
description: Tento průvodce úkoly vás provede vytvářením a přiřazením struktury rozšířeného pravidla do účetní struktury.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558899"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="f22a5-103">Vytvoření a přiřazení struktur rozšířeného pravidla</span><span class="sxs-lookup"><span data-stu-id="f22a5-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f22a5-104">Tento průvodce úkoly vás provede vytvářením a přiřazením struktury rozšířeného pravidla do účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="f22a5-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="f22a5-105">Tento průvodce používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="f22a5-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="f22a5-106">Vytvořit strukturu rozšířeného pravidla</span><span class="sxs-lookup"><span data-stu-id="f22a5-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="f22a5-107">Přejděte do části Hlavní kniha > Účtová osnova > Struktury > Rozšířené struktury pravidel.</span><span class="sxs-lookup"><span data-stu-id="f22a5-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="f22a5-108">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="f22a5-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="f22a5-109">V poli Rozšířené struktury pravidel zadejte název k popisu struktury pravidla.</span><span class="sxs-lookup"><span data-stu-id="f22a5-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="f22a5-110">V poli Popis zadejte hodnotu k popisu struktury.</span><span class="sxs-lookup"><span data-stu-id="f22a5-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="f22a5-111">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f22a5-111">Click OK.</span></span>
6. <span data-ttu-id="f22a5-112">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="f22a5-112">Click Add segment.</span></span>
7. <span data-ttu-id="f22a5-113">V seznamu segmentů vyberte finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="f22a5-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="f22a5-114">Například Obchod.</span><span class="sxs-lookup"><span data-stu-id="f22a5-114">For example, Store.</span></span>  
8. <span data-ttu-id="f22a5-115">Klepněte na Přidat segment.</span><span class="sxs-lookup"><span data-stu-id="f22a5-115">Click Add segment.</span></span>
9. <span data-ttu-id="f22a5-116">Pro zobrazení klepněte v seznamu na odkaz struktura rozšířeného pravidla.</span><span class="sxs-lookup"><span data-stu-id="f22a5-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="f22a5-117">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="f22a5-117">Click Activate.</span></span>
11. <span data-ttu-id="f22a5-118">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="f22a5-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="f22a5-119">Použití struktury rozšířeného pravidla na účetní strukturu</span><span class="sxs-lookup"><span data-stu-id="f22a5-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="f22a5-120">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="f22a5-120">Close the form.</span></span>
2. <span data-ttu-id="f22a5-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f22a5-121">Close the page.</span></span>
3. <span data-ttu-id="f22a5-122">Přejděte do části Hlavní kniha > Účtová osnova > Struktury > Konfigurovat účetní struktury.</span><span class="sxs-lookup"><span data-stu-id="f22a5-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="f22a5-123">V seznamu vyhledejte a vyberte účetní struktury, na které chcete uplatnit rozšířené pravidlo.</span><span class="sxs-lookup"><span data-stu-id="f22a5-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="f22a5-124">Účetní strukturu otevřete klepnutím na její název.</span><span class="sxs-lookup"><span data-stu-id="f22a5-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="f22a5-125">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="f22a5-125">Click Edit.</span></span>
    * <span data-ttu-id="f22a5-126">Můžete také klepnout na Rozšířená pravidla a budete vyzváni vložit účetní strukturu do stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="f22a5-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="f22a5-127">Klepněte na Rozšířená pravidla.</span><span class="sxs-lookup"><span data-stu-id="f22a5-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="f22a5-128">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="f22a5-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="f22a5-129">Zadejte hodnotu do pole Rozšířené pravidlo.</span><span class="sxs-lookup"><span data-stu-id="f22a5-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="f22a5-130">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="f22a5-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="f22a5-131">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="f22a5-131">Click Create.</span></span>
12. <span data-ttu-id="f22a5-132">Klepněte na Přidat nová kritéria.</span><span class="sxs-lookup"><span data-stu-id="f22a5-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="f22a5-133">V poli Kde vyberte hlavní účet nebo finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="f22a5-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="f22a5-134">V poli Operátor vyberte možnost, jako je „mezi“ a „zahrnuje“.</span><span class="sxs-lookup"><span data-stu-id="f22a5-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="f22a5-135">Zadejte hodnotu do pole Hodnota.</span><span class="sxs-lookup"><span data-stu-id="f22a5-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="f22a5-136">Zadejte hodnotu do pole „prostřednictvím“.</span><span class="sxs-lookup"><span data-stu-id="f22a5-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="f22a5-137">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="f22a5-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="f22a5-138">V seznamu vyhledejte pokročilé pravidlo, které chcete použít, když jsou splněna zadaná kritéria.</span><span class="sxs-lookup"><span data-stu-id="f22a5-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="f22a5-139">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="f22a5-139">Click Add.</span></span>
20. <span data-ttu-id="f22a5-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f22a5-140">Close the page.</span></span>
21. <span data-ttu-id="f22a5-141">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="f22a5-141">Click Activate.</span></span>
22. <span data-ttu-id="f22a5-142">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="f22a5-142">Click Activate.</span></span>

