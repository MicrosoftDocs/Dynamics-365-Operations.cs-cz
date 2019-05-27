---
title: Požadavky na nastavení výroby
description: V tomto článku jsou informace o požadavcích na nastavení předtím, než bude možné pracovat s modulem řízení výroby.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b811c11271097f4bb7910c34f7775955abba526d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559110"
---
# <a name="production-setup-requirements"></a><span data-ttu-id="cffdb-103">Požadavky na nastavení výroby</span><span class="sxs-lookup"><span data-stu-id="cffdb-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cffdb-104">V tomto článku jsou informace o požadavcích na nastavení předtím, než bude možné pracovat s modulem řízení výroby.</span><span class="sxs-lookup"><span data-stu-id="cffdb-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="cffdb-105">Modul Řízení výroby je integrován s funkcemi v ostatních modulech.</span><span class="sxs-lookup"><span data-stu-id="cffdb-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="cffdb-106">Díky této propojenosti můžete měnit výrobní zakázky a spolehnout se na to, že tyto zakázky budou automaticky aktualizovány ve všech souvisejících procesech a výpočtech v daném systému.</span><span class="sxs-lookup"><span data-stu-id="cffdb-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="cffdb-107">Následující procesy nastavení by měly být provedeny v pořadí, v jakém jsou uvedeny.</span><span class="sxs-lookup"><span data-stu-id="cffdb-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="cffdb-108">Vyžadované základní nastavení v jiných modulech</span><span class="sxs-lookup"><span data-stu-id="cffdb-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="cffdb-109">Před prací s modulem Řízení výroby je nutné nastavit informace v jiných modulech.</span><span class="sxs-lookup"><span data-stu-id="cffdb-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="cffdb-110">Tato nastavení zahrnuje následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="cffdb-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="cffdb-111">Nastavení obecných informací o společnosti</span><span class="sxs-lookup"><span data-stu-id="cffdb-111">Set up general company information.</span></span>
-   <span data-ttu-id="cffdb-112">Nastavení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="cffdb-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="cffdb-113">Definování skupin položek</span><span class="sxs-lookup"><span data-stu-id="cffdb-113">Define item groups.</span></span>
-   <span data-ttu-id="cffdb-114">Nastavení účtů hlavní knihy pro skupiny položek</span><span class="sxs-lookup"><span data-stu-id="cffdb-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="cffdb-115">Nastavení tabulky položek zásob v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="cffdb-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="cffdb-116">V modulu Řízení zásob vytvořte kusovníky (BOM) a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cffdb-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="cffdb-117">Potřebné nastavení kalendáře a prostředků</span><span class="sxs-lookup"><span data-stu-id="cffdb-117">Required calendar and resource setup</span></span>
<span data-ttu-id="cffdb-118">Před použitím modulu Řízení výroby otevřete modul Správa organizace a v následujícím pořadí vytvořte a definujte kalendář a provozní prostředky:</span><span class="sxs-lookup"><span data-stu-id="cffdb-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="cffdb-119">**Šablony pracovní doby** – Nastavením šablon pracovní doby definujte doby, které jsou k dispozici pro plánování výroby.</span><span class="sxs-lookup"><span data-stu-id="cffdb-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="cffdb-120">**Kalendáře** – Nastavením kalendářů pracovní doby definujte dny v roce, které jsou k dispozici pro plánování výroby.</span><span class="sxs-lookup"><span data-stu-id="cffdb-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="cffdb-121">**Skupiny prostředků** – Nastavením skupiny prostředků seskupte provozní prostředky, abyste mohli při spuštění plánování získat přehled o všech volných kapacitách.</span><span class="sxs-lookup"><span data-stu-id="cffdb-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="cffdb-122">Není nutné nastavovat provozní prostředky ještě před nastavením skupin prostředků.</span><span class="sxs-lookup"><span data-stu-id="cffdb-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="cffdb-123">Doporučujeme však, abyste se seznámili se způsobem, jakým se při nastavování v modulu Řízení výroby seskupují prostředky.</span><span class="sxs-lookup"><span data-stu-id="cffdb-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="cffdb-124">**Zdroje** – Nastavením provozních prostředků definujte zdroje používané k provedení výrobního procesu a k plánování kapacity.</span><span class="sxs-lookup"><span data-stu-id="cffdb-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="cffdb-125">Vyžadovaná nastavení parametrů výroby</span><span class="sxs-lookup"><span data-stu-id="cffdb-125">Required production parameters setup</span></span>
<span data-ttu-id="cffdb-126">**Parametry řízení výroby** – Nastavením základních parametrů výroby definujte způsob, jakým systém zpracovává výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="cffdb-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="cffdb-127">Určete způsob, jakým jsou výrobní zakázky vytvářeny, odhadovány, plánovány a spotřebovávány.</span><span class="sxs-lookup"><span data-stu-id="cffdb-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="cffdb-128">Dále je možné vybrat požadovaný druh zpětné vazby a způsob provádění nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="cffdb-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="cffdb-129">Vyžadovaná identifikace názvu deníku</span><span class="sxs-lookup"><span data-stu-id="cffdb-129">Required journal name identification</span></span>
<span data-ttu-id="cffdb-130">**Názvy deníků výroby** - Určete názvy deníků výroby používaných k zaznamenání a zaúčtování transakcí.</span><span class="sxs-lookup"><span data-stu-id="cffdb-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="cffdb-131">Nastavení při použití operací</span><span class="sxs-lookup"><span data-stu-id="cffdb-131">Setup if you use operations</span></span>
<span data-ttu-id="cffdb-132">Operace reprezentují specifické aktivity prováděné za účelem výroby hotového výrobku.</span><span class="sxs-lookup"><span data-stu-id="cffdb-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="cffdb-133">**Poznámka:** Je nutné znát typy aktivit, které jsou zapotřebí k výrobě položky, a také pořadí a priority těchto aktivit.</span><span class="sxs-lookup"><span data-stu-id="cffdb-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="cffdb-134">Také musíte vědět, které prostředky jsou zapojeny a kolik jich je.</span><span class="sxs-lookup"><span data-stu-id="cffdb-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="cffdb-135">**Operace** – Nastavte operace reprezentující úkoly, které je nutné dokončit při výrobě hotové položky.</span><span class="sxs-lookup"><span data-stu-id="cffdb-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="cffdb-136">**Vztahy** – Nastavením vztahů operací vytvořte podrobné vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="cffdb-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="cffdb-137">Vztahy operací můžete definovat kliknutím na tlačítko **Vztahy** na stránce **Operace**.</span><span class="sxs-lookup"><span data-stu-id="cffdb-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="cffdb-138">Nastavení při použití postupů</span><span class="sxs-lookup"><span data-stu-id="cffdb-138">Setup if you use routes</span></span>
<span data-ttu-id="cffdb-139">Pokud pracujete s postupy, je nutné definovat operaci pro každý nastavený výrobní postup.</span><span class="sxs-lookup"><span data-stu-id="cffdb-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="cffdb-140">Postup reprezentuje cestu, kterou položka urazí mezi operacemi od počátku procesu výroby až po jeho konec.</span><span class="sxs-lookup"><span data-stu-id="cffdb-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="cffdb-141">**Nákladové kategorie** – Nastavením nákladových kategorií definujte náklady na hodinu pro stanované procesy a přípravné časy.</span><span class="sxs-lookup"><span data-stu-id="cffdb-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="cffdb-142">**Nákladové skupiny** – Nastavením nákladových skupin můžete vytvořit a udržovat různé typy nákladů.</span><span class="sxs-lookup"><span data-stu-id="cffdb-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="cffdb-143">**Skupiny postupů** – Nastavením skupin postupů můžete definovat parametry týkající se skupin postupů.</span><span class="sxs-lookup"><span data-stu-id="cffdb-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="cffdb-144">Skupiny postupů je nutné nastavit před vytvořením výrobních postupů.</span><span class="sxs-lookup"><span data-stu-id="cffdb-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="cffdb-145">**Postupy** – Nastavením výrobních postupů a definováním výchozích nastavení můžete řídit plánování, náklady a oceňování operací postupů a hlášení průběhu.</span><span class="sxs-lookup"><span data-stu-id="cffdb-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="cffdb-146">**Postupy** – Nastavením verzí postupů povolíte odchylky položek ve výrobě.</span><span class="sxs-lookup"><span data-stu-id="cffdb-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="cffdb-147">Volitelná rozšířená nastavení</span><span class="sxs-lookup"><span data-stu-id="cffdb-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="cffdb-148">**Skupiny výroby** – Nastavením skupin výroby vytvoříte vztahy mezi výrobní zakázkou a účty hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="cffdb-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="cffdb-149">Účty hlavní knihy jsou používány k zaúčtování nebo seskupení objednávek pro vykazování.</span><span class="sxs-lookup"><span data-stu-id="cffdb-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="cffdb-150">**Skupiny produktů** – Vytvořením skupin výrobků můžete seskupit výrobní zakázky tak, že bude možné zpracovat naléhavé výrobní zakázky nebo odstranit a zaúčtovat skupiny objednávek.</span><span class="sxs-lookup"><span data-stu-id="cffdb-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="cffdb-151">**Vlastnosti** – Definováním vlastností můžete vytvořit speciální atributy, které lze přiřadit zdrojům a řídit tak pořadí výroby.</span><span class="sxs-lookup"><span data-stu-id="cffdb-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="cffdb-152">Tyto atributy jsou spojeny se šablonou pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="cffdb-152">These attributes are connected to the working time template.</span></span>




