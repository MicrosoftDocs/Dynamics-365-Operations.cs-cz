---
title: Odeslat jiné soubory než obrázky a videa
description: V tomto tématu je popsán postup při odesílání binárních souborů kromě obrázků a videí v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799246"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="c7803-103">Odeslání souborů jiných než obrázky a videa</span><span class="sxs-lookup"><span data-stu-id="c7803-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7803-104">V tomto tématu je popsán postup při odesílání souborů kromě obrázků a videí v konfigurátoru webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7803-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="c7803-105">Knihovna médií konfigurátoru webu Commerce podporuje odesílání binárních datových zdrojů s výjimkou obrázků a videí.</span><span class="sxs-lookup"><span data-stu-id="c7803-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="c7803-106">Můžete například chtít odeslat soubory aplikace Microsoft Excel, Microsoft Word, Microsoft PowerPoint nebo PDF.</span><span class="sxs-lookup"><span data-stu-id="c7803-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="c7803-107">Podporovány jsou následující typy dokumentů:</span><span class="sxs-lookup"><span data-stu-id="c7803-107">The following document types are supported:</span></span>
- <span data-ttu-id="c7803-108">7Z</span><span class="sxs-lookup"><span data-stu-id="c7803-108">7Z</span></span>
- <span data-ttu-id="c7803-109">AVI</span><span class="sxs-lookup"><span data-stu-id="c7803-109">AVI</span></span>
- <span data-ttu-id="c7803-110">CS</span><span class="sxs-lookup"><span data-stu-id="c7803-110">CS</span></span>
- <span data-ttu-id="c7803-111">CSS</span><span class="sxs-lookup"><span data-stu-id="c7803-111">CSS</span></span>
- <span data-ttu-id="c7803-112">DOC</span><span class="sxs-lookup"><span data-stu-id="c7803-112">DOC</span></span>
- <span data-ttu-id="c7803-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="c7803-113">DOCX</span></span>
- <span data-ttu-id="c7803-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="c7803-114">EPUB</span></span>
- <span data-ttu-id="c7803-115">GIF</span><span class="sxs-lookup"><span data-stu-id="c7803-115">GIF</span></span>
- <span data-ttu-id="c7803-116">INDD</span><span class="sxs-lookup"><span data-stu-id="c7803-116">INDD</span></span>
- <span data-ttu-id="c7803-117">JAR</span><span class="sxs-lookup"><span data-stu-id="c7803-117">JAR</span></span>
- <span data-ttu-id="c7803-118">JPG</span><span class="sxs-lookup"><span data-stu-id="c7803-118">JPG</span></span>
- <span data-ttu-id="c7803-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="c7803-119">JPEG</span></span>
- <span data-ttu-id="c7803-120">JS</span><span class="sxs-lookup"><span data-stu-id="c7803-120">JS</span></span>
- <span data-ttu-id="c7803-121">MP3</span><span class="sxs-lookup"><span data-stu-id="c7803-121">MP3</span></span>
- <span data-ttu-id="c7803-122">MP4</span><span class="sxs-lookup"><span data-stu-id="c7803-122">MP4</span></span>
- <span data-ttu-id="c7803-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="c7803-123">MPEG</span></span>
- <span data-ttu-id="c7803-124">MPG</span><span class="sxs-lookup"><span data-stu-id="c7803-124">MPG</span></span>
- <span data-ttu-id="c7803-125">ODP</span><span class="sxs-lookup"><span data-stu-id="c7803-125">ODP</span></span>
- <span data-ttu-id="c7803-126">ODS</span><span class="sxs-lookup"><span data-stu-id="c7803-126">ODS</span></span>
- <span data-ttu-id="c7803-127">ODT</span><span class="sxs-lookup"><span data-stu-id="c7803-127">ODT</span></span>
- <span data-ttu-id="c7803-128">PDF</span><span class="sxs-lookup"><span data-stu-id="c7803-128">PDF</span></span>
- <span data-ttu-id="c7803-129">PNG</span><span class="sxs-lookup"><span data-stu-id="c7803-129">PNG</span></span>
- <span data-ttu-id="c7803-130">PPT</span><span class="sxs-lookup"><span data-stu-id="c7803-130">PPT</span></span>
- <span data-ttu-id="c7803-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="c7803-131">PPTX</span></span>
- <span data-ttu-id="c7803-132">PS</span><span class="sxs-lookup"><span data-stu-id="c7803-132">PS</span></span>
- <span data-ttu-id="c7803-133">QXP</span><span class="sxs-lookup"><span data-stu-id="c7803-133">QXP</span></span>
- <span data-ttu-id="c7803-134">RAR</span><span class="sxs-lookup"><span data-stu-id="c7803-134">RAR</span></span>
- <span data-ttu-id="c7803-135">RTF</span><span class="sxs-lookup"><span data-stu-id="c7803-135">RTF</span></span>
- <span data-ttu-id="c7803-136">SVG</span><span class="sxs-lookup"><span data-stu-id="c7803-136">SVG</span></span>
- <span data-ttu-id="c7803-137">TAR</span><span class="sxs-lookup"><span data-stu-id="c7803-137">TAR</span></span>
- <span data-ttu-id="c7803-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="c7803-138">TGZ</span></span>
- <span data-ttu-id="c7803-139">TXT</span><span class="sxs-lookup"><span data-stu-id="c7803-139">TXT</span></span>
- <span data-ttu-id="c7803-140">WMV</span><span class="sxs-lookup"><span data-stu-id="c7803-140">WMV</span></span>
- <span data-ttu-id="c7803-141">XLS</span><span class="sxs-lookup"><span data-stu-id="c7803-141">XLS</span></span>
- <span data-ttu-id="c7803-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="c7803-142">XLSX</span></span>
- <span data-ttu-id="c7803-143">XML</span><span class="sxs-lookup"><span data-stu-id="c7803-143">XML</span></span>
- <span data-ttu-id="c7803-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="c7803-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="c7803-145">Odeslat soubor</span><span class="sxs-lookup"><span data-stu-id="c7803-145">Upload a file</span></span>

<span data-ttu-id="c7803-146">Pokud chcete odeslat soubor do konfigurátoru webu v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="c7803-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7803-147">V levém navigačním podokně vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="c7803-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="c7803-148">Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.</span><span class="sxs-lookup"><span data-stu-id="c7803-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="c7803-149">V Průzkumníkovi souborů vyberte jeden nebo více souborů a pak vyberte možnost **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="c7803-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="c7803-150">V dialogovém okně **Odeslat mediální položku** zadejte podle potřeby název, popis a metadata klíčových slov.</span><span class="sxs-lookup"><span data-stu-id="c7803-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="c7803-151">Chcete-li publikovat soubory ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.</span><span class="sxs-lookup"><span data-stu-id="c7803-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="c7803-152">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7803-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7803-153">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="c7803-153">Additional resources</span></span>

[<span data-ttu-id="c7803-154">Přehled správy digitálního majetku</span><span class="sxs-lookup"><span data-stu-id="c7803-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c7803-155">Odeslání obrázků</span><span class="sxs-lookup"><span data-stu-id="c7803-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c7803-156">Odeslání videa</span><span class="sxs-lookup"><span data-stu-id="c7803-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="c7803-157">Oříznutí obrázků</span><span class="sxs-lookup"><span data-stu-id="c7803-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c7803-158">Přizpůsobení ohniska obrázku</span><span class="sxs-lookup"><span data-stu-id="c7803-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="c7803-159">Nahrání a obsloužení statických souborů</span><span class="sxs-lookup"><span data-stu-id="c7803-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
