---
title: Výpočty modelu konfigurace produktu
description: Toto téma popisuje, jak vytvořit výpočty pro atributy v modelu konfigurace produktu.
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829611"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="5aa07-103">Výpočty modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="5aa07-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aa07-104">Toto téma popisuje, jak vytvořit výpočty pro atributy v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5aa07-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="5aa07-105">Prerequisites</span></span>

<span data-ttu-id="5aa07-106">Výpočty se používají v modelu konfigurace produktu pro výpočet hodnot konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="5aa07-107">Než začnete nastavovat výpočty, musí existovat model konfigurace souvisejícího produktu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="5aa07-108">Přehled procesu nastavení konfiguračních modelů a souvisejících úkolů najdete v části [Nastavení modelu konfigurace produktu](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="5aa07-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="5aa07-109">Tvorba výpočtů</span><span class="sxs-lookup"><span data-stu-id="5aa07-109">Create a calculation</span></span>

<span data-ttu-id="5aa07-110">Výpočet se skládá z výrazu a cílového atributu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="5aa07-111">Další informace najdete v části [Výpočty pro modely konfigurace produktu - často kladené dotazy](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="5aa07-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="5aa07-112">Chcete-li vytvořit výpočet pro existující model produktu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5aa07-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="5aa07-113">Přejděte na **Řízení informací o produktech \> Společné \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="5aa07-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="5aa07-114">Otevřete model konfigurace produktu a zvolte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5aa07-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="5aa07-115">Na záložce s náhledem **Výpočty** vyberte **Přidat**, chcete-li přidat výpočet, a poté pro něj nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="5aa07-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="5aa07-116">**Název** - Zadejte název výpočtu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="5aa07-117">**Popis** - Zadejte popis výpočtu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="5aa07-118">**Cílový atribut** - Vyberte atribut, pro který provádíte výpočet.</span><span class="sxs-lookup"><span data-stu-id="5aa07-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="5aa07-119">Vyberte **Upravit výraz**.</span><span class="sxs-lookup"><span data-stu-id="5aa07-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="5aa07-120">V dialogovém okně **Zadat výpočet**, přidejte do výrazu požadované atributy, operátory a hodnoty.</span><span class="sxs-lookup"><span data-stu-id="5aa07-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="5aa07-121">Další informace o tom, jak pracovat s těmito prvky, najdete v části [Omezení výrazu a omezení tabulky v modelech konfigurace produktu](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="5aa07-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="5aa07-122">Když je váš výraz připraven, vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="5aa07-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="5aa07-123">Příklady výpočtů</span><span class="sxs-lookup"><span data-stu-id="5aa07-123">Calculation examples</span></span>

<span data-ttu-id="5aa07-124">Tato část poskytuje několik příkladů, které ukazují, jak výpočty fungují.</span><span class="sxs-lookup"><span data-stu-id="5aa07-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="5aa07-125">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="5aa07-125">Example 1</span></span>

<span data-ttu-id="5aa07-126">Atribut target má logickou hodnotu a výpočet používá následující podmíněný výraz:</span><span class="sxs-lookup"><span data-stu-id="5aa07-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="5aa07-127">Tento výraz vrací hodnotu *True* do cílového atributu, pokud je `decimalAttribute2` větší nebo rovno `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="5aa07-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="5aa07-128">V opačném případě vrátí hodnotu *False*.</span><span class="sxs-lookup"><span data-stu-id="5aa07-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="5aa07-129">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="5aa07-129">Example 2</span></span>

<span data-ttu-id="5aa07-130">Tento příklad používá textový atribut `textFixedList` jako cílový atribut.</span><span class="sxs-lookup"><span data-stu-id="5aa07-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="5aa07-131">Tento atribut obsahuje následující pevný seznam.</span><span class="sxs-lookup"><span data-stu-id="5aa07-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="5aa07-132">Hodnota</span><span class="sxs-lookup"><span data-stu-id="5aa07-132">Value</span></span> | <span data-ttu-id="5aa07-133">Hodnota řešitele</span><span class="sxs-lookup"><span data-stu-id="5aa07-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="5aa07-134">A</span><span class="sxs-lookup"><span data-stu-id="5aa07-134">A</span></span> | <span data-ttu-id="5aa07-135">1a</span><span class="sxs-lookup"><span data-stu-id="5aa07-135">1a</span></span> |
| <span data-ttu-id="5aa07-136">mld.</span><span class="sxs-lookup"><span data-stu-id="5aa07-136">B</span></span> | <span data-ttu-id="5aa07-137">2b</span><span class="sxs-lookup"><span data-stu-id="5aa07-137">2b</span></span> |
| <span data-ttu-id="5aa07-138">K</span><span class="sxs-lookup"><span data-stu-id="5aa07-138">C</span></span> | <span data-ttu-id="5aa07-139">2c</span><span class="sxs-lookup"><span data-stu-id="5aa07-139">2c</span></span> |

<span data-ttu-id="5aa07-140">Následující snímek obrazovky ukazuje, jak by nastavení tohoto atributu mohlo vypadat ve vašem systému.</span><span class="sxs-lookup"><span data-stu-id="5aa07-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="5aa07-141">![Nastavení typu atributu pro příklad 2](media/model-calculations-example2.png "Nastavení typu atributu pro příklad 2")</span><span class="sxs-lookup"><span data-stu-id="5aa07-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="5aa07-142">Atribut se používá v následujícím podmíněném příkazu:</span><span class="sxs-lookup"><span data-stu-id="5aa07-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="5aa07-143">Pokud je `integerAttribute` menší než 150, tento příkaz vrátí textovou hodnotu prvního záznamu v pevném seznamu *A*. V opačném případě vrátí textovou hodnotu třetího záznamu v pevném seznamu *C*.</span><span class="sxs-lookup"><span data-stu-id="5aa07-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="5aa07-144">Pevný seznam je ekvivalentní výčtu založenému na nule (enum) a k jeho hodnotám se přistupuje příslušnou celočíselnou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="5aa07-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="5aa07-145">Proto první pevná hodnota seznamu (*A*) odpovídá *0*, druhá hodnota (*B*) odpovídá *1* a třetí hodnota (*C*) odpovídá *2*.</span><span class="sxs-lookup"><span data-stu-id="5aa07-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="5aa07-146">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="5aa07-146">Example 3</span></span>

<span data-ttu-id="5aa07-147">Tento příklad používá cílový atribut `textFixedList` z předchozího příkladu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="5aa07-148">Používá také jiný textový atribut, `textAttribute`, který obsahuje následující pevný seznam.</span><span class="sxs-lookup"><span data-stu-id="5aa07-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="5aa07-149">Hodnota</span><span class="sxs-lookup"><span data-stu-id="5aa07-149">Value</span></span> | <span data-ttu-id="5aa07-150">Hodnota řešitele</span><span class="sxs-lookup"><span data-stu-id="5aa07-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="5aa07-151">AA</span><span class="sxs-lookup"><span data-stu-id="5aa07-151">AA</span></span> | <span data-ttu-id="5aa07-152">1aa</span><span class="sxs-lookup"><span data-stu-id="5aa07-152">1aa</span></span> |
| <span data-ttu-id="5aa07-153">BB</span><span class="sxs-lookup"><span data-stu-id="5aa07-153">BB</span></span> | <span data-ttu-id="5aa07-154">2bb</span><span class="sxs-lookup"><span data-stu-id="5aa07-154">2bb</span></span> |

<span data-ttu-id="5aa07-155">Následující snímek obrazovky ukazuje, jak by nastavení tohoto atributu mohlo vypadat ve vašem systému.</span><span class="sxs-lookup"><span data-stu-id="5aa07-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="5aa07-156">![Nastavení typu atributu pro příklad 3](media/model-calculations-example3.png "Nastavení typu atributu pro příklad 3")</span><span class="sxs-lookup"><span data-stu-id="5aa07-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="5aa07-157">Hodnota pro atribut `textFixedList` se počítá pomocí následujícího podmíněného příkazu:</span><span class="sxs-lookup"><span data-stu-id="5aa07-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="5aa07-158">Pokud hodnota `textAttribute` má hodnotu řešitele rovnající se *1aa*, tento výraz vrací textovou hodnotu prvního záznamu v pevném seznamu `textFixedList` *A*. V opačném případě vrátí textovou hodnotu třetího záznamu v pevném seznamu `textFixedList` *C*.</span><span class="sxs-lookup"><span data-stu-id="5aa07-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="5aa07-159">Podmíněný příkaz musí používat hodnotu řešitele atributu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="5aa07-160">Ve výpočtech lze použít pouze textové atributy pevného seznamu.</span><span class="sxs-lookup"><span data-stu-id="5aa07-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="5aa07-161">Viz také</span><span class="sxs-lookup"><span data-stu-id="5aa07-161">See also</span></span>

- [<span data-ttu-id="5aa07-162">Výpočty pro modely konfigurace produktu - často kladené dotazy</span><span class="sxs-lookup"><span data-stu-id="5aa07-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="5aa07-163">Přidání omezení výrazu do modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="5aa07-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="5aa07-164">Přehled modelů konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="5aa07-164">Product configuration models overview</span></span>](product-configuration-models.md)
