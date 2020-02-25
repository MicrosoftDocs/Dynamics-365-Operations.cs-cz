---
title: Vytvoření možností pokrytí
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008300"
---
# <a name="create-coverage-options"></a><span data-ttu-id="014ad-102">Vytvoření možností pokrytí</span><span class="sxs-lookup"><span data-stu-id="014ad-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="014ad-103">Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody, jako je například zaměstnanec pro lékařský plán, nebo dvojnásobný plat pro plán životního pojištění.</span><span class="sxs-lookup"><span data-stu-id="014ad-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="014ad-104">Po definování jsou možnosti pokrytí zaměstnaneckých výhod opětovně použitelné a možnost lze přidružit k jednomu nebo více plánům.</span><span class="sxs-lookup"><span data-stu-id="014ad-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="014ad-105">Po definování možností pokrytí připojte možnosti pokrytí k typu plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="014ad-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="014ad-106">Typ plánu je poté přidružen k plánu zaměstnaneckých výhod nebo k programu.</span><span class="sxs-lookup"><span data-stu-id="014ad-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="014ad-107">Možnosti disponibility, které jsou přidruženy k typu plánu, budou dostupné pro všechny plány vytvořené s tímto typem plánu.</span><span class="sxs-lookup"><span data-stu-id="014ad-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="014ad-108">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** **Možnosti pokrytí**.</span><span class="sxs-lookup"><span data-stu-id="014ad-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="014ad-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="014ad-109">Select **New**.</span></span>

3. <span data-ttu-id="014ad-110">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="014ad-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="014ad-111">Pole</span><span class="sxs-lookup"><span data-stu-id="014ad-111">Field</span></span> | <span data-ttu-id="014ad-112">Popis</span><span class="sxs-lookup"><span data-stu-id="014ad-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="014ad-113">**Možnost pokrytí**</span><span class="sxs-lookup"><span data-stu-id="014ad-113">**Coverage option**</span></span> | <span data-ttu-id="014ad-114">Jedinečný název možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="014ad-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="014ad-115">**Popis**</span><span class="sxs-lookup"><span data-stu-id="014ad-115">**Description**</span></span> | <span data-ttu-id="014ad-116">Popis možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="014ad-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="014ad-117">**Kód pokrytí**</span><span class="sxs-lookup"><span data-stu-id="014ad-117">**Coverage code**</span></span> | <span data-ttu-id="014ad-118">Kódy pokrytí přiřazují minimální a maximální částky každému typu osoby s nárokem na pokrytí.</span><span class="sxs-lookup"><span data-stu-id="014ad-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="014ad-119">Kód pokrytí indikuje, kdo má pokrytí nebo jaká částka pokrytí je povolena pro daný typ plánu.</span><span class="sxs-lookup"><span data-stu-id="014ad-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="014ad-120">Částku pokrytí lze vyjádřit jako částku v korunách nebo v procentech.</span><span class="sxs-lookup"><span data-stu-id="014ad-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="014ad-121">Například:</span><span class="sxs-lookup"><span data-stu-id="014ad-121">For example:</span></span></br></br><span data-ttu-id="014ad-122">- **Emp+1** – aby měl zaměstnanec nárok, musí mít vybranou jednu závislou osobu (pokud jich je vybráno více, nárok se ztrácí).</span><span class="sxs-lookup"><span data-stu-id="014ad-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="014ad-123">- **Emp+family** – abyste mohl mít zaměstnanec nárok, musí mít vybrané nejméně dvě závislé osoby.</span><span class="sxs-lookup"><span data-stu-id="014ad-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="014ad-124">**Maximální počet**</span><span class="sxs-lookup"><span data-stu-id="014ad-124">**Maximum number**</span></span> | <span data-ttu-id="014ad-125">Maximální počet závislých osob</span><span class="sxs-lookup"><span data-stu-id="014ad-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="014ad-126">**Stav**</span><span class="sxs-lookup"><span data-stu-id="014ad-126">**Status**</span></span> | <span data-ttu-id="014ad-127">Stav možnosti pokrytí.</span><span class="sxs-lookup"><span data-stu-id="014ad-127">The status of the coverage option.</span></span> <span data-ttu-id="014ad-128">Je-li stav možnosti pokrytí nastaven na hodnotu Neaktivní, nelze pro typy plánů vybrat možnost Pokrytí.</span><span class="sxs-lookup"><span data-stu-id="014ad-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="014ad-129">**Procento**</span><span class="sxs-lookup"><span data-stu-id="014ad-129">**Percent**</span></span> | <span data-ttu-id="014ad-130">Procentuální částka.</span><span class="sxs-lookup"><span data-stu-id="014ad-130">The percent amount.</span></span> <span data-ttu-id="014ad-131">Toto pole je aktivní pouze v případě, že v poli kód disponibility byla vybrána možnost % x mzdy.</span><span class="sxs-lookup"><span data-stu-id="014ad-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="014ad-132">**Dělitel**</span><span class="sxs-lookup"><span data-stu-id="014ad-132">**Divisor**</span></span> | <span data-ttu-id="014ad-133">Dělitel, který má být použit ve výpočtu po výběru kódu pokrytí % x platu.</span><span class="sxs-lookup"><span data-stu-id="014ad-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="014ad-134">**Minimální procento**</span><span class="sxs-lookup"><span data-stu-id="014ad-134">**Percent minimum**</span></span> | <span data-ttu-id="014ad-135">Minimální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="014ad-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="014ad-136">**Maximální procento**</span><span class="sxs-lookup"><span data-stu-id="014ad-136">**Percent maximum**</span></span> | <span data-ttu-id="014ad-137">Maximální procento, když vyberete kód procentuálního pokrytí.</span><span class="sxs-lookup"><span data-stu-id="014ad-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="014ad-138">Ve skupinovém rámečku **Možnosti nároku na osobní kontakt** připojte ke každé možnosti nároku odpovídající osobní kontakty.</span><span class="sxs-lookup"><span data-stu-id="014ad-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="014ad-139">V části **Samoobsluha** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="014ad-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="014ad-140">Pole</span><span class="sxs-lookup"><span data-stu-id="014ad-140">Field</span></span> | <span data-ttu-id="014ad-141">Popis</span><span class="sxs-lookup"><span data-stu-id="014ad-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="014ad-142">**Povolit částku příspěvku zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="014ad-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="014ad-143">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku příspěvku na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="014ad-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="014ad-144">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky příspěvku, kterou zaměstnanec zadá do samoobsluhy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="014ad-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="014ad-145">**Povolit částku pokrytí zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="014ad-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="014ad-146">Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku pokrytí na samoobslužné služby.</span><span class="sxs-lookup"><span data-stu-id="014ad-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="014ad-147">Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky pokrytí, kterou zaměstnanec zadá do samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="014ad-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="014ad-148">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="014ad-148">Select **Save**.</span></span> 
