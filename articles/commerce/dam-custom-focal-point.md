---
title: Přizpůsobit fokální místa obrázku
description: Toto téma popisuje, jak přizpůsobit fokální místa obrázku v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: af922e857e6bd7a58c0b9891939c8265568b549b
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269514"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="40703-103">Přizpůsobit fokální místa obrázku</span><span class="sxs-lookup"><span data-stu-id="40703-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="40703-104">Toto téma popisuje, jak přizpůsobit fokální místa obrázku v konfigurátoru webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40703-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="40703-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="40703-105">Overview</span></span>

<span data-ttu-id="40703-106">Po odeslání obrazu do knihovny médií služby Commerce Services pro konfigurátor systému se systém pokusí určit fokální místo obrázku.</span><span class="sxs-lookup"><span data-stu-id="40703-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="40703-107">Pokud například obrázek obsahuje osobu, systém ve výchozím nastavení nastaví fokální místo na obličej této osoby.</span><span class="sxs-lookup"><span data-stu-id="40703-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="40703-108">Ve většině případů se automaticky nastaví fokální bod dobře pro všechna zobrazení, ale někdy můžete chtít upravit fokální bod, aby se zajistilo, že určitá část obrazu bude vždy viditelná.</span><span class="sxs-lookup"><span data-stu-id="40703-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="40703-109">Definovat vlastní fokální bod pro obrázek</span><span class="sxs-lookup"><span data-stu-id="40703-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="40703-110">Chcete-li definovat vlastní fokální bod pro obrázek, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="40703-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="40703-111">V levém navigačním podokně konfigurátoru webu Commerce vyberte položku **Knihovna médií**.</span><span class="sxs-lookup"><span data-stu-id="40703-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="40703-112">V hlavním okně vyberte obrázek, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="40703-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="40703-113">Na příkazovém řádku vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="40703-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="40703-114">Vyberte obrázek pro **Režim úprav**.</span><span class="sxs-lookup"><span data-stu-id="40703-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="40703-115">V nabídce **Režim úprav** vyberte **Změnit fokální bod**.</span><span class="sxs-lookup"><span data-stu-id="40703-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="40703-116">Nad obrázkem se zobrazí kruhový ovládací prvek fokálního bodu.</span><span class="sxs-lookup"><span data-stu-id="40703-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="40703-117">Vyberte ovládací prvek fokálního bodu, abyste jej přesunuli na požadovaný fokální bod.</span><span class="sxs-lookup"><span data-stu-id="40703-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="40703-118">Až skončíte, vyberte v panelu příkazů **Uložit** a pak vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="40703-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40703-119">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="40703-119">Additional resources</span></span>

[<span data-ttu-id="40703-120">Přehled správy digitálního majetku</span><span class="sxs-lookup"><span data-stu-id="40703-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="40703-121">Odeslat obrázky</span><span class="sxs-lookup"><span data-stu-id="40703-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="40703-122">Odeslat video</span><span class="sxs-lookup"><span data-stu-id="40703-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="40703-123">Odeslat soubory</span><span class="sxs-lookup"><span data-stu-id="40703-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="40703-124">Oříznout obrázky</span><span class="sxs-lookup"><span data-stu-id="40703-124">Crop images</span></span>](dam-crop-images.md)
