---
title: Testovací proměnné správy kvality
description: Toto téma popisuje, jak vytvořit testovací proměnné, které bude možné použít pro testy kvality na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021701"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="e14a2-103">Testovací proměnné správy kvality</span><span class="sxs-lookup"><span data-stu-id="e14a2-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e14a2-104">Toto téma popisuje, jak vytvořit testovací proměnné, které bude možné použít pro testy kvality na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e14a2-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e14a2-105">Pro každý test kvality definovaný na stránce **Testy** musíte definovat testovací proměnnou a její možné výstupy (výsledky).</span><span class="sxs-lookup"><span data-stu-id="e14a2-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="e14a2-106">(U testů kvality je nutné v poli **Typ** stránce **Testy** nastavit hodnotu *Možnost*.)</span><span class="sxs-lookup"><span data-stu-id="e14a2-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="e14a2-107">Stránku **Testovací proměnné** použijte k nastavení, úpravě nebo zobrazení možných výsledků pro testovací proměnnou, která je přidružena k testu kvality.</span><span class="sxs-lookup"><span data-stu-id="e14a2-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="e14a2-108">Každému výsledku přiřadíte stav výsledku *Úspěšné* nebo *Neúspěšné* k označení, zda je test úspěšný nebo neúspěšný, když je daný výsledek vybrán jako výsledek testu.</span><span class="sxs-lookup"><span data-stu-id="e14a2-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="e14a2-109">Stránku **Testovací skupiny** použijte k přiřazení testovací proměnné a výchozího výsledku k jednotlivému testu kvality.</span><span class="sxs-lookup"><span data-stu-id="e14a2-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="e14a2-110">Pro každou testovací proměnnou doporučujeme definovat alespoň dva výsledky: jeden, který má stav výsledku *Úspěšné* a ten, který má stav výsledku *Neúspěšné*.</span><span class="sxs-lookup"><span data-stu-id="e14a2-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="e14a2-111">Celkový počet proměnných nebo výsledků, které lze definovat, není nijak omezen.</span><span class="sxs-lookup"><span data-stu-id="e14a2-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="e14a2-112">Několik testů může navíc k zaznamenávání výsledků používat stejné testovací proměnné.</span><span class="sxs-lookup"><span data-stu-id="e14a2-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="e14a2-113">Příklady testovacích proměnných</span><span class="sxs-lookup"><span data-stu-id="e14a2-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="e14a2-114">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="e14a2-114">Example 1</span></span>

<span data-ttu-id="e14a2-115">Výrobní společnost provádí dva testy na vyráběných materiálech.</span><span class="sxs-lookup"><span data-stu-id="e14a2-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="e14a2-116">V jednom testu je hladina pH přiřazena k barevnému pruhu.</span><span class="sxs-lookup"><span data-stu-id="e14a2-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="e14a2-117">Přijatelné úrovně pH jsou ve světlejších barvách a nepřijatelné úrovně pH jsou v tmavších barvách.</span><span class="sxs-lookup"><span data-stu-id="e14a2-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="e14a2-118">V jiném testu se provádí několik vizuálních kontrol a pracovníci v oblasti kvality pomocí svého úsudku určují, zda položka vizuální kontrole vyhovuje nebo zda neprochází.</span><span class="sxs-lookup"><span data-stu-id="e14a2-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="e14a2-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="e14a2-119">Example 2</span></span>

<span data-ttu-id="e14a2-120">Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky.</span><span class="sxs-lookup"><span data-stu-id="e14a2-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="e14a2-121">Kontrolní test má několik proměnných.</span><span class="sxs-lookup"><span data-stu-id="e14a2-121">This inspection test has several variables.</span></span> <span data-ttu-id="e14a2-122">Jedna proměnná odpovídá chuti, přičemž možné výsledky pro tuto proměnnou jsou „dobrá“ a „špatná“.</span><span class="sxs-lookup"><span data-stu-id="e14a2-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="e14a2-123">Druhá proměnná odpovídá barvě, přičemž možné výsledky jsou „příliš tmavá“, „příliš světlá“ a „správná“.</span><span class="sxs-lookup"><span data-stu-id="e14a2-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="e14a2-124">Vytvoření testovací proměnné</span><span class="sxs-lookup"><span data-stu-id="e14a2-124">Create a test variable</span></span>

<span data-ttu-id="e14a2-125">Pokud chcete vytvořit testovací proměnnou, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="e14a2-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="e14a2-126">Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testovací proměnné**.</span><span class="sxs-lookup"><span data-stu-id="e14a2-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="e14a2-127">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="e14a2-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e14a2-128">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="e14a2-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e14a2-129">**Proměnná** – zadejte jedinečné ID nebo název proměnné.</span><span class="sxs-lookup"><span data-stu-id="e14a2-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="e14a2-130">**Popis** – zadejte podrobný popis proměnné.</span><span class="sxs-lookup"><span data-stu-id="e14a2-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="e14a2-131">Zatímco je stále vybrán nový řádek, vyberte v podokně akcí možnost **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="e14a2-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="e14a2-132">Na stránce **Výsledky testovacích proměnných** vyberte v podokně akcí možnost **Nový**, a přidejte tak řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="e14a2-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e14a2-133">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="e14a2-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e14a2-134">**Výsledek** – zadejte jedinečné ID nebo název výsledku.</span><span class="sxs-lookup"><span data-stu-id="e14a2-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="e14a2-135">**Popis** – zadejte podrobný popis výsledku.</span><span class="sxs-lookup"><span data-stu-id="e14a2-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="e14a2-136">**Stav výsledku** – vyberte buď hodnotu *Úspěšné*, nebo *Neúspěšné* k označení, zda je test úspěšný nebo neúspěšný, když je daný výsledek vybrán jako výsledek testu.</span><span class="sxs-lookup"><span data-stu-id="e14a2-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="e14a2-137">Opakujte předchozí krok pro každý další výsledek.</span><span class="sxs-lookup"><span data-stu-id="e14a2-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="e14a2-138">Ujistěte se, že alespoň jeden výsledek má stav výsledku *Úspěšné* a alespoň jeden má stav výsledku *Neúspěšné*.</span><span class="sxs-lookup"><span data-stu-id="e14a2-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="e14a2-139">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="e14a2-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e14a2-140">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="e14a2-140">Additional resources</span></span>

- [<span data-ttu-id="e14a2-141">Testovací nástroje pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="e14a2-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="e14a2-142">Testy správy kvality</span><span class="sxs-lookup"><span data-stu-id="e14a2-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="e14a2-143">Testovací skupiny pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="e14a2-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
