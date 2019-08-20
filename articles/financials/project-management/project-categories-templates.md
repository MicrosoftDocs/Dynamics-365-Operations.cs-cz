---
title: Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838360"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="adf76-103">Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="adf76-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="adf76-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="adf76-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="adf76-105">Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0.</span><span class="sxs-lookup"><span data-stu-id="adf76-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="adf76-106">Integrace skutečných hodnot je k dispozici v Microsoft Dynamics 365 for Finance and Operations verze 8.0.1 nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="adf76-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="adf76-107">Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení.</span><span class="sxs-lookup"><span data-stu-id="adf76-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="adf76-108">Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="adf76-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="adf76-109">Tok dat pro Project Service Automation a aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adf76-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="adf76-110">Řešení integrace Project Service Automation a Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="adf76-111">Šablony integrace, která jsou k dispozici s funkcí integrace dat, umožňují tok dat o kategoriích transakcí projektových výdajů mezi aplikacemi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="adf76-112">Pokud jsou kategorie výdajů projektu řízeny v Finance and Operations, tok integrace je nejdříve z Finance and Operations do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="adf76-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="adf76-113">ID integrace kategorií výdajů projektu se poté aktualizují pomocí synchronizace z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="adf76-114">Pokud jsou kategorie výdajů projektu řízeny v Project Service Automation, tok integrace je nejdříve z Prroject Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="adf76-115">Kategorie projektu musí být již nakonfigurována v aplikaci Finance and Operations před synchronizací z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="adf76-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="adf76-116">Poté se synchronizuje z Finance and Operations zpět do Project Service Automation a poté znovu z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="adf76-117">Tímto způsobem pomůžete zajistit, aby byly kategorie propojeny a aby nebyly vytvořeny žádné duplicity.</span><span class="sxs-lookup"><span data-stu-id="adf76-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="adf76-118">Obvykle jsou kategorie výdajů projektu řízeny v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="adf76-119">Pokud však nejsou v aplikaci Finance and Operations řízeny nebo pokud byly v aplikaci Project Service Automation vytvořeny kategorie výdajů, musíte nejprve synchronizovat pomocí šablony kategorií transakcí nákladů projektu (PSA do Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="adf76-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="adf76-120">Poté synchronizujte pomocí šablony kategorií transakcí projektových výdajů (Fin and Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="adf76-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="adf76-121">Poté spusťte synchronizaci z Project Service Automation do Finance and Operations ještě jednou.</span><span class="sxs-lookup"><span data-stu-id="adf76-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="adf76-122">Pokud synchronizujete nejprve z Project Service Automation, musí být splněny následujíc požadavky v Finance and Operations před spuštěním synchronizace:</span><span class="sxs-lookup"><span data-stu-id="adf76-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="adf76-123">Musí existovat sdílená kategorie, která odpovídá nastavené kategorii projektu v aplikaci Project Service Automation, a musí být povolena pro obě položky **Projekt** a **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="adf76-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="adf76-124">Pro každou právnickou osobu Finance and Operations, se kterou je třeba integrovat, musí existovat následující kategorie projektu:</span><span class="sxs-lookup"><span data-stu-id="adf76-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="adf76-125">**Kategorie projektu** existuje.</span><span class="sxs-lookup"><span data-stu-id="adf76-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="adf76-126">**Použít ve výdajích** je povoleno.</span><span class="sxs-lookup"><span data-stu-id="adf76-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="adf76-127">**Aktivní v denících** je povoleno.</span><span class="sxs-lookup"><span data-stu-id="adf76-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="adf76-128">**Typ transakce** je nastaven na **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="adf76-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="adf76-129">Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="adf76-130">[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="adf76-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="adf76-131">Synchronizace kategorie projektových výdajů z Finance and Operations do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="adf76-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="adf76-132">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="adf76-132">Template and task</span></span>

<span data-ttu-id="adf76-133">Chcete-li získat přístup k šabloně, zvolte v centru správy Microsoft PowerApps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.</span><span class="sxs-lookup"><span data-stu-id="adf76-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="adf76-134">K synchronizaci kategorií projektových výdajů z aplikace Finance and Operations do aplikace Project Service Automation slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="adf76-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="adf76-135">**Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (Fin and Ops do PSA)</span><span class="sxs-lookup"><span data-stu-id="adf76-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="adf76-136">**Název úkolu v projektu:** Synchronizace kategorií do PSA</span><span class="sxs-lookup"><span data-stu-id="adf76-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="adf76-137">Sada entit</span><span class="sxs-lookup"><span data-stu-id="adf76-137">Entity set</span></span>

| <span data-ttu-id="adf76-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adf76-138">Finance and Operations</span></span>            | <span data-ttu-id="adf76-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="adf76-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="adf76-140">Entita integrace pro kategorie</span><span class="sxs-lookup"><span data-stu-id="adf76-140">Integration entity for categories</span></span> | <span data-ttu-id="adf76-141">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="adf76-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="adf76-142">Tok entity</span><span class="sxs-lookup"><span data-stu-id="adf76-142">Entity flow</span></span>

<span data-ttu-id="adf76-143">Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="adf76-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="adf76-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="adf76-144">Power Query</span></span>

<span data-ttu-id="adf76-145">Musíte použít Microsoft Power Query pro Excel pro nastavení typu účtování na kategorii transakce při synchronizaci do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="adf76-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="adf76-146">Šablona kategorie transakce výdajů projektu (Fin and Ops do PSA) poskytuje výchozí sloupec a mapování.</span><span class="sxs-lookup"><span data-stu-id="adf76-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="adf76-147">Pokud vytvoříte vlastní šablony, je nutné přidat podmíněný sloupe v Power Query.</span><span class="sxs-lookup"><span data-stu-id="adf76-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="adf76-148">Postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="adf76-148">Follow these steps.</span></span>

1. <span data-ttu-id="adf76-149">Kliknutím na šipku otevřete mapování úlohy kategorie výdajů projektu v šabloně kategorií transakcí výdajů projektu (Fin and Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="adf76-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="adf76-150">Klikněte na odkaz **Filtrování a rozšířený dotaz** pro otevření Power Query.</span><span class="sxs-lookup"><span data-stu-id="adf76-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="adf76-151">Vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="adf76-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="adf76-152">Zadejte název pro nový sloupec, jako je například **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="adf76-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="adf76-153">Zadejte následující podmínku: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="adf76-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="adf76-154">Klikněte na **OK** na sloupci.</span><span class="sxs-lookup"><span data-stu-id="adf76-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="adf76-155">Ujistěte se, že mapujete tento nový sloupec na stránce mapování.</span><span class="sxs-lookup"><span data-stu-id="adf76-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="adf76-156">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="adf76-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="adf76-157">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Finance and Operations do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="adf76-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="adf76-158">[![Mapování šablony](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="adf76-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="adf76-159">Synchronizace kategorie projektových výdajů z Project Service Automation do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adf76-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="adf76-160">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="adf76-160">Template and task</span></span>

<span data-ttu-id="adf76-161">K synchronizaci kategorií projektových výdajů z aplikace Project Service Automation do Finance and Operations slouží následující šablona a základní úkoly:</span><span class="sxs-lookup"><span data-stu-id="adf76-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="adf76-162">**Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="adf76-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="adf76-163">**Název úkolu v projektu:** Synchronizace kategorií do Fin Ops</span><span class="sxs-lookup"><span data-stu-id="adf76-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="adf76-164">Sada entit</span><span class="sxs-lookup"><span data-stu-id="adf76-164">Entity set</span></span>

| <span data-ttu-id="adf76-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="adf76-165">Project Service Automation</span></span> | <span data-ttu-id="adf76-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adf76-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="adf76-167">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="adf76-167">Transaction categories</span></span>     | <span data-ttu-id="adf76-168">Entita integrace pro kategorie</span><span class="sxs-lookup"><span data-stu-id="adf76-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="adf76-169">Tok entity</span><span class="sxs-lookup"><span data-stu-id="adf76-169">Entity flow</span></span>

<span data-ttu-id="adf76-170">Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="adf76-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="adf76-171">Synchronizace zpět do Finance and Operations aktualizuje kategorie projektu v aplikaci Finance and Operations s ID integrace z aplikace Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="adf76-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="adf76-172">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="adf76-172">Template mapping in Data integration</span></span>

<span data-ttu-id="adf76-173">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="adf76-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="adf76-174">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adf76-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="adf76-175">[![Mapování šablony](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="adf76-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
