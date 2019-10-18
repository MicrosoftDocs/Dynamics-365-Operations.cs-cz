---
title: Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Microsoft Dynamics 365 Finance a Dynamics 365 Project Service Automation.
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
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250500"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="c752e-103">Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c752e-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c752e-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Dynamics 365 Finance a Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c752e-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="c752e-105">Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici ve verzi 8.0.</span><span class="sxs-lookup"><span data-stu-id="c752e-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="c752e-106">Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="c752e-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="c752e-107">Pokud používáte Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení.</span><span class="sxs-lookup"><span data-stu-id="c752e-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="c752e-108">Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="c752e-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="c752e-109">Tok dat pro Project Service Automation a Finance</span><span class="sxs-lookup"><span data-stu-id="c752e-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="c752e-110">Řešení integrace Project Service Automation a Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c752e-111">Šablony integrace, která jsou k dispozici s funkcí integrace dat, umožňují tok dat o kategoriích transakcí projektových výdajů mezi aplikacemi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="c752e-112">Pokud jsou kategorie výdajů projektu řízeny v Finance, tok integrace je nejdříve z Finance and Operations do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c752e-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="c752e-113">ID integrace kategorií výdajů projektu se poté aktualizují pomocí synchronizace z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c752e-114">Pokud jsou kategorie výdajů projektu řízeny v Project Service Automation, tok integrace je nejdříve z Prroject Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="c752e-115">Kategorie projektu musí být již nakonfigurována v aplikaci Finance před synchronizací z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c752e-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="c752e-116">Poté se synchronizuje z Finance zpět do Project Service Automation a poté znovu z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="c752e-117">Tímto způsobem pomůžete zajistit, aby byly kategorie propojeny a aby nebyly vytvořeny žádné duplicity.</span><span class="sxs-lookup"><span data-stu-id="c752e-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="c752e-118">Obvykle jsou kategorie výdajů projektu řízeny v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="c752e-119">Pokud však nejsou nebo pokud byly v aplikaci Project Service Automation vytvořeny kategorie výdajů, musíte nejprve synchronizovat pomocí šablony kategorií transakcí nákladů projektu (PSA do Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="c752e-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="c752e-120">Poté synchronizujte pomocí šablony kategorií transakcí projektových výdajů (Fin and Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="c752e-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="c752e-121">Poté spusťte synchronizaci z Project Service Automation do Finance ještě jednou.</span><span class="sxs-lookup"><span data-stu-id="c752e-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="c752e-122">Pokud synchronizujete nejprve z Project Service Automation, musí být splněny následujíc požadavky ve Finance před spuštěním synchronizace:</span><span class="sxs-lookup"><span data-stu-id="c752e-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="c752e-123">Musí existovat sdílená kategorie, která odpovídá nastavené kategorii projektu v aplikaci Project Service Automation, a musí být povolena pro obě položky **Projekt** a **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="c752e-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="c752e-124">Pro každou právnickou osobu Finance, se kterou je třeba integrovat, musí existovat následující kategorie projektu:</span><span class="sxs-lookup"><span data-stu-id="c752e-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="c752e-125">**Kategorie projektu** existuje.</span><span class="sxs-lookup"><span data-stu-id="c752e-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="c752e-126">**Použít ve výdajích** je povoleno.</span><span class="sxs-lookup"><span data-stu-id="c752e-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="c752e-127">**Aktivní v denících** je povoleno.</span><span class="sxs-lookup"><span data-stu-id="c752e-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="c752e-128">**Typ transakce** je nastaven na **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="c752e-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="c752e-129">Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c752e-130">[![Tok dat pro integraci Project Service Automation s aplikací Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c752e-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="c752e-131">Synchronizace kategorie projektových výdajů z Finance do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c752e-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="c752e-132">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="c752e-132">Template and task</span></span>

<span data-ttu-id="c752e-133">Chcete-li získat přístup k šabloně, zvolte v centru správy Microsoft PowerApps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.</span><span class="sxs-lookup"><span data-stu-id="c752e-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c752e-134">K synchronizaci kategorií projektových výdajů z aplikace Finance do Project Service Automation slouží následující šablona a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="c752e-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="c752e-135">**Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (Fin and Ops do PSA)</span><span class="sxs-lookup"><span data-stu-id="c752e-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="c752e-136">**Název úkolu v projektu:** Synchronizace kategorií do PSA</span><span class="sxs-lookup"><span data-stu-id="c752e-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="c752e-137">Sada entit</span><span class="sxs-lookup"><span data-stu-id="c752e-137">Entity set</span></span>

| <span data-ttu-id="c752e-138">Finance</span><span class="sxs-lookup"><span data-stu-id="c752e-138">Finance</span></span>                           | <span data-ttu-id="c752e-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c752e-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="c752e-140">Entita integrace pro kategorie</span><span class="sxs-lookup"><span data-stu-id="c752e-140">Integration entity for categories</span></span> | <span data-ttu-id="c752e-141">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="c752e-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="c752e-142">Tok entity</span><span class="sxs-lookup"><span data-stu-id="c752e-142">Entity flow</span></span>

<span data-ttu-id="c752e-143">Kategorie projektových výdajů jsou spravovány v aplikaci Finance a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="c752e-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c752e-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="c752e-144">Power Query</span></span>

<span data-ttu-id="c752e-145">Musíte použít Microsoft Power Query pro Excel pro nastavení typu účtování na kategorii transakce při synchronizaci do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c752e-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="c752e-146">Šablona kategorie transakce výdajů projektu (Fin and Ops do PSA) poskytuje výchozí sloupec a mapování.</span><span class="sxs-lookup"><span data-stu-id="c752e-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="c752e-147">Pokud vytvoříte vlastní šablony, je nutné přidat podmíněný sloupe v Power Query.</span><span class="sxs-lookup"><span data-stu-id="c752e-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="c752e-148">Postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="c752e-148">Follow these steps.</span></span>

1. <span data-ttu-id="c752e-149">Kliknutím na šipku otevřete mapování úlohy kategorie výdajů projektu v šabloně kategorií transakcí výdajů projektu (Fin and Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="c752e-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="c752e-150">Klikněte na odkaz **Filtrování a rozšířený dotaz** pro otevření Power Query.</span><span class="sxs-lookup"><span data-stu-id="c752e-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="c752e-151">Vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="c752e-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="c752e-152">Zadejte název pro nový sloupec, jako je například **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="c752e-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="c752e-153">Zadejte následující podmínku: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="c752e-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="c752e-154">Klikněte na **OK** na sloupci.</span><span class="sxs-lookup"><span data-stu-id="c752e-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="c752e-155">Ujistěte se, že mapujete tento nový sloupec na stránce mapování.</span><span class="sxs-lookup"><span data-stu-id="c752e-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="c752e-156">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="c752e-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="c752e-157">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c752e-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="c752e-158">[![Mapování šablony](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c752e-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="c752e-159">Synchronizace kategorie projektových výdajů z Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="c752e-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="c752e-160">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="c752e-160">Template and task</span></span>

<span data-ttu-id="c752e-161">K synchronizaci kategorií projektových výdajů z aplikace Project Service Automation do Finance slouží následující šablona a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="c752e-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c752e-162">**Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c752e-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c752e-163">**Název úkolu v projektu:** Synchronizace kategorií do Fin Ops</span><span class="sxs-lookup"><span data-stu-id="c752e-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="c752e-164">Sada entit</span><span class="sxs-lookup"><span data-stu-id="c752e-164">Entity set</span></span>

| <span data-ttu-id="c752e-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c752e-165">Project Service Automation</span></span> | <span data-ttu-id="c752e-166">Finance</span><span class="sxs-lookup"><span data-stu-id="c752e-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="c752e-167">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="c752e-167">Transaction categories</span></span>     | <span data-ttu-id="c752e-168">Entita integrace pro kategorie</span><span class="sxs-lookup"><span data-stu-id="c752e-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="c752e-169">Tok entity</span><span class="sxs-lookup"><span data-stu-id="c752e-169">Entity flow</span></span>

<span data-ttu-id="c752e-170">Kategorie projektových výdajů jsou spravovány v aplikaci Finance a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="c752e-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="c752e-171">Synchronizace zpět do Finance and Operations aktualizuje kategorie projektu v aplikaci Finance s ID integrace z aplikace Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c752e-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c752e-172">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="c752e-172">Template mapping in Data integration</span></span>

<span data-ttu-id="c752e-173">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="c752e-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="c752e-174">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="c752e-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c752e-175">[![Mapování šablony](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c752e-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
