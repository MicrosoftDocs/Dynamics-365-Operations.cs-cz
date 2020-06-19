---
title: Přidávání informací do deníku výkonnosti a udělení pochvaly některému z uživatelů
description: Deník výkonnosti obsahuje informace, které se týkají toho, jak jste splnili své cíle nebo jak jste si vedli během období.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2a90a5f746e49e1a5df9910867e8cd35feb1147
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430502"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="ab1e1-103">Přidávání informací do deníku výkonnosti a udělení pochvaly některému z uživatelů</span><span class="sxs-lookup"><span data-stu-id="ab1e1-103">Add to your performance journal and send praise to someone</span></span>

<span data-ttu-id="ab1e1-104">Deník výkonnosti obsahuje informace, které se týkají toho, jak jste splnili své cíle nebo jak jste si vedli během období.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="ab1e1-105">Můžete také ocenit akce kolegy z deníku.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="ab1e1-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ab1e1-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="ab1e1-108">Přejděte na Všechny pracovní prostory > Samoobsluha pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="ab1e1-109">Klikněte na Deník výkonnosti.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-109">Click Performance journal.</span></span>
3. <span data-ttu-id="ab1e1-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-110">Click New.</span></span>
4. <span data-ttu-id="ab1e1-111">Zadejte hodnotu do pole Titul.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="ab1e1-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ab1e1-113">Datum deníku výkonnosti je datum, kdy byl deník vytvořen.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="ab1e1-114">Zdroj označuje zdroj, odkud deník výkonnosti pochází.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="ab1e1-115">Když ho vytvoříte, pochází z okna Můj deník.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="ab1e1-116">Když ho vytvoří manažer, pochází z deníku manažera.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="ab1e1-117">Tento deník můžete sdílet s manažerem nebo ho nastavit jako viditelný pouze pro sebe.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="ab1e1-118">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="ab1e1-119">Do pole Datum dokončení zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="ab1e1-120">Vyberte možnost Ano v poli Plán rozvoje.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="ab1e1-121">Zadejte hodnotu do pole Klíčová slova.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="ab1e1-122">Klikněte na Přidat externí odkaz.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-122">Click Add external link.</span></span>
11. <span data-ttu-id="ab1e1-123">Do pole popis napište 'Envision'.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="ab1e1-124">Do pole Internetová adresa zadejte "https://www.microsoft.com/en/envision/default'.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="ab1e1-125">Klepněte na titulek pod tlačítkem Uložit nazvaný "Deník výkonnosti" pro návrat do mřížky.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="ab1e1-126">Vybraný deník nebo deníky můžete přidat k cíli tak, aby se zobrazil při otevření cíle.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="ab1e1-127">Odkaz bude přidán na pevné záložce Odkazy.   Pokud přidáte deník do cíle a potom přidáte cíl do kontroly, deník se v kontrole zobrazí automaticky.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="ab1e1-128">Vybraný deník nebo deníky můžete přidat ke kontrole tak, aby se zobrazil při otevření kontroly.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="ab1e1-129">Odkaz bude přidán na pevné záložce Odkazy.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="ab1e1-130">Klikněte na Přidat rychlý odkaz.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-130">Click Quick add.</span></span>
15. <span data-ttu-id="ab1e1-131">Zadejte hodnotu do pole Titul.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="ab1e1-132">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="ab1e1-133">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-133">Click Save.</span></span>
18. <span data-ttu-id="ab1e1-134">Klikněte na Udělit pochvalu pro.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-134">Click Send praise.</span></span>
19. <span data-ttu-id="ab1e1-135">Vyberte některého zaměstnance ze seznamu zaměstnanců společnosti.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="ab1e1-136">Do pole Popis zadejte "Děkujeme za veškerou podporu na konferenci!".</span><span class="sxs-lookup"><span data-stu-id="ab1e1-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="ab1e1-137">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="ab1e1-137">Click Send.</span></span>

