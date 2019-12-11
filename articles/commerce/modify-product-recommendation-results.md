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
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770063"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="09020-103">Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení</span><span class="sxs-lookup"><span data-stu-id="09020-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="09020-104">V tomto tématu je vysvětleno, jak přizpůsobovat výsledky doporučení produktu na základě umělé inteligence-strojového učení (AI-ML) pro váš podnik.</span><span class="sxs-lookup"><span data-stu-id="09020-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="09020-105">Po povolení doporučení produktu budou výchozí nastavení účinná. Tyto parametry budou nebo mohou fungovat pro mnoho potřeb.</span><span class="sxs-lookup"><span data-stu-id="09020-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="09020-106">Je nejvhodnější naplánovat strávený čas k vyhodnocení, zda výsledky odpovídají prodejnímu pohybu produktů.</span><span class="sxs-lookup"><span data-stu-id="09020-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="09020-107">Před dalším provedením testování navrhujeme vyhodnocení výsledků za několik dní.</span><span class="sxs-lookup"><span data-stu-id="09020-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="09020-108">Principy parametrů seznamu doporučení</span><span class="sxs-lookup"><span data-stu-id="09020-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="09020-109">Před změnou parametrů se seznamte s tím, jak ovlivní výsledky níže.</span><span class="sxs-lookup"><span data-stu-id="09020-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="09020-110">Seznam trendujících produktů</span><span class="sxs-lookup"><span data-stu-id="09020-110">Trending product list</span></span>

<span data-ttu-id="09020-111">Seznam **Trendujících** produktů obsahuje dva parametry, které lze změnit: ![Příklad nastavení parametrů seznamu trendujíích produktů](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="09020-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="09020-112">**Zahrnout nové produkty z posledních X dnů** - produkty, které byly přidány do zadaného počtu dnů před aktuálním datem, lze použít k výběru kandidátů produktu.</span><span class="sxs-lookup"><span data-stu-id="09020-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="09020-113">Výchozí hodnota v obrázku naznačuje, že v seznamu produktů pro trend je možné použít produkty v rozmezí 180 dnů.</span><span class="sxs-lookup"><span data-stu-id="09020-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="09020-114">**Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů.</span><span class="sxs-lookup"><span data-stu-id="09020-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="09020-115">Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu trendujících produktů se použijí všechny nákupy produktu za posledních 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="09020-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="09020-116">Seznam nejlépe se prodávajících produktů</span><span class="sxs-lookup"><span data-stu-id="09020-116">Best selling product list</span></span>

<span data-ttu-id="09020-117">V závislosti na vaší společnosti může nejlepší prodej vést k různým výsledkům, než je trend, přestože obě používají data transakcí k objednání produktů.</span><span class="sxs-lookup"><span data-stu-id="09020-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="09020-118">Vzhledem k tomu, že nejlepší prodej nemá žádné přerušení na základě data sortimentu, je možné, že nejlepší prodeje budou stále obsahovat velmi populární starší produkty, které mohly být vyřazeny ze seznamu trendujících produktů.</span><span class="sxs-lookup"><span data-stu-id="09020-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="09020-119">Seznam **Nejlépe se prodávajících** produktů má jeden parametr, který lze změnit:</span><span class="sxs-lookup"><span data-stu-id="09020-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Příklad výchozího parametru seznamu nejlépe se prodávajících produktů](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="09020-121">**Zahrnout prodeje z posledních X dnů** - prodejní transakce, které se vyskytly během zadaného počtu dnů před aktuálním datem, lze použít k objednání produktů.</span><span class="sxs-lookup"><span data-stu-id="09020-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="09020-122">Výchozí hodnota výše naznačuje, že k určení umístění produktu v seznamu nejlépe se prodávajících produktů se použijí všechny nákupy produktu za posledních 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="09020-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="09020-123">Ručně přidat nebo odebrat produkty ze seznamů doporučení</span><span class="sxs-lookup"><span data-stu-id="09020-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="09020-124">Pro nové, trendující nebo nejlépe se prodávající</span><span class="sxs-lookup"><span data-stu-id="09020-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="09020-125">Přejděte na **Maloobchod** > **Doporučení prouktů** > **Parametry doporučení**.</span><span class="sxs-lookup"><span data-stu-id="09020-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="09020-126">V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.</span><span class="sxs-lookup"><span data-stu-id="09020-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="09020-127">Vyberte seznam, do kterého přidat či z kterého odebrat produkty.</span><span class="sxs-lookup"><span data-stu-id="09020-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="09020-128">Chcete-li přidat produkty do tabulky, vyberte možnost **Přidat řádek.**</span><span class="sxs-lookup"><span data-stu-id="09020-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="09020-129">Ve sloupci produkt vyhledejte produkt podle **Názvu** nebo **Čísla produktu**.
![Příklad hledání produktu v seznamu nových produktů](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="09020-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="09020-130">Ve sloupci Typ řádku vyberte jednu z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="09020-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="09020-131">**Zahrnout** – vynutí umístění produkt v předu na seznamu</span><span class="sxs-lookup"><span data-stu-id="09020-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="09020-132">**Vyloučit** – odebere produkt z tohoto seznamu ![Příklad zahrnutí nebo vyloučení produktu z nového seznamu produktů.](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="09020-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="09020-133">Při změně **Pořadí zobrazení** se změní pořadí, v jakém se produkty označené jako **zahrnout** objeví na seznamu.</span><span class="sxs-lookup"><span data-stu-id="09020-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="09020-134">Pokud mají dva produkty stejnou hodnotu **pořadí zobrazení**, pak se konečné pořadí těchto dvou výsledků může lišit od back office.</span><span class="sxs-lookup"><span data-stu-id="09020-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="09020-135">Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="09020-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="09020-136">Pro seznamy Lidem se také líbí a Často zakoupeno společně</span><span class="sxs-lookup"><span data-stu-id="09020-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="09020-137">V kontextu seznamů **Často zakoupeno společně** nebo **Lidem se také líbí** se strojní učení používá k analýze zákaznických vzorů nákupů, které doporučují související produkty často zakoupené společně pro jedinečný produkt typu seed.</span><span class="sxs-lookup"><span data-stu-id="09020-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="09020-138">**Produkt typu seed** je produkt, pro který chcete generovat výsledky.</span><span class="sxs-lookup"><span data-stu-id="09020-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="09020-139">V kontextu ruční úpravy seznamů doporučení přidáváte nebo odebíráte výsledky pro tento produkt.</span><span class="sxs-lookup"><span data-stu-id="09020-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="09020-140">Chcete-li ručně přidat nebo odebrat výsledky pro produkt typu seed, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="09020-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="09020-141">Vyberte **Produkt typu seed**.</span><span class="sxs-lookup"><span data-stu-id="09020-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="09020-142">Ve sloupci **Produkt** vyhledejte produkt podle **Názvu** nebo **Čísla produktu.**
![Příklad hledání produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="09020-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="09020-143">Ve sloupci **Typ řádku** vyberte jednu z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="09020-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="09020-144">**Zahrnout** – vynutí umístění produkt v předu na seznamu</span><span class="sxs-lookup"><span data-stu-id="09020-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="09020-145">**Vyloučit** – odebere produkt ze zobrazení v seznamu.</span><span class="sxs-lookup"><span data-stu-id="09020-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="09020-146">![Příklad zahrnutí nebo vyloučení produktu v seznamu Často zakoupeno společně](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="09020-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="09020-147">Odebrání produktů z tabulky: vyberte řádek, který chcete odebrat, a vyberte možnost Odstranit.</span><span class="sxs-lookup"><span data-stu-id="09020-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="09020-148">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="09020-148">Additional resources</span></span>

[<span data-ttu-id="09020-149">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="09020-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="09020-150">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="09020-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="09020-151">Přidání seznamů doporučení produktu na stránky</span><span class="sxs-lookup"><span data-stu-id="09020-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
