---
title: Vytvoření a zpracování neshody
description: Tento postup slouží k provádění správy neshody a je založen na existující objednávce kvality.
author: perlynne
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
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "336283"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="553c7-103">Vytvoření a zpracování neshody</span><span class="sxs-lookup"><span data-stu-id="553c7-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="553c7-104">Tento postup slouží k provádění správy neshody a je založen na existující objednávce kvality.</span><span class="sxs-lookup"><span data-stu-id="553c7-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="553c7-105">Tento záznam lze spustit v ukázkové společnosti USMF a můžete navrhované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="553c7-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="553c7-106">Tento postup obvykle provádí úředník řízení kvality.</span><span class="sxs-lookup"><span data-stu-id="553c7-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="553c7-107">Nezbytným předpokladem je spuštění záznamu úkolu „Kontrola kvality zboží“.</span><span class="sxs-lookup"><span data-stu-id="553c7-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="553c7-108">Aby bylo možné zpracovat schválení neshody, uživatel, který spustí záznam úkolu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="553c7-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="553c7-109">Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.</span><span class="sxs-lookup"><span data-stu-id="553c7-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="553c7-110">Vyberte objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="553c7-110">Select a quality order</span></span>
1. <span data-ttu-id="553c7-111">Přejděte do nabídky Objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="553c7-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="553c7-112">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="553c7-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="553c7-113">Vyberte objednávku kvality, která byla vytvořena na základě záznamu úkolu "Kontrola kvality zboží".</span><span class="sxs-lookup"><span data-stu-id="553c7-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="553c7-114">Vytvoření neshody</span><span class="sxs-lookup"><span data-stu-id="553c7-114">Create a nonconformance</span></span>
1. <span data-ttu-id="553c7-115">Klepněte na možnost Dotazy.</span><span class="sxs-lookup"><span data-stu-id="553c7-115">Click Inquiries.</span></span>
2. <span data-ttu-id="553c7-116">Klikněte na možnost Neshody.</span><span class="sxs-lookup"><span data-stu-id="553c7-116">Click Non conformances.</span></span>
3. <span data-ttu-id="553c7-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="553c7-117">Click New.</span></span>
4. <span data-ttu-id="553c7-118">V poli Typ problému kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="553c7-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="553c7-119">Vyberte problém, který byl zjištěn během procesu kontroly.</span><span class="sxs-lookup"><span data-stu-id="553c7-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="553c7-120">V poli Typ problému kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="553c7-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="553c7-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="553c7-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="553c7-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="553c7-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="553c7-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="553c7-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="553c7-124">Schválení/zamítnutí neshody</span><span class="sxs-lookup"><span data-stu-id="553c7-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="553c7-125">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="553c7-125">Click Functions.</span></span>
2. <span data-ttu-id="553c7-126">Klikněte na možnost Schválit neshodu.</span><span class="sxs-lookup"><span data-stu-id="553c7-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="553c7-127">V tomto příkladu to je schválení neshody.</span><span class="sxs-lookup"><span data-stu-id="553c7-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="553c7-128">Schválené neshody lze přidružit k souvisejícím operacím k zaznamenání práce, která je provedena v průběhu zpracování neshody nebo během zpracování oprav jako v rámci tohoto záznamu úkolu.</span><span class="sxs-lookup"><span data-stu-id="553c7-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="553c7-129">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="553c7-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="553c7-130">Vytvoření akce opravy</span><span class="sxs-lookup"><span data-stu-id="553c7-130">Create a correction action</span></span>
1. <span data-ttu-id="553c7-131">Klikněte na možnost Opravy.</span><span class="sxs-lookup"><span data-stu-id="553c7-131">Click Corrections.</span></span>
2. <span data-ttu-id="553c7-132">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="553c7-132">Click New.</span></span>
3. <span data-ttu-id="553c7-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="553c7-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="553c7-134">V poli Číslo pracovníka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="553c7-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="553c7-135">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="553c7-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="553c7-136">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="553c7-136">Click Select.</span></span>
7. <span data-ttu-id="553c7-137">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="553c7-137">Click Attach.</span></span>
    * <span data-ttu-id="553c7-138">Vytvořte poznámku o opravě.</span><span class="sxs-lookup"><span data-stu-id="553c7-138">Create a note about the correction.</span></span> <span data-ttu-id="553c7-139">V tomto příkladu akce představuje kontaktování dodavatele za účelem diskuze o případu neshody.</span><span class="sxs-lookup"><span data-stu-id="553c7-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="553c7-140">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="553c7-140">Click New.</span></span>
9. <span data-ttu-id="553c7-141">Klikněte na možnost Poznámka.</span><span class="sxs-lookup"><span data-stu-id="553c7-141">Click Note.</span></span>
    * <span data-ttu-id="553c7-142">Všimněte si, že v závislosti na nastavení sestavy lze vytisknout různé typy dokumentů v sestavách, které se vztahují ke správě neshody.</span><span class="sxs-lookup"><span data-stu-id="553c7-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="553c7-143">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="553c7-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="553c7-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="553c7-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="553c7-145">Údržba opravy</span><span class="sxs-lookup"><span data-stu-id="553c7-145">Maintain a correction</span></span>
1. <span data-ttu-id="553c7-146">Klikněte na možnost Označit jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="553c7-146">Click Mark complete.</span></span>
2. <span data-ttu-id="553c7-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="553c7-147">Click OK.</span></span>
3. <span data-ttu-id="553c7-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="553c7-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="553c7-149">Zavření neshody</span><span class="sxs-lookup"><span data-stu-id="553c7-149">Close a nonconformance</span></span>
1. <span data-ttu-id="553c7-150">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="553c7-150">Click Functions.</span></span>
2. <span data-ttu-id="553c7-151">Klikněte na možnost Zavřít neshodu.</span><span class="sxs-lookup"><span data-stu-id="553c7-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="553c7-152">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="553c7-152">Click Yes.</span></span>
4. <span data-ttu-id="553c7-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="553c7-153">Close the page.</span></span>
5. <span data-ttu-id="553c7-154">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="553c7-154">Close the page.</span></span>
