--- 
title: "Zkopírování vedlejších produktů z existující verze receptury"
description: "Tato procedura popisuje postup kopírování vedlejších produktů z existující verze receptury do jiné verze receptury pro uvolněný produkt."
author: YuyuScheller
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 80543780c423b5beac3ec57f4fa035e560aaa4ce
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="cc984-103">Zkopírování vedlejších produktů z existující verze receptury</span><span class="sxs-lookup"><span data-stu-id="cc984-103">Copy co-products from an existing formula version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc984-104">Tato procedura popisuje postup kopírování vedlejších produktů z existující verze receptury do jiné verze receptury pro uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="cc984-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="cc984-105">Je důležité, aby existovala alespoň jedna verze receptury přidružená k vedlejším produktům.</span><span class="sxs-lookup"><span data-stu-id="cc984-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="cc984-106">Společnost s ukázkovými daty USP2 slouží k vytváření této procedury.</span><span class="sxs-lookup"><span data-stu-id="cc984-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="cc984-107">Vyhledat uvolněný produkt</span><span class="sxs-lookup"><span data-stu-id="cc984-107">Find a released product</span></span>
1. <span data-ttu-id="cc984-108">Přejděte na Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="cc984-108">Go to Released products.</span></span>
2. <span data-ttu-id="cc984-109">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="cc984-109">Click Show filters.</span></span>
    * <span data-ttu-id="cc984-110">Chystáte se v dialogovém okně Filtr přidat pole Výrobní typ.</span><span class="sxs-lookup"><span data-stu-id="cc984-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="cc984-111">Klepnutím na tlačítko Přidat pole filtru přidáte pole Typ výroby.</span><span class="sxs-lookup"><span data-stu-id="cc984-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="cc984-112">V dalším kroku je třeba ručně zadat vzorec do pole Typ výroby předtím, než vyberete možnost Použít.</span><span class="sxs-lookup"><span data-stu-id="cc984-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="cc984-113">Tím nastavíte filtr na seznamu vydaných produktů.</span><span class="sxs-lookup"><span data-stu-id="cc984-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="cc984-114">V poli Typ výroby ručně zadejte vzorec.</span><span class="sxs-lookup"><span data-stu-id="cc984-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="cc984-115">Klepněte na možnost Použít.</span><span class="sxs-lookup"><span data-stu-id="cc984-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="cc984-116">Vybrat uvolněný produkt</span><span class="sxs-lookup"><span data-stu-id="cc984-116">Select a released product</span></span>
1. <span data-ttu-id="cc984-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cc984-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="cc984-118">Klikněte na Verze receptury.</span><span class="sxs-lookup"><span data-stu-id="cc984-118">Click Formula versions.</span></span>
    * <span data-ttu-id="cc984-119">V podokně akcí Analýza klikněte na položku Verze receptur.</span><span class="sxs-lookup"><span data-stu-id="cc984-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="cc984-120">Kopírovat souběžný produkt</span><span class="sxs-lookup"><span data-stu-id="cc984-120">Copy co-products</span></span>
1. <span data-ttu-id="cc984-121">V podokně akcí klikněte na možnost Verze receptury.</span><span class="sxs-lookup"><span data-stu-id="cc984-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="cc984-122">Klepněte na možnost Souběžné produkty.</span><span class="sxs-lookup"><span data-stu-id="cc984-122">Click Co-products.</span></span>
3. <span data-ttu-id="cc984-123">Klepněte na tlačítko Kopírovat.</span><span class="sxs-lookup"><span data-stu-id="cc984-123">Click Copy.</span></span>
4. <span data-ttu-id="cc984-124">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cc984-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="cc984-125">V poli Verze receptury zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cc984-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="cc984-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cc984-126">Click OK.</span></span>
7. <span data-ttu-id="cc984-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cc984-127">Close the page.</span></span>


