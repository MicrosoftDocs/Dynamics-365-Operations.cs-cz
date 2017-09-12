---
title: "Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="8d7b0-103">Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="8d7b0-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="8d7b0-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="8d7b0-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="8d7b0-105">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="8d7b0-106">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="8d7b0-106">Template and task</span></span>

<span data-ttu-id="8d7b0-107">Následující šablony a základní úlohy se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) do aplikace Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="8d7b0-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="8d7b0-108">Název šablony: Products (Fin and Ops to Sales)</span><span class="sxs-lookup"><span data-stu-id="8d7b0-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="8d7b0-109">Název úkolu v projektu: Produkty</span><span class="sxs-lookup"><span data-stu-id="8d7b0-109">Name of task in project: Products</span></span>

<span data-ttu-id="8d7b0-110">Synchronizace úkolů vyžadovaných před synchronizací produktů: žádná</span><span class="sxs-lookup"><span data-stu-id="8d7b0-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="8d7b0-111">Sada entit</span><span class="sxs-lookup"><span data-stu-id="8d7b0-111">Entity set</span></span>

| <span data-ttu-id="8d7b0-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="8d7b0-112">**Finance and Operations**</span></span> | <span data-ttu-id="8d7b0-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="8d7b0-113">**CDS**</span></span> | <span data-ttu-id="8d7b0-114">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="8d7b0-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="8d7b0-115">Prodejné uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="8d7b0-115">Sellable released products</span></span> | <span data-ttu-id="8d7b0-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="8d7b0-116">Product</span></span> | <span data-ttu-id="8d7b0-117">Produkty</span><span class="sxs-lookup"><span data-stu-id="8d7b0-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="8d7b0-118">Tok entity</span><span class="sxs-lookup"><span data-stu-id="8d7b0-118">Entity flow</span></span>

<span data-ttu-id="8d7b0-119">Produkty se spravují v aplikaci Finance and Operations a synchronizují s aplikací Sales.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="8d7b0-120">Entita dat **Sellable uvolněných produktů** na penále a operace exportuje pouze produkty, které jsou prodejnosti, což znamená, že produkty požadované informace pro použití v prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="8d7b0-121">Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Vydaný produkt**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="8d7b0-122">**Číslo produktu** slouží jako klíč, tj. varianty produktu budou synchronizovány se službou CDS a aplikací Sales u jednotlivých **ID produktu** podle **varianty produktu**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8d7b0-123">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="8d7b0-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="8d7b0-124">V aplikaci Sales je přidáno nové pole **Je externě spravováno** k označení, že je daný produkt spravován externě.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="8d7b0-125">Hodnota je ve výchozím nastavení při importu prodeje nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="8d7b0-126">**Je externě spravována = Ano**: produkt pochází z aplikace Finance and Operations a nebude možné ho upravovat v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="8d7b0-127">**Je externě spravován = Ne**: Produkt je zadán přímo v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="8d7b0-128">**Je externě spravován = prázdné**: produkt existuje v aplikaci Sales před povolením řešení Zpeněžnění potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="8d7b0-129">Informace **Je externě spravován** slouží k zajištění, že se v aplikaci Finance and Operations budou synchronizovat pouze pole **Nabídky** a **Prodejní objednávky** s možností **Externě spravované produkty**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="8d7b0-130">**Externě spravované produkty** jsou automaticky přidány k prvnímu platnému **ceníku** ve stejné měně.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="8d7b0-131">Všimněte si, že je seznam seřazený abecedně podle **názvu**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="8d7b0-132">Jako cena v **ceníku** se používá prodejní cena produktu z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="8d7b0-133">To znamená, že je třeba mít **ceník** v aplikaci Sales pro každou **Prodejní měnu produktu** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="8d7b0-134">Měna pro uvolněné prodejné produkty je nastavena na zúčtovací měnu v právnické osobě, z níž je exportován produkt.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="8d7b0-135">Synchronizace produktu se nezdaří bez **ceníku** v odpovídající měně.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="8d7b0-136">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="8d7b0-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="8d7b0-137">Před spuštěním úplně první synchronizace he třeba naplnit **tabulka odlišného produktu** pro existující produkty v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="8d7b0-138">Stávajících produkty nebudou synchronizovány před dokončením této úlohy.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="8d7b0-139">V aplikaci Finance and Operations použijte funkci hledání pro **Naplnění tabulky různých produktů**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="8d7b0-140">Kliknutím na **Naplnit tabulku různých produktů** spusťte úlohu.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="8d7b0-141">Tuto úlohu je nutné spustit pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="8d7b0-142">Ujistěte se, že existuje potřebný parametr **ValueMap** pro **Měrnou jednotku** (MJ) prodeje v aplikaci Finance and Operations v části **Zdroj -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="8d7b0-143">Ujistěte se, že **podporované desetinné hodnoty** pro JM odpovídají vašim požadavkům definovaným ve službě **CDS -\> Cíl**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="8d7b0-144">Pokud požadujete různé hodnoty na MJ, lze to provést pomocí atributu **ValueMap** z jednotky, například [Ks : 0] & [Libra : 2].</span><span class="sxs-lookup"><span data-stu-id="8d7b0-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="8d7b0-145">Výchozí hodnota šablony je 0.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="8d7b0-146">Aktualizujte **CDS Organization ID Organization_OrganizationId** v poli **Zdroj -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="8d7b0-147">Výchozí hodnota šablony je ORG001.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="8d7b0-148">Aktualizujte hodnotu **ValueMap** pro **skupinu jednotky** (**defaultuomscheduleid.name**) v poli **CDS -\> Cíl** tak, aby odpovídala **skupinám jednotek** v modulu Sales.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="8d7b0-149">Hodnota šablony je nastavena na **Výchozí jednotka**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="8d7b0-150">Ověřte, že všechny produkty prodávající MJ ze modulu Finance and Operations existují v aplikaci Sales s hodnotou **Seznamy vyskladnění CDS**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="8d7b0-151">Zkontrolujte, zda **ceníky** existují v aplikaci Sales pro každou prodejní měnu produktu v aplikaciFinance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="8d7b0-152">V aplikaci Sales lze vytvářet produkty se stavem **Koncept** nebo **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="8d7b0-153">To se řídí v **Nastavení systému** pod možností **Sales** v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="8d7b0-154">Produkty, které jsou vytvořeny se stavem konceptu, je třeba aktivovat před jejich přidáním do pole **nabídka** nebo **prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="8d7b0-155">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="8d7b0-155">Template mapping in data integrator</span></span>

<span data-ttu-id="8d7b0-156">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="8d7b0-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![mapování šablony v integrátoru dat](./media/products-template-mapping-data-integrator-1.png)

![mapování šablony pro produkty v integrátoru dat](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="8d7b0-159">Související témata</span><span class="sxs-lookup"><span data-stu-id="8d7b0-159">Related topics</span></span>

[<span data-ttu-id="8d7b0-160">Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8d7b0-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="8d7b0-161">Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8d7b0-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="8d7b0-162">Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8d7b0-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


