---
title: Integrovaná hlavní data odběratelů
description: Toto téma popisuje integraci dat zákazníků mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685632"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="6ea4f-103">Integrovaná hlavní data odběratelů</span><span class="sxs-lookup"><span data-stu-id="6ea4f-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="6ea4f-104">Zákaznická data mohou být vyplněna ve více než jedné aplikaci Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="6ea4f-105">Například řádek odběratele může pocházet z prodejní aktivity v Dynamics 365 Sales (aplikace řízená podle modelu v Dynamics 365) nebo může řádek pocházet z maloobchodní aktivity v Dynamics 365 Commerce (aplikace Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="6ea4f-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="6ea4f-106">Bez ohledu na místo, odkud pocházejí data odběratele, je integrováno na pozadí.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="6ea4f-107">Integrovaná hlavní předloha odběratele poskytuje flexibilitu pro hlavní zákaznická data v jakékoli aplikaci Dynamics 365 a poskytuje komplexní přehled o zákaznících v rámci aplikační sady Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="6ea4f-108">Tok dat odběratele</span><span class="sxs-lookup"><span data-stu-id="6ea4f-108">Customer data flow</span></span>

<span data-ttu-id="6ea4f-109">*Odběratel* je dobře definovaný koncept v aplikacích.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="6ea4f-110">Proto integrace zákaznických dat pouze zahrnuje harmonizaci koncepce zákazníků mezi těmito dvěmi aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="6ea4f-111">Následující obrázek znázorňuje tok dat odběratele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-111">The following illustration shows the customer data flow.</span></span>

![Tok dat odběratele](media/dual-write-customer-data-flow.png)

<span data-ttu-id="6ea4f-113">Zákazníci mohou být široce řazeni do dvou typů: obchodní/organizační zákazníci a spotřebitelé/koncoví uživatelé.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="6ea4f-114">Tyto dva typy zákazníků jsou ukládány a zpracovávány odlišně v aplikacích Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="6ea4f-115">V aplikaci Finance and Operations jsou obchodní/organizační zákazníci i spotřebitelé/koncoví uživatelé řízeni v jedné tabulce s názvem **CustTable** (CustCustomerV3Entity) a jsou klasifikováni podle atributu **Typ**.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="6ea4f-116">(Je -li **Typ** nastaven na **Organizace**, je zákazníkem obchodní/organizační zákazník a pokud je **Typ** nastaven na **Osoba**, je zákazníkem zákazník/koncový uživatel.) Informace o primární kontaktní osobě jsou zpracovány prostřednictvím entity SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="6ea4f-117">V Dataverse jsou obchodní/organizační zákazníci ovládáni entitou obchodní vztah a jsou identifikováni jako zákazníci, když je atribut **RelationshipType** nastaven na **Odběratel**.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-117">In Dataverse, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="6ea4f-118">Entita kontakt reprezentuje spotřebitele/koncové uživatele i kontaktní osobu.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="6ea4f-119">Chcete-li zajistit jasné oddělení mezi spotřebitelem/koncovým uživatelem a kontaktní osobou, má entita **Kontakt** logický příznak, který se jmenuje **Prodejné**.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="6ea4f-120">Pokud je **Prodejné** je **True** je kontaktem spotřebitel/koncový uživatel a nabídky a objednávky lze vytvořit pro kontakt.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="6ea4f-121">Je-li **Prodejné** je **False** je kontaktem pouze primární kontaktní osoba zákazníka.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="6ea4f-122">Pokud se procesu nabídky nebo objednávky účastní neprodejný kontakt, je **Prodejné** nastaveno na **True** pro označení kontaktu jako prodejného.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="6ea4f-123">Kontakt, který se stal prodejním kontaktem, zůstává prodejním kontaktem.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="6ea4f-124">Šablony</span><span class="sxs-lookup"><span data-stu-id="6ea4f-124">Templates</span></span>

<span data-ttu-id="6ea4f-125">Data odběratele zahrnují všechny informace o odběrateli, například skupinu odběratelů, adresy, kontaktní informace, platební profil a profil faktury a věrnostní stav.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="6ea4f-126">Kolekce mapování tabulek pracuje společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="6ea4f-127">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6ea4f-127">Finance and Operations apps</span></span> | <span data-ttu-id="6ea4f-128">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6ea4f-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="6ea4f-129">Popis</span><span class="sxs-lookup"><span data-stu-id="6ea4f-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="6ea4f-130">CDS kontakty V2</span><span class="sxs-lookup"><span data-stu-id="6ea4f-130">CDS Contacts V2</span></span>             | <span data-ttu-id="6ea4f-131">kontakty</span><span class="sxs-lookup"><span data-stu-id="6ea4f-131">contacts</span></span>                        | <span data-ttu-id="6ea4f-132">Tato šablona synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="6ea4f-133">Skupiny odběratelů</span><span class="sxs-lookup"><span data-stu-id="6ea4f-133">Customer groups</span></span>             | <span data-ttu-id="6ea4f-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="6ea4f-134">msdyn_customergroups</span></span>            | <span data-ttu-id="6ea4f-135">Tato šablona slouží k synchronizaci informací o skupinách odběratele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="6ea4f-136">Způsob platby odběratele</span><span class="sxs-lookup"><span data-stu-id="6ea4f-136">Customer payment method</span></span>     | <span data-ttu-id="6ea4f-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="6ea4f-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="6ea4f-138">Tato šablona slouží k synchronizaci informací o způsobu platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="6ea4f-139">Zákazníci V3</span><span class="sxs-lookup"><span data-stu-id="6ea4f-139">Customers V3</span></span>                | <span data-ttu-id="6ea4f-140">účty</span><span class="sxs-lookup"><span data-stu-id="6ea4f-140">accounts</span></span>                        | <span data-ttu-id="6ea4f-141">Tato šablona synchronizuje hlavní informace o zákaznících pro komerční a organizační zákazníky.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="6ea4f-142">Zákazníci V3</span><span class="sxs-lookup"><span data-stu-id="6ea4f-142">Customers V3</span></span>                | <span data-ttu-id="6ea4f-143">kontakty</span><span class="sxs-lookup"><span data-stu-id="6ea4f-143">contacts</span></span>                        | <span data-ttu-id="6ea4f-144">Tato šablona synchronizuje hlavní data odběratele pro spotřebitele a koncové uživatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="6ea4f-145">Přípony názvu</span><span class="sxs-lookup"><span data-stu-id="6ea4f-145">Name affixes</span></span>                | <span data-ttu-id="6ea4f-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="6ea4f-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="6ea4f-147">Tato šablona synchronizuje referenční data přípon názvů pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6ea4f-148">Řádky dnů platby CDS V2</span><span class="sxs-lookup"><span data-stu-id="6ea4f-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="6ea4f-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="6ea4f-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="6ea4f-150">Tato šablona synchronizuje referenční data řádků dnů platby pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6ea4f-151">Dny platby CDS</span><span class="sxs-lookup"><span data-stu-id="6ea4f-151">Payment days CDS</span></span>            | <span data-ttu-id="6ea4f-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="6ea4f-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="6ea4f-153">Tato šablona synchronizuje referenční data dnů platby pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6ea4f-154">Řádky platebního kalendáře</span><span class="sxs-lookup"><span data-stu-id="6ea4f-154">Payment schedule lines</span></span>      | <span data-ttu-id="6ea4f-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="6ea4f-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="6ea4f-156">Synchronizuje referenční data řádků platebního kalendáře pro odběratele i dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6ea4f-157">Platební kalendář</span><span class="sxs-lookup"><span data-stu-id="6ea4f-157">Payment schedule</span></span>            | <span data-ttu-id="6ea4f-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="6ea4f-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="6ea4f-159">Tato šablona synchronizuje referenční data platebního kalendáře pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6ea4f-160">Platební podmínky</span><span class="sxs-lookup"><span data-stu-id="6ea4f-160">Terms of payment</span></span>            | <span data-ttu-id="6ea4f-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="6ea4f-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="6ea4f-162">Tato šablona synchronizuje referenční data platebních podmínek (podmínek platby) pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6ea4f-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
