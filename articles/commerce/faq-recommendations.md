---
title: Často kladené dotazy k doporučení produktu
description: Toto téma obsahuje informace o procesech a nástrojích, které lze použít při řešení problémů souvisejících s doporučeními produktů nebo s jejich výsledky.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fa845f4d41e0bd7725349a216b9e4ee79efee79d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792408"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="d54d3-103">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="d54d3-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d54d3-104">Toto téma obsahuje informace o procesech a nástrojích, které lze použít při řešení problémů souvisejících s [doporučeními produktů](product-recommendations.md) nebo s jejich výsledky.</span><span class="sxs-lookup"><span data-stu-id="d54d3-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="d54d3-105">Doporučené postupy</span><span class="sxs-lookup"><span data-stu-id="d54d3-105">Best practices</span></span>
<span data-ttu-id="d54d3-106">Je velmi důležité používat koncept základních produktů a variant.</span><span class="sxs-lookup"><span data-stu-id="d54d3-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="d54d3-107">Praktické seskupení variant do nadřazeného základního produktu pomáhá vytvářet algoritmy a služby pro lepší modely.</span><span class="sxs-lookup"><span data-stu-id="d54d3-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="d54d3-108">Kromě toho může služba obsloužit pouze jednu instanci produktu namísto vkládání všech úzce souvisejících variant do seznamu.</span><span class="sxs-lookup"><span data-stu-id="d54d3-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="d54d3-109">Když jsou všechny úzce související varianty vloženy do seznamu, může dojít k chybám nebo duplicitním výsledkům.</span><span class="sxs-lookup"><span data-stu-id="d54d3-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="d54d3-110">Proč v seznamech doporučení chybějí produkty?</span><span class="sxs-lookup"><span data-stu-id="d54d3-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="d54d3-111">Obyčejně pokud v seznamu doporučení produktů chybí některá položka, může se jednat o problém s konfigurací produktu.</span><span class="sxs-lookup"><span data-stu-id="d54d3-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="d54d3-112">Může se například jednat o nesprávné počáteční nebo koncové datum produktu, může být nesprávně nakonfigurován rozměr nebo se produkt nemusí nacházet ve správném sortimentu kanálů atd.</span><span class="sxs-lookup"><span data-stu-id="d54d3-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="d54d3-113">Pokud položka chybí v seznamu doporučení, který vychází ze strojového učení na bázi umělé inteligence (AI-ML), položka pravděpodobně nesplňuje kritéria seznamu doporučení nebo nemá dostatek nákupních transakcí pro seznam doporučení, aby ji bylo možné zobrazit.</span><span class="sxs-lookup"><span data-stu-id="d54d3-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="d54d3-114">Doporučujeme, abyste provedli kontrolu následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="d54d3-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="d54d3-115">**Zkontrolujte, zda byla v centrále povolena doporučení produktu.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="d54d3-116">Další informace o povolení této služby naleznete v tématu [Povolení doporučení produktů](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="d54d3-117">**Zkontrolujte, zda jsou nastaveny klíčové vlastnosti produktu.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="d54d3-118">Například sortimenty výrobků musí být nastaveny tak, aby byly **zahrnuty**.</span><span class="sxs-lookup"><span data-stu-id="d54d3-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="d54d3-119">**U nově roztříděných produktů může trvat až 3 hodiny, než se produkt začne zobrazovat v novém seznamu.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="d54d3-120">**Pokud se produkt stále nezobrazuje v seznamech V kurzu, Nejprodávanější, Lidem se také líbí nebo Často zakoupeno společně, je možné, že tento produkt nemá dostatek transakcí.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="d54d3-121">V takovém případě můžete počkat, až se vyskytnou další transakce, aktualizovat výchozí parametry seznamu doporučení nebo pomocí ručního zásahu upravit výsledky seznamu doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="d54d3-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="d54d3-122">Další informace o parametrech doporučení naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="d54d3-123">**Ujistěte se, že produkt splňuje kritéria doporučení pro daný seznam.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="d54d3-124">Další informace o parametrech doporučení produktů naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="d54d3-125">Jak lze zabránit vrácení špatných výsledků doporučení?</span><span class="sxs-lookup"><span data-stu-id="d54d3-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="d54d3-126">Seznamy doporučení vyžadují k vytvoření výsledků velký objem transakcí.</span><span class="sxs-lookup"><span data-stu-id="d54d3-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="d54d3-127">Proto je důležité, aby uživatelé poskytovali úplná historická data transakcí.</span><span class="sxs-lookup"><span data-stu-id="d54d3-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="d54d3-128">Dále produkty, které nemají žádné nebo málo transakcí, obvykle nedosahují výsledků **Lidem se také líbí** nebo **Často zakoupeno společně** a nezobrazují se v seznamech doporučení **V kurzu** nebo **Nejprodávanější**.</span><span class="sxs-lookup"><span data-stu-id="d54d3-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="d54d3-129">Tato situace může často nastat u velmi nových nebo u starých produktů, které mají malý počet nákupů.</span><span class="sxs-lookup"><span data-stu-id="d54d3-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="d54d3-130">Populární nové položky snadno vyřeší tento problém.</span><span class="sxs-lookup"><span data-stu-id="d54d3-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="d54d3-131">Doporučujeme, abyste se řídili následujícími kroky:</span><span class="sxs-lookup"><span data-stu-id="d54d3-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="d54d3-132">**Ujistěte se, že produkt splňuje kritéria doporučení pro daný seznam.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="d54d3-133">Další informace o parametrech doporučení produktů naleznete v tématu Úprava výsledků doporučení produktů na základě umělé inteligence a strojového učení.</span><span class="sxs-lookup"><span data-stu-id="d54d3-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="d54d3-134">**Je-li produkt nový, zvažte úpravu seznamu doporučení, dokud produkt nemá více transakcí.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="d54d3-135">Další informace o úpravách výsledků seznamu doporučení naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="d54d3-136">**Ujistěte se, že produkt splňuje kritéria doporučení pro daný seznam.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="d54d3-137">Další informace o parametrech doporučení produktů naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="d54d3-138">**Je-li produkt nový, zvažte úpravu seznamu doporučení, dokud produkt nemá více transakcí.**</span><span class="sxs-lookup"><span data-stu-id="d54d3-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="d54d3-139">Další informace o úpravách výsledků seznamu doporučení naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="d54d3-140">Mohu produkt odebrat, aby se přesto zobrazoval v obchodě?</span><span class="sxs-lookup"><span data-stu-id="d54d3-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="d54d3-141">Můžete upravit seznamy, které jsou algoritmicky vygenerovány v případě obchodní potřeby.</span><span class="sxs-lookup"><span data-stu-id="d54d3-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="d54d3-142">Pokud je však produkt odebrán ze seznamu doporučení, bude produkt v obchodě stále vyhledatelný.</span><span class="sxs-lookup"><span data-stu-id="d54d3-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="d54d3-143">Další informace o úpravách výsledků doporučení produktů naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="d54d3-144">Pokud je nutné blokovat určitou položku v obchodě, aby ji nebylo možné vyhledat, je nutné změnit hodnotu **Sortimenty položek** tak, aby byla **vyloučena**.</span><span class="sxs-lookup"><span data-stu-id="d54d3-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="d54d3-145">Jak lze přidat seznam na stránku elektronického obchodu?</span><span class="sxs-lookup"><span data-stu-id="d54d3-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="d54d3-146">Informace o tom, jak přidat stránky doporučení produktů na web elektronického obchodování, naleznete v tématu [Přidání seznamů doporučení produktů na stránky](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="d54d3-147">Jak lze povolit doporučení v POS?</span><span class="sxs-lookup"><span data-stu-id="d54d3-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="d54d3-148">Po povolení doporučení produktů budete muset přidat panel doporučení na řídicí obrazovku POS.</span><span class="sxs-lookup"><span data-stu-id="d54d3-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="d54d3-149">Další informace viz [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="d54d3-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d54d3-150">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d54d3-150">Additional resources</span></span>

[<span data-ttu-id="d54d3-151">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="d54d3-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d54d3-152">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d54d3-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d54d3-153">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="d54d3-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d54d3-154">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="d54d3-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d54d3-155">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="d54d3-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d54d3-156">Povolit doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="d54d3-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="d54d3-157">Přidání doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="d54d3-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d54d3-158">Přidání doporučení na obrazovku transakcí</span><span class="sxs-lookup"><span data-stu-id="d54d3-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d54d3-159">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="d54d3-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d54d3-160">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="d54d3-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d54d3-161">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="d54d3-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]