---
title: Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci entit Kontakt (Kontakty) a Kontakty (Odběratelé) z Dynamics 365 Sales do Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994037"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="8801a-103">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8801a-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="8801a-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="8801a-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="8801a-105">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci tabulek Kontakt (Kontakty) a Kontakty (Odběratelé) přímo z Dynamics 365 Sales do Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="8801a-106">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="8801a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="8801a-107">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="8801a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="8801a-108">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="8801a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="8801a-109">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="8801a-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="8801a-110">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="8801a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="8801a-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="8801a-111">Templates and tasks</span></span>

<span data-ttu-id="8801a-112">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="8801a-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="8801a-113">Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="8801a-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8801a-114">K synchronizaci tabulek Kontakt (Kontakty) v aplikaci Sales a Kontakt (Odběratelé) v aplikaci Supply Chain Management slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="8801a-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="8801a-115">**Názvy šablon v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="8801a-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="8801a-116">Kontakty (Sales do Supply Chain Management) – Přímo</span><span class="sxs-lookup"><span data-stu-id="8801a-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="8801a-117">Kontakty do odběratele (Sales do Supply Chain Management) – Přímo</span><span class="sxs-lookup"><span data-stu-id="8801a-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="8801a-118">**Názvy úkolů v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="8801a-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="8801a-119">Kontakty</span><span class="sxs-lookup"><span data-stu-id="8801a-119">Contacts</span></span>
    - <span data-ttu-id="8801a-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="8801a-120">ContactToCustomer</span></span>

<span data-ttu-id="8801a-121">Následující úkol synchronizace je požadován před tím, než může dojít k synchronizací kontaktů: Účty (Sales do Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="8801a-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="8801a-122">Sady entit</span><span class="sxs-lookup"><span data-stu-id="8801a-122">Entity sets</span></span>

| <span data-ttu-id="8801a-123">Prodej.</span><span class="sxs-lookup"><span data-stu-id="8801a-123">Sales</span></span>    | <span data-ttu-id="8801a-124">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="8801a-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="8801a-125">Kontakty</span><span class="sxs-lookup"><span data-stu-id="8801a-125">Contacts</span></span> | <span data-ttu-id="8801a-126">Dataverse kontakty</span><span class="sxs-lookup"><span data-stu-id="8801a-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="8801a-127">Kontakty</span><span class="sxs-lookup"><span data-stu-id="8801a-127">Contacts</span></span> | <span data-ttu-id="8801a-128">Zákazníci V2</span><span class="sxs-lookup"><span data-stu-id="8801a-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="8801a-129">Tok entity</span><span class="sxs-lookup"><span data-stu-id="8801a-129">Entity flow</span></span>

<span data-ttu-id="8801a-130">Kontakty se spravují v aplikaci Sales a synchronizují se do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="8801a-131">Kontakt v aplikaci Sales se může stát buď kontaktem nebo odběratelem v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="8801a-132">K určení toho, zda kontakt v aplikaci Sales má být synchronizován do aplikace Supply Chain Management jako kontakt nebo odběratel, vyhledá systém následující vlastnosti kontaktu v aplikaci Sales:</span><span class="sxs-lookup"><span data-stu-id="8801a-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="8801a-133">**Synchronizace na odběratele v aplikaci Supply Chain Management:** Kontakty, u nichž je možnost **Je aktivní zákazník** nastavena na **Ano**</span><span class="sxs-lookup"><span data-stu-id="8801a-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="8801a-134">**Synchronizace na kontakt v aplikaci Supply Chain Management:** Kontakty, kde je možnost **Je aktivní zákazník** nastavena na **Ne** a **Společnost** (nadřazený účet/kontakt) odkazuje na účet (ne na kontakt)</span><span class="sxs-lookup"><span data-stu-id="8801a-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8801a-135">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="8801a-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="8801a-136">Do kontaktu byl přidán nový sloupec **Je aktivní odběratel**.</span><span class="sxs-lookup"><span data-stu-id="8801a-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="8801a-137">Tento sloupec slouží k rozlišení kontaktů, které mají prodejní aktivitu, a kontaktů, které nemají prodejní aktivitu.</span><span class="sxs-lookup"><span data-stu-id="8801a-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="8801a-138">Hodnota **Je aktivní odběratel** je nastavena na **Ano** pouze pro kontakty, které obsahují odpovídající nabídky, objednávky nebo faktury.</span><span class="sxs-lookup"><span data-stu-id="8801a-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="8801a-139">V aplikaci Supply Chain Management jsou jako odběratelé synchronizováni pouze tyto kontakty.</span><span class="sxs-lookup"><span data-stu-id="8801a-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="8801a-140">Do kontaktu byl přidán nový sloupec **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="8801a-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="8801a-141">Tento sloupec označuje, zda je kontakt propojen se společností (nadřazený účet/kontakt) typu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="8801a-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="8801a-142">Tyto informace slouží k identifikaci kontaktů, které mají být synchronizovány s aplikací Supply Chain Management jako kontakty.</span><span class="sxs-lookup"><span data-stu-id="8801a-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="8801a-143">Do kontaktu byl přidán nový sloupec **Číslo kontaktu** pro pomoc se zaručením přirozeného a jedinečného klíče pro integraci.</span><span class="sxs-lookup"><span data-stu-id="8801a-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="8801a-144">Po vytvoření nového kontaktu je automaticky generována hodnota **Číslo kontaktu** pomocí číselné řady.</span><span class="sxs-lookup"><span data-stu-id="8801a-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="8801a-145">Hodnota se skládá z údaje **CON** a následně dalšího čísla číselné řady, a pak přípony šest znaků.</span><span class="sxs-lookup"><span data-stu-id="8801a-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="8801a-146">Tady je příklad: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="8801a-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="8801a-147">Když je pro aplikaci Sales použito integrační řešení, skript pro upgrade nastaví sloupec **Číslo kontaktu** pro existující kontakty pomocí číselné řady, o které jsme mluvili dříve.</span><span class="sxs-lookup"><span data-stu-id="8801a-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="8801a-148">Skript pro upgrade nastaví také hodnotu ve sloupci **Je aktivní zákazník** na **Ano** u všech kontaktů, které mají aktivitu prodeje.</span><span class="sxs-lookup"><span data-stu-id="8801a-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="8801a-149">V Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8801a-149">In Supply Chain Management</span></span>

<span data-ttu-id="8801a-150">Kontakty jsou označeny pomocí vlastnosti **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="8801a-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="8801a-151">Tato vlastnost označuje, že je daný kontakt spravován externě.</span><span class="sxs-lookup"><span data-stu-id="8801a-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="8801a-152">V takovém případě jsou externě spravované kontakty evidovány v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="8801a-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="8801a-153">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="8801a-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="8801a-154">Kontakt na odběratele</span><span class="sxs-lookup"><span data-stu-id="8801a-154">Contact to customer</span></span>

- <span data-ttu-id="8801a-155">**Skupina odběratelů** je požadována v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="8801a-156">Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování.</span><span class="sxs-lookup"><span data-stu-id="8801a-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="8801a-157">Tato výchozí hodnota se pak použije, pokud sloupec v aplikaci Sales zůstane prázdný.</span><span class="sxs-lookup"><span data-stu-id="8801a-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="8801a-158">Výchozí hodnota šablony je **10**.</span><span class="sxs-lookup"><span data-stu-id="8801a-158">The default template value is **10**.</span></span>

- <span data-ttu-id="8801a-159">Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="8801a-160">Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.</span><span class="sxs-lookup"><span data-stu-id="8801a-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="8801a-161">**SiteId** - Pro produkty v aplikaci Supply Chain Management je také možné definovat výchozí pracoviště.</span><span class="sxs-lookup"><span data-stu-id="8801a-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="8801a-162">Pracoviště je nutné za účelem generování nabídky a prodejních objednávek v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="8801a-163">Hodnota šablony pro **SiteId** není definována.</span><span class="sxs-lookup"><span data-stu-id="8801a-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="8801a-164">**WarehouseId** - Pro produkty v aplikaci Supply Chain Management je také možné definovat výchozí sklad.</span><span class="sxs-lookup"><span data-stu-id="8801a-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="8801a-165">Sklad je nutný za účelem generování nabídky a prodejních objednávek v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="8801a-166">Hodnota šablony pro **WarehouseId** není definována.</span><span class="sxs-lookup"><span data-stu-id="8801a-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="8801a-167">**LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="8801a-168">Výchozí hodnota šablony je **en-us**.</span><span class="sxs-lookup"><span data-stu-id="8801a-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8801a-169">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="8801a-169">Template mapping in Data integration</span></span>

<span data-ttu-id="8801a-170">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="8801a-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="8801a-171">Mapování ukazuje, jaké informace o sloupci budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="8801a-172">Kontakt na kontakt</span><span class="sxs-lookup"><span data-stu-id="8801a-172">Contact to contact</span></span>

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="8801a-174">Kontakt na odběratele</span><span class="sxs-lookup"><span data-stu-id="8801a-174">Contact to customer</span></span>

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="8801a-176">Související témata</span><span class="sxs-lookup"><span data-stu-id="8801a-176">Related topics</span></span>

[<span data-ttu-id="8801a-177">Zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="8801a-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="8801a-178">Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8801a-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="8801a-179">Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales</span><span class="sxs-lookup"><span data-stu-id="8801a-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="8801a-180">Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8801a-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="8801a-181">Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="8801a-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


