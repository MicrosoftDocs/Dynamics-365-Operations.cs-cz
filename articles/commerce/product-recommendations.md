---
title: Přehled doporučení produktu
description: V tomto tématu jsou obecné informace o doporučování produktů. Doporučení produktů umožňují zákazníkům snadno a rychle vyhledat produkty, které chtějí, a také produkty, které původně nechtěly nakupovat.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5aa7db8e53906f9e1416b912fe2c3b70d5430258
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664875"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="7e37d-104">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="7e37d-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e37d-105">Microsoft Dynamics 365 Commerce lze použít k zobrazení doporučení produktů na webu e-Commerce a v zařízení pro prodej na místě (POS).</span><span class="sxs-lookup"><span data-stu-id="7e37d-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="7e37d-106">Doporučení produktu jsou položky, o které se může zákazník zajímat.</span><span class="sxs-lookup"><span data-stu-id="7e37d-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="7e37d-107">Doporučení jsou založena na trendech nákupu ostatních zákazníků v online i kamených obchodech.</span><span class="sxs-lookup"><span data-stu-id="7e37d-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="7e37d-108">Doporučení produktů umožňují zákazníkům snadno a rychle najít produkty, které chtějí, a u toho mají pozitivní zkušenosti.</span><span class="sxs-lookup"><span data-stu-id="7e37d-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="7e37d-109">Křížový prodej a návazný prodej může dokonce zákazníkům pomoci najít další produkty, než které původně nakupují.</span><span class="sxs-lookup"><span data-stu-id="7e37d-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="7e37d-110">Pokud se při zjišťování produktů používají doporučení, mohou vytvářet více možností převodu, pomoci zvýšit výnosy z prodeje a dokonce také zvýšit spokojenost a uchování zákazníků.</span><span class="sxs-lookup"><span data-stu-id="7e37d-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="7e37d-111">V platformě e-Commerce doporučení produktů využívají technologie strojového učení Microsoft Recommendations ve velkém měřítku.</span><span class="sxs-lookup"><span data-stu-id="7e37d-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="7e37d-112">Služba doporučení</span><span class="sxs-lookup"><span data-stu-id="7e37d-112">Recommendation service</span></span>

<span data-ttu-id="7e37d-113">Služba doporučení produktů používá technologie umělé inteligence a strojového učení (AI-ML) následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="7e37d-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="7e37d-114">Data ve formátu vyžadovaném službami Recommendation jsou extrahována z pracovní databáze Commerce a odeslána do Azure Data Lake Storage nebo úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="7e37d-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="7e37d-115">Služba doporučení používá tato uložená data k trénování modelů doporučení pro seznamy **Lidem se také líbí**, **Často zakoupené společně**, **Nový**, **Nejprodávanější** a **Trendující**.</span><span class="sxs-lookup"><span data-stu-id="7e37d-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="7e37d-116">Scénáře</span><span class="sxs-lookup"><span data-stu-id="7e37d-116">Scenarios</span></span>

<span data-ttu-id="7e37d-117">Doporučení produktu jsou dostupná pro následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="7e37d-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="7e37d-118">**Na libovolné stránce obchodu pro procházení nebo cílovou stránku v e-Commerce:** Pokud zákazníci nebo pracovníci obchodu navštíví stránku obchodu, může modul doporučení navrhovat produkty v seznamech **Nový**, **Nejprodávanější**a **Trendující**.</span><span class="sxs-lookup"><span data-stu-id="7e37d-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="7e37d-119">**Na stránce Podrobnosti produktu:** Pokud zákaznící nebo pracovníci obchodu navštíví stránku **Podrobnosti produktu**, nabídne modul doporučení další položky, které se také mohou nakoupit.</span><span class="sxs-lookup"><span data-stu-id="7e37d-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="7e37d-120">Tyto položky se zobrazí v seznamu **Lidem se také líbí**.</span><span class="sxs-lookup"><span data-stu-id="7e37d-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="7e37d-121">**Na stránce transakce nebo na stránce s pokladnou:** modul doporučení navrhuje položky na základě celého seznamu položek v nákupním košíku.</span><span class="sxs-lookup"><span data-stu-id="7e37d-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="7e37d-122">Tyto položky se zobrazí v seznamu **Často zakoupené společně**.</span><span class="sxs-lookup"><span data-stu-id="7e37d-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="7e37d-123">**Přizpůsobená doporučení:** Maloobchodníci mohou poskytnout přihlášeným zákazníkům seznam **přizpůsobených možností** a také nové funkce, které umožňují, aby byly existující scénáře seznamu přizpůsobeny na základě tohoto odběratele.</span><span class="sxs-lookup"><span data-stu-id="7e37d-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="7e37d-124">Chcete-li zjistit více, přečtěte si téma [Povolení přizpůsobených doporučení](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="7e37d-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="7e37d-125">Typy doporučení produktů</span><span class="sxs-lookup"><span data-stu-id="7e37d-125">Types of product recommendations</span></span>

<span data-ttu-id="7e37d-126">V následující tabulce jsou popsány různé typy automatických doporučení produktů, které jsou k dispozici pro maloobchodní prodejce k implementaci do řešení Dynamics 365 Commerce prostřednictvím [modulu kolekce produktů](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7e37d-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="7e37d-127">Maloobchodníci mohou také zobrazit individuální výsledky pro přihlášeného uživatele, pokud tuto možnost zvolí autor webu.</span><span class="sxs-lookup"><span data-stu-id="7e37d-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="7e37d-128">Modul kolekce produktů</span><span class="sxs-lookup"><span data-stu-id="7e37d-128">Product collection module</span></span>  | <span data-ttu-id="7e37d-129">Typ</span><span class="sxs-lookup"><span data-stu-id="7e37d-129">Type</span></span> | <span data-ttu-id="7e37d-130">popis</span><span class="sxs-lookup"><span data-stu-id="7e37d-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="7e37d-131">Nová</span><span class="sxs-lookup"><span data-stu-id="7e37d-131">New</span></span>                        | <span data-ttu-id="7e37d-132">Algoritmický</span><span class="sxs-lookup"><span data-stu-id="7e37d-132">Algorithmic</span></span> | <span data-ttu-id="7e37d-133">Tento modul zobrazuje seznam nejnovějších produktů, které byly nedávno roztříděny do kanálů a katalogů.</span><span class="sxs-lookup"><span data-stu-id="7e37d-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="7e37d-134">Nejprodávanější</span><span class="sxs-lookup"><span data-stu-id="7e37d-134">Best selling</span></span>               | <span data-ttu-id="7e37d-135">Algoritmický</span><span class="sxs-lookup"><span data-stu-id="7e37d-135">Algorithmic</span></span> | <span data-ttu-id="7e37d-136">Tento modul zobrazuje seznam produktů, které jsou seřazeny podle nejvyššího počtu prodejů.</span><span class="sxs-lookup"><span data-stu-id="7e37d-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="7e37d-137">Trendy</span><span class="sxs-lookup"><span data-stu-id="7e37d-137">Trending</span></span>                   | <span data-ttu-id="7e37d-138">Algoritmický</span><span class="sxs-lookup"><span data-stu-id="7e37d-138">Algorithmic</span></span> | <span data-ttu-id="7e37d-139">Tento modul zobrazuje seznam nejprodávanějších produktů za dané období seřazených podle nejvyššího počtu prodejů.</span><span class="sxs-lookup"><span data-stu-id="7e37d-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="7e37d-140">Často nakupované společně</span><span class="sxs-lookup"><span data-stu-id="7e37d-140">Frequently bought together</span></span> | <span data-ttu-id="7e37d-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="7e37d-141">AI-ML</span></span> | <span data-ttu-id="7e37d-142">Tento modul doporučuje seznam produktů, které jsou běžně kupovány dohromady, spolu s obsahem aktuálního vozíku spotřebitele.</span><span class="sxs-lookup"><span data-stu-id="7e37d-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="7e37d-143">Lidem se též líbí</span><span class="sxs-lookup"><span data-stu-id="7e37d-143">People also like</span></span>           | <span data-ttu-id="7e37d-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="7e37d-144">AI-ML</span></span> | <span data-ttu-id="7e37d-145">Tento modul doporučuje produkty pro daný produkt typu seed na základě zákaznických vzorů nákupů.</span><span class="sxs-lookup"><span data-stu-id="7e37d-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="7e37d-146">Výběry pro vás</span><span class="sxs-lookup"><span data-stu-id="7e37d-146">Picks for you</span></span>              | <span data-ttu-id="7e37d-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="7e37d-147">AI-ML</span></span> | <span data-ttu-id="7e37d-148">Tento modul doporučuje individuální seznam produktů na základě zákaznických vzorů nákupů.</span><span class="sxs-lookup"><span data-stu-id="7e37d-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="7e37d-149">Pro uživatele typu host bude tento seznam sbalen.</span><span class="sxs-lookup"><span data-stu-id="7e37d-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7e37d-150">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="7e37d-150">Additional resources</span></span>

[<span data-ttu-id="7e37d-151">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7e37d-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="7e37d-152">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="7e37d-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="7e37d-153">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="7e37d-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="7e37d-154">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="7e37d-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="7e37d-155">Povolit doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="7e37d-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="7e37d-156">Přidání doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="7e37d-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="7e37d-157">Přidání doporučení na obrazovku transakcí</span><span class="sxs-lookup"><span data-stu-id="7e37d-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="7e37d-158">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="7e37d-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="7e37d-159">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="7e37d-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="7e37d-160">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="7e37d-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="7e37d-161">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="7e37d-161">Product recommendations FAQ</span></span>](faq-recommendations.md)
