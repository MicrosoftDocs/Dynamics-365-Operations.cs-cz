---
title: "Výpočty pro modely konfigurace produktu - často kladené dotazy"
description: "Toto téma popisuje výpočty pro modely konfigurace produktu a vysvětluje, jak použít výpočty spolu s omezeními."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: daae96502f705f05076cb351aa1baefc37957803
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="calculations-for-product-configuration-models-faq"></a><span data-ttu-id="03f5a-103">Výpočty pro modely konfigurace produktu - často kladené dotazy</span><span class="sxs-lookup"><span data-stu-id="03f5a-103">Calculations for product configuration models FAQ</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="03f5a-104">Toto téma popisuje výpočty pro modely konfigurace produktu a vysvětluje, jak použít výpočty spolu s omezeními.</span><span class="sxs-lookup"><span data-stu-id="03f5a-104">This topic describes calculations for product configuration models and explains how to use calculations together with constraints.</span></span>

<span data-ttu-id="03f5a-105">Výpočty lze použít pro aritmetické nebo logické operace.</span><span class="sxs-lookup"><span data-stu-id="03f5a-105">Calculations can be used for arithmetic or logical operations.</span></span> <span data-ttu-id="03f5a-106">Doplňují omezení výrazu v modelech konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-106">They complement expression constraints in product configuration models.</span></span> <span data-ttu-id="03f5a-107">Je možné určit výpočty na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních** a pak vytvořit výrazy pro výpočty v editoru výrazu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-107">You can define calculations on the **Constraint-based product configuration model details** page and then build expressions for the calculations in the expression editor.</span></span> <span data-ttu-id="03f5a-108">Další informace viz Vytvořit výpočty.</span><span class="sxs-lookup"><span data-stu-id="03f5a-108">For more information, see Create calculations.</span></span>

## <a name="what-is-a-calculation"></a><span data-ttu-id="03f5a-109">Co je výpočet?</span><span class="sxs-lookup"><span data-stu-id="03f5a-109">What is a calculation?</span></span>
<span data-ttu-id="03f5a-110">Výpočet je prvek, který můžete použít v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-110">A calculation is an element that you can use in a product configuration model.</span></span> <span data-ttu-id="03f5a-111">Výpočty doplňují omezení tak, že vám při konfiguraci produktu umožňují pomocí desetinných čísel vypočítat hodnoty.</span><span class="sxs-lookup"><span data-stu-id="03f5a-111">Calculations complement constraints by letting you use decimal numbers to calculate values when you configure a product.</span></span> <span data-ttu-id="03f5a-112">Kromě toho výpočty mají k dispozici větší sadu operátorů než omezení.</span><span class="sxs-lookup"><span data-stu-id="03f5a-112">Additionally, calculations have a larger set of available operators than constraints have.</span></span>  

<span data-ttu-id="03f5a-113">Podobně jako omezení je výpočet přidružen k určité součásti ve modelu konfigurace produktu a nelze ho znovu použít nebo sdílet s jinou součástí.</span><span class="sxs-lookup"><span data-stu-id="03f5a-113">Like a constraint, a calculation is associated with a specific component in a product configuration model, and can’t be reused by or shared with another component.</span></span> <span data-ttu-id="03f5a-114">Jeden důležitý rozdíl mezi výpočty a omezení, je, že výpočty jsou imperativní (jednosměrné), zatímco omezení jsou deklarativní (obousměrné).</span><span class="sxs-lookup"><span data-stu-id="03f5a-114">One important difference between calculations and constraints is that calculations are imperative (unidirectional), whereas constraints are declarative (bi-directional).</span></span> <span data-ttu-id="03f5a-115">Další informace o omezení viz [Omezení výrazu a omezení tabulky](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="03f5a-115">For more information about constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span>  

<span data-ttu-id="03f5a-116">Výpočet se skládá z cílového atributu a vzorce výpočtu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-116">A calculation consists of a target attribute and a calculation expression.</span></span>

## <a name="what-is-a-target-attribute"></a><span data-ttu-id="03f5a-117">Co je cílový atribut?</span><span class="sxs-lookup"><span data-stu-id="03f5a-117">What is a target attribute?</span></span>
<span data-ttu-id="03f5a-118">Cílový atribut je atribut, který přijme výsledek výpočtu ve výrazu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-118">A target attribute is an attribute that receives the result of the calculation expression.</span></span>  

<span data-ttu-id="03f5a-119">V následujícím výrazu je cílový atribut měření ubrusu:</span><span class="sxs-lookup"><span data-stu-id="03f5a-119">In the following expression, the target attribute is a tablecloth measurement:</span></span>  

<span data-ttu-id="03f5a-120">**Výraz:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span><span class="sxs-lookup"><span data-stu-id="03f5a-120">**Expression:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span></span>  

<span data-ttu-id="03f5a-121">**DecimalAttribute1** je délka stolu a **decimalAttribute2** je délka ubrusu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-121">**DecimalAttribute1** is the table length, and **decimalAttribute2** is the tablecloth length.</span></span> <span data-ttu-id="03f5a-122">Výraz vrací hodnotu **True** do cílového atributu, pokud je **decimalAttribute2** větší nebo roven **decimalAttribute1**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-122">The expression returns the value **True** to the target attribute if **decimalAttribute2** is greater than or equal to **decimalAttribute1**.</span></span> <span data-ttu-id="03f5a-123">V opačném případě se výraz vrací hodnotu **Nepravda**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-123">Otherwise, the expression returns **False**.</span></span> <span data-ttu-id="03f5a-124">Měření ubrusu je tedy přípustné, pokud je délka ubrusu rovná nebo překračuje délku stolu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-124">Therefore, the tablecloth measurement is acceptable if the tablecloth length is the same as or exceeds the length of the table.</span></span>

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a><span data-ttu-id="03f5a-125">Které typy atributů lze nastavit jako cílové atributy?</span><span class="sxs-lookup"><span data-stu-id="03f5a-125">What attribute types can be set to target attributes?</span></span>
<span data-ttu-id="03f5a-126">Všechny typy atributů, které jsou podporovány pro konfigurátor výrobku lze nastavit jako cílové atributy kromě textu bez pevného seznamu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-126">All attribute types that the product configurator supports can be set to target attributes, except text without a fixed list.</span></span>

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a><span data-ttu-id="03f5a-127">Může hodnota pro cílový atribut omezit hodnoty vstupních atributů ve výpočtu?</span><span class="sxs-lookup"><span data-stu-id="03f5a-127">Can the value of a target attribute restrict the values of the input attributes in a calculation?</span></span>
<span data-ttu-id="03f5a-128">Ne. Hodnota pro cílový atribut nemůže omezit hodnoty vstupních atributů, protože výpočty jsou jednosměrné.</span><span class="sxs-lookup"><span data-stu-id="03f5a-128">No, the value of a target attribute can’t restrict the values of the input attributes, because calculations are unidirectional.</span></span> <span data-ttu-id="03f5a-129">Proto je hodnota cílového atributu nastavena podle změny hodnoty u vstupních atributů, ale změna hodnoty cíle neovlivní hodnotu vstupních atributů.</span><span class="sxs-lookup"><span data-stu-id="03f5a-129">Therefore, the value of the target attribute is set based on changes in the value of the input attributes, but a change in the value of the target doesn’t affect the value of the input attributes.</span></span> <span data-ttu-id="03f5a-130">Toto chování se liší od chování omezení.</span><span class="sxs-lookup"><span data-stu-id="03f5a-130">This behavior differs from the behavior for constraints.</span></span> <span data-ttu-id="03f5a-131">K omezení dochází oběma směry.</span><span class="sxs-lookup"><span data-stu-id="03f5a-131">Constraints occur in both directions.</span></span>

### <a name="example"></a><span data-ttu-id="03f5a-132">Příklad</span><span class="sxs-lookup"><span data-stu-id="03f5a-132">Example</span></span>

<span data-ttu-id="03f5a-133">V následujícím výrazu je cíl pro výpočet délka napájecího kabelu a vstupní hodnota je barva:</span><span class="sxs-lookup"><span data-stu-id="03f5a-133">In the following expression, the target for the calculation is the length of a power cord, and the input value is a color:</span></span>  

<span data-ttu-id="03f5a-134">**Výraz:** \[If Color == "Green", 1.5, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="03f5a-134">**Expression:** \[If Color == "Green", 1.5, 1.0\]</span></span>  

<span data-ttu-id="03f5a-135">Při konfiguraci položky je délka napájecího kabelu nastavena na **1.5**, zadáte-li **Green** jako hodnotu atributu barvy.</span><span class="sxs-lookup"><span data-stu-id="03f5a-135">When you configure the item, the length of the power cord is set to **1.5** if you specify **Green** as the value of color attribute.</span></span> <span data-ttu-id="03f5a-136">Pokud zadáte libovolnou jinou barvu, délka je nastavena na **1,0**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-136">If you specify any other color, the length is set to **1.0**.</span></span> <span data-ttu-id="03f5a-137">Vzhledem k tomu, že jsou výpočty jednosměrné, však výpočet nenastaví hodnotu atributu barva na **Zelená** při zadání délky **1,5**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-137">However, because calculations are unidirectional, the calculation doesn't set the value of the color attribute to **Green** if you specify a length of **1.5**.</span></span>

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a><span data-ttu-id="03f5a-138">Co se stane, má-li výpočet cílový atribut typu celé číslo, ale výpočet poskytne desetinné číslo?</span><span class="sxs-lookup"><span data-stu-id="03f5a-138">What happens if a calculation has a target attribute of the integer type but a calculation generates a decimal number?</span></span>
<span data-ttu-id="03f5a-139">Pokud cílový atribut je celé číslo, ale výpočet vygeneruje desetinné číslo, bude vrácena pouze část „celé číslo“ z výsledného výpočtu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-139">If a target attribute is of the integer type, but a calculation generates a decimal number, only the integer part of the calculated result is returned.</span></span> <span data-ttu-id="03f5a-140">Desetinná část bude odebrána, a výsledek nebude zaokrouhlen.</span><span class="sxs-lookup"><span data-stu-id="03f5a-140">The decimal part is removed, and the result isn't rounded.</span></span> <span data-ttu-id="03f5a-141">Například výsledek 12,70 se zobrazí jako 12.</span><span class="sxs-lookup"><span data-stu-id="03f5a-141">For example, a result of 12.70 is shown as 12.</span></span>

## <a name="when-do-calculations-occur"></a><span data-ttu-id="03f5a-142">Kdy dojde k výpočtům?</span><span class="sxs-lookup"><span data-stu-id="03f5a-142">When do calculations occur?</span></span>
<span data-ttu-id="03f5a-143">Výpočet proběhne při zadání hodnoty všech vstupních atributů.</span><span class="sxs-lookup"><span data-stu-id="03f5a-143">Calculations occur when a value has been provided for all input attributes.</span></span>

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a><span data-ttu-id="03f5a-144">Lze přepsat hodnotu, která byla vypočtena pro cílový atribut?</span><span class="sxs-lookup"><span data-stu-id="03f5a-144">Can I overwrite the value that is calculated for the target attribute?</span></span>
<span data-ttu-id="03f5a-145">Můžete přepsat hodnotu, která byla vypočtena pro cílový atribut, ledaže by byl cílový atribut nastaven jako skrytý nebo jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="03f5a-145">You can overwrite the value that is calculated for the target attribute, unless the target attribute is set as hidden or read-only.</span></span>

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a><span data-ttu-id="03f5a-146">Jak nastavím cílový atribut jako skrytý nebo jen pro čtení?</span><span class="sxs-lookup"><span data-stu-id="03f5a-146">How do I set a target attribute as hidden or read-only?</span></span>
<span data-ttu-id="03f5a-147">Pokud chcete nastavit atribut jako skrytý nebo jen pro čtení, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="03f5a-147">To set an attribute as hidden or read-only, follow these steps.</span></span>

1.  <span data-ttu-id="03f5a-148">Klikněte na **Řízení informací o produktech** &gt; **Společné** &gt; **Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-148">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="03f5a-149">Vyberte model konfigurace produktu a klepněte na panelu akcí na **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-149">Select a product configuration model, and then, on the Action Pane, click **Edit**.</span></span>
3.  <span data-ttu-id="03f5a-150">Na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních** vyberte atribut, který má být použit jako cílový atribut.</span><span class="sxs-lookup"><span data-stu-id="03f5a-150">On the **Constraint-based product configuration model details** page, select the attribute to use as a target attribute.</span></span>
4.  <span data-ttu-id="03f5a-151">Na pevné záložce **Atributy** vyberte **Skrytý** nebo **Jen pro čtení**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-151">On the **Attributes** FastTab, select **Hidden** or **Read-only**.</span></span>

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a><span data-ttu-id="03f5a-152">Může výpočet hodnoty přepsat mnou nastavené hodnoty?</span><span class="sxs-lookup"><span data-stu-id="03f5a-152">Can a calculation overwrite the values that I set?</span></span>
<span data-ttu-id="03f5a-153">Č.</span><span class="sxs-lookup"><span data-stu-id="03f5a-153">No.</span></span> <span data-ttu-id="03f5a-154">Hodnoty, které jste nastavili při konfiguraci produktu, jsou hodnoty, které budou použity.</span><span class="sxs-lookup"><span data-stu-id="03f5a-154">The values that you set when you configure a product are the values that are used.</span></span> <span data-ttu-id="03f5a-155">Výpočet, ke kterému dochází při změně vstupních hodnot ve výpočtu, nemůže přepsat hodnoty, které zadáte pro konkrétní atribut.</span><span class="sxs-lookup"><span data-stu-id="03f5a-155">The calculation that occurs when the input values in a calculation are changed can’t overwrite the values that you provide for a specific attribute.</span></span>

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a><span data-ttu-id="03f5a-156">Co se stane, odeberu-li vstupní hodnotu ve výpočtu?</span><span class="sxs-lookup"><span data-stu-id="03f5a-156">What happens if I remove an input value in a calculation?</span></span>
<span data-ttu-id="03f5a-157">Pokud odeberete vstupní hodnotu ve výpočtu, hodnota cílového atributu je rovněž odebrána.</span><span class="sxs-lookup"><span data-stu-id="03f5a-157">If you remove an input value in a calculation, the value of the target attribute is also removed.</span></span>

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a><span data-ttu-id="03f5a-158">Proč se zobrazila chybová zpráva s upozorněním, že tento model je v rozporu?</span><span class="sxs-lookup"><span data-stu-id="03f5a-158">Why do I receive an error message that says that my model is in contradiction?</span></span>
<span data-ttu-id="03f5a-159">Tato zpráva se zobrazí, když výpočet obsahuje chybu nebo v jedné nebo více omezeních existuje rozpor.</span><span class="sxs-lookup"><span data-stu-id="03f5a-159">This message is shown when a calculation includes an error, or when a contradiction exists in one or more constraints.</span></span> <span data-ttu-id="03f5a-160">Další informace o rozporech v omezeních viz [Omezení výrazu a omezení tabulky](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="03f5a-160">For more information about contradictions in constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span> <span data-ttu-id="03f5a-161">Zde jsou uvedeny situace, kdy může dojít k chybám ve výpočtu:</span><span class="sxs-lookup"><span data-stu-id="03f5a-161">Here are some situations where errors can occur in calculations:</span></span>

-   <span data-ttu-id="03f5a-162">Hodnota je dělena nulou.</span><span class="sxs-lookup"><span data-stu-id="03f5a-162">A value is divided by 0 (zero).</span></span>
-   <span data-ttu-id="03f5a-163">Došlo ke konfliktu mezi těmito dvěma prvky:</span><span class="sxs-lookup"><span data-stu-id="03f5a-163">A conflict exists between the following two elements:</span></span>
    -   <span data-ttu-id="03f5a-164">Hodnoty, které jsou k dispozici pro atribut a které jsou vymezeny omezením.</span><span class="sxs-lookup"><span data-stu-id="03f5a-164">The values that are available for an attribute and are limited by a constraint</span></span>
    -   <span data-ttu-id="03f5a-165">Hodnota, která je generována výpočtem.</span><span class="sxs-lookup"><span data-stu-id="03f5a-165">A value that is generated by a calculation</span></span>
-   <span data-ttu-id="03f5a-166">Hodnoty, které jsou vráceny výpočem, jsou mimo doménu atributu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-166">The values that are returned by the calculation are outside the domain of the attribute.</span></span> <span data-ttu-id="03f5a-167">Například celé číslo z \[1..10\], které je vypočítáno na hodnotu 0.</span><span class="sxs-lookup"><span data-stu-id="03f5a-167">An example is an integer from \[1..10\] that is calculated to 0.</span></span>

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a><span data-ttu-id="03f5a-168">Proč se zobrazila chybová zpráva i v případě, že tento model výrobku byl úspěšně ověřen?</span><span class="sxs-lookup"><span data-stu-id="03f5a-168">Why do I receive an error message even though I successfully validated my product model?</span></span>
<span data-ttu-id="03f5a-169">Výpočty nejsou zahrnuty do ověření.</span><span class="sxs-lookup"><span data-stu-id="03f5a-169">Calculations aren't included in the validation.</span></span> <span data-ttu-id="03f5a-170">Je nutné vyzkoušet model konfigurace produktu pro nalezení chyb při výpočtech.</span><span class="sxs-lookup"><span data-stu-id="03f5a-170">You must test the product configuration model to find errors in calculations.</span></span> <span data-ttu-id="03f5a-171">Následující postup umožňuje otestovat model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="03f5a-171">To test a product configuration model, follow these steps.</span></span>

1.  <span data-ttu-id="03f5a-172">Klikněte na **Řízení informací o produktech** &gt; **Společné** &gt; **Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-172">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="03f5a-173">Vyberte model konfigurace produktu a klepněte na panelu akcí ve skupině **Spustit** klikněte na **Test**.</span><span class="sxs-lookup"><span data-stu-id="03f5a-173">Select a product configuration model, and then, on the Action Pane, in the **Run** group, click **Test**.</span></span>





