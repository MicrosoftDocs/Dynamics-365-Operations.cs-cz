---
title: " Konfigurace zpracování platební karty"
description: Tato procedura vás provede zobrazením seznamu zprostředkovatelů plateb a způsobem konfigurace účtu plateb pro pohledávky.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cfec44bc1c767dff1109c4ecd4e2862443fb1d0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141492"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="a2245-103"> Konfigurace zpracování platební karty</span><span class="sxs-lookup"><span data-stu-id="a2245-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2245-104">Tato procedura vás provede zobrazením seznamu zprostředkovatelů plateb a způsobem konfigurace účtu plateb pro pohledávky.</span><span class="sxs-lookup"><span data-stu-id="a2245-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="a2245-105">Tato procedura používá ukázková data společnosti USRT a je určena pro správce a odborníky v oblasti IT.</span><span class="sxs-lookup"><span data-stu-id="a2245-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="a2245-106">Zobrazení seznamu zprostředkovatelů plateb</span><span class="sxs-lookup"><span data-stu-id="a2245-106">View a list of payment providers</span></span>
1. <span data-ttu-id="a2245-107">Přejděte do nabídky Pohledávky > Nastavení platby > Služby pro platby.</span><span class="sxs-lookup"><span data-stu-id="a2245-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="a2245-108">Klikněte na Zobrazit dostupné poskytovatele.</span><span class="sxs-lookup"><span data-stu-id="a2245-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="a2245-109">Konfigurace účtu platby</span><span class="sxs-lookup"><span data-stu-id="a2245-109">Configure payment account</span></span>
1. <span data-ttu-id="a2245-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a2245-110">Click New.</span></span>
2. <span data-ttu-id="a2245-111">Zadejte hodnotu do pole Služba pro platby.</span><span class="sxs-lookup"><span data-stu-id="a2245-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="a2245-112">Vyberte volbu v poli Konektor platby.</span><span class="sxs-lookup"><span data-stu-id="a2245-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="a2245-113">Přepněte rozšíření části Účet služby pro platby.</span><span class="sxs-lookup"><span data-stu-id="a2245-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="a2245-114">Do pole Prostředí: Zadejte hodnotu „PROD“.</span><span class="sxs-lookup"><span data-stu-id="a2245-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="a2245-115">Klikněte na Typy platebních karet.</span><span class="sxs-lookup"><span data-stu-id="a2245-115">Click Credit card types.</span></span>
7. <span data-ttu-id="a2245-116">V poli Deník plateb kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a2245-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a2245-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a2245-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a2245-118">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a2245-118">Click Add.</span></span>
10. <span data-ttu-id="a2245-119">Zadejte hodnotu do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="a2245-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="a2245-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a2245-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="a2245-121">V poli Deník plateb kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a2245-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="a2245-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a2245-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a2245-123">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a2245-123">Click Add.</span></span>
15. <span data-ttu-id="a2245-124">Zadejte hodnotu do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="a2245-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="a2245-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a2245-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a2245-126">Takto postup lze zopakovat podle potřeby pro všechny typy karet.</span><span class="sxs-lookup"><span data-stu-id="a2245-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="a2245-127">V poli Deník plateb kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a2245-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="a2245-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a2245-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="a2245-129">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a2245-129">Click Add.</span></span>
20. <span data-ttu-id="a2245-130">Zadejte hodnotu do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="a2245-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="a2245-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a2245-131">Click Save.</span></span>
22. <span data-ttu-id="a2245-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a2245-132">Close the page.</span></span>
23. <span data-ttu-id="a2245-133">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="a2245-133">Click Validate.</span></span>
24. <span data-ttu-id="a2245-134">Zaškrtněte políčko Výchozí procesor pro nové platebních karty.</span><span class="sxs-lookup"><span data-stu-id="a2245-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="a2245-135">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a2245-135">Click Save.</span></span>

