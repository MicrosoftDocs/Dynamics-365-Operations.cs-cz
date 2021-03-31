---
title: Nastavení knih odpisů
description: Tento postup prochází procesem vytvoření nové knihy odpisů a jejím přidružením ke skupině dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd65cb77872b3e2f74402cf8c92c8b8989cea6ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224686"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="65f4e-103">Nastavení knih odpisů</span><span class="sxs-lookup"><span data-stu-id="65f4e-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65f4e-104">Tento postup prochází procesem vytvoření nové knihy odpisů a jejím přidružením ke skupině dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="65f4e-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="65f4e-105">Vytvoření knihy odpisů</span><span class="sxs-lookup"><span data-stu-id="65f4e-105">Create a depreciation book</span></span>
1. <span data-ttu-id="65f4e-106">Přejděte do části Dlouhodobý majetek > Nastavení > Knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="65f4e-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="65f4e-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="65f4e-107">Click New.</span></span>
3. <span data-ttu-id="65f4e-108">Zadejte hodnotu do pole Kniha odpisů.</span><span class="sxs-lookup"><span data-stu-id="65f4e-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="65f4e-109">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="65f4e-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="65f4e-110">Zaškrtněte nebo zrušte zaškrtnutí políčka Vypočítat odpis.</span><span class="sxs-lookup"><span data-stu-id="65f4e-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="65f4e-111">V poli Odpisový plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="65f4e-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="65f4e-112">Vyhledejte na seznamu požadovaný odpisový plán a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="65f4e-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="65f4e-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="65f4e-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="65f4e-114">V poli Alternativní odpisový plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="65f4e-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="65f4e-115">V seznamu vyberte požadovaný odpisový plán.</span><span class="sxs-lookup"><span data-stu-id="65f4e-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="65f4e-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="65f4e-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="65f4e-117">Plán mimořádných odpisů se používá pro dodatečný odpis majetku při neobvyklých okolností.</span><span class="sxs-lookup"><span data-stu-id="65f4e-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="65f4e-118">Například to můžete použít k záznamu odpisů, které je výsledkem živelné pohromy.</span><span class="sxs-lookup"><span data-stu-id="65f4e-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="65f4e-119">Zaškrtněte nebo zrušte zaškrtnutí políčka Vytvořit úpravy odpisů s úpravami základu.</span><span class="sxs-lookup"><span data-stu-id="65f4e-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="65f4e-120">V poli Kalendář kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="65f4e-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="65f4e-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="65f4e-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="65f4e-122">Přiřazení knihy odpisů ke skupině dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="65f4e-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="65f4e-123">Klikněte na Skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="65f4e-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="65f4e-124">V poli Skupina dlouhodobého majetku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="65f4e-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="65f4e-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="65f4e-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="65f4e-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="65f4e-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="65f4e-127">Vyberte volbu v poli Způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="65f4e-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="65f4e-128">Zadejte číslo do pole Doba životnosti.</span><span class="sxs-lookup"><span data-stu-id="65f4e-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="65f4e-129">Všimněte si, že hodnota pole Období odpisu se vypočítá po nastavení doby životnosti.</span><span class="sxs-lookup"><span data-stu-id="65f4e-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]