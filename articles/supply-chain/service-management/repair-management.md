---
title: Správa oprav
description: Systematicky seskupujte problémy s cílem usnadnit nalezení návrhů řešení, která byla úspěšná v minulosti.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265709f298d9310d5d647eaa029ece778d2e226e
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470634"
---
# <a name="repair-management"></a><span data-ttu-id="f26a6-103">Správa oprav</span><span class="sxs-lookup"><span data-stu-id="f26a6-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f26a6-104">Při správě oprav můžete systematicky seskupovat problémy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="f26a6-105">Cílem je usnadnit nalezení návrhů řešení, která byla úspěšná v minulosti.</span><span class="sxs-lookup"><span data-stu-id="f26a6-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="f26a6-106">Můžete nastavit příznaky, diagnózu a řešení.</span><span class="sxs-lookup"><span data-stu-id="f26a6-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="f26a6-107">Všechny můžete později použít v případě, obdržíte obdobné položky k opravě.</span><span class="sxs-lookup"><span data-stu-id="f26a6-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="f26a6-108">Můžete také nastavit fáze oprav, které mohou sledovat postup opravy určité položky.</span><span class="sxs-lookup"><span data-stu-id="f26a6-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="f26a6-109">Nastavení správy oprav</span><span class="sxs-lookup"><span data-stu-id="f26a6-109">Setting up repair management</span></span>

<span data-ttu-id="f26a6-110">Formuláře pro nastavení slouží k zadávání informací, které budou použity k zadání symptomů, diagnózy a rozhodnutí opravy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

- <span data-ttu-id="f26a6-111">**Správa servisu** \> **Nastavení** \> **Opravy** \> **Podmínky**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-111">**Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>
- <span data-ttu-id="f26a6-112">**Správa servisu** \> **nastavení** \> **opravy** \> **Oblasti příznaků**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-112">**Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>
-  <span data-ttu-id="f26a6-113">**Správa servisu** \> **nastavení** \> **opravy** \> **Oblasti diagnózy**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-113">**Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>
- <span data-ttu-id="f26a6-114">**Správa servisu** \> **nastavení** \> **opravy** \> **Řešení**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-114">**Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>
- <span data-ttu-id="f26a6-115">**Správa servisu** \> **nastavení** \> **opravy** \> **Fáze oprav**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-115">**Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="f26a6-116">Příznaky a podmínky</span><span class="sxs-lookup"><span data-stu-id="f26a6-116">Symptoms and conditions</span></span>

<span data-ttu-id="f26a6-117">Příznaky definují, jak odběratel charakterizuje problém.</span><span class="sxs-lookup"><span data-stu-id="f26a6-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="f26a6-118">Mezi příznaky patří postřehy odběratele, kterými oznamuje nutnost opravy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="f26a6-119">Můžete definovat oblasti symptomů, kódy symptomů a stavy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="f26a6-120">Oblast symptomů odpovídá oblasti, v níž se projevují příznaky nefunkčnosti, a kód symptomu popisuje symptom nefunkčnosti.</span><span class="sxs-lookup"><span data-stu-id="f26a6-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="f26a6-121">Podmínka popisuje stav nebo prostředí, které je k dispozici v případě, že dochází k potížím.</span><span class="sxs-lookup"><span data-stu-id="f26a6-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="f26a6-122">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="f26a6-122">**Example**</span></span>

<span data-ttu-id="f26a6-123">Počítač je předán do opravy vzhledem k tomu, že po delším používání selhává pevný disk.</span><span class="sxs-lookup"><span data-stu-id="f26a6-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="f26a6-124">Chyba pevného disku způsobí chybu modré obrazovky.</span><span class="sxs-lookup"><span data-stu-id="f26a6-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="f26a6-125">Technik, který obdrží počítač, zadá následující příznaky a podmínky:</span><span class="sxs-lookup"><span data-stu-id="f26a6-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="f26a6-126">Oblast symptomů je pevný disk</span><span class="sxs-lookup"><span data-stu-id="f26a6-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="f26a6-127">Kód symptomu je chyba modré obrazovky</span><span class="sxs-lookup"><span data-stu-id="f26a6-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="f26a6-128">Podmínkou je, že pevný disk po delším použití selhává</span><span class="sxs-lookup"><span data-stu-id="f26a6-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="f26a6-129">Diagnóza a řešení</span><span class="sxs-lookup"><span data-stu-id="f26a6-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="f26a6-130">Pole diagnózy a řešení obsahují příkazy z hlediska oprav.</span><span class="sxs-lookup"><span data-stu-id="f26a6-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="f26a6-131">Jedná se o kroky, které servisní technik provedl při prověřování daného problému.</span><span class="sxs-lookup"><span data-stu-id="f26a6-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="f26a6-132">Oblast diagnózy popisuje operace, které je třeba podniknout s cílem vyřešení problému.</span><span class="sxs-lookup"><span data-stu-id="f26a6-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="f26a6-133">Kód diagnózy popisuje postup při zpracování problému a řešením je například oprava či výměna položky nebo zrušení objednávky odběratelem.</span><span class="sxs-lookup"><span data-stu-id="f26a6-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="f26a6-134">Pokud je počítač opraven, může být oblastí diagnózy například "vadný díl," kódem opravy může být "nainstalovaná nová videokarta" a řešením bude "výměna".</span><span class="sxs-lookup"><span data-stu-id="f26a6-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="f26a6-135">Fáze opravy</span><span class="sxs-lookup"><span data-stu-id="f26a6-135">Repair stages</span></span>

<span data-ttu-id="f26a6-136">Fáze opravy popisují průběh procesu opravy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="f26a6-137">Fáze opravy obsahuje parametr **Dokončeno**, který udává, že zpracování řádku opravy bylo dokončeno a datum a čas dokončení byl zaznamenán.</span><span class="sxs-lookup"><span data-stu-id="f26a6-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="f26a6-138">Použití správy oprav</span><span class="sxs-lookup"><span data-stu-id="f26a6-138">Applying repair management</span></span>

<span data-ttu-id="f26a6-139">Chcete-li pro určitou položku použít správu oprav, musí být tato položka konfigurována prostřednictvím relace předmětu servisu v servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="f26a6-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="f26a6-140">Ze servisní zakázky můžete poté vytvořit řádek opravy s údaji o aktuálním problému.</span><span class="sxs-lookup"><span data-stu-id="f26a6-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="f26a6-141">Na řádku opravy definujete předmět servisu, který je předmětem opravy a také informace o symptomech, diagnóze a zpracování.</span><span class="sxs-lookup"><span data-stu-id="f26a6-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="f26a6-142">Pro řádek opravy můžete též vytvořit poznámku.</span><span class="sxs-lookup"><span data-stu-id="f26a6-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="f26a6-143">Řádky oprav lze vytvořit pro všechny kroky v procesu opravy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="f26a6-144">Vytvoření řádku opravy pro servisní zakázku</span><span class="sxs-lookup"><span data-stu-id="f26a6-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="f26a6-145">Přejděte na **Správa servisu** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-145">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f26a6-146">Vyberte servisní zakázku s předmětem servisu, který vyžaduje opravu.</span><span class="sxs-lookup"><span data-stu-id="f26a6-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="f26a6-147">Vyberte formulář **Oprava** \> **Řádky opravy** k otevření formuláře **řádky oprav**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-147">Select **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="f26a6-148">Zvolte **Nový** pro vytvoření nového řádku.</span><span class="sxs-lookup"><span data-stu-id="f26a6-148">Select **New** to create a new line.</span></span>

5.  <span data-ttu-id="f26a6-149">Vyberte předmět servisu.</span><span class="sxs-lookup"><span data-stu-id="f26a6-149">Select a service object.</span></span> <span data-ttu-id="f26a6-150">Můžete vybrat libovolný předmět servisu, který byl konfigurován prostřednictvím relace předmětu v servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="f26a6-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="f26a6-151">Vyberte libovolné přednastavené symptomy, diagnózy či hodnoty zpracování, které jsou relevantní pro daný řádek opravy, a v případě potřeby vyberte **Poznámka** a vytvořte na řádku opravy poznámku.</span><span class="sxs-lookup"><span data-stu-id="f26a6-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then select the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="f26a6-152">Kliknutím na tlačítko **Uložit** uložte nový řádek opravy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-152">Select **Save** to save the new repair line.</span></span> <span data-ttu-id="f26a6-153">Pole **Vytvořené datum a čas** na kartě **hlavní** ve formuláři **řádky oprav** se aktualizuje s použitím času uložení.</span><span class="sxs-lookup"><span data-stu-id="f26a6-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="f26a6-154">Sledování průběhu a vyřešení opravy problému</span><span class="sxs-lookup"><span data-stu-id="f26a6-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="f26a6-155">Chcete-li sledovat průběh opravy problému, můžete pro řádek opravy definovat fáze opravy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="f26a6-156">Po vyřešení problému s opravou můžete řádek opravy zavřít.</span><span class="sxs-lookup"><span data-stu-id="f26a6-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="f26a6-157">Nastavte fázi opravy na fázi s aktivovanou vlastností **dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="f26a6-158">Jako čas dokončení zpracování řádku bude zaregistrováno aktuální datum a čas.</span><span class="sxs-lookup"><span data-stu-id="f26a6-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="f26a6-159">Zavřete řádek opravy pro vyřešený problém</span><span class="sxs-lookup"><span data-stu-id="f26a6-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="f26a6-160">Otevřete formulář **Řádky opravy**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="f26a6-161">Pomocí postupu popsaného dříve v tomto tématu vytvořte řádek opravy.</span><span class="sxs-lookup"><span data-stu-id="f26a6-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="f26a6-162">Vyberte řádek opravy s položkou opravy, kterou chcete uzavřít.</span><span class="sxs-lookup"><span data-stu-id="f26a6-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="f26a6-163">V poli **Fáze opravy** vyberte fázi s aktivovanou vlastností **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="f26a6-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]