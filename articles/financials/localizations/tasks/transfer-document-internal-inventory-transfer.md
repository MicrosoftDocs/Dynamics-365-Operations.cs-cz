--- 
title: "Vygenerování dokladu převodu pro interní převod zásob"
description: "Tato procedura ukazuje postup vytvoření přepravních dokladů pro pohyb zboží v rámci společnosti."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 30e5f6ad184720d0e119f86fb703ed7211b27fab
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="c8602-103">Vygenerování dokladu převodu pro interní převod zásob</span><span class="sxs-lookup"><span data-stu-id="c8602-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8602-104">Tato procedura ukazuje postup vytvoření přepravních dokladů pro pohyb zboží v rámci společnosti.</span><span class="sxs-lookup"><span data-stu-id="c8602-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="c8602-105">Tato procedura je k dispozici pouze pro právnické osoby, jejichž primární adresa je v Litvě.</span><span class="sxs-lookup"><span data-stu-id="c8602-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="c8602-106">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Litvě.</span><span class="sxs-lookup"><span data-stu-id="c8602-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="c8602-107">Než bude možné tuto proceduru dokončit, je nutné dokončit proceduru "Nastavení převodních dokumentů pro pohyb zboží uvnitř společnosti".</span><span class="sxs-lookup"><span data-stu-id="c8602-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="c8602-108">Tato procedura je určena pouze pro skladové účetní.</span><span class="sxs-lookup"><span data-stu-id="c8602-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="c8602-109">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="c8602-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="c8602-110">Vytvoření převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="c8602-110">Create a transfer order</span></span>
1. <span data-ttu-id="c8602-111">Přejděte na Správa zásob > Příchozí objednávky > Objednávka převozu.</span><span class="sxs-lookup"><span data-stu-id="c8602-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="c8602-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c8602-112">Click New.</span></span>
3. <span data-ttu-id="c8602-113">V poli Ze skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="c8602-114">V poli Do skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="c8602-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c8602-115">Click Add.</span></span>
6. <span data-ttu-id="c8602-116">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c8602-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c8602-117">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="c8602-118">Zadání podrobností přepravy pro převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="c8602-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="c8602-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8602-119">Click Save.</span></span>
2. <span data-ttu-id="c8602-120">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="c8602-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="c8602-121">Klikněte na Podrobnosti přepravy.</span><span class="sxs-lookup"><span data-stu-id="c8602-121">Click Transportation details.</span></span>
4. <span data-ttu-id="c8602-122">Vyberte možnost Ano v poli Tisk podrobností o přepravě.</span><span class="sxs-lookup"><span data-stu-id="c8602-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="c8602-123">V poli Zboží vydal zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="c8602-124">Zadejte hodnotu do pole Balík.</span><span class="sxs-lookup"><span data-stu-id="c8602-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="c8602-125">Do pole Úroveň rizika zatížení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="c8602-126">V poli Dopravce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="c8602-127">V poli Model zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="c8602-128">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="c8602-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="c8602-129">Zadejte hodnotu do pole Registrační číslo přívěsu.</span><span class="sxs-lookup"><span data-stu-id="c8602-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="c8602-130">V poli Řidič zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="c8602-131">Do pole Jméno řidiče zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8602-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="c8602-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c8602-132">Click Save.</span></span>
15. <span data-ttu-id="c8602-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8602-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="c8602-134">Zobrazení dodacího listu pro nezaúčtovaný převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="c8602-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="c8602-135">Klepněte na Dodací list.</span><span class="sxs-lookup"><span data-stu-id="c8602-135">Click Packing slip.</span></span>
2. <span data-ttu-id="c8602-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c8602-136">Click OK.</span></span>
3. <span data-ttu-id="c8602-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8602-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="c8602-138">Zobrazení dodacího listu pro zaúčtovaný převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="c8602-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="c8602-139">V podokně akcí klikněte na možnost Převodní příkaz.</span><span class="sxs-lookup"><span data-stu-id="c8602-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="c8602-140">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="c8602-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="c8602-141">Klikněte na Převodní příkaz expedice.</span><span class="sxs-lookup"><span data-stu-id="c8602-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="c8602-142">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="c8602-142">Click the General tab.</span></span>
5. <span data-ttu-id="c8602-143">Vyberte volbu v poli Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="c8602-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="c8602-144">Klikněte na záložku Přehled.</span><span class="sxs-lookup"><span data-stu-id="c8602-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="c8602-145">Zadejte hodnotu do pole Dodací list.</span><span class="sxs-lookup"><span data-stu-id="c8602-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="c8602-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c8602-146">Click OK.</span></span>
9. <span data-ttu-id="c8602-147">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="c8602-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="c8602-148">Klepněte na Dodací list.</span><span class="sxs-lookup"><span data-stu-id="c8602-148">Click Packing slip.</span></span>
11. <span data-ttu-id="c8602-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c8602-149">Click OK.</span></span>


