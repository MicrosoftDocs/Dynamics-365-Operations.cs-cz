---
title: Nastavení elektronických podpisů
description: Tento postup použijte k nastavení elektronických podpisů.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad4ef067841511e235dcf538c720b72283d31c3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176871"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="c8584-103">Nastavení elektronických podpisů</span><span class="sxs-lookup"><span data-stu-id="c8584-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8584-104">Tento postup použijte k nastavení elektronických podpisů.</span><span class="sxs-lookup"><span data-stu-id="c8584-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="c8584-105">Elektronický podpis potvrzuje identitu osoby, která spouští nebo schvaluje určitý proces využívající výpočetní techniku.</span><span class="sxs-lookup"><span data-stu-id="c8584-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="c8584-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti DAT.</span><span class="sxs-lookup"><span data-stu-id="c8584-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="c8584-107">Povolení konfiguračního klíče Elektronický podpis</span><span class="sxs-lookup"><span data-stu-id="c8584-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="c8584-108">Přejděte do nabídky Správa systému > Nastavení > Konfigurace licence.</span><span class="sxs-lookup"><span data-stu-id="c8584-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="c8584-109">Ve stromu rozbalte možnost Správa.</span><span class="sxs-lookup"><span data-stu-id="c8584-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="c8584-110">Zkontrolujte, zda je zaškrtnuto políčko Elektronický podpis.</span><span class="sxs-lookup"><span data-stu-id="c8584-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="c8584-111">Pokud není zaškrtnuté políčko Elektronický podpis, je nutné povolit režim údržby.</span><span class="sxs-lookup"><span data-stu-id="c8584-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="c8584-112">Režim údržby lze povolit v tomto prostředí jen provedením úlohy údržby pomocí služeb Lifecycle Services nebo místním použitím nástroje Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="c8584-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="c8584-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8584-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="c8584-114">Nastavení parametrů elektronického podpisu</span><span class="sxs-lookup"><span data-stu-id="c8584-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="c8584-115">Přejděte do nabídky Správa organizace > Nastavení > Elektronický podpis > Parametry elektronického podpisu.</span><span class="sxs-lookup"><span data-stu-id="c8584-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="c8584-116">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="c8584-116">Click Edit.</span></span>
3. <span data-ttu-id="c8584-117">Zadejte hodnotu do pole Oznámení.</span><span class="sxs-lookup"><span data-stu-id="c8584-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="c8584-118">Zadejte zprávu, kterou podepisující uživatelé uvidí v případech, kdy je vyžadován podpis.</span><span class="sxs-lookup"><span data-stu-id="c8584-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="c8584-119">Můžete zadat libovolný text.</span><span class="sxs-lookup"><span data-stu-id="c8584-119">You can enter any text.</span></span> <span data-ttu-id="c8584-120">Tato zpráva uživatele obvykle informuje o významu elektronického podpisu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c8584-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="c8584-121">Pokud chcete zadat text oznámení v dalších jazycích, klikněte na tlačítko Překlady.</span><span class="sxs-lookup"><span data-stu-id="c8584-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="c8584-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8584-122">Click Save.</span></span>
5. <span data-ttu-id="c8584-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8584-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="c8584-124">Nastavení kódů důvodů pro elektronické podpisy</span><span class="sxs-lookup"><span data-stu-id="c8584-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="c8584-125">Přejděte do nabídky Správa organizace > Nastavení > Elektronický podpis > Kódy důvodů pro elektronický podpis.</span><span class="sxs-lookup"><span data-stu-id="c8584-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="c8584-126">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c8584-126">Click New.</span></span>
    * <span data-ttu-id="c8584-127">Kódy důvodů je třeba nastavit dříve, než začnete elektronické podpisy používat.</span><span class="sxs-lookup"><span data-stu-id="c8584-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="c8584-128">Při podepisování dokumentu je vyžadován platný kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="c8584-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="c8584-129">Podepisující uživatel vybere kód důvodu, který bude vyjadřovat účel elektronického podpisu.</span><span class="sxs-lookup"><span data-stu-id="c8584-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="c8584-130">Jeden z kódů důvodu může například označovat schválení dokumentu právníkem.</span><span class="sxs-lookup"><span data-stu-id="c8584-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="c8584-131">Zadejte hodnotu do pole Kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="c8584-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="c8584-132">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="c8584-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c8584-133">Zadejte další kódy důvodů, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="c8584-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="c8584-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8584-134">Click Save.</span></span>
6. <span data-ttu-id="c8584-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8584-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="c8584-136">Vyžádání elektronických podpisů pro existující procesy</span><span class="sxs-lookup"><span data-stu-id="c8584-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="c8584-137">Přejděte do nabídky Správa organizace > Nastavení > Elektronický podpis > Požadavky na elektronický podpis.</span><span class="sxs-lookup"><span data-stu-id="c8584-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="c8584-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c8584-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c8584-139">Vyberte proces vyžadující elektronický podpis.</span><span class="sxs-lookup"><span data-stu-id="c8584-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="c8584-140">Zaškrtněte políčko Je požadován podpis nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="c8584-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="c8584-141">Opakujte tyto kroky pro každý proces, který vyžaduje elektronický podpis.</span><span class="sxs-lookup"><span data-stu-id="c8584-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="c8584-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8584-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="c8584-143">Vytvoření vlastního požadavku na elektronické podpisy</span><span class="sxs-lookup"><span data-stu-id="c8584-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="c8584-144">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c8584-144">Click New.</span></span>
2. <span data-ttu-id="c8584-145">Zaškrtněte políčko Je požadován podpis nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="c8584-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="c8584-146">V poli Název zadejte název procesu, který vyžaduje elektronický podpis.</span><span class="sxs-lookup"><span data-stu-id="c8584-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="c8584-147">V poli Název tabulky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c8584-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c8584-148">V seznamu najděte a vyberte tabulku, v níž jsou uložena data, která je třeba podepsat.</span><span class="sxs-lookup"><span data-stu-id="c8584-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="c8584-149">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c8584-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c8584-150">V poli Název pole kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c8584-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c8584-151">V seznamu najděte a vyberte pole tabulky, které chcete sledovat.</span><span class="sxs-lookup"><span data-stu-id="c8584-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="c8584-152">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c8584-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c8584-153">Určete, kdy je podpis požadován.</span><span class="sxs-lookup"><span data-stu-id="c8584-153">Specify when a signature is required.</span></span>     <span data-ttu-id="c8584-154">Je-li požadován podpis při každé změně dat v poli, vyberte možnost Vždy.</span><span class="sxs-lookup"><span data-stu-id="c8584-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="c8584-155">Vyberte možnost Pouze, pokud je podpis vyžadován pouze za určitých podmínek.</span><span class="sxs-lookup"><span data-stu-id="c8584-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="c8584-156">Pokud vyberete Pouze, je nutné vybrat také jednu z následujících možností: Při vložení záznamu, Při aktualizaci záznamu nebo Při odstranění záznamu.</span><span class="sxs-lookup"><span data-stu-id="c8584-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="c8584-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8584-157">Click Save.</span></span>
11. <span data-ttu-id="c8584-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8584-158">Close the page.</span></span>

