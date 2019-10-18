---
title: Výběr definic datového modelu při vytváření formátů
description: K provedení kroků v tomto postupu musíte nejprve dokončit postup "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66b9636f6d9da06f0ea65ab311dd9308ff6ae020
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184708"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="153d7-103">Výběr definic datového modelu při vytváření formátů</span><span class="sxs-lookup"><span data-stu-id="153d7-103">Select data model definitions when you create formats</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="153d7-104">K provedení kroků v tomto postupu musíte nejprve dokončit postup "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="153d7-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="153d7-105">Tento postup popisuje, jak lze vybrat kořenovou položku modelu jako definici datového modelu pro vložení konfigurace nastavení elektronického vykazování (ER), které slouží ke generování elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="153d7-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="153d7-106">V tomto postupu přidáte novou konfiguraci formátu ER pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="153d7-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="153d7-107">Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="153d7-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="153d7-108">Kroky lze dokončit za použití libovolné datové sady.</span><span class="sxs-lookup"><span data-stu-id="153d7-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="153d7-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="153d7-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="153d7-110">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní.</span><span class="sxs-lookup"><span data-stu-id="153d7-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="153d7-111">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.</span><span class="sxs-lookup"><span data-stu-id="153d7-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="153d7-112">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="153d7-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="153d7-113">Přidání nové konfigurace datového modelu ER</span><span class="sxs-lookup"><span data-stu-id="153d7-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="153d7-114">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="153d7-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="153d7-115">Doporučujeme přidat novou konfiguraci modelu ER, která obsahuje datový model, který je určen jako zdroj dat pro generování sestav ER.</span><span class="sxs-lookup"><span data-stu-id="153d7-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="153d7-116">V poli Název zadejte Model platby (fiktivní).</span><span class="sxs-lookup"><span data-stu-id="153d7-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="153d7-117">Model platby (fiktivní)</span><span class="sxs-lookup"><span data-stu-id="153d7-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="153d7-118">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="153d7-118">Click Create configuration.</span></span>
4. <span data-ttu-id="153d7-119">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="153d7-119">Click Designer.</span></span>
    * <span data-ttu-id="153d7-120">Otevřete návrháře ER a určete strukturu datového modelu této konfigurace.</span><span class="sxs-lookup"><span data-stu-id="153d7-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="153d7-121">Předpokládejme, že navrhneme datový model obchodní domény pro platby tak, aby podporovala 2 způsoby platby – bezhotovostní a přímý debet.</span><span class="sxs-lookup"><span data-stu-id="153d7-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="153d7-122">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="153d7-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="153d7-123">Do pole Název zadejte Platby – převedení kreditu.</span><span class="sxs-lookup"><span data-stu-id="153d7-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="153d7-124">Platby – převedení kreditu</span><span class="sxs-lookup"><span data-stu-id="153d7-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="153d7-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="153d7-125">Click Add.</span></span>
8. <span data-ttu-id="153d7-126">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="153d7-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="153d7-127">Do pole Nový uzel zadejte Kořen modelu.</span><span class="sxs-lookup"><span data-stu-id="153d7-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="153d7-128">Do pole Název zadejte Platby – přímý debet.</span><span class="sxs-lookup"><span data-stu-id="153d7-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="153d7-129">Platby – přímý debet</span><span class="sxs-lookup"><span data-stu-id="153d7-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="153d7-130">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="153d7-130">Click Add.</span></span>
12. <span data-ttu-id="153d7-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="153d7-131">Click Save.</span></span>
13. <span data-ttu-id="153d7-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="153d7-132">Close the page.</span></span>
14. <span data-ttu-id="153d7-133">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="153d7-133">Click Change status.</span></span>
    * <span data-ttu-id="153d7-134">Dokončete pracovní verzi modelu a umožněte tak, aby byla k dispozici v mapování a formátech nového modelu.</span><span class="sxs-lookup"><span data-stu-id="153d7-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="153d7-135">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="153d7-135">Click Complete.</span></span>
16. <span data-ttu-id="153d7-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="153d7-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="153d7-137">Začněte zadáním nové konfigurace formátu ER</span><span class="sxs-lookup"><span data-stu-id="153d7-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="153d7-138">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="153d7-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="153d7-139">V poli Nový zadejte Formát založený na datovém modelu Model platby (fiktivní).</span><span class="sxs-lookup"><span data-stu-id="153d7-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="153d7-140">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="153d7-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="153d7-141">Všimněte si, že všechny kořenové položky vybraného datového modelu jsou aktuálně k dispozici pro výběr jako definice datového modelu.</span><span class="sxs-lookup"><span data-stu-id="153d7-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="153d7-142">Můžete dále navrhovat formát pomocí některé z požadovaných kořenových položek datového modelu.</span><span class="sxs-lookup"><span data-stu-id="153d7-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="153d7-143">Chybějící mapování modelu pro vybranou kořenovou položku vám nezabrání pokračovat.</span><span class="sxs-lookup"><span data-stu-id="153d7-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="153d7-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="153d7-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="153d7-145">Přidání nové konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="153d7-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="153d7-146">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="153d7-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="153d7-147">V poli Nový zadejte Mapování modelu založené na datovém modelu Model platby (fiktivní).</span><span class="sxs-lookup"><span data-stu-id="153d7-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="153d7-148">V poli Název zadejte Mapování modelu platby (fiktivní).</span><span class="sxs-lookup"><span data-stu-id="153d7-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="153d7-149">Mapování modelu platby (fiktivní)</span><span class="sxs-lookup"><span data-stu-id="153d7-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="153d7-150">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="153d7-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="153d7-151">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="153d7-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="153d7-152">Navrhněte mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="153d7-152">Design ER model mappings</span></span>
1. <span data-ttu-id="153d7-153">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="153d7-153">Click Designer.</span></span>
    * <span data-ttu-id="153d7-154">Pomocí návrháře ER určete mapování modelu pro požadované kořenové položky.</span><span class="sxs-lookup"><span data-stu-id="153d7-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="153d7-155">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="153d7-155">Click Designer.</span></span>
    * <span data-ttu-id="153d7-156">Simulujte nastavení vybraného mapování modelu pro kořenovou položku vybraného modelu.</span><span class="sxs-lookup"><span data-stu-id="153d7-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="153d7-157">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.</span><span class="sxs-lookup"><span data-stu-id="153d7-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="153d7-158">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="153d7-158">Click Add root.</span></span>
5. <span data-ttu-id="153d7-159">Do pole Název zadejte Hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="153d7-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="153d7-160">Do pole Tabulka zadejte hodnotu „LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="153d7-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="153d7-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="153d7-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="153d7-162">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="153d7-162">Click OK.</span></span>
8. <span data-ttu-id="153d7-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="153d7-163">Click Save.</span></span>
9. <span data-ttu-id="153d7-164">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="153d7-164">Close the page.</span></span>
10. <span data-ttu-id="153d7-165">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="153d7-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="153d7-166">Začněte zadáním další nové konfigurace formátu ER</span><span class="sxs-lookup"><span data-stu-id="153d7-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="153d7-167">Ve stromovém zobrazení vyberte Model platby (fiktivní).</span><span class="sxs-lookup"><span data-stu-id="153d7-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="153d7-168">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="153d7-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="153d7-169">V poli Nový zadejte Formát založený na datovém modelu Model platby (fiktivní).</span><span class="sxs-lookup"><span data-stu-id="153d7-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="153d7-170">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="153d7-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="153d7-171">Nyní je tak k dispozici k mapování zdrojů dat aplikace pouze jedna kořenová položka.</span><span class="sxs-lookup"><span data-stu-id="153d7-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="153d7-172">Po uvedení alespoň jednoho modelu mapování jsou mapovány ke zdrojům dat aplikace pouze kořenové položky modelu, které lze vybrat jako definici modelu po přidání formátu ER.</span><span class="sxs-lookup"><span data-stu-id="153d7-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="153d7-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="153d7-173">Close the page.</span></span>

