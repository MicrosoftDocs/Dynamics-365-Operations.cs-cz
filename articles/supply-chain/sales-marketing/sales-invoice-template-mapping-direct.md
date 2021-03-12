---
title: Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales
description: Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci záhlaví a řádek prodejní faktury přímo z aplikace Dynamics 365 Supply Chain Management do Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
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
ms.openlocfilehash: d7f104b3f2e132b5b517443577a020fda7fa9af3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975003"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="7b2d3-103">Synchronizace záhlaví a řádků prodejních faktur přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="7b2d3-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b2d3-104">Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci záhlaví a řádek prodejní faktury přímo z aplikace Dynamics 365 Supply Chain Management do Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="7b2d3-105">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="7b2d3-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="7b2d3-106">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="7b2d3-107">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="7b2d3-108">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="7b2d3-109">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="7b2d3-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7b2d3-110">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="7b2d3-110">Templates and tasks</span></span>

<span data-ttu-id="7b2d3-111">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="7b2d3-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="7b2d3-112">Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7b2d3-113">K synchronizaci hlaviček a řádků prodejních faktur z aplikace Supply Chain Management do aplikace Sales slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="7b2d3-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="7b2d3-114">**Název šablony v integraci dat:** Prodejní faktury (Fin and Ops do Sales) - Přímo</span><span class="sxs-lookup"><span data-stu-id="7b2d3-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="7b2d3-115">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="7b2d3-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="7b2d3-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="7b2d3-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="7b2d3-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="7b2d3-117">SalesInvoiceLine</span></span>

<span data-ttu-id="7b2d3-118">Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní faktury a mohou se objevit řádky:</span><span class="sxs-lookup"><span data-stu-id="7b2d3-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="7b2d3-119">Produkty (Supply Chain Management do Sales) – Přímo</span><span class="sxs-lookup"><span data-stu-id="7b2d3-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="7b2d3-120">Obchodní vztahy (Sales do Supply Chain Management) – Přímo (pokud se používá)</span><span class="sxs-lookup"><span data-stu-id="7b2d3-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="7b2d3-121">Kontakty (Sales do Supply Chain Management) – Přímo (pokud se používá)</span><span class="sxs-lookup"><span data-stu-id="7b2d3-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="7b2d3-122">Hlavička a řádky prodejní objednávky (Supply Chain Management do Sales): OrderHeader</span><span class="sxs-lookup"><span data-stu-id="7b2d3-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="7b2d3-123">Sada entit</span><span class="sxs-lookup"><span data-stu-id="7b2d3-123">Entity set</span></span>

| <span data-ttu-id="7b2d3-124">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="7b2d3-124">Supply Chain Management</span></span>                              | <span data-ttu-id="7b2d3-125">Prodej.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="7b2d3-126">Záhlaví prodejní faktury odběratele udržované externě</span><span class="sxs-lookup"><span data-stu-id="7b2d3-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="7b2d3-127">Faktury</span><span class="sxs-lookup"><span data-stu-id="7b2d3-127">Invoices</span></span>       |
| <span data-ttu-id="7b2d3-128">Řádky prodejní faktury odběratele udržované externě</span><span class="sxs-lookup"><span data-stu-id="7b2d3-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="7b2d3-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="7b2d3-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="7b2d3-130">Tok entity</span><span class="sxs-lookup"><span data-stu-id="7b2d3-130">Entity flow</span></span>

<span data-ttu-id="7b2d3-131">Prodejní faktury jsou vytvořeny v aplikaci Supply Chain Management a jsou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="7b2d3-132">Aktuálně není daň související s náklady na záhlaví prodejní faktury zahrnuta do synchronizace z aplikace Supply Chain Management do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="7b2d3-133">Aplikace Sales nepodporuje daňové informace na úrovni záhlaví.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="7b2d3-134">Daň, která souvisí s náklady na úrovni řádku, bude zahrnuta do procesu synchronizace.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="7b2d3-135">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="7b2d3-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="7b2d3-136">Pole **Číslo faktury** bylo přidáno do entity **Faktura** a zobrazí se na stránce.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="7b2d3-137">Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Supply Chain Management a synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="7b2d3-138">Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="7b2d3-139">Hodnota **Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Supply Chain Management do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="7b2d3-140">Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="7b2d3-141">Vlastník prodejní objednávky tudíž může zobrazit fakturu.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="7b2d3-142">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="7b2d3-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="7b2d3-143">Před synchronizací prodejních faktur je důležité aktualizovat následující nastavení v systémech:</span><span class="sxs-lookup"><span data-stu-id="7b2d3-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="7b2d3-144">Nastavení v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="7b2d3-144">Setup in Sales</span></span>

<span data-ttu-id="7b2d3-145">Přejděte na **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** a ujistěte se, že se používají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="7b2d3-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="7b2d3-146">Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="7b2d3-147">Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="7b2d3-148">Nastavení projektu integrace dat</span><span class="sxs-lookup"><span data-stu-id="7b2d3-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="7b2d3-149">Úloha SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="7b2d3-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="7b2d3-150">Ujistěte se, že existuje požadované mapování pro  **InvoiceCountryRegionId** do **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="7b2d3-151">Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="7b2d3-152">Ceník je povinný pro vytvoření faktur v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="7b2d3-153">Aktualizujte mapu hodnot pro **pricelevelid.name \[Název ceníku\]** do ceníku, použitého v aplikaci Sales podle měny.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="7b2d3-154">Výchozí ceník můžete použít pro jednu měnu.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="7b2d3-155">Popřípadě pokud máte ceníky v několika měnách, můžete použít mapu hodnot.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="7b2d3-156">Hodnota šablony pro **pricelevelid.name \[Název ceníku\]** je mapa hodnot založená na měně s USD = CRM služba USA (vzorek).</span><span class="sxs-lookup"><span data-stu-id="7b2d3-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="7b2d3-157">Úloha SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="7b2d3-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="7b2d3-158">Ujistěte se, že existuje požadované mapování pro položku **Měrná jednotka**.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="7b2d3-159">Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="7b2d3-160">Hodnota šablony, která má mapu hodnoty, je definována pro o **SalesUnitSymbol** do **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b2d3-161">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="7b2d3-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="7b2d3-162">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="7b2d3-163">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="7b2d3-164">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="7b2d3-165">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="7b2d3-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="7b2d3-166">SalesInvoiceHeader</span></span>

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="7b2d3-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="7b2d3-168">SalesInvoiceLine</span></span>

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="7b2d3-170">Související témata</span><span class="sxs-lookup"><span data-stu-id="7b2d3-170">Related topics</span></span>

[<span data-ttu-id="7b2d3-171">Zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="7b2d3-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="7b2d3-172">Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b2d3-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="7b2d3-173">Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales</span><span class="sxs-lookup"><span data-stu-id="7b2d3-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="7b2d3-174">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7b2d3-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="7b2d3-175">Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7b2d3-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
