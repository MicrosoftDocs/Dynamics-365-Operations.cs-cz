---
title: Odeslání obrázků
description: Toto téma popisuje, jak nahrát obrázky v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51571ce221714598b2e2d39c76cb69dcb57cc52b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213787"
---
# <a name="upload-images"></a><span data-ttu-id="e8608-103">Odeslání obrázků</span><span class="sxs-lookup"><span data-stu-id="e8608-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8608-104">Toto téma popisuje, jak nahrát obrázky v konfigurátoru webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8608-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="e8608-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="e8608-105">Overview</span></span>

<span data-ttu-id="e8608-106">Knihovna médií pro konfigurátor webu Commerce umožňuje odesílat obrázky buď jednotlivě, nebo hromadně pomocí složek.</span><span class="sxs-lookup"><span data-stu-id="e8608-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="e8608-107">Vždy byste měli odeslat verzi obrázku s nejvyšším rozlišením a kvalitou, protože komponenta pro změně velikosti obrázku automaticky optimalizuje obrázek pro různá zobrazení a jejich zarážky.</span><span class="sxs-lookup"><span data-stu-id="e8608-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="e8608-108">Informace o obrázku zadané při odeslání</span><span class="sxs-lookup"><span data-stu-id="e8608-108">Image information specified during upload</span></span>

<span data-ttu-id="e8608-109">Při odesílání obrázku lze zadat následující informace.</span><span class="sxs-lookup"><span data-stu-id="e8608-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="e8608-110">**Název, alternativní text, popis, klíčová slova**: metadata obrázku nebo obrázky.</span><span class="sxs-lookup"><span data-stu-id="e8608-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="e8608-111">Nadpis a alternativní text jsou povinné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e8608-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="e8608-112">**Vybrat kategorii**:</span><span class="sxs-lookup"><span data-stu-id="e8608-112">**Select category**:</span></span>
    - <span data-ttu-id="e8608-113">**Žádná**: používá se pro obrázky příběhu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8608-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="e8608-114">**Produkt, kategorie, odběratel, zaměstnanec, katalog**: používá se pro multikanálové obrázky Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8608-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="e8608-115">**Publikovat majetek po odeslání**: Pokud je toto políčko zaškrtnuto, bude obrázek nebo obrázky publikovány ihned po odeslání.</span><span class="sxs-lookup"><span data-stu-id="e8608-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="e8608-116">Obrazové prvky s přiřazenou kategorií jsou také automaticky označeny kategorií jako klíčové slovo, které pomáhá vyhledávat majetek určité kategorie.</span><span class="sxs-lookup"><span data-stu-id="e8608-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="e8608-117">Zásady vytváření názvů pro multikanálové obrázky</span><span class="sxs-lookup"><span data-stu-id="e8608-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="e8608-118">Pokud jste nakonfigurovali knihovnu médií jako multikanálový obrázkový backend, můžete použít kategorie obrázků k označení kategorie, do které nahraný obrázek patří.</span><span class="sxs-lookup"><span data-stu-id="e8608-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="e8608-119">Existuje také konvence pro vytváření názvů, která by měla být následována, aby bylo zajištěno správné načítání obrázků jinými kanály, jako je například pokladní místo (POS).</span><span class="sxs-lookup"><span data-stu-id="e8608-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="e8608-120">Výchozí zásady vytváření názvů se liší podle kategorie:</span><span class="sxs-lookup"><span data-stu-id="e8608-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="e8608-121">Obrázky katalogu by měly mít název "**/Katalogy/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="e8608-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="e8608-122">Obrázky kategorií by měly být pojmenované **"\{/Kategorie/\}CategoryName.** png"</span><span class="sxs-lookup"><span data-stu-id="e8608-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="e8608-123">Obrázky zákazníků by měly mít název **"\{/Zákazníci/\}CustomerNumber.** jpg"</span><span class="sxs-lookup"><span data-stu-id="e8608-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="e8608-124">Obrázky zaměstnanců by měly mít název **"\{/Pracovníci/\}WorkerNumber.** jpg"</span><span class="sxs-lookup"><span data-stu-id="e8608-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="e8608-125">Obrázky produktu by měly mít název **"\{/Produkty/\}ProductNumber _000_001.** png"</span><span class="sxs-lookup"><span data-stu-id="e8608-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="e8608-126">001 je posloupnost obrázku a může být 001, 002, 003, 004 nebo 005</span><span class="sxs-lookup"><span data-stu-id="e8608-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="e8608-127">Obrázky variant produktu by měly mít název "**/Produkty/\{ProductNumber\}\_\{Velikost\}\_\{Barva\}\_\{Styl\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="e8608-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="e8608-128">Odeslat obrázek</span><span class="sxs-lookup"><span data-stu-id="e8608-128">Upload an image</span></span>

<span data-ttu-id="e8608-129">Chcete-li odeslat obrázek v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="e8608-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e8608-130">V levém navigačním podokně vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="e8608-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="e8608-131">Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.</span><span class="sxs-lookup"><span data-stu-id="e8608-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="e8608-132">V okně Průzkumník souborů přejděte na jeden nebo více souborů s obrázky, které chcete odeslat, a vyberte možnost **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="e8608-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="e8608-133">V dialogovém okně **Odeslat mediální položku** zadejte požadovaný název a alternativní text.</span><span class="sxs-lookup"><span data-stu-id="e8608-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="e8608-134">Zadejte volitelný popis a klíčová slova a v případě potřeby vyberte kategorii.</span><span class="sxs-lookup"><span data-stu-id="e8608-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="e8608-135">Chcete-li publikovat obrázky ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.</span><span class="sxs-lookup"><span data-stu-id="e8608-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="e8608-136">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8608-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="e8608-137">Odeslat složku obrázků</span><span class="sxs-lookup"><span data-stu-id="e8608-137">Upload a folder of images</span></span>

<span data-ttu-id="e8608-138">Chcete-li hromadně odeslat složku obrázků v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="e8608-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e8608-139">V levém navigačním podokně vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="e8608-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="e8608-140">Na panelu příkazů vyberte možnost **Odeslat \> Odeslání složek**.</span><span class="sxs-lookup"><span data-stu-id="e8608-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="e8608-141">V okně Průzkumník souborů vyberte složku s obrázky, které chcete odeslat, a vyberte možnost **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="e8608-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="e8608-142">V dialogovém okně **Odeslat mediální položky** zadejte volitelná klíčová slova a v případě potřeby vyberte kategorii.</span><span class="sxs-lookup"><span data-stu-id="e8608-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="e8608-143">Chcete-li publikovat obrázky ve složce ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.</span><span class="sxs-lookup"><span data-stu-id="e8608-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="e8608-144">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8608-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8608-145">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="e8608-145">Additional resources</span></span>

[<span data-ttu-id="e8608-146">Přehled správy digitálního majetku</span><span class="sxs-lookup"><span data-stu-id="e8608-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="e8608-147">Odeslání videa</span><span class="sxs-lookup"><span data-stu-id="e8608-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="e8608-148">Odeslat soubory</span><span class="sxs-lookup"><span data-stu-id="e8608-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="e8608-149">Oříznutí obrázků</span><span class="sxs-lookup"><span data-stu-id="e8608-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="e8608-150">Přizpůsobení ohniska obrázku</span><span class="sxs-lookup"><span data-stu-id="e8608-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="e8608-151">Nahrání a obsloužení statických souborů</span><span class="sxs-lookup"><span data-stu-id="e8608-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]