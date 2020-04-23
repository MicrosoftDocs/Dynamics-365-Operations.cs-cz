---
title: Zkopírování receptury
description: Tento postup se zaměřuje na vytvoření receptury, která zahrnuje stejné látky jako existující receptura, ale s drobnými odlišnostmi.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 624e06c2184764f3fd8df3ddf7d90753ef2cb9d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210932"
---
# <a name="copy-a-formula"></a><span data-ttu-id="4eeb4-103">Zkopírování receptury</span><span class="sxs-lookup"><span data-stu-id="4eeb4-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4eeb4-104">Tento postup se zaměřuje na vytvoření receptury, která zahrnuje stejné látky jako existující receptura, ale s drobnými odlišnostmi.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="4eeb4-105">Chcete-li vytvořit řádky receptury, pomocí funkce Kopírovat můžete zkopírovat existující recepturu, který má většinu potřebných látek.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="4eeb4-106">Jednotlivé řádky v nové verzi lze libovolně upravit.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="4eeb4-107">Díky funkci Kopírovat není nutno vytvořit více receptur, které jsou téměř totožné.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="4eeb4-108">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="4eeb4-109">Vytvoření receptury</span><span class="sxs-lookup"><span data-stu-id="4eeb4-109">Create a formula</span></span>
1. <span data-ttu-id="4eeb4-110">Přejděte do nabídky Řízení informací o produktech > Kusovníky a receptury > Receptury.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="4eeb4-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-111">Click New.</span></span>
3. <span data-ttu-id="4eeb4-112">Zadejte hodnotu do pole Receptura.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="4eeb4-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="4eeb4-114">Zadejte popisný název receptury.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="4eeb4-115">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4eeb4-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4eeb4-117">V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4eeb4-118">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="4eeb4-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4eeb4-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="4eeb4-121">Zkopírování řádků receptury</span><span class="sxs-lookup"><span data-stu-id="4eeb4-121">Copy formula lines</span></span>
1. <span data-ttu-id="4eeb4-122">V podokně akcí klikněte na možnost Receptura.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="4eeb4-123">Klepněte na tlačítko Kopírovat.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-123">Click Copy.</span></span>
3. <span data-ttu-id="4eeb4-124">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4eeb4-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4eeb4-126">V poli Verze receptury kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4eeb4-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4eeb4-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="4eeb4-129">Úprava zkopírovaných řádků receptury</span><span class="sxs-lookup"><span data-stu-id="4eeb4-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="4eeb4-130">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="4eeb4-131">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-131">Click Delete.</span></span>
3. <span data-ttu-id="4eeb4-132">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="4eeb4-133">Schválit recepturu</span><span class="sxs-lookup"><span data-stu-id="4eeb4-133">Approve formula</span></span>
1. <span data-ttu-id="4eeb4-134">V podokně akcí klikněte na možnost Receptura.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="4eeb4-135">Klepněte na možnost Schválit recepturu.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-135">Click Approve formula.</span></span>
3. <span data-ttu-id="4eeb4-136">V poli Schválil(a) kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4eeb4-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4eeb4-138">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-138">Click Select.</span></span>
6. <span data-ttu-id="4eeb4-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4eeb4-139">Click OK.</span></span>

