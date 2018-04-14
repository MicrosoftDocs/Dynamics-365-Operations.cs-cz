--- 
title: "Definování pravidel a zásad nároků na zaměstnanecké výhody"
description: "Tento záznam zobrazí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 807e6a41d603a5327d713d1ab742cc0d961a7784
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="7b72e-103">Definování pravidel a zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="7b72e-103">Define benefit eligibility rules and policies</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b72e-104">Tento záznam zobrazí způsob, jakým můžete vytvořit pravidla nároku na zaměstnanecké výhody a zásady a přiřadit pravidla k zaměstnaneckým výhodám.</span><span class="sxs-lookup"><span data-stu-id="7b72e-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="7b72e-105">K vytvoření tohoto záznamu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="7b72e-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="7b72e-106">Vytvoření typu pravidel zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="7b72e-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="7b72e-107">Přejděte na Lidské zdroje > Výhody > Nárok > Typy pravidel zásad nároků na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="7b72e-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="7b72e-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7b72e-108">Click New.</span></span>
3. <span data-ttu-id="7b72e-109">Zadejte hodnotu do pole Název pravidla.</span><span class="sxs-lookup"><span data-stu-id="7b72e-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="7b72e-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="7b72e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7b72e-111">V poli Název dotazu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7b72e-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7b72e-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7b72e-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7b72e-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7b72e-113">Click Save.</span></span>
8. <span data-ttu-id="7b72e-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7b72e-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="7b72e-115">Zásady nároku na zaměstnaneckou výhodu</span><span class="sxs-lookup"><span data-stu-id="7b72e-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="7b72e-116">Přejděte na Lidské zdroje > Výhody > Nárok > Zásady způsobilosti k zaměstnaneckým výhodám.</span><span class="sxs-lookup"><span data-stu-id="7b72e-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="7b72e-117">Vyberte existující zásady pro zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="7b72e-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="7b72e-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7b72e-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7b72e-119">Přepněte rozšíření oddílů Organizace zásad.</span><span class="sxs-lookup"><span data-stu-id="7b72e-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="7b72e-120">Zde můžete přidat nebo odebrat všechny organizace, které chcete zahrnout do zásad.</span><span class="sxs-lookup"><span data-stu-id="7b72e-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="7b72e-121">Rozbalte nebo sbalte část Pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="7b72e-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="7b72e-122">V seznamu vyhledejte pravidlo zásad, které již bylo vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="7b72e-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="7b72e-123">Klikněte na Vytvořit pravidlo zásad.</span><span class="sxs-lookup"><span data-stu-id="7b72e-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="7b72e-124">Do pole Datum platnosti zadejte datum, ke kterému chcete, aby tato zásada zahájila platnost.</span><span class="sxs-lookup"><span data-stu-id="7b72e-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="7b72e-125">Nastavení data platnosti a koncového data umožňuje provádět v budoucnu změny v pravidlech zásad a odstranit potřebu vracet se k zásadám, když budete chtít, aby se tyto změny projevily.</span><span class="sxs-lookup"><span data-stu-id="7b72e-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="7b72e-126">Například pokud byste chtěli, aby se pravidlo vztahovalo pouze na manažery prodeje, je možné vytvořit klauzuli Where, tj.: popis pozice Where obsahuje manažera prodeje.</span><span class="sxs-lookup"><span data-stu-id="7b72e-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="7b72e-127">Je možné používat logické výrazy And nebo Or pro více výroků Where současně v pravidle.</span><span class="sxs-lookup"><span data-stu-id="7b72e-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="7b72e-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7b72e-128">Click OK.</span></span>
11. <span data-ttu-id="7b72e-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7b72e-129">Close the page.</span></span>
12. <span data-ttu-id="7b72e-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7b72e-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="7b72e-131">Přiřazení pravidla k zaměstnaneckým výhodám</span><span class="sxs-lookup"><span data-stu-id="7b72e-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="7b72e-132">Přejděte k nabídce Lidské zdroje > Výhody > Výhody.</span><span class="sxs-lookup"><span data-stu-id="7b72e-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="7b72e-133">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7b72e-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7b72e-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7b72e-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7b72e-135">Rozbalte nebo sbalte část Pravidla způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="7b72e-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="7b72e-136">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="7b72e-136">Click Edit.</span></span>
6. <span data-ttu-id="7b72e-137">V poli Nárok vyberte ze seznamu možnost „Podle pravidel“.</span><span class="sxs-lookup"><span data-stu-id="7b72e-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="7b72e-138">V poli Typ pravidla kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7b72e-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="7b72e-139">V seznamu vyhledejte a vyberte pravidlo, které již bylo vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="7b72e-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="7b72e-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7b72e-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7b72e-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7b72e-141">Click Save.</span></span>
11. <span data-ttu-id="7b72e-142">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="7b72e-142">Close the form.</span></span>


