---
title: Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.
description: Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci obchodních vztahů z Dynamics 365 Sales do Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.openlocfilehash: 8aa03f94e0fb89a6d34ce014dbb6004a1a666327
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529203"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="f0ef6-103">Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="f0ef6-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="f0ef6-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="f0ef6-105">Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci obchodních vztahů přímo z Dynamics 365 Sales do Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="f0ef6-106">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="f0ef6-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="f0ef6-107">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="f0ef6-108">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="f0ef6-109">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="f0ef6-110">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="f0ef6-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f0ef6-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="f0ef6-111">Templates and tasks</span></span>

<span data-ttu-id="f0ef6-112">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="f0ef6-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="f0ef6-113">Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f0ef6-114">K synchronizaci účtů z aplikace Sales do aplikace Supply Chain Management slouží následující šablony a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="f0ef6-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="f0ef6-115">**Název šablony v integraci dat:** Účty (Sales do Fin and Ops) - Přímo</span><span class="sxs-lookup"><span data-stu-id="f0ef6-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="f0ef6-116">**Název úkolu v projektu:** Účty – Odběratelé</span><span class="sxs-lookup"><span data-stu-id="f0ef6-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="f0ef6-117">Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci účtu/odběratele.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f0ef6-118">Sada entit</span><span class="sxs-lookup"><span data-stu-id="f0ef6-118">Entity set</span></span>

| <span data-ttu-id="f0ef6-119">Prodej.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-119">Sales</span></span>    | <span data-ttu-id="f0ef6-120">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="f0ef6-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="f0ef6-121">Účty</span><span class="sxs-lookup"><span data-stu-id="f0ef6-121">Accounts</span></span> | <span data-ttu-id="f0ef6-122">Zákazníci V2</span><span class="sxs-lookup"><span data-stu-id="f0ef6-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="f0ef6-123">Tok entity</span><span class="sxs-lookup"><span data-stu-id="f0ef6-123">Entity flow</span></span>

<span data-ttu-id="f0ef6-124">Účty se spravují v aplikaci Sales a synchronizují se do aplikace Supply Chain Management jako odběratelé.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="f0ef6-125">Vlastnost **Je externě udržována** těchto odběratelů je nastavena na **Ano** ke sledování odběratelů, kteří pocházejí z aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="f0ef6-126">Při fakturaci tyto informace slouží k filtrování faktur, které budou synchronizovány s aplikací Sales.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f0ef6-127">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="f0ef6-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f0ef6-128">Pole **Číslo účtu** je k dispozici na stránce **Účet**.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="f0ef6-129">Slouží jako fyzický a jedinečný klíč k podpoře integrace.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="f0ef6-130">Přirozená klíčová funkce řešení řízení vztahů se zákazníky (CRM) může mít vliv na zákazníky, kteří již používají pole **číslo účtu**, které však nepoužívá jedinečné hodnoty **Číslo účtu** na účet.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="f0ef6-131">V současné době nepodporuje řešení integrace tento případ.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="f0ef6-132">Když je vytvořen nový účet a pokud hodnota **Číslo účtu** ještě neexistuje, je automaticky generováno pomocí číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="f0ef6-133">Hodnota se skládá z údaje **ACC** a následně dalšího čísla číselné řady, a pak přípony šest znaků.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="f0ef6-134">Tady je příklad: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="f0ef6-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="f0ef6-135">Při použití řešení integrace prodeje nastaví skript pro upgrade pole **číslo účtu** pole existující účty v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="f0ef6-136">Pokud neexistují žádné hodnoty pro **Číslo účtu**, použije se číselná řada, která byla zmíněna dříve.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f0ef6-137">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="f0ef6-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="f0ef6-138">Mapování **CustomerGroupId** musí být aktualizováno na platnou hodnotu v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="f0ef6-139">Lze určit výchozí hodnotu nebo můžete nastavit hodnoty pomocí mapování hodnot.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="f0ef6-140">Výchozí hodnota šablony je **10**.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-140">The default template value is **10**.</span></span>

- <span data-ttu-id="f0ef6-141">Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="f0ef6-142">Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="f0ef6-143">**SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="f0ef6-144">Výchozí pracoviště lze získávat z produktu nebo od odběratele ze záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="f0ef6-145">Výchozí hodnota šablony je **1**.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="f0ef6-146">**WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="f0ef6-147">Výchozí sklad lze získat z produktu nebo od odběratele ze záhlaví objednávky aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="f0ef6-148">Výchozí hodnota šablony je **13**.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="f0ef6-149">**LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="f0ef6-150">Ve výchozím nastavení se používá jazyk ze záhlaví objednávky od odběratele.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="f0ef6-151">Výchozí hodnota šablony je **en-us**.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f0ef6-152">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="f0ef6-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="f0ef6-153">Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="f0ef6-154">Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f0ef6-155">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="f0ef6-156">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Mapování šablony v integraci dat](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="f0ef6-158">Související témata</span><span class="sxs-lookup"><span data-stu-id="f0ef6-158">Related topics</span></span>


[<span data-ttu-id="f0ef6-159">Zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="f0ef6-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="f0ef6-160">Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="f0ef6-161">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f0ef6-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="f0ef6-162">Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f0ef6-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="f0ef6-163">Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="f0ef6-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

