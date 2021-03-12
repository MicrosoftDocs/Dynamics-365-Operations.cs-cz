---
title: Nastavení automatického odsouhlasení dopravného
description: Tato procedura ukazuje, jak nastavit data pro automatické odsouhlasení dopravného.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bfd96fcae78fd0fe383781112c17c7a3b5ea1d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974003"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="5b77b-103">Nastavení automatického odsouhlasení dopravného</span><span class="sxs-lookup"><span data-stu-id="5b77b-103">Set up automatic freight reconciliation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b77b-104">Tato procedura ukazuje, jak nastavit data pro automatické odsouhlasení dopravného.</span><span class="sxs-lookup"><span data-stu-id="5b77b-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="5b77b-105">Obvykle to provádějí vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="5b77b-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="5b77b-106">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="5b77b-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="5b77b-107">Nastavení typu účtu dopravného</span><span class="sxs-lookup"><span data-stu-id="5b77b-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="5b77b-108">Přejděte do nabídky Správa přepravy > Nastavení > Odsouhlasení dopravného > Typ účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="5b77b-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="5b77b-109">Typ kusovníku dopravného definuje, jak by měly být spárovány účty za dopravné a faktury dopravce.</span><span class="sxs-lookup"><span data-stu-id="5b77b-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="5b77b-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5b77b-110">Click New.</span></span>
3. <span data-ttu-id="5b77b-111">Zadejte hodnotu do pole Typ účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="5b77b-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="5b77b-112">Do pole Sestavení modulu zadejte Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.</span><span class="sxs-lookup"><span data-stu-id="5b77b-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="5b77b-113">Toto je standardní knihovna kódu modulu odpovídající řízení přepravy.</span><span class="sxs-lookup"><span data-stu-id="5b77b-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="5b77b-114">Do pole Třída modulu zadejte "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer".</span><span class="sxs-lookup"><span data-stu-id="5b77b-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="5b77b-115">Toto je standardní třída modulu odpovídající řízení přepravy.</span><span class="sxs-lookup"><span data-stu-id="5b77b-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="5b77b-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5b77b-116">Click New.</span></span>
7. <span data-ttu-id="5b77b-117">V poli Popis vyberte hodnotu, která by měla odpovídat hodnotě na účtu dopravného a faktuře dopravce.</span><span class="sxs-lookup"><span data-stu-id="5b77b-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="5b77b-118">V poli Párování požadováno vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="5b77b-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="5b77b-119">Pokud nastavíte do tohoto pole hodnotu Ano, znamená to, že hodnota vybraná v poli Popis musí odpovídat faktuře za dopravu i faktuře dopravce.</span><span class="sxs-lookup"><span data-stu-id="5b77b-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="5b77b-120">Pokud je nastavena na hodnotu Ne, může být pole na jedné z nich prázdné.</span><span class="sxs-lookup"><span data-stu-id="5b77b-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="5b77b-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5b77b-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="5b77b-122">Nastavení přiřazení typu účtu dopravného</span><span class="sxs-lookup"><span data-stu-id="5b77b-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="5b77b-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5b77b-123">Close the page.</span></span>
2. <span data-ttu-id="5b77b-124">Přejděte do nabídky Správa přepravy > Nastavení > Odsouhlasení dopravného > Přiřazení typů účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="5b77b-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="5b77b-125">Přiřazení typu účtu dopravného se používá k určení, jaký typ účtu dopravného se používá pro konkrétní dopravce.</span><span class="sxs-lookup"><span data-stu-id="5b77b-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="5b77b-126">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5b77b-126">Click New.</span></span>
4. <span data-ttu-id="5b77b-127">V poli Režim zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b77b-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="5b77b-128">V poli Dopravce dodávky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b77b-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="5b77b-129">V poli Typ účtu dopravného vyberte typ účtu dopravného, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="5b77b-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="5b77b-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5b77b-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="5b77b-131">Nastavení hlavního auditu</span><span class="sxs-lookup"><span data-stu-id="5b77b-131">Set up the audit master</span></span>
1. <span data-ttu-id="5b77b-132">Přejděte do nabídky Správa přepravy > Nastavení > Odsouhlasení dopravného > Hlavní audit.</span><span class="sxs-lookup"><span data-stu-id="5b77b-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="5b77b-133">Hlavní audit definuje přípustné limity pro automatické odsouhlasení dopravného.</span><span class="sxs-lookup"><span data-stu-id="5b77b-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="5b77b-134">Určuje, o kolik se mohou lišit peněžní částky na účtu dopravného a faktuře dopravce, a umožňuje odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="5b77b-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="5b77b-135">Také definuje, jak zpracovat nesrovnalosti.</span><span class="sxs-lookup"><span data-stu-id="5b77b-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="5b77b-136">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5b77b-136">Click New.</span></span>
3. <span data-ttu-id="5b77b-137">Zadejte hodnotu do pole ID hlavního auditu.</span><span class="sxs-lookup"><span data-stu-id="5b77b-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="5b77b-138">V poli Dopravce dodávky vyberte stejného dopravce dodávky jako dříve.</span><span class="sxs-lookup"><span data-stu-id="5b77b-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="5b77b-139">V poli Typ účtu dopravného vyberte typ účtu dopravného, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="5b77b-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="5b77b-140">Rozbalte oddíl Tolerance.</span><span class="sxs-lookup"><span data-stu-id="5b77b-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="5b77b-141">V poli Minimální úroveň tolerance zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="5b77b-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="5b77b-142">V poli Maximální úroveň tolerance zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="5b77b-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="5b77b-143">Rozbalte sekci Výsledek.</span><span class="sxs-lookup"><span data-stu-id="5b77b-143">Expand the Result section.</span></span>
10. <span data-ttu-id="5b77b-144">V poli Kód důvodu přeplatku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b77b-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="5b77b-145">Pokud se peněžní částky na účtu dopravného a faktuře dopravce liší, kódy důvodu přeplatku či nedoplatku určují účty, na kterých má být registrován rozdíl, dokud je rozdíl v rámci úrovní tolerance.</span><span class="sxs-lookup"><span data-stu-id="5b77b-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="5b77b-146">V poli Kód důvodu nedoplatku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b77b-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="5b77b-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5b77b-147">Close the page.</span></span>

