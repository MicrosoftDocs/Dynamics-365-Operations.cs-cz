---
title: "Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 6c68c4482cacf70f003669cf335e52e47425d2f7
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="9fe5c-103">Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="9fe5c-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9fe5c-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="9fe5c-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="9fe5c-105">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů přímo z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="9fe5c-106">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="9fe5c-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="9fe5c-107">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="9fe5c-108">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="9fe5c-109">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="9fe5c-110">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="9fe5c-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9fe5c-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="9fe5c-111">Templates and tasks</span></span>

<span data-ttu-id="9fe5c-112">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="9fe5c-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="9fe5c-113">Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9fe5c-114">K synchronizaci produktů z aplikace Finance and Operations do aplikace Sales slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="9fe5c-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="9fe5c-115">**Název šablony v integraci dat:** Produkty (Fin and Ops do Sales) - Přímo</span><span class="sxs-lookup"><span data-stu-id="9fe5c-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="9fe5c-116">**Název úkolu v projektu integrace dat:** Produkty</span><span class="sxs-lookup"><span data-stu-id="9fe5c-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="9fe5c-117">Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci produktu.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="9fe5c-118">Sada entit</span><span class="sxs-lookup"><span data-stu-id="9fe5c-118">Entity set</span></span>

| <span data-ttu-id="9fe5c-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9fe5c-119">Finance and Operations</span></span>     | <span data-ttu-id="9fe5c-120">Prodej.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="9fe5c-121">Prodejné uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="9fe5c-121">Sellable released products</span></span> | <span data-ttu-id="9fe5c-122">Produkty</span><span class="sxs-lookup"><span data-stu-id="9fe5c-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="9fe5c-123">Tok entity</span><span class="sxs-lookup"><span data-stu-id="9fe5c-123">Entity flow</span></span>

<span data-ttu-id="9fe5c-124">Produkty se spravují v aplikaci Finance and Operations a synchronizují s aplikací Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="9fe5c-125">Datová entita **Prodejné uvolněné produkty** v aplikaci Finance and Operations exportuje pouze produkty, které jsou *prodejné*.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="9fe5c-126">Prodejné produkty jsou produkty, které mají informace potřebné k tomu, aby mohly být použity na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="9fe5c-127">Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Uvolněný produkt**.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="9fe5c-128">Číslo produktu je použito jako klíč.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-128">The product number is used as a key.</span></span> <span data-ttu-id="9fe5c-129">Proto při synchronizaci variant produktu do aplikace Sales má každá variantu produktu individuální ID produktu.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9fe5c-130">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="9fe5c-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9fe5c-131">V aplikaci Sales je přidáno u produktů nové pole **Je externě spravováno** k označení, že je daný produkt spravován externě.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="9fe5c-132">Hodnota je ve výchozím nastavení při importu do aplikace Sales nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="9fe5c-133">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="9fe5c-133">The following values are available:</span></span>

- <span data-ttu-id="9fe5c-134">**Ano** – Produkt pochází z aplikace Finance and Operations a nebude ho možné upravovat v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="9fe5c-135">**Ne** – Produkt byl zadána přímo do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="9fe5c-136">**(Prázdné)** – Produkt existoval v aplikaci Sales před povolením řešení zpeněžení potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="9fe5c-137">Pole **Je externě spravován** pomáhá zajistit,, že se do aplikaci Finance and Operations budou synchronizovat pouze nabídky a prodejní objednávky, které mají externě spravované produkty.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="9fe5c-138">Externě spravované produkty jsou automaticky přidány k prvnímu platnému ceníku se stejnou měnou.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="9fe5c-139">Ceníky jsou uspořádány abecedně podle názvu.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="9fe5c-140">Jako cena v ceníku se používá prodejní cena produktu z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="9fe5c-141">Proto musí být v aplikaci Sales ceník pro každou prodejní měnu produktu v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="9fe5c-142">Měna pro uvolněné prodejné produkty je nastavena na zúčtovací měnu v právnické osobě, z níž je exportován produkt.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="9fe5c-143">Synchronizaci produktů se nezdaří, pokud neexistuje ceník se shodnou měnou.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9fe5c-144">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="9fe5c-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="9fe5c-145">Před spuštěním první synchronizace je třeba vyplnit tabulku Jedinečný produkt pro existující produkty v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="9fe5c-146">Stávajících produkty nebudou synchronizovány před dokončením této úlohy.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="9fe5c-147">V aplikaci Finance and Operations použijte funkci hledání pro **Naplnění tabulky různých produktů**.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="9fe5c-148">Zvolte možnost **Vyplnit tabulku jedinečných produktů** ke spuštění úlohy.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="9fe5c-149">Tato úloha musí být spuštěna pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-149">This job must be run only one time.</span></span>

- <span data-ttu-id="9fe5c-150">Ujistěte se, že požadovaná mapa hodnot pro měrnou jednotku prodeje mezi aplikacemi Finance and Operations a Sales existuje v mapování **SalesUnitSymbol** na **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="9fe5c-151">Aktualizujte mapu hodnot pro položku **Skupina jednotky** (**defaultuomscheduleid.name**), aby odpovídala položce **Skupiny jednotek** v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="9fe5c-152">Výchozí hodnota šablony je **Výchozí jednotka**.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="9fe5c-153">Ujistěte se, že všechny prodejní měrné jednotky pro všechny produkty z aplikace Finance and Operations existují v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="9fe5c-154">Ujistěte se, že existují ceníky v aplikaci Sales pro každou prodejní měnu produktu v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="9fe5c-155">Při vytváření produktů v aplikaci Sales mohou mít stav **Koncept** nebo **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="9fe5c-156">Chování se řídí pomocí **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="9fe5c-157">Produkty, které mají při vytváření stav **Koncept** musí být aktivovány předtím, než mohou být přidány do nabídek nebo prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9fe5c-158">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="9fe5c-158">Template mapping in Data integration</span></span>

<span data-ttu-id="9fe5c-159">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="9fe5c-160">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe5c-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Mapování šablony v integrátoru dat](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="9fe5c-162">Související témata</span><span class="sxs-lookup"><span data-stu-id="9fe5c-162">Related topics</span></span>

[<span data-ttu-id="9fe5c-163">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="9fe5c-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="9fe5c-164">Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9fe5c-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="9fe5c-165">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9fe5c-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="9fe5c-166">Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="9fe5c-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="9fe5c-167">Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="9fe5c-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



