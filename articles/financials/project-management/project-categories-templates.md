---
title: "Synchronizace kategorií nákladů projektu z Project Service Automation"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci kategorií projektových nákladů mezi Microsoft Dynamics 365 for for Finance and Operations a Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: cs-cz
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="ff2ea-103">Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff2ea-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="ff2ea-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci kategorií projektových nákladů mezi Microsoft Dynamics 365 for for Finance and Operations a Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="ff2ea-105">Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Dynamics 365 for Finance and Operations verze 8.0.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="ff2ea-106">Tok dat pro Project Service Automation a aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff2ea-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="ff2ea-107">Řešení integrace Project Service Automation a Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="ff2ea-108">Šablony integrace, která jsou k dispozici s funkcí integrace dat, umožňují tok dat o kategoriích transakcí projektových výdajů mezi aplikacemi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="ff2ea-109">Pokud jsou kategorie výdajů projektu řízeny v aplikaci Finance and Operations, tok integrace je nejprve z Finance and Operations do Project Service Automation, a poté se aktualizují ID integrace kategorií projektových výdajů synchronizací z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ff2ea-110">Pokud jsou kategorie výdajů projektu řízeny v Project Service Automation, tok integrace je nejdříve z Prroject Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="ff2ea-111">Kategorie projektu musí být již nakonfigurována v aplikaci Finance and Operations před synchronizací z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="ff2ea-112">Poté se synchronizuje z Finance and Operations zpět do Project Service Automation a poté znovu z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="ff2ea-113">Tím zajistíte, že jsou kategorie propojeny a nejsou vytvořeny duplicitní položky.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="ff2ea-114">Obvykle budou kategorie výdajů projektu řízeny v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="ff2ea-115">Pokud se nejedná o tuto situaci nebo již máte kategorie výdajů vytvořeny v Project Service Automation, musíte nejprve synchronizovat pomocí kategorií transakcí výdajů projektu (PSA do Fin and Ops) a poté synchronizovat pomocí kategorií transakce výdajů projektu (Fin and OPS do PSA).</span><span class="sxs-lookup"><span data-stu-id="ff2ea-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="ff2ea-116">Pak spusťte synchronizaci z PSA do Fin and Ops ještě jednou.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="ff2ea-117">Při synchronizaci nejprve z Project Service Automation musí být již kategorie projektu nastaveny v aplikaci Finance and Operations a všechny projektové kategorie, které musí být synchronizovány s kategoriemi transakcí Project Service Automation musí být nastaveny tak, aby byly **Aktivní v denících**.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="ff2ea-118">Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="ff2ea-119">[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ff2ea-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="ff2ea-120">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="ff2ea-120">Templates and tasks</span></span>

<span data-ttu-id="ff2ea-121">Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty**a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ff2ea-122">K synchronizaci kategorií projektových výdajů z aplikace Finance and Operations do aplikace Project Service Automation slouží následující šablona a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="ff2ea-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="ff2ea-123">**Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (Fin and Ops do PSA)</span><span class="sxs-lookup"><span data-stu-id="ff2ea-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="ff2ea-124">**Název úkolu v projektu:** Synchronizace kategorií do PSA</span><span class="sxs-lookup"><span data-stu-id="ff2ea-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="ff2ea-125">Sada entit</span><span class="sxs-lookup"><span data-stu-id="ff2ea-125">Entity set</span></span>

| <span data-ttu-id="ff2ea-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff2ea-126">Finance and Operations</span></span>               | <span data-ttu-id="ff2ea-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff2ea-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="ff2ea-128">Entita integrace pro kategorie</span><span class="sxs-lookup"><span data-stu-id="ff2ea-128">Integration entity for categories</span></span>    | <span data-ttu-id="ff2ea-129">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="ff2ea-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="ff2ea-130">Tok entity</span><span class="sxs-lookup"><span data-stu-id="ff2ea-130">Entity flow</span></span>

<span data-ttu-id="ff2ea-131">Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="ff2ea-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="ff2ea-132">Power Query</span></span>

<span data-ttu-id="ff2ea-133">Musíte použít Microsoft Power Query pro nastavení typu účtování na kategorii transakce při synchronizaci do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="ff2ea-134">Šablona kategorie transakce výdajů projektu (Fin and Ops do PSA) má výchozí sloupec a mapování je již zadáno.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="ff2ea-135">Pokud vytvoříte vlastní šablony, je nutné přidat podmíněný sloupe v Power Query.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="ff2ea-136">Otevřete formulář filtrování a rozšířeného dotazu z mapování úkolu kategorie výdajů projektu.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="ff2ea-137">Vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="ff2ea-138">Zadejte nový název sloupce, například BillingType.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="ff2ea-139">Zadejte následující podmínku: pokud **CATEGORYID se nerovná null, pak 19235001, jinak null**.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="ff2ea-140">Klikněte na **OK** na sloupci.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="ff2ea-141">Ujistěte se, že mapujete tento nový sloupec na stránce mapování.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="ff2ea-142">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ff2ea-143">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Finance and Operations do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="ff2ea-144">[![Mapování šablony](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ff2ea-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="ff2ea-145">K synchronizaci kategorií projektových výdajů z aplikace Project Service Automation do aplikace inance and Operations slouží následující šablona a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="ff2ea-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="ff2ea-146">-**Název šablony v integraci dat:** Kategorie transakcí výdajů projektu (PSA do Fin and Ops) -**Název úkolu v projektu:** Synchronizace kategorií do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="ff2ea-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="ff2ea-147">Sada entit</span><span class="sxs-lookup"><span data-stu-id="ff2ea-147">Entity set</span></span>

| <span data-ttu-id="ff2ea-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff2ea-148">Project Service Automation</span></span>      | <span data-ttu-id="ff2ea-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff2ea-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="ff2ea-150">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="ff2ea-150">Transaction categories</span></span>          | <span data-ttu-id="ff2ea-151">Entita integrace pro kategorie</span><span class="sxs-lookup"><span data-stu-id="ff2ea-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="ff2ea-152">Tok entity</span><span class="sxs-lookup"><span data-stu-id="ff2ea-152">Entity flow</span></span>

<span data-ttu-id="ff2ea-153">Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="ff2ea-154">Synchronizace zpět do Finance and Operations aktualizuje ID integrace Project Service Automation na kategorie projektu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="ff2ea-155">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ff2ea-156">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff2ea-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ff2ea-157">[![Mapování šablony](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ff2ea-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

