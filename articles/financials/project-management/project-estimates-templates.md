---
title: Synchronizace odhadů projektu přímo z Project Service Automation do aplikace Finance and Operations.
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556545"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="7a07f-103">Synchronizace odhadů projektu přímo z Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a07f-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7a07f-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a07f-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="7a07f-105">Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0.</span><span class="sxs-lookup"><span data-stu-id="7a07f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="7a07f-106">Integrace skutečných hodnot je k dispozici v Microsoft Dynamics 365 for Finance and Operations verze 8.0.1 nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="7a07f-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="7a07f-107">Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení.</span><span class="sxs-lookup"><span data-stu-id="7a07f-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="7a07f-108">Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="7a07f-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="7a07f-109">Tok dat pro Project Service Automation a aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a07f-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="7a07f-110">Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a07f-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="7a07f-111">Šablony integrace, které jsou k dispozici s funkcí integrace dat, umožňují tok dat o odhadech projektových hodin a výdajů z aplikace Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a07f-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="7a07f-112">Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a07f-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="7a07f-113">[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="7a07f-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="7a07f-114">Odhady hodin projektů</span><span class="sxs-lookup"><span data-stu-id="7a07f-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7a07f-115">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="7a07f-115">Template and tasks</span></span>

<span data-ttu-id="7a07f-116">Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.</span><span class="sxs-lookup"><span data-stu-id="7a07f-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7a07f-117">K synchronizaci odhadů projektových hodin z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="7a07f-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="7a07f-118">**Název šablony v integraci dat:** Odhady projektových hodin (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7a07f-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7a07f-119">**Název úkolů v projektu:**</span><span class="sxs-lookup"><span data-stu-id="7a07f-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7a07f-120">Vztahy transakce</span><span class="sxs-lookup"><span data-stu-id="7a07f-120">Transaction relationships</span></span>
    - <span data-ttu-id="7a07f-121">Odhady výdajů</span><span class="sxs-lookup"><span data-stu-id="7a07f-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7a07f-122">Sada entit</span><span class="sxs-lookup"><span data-stu-id="7a07f-122">Entity set</span></span>

| <span data-ttu-id="7a07f-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7a07f-123">Project Service Automation</span></span> | <span data-ttu-id="7a07f-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a07f-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7a07f-125">Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="7a07f-125">Project tasks</span></span>              | <span data-ttu-id="7a07f-126">Entita integrace pro odhady hodin projektu</span><span class="sxs-lookup"><span data-stu-id="7a07f-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="7a07f-127">Tok entity</span><span class="sxs-lookup"><span data-stu-id="7a07f-127">Entity flow</span></span>

<span data-ttu-id="7a07f-128">Odhady projektových hodin jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako prognózy projektových hodin.</span><span class="sxs-lookup"><span data-stu-id="7a07f-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7a07f-129">Požadavky</span><span class="sxs-lookup"><span data-stu-id="7a07f-129">Prerequisites</span></span>

<span data-ttu-id="7a07f-130">Než dojde k synchronizaci odhadů projektových hodin, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.</span><span class="sxs-lookup"><span data-stu-id="7a07f-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7a07f-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="7a07f-131">Power Query</span></span>

<span data-ttu-id="7a07f-132">V šabloně odhadů hodin projektu je nutné použít Microsoft Power Query pro Excel za účelem dokončení těchto úkolů:</span><span class="sxs-lookup"><span data-stu-id="7a07f-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="7a07f-133">Nastavení výchozího ID modelu prognózy, které se použije, když integrace vytvoří nové prognózy hodin.</span><span class="sxs-lookup"><span data-stu-id="7a07f-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7a07f-134">Filtrování libovolných záznamů specifických pro zdroj v úkolu, který neumožní integraci do prognóz hodin.</span><span class="sxs-lookup"><span data-stu-id="7a07f-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="7a07f-135">Filtrování prázdných řádků kategorie transakce.</span><span class="sxs-lookup"><span data-stu-id="7a07f-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="7a07f-136">Když nedokončíte tento úkol, může to způsobit chybné hodinové prognózy.</span><span class="sxs-lookup"><span data-stu-id="7a07f-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7a07f-137">Nastavení výchozího ID modelu prognózy</span><span class="sxs-lookup"><span data-stu-id="7a07f-137">Set the default forecast model ID</span></span>

<span data-ttu-id="7a07f-138">Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, klikněte na šipku **Mapa** a otevřete mapování.</span><span class="sxs-lookup"><span data-stu-id="7a07f-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7a07f-139">Poté zvolte odkaz na **Filtrování a rozšířený dotaz**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7a07f-140">Pokud použijete výchozí šablonu odhadu hodin Microsoft Project (PSA do Fin and Ops), vyberte **Vložená podmínka** v seznamu **Použité kroky**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="7a07f-141">V zadání **Funkce** nahraďte **O\_forecast** názvem ID modelu prognózy, které má být použito s integrací.</span><span class="sxs-lookup"><span data-stu-id="7a07f-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7a07f-142">Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="7a07f-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7a07f-143">Při vytváření nové šablony je nutné přidat tento sloupec.</span><span class="sxs-lookup"><span data-stu-id="7a07f-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7a07f-144">V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7a07f-145">Zadejte podmínku pro sloupec, kde pokud úloha projektu není null, pak \<enter the forecast model ID\> má jinou hodnotu než null.</span><span class="sxs-lookup"><span data-stu-id="7a07f-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="7a07f-146">Filtrování záznamů specifických pro zdroj</span><span class="sxs-lookup"><span data-stu-id="7a07f-146">Filter out resource-specific records</span></span>

<span data-ttu-id="7a07f-147">Šablona odhadu hodin projektu odhadů (PSA do Fin and Ops) má výchozí filtr, který odstraní všechny záznamy specifické pro zdroj.</span><span class="sxs-lookup"><span data-stu-id="7a07f-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="7a07f-148">Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="7a07f-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7a07f-149">Zvolte odkaz **Filtrování a rozšířený dotaz** pro filtrování na sloupci **msdyn\_islinetask**, aby byly zahrnuty pouze záznamy **False**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="7a07f-150">Filtrování prázdných řádků kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="7a07f-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="7a07f-151">Je nutné přidat filtr k odstranění všech řádků s prázdnými kategoriemi transakce.</span><span class="sxs-lookup"><span data-stu-id="7a07f-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="7a07f-152">Tento úkol je povinný, bez ohledu na to, jestli používáte výchozí šablonu nebo vytváříte vlastní šablonu.</span><span class="sxs-lookup"><span data-stu-id="7a07f-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="7a07f-153">Tento filtr odebere všechny souhrnné řádky pocházející z Project Service Automation, které by mohly způsobit, že prognózy hodin v Finance and Operations budou nesprávné.</span><span class="sxs-lookup"><span data-stu-id="7a07f-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="7a07f-154">Zvolte odkaz **Filtrování a rozšířený dotaz** pro odfiltrování nulových záznamů ve sloupci **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7a07f-155">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="7a07f-155">Template mapping in Data integration</span></span>

<span data-ttu-id="7a07f-156">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="7a07f-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="7a07f-157">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a07f-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="7a07f-158">[![Mapování šablony](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7a07f-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="7a07f-159">Odhady výdajů projektu</span><span class="sxs-lookup"><span data-stu-id="7a07f-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7a07f-160">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="7a07f-160">Template and tasks</span></span>

<span data-ttu-id="7a07f-161">K synchronizaci odhadů projektových výdajů z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="7a07f-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="7a07f-162">**Název šablony v integraci dat:** Odhady projektových výdajů (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7a07f-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7a07f-163">**Název úkolů v projektu:**</span><span class="sxs-lookup"><span data-stu-id="7a07f-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7a07f-164">Vztahy transakce</span><span class="sxs-lookup"><span data-stu-id="7a07f-164">Transaction relationships</span></span> 
    - <span data-ttu-id="7a07f-165">Odhady výdajů</span><span class="sxs-lookup"><span data-stu-id="7a07f-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7a07f-166">Sada entit</span><span class="sxs-lookup"><span data-stu-id="7a07f-166">Entity set</span></span>

| <span data-ttu-id="7a07f-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7a07f-167">Project Service Automation</span></span> | <span data-ttu-id="7a07f-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a07f-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="7a07f-169">Připojení transakce</span><span class="sxs-lookup"><span data-stu-id="7a07f-169">Transaction Connections</span></span>    | <span data-ttu-id="7a07f-170">Entita integrace pro vztahy transakce projektu</span><span class="sxs-lookup"><span data-stu-id="7a07f-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="7a07f-171">Řádky odhadu</span><span class="sxs-lookup"><span data-stu-id="7a07f-171">Estimate Lines</span></span>             | <span data-ttu-id="7a07f-172">Entita integrace pro odhady nákladu projektu</span><span class="sxs-lookup"><span data-stu-id="7a07f-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="7a07f-173">Tok entity</span><span class="sxs-lookup"><span data-stu-id="7a07f-173">Entity flow</span></span>

<span data-ttu-id="7a07f-174">Odhady projektových výdajů jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako prognózy projektových výdajů.</span><span class="sxs-lookup"><span data-stu-id="7a07f-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7a07f-175">Požadavky</span><span class="sxs-lookup"><span data-stu-id="7a07f-175">Prerequisites</span></span>

<span data-ttu-id="7a07f-176">Než dojde k synchronizaci odhadů projektových výdajů, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.</span><span class="sxs-lookup"><span data-stu-id="7a07f-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7a07f-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="7a07f-177">Power Query</span></span>

<span data-ttu-id="7a07f-178">Je nutné použít Power Query v šabloně odhadů výdajů projektu pro dokončení následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="7a07f-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="7a07f-179">Filtrování, aby byly zahrnuty pouze záznamy řádku odhadu výdajů.</span><span class="sxs-lookup"><span data-stu-id="7a07f-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="7a07f-180">Nastavení výchozího ID modelu prognózy, které se použije, když integrace vytvoří nové prognózy hodin.</span><span class="sxs-lookup"><span data-stu-id="7a07f-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7a07f-181">Převod typu účtování.</span><span class="sxs-lookup"><span data-stu-id="7a07f-181">Transform the billing types.</span></span>
- <span data-ttu-id="7a07f-182">Převod typů transakcí.</span><span class="sxs-lookup"><span data-stu-id="7a07f-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="7a07f-183">Filtrování, aby byly zahrnuty pouze řádky odhadu výdajů</span><span class="sxs-lookup"><span data-stu-id="7a07f-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="7a07f-184">Šablona odhadů výdajů projektu (PSA do Fin and Ops) má výchozí filtr, který zahrnuje pouze řádky výdajů v integraci.</span><span class="sxs-lookup"><span data-stu-id="7a07f-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="7a07f-185">Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="7a07f-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7a07f-186">Vyberte úlohu **Vztah transakcí** a klikněte na šipku **Mapa** pro otevření mapování.</span><span class="sxs-lookup"><span data-stu-id="7a07f-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7a07f-187">Zvolte odkaz na **Filtrování a rozšířený dotaz**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="7a07f-188">Vyfiltrujte sloupec **msdyn\_transactiontype1**, aby obsahoval pouze **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7a07f-189">Nastavení výchozího ID modelu prognózy</span><span class="sxs-lookup"><span data-stu-id="7a07f-189">Set the default forecast model ID</span></span>

<span data-ttu-id="7a07f-190">Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, pro úlohu **Odhady výdajů** a poté klikněte na šipku **Mapa** a otevřete mapování.</span><span class="sxs-lookup"><span data-stu-id="7a07f-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7a07f-191">Zvolte odkaz na **Filtrování a rozšířený dotaz**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7a07f-192">Pokud použijete výchozí šablonu odhadu výdajů projektu (PSA do Fin and Ops), vyberte nejdříve v Power Query možnost **Vložená podmínka** v části **Použité kroky**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="7a07f-193">V zadání **Funkce** nahraďte **O\_forecast** názvem ID modelu prognózy, které má být použito s integrací.</span><span class="sxs-lookup"><span data-stu-id="7a07f-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7a07f-194">Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="7a07f-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7a07f-195">Při vytváření nové šablony je nutné přidat tento sloupec.</span><span class="sxs-lookup"><span data-stu-id="7a07f-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7a07f-196">V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7a07f-197">Zadejte podmínku pro sloupec, kde pokud ID řádku odhadu není null, pak \<enter the forecast model ID\>; jinou hodnotu než null.</span><span class="sxs-lookup"><span data-stu-id="7a07f-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="7a07f-198">Převod typu účtování</span><span class="sxs-lookup"><span data-stu-id="7a07f-198">Transform the billing types</span></span>

<span data-ttu-id="7a07f-199">Šablona odhadů výdajů projektu (PSA do Fin and Ops) obsahuje podmíněný sloupec použitý k převodu typů účtování přijatých z Project Service Automation během integrace</span><span class="sxs-lookup"><span data-stu-id="7a07f-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7a07f-200">Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec.</span><span class="sxs-lookup"><span data-stu-id="7a07f-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7a07f-201">Zvolte odkaz **Filtrování a rozšířený dotaz** a pak vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7a07f-202">Zadejte název pro nový sloupec, jako je například **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="7a07f-203">Poté zadejte následující podmínku:</span><span class="sxs-lookup"><span data-stu-id="7a07f-203">Then enter the following condition:</span></span>

<span data-ttu-id="7a07f-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="7a07f-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="7a07f-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="7a07f-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="7a07f-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="7a07f-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="7a07f-207">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="7a07f-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="7a07f-208">Převod typů transakcí</span><span class="sxs-lookup"><span data-stu-id="7a07f-208">Transform the transaction types</span></span>

<span data-ttu-id="7a07f-209">Šablona odhadů výdajů projektu (PSA do Fin and Ops) obsahuje podmíněný sloupec použitý k převodu typů transakcí přijatých z Project Service Automation během integrace</span><span class="sxs-lookup"><span data-stu-id="7a07f-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7a07f-210">Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec.</span><span class="sxs-lookup"><span data-stu-id="7a07f-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7a07f-211">Zvolte odkaz **Filtrování a rozšířený dotaz** a pak vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7a07f-212">Zadejte název pro nový sloupec, jako je například **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="7a07f-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="7a07f-213">Poté zadejte následující podmínku:</span><span class="sxs-lookup"><span data-stu-id="7a07f-213">Then enter the following condition:</span></span>

<span data-ttu-id="7a07f-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="7a07f-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="7a07f-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="7a07f-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="7a07f-216">else **null**</span><span class="sxs-lookup"><span data-stu-id="7a07f-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7a07f-217">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="7a07f-217">Template mapping in Data integration</span></span>

<span data-ttu-id="7a07f-218">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="7a07f-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="7a07f-219">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a07f-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="7a07f-220">[![Mapování šablony](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7a07f-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="7a07f-221">[![Mapování šablony](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7a07f-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
