---
title: Vytvoření šablon pracovní doby
description: Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c82126d64954f8691571b80ab97b198d58a9e2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837703"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="da172-103">Vytvoření šablon pracovní doby</span><span class="sxs-lookup"><span data-stu-id="da172-103">Create working time templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da172-104">Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek.</span><span class="sxs-lookup"><span data-stu-id="da172-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="da172-105">Tento postup popisuje, jak definovat šablony pracovní doby pomocí vlastností plánování pracovní doby pro zařazení časových intervalů práce.</span><span class="sxs-lookup"><span data-stu-id="da172-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="da172-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="da172-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="da172-107">Přejít na Všechny pracovní prostory > Správa životního cyklu prostředků.</span><span class="sxs-lookup"><span data-stu-id="da172-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="da172-108">Klepněte na Šablony pracovních dob.</span><span class="sxs-lookup"><span data-stu-id="da172-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="da172-109">Vytvoření šablony pracovní doby</span><span class="sxs-lookup"><span data-stu-id="da172-109">Create working time template</span></span>
1. <span data-ttu-id="da172-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="da172-110">Click New.</span></span>
2. <span data-ttu-id="da172-111">Zadejte hodnotu do pole Pracovní doba.</span><span class="sxs-lookup"><span data-stu-id="da172-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="da172-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="da172-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="da172-113">Rozbalte sekci Pondělí.</span><span class="sxs-lookup"><span data-stu-id="da172-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="da172-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="da172-114">Click Add.</span></span>
6. <span data-ttu-id="da172-115">Do pole Od zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="da172-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="da172-116">Určete čas při zahájení práce ráno.</span><span class="sxs-lookup"><span data-stu-id="da172-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="da172-117">Do pole Do zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="da172-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="da172-118">Zadejte čas, kdy zaměstnanci mají přestávku na oběd.</span><span class="sxs-lookup"><span data-stu-id="da172-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="da172-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="da172-119">Click Add.</span></span>
9. <span data-ttu-id="da172-120">Do pole Od zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="da172-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="da172-121">Zadejte čas, kdy práci obnoví po obědě.</span><span class="sxs-lookup"><span data-stu-id="da172-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="da172-122">Do pole Do zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="da172-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="da172-123">Určete konec pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="da172-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="da172-124">Replikace pracovní doby pro všechny dny v týdnu</span><span class="sxs-lookup"><span data-stu-id="da172-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="da172-125">Klepněte na Kopírovat den.</span><span class="sxs-lookup"><span data-stu-id="da172-125">Click Copy day.</span></span>
    * <span data-ttu-id="da172-126">Zkopírujte definice pracovní doby od pondělí do úterý.</span><span class="sxs-lookup"><span data-stu-id="da172-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="da172-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="da172-127">Click OK.</span></span>
3. <span data-ttu-id="da172-128">Klepněte na Kopírovat den.</span><span class="sxs-lookup"><span data-stu-id="da172-128">Click Copy day.</span></span>
    * <span data-ttu-id="da172-129">Zkopírujte definice pracovní doby od pondělí do středa.</span><span class="sxs-lookup"><span data-stu-id="da172-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="da172-130">Vyberte volbu v poli Do pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="da172-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="da172-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="da172-131">Click OK.</span></span>
6. <span data-ttu-id="da172-132">Klepněte na Kopírovat den.</span><span class="sxs-lookup"><span data-stu-id="da172-132">Click Copy day.</span></span>
    * <span data-ttu-id="da172-133">Zkopírujte definice pracovní doby od pondělí do čtvrtka.</span><span class="sxs-lookup"><span data-stu-id="da172-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="da172-134">Vyberte volbu v poli Do pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="da172-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="da172-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="da172-135">Click OK.</span></span>
9. <span data-ttu-id="da172-136">Klepněte na Kopírovat den.</span><span class="sxs-lookup"><span data-stu-id="da172-136">Click Copy day.</span></span>
    * <span data-ttu-id="da172-137">Zkopírujte definice pracovní doby od pondělí do pátku.</span><span class="sxs-lookup"><span data-stu-id="da172-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="da172-138">Vyberte volbu v poli Do pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="da172-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="da172-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="da172-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="da172-140">Definování časových úseků pro zvláštní operace</span><span class="sxs-lookup"><span data-stu-id="da172-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="da172-141">Rozbalte sekci Pátek.</span><span class="sxs-lookup"><span data-stu-id="da172-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="da172-142">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="da172-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="da172-143">V poli Vlastnosti zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="da172-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="da172-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="da172-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="da172-145">V poli Vlastnosti zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="da172-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="da172-146">Označení víkendových dnů jako uzavřených pro výdej</span><span class="sxs-lookup"><span data-stu-id="da172-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="da172-147">Rozbalte sekci Sobota.</span><span class="sxs-lookup"><span data-stu-id="da172-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="da172-148">Vyberte možnost Ano v poli Uzavřeno pro výdej.</span><span class="sxs-lookup"><span data-stu-id="da172-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="da172-149">Rozbalte sekci Neděle.</span><span class="sxs-lookup"><span data-stu-id="da172-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="da172-150">Vyberte možnost Ano v poli Uzavřeno pro výdej.</span><span class="sxs-lookup"><span data-stu-id="da172-150">Select Yes in the Closed for pickup field.</span></span>

