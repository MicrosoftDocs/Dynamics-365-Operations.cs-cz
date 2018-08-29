--- 
title: "Vytvoření kalendářů a vygenerování pracovní doby"
description: "Kalendáře popisují kapacitu a pracovní dobu provozních prostředků."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 9e0b574d83272acf9ccad49e29e80827810b783a
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="6a009-103">Vytvoření kalendářů a vygenerování pracovní doby</span><span class="sxs-lookup"><span data-stu-id="6a009-103">Create calendars and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a009-104">Kalendáře popisují kapacitu a pracovní dobu provozních prostředků.</span><span class="sxs-lookup"><span data-stu-id="6a009-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="6a009-105">Tento postup vám usnadní definování pracovního kalendář podle šablony pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="6a009-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="6a009-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="6a009-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="6a009-107">Přejít na Všechny pracovní prostory > Správa životního cyklu prostředků.</span><span class="sxs-lookup"><span data-stu-id="6a009-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="6a009-108">Klepněte na Kalendáře.</span><span class="sxs-lookup"><span data-stu-id="6a009-108">Click Calendars.</span></span>
3. <span data-ttu-id="6a009-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6a009-109">Click New.</span></span>
4. <span data-ttu-id="6a009-110">Zadejte hodnotu do pole Kalendář.</span><span class="sxs-lookup"><span data-stu-id="6a009-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="6a009-111">Toto je ID kalendáře, který se používá jako odkaz k přiřazení kalendářů, jako jsou například provozní prostředek nebo skupina prostředků.</span><span class="sxs-lookup"><span data-stu-id="6a009-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="6a009-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="6a009-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="6a009-113">Do pole Standardní pracovní den v hodinách zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="6a009-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="6a009-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6a009-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="6a009-115">Klepněte na Pracovní doba.</span><span class="sxs-lookup"><span data-stu-id="6a009-115">Click Working times.</span></span>
9. <span data-ttu-id="6a009-116">Klepněte na Vytvořit pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="6a009-116">Click Compose working times.</span></span>
    * <span data-ttu-id="6a009-117">Generujte pracovní dobu pro každý den v období, kdy chcete mít možnost naplánovat práci.</span><span class="sxs-lookup"><span data-stu-id="6a009-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="6a009-118">Postupem času lze generovat pracovní dobu pro další období.</span><span class="sxs-lookup"><span data-stu-id="6a009-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="6a009-119">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="6a009-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="6a009-120">Toto je první den, kdy musí být tento kalendář otevřen.</span><span class="sxs-lookup"><span data-stu-id="6a009-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="6a009-121">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="6a009-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="6a009-122">Toto je poslední den, kdy je tento kalendář otevřen.</span><span class="sxs-lookup"><span data-stu-id="6a009-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="6a009-123">V poli Šablona pracovní doby zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6a009-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="6a009-124">Šablona pracovní doby určuje pracovní dobu pro každý den v týdnu.</span><span class="sxs-lookup"><span data-stu-id="6a009-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="6a009-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6a009-125">Click OK.</span></span>
14. <span data-ttu-id="6a009-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6a009-126">Close the page.</span></span>


