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
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697605"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="68e43-103">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="68e43-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="68e43-104">Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68e43-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="68e43-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="68e43-105">Overview</span></span>

<span data-ttu-id="68e43-106">Zjišťování obchodu na základě polohy umožňuje poskytovat zákazníkům relevantní obsah webu na základě jejich umístění.</span><span class="sxs-lookup"><span data-stu-id="68e43-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="68e43-107">Je-li zapnuto zjišťování obchodu na základě polohy, služba vykreslování Commerce používá informace o zemi nebo oblasti z IP adresy webového prohlížeče zákazníka k nasměrování zákazníka na nejvhodnější geografickou konfiguraci webu, která je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="68e43-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="68e43-108">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="68e43-108">Privacy notice</span></span>

<span data-ttu-id="68e43-109">Pokud zapnete funkci zjišťování obchodu na základě polohy, budou informace z prohlížeče zákazníka odeslány do služby zjišťování polohy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="68e43-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="68e43-110">Tyto informace pak slouží k poskytnutí obsahu zákazníkovi, který je relevantní pro jeho umístění.</span><span class="sxs-lookup"><span data-stu-id="68e43-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="68e43-111">Informace, které jsou odeslány z prohlížeče zákazníka, a informace na základě umístění, které jsou vráceny zákazníkovi, podléhají zásadám ochrany osobních údajů a souborů cookie.</span><span class="sxs-lookup"><span data-stu-id="68e43-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="68e43-112">Zapnutí zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="68e43-112">Turn on location-based store detection</span></span>

<span data-ttu-id="68e43-113">Chcete-li zapnout zjišťování obchodu na základě polohy, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="68e43-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="68e43-114">Ve nástroji pro tvorbu obsahu přejděte ke svému webu.</span><span class="sxs-lookup"><span data-stu-id="68e43-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="68e43-115">V navigačním podokně nalevo vyberte položku **Správa webu**.</span><span class="sxs-lookup"><span data-stu-id="68e43-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="68e43-116">Vyberte **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="68e43-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="68e43-117">Nastavte možnost **Povolit zjišťování obchodu na základě polohy** na hodnotu **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="68e43-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68e43-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="68e43-118">Additional resources</span></span>

[<span data-ttu-id="68e43-119">Přehled online obchodu</span><span class="sxs-lookup"><span data-stu-id="68e43-119">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="68e43-120">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="68e43-120">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="68e43-121">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="68e43-121">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="68e43-122">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="68e43-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="68e43-123">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="68e43-123">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="68e43-124">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="68e43-124">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="68e43-125">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="68e43-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
