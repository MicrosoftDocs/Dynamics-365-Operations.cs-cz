---
title: "Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci entit kontaktu (Kontakty) a kontaktu (odběratelé) z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="4d489-103">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d489-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4d489-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="4d489-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="4d489-105">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci entit kontaktu (Kontakty) a kontaktu (odběratelé) přímo z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="4d489-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="4d489-106">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="4d489-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="4d489-107">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="4d489-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="4d489-108">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="4d489-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="4d489-109">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="4d489-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="4d489-110">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="4d489-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4d489-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="4d489-111">Templates and tasks</span></span>

<span data-ttu-id="4d489-112">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="4d489-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="4d489-113">Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="4d489-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4d489-114">K synchronizaci entit Kontakt (Kontakty) v aplikaci Sales a Kontakt (Odběratelé) v aplikaci Finance and Operations slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="4d489-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="4d489-115">**Názvy šablon v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="4d489-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="4d489-116">Kontakty (Sales do Fin and Ops) - přímo</span><span class="sxs-lookup"><span data-stu-id="4d489-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="4d489-117">Kontakty na odběratele (Sales do Fin and Ops) - přímo</span><span class="sxs-lookup"><span data-stu-id="4d489-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="4d489-118">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="4d489-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="4d489-119">Kontakty</span><span class="sxs-lookup"><span data-stu-id="4d489-119">Contacts</span></span>
    - <span data-ttu-id="4d489-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="4d489-120">ContactToCustomer</span></span>

<span data-ttu-id="4d489-121">Následující úkol synchronizace je požadován před tím, než může dojít k synchronizací kontaktů: Účty (Sales do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4d489-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="4d489-122">Sady entit</span><span class="sxs-lookup"><span data-stu-id="4d489-122">Entity sets</span></span>

| <span data-ttu-id="4d489-123">Sales</span><span class="sxs-lookup"><span data-stu-id="4d489-123">Sales</span></span>    | <span data-ttu-id="4d489-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d489-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="4d489-125">Kontakty</span><span class="sxs-lookup"><span data-stu-id="4d489-125">Contacts</span></span> | <span data-ttu-id="4d489-126">CDS kontakty</span><span class="sxs-lookup"><span data-stu-id="4d489-126">CDS Contacts</span></span>           |
| <span data-ttu-id="4d489-127">Kontakty</span><span class="sxs-lookup"><span data-stu-id="4d489-127">Contacts</span></span> | <span data-ttu-id="4d489-128">Zákazníci V2</span><span class="sxs-lookup"><span data-stu-id="4d489-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="4d489-129">Tok entity</span><span class="sxs-lookup"><span data-stu-id="4d489-129">Entity flow</span></span>

<span data-ttu-id="4d489-130">Kontakty se spravují v aplikaci Sales a synchronizují se do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d489-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="4d489-131">Kontakt v aplikaci Sales se může stát buď kontaktem nebo odběratelem v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d489-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="4d489-132">K určení toho, zda kontakt v aplikaci Sales má být synchronizován do aplikace Finance and Operations jako kontakt nebo odběratel, vyhledá systém následující vlastnosti kontaktu v aplikaci Sales:</span><span class="sxs-lookup"><span data-stu-id="4d489-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="4d489-133">**Synchronizace na odběratele v aplikaci Finance and Operations:** Kontakty, u nichž je možnost **Je aktivní zákazník** nastavena na **Ano**</span><span class="sxs-lookup"><span data-stu-id="4d489-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="4d489-134">**Synchronizace na kontakt v aplikaci Finance and Operations:** Kontakty, kde je možnost **Je aktivní zákazník** nastavena na **Ne** a **Společnost** (nadřazený účet/kontakt) odkazuje na účet (ne na kontakt)</span><span class="sxs-lookup"><span data-stu-id="4d489-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4d489-135">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="4d489-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4d489-136">Do kontaktu bylo přidáno nové pole **Je aktivní odběratel**.</span><span class="sxs-lookup"><span data-stu-id="4d489-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="4d489-137">Toto pole slouží k rozlišení kontaktů, které mají prodejní aktivitu, a kontaktů, které nemají prodejní aktivitu.</span><span class="sxs-lookup"><span data-stu-id="4d489-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="4d489-138">Hodnota **Je aktivní odběratel** je nastavena na **Ano** pouze pro kontakty, které obsahují odpovídající nabídky, objednávky nebo faktury.</span><span class="sxs-lookup"><span data-stu-id="4d489-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="4d489-139">V aplikaci Finance and Operations jsou jako odběratelé synchronizováni pouze tyto kontakty.</span><span class="sxs-lookup"><span data-stu-id="4d489-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="4d489-140">Do kontaktu bylo přidáno nové pole **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="4d489-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="4d489-141">Toto pole označuje, zda je kontakt propojen se společností (nadřazený účet/kontakt) typu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="4d489-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="4d489-142">Tyto informace slouží k identifikaci kontaktů, které mají být synchronizovány s aplikací Finance and Operations jako kontakty.</span><span class="sxs-lookup"><span data-stu-id="4d489-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="4d489-143">Do kontaktu bylo přidáno nové pole **Číslo kontaktu** pro pomoc se zaručením přirozeného a jedinečného klíče pro integraci.</span><span class="sxs-lookup"><span data-stu-id="4d489-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="4d489-144">Po vytvoření nového kontaktu je automaticky generována hodnota **Číslo kontaktu** pomocí číselné řady.</span><span class="sxs-lookup"><span data-stu-id="4d489-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="4d489-145">Hodnota se skládá z údaje **CON** a následně dalšího čísla číselné řady, a pak přípony šest znaků.</span><span class="sxs-lookup"><span data-stu-id="4d489-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="4d489-146">Tady je příklad: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="4d489-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="4d489-147">Když je pro aplikaci Sales použito integrační řešení, skript pro upgrade nastaví pole **Číslo kontaktu** pro existující kontakty pomocí číselné řady, o které jsme mluvili dříve.</span><span class="sxs-lookup"><span data-stu-id="4d489-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="4d489-148">Skript pro upgrade nastaví také hodnotu v poli **Je aktivní zákazník** na **Ano** u všech kontaktů, které mají aktivitu prodeje.</span><span class="sxs-lookup"><span data-stu-id="4d489-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="4d489-149">V aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d489-149">In Finance and Operations</span></span>

<span data-ttu-id="4d489-150">Kontakty jsou označeny pomocí vlastnosti **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="4d489-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="4d489-151">Tato vlastnost označuje, že je daný kontakt spravován externě.</span><span class="sxs-lookup"><span data-stu-id="4d489-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="4d489-152">V takovém případě jsou externě spravované kontakty evidovány v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="4d489-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4d489-153">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="4d489-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="4d489-154">Kontakt na odběratele</span><span class="sxs-lookup"><span data-stu-id="4d489-154">Contact to customer</span></span>

- <span data-ttu-id="4d489-155">**CustomerGroup** je v aplikaci Finance and Operations povinná.</span><span class="sxs-lookup"><span data-stu-id="4d489-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="4d489-156">Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování.</span><span class="sxs-lookup"><span data-stu-id="4d489-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="4d489-157">Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné.</span><span class="sxs-lookup"><span data-stu-id="4d489-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="4d489-158">Výchozí hodnota šablony je **10**.</span><span class="sxs-lookup"><span data-stu-id="4d489-158">The default template value is **10**.</span></span>

- <span data-ttu-id="4d489-159">Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d489-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="4d489-160">Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.</span><span class="sxs-lookup"><span data-stu-id="4d489-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="4d489-161">**SiteId** - Pro produkty v aplikaci Finance and Operations je také možné definovat výchozí pracoviště.</span><span class="sxs-lookup"><span data-stu-id="4d489-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="4d489-162">Pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d489-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="4d489-163">Hodnota šablony pro **SiteId** není definována.</span><span class="sxs-lookup"><span data-stu-id="4d489-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="4d489-164">**WarehouseId** - Pro produkty v aplikaci Finance and Operations je také možné definovat výchozí sklad.</span><span class="sxs-lookup"><span data-stu-id="4d489-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="4d489-165">Sklad je nutné zadat za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d489-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="4d489-166">Hodnota šablony pro **WarehouseId** není definována.</span><span class="sxs-lookup"><span data-stu-id="4d489-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="4d489-167">**LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d489-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="4d489-168">Výchozí hodnota šablony je **en-us**.</span><span class="sxs-lookup"><span data-stu-id="4d489-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4d489-169">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="4d489-169">Template mapping in Data integration</span></span>

<span data-ttu-id="4d489-170">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="4d489-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="4d489-171">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d489-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="4d489-172">Kontakt na kontakt</span><span class="sxs-lookup"><span data-stu-id="4d489-172">Contact to contact</span></span>

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="4d489-174">Kontakt na odběratele</span><span class="sxs-lookup"><span data-stu-id="4d489-174">Contact to customer</span></span>

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="4d489-176">Související témata</span><span class="sxs-lookup"><span data-stu-id="4d489-176">Related topics</span></span>

[<span data-ttu-id="4d489-177">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="4d489-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="4d489-178">Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d489-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="4d489-179">Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="4d489-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="4d489-180">Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="4d489-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="4d489-181">Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="4d489-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



