---
title: Vytvoření kódu úroků s rozsahem
description: Kódy úroků lze nastavit pro výpočet různých částek úroků podle rozsahu hodnot.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d76ae320ee43a473b64afe311876cc94b953b20
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546563"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="e0e1b-103">Vytvoření kódu úroků s rozsahem</span><span class="sxs-lookup"><span data-stu-id="e0e1b-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0e1b-104">Kódy úroků lze nastavit pro výpočet různých částek úroků podle rozsahu hodnot.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="e0e1b-105">Tato procedura vám ukáže, jak přidáte kód úroků a jak k němu přidáte rozsah.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="e0e1b-106">Přejděte do nabídky Úvěry a inkasa > Úrok > Nastavení kódů úroku.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="e0e1b-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-107">Click New.</span></span>
3. <span data-ttu-id="e0e1b-108">V poli Kód úroku zadejte název kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="e0e1b-109">Do pole Popis zadejte popis kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="e0e1b-110">Vyberte měsíc.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-110">Select Month.</span></span>
6. <span data-ttu-id="e0e1b-111">Rozbalte část Zisky.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="e0e1b-112">Rozbalte část Zisky podle měny.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="e0e1b-113">Zadejte požadované hodnoty do pole Účet pro zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="e0e1b-114">Vyberte možnost „Měsíce“ v poli Úrok podle rozsahu.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="e0e1b-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-115">Click Add.</span></span>
11. <span data-ttu-id="e0e1b-116">Do pole Popis zadejte popis pro tuto měnu a rozsah.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="e0e1b-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-117">Click Save.</span></span>
13. <span data-ttu-id="e0e1b-118">Klikněte na Rozsahy.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-118">Click Ranges.</span></span>
14. <span data-ttu-id="e0e1b-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-119">Click New.</span></span>
15. <span data-ttu-id="e0e1b-120">Zadejte možnost 0 pro pole Od hodnoty a poté zadejte procento úroku za měsíc, který se použije pro výpočet úroků.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="e0e1b-121">V našem příkladu to je 1,5.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="e0e1b-122">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-122">Click New.</span></span>
17. <span data-ttu-id="e0e1b-123">Do dalšího pole Hodnota od zadejte možnost 4, což je první měsíc, kdy budete počítat novou částku úroku.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="e0e1b-124">Zadejte procento měsíčního úroku, který se použije pro výpočet úroku počínaje 4. měsícem.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="e0e1b-125">V tomto příkladu to je 2.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="e0e1b-126">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-126">Click New.</span></span>
20. <span data-ttu-id="e0e1b-127">Do dalšího pole Hodnota od zadejte možnost 7, což je další měsíc, kdy budete počítat novou částku úroku.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="e0e1b-128">Zadejte procento měsíčního úroku, který se použije pro výpočet úroku počínaje 7. měsícem.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="e0e1b-129">V tomto příkladu to je 2,5.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="e0e1b-130">Chcete-li dokončit nastavení, klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="e0e1b-130">Click Close to complete the setup.</span></span>

