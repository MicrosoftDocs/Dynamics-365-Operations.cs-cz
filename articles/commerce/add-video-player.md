---
title: Modul přehrávače videa
description: Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025636"
---
# <a name="video-player-module"></a><span data-ttu-id="6e79b-103">Modul přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="6e79b-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6e79b-104">Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e79b-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6e79b-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="6e79b-105">Overview</span></span>

<span data-ttu-id="6e79b-106">Modul přehrávače videa se používá k podpoře přehrávání videa.</span><span class="sxs-lookup"><span data-stu-id="6e79b-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="6e79b-107">Lze jej přidat na libovolnou stránku za předpokladu, že se obsah videa nahrává do systému správy obsahu (CMS) a je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="6e79b-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="6e79b-108">Modul přehrávače videa podporuje typ média MP4.</span><span class="sxs-lookup"><span data-stu-id="6e79b-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="6e79b-109">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="6e79b-109">Video player module</span></span>

<span data-ttu-id="6e79b-110">Modul přehrávače videa lze použít k prezentaci videí na webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="6e79b-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="6e79b-111">Podporuje všechny schopnosti přehrávání, jako je například přehrávání, pozastavení, režim úplné velikosti, audio popis a skryté titulky.</span><span class="sxs-lookup"><span data-stu-id="6e79b-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="6e79b-112">Modul přehrávače videa podporuje také přizpůsobení skrytých titulků, které vyhovují standardům přístupnosti.</span><span class="sxs-lookup"><span data-stu-id="6e79b-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="6e79b-113">Můžete například přizpůsobit velikost písma a barvu pozadí.</span><span class="sxs-lookup"><span data-stu-id="6e79b-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="6e79b-114">Modul přehrávače videa také podporuje sekundární zvukové stopy.</span><span class="sxs-lookup"><span data-stu-id="6e79b-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="6e79b-115">Po nahrání videa do CMS lze také nahrát sekundární zvukovou stopu.</span><span class="sxs-lookup"><span data-stu-id="6e79b-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="6e79b-116">Modul přehrávače videa pak může přehrávat sekundární zvukovou stopu, pokud ji uživatel vybere.</span><span class="sxs-lookup"><span data-stu-id="6e79b-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="6e79b-117">Příklady modulů přehrávače videa v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="6e79b-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="6e79b-118">Instruktážní videa na stránkách s podrobnostmi o produktech nebo na marketingových stránkách</span><span class="sxs-lookup"><span data-stu-id="6e79b-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="6e79b-119">Reklamní videa a videa o zásadách na marketingové stránce</span><span class="sxs-lookup"><span data-stu-id="6e79b-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="6e79b-120">Marketingová videa se zvýrazněním charakteristik produktů na stránkách s podrobnostmi o produktech nebo na marketingových stránkách</span><span class="sxs-lookup"><span data-stu-id="6e79b-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="6e79b-121">Vlastnosti modulu přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="6e79b-121">Video player module properties</span></span>

| <span data-ttu-id="6e79b-122">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="6e79b-122">Property name</span></span>         | <span data-ttu-id="6e79b-123">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6e79b-123">Value</span></span>                               | <span data-ttu-id="6e79b-124">Popis</span><span class="sxs-lookup"><span data-stu-id="6e79b-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="6e79b-125">Automatické přehrání</span><span class="sxs-lookup"><span data-stu-id="6e79b-125">Auto play</span></span>             | <span data-ttu-id="6e79b-126">**Pravda** nebo **Nepravda**</span><span class="sxs-lookup"><span data-stu-id="6e79b-126">**True** or **False**</span></span>               | <span data-ttu-id="6e79b-127">Je-li hodnota nastavena na **Pravda**, video se automaticky přehraje.</span><span class="sxs-lookup"><span data-stu-id="6e79b-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="6e79b-128">Ztlumit</span><span class="sxs-lookup"><span data-stu-id="6e79b-128">Mute</span></span>                  | <span data-ttu-id="6e79b-129">**Pravda** nebo **Nepravda**</span><span class="sxs-lookup"><span data-stu-id="6e79b-129">**True** or **False**</span></span>               | <span data-ttu-id="6e79b-130">Je-li hodnota nastavena na **Pravda**, zvuk je ztlumen.</span><span class="sxs-lookup"><span data-stu-id="6e79b-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="6e79b-131">Pro tento přehrávač je výchozí hodnota **Nepravda**.</span><span class="sxs-lookup"><span data-stu-id="6e79b-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="6e79b-132">V prohlížeči Chrome je ve výchozím nastavení ztlumeno přehrávání videozáznamů a zvuk je přehráván pouze v případě, že uživatel video přehrává ručně.</span><span class="sxs-lookup"><span data-stu-id="6e79b-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="6e79b-133">Smyčka</span><span class="sxs-lookup"><span data-stu-id="6e79b-133">Loop</span></span>                  | <span data-ttu-id="6e79b-134">**Pravda** nebo **Nepravda**</span><span class="sxs-lookup"><span data-stu-id="6e79b-134">**True** or **False**</span></span>               | <span data-ttu-id="6e79b-135">Je-li hodnota nastavena na **Pravda**, video se opakuje ve smyčce.</span><span class="sxs-lookup"><span data-stu-id="6e79b-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="6e79b-136">Média</span><span class="sxs-lookup"><span data-stu-id="6e79b-136">Media</span></span>                 | <span data-ttu-id="6e79b-137">Cesta a název souboru videa</span><span class="sxs-lookup"><span data-stu-id="6e79b-137">Video file path and name</span></span> | <span data-ttu-id="6e79b-138">Soubor videa, který je přehráván přehrávačem videa.</span><span class="sxs-lookup"><span data-stu-id="6e79b-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="6e79b-139">Přehrání na celé obrazovce</span><span class="sxs-lookup"><span data-stu-id="6e79b-139">Play fullscreen</span></span>       | <span data-ttu-id="6e79b-140">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="6e79b-140">**True** or **False**</span></span>               | <span data-ttu-id="6e79b-141">Je-li hodnota nastavena na **Pravda**, video se přehraje v režimu celé obrazovky.</span><span class="sxs-lookup"><span data-stu-id="6e79b-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="6e79b-142">Spuštění přehrání a pozastavení</span><span class="sxs-lookup"><span data-stu-id="6e79b-142">Play pause trigger</span></span>    | <span data-ttu-id="6e79b-143">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="6e79b-143">**True** or **False**</span></span>               | <span data-ttu-id="6e79b-144">Je-li hodnota nastavena na **Pravda**, na videu se zobrazí tlačítko Přehrát/pozastavit.</span><span class="sxs-lookup"><span data-stu-id="6e79b-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="6e79b-145">Ovládací prvky přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="6e79b-145">Video player controls</span></span> | <span data-ttu-id="6e79b-146">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="6e79b-146">**True** or **False**</span></span>               | <span data-ttu-id="6e79b-147">Je-li tato hodnota nastavena nahodnotu **Pravda**, zobrazí se všechny ovládací prvky přehrávače videa.</span><span class="sxs-lookup"><span data-stu-id="6e79b-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="6e79b-148">Tyto ovládací prvky zahrnují tlačítka Přehrát a Pozastavit, ukazatel průběhu a možnosti skrytých titulků.</span><span class="sxs-lookup"><span data-stu-id="6e79b-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="6e79b-149">Skrýt obrázek plakátu</span><span class="sxs-lookup"><span data-stu-id="6e79b-149">Hide poster image</span></span>     | <span data-ttu-id="6e79b-150">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="6e79b-150">**True** or **False**</span></span>               | <span data-ttu-id="6e79b-151">Video může mít titulní snímek.</span><span class="sxs-lookup"><span data-stu-id="6e79b-151">A video can have a poster frame.</span></span> <span data-ttu-id="6e79b-152">Je-li tato vlastnost nastavena na hodnotu **Pravda**, je titulní snímek skrytý.</span><span class="sxs-lookup"><span data-stu-id="6e79b-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="6e79b-153">Úroveň masky</span><span class="sxs-lookup"><span data-stu-id="6e79b-153">Mask level</span></span>            | <span data-ttu-id="6e79b-154">Číslo od **0** do **100**</span><span class="sxs-lookup"><span data-stu-id="6e79b-154">A number from **0** through **100**</span></span> | <span data-ttu-id="6e79b-155">Maska použitá na video pro úpravu stylů.</span><span class="sxs-lookup"><span data-stu-id="6e79b-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="6e79b-156">Přidání modulu přehrávače videa na stránku</span><span class="sxs-lookup"><span data-stu-id="6e79b-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="6e79b-157">Před vytvořením modulu přehrávače videa je nejprve nutné odeslat video do knihovny médií.</span><span class="sxs-lookup"><span data-stu-id="6e79b-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="6e79b-158">Chcete-li přidat modul přehrávače videa na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6e79b-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6e79b-159">Vytvořte šablonu stránky s názvem **Šablona přehrávače videa**.</span><span class="sxs-lookup"><span data-stu-id="6e79b-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="6e79b-160">V pozici **Hlavní** na výchozí stránce přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="6e79b-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="6e79b-161">V modulu kontejneru přidejte moduly přehrávače videa a přehrávače ambientního videa.</span><span class="sxs-lookup"><span data-stu-id="6e79b-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="6e79b-162">Dokončete úpravy šablony a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="6e79b-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="6e79b-163">Šablonu přehrávače videa, kterou jste vytvořili, použijte pro vytvoření stránky s názvem **Stránka přehrávače videa**.</span><span class="sxs-lookup"><span data-stu-id="6e79b-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="6e79b-164">V pozici **Hlavní** nové stránky přidejte modul přehrávače videa.</span><span class="sxs-lookup"><span data-stu-id="6e79b-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="6e79b-165">V podokně vlastností modulu přehrávač videa vyberte možnost **Přidat video**.</span><span class="sxs-lookup"><span data-stu-id="6e79b-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="6e79b-166">V dialogovém okně **Výběr média** vyberte video a poté vyberte možnost **Odeslat novou mediální položku**.</span><span class="sxs-lookup"><span data-stu-id="6e79b-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="6e79b-167">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="6e79b-167">Save and preview the page.</span></span> <span data-ttu-id="6e79b-168">Na stránce by měl být zobrazen modul videa.</span><span class="sxs-lookup"><span data-stu-id="6e79b-168">You should see the video module on the page.</span></span> <span data-ttu-id="6e79b-169">Chcete-li přizpůsobit chování modulu, můžete změnit další nastavení.</span><span class="sxs-lookup"><span data-stu-id="6e79b-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="6e79b-170">Dokončete úpravy stránky a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="6e79b-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e79b-171">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="6e79b-171">Additional resources</span></span>

[<span data-ttu-id="6e79b-172">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="6e79b-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6e79b-173">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="6e79b-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="6e79b-174">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="6e79b-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="6e79b-175">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="6e79b-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6e79b-176">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="6e79b-176">Content block module</span></span>](add-hero-module.md)
