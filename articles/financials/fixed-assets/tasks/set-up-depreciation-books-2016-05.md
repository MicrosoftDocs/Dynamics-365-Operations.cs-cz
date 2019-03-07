---
title: Nastavení knih odpisů (květen 2016)
description: Tento průvodce úkolem vytvoří novou knihu odpisů a přiřadí ji ke skupině dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "355557"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="469cd-103">Nastavení knih odpisů (květen 2016)</span><span class="sxs-lookup"><span data-stu-id="469cd-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="469cd-104">Tento průvodce úkolem vytvoří novou knihu odpisů a přiřadí ji ke skupině dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="469cd-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="469cd-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="469cd-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="469cd-106">Vytvoření knihy odpisů</span><span class="sxs-lookup"><span data-stu-id="469cd-106">Create a depreciation book</span></span>
1. <span data-ttu-id="469cd-107">Přejděte do části Dlouhodobý majetek > Nastavení > Knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="469cd-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="469cd-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="469cd-108">Click New.</span></span>
3. <span data-ttu-id="469cd-109">Zadejte hodnotu do pole Kniha odpisů.</span><span class="sxs-lookup"><span data-stu-id="469cd-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="469cd-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="469cd-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="469cd-111">Zaškrtněte nebo zrušte zaškrtnutí políčka Vypočítat odpis.</span><span class="sxs-lookup"><span data-stu-id="469cd-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="469cd-112">V poli Odpisový plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="469cd-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="469cd-113">Vyhledejte na seznamu požadovaný odpisový plán a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="469cd-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="469cd-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="469cd-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="469cd-115">V poli Alternativní odpisový plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="469cd-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="469cd-116">V seznamu vyberte požadovaný odpisový plán.</span><span class="sxs-lookup"><span data-stu-id="469cd-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="469cd-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="469cd-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="469cd-118">Plán mimořádných odpisů se používá pro dodatečný odpis majetku při neobvyklých okolností.</span><span class="sxs-lookup"><span data-stu-id="469cd-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="469cd-119">Například to můžete použít k záznamu odpisů, které je výsledkem živelné pohromy.</span><span class="sxs-lookup"><span data-stu-id="469cd-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="469cd-120">Zaškrtněte nebo zrušte zaškrtnutí políčka Vytvořit úpravy odpisů s úpravami základu.</span><span class="sxs-lookup"><span data-stu-id="469cd-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="469cd-121">V poli Kalendář kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="469cd-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="469cd-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="469cd-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="469cd-123">Přiřazení knihy odpisů ke skupině dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="469cd-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="469cd-124">Klikněte na Skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="469cd-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="469cd-125">V poli Skupina dlouhodobého majetku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="469cd-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="469cd-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="469cd-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="469cd-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="469cd-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="469cd-128">Vyberte volbu v poli Způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="469cd-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="469cd-129">Zadejte číslo do pole Doba životnosti.</span><span class="sxs-lookup"><span data-stu-id="469cd-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="469cd-130">Všimněte si, že hodnota pole Období odpisu se vypočítá po nastavení doby životnosti.</span><span class="sxs-lookup"><span data-stu-id="469cd-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

