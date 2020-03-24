---
title: Odeslat jiné soubory než obrázky a videa
description: V tomto tématu je popsán postup při odesílání binárních souborů kromě obrázků a videí v konfigurátoru webu Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096982"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="b8880-103">Odeslat jiné soubory než obrázky a videa</span><span class="sxs-lookup"><span data-stu-id="b8880-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8880-104">V tomto tématu je popsán postup při odesílání souborů kromě obrázků a videí v konfigurátoru webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8880-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="b8880-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b8880-105">Overview</span></span>

<span data-ttu-id="b8880-106">Knihovna médií konfigurátoru webu Commerce podporuje odesílání binárních datových zdrojů s výjimkou obrázků a videí.</span><span class="sxs-lookup"><span data-stu-id="b8880-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="b8880-107">Můžete například chtít odeslat soubory aplikace Microsoft Excel, Microsoft Word, Microsoft PowerPoint nebo PDF.</span><span class="sxs-lookup"><span data-stu-id="b8880-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="b8880-108">Podporovány jsou následující typy dokumentů:</span><span class="sxs-lookup"><span data-stu-id="b8880-108">The following document types are supported:</span></span>
- <span data-ttu-id="b8880-109">7Z</span><span class="sxs-lookup"><span data-stu-id="b8880-109">7Z</span></span>
- <span data-ttu-id="b8880-110">AVI</span><span class="sxs-lookup"><span data-stu-id="b8880-110">AVI</span></span>
- <span data-ttu-id="b8880-111">CS</span><span class="sxs-lookup"><span data-stu-id="b8880-111">CS</span></span>
- <span data-ttu-id="b8880-112">CSS</span><span class="sxs-lookup"><span data-stu-id="b8880-112">CSS</span></span>
- <span data-ttu-id="b8880-113">DOC</span><span class="sxs-lookup"><span data-stu-id="b8880-113">DOC</span></span>
- <span data-ttu-id="b8880-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="b8880-114">DOCX</span></span>
- <span data-ttu-id="b8880-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="b8880-115">EPUB</span></span>
- <span data-ttu-id="b8880-116">GIF</span><span class="sxs-lookup"><span data-stu-id="b8880-116">GIF</span></span>
- <span data-ttu-id="b8880-117">INDD</span><span class="sxs-lookup"><span data-stu-id="b8880-117">INDD</span></span>
- <span data-ttu-id="b8880-118">JAR</span><span class="sxs-lookup"><span data-stu-id="b8880-118">JAR</span></span>
- <span data-ttu-id="b8880-119">JPG</span><span class="sxs-lookup"><span data-stu-id="b8880-119">JPG</span></span>
- <span data-ttu-id="b8880-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="b8880-120">JPEG</span></span>
- <span data-ttu-id="b8880-121">JS</span><span class="sxs-lookup"><span data-stu-id="b8880-121">JS</span></span>
- <span data-ttu-id="b8880-122">MP3</span><span class="sxs-lookup"><span data-stu-id="b8880-122">MP3</span></span>
- <span data-ttu-id="b8880-123">MP4</span><span class="sxs-lookup"><span data-stu-id="b8880-123">MP4</span></span>
- <span data-ttu-id="b8880-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="b8880-124">MPEG</span></span>
- <span data-ttu-id="b8880-125">MPG</span><span class="sxs-lookup"><span data-stu-id="b8880-125">MPG</span></span>
- <span data-ttu-id="b8880-126">ODP</span><span class="sxs-lookup"><span data-stu-id="b8880-126">ODP</span></span>
- <span data-ttu-id="b8880-127">ODS</span><span class="sxs-lookup"><span data-stu-id="b8880-127">ODS</span></span>
- <span data-ttu-id="b8880-128">ODT</span><span class="sxs-lookup"><span data-stu-id="b8880-128">ODT</span></span>
- <span data-ttu-id="b8880-129">PDF</span><span class="sxs-lookup"><span data-stu-id="b8880-129">PDF</span></span>
- <span data-ttu-id="b8880-130">PNG</span><span class="sxs-lookup"><span data-stu-id="b8880-130">PNG</span></span>
- <span data-ttu-id="b8880-131">PPT</span><span class="sxs-lookup"><span data-stu-id="b8880-131">PPT</span></span>
- <span data-ttu-id="b8880-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="b8880-132">PPTX</span></span>
- <span data-ttu-id="b8880-133">PS</span><span class="sxs-lookup"><span data-stu-id="b8880-133">PS</span></span>
- <span data-ttu-id="b8880-134">QXP</span><span class="sxs-lookup"><span data-stu-id="b8880-134">QXP</span></span>
- <span data-ttu-id="b8880-135">RAR</span><span class="sxs-lookup"><span data-stu-id="b8880-135">RAR</span></span>
- <span data-ttu-id="b8880-136">RTF</span><span class="sxs-lookup"><span data-stu-id="b8880-136">RTF</span></span>
- <span data-ttu-id="b8880-137">SVG</span><span class="sxs-lookup"><span data-stu-id="b8880-137">SVG</span></span>
- <span data-ttu-id="b8880-138">TAR</span><span class="sxs-lookup"><span data-stu-id="b8880-138">TAR</span></span>
- <span data-ttu-id="b8880-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="b8880-139">TGZ</span></span>
- <span data-ttu-id="b8880-140">TXT</span><span class="sxs-lookup"><span data-stu-id="b8880-140">TXT</span></span>
- <span data-ttu-id="b8880-141">WMV</span><span class="sxs-lookup"><span data-stu-id="b8880-141">WMV</span></span>
- <span data-ttu-id="b8880-142">XLS</span><span class="sxs-lookup"><span data-stu-id="b8880-142">XLS</span></span>
- <span data-ttu-id="b8880-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="b8880-143">XLSX</span></span>
- <span data-ttu-id="b8880-144">XML</span><span class="sxs-lookup"><span data-stu-id="b8880-144">XML</span></span>
- <span data-ttu-id="b8880-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="b8880-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="b8880-146">Odeslat soubor</span><span class="sxs-lookup"><span data-stu-id="b8880-146">Upload a file</span></span>

<span data-ttu-id="b8880-147">Pokud chcete odeslat soubor do konfigurátoru webu v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="b8880-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b8880-148">V levém navigačním podokně vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="b8880-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="b8880-149">Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.</span><span class="sxs-lookup"><span data-stu-id="b8880-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="b8880-150">V Průzkumníkovi souborů vyberte jeden nebo více souborů a pak vyberte možnost **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="b8880-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="b8880-151">V dialogovém okně **Odeslat mediální položku** zadejte podle potřeby název, popis a metadata klíčových slov.</span><span class="sxs-lookup"><span data-stu-id="b8880-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="b8880-152">Chcete-li publikovat soubory ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.</span><span class="sxs-lookup"><span data-stu-id="b8880-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="b8880-153">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8880-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8880-154">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b8880-154">Additional resources</span></span>

[<span data-ttu-id="b8880-155">Přehled správy digitálního majetku</span><span class="sxs-lookup"><span data-stu-id="b8880-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="b8880-156">Odeslat obrázky</span><span class="sxs-lookup"><span data-stu-id="b8880-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="b8880-157">Odeslat video</span><span class="sxs-lookup"><span data-stu-id="b8880-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="b8880-158">Oříznout obrázky</span><span class="sxs-lookup"><span data-stu-id="b8880-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="b8880-159">Přizpůsobit fokální místa obrázku</span><span class="sxs-lookup"><span data-stu-id="b8880-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
