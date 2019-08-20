---
title: Vytvoření a přiřazení struktur rozšířeného pravidla
description: Toto téma vysvětluje, jak vytvořit pokročilou strukturu pravidel a přiřadit ji k účetní struktuře.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834878"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="2444a-103">Vytvoření a přiřazení struktur rozšířeného pravidla</span><span class="sxs-lookup"><span data-stu-id="2444a-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2444a-104">Toto téma vysvětluje, jak vytvořit pokročilou strukturu pravidel a přiřadit ji k účetní struktuře.</span><span class="sxs-lookup"><span data-stu-id="2444a-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="2444a-105">Tento průvodce používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="2444a-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="2444a-106">Vytvořit strukturu rozšířeného pravidla</span><span class="sxs-lookup"><span data-stu-id="2444a-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="2444a-107">Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Účetní osnovy > Struktury > Pokročilé struktury pravidel**.</span><span class="sxs-lookup"><span data-stu-id="2444a-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="2444a-108">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2444a-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="2444a-109">V poli **Rozšířené struktury pravidel** zadejte název k popisu struktury pravidla.</span><span class="sxs-lookup"><span data-stu-id="2444a-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="2444a-110">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2444a-110">Select **OK**.</span></span>
5. <span data-ttu-id="2444a-111">Vyberte **Přidat segment**.</span><span class="sxs-lookup"><span data-stu-id="2444a-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="2444a-112">V seznamu segmentů vyberte finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="2444a-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="2444a-113">Například **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="2444a-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="2444a-114">Vyberte **Přidat segment**.</span><span class="sxs-lookup"><span data-stu-id="2444a-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="2444a-115">Vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="2444a-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="2444a-116">Použití struktury rozšířeného pravidla na účetní strukturu</span><span class="sxs-lookup"><span data-stu-id="2444a-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="2444a-117">Přejděte na **navigační podokno > Moduly > Hlavní kniha > Účetní osnovy > Struktury > Konfigurovat účetní struktury**.</span><span class="sxs-lookup"><span data-stu-id="2444a-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="2444a-118">V seznamu vyhledejte a vyberte účetní struktury, na které chcete uplatnit rozšířené pravidlo.</span><span class="sxs-lookup"><span data-stu-id="2444a-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="2444a-119">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="2444a-119">Select **Edit**.</span></span> <span data-ttu-id="2444a-120">Můžete také vybrat **Pokročilá pravidla** a budete vyzváni vložit účetní strukturu v **režimu konceptu**.</span><span class="sxs-lookup"><span data-stu-id="2444a-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="2444a-121">Vyberte **Upřesnit pravidla**.</span><span class="sxs-lookup"><span data-stu-id="2444a-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="2444a-122">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2444a-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="2444a-123">Zadejte hodnotu do pole **Upřesnit pravidlo**.</span><span class="sxs-lookup"><span data-stu-id="2444a-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="2444a-124">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="2444a-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="2444a-125">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="2444a-125">Select **Create**.</span></span>
9. <span data-ttu-id="2444a-126">Vyberte **Přidat nová kritéria**.</span><span class="sxs-lookup"><span data-stu-id="2444a-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="2444a-127">V poli **Kde** vyberte hlavní účet nebo finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="2444a-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="2444a-128">V poli **Operátor** vyberte možnost, jako **je mezi** a **zahrnuje**.</span><span class="sxs-lookup"><span data-stu-id="2444a-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="2444a-129">Zadejte hodnotu do pole **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="2444a-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="2444a-130">Zadejte hodnotu do pole **prostřednictvím**.</span><span class="sxs-lookup"><span data-stu-id="2444a-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="2444a-131">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="2444a-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="2444a-132">V seznamu vyhledejte pokročilé pravidlo, které chcete použít, když jsou splněna zadaná kritéria.</span><span class="sxs-lookup"><span data-stu-id="2444a-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="2444a-133">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="2444a-133">Select **Add**.</span></span>
17. <span data-ttu-id="2444a-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2444a-134">Close the page.</span></span>
18. <span data-ttu-id="2444a-135">Vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="2444a-135">Select **Activate**.</span></span>

