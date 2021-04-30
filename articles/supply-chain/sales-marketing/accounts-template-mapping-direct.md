---
title: Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.
description: Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci obchodních vztahů z Dynamics 365 Sales do Supply Chain Management.
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
ms.openlocfilehash: fff9171966045e9dad5f2c70087a568cfa075e43
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908125"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="501d8-103">Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="501d8-104">Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="501d8-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="501d8-105">Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci obchodních vztahů přímo z Dynamics 365 Sales do Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="501d8-106">Tok dat ve zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="501d8-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="501d8-107">Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="501d8-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="501d8-108">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="501d8-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="501d8-109">Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.</span><span class="sxs-lookup"><span data-stu-id="501d8-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="501d8-110">[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="501d8-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="501d8-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="501d8-111">Templates and tasks</span></span>

<span data-ttu-id="501d8-112">Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="501d8-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="501d8-113">Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="501d8-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="501d8-114">K synchronizaci účtů z aplikace Sales do aplikace Supply Chain Management slouží následující šablony a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="501d8-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="501d8-115">**Název šablony v integraci dat:** Účty (Sales do Fin and Ops) - Přímo</span><span class="sxs-lookup"><span data-stu-id="501d8-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="501d8-116">**Název úkolu v projektu:** Účty – Odběratelé</span><span class="sxs-lookup"><span data-stu-id="501d8-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="501d8-117">Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci účtu/odběratele.</span><span class="sxs-lookup"><span data-stu-id="501d8-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="501d8-118">Sada entit</span><span class="sxs-lookup"><span data-stu-id="501d8-118">Entity set</span></span>

| <span data-ttu-id="501d8-119">Prodej.</span><span class="sxs-lookup"><span data-stu-id="501d8-119">Sales</span></span>    | <span data-ttu-id="501d8-120">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="501d8-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="501d8-121">Účty</span><span class="sxs-lookup"><span data-stu-id="501d8-121">Accounts</span></span> | <span data-ttu-id="501d8-122">Zákazníci V2</span><span class="sxs-lookup"><span data-stu-id="501d8-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="501d8-123">Tok entity</span><span class="sxs-lookup"><span data-stu-id="501d8-123">Entity flow</span></span>

<span data-ttu-id="501d8-124">Účty se spravují v aplikaci Sales a synchronizují se do aplikace Supply Chain Management jako odběratelé.</span><span class="sxs-lookup"><span data-stu-id="501d8-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="501d8-125">Vlastnost **Je externě udržována** těchto odběratelů je nastavena na **Ano** ke sledování odběratelů, kteří pocházejí z aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="501d8-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="501d8-126">Při fakturaci tyto informace slouží k filtrování faktur, které budou synchronizovány s aplikací Sales.</span><span class="sxs-lookup"><span data-stu-id="501d8-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="501d8-127">Řešení Potenciální zákazník pro hotovost v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="501d8-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="501d8-128">Sloupec **Číslo účtu** je dostupný na stránce **Účet**.</span><span class="sxs-lookup"><span data-stu-id="501d8-128">The **Account Number** column is available on the **Account** page.</span></span> <span data-ttu-id="501d8-129">Slouží jako fyzický a jedinečný klíč k podpoře integrace.</span><span class="sxs-lookup"><span data-stu-id="501d8-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="501d8-130">Přirozená klíčová funkce řešení řízení vztahů se zákazníky (CRM) může mít vliv na zákazníky, kteří již používají sloupec **číslo účtu**, které však nepoužívá jedinečné hodnoty **Číslo účtu** na účet.</span><span class="sxs-lookup"><span data-stu-id="501d8-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** column, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="501d8-131">V současné době nepodporuje řešení integrace tento případ.</span><span class="sxs-lookup"><span data-stu-id="501d8-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="501d8-132">Když je vytvořen nový účet a pokud hodnota **Číslo účtu** ještě neexistuje, je automaticky generováno pomocí číselné řady.</span><span class="sxs-lookup"><span data-stu-id="501d8-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="501d8-133">Hodnota se skládá z údaje **ACC** a následně dalšího čísla číselné řady, a pak přípony šest znaků.</span><span class="sxs-lookup"><span data-stu-id="501d8-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="501d8-134">Tady je příklad: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="501d8-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="501d8-135">Při použití řešení integrace prodeje nastaví skript pro upgrade sloupec **číslo účtu** pro existující účty v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="501d8-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** column for existing accounts in Sales.</span></span> <span data-ttu-id="501d8-136">Pokud neexistují žádné hodnoty pro **Číslo účtu**, použije se číselná řada, která byla zmíněna dříve.</span><span class="sxs-lookup"><span data-stu-id="501d8-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="501d8-137">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="501d8-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="501d8-138">Mapování **CustomerGroupId** musí být aktualizováno na platnou hodnotu v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="501d8-139">Lze určit výchozí hodnotu nebo můžete nastavit hodnoty pomocí mapování hodnot.</span><span class="sxs-lookup"><span data-stu-id="501d8-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="501d8-140">Výchozí hodnota šablony je **10**.</span><span class="sxs-lookup"><span data-stu-id="501d8-140">The default template value is **10**.</span></span>

- <span data-ttu-id="501d8-141">Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="501d8-142">Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.</span><span class="sxs-lookup"><span data-stu-id="501d8-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="501d8-143">**SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="501d8-144">Výchozí pracoviště lze získávat z produktu nebo od odběratele ze záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="501d8-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="501d8-145">Výchozí hodnota šablony je **1**.</span><span class="sxs-lookup"><span data-stu-id="501d8-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="501d8-146">**WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="501d8-147">Výchozí sklad lze získat z produktu nebo od odběratele ze záhlaví objednávky aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="501d8-148">Výchozí hodnota šablony je **13**.</span><span class="sxs-lookup"><span data-stu-id="501d8-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="501d8-149">**LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="501d8-150">Ve výchozím nastavení se používá jazyk ze záhlaví objednávky od odběratele.</span><span class="sxs-lookup"><span data-stu-id="501d8-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="501d8-151">Výchozí hodnota šablony je **en-us**.</span><span class="sxs-lookup"><span data-stu-id="501d8-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="501d8-152">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="501d8-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="501d8-153">Sloupce **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **Způsob dopravy** a **Způsob dodání** nejsou zahrnuty do výchozího mapování.</span><span class="sxs-lookup"><span data-stu-id="501d8-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't included in the default mappings.</span></span> <span data-ttu-id="501d8-154">Pokud chcete tyto sloupce mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je tabulka synchronizována.</span><span class="sxs-lookup"><span data-stu-id="501d8-154">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synchronized between.</span></span>

<span data-ttu-id="501d8-155">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="501d8-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="501d8-156">Mapování ukazuje, jaké informace o sloupci budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-156">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

![Mapování šablony v integraci dat](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="501d8-158">Související témata</span><span class="sxs-lookup"><span data-stu-id="501d8-158">Related topics</span></span>


[<span data-ttu-id="501d8-159">Zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="501d8-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="501d8-160">Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="501d8-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="501d8-161">Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="501d8-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="501d8-162">Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="501d8-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="501d8-163">Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="501d8-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]