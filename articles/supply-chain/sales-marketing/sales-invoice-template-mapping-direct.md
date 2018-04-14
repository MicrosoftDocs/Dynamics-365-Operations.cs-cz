---
title: "Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních faktur a řádků z přímo aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6cf267d85795f6a7c253782b826cc75abef89d9f
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="ddbac-103">Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="ddbac-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ddbac-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních faktur a řádků z přímo aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="ddbac-105">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="ddbac-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="ddbac-106">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="ddbac-107">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="ddbac-108">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="ddbac-109">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="ddbac-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ddbac-110">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="ddbac-110">Templates and tasks</span></span>

<span data-ttu-id="ddbac-111">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="ddbac-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="ddbac-112">Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="ddbac-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ddbac-113">K synchronizaci hlaviček a řádků prodejních faktur z aplikace Finance and Operations do aplikace Sales slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="ddbac-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="ddbac-114">**Název šablony v integraci dat:** Prodejní faktury (Fin and Ops do Sales) - Přímo</span><span class="sxs-lookup"><span data-stu-id="ddbac-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="ddbac-115">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="ddbac-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="ddbac-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="ddbac-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="ddbac-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="ddbac-117">SalesInvoiceLine</span></span>

<span data-ttu-id="ddbac-118">Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní faktury a mohou se objevit řádky:</span><span class="sxs-lookup"><span data-stu-id="ddbac-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="ddbac-119">Produkty (Fin and Ops do Sales) - přímo</span><span class="sxs-lookup"><span data-stu-id="ddbac-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="ddbac-120">Účty (Sales do Fin and Ops) - přímo (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="ddbac-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="ddbac-121">Kontakty (Sales do Fin and Ops) - přímo (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="ddbac-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="ddbac-122">Záhlaví a řádky prodejní objednávky (Fin and Ops do Sales) - přímo</span><span class="sxs-lookup"><span data-stu-id="ddbac-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="ddbac-123">Sada entit</span><span class="sxs-lookup"><span data-stu-id="ddbac-123">Entity set</span></span>

| <span data-ttu-id="ddbac-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddbac-124">Finance and Operations</span></span>                               | <span data-ttu-id="ddbac-125">Prodej.</span><span class="sxs-lookup"><span data-stu-id="ddbac-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="ddbac-126">Záhlaví prodejní faktury odběratele udržované externě</span><span class="sxs-lookup"><span data-stu-id="ddbac-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="ddbac-127">Faktury</span><span class="sxs-lookup"><span data-stu-id="ddbac-127">Invoices</span></span>       |
| <span data-ttu-id="ddbac-128">Řádky prodejní faktury odběratele udržované externě</span><span class="sxs-lookup"><span data-stu-id="ddbac-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="ddbac-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="ddbac-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="ddbac-130">Tok entity</span><span class="sxs-lookup"><span data-stu-id="ddbac-130">Entity flow</span></span>

<span data-ttu-id="ddbac-131">Prodejní faktury jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="ddbac-132">Aktuálně není daň související s náklady na záhlaví prodejní faktury zahrnuta do synchronizace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="ddbac-133">Aplikace Sales nepodporuje daňové informace na úrovni záhlaví.</span><span class="sxs-lookup"><span data-stu-id="ddbac-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="ddbac-134">Daň, která souvisí s náklady na úrovni řádku, bude zahrnuta do procesu synchronizace.</span><span class="sxs-lookup"><span data-stu-id="ddbac-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ddbac-135">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="ddbac-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="ddbac-136">Pole **Číslo faktury** bylo přidáno do entity **Faktura** a zobrazí se na stránce.</span><span class="sxs-lookup"><span data-stu-id="ddbac-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="ddbac-137">Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="ddbac-138">Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddbac-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="ddbac-139">Hodnota **Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="ddbac-140">Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury.</span><span class="sxs-lookup"><span data-stu-id="ddbac-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="ddbac-141">Vlastník prodejní objednávky tudíž může zobrazit fakturu.</span><span class="sxs-lookup"><span data-stu-id="ddbac-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ddbac-142">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="ddbac-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="ddbac-143">Před synchronizací prodejních faktur je důležité aktualizovat následující nastavení v systémech:</span><span class="sxs-lookup"><span data-stu-id="ddbac-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="ddbac-144">Nastavení v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="ddbac-144">Setup in Sales</span></span>

<span data-ttu-id="ddbac-145">Přejděte na **Nastavení** > **Správa** > **Nastavení systému** > **Prodej**a ujistěte se, že se používají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ddbac-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="ddbac-146">Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ddbac-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="ddbac-147">Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.</span><span class="sxs-lookup"><span data-stu-id="ddbac-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="ddbac-148">Nastavení projektu integrace dat</span><span class="sxs-lookup"><span data-stu-id="ddbac-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="ddbac-149">Úloha SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="ddbac-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="ddbac-150">Ujistěte se, že existuje požadované mapování pro  **InvoiceCountryRegionId** do **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="ddbac-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="ddbac-151">Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí.</span><span class="sxs-lookup"><span data-stu-id="ddbac-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="ddbac-152">Ceník je povinný pro vytvoření faktur v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="ddbac-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="ddbac-153">Aktualizujte mapu hodnot pro **pricelevelid.name \[Název ceníku\]** do ceníku, použitého v aplikaci Sales podle měny.</span><span class="sxs-lookup"><span data-stu-id="ddbac-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="ddbac-154">Výchozí ceník můžete použít pro jednu měnu.</span><span class="sxs-lookup"><span data-stu-id="ddbac-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="ddbac-155">Popřípadě pokud máte ceníky v několika měnách, můžete použít mapu hodnot.</span><span class="sxs-lookup"><span data-stu-id="ddbac-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="ddbac-156">Hodnota šablony pro **pricelevelid.name \[Název ceníku\]** je mapa hodnot založená na měně s USD = CRM služba USA (vzorek).</span><span class="sxs-lookup"><span data-stu-id="ddbac-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="ddbac-157">Úloha SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="ddbac-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="ddbac-158">Ujistěte se, že existuje požadované mapování pro položku **Měrná jednotka**.</span><span class="sxs-lookup"><span data-stu-id="ddbac-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="ddbac-159">Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ddbac-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="ddbac-160">Hodnota šablony, která má mapu hodnoty, je definována pro o**SalesUnitSymbol** do **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="ddbac-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ddbac-161">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="ddbac-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="ddbac-162">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="ddbac-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="ddbac-163">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="ddbac-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="ddbac-164">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="ddbac-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="ddbac-165">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ddbac-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="ddbac-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="ddbac-166">SalesInvoiceHeader</span></span>

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="ddbac-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="ddbac-168">SalesInvoiceLine</span></span>

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="ddbac-170">Související témata</span><span class="sxs-lookup"><span data-stu-id="ddbac-170">Related topics</span></span>

[<span data-ttu-id="ddbac-171">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="ddbac-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="ddbac-172">Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddbac-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="ddbac-173">Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="ddbac-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="ddbac-174">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddbac-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="ddbac-175">Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="ddbac-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







