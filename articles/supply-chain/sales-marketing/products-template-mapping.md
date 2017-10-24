---
title: "Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="cb256-103">Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="cb256-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="cb256-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="cb256-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="cb256-105">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="cb256-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="cb256-106">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="cb256-106">Template and task</span></span>

<span data-ttu-id="cb256-107">Následující šablony a základní úlohy se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) do aplikace Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="cb256-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="cb256-108">Název šablony: Products (Fin and Ops to Sales)</span><span class="sxs-lookup"><span data-stu-id="cb256-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="cb256-109">Název úkolu v projektu: Produkty</span><span class="sxs-lookup"><span data-stu-id="cb256-109">Name of task in project: Products</span></span>

<span data-ttu-id="cb256-110">Synchronizace úkolů vyžadovaných před synchronizací produktů: žádná</span><span class="sxs-lookup"><span data-stu-id="cb256-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="cb256-111">Sada entit</span><span class="sxs-lookup"><span data-stu-id="cb256-111">Entity set</span></span>

| <span data-ttu-id="cb256-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="cb256-112">**Finance and Operations**</span></span> | <span data-ttu-id="cb256-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="cb256-113">**CDS**</span></span> | <span data-ttu-id="cb256-114">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="cb256-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="cb256-115">Prodejné uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="cb256-115">Sellable released products</span></span> | <span data-ttu-id="cb256-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="cb256-116">Product</span></span> | <span data-ttu-id="cb256-117">Produkty</span><span class="sxs-lookup"><span data-stu-id="cb256-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="cb256-118">Tok entity</span><span class="sxs-lookup"><span data-stu-id="cb256-118">Entity flow</span></span>

<span data-ttu-id="cb256-119">Produkty se spravují v aplikaci Finance and Operations a synchronizují s aplikací Sales.</span><span class="sxs-lookup"><span data-stu-id="cb256-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="cb256-120">Entita dat **Sellable uvolněných produktů** na penále a operace exportuje pouze produkty, které jsou prodejnosti, což znamená, že produkty požadované informace pro použití v prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="cb256-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="cb256-121">Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Vydaný produkt**.</span><span class="sxs-lookup"><span data-stu-id="cb256-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="cb256-122">**Číslo produktu** slouží jako klíč, tj. varianty produktu budou synchronizovány se službou CDS a aplikací Sales u jednotlivých **ID produktu** podle **varianty produktu**.</span><span class="sxs-lookup"><span data-stu-id="cb256-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="cb256-123">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="cb256-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="cb256-124">V aplikaci Sales je přidáno nové pole **Je externě spravováno** k označení, že je daný produkt spravován externě.</span><span class="sxs-lookup"><span data-stu-id="cb256-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="cb256-125">Hodnota je ve výchozím nastavení při importu prodeje nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cb256-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="cb256-126">**Je externě spravována = Ano**: produkt pochází z aplikace Finance and Operations a nebude možné ho upravovat v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="cb256-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="cb256-127">**Je externě spravován = Ne**: Produkt je zadán přímo v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="cb256-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="cb256-128">**Je externě spravován = prázdné**: produkt existuje v aplikaci Sales před povolením řešení Zpeněžnění potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="cb256-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="cb256-129">Informace **Je externě spravován** slouží k zajištění, že se v aplikaci Finance and Operations budou synchronizovat pouze pole **Nabídky** a **Prodejní objednávky** s možností **Externě spravované produkty**.</span><span class="sxs-lookup"><span data-stu-id="cb256-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="cb256-130">**Externě spravované produkty** jsou automaticky přidány k prvnímu platnému **ceníku** ve stejné měně.</span><span class="sxs-lookup"><span data-stu-id="cb256-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="cb256-131">Všimněte si, že je seznam seřazený abecedně podle **názvu**.</span><span class="sxs-lookup"><span data-stu-id="cb256-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="cb256-132">Jako cena v **ceníku** se používá prodejní cena produktu z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cb256-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="cb256-133">To znamená, že je třeba mít **ceník** v aplikaci Sales pro každou **Prodejní měnu produktu** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cb256-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="cb256-134">Měna pro uvolněné prodejné produkty je nastavena na zúčtovací měnu v právnické osobě, z níž je exportován produkt.</span><span class="sxs-lookup"><span data-stu-id="cb256-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="cb256-135">Synchronizace produktu se nezdaří bez **ceníku** v odpovídající měně.</span><span class="sxs-lookup"><span data-stu-id="cb256-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="cb256-136">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="cb256-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="cb256-137">Před spuštěním úplně první synchronizace he třeba naplnit **tabulka odlišného produktu** pro existující produkty v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cb256-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="cb256-138">Stávajících produkty nebudou synchronizovány před dokončením této úlohy.</span><span class="sxs-lookup"><span data-stu-id="cb256-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="cb256-139">V aplikaci Finance and Operations použijte funkci hledání pro **Naplnění tabulky různých produktů**.</span><span class="sxs-lookup"><span data-stu-id="cb256-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="cb256-140">Kliknutím na **Naplnit tabulku různých produktů** spusťte úlohu.</span><span class="sxs-lookup"><span data-stu-id="cb256-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="cb256-141">Tuto úlohu je nutné spustit pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="cb256-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="cb256-142">Ujistěte se, že existuje potřebný parametr **ValueMap** pro **Měrnou jednotku** (MJ) prodeje v aplikaci Finance and Operations v části **Zdroj -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="cb256-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="cb256-143">Aktualizujte **CDS Organization ID Organization_OrganizationId** v poli **Zdroj -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="cb256-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="cb256-144">Výchozí hodnota šablony je ORG001.</span><span class="sxs-lookup"><span data-stu-id="cb256-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="cb256-145">Aktualizujte hodnotu **ValueMap** pro **skupinu jednotky** (**defaultuomscheduleid.name**) v poli **CDS -\> Cíl** tak, aby odpovídala **skupinám jednotek** v modulu Sales.</span><span class="sxs-lookup"><span data-stu-id="cb256-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="cb256-146">Hodnota šablony je nastavena na **Výchozí jednotka**.</span><span class="sxs-lookup"><span data-stu-id="cb256-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="cb256-147">Ověřte, že všechny produkty prodávající MJ ze modulu Finance and Operations existují v aplikaci Sales s hodnotou **Seznamy vyskladnění CDS**.</span><span class="sxs-lookup"><span data-stu-id="cb256-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="cb256-148">Zkontrolujte, zda **ceníky** existují v aplikaci Sales pro každou prodejní měnu produktu v aplikaciFinance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cb256-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="cb256-149">V aplikaci Sales lze vytvářet produkty se stavem **Koncept** nebo **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="cb256-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="cb256-150">To se řídí v **Nastavení systému** pod možností **Sales** v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="cb256-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="cb256-151">Produkty, které jsou vytvořeny se stavem konceptu, je třeba aktivovat před jejich přidáním do pole **nabídka** nebo **prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="cb256-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="cb256-152">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="cb256-152">Template mapping in data integrator</span></span>

<span data-ttu-id="cb256-153">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="cb256-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![mapování šablony v integrátoru dat](./media/products-template-mapping-data-integrator-1.png)

![mapování šablony pro produkty v integrátoru dat](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="cb256-156">Související témata</span><span class="sxs-lookup"><span data-stu-id="cb256-156">Related topics</span></span>

[<span data-ttu-id="cb256-157">Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cb256-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="cb256-158">Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cb256-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="cb256-159">Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cb256-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="cb256-160">Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="cb256-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="cb256-161">Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="cb256-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


