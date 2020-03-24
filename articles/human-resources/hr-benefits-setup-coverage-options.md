---
title: Vytvoření možností pokrytí
description: Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody, jako je například zaměstnanec pro lékařský plán, nebo dvojnásobný plat pro plán životního pojištění.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092699"
---
# <a name="create-coverage-options"></a><span data-ttu-id="f1477-103">Vytvoření možností pokrytí</span><span class="sxs-lookup"><span data-stu-id="f1477-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f1477-104">Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody, jako je například zaměstnanec pro lékařský plán, nebo dvojnásobný plat pro plán životního pojištění.</span><span class="sxs-lookup"><span data-stu-id="f1477-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="f1477-105">Po definování jsou možnosti pokrytí zaměstnaneckých výhod opětovně použitelné a možnost lze přidružit k jednomu nebo více plánům.</span><span class="sxs-lookup"><span data-stu-id="f1477-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="f1477-106">Po definování možností pokrytí připojte možnosti pokrytí k typu plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="f1477-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="f1477-107">Typ plánu je poté přidružen k plánu zaměstnaneckých výhod nebo k programu.</span><span class="sxs-lookup"><span data-stu-id="f1477-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="f1477-108">Možnosti disponibility, které jsou přidruženy k typu plánu, budou dostupné pro všechny plány vytvořené s tímto typem plánu.</span><span class="sxs-lookup"><span data-stu-id="f1477-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="f1477-109">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** **Možnosti pokrytí**.</span><span class="sxs-lookup"><span data-stu-id="f1477-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="f1477-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f1477-110">Select **New**.</span></span>

3. <span data-ttu-id="f1477-111">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="f1477-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f1477-112">Pole</span><span class="sxs-lookup"><span data-stu-id="f1477-112">Field</span></span> | <span data-ttu-id="f1477-113">Popis</span><span class="sxs-lookup"><span data-stu-id="f1477-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f1477-114">**Možnost pokrytí**</span><span class="sxs-lookup"><span data-stu-id="f1477-114">**Coverage option**</span></span> | <span data-ttu-id="f1477-115">Jedinečný název možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f1477-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="f1477-116">**Popis**</span><span class="sxs-lookup"><span data-stu-id="f1477-116">**Description**</span></span> | <span data-ttu-id="f1477-117">Popis možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f1477-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="f1477-118">**Kód pokrytí**</span><span class="sxs-lookup"><span data-stu-id="f1477-118">**Coverage code**</span></span> | <span data-ttu-id="f1477-119">Kódy pokrytí přiřazují minimální a maximální částky každému typu osoby s nárokem na pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f1477-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="f1477-120">Kód pokrytí indikuje, kdo má pokrytí nebo jaká částka pokrytí je povolena pro daný typ plánu.</span><span class="sxs-lookup"><span data-stu-id="f1477-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="f1477-121">Částku pokrytí lze vyjádřit jako částku v korunách nebo v procentech.</span><span class="sxs-lookup"><span data-stu-id="f1477-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="f1477-122">Například:</span><span class="sxs-lookup"><span data-stu-id="f1477-122">For example:</span></span></br></br><span data-ttu-id="f1477-123">- **Emp+1** – aby měl zaměstnanec nárok, musí mít vybranou jednu závislou osobu (pokud jich je vybráno více, nárok se ztrácí).</span><span class="sxs-lookup"><span data-stu-id="f1477-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="f1477-124">- **Emp+family** – abyste mohl mít zaměstnanec nárok, musí mít vybrané nejméně dvě závislé osoby.</span><span class="sxs-lookup"><span data-stu-id="f1477-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="f1477-125">**Maximální počet**</span><span class="sxs-lookup"><span data-stu-id="f1477-125">**Maximum number**</span></span> | <span data-ttu-id="f1477-126">Maximální počet závislých osob</span><span class="sxs-lookup"><span data-stu-id="f1477-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="f1477-127">**Stav**</span><span class="sxs-lookup"><span data-stu-id="f1477-127">**Status**</span></span> | <span data-ttu-id="f1477-128">Stav možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f1477-128">The status of the coverage option.</span></span> <span data-ttu-id="f1477-129">Je-li stav možnosti pokrytí nastaven na hodnotu Neaktivní, nelze pro typy plánů vybrat možnost Pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f1477-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="f1477-130">**Procento**</span><span class="sxs-lookup"><span data-stu-id="f1477-130">**Percent**</span></span> | <span data-ttu-id="f1477-131">Procentuální částka.</span><span class="sxs-lookup"><span data-stu-id="f1477-131">The percent amount.</span></span> <span data-ttu-id="f1477-132">Toto pole je aktivní pouze v případě, že v poli kód disponibility byla vybrána možnost % x mzdy.</span><span class="sxs-lookup"><span data-stu-id="f1477-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="f1477-133">**Dělitel**</span><span class="sxs-lookup"><span data-stu-id="f1477-133">**Divisor**</span></span> | <span data-ttu-id="f1477-134">Dělitel, který má být použit ve výpočtu po výběru kódu pokrytí % x platu.</span><span class="sxs-lookup"><span data-stu-id="f1477-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="f1477-135">**Minimální procento**</span><span class="sxs-lookup"><span data-stu-id="f1477-135">**Percent minimum**</span></span> | <span data-ttu-id="f1477-136">Minimální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f1477-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="f1477-137">**Maximální procento**</span><span class="sxs-lookup"><span data-stu-id="f1477-137">**Percent maximum**</span></span> | <span data-ttu-id="f1477-138">Maximální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="f1477-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="f1477-139">Ve skupinovém rámečku **Možnosti nároku na osobní kontakt** připojte ke každé možnosti nároku odpovídající osobní kontakty.</span><span class="sxs-lookup"><span data-stu-id="f1477-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="f1477-140">V části **Samoobsluha** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="f1477-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="f1477-141">Pole</span><span class="sxs-lookup"><span data-stu-id="f1477-141">Field</span></span> | <span data-ttu-id="f1477-142">Popis</span><span class="sxs-lookup"><span data-stu-id="f1477-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f1477-143">**Povolit částku příspěvku zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="f1477-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="f1477-144">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku příspěvku na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="f1477-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f1477-145">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky příspěvku, kterou zaměstnanec zadá do samoobsluhy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="f1477-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="f1477-146">**Povolit částku pokrytí zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="f1477-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="f1477-147">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku pokrytí na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="f1477-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f1477-148">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky pokrytí, kterou zaměstnanec zadá do samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f1477-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="f1477-149">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f1477-149">Select **Save**.</span></span> 
