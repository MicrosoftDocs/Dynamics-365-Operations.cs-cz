---
title: Schválení dodavatelů pro konkrétní produkty
description: Tento postup popisuje způsob schválení dodavatelů pro určité produkty.
author: mkirknel
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 815d968b37cf285544799735fdd3f00f0c7ebffb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838159"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="ef1c5-103">Schválení dodavatelů pro konkrétní produkty</span><span class="sxs-lookup"><span data-stu-id="ef1c5-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef1c5-104">Tento postup popisuje způsob schválení dodavatelů pro určité produkty.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="ef1c5-105">Tímto způsobem lze určit, které dodavatele lze použít při přidání produktu do nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="ef1c5-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="ef1c5-107">Tento úkol obvykle provádí manažer nákupu.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="ef1c5-108">V navigačním podokně přejděte na **Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="ef1c5-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ef1c5-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ef1c5-111">Rozbalte pevnou záložku **Nákup**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="ef1c5-112">Pokud je v poli **Dodavatel** zobrazen primární dodavatel, je třeba přidat tohoto dodavatele jako schváleného dodavatele v následujících krocích.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="ef1c5-113">Poznamenejte si číslo dodavatele, pokud je uvedeno.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="ef1c5-114">V podokně akcí klikněte na možnost **Zakoupit**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-114">On Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="ef1c5-115">Klikněte na možnost **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-115">Click **Setup**.</span></span>
7. <span data-ttu-id="ef1c5-116">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-116">Click **Add**.</span></span>
8. <span data-ttu-id="ef1c5-117">V poli Dodavatel zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="ef1c5-118">Vyberte schváleného dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-118">Select the approved vendor.</span></span> <span data-ttu-id="ef1c5-119">Alespoň jeden z řádků musí být hlavním dodavatelem, pokud existují dodavatelé v záznamu produktů.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="ef1c5-120">Pokud jste si dříve číslo dodavatele poznamenali, vyberte je zde.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="ef1c5-121">Do pole **Vypršení platnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="ef1c5-122">Vyberte datum, které je několik měsíců v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="ef1c5-123">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-123">Click **Add**.</span></span>
11. <span data-ttu-id="ef1c5-124">V poli **Dodavatel** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="ef1c5-125">Do pole **Vypršení platnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="ef1c5-126">Vyberte datum, které se liší od předchozího data vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="ef1c5-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-127">Close the page.</span></span>
14. <span data-ttu-id="ef1c5-128">V podokně akcí klikněte na **Schválení dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-128">On Action pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="ef1c5-129">Do pole **Vypršení platnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="ef1c5-130">Toto datum se chová jako filtr, abyste viděli, kdo jsou schválení dodavatelé, a to až do určitého data.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="ef1c5-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-131">Close the page.</span></span>
17. <span data-ttu-id="ef1c5-132">V podokně akcí klikněte na **Období platnosti**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-132">On Action pane, click **Effective period**.</span></span>
18. <span data-ttu-id="ef1c5-133">V poli **Zobrazit dodavatele s ukončenou platností k** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="ef1c5-134">Tato stránka slouží k identifikaci dodavatelů, kde stav schválení vyprší po určitém datu.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="ef1c5-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-135">Close the page.</span></span>
20. <span data-ttu-id="ef1c5-136">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-136">Click **Edit**.</span></span>
21. <span data-ttu-id="ef1c5-137">Poté vyberte možnost v poli **Metoda kontroly schválených dodavatelů**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="ef1c5-138">Toto pole umožňuje vybrat zásady pro situace, které nastanou při přidání produktu na řádek nákupní objednávky, pokud dodavatel není schváleným dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="ef1c5-139">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-139">Click **Save**.</span></span>
23. <span data-ttu-id="ef1c5-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-140">Close the page.</span></span>
24. <span data-ttu-id="ef1c5-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-141">Close the page.</span></span>
25. <span data-ttu-id="ef1c5-142">V navigačním podokně přejděte na **Moduly >Zásobování a zdroje > Dodavatelé > Vztahy dodavatel/položka > Seznam schválených dodavatelů podle položky**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="ef1c5-143">Na této stránce je uveden přehled všech produktů a schválení dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="ef1c5-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-144">Close the page.</span></span>
27. <span data-ttu-id="ef1c5-145">V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Dodavatelé > Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="ef1c5-146">Můžete také začít od dodavatele a přejít na seznam schválených produktů pro tento účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="ef1c5-147">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="ef1c5-148">V podokně akcí klikněte na možnost **Zásobování**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-148">On Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="ef1c5-149">Klikněte na **Seznam schválených dodavatelů podle dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="ef1c5-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-150">Close the page.</span></span>
32. <span data-ttu-id="ef1c5-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef1c5-151">Close the page.</span></span>

