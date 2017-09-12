---
title: "Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="1d1ea-103">Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1d1ea-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1d1ea-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="1d1ea-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="1d1ea-105">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků z aplikace Microsoft Dynamics 365 for Sales (Sales) do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="1d1ea-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="1d1ea-106">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="1d1ea-106">Template and tasks</span></span>

<span data-ttu-id="1d1ea-107">K synchronizaci hlaviček a řádků prodejních nabídek v aplikaci Finance and Operations slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="1d1ea-108">**Název šablony:** Sales Quotes (Sales to Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1d1ea-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="1d1ea-109">**Názvy úkolů v projektu:**</span><span class="sxs-lookup"><span data-stu-id="1d1ea-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="1d1ea-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="1d1ea-110">QuoteHeader</span></span>
    - <span data-ttu-id="1d1ea-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="1d1ea-111">QuoteLine</span></span>

<span data-ttu-id="1d1ea-112">Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní nabídky a mmohou se objevit řádky:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="1d1ea-113">Produkty</span><span class="sxs-lookup"><span data-stu-id="1d1ea-113">Products</span></span>
- <span data-ttu-id="1d1ea-114">Obchodní vztahy (pokud jsou použity)</span><span class="sxs-lookup"><span data-stu-id="1d1ea-114">Accounts (if used)</span></span>
- <span data-ttu-id="1d1ea-115">Kontakty (pokud jsou použity)</span><span class="sxs-lookup"><span data-stu-id="1d1ea-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="1d1ea-116">Sada entit</span><span class="sxs-lookup"><span data-stu-id="1d1ea-116">Entity set</span></span>

| <span data-ttu-id="1d1ea-117">Prodej.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-117">Sales</span></span>        | <span data-ttu-id="1d1ea-118">CDS</span><span class="sxs-lookup"><span data-stu-id="1d1ea-118">CDS</span></span>           | <span data-ttu-id="1d1ea-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1d1ea-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="1d1ea-120">Citáty</span><span class="sxs-lookup"><span data-stu-id="1d1ea-120">Quotes</span></span>       | <span data-ttu-id="1d1ea-121">Nabídka</span><span class="sxs-lookup"><span data-stu-id="1d1ea-121">Quotation</span></span>     | <span data-ttu-id="1d1ea-122">Záhlaví prodejní nabídky</span><span class="sxs-lookup"><span data-stu-id="1d1ea-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="1d1ea-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="1d1ea-123">QuoteDetails</span></span> | <span data-ttu-id="1d1ea-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="1d1ea-124">QuotationLine</span></span> | <span data-ttu-id="1d1ea-125">Řádky prodejní nabídky CDS</span><span class="sxs-lookup"><span data-stu-id="1d1ea-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="1d1ea-126">Tok entity</span><span class="sxs-lookup"><span data-stu-id="1d1ea-126">Entity flow</span></span>

<span data-ttu-id="1d1ea-127">Prodejní nabídky jsou vytvořeny v aplikaci Sales a jsou synchronizovány do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1d1ea-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="1d1ea-128">Prodejní nabídky z aplikace Sales jsou synchronizovány pouze v případě, že jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="1d1ea-129">Jsou externě zachovány všechny produkty v řádcích prodejní nabídky.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="1d1ea-130">Prodejní nabídka je aktivní nebo aktivovaná.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1d1ea-131">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="1d1ea-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="1d1ea-132">Pole **Má pouze externě udržované produkty** bylo přidáno do entity Nabídka ke konzistentnímu sledování, zda prodejní nabídka sestává zcela z externě spravovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="1d1ea-133">Pokud má prodejní nabídka pouze externě spravované produkty, produkty jsou evidovány v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="1d1ea-134">Toto chování pomáhá zaručit že nezkusíte synchronizovat řádky prodejní nabídky s produkty, které nejsou známy v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="1d1ea-135">Všechny produkty a řádky nabídky jsou aktualizovány informacemi z pole **Má pouze externě udržované produkty** ze záhlaví nabídky.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="1d1ea-136">Tyto informace lze najít v poli **Nabídka má pouze externě udržované produkty** v entitě Řádek nabídky.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="1d1ea-137">Pole **Slevy**, **náklady**, a **daň** jsou kontrolovány složitým nastavením aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="1d1ea-138">Toto nastavení v současné době nepodporuje mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="1d1ea-139">V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** řízena s zpracována aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="1d1ea-140">V aplikaci Sales způsobuje toto řešení, že jsou následující pole jen pro čtení, protože hodnoty nejsou synchronizovány s aplikací Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="1d1ea-141">**Pole jen pro čtení v záhlaví prodejní nabídky:** % slevy, Sleva, částka dopravného</span><span class="sxs-lookup"><span data-stu-id="1d1ea-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="1d1ea-142">**Pole jen pro čtení pro řádky prodejní nabídky:** Daň</span><span class="sxs-lookup"><span data-stu-id="1d1ea-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1d1ea-143">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="1d1ea-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="1d1ea-144">Před synchronizací prodejních nabídek v aplikaci Sales přejděte na **Nastavení** &gt; **Správa** &gt; **Nastavení systému** &gt; **Sales** a ujistěte se, že je pole **metoda výpočtu slevy** nastaveno na **jednotkové**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="1d1ea-145">Toto nastavení pomáhá zajistit, že sleva položky řádku z aplikace Sales odpovídá nastavení v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="1d1ea-146">V opačném případě nebude sleva opravena v aplikaci Finance and Operations, protože aplikace Finance and Operations bude číst slevu jako slevu podle jednotky i když byla v aplikaci Sales slevou podle řádku.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="1d1ea-147">V aplikaci Finance and Operations přejděte na **Pohledávky** &gt; **Nastavení** &gt; **Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="1d1ea-148">Na kartě **Číselná řada** vyberte číselné řady pro prodejní nabídky a klepněte na tlačítko **Zobrazit podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="1d1ea-149">Poté v části **Obecné nastavení**, nastavte pole **Ruční** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="1d1ea-150">V aplikaci Finance and Operations přejděte na **Pohledávky** &gt; **Nastavení** &gt; **Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="1d1ea-151">Poté na kartě **dodávky** nastavte hodnotu v poli **řízení data dodání** na **žádná**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="1d1ea-152">Toto nastavení pomáhá předcházet selháním synchronizace pro prodejní nabídky.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="1d1ea-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="1d1ea-153">QuoteHeader</span></span>

- <span data-ttu-id="1d1ea-154">Pole **Požadované datum dodání** je v aplikaci Finance and Operations povinné a synchronizace se nezdaří, když je toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="1d1ea-155">Aby se tomuto problému předešlo, je v případě, že je toto pole prázdné, výchozí datum převzato z pole **Zdroj &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="1d1ea-156">Datum by mělo být aktualizováno na preferovanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="1d1ea-157">V současné době nelze zadat hodnotu jako **Dnes** představující dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="1d1ea-158">Je nutné zadat konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-158">You must enter a specific date.</span></span> <span data-ttu-id="1d1ea-159">Výchozí hodnota šablony pro **Požadovat datum doručení** je **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="1d1ea-160">Pole **Kód země/oblasti pro adresu** je v aplikaci Finance and Operations povinné.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="1d1ea-161">Aby nedocházelo k chybám synchronizace, můžete určit výchozí hodnotu, která se použije v případě, že pole v aplikaci Sales zůstane prázdné.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="1d1ea-162">Tato výchozí hodnota je rovněž užitečná, protože není nutné ručně zadat hodnotu do pole **Země** pro místní adresy.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="1d1ea-163">Neexistuje žádná výchozí hodnota šablony pro **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="1d1ea-164">Aktualizujte mapování pro **ID organizace CDS** v okně **Zdroj &gt; CDS** tak, aby odpovídala hodnotě **Organizace CDS** v entitě Organizace:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="1d1ea-165">Výchozí hodnota šablony pro **Organization_OrganizationId** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="1d1ea-166">Výchozí hodnota šablony pro **Account_Organization_OrganizationId** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="1d1ea-167">Výchozí hodnota šablony pro **InvoiceAccount_OrganizationId** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="1d1ea-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="1d1ea-168">QuoteLine</span></span>

- <span data-ttu-id="1d1ea-169">Aktualizujte mapování pro **ID organizace CDS** v okně **Zdroj &gt; CDS** tak, aby odpovídala hodnotě **Organizace CDS** v entitě Organizace:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="1d1ea-170">Výchozí hodnota šablony pro **Organization_OrganizationId** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="1d1ea-171">Výchozí hodnota šablony pro **Product_Organization_Organization_OrganizationId** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="1d1ea-172">Výchozí hodnota šablony pro **Quotation_Organization_Organization_OrganizationId** je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="1d1ea-173">Pole **Požadované datum dodání** je v aplikaci Finance and Operations povinné a synchronizace se nezdaří, když je toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="1d1ea-174">Aby se tomuto problému předešlo, je v případě, že je toto pole prázdné, výchozí datum převzato z pole **Zdroj &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="1d1ea-175">Datum by mělo být aktualizováno na preferovanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="1d1ea-176">V současné době nelze zadat hodnotu jako **Dnes** představující dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="1d1ea-177">Je nutné zadat konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-177">You must enter a specific date.</span></span> <span data-ttu-id="1d1ea-178">Výchozí hodnota šablony pro **Požadovat datum doručení** je **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="1d1ea-179">Můžete přidat následující mapování z okna **CDS &gt; Cíl** na pomoc při zajištění, že budou řádky nabídky importovány do aplikace Finance and Operations, pokud neexistují žádné výchozí informace od odběratele nebo produktu:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="1d1ea-180">**SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="1d1ea-181">Neexistuje žádná výchozí hodnota šablony pro **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="1d1ea-182">**WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="1d1ea-183">Neexistuje žádná výchozí hodnota šablony pro **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="1d1ea-184">Ujistěte se, že požadovaná mapa hodnot pro měrnou jednotku prodeje (MJ) v modulu Finance and Operations existuje v mapování **CDS &gt; Cíl** pro **Quantity_UOM** na **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="1d1ea-185">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="1d1ea-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="1d1ea-186">Pole **Slevy**, **náklady**, a **daň** jsou kontrolovány složitým nastavením aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="1d1ea-187">Toto nastavení v současné době nepodporuje mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="1d1ea-188">V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** zpracována aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="1d1ea-189">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="1d1ea-190">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="1d1ea-191">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="1d1ea-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="1d1ea-192">QuoteHeader</span></span>

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="1d1ea-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="1d1ea-195">QuoteLine</span></span>

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="1d1ea-198">Související témata</span><span class="sxs-lookup"><span data-stu-id="1d1ea-198">Related topics</span></span>

[<span data-ttu-id="1d1ea-199">Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="1d1ea-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="1d1ea-200">Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1d1ea-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="1d1ea-201">Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1d1ea-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



