---
title: Účtování periodických deníků
description: Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém získání periodického deníku.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deae523d922e1d6a4f7bb05433e9b1568c9c1ee9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562223"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="e0a97-103">Účtování periodických deníků</span><span class="sxs-lookup"><span data-stu-id="e0a97-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0a97-104">Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém získání periodického deníku.</span><span class="sxs-lookup"><span data-stu-id="e0a97-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="e0a97-105">Při vytváření periodického deníku zadáte interval pro opakování, například dny nebo měsíce.</span><span class="sxs-lookup"><span data-stu-id="e0a97-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="e0a97-106">Tento průvodce úkolem vytvoří periodický deník s měsíčním opakováním.</span><span class="sxs-lookup"><span data-stu-id="e0a97-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="e0a97-107">Přejděte do hlavní knihy > Periodické úkoly > Periodické deníky.</span><span class="sxs-lookup"><span data-stu-id="e0a97-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="e0a97-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0a97-108">Click New.</span></span>
3. <span data-ttu-id="e0a97-109">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e0a97-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="e0a97-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0a97-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e0a97-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e0a97-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e0a97-112">Popis bude představovat název periodického deníku při jeho pozdějším použití, takže nezapomeňte použít vhodný název.</span><span class="sxs-lookup"><span data-stu-id="e0a97-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="e0a97-113">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="e0a97-113">Click Lines.</span></span>
    * <span data-ttu-id="e0a97-114">Periodický deník obvykle zahrnuje několik řádků deníku.</span><span class="sxs-lookup"><span data-stu-id="e0a97-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="e0a97-115">Tento průvodce úkolem však přidá pouze jeden řádek.</span><span class="sxs-lookup"><span data-stu-id="e0a97-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="e0a97-116">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="e0a97-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="e0a97-117">Pole Datum obsahuje datum zaúčtování pro následující přenos do denního deníku.</span><span class="sxs-lookup"><span data-stu-id="e0a97-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="e0a97-118">Pro deníky, které budou načteny každý měsíc, je doporučeno použít datum v měsíci odpovídající jeho zaúčtování - typicky první nebo poslední den daného období.</span><span class="sxs-lookup"><span data-stu-id="e0a97-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="e0a97-119">Je možné ponechat pole Datum prázdné a datum doplnit, až je deník načten (pomocí pole Prázdné datum).</span><span class="sxs-lookup"><span data-stu-id="e0a97-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="e0a97-120">Pole je automaticky aktualizováno na další opakující se datum, kdy jsou načteny transakce.</span><span class="sxs-lookup"><span data-stu-id="e0a97-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="e0a97-121">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="e0a97-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="e0a97-122">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e0a97-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="e0a97-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0a97-123">Close the page.</span></span>
11. <span data-ttu-id="e0a97-124">Do pole Má dáti zadejte čísl.</span><span class="sxs-lookup"><span data-stu-id="e0a97-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="e0a97-125">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="e0a97-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="e0a97-126">V poli Jednotka pak vyberte možnost Měsíce.</span><span class="sxs-lookup"><span data-stu-id="e0a97-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="e0a97-127">Do pole Počet jednotek zadejte „1“.</span><span class="sxs-lookup"><span data-stu-id="e0a97-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="e0a97-128">V poli Poslední datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="e0a97-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="e0a97-129">Zadání koncového data do předchozího období zabrání nechtěnému vytvoření periodického deníku v nesprávném počátečním období.</span><span class="sxs-lookup"><span data-stu-id="e0a97-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="e0a97-130">Poslední datum bude později aktualizováno pokaždé, když je načten periodický deník.</span><span class="sxs-lookup"><span data-stu-id="e0a97-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="e0a97-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e0a97-131">Click Save.</span></span>
17. <span data-ttu-id="e0a97-132">Přejděte na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="e0a97-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="e0a97-133">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="e0a97-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="e0a97-134">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0a97-134">Click New.</span></span>
20. <span data-ttu-id="e0a97-135">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e0a97-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="e0a97-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0a97-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="e0a97-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0a97-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="e0a97-138">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e0a97-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="e0a97-139">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="e0a97-139">Click Lines.</span></span>
25. <span data-ttu-id="e0a97-140">Klikněte na Periodický deník.</span><span class="sxs-lookup"><span data-stu-id="e0a97-140">Click Period journal.</span></span>
26. <span data-ttu-id="e0a97-141">Klikněte na Načíst deník.</span><span class="sxs-lookup"><span data-stu-id="e0a97-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="e0a97-142">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="e0a97-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e0a97-143">Koncové datum slouží jako datum přerušení pro periodické řádky dokladu.</span><span class="sxs-lookup"><span data-stu-id="e0a97-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="e0a97-144">Na základě nastavení opakování může stejný řádek Koncové datum a Do data být zahrnut vícekrát ve výsledném deníku.</span><span class="sxs-lookup"><span data-stu-id="e0a97-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="e0a97-145">Do data je automaticky aktualizováno na základě data relace – poslední datum, kdy byl řádek přenesen do deníku.</span><span class="sxs-lookup"><span data-stu-id="e0a97-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="e0a97-146">V poli Číslo periodického deníku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e0a97-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="e0a97-147">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0a97-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="e0a97-148">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e0a97-148">Click OK.</span></span>
    * <span data-ttu-id="e0a97-149">Periodický deník lze nyní zkontrolovat, schválit nebo zaúčtovat v závislosti na požadavcích a nastavení.</span><span class="sxs-lookup"><span data-stu-id="e0a97-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  

