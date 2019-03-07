---
title: Vytvoření atributů dávky pro produkt
description: Tento postup popisuje vytvoření atributu dávky, přiřazení výchozích rozsahů hodnot a zahrnutí atributu do skupiny.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65153dbcfa69046e4f38eb6ffa013bb6fb87ebd8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "330648"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="50c61-103">Vytvoření atributů dávky pro produkt</span><span class="sxs-lookup"><span data-stu-id="50c61-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50c61-104">Tento postup popisuje vytvoření atributu dávky, přiřazení výchozích rozsahů hodnot a zahrnutí atributu do skupiny.</span><span class="sxs-lookup"><span data-stu-id="50c61-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="50c61-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="50c61-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="50c61-106">Přejděte do nabídky Řízení zásob > Nastavení > Dávka > Atributy dávky.</span><span class="sxs-lookup"><span data-stu-id="50c61-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="50c61-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50c61-107">Click New.</span></span>
3. <span data-ttu-id="50c61-108">Zadejte hodnotu do pole Atribut.</span><span class="sxs-lookup"><span data-stu-id="50c61-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="50c61-109">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="50c61-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="50c61-110">V poli Typ atributu vyberte možnost Zlomek.</span><span class="sxs-lookup"><span data-stu-id="50c61-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="50c61-111">Tento postup používá typ Zlomek pro povolení desetinných hodnot.</span><span class="sxs-lookup"><span data-stu-id="50c61-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="50c61-112">Můžete vybrat i jiné typy atributů.</span><span class="sxs-lookup"><span data-stu-id="50c61-112">You can select other attribute types.</span></span> <span data-ttu-id="50c61-113">Pokud jste vybrali typ Výčet, je nutné zadat hodnoty seznamu výčtů a až potom zadat hodnotu do pole Cíl.</span><span class="sxs-lookup"><span data-stu-id="50c61-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="50c61-114">Do pole Minimum zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="50c61-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="50c61-115">Do pole Maximum zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="50c61-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="50c61-116">V poli Přírůstek zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="50c61-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="50c61-117">V poli Cíl zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50c61-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="50c61-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="50c61-118">Click Save.</span></span>
11. <span data-ttu-id="50c61-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50c61-119">Close the page.</span></span>
12. <span data-ttu-id="50c61-120">Přejděte do nabídky Řízení zásob > Nastavení > Dávka > Skupiny atributů dávky.</span><span class="sxs-lookup"><span data-stu-id="50c61-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="50c61-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50c61-121">Click New.</span></span>
14. <span data-ttu-id="50c61-122">Zadejte hodnotu do pole Skupina atributů.</span><span class="sxs-lookup"><span data-stu-id="50c61-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="50c61-123">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="50c61-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="50c61-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="50c61-124">Click Save.</span></span>
17. <span data-ttu-id="50c61-125">Klepněte na možnost Seskupit atributy.</span><span class="sxs-lookup"><span data-stu-id="50c61-125">Click Group attributes.</span></span>
18. <span data-ttu-id="50c61-126">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50c61-126">Click New.</span></span>
19. <span data-ttu-id="50c61-127">V poli Atribut kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="50c61-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="50c61-128">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="50c61-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="50c61-129">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="50c61-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="50c61-130">Atribut lze zahrnout do jakékoli skupiny.</span><span class="sxs-lookup"><span data-stu-id="50c61-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="50c61-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="50c61-131">Click Save.</span></span>
23. <span data-ttu-id="50c61-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50c61-132">Close the page.</span></span>

