---
title: Definice účtování
description: Tento článek obsahuje informace o definicích účtování a o tom, jak je lze definovat a propojit. U podporovaných typů zaúčtování a dokumentů můžete ke klasifikaci hlavních účtů a finančních dimenzí účetních položek použít namísto účetních profilů definice účtování.
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52a0bb163363c26f5c782ae0efbae31918ee918d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230219"
---
# <a name="posting-definitions"></a><span data-ttu-id="5ef86-104">Definice účtování</span><span class="sxs-lookup"><span data-stu-id="5ef86-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ef86-105">Tento článek obsahuje informace o definicích účtování a o tom, jak je lze definovat a propojit.</span><span class="sxs-lookup"><span data-stu-id="5ef86-105">This article provides information about posting definitions, and how to define and link them.</span></span>
<span data-ttu-id="5ef86-106">U podporovaných typů zaúčtování a dokumentů můžete ke klasifikaci hlavních účtů a finančních dimenzí účetních položek použít namísto účetních profilů definice účtování.</span><span class="sxs-lookup"><span data-stu-id="5ef86-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="5ef86-107">Podporované dokumenty a typy účtování můžete prohlížet na stránce **Definice účtování transakcí**.</span><span class="sxs-lookup"><span data-stu-id="5ef86-107">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="5ef86-108">Chcete-li začít definice účtování používat, vyberte možnost **Použít definice účtování** na stránce **Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="5ef86-108">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="5ef86-109">I když použijete definice účtování, stále je nutné definovat účetní profily pro původní položky a nepodporované typy zaúčtování a dokumentů.</span><span class="sxs-lookup"><span data-stu-id="5ef86-109">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="5ef86-110">Definice účtování musíte použít, abyste umožnili účtování břemen pro nákupní objednávky a účtování předběžných břemen pro nákupní požadavky.</span><span class="sxs-lookup"><span data-stu-id="5ef86-110">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="5ef86-111">Definování definic účtování</span><span class="sxs-lookup"><span data-stu-id="5ef86-111">Defining posting definitions</span></span>
<span data-ttu-id="5ef86-112">Použijte stránku **Definice účtování** k určení kritérií shody a definování položek, které by se měly generovat, pokud dojde ke shodě.</span><span class="sxs-lookup"><span data-stu-id="5ef86-112">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="5ef86-113">Kritéria shody se posuzují pro původní položky jako rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="5ef86-113">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="5ef86-114">Na stránce **Definice účtování** můžete také řádkům položek přiřadit čísla priorit, abyste mohli řídit pořadí, v jakém se řádky posuzují.</span><span class="sxs-lookup"><span data-stu-id="5ef86-114">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="5ef86-115">Řádky, které mají nejnižší číslo priority, se vyhodnocují jako první.</span><span class="sxs-lookup"><span data-stu-id="5ef86-115">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="5ef86-116">Příklad: posoudí se všechny řádky, které mají prioritu 1, poté řádky, které mají prioritu 2, a tak dále.</span><span class="sxs-lookup"><span data-stu-id="5ef86-116">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="5ef86-117">Při zjištění shody jsou ostatní kritéria párování ignorována.</span><span class="sxs-lookup"><span data-stu-id="5ef86-117">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="5ef86-118">Pouze kritéria ve skupině, která odpovídá původní transakci, vytvářejí generované položky.</span><span class="sxs-lookup"><span data-stu-id="5ef86-118">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="5ef86-119">Definice účtování můžete ověřit pomocí **Průvodce definicí účtování (testu)**.</span><span class="sxs-lookup"><span data-stu-id="5ef86-119">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="5ef86-120">Po definování vzorové původní položky pro definici účtování se zobrazí generované položky.</span><span class="sxs-lookup"><span data-stu-id="5ef86-120">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="5ef86-121">Verze definic účtování můžete použít spolu s daty účinnosti.</span><span class="sxs-lookup"><span data-stu-id="5ef86-121">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="5ef86-122">Na příklad můžete vytvořit příští verzi definice účtování k účtování jiného účtu hlavní knihy v novém fiskálním roce.</span><span class="sxs-lookup"><span data-stu-id="5ef86-122">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="5ef86-123">Použijte stránku **Definice účtování transakcí** pro přiřazení účtovacích definic k typům transakcí.</span><span class="sxs-lookup"><span data-stu-id="5ef86-123">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="5ef86-124">Propojení definic účtování</span><span class="sxs-lookup"><span data-stu-id="5ef86-124">Linking posting definitions</span></span>
<span data-ttu-id="5ef86-125">Při vytváření účtovacích definic můžete propojit jednu účtovací definici s jinou.</span><span class="sxs-lookup"><span data-stu-id="5ef86-125">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="5ef86-126">Kritéria definice, s kterou propojujete, se považují za rozšíření kritérií aktuální definice účtování.</span><span class="sxs-lookup"><span data-stu-id="5ef86-126">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="5ef86-127">Tato funkce pomáhá ušetřit čas, protože pro aktuální definice účtování není nutné znovu zadat kritéria na pevné záložce **Položky** na stránce **Definice účtování**, pokud jste již řádky zadali pro jinou definici.</span><span class="sxs-lookup"><span data-stu-id="5ef86-127">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="5ef86-128">Do diagramů nebo tabulek zahrňte všechny odkazy, které byste mohli použít.</span><span class="sxs-lookup"><span data-stu-id="5ef86-128">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="5ef86-129">Abyste zabránili konfliktům s aktuální definicí účtování, ujistěte se, že všechny řádky v definicích účtování, s kterými propojujete, jsou jedinečné.</span><span class="sxs-lookup"><span data-stu-id="5ef86-129">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="5ef86-130">Tato omezení platí v případě, že vytvoříte odkazy v definicích účtování:</span><span class="sxs-lookup"><span data-stu-id="5ef86-130">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="5ef86-131">Konkrétní definice účtování může buď odkazovat na jinou definici účtování, nebo může jiná definice účtování odkazovat na ni, ale nemohou nastat obě situace zároveň.</span><span class="sxs-lookup"><span data-stu-id="5ef86-131">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="5ef86-132">Definice účtování ovšem může odkazovat na více definic účtování.</span><span class="sxs-lookup"><span data-stu-id="5ef86-132">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="5ef86-133">Odkazy můžete nastavit pouze mezi definicemi účtování, které jsou ve stejném modulu.</span><span class="sxs-lookup"><span data-stu-id="5ef86-133">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="5ef86-134">Definici účtování můžete přiřadit k libovolnému typu transakce, ale tento typ transakce musí být ve stejném modulu jako definice účtování.</span><span class="sxs-lookup"><span data-stu-id="5ef86-134">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="5ef86-135">Použijte stránku **Definice účtování transakcí** a podívejte se, v kterém modulu typ transakce je.</span><span class="sxs-lookup"><span data-stu-id="5ef86-135">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="5ef86-136">Další informace získáte v části [Příklady definice účtování](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="5ef86-136">For more information, see [Posting definition examples](example-posting-definitions.md).</span></span> 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]