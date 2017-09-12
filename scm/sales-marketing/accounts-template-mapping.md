---
title: "Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci obchodních vztahů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: b497f078d9786a5c7630e924da6bb04cad37f5e9
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="7f4cd-103">Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7f4cd-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7f4cd-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="7f4cd-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="7f4cd-105">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci účtů z aplikace Microsoft Dynamics 365 for Sales (Sales) do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="7f4cd-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="7f4cd-106">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="7f4cd-106">Template and task</span></span>

<span data-ttu-id="7f4cd-107">K synchronizaci účtů a řádků prodejních nabídek v aplikaci Finance and Operations slouží následující šablony a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="7f4cd-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="7f4cd-108">**Název šablony:** Accounts (Sales to Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7f4cd-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="7f4cd-109">**Název úkolu do projektu:** účty – účet – Odběratelé</span><span class="sxs-lookup"><span data-stu-id="7f4cd-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="7f4cd-110">Synchronizace úkolů vyžadovaných před synchronizací Účet / Odběratel</span><span class="sxs-lookup"><span data-stu-id="7f4cd-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="7f4cd-111">Sada entit</span><span class="sxs-lookup"><span data-stu-id="7f4cd-111">Entity set</span></span>

| <span data-ttu-id="7f4cd-112">Prodej.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-112">Sales</span></span>    | <span data-ttu-id="7f4cd-113">CDS</span><span class="sxs-lookup"><span data-stu-id="7f4cd-113">CDS</span></span>     | <span data-ttu-id="7f4cd-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7f4cd-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="7f4cd-115">Účty</span><span class="sxs-lookup"><span data-stu-id="7f4cd-115">Accounts</span></span> | <span data-ttu-id="7f4cd-116">Účet</span><span class="sxs-lookup"><span data-stu-id="7f4cd-116">Account</span></span> | <span data-ttu-id="7f4cd-117">Zákazníci</span><span class="sxs-lookup"><span data-stu-id="7f4cd-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="7f4cd-118">Tok entity</span><span class="sxs-lookup"><span data-stu-id="7f4cd-118">Entity flow</span></span>

<span data-ttu-id="7f4cd-119">Účty se spravují v aplikaci Sales a synchronizují s aplikací Finance and Operations jako zákazníci.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="7f4cd-120">Vlastnost **Je externě udržována** těchto odběratelů je nastavena na **Ano** ke sledování odběratelů, kteří pocházejí z prodeje.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="7f4cd-121">Při fakturaci tyto informace slouží k filtrování faktur, které budou synchronizovány s aplikací Sales.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="7f4cd-122">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="7f4cd-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="7f4cd-123">Pole **Číslo účtu** je k dispozici na stránce **Účet**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="7f4cd-124">Slouží jako fyzický a jedinečný klíč k podpoře integrace.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="7f4cd-125">Přirozená klíčová funkce řešení řízení vztahů se zákazníky (CRM) může mít vliv na zákazníky, kteří již používají pole **číslo účtu**, které však nepoužívá jedinečné hodnoty **Číslo účtu** na účet.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="7f4cd-126">V současné době nepodporuje řešení integrace tento případ.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="7f4cd-127">Když je vytvořen nový účet a pokud hodnota **Číslo účtu** ještě neexistuje, je automaticky generováno pomocí číselné řady.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="7f4cd-128">Hodnota se skládá z údaje **ACC** a následně dalšího čísla číselné řady, a pak přípony šest znaků.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="7f4cd-129">Tady je příklad: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="7f4cd-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="7f4cd-130">Při použití řešení integrace prodeje nastaví skript pro upgrade pole **číslo účtu** pole existující účty v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="7f4cd-131">Pokud neexistují žádné hodnoty **Číslo účtu**, použije se číselná řada, která byla uvedena dříve.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="7f4cd-132">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="7f4cd-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="7f4cd-133">**CustomerGroupId** musí být aktualizován na platnou hodnotu v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-133">**CustomerGroupId** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="7f4cd-134">Lze určit výchozí hodnotu nebo můžete nastavit hodnoty pomocí mapování hodnot.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="7f4cd-135">Výchozí hodnota šablony je **10**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-135">The default template value is **10**.</span></span>
- <span data-ttu-id="7f4cd-136">**Kód země/oblasti pro adresu** je v aplikaci Finance and Operations vyžadován.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="7f4cd-137">Abyste zabránili chybám synchronizace, můžete určit výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-137">To avoid synchronization errors, you can specify a default value.</span></span> <span data-ttu-id="7f4cd-138">Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="7f4cd-139">Výchozí hodnota šablony pro **AddressCountryRegionISOCode** je **USA**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="7f4cd-140">Výchozí hodnota šablony pro **DeliveryAddressCountryRegionISOCode** je **USA**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="7f4cd-141">Přidáním následujících mapování z aplikace **CD &gt; Cíl** můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="7f4cd-142">Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="7f4cd-143">**SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="7f4cd-144">Výchozí pracoviště lze získávat z produktu nebo od odběratele ze záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="7f4cd-145">Výchozí hodnota šablony pro **SiteId** je **1**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="7f4cd-146">**WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="7f4cd-147">Výchozí sklad lze získat z produktu nebo od odběratele ze záhlaví objednávky aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="7f4cd-148">Výchozí hodnota šablony pro **WarehouseId** je **13**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="7f4cd-149">**LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="7f4cd-150">Ve výchozím nastavení se používá jazyk ze záhlaví objednávky od odběratele.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="7f4cd-151">Výchozí hodnota šablony pro **LanguageId** je **en-us**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="7f4cd-152">Aktualizujte ID objednávky CDS (**Organization_OrganizationId**) v mapování **Zdroj &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="7f4cd-153">Výchozí hodnota šablony je **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="7f4cd-154">Mapování šablony v integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="7f4cd-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="7f4cd-155">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="7f4cd-156">Pokud chcete tato pole mapovat, nastavte mapování hodnoty.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="7f4cd-157">Mapování hodnot jsou specifická pro data v organizacích, mezi nimiž probíhá synchronizace dané entity.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="7f4cd-158">Na následujícím obrázku je příklad mapování šablony v integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="7f4cd-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Mapování šablony v integrátoru dat](./media/accounts-template-mapping-data-integrator-1.png)

![Mapování šablony pro účty v integrátoru dat](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="7f4cd-161">Související témata</span><span class="sxs-lookup"><span data-stu-id="7f4cd-161">Related topics</span></span>

[<span data-ttu-id="7f4cd-162">Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="7f4cd-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="7f4cd-163">Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7f4cd-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="7f4cd-164">Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7f4cd-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)




