---
title: Vytvoření kalendáře a generování pracovní doby
description: Kalendáře popisují kapacitu a pracovní dobu provozních prostředků.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a556367857890acdb926ed29518cf2f2f2b92ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "336007"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="d3222-103">Vytvoření kalendáře a generování pracovní doby</span><span class="sxs-lookup"><span data-stu-id="d3222-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3222-104">Kalendáře popisují kapacitu a pracovní dobu provozních prostředků.</span><span class="sxs-lookup"><span data-stu-id="d3222-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="d3222-105">Tento postup vám usnadní definování pracovního kalendář podle šablony pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="d3222-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="d3222-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="d3222-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d3222-107">Přejít na Všechny pracovní prostory > Správa životního cyklu prostředků.</span><span class="sxs-lookup"><span data-stu-id="d3222-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="d3222-108">Klepněte na Kalendáře.</span><span class="sxs-lookup"><span data-stu-id="d3222-108">Click Calendars.</span></span>
3. <span data-ttu-id="d3222-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d3222-109">Click New.</span></span>
4. <span data-ttu-id="d3222-110">Zadejte hodnotu do pole Kalendář.</span><span class="sxs-lookup"><span data-stu-id="d3222-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="d3222-111">Toto je ID kalendáře, který se používá jako odkaz k přiřazení kalendářů, jako jsou například provozní prostředek nebo skupina prostředků.</span><span class="sxs-lookup"><span data-stu-id="d3222-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="d3222-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d3222-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d3222-113">Do pole Standardní pracovní den v hodinách zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="d3222-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="d3222-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d3222-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d3222-115">Klepněte na Pracovní doba.</span><span class="sxs-lookup"><span data-stu-id="d3222-115">Click Working times.</span></span>
9. <span data-ttu-id="d3222-116">Klepněte na Vytvořit pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="d3222-116">Click Compose working times.</span></span>
    * <span data-ttu-id="d3222-117">Generujte pracovní dobu pro každý den v období, kdy chcete mít možnost naplánovat práci.</span><span class="sxs-lookup"><span data-stu-id="d3222-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="d3222-118">Postupem času lze generovat pracovní dobu pro další období.</span><span class="sxs-lookup"><span data-stu-id="d3222-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="d3222-119">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="d3222-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="d3222-120">Toto je první den, kdy musí být tento kalendář otevřen.</span><span class="sxs-lookup"><span data-stu-id="d3222-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="d3222-121">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="d3222-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="d3222-122">Toto je poslední den, kdy je tento kalendář otevřen.</span><span class="sxs-lookup"><span data-stu-id="d3222-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="d3222-123">V poli Šablona pracovní doby zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d3222-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="d3222-124">Šablona pracovní doby určuje pracovní dobu pro každý den v týdnu.</span><span class="sxs-lookup"><span data-stu-id="d3222-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="d3222-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d3222-125">Click OK.</span></span>
14. <span data-ttu-id="d3222-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d3222-126">Close the page.</span></span>

