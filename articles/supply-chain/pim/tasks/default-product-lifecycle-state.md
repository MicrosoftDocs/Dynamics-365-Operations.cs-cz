---
title: Vytvoření výchozího stavu životního cyklu produktu
description: Tento postup popisuje, jak vytvoříte výchozí stav životního cyklu produktu i jak přidružit výchozí stav uvolněným produktům.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd346f338a14476960ab47db2e3013402f4c43af
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213163"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="8f289-103">Vytvoření výchozího stavu životního cyklu produktu</span><span class="sxs-lookup"><span data-stu-id="8f289-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f289-104">Tento postup popisuje, jak vytvoříte výchozí stav životního cyklu produktu i jak přidružit výchozí stav uvolněným produktům.</span><span class="sxs-lookup"><span data-stu-id="8f289-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="8f289-105">Vytvoření výchozího stavu životního cyklu</span><span class="sxs-lookup"><span data-stu-id="8f289-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="8f289-106">Přejděte na Řízení informací o produktech > Nastavení > Stav životnosti produktu.</span><span class="sxs-lookup"><span data-stu-id="8f289-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="8f289-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8f289-107">Click New.</span></span>
3. <span data-ttu-id="8f289-108">Zadejte hodnotu do pole Stav.</span><span class="sxs-lookup"><span data-stu-id="8f289-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="8f289-109">Vyberte možnost Ano výchozí pro uvolněné pole právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="8f289-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="8f289-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="8f289-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8f289-111">Vyberte možnost Ne v poli Je aktivní pro plánování.</span><span class="sxs-lookup"><span data-stu-id="8f289-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="8f289-112">Pokud nemá nový uvolněný produkt být zahrnut do hlavního plánování, vyberte Ne.</span><span class="sxs-lookup"><span data-stu-id="8f289-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="8f289-113">Pokud má být zahrnutý do hlavního plánování, ponechte ovládací prvek na výchozí hodnotě Ano.</span><span class="sxs-lookup"><span data-stu-id="8f289-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="8f289-114">Vytvoření nového uvolněného produktu</span><span class="sxs-lookup"><span data-stu-id="8f289-114">Create a new released product</span></span>
1. <span data-ttu-id="8f289-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8f289-115">Close the page.</span></span>
2. <span data-ttu-id="8f289-116">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="8f289-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="8f289-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8f289-117">Click New.</span></span>
4. <span data-ttu-id="8f289-118">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="8f289-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="8f289-119">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f289-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="8f289-120">Do pole Vyhledávání jména zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f289-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="8f289-121">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f289-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="8f289-122">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f289-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="8f289-123">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f289-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="8f289-124">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f289-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="8f289-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8f289-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="8f289-126">Výchozí stav životního cyklu produktu je globální definice.</span><span class="sxs-lookup"><span data-stu-id="8f289-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="8f289-127">Změna produktu na aktivní stav</span><span class="sxs-lookup"><span data-stu-id="8f289-127">Change the product to an active state</span></span>
1. <span data-ttu-id="8f289-128">V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f289-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="8f289-129">Předpokládejme, že jste nastavili aktivní stav, nyní můžete vybrat aktivní stav pro povolení použití produktu v hlavmím plánování a výpočtu na úrovni kusovníku.</span><span class="sxs-lookup"><span data-stu-id="8f289-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="8f289-130">Samozřejmě to dává smysl, pouze pokud nejsou zadány všechny podrobnosti o produktu vyžadované pro konzistentní plánování.</span><span class="sxs-lookup"><span data-stu-id="8f289-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

