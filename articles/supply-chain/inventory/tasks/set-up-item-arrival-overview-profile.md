---
title: Nastavení profilu přehledu doručení zboží
description: Tento úkol je zaměřen na nastavení profilu přehledu doručení.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 20472f76a03a2a7bb1a7a87e2687135bce35dfa1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845435"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="0f094-103">Nastavení profilu přehledu doručení zboží</span><span class="sxs-lookup"><span data-stu-id="0f094-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f094-104">Tento úkol je zaměřen na nastavení profilu přehledu doručení.</span><span class="sxs-lookup"><span data-stu-id="0f094-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="0f094-105">Profil přehledu doručení je kolekce pravidel, která budou použita při otevření stránky přehledu doručení uživatelem.</span><span class="sxs-lookup"><span data-stu-id="0f094-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="0f094-106">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0f094-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="0f094-107">Tento proces obvykle provádí přijímající pracovník.</span><span class="sxs-lookup"><span data-stu-id="0f094-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="0f094-108">Přejděte do nabídky Řízení zásob > Nastavení > Distribuce > Profily přehledu doručení.</span><span class="sxs-lookup"><span data-stu-id="0f094-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="0f094-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0f094-109">Click New.</span></span>
    * <span data-ttu-id="0f094-110">Vzhledem k tomu, že budete téměř vždy pracovat ve stejném skladu s vykládkou úplných vytížení, pro zjednodušení procesu registrace přijatého zboží byste měli vytvořit profil přehledu doručení.</span><span class="sxs-lookup"><span data-stu-id="0f094-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="0f094-111">Do pole Profil přehledu doručení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0f094-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="0f094-112">Vyberte možnost v poli Zobrazit řádky.</span><span class="sxs-lookup"><span data-stu-id="0f094-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="0f094-113">Vyberte řádky, které se mají zobrazit pro příjmy:  Vše – Zobrazení všech řádků bez ohledu na stav.</span><span class="sxs-lookup"><span data-stu-id="0f094-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="0f094-114">Probíhá: Zobrazí řádky pro příjmy s průběhem Dokončeno nebo Částečné.</span><span class="sxs-lookup"><span data-stu-id="0f094-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="0f094-115">To znamená, že pro každý řádek bylo v deníku doručení zaregistrováno buď úplné množství, nebo jeho část.</span><span class="sxs-lookup"><span data-stu-id="0f094-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="0f094-116">Nedokončené: Zobrazí řádky pro příjmy s průběhem Žádné nebo Částečné.</span><span class="sxs-lookup"><span data-stu-id="0f094-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="0f094-117">To znamená, že pro každý řádek nebylo v deníku doručení zaregistrováno nic nebo byla zaregistrována jen část.</span><span class="sxs-lookup"><span data-stu-id="0f094-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="0f094-118">Rozbalte nebo sbalte oddíl Možnosti doručení.</span><span class="sxs-lookup"><span data-stu-id="0f094-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="0f094-119">Zadejte hodnotu do pole Dny dopředu.</span><span class="sxs-lookup"><span data-stu-id="0f094-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="0f094-120">Umožňuje nastavit filtr pro zobrazení řádků příjemky s očekávaným příjmem během několika příštích dní (v závislosti na vámi nastaveném čísle).</span><span class="sxs-lookup"><span data-stu-id="0f094-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="0f094-121">Zadejte hodnotu do pole Dny zpětně.</span><span class="sxs-lookup"><span data-stu-id="0f094-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="0f094-122">Umožňuje nastavit filtr pro zobrazení řádků příjemky s očekávaným příjmem několik dní před aktuálním datem.</span><span class="sxs-lookup"><span data-stu-id="0f094-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="0f094-123">Zadejte hodnotu do pole Sklady.</span><span class="sxs-lookup"><span data-stu-id="0f094-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="0f094-124">Filtrujte pomocí jednoho nebo více skladů.</span><span class="sxs-lookup"><span data-stu-id="0f094-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="0f094-125">Vyberte hodnotu v poli Způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="0f094-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="0f094-126">Umožňuje nastavit filtr, aby se zobrazovaly pouze řádky příjemky s tímto způsobem dodání.</span><span class="sxs-lookup"><span data-stu-id="0f094-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="0f094-127">V poli Název vyberte WHS.</span><span class="sxs-lookup"><span data-stu-id="0f094-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="0f094-128">V poli Sklad vyberte sklad 24.</span><span class="sxs-lookup"><span data-stu-id="0f094-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="0f094-129">Toto je výchozí sklad, který bude použit pro registrované řádky příjemky, které používají tento profil.</span><span class="sxs-lookup"><span data-stu-id="0f094-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="0f094-130">V poli Místo vyberte Baydoor.</span><span class="sxs-lookup"><span data-stu-id="0f094-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="0f094-131">Toto je výchozí umístění, které bude použito pro registrované řádky příjemky, které používají tento profil.</span><span class="sxs-lookup"><span data-stu-id="0f094-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="0f094-132">Rozbalte nebo sbalte oddíl Podrobnosti dotazu k doručení.</span><span class="sxs-lookup"><span data-stu-id="0f094-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="0f094-133">V poli Omezit na pracoviště vyberte pracoviště 2.</span><span class="sxs-lookup"><span data-stu-id="0f094-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="0f094-134">Umožňuje nastavit filtr, aby se zobrazovaly pouze řádky příjemky s tímto sitem.</span><span class="sxs-lookup"><span data-stu-id="0f094-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="0f094-135">Nastavte možnost Nákupní objednávky na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="0f094-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="0f094-136">Vyberte řádky příjemky z nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="0f094-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="0f094-137">Nastavte možnost Převodní příkazy na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="0f094-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="0f094-138">Vyberte řádky příjemky z převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="0f094-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="0f094-139">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0f094-139">Click Save.</span></span>
18. <span data-ttu-id="0f094-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0f094-140">Close the page.</span></span>

