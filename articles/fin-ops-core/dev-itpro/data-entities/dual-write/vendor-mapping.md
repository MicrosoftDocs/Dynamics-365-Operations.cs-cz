---
title: Integrovaná hlavní data dodavatelů
description: Toto téma popisuje integraci dat dodavatele mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 272962b58d8d654c2640a51ef2dbdcd1b05cf8c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560306"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="e61e6-103">Integrovaná hlavní data dodavatelů</span><span class="sxs-lookup"><span data-stu-id="e61e6-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="e61e6-104">Pojem *dodavatel* se týká dodavatelské organizace nebo jediného majitele, který dodává zboží nebo služby nějakému podniku.</span><span class="sxs-lookup"><span data-stu-id="e61e6-104">The term *vendor* refers to a supplier organization, or a sole proprietor who supplies goods or services to a business.</span></span> <span data-ttu-id="e61e6-105">Ačkoli je *dodavatel* zavedeným konceptem v aplikacích Microsoft Dynamics 365 Supply Chain Management, v modelem řízených aplikacích Dynamics 365 žádný koncept dodavatele neexistuje.</span><span class="sxs-lookup"><span data-stu-id="e61e6-105">Although *vendor* is an established concept in Microsoft Dynamics 365 Supply Chain Management, no vendor concept exists in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="e61e6-106">Chcete-li však uložit informace o dodavateli, můžete přetížit tabulku **Účet/kontakt**.</span><span class="sxs-lookup"><span data-stu-id="e61e6-106">However, you can overload the **Account/Contact** table to store vendor information.</span></span> <span data-ttu-id="e61e6-107">Integrovaná hlavní data dodavatelů zavádí explicitní koncept dodavatele v modelem řízených aplikacích Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e61e6-107">The integrated vendor master introduces an explicit vendor concept in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="e61e6-108">V tabulce **Účet/kontakt** můžete použít nový návrh dodavatele nebo uložit data dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-108">You can either use the new vendor design or store vendor data in the **Account/Contact** table.</span></span> <span data-ttu-id="e61e6-109">Dvojitý zápis podporuje oba přístupy.</span><span class="sxs-lookup"><span data-stu-id="e61e6-109">Dual-write supports both approaches.</span></span>

<span data-ttu-id="e61e6-110">U obou přístupů jsou data dodavatele integrována mezi Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service a portály Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e61e6-110">In both approaches, the vendor data is integrated between Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, and Power Apps portals.</span></span> <span data-ttu-id="e61e6-111">V Supply Chain Management jsou data k dispozici pro workflowy, jako jsou nákupní žádanky a nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e61e6-111">In Supply Chain Management, the data is available for workflows such as purchase requisitions and purchase orders.</span></span>

## <a name="vendor-data-flow"></a><span data-ttu-id="e61e6-112">Tok dat dodavatele</span><span class="sxs-lookup"><span data-stu-id="e61e6-112">Vendor data flow</span></span>

<span data-ttu-id="e61e6-113">Pokud nechcete uložit data dodavatele v tabulce **Účet/kontakt** v Dataverse, můžete použít nový návrh dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-113">If you don't want to store vendor data in the **Account/Contact** table in Dataverse, you can use the new vendor design.</span></span>

![Tok dat dodavatele](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="e61e6-115">Pokud nechcete nadále ukládat data dodavatele v tabulce **Účet/kontakt**, můžete použít rozšířený návrh dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-115">If you want to continue to store vendor data in the **Account/Contact** table, you can use the extended vendor design.</span></span> <span data-ttu-id="e61e6-116">Chcete-li použít rozšířený návrh dodavatele, je nutné nakonfigurovat workflowy dodavatele v balíčku řešení dvojitého zápisu.</span><span class="sxs-lookup"><span data-stu-id="e61e6-116">To use the extended vendor design, you must configure the vendor workflows in the dual-write solution package.</span></span> <span data-ttu-id="e61e6-117">Další informace naleznete v tématu [Přepínání mezi návrhy dodavatele](vendor-switch.md).</span><span class="sxs-lookup"><span data-stu-id="e61e6-117">For more information, see [Switch between vendor designs](vendor-switch.md).</span></span>

![Rozšířený tok dat dodavatele](media/dual-write-vendor-detail.jpg)

> [!TIP]
> <span data-ttu-id="e61e6-119">Používáte portály Power Apps pro samoobslužné dodavatele, mohou informace o dodavateli téci přímo do aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e61e6-119">If you're using Power Apps portals for self-service vendors, the vendor information can flow directly to Finance and Operations apps.</span></span>

## <a name="templates"></a><span data-ttu-id="e61e6-120">Šablony</span><span class="sxs-lookup"><span data-stu-id="e61e6-120">Templates</span></span>

<span data-ttu-id="e61e6-121">Data dodavatele zahrnují všechny informace o dodavateli, například skupinu dodavatelů, adresy, kontaktní informace, platební profil a profil faktury.</span><span class="sxs-lookup"><span data-stu-id="e61e6-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="e61e6-122">Kolekce mapování tabulek pracují společně během interakce s daty dodavatele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="e61e6-122">A collection of table maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="e61e6-123">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e61e6-123">Finance and Operations apps</span></span> | <span data-ttu-id="e61e6-124">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e61e6-124">Other Dynamics 365 apps</span></span>     | <span data-ttu-id="e61e6-125">popis</span><span class="sxs-lookup"><span data-stu-id="e61e6-125">Description</span></span>
----------------------------|-----------------------------|------------
<span data-ttu-id="e61e6-126">Dodavatel V2</span><span class="sxs-lookup"><span data-stu-id="e61e6-126">Vendor V2</span></span>                   | <span data-ttu-id="e61e6-127">Účet</span><span class="sxs-lookup"><span data-stu-id="e61e6-127">Account</span></span>                     | <span data-ttu-id="e61e6-128">Firmy, které používají tabulku obchodní vztah k ukládání informací o dodavateli, jí mohou nadále používat stejným způsobem.</span><span class="sxs-lookup"><span data-stu-id="e61e6-128">Businesses that use the Account table to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="e61e6-129">Mohou také využít explicitní funkce dodavatele, které přicházejí z důvodu integrace s aplikacemi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e61e6-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="e61e6-130">Dodavatel V2</span><span class="sxs-lookup"><span data-stu-id="e61e6-130">Vendor V2</span></span>                   | <span data-ttu-id="e61e6-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="e61e6-131">Msdyn\_vendors</span></span>              | <span data-ttu-id="e61e6-132">Firmy, které používají vlastní řešení pro dodavatele, mohou využít výhod integrované koncepce dodavatele, která je zaváděna v Dataverse z důvodu integrace s aplikacemi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e61e6-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Dataverse because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="e61e6-133">Skupiny dodavatelů</span><span class="sxs-lookup"><span data-stu-id="e61e6-133">Vendor groups</span></span>               | <span data-ttu-id="e61e6-134">msdyn\_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="e61e6-134">msdyn\_vendorgroups</span></span>         | <span data-ttu-id="e61e6-135">Tato šablona slouží k synchronizaci informací o skupinách dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="e61e6-136">Platební metoda dodavatele</span><span class="sxs-lookup"><span data-stu-id="e61e6-136">Vendor payment method</span></span>       | <span data-ttu-id="e61e6-137">msdyn\_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="e61e6-137">msdyn\_vendorpaymentmethods</span></span> | <span data-ttu-id="e61e6-138">Tato šablona slouží k synchronizaci informací o způsobu platby dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="e61e6-139">CDS kontakty V2</span><span class="sxs-lookup"><span data-stu-id="e61e6-139">CDS Contacts V2</span></span>             | <span data-ttu-id="e61e6-140">kontakty</span><span class="sxs-lookup"><span data-stu-id="e61e6-140">contacts</span></span>                    | <span data-ttu-id="e61e6-141">Šablona [kontakty](customer-mapping.md#cds-contacts-v2-to-contacts) synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="e61e6-142">Řádky platebního kalendáře</span><span class="sxs-lookup"><span data-stu-id="e61e6-142">Payment schedule lines</span></span>      | <span data-ttu-id="e61e6-143">msdyn\_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="e61e6-143">msdyn\_paymentschedulelines</span></span> | <span data-ttu-id="e61e6-144">Šablona [řádky platebního kalendáře](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synchronizuje referenční data pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="e61e6-145">Platební kalendář</span><span class="sxs-lookup"><span data-stu-id="e61e6-145">Payment schedule</span></span>            | <span data-ttu-id="e61e6-146">msdyn\_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="e61e6-146">msdyn\_paymentschedules</span></span>     | <span data-ttu-id="e61e6-147">Šablona [plány plateb](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) synchronizuje referenční data pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e61e6-148">Řádky dnů platby CDS V2</span><span class="sxs-lookup"><span data-stu-id="e61e6-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="e61e6-149">msdyn\_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="e61e6-149">msdyn\_paymentdaylines</span></span>      | <span data-ttu-id="e61e6-150">Šablona [řádky dní platby](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synchronizuje referenční data řádků dní platby pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="e61e6-151">Dny platby CDS</span><span class="sxs-lookup"><span data-stu-id="e61e6-151">Payment days CDS</span></span>            | <span data-ttu-id="e61e6-152">msdyn\_paymentdays</span><span class="sxs-lookup"><span data-stu-id="e61e6-152">msdyn\_paymentdays</span></span>          | <span data-ttu-id="e61e6-153">Šablona [dny platby](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) synchronizuje referenční data dní plateb pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e61e6-154">Platební podmínky</span><span class="sxs-lookup"><span data-stu-id="e61e6-154">Terms of payment</span></span>            | <span data-ttu-id="e61e6-155">msdyn\_paymentterms</span><span class="sxs-lookup"><span data-stu-id="e61e6-155">msdyn\_paymentterms</span></span>         | <span data-ttu-id="e61e6-156">Šablona [platební podmínky](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) synchronizuje referenční data platebních podmínek pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e61e6-157">Přípony názvu</span><span class="sxs-lookup"><span data-stu-id="e61e6-157">Name affixes</span></span>                | <span data-ttu-id="e61e6-158">msdyn\_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="e61e6-158">msdyn\_nameaffixes</span></span>          | <span data-ttu-id="e61e6-159">Šablona [přípony názvů](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) synchronizuje referenční data přípon názvů pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e61e6-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]