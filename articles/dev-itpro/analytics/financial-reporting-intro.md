---
title: Finanční výkaznictví
description: Finanční výkaznictví v aplikaci Finance and Operations je nástroj, pomocí kterého mohou pracovníci v oblasti financí a obchodu vytvářet, spravovat, nasazovat a kontrolovat finanční výkazy. Obchází omezení tradičních sestav a pomáhá efektivně navrhnout různé typy sestav.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ae2087cf142fc2670bda3c542b336f12978178a6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "323771"
---
# <a name="financial-reporting"></a><span data-ttu-id="f12aa-104">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f12aa-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f12aa-105">Finanční výkaznictví v aplikaci Finance and Operations je nástroj, pomocí kterého mohou pracovníci v oblasti financí a obchodu vytvářet, spravovat, nasazovat a kontrolovat finanční výkazy.</span><span class="sxs-lookup"><span data-stu-id="f12aa-105">Financial reporting for Finance and Operations allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="f12aa-106">Obchází omezení tradičních sestav a pomáhá efektivně navrhnout různé typy sestav.</span><span class="sxs-lookup"><span data-stu-id="f12aa-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="f12aa-107">Finanční výkaznictví zahrnuje podporu dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f12aa-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="f12aa-108">Proto jsou segmenty účtu nebo dimenze okamžitě k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f12aa-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="f12aa-109">Žádné další nástroje nebo konfigurační kroky nejsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="f12aa-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="f12aa-110">Nastavení finančního výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f12aa-110">Financial reporting setup</span></span>
<span data-ttu-id="f12aa-111">Stránka **Nastavení finančního výkaznictví** obsahuje seznam všech finančních dimenzí v systému.</span><span class="sxs-lookup"><span data-stu-id="f12aa-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="f12aa-112">**Hlavní kniha** \> **Nastavení hlavní knihy** \> **Nastavení finančního výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f12aa-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="f12aa-113">Stránka **Nastavení finančního výkaznictví** má dvě části, které určují data vykazovaná ve finančním výkaznictví:</span><span class="sxs-lookup"><span data-stu-id="f12aa-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="f12aa-114">**Karta Dimenze** – Vzhledem k tomu, že různé společnosti používají různé dimenze a účetní struktury, nelze určit pořadí, ve kterém uživatelé potřebují zobrazit všechny finanční dimenze v sestavách.</span><span class="sxs-lookup"><span data-stu-id="f12aa-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="f12aa-115">Tato stránka vám umožní nastavit pořadí, ve kterém si přejete zobrazovat finanční dimenze při tvorbě a zobrazení sestavy ve finančním výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f12aa-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="f12aa-116">**Karta Atributy** je místem, kde můžete zvolit, zda chcete použít možnosti **Dodavatelé** a **Odběratelé** jako atributy pro účely filtrování a návrhu sestav.</span><span class="sxs-lookup"><span data-stu-id="f12aa-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="f12aa-117">Vykazování na úrovni dodavatele a odběratele bude užitečné pouze tehdy, pokud nezadáte do jednoho dokladu při zaúčtování transakcí více dodavatelů a odběratelů.</span><span class="sxs-lookup"><span data-stu-id="f12aa-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="f12aa-118">Výběr dodavatele anebo odběratele přidá další čas pro integraci.</span><span class="sxs-lookup"><span data-stu-id="f12aa-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="f12aa-119">Součásti finančního výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f12aa-119">Financial reporting components</span></span>
<span data-ttu-id="f12aa-120">Následující součásti finančního výkaznictví umožňují snadné vytváření, zobrazování a plánování sestav.</span><span class="sxs-lookup"><span data-stu-id="f12aa-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="f12aa-121">Součást</span><span class="sxs-lookup"><span data-stu-id="f12aa-121">Component</span></span>        | <span data-ttu-id="f12aa-122">Funkce</span><span class="sxs-lookup"><span data-stu-id="f12aa-122">Functions</span></span> | <span data-ttu-id="f12aa-123">Doplňkové informace</span><span class="sxs-lookup"><span data-stu-id="f12aa-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="f12aa-124">Návrhář sestav</span><span class="sxs-lookup"><span data-stu-id="f12aa-124">Report Designer</span></span>  | <span data-ttu-id="f12aa-125">Vytváření stavebních bloků sestav, které v kombinaci definují a generují sestavy.</span><span class="sxs-lookup"><span data-stu-id="f12aa-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="f12aa-126">Průvodce sestavou provádí méně zkušené uživatele procesem návrhu.</span><span class="sxs-lookup"><span data-stu-id="f12aa-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="f12aa-127">Pokročilí uživatelé mohou vytvořit nové stavební bloky sestav nebo upravit existující stavební bloky podle svých potřeb.</span><span class="sxs-lookup"><span data-stu-id="f12aa-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="f12aa-128">Plánování sestav</span><span class="sxs-lookup"><span data-stu-id="f12aa-128">Report schedules</span></span> | <span data-ttu-id="f12aa-129">Naplánujte jednu sestavu nebo skupinu sestav tak, aby se generovala v pravidelných intervalech.</span><span class="sxs-lookup"><span data-stu-id="f12aa-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="f12aa-130">Generování finanční sestavy</span><span class="sxs-lookup"><span data-stu-id="f12aa-130">Generate a financial report</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="f12aa-131">Funkce</span><span class="sxs-lookup"><span data-stu-id="f12aa-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="f12aa-132">Funkce</span><span class="sxs-lookup"><span data-stu-id="f12aa-132">Feature</span></span></th>
<th><span data-ttu-id="f12aa-133">popis</span><span class="sxs-lookup"><span data-stu-id="f12aa-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f12aa-134">Flexibilita navrhování sestav</span><span class="sxs-lookup"><span data-stu-id="f12aa-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="f12aa-135">Návrhář sestav zahrnuje následující možnosti vykazování při navrhování sestavy:</span><span class="sxs-lookup"><span data-stu-id="f12aa-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="f12aa-136">ukládat kombinace dimenzí a znovu používat dimenze pro více sestav;</span><span class="sxs-lookup"><span data-stu-id="f12aa-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="f12aa-137">řídit způsob formátování a zobrazování popisů dimenzí;</span><span class="sxs-lookup"><span data-stu-id="f12aa-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="f12aa-138">Rozpoznejte účty nebo dimenzí, které byly vynechány ve stavebních blocích sestavy.</span><span class="sxs-lookup"><span data-stu-id="f12aa-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="f12aa-139">Formátování záhlaví pro klouzavé prognózy.</span><span class="sxs-lookup"><span data-stu-id="f12aa-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="f12aa-140">Spolupráce při vytváření finančních sestav</span><span class="sxs-lookup"><span data-stu-id="f12aa-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="f12aa-141">Následující funkce pomáhají spravovat generování a distribuci sestav:</span><span class="sxs-lookup"><span data-stu-id="f12aa-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="f12aa-142">plánování automatického generování sestav s denní, týdenní, měsíční nebo roční pravidelností;</span><span class="sxs-lookup"><span data-stu-id="f12aa-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="f12aa-143">export do formátu jen pro čtení XPS, který poskytuje lepší zabezpečení dokumentů s digitálními podpisy;</span><span class="sxs-lookup"><span data-stu-id="f12aa-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="f12aa-144">Export do listu aplikace Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f12aa-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="f12aa-145">pokud chcete sdílet sestavy, můžete vytvářet e-mailové zprávy, které obsahují odkazy na sestavy.</span><span class="sxs-lookup"><span data-stu-id="f12aa-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="f12aa-146">Prohlížení interaktivních sestav</span><span class="sxs-lookup"><span data-stu-id="f12aa-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="f12aa-147">Interaktivní funkce umožňují provádět následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="f12aa-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="f12aa-148">Změna data sestavy pro sestavu, kterou prohlížíte.</span><span class="sxs-lookup"><span data-stu-id="f12aa-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="f12aa-149">Změna měny sestavy, kterou prohlížíte.</span><span class="sxs-lookup"><span data-stu-id="f12aa-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="f12aa-150">Zobrazení sestavy v souhrnném zobrazení nebo podrobném zobrazení.</span><span class="sxs-lookup"><span data-stu-id="f12aa-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="f12aa-151">Přidání filtrů dimenze pro omezení obsahu sestavy na specifickou dimenzi nebo kombinaci dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f12aa-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="f12aa-152">Přidání filtrů atributu pro omezení obsahu sestavy na specifický atribut nebo kombinaci atributů.</span><span class="sxs-lookup"><span data-stu-id="f12aa-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="f12aa-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f12aa-153">Additional resources</span></span>
[<span data-ttu-id="f12aa-154">Generování finanční sestavy</span><span class="sxs-lookup"><span data-stu-id="f12aa-154">Generate a financial report</span></span>](generate-financial-report.md)
