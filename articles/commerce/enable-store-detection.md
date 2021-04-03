---
title: Povolení zjišťování obchodu na základě polohy
description: Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b34f156642b23f7b9754dac1ee81c7d0004872d8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478181"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="3f6e4-103">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="3f6e4-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f6e4-104">Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="3f6e4-105">Zjišťování obchodu na základě polohy umožňuje poskytovat zákazníkům relevantní obsah webu na základě jejich umístění.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="3f6e4-106">Je-li zapnuto zjišťování obchodu na základě polohy, služba vykreslování Commerce používá informace o zemi nebo oblasti z IP adresy webového prohlížeče zákazníka k nasměrování zákazníka na nejvhodnější geografickou konfiguraci webu, která je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="3f6e4-107">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="3f6e4-107">Privacy notice</span></span>

<span data-ttu-id="3f6e4-108">Pokud zapnete funkci zjišťování obchodu na základě polohy, budou informace z prohlížeče zákazníka odeslány do služby zjišťování polohy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="3f6e4-109">Tyto informace pak slouží k poskytnutí obsahu zákazníkovi, který je relevantní pro jeho umístění.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="3f6e4-110">Informace, které jsou odeslány z prohlížeče zákazníka, a informace na základě umístění, které jsou vráceny zákazníkovi, podléhají zásadám ochrany osobních údajů a souborů cookie.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="3f6e4-111">Zapnutí zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="3f6e4-111">Turn on location-based store detection</span></span>

<span data-ttu-id="3f6e4-112">Chcete-li zapnout zjišťování obchodu na základě polohy, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3f6e4-113">Ve nástroji pro tvorbu obsahu přejděte ke svému webu.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="3f6e4-114">V navigačním podokně nalevo vyberte položku **Správa webu**.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="3f6e4-115">Vyberte **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="3f6e4-116">Nastavte možnost **Povolit zjišťování obchodu na základě polohy** na hodnotu **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f6e4-117">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3f6e4-117">Additional resources</span></span>

[<span data-ttu-id="3f6e4-118">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="3f6e4-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3f6e4-119">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3f6e4-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3f6e4-120">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3f6e4-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3f6e4-121">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="3f6e4-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3f6e4-122">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="3f6e4-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3f6e4-123">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="3f6e4-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="3f6e4-124">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="3f6e4-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="3f6e4-125">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="3f6e4-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3f6e4-126">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="3f6e4-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="3f6e4-127">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="3f6e4-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
