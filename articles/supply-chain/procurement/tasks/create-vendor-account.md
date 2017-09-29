--- 
title: "Vytvoření účtu dodavatele"
description: "Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="cde4e-103">Vytvoření účtu dodavatele</span><span class="sxs-lookup"><span data-stu-id="cde4e-103">Create a vendor account</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cde4e-104">Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací.</span><span class="sxs-lookup"><span data-stu-id="cde4e-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="cde4e-105">Postup neukazuje vyplnění všech polí pro nákupní a finanční účely.</span><span class="sxs-lookup"><span data-stu-id="cde4e-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="cde4e-106">Další informace o těchto polích naleznete v popisech polí.</span><span class="sxs-lookup"><span data-stu-id="cde4e-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="cde4e-107">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="cde4e-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="cde4e-108">Účty dodavatele jsou obvykle vytvářeny pracovníky zásobování nebo zaměstnanci starající se o pohledávky.</span><span class="sxs-lookup"><span data-stu-id="cde4e-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="cde4e-109">Vytvoření účtu dodavatele</span><span class="sxs-lookup"><span data-stu-id="cde4e-109">Create a vendor account</span></span>
1. <span data-ttu-id="cde4e-110">Přejděte na Zásobování a zdroje > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="cde4e-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="cde4e-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cde4e-111">Click New.</span></span>
3. <span data-ttu-id="cde4e-112">Zadejte hodnotu do pole Účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="cde4e-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="cde4e-113">Hodnota může být vyplněna automaticky.</span><span class="sxs-lookup"><span data-stu-id="cde4e-113">The value may be populated automatically.</span></span> <span data-ttu-id="cde4e-114">Pokud tomu tak je, můžete tento krok vynechat.</span><span class="sxs-lookup"><span data-stu-id="cde4e-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="cde4e-115">Můžete vytvořit účty dodavatelů pro osobu nebo organizaci.</span><span class="sxs-lookup"><span data-stu-id="cde4e-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="cde4e-116">Tato akce ovlivní dostupnost polí.</span><span class="sxs-lookup"><span data-stu-id="cde4e-116">This will affect which fields are available.</span></span> <span data-ttu-id="cde4e-117">V tomto příkladu vytvoříte účet dodavatele pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="cde4e-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="cde4e-118">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde4e-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="cde4e-119">Pokud je daný dodavatel již registrovanou stranou v systému, můžete použít rozevírací seznam a vybrat jej v tomto poli, přičemž nový účet dodavatele převezme adresu a kontaktní informace, které jsou již registrované.</span><span class="sxs-lookup"><span data-stu-id="cde4e-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="cde4e-120">V poli Skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde4e-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="cde4e-121">Skupina dodavatelů se používá pro seskupení dodavatelů, kteří mají společné následující parametry: platební podmínky, období vyrovnání, skladové účty hlavní knihy včetně skupiny DPH, výchozí účty hlavní knihy, kódy filtru produktu a konfigurace prognózy dodávek.</span><span class="sxs-lookup"><span data-stu-id="cde4e-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="cde4e-122">Do pole Počet zaměstnanců zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="cde4e-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="cde4e-123">Zadejte hodnotu do pole Číslo organizace.</span><span class="sxs-lookup"><span data-stu-id="cde4e-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="cde4e-124">Přidání adresy</span><span class="sxs-lookup"><span data-stu-id="cde4e-124">Add an address</span></span>
1. <span data-ttu-id="cde4e-125">Rozbalte sekci Adresy.</span><span class="sxs-lookup"><span data-stu-id="cde4e-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="cde4e-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="cde4e-126">Click Add.</span></span>
3. <span data-ttu-id="cde4e-127">V poli Účel zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde4e-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="cde4e-128">Lze vybrat jeden nebo více účelů.</span><span class="sxs-lookup"><span data-stu-id="cde4e-128">You can select one or more purposes.</span></span> <span data-ttu-id="cde4e-129">Ty se používají k výběru správné adresy pro daný účel.</span><span class="sxs-lookup"><span data-stu-id="cde4e-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="cde4e-130">Například pokud je účelem "Faktura", daná adresa bude použita při odesílání faktur.</span><span class="sxs-lookup"><span data-stu-id="cde4e-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="cde4e-131">Zadejte hodnotu do pole Název nebo popis.</span><span class="sxs-lookup"><span data-stu-id="cde4e-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="cde4e-132">V poli Země/oblast zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde4e-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="cde4e-133">Zadejte podrobnosti adresy.</span><span class="sxs-lookup"><span data-stu-id="cde4e-133">Enter the address details.</span></span> <span data-ttu-id="cde4e-134">Vámi vybraná země/oblast určuje pole, která se zobrazí, a budou odpovídat formátu adresy pro danou zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="cde4e-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="cde4e-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cde4e-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="cde4e-136">Přidání kontaktních informací</span><span class="sxs-lookup"><span data-stu-id="cde4e-136">Add contact information</span></span>
1. <span data-ttu-id="cde4e-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="cde4e-137">Click Add.</span></span>
2. <span data-ttu-id="cde4e-138">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="cde4e-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="cde4e-139">Vyberte volbu v poli Typ.</span><span class="sxs-lookup"><span data-stu-id="cde4e-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="cde4e-140">Zadejte hodnotu do pole Kontaktní číslo/adresa.</span><span class="sxs-lookup"><span data-stu-id="cde4e-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="cde4e-141">Pole Primární můžete vybrat, je-li daná adresa primární adresou kontaktní osoby.</span><span class="sxs-lookup"><span data-stu-id="cde4e-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="cde4e-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cde4e-142">Click Save.</span></span>
6. <span data-ttu-id="cde4e-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde4e-143">Close the page.</span></span>
7. <span data-ttu-id="cde4e-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde4e-144">Close the page.</span></span>


