---
title: Definování pravidel a zásad nároků na zaměstnanecké výhody
description: Tento článek uvádí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 39a9a1c96ae2a12a32b3c5fbc67571bcf983c898
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467980"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="31613-103">Definování pravidel a zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="31613-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="31613-104">Toto téma uvádí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám.</span><span class="sxs-lookup"><span data-stu-id="31613-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="31613-105">Vytvoření typu pravidel zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="31613-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="31613-106">Přejděte na **Lidské zdroje > Výhody > Nárok > Typy pravidel zásad nároků na zaměstnanecké výhody**.</span><span class="sxs-lookup"><span data-stu-id="31613-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="31613-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="31613-107">Select **New**.</span></span>
3. <span data-ttu-id="31613-108">Zadejte hodnotu do pole **Název pravidla**.</span><span class="sxs-lookup"><span data-stu-id="31613-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="31613-109">V poli **Popis** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="31613-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="31613-110">V poli **Název dotazu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="31613-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="31613-111">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="31613-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="31613-112">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="31613-112">Select **Save**.</span></span>
8. <span data-ttu-id="31613-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="31613-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="31613-114">Zásady nároku na zaměstnaneckou výhodu</span><span class="sxs-lookup"><span data-stu-id="31613-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="31613-115">Přejděte na **Lidské zdroje > Výhody > Nárok > Zásady způsobilosti k zaměstnaneckým výhodám**.</span><span class="sxs-lookup"><span data-stu-id="31613-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="31613-116">Vyberte existující zásady pro zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="31613-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="31613-117">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="31613-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="31613-118">Přepněte rozšíření oddílů **Organizace zásad**.</span><span class="sxs-lookup"><span data-stu-id="31613-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="31613-119">Zde můžete přidat nebo odebrat všechny organizace, které chcete zahrnout do zásad.</span><span class="sxs-lookup"><span data-stu-id="31613-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="31613-120">Rozbalte nebo sbalte část **Pravidla zásad**.</span><span class="sxs-lookup"><span data-stu-id="31613-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="31613-121">V seznamu vyhledejte pravidlo zásad, které již bylo vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="31613-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="31613-122">Vyberte **Vytvořit pravidlo zásad**.</span><span class="sxs-lookup"><span data-stu-id="31613-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="31613-123">Do pole **Datum platnosti** zadejte datum, ke kterému chcete, aby tato zásada zahájila platnost.</span><span class="sxs-lookup"><span data-stu-id="31613-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="31613-124">Nastavení data platnosti a koncového data umožňuje provádět v budoucnu změny v pravidlech zásad a odstranit potřebu vracet se k zásadám, když budete chtít, aby se tyto změny projevily.</span><span class="sxs-lookup"><span data-stu-id="31613-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="31613-125">V případě potřeby přidejte klauzuli where do pole **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="31613-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="31613-126">Například pokud byste chtěli, aby se pravidlo vztahovalo pouze na manažery prodeje, je možné vytvořit klauzuli Where, tj.: popis pozice Where obsahuje manažera prodeje.</span><span class="sxs-lookup"><span data-stu-id="31613-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="31613-127">Je možné používat logické výrazy And pro více výroků Where současně v pravidle.</span><span class="sxs-lookup"><span data-stu-id="31613-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="31613-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="31613-128">Select **OK**.</span></span>
11. <span data-ttu-id="31613-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="31613-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="31613-130">Přiřazení pravidla k zaměstnaneckým výhodám</span><span class="sxs-lookup"><span data-stu-id="31613-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="31613-131">Přejděte k nabídce **Lidské zdroje > Výhody > Výhody**.</span><span class="sxs-lookup"><span data-stu-id="31613-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="31613-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="31613-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="31613-133">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="31613-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="31613-134">Rozbalte nebo sbalte část **Pravidla způsobilosti**.</span><span class="sxs-lookup"><span data-stu-id="31613-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="31613-135">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="31613-135">Select **Edit**.</span></span>
6. <span data-ttu-id="31613-136">V poli **Nárok** vyberte pravidlo.</span><span class="sxs-lookup"><span data-stu-id="31613-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="31613-137">V poli **Typ pravidla** vyberte vytvořené pravidlo.</span><span class="sxs-lookup"><span data-stu-id="31613-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="31613-138">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="31613-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="31613-139">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="31613-139">Select **Save**.</span></span>
11. <span data-ttu-id="31613-140">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="31613-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]