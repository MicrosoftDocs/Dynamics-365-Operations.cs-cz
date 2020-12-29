---
title: Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6ffd55585ff43f993876de6c669eb61e74a9fd79
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527307"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="64ee9-103">Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales</span><span class="sxs-lookup"><span data-stu-id="64ee9-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="64ee9-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="64ee9-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="64ee9-105">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci produktů přímo z Dynamics 365 Supply Chain Management do Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="64ee9-106">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="64ee9-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="64ee9-107">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="64ee9-108">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="64ee9-109">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="64ee9-110">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="64ee9-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="64ee9-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="64ee9-111">Templates and tasks</span></span>

<span data-ttu-id="64ee9-112">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="64ee9-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="64ee9-113">Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="64ee9-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="64ee9-114">K synchronizaci účtů z aplikace Supply Chain Management do aplikace Sales slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="64ee9-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="64ee9-115">**Název šablony v integraci dat:** Produkty (Supply Chain Management do Sales) - Přímo</span><span class="sxs-lookup"><span data-stu-id="64ee9-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="64ee9-116">**Název úkolu v projektu integrace dat:** Produkty</span><span class="sxs-lookup"><span data-stu-id="64ee9-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="64ee9-117">Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci produktu.</span><span class="sxs-lookup"><span data-stu-id="64ee9-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="64ee9-118">Sada entit</span><span class="sxs-lookup"><span data-stu-id="64ee9-118">Entity set</span></span>

| <span data-ttu-id="64ee9-119">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="64ee9-119">Supply Chain Management</span></span>    | <span data-ttu-id="64ee9-120">Prodej.</span><span class="sxs-lookup"><span data-stu-id="64ee9-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="64ee9-121">Prodejné uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="64ee9-121">Sellable released products</span></span> | <span data-ttu-id="64ee9-122">Produkty</span><span class="sxs-lookup"><span data-stu-id="64ee9-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="64ee9-123">Tok entity</span><span class="sxs-lookup"><span data-stu-id="64ee9-123">Entity flow</span></span>

<span data-ttu-id="64ee9-124">Produkty se spravují v aplikaci Supply Chain Management a synchronizují se do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="64ee9-125">Datová entita **Prodejné uvolněné produkty** v aplikaci Supply Chain Management exportuje pouze produkty, které jsou *prodejné*.</span><span class="sxs-lookup"><span data-stu-id="64ee9-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="64ee9-126">Prodejné produkty jsou produkty, které mají informace potřebné k tomu, aby mohly být použity na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="64ee9-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="64ee9-127">Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Uvolněný produkt**.</span><span class="sxs-lookup"><span data-stu-id="64ee9-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="64ee9-128">Číslo produktu je použito jako klíč.</span><span class="sxs-lookup"><span data-stu-id="64ee9-128">The product number is used as a key.</span></span> <span data-ttu-id="64ee9-129">Proto při synchronizaci variant produktu do aplikace Sales má každá variantu produktu individuální ID produktu.</span><span class="sxs-lookup"><span data-stu-id="64ee9-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="64ee9-130">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="64ee9-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="64ee9-131">V aplikaci Sales je přidáno u produktů nové pole **Je externě spravováno** k označení, že je daný produkt spravován externě.</span><span class="sxs-lookup"><span data-stu-id="64ee9-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="64ee9-132">Hodnota je ve výchozím nastavení při importu do aplikace Sales nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="64ee9-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="64ee9-133">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="64ee9-133">The following values are available:</span></span>

- <span data-ttu-id="64ee9-134">**Ano** – Produkt pochází z aplikace Supply Chain Management a nebude ho možné upravovat v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="64ee9-135">**Ne** – Produkt byl zadána přímo do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="64ee9-136">**(Prázdné)** – Produkt existoval v aplikaci Sales před povolením řešení zpeněžení potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="64ee9-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="64ee9-137">Pole **Je externě spravován** pomáhá zajistit, že se do aplikaci Supply Chain Management budou synchronizovat pouze nabídky a prodejní objednávky, které mají externě spravované produkty.</span><span class="sxs-lookup"><span data-stu-id="64ee9-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="64ee9-138">Externě spravované produkty jsou automaticky přidány k prvnímu platnému ceníku se stejnou měnou.</span><span class="sxs-lookup"><span data-stu-id="64ee9-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="64ee9-139">Ceníky jsou uspořádány abecedně podle názvu.</span><span class="sxs-lookup"><span data-stu-id="64ee9-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="64ee9-140">Jako cena v ceníku se používá prodejní cena produktu z aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="64ee9-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="64ee9-141">Proto musí být v aplikaci Sales ceník pro každou prodejní měnu produktu v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="64ee9-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="64ee9-142">Měna pro uvolněné prodejné produkty je nastavena na zúčtovací měnu v právnické osobě, z níž je exportován produkt.</span><span class="sxs-lookup"><span data-stu-id="64ee9-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="64ee9-143">Synchronizaci produktů se nezdaří, pokud neexistuje ceník se shodnou měnou.</span><span class="sxs-lookup"><span data-stu-id="64ee9-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="64ee9-144">Můžete kontrolovat použitý ceník s integrací pomocí mapování pricelevelid.name [výchozí ceník (název)] v projektu integrace dat.</span><span class="sxs-lookup"><span data-stu-id="64ee9-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="64ee9-145">Vstup musí být pouze malými písmeny.</span><span class="sxs-lookup"><span data-stu-id="64ee9-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="64ee9-146">Například výchozí hodnota pro ceník v aplikaci Sales s názvem 'Standardní' bude: Cílové pole:pricelevelid.name [Výchozí ceník (název)] a typ mapování: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="64ee9-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="64ee9-147">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="64ee9-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="64ee9-148">Před spuštěním první synchronizace je třeba vyplnit tabulku Jedinečný produkt pro existující produkty v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="64ee9-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="64ee9-149">Stávajících produkty nebudou synchronizovány před dokončením této úlohy.</span><span class="sxs-lookup"><span data-stu-id="64ee9-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="64ee9-150">V aplikaci Supply Chain Management použijte funkci hledání pro **Naplnění tabulky různých produktů**.</span><span class="sxs-lookup"><span data-stu-id="64ee9-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="64ee9-151">Zvolte možnost **Vyplnit tabulku jedinečných produktů** ke spuštění úlohy.</span><span class="sxs-lookup"><span data-stu-id="64ee9-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="64ee9-152">Tato úloha musí být spuštěna pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="64ee9-152">This job must be run only one time.</span></span>

- <span data-ttu-id="64ee9-153">Ujistěte se, že požadovaná mapa hodnot pro měrnou jednotku prodeje mezi aplikacemi Supply Chain Management a Sales existuje v mapování **SalesUnitSymbol** na **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="64ee9-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="64ee9-154">Aktualizujte mapu hodnot pro položku **Skupina jednotky** (**defaultuomscheduleid.name**), aby odpovídala položce **Skupiny jednotek** v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="64ee9-155">Výchozí hodnota šablony je **Výchozí jednotka**.</span><span class="sxs-lookup"><span data-stu-id="64ee9-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="64ee9-156">Ujistěte se, že všechny prodejní měrné jednotky pro všechny produkty z aplikace Supply Chain Management existují v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="64ee9-157">Ujistěte se, že existují ceníky v aplikaci Sales pro každou prodejní měnu produktu v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="64ee9-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="64ee9-158">Při vytváření produktů v aplikaci Sales mohou mít stav **Koncept** nebo **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="64ee9-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="64ee9-159">Chování se řídí pomocí **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="64ee9-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="64ee9-160">Produkty, které mají při vytváření stav **Koncept** musí být aktivovány předtím, než mohou být přidány do nabídek nebo prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="64ee9-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="64ee9-161">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="64ee9-161">Template mapping in Data integration</span></span>

<span data-ttu-id="64ee9-162">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="64ee9-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="64ee9-163">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="64ee9-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Mapování šablony v integrátoru dat](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="64ee9-165">Související témata</span><span class="sxs-lookup"><span data-stu-id="64ee9-165">Related topics</span></span>

[<span data-ttu-id="64ee9-166">Zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="64ee9-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="64ee9-167">Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="64ee9-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="64ee9-168">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="64ee9-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="64ee9-169">Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="64ee9-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="64ee9-170">Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="64ee9-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



