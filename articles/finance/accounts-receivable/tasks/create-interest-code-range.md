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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b98436d6e0c40f0458dc4744b8b1d96baa8b54
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216562"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="1fc26-103">Vytvoření kódu úroků s rozsahem</span><span class="sxs-lookup"><span data-stu-id="1fc26-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="1fc26-104">Kódy úroků lze nastavit pro výpočet různých částek úroků podle rozsahu hodnot.</span><span class="sxs-lookup"><span data-stu-id="1fc26-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="1fc26-105">Tato procedura vám ukáže, jak přidáte kód úroků a jak k němu přidáte rozsah.</span><span class="sxs-lookup"><span data-stu-id="1fc26-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="1fc26-106">Přejděte do nabídky Úvěry a inkasa > Úrok > Nastavení kódů úroku.</span><span class="sxs-lookup"><span data-stu-id="1fc26-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="1fc26-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1fc26-107">Click New.</span></span>
3. <span data-ttu-id="1fc26-108">V poli Kód úroku zadejte název kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="1fc26-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="1fc26-109">Do pole Popis zadejte popis kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="1fc26-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="1fc26-110">Vyberte měsíc.</span><span class="sxs-lookup"><span data-stu-id="1fc26-110">Select Month.</span></span>
6. <span data-ttu-id="1fc26-111">Rozbalte část Zisky.</span><span class="sxs-lookup"><span data-stu-id="1fc26-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="1fc26-112">Rozbalte část Zisky podle měny.</span><span class="sxs-lookup"><span data-stu-id="1fc26-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="1fc26-113">Zadejte požadované hodnoty do pole Účet pro zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="1fc26-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="1fc26-114">Vyberte možnost „Měsíce“ v poli Úrok podle rozsahu.</span><span class="sxs-lookup"><span data-stu-id="1fc26-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="1fc26-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="1fc26-115">Click Add.</span></span>
11. <span data-ttu-id="1fc26-116">Do pole Popis zadejte popis pro tuto měnu a rozsah.</span><span class="sxs-lookup"><span data-stu-id="1fc26-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="1fc26-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1fc26-117">Click Save.</span></span>
13. <span data-ttu-id="1fc26-118">Klikněte na Rozsahy.</span><span class="sxs-lookup"><span data-stu-id="1fc26-118">Click Ranges.</span></span>
14. <span data-ttu-id="1fc26-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1fc26-119">Click New.</span></span>
15. <span data-ttu-id="1fc26-120">Zadejte možnost 0 pro pole Od hodnoty a poté zadejte procento úroku za měsíc, který se použije pro výpočet úroků.</span><span class="sxs-lookup"><span data-stu-id="1fc26-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="1fc26-121">V našem příkladu to je 1,5.</span><span class="sxs-lookup"><span data-stu-id="1fc26-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="1fc26-122">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="1fc26-122">Click New.</span></span>
17. <span data-ttu-id="1fc26-123">Do dalšího pole Hodnota od zadejte možnost 4, což je první měsíc, kdy budete počítat novou částku úroku.</span><span class="sxs-lookup"><span data-stu-id="1fc26-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="1fc26-124">Zadejte procento měsíčního úroku, který se použije pro výpočet úroku počínaje 4. měsícem.</span><span class="sxs-lookup"><span data-stu-id="1fc26-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="1fc26-125">V tomto příkladu to je 2.</span><span class="sxs-lookup"><span data-stu-id="1fc26-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="1fc26-126">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="1fc26-126">Click New.</span></span>
20. <span data-ttu-id="1fc26-127">Do dalšího pole Hodnota od zadejte možnost 7, což je další měsíc, kdy budete počítat novou částku úroku.</span><span class="sxs-lookup"><span data-stu-id="1fc26-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="1fc26-128">Zadejte procento měsíčního úroku, který se použije pro výpočet úroku počínaje 7. měsícem.</span><span class="sxs-lookup"><span data-stu-id="1fc26-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="1fc26-129">V tomto příkladu to je 2,5.</span><span class="sxs-lookup"><span data-stu-id="1fc26-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="1fc26-130">Chcete-li dokončit nastavení, klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="1fc26-130">Click Close to complete the setup.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]