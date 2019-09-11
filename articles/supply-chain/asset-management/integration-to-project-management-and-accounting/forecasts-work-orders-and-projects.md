---
title: Prognózy, pracovní příkazy a projekty
description: Toto téma popisuje integraci prognóz a pracovních příkazů s modulem Řízení a účetnictví projektů ve Správě majetku.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886809"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="6939c-103">Prognózy, pracovní příkazy a projekty</span><span class="sxs-lookup"><span data-stu-id="6939c-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6939c-104">Ve Správě majetku se provádí integrace s modulem **Řízení a účetnictví projektů** za účelem optimalizace řízení nákladů, což uživatelům umožňuje sledovat náklady v rámci prognóz typů prací údržby a úloh pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="6939c-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="6939c-105">Chcete-li sledovat prognózu typu prací údržby, je nutné provést dvě nastavení:</span><span class="sxs-lookup"><span data-stu-id="6939c-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="6939c-106">Přejděte do **Správa majetku** > **Nastavení** > **Parametry správy majetku** > odkaz **Majetek** > záložka s náhledem **Projekt** > pole **Projekt prognózy údržby**.</span><span class="sxs-lookup"><span data-stu-id="6939c-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="6939c-107">V části **Výchozí nastavení typu práce údržby** při vytvoření výchozího řádku typu práce údržby je automaticky vytvořeno číslo aktivity pro daný řádek (**Správa majetku** > **Nastavení** > **Práce** > **Výchozí nastavení typu práce**).</span><span class="sxs-lookup"><span data-stu-id="6939c-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="6939c-108">Prognózy typu práce údržby slouží dvěma účelům: v modulu **Řízení a účetnictví projektů** můžete sledovat náklady na prognózy typů prací údržby.</span><span class="sxs-lookup"><span data-stu-id="6939c-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="6939c-109">Prognózy se dále automaticky přenesou do projektu úlohy pracovního příkazu při výběru typu práce údržby na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="6939c-110">Chcete-li sledovat náklady na úlohy pracovních příkazů, musíte nejprve nastavit projekty pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="6939c-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="6939c-111">Popis potřebného postupu naleznete v části [Nastavení projektu pracovního příkazu](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="6939c-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="6939c-112">Projekty úloh pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="6939c-112">Work order job projects</span></span>

<span data-ttu-id="6939c-113">Při vytváření úlohy pracovního příkazu na pracovním příkazu je projekt pracovního příkazu určen nastavením nadřazeného projektu pro pracovní příkazy v sekci **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**.</span><span class="sxs-lookup"><span data-stu-id="6939c-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="6939c-114">Projekty úloh pracovních příkazů jsou vytvářeny pomocí kombinace následujících informací o pracovním příkazu:</span><span class="sxs-lookup"><span data-stu-id="6939c-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="6939c-115">Typ pracovního příkazu vybraný na pracovním příkazu</span><span class="sxs-lookup"><span data-stu-id="6939c-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="6939c-116">Funkční místo související s majetkem v úloze pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="6939c-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="6939c-117">Typ majetku související s majetkem v úloze pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="6939c-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="6939c-118">Očekávaný čas zahájení a ukončení nastavený na pracovním příkazu</span><span class="sxs-lookup"><span data-stu-id="6939c-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="6939c-119">Je možné, že ne všechny výše uvedené informace se nacházejí v pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="6939c-120">Vyhledávání nadřazeného projektu pracovního příkazu je proto provedeno pomocí dostupné kombinace dat a výběrem ID projektu, které odpovídá údajům pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="6939c-121">Příklad: Na níže uvedeném obrázku je nastavení typu majetku „Motor nákladního automobilu“ znamená, že každá úloha pracovního příkazu vytvořená s tímto typem majetku bude dílčím projektem pro ID projektu „000186“.</span><span class="sxs-lookup"><span data-stu-id="6939c-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![Obrázek č. 1](media/01-integration-to-pma.png)

<span data-ttu-id="6939c-123">Účelem ID projektu v úloze pracovního příkazu a souvisejícího čísla aktivity (**Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** > v seznamu vyberte pracovní příkaz > záložka s náhledem **Podrobnosti řádku** > pole **ID projektu** a pole **Číslo aktivity**) je sledování nákladů souvisejících s úlohou pracovního příkazu a majetku vybraného v úloze pracovního příkazu v modulu **Řízení a účetnictví projektů**.</span><span class="sxs-lookup"><span data-stu-id="6939c-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="6939c-124">Na následujícím obrázku je zobrazen grafický přehled projektů pracovních příkazů a souvisejících aktivit projektu.</span><span class="sxs-lookup"><span data-stu-id="6939c-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![Obrázek č. 2](media/02-integration-to-pma.png)

<span data-ttu-id="6939c-126">Při vytvoření nové úlohy pracovního příkazu na pracovním příkazu je automaticky vytvořen projekt pracovního příkazu pro danou úlohu.</span><span class="sxs-lookup"><span data-stu-id="6939c-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="6939c-127">Finanční dimenze majetku souvisejícího s úlohou pracovního příkazu se automaticky přenesou do projektu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="6939c-128">Aktivita projektu vytvořená pro úlohu pracovního příkazu obsahuje související informace týkající se typu práce údržby, typu operace údržby a obchodu.</span><span class="sxs-lookup"><span data-stu-id="6939c-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="6939c-129">Tyto údaje jsou užitečné, pokud například vytvoříte nákupní objednávku z pracovního příkazu (viz [Zásobování](../work-orders/procurement.md)) nebo pokud pro registraci pracovní doby používáte modul **Řízení a účetnictví projektů**.</span><span class="sxs-lookup"><span data-stu-id="6939c-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="6939c-130">Pokud byl majetek instalován ve funkčním místě a tento majetek je později nainstalován v jiném funkčním místě, finanční dimenze majetku související s novým funkčním místem se automaticky aktualizují.</span><span class="sxs-lookup"><span data-stu-id="6939c-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="6939c-131">Poté, když pro daný majetek vytvoříte úlohu pracovního příkazu, projekt pracovního příkazu pro úlohu pracovního příkazu automaticky získá finanční dimenze, které aktuálně souvisejí s majetkem.</span><span class="sxs-lookup"><span data-stu-id="6939c-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="6939c-132">To znamená, že při použití funkčních míst mohou být náklady vždy sledovány ve funkčních místech, ve kterých byl majetek nainstalován v daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="6939c-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="6939c-133">Automatická aktualizace finančních dimenzí zajišťuje úplnou sledovatelnost nákladů pro řízení a vykazování projektů.</span><span class="sxs-lookup"><span data-stu-id="6939c-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="6939c-134">Projekty s pracovními příkazy, stavy životního cyklu pracovních příkazů, fáze projektu a typy projektů</span><span class="sxs-lookup"><span data-stu-id="6939c-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="6939c-135">Chcete-li zajistit správné používání stavů životního cyklu pracovních příkazů a souvisejících fází projektu v pracovních příkazech, zvažte závislosti na modulu **Řízení a účetnictví projektů**:</span><span class="sxs-lookup"><span data-stu-id="6939c-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="6939c-136">V modulu **Řízení a účetnictví projektů** se fáze projektu nastavují pro typy projektů v části **Parametry řízení a účetnictví projektů**.</span><span class="sxs-lookup"><span data-stu-id="6939c-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="6939c-137">V části **Parametry řízení a účetnictví projektů** nezapomeňte zaškrtnout příslušná políčka fáze projektu pro všechny typy projektů, které hodláte použít.</span><span class="sxs-lookup"><span data-stu-id="6939c-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="6939c-138">Na níže uvedeném obrázku jsou pro typy projektů „Čas a materiál“ a „Interní“ vybráno pět fází: **Vytvořeno** - **Odhad** - **Rozvrh** - **Zpracování** - **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="6939c-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="6939c-139">Těchto pět fází souvisí s interními pracemi údržby i servisními pracemi údržby.</span><span class="sxs-lookup"><span data-stu-id="6939c-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="6939c-140">V modulu **Správa majetku** jsou typy projektů definovány skupinami projektů, které nastavíte ve formuláři **Nastavení projektu pracovního příkazu** > odkaz **Skupina projektů**.</span><span class="sxs-lookup"><span data-stu-id="6939c-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="6939c-141">Nastavení skupin projektů v **Nastavení projektu pracovního příkazu** se používá při vytváření pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="6939c-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="6939c-142">Při vytvoření pracovního příkazu je pro daný pracovní příkaz automaticky vytvořen projekt pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="6939c-143">Každý stav životního cyklu pracovního příkazu musí mít související fázi projektu.</span><span class="sxs-lookup"><span data-stu-id="6939c-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="6939c-144">Fáze projektu související se stavem životního cyklu pracovního příkazu musí být definována jako aktivní fáze pro skupinu projektů definovanou v projektu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="6939c-145">Projekt pracovního příkazu je automaticky vytvořen v rámci pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="6939c-146">Při vytvoření nového pracovního příkazu je automatické přidělení projektu pracovního příkazu založeno na **nastavení projektu pracovního příkazu** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**).</span><span class="sxs-lookup"><span data-stu-id="6939c-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="6939c-147">Následující obrázky znázorňují přidružení mezi skupinami projektů pracovních příkazů, typy souvisejících projektů, fázemi projektu a stavy životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6939c-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![Obrázek č. 3](media/03-integration-to-pma.png)

![Obrázek č. 4](media/04-integration-to-pma.png)

![Obrázek č. 5](media/05-integration-to-pma.png)

<span data-ttu-id="6939c-151">V části [Nastavení projektu pracovního příkazu](../setup-for-work-orders/work-order-project-setup.md) najdete informace, jak nastavit projekty pracovních příkazů, a v části [Stavy životního cyklu pracovního příkazu](../setup-for-work-orders/work-order-lifecycle-states.md) zjistíte, jak vytvořit stavy životního cyklu pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="6939c-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="6939c-152">Na následujícím obrázku je znázorněn grafický přehled různých projektů vytvořených v modulu **Správa majetku**, které umožňují integraci s modulem **Řízení a účetnictví projektů**, a také o pracovních procesech souvisejících s projekty.</span><span class="sxs-lookup"><span data-stu-id="6939c-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![Obrázek č. 6](media/06-integration-to-pma.png)

