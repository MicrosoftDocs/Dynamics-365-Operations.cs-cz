---
title: Vytvoření šablon pracovní doby
description: Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920921"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="c898a-103">Vytvoření šablon pracovní doby</span><span class="sxs-lookup"><span data-stu-id="c898a-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c898a-104">Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek.</span><span class="sxs-lookup"><span data-stu-id="c898a-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="c898a-105">Tento postup popisuje, jak definovat šablony pracovní doby pomocí vlastností plánování pracovní doby pro zařazení časových intervalů práce.</span><span class="sxs-lookup"><span data-stu-id="c898a-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="c898a-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="c898a-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="c898a-107">Přejděte na **Pracovní prostory > Správa životního cyklu prostředků**.</span><span class="sxs-lookup"><span data-stu-id="c898a-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="c898a-108">Vyberte **Šablon pracovní doby**.</span><span class="sxs-lookup"><span data-stu-id="c898a-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="c898a-109">Vytvoření šablony pracovní doby</span><span class="sxs-lookup"><span data-stu-id="c898a-109">Create working time template</span></span>

1. <span data-ttu-id="c898a-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c898a-110">Select **New**.</span></span>
1. <span data-ttu-id="c898a-111">Zadejte hodnotu do pole **Šablona pracovní doby**.</span><span class="sxs-lookup"><span data-stu-id="c898a-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="c898a-112">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="c898a-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="c898a-113">Rozbalte sekci **Pondělí**.</span><span class="sxs-lookup"><span data-stu-id="c898a-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="c898a-114">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="c898a-114">Select **Add**.</span></span>
1. <span data-ttu-id="c898a-115">Do pole **Od** zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="c898a-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="c898a-116">Určete čas při zahájení práce ráno.</span><span class="sxs-lookup"><span data-stu-id="c898a-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="c898a-117">Do pole **Do** zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="c898a-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="c898a-118">Zadejte čas, kdy zaměstnanci mají přestávku na oběd.</span><span class="sxs-lookup"><span data-stu-id="c898a-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="c898a-119">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="c898a-119">Select **Add**.</span></span>
1. <span data-ttu-id="c898a-120">Do pole **Od** zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="c898a-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="c898a-121">Zadejte čas, kdy práci obnoví po obědě.</span><span class="sxs-lookup"><span data-stu-id="c898a-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="c898a-122">Do pole **Do** zadejte čas.</span><span class="sxs-lookup"><span data-stu-id="c898a-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="c898a-123">Určete konec pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="c898a-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="c898a-124">Replikace pracovní doby pro všechny dny v týdnu</span><span class="sxs-lookup"><span data-stu-id="c898a-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="c898a-125">Vyberte **Kopírovat den**.</span><span class="sxs-lookup"><span data-stu-id="c898a-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="c898a-126">Zkopírujte definice pracovní doby od pondělí do úterý.</span><span class="sxs-lookup"><span data-stu-id="c898a-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="c898a-127">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c898a-127">Select **OK**.</span></span>
1. <span data-ttu-id="c898a-128">Vyberte **Kopírovat den**.</span><span class="sxs-lookup"><span data-stu-id="c898a-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="c898a-129">Zkopírujte definice pracovní doby od pondělí do středa.</span><span class="sxs-lookup"><span data-stu-id="c898a-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="c898a-130">Vyberte volbu v poli **Do pracovního dne**.</span><span class="sxs-lookup"><span data-stu-id="c898a-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="c898a-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c898a-131">Select **OK**.</span></span>
1. <span data-ttu-id="c898a-132">Vyberte **Kopírovat den**.</span><span class="sxs-lookup"><span data-stu-id="c898a-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="c898a-133">Zkopírujte definice pracovní doby od pondělí do čtvrtka.</span><span class="sxs-lookup"><span data-stu-id="c898a-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="c898a-134">Vyberte volbu v poli **Do pracovního dne**.</span><span class="sxs-lookup"><span data-stu-id="c898a-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="c898a-135">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c898a-135">Select **OK**.</span></span>
1. <span data-ttu-id="c898a-136">Vyberte **Kopírovat den**.</span><span class="sxs-lookup"><span data-stu-id="c898a-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="c898a-137">Zkopírujte definice pracovní doby od pondělí do pátku.</span><span class="sxs-lookup"><span data-stu-id="c898a-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="c898a-138">Vyberte volbu v poli **Do pracovního dne**.</span><span class="sxs-lookup"><span data-stu-id="c898a-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="c898a-139">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c898a-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="c898a-140">Definování časových úseků pro zvláštní operace</span><span class="sxs-lookup"><span data-stu-id="c898a-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="c898a-141">Rozbalte sekci **Pátek**.</span><span class="sxs-lookup"><span data-stu-id="c898a-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="c898a-142">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c898a-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="c898a-143">V poli **Vlastnosti** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c898a-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="c898a-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c898a-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="c898a-145">V poli **Vlastnosti** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c898a-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="c898a-146">Označení víkendových dnů jako uzavřených pro výdej</span><span class="sxs-lookup"><span data-stu-id="c898a-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="c898a-147">Rozbalte sekci **Sobota**.</span><span class="sxs-lookup"><span data-stu-id="c898a-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="c898a-148">Vyberte možnost *Ano* v poli **Uzavřeno pro výdej**.</span><span class="sxs-lookup"><span data-stu-id="c898a-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="c898a-149">Rozbalte sekci **Neděle**.</span><span class="sxs-lookup"><span data-stu-id="c898a-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="c898a-150">Vyberte možnost *Ano* v poli **Uzavřeno pro výdej**.</span><span class="sxs-lookup"><span data-stu-id="c898a-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]