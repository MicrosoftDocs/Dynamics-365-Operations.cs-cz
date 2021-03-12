---
title: Povolit doporučení typu „podobný vzhled“
description: Toto téma popisuje, jak povolit v doporučení typu „podobný vzhled“ v produktu Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 95e4246d6c5f9ac5bc86b626be0d971f756c5130
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985604"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="9d1fc-103">Povolit doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="9d1fc-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d1fc-104">Toto téma popisuje, jak povolit v doporučení typu „podobný vzhled“ v produktu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9d1fc-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="9d1fc-105">Overview</span></span>

<span data-ttu-id="9d1fc-106">Doporučení typu "podobný vzhled" v produktu Dynamics 365 Commerce využívá sílu umělé inteligence a strojového učení (AI-ML) k poskytování doporučení pro vizuálně podobné produkty zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="9d1fc-107">Poskytnutím doporučení typu „podobný vzhled“ pro všechny maloobchodní kanály v obchodě mohou maloobchodníci zvýšit spokojenost zákazníků tím, že zákazníkům pomohou snadno najít to, co chtějí.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="9d1fc-108">Funkce pro doporučení „podobný vzhled obchodu“ používá obrazy produktů zárodečných variant produktů k nalezení a doporučování vizuálně podobných produktů v katalogu produktů maloobchodníka.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="9d1fc-109">Doporučení typu „podobný vzhled“ jsou k dispozici jak v místě prodeje (POS), tak v prostředí elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="9d1fc-110">Ukázkové scénáře</span><span class="sxs-lookup"><span data-stu-id="9d1fc-110">Example scenarios</span></span>

- <span data-ttu-id="9d1fc-111">Zákazník si prohlédne černý pruhovaný svetr a obdrží doporučení pro podobný svetr v červené.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="9d1fc-112">Zákazník vybere doporučený produkt místo původně prohlíženého produktu a poté obdrží doporučení pro podobné produkty v červené.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="9d1fc-113">Zákazník používá doporučení typu „podobný vzhled“, aby objevil vyhovující náušnice pro prsten, který má zákazník zájem koupit.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="9d1fc-114">V centrále Commerce povolte doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="9d1fc-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="9d1fc-115">Doporučení produktů jsou podporována pouze u užovatelů Commerce, kteří migrovali své úložiště do služby Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9d1fc-116">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="9d1fc-116">Prerequisites</span></span>

<span data-ttu-id="9d1fc-117">Než mohou maloobchodníci začít zákazníkům zobrazovat doporučení typu „podobný vzhled“, musí provést dva nezbytné kroky:</span><span class="sxs-lookup"><span data-stu-id="9d1fc-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="9d1fc-118">[Povolit doporučení produktů](enable-product-recommendations.md) v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="9d1fc-119">Ověřit, zda mediální server podporuje volání HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="9d1fc-120">Aby mohl modul doporučení získat přístup k obrázkům produktů, musí maloobchodníci vygenerovat adresy URL produktů.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="9d1fc-121">Při generování adres URL produktů v centrále aplikace Commerce postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9d1fc-122">Přejděte do části **Obrázky produktu**.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="9d1fc-123">V podokně Akce vyberte možnost **Definovat šablonu média**.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="9d1fc-124">V **Definovat šablonu média** podokně vlastností, pod **Mediální adresy URL**, vyberte **Vygenerujte adresy URL**.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="9d1fc-125">Když povolíte funkci doporučení typu „podobný vzhled“, začne proces generování seznamů doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="9d1fc-126">Tyto seznamy budou k dispozici a budou viditelné online a v POS terminálech do následujícího dne.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="9d1fc-127">Chcete-li aktivovat funkci doporučení typu „podobný vzhled“ v centrále Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9d1fc-128">Přejděte na **Správu funkcí**.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="9d1fc-129">V seznamu dostupných funkcí vyhledejte a vyberte **Doporučení typu podobný vzhled**.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="9d1fc-130">V pravém podokně vyberte **Povolit** k zapnutí služby.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="9d1fc-131">Následující obrázek ukazuje funkci **Doporučení typu „podobný vzhled“** na stránce **Správa funkcí** v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Funkce Doporučení typu „podobný vzhled“ na stránce Správa funkcí v centrále Commerce.](./media/enableshopsimilarlooks.png)

<span data-ttu-id="9d1fc-133">Po dokončení předchozích úkolů bude do terminálů POS automaticky přidán kontextový panel **Doporučení podobných výrobků**.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="9d1fc-134">Výběrem **Zobrazit více** uživatelé POS terminálů mohou být přesměrováni na vyhrazenou stránku „podobný vzhled“, kterou lze dále filtrovat.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="9d1fc-135">Pokud vypnete funkci doporučení typu „podobný vzhled“, nebudou ovlivněny žádné jiné typy doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="9d1fc-136">Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9d1fc-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="9d1fc-137">Přidejte na stránky s podrobnostmi o produktech tlačítko Podobný vzhled pomocí tvůrce webu Commerce</span><span class="sxs-lookup"><span data-stu-id="9d1fc-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="9d1fc-138">Poté, co v centrále Commerce obchodu povolíte funkci doporučení typu „podobný vzhled“, tvůrce webu Commerce umožní maloobchodníkům přidat **Podobný vzhled** na nákupní stránce na jakékoli stránce s podrobnostmi o produktu (PDP).</span><span class="sxs-lookup"><span data-stu-id="9d1fc-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="9d1fc-139">Zákazník, který vybere toto tlačítko, se přesune na vyhrazenou stránku „podobný vzhled“, která zobrazí vizuálně podobné produkty.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="9d1fc-140">Tam může zákazník pomocí selektorů dále filtrovat produkty.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="9d1fc-141">K přidání tlačítka **Podobný vzhled** na PDP pomocí tvůrce webu Commerce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9d1fc-142">Otevře existující stránku konfigurátoru webu, která obsahuje modul buy boxu.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="9d1fc-143">V levém navigačním podokně vyberte modul buy boxu.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="9d1fc-144">V pravém navigačním podokně vyberte **Povolit odkaz na stránku Podobný vzhled** zaškrtávací políčko.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="9d1fc-145">Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="9d1fc-146">Po publikování stránky bude PDP obsahovat tlačítko **Podobný vzhled**.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="9d1fc-147">Následující obrázek ukazuje zaškrtávací políčko **Povolit odkaz na stránku Podobný vzhled** a tlačitko **Podobný vzhled** na příkladu PDP ve tvůrci webů.</span><span class="sxs-lookup"><span data-stu-id="9d1fc-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Zaškrtávací políčko Povolit odkaz na stránku Podobný vzhled a tlačitko Podobný vzhled na PDP ve tvůrci webů.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="9d1fc-149">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9d1fc-149">Additional resources</span></span>

[<span data-ttu-id="9d1fc-150">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="9d1fc-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9d1fc-151">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9d1fc-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9d1fc-152">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="9d1fc-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9d1fc-153">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="9d1fc-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9d1fc-154">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="9d1fc-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9d1fc-155">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="9d1fc-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9d1fc-156">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="9d1fc-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9d1fc-157">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="9d1fc-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9d1fc-158">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="9d1fc-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9d1fc-159">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="9d1fc-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
