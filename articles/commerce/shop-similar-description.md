---
title: Povolení doporučení „nákupu zboží s podobným popisem“
description: Toto téma popisuje, jak povolit v doporučení „nákupu zboží s podobným popisem“ v Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b3b7abf47a3bdacaa4b91ae32b68a809a84b0b1d
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098616"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="6b6e6-103">Povolení doporučení „nákupu zboží s podobným popisem“</span><span class="sxs-lookup"><span data-stu-id="6b6e6-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b6e6-104">Toto téma popisuje, jak povolit v doporučení „nákupu zboží s podobným popisem“ v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6b6e6-105">Doporučení "nákupu zboží s podobným popisem" v Dynamics 365 Commerce využívá umělou inteligenci a strojové učení (AI-ML) k poskytování doporučení produkty, které mají podobný popis jako produkty, které zákazníci hledají.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="6b6e6-106">Poskytnutím doporučení typu „podobný popis“ pro všechny maloobchodní kanály v Commerce mohou maloobchodní prodejci pomoci zákazníkům snadno najít to, co hledají.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="6b6e6-107">Funkce pro doporučení „nákupu zboží s podobným popisem“ používá název a popis produktů produktů typu seed k nalezení a doporučení podobných produktů v katalogu produktů maloobchodního prodejce.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="6b6e6-108">Doporučení typu „podobný popis“ jsou k dispozici jak v místě prodeje (POS), tak v prostředí elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="6b6e6-109">Ukázkové scénáře</span><span class="sxs-lookup"><span data-stu-id="6b6e6-109">Example scenarios</span></span>

<span data-ttu-id="6b6e6-110">Následující ukázkové scénáře ukazují typy doporučení, které může funkce „nákupu zboží s podobným popisem“ poskytnout:</span><span class="sxs-lookup"><span data-stu-id="6b6e6-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="6b6e6-111">Zákazník si prohlíží brýle v retro stylu s rohovou obroučkou a dostane několik doporučení na další brýle, které mají podobný design, v kontextu sortimentu maloobchodního prodejce.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="6b6e6-112">Zákazník používá doporučení k „nákupu zboží s podobným popisem“ k objevení dalších příchutí kávy, které jsou podobné příchuti, kterou již dříve od maloobchodního prodejce zakoupil.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="6b6e6-113">Nastavení doporučení „nákupu zboží s podobným popisem“</span><span class="sxs-lookup"><span data-stu-id="6b6e6-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="6b6e6-114">Doporučení produktů jsou podporována pouze u užovatelů Commerce, kteří migrovali své úložiště do služby Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6b6e6-115">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="6b6e6-115">Prerequisites</span></span>

<span data-ttu-id="6b6e6-116">Než se zákazníkům mohou zobrazit doporučení k „nákupu zboží s podobným popisem“, musíte splnit následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="6b6e6-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="6b6e6-117">[Povolit doporučení produktů](enable-product-recommendations.md) v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="6b6e6-118">Ověřit, zda mediální server podporuje volání HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="6b6e6-119">Zapnutí funkce „nákupu zboží s podobným popisem“</span><span class="sxs-lookup"><span data-stu-id="6b6e6-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="6b6e6-120">Chcete-li zapnout funkci doporučení typu „podobný popis“ v centrále Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6b6e6-121">V pracovním prostoru **Správa funkcí**, v seznamu dostupných funkcí vyhledejte a vyberte **Nákup zboží s podobným popisem**.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="6b6e6-122">V pravém podokně vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="6b6e6-123">Když tuto funkci zapnete, systém začne generovat seznamy doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="6b6e6-124">Může trvat až jeden den, než busou tyto seznamy k dispozici a viditelné online a v POS terminálech.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="6b6e6-125">Pokud tuto funkci vypnete, ostatních typů doporučení produktů se to nedotkne.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="6b6e6-126">Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6b6e6-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="6b6e6-127">Přidejte tlačítko Nákup zboží s podobným popisem na stránky s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="6b6e6-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="6b6e6-128">Poté, co v centrále Commerce zapnete funkci doporučení typu „podobný popis“, můžete přidat tlačítko **Zboží s podobným popisem** do buy boxu na jakékoli stránce s podrobnostmi o produktu (PDP).</span><span class="sxs-lookup"><span data-stu-id="6b6e6-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="6b6e6-129">Zákazník, který vybere toto tlačítko, se přesune na vyhrazenou stránku **Nákup zboží s podobným popisem**, která zobrazí vizuálně podobné produkty.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="6b6e6-130">Zákazník pak může pomocí selektorů dále filtrovat produkty.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="6b6e6-131">K přidání tlačítka **Nákup zboží s podobným popisem** na PDP pomocí konfigurátoru webu Commerce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6b6e6-132">Otevře existující stránku konfigurátoru webu, která obsahuje modul buy boxu.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="6b6e6-133">V levém navigačním podokně vyberte modul buy boxu.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="6b6e6-134">V pravém navigačním podokně zaškrtněte políčko **Povolit odkaz na zboží s podobným popisem**.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="6b6e6-135">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-135">Select **Save**.</span></span>
1. <span data-ttu-id="6b6e6-136">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="6b6e6-137">Po publikování stránky bude PDP obsahovat tlačítko **Nákup zboží s podobným popisem**.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="6b6e6-138">Následující obrázek ukazuje zaškrtávací políčko **Povolit odkaz na na zboží s podobným popisem** a tlačítko **Podobný popis** na příkladu PDP v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Zaškrtávací políčko Povolit odkaz na zboží s podobným popisem a tlačitko Podobný popis na PDP v konfigurátoru webů.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="6b6e6-140">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="6b6e6-140">Additional resources</span></span>

[<span data-ttu-id="6b6e6-141">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="6b6e6-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6b6e6-142">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6b6e6-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="6b6e6-143">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="6b6e6-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6b6e6-144">Povolení doporučení „nákupu podobného vzhledu“</span><span class="sxs-lookup"><span data-stu-id="6b6e6-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="6b6e6-145">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="6b6e6-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="6b6e6-146">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="6b6e6-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6b6e6-147">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="6b6e6-147">Product recommendations FAQ</span></span>](faq-recommendations.md)
