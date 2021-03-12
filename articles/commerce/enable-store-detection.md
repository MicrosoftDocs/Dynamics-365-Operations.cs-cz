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
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000714"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="f9517-103">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="f9517-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f9517-104">Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f9517-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="f9517-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="f9517-105">Overview</span></span>

<span data-ttu-id="f9517-106">Zjišťování obchodu na základě polohy umožňuje poskytovat zákazníkům relevantní obsah webu na základě jejich umístění.</span><span class="sxs-lookup"><span data-stu-id="f9517-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="f9517-107">Je-li zapnuto zjišťování obchodu na základě polohy, služba vykreslování Commerce používá informace o zemi nebo oblasti z IP adresy webového prohlížeče zákazníka k nasměrování zákazníka na nejvhodnější geografickou konfiguraci webu, která je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f9517-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f9517-108">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="f9517-108">Privacy notice</span></span>

<span data-ttu-id="f9517-109">Pokud zapnete funkci zjišťování obchodu na základě polohy, budou informace z prohlížeče zákazníka odeslány do služby zjišťování polohy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f9517-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="f9517-110">Tyto informace pak slouží k poskytnutí obsahu zákazníkovi, který je relevantní pro jeho umístění.</span><span class="sxs-lookup"><span data-stu-id="f9517-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="f9517-111">Informace, které jsou odeslány z prohlížeče zákazníka, a informace na základě umístění, které jsou vráceny zákazníkovi, podléhají zásadám ochrany osobních údajů a souborů cookie.</span><span class="sxs-lookup"><span data-stu-id="f9517-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="f9517-112">Zapnutí zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="f9517-112">Turn on location-based store detection</span></span>

<span data-ttu-id="f9517-113">Chcete-li zapnout zjišťování obchodu na základě polohy, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="f9517-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f9517-114">Ve nástroji pro tvorbu obsahu přejděte ke svému webu.</span><span class="sxs-lookup"><span data-stu-id="f9517-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="f9517-115">V navigačním podokně nalevo vyberte položku **Správa webu**.</span><span class="sxs-lookup"><span data-stu-id="f9517-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="f9517-116">Vyberte **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="f9517-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="f9517-117">Nastavte možnost **Povolit zjišťování obchodu na základě polohy** na hodnotu **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="f9517-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9517-118">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f9517-118">Additional resources</span></span>

[<span data-ttu-id="f9517-119">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="f9517-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f9517-120">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="f9517-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f9517-121">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="f9517-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f9517-122">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="f9517-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f9517-123">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="f9517-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f9517-124">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="f9517-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f9517-125">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="f9517-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="f9517-126">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="f9517-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f9517-127">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="f9517-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="f9517-128">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="f9517-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
