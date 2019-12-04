---
title: Integrovaná hlavní data odběratelů
description: Toto téma popisuje integraci dat odběratele mezi aplikacemi Finance and Operations a Common Data Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769676"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="6491c-103">Integrovaná hlavní data odběratelů</span><span class="sxs-lookup"><span data-stu-id="6491c-103">Integrated customer master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6491c-104">Pro záznamy zákazníků je typické, že je možné je řídit ve více než jedné aplikaci.</span><span class="sxs-lookup"><span data-stu-id="6491c-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="6491c-105">Prodejní aktivita může například přinést záznamy komerčních zákazníků prostřednictvím aplikace Sales a elektronický obchod nebo maloobchodní prodej mohou přinést záznamy zákazníků v rámci aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6491c-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="6491c-106">Bez ohledu na to, odkud záznam odběratele pochází, je integrován v pozadí mezi hranicemi aplikace a rozdíly v infrastruktuře.</span><span class="sxs-lookup"><span data-stu-id="6491c-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="6491c-107">Integrované řízení zákazníků pomáhá zvládat scénáře vícenásobného řízení a poskytuje komplexní přehled o zákaznících do sady aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6491c-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="6491c-108">Tok dat odběratele</span><span class="sxs-lookup"><span data-stu-id="6491c-108">Customer data flow</span></span>

<span data-ttu-id="6491c-109">*Odběratel* je dobře definovaný koncept v aplikacích.</span><span class="sxs-lookup"><span data-stu-id="6491c-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="6491c-110">Proto integrace zákaznických dat pouze zahrnuje harmonizaci koncepce zákazníků mezi těmito dvěmi aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="6491c-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="6491c-111">Následující obrázek znázorňuje tok dat odběratele.</span><span class="sxs-lookup"><span data-stu-id="6491c-111">The following illustration shows the customer data flow.</span></span>

![Tok dat odběratele](media/dual-write-customer-data-flow.png)

<span data-ttu-id="6491c-113">Zákazníci mohou být široce řazeni do dvou typů: obchodní/organizační zákazníci a spotřebitelé/koncoví uživatelé.</span><span class="sxs-lookup"><span data-stu-id="6491c-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="6491c-114">Tyto dva typy zákazníků jsou ukládány a zpracovávány odlišně v aplikacích Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6491c-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="6491c-115">V aplikaci Finance and Operations jsou obchodní/organizační zákazníci i spotřebitelé/koncoví uživatelé řízeni v jedné tabulce s názvem **CustTable** (CustomerCustomerV3Entity) a jsou klasifikováni podle atributu **Typ**.</span><span class="sxs-lookup"><span data-stu-id="6491c-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="6491c-116">(Je -li **Typ** nastaven na **Organizace**, je zákazníkem obchodní/organizační zákazník a pokud je **Typ** nastaven na **Osoba**, je zákazníkem zákazník/koncový uživatel.) Informace o primární kontaktní osobě jsou zpracovány prostřednictvím entity SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="6491c-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="6491c-117">V Common Data Service jsou obchodní/organizační zákazníci ovládáni entitou obchodní vztah a jsou identifikováni jako zákazníci, když je atribut **RelationshipType** nastaven na **Odběratel**.</span><span class="sxs-lookup"><span data-stu-id="6491c-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="6491c-118">Entita kontakt reprezentuje spotřebitele/koncové uživatele i kontaktní osobu.</span><span class="sxs-lookup"><span data-stu-id="6491c-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="6491c-119">Chcete-li zajistit jasné oddělení mezi spotřebitelem/koncovým uživatelem a kontaktní osobou, má entita **Kontakt** logický příznak, který se jmenuje **Prodejné**.</span><span class="sxs-lookup"><span data-stu-id="6491c-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="6491c-120">Pokud je **Prodejné** je **True** je kontaktem spotřebitel/koncový uživatel a nabídky a objednávky lze vytvořit pro kontakt.</span><span class="sxs-lookup"><span data-stu-id="6491c-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="6491c-121">Je-li **Prodejné** je **False** je kontaktem pouze primární kontaktní osoba zákazníka.</span><span class="sxs-lookup"><span data-stu-id="6491c-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="6491c-122">Pokud se procesu nabídky nebo objednávky účastní neprodejný kontakt, je **Prodejné** nastaveno na **True** pro označení kontaktu jako prodejného.</span><span class="sxs-lookup"><span data-stu-id="6491c-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="6491c-123">Kontakt, který se stal prodejním kontaktem, zůstává prodejním kontaktem.</span><span class="sxs-lookup"><span data-stu-id="6491c-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="6491c-124">Šablony</span><span class="sxs-lookup"><span data-stu-id="6491c-124">Templates</span></span>

<span data-ttu-id="6491c-125">Data odběratele zahrnují všechny informace o odběrateli, například skupinu odběratelů, adresy, kontaktní informace, platební profil a profil faktury a věrnostní stav.</span><span class="sxs-lookup"><span data-stu-id="6491c-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="6491c-126">Kolekce mapování entit pracuje společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="6491c-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="6491c-127">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6491c-127">Finance and Operations apps</span></span> | <span data-ttu-id="6491c-128">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6491c-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="6491c-129">Popis</span><span class="sxs-lookup"><span data-stu-id="6491c-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="6491c-130">CDS kontakty V2</span><span class="sxs-lookup"><span data-stu-id="6491c-130">CDS Contacts V2</span></span>             | <span data-ttu-id="6491c-131">kontakty</span><span class="sxs-lookup"><span data-stu-id="6491c-131">contacts</span></span>                        | <span data-ttu-id="6491c-132">Tato šablona synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="6491c-133">Skupiny odběratelů</span><span class="sxs-lookup"><span data-stu-id="6491c-133">Customer groups</span></span>             | <span data-ttu-id="6491c-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="6491c-134">msdyn_customergroups</span></span>            | <span data-ttu-id="6491c-135">Tato šablona slouží k synchronizaci informací o skupinách odběratele.</span><span class="sxs-lookup"><span data-stu-id="6491c-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="6491c-136">Způsob platby odběratele</span><span class="sxs-lookup"><span data-stu-id="6491c-136">Customer payment method</span></span>     | <span data-ttu-id="6491c-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="6491c-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="6491c-138">Tato šablona slouží k synchronizaci informací o způsobu platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="6491c-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="6491c-139">Zákazníci V3</span><span class="sxs-lookup"><span data-stu-id="6491c-139">Customers V3</span></span>                | <span data-ttu-id="6491c-140">účty</span><span class="sxs-lookup"><span data-stu-id="6491c-140">accounts</span></span>                        | <span data-ttu-id="6491c-141">Tato šablona synchronizuje hlavní informace o zákaznících pro komerční a organizační zákazníky.</span><span class="sxs-lookup"><span data-stu-id="6491c-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="6491c-142">Zákazníci V3</span><span class="sxs-lookup"><span data-stu-id="6491c-142">Customers V3</span></span>                | <span data-ttu-id="6491c-143">kontakty</span><span class="sxs-lookup"><span data-stu-id="6491c-143">contacts</span></span>                        | <span data-ttu-id="6491c-144">Tato šablona synchronizuje hlavní data odběratele pro spotřebitele a koncové uživatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="6491c-145">Věrnostní karta</span><span class="sxs-lookup"><span data-stu-id="6491c-145">Loyalty card</span></span>                | <span data-ttu-id="6491c-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="6491c-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="6491c-147">Tato šablona slouží k synchronizaci informací o věrnostních kartách.</span><span class="sxs-lookup"><span data-stu-id="6491c-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="6491c-148">Přípony názvu</span><span class="sxs-lookup"><span data-stu-id="6491c-148">Name affixes</span></span>                | <span data-ttu-id="6491c-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="6491c-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="6491c-150">Tato šablona synchronizuje referenční data přípon názvů pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6491c-151">Řádky dnů platby CDS V2</span><span class="sxs-lookup"><span data-stu-id="6491c-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="6491c-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="6491c-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="6491c-153">Tato šablona synchronizuje referenční data řádků dnů platby pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6491c-154">Dny platby CDS</span><span class="sxs-lookup"><span data-stu-id="6491c-154">Payment days CDS</span></span>            | <span data-ttu-id="6491c-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="6491c-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="6491c-156">Tato šablona synchronizuje referenční data dnů platby pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6491c-157">Řádky platebního kalendáře</span><span class="sxs-lookup"><span data-stu-id="6491c-157">Payment schedule lines</span></span>      | <span data-ttu-id="6491c-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="6491c-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="6491c-159">Synchronizuje referenční data řádků platebního kalendáře pro odběratele i dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6491c-160">Platební kalendář</span><span class="sxs-lookup"><span data-stu-id="6491c-160">Payment schedule</span></span>            | <span data-ttu-id="6491c-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="6491c-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="6491c-162">Tato šablona synchronizuje referenční data platebního kalendáře pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6491c-163">Platební podmínky</span><span class="sxs-lookup"><span data-stu-id="6491c-163">Terms of payment</span></span>            | <span data-ttu-id="6491c-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="6491c-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="6491c-165">Tato šablona synchronizuje referenční data platebních podmínek (podmínek platby) pro odběratele a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6491c-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
