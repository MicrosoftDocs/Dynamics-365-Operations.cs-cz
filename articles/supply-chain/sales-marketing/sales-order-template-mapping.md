---
title: "Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních objednávek z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 707efc97afc0679ed1fc22539789e98cbabcb581
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="58573-103">Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="58573-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58573-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních objednávek z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="58573-105">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="58573-105">Template and tasks</span></span>

<span data-ttu-id="58573-106">K synchronizaci hlaviček a řádků prodejních objednávek z aplikace Finance and Operations do aplikace Sales slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="58573-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="58573-107">**Název šablony v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="58573-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="58573-108">Prodejní objednávky (Fin and Ops do Sales)</span><span class="sxs-lookup"><span data-stu-id="58573-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="58573-109">**Názvy úkolů v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="58573-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="58573-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="58573-110">OrderHeader</span></span>
    - <span data-ttu-id="58573-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="58573-111">OrderLine</span></span>

<span data-ttu-id="58573-112">Synchronizace úkolů vyžadovaných před synchronizací záhlaví a řádků prodejní objednávky:</span><span class="sxs-lookup"><span data-stu-id="58573-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="58573-113">Produkty (Fin and Ops do Sales)</span><span class="sxs-lookup"><span data-stu-id="58573-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="58573-114">Účty (Sales do Fin and Ops) (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="58573-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="58573-115">Kontakty na zákazníky (Sales do Fin and Ops) (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="58573-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="58573-116">Sada entit</span><span class="sxs-lookup"><span data-stu-id="58573-116">Entity set</span></span>

| <span data-ttu-id="58573-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58573-117">Finance and Operations</span></span> |    <span data-ttu-id="58573-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="58573-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="58573-119">Prodej.</span><span class="sxs-lookup"><span data-stu-id="58573-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="58573-120">Záhlaví prodejní objednávky CDS</span><span class="sxs-lookup"><span data-stu-id="58573-120">CDS sales order headers</span></span>| <span data-ttu-id="58573-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="58573-121">SalesOrder</span></span>     | <span data-ttu-id="58573-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="58573-122">SalesOrders</span></span> |
| <span data-ttu-id="58573-123">Řádky prodejní objednávky CDS</span><span class="sxs-lookup"><span data-stu-id="58573-123">CDS sales order lines</span></span>  | <span data-ttu-id="58573-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="58573-124">SalesOrderLine</span></span> | <span data-ttu-id="58573-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="58573-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="58573-126">Tok entity</span><span class="sxs-lookup"><span data-stu-id="58573-126">Entity flow</span></span>

<span data-ttu-id="58573-127">Prodejní objednávky jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="58573-128">Filtry v šabloně zajišťují, že do synchronizace jsou zahrnuty pouze příslušné prodejní objednávky:</span><span class="sxs-lookup"><span data-stu-id="58573-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="58573-129">Objednávající a fakturující odběratel na prodejní objednávce, která pochází z aplikace Sales, budou zahrnuti do procesu synchronizace.</span><span class="sxs-lookup"><span data-stu-id="58573-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="58573-130">V aplikaci Finance and Operations se používají pole **OrderingCustomerIsExternallyMaintained** a **InvoiceCustomerIsExternallyMaintained** ke sledování ke sledování synchronizace v datových entitách.</span><span class="sxs-lookup"><span data-stu-id="58573-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="58573-131">**Prodejní objednávka** musí být v aplikaci Finance and Operations potvrzena.</span><span class="sxs-lookup"><span data-stu-id="58573-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="58573-132">Pouze potvrzené prodejní objednávky nebo prodejní objednávky s vyšším stavem zpracování, například stavem Expedováno nebo Fakturováno, budou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="58573-133">Po vytvoření nebo úpravě prodejní objednávky, musí být provedena v aplikaci Finance and Operations dávková úloha **Vypočítat celkové tržby**.</span><span class="sxs-lookup"><span data-stu-id="58573-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="58573-134">Pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do CDS a aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="58573-135">Daně související s náklady na **Záhlaví prodejní objednávky** aktuálně nejsou zahrnuty do synchronizace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="58573-136">Důvodem je skutečnost, že aplikace Sales nepodporuje daňové informace na úrovni záhlaví.</span><span class="sxs-lookup"><span data-stu-id="58573-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="58573-137">Je zahrnuta daň související s náklady na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="58573-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="58573-138">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="58573-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="58573-139">Nová pole se přidají do entity **Objednávka** a zobrazí na stránce:</span><span class="sxs-lookup"><span data-stu-id="58573-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="58573-140">**Je externě spravováno** - Nastavte na **Ano**, když pořadí pochází z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58573-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="58573-141">**Stav zpracování** - Používá se k zobrazení stavu zpracování objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58573-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="58573-142">Hodnoty jsou:</span><span class="sxs-lookup"><span data-stu-id="58573-142">Values are:</span></span>

    - <span data-ttu-id="58573-143">Aktivní</span><span class="sxs-lookup"><span data-stu-id="58573-143">Active</span></span>
    - <span data-ttu-id="58573-144">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="58573-144">Confirmed</span></span>
    - <span data-ttu-id="58573-145">Dodací list</span><span class="sxs-lookup"><span data-stu-id="58573-145">Packing Slip</span></span>
    - <span data-ttu-id="58573-146">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="58573-146">Invoiced</span></span>
    - <span data-ttu-id="58573-147">Vydáno</span><span class="sxs-lookup"><span data-stu-id="58573-147">Picked</span></span>
    - <span data-ttu-id="58573-148">Částečně vyskladněno</span><span class="sxs-lookup"><span data-stu-id="58573-148">Partially Picked</span></span>
    - <span data-ttu-id="58573-149">Částečně zabaleno</span><span class="sxs-lookup"><span data-stu-id="58573-149">Partially Packed</span></span>
    - <span data-ttu-id="58573-150">Expedováno</span><span class="sxs-lookup"><span data-stu-id="58573-150">Shipped</span></span>
    - <span data-ttu-id="58573-151">Částečně expedováno</span><span class="sxs-lookup"><span data-stu-id="58573-151">Partially Shipped</span></span>
    - <span data-ttu-id="58573-152">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="58573-152">Partially Invoiced</span></span>
    - <span data-ttu-id="58573-153">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="58573-153">Cancelled</span></span>

<span data-ttu-id="58573-154">Nastavení **Má pouze externě udržované produkty** se používá v jiných scénářích prodejní objednávky (synchronizace z aplikace Sales do aplikace Finance and Operations), aby se konzistentně sledovalo, zda je prodejní objednávka tvořena zcela z **externě udržovaných produktů**, přičemž produkty jsou udržovány v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58573-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="58573-155">Toto chování pomáhá zaručit, že nezkusíte synchronizovat řádky prodejní objednávky s produkty, které nejsou známy v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58573-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="58573-156">Tlačítka **Vytvořit fakturu**, **Zrušit objednávku**, **Přepočítat**, **Získat produkty** a **Vyhledávání adresy** na stránce **Prodejní objednávka** jsou pro externě udržované objednávky skryta, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="58573-157">Stránku objednávky nelze upravovat, protože informace o prodejních objednávkách budou synchronizovány z aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58573-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="58573-158">**Stav prodejní objednávky** zůstane aktivní, aby se zajistilo, že změny z aplikace Finance and Operations mohou být odeslány do **prodejní objednávky** v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="58573-159">Toto je kontrolováno nastavením výchozího **Statecode [stavu]** na **Aktivní** v projektu integrace dat.</span><span class="sxs-lookup"><span data-stu-id="58573-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="58573-160">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="58573-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="58573-161">Před synchronizací prodejních objednávek je důležité aktualizovat systémy s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="58573-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="58573-162">Nastavení v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="58573-162">Setup in Sales</span></span>

- <span data-ttu-id="58573-163">Zajistěte oprávnění pro tým, ke kterému je uživatel (ze **sady připojení** aplikace Sales) přiřazen.</span><span class="sxs-lookup"><span data-stu-id="58573-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="58573-164">Používáte-li ukázková data, má obvykle uživatel přístup správce, ale nikoli týmu.</span><span class="sxs-lookup"><span data-stu-id="58573-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="58573-165">Bez toho je vygenerována chyba, která oznamuje, že chybí hlavní tým při spuštění projektu z integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="58573-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="58573-166">V **Nastavení** > **Zabezpečení** > **Týmy**, vyberte příslušný tým, klikněte na **Spravovat role** a vyberte roli s požadovanými oprávněními, například správce systému.</span><span class="sxs-lookup"><span data-stu-id="58573-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="58573-167">V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="58573-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="58573-168">V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Metoda výpočtu slevy** je nastavena na **Položka řádku**.</span><span class="sxs-lookup"><span data-stu-id="58573-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="58573-169">Nastavení v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58573-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="58573-170">Nastavte **Prodej a marketing** > **Periodické úlohy** > **Vypočítat celkové tržby** pro spouštění v podobě dávkové úlohy, s možností **Vypočítat celkové částky prodejních objednávek** nastavenou na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="58573-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="58573-171">Je to důležité, protože pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do CDS a aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="58573-172">Frekvence dávkové úlohy musí být ve shodě s frekvencí synchronizace prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58573-172">The frequence of the batch job should be alligned with the frequence of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="58573-173">Nastavení projektu integrace dat</span><span class="sxs-lookup"><span data-stu-id="58573-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="58573-174">Úloha SalesHeader</span><span class="sxs-lookup"><span data-stu-id="58573-174">SalesHeader task</span></span>

- <span data-ttu-id="58573-175">Aktualizujte mapování pro **CDS ID organizace v možnostech Zdroj** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="58573-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="58573-176">Výchozí hodnota šablony pro **Account_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="58573-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="58573-177">Výchozí hodnota šablony pro **InvoiceAccount_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="58573-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="58573-178">Výchozí hodnota šablony pro **Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="58573-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="58573-179">Ujistěte se, že existuje potřebné mapování v možnostech **Zdroj** > **CDS pro InvoiceCountryRegionId do BillingAddress_Country** a pro **DeliveryCountryRegionId do DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="58573-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="58573-180">Hodnota šablony je **ValueMap** s určitým počtem namapovaných zemí.</span><span class="sxs-lookup"><span data-stu-id="58573-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="58573-181">**Ceník** je povinný pro vytvoření objednávek v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="58573-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="58573-182">Aktualizujte **ValueMap** v **CDS** > **Cíl** pro **pricelevelid.name [název ceníku]** do **ceníku** použitého v aplikaci Sales podle měny.</span><span class="sxs-lookup"><span data-stu-id="58573-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="58573-183">Můžete buď použít výchozí **ceník** pro jednu měnu nebo použít **ValueMap**, máte-li **ceníky** v různých měnách.</span><span class="sxs-lookup"><span data-stu-id="58573-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="58573-184">Výchozí hodnota šablony pro **pricelevelid.name [název ceníku]** je CRM Service USA (vzorek).</span><span class="sxs-lookup"><span data-stu-id="58573-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="58573-185">Úloha SalesLine</span><span class="sxs-lookup"><span data-stu-id="58573-185">SalesLine task</span></span>

- <span data-ttu-id="58573-186">Aktualizujte mapování pro **CDS ID organizace v možnostech Zdroj** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="58573-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="58573-187">Výchozí hodnota šablony pro **SalesOrder_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="58573-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="58573-188">Výchozí hodnota šablony pro **Product_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="58573-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="58573-189">Ujistěte se, že existuje potřebné mapování v možnostech **Zdroj** > **CDS** pro **DeliveryCountryRegionId** do **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="58573-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="58573-190">Hodnota šablony je **ValueMap** s určitým počtem namapovaných zemí.</span><span class="sxs-lookup"><span data-stu-id="58573-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="58573-191">Ujistěte se, že existuje potřebná hodnota **ValueMap** pro **SalesUnitSymbol** v aplikaci Finance and Operations v možnostech **Zdroj** > **CDS mapování**.</span><span class="sxs-lookup"><span data-stu-id="58573-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="58573-192">Hodnota šablony s **ValueMap** je definovaná pro **SalesUnitSymbol to Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="58573-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="58573-193">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="58573-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="58573-194">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="58573-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="58573-195">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="58573-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="58573-196">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="58573-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="58573-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="58573-197">OrderHeader</span></span>

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-1.png)

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="58573-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="58573-200">OrderLine</span></span>

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-3.png)

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="58573-203">Související témata</span><span class="sxs-lookup"><span data-stu-id="58573-203">Related topics</span></span>

[<span data-ttu-id="58573-204">Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="58573-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="58573-205">Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58573-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="58573-206">Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58573-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="58573-207">Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58573-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="58573-208">Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="58573-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


