---
title: "Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních objednávek a řádků přímo z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="98680-103">Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="98680-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="98680-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních objednávek a řádků přímo z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="98680-105">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="98680-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="98680-106">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="98680-107">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="98680-108">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="98680-109">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="98680-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="98680-110">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="98680-110">Templates and tasks</span></span>

<span data-ttu-id="98680-111">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="98680-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="98680-112">Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="98680-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="98680-113">K synchronizaci hlaviček a řádků prodejních objednávek z aplikace Finance and Operations do aplikace Sales slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="98680-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="98680-114">**Název šablony v integraci dat:** Prodejní objednávky (Fin and Ops do Sales) - Přímo</span><span class="sxs-lookup"><span data-stu-id="98680-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="98680-115">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="98680-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="98680-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="98680-116">OrderHeader</span></span>
    - <span data-ttu-id="98680-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="98680-117">OrderLine</span></span>

<span data-ttu-id="98680-118">Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní faktury a mohou se objevit řádky:</span><span class="sxs-lookup"><span data-stu-id="98680-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="98680-119">Produkty (Fin and Ops do Sales) - přímo</span><span class="sxs-lookup"><span data-stu-id="98680-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="98680-120">Účty (Sales do Fin and Ops) - přímo (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="98680-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="98680-121">Kontakty na zákazníky (Sales do Fin and Ops) - přímo (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="98680-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="98680-122">Sada entit</span><span class="sxs-lookup"><span data-stu-id="98680-122">Entity set</span></span>

| <span data-ttu-id="98680-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="98680-123">Finance and Operations</span></span>  | <span data-ttu-id="98680-124">Prodej.</span><span class="sxs-lookup"><span data-stu-id="98680-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="98680-125">Záhlaví prodejní objednávky CDS</span><span class="sxs-lookup"><span data-stu-id="98680-125">CDS sales order headers</span></span> | <span data-ttu-id="98680-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="98680-126">SalesOrders</span></span>       |
| <span data-ttu-id="98680-127">Řádky prodejní objednávky CDS</span><span class="sxs-lookup"><span data-stu-id="98680-127">CDS sales order lines</span></span>   | <span data-ttu-id="98680-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="98680-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="98680-129">Tok entity</span><span class="sxs-lookup"><span data-stu-id="98680-129">Entity flow</span></span>

<span data-ttu-id="98680-130">Prodejní objednávky jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="98680-131">Filtry v šabloně pomáhají zajistit, že do synchronizace jsou zahrnuty pouze příslušné prodejní objednávky:</span><span class="sxs-lookup"><span data-stu-id="98680-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="98680-132">Objednávající a fakturující odběratel na prodejní objednávce, která pochází z aplikace Sales, budou zahrnuti do procesu synchronizace.</span><span class="sxs-lookup"><span data-stu-id="98680-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="98680-133">V aplikaci Finance and Operations se používají pole **OrderingCustomerIsExternallyMaintained** a **InvoiceCustomerIsExternallyMaintained** ke sledování ke sledování synchronizace v datových entitách.</span><span class="sxs-lookup"><span data-stu-id="98680-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="98680-134">Prodejní objednávka musí být v aplikaci Finance and Operations potvrzena.</span><span class="sxs-lookup"><span data-stu-id="98680-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="98680-135">Pouze potvrzené prodejní objednávky nebo prodejní objednávky s vyšším stavem zpracování, například stavem **Expedováno** nebo **Fakturováno**, budou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="98680-136">Po vytvoření nebo úpravě prodejní objednávky musí být provedena v aplikaci Finance and Operations dávková úloha **Vypočítat celkové tržby**.</span><span class="sxs-lookup"><span data-stu-id="98680-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="98680-137">Pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="98680-138">Aktuálně není daň související s náklady na záhlaví prodejní objednávky zahrnuta do synchronizace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="98680-139">Aplikace Sales nepodporuje daňové informace na úrovni záhlaví.</span><span class="sxs-lookup"><span data-stu-id="98680-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="98680-140">Daň, která souvisí s náklady na úrovni řádku, bude zahrnuta do procesu synchronizace.</span><span class="sxs-lookup"><span data-stu-id="98680-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="98680-141">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="98680-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="98680-142">Nová pole byla přidána do entity **Objednávka** a zobrazí na stránce:</span><span class="sxs-lookup"><span data-stu-id="98680-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="98680-143">**Je externě spravováno** - Nastavte tuto možnost na **Ano**, když pořadí pochází z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="98680-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="98680-144">**Stav zpracování** - Toto pole ukazuje stav zpracování objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="98680-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="98680-145">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="98680-145">The following values are available:</span></span>

    - <span data-ttu-id="98680-146">Aktivní</span><span class="sxs-lookup"><span data-stu-id="98680-146">Active</span></span>
    - <span data-ttu-id="98680-147">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="98680-147">Confirmed</span></span>
    - <span data-ttu-id="98680-148">Dodací list</span><span class="sxs-lookup"><span data-stu-id="98680-148">Packing Slip</span></span>
    - <span data-ttu-id="98680-149">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="98680-149">Invoiced</span></span>
    - <span data-ttu-id="98680-150">Vydáno</span><span class="sxs-lookup"><span data-stu-id="98680-150">Picked</span></span>
    - <span data-ttu-id="98680-151">Částečně vyskladněno</span><span class="sxs-lookup"><span data-stu-id="98680-151">Partially Picked</span></span>
    - <span data-ttu-id="98680-152">Částečně zabaleno</span><span class="sxs-lookup"><span data-stu-id="98680-152">Partially Packed</span></span>
    - <span data-ttu-id="98680-153">Expedováno</span><span class="sxs-lookup"><span data-stu-id="98680-153">Shipped</span></span>
    - <span data-ttu-id="98680-154">Částečně expedováno</span><span class="sxs-lookup"><span data-stu-id="98680-154">Partially Shipped</span></span>
    - <span data-ttu-id="98680-155">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="98680-155">Partially Invoiced</span></span>
    - <span data-ttu-id="98680-156">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="98680-156">Cancelled</span></span>

<span data-ttu-id="98680-157">Nastavení **Má pouze externě udržované produkty** se používá v jiných scénářích prodejní objednávky (například při synchronizaci z aplikace Sales do aplikace Finance and Operations), aby se konzistentně sledovalo, zda je prodejní objednávka tvořena zcela z externě udržovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="98680-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="98680-158">Pokud prodejní objednávka sestává zcela z externě spravovaných produktů, produkty jsou evidovány v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="98680-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="98680-159">Toto nastavení pomáhá zaručit, že se nepokusíte synchronizovat řádky prodejní objednávky s produkty, které mají v aplikaci Finance and Operations neznámé produkty.</span><span class="sxs-lookup"><span data-stu-id="98680-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="98680-160">Tlačítka **Vytvořit fakturu**, **Zrušit objednávku**, **Přepočítat**, **Získat produkty** a **Vyhledávání adresy** na stránce **Prodejní objednávka** jsou pro externě udržované objednávky skryta, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="98680-161">Stránku objednávky nelze upravovat, protože informace o prodejní objednávce budou synchronizovány z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="98680-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="98680-162">Stav prodejní objednávky zůstane **Aktivní**, aby se zajistilo, že změny z aplikace Finance and Operations mohou být odeslány do prodejní objednávky v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="98680-163">Chcete-li kontrolovat toto chování, nastavte hodnotu **Statecode \[Stav\]** na **Aktivní** v projektu integrace dat.</span><span class="sxs-lookup"><span data-stu-id="98680-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="98680-164">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="98680-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="98680-165">Před synchronizací prodejních objednávek je důležité aktualizovat následující nastavení v systémech:</span><span class="sxs-lookup"><span data-stu-id="98680-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="98680-166">Nastavení v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="98680-166">Setup in Sales</span></span>

- <span data-ttu-id="98680-167">Zajistěte, že jsou nastavena oprávnění pro tým, ke kterému je uživatel ze sady připojení aplikace Sales přiřazen.</span><span class="sxs-lookup"><span data-stu-id="98680-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="98680-168">Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým ho nemá.</span><span class="sxs-lookup"><span data-stu-id="98680-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="98680-169">Pokud nemá tým přístup správce při spuštění projektu z integrace dat, dostanete chybovou zprávu s oznámením, že hlavní tým chybí.</span><span class="sxs-lookup"><span data-stu-id="98680-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="98680-170">Přejděte na **Nastavení** > **Zabezpečení** > **Týmy**, vyberte příslušný tým, zvolte **Spravovat role** a vyberte roli s požadovanými oprávněními, například **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="98680-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="98680-171">Přejděte na **Nastavení** > **Správa** > **Nastavení systému** > **Prodej**a ujistěte se, že se používají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="98680-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="98680-172">Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="98680-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="98680-173">Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.</span><span class="sxs-lookup"><span data-stu-id="98680-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="98680-174">Nastavení v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="98680-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="98680-175">Přejděte na  **Prodej a marketing** > **Periodické úlohy** > **Vypočítat celkové tržby** a nastavte úlohu, aby se spustila jako dávková úloha.</span><span class="sxs-lookup"><span data-stu-id="98680-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="98680-176">Nastavte možnost **Vypočítat celkové částky prodejních objednávek** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="98680-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="98680-177">Tento krok je důležitý, protože pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="98680-178">Frekvence dávkové úlohy musí být ve shodě s frekvencí synchronizace prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="98680-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="98680-179">Nastavení projektu integrace dat</span><span class="sxs-lookup"><span data-stu-id="98680-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="98680-180">Úloha SalesHeader</span><span class="sxs-lookup"><span data-stu-id="98680-180">SalesHeader task</span></span>

- <span data-ttu-id="98680-181">Ujistěte se, že existuje požadované mapování pro **InvoiceCountryRegionId** do **BillingAddress\_Country** a pro **DeliveryCountryRegionId** do **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="98680-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="98680-182">Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí.</span><span class="sxs-lookup"><span data-stu-id="98680-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="98680-183">Ceník je povinný pro vytvoření objednávek v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="98680-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="98680-184">Aktualizujte mapu hodnot pro **pricelevelid.name \[Název ceníku\]** do ceníku, použitého v aplikaci Sales podle měny.</span><span class="sxs-lookup"><span data-stu-id="98680-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="98680-185">Výchozí ceník můžete použít pro jednu měnu.</span><span class="sxs-lookup"><span data-stu-id="98680-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="98680-186">Popřípadě pokud máte ceníky v několika měnách, můžete použít mapu hodnot.</span><span class="sxs-lookup"><span data-stu-id="98680-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="98680-187">Výchozí hodnota šablony pro  **pricelevelid.name \[Název ceníku\]** je **CRM služba USA (vzorek)**.</span><span class="sxs-lookup"><span data-stu-id="98680-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="98680-188">Úloha SalesLine</span><span class="sxs-lookup"><span data-stu-id="98680-188">SalesLine task</span></span>

- <span data-ttu-id="98680-189">Ujistěte se, že existuje požadované mapování pro  **DeliveryCountryRegionId** do **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="98680-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="98680-190">Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí.</span><span class="sxs-lookup"><span data-stu-id="98680-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="98680-191">Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="98680-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="98680-192">Hodnota šablony, která má mapu hodnoty, je definována pro o**SalesUnitSymbol** do **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="98680-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="98680-193">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="98680-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="98680-194">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="98680-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="98680-195">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="98680-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="98680-196">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="98680-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="98680-197">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="98680-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="98680-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="98680-198">OrderHeader</span></span>

![Mapování šablony v integrátoru dat](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="98680-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="98680-200">OrderLine</span></span>

![Mapování šablony v integrátoru dat](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="98680-202">Související témata</span><span class="sxs-lookup"><span data-stu-id="98680-202">Related topics</span></span>

[<span data-ttu-id="98680-203">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="98680-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="98680-204">Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="98680-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="98680-205">Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="98680-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="98680-206">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="98680-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="98680-207">Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="98680-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




