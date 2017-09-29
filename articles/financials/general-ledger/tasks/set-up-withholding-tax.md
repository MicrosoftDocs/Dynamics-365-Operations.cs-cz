--- 
title: "Nastavení srážkové daně"
description: "Srážková daň je daň uvalená na dodavatele, která nevytváří transakce prodejní daně."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc4c0745235052cb4145bc7083fef1a88c8bb5c9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="38a03-103">Nastavení srážkové daně</span><span class="sxs-lookup"><span data-stu-id="38a03-103">Set up withholding tax</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38a03-104">Srážková daň je daň uvalená na dodavatele, která nevytváří transakce prodejní daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="38a03-105">Srážková daň vypočtená pro platby dodavatelů je povinná.</span><span class="sxs-lookup"><span data-stu-id="38a03-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="38a03-106">Pro zaúčtování srážkové daně jsou proto platnými účty pouze účty rozvahy nebo závazků.</span><span class="sxs-lookup"><span data-stu-id="38a03-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="38a03-107">Tento průvodce úkolem popisuje, jak nastavit srážkovou daň.</span><span class="sxs-lookup"><span data-stu-id="38a03-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="38a03-108">Přejděte na Daň > Nepřímé daně > Srážková daň > Kódy srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="38a03-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="38a03-109">Click New.</span></span>
3. <span data-ttu-id="38a03-110">V poli Kód srážkové daně zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="38a03-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="38a03-111">Do pole Název srážkové daně zadejte název kódu srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="38a03-112">V poli Hlavní účet vyberte hlavní účet pro zaúčtování povinnosti srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="38a03-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="38a03-113">Click Save.</span></span>
7. <span data-ttu-id="38a03-114">Klepněte na položku Hodnoty.</span><span class="sxs-lookup"><span data-stu-id="38a03-114">Click Values.</span></span>
8. <span data-ttu-id="38a03-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="38a03-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="38a03-116">V poli Hodnota zadejte procento používané pro výpočet srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="38a03-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="38a03-117">Click Save.</span></span>
11. <span data-ttu-id="38a03-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="38a03-118">Close the page.</span></span>
12. <span data-ttu-id="38a03-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="38a03-119">Click Save.</span></span>
13. <span data-ttu-id="38a03-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="38a03-120">Close the page.</span></span>
14. <span data-ttu-id="38a03-121">Přejděte na Daň > Nepřímé daně > Srážková daň > Skupiny srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="38a03-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="38a03-122">Click New.</span></span>
16. <span data-ttu-id="38a03-123">Do pole Skupina srážkové daně zadejte identifikátor skupiny srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="38a03-124">Do pole Popis zadejte název skupiny srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="38a03-125">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="38a03-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="38a03-126">V poli Kód srážkové daně vyberte kód srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="38a03-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="38a03-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="38a03-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="38a03-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="38a03-128">Click Save.</span></span>


