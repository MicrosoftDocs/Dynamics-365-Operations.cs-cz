---
title: Vytvoření kalendářů a vygenerování pracovní doby
description: Kalendáře popisují kapacitu a pracovní dobu provozních prostředků. Tento článek vysvětluje, jak definovat pracovní kalendář podle šablony pracovní doby.
author: andreabichsel
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16decd94f72e6aefe4e1d058f4cfd6215d14f569
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058889"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="dfa90-104">Vytvoření kalendářů a vygenerování pracovní doby</span><span class="sxs-lookup"><span data-stu-id="dfa90-104">Create calendars and generate working times</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="dfa90-105">Kalendáře popisují kapacitu a pracovní dobu provozních prostředků.</span><span class="sxs-lookup"><span data-stu-id="dfa90-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="dfa90-106">Tento článek vysvětluje, jak definovat pracovní kalendář podle šablony pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="dfa90-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="dfa90-107">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="dfa90-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="dfa90-108">Na domovské stránce vyberte položku **Správa životního cyklu zdroje**.</span><span class="sxs-lookup"><span data-stu-id="dfa90-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="dfa90-109">Vyberte **Kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="dfa90-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="dfa90-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dfa90-110">Select **New**.</span></span>
4. <span data-ttu-id="dfa90-111">V poli **Kalendář** označte kalendář.</span><span class="sxs-lookup"><span data-stu-id="dfa90-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="dfa90-112">Toto je ID kalendáře, který se používá jako odkaz k přiřazení kalendářů, jako jsou například provozní prostředek nebo skupina prostředků.</span><span class="sxs-lookup"><span data-stu-id="dfa90-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="dfa90-113">Do pole **Název** zadejte název kalendáře.</span><span class="sxs-lookup"><span data-stu-id="dfa90-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="dfa90-114">Do pole **Standardní pracovní den v hodinách** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="dfa90-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="dfa90-115">Přesvědčte se, zda je řádek vybrán, a v podokně akcí vyberte možnost **Pracovní doba**.</span><span class="sxs-lookup"><span data-stu-id="dfa90-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="dfa90-116">Vyberte **Vytvořit pracovní doby**.</span><span class="sxs-lookup"><span data-stu-id="dfa90-116">Select **Compose working times**.</span></span> <span data-ttu-id="dfa90-117">Generujte pracovní dobu pro každý den v období, kdy chcete mít možnost naplánovat práci.</span><span class="sxs-lookup"><span data-stu-id="dfa90-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="dfa90-118">Postupem času lze generovat pracovní dobu pro další období.</span><span class="sxs-lookup"><span data-stu-id="dfa90-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="dfa90-119">Do pole **Od data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="dfa90-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="dfa90-120">Toto je první den, kdy musí být tento kalendář otevřen.</span><span class="sxs-lookup"><span data-stu-id="dfa90-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="dfa90-121">Do pole **Do data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="dfa90-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="dfa90-122">Toto je poslední den, kdy je tento kalendář otevřen.</span><span class="sxs-lookup"><span data-stu-id="dfa90-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="dfa90-123">V poli **Šablona pracovní doby** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dfa90-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="dfa90-124">Šablona pracovní doby určuje pracovní dobu pro každý den v týdnu.</span><span class="sxs-lookup"><span data-stu-id="dfa90-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="dfa90-125">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfa90-125">Select **OK**.</span></span>
13. <span data-ttu-id="dfa90-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa90-126">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]