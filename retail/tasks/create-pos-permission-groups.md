--- 
title: " Vytváření skupin oprávnění POS"
description: "Tato procedura vysvětlí, jak vytvořit skupiny oprávnění POS."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e924dc59c3e4cb9b6979014852512453dd3d70db
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="38296-103"> Vytváření skupin oprávnění POS</span><span class="sxs-lookup"><span data-stu-id="38296-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="38296-104">Tato procedura vysvětlí, jak vytvořit skupiny oprávnění POS.</span><span class="sxs-lookup"><span data-stu-id="38296-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="38296-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="38296-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="38296-106">Tento úkol je určen pro roli Manažer maloobchodních operací.</span><span class="sxs-lookup"><span data-stu-id="38296-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="38296-107">Přejděte na Skupiny oprávnění.</span><span class="sxs-lookup"><span data-stu-id="38296-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="38296-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="38296-108">Click New.</span></span>
3. <span data-ttu-id="38296-109">Zadejte hodnotu do pole ID skupiny oprávnění POS.</span><span class="sxs-lookup"><span data-stu-id="38296-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="38296-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="38296-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38296-111">Vyberte možnost Ano v poli Zobrazit časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="38296-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="38296-112">Nyní můžete povolit nebo zakázat různá oprávnění pro skupinu oprávnění POS.</span><span class="sxs-lookup"><span data-stu-id="38296-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="38296-113">U některých oprávnění můžete nastavit hodnotu, která se použije k vyhodnocení, zda může uživatel POS provést akci.</span><span class="sxs-lookup"><span data-stu-id="38296-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="38296-114">Tento průvodce úkolem povolí několik oprávnění, která můžete udělit pokladníkovi.</span><span class="sxs-lookup"><span data-stu-id="38296-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="38296-115">Vyberte možnost Ano v poli Povolit vytvoření objednávky.</span><span class="sxs-lookup"><span data-stu-id="38296-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="38296-116">Vyberte možnost Ano v poli Povolit úpravu objednávky.</span><span class="sxs-lookup"><span data-stu-id="38296-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="38296-117">Vyberte možnost Ano v poli Povolit načtení objednávky.</span><span class="sxs-lookup"><span data-stu-id="38296-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="38296-118">Vyberte možnost Ano v poli Povolit změnu hesla.</span><span class="sxs-lookup"><span data-stu-id="38296-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="38296-119">Vyberte možnost Ano v poli Povolit uzavření bez zadání částky.</span><span class="sxs-lookup"><span data-stu-id="38296-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="38296-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="38296-120">Click Save.</span></span>
    * <span data-ttu-id="38296-121">Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v maloobchodní síti.</span><span class="sxs-lookup"><span data-stu-id="38296-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="38296-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="38296-122">Close the page.</span></span>
13. <span data-ttu-id="38296-123">Přejděte na položku Úlohy.</span><span class="sxs-lookup"><span data-stu-id="38296-123">Go to Jobs.</span></span>
    * <span data-ttu-id="38296-124">Dále přiřadíme skupinu oprávnění POS úloze.</span><span class="sxs-lookup"><span data-stu-id="38296-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="38296-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="38296-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="38296-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="38296-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="38296-127">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="38296-127">Click Edit.</span></span>
17. <span data-ttu-id="38296-128">Rozbalte část Klasifikace úlohy.</span><span class="sxs-lookup"><span data-stu-id="38296-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="38296-129">V poli Skupina oprávnění POS zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="38296-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="38296-130">Pozice všech pracovníků pro tuto úlohu budou používat toto nastavení skupiny oprávnění POS, pokud oprávnění POS pracovníků nebylo přepsáno na úrovni jejich pozice.</span><span class="sxs-lookup"><span data-stu-id="38296-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="38296-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="38296-131">Click Save.</span></span>
    * <span data-ttu-id="38296-132">Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v maloobchodní síti.</span><span class="sxs-lookup"><span data-stu-id="38296-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


