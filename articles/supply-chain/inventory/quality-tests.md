---
title: Testy správy kvality
description: Toto téma popisuje, jak vytvořit testy, které bude možné použít pro objednávky kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021677"
---
# <a name="quality-management-tests"></a><span data-ttu-id="c24eb-103">Testy správy kvality</span><span class="sxs-lookup"><span data-stu-id="c24eb-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c24eb-104">Toto téma popisuje, jak vytvořit testy, které bude možné použít pro objednávky kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c24eb-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="c24eb-105">Stránku **Testy** použijete k definování a prohlížení individuálních testů, které zjišťují, zda vaše produkty splňují specifikace kvality.</span><span class="sxs-lookup"><span data-stu-id="c24eb-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="c24eb-106">Ke skupině testů můžete přiřadit jeden nebo více individuálních testů.</span><span class="sxs-lookup"><span data-stu-id="c24eb-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="c24eb-107">V tomto případě zadáte také informace specifické pro daný test, jako jsou například přijatelné hodnoty měření.</span><span class="sxs-lookup"><span data-stu-id="c24eb-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="c24eb-108">Naměřené hodnoty se používají pro testy množství.</span><span class="sxs-lookup"><span data-stu-id="c24eb-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="c24eb-109">Pro testy kvality se používají testovací proměnné.</span><span class="sxs-lookup"><span data-stu-id="c24eb-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="c24eb-110">Pro testy množství je pole **Typ** nastaveno na hodnotu *Celé číslo* nebo *Zlomek*.</span><span class="sxs-lookup"><span data-stu-id="c24eb-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="c24eb-111">Zadána je také měrná jednotka.</span><span class="sxs-lookup"><span data-stu-id="c24eb-111">A unit of measure is also specified.</span></span> <span data-ttu-id="c24eb-112">Specifikace kvality a výsledky testu jsou vyjádřeny jako čísla.</span><span class="sxs-lookup"><span data-stu-id="c24eb-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="c24eb-113">U testů kvality je pole **Typ** nastaveno na hodnotu *Možnost*.</span><span class="sxs-lookup"><span data-stu-id="c24eb-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="c24eb-114">Testy kvality vyžadují další informace o měřených testovacích proměnných a o výčtu jejich hodnot.</span><span class="sxs-lookup"><span data-stu-id="c24eb-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="c24eb-115">Specifikace kvality a výsledky testu jsou vyjádřeny v závislosti na výstupu.</span><span class="sxs-lookup"><span data-stu-id="c24eb-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="c24eb-116">Testovací přístroj lze volitelně přiřadit k testování.</span><span class="sxs-lookup"><span data-stu-id="c24eb-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="c24eb-117">Testovací přístroje však nejsou nutné k vytváření a používání testů s objednávkami kvality.</span><span class="sxs-lookup"><span data-stu-id="c24eb-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="c24eb-118">Další informace viz [Testovací přístroje pro řízení kvality](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="c24eb-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="c24eb-119">Můžete také volitelně určit jednotku pro test, abyste označili měrnou jednotku, ve které jsou zaznamenány výsledky testu.</span><span class="sxs-lookup"><span data-stu-id="c24eb-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="c24eb-120">Například test teploty může zahrnovat jednotku buď stupňů Fahrenheita, nebo stupňů Celsia.</span><span class="sxs-lookup"><span data-stu-id="c24eb-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="c24eb-121">Příklad testu</span><span class="sxs-lookup"><span data-stu-id="c24eb-121">Example of a test</span></span>

<span data-ttu-id="c24eb-122">Výrobní společnost provádí dva testy na zakoupeném materiálu: test množství ohledně kvality materiálu a test kvality ohledně poškození balení.</span><span class="sxs-lookup"><span data-stu-id="c24eb-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="c24eb-123">Tato společnost určuje další informace ohledně testu kvality s cílem definovat testovací proměnnou (například poškozené balení) a její výsledky.</span><span class="sxs-lookup"><span data-stu-id="c24eb-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="c24eb-124">Společnost používá stránku **Testovací skupiny** k přiřazení dvou testů do skupiny testů a k určení informací o daném testu.</span><span class="sxs-lookup"><span data-stu-id="c24eb-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="c24eb-125">Testovací skupina je přiřazena k objednávce kvality, takže daná společnost může vytvořit sestavu výsledků testů pro dané dva testy.</span><span class="sxs-lookup"><span data-stu-id="c24eb-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="c24eb-126">Vytvoření testu</span><span class="sxs-lookup"><span data-stu-id="c24eb-126">Create a test</span></span>

<span data-ttu-id="c24eb-127">Při vytváření testu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c24eb-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="c24eb-128">Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testy**.</span><span class="sxs-lookup"><span data-stu-id="c24eb-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="c24eb-129">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="c24eb-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c24eb-130">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="c24eb-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c24eb-131">**Test** – zadejte jedinečné ID nebo název testu.</span><span class="sxs-lookup"><span data-stu-id="c24eb-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="c24eb-132">**Popis** – zadejte podrobný popis testu.</span><span class="sxs-lookup"><span data-stu-id="c24eb-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="c24eb-133">**Typ** – vyberte typ výsledků, které test produkuje.</span><span class="sxs-lookup"><span data-stu-id="c24eb-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="c24eb-134">U testů množství vyberte *Zlomek* nebo *Celé číslo*.</span><span class="sxs-lookup"><span data-stu-id="c24eb-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="c24eb-135">U testů kvality vyberte hodnotu *Možnost*.</span><span class="sxs-lookup"><span data-stu-id="c24eb-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="c24eb-136">**Testovací přístroj** – vyberte [testovací přístroj](quality-test-instruments.md), který má být použit pro test.</span><span class="sxs-lookup"><span data-stu-id="c24eb-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="c24eb-137">**Jednotka** – pokud jste vybrali *Zlomek* nebo *Celé číslo* v poli **Typ** (tj. je-li testem test množství), vyberte měrnou jednotku, ve které by měly být zaznamenány výsledky testu.</span><span class="sxs-lookup"><span data-stu-id="c24eb-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="c24eb-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c24eb-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="c24eb-139">Po uložení testu již nebudete moci upravit pole **Typ** v mřížce.</span><span class="sxs-lookup"><span data-stu-id="c24eb-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="c24eb-140">Pokud musíte změnit typ výsledků testu, které budou pro test zaznamenány, vyberte v podokně akcí možnost **Změnit testovací typ kvality**.</span><span class="sxs-lookup"><span data-stu-id="c24eb-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="c24eb-141">V dialogovém okně **Změnit testovací typ kvality** nastavte pole **Nový typ** na požadovaný typ a poté výběrem tlačítka **OK** zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c24eb-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c24eb-142">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="c24eb-142">Additional resources</span></span>

- [<span data-ttu-id="c24eb-143">Testovací nástroje pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="c24eb-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="c24eb-144">Testovací skupiny pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="c24eb-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="c24eb-145">Testovací proměnné pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="c24eb-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="c24eb-146">Přiřazení kvality</span><span class="sxs-lookup"><span data-stu-id="c24eb-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
