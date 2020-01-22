---
title: Povolení zjišťování obchodu na základě polohy
description: Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c5fb59a9798e2cddfb75b71235ee7754e54b0e28
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945759"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="b2d59-103">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="b2d59-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b2d59-104">Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2d59-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="b2d59-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b2d59-105">Overview</span></span>

<span data-ttu-id="b2d59-106">Zjišťování obchodu na základě polohy umožňuje poskytovat zákazníkům relevantní obsah webu na základě jejich umístění.</span><span class="sxs-lookup"><span data-stu-id="b2d59-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="b2d59-107">Je-li zapnuto zjišťování obchodu na základě polohy, služba vykreslování Commerce používá informace o zemi nebo oblasti z IP adresy webového prohlížeče zákazníka k nasměrování zákazníka na nejvhodnější geografickou konfiguraci webu, která je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="b2d59-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="b2d59-108">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="b2d59-108">Privacy notice</span></span>

<span data-ttu-id="b2d59-109">Pokud zapnete funkci zjišťování obchodu na základě polohy, budou informace z prohlížeče zákazníka odeslány do služby zjišťování polohy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2d59-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="b2d59-110">Tyto informace pak slouží k poskytnutí obsahu zákazníkovi, který je relevantní pro jeho umístění.</span><span class="sxs-lookup"><span data-stu-id="b2d59-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="b2d59-111">Informace, které jsou odeslány z prohlížeče zákazníka, a informace na základě umístění, které jsou vráceny zákazníkovi, podléhají zásadám ochrany osobních údajů a souborů cookie.</span><span class="sxs-lookup"><span data-stu-id="b2d59-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="b2d59-112">Zapnutí zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="b2d59-112">Turn on location-based store detection</span></span>

<span data-ttu-id="b2d59-113">Chcete-li zapnout zjišťování obchodu na základě polohy, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b2d59-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b2d59-114">Ve nástroji pro tvorbu obsahu přejděte ke svému webu.</span><span class="sxs-lookup"><span data-stu-id="b2d59-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="b2d59-115">V navigačním podokně nalevo vyberte položku **Správa webu**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="b2d59-116">Vyberte **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="b2d59-117">Nastavte možnost **Povolit zjišťování obchodu na základě polohy** na hodnotu **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2d59-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b2d59-118">Additional resources</span></span>

[<span data-ttu-id="b2d59-119">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="b2d59-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b2d59-120">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="b2d59-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b2d59-121">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="b2d59-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b2d59-122">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="b2d59-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b2d59-123">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="b2d59-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b2d59-124">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="b2d59-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b2d59-125">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="b2d59-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
