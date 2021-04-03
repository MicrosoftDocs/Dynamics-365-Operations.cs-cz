---
title: Postup přípravy na správu standardních nákladů pro vyráběné položky
description: Toto téma popisuje kroky pro přípravu správy nákladů pro vyráběné položky.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f428f2e3966155b4fc95fd94b6a55d059eb3533d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263511"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="07f1d-103">Postup přípravy na správu standardních nákladů pro vyráběné položky</span><span class="sxs-lookup"><span data-stu-id="07f1d-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07f1d-104">Toto téma popisuje kroky pro přípravu správy nákladů pro vyráběné položky.</span><span class="sxs-lookup"><span data-stu-id="07f1d-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="07f1d-105">Kroky pro vyrobené položky se mírně liší od kroků pro zakoupené položky.</span><span class="sxs-lookup"><span data-stu-id="07f1d-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="07f1d-106">Zásady přiřazené vyráběným položkám mohou mít vliv na výpočty nákladů pro nadřazené vyráběné položky.</span><span class="sxs-lookup"><span data-stu-id="07f1d-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="07f1d-107">Chcete-li připravit na správu nákladů vyráběných položek, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="07f1d-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="07f1d-108">Přiřaďte k vyráběné položce skupinu modelů položky.</span><span class="sxs-lookup"><span data-stu-id="07f1d-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="07f1d-109">Skupina modelů položky identifikuje použití standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="07f1d-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="07f1d-110">Přiřaďte k vyráběné položce skupinu položek.</span><span class="sxs-lookup"><span data-stu-id="07f1d-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="07f1d-111">Skupina položek obsahuje účty hlavní knihy, které se týkají vyráběné položky.</span><span class="sxs-lookup"><span data-stu-id="07f1d-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="07f1d-112">Účty hlavní knihy pro vyráběnou položku se standardním modelem skladových nákladů zahrnují několik výrobních odchylek, odchylku změn nákladů a přecenění nákladů skladu.</span><span class="sxs-lookup"><span data-stu-id="07f1d-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="07f1d-113">Přiřaďte k položce měrnou jednotku zásob.</span><span class="sxs-lookup"><span data-stu-id="07f1d-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="07f1d-114">Náklady položky jsou vždy vyjádřeny v měrných jednotkách zásob pro danou položku.</span><span class="sxs-lookup"><span data-stu-id="07f1d-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="07f1d-115">Nepřiřazujte nákladovou skupinu k vyráběné položce, s výjimkou případů, kdy tato položka bude zpracována jako zakoupená položka.</span><span class="sxs-lookup"><span data-stu-id="07f1d-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="07f1d-116">Přiřaďte k vyráběné položce skupinu výpočtu kusovníku.</span><span class="sxs-lookup"><span data-stu-id="07f1d-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="07f1d-117">Skupina výpočtu kusovníku položek definuje podmínky použitých upozornění.</span><span class="sxs-lookup"><span data-stu-id="07f1d-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="07f1d-118">Tímto způsobem lze po provedení výpočtu kusovníku vygenerovat zprávy s upozorněním o možných zdrojích chyb výpočtu.</span><span class="sxs-lookup"><span data-stu-id="07f1d-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="07f1d-119">Zpráva s upozorněním může například upozornit na situaci, kdy neexistuje aktivní kusovník nebo postup.</span><span class="sxs-lookup"><span data-stu-id="07f1d-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="07f1d-120">Skupina výpočtů kusovníku obsahuje zásadu pro zastavení rozpadu, která určuje, kdy má být vyrobená položka zpracována jako zakoupená položka.</span><span class="sxs-lookup"><span data-stu-id="07f1d-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="07f1d-121">Přiřaďte k vyráběné položce standardní množství objednávky, pokud má vyráběná položka konstantní náklady.</span><span class="sxs-lookup"><span data-stu-id="07f1d-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="07f1d-122">Standardní množství objednávky je velikost účetní šarže pro amortizaci konstantních nákladů.</span><span class="sxs-lookup"><span data-stu-id="07f1d-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="07f1d-123">Příklady konstatních nákladů zahrnují časy nastavení v operacích postupu a konstantní množství komponent v kusovníku.</span><span class="sxs-lookup"><span data-stu-id="07f1d-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="07f1d-124">Definujte kusovník pro vyráběnou položku.</span><span class="sxs-lookup"><span data-stu-id="07f1d-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="07f1d-125">Pro vyráběnou položku může být definována jedna nebo více verzí kusovníku.</span><span class="sxs-lookup"><span data-stu-id="07f1d-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="07f1d-126">Ověřte, zda požadované verze byly označeny jako schválené a aktivní, a zda mají požadovaná efektivní data.</span><span class="sxs-lookup"><span data-stu-id="07f1d-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="07f1d-127">Verze kusovníku může být platná pro celou společnost nebo pouze pro specifické pracoviště.</span><span class="sxs-lookup"><span data-stu-id="07f1d-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="07f1d-128">Definujte postup pro vyráběnou položku.</span><span class="sxs-lookup"><span data-stu-id="07f1d-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="07f1d-129">Pro vyráběnou položku může být definována jedna nebo více verzí postupu.</span><span class="sxs-lookup"><span data-stu-id="07f1d-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="07f1d-130">Ověřte, zda požadované verze byly označeny jako schválené a aktivní, a zda mají požadovaná efektivní data.</span><span class="sxs-lookup"><span data-stu-id="07f1d-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="07f1d-131">Verze postupu musí být specifická pro určité pracoviště.</span><span class="sxs-lookup"><span data-stu-id="07f1d-131">The route version must be site-specific.</span></span>

<span data-ttu-id="07f1d-132">Pokud chcete použít informace o postupu pro účely nákladů, jsou vyžadovány dodatečné přípravné kroky.</span><span class="sxs-lookup"><span data-stu-id="07f1d-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="07f1d-133">Jako příklad lze uvést kategorie nákladů přiřazené k operacím postupu - musí být správné a úplné.</span><span class="sxs-lookup"><span data-stu-id="07f1d-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="07f1d-134">Související témata</span><span class="sxs-lookup"><span data-stu-id="07f1d-134">Related topics</span></span>
--------

[<span data-ttu-id="07f1d-135">Amortizace konstantních nákladů na vyráběnou položku</span><span class="sxs-lookup"><span data-stu-id="07f1d-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="07f1d-136">Nastavení produktů, které mohou být vyrobeny nebo pořízeny</span><span class="sxs-lookup"><span data-stu-id="07f1d-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]