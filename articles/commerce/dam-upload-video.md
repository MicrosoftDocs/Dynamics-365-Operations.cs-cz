---
title: Odeslat videa
description: Toto téma popisuje, jak odeslat videa v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8dd9e710f9a6ea593a0673e7902fadf84ca05cff
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594301"
---
# <a name="upload-videos"></a><span data-ttu-id="65163-103">Odeslat videa</span><span class="sxs-lookup"><span data-stu-id="65163-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65163-104">Toto téma popisuje, jak odeslat videa v konfigurátoru webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="65163-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="65163-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="65163-105">Overview</span></span>

<span data-ttu-id="65163-106">Knihovna médií konfigurátoru webu Commerce umožňuje odesílat videozáznamy.</span><span class="sxs-lookup"><span data-stu-id="65163-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="65163-107">Vždy byste měli odeslat verzi videa s nejvyšším datovým tokem a rozlišením, protože video bude automaticky konvertováno, aby bylo použitelné pro různá zobrazení a jejich zarážky.</span><span class="sxs-lookup"><span data-stu-id="65163-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="65163-108">Informace o video zadané při odeslání</span><span class="sxs-lookup"><span data-stu-id="65163-108">Video information specified during upload</span></span>

<span data-ttu-id="65163-109">Při odesílání videa lze zadat následující informace.</span><span class="sxs-lookup"><span data-stu-id="65163-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="65163-110">**Nadpis, popis, klíčová slova**: metadata videa.</span><span class="sxs-lookup"><span data-stu-id="65163-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="65163-111">**Automaticky generovat skryté titulky**: Určuje, zda mají být automaticky vygenerovány skryté titulky pro video.</span><span class="sxs-lookup"><span data-stu-id="65163-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="65163-112">**Skryté titulky**: Určuje skryté titulky, které mají být použity.</span><span class="sxs-lookup"><span data-stu-id="65163-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="65163-113">**Normální zvuk**: Určuje běžnou zvukovou stopu, která má být použita.</span><span class="sxs-lookup"><span data-stu-id="65163-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="65163-114">**Miniatura**: Určuje miniaturu videa.</span><span class="sxs-lookup"><span data-stu-id="65163-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="65163-115">Pokud není zadána, nebude generován automaticky.</span><span class="sxs-lookup"><span data-stu-id="65163-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="65163-116">**Popisný zvuk**: Určuje popisnou zvukovou stopu, která má být použita.</span><span class="sxs-lookup"><span data-stu-id="65163-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="65163-117">Odeslat video</span><span class="sxs-lookup"><span data-stu-id="65163-117">Upload a video</span></span>

<span data-ttu-id="65163-118">Chcete-li odeslat video v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="65163-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="65163-119">V levém navigačním podokně vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="65163-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="65163-120">Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.</span><span class="sxs-lookup"><span data-stu-id="65163-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="65163-121">V okně Průzkumník souborů přejděte na jeden nebo více souborů s videi, které chcete odeslat, a vyberte možnost **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="65163-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="65163-122">V dialogovém okně **Odeslat mediální položku** zadejte požadovaný název a alternativní text.</span><span class="sxs-lookup"><span data-stu-id="65163-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="65163-123">Zadejte volitelný popis a klíčová slova a v případě potřeby vyberte kategorii.</span><span class="sxs-lookup"><span data-stu-id="65163-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="65163-124">Chcete-li publikovat obrázky ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**</span><span class="sxs-lookup"><span data-stu-id="65163-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="65163-125">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="65163-125">Select **OK**.</span></span>

<span data-ttu-id="65163-126">Pokud odesíláte více typů majetku současně (například obrázky a videozáznamy), můžete v dialogovém okně **Odeslat mediální položku** zadat pouze klíčová slova, zda mají být soubory publikovány ihned po odeslání a zda mají být automaticky vygenerovány skryté titulky pro videosoubory.</span><span class="sxs-lookup"><span data-stu-id="65163-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="65163-127">Všechny majetky budou sdílet stejná klíčová slova.</span><span class="sxs-lookup"><span data-stu-id="65163-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65163-128">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="65163-128">Additional resources</span></span>

[<span data-ttu-id="65163-129">Přehled správy digitálního majetku</span><span class="sxs-lookup"><span data-stu-id="65163-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="65163-130">Odeslání obrázků</span><span class="sxs-lookup"><span data-stu-id="65163-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="65163-131">Odeslat soubory</span><span class="sxs-lookup"><span data-stu-id="65163-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="65163-132">Oříznutí obrázků</span><span class="sxs-lookup"><span data-stu-id="65163-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="65163-133">Přizpůsobení ohniska obrázku</span><span class="sxs-lookup"><span data-stu-id="65163-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="65163-134">Nahrání a obsloužení statických souborů</span><span class="sxs-lookup"><span data-stu-id="65163-134">Upload and serve static files</span></span>](upload-serve-static-files.md)
