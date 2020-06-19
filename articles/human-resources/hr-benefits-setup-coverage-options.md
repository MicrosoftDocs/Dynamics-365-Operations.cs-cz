---
title: Vytvoření možností pokrytí
description: Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 8690dbe00c2316ccf745f5222c3cbaa9c3379f85
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430732"
---
# <a name="create-coverage-options"></a><span data-ttu-id="f37a9-103">Vytvoření možností pokrytí</span><span class="sxs-lookup"><span data-stu-id="f37a9-103">Create coverage options</span></span>

<span data-ttu-id="f37a9-104">Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="f37a9-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="f37a9-105">Možnosti pokrytí mohou například zahrnovat **pouze zaměstnance** pro lékařský plán nebo **2x plat** pro plán životního pojištění.</span><span class="sxs-lookup"><span data-stu-id="f37a9-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="f37a9-106">Po definování můžete znovu použít možnosti pokrytí zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="f37a9-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="f37a9-107">Můžete přidružit možnost k jednomu nebo více plánům.</span><span class="sxs-lookup"><span data-stu-id="f37a9-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="f37a9-108">Po definování možností pokrytí připojte možnosti pokrytí k typu plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="f37a9-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="f37a9-109">Typ plánu je poté přidružen k plánu zaměstnaneckých výhod nebo k programu.</span><span class="sxs-lookup"><span data-stu-id="f37a9-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="f37a9-110">Možnosti disponibility, které jsou přidruženy k typu plánu, jsou dostupné pro všechny plány vytvořené s tímto typem plánu.</span><span class="sxs-lookup"><span data-stu-id="f37a9-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="f37a9-111">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** **Možnosti pokrytí**.</span><span class="sxs-lookup"><span data-stu-id="f37a9-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="f37a9-112">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f37a9-112">Select **New**.</span></span>

3. <span data-ttu-id="f37a9-113">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="f37a9-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f37a9-114">Pole</span><span class="sxs-lookup"><span data-stu-id="f37a9-114">Field</span></span> | <span data-ttu-id="f37a9-115">Popis</span><span class="sxs-lookup"><span data-stu-id="f37a9-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f37a9-116">**Možnost pokrytí**</span><span class="sxs-lookup"><span data-stu-id="f37a9-116">**Coverage option**</span></span> | <span data-ttu-id="f37a9-117">Jedinečný název možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f37a9-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="f37a9-118">**Popis**</span><span class="sxs-lookup"><span data-stu-id="f37a9-118">**Description**</span></span> | <span data-ttu-id="f37a9-119">Popis možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f37a9-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="f37a9-120">**Kód pokrytí**</span><span class="sxs-lookup"><span data-stu-id="f37a9-120">**Coverage code**</span></span> | <span data-ttu-id="f37a9-121">Kódy pokrytí přiřazují minimální a maximální částky každému typu osoby s nárokem na pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f37a9-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="f37a9-122">Kód pokrytí indikuje, kdo má pokrytí nebo jaká částka pokrytí je povolena pro daný typ plánu.</span><span class="sxs-lookup"><span data-stu-id="f37a9-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="f37a9-123">Částku pokrytí lze vyjádřit jako částku v korunách nebo v procentech.</span><span class="sxs-lookup"><span data-stu-id="f37a9-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="f37a9-124">Například:</span><span class="sxs-lookup"><span data-stu-id="f37a9-124">For example:</span></span></br></br><span data-ttu-id="f37a9-125">- **Emp+1** – aby měl zaměstnanec nárok, musí mít vybranou jednu závislou osobu (pokud jich je vybráno více, nárok se ztrácí).</span><span class="sxs-lookup"><span data-stu-id="f37a9-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="f37a9-126">- **Emp+family** – abyste mohl mít zaměstnanec nárok, musí mít vybrané nejméně dvě závislé osoby.</span><span class="sxs-lookup"><span data-stu-id="f37a9-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="f37a9-127">**Maximální počet**</span><span class="sxs-lookup"><span data-stu-id="f37a9-127">**Maximum number**</span></span> | <span data-ttu-id="f37a9-128">Maximální počet závislých osob</span><span class="sxs-lookup"><span data-stu-id="f37a9-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="f37a9-129">**Stav**</span><span class="sxs-lookup"><span data-stu-id="f37a9-129">**Status**</span></span> | <span data-ttu-id="f37a9-130">Stav možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f37a9-130">The status of the coverage option.</span></span> <span data-ttu-id="f37a9-131">Je-li stav možnosti pokrytí nastaven na hodnotu Neaktivní, nelze pro typy plánů vybrat možnost Pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f37a9-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="f37a9-132">**Procento**</span><span class="sxs-lookup"><span data-stu-id="f37a9-132">**Percent**</span></span> | <span data-ttu-id="f37a9-133">Procentuální částka.</span><span class="sxs-lookup"><span data-stu-id="f37a9-133">The percent amount.</span></span> <span data-ttu-id="f37a9-134">Toto pole je aktivní pouze v případě, že v poli kód disponibility byla vybrána možnost % x mzdy.</span><span class="sxs-lookup"><span data-stu-id="f37a9-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="f37a9-135">**Dělitel**</span><span class="sxs-lookup"><span data-stu-id="f37a9-135">**Divisor**</span></span> | <span data-ttu-id="f37a9-136">Dělitel, který má být použit ve výpočtu po výběru kódu pokrytí % x platu.</span><span class="sxs-lookup"><span data-stu-id="f37a9-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="f37a9-137">**Minimální procento**</span><span class="sxs-lookup"><span data-stu-id="f37a9-137">**Percent minimum**</span></span> | <span data-ttu-id="f37a9-138">Minimální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f37a9-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="f37a9-139">**Maximální procento**</span><span class="sxs-lookup"><span data-stu-id="f37a9-139">**Percent maximum**</span></span> | <span data-ttu-id="f37a9-140">Maximální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f37a9-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="f37a9-141">Ve skupinovém rámečku **Možnosti nároku na osobní kontakt** připojte ke každé možnosti nároku odpovídající osobní kontakty.</span><span class="sxs-lookup"><span data-stu-id="f37a9-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="f37a9-142">V části **Samoobsluha** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="f37a9-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="f37a9-143">Pole</span><span class="sxs-lookup"><span data-stu-id="f37a9-143">Field</span></span> | <span data-ttu-id="f37a9-144">Popis</span><span class="sxs-lookup"><span data-stu-id="f37a9-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f37a9-145">**Povolit částku příspěvku zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="f37a9-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="f37a9-146">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku příspěvku na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="f37a9-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f37a9-147">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky příspěvku, kterou zaměstnanec zadá do samoobsluhy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="f37a9-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="f37a9-148">**Povolit částku pokrytí zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="f37a9-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="f37a9-149">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku pokrytí na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="f37a9-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f37a9-150">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky pokrytí, kterou zaměstnanec zadá do samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f37a9-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="f37a9-151">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f37a9-151">Select **Save**.</span></span> 
