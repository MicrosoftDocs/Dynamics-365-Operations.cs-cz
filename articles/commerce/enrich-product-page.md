---
title: Obohacení stránky produktu
description: Toto téma popisuje, jak obohatit stránku produktu v řešení Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799030"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="4fafb-103">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="4fafb-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4fafb-104">Toto téma popisuje, jak obohatit stránku produktu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4fafb-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4fafb-105">Ve výchozím nastavení používá web pro zobrazení dat produktu běžnou stránku.</span><span class="sxs-lookup"><span data-stu-id="4fafb-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="4fafb-106">Tato stránka obsahuje základní informace o produktu a ovládací prvky, které jsou nutné k jeho prodeji.</span><span class="sxs-lookup"><span data-stu-id="4fafb-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="4fafb-107">Můžete však doplnit informace, které pocházejí z Commerce Scale Unit, o další obrázky nebo text pro určitý produkt.</span><span class="sxs-lookup"><span data-stu-id="4fafb-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="4fafb-108">Tento proces nazýváme obohacováním stránky produktu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="4fafb-109">V mnoha případech budete chtít pro vaše produkty použít určitý dodatečný obsah.</span><span class="sxs-lookup"><span data-stu-id="4fafb-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="4fafb-110">Když přejdete do části **Retail a Commerce** ve vývojovém nástroji, zobrazí se seznam produktů z kanálu, který je přiřazený k danému webu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="4fafb-111">V tomto seznamu určuje sloupec **Obohaceno**, zda byla stránka produktu pro produkt obohacena.</span><span class="sxs-lookup"><span data-stu-id="4fafb-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="4fafb-112">Je-li ve sloupci zobrazeno zaškrtávací políčko, pro produkt existuje obohacená stránka produktu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="4fafb-113">Pokud se zaškrtávací políčko nezobrazuje, pro produkt je použita výchozí stránka a obsah produktu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="4fafb-114">Chcete-li zobrazit náhled obohacených i neobohacených stránek produktu, vyberte v seznamu název produktu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="4fafb-115">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="4fafb-115">Enrich a product page</span></span>

<span data-ttu-id="4fafb-116">Chcete-li obohatit stránku produktu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="4fafb-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="4fafb-117">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="4fafb-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4fafb-118">V navigačním podokně nalevo vyberte položku **Produkty**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="4fafb-119">Vyberte libovolný produkt, který nemá obohacenou stránku.</span><span class="sxs-lookup"><span data-stu-id="4fafb-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="4fafb-120">V podokně akcí klikněte na možnost **Obohatit stránku produktu**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="4fafb-121">Vyberte **Šablona stránky s podrobnostmi o produktu** a potom **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="4fafb-122">Ve stromu osnovy stránky nalevo rozbalte pozici **Hlavní**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="4fafb-123">Vyberte tlačítko se třemi tečkami (**...**) vedle pozice **Hlavní** a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4fafb-124">Vyberte **Kontejner 2** a potom **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="4fafb-125">Pro **Kontejner 2** vyberte tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4fafb-126">Vyberte možnost **Funkce** a potom **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="4fafb-127">V podokně vlastností vpravo v poli **Formátovaný text** zadejte aktualizovaný popis produktu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="4fafb-128">Do pole **Nadpis** zadejte text nadpisu a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="4fafb-129">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4fafb-130">Do pole **Komentáře** zadejte **Obohacený produkt** a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="4fafb-131">Volbou **Náhled** zobrazíte náhled obohacené stránky produktu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="4fafb-132">Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="4fafb-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="4fafb-133">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="4fafb-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fafb-134">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4fafb-134">Additional resources</span></span>

[<span data-ttu-id="4fafb-135">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="4fafb-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="4fafb-136">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="4fafb-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="4fafb-137">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="4fafb-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="4fafb-138">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="4fafb-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="4fafb-139">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="4fafb-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="4fafb-140">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="4fafb-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="4fafb-141">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="4fafb-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="4fafb-142">Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL</span><span class="sxs-lookup"><span data-stu-id="4fafb-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
