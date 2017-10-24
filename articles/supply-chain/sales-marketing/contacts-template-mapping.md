---
title: "Synchronizace kontaktů z aplikace Sales s kontakty nebo odběrateli v aplikaci Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci kontaktu (Kontakty) a kontaktu (odběratelé) z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="1e313-103">Synchronizace kontaktů z aplikace Sales s kontakty nebo odběrateli v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1e313-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1e313-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="1e313-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="1e313-105">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci entit Kontakt (Kontakty) a Kontakt (Odběratelé) z aplikace Microsoft Dynamics 365 for Sales (Sales) do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="1e313-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1e313-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="1e313-106">Templates and tasks</span></span>

<span data-ttu-id="1e313-107">K synchronizaci entit Kontakt (Kontakty) v aplikaci Sales a Kontakt (Odběratelé) v aplikaci Finance and Operations slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="1e313-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="1e313-108">**Názvy šablon:**</span><span class="sxs-lookup"><span data-stu-id="1e313-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="1e313-109">Kontakty (Sales do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1e313-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="1e313-110">Kontakty s entitou Odběratel (prodej do modulů Fin a Ops)</span><span class="sxs-lookup"><span data-stu-id="1e313-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="1e313-111">**Názvy úkolů v projektu:**</span><span class="sxs-lookup"><span data-stu-id="1e313-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="1e313-112">Kontakty</span><span class="sxs-lookup"><span data-stu-id="1e313-112">Contacts</span></span>
    - <span data-ttu-id="1e313-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="1e313-113">ContactToCustomer</span></span>

<span data-ttu-id="1e313-114">Následující úkol synchronizace je požadován před synchronizací kontaktu: Účty (Prodej do modulů Fin a Ops)</span><span class="sxs-lookup"><span data-stu-id="1e313-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="1e313-115">Sady entit</span><span class="sxs-lookup"><span data-stu-id="1e313-115">Entity sets</span></span>

| <span data-ttu-id="1e313-116">Prodej.</span><span class="sxs-lookup"><span data-stu-id="1e313-116">Sales</span></span>    | <span data-ttu-id="1e313-117">CDS</span><span class="sxs-lookup"><span data-stu-id="1e313-117">CDS</span></span>     | <span data-ttu-id="1e313-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1e313-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="1e313-119">Kontakty</span><span class="sxs-lookup"><span data-stu-id="1e313-119">Contacts</span></span> | <span data-ttu-id="1e313-120">Kontakt</span><span class="sxs-lookup"><span data-stu-id="1e313-120">Contact</span></span> | <span data-ttu-id="1e313-121">CDS kontakty</span><span class="sxs-lookup"><span data-stu-id="1e313-121">CDS Contacts</span></span>           |
| <span data-ttu-id="1e313-122">Kontakty</span><span class="sxs-lookup"><span data-stu-id="1e313-122">Contacts</span></span> | <span data-ttu-id="1e313-123">Účet</span><span class="sxs-lookup"><span data-stu-id="1e313-123">Account</span></span> | <span data-ttu-id="1e313-124">Zákazníci V2</span><span class="sxs-lookup"><span data-stu-id="1e313-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="1e313-125">Tok entity</span><span class="sxs-lookup"><span data-stu-id="1e313-125">Entity flow</span></span>

<span data-ttu-id="1e313-126">Kontakty jsou spravovány v modulu Sales a jsou synchronizovány pro Common Data Service (CDS) a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e313-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="1e313-127">Kontakt v aplikaci Sales se může stát kontaktem v CDS a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e313-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="1e313-128">Případně to může být účet v CDS a odběratel v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e313-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="1e313-129">K určení, zda kontakt má být vydán v aplikaci Sales pro synchronizaci s aplikací CDS a Finance and Operations (například kontakty v aplikaci Sales &gt; kontakt v CDS &gt; Kontakty v aplikaci Finance and Operations), systém vyhledá následující vlastnosti kontaktu v aplikaci Sales:</span><span class="sxs-lookup"><span data-stu-id="1e313-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="1e313-130">**Synchronizace s účtem v aplikaci CDS a zákazníkem v aplikaci Finance and Operations:** Kontakty, u nichž je možnost **Je aktivní zákazník** nastavena na **Ano**</span><span class="sxs-lookup"><span data-stu-id="1e313-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="1e313-131">**Synchronizace s kontaktem v aplikaci CDS a kontaktem v aplikaci Finance and Operations:** Kontakty, kde je možnost **Je aktivní zákazník** nastavena na **Ne** a **Společnost** (Nadřazený účet/Kontakt) odkazuje na účet (ne na kontakt)</span><span class="sxs-lookup"><span data-stu-id="1e313-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1e313-132">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="1e313-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="1e313-133">Do kontaktu bylo přidáno nové pole **Je aktivní odběratel**.</span><span class="sxs-lookup"><span data-stu-id="1e313-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="1e313-134">Toto pole slouží k rozlišení kontaktů, které mají prodejní aktivitu, a kontaktů, které nemají prodejní aktivitu.</span><span class="sxs-lookup"><span data-stu-id="1e313-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="1e313-135">Hodnota **Je aktivní odběratel** je nastavena na **Ano** pouze pro kontakty, které obsahují odpovídající nabídky, objednávky nebo faktury.</span><span class="sxs-lookup"><span data-stu-id="1e313-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="1e313-136">V aplikaci Finance and Operations jsou jako zákazníci synchronizovány pouze tyto kontakty.</span><span class="sxs-lookup"><span data-stu-id="1e313-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="1e313-137">Do kontaktu bylo přidáno nové pole **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="1e313-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="1e313-138">Toto pole se používá k označení, zda je kontakt propojen se společností (nadřazený účet/kontakt) typu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="1e313-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="1e313-139">Tyto informace slouží k identifikaci kontaktů, které mají být synchronizovány s aplikací Finance and Operations jako kontakty.</span><span class="sxs-lookup"><span data-stu-id="1e313-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="1e313-140">Do kontaktu bylo přidáno nové pole **Číslo kontaktu** na pomoc se zaručení přirozeného a jedinečného klíče pro integraci.</span><span class="sxs-lookup"><span data-stu-id="1e313-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="1e313-141">Po vytvoření nového kontaktu je automaticky generována hodnota **číslo kontaktu** pomocí číselné řady.</span><span class="sxs-lookup"><span data-stu-id="1e313-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="1e313-142">Hodnota se skládá z údaje **CON** a následně dalšího čísla číselné řady, a pak přípony šest znaků.</span><span class="sxs-lookup"><span data-stu-id="1e313-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="1e313-143">Tady je příklad: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="1e313-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="1e313-144">Když je do aplikace Sales přidáno integrační řešení pro aplikaci Sales, skript pro upgrade nastaví pole **Číslo kontaktu** pro existující kontakty pomocí číselné řady, o které jsme diskutovali dříve.</span><span class="sxs-lookup"><span data-stu-id="1e313-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="1e313-145">Skript pro upgrade nastaví také hodnotu v poli **Je aktivní zákazník** na **Ano** u všech kontaktů, které mají aktivitu prodeje.</span><span class="sxs-lookup"><span data-stu-id="1e313-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="1e313-146">V aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1e313-146">In Finance and Operations</span></span> 

<span data-ttu-id="1e313-147">Kontakty jsou označeny pomocí vlastnosti **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="1e313-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="1e313-148">Tato vlastnost označuje, že je daný kontakt spravován externě.</span><span class="sxs-lookup"><span data-stu-id="1e313-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="1e313-149">V takovém případě jsou externě spravované kontakty evidovány v prodeji.</span><span class="sxs-lookup"><span data-stu-id="1e313-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1e313-150">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="1e313-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="1e313-151">Kontakt do kontaktu</span><span class="sxs-lookup"><span data-stu-id="1e313-151">Contact to Contact</span></span>

- <span data-ttu-id="1e313-152">Aktualizujte **ID organizace CDS** mapování **Zdroj &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="1e313-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="1e313-153">Výchozí hodnota šablony pro **Organization_OrganizationId [Organization ID]** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1e313-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="1e313-154">Výchozí hodnota šablony pro **PrimaryAccount_Organization_OrganizationId [ID organizace]** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1e313-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="1e313-155">**Kód země/oblasti pro adresu** je v aplikaci Finance and Operations vyžadován.</span><span class="sxs-lookup"><span data-stu-id="1e313-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="1e313-156">Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování **CDS &gt; Operace**.</span><span class="sxs-lookup"><span data-stu-id="1e313-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="1e313-157">Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné.</span><span class="sxs-lookup"><span data-stu-id="1e313-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="1e313-158">Výchozí hodnota šablony pro **PrimaryAddressCountryRegionISOCode** je **USA**.</span><span class="sxs-lookup"><span data-stu-id="1e313-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="1e313-159">Zkontrolujte, že v aplikaci Finance and Operations existuje hodnota pro následující pole.</span><span class="sxs-lookup"><span data-stu-id="1e313-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="1e313-160">Pokud tyto informace nejsou v aplikaci Finance and Operations požadovány, můžete odebrat mapování z mapování **CDS &gt; Cíl**.</span><span class="sxs-lookup"><span data-stu-id="1e313-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="1e313-161">**Název pole v aplikaci Finance and Operations:** Rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="1e313-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="1e313-162">**Mapování:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="1e313-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="1e313-163">Kontakt na odběratele</span><span class="sxs-lookup"><span data-stu-id="1e313-163">Contact to Customer</span></span>

- <span data-ttu-id="1e313-164">Aktualizujte **ID organizace CDS** mapování **Zdroj &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="1e313-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="1e313-165">Výchozí hodnota šablony pro **Organization_OrganizationId [Organization ID]** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1e313-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="1e313-166">**Kód země/oblasti pro adresu** je v aplikaci Finance and Operations vyžadován.</span><span class="sxs-lookup"><span data-stu-id="1e313-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="1e313-167">Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování **CDS &gt; Cíl**.</span><span class="sxs-lookup"><span data-stu-id="1e313-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="1e313-168">Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné.</span><span class="sxs-lookup"><span data-stu-id="1e313-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="1e313-169">Výchozí hodnota šablony pro **PrimaryAddressCountryRegionISOCode** je **USA**.</span><span class="sxs-lookup"><span data-stu-id="1e313-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="1e313-170">**CustomerGroup** je v aplikaci Finance and Operations povinná.</span><span class="sxs-lookup"><span data-stu-id="1e313-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="1e313-171">Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování **CDS &gt; Cíl**.</span><span class="sxs-lookup"><span data-stu-id="1e313-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="1e313-172">Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné.</span><span class="sxs-lookup"><span data-stu-id="1e313-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="1e313-173">Výchozí hodnota šablony pro **CustomerGroupId** je **10**.</span><span class="sxs-lookup"><span data-stu-id="1e313-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="1e313-174">Přidáním následujících mapování z aplikace **CD &gt; Cíl** můžete snížit počet ručních aktualizací, které jsou povinné v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e313-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="1e313-175">Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.</span><span class="sxs-lookup"><span data-stu-id="1e313-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="1e313-176">**SiteId** - pro produkty v aplikaci Finance and Operations je také možné definovat výchozí pracoviště.</span><span class="sxs-lookup"><span data-stu-id="1e313-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="1e313-177">Pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e313-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="1e313-178">Hodnota šablony pro **SiteId** není definována.</span><span class="sxs-lookup"><span data-stu-id="1e313-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="1e313-179">**WarehouseId** - pro produkty v aplikaci Finance and Operations je také možné definovat výchozí sklad.</span><span class="sxs-lookup"><span data-stu-id="1e313-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="1e313-180">Sklad je nutné zadat za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e313-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="1e313-181">Hodnota šablony pro **WarehouseId** není definována.</span><span class="sxs-lookup"><span data-stu-id="1e313-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="1e313-182">**LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e313-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="1e313-183">Výchozí hodnota šablony pro **LanguageId** je **en-us**.</span><span class="sxs-lookup"><span data-stu-id="1e313-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="1e313-184">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="1e313-184">Template mapping in data integrator</span></span>

<span data-ttu-id="1e313-185">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="1e313-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="1e313-186">Kontakt do kontaktu</span><span class="sxs-lookup"><span data-stu-id="1e313-186">Contact to Contact</span></span>

![Mapování šablony v integrátoru dat](./media/contacts-template-mapping-data-integrator-1.png)

![Mapování šablony pro kontakty v integrátoru dat](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="1e313-189">Kontakt na odběratele</span><span class="sxs-lookup"><span data-stu-id="1e313-189">Contact to Customer</span></span>

![Mapování šablony v integrátoru dat](./media/contacts-template-mapping-data-integrator-3.png)

![Mapování šablony pro kontakty v integrátoru dat](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="1e313-192">Související témata</span><span class="sxs-lookup"><span data-stu-id="1e313-192">Related topics</span></span>

[<span data-ttu-id="1e313-193">Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="1e313-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="1e313-194">Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1e313-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="1e313-195">Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1e313-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="1e313-196">Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="1e313-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="1e313-197">Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="1e313-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

