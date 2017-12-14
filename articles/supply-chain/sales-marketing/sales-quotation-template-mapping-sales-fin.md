---
title: "Synchronizace hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků přímo z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 8a75c6dd91020ab3e676e2bb40d5c822731e244f
ms.contentlocale: cs-cz
ms.lasthandoff: 11/14/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="8c9d5-103">Synchronizace hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8c9d5-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8c9d5-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků přímo z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

> [!NOTE]
> <span data-ttu-id="8c9d5-105">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="8c9d5-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="8c9d5-106">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="8c9d5-106">Template and tasks</span></span>

<span data-ttu-id="8c9d5-107">K synchronizaci hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="8c9d5-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="8c9d5-108">**Název šablony v integraci dat:** Prodejní nabídky (Sales do Fin and Ops) - Přímo</span><span class="sxs-lookup"><span data-stu-id="8c9d5-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="8c9d5-109">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="8c9d5-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="8c9d5-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="8c9d5-110">QuoteHeader</span></span>
    - <span data-ttu-id="8c9d5-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="8c9d5-111">QuoteLine</span></span>

<span data-ttu-id="8c9d5-112">Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní nabídky a mmohou se objevit řádky:</span><span class="sxs-lookup"><span data-stu-id="8c9d5-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="8c9d5-113">Produkty (Fin and Ops do Sales) - přímo</span><span class="sxs-lookup"><span data-stu-id="8c9d5-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="8c9d5-114">Účty (Sales do Fin and Ops) - přímo (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="8c9d5-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="8c9d5-115">Kontakty na zákazníky (Sales do Fin and Ops) - přímo (pokud se používají)</span><span class="sxs-lookup"><span data-stu-id="8c9d5-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="8c9d5-116">Sada entit</span><span class="sxs-lookup"><span data-stu-id="8c9d5-116">Entity set</span></span>

| <span data-ttu-id="8c9d5-117">Prodej.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-117">Sales</span></span>        | <span data-ttu-id="8c9d5-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8c9d5-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="8c9d5-119">Citáty</span><span class="sxs-lookup"><span data-stu-id="8c9d5-119">Quotes</span></span>       | <span data-ttu-id="8c9d5-120">Záhlaví prodejní nabídky CDS</span><span class="sxs-lookup"><span data-stu-id="8c9d5-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="8c9d5-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="8c9d5-121">QuoteDetails</span></span> | <span data-ttu-id="8c9d5-122">Řádky prodejní nabídky CDS</span><span class="sxs-lookup"><span data-stu-id="8c9d5-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="8c9d5-123">Tok entity</span><span class="sxs-lookup"><span data-stu-id="8c9d5-123">Entity flow</span></span>

<span data-ttu-id="8c9d5-124">Prodejní nabídky jsou vytvořeny v aplikaci Sales a jsou synchronizovány do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8c9d5-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="8c9d5-125">Prodejní nabídky z aplikace Sales jsou synchronizovány pouze v případě, že jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="8c9d5-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="8c9d5-126">Jsou externě zachovány všechny nabídky produktu na prodejní nabídce.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="8c9d5-127">Po kliknutí na tlačítko **Aktivovat nabídku** bude prodejní nabídka aktivní.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8c9d5-128">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="8c9d5-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="8c9d5-129">Pole **Má pouze externě udržované produkty** bylo přidáno do entity **Nabídka** ke konzistentnímu sledování, zda prodejní nabídka sestává zcela z externě spravovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="8c9d5-130">Pokud má prodejní nabídka pouze externě spravované produkty, produkty jsou evidovány v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="8c9d5-131">Toto chování pomáhá zaručit že nezkusíte synchronizovat řádky prodejní nabídky s produkty, které mají v aplikaci Finance and Operations neznámé produkty.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="8c9d5-132">Všechny produkty nabídky na prodejní nabídce jsou aktualizovány informacemi z pole **Má pouze externě udržované produkty** ze záhlaví prodejní nabídky.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="8c9d5-133">Tato informace se nachází v poli **Nabídka má pouze externě udržované produkty** v entitě **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="8c9d5-134">Slevu lze přidat k produkt nabídky a tato sleva bude synchronizována do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="8c9d5-135">Pole **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolována nastavením v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="8c9d5-136">Toto nastavení v současné době nepodporuje mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="8c9d5-137">V aktuálním designu jsou pole **Cena**, **Sleva**, **Náklady** a **Daň** udržována a zpracovávána v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="8c9d5-138">V aplikaci Sales způsobuje toto řešení, že jsou následující pole jen pro čtení, protože hodnoty nejsou synchronizovány s aplikací Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="8c9d5-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="8c9d5-139">Pole jen pro čtení v záhlaví prodejní nabídky: **Sleva %**, **Sleva** a **Částka dopravného**</span><span class="sxs-lookup"><span data-stu-id="8c9d5-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="8c9d5-140">Pole jen pro čtení u produktů nabídky: **Daň**</span><span class="sxs-lookup"><span data-stu-id="8c9d5-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="8c9d5-141">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="8c9d5-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="8c9d5-142">Před synchronizací prodejních nabídek je důležité, abyste aktualizovali následující nastavení.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="8c9d5-143">Nastavení v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="8c9d5-143">Setup in Sales</span></span>

- <span data-ttu-id="8c9d5-144">Zajistěte, že jsou nastavena oprávnění pro tým, ke kterému je uživatel ze sady připojení v aplikaci Sales přiřazen.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="8c9d5-145">Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým ho nemá.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="8c9d5-146">Pokud nemá tým přístup správce při spuštění projektu z integrace dat, dostanete chybovou zprávu s oznámením, že hlavní tým chybí.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="8c9d5-147">Chcete-li nastavit oprávnění pro tým, přejděte na **Nastavení** &gt; **Zabezpečení** &gt; **Týmy**a vyberte příslušný tým.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="8c9d5-148">Vyberte **Spravovat role**a poté vyberte roli, která má požadovaná oprávnění, jako je například **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="8c9d5-149">Přejděte na **Nastavení** &gt; **Správa** &gt; **Nastavení systému** &gt; **Prodej** a ujistěte se, že se používají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="8c9d5-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="8c9d5-150">Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="8c9d5-151">Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="8c9d5-152">Nastavení projektu integrace dat</span><span class="sxs-lookup"><span data-stu-id="8c9d5-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="8c9d5-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="8c9d5-153">QuoteHeader</span></span>

- <span data-ttu-id="8c9d5-154">Ujistěte se, že existuje požadované mapování pro **Shipto\_country** do **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="8c9d5-155">V mapě hodnot můžete definovat výchozí hodnotu, která se používá v případě, že je ponechána prázdná.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="8c9d5-156">Pouze ponechte levou stranu prázdnou a pravou stranu nastavte na požadovanou zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="8c9d5-157">Tímto způsobem nemusíte zadávat zemi nebo oblast pro národní objednávky.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="8c9d5-158">Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí a kde prázdná hodnota se rovná **US**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="8c9d5-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="8c9d5-159">QuoteLine</span></span>

- <span data-ttu-id="8c9d5-160">Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="8c9d5-161">Ujistěte se, že požadované jednotky jsou definovány v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="8c9d5-162">Hodnota šablony, která má mapu hodnoty, je definována pro **oumid.name** do **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="8c9d5-163">Volitelné: Můžete přidat následující mapování na pomoc při zajištění, že budou řádky prodejní nabídky importovány do aplikace Finance and Operations, pokud neexistují žádné výchozí informace od odběratele nebo produktu:</span><span class="sxs-lookup"><span data-stu-id="8c9d5-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="8c9d5-164">**SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="8c9d5-165">Neexistuje žádná výchozí hodnota šablony pro **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="8c9d5-166">**WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="8c9d5-167">Neexistuje žádná výchozí hodnota šablony pro **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="8c9d5-168">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="8c9d5-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="8c9d5-169">Pole **Slevy**, **náklady**, a **daň** jsou kontrolovány složitým nastavením aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="8c9d5-170">Toto nastavení v současné době nepodporuje mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="8c9d5-171">V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** zpracována aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="8c9d5-172">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="8c9d5-173">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="8c9d5-174">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="8c9d5-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="8c9d5-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="8c9d5-175">QuoteHeader</span></span>

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="8c9d5-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="8c9d5-177">QuoteLine</span></span>

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="8c9d5-179">Související témata</span><span class="sxs-lookup"><span data-stu-id="8c9d5-179">Related topics</span></span>

[<span data-ttu-id="8c9d5-180">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="8c9d5-180">Prospect to cash</span></span>](prospect-to-cash.md)

