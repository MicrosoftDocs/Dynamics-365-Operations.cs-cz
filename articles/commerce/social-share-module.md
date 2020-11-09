---
title: Modul pro sdílení na sociálních sítích
description: Tohle téma se zabývá moduly pro sdílení na sociálních sítích a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022068"
---
# <a name="social-share-module"></a><span data-ttu-id="12a7a-103">Modul pro sdílení na sociálních sítích</span><span class="sxs-lookup"><span data-stu-id="12a7a-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12a7a-104">Tohle téma se zabývá moduly pro sdílení na sociálních sítích a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12a7a-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="12a7a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="12a7a-105">Overview</span></span>

<span data-ttu-id="12a7a-106">Moduly pro sdílení na sociálních sítích umožňují uživatelům sdílet adresy URL webových stránek e-Commerce na sociálních médiích, jako je Facebook , Twitter, Pinterest a LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="12a7a-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="12a7a-107">Adresy URL webových stránek lze také sdílet prostřednictvím e-mailu.</span><span class="sxs-lookup"><span data-stu-id="12a7a-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="12a7a-108">Moduly pro sdílení na sociálních sítích se běžně používají na stránkách s podrobnostmi o produktu (PDP), které uživatelům pomáhají sdílet informace o produktu.</span><span class="sxs-lookup"><span data-stu-id="12a7a-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="12a7a-109">Každý modul pro sdílení na sociálních sítích je kontejnerem pro moduly položek pro sdílení na sociálních sítích.</span><span class="sxs-lookup"><span data-stu-id="12a7a-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="12a7a-110">Každý modul položky pro sdílení na sociálních sítích lze nakonfigurovat tak, aby odkazoval na konkrétní web sociálních médií.</span><span class="sxs-lookup"><span data-stu-id="12a7a-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="12a7a-111">Integrace se službami Facebook, Twitter, Pinterest, LinkedIn a e-mailem jsou podporovány ihned z výroby.</span><span class="sxs-lookup"><span data-stu-id="12a7a-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="12a7a-112">Když uživatel webu vybere symbol sociálního média, spustí se iframe HTML pro příslušný web sociálního média.</span><span class="sxs-lookup"><span data-stu-id="12a7a-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="12a7a-113">V rámci iframe se uživatel může přihlásit a zveřejnit obsah stránky, kterou prohlížel.</span><span class="sxs-lookup"><span data-stu-id="12a7a-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="12a7a-114">Každá platforma sociálních médií může sledovat soubory cookie, takže tento modul vyžaduje, aby uživatelé stránek přijali zprávu s oznámením o souhlasu se soubory cookie.</span><span class="sxs-lookup"><span data-stu-id="12a7a-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="12a7a-115">Pokud souhlas se soubory cookies nebude přijat, bude modul na stránce skrytý.</span><span class="sxs-lookup"><span data-stu-id="12a7a-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="12a7a-116">Další informace viz [Zásady zacházení se soubory cookie](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="12a7a-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="12a7a-117">Následující obrázek znázorňuje příklad modulu pro sdílení na sociálních sítích použitého na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="12a7a-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Příklad modulu pro sdílení na sociálních sítích](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="12a7a-119">Vlastnosti modulu pro sdílení na sociálních sítích</span><span class="sxs-lookup"><span data-stu-id="12a7a-119">Social share module properties</span></span>

| <span data-ttu-id="12a7a-120">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="12a7a-120">Property name</span></span>             | <span data-ttu-id="12a7a-121">Hodnota</span><span class="sxs-lookup"><span data-stu-id="12a7a-121">Value</span></span>                 | <span data-ttu-id="12a7a-122">popis</span><span class="sxs-lookup"><span data-stu-id="12a7a-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="12a7a-123">Titulek</span><span class="sxs-lookup"><span data-stu-id="12a7a-123">Caption</span></span>                  | <span data-ttu-id="12a7a-124">Text</span><span class="sxs-lookup"><span data-stu-id="12a7a-124">Text</span></span> | <span data-ttu-id="12a7a-125">Tato vlastnost určuje titulek modulu.</span><span class="sxs-lookup"><span data-stu-id="12a7a-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="12a7a-126">Orientace</span><span class="sxs-lookup"><span data-stu-id="12a7a-126">Orientation</span></span> | <span data-ttu-id="12a7a-127">**Horizontální** nebo **Vertikální**</span><span class="sxs-lookup"><span data-stu-id="12a7a-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="12a7a-128">Tato vlastnost definuje orientaci rozložení pro položky sociálních médií.</span><span class="sxs-lookup"><span data-stu-id="12a7a-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="12a7a-129">Vlastnosti modulu položky pro sdílení na sociálních sítích</span><span class="sxs-lookup"><span data-stu-id="12a7a-129">Social share item module properties</span></span>
| <span data-ttu-id="12a7a-130">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="12a7a-130">Property name</span></span>             | <span data-ttu-id="12a7a-131">Hodnota</span><span class="sxs-lookup"><span data-stu-id="12a7a-131">Value</span></span>                 | <span data-ttu-id="12a7a-132">popis</span><span class="sxs-lookup"><span data-stu-id="12a7a-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="12a7a-133">Sociální média</span><span class="sxs-lookup"><span data-stu-id="12a7a-133">Social media</span></span>              | <span data-ttu-id="12a7a-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **Mail**</span><span class="sxs-lookup"><span data-stu-id="12a7a-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **Mail**</span></span> | <span data-ttu-id="12a7a-135">Rozbalovací nabídka se seznamem platforem sociálních médií.</span><span class="sxs-lookup"><span data-stu-id="12a7a-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="12a7a-136">Ikona</span><span class="sxs-lookup"><span data-stu-id="12a7a-136">Icon</span></span> |<span data-ttu-id="12a7a-137">Obrázek</span><span class="sxs-lookup"><span data-stu-id="12a7a-137">Image</span></span>    | <span data-ttu-id="12a7a-138">Toto bude obrázek, který se zobrazí pro příslušné sociální médium.</span><span class="sxs-lookup"><span data-stu-id="12a7a-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="12a7a-139">Doporučujeme použít SDK platformy sociálních médií pro výběr doporučeného obrázku jednotlivých platforem.</span><span class="sxs-lookup"><span data-stu-id="12a7a-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="12a7a-140">Přidání modulu pro sdílení na sociálních sítích do modulu buy boxu</span><span class="sxs-lookup"><span data-stu-id="12a7a-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="12a7a-141">Chcete-li přidat modul pro sdílení na sociálních sítích do modulu buy boxu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="12a7a-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="12a7a-142">Na webu Fabrikam vyberte **Stránky** a potom vyberte stránku **DefaultPDP** pro otevření stránky s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="12a7a-142">In the Fabrikam site, select **Pages** , and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="12a7a-143">V pozici **Buybox (povinné)** vyberte tři tečky ( **...** ) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-143">In the **Buybox (required)** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="12a7a-144">V dialogovém okně **Přidat modul** vyberte modul **Sdílení na sociálních sítích** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="12a7a-145">V pozici **Sdílení na sociálních sítích** vyberte tři tečky ( **...** ) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-145">In the **Social Share** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="12a7a-146">V dialogovém okně **Přidat modul** vyberte modul **SocialShare** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="12a7a-147">V podokně vlastností modulu **SocialShare** v sekci **Orientace** vyberte **Horizontální** .</span><span class="sxs-lookup"><span data-stu-id="12a7a-147">In the properties pane of the **SocialShare** module, under **Orientation** , select **Horizontal**.</span></span> <span data-ttu-id="12a7a-148">Podle potřeby přidejte titulek.</span><span class="sxs-lookup"><span data-stu-id="12a7a-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="12a7a-149">V pozici **SocialShare** vyberte tři tečky ( **...** ) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-149">In the **SocialShare** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="12a7a-150">V dialogovém okně **Přidat modul** vyberte modul **SocialShareItem** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="12a7a-151">V podokně vlastností modulu **SocialShareItem** v sekci **SocialMedia** vyberte **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-151">In the properties pane of the **SocialShareItem** module, under **Social Media** , select **Facebook**.</span></span>
1. <span data-ttu-id="12a7a-152">V podokně vlastností modulu **SocialShareItem** v sekci **Ikona** vyberte **+ Přidat obrázek**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-152">In the properties pane of the **SocialShareItem** module, under **Icon** , select **+ Add an image**.</span></span>
1. <span data-ttu-id="12a7a-153">V dialogovém okně **Výběr média** vyberte obrázek loga Facebook a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="12a7a-154">Jestli není dostupný obrázek s logem Facebook, volbou **Odeslat novou mediální položku** jej nahrajte.</span><span class="sxs-lookup"><span data-stu-id="12a7a-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="12a7a-155">Přidejte a nakonfigurujte další moduly **SocialShareItem** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="12a7a-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="12a7a-156">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled** , chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="12a7a-156">Select **Save** , and then select **Preview** to preview the page.</span></span> <span data-ttu-id="12a7a-157">Na stránce se zobrazí modul pro sdílení na sociálních sítích.</span><span class="sxs-lookup"><span data-stu-id="12a7a-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="12a7a-158">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="12a7a-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12a7a-159">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="12a7a-159">Additional resources</span></span>

[<span data-ttu-id="12a7a-160">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="12a7a-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="12a7a-161">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="12a7a-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="12a7a-162">Zásady zacházení se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="12a7a-162">Cookie compliance</span></span>](cookie-compliance.md)
