---
title: Přizpůsobení navigace na webu
description: V tomto tématu je popsán postup při vytvoření přizpůsobené online hierarchie navigace pro uspořádání produktů pro procházení na webu Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 642cb5c145dec68631eb9ab27d926ba8ab75c59b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914903"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="127b3-103">Přizpůsobení navigace na webu</span><span class="sxs-lookup"><span data-stu-id="127b3-103">Customize site navigation</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="127b3-104">V tomto tématu je popsán postup při vytvoření přizpůsobené online hierarchie navigace pro uspořádání produktů pro procházení na webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="127b3-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="127b3-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="127b3-105">Overview</span></span>

<span data-ttu-id="127b3-106">Online výkladní skříně obvykle zákazníkům umožňují vyhledat a procházet produkty pomocí procházení kategorií produktů.</span><span class="sxs-lookup"><span data-stu-id="127b3-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="127b3-107">Takovou možnost obvykle poskytují karty v horní části stránky nebo navigační panel vlevo.</span><span class="sxs-lookup"><span data-stu-id="127b3-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="127b3-108">V řešení Dynamics 365 Commerce můžete vytvářet a spravovat hierarchickou strukturu navigace mezi kategoriemi a produkty zahrnuté do různých kategorií.</span><span class="sxs-lookup"><span data-stu-id="127b3-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-retail-channel-navigation-hierarchy"></a><span data-ttu-id="127b3-109">Vytvoření hierarchie navigace maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="127b3-109">Create a retail channel navigation hierarchy</span></span>

<span data-ttu-id="127b3-110">Chcete-li vytvořit hierarchii navigace maloobchodní sítě, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="127b3-110">To create a retail channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="127b3-111">Přejděte do nabídky **Maloobchod \> Produkty a kategorie \> Správa kategorií a produktů**.</span><span class="sxs-lookup"><span data-stu-id="127b3-111">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="127b3-112">Vyberte **Hierarchie kategorií** a pak vyberte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="127b3-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="127b3-113">Pojmenujte hierarchii.</span><span class="sxs-lookup"><span data-stu-id="127b3-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="127b3-114">Nejvyšší vytvořená kategorie je uzel kořenové kategorie.</span><span class="sxs-lookup"><span data-stu-id="127b3-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="127b3-115">Tato stránka nebude zobrazena na vašem webu.</span><span class="sxs-lookup"><span data-stu-id="127b3-115">It won't be shown on your site.</span></span> <span data-ttu-id="127b3-116">Chcete-li vytvořit hierarchii kategorií, v níž se na webu zobrazí jeden uzel nejvyšší úrovně, vytvořte a pojmenujte kategorii jako podřízenou položku kořenové kategorie.</span><span class="sxs-lookup"><span data-stu-id="127b3-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="127b3-117">Vyberte možnost **Nový uzel kategorie** a pojmenujte kategorii.</span><span class="sxs-lookup"><span data-stu-id="127b3-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="127b3-118">Pokračujte ve vytváření kategorií na stejné a podřízené úrovni podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="127b3-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="127b3-119">Nyní můžete přiřadit produkty ke každé kategorii, kterou jste vytvořili pod kategorií nejvyšší úrovně.</span><span class="sxs-lookup"><span data-stu-id="127b3-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="127b3-120">Vlastní nastavení pořadí kategorií</span><span class="sxs-lookup"><span data-stu-id="127b3-120">Customize the order of categories</span></span>

<span data-ttu-id="127b3-121">Ve výchozím nastavení se kategorie, které definujete, zobrazí v abecedním pořadí na webu.</span><span class="sxs-lookup"><span data-stu-id="127b3-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="127b3-122">Lze však také přizpůsobit pořadí zobrazení kategorií.</span><span class="sxs-lookup"><span data-stu-id="127b3-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="127b3-123">Přiřazení typu hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="127b3-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="127b3-124">Přejděte do nabídky **Maloobchod \> Produkty a kategorie \> Správa kategorií a produktů**.</span><span class="sxs-lookup"><span data-stu-id="127b3-124">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="127b3-125">Vyberte možnost **Hierarchie kategorií**.</span><span class="sxs-lookup"><span data-stu-id="127b3-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="127b3-126">V podokně akcí na kartě **Hierarchie kategorií** ve skupině **Nastavení** zvolte **Přidružit typ hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="127b3-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="127b3-127">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="127b3-127">Select **New**.</span></span>
1. <span data-ttu-id="127b3-128">V poli **Typ hierarchie kategorií** vyberte možnost **Hierarchie navigace maloobchodní sítě**.</span><span class="sxs-lookup"><span data-stu-id="127b3-128">In the **Category hierarchy type** field, select **Retail channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="127b3-129">V poli **Hierarchie kategorií** vyberte hierarchii navigace sítě, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="127b3-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="127b3-130">Publikování nových nebo aktualizovaných hierarchií navigací</span><span class="sxs-lookup"><span data-stu-id="127b3-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="127b3-131">Chcete-li hierarchii navigace zpřístupnit v online výkladní skříni, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="127b3-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="127b3-132">Přejděte na **Maloobchod \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.</span><span class="sxs-lookup"><span data-stu-id="127b3-132">Go to **Retail \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="127b3-133">Ve stromu vlevo vyberte svůj online obchod.</span><span class="sxs-lookup"><span data-stu-id="127b3-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="127b3-134">Vyberte možnost **Publikovat aktualizace kanálů**.</span><span class="sxs-lookup"><span data-stu-id="127b3-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="127b3-135">Přejděte do nabídky **Maloobchodní prodej \> Maloobchodní IT \> Distribuční plán**.</span><span class="sxs-lookup"><span data-stu-id="127b3-135">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="127b3-136">V seznamu vyhledejte a vyberte **Úloha 1040**.</span><span class="sxs-lookup"><span data-stu-id="127b3-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="127b3-137">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="127b3-137">Select **Run now**.</span></span>
1. <span data-ttu-id="127b3-138">Zopakujte kroky 5 a 6 pro úlohy 1070 a 1150.</span><span class="sxs-lookup"><span data-stu-id="127b3-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="127b3-139">Zobrazení kategorií na vašem webu</span><span class="sxs-lookup"><span data-stu-id="127b3-139">Show categories on your site</span></span>

<span data-ttu-id="127b3-140">Chcete-li zobrazit hierarchii kategorií v online výkladní skříni, je nutné přidat modul navigační nabídky do příslušného umístění v šabloně nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="127b3-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="127b3-141">Modul navigační nabídky pak zobrazí hierarchii navigace za předpokladu, že jste publikovali hierarchii navigace maloobchodu v kanálu, na který je vázán váš web.</span><span class="sxs-lookup"><span data-stu-id="127b3-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your retail navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="127b3-142">Modul navigační nabídky, který je součástí startovací sady obchodu, umožňuje uživatelům přejít pouze ke kategoriím, které nemají podkategorie.</span><span class="sxs-lookup"><span data-stu-id="127b3-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="127b3-143">Chcete-li, aby vaši zákazníci mohli přejít do kategorií s podkategoriemi, je nutné upravit modul navigační nabídky.</span><span class="sxs-lookup"><span data-stu-id="127b3-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="127b3-144">Přidání vlastních možností navigace</span><span class="sxs-lookup"><span data-stu-id="127b3-144">Add custom navigation options</span></span>

<span data-ttu-id="127b3-145">V navigační nabídce můžete přidat možnosti navigace, které nejsou součástí hierarchie kategorií produktů.</span><span class="sxs-lookup"><span data-stu-id="127b3-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="127b3-146">Na konci seznamu kategorií produktů můžete například přidat položku **Kontaktujte nás**, která odkazuje na stránku kontaktu, kterou jste vytvořili pro váš web.</span><span class="sxs-lookup"><span data-stu-id="127b3-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="127b3-147">Chcete-li do navigační nabídky přidat vlastní možnosti navigace, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="127b3-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="127b3-148">V šabloně nebo fragmentu, který chcete přizpůsobit, vyberte modul navigační nabídky.</span><span class="sxs-lookup"><span data-stu-id="127b3-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="127b3-149">Chcete-li vytvořit novou navigační položku systému správy obsahu (CMS), v podokně vlastností na kartě **Data** vyberte možnost **Přidat položku**.</span><span class="sxs-lookup"><span data-stu-id="127b3-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="127b3-150">Zadejte text a adresu URL odkazu.</span><span class="sxs-lookup"><span data-stu-id="127b3-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="127b3-151">Chcete-li přidat další vlastní možnosti navigace, opakujte kroky 2 a 3.</span><span class="sxs-lookup"><span data-stu-id="127b3-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="127b3-152">Po dokončení uložte šablonu nebo fragment a proveďte vrácení se změnami.</span><span class="sxs-lookup"><span data-stu-id="127b3-152">When you've finished, save the template or fragment, and check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="127b3-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="127b3-153">Additional resources</span></span>

[<span data-ttu-id="127b3-154">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="127b3-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="127b3-155">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="127b3-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="127b3-156">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="127b3-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="127b3-157">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="127b3-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="127b3-158">Práce s moduly</span><span class="sxs-lookup"><span data-stu-id="127b3-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="127b3-159">Vytvoření URL adresy stránky</span><span class="sxs-lookup"><span data-stu-id="127b3-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="127b3-160">Práce se skupinami publikování</span><span class="sxs-lookup"><span data-stu-id="127b3-160">Work with publish groups</span></span>](publish-groups.md)