---
title: Nastavení profilu přehledu doručení zboží
description: Toto téma je zaměřeno na nastavení profilu přehledu doručení.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55512c75445a5f3b9c1521376a20d48dd60e22c6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145518"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="91153-103">Nastavení profilu přehledu doručení zboží</span><span class="sxs-lookup"><span data-stu-id="91153-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="91153-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="91153-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="91153-105">Toto téma je zaměřeno na nastavení profilu přehledu doručení.</span><span class="sxs-lookup"><span data-stu-id="91153-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="91153-106">Profil přehledu doručení je kolekce pravidel, která budou použita při otevření stránky přehledu doručení uživatelem.</span><span class="sxs-lookup"><span data-stu-id="91153-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="91153-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="91153-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="91153-108">Tento proces obvykle provádí přijímající pracovník.</span><span class="sxs-lookup"><span data-stu-id="91153-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="91153-109">V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Distribuce > Profily přehledu doručení**.</span><span class="sxs-lookup"><span data-stu-id="91153-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="91153-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="91153-110">Select **New**.</span></span> <span data-ttu-id="91153-111">Vzhledem k tomu, že budete téměř vždy pracovat ve stejném skladu s vykládkou úplných vytížení, pro zjednodušení procesu registrace přijatého zboží byste měli vytvořit profil přehledu doručení.</span><span class="sxs-lookup"><span data-stu-id="91153-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="91153-112">Do pole **Profil přehledu doručení** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="91153-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="91153-113">Vyberte možnost v poli **Zobrazit řádky**.</span><span class="sxs-lookup"><span data-stu-id="91153-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="91153-114">Výběr řádků zobrazených pro příjmy:</span><span class="sxs-lookup"><span data-stu-id="91153-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="91153-115">**Vše** – Zobrazení všech řádků bez ohledu na stav.</span><span class="sxs-lookup"><span data-stu-id="91153-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="91153-116">**Probíhá** – Zobrazí řádky pro příjmy s průběhem Dokončeno nebo Částečné.</span><span class="sxs-lookup"><span data-stu-id="91153-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="91153-117">To znamená, že pro každý řádek bylo v deníku doručení zaregistrováno buď úplné množství, nebo jeho část.</span><span class="sxs-lookup"><span data-stu-id="91153-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="91153-118">**Nedokončené** – Zobrazí řádky pro příjmy s průběhem Žádné nebo Částečné.</span><span class="sxs-lookup"><span data-stu-id="91153-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="91153-119">To znamená, že pro každý řádek nebylo v deníku doručení zaregistrováno nic nebo byla zaregistrována jen část.</span><span class="sxs-lookup"><span data-stu-id="91153-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="91153-120">Rozbalte nebo sbalte oddíl **Možnosti doručení**.</span><span class="sxs-lookup"><span data-stu-id="91153-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="91153-121">Zadejte hodnotu do pole **Dny dopředu**.</span><span class="sxs-lookup"><span data-stu-id="91153-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="91153-122">Umožňuje nastavit filtr pro zobrazení řádků příjemky s očekávaným příjmem během několika příštích dní (v závislosti na vámi nastaveném čísle).</span><span class="sxs-lookup"><span data-stu-id="91153-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="91153-123">Zadejte hodnotu do pole **Dny zpětně**.</span><span class="sxs-lookup"><span data-stu-id="91153-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="91153-124">Umožňuje nastavit filtr pro zobrazení řádků příjemky s očekávaným příjmem několik dní před aktuálním datem.</span><span class="sxs-lookup"><span data-stu-id="91153-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="91153-125">Zadejte hodnotu do pole **Sklady**.</span><span class="sxs-lookup"><span data-stu-id="91153-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="91153-126">Filtrujte pomocí jednoho nebo více skladů.</span><span class="sxs-lookup"><span data-stu-id="91153-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="91153-127">Vyberte hodnotu v poli **Způsob dodání**.</span><span class="sxs-lookup"><span data-stu-id="91153-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="91153-128">Umožňuje nastavit filtr, aby se zobrazovaly pouze řádky příjemky s tímto způsobem dodání.</span><span class="sxs-lookup"><span data-stu-id="91153-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="91153-129">V poli **Název** vyberte WHS.</span><span class="sxs-lookup"><span data-stu-id="91153-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="91153-130">V poli **Sklad** vyberte sklad 24.</span><span class="sxs-lookup"><span data-stu-id="91153-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="91153-131">Toto je výchozí sklad, který bude použit pro registrované řádky příjemky, které používají tento profil.</span><span class="sxs-lookup"><span data-stu-id="91153-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="91153-132">V poli **Místo** vyberte **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="91153-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="91153-133">Toto je výchozí umístění, které bude použito pro registrované řádky příjemky, které používají tento profil.</span><span class="sxs-lookup"><span data-stu-id="91153-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="91153-134">Rozbalte nebo sbalte oddíl **Podrobnosti dotazu k doručení**.</span><span class="sxs-lookup"><span data-stu-id="91153-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="91153-135">V poli **Omezit na pracoviště** vyberte pracoviště 2.</span><span class="sxs-lookup"><span data-stu-id="91153-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="91153-136">Umožňuje nastavit filtr, aby se zobrazovaly pouze řádky příjemky s tímto sitem.</span><span class="sxs-lookup"><span data-stu-id="91153-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="91153-137">Nastavte možnost **Nákupní objednávky** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="91153-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="91153-138">Vyberte řádky příjemky z nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="91153-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="91153-139">Nastavte možnost **Převodní příkazy** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="91153-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="91153-140">Vyberte řádky příjemky z převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="91153-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="91153-141">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="91153-141">Select **Save**.</span></span>
18. <span data-ttu-id="91153-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="91153-142">Close the page.</span></span>

