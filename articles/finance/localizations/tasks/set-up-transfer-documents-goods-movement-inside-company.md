---
title: Nastavení dokladů převodu pro pohyb zboží v rámci společnosti
description: Tato procedura ukazuje postup vytvoření přepravních dokladů pro pohyb zboží v rámci společnosti.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185674"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="d18c4-103">Nastavení dokladů převodu pro pohyb zboží v rámci společnosti</span><span class="sxs-lookup"><span data-stu-id="d18c4-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d18c4-104">Tato procedura ukazuje postup vytvoření přepravních dokladů pro pohyb zboží v rámci společnosti.</span><span class="sxs-lookup"><span data-stu-id="d18c4-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="d18c4-105">Tato procedura je k dispozici pouze pro právnické osoby, jejichž primární adresa je v Litvě.</span><span class="sxs-lookup"><span data-stu-id="d18c4-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="d18c4-106">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Litvě.</span><span class="sxs-lookup"><span data-stu-id="d18c4-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="d18c4-107">Než bude možné tuto proceduru dokončit, je nutné dokončit proceduru "Nastavení převodních dokumentů pro pohyb zboží uvnitř společnosti".</span><span class="sxs-lookup"><span data-stu-id="d18c4-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="d18c4-108">Tato procedura je určena pouze pro skladové účetní.</span><span class="sxs-lookup"><span data-stu-id="d18c4-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="d18c4-109">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="d18c4-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="d18c4-110">Vytvoření převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="d18c4-110">Create a transfer order</span></span>
1. <span data-ttu-id="d18c4-111">Přejděte na Správa zásob > Příchozí objednávky > Objednávka převozu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="d18c4-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d18c4-112">Click New.</span></span>
3. <span data-ttu-id="d18c4-113">V poli Ze skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="d18c4-114">V poli Do skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="d18c4-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d18c4-115">Click Add.</span></span>
6. <span data-ttu-id="d18c4-116">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d18c4-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="d18c4-117">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="d18c4-118">Zadání podrobností přepravy pro převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="d18c4-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="d18c4-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d18c4-119">Click Save.</span></span>
2. <span data-ttu-id="d18c4-120">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="d18c4-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="d18c4-121">Klikněte na Podrobnosti přepravy.</span><span class="sxs-lookup"><span data-stu-id="d18c4-121">Click Transportation details.</span></span>
4. <span data-ttu-id="d18c4-122">Vyberte možnost Ano v poli Tisk podrobností o přepravě.</span><span class="sxs-lookup"><span data-stu-id="d18c4-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="d18c4-123">V poli Zboží vydal zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="d18c4-124">Zadejte hodnotu do pole Balík.</span><span class="sxs-lookup"><span data-stu-id="d18c4-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="d18c4-125">Do pole Úroveň rizika zatížení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="d18c4-126">V poli Dopravce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="d18c4-127">V poli Model zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="d18c4-128">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="d18c4-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="d18c4-129">Zadejte hodnotu do pole Registrační číslo přívěsu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="d18c4-130">V poli Řidič zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="d18c4-131">Do pole Jméno řidiče zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d18c4-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="d18c4-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d18c4-132">Click Save.</span></span>
15. <span data-ttu-id="d18c4-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d18c4-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="d18c4-134">Zobrazení dodacího listu pro nezaúčtovaný převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="d18c4-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="d18c4-135">Klepněte na Dodací list.</span><span class="sxs-lookup"><span data-stu-id="d18c4-135">Click Packing slip.</span></span>
2. <span data-ttu-id="d18c4-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d18c4-136">Click OK.</span></span>
3. <span data-ttu-id="d18c4-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d18c4-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="d18c4-138">Zobrazení dodacího listu pro zaúčtovaný převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="d18c4-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="d18c4-139">V podokně akcí klikněte na možnost Převodní příkaz.</span><span class="sxs-lookup"><span data-stu-id="d18c4-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="d18c4-140">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="d18c4-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="d18c4-141">Klikněte na Převodní příkaz expedice.</span><span class="sxs-lookup"><span data-stu-id="d18c4-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="d18c4-142">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="d18c4-142">Click the General tab.</span></span>
5. <span data-ttu-id="d18c4-143">Vyberte volbu v poli Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="d18c4-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="d18c4-144">Klikněte na záložku Přehled.</span><span class="sxs-lookup"><span data-stu-id="d18c4-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="d18c4-145">Zadejte hodnotu do pole Dodací list.</span><span class="sxs-lookup"><span data-stu-id="d18c4-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="d18c4-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d18c4-146">Click OK.</span></span>
9. <span data-ttu-id="d18c4-147">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="d18c4-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="d18c4-148">Klepněte na Dodací list.</span><span class="sxs-lookup"><span data-stu-id="d18c4-148">Click Packing slip.</span></span>
11. <span data-ttu-id="d18c4-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d18c4-149">Click OK.</span></span>

