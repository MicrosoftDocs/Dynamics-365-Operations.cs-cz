---
title: Konfigurace fakturování mezipodnikového projektu
description: Toto téma popisuje nastavení fakturace projektu mezi dvěma společnostmi v rámci organizace.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867312"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="a6f29-103">Konfigurace fakturování mezipodnikového projektu</span><span class="sxs-lookup"><span data-stu-id="a6f29-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a6f29-104">Toto téma popisuje nastavení fakturace projektu mezi dvěma společnostmi v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="a6f29-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="a6f29-105">Tato úloha používá sadu dat USSI.</span><span class="sxs-lookup"><span data-stu-id="a6f29-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="a6f29-106">V navigačním podokně přejděte na **Moduly > Závazky > Dodavatelé > Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="a6f29-107">V seznamu **Všichni dodavatelé** vyhledejte a vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="a6f29-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="a6f29-108">V podokně akcí klikněte na možnost **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="a6f29-109">Vyberte **Mezipodnikový**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="a6f29-110">Nastavte položku **Aktivní** na hodnotu **Ano**, chcete-li povolit mezipodnikové obchodování.</span><span class="sxs-lookup"><span data-stu-id="a6f29-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="a6f29-111">V poli **Společnost odběratele** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6f29-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="a6f29-112">V poli **Můj účet** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6f29-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="a6f29-113">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-113">Select **Save**.</span></span>
9. <span data-ttu-id="a6f29-114">Zavřete stránky a vraťte se na domovskou stránku.</span><span class="sxs-lookup"><span data-stu-id="a6f29-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="a6f29-115">V navigačním podokně přejděte na **Moduly > Řízení a účetnictví projektů > Nastavení > Parametry modulu Řízení a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="a6f29-116">Vyberte kartu **Mezipodnikové**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="a6f29-117">Posuňte posuvník na **Ano**, abyste povolili mezipodnikové plánování prostředků a časové rozvrhy.</span><span class="sxs-lookup"><span data-stu-id="a6f29-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="a6f29-118">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="a6f29-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="a6f29-119">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-119">Select **New**.</span></span>
15. <span data-ttu-id="a6f29-120">V poli **Právnická osoba, která si půjčuje**, zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6f29-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="a6f29-121">Zaškrtněte pole **Časově rozlišené výnosy**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="a6f29-122">V poli **Výchozí kategorie časového rozvrhu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6f29-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="a6f29-123">V poli **Výchozí kategorie výdajů** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6f29-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="a6f29-124">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-124">Select **Save**.</span></span>
20. <span data-ttu-id="a6f29-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a6f29-125">Close the page.</span></span>
21. <span data-ttu-id="a6f29-126">V navigačním podokně přejděte na **Moduly > Řízení a účetnictví projektů > Nastavení > Zaúčtování > Nastavení účtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="a6f29-127">V poli **Typy účtů hlavní knihy** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="a6f29-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="a6f29-128">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-128">Select **New**.</span></span>
24. <span data-ttu-id="a6f29-129">Zadejte požadované hodnoty do pole nového řádku **Hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="a6f29-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-130">Select **Save**.</span></span>
26. <span data-ttu-id="a6f29-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a6f29-131">Close the page.</span></span>
27. <span data-ttu-id="a6f29-132">V navigačním podokně přejděte na **Moduly > Řízení a účetnictví projektů > Nastavení > Ceny > Převést cenu**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="a6f29-133">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-133">Select **New**.</span></span>
29. <span data-ttu-id="a6f29-134">Zadejte datum do pole **Datum platnosti**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="a6f29-135">V poli **Právnická osoba, která si půjčuje**, zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6f29-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="a6f29-136">V poli **Model přenosu ceny** zvolte možnost.</span><span class="sxs-lookup"><span data-stu-id="a6f29-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="a6f29-137">Do pole **Oceňování** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="a6f29-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="a6f29-138">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a6f29-138">Select **Save**.</span></span>

