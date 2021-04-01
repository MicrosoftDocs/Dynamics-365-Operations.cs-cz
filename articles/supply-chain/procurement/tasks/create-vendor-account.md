---
title: Vytvoření účtu dodavatele
description: Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací.
author: RichardLuan
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d67af36b20be86456e5dff2cfc7fda893b98e1d5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262158"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="4fc42-103">Vytvoření účtu dodavatele</span><span class="sxs-lookup"><span data-stu-id="4fc42-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fc42-104">Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací.</span><span class="sxs-lookup"><span data-stu-id="4fc42-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="4fc42-105">Postup neukazuje vyplnění všech polí pro nákupní a finanční účely.</span><span class="sxs-lookup"><span data-stu-id="4fc42-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="4fc42-106">Další informace o těchto polích naleznete v popisech polí.</span><span class="sxs-lookup"><span data-stu-id="4fc42-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="4fc42-107">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="4fc42-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4fc42-108">Účty dodavatele jsou obvykle vytvářeny pracovníky zásobování nebo zaměstnanci starající se o pohledávky.</span><span class="sxs-lookup"><span data-stu-id="4fc42-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="4fc42-109">Vytvoření účtu dodavatele</span><span class="sxs-lookup"><span data-stu-id="4fc42-109">Create a vendor account</span></span>
1. <span data-ttu-id="4fc42-110">Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Dodavatelé > Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="4fc42-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-111">Click **New**.</span></span>
3. <span data-ttu-id="4fc42-112">Zadejte hodnotu do pole **Účet dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="4fc42-113">Hodnota může být vyplněna automaticky.</span><span class="sxs-lookup"><span data-stu-id="4fc42-113">The value may be populated automatically.</span></span> <span data-ttu-id="4fc42-114">Pokud tomu tak je, můžete tento krok vynechat.</span><span class="sxs-lookup"><span data-stu-id="4fc42-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="4fc42-115">Můžete vytvořit účty dodavatelů pro osobu nebo organizaci.</span><span class="sxs-lookup"><span data-stu-id="4fc42-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="4fc42-116">Tato akce ovlivní dostupnost polí.</span><span class="sxs-lookup"><span data-stu-id="4fc42-116">This will affect which fields are available.</span></span> <span data-ttu-id="4fc42-117">V tomto příkladu vytvoříte účet dodavatele pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="4fc42-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="4fc42-118">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4fc42-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="4fc42-119">Pokud je daný dodavatel již registrovanou stranou v systému, můžete použít rozevírací seznam a vybrat jej v tomto poli, přičemž nový účet dodavatele převezme adresu a kontaktní informace, které jsou již registrované.</span><span class="sxs-lookup"><span data-stu-id="4fc42-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="4fc42-120">V poli **Skupina** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4fc42-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="4fc42-121">Skupina dodavatelů se používá pro seskupení dodavatelů, kteří mají společné následující parametry: platební podmínky, období vyrovnání, skladové účty hlavní knihy včetně skupiny DPH, výchozí účty hlavní knihy, kódy filtru produktu a konfigurace prognózy dodávek.</span><span class="sxs-lookup"><span data-stu-id="4fc42-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="4fc42-122">Do pole **Počet zaměstnanců** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4fc42-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="4fc42-123">Zadejte hodnotu do pole **Číslo organizace**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="4fc42-124">Přidání adresy</span><span class="sxs-lookup"><span data-stu-id="4fc42-124">Add an address</span></span>
1. <span data-ttu-id="4fc42-125">Rozbalte sekci **Adresy**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="4fc42-126">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-126">Click **Add**.</span></span>
3. <span data-ttu-id="4fc42-127">V poli **Účel** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4fc42-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="4fc42-128">Lze vybrat jeden nebo více účelů.</span><span class="sxs-lookup"><span data-stu-id="4fc42-128">You can select one or more purposes.</span></span> <span data-ttu-id="4fc42-129">Ty se používají k výběru správné adresy pro daný účel.</span><span class="sxs-lookup"><span data-stu-id="4fc42-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="4fc42-130">Například pokud je účelem "Faktura", daná adresa bude použita při odesílání faktur.</span><span class="sxs-lookup"><span data-stu-id="4fc42-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="4fc42-131">Zadejte hodnotu do pole **Název nebo popis**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="4fc42-132">V poli **Země/oblast** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4fc42-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="4fc42-133">Zadejte podrobnosti adresy.</span><span class="sxs-lookup"><span data-stu-id="4fc42-133">Enter the address details.</span></span> <span data-ttu-id="4fc42-134">Vámi vybraná země/oblast určuje pole, která se zobrazí, a budou odpovídat formátu adresy pro danou zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="4fc42-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="4fc42-135">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="4fc42-136">Přidání kontaktních informací</span><span class="sxs-lookup"><span data-stu-id="4fc42-136">Add contact information</span></span>
1. <span data-ttu-id="4fc42-137">Rozbalte oddíl **Kontaktní informace**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="4fc42-138">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-138">Click **Add**.</span></span>
3. <span data-ttu-id="4fc42-139">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="4fc42-140">Vyberte volbu v poli **Typ**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="4fc42-141">Zadejte hodnotu do pole **Kontaktní číslo/adresa**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="4fc42-142">Pole Primární můžete vybrat, je-li daná adresa primární adresou kontaktní osoby.</span><span class="sxs-lookup"><span data-stu-id="4fc42-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="4fc42-143">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-143">Click **Save**.</span></span>
7. <span data-ttu-id="4fc42-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4fc42-144">Close the page.</span></span>
8. <span data-ttu-id="4fc42-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4fc42-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]