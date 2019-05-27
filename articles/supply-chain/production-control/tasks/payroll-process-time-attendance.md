---
title: Povolení procesu mezd pro čas a docházku
description: Tento postup popisuje, jak povolit mzdový proces pro čas a docházku.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0174f438396d814d153befe4a59a79b6eebb2288
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560176"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="b673f-103">Povolení procesu mezd pro čas a docházku</span><span class="sxs-lookup"><span data-stu-id="b673f-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b673f-104">Tento postup popisuje, jak povolit mzdový proces pro čas a docházku.</span><span class="sxs-lookup"><span data-stu-id="b673f-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="b673f-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="b673f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="b673f-106">Vytvoření typu mzdy podle související mzdové sazby</span><span class="sxs-lookup"><span data-stu-id="b673f-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="b673f-107">Čas a docházka > Nastavení > Platba > Typy mezd</span><span class="sxs-lookup"><span data-stu-id="b673f-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="b673f-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b673f-108">Click New.</span></span>
3. <span data-ttu-id="b673f-109">Zadejte hodnotu do pole Typ mzdy.</span><span class="sxs-lookup"><span data-stu-id="b673f-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="b673f-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b673f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b673f-111">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b673f-111">Click Save.</span></span>
6. <span data-ttu-id="b673f-112">Klepněte na tlačítko Sazby.</span><span class="sxs-lookup"><span data-stu-id="b673f-112">Click Rates.</span></span>
    * <span data-ttu-id="b673f-113">Sazby typů mezd se nastavují pro příslušné časové intervaly a jednotlivé sazby lze vytvořit zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="b673f-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="b673f-114">Není vždy nutné, abyste sazby vytvářeli pro typy mezd podle času a docházky.</span><span class="sxs-lookup"><span data-stu-id="b673f-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="b673f-115">Tato informace může již existovat v systému mezd, který slouží ke generování mezd.</span><span class="sxs-lookup"><span data-stu-id="b673f-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="b673f-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b673f-116">Click New.</span></span>
8. <span data-ttu-id="b673f-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b673f-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b673f-118">Do pole Sazba zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b673f-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="b673f-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b673f-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="b673f-120">Vytvoření mzdové smlouvy</span><span class="sxs-lookup"><span data-stu-id="b673f-120">Create a pay agreement</span></span>
1. <span data-ttu-id="b673f-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b673f-121">Close the page.</span></span>
2. <span data-ttu-id="b673f-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b673f-122">Close the page.</span></span>
3. <span data-ttu-id="b673f-123">Přejděte na Platební smlouvy.</span><span class="sxs-lookup"><span data-stu-id="b673f-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="b673f-124">Čas a docházka > Nastavení > Platební smlouvy</span><span class="sxs-lookup"><span data-stu-id="b673f-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="b673f-125">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b673f-125">Click New.</span></span>
5. <span data-ttu-id="b673f-126">Zadejte hodnotu do pole Platební smlouva.</span><span class="sxs-lookup"><span data-stu-id="b673f-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="b673f-127">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b673f-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="b673f-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b673f-128">Click Save.</span></span>
8. <span data-ttu-id="b673f-129">Klikněte na Řádky smlouvy.</span><span class="sxs-lookup"><span data-stu-id="b673f-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="b673f-130">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b673f-130">Click New.</span></span>
10. <span data-ttu-id="b673f-131">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b673f-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b673f-132">V poli Typ profilu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b673f-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="b673f-133">V poli Typ mzdy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b673f-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="b673f-134">Nastavení platební dohody pro čas a registraci pracovníka</span><span class="sxs-lookup"><span data-stu-id="b673f-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="b673f-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b673f-135">Close the page.</span></span>
2. <span data-ttu-id="b673f-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b673f-136">Close the page.</span></span>
3. <span data-ttu-id="b673f-137">Přejděte na Pracovníci registrace času.</span><span class="sxs-lookup"><span data-stu-id="b673f-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="b673f-138">Čas a docházka > Nastavení > Pracovníci registrace času</span><span class="sxs-lookup"><span data-stu-id="b673f-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="b673f-139">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b673f-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b673f-140">Klikněte na kartu Zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="b673f-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="b673f-141">Rozbalte položku Časová registrace.</span><span class="sxs-lookup"><span data-stu-id="b673f-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="b673f-142">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="b673f-142">Click Edit.</span></span>
8. <span data-ttu-id="b673f-143">V poli Platební smlouva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b673f-143">In the Pay agreement field, enter or select a value.</span></span>

