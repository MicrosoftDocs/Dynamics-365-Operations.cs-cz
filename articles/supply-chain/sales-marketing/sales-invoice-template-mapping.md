---
title: "Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních faktur z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="930a2-103">Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="930a2-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="930a2-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních faktur z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="930a2-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="930a2-105">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="930a2-105">Templates and tasks</span></span>

<span data-ttu-id="930a2-106">K synchronizaci hlaviček a řádků prodejních faktur z aplikace Finance and Operations do aplikace Sales slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="930a2-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="930a2-107">**Název šablony v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="930a2-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="930a2-108">Prodejní faktury (Fin and Ops do Sales)</span><span class="sxs-lookup"><span data-stu-id="930a2-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="930a2-109">**Názvy úkolů v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="930a2-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="930a2-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="930a2-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="930a2-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="930a2-111">SalesInvoiceLine</span></span>

<span data-ttu-id="930a2-112">Synchronizace úkolů vyžadovaných před synchronizací záhlaví a řádků prodejní faktury:</span><span class="sxs-lookup"><span data-stu-id="930a2-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="930a2-113">Produkty (Fin and Ops do Sales)</span><span class="sxs-lookup"><span data-stu-id="930a2-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="930a2-114">Účty (Sales do Fin and Ops) (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="930a2-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="930a2-115">Kontakty (Sales do Fin and Ops) (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="930a2-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="930a2-116">Záhlaví a řádky prodejní objednávky (Fin and Ops do Sales)</span><span class="sxs-lookup"><span data-stu-id="930a2-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="930a2-117">Sada entit</span><span class="sxs-lookup"><span data-stu-id="930a2-117">Entity set</span></span>

| <span data-ttu-id="930a2-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="930a2-118">Finance and Operations</span></span>                               | <span data-ttu-id="930a2-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="930a2-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="930a2-120">Prodej.</span><span class="sxs-lookup"><span data-stu-id="930a2-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="930a2-121">Záhlaví prodejní faktury odběratele udržované externě</span><span class="sxs-lookup"><span data-stu-id="930a2-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="930a2-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="930a2-122">SalesInvoice</span></span>     | <span data-ttu-id="930a2-123">Faktury</span><span class="sxs-lookup"><span data-stu-id="930a2-123">Invoices</span></span>       |
| <span data-ttu-id="930a2-124">Řádky prodejní faktury odběratele udržované externě</span><span class="sxs-lookup"><span data-stu-id="930a2-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="930a2-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="930a2-125">SalesInvoiceLine</span></span> | <span data-ttu-id="930a2-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="930a2-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="930a2-127">Tok entity</span><span class="sxs-lookup"><span data-stu-id="930a2-127">Entity flow</span></span>

<span data-ttu-id="930a2-128">Prodejní faktury jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="930a2-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="930a2-129">Daně související s náklady na **Záhlaví prodejní faktury** aktuálně nejsou zahrnuty do synchronizace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="930a2-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="930a2-130">Důvodem je skutečnost, že aplikace Sales nepodporuje daňové informace na úrovni záhlaví.</span><span class="sxs-lookup"><span data-stu-id="930a2-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="930a2-131">Je zahrnuta daň související s náklady na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="930a2-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="930a2-132">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="930a2-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="930a2-133">Pole **Číslo faktury** je přidáno do entity **Faktura** a zobrazí na stránce.</span><span class="sxs-lookup"><span data-stu-id="930a2-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="930a2-134">Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="930a2-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="930a2-135">Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="930a2-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="930a2-136">**Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="930a2-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="930a2-137">Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury.</span><span class="sxs-lookup"><span data-stu-id="930a2-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="930a2-138">To umožňuje vlastníkovi prodejní objednávky zobrazit fakturu.</span><span class="sxs-lookup"><span data-stu-id="930a2-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="930a2-139">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="930a2-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="930a2-140">Před synchronizací prodejních faktur je důležité aktualizovat systémy s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="930a2-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="930a2-141">Nastavení v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="930a2-141">Setup in Sales</span></span>

- <span data-ttu-id="930a2-142">V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="930a2-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="930a2-143">V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Metoda výpočtu slevy** je nastavena na **Položka řádku**.</span><span class="sxs-lookup"><span data-stu-id="930a2-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="930a2-144">Nastavení projektu integrace dat</span><span class="sxs-lookup"><span data-stu-id="930a2-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="930a2-145">Úloha SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="930a2-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="930a2-146">Aktualizujte mapování pro **CDS ID organizace** v možnostech **Zdroj** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="930a2-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="930a2-147">Výchozí hodnota šablony pro **SalesOrder_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="930a2-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="930a2-148">Výchozí hodnota šablony pro **Account_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="930a2-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="930a2-149">Výchozí hodnota šablony pro **Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="930a2-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="930a2-150">Ujistěte se, že existuje potřebné mapování v možnostech **Zdroj** > **CDS pro InvoiceCountryRegionId** do **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="930a2-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="930a2-151">Hodnota šablony je **ValueMap** s určitým počtem namapovaných zemí.</span><span class="sxs-lookup"><span data-stu-id="930a2-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="930a2-152">**Ceník** je povinný pro vytvoření faktur v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="930a2-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="930a2-153">Aktualizujte **ValueMap** v **CDS** > **Destination for pricelevelid.name [název ceníku]** na **ceník** použitý v aplikaci Sales podle měny.</span><span class="sxs-lookup"><span data-stu-id="930a2-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="930a2-154">Můžete buď použít výchozí **ceník** pro jednu měnu nebo použít **ValueMap**, máte-li **ceníky** v různých měnách.</span><span class="sxs-lookup"><span data-stu-id="930a2-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="930a2-155">Hodnota šablony pro **pricelevelid.name [název ceníku]** je **ValueMap** na základě **měny**.</span><span class="sxs-lookup"><span data-stu-id="930a2-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="930a2-156">usd: CRM Service USA (vzorek).</span><span class="sxs-lookup"><span data-stu-id="930a2-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="930a2-157">Úloha SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="930a2-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="930a2-158">Ujistěte se, že existuje potřebné mapování v položkách **Zdroj** > **CDS pro měrnou jednotku**.</span><span class="sxs-lookup"><span data-stu-id="930a2-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="930a2-159">Ujistěte se, že existuje potřebná hodnota **ValueMap** pro **SalesUnitSymbol** v aplikaci Finance and Operations v možnostech **Zdroj** > **CDS mapování**.</span><span class="sxs-lookup"><span data-stu-id="930a2-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="930a2-160">Hodnota šablony s **ValueMap** je definovaná pro **SalesUnitSymbol to Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="930a2-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="930a2-161">Aktualizujte mapování pro **CDS ID organizace v možnostech Zdroj** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="930a2-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="930a2-162">Výchozí hodnota šablony pro **SalesInvoicer_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="930a2-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="930a2-163">Výchozí hodnota šablony pro **Product_Organization_OrganizationId** je ORG001.</span><span class="sxs-lookup"><span data-stu-id="930a2-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="930a2-164">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="930a2-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="930a2-165">**Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **Způsob dopravy** a **Způsob dodání** nejsou součástí výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="930a2-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="930a2-166">Mapování těchto polí vyžaduje nastavení mapování hodnoty, což je specifické pro data v organizacích, mezi kterými je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="930a2-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="930a2-167">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="930a2-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="930a2-172">Související témata</span><span class="sxs-lookup"><span data-stu-id="930a2-172">Related topics</span></span>

[<span data-ttu-id="930a2-173">Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="930a2-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="930a2-174">Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="930a2-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="930a2-175">Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="930a2-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="930a2-176">Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="930a2-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="930a2-177">Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="930a2-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


