---
title: Synchronizace hlaviček a řádků prodejní nabídky přímo z aplikace Sales do Supply Chain Management
description: Toto téma se věnuje šablonám a základním úlohám, které se používají k synchronizaci záhlaví a řádek prodejní nabídky přímo z aplikace Dynamics 365 Sales do Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 848464cbc62623502b9b87b9b41dcc17150e85ba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838998"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="2c98a-103">Synchronizace hlaviček a řádků prodejní nabídky přímo z aplikace Sales do Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2c98a-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2c98a-104">Toto téma se věnuje šablonám a základním úlohám, které se používají k synchronizaci záhlaví a řádek prodejní nabídky přímo z aplikace Dynamics 365 Sales do Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="2c98a-105">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="2c98a-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2c98a-106">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="2c98a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2c98a-107">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="2c98a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="2c98a-108">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="2c98a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="2c98a-109">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="2c98a-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="2c98a-110">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2c98a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="2c98a-111">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="2c98a-111">Template and tasks</span></span>

<span data-ttu-id="2c98a-112">K synchronizaci hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Supply Chain Management slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="2c98a-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="2c98a-113">**Název šablony v integraci dat:** Prodejní nabídky (Sales do Supply Chain Management) - Přímo</span><span class="sxs-lookup"><span data-stu-id="2c98a-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="2c98a-114">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="2c98a-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="2c98a-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2c98a-115">QuoteHeader</span></span>
    - <span data-ttu-id="2c98a-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2c98a-116">QuoteLine</span></span>

<span data-ttu-id="2c98a-117">Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní nabídky a mmohou se objevit řádky:</span><span class="sxs-lookup"><span data-stu-id="2c98a-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="2c98a-118">Produkty (Supply Chain Management do Sales) – Přímo</span><span class="sxs-lookup"><span data-stu-id="2c98a-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="2c98a-119">Obchodní vztahy (Sales do Supply Chain Management) – Přímo (pokud se používá)</span><span class="sxs-lookup"><span data-stu-id="2c98a-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="2c98a-120">Kontakty na odběratele (Sales do Supply Chain Management) – Přímo (pokud se používá)</span><span class="sxs-lookup"><span data-stu-id="2c98a-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="2c98a-121">Sada entit</span><span class="sxs-lookup"><span data-stu-id="2c98a-121">Entity set</span></span>

| <span data-ttu-id="2c98a-122">Prodej.</span><span class="sxs-lookup"><span data-stu-id="2c98a-122">Sales</span></span>        | <span data-ttu-id="2c98a-123">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="2c98a-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="2c98a-124">Citáty</span><span class="sxs-lookup"><span data-stu-id="2c98a-124">Quotes</span></span>       | <span data-ttu-id="2c98a-125">Záhlaví prodejní nabídky Dataverse</span><span class="sxs-lookup"><span data-stu-id="2c98a-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="2c98a-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="2c98a-126">QuoteDetails</span></span> | <span data-ttu-id="2c98a-127">Řádky prodejní nabídky Dataverse</span><span class="sxs-lookup"><span data-stu-id="2c98a-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="2c98a-128">Tok entity</span><span class="sxs-lookup"><span data-stu-id="2c98a-128">Entity flow</span></span>

<span data-ttu-id="2c98a-129">Prodejní nabídky jsou vytvořeny v aplikaci Sales a jsou synchronizovány do Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="2c98a-130">Prodejní nabídky z aplikace Sales jsou synchronizovány pouze v případě, že jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="2c98a-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="2c98a-131">Jsou externě zachovány všechny nabídky produktu na prodejní nabídce.</span><span class="sxs-lookup"><span data-stu-id="2c98a-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="2c98a-132">Po kliknutí na tlačítko **Aktivovat nabídku** bude prodejní nabídka aktivní.</span><span class="sxs-lookup"><span data-stu-id="2c98a-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2c98a-133">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="2c98a-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="2c98a-134">Pole **Má pouze externě udržované produkty** bylo přidáno do entity **Nabídka** ke konzistentnímu sledování, zda prodejní nabídka sestává zcela z externě spravovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="2c98a-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="2c98a-135">Pokud má prodejní nabídka pouze externě spravované produkty, produkty jsou evidovány v modulu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="2c98a-136">Toto chování pomáhá zaručit že nezkusíte synchronizovat řádky prodejní nabídky s produkty, které mají v aplikaci Supply Chain Management neznámé produkty.</span><span class="sxs-lookup"><span data-stu-id="2c98a-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="2c98a-137">Všechny produkty nabídky na prodejní nabídce jsou aktualizovány informacemi z pole **Má pouze externě udržované produkty** ze záhlaví prodejní nabídky.</span><span class="sxs-lookup"><span data-stu-id="2c98a-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="2c98a-138">Tato informace se nachází v poli **Nabídka má pouze externě udržované produkty** v entitě **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="2c98a-139">Slevu lze přidat k produkt nabídky a tato sleva bude synchronizována do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="2c98a-140">Pole **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolována nastavením v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="2c98a-141">Toto nastavení v současné době nepodporuje mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="2c98a-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="2c98a-142">V aktuálním designu jsou pole **Cena**, **Sleva**, **Náklady** a **Daň** udržována a zpracovávána v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="2c98a-143">V aplikaci Sales způsobuje toto řešení, že jsou následující pole jen pro čtení, protože hodnoty nejsou synchronizovány s aplikací Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="2c98a-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="2c98a-144">Pole jen pro čtení v záhlaví prodejní nabídky: **Sleva %**, **Sleva** a **Částka dopravného**</span><span class="sxs-lookup"><span data-stu-id="2c98a-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="2c98a-145">Pole jen pro čtení u produktů nabídky: **Daň**</span><span class="sxs-lookup"><span data-stu-id="2c98a-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2c98a-146">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="2c98a-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="2c98a-147">Před synchronizací prodejních nabídek je důležité, abyste aktualizovali následující nastavení.</span><span class="sxs-lookup"><span data-stu-id="2c98a-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="2c98a-148">Nastavení v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="2c98a-148">Setup in Sales</span></span>

- <span data-ttu-id="2c98a-149">Zajistěte, že jsou nastavena oprávnění pro tým, ke kterému je uživatel ze sady připojení v aplikaci Sales přiřazen.</span><span class="sxs-lookup"><span data-stu-id="2c98a-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="2c98a-150">Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým ho nemá.</span><span class="sxs-lookup"><span data-stu-id="2c98a-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="2c98a-151">Pokud nemá tým přístup správce při spuštění projektu z integrace dat, dostanete chybovou zprávu s oznámením, že hlavní tým chybí.</span><span class="sxs-lookup"><span data-stu-id="2c98a-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="2c98a-152">Chcete-li nastavit oprávnění pro tým, přejděte na **Nastavení** &gt; **Zabezpečení** &gt; **Týmy** a vyberte příslušný tým.</span><span class="sxs-lookup"><span data-stu-id="2c98a-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="2c98a-153">Vyberte **Spravovat role** a poté vyberte roli, která má požadovaná oprávnění, jako je například **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="2c98a-154">Přejděte na **Nastavení** &gt; **Správa** &gt; **Nastavení systému** &gt; **Prodej** a ujistěte se, že se používají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="2c98a-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="2c98a-155">Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="2c98a-156">Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="2c98a-157">Nastavení projektu integrace dat</span><span class="sxs-lookup"><span data-stu-id="2c98a-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="2c98a-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2c98a-158">QuoteHeader</span></span>

- <span data-ttu-id="2c98a-159">Ujistěte se, že existuje požadované mapování pro **Shipto\_country** do **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="2c98a-160">V mapě hodnot můžete definovat výchozí hodnotu, která se používá v případě, že je ponechána prázdná.</span><span class="sxs-lookup"><span data-stu-id="2c98a-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="2c98a-161">Pouze ponechte levou stranu prázdnou a pravou stranu nastavte na požadovanou zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="2c98a-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="2c98a-162">Tímto způsobem nemusíte zadávat zemi nebo oblast pro národní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2c98a-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="2c98a-163">Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí a kde prázdná hodnota se rovná **US**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="2c98a-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2c98a-164">QuoteLine</span></span>

- <span data-ttu-id="2c98a-165">Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="2c98a-166">Ujistěte se, že požadované jednotky jsou definovány v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="2c98a-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="2c98a-167">Hodnota šablony, která má mapu hodnoty, je definována pro **oumid.name** do **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="2c98a-168">Volitelné: Můžete přidat následující mapování na pomoc při zajištění, že budou řádky prodejní nabídky importovány do aplikace Supply Chain Management, pokud neexistují žádné výchozí informace od odběratele nebo produktu:</span><span class="sxs-lookup"><span data-stu-id="2c98a-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="2c98a-169">**SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="2c98a-170">Neexistuje žádná výchozí hodnota šablony pro **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="2c98a-171">**WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="2c98a-172">Neexistuje žádná výchozí hodnota šablony pro **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="2c98a-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="2c98a-173">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="2c98a-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="2c98a-174">Pole **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolována složitým nastavením v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="2c98a-175">Toto nastavení v současné době nepodporuje mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="2c98a-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="2c98a-176">V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** zpracována aplikací Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c98a-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="2c98a-177">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="2c98a-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="2c98a-178">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="2c98a-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2c98a-179">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="2c98a-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="2c98a-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2c98a-180">QuoteHeader</span></span>

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="2c98a-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2c98a-182">QuoteLine</span></span>

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="2c98a-184">Související témata</span><span class="sxs-lookup"><span data-stu-id="2c98a-184">Related topics</span></span>

[<span data-ttu-id="2c98a-185">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="2c98a-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]