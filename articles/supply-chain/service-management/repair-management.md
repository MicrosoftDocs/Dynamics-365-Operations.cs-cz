---
title: Správa oprav
description: Systematicky seskupujte problémy s cílem usnadnit nalezení návrhů řešení, která byla úspěšná v minulosti.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32202344f77352cd3f9c1a807d14192a9bf0d9e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "349278"
---
# <a name="repair-management"></a><span data-ttu-id="924ac-103">Správa oprav</span><span class="sxs-lookup"><span data-stu-id="924ac-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="924ac-104">Při správě oprav můžete systematicky seskupovat problémy.</span><span class="sxs-lookup"><span data-stu-id="924ac-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="924ac-105">Cílem je usnadnit nalezení návrhů řešení, která byla úspěšná v minulosti.</span><span class="sxs-lookup"><span data-stu-id="924ac-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="924ac-106">Můžete nastavit příznaky, diagnózu a řešení.</span><span class="sxs-lookup"><span data-stu-id="924ac-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="924ac-107">Všechny můžete později použít v případě, obdržíte obdobné položky k opravě.</span><span class="sxs-lookup"><span data-stu-id="924ac-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="924ac-108">Můžete také nastavit fáze oprav, které mohou sledovat postup opravy určité položky.</span><span class="sxs-lookup"><span data-stu-id="924ac-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="924ac-109">Nastavení správy oprav</span><span class="sxs-lookup"><span data-stu-id="924ac-109">Setting up repair management</span></span>

<span data-ttu-id="924ac-110">Formuláře pro nastavení slouží k zadávání informací, které budou použity k zadání symptomů, diagnózy a rozhodnutí opravy.</span><span class="sxs-lookup"><span data-stu-id="924ac-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

1.  <span data-ttu-id="924ac-111">Klepněte na tlačítko **řízení servisu** \> **nastavení** \> **opravy** \> **podmínky**.</span><span class="sxs-lookup"><span data-stu-id="924ac-111">Click **Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>

2.  <span data-ttu-id="924ac-112">Klepněte na tlačítko **řízení servisu** \> **nastavení** \> **opravy** \> **Oblasti příznaků**.</span><span class="sxs-lookup"><span data-stu-id="924ac-112">Click **Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>

3.  <span data-ttu-id="924ac-113">Klepněte na tlačítko **řízení servisu** \> **nastavení** \> **opravy** \> **Oblasti diagnózy**.</span><span class="sxs-lookup"><span data-stu-id="924ac-113">Click **Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>

4.  <span data-ttu-id="924ac-114">Klepněte na tlačítko **řízení servisu** \> **nastavení** \> **opravy** \> **Řešení**.</span><span class="sxs-lookup"><span data-stu-id="924ac-114">Click **Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>

5.  <span data-ttu-id="924ac-115">Klepněte na tlačítko **řízení servisu** \> **nastavení** \> **opravy** \> **Fáze oprav**.</span><span class="sxs-lookup"><span data-stu-id="924ac-115">Click **Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="924ac-116">Příznaky a podmínky</span><span class="sxs-lookup"><span data-stu-id="924ac-116">Symptoms and conditions</span></span>

<span data-ttu-id="924ac-117">Příznaky definují, jak odběratel charakterizuje problém.</span><span class="sxs-lookup"><span data-stu-id="924ac-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="924ac-118">Mezi příznaky patří postřehy odběratele, kterými oznamuje nutnost opravy.</span><span class="sxs-lookup"><span data-stu-id="924ac-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="924ac-119">Můžete definovat oblasti symptomů, kódy symptomů a stavy.</span><span class="sxs-lookup"><span data-stu-id="924ac-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="924ac-120">Oblast symptomů odpovídá oblasti, v níž se projevují příznaky nefunkčnosti, a kód symptomu popisuje symptom nefunkčnosti.</span><span class="sxs-lookup"><span data-stu-id="924ac-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="924ac-121">Podmínka popisuje stav nebo prostředí, které je k dispozici v případě, že dochází k potížím.</span><span class="sxs-lookup"><span data-stu-id="924ac-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="924ac-122">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="924ac-122">**Example**</span></span>

<span data-ttu-id="924ac-123">Počítač je předán do opravy vzhledem k tomu, že po delším používání selhává pevný disk.</span><span class="sxs-lookup"><span data-stu-id="924ac-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="924ac-124">Chyba pevného disku způsobí chybu modré obrazovky.</span><span class="sxs-lookup"><span data-stu-id="924ac-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="924ac-125">Technik, který obdrží počítač, zadá následující příznaky a podmínky:</span><span class="sxs-lookup"><span data-stu-id="924ac-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="924ac-126">Oblast symptomů je pevný disk</span><span class="sxs-lookup"><span data-stu-id="924ac-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="924ac-127">Kód symptomu je chyba modré obrazovky</span><span class="sxs-lookup"><span data-stu-id="924ac-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="924ac-128">Podmínkou je, že pevný disk po delším použití selhává</span><span class="sxs-lookup"><span data-stu-id="924ac-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="924ac-129">Diagnóza a řešení</span><span class="sxs-lookup"><span data-stu-id="924ac-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="924ac-130">Pole diagnózy a řešení obsahují příkazy z hlediska oprav.</span><span class="sxs-lookup"><span data-stu-id="924ac-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="924ac-131">Jedná se o kroky, které servisní technik provedl při prověřování daného problému.</span><span class="sxs-lookup"><span data-stu-id="924ac-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="924ac-132">Oblast diagnózy popisuje operace, které je třeba podniknout s cílem vyřešení problému.</span><span class="sxs-lookup"><span data-stu-id="924ac-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="924ac-133">Kód diagnózy popisuje postup při zpracování problému a řešením je například oprava či výměna položky nebo zrušení objednávky odběratelem.</span><span class="sxs-lookup"><span data-stu-id="924ac-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="924ac-134">Pokud je počítač opraven, může být oblastí diagnózy například "vadný díl," kódem opravy může být "nainstalovaná nová videokarta" a řešením bude "výměna".</span><span class="sxs-lookup"><span data-stu-id="924ac-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="924ac-135">Fáze opravy</span><span class="sxs-lookup"><span data-stu-id="924ac-135">Repair stages</span></span>

<span data-ttu-id="924ac-136">Fáze opravy popisují průběh procesu opravy.</span><span class="sxs-lookup"><span data-stu-id="924ac-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="924ac-137">Fáze opravy obsahuje parametr **Dokončeno**, který udává, že zpracování řádku opravy bylo dokončeno a datum a čas dokončení byl zaznamenán.</span><span class="sxs-lookup"><span data-stu-id="924ac-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="924ac-138">Použití správy oprav</span><span class="sxs-lookup"><span data-stu-id="924ac-138">Applying repair management</span></span>

<span data-ttu-id="924ac-139">Chcete-li pro určitou položku použít správu oprav, musí být tato položka konfigurována prostřednictvím relace předmětu servisu v servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="924ac-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="924ac-140">Ze servisní zakázky můžete poté vytvořit řádek opravy s údaji o aktuálním problému.</span><span class="sxs-lookup"><span data-stu-id="924ac-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="924ac-141">Na řádku opravy definujete předmět servisu, který je předmětem opravy a také informace o symptomech, diagnóze a zpracování.</span><span class="sxs-lookup"><span data-stu-id="924ac-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="924ac-142">Pro řádek opravy můžete též vytvořit poznámku.</span><span class="sxs-lookup"><span data-stu-id="924ac-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="924ac-143">Řádky oprav lze vytvořit pro všechny kroky v procesu opravy.</span><span class="sxs-lookup"><span data-stu-id="924ac-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="924ac-144">Vytvoření řádku opravy pro servisní zakázku</span><span class="sxs-lookup"><span data-stu-id="924ac-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="924ac-145">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="924ac-145">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="924ac-146">Vyberte servisní zakázku s předmětem servisu, který vyžaduje opravu.</span><span class="sxs-lookup"><span data-stu-id="924ac-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="924ac-147">Klepněte na tlačítko **Oprava** \> **Řádky opravy** k otevření formuláře **řádky oprav**.</span><span class="sxs-lookup"><span data-stu-id="924ac-147">Click **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="924ac-148">Stisknutím kombinace kláves CTRL+N vytvořte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="924ac-148">Press CTRL+N to create a new line.</span></span>

5.  <span data-ttu-id="924ac-149">Vyberte předmět servisu.</span><span class="sxs-lookup"><span data-stu-id="924ac-149">Select a service object.</span></span> <span data-ttu-id="924ac-150">Můžete vybrat libovolný předmět servisu, který byl konfigurován prostřednictvím relace předmětu v servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="924ac-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="924ac-151">Vyberte libovolné přednastavené symptomy, diagnózy či hodnoty zpracování, které jsou relevantní pro daný řádek opravy, a v případě potřeby klepněte na kartu **Poznámka** a vytvořte na řádku opravy poznámku.</span><span class="sxs-lookup"><span data-stu-id="924ac-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then click the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="924ac-152">Stisknutím kombinace kláves CTRL+S nový řádek opravy uložte.</span><span class="sxs-lookup"><span data-stu-id="924ac-152">Press CTRL+S to save the new repair line.</span></span> <span data-ttu-id="924ac-153">Pole **Vytvořené datum a čas** na kartě **hlavní** ve formuláři **řádky oprav** se aktualizuje s použitím času uložení.</span><span class="sxs-lookup"><span data-stu-id="924ac-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="924ac-154">Sledování průběhu a vyřešení opravy problému</span><span class="sxs-lookup"><span data-stu-id="924ac-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="924ac-155">Chcete-li sledovat průběh opravy problému, můžete pro řádek opravy definovat fáze opravy.</span><span class="sxs-lookup"><span data-stu-id="924ac-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="924ac-156">Po vyřešení problému s opravou můžete řádek opravy zavřít.</span><span class="sxs-lookup"><span data-stu-id="924ac-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="924ac-157">Nastavte fázi opravy na fázi s aktivovanou vlastností **dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="924ac-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="924ac-158">Jako čas dokončení zpracování řádku bude zaregistrováno aktuální datum a čas.</span><span class="sxs-lookup"><span data-stu-id="924ac-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="924ac-159">Zavřete řádek opravy pro vyřešený problém</span><span class="sxs-lookup"><span data-stu-id="924ac-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="924ac-160">Otevřete formulář **Řádky opravy**.</span><span class="sxs-lookup"><span data-stu-id="924ac-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="924ac-161">Pomocí postupu popsaného dříve v tomto tématu vytvořte řádek opravy.</span><span class="sxs-lookup"><span data-stu-id="924ac-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="924ac-162">Vyberte řádek opravy s položkou opravy, kterou chcete uzavřít.</span><span class="sxs-lookup"><span data-stu-id="924ac-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="924ac-163">V poli **Fáze opravy** vyberte fázi s aktivovanou vlastností **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="924ac-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  


