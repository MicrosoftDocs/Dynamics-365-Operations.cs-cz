---
title: Vytvoření možností pokrytí
description: Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d304b0cf65c7833ebc7f21323efc59540289de8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803674"
---
# <a name="create-coverage-options"></a><span data-ttu-id="1082f-103">Vytvoření možností pokrytí</span><span class="sxs-lookup"><span data-stu-id="1082f-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1082f-104">Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="1082f-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="1082f-105">Možnosti pokrytí mohou například zahrnovat **pouze zaměstnance** pro lékařský plán nebo **2x plat** pro plán životního pojištění.</span><span class="sxs-lookup"><span data-stu-id="1082f-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="1082f-106">Po definování můžete znovu použít možnosti pokrytí zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="1082f-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="1082f-107">Můžete přidružit možnost k jednomu nebo více plánům.</span><span class="sxs-lookup"><span data-stu-id="1082f-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="1082f-108">Po definování možností pokrytí připojte možnosti pokrytí k typu plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="1082f-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="1082f-109">Typ plánu je poté přidružen k plánu zaměstnaneckých výhod nebo k programu.</span><span class="sxs-lookup"><span data-stu-id="1082f-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="1082f-110">Možnosti disponibility, které jsou přidruženy k typu plánu, jsou dostupné pro všechny plány vytvořené s tímto typem plánu.</span><span class="sxs-lookup"><span data-stu-id="1082f-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="1082f-111">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** **Možnosti pokrytí**.</span><span class="sxs-lookup"><span data-stu-id="1082f-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="1082f-112">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="1082f-112">Select **New**.</span></span>

3. <span data-ttu-id="1082f-113">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="1082f-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1082f-114">Pole</span><span class="sxs-lookup"><span data-stu-id="1082f-114">Field</span></span> | <span data-ttu-id="1082f-115">Popis</span><span class="sxs-lookup"><span data-stu-id="1082f-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1082f-116">**Možnost pokrytí**</span><span class="sxs-lookup"><span data-stu-id="1082f-116">**Coverage option**</span></span> | <span data-ttu-id="1082f-117">Jedinečný název možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="1082f-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="1082f-118">**Popis**</span><span class="sxs-lookup"><span data-stu-id="1082f-118">**Description**</span></span> | <span data-ttu-id="1082f-119">Popis možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="1082f-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="1082f-120">**Kód pokrytí**</span><span class="sxs-lookup"><span data-stu-id="1082f-120">**Coverage code**</span></span> | <span data-ttu-id="1082f-121">Kódy pokrytí přiřazují minimální a maximální částky každému typu osoby s nárokem na pokrytí.</span><span class="sxs-lookup"><span data-stu-id="1082f-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="1082f-122">Kód pokrytí indikuje, kdo má pokrytí nebo jaká částka pokrytí je povolena pro daný typ plánu.</span><span class="sxs-lookup"><span data-stu-id="1082f-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="1082f-123">Částku pokrytí lze vyjádřit jako částku v korunách nebo v procentech.</span><span class="sxs-lookup"><span data-stu-id="1082f-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="1082f-124">Například:</span><span class="sxs-lookup"><span data-stu-id="1082f-124">For example:</span></span></br></br><span data-ttu-id="1082f-125">- **Emp+1** – aby měl zaměstnanec nárok, musí mít vybranou jednu závislou osobu (pokud jich je vybráno více, nárok se ztrácí).</span><span class="sxs-lookup"><span data-stu-id="1082f-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="1082f-126">- **Emp+family** – abyste mohl mít zaměstnanec nárok, musí mít vybrané nejméně dvě závislé osoby.</span><span class="sxs-lookup"><span data-stu-id="1082f-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="1082f-127">**Maximální počet**</span><span class="sxs-lookup"><span data-stu-id="1082f-127">**Maximum number**</span></span> | <span data-ttu-id="1082f-128">Maximální počet závislých osob</span><span class="sxs-lookup"><span data-stu-id="1082f-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="1082f-129">**Stav**</span><span class="sxs-lookup"><span data-stu-id="1082f-129">**Status**</span></span> | <span data-ttu-id="1082f-130">Stav možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="1082f-130">The status of the coverage option.</span></span> <span data-ttu-id="1082f-131">Je-li stav možnosti pokrytí nastaven na hodnotu Neaktivní, nelze pro typy plánů vybrat možnost Pokrytí.</span><span class="sxs-lookup"><span data-stu-id="1082f-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="1082f-132">**Procento**</span><span class="sxs-lookup"><span data-stu-id="1082f-132">**Percent**</span></span> | <span data-ttu-id="1082f-133">Procentuální částka.</span><span class="sxs-lookup"><span data-stu-id="1082f-133">The percent amount.</span></span> <span data-ttu-id="1082f-134">Toto pole je aktivní pouze v případě, že v poli kód disponibility byla vybrána možnost % x mzdy.</span><span class="sxs-lookup"><span data-stu-id="1082f-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="1082f-135">**Dělitel**</span><span class="sxs-lookup"><span data-stu-id="1082f-135">**Divisor**</span></span> | <span data-ttu-id="1082f-136">Dělitel, který má být použit ve výpočtu po výběru kódu pokrytí % x platu.</span><span class="sxs-lookup"><span data-stu-id="1082f-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="1082f-137">**Minimální procento**</span><span class="sxs-lookup"><span data-stu-id="1082f-137">**Percent minimum**</span></span> | <span data-ttu-id="1082f-138">Minimální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="1082f-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="1082f-139">**Maximální procento**</span><span class="sxs-lookup"><span data-stu-id="1082f-139">**Percent maximum**</span></span> | <span data-ttu-id="1082f-140">Maximální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="1082f-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="1082f-141">Ve skupinovém rámečku **Možnosti nároku na osobní kontakt** připojte ke každé možnosti nároku odpovídající osobní kontakty.</span><span class="sxs-lookup"><span data-stu-id="1082f-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="1082f-142">V části **Samoobsluha** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="1082f-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="1082f-143">Pole</span><span class="sxs-lookup"><span data-stu-id="1082f-143">Field</span></span> | <span data-ttu-id="1082f-144">Popis</span><span class="sxs-lookup"><span data-stu-id="1082f-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1082f-145">**Povolit částku příspěvku zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="1082f-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="1082f-146">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku příspěvku na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="1082f-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="1082f-147">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky příspěvku, kterou zaměstnanec zadá do samoobsluhy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="1082f-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="1082f-148">**Povolit částku pokrytí zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="1082f-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="1082f-149">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku pokrytí na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="1082f-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="1082f-150">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky pokrytí, kterou zaměstnanec zadá do samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="1082f-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="1082f-151">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1082f-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]