---
title: Oříznutí obrázků
description: Toto téma popisuje, jak oříznout obrázky v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 7af1378e26368c4f35f4661f41c066baeaa09803
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222578"
---
# <a name="crop-images"></a><span data-ttu-id="5e6c1-103">Oříznutí obrázků</span><span class="sxs-lookup"><span data-stu-id="5e6c1-103">Crop images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e6c1-104">Toto téma popisuje, jak oříznout obrázky v konfigurátoru webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-104">This topic describes how to crop images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="5e6c1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="5e6c1-105">Overview</span></span>

<span data-ttu-id="5e6c1-106">Knihovna médií konfigurátoru webu Commerce umožňuje oříznout obrázky a optimalizovat je pro různé typy a zobrazení modulů.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-106">The Commerce site builder Media Library allows you to crop images to optimize them for different module types and viewports.</span></span>

## <a name="crop-an-image"></a><span data-ttu-id="5e6c1-107">Oříznout obrázek</span><span class="sxs-lookup"><span data-stu-id="5e6c1-107">Crop an image</span></span>

<span data-ttu-id="5e6c1-108">Chcete-li oříznout obrázek v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-108">To crop an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5e6c1-109">V levém navigačním podokně konfigurátoru webu Commerce vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-109">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="5e6c1-110">V hlavním okně vyberte obrázek, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-110">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="5e6c1-111">Na příkazovém řádku vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-111">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="5e6c1-112">Vyberte obrázek pro **Režim úprav**.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-112">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="5e6c1-113">V **Režimu úprav** vyberte **Upravit zobrazení podle modulu**.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-113">Under **Edit Mode**, select **Edit View by Module**.</span></span>
1. <span data-ttu-id="5e6c1-114">Z rozevírací nabídky **Modul** vyberte typ modulu.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-114">From the **Module** drop-down menu, select the module type.</span></span>
1. <span data-ttu-id="5e6c1-115">Z rozevírací nabídky **Typ zobrazení** vyberte typ zobrazení.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-115">From the **View type** drop-down menu, select the view type.</span></span>
1. <span data-ttu-id="5e6c1-116">Z rozevírací nabídky **mmístění** vyberte umístění obrázku.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-116">From the **Placement** drop-down menu, select the image placement.</span></span>
1. <span data-ttu-id="5e6c1-117">Z rozevírací nabídky **Zobrazení** vyberte velikost zobrazení.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-117">From the **Viewport** drop-down menu, select the viewport size.</span></span>
1. <span data-ttu-id="5e6c1-118">Obrázek je překrytý oblastí, která představuje oblast oříznutí.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-118">The image is overlaid with the area representing the crop region.</span></span> <span data-ttu-id="5e6c1-119">Podle potřeby přesuňte nebo změňte velikost oblasti oříznutí.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-119">Move and resize the crop region as needed.</span></span> <span data-ttu-id="5e6c1-120">Poměr stran bude zachován automaticky.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-120">The aspect ratio will be maintained automatically.</span></span>
1. <span data-ttu-id="5e6c1-121">Až skončíte, vyberte v panelu příkazů **Uložit** a pak vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-121">When you're done, on the command bar, select **Save**, and then select **Finish editing**.</span></span> 

<span data-ttu-id="5e6c1-122">Po dokončení vlastního oříznutí se úpravy obrazu projeví téměř okamžitě.</span><span class="sxs-lookup"><span data-stu-id="5e6c1-122">After custom cropping is completed, image modifications will take effect almost immediately.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e6c1-123">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="5e6c1-123">Additional resources</span></span>

[<span data-ttu-id="5e6c1-124">Přehled správy digitálního majetku</span><span class="sxs-lookup"><span data-stu-id="5e6c1-124">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="5e6c1-125">Odeslání obrázků</span><span class="sxs-lookup"><span data-stu-id="5e6c1-125">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="5e6c1-126">Odeslání videa</span><span class="sxs-lookup"><span data-stu-id="5e6c1-126">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="5e6c1-127">Odeslat soubory</span><span class="sxs-lookup"><span data-stu-id="5e6c1-127">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="5e6c1-128">Přizpůsobení ohniska obrázku</span><span class="sxs-lookup"><span data-stu-id="5e6c1-128">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="5e6c1-129">Nahrání a obsloužení statických souborů</span><span class="sxs-lookup"><span data-stu-id="5e6c1-129">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]