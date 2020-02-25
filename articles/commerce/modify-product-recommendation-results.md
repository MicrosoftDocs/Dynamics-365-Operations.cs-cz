---
title: Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení
description: V tomto tématu je vysvětleno, jak přizpůsobovat výsledky doporučení produktu na základě umělé inteligence-strojového učení (AI-ML) pro váš podnik.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5da77f71fb2569adc011bb9ee9c8c795d85545f8
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024995"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="12ddd-103">Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení</span><span class="sxs-lookup"><span data-stu-id="12ddd-103">Manage AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="12ddd-104">V tomto tématu je vysvětleno, jak přizpůsobovat výsledky doporučení produktu na základě umělé inteligence-strojového učení (AI-ML) pro váš podnik.</span><span class="sxs-lookup"><span data-stu-id="12ddd-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="12ddd-105">Po povolení doporučení produktu budou výchozí nastavení účinná. Tyto parametry budou nebo mohou fungovat pro mnoho potřeb.</span><span class="sxs-lookup"><span data-stu-id="12ddd-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="12ddd-106">Je nejvhodnější naplánovat strávený čas k vyhodnocení, zda výsledky odpovídají prodejnímu pohybu produktů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="12ddd-107">Před dalším provedením testování navrhujeme vyhodnocení výsledků za několik dní.</span><span class="sxs-lookup"><span data-stu-id="12ddd-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="12ddd-108">Principy parametrů seznamu doporučení</span><span class="sxs-lookup"><span data-stu-id="12ddd-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="12ddd-109">Před změnou parametrů se seznamte s tím, jak ovlivní výsledky níže.</span><span class="sxs-lookup"><span data-stu-id="12ddd-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="12ddd-110">Seznam "trendových" produktů</span><span class="sxs-lookup"><span data-stu-id="12ddd-110">"Trending" product list</span></span>

<span data-ttu-id="12ddd-111">Seznam "trendových" produktů má dva parametry, které lze změnit:</span><span class="sxs-lookup"><span data-stu-id="12ddd-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Příklad výchozích parametrů seznamu "trendů"](./media/exampletrendingparameters.png)

1. <span data-ttu-id="12ddd-113">**Zahrnout nové produkty z posledních X dnů** - produkty, které byly přidány do zadaného počtu dnů před aktuálním datem, lze použít k výběru kandidátů produktu.</span><span class="sxs-lookup"><span data-stu-id="12ddd-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="12ddd-114">Výchozí hodnota v obrázku naznačuje, že v seznamu produktů pro trend je možné použít produkty v rozmezí 180 dnů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="12ddd-115">**Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="12ddd-116">Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu trendujících produktů se použijí všechny nákupy produktu za posledních 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="12ddd-117">Seznam "nejlépe prodávaných" produktů</span><span class="sxs-lookup"><span data-stu-id="12ddd-117">"Best selling" product list</span></span>

<span data-ttu-id="12ddd-118">V závislosti na vaší společnosti může seznam "nejlépe prodávaných produktů" vést k jiným výsledkům, než je trend, přestože oba používají data transakcí k objednání produktů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="12ddd-119">Vzhledem k tomu, že nejlepší prodej nemá žádné přerušení na základě data sortimentu, je možné, že nejlepší prodeje budou stále obsahovat velmi populární starší produkty, které mohly být vyřazeny ze seznamu trendujících produktů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="12ddd-120">Seznam "nejlépe prodávaných" produktů má jeden parametr, který lze změnit:</span><span class="sxs-lookup"><span data-stu-id="12ddd-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Příklad výchozího parametru seznamu nejlépe se prodávajících produktů](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="12ddd-122">**Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="12ddd-123">Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu nejlépe se prodávajících produktů se použijí všechny nákupy produktu za posledních 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="12ddd-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="12ddd-124">Ručně přidat nebo odebrat produkty ze seznamů doporučení</span><span class="sxs-lookup"><span data-stu-id="12ddd-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="12ddd-125">Pro nové, trendující nebo nejlépe prodávané</span><span class="sxs-lookup"><span data-stu-id="12ddd-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="12ddd-126">Přejděte na **Maloobchod a velkoobchod** > **Doporučení produktů** > **Parametry doporučení**.</span><span class="sxs-lookup"><span data-stu-id="12ddd-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="12ddd-127">V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.</span><span class="sxs-lookup"><span data-stu-id="12ddd-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="12ddd-128">Vyberte seznam, do kterého přidat či z kterého odebrat produkty.</span><span class="sxs-lookup"><span data-stu-id="12ddd-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="12ddd-129">Chcete-li přidat produkty do tabulky, vyberte možnost **Přidat řádek.**</span><span class="sxs-lookup"><span data-stu-id="12ddd-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="12ddd-130">Ve sloupci produkt vyhledejte produkt podle **názvu** nebo **čísla produktu**.</span><span class="sxs-lookup"><span data-stu-id="12ddd-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Příklad hledání produktu v novém seznamu produktů](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="12ddd-132">Ve sloupci Typ řádku vyberte jednu z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="12ddd-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="12ddd-133">**Zahrnout** – vynutí umístění produkt v předu na seznamu</span><span class="sxs-lookup"><span data-stu-id="12ddd-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="12ddd-134">**Vyloučit** – odebere produkt ze zobrazení v seznamu.</span><span class="sxs-lookup"><span data-stu-id="12ddd-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Příklad zahrnutí nebo vyloučení produktu z nového seznamu produktů](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="12ddd-136">Při změně **Pořadí zobrazení** se změní pořadí, v jakém se produkty označené jako **zahrnout** objeví na seznamu.</span><span class="sxs-lookup"><span data-stu-id="12ddd-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="12ddd-137">Pokud mají dva produkty stejnou hodnotu **pořadí zobrazení**, pak se konečné pořadí těchto dvou výsledků může lišit od back office.</span><span class="sxs-lookup"><span data-stu-id="12ddd-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="12ddd-138">Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="12ddd-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="12ddd-139">Pro seznamy Lidem se také líbí a Často zakoupeno společně</span><span class="sxs-lookup"><span data-stu-id="12ddd-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="12ddd-140">V kontextu seznamů Často zakoupeno společně nebo Lidem se také líbí se strojní učení používá k analýze zákaznických vzorů nákupů, které doporučují související produkty často zakoupené společně pro jedinečný produkt typu seed.</span><span class="sxs-lookup"><span data-stu-id="12ddd-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="12ddd-141">*Produkt typu seed* je produkt, pro který chcete generovat výsledky.</span><span class="sxs-lookup"><span data-stu-id="12ddd-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="12ddd-142">V kontextu ruční úpravy seznamů doporučení přidáváte nebo odebíráte výsledky pro tento produkt.</span><span class="sxs-lookup"><span data-stu-id="12ddd-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="12ddd-143">Chcete-li ručně přidat nebo odebrat výsledky pro produkt typu seed, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="12ddd-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="12ddd-144">Vyberte **Produkt typu seed**.</span><span class="sxs-lookup"><span data-stu-id="12ddd-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="12ddd-145">Ve sloupci **Produkt** vyhledejte produkt podle **Názvu** nebo **Čísla produktu.**
![Příklad hledání produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="12ddd-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="12ddd-146">Ve sloupci **Typ řádku** vyberte jednu z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="12ddd-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="12ddd-147">**Zahrnout** – vynutí umístění produkt v předu na seznamu</span><span class="sxs-lookup"><span data-stu-id="12ddd-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="12ddd-148">**Vyloučit** – odebere produkt ze zobrazení v seznamu.</span><span class="sxs-lookup"><span data-stu-id="12ddd-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="12ddd-149">![Příklad zahrnutí nebo vyloučení produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="12ddd-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="12ddd-150">Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost Odstranit.</span><span class="sxs-lookup"><span data-stu-id="12ddd-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="12ddd-151">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="12ddd-151">Additional resources</span></span>

[<span data-ttu-id="12ddd-152">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="12ddd-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="12ddd-153">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="12ddd-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="12ddd-154">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="12ddd-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="12ddd-155">Přidání seznamů doporučení produktu na stránky</span><span class="sxs-lookup"><span data-stu-id="12ddd-155">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="12ddd-156">Přehled modulu kolekce produktů</span><span class="sxs-lookup"><span data-stu-id="12ddd-156">Product collection module overview</span></span>](product-collection-module-overview.md)
