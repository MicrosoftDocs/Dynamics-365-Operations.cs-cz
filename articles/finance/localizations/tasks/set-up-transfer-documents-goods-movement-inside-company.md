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
ms.openlocfilehash: e85bd359ce1053629ad4217cf623e57b2976463a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441199"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="a65fb-103">Nastavení dokladů převodu pro pohyb zboží v rámci společnosti</span><span class="sxs-lookup"><span data-stu-id="a65fb-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a65fb-104">Tato procedura ukazuje postup vytvoření přepravních dokladů pro pohyb zboží v rámci společnosti.</span><span class="sxs-lookup"><span data-stu-id="a65fb-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="a65fb-105">Tato procedura je k dispozici pouze pro právnické osoby, jejichž primární adresa je v Litvě.</span><span class="sxs-lookup"><span data-stu-id="a65fb-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="a65fb-106">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Litvě.</span><span class="sxs-lookup"><span data-stu-id="a65fb-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="a65fb-107">Než bude možné tuto proceduru dokončit, je nutné dokončit proceduru „Nastavení převodních dokumentů pro pohyb zboží uvnitř společnosti“.</span><span class="sxs-lookup"><span data-stu-id="a65fb-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="a65fb-108">Tato procedura je určena pouze pro skladové účetní.</span><span class="sxs-lookup"><span data-stu-id="a65fb-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="a65fb-109">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="a65fb-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="a65fb-110">Vytvoření převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="a65fb-110">Create a transfer order</span></span>
1. <span data-ttu-id="a65fb-111">Přejděte na Správa zásob > Příchozí objednávky > Objednávka převozu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="a65fb-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a65fb-112">Click New.</span></span>
3. <span data-ttu-id="a65fb-113">V poli Ze skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="a65fb-114">V poli Do skladu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="a65fb-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a65fb-115">Click Add.</span></span>
6. <span data-ttu-id="a65fb-116">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="a65fb-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a65fb-117">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="a65fb-118">Zadání podrobností přepravy pro převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="a65fb-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="a65fb-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a65fb-119">Click Save.</span></span>
2. <span data-ttu-id="a65fb-120">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="a65fb-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="a65fb-121">Klikněte na Podrobnosti přepravy.</span><span class="sxs-lookup"><span data-stu-id="a65fb-121">Click Transportation details.</span></span>
4. <span data-ttu-id="a65fb-122">Vyberte možnost Ano v poli Tisk podrobností o přepravě.</span><span class="sxs-lookup"><span data-stu-id="a65fb-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="a65fb-123">V poli Zboží vydal zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="a65fb-124">Zadejte hodnotu do pole Balík.</span><span class="sxs-lookup"><span data-stu-id="a65fb-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="a65fb-125">Do pole Úroveň rizika zatížení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="a65fb-126">V poli Dopravce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="a65fb-127">V poli Model zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="a65fb-128">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="a65fb-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="a65fb-129">Zadejte hodnotu do pole Registrační číslo přívěsu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="a65fb-130">V poli Řidič zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="a65fb-131">Do pole Jméno řidiče zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a65fb-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="a65fb-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a65fb-132">Click Save.</span></span>
15. <span data-ttu-id="a65fb-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a65fb-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="a65fb-134">Zobrazení dodacího listu pro nezaúčtovaný převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="a65fb-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="a65fb-135">Klepněte na Dodací list.</span><span class="sxs-lookup"><span data-stu-id="a65fb-135">Click Packing slip.</span></span>
2. <span data-ttu-id="a65fb-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a65fb-136">Click OK.</span></span>
3. <span data-ttu-id="a65fb-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a65fb-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="a65fb-138">Zobrazení dodacího listu pro zaúčtovaný převodní příkaz</span><span class="sxs-lookup"><span data-stu-id="a65fb-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="a65fb-139">V podokně akcí klikněte na možnost Převodní příkaz.</span><span class="sxs-lookup"><span data-stu-id="a65fb-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="a65fb-140">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="a65fb-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="a65fb-141">Klikněte na Převodní příkaz expedice.</span><span class="sxs-lookup"><span data-stu-id="a65fb-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="a65fb-142">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="a65fb-142">Click the General tab.</span></span>
5. <span data-ttu-id="a65fb-143">Vyberte volbu v poli Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="a65fb-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="a65fb-144">Klikněte na záložku Přehled.</span><span class="sxs-lookup"><span data-stu-id="a65fb-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="a65fb-145">Zadejte hodnotu do pole Dodací list.</span><span class="sxs-lookup"><span data-stu-id="a65fb-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="a65fb-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a65fb-146">Click OK.</span></span>
9. <span data-ttu-id="a65fb-147">V podokně akcí klikněte na možnost Expedovat.</span><span class="sxs-lookup"><span data-stu-id="a65fb-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="a65fb-148">Klepněte na Dodací list.</span><span class="sxs-lookup"><span data-stu-id="a65fb-148">Click Packing slip.</span></span>
11. <span data-ttu-id="a65fb-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a65fb-149">Click OK.</span></span>

