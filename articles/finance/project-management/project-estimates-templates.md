---
title: Synchronizace odhadů projektu přímo z Project Service Automation do aplikace Finance and Operations.
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770282"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f38b9-103">Synchronizace odhadů projektu přímo z Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f38b9-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f38b9-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f38b9-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="f38b9-105">Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici ve verzi 8.0.</span><span class="sxs-lookup"><span data-stu-id="f38b9-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="f38b9-106">Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="f38b9-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="f38b9-107">Tok dat pro Project Service Automation a aplikaci Finance</span><span class="sxs-lookup"><span data-stu-id="f38b9-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="f38b9-108">Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="f38b9-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="f38b9-109">Šablony integrace, které jsou k dispozici s funkcí integrace dat, umožňují tok dat o odhadech projektových hodin a výdajů z aplikace Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="f38b9-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f38b9-110">Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="f38b9-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="f38b9-111">[![Tok dat pro integraci Project Service Automation s aplikací Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f38b9-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="f38b9-112">Odhady hodin projektů</span><span class="sxs-lookup"><span data-stu-id="f38b9-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="f38b9-113">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="f38b9-113">Template and tasks</span></span>

<span data-ttu-id="f38b9-114">Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft Power Apps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.</span><span class="sxs-lookup"><span data-stu-id="f38b9-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f38b9-115">K synchronizaci odhadů projektových hodin z aplikace Project Service Automation do aplikace Finance slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="f38b9-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f38b9-116">**Název šablony v integraci dat:** Odhady projektových hodin (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f38b9-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f38b9-117">**Název úkolů v projektu:**</span><span class="sxs-lookup"><span data-stu-id="f38b9-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="f38b9-118">Vztahy transakce</span><span class="sxs-lookup"><span data-stu-id="f38b9-118">Transaction relationships</span></span>
    - <span data-ttu-id="f38b9-119">Odhady výdajů</span><span class="sxs-lookup"><span data-stu-id="f38b9-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="f38b9-120">Sada entit</span><span class="sxs-lookup"><span data-stu-id="f38b9-120">Entity set</span></span>

| <span data-ttu-id="f38b9-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f38b9-121">Project Service Automation</span></span> | <span data-ttu-id="f38b9-122">Finance</span><span class="sxs-lookup"><span data-stu-id="f38b9-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f38b9-123">Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="f38b9-123">Project tasks</span></span>              | <span data-ttu-id="f38b9-124">Entita integrace pro odhady hodin projektu</span><span class="sxs-lookup"><span data-stu-id="f38b9-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="f38b9-125">Tok entity</span><span class="sxs-lookup"><span data-stu-id="f38b9-125">Entity flow</span></span>

<span data-ttu-id="f38b9-126">Odhady projektových hodin jsou spravovány v Project Service Automation a jsou synchronizovány do Finance jako prognózy projektových hodin.</span><span class="sxs-lookup"><span data-stu-id="f38b9-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f38b9-127">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="f38b9-127">Prerequisites</span></span>

<span data-ttu-id="f38b9-128">Než dojde k synchronizaci odhadů projektových hodin, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.</span><span class="sxs-lookup"><span data-stu-id="f38b9-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f38b9-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="f38b9-129">Power Query</span></span>

<span data-ttu-id="f38b9-130">V šabloně odhadů hodin projektu je nutné použít Microsoft Power Query pro Excel za účelem dokončení těchto úkolů:</span><span class="sxs-lookup"><span data-stu-id="f38b9-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="f38b9-131">Nastavení výchozího ID modelu prognózy, které se použije, když integrace vytvoří nové prognózy hodin.</span><span class="sxs-lookup"><span data-stu-id="f38b9-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="f38b9-132">Filtrování libovolných záznamů specifických pro zdroj v úkolu, který neumožní integraci do prognóz hodin.</span><span class="sxs-lookup"><span data-stu-id="f38b9-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="f38b9-133">Filtrování prázdných řádků kategorie transakce.</span><span class="sxs-lookup"><span data-stu-id="f38b9-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="f38b9-134">Když nedokončíte tento úkol, může to způsobit chybné hodinové prognózy.</span><span class="sxs-lookup"><span data-stu-id="f38b9-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="f38b9-135">Nastavení výchozího ID modelu prognózy</span><span class="sxs-lookup"><span data-stu-id="f38b9-135">Set the default forecast model ID</span></span>

<span data-ttu-id="f38b9-136">Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, klikněte na šipku **Mapa** a otevřete mapování.</span><span class="sxs-lookup"><span data-stu-id="f38b9-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f38b9-137">Poté zvolte odkaz na **Filtrování a rozšířený dotaz**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="f38b9-138">Pokud použijete výchozí šablonu odhadu hodin Microsoft Project (PSA do Fin and Ops), vyberte **Vložená podmínka** v seznamu **Použité kroky**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="f38b9-139">V zadání **Funkce** nahraďte **O\_forecast** názvem ID modelu prognózy, které má být použito s integrací.</span><span class="sxs-lookup"><span data-stu-id="f38b9-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="f38b9-140">Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="f38b9-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="f38b9-141">Při vytváření nové šablony je nutné přidat tento sloupec.</span><span class="sxs-lookup"><span data-stu-id="f38b9-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="f38b9-142">V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="f38b9-143">Zadejte podmínku pro sloupec, kde pokud úloha projektu není null, pak \<enter the forecast model ID\> má jinou hodnotu než null.</span><span class="sxs-lookup"><span data-stu-id="f38b9-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="f38b9-144">Filtrování záznamů specifických pro zdroj</span><span class="sxs-lookup"><span data-stu-id="f38b9-144">Filter out resource-specific records</span></span>

<span data-ttu-id="f38b9-145">Šablona odhadu hodin projektu odhadů (PSA do Fin and Ops) má výchozí filtr, který odstraní všechny záznamy specifické pro zdroj.</span><span class="sxs-lookup"><span data-stu-id="f38b9-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="f38b9-146">Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="f38b9-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="f38b9-147">Zvolte odkaz **Filtrování a rozšířený dotaz** pro filtrování na sloupci **msdyn\_islinetask**, aby byly zahrnuty pouze záznamy **False**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="f38b9-148">Filtrování prázdných řádků kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="f38b9-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="f38b9-149">Je nutné přidat filtr k odstranění všech řádků s prázdnými kategoriemi transakce.</span><span class="sxs-lookup"><span data-stu-id="f38b9-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="f38b9-150">Tento úkol je povinný, bez ohledu na to, jestli používáte výchozí šablonu nebo vytváříte vlastní šablonu.</span><span class="sxs-lookup"><span data-stu-id="f38b9-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="f38b9-151">Tento filtr odebere všechny souhrnné řádky pocházející z Project Service Automation, které by mohly způsobit, že prognózy hodin v Finance budou nesprávné.</span><span class="sxs-lookup"><span data-stu-id="f38b9-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="f38b9-152">Zvolte odkaz **Filtrování a rozšířený dotaz** pro odfiltrování nulových záznamů ve sloupci **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f38b9-153">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="f38b9-153">Template mapping in Data integration</span></span>

<span data-ttu-id="f38b9-154">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="f38b9-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="f38b9-155">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="f38b9-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f38b9-156">[![Mapování šablony](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f38b9-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="f38b9-157">Odhady výdajů projektu</span><span class="sxs-lookup"><span data-stu-id="f38b9-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="f38b9-158">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="f38b9-158">Template and tasks</span></span>

<span data-ttu-id="f38b9-159">K synchronizaci odhadů projektových výdajů z aplikace Project Service Automation do aplikace Finance slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="f38b9-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f38b9-160">**Název šablony v integraci dat:** Odhady projektových výdajů (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f38b9-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f38b9-161">**Název úkolů v projektu:**</span><span class="sxs-lookup"><span data-stu-id="f38b9-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="f38b9-162">Vztahy transakce</span><span class="sxs-lookup"><span data-stu-id="f38b9-162">Transaction relationships</span></span> 
    - <span data-ttu-id="f38b9-163">Odhady výdajů</span><span class="sxs-lookup"><span data-stu-id="f38b9-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="f38b9-164">Sada entit</span><span class="sxs-lookup"><span data-stu-id="f38b9-164">Entity set</span></span>

| <span data-ttu-id="f38b9-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f38b9-165">Project Service Automation</span></span> | <span data-ttu-id="f38b9-166">Finance</span><span class="sxs-lookup"><span data-stu-id="f38b9-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="f38b9-167">Připojení transakce</span><span class="sxs-lookup"><span data-stu-id="f38b9-167">Transaction Connections</span></span>    | <span data-ttu-id="f38b9-168">Entita integrace pro vztahy transakce projektu</span><span class="sxs-lookup"><span data-stu-id="f38b9-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="f38b9-169">Řádky odhadu</span><span class="sxs-lookup"><span data-stu-id="f38b9-169">Estimate Lines</span></span>             | <span data-ttu-id="f38b9-170">Entita integrace pro odhady nákladu projektu</span><span class="sxs-lookup"><span data-stu-id="f38b9-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="f38b9-171">Tok entity</span><span class="sxs-lookup"><span data-stu-id="f38b9-171">Entity flow</span></span>

<span data-ttu-id="f38b9-172">Odhady projektových výdajů jsou spravovány v Project Service Automation a jsou synchronizovány do Finance jako prognózy projektových výdajů.</span><span class="sxs-lookup"><span data-stu-id="f38b9-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f38b9-173">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="f38b9-173">Prerequisites</span></span>

<span data-ttu-id="f38b9-174">Než dojde k synchronizaci odhadů projektových výdajů, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.</span><span class="sxs-lookup"><span data-stu-id="f38b9-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f38b9-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="f38b9-175">Power Query</span></span>

<span data-ttu-id="f38b9-176">Je nutné použít Power Query v šabloně odhadů výdajů projektu pro dokončení následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="f38b9-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="f38b9-177">Filtrování, aby byly zahrnuty pouze záznamy řádku odhadu výdajů.</span><span class="sxs-lookup"><span data-stu-id="f38b9-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="f38b9-178">Nastavení výchozího ID modelu prognózy, které se použije, když integrace vytvoří nové prognózy hodin.</span><span class="sxs-lookup"><span data-stu-id="f38b9-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="f38b9-179">Převod typu účtování.</span><span class="sxs-lookup"><span data-stu-id="f38b9-179">Transform the billing types.</span></span>
- <span data-ttu-id="f38b9-180">Převod typů transakcí.</span><span class="sxs-lookup"><span data-stu-id="f38b9-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="f38b9-181">Filtrování, aby byly zahrnuty pouze řádky odhadu výdajů</span><span class="sxs-lookup"><span data-stu-id="f38b9-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="f38b9-182">Šablona odhadů výdajů projektu (PSA do Fin and Ops) má výchozí filtr, který zahrnuje pouze řádky výdajů v integraci.</span><span class="sxs-lookup"><span data-stu-id="f38b9-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="f38b9-183">Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="f38b9-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="f38b9-184">Vyberte úlohu **Vztah transakcí** a klikněte na šipku **Mapa** pro otevření mapování.</span><span class="sxs-lookup"><span data-stu-id="f38b9-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f38b9-185">Zvolte odkaz na **Filtrování a rozšířený dotaz**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="f38b9-186">Vyfiltrujte sloupec **msdyn\_transactiontype1**, aby obsahoval pouze **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="f38b9-187">Nastavení výchozího ID modelu prognózy</span><span class="sxs-lookup"><span data-stu-id="f38b9-187">Set the default forecast model ID</span></span>

<span data-ttu-id="f38b9-188">Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, pro úlohu **Odhady výdajů** a poté klikněte na šipku **Mapa** a otevřete mapování.</span><span class="sxs-lookup"><span data-stu-id="f38b9-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f38b9-189">Zvolte odkaz na **Filtrování a rozšířený dotaz**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="f38b9-190">Pokud použijete výchozí šablonu odhadu výdajů projektu (PSA do Fin and Ops), vyberte nejdříve v Power Query možnost **Vložená podmínka** v části **Použité kroky**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="f38b9-191">V zadání **Funkce** nahraďte **O\_forecast** názvem ID modelu prognózy, které má být použito s integrací.</span><span class="sxs-lookup"><span data-stu-id="f38b9-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="f38b9-192">Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="f38b9-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="f38b9-193">Při vytváření nové šablony je nutné přidat tento sloupec.</span><span class="sxs-lookup"><span data-stu-id="f38b9-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="f38b9-194">V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="f38b9-195">Zadejte podmínku pro sloupec, kde pokud ID řádku odhadu není null, pak \<enter the forecast model ID\>; jinou hodnotu než null.</span><span class="sxs-lookup"><span data-stu-id="f38b9-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="f38b9-196">Převod typu účtování</span><span class="sxs-lookup"><span data-stu-id="f38b9-196">Transform the billing types</span></span>

<span data-ttu-id="f38b9-197">Šablona odhadů výdajů projektu (PSA do Fin and Ops) obsahuje podmíněný sloupec použitý k převodu typů účtování přijatých z Project Service Automation během integrace</span><span class="sxs-lookup"><span data-stu-id="f38b9-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="f38b9-198">Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec.</span><span class="sxs-lookup"><span data-stu-id="f38b9-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="f38b9-199">Zvolte odkaz **Filtrování a rozšířený dotaz** a pak vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="f38b9-200">Zadejte název pro nový sloupec, jako je například **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="f38b9-201">Poté zadejte následující podmínku:</span><span class="sxs-lookup"><span data-stu-id="f38b9-201">Then enter the following condition:</span></span>

<span data-ttu-id="f38b9-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="f38b9-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="f38b9-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="f38b9-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="f38b9-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="f38b9-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="f38b9-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="f38b9-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="f38b9-206">Převod typů transakcí</span><span class="sxs-lookup"><span data-stu-id="f38b9-206">Transform the transaction types</span></span>

<span data-ttu-id="f38b9-207">Šablona odhadů výdajů projektu (PSA do Fin and Ops) obsahuje podmíněný sloupec použitý k převodu typů transakcí přijatých z Project Service Automation během integrace</span><span class="sxs-lookup"><span data-stu-id="f38b9-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="f38b9-208">Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec.</span><span class="sxs-lookup"><span data-stu-id="f38b9-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="f38b9-209">Zvolte odkaz **Filtrování a rozšířený dotaz** a pak vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="f38b9-210">Zadejte název pro nový sloupec, jako je například **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="f38b9-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="f38b9-211">Poté zadejte následující podmínku:</span><span class="sxs-lookup"><span data-stu-id="f38b9-211">Then enter the following condition:</span></span>

<span data-ttu-id="f38b9-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="f38b9-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="f38b9-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="f38b9-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="f38b9-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="f38b9-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f38b9-215">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="f38b9-215">Template mapping in Data integration</span></span>

<span data-ttu-id="f38b9-216">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="f38b9-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="f38b9-217">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="f38b9-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f38b9-218">[![Mapování šablony](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f38b9-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="f38b9-219">[![Mapování šablony](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f38b9-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
