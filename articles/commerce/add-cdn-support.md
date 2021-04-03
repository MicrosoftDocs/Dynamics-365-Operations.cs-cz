---
title: Přidání podpory pro síť CDN
description: V tomto tématu je popsán postup při přidání sítě pro doručování obsahu (CDN) do prostředí Microsoft Dynamics 365 Commerce.
author: brianshook
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582712"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="4caaf-103">Přidání podpory sítě pro doručování obsahu (CDN)</span><span class="sxs-lookup"><span data-stu-id="4caaf-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4caaf-104">V tomto tématu je popsán postup při přidání sítě pro doručování obsahu (CDN) do prostředí Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4caaf-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="4caaf-105">Pokud zřídíte prostředí elektronického obchodu v řešení Dynamics 365 Commerce, můžete jej nakonfigurovat tak, aby spolupracovalo se službou CDN.</span><span class="sxs-lookup"><span data-stu-id="4caaf-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="4caaf-106">Vaši vlastní doménu lze povolit během procesu zřízení pro vaše prostředí elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="4caaf-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="4caaf-107">Další možností je k jejímu nastavení použít servisní požadavek až po dokončení procesu zřízení.</span><span class="sxs-lookup"><span data-stu-id="4caaf-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="4caaf-108">Proces zřízení pro prostředí elektronického obchodu generuje název hostitele, který je přidružen k prostředí.</span><span class="sxs-lookup"><span data-stu-id="4caaf-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="4caaf-109">Tento název hostitele má následující formát, kde \<*e-commerce-tenant-name*\> je název vašeho prostředí:</span><span class="sxs-lookup"><span data-stu-id="4caaf-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="4caaf-110">&lt;název-klienta-prostředí-elektronického-obchodu&gt;commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="4caaf-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="4caaf-111">Název hostitele nebo koncový bod, který je generován během procesu zřízení, podporuje certifikát SSL (Secure Sockets Layer) pouze pro \*commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="4caaf-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="4caaf-112">Nepodporuje protokol SSL pro vlastní domény.</span><span class="sxs-lookup"><span data-stu-id="4caaf-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="4caaf-113">V takovém případě je nutné ukončit protokol SSL pro vlastní domény v síti CDN a předat komunikaci ze sítě CDN názvu hostitele nebo koncovému bodu, který vytvořilo řešení Commerce.</span><span class="sxs-lookup"><span data-stu-id="4caaf-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="4caaf-114">Kromě toho, *statické objekty* (soubory JavaScript nebo \[CSS\]) z řešení Commerce jsou dále obsluhovány z koncového bodu vygenerovaného řešením Commerce (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="4caaf-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="4caaf-115">Statické objekty mohou být uloženy do mezipaměti pouze v případě, že název hostitele nebo koncový bod, který řešení Commerce vygenerovalo, se nachází za CDN.</span><span class="sxs-lookup"><span data-stu-id="4caaf-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="4caaf-116">Nastavit formát SSL</span><span class="sxs-lookup"><span data-stu-id="4caaf-116">Set up SSL</span></span>

<span data-ttu-id="4caaf-117">Chcete-li zaručit, že je konfigurován protokol SSL a že jsou statické objekty uloženy do mezipaměti, je nutné nakonfigurovat síť CDN tak, aby byla přidružena k názvu hostitele, který řešení Commerce vygenerovalo pro vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="4caaf-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="4caaf-118">Je také nutné uložit do mezipaměti následující vzor výhradně pro statické objekty:</span><span class="sxs-lookup"><span data-stu-id="4caaf-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="4caaf-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="4caaf-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="4caaf-120">Po zřízení vašeho prostředí Commerce s vlastní doménou, která je k dispozici, nebo po zadání vlastní domény pro dané prostředí pomocí požadavku na službu nasměrujte vlastní doménu na název hostitele nebo koncový bod vytvoření řešením Commerce.</span><span class="sxs-lookup"><span data-stu-id="4caaf-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="4caaf-121">Jak bylo uvedeno dříve, vygenerovaný název hostitele nebo koncový bod podporuje certifikát SSL pouze pro \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="4caaf-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="4caaf-122">Nepodporuje protokol SSL pro vlastní domény.</span><span class="sxs-lookup"><span data-stu-id="4caaf-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="4caaf-123">Služby CDN</span><span class="sxs-lookup"><span data-stu-id="4caaf-123">CDN services</span></span>

<span data-ttu-id="4caaf-124">Jakoukoli službu CDN lze používat v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="4caaf-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="4caaf-125">Zde jsou dva příklady:</span><span class="sxs-lookup"><span data-stu-id="4caaf-125">Here are two examples:</span></span>

- <span data-ttu-id="4caaf-126">**Microsoft Azure Front Door Service** – řešení Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4caaf-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="4caaf-127">Další informace o řešení Azure Front Door Service naleznete [v dokumentaci k Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="4caaf-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="4caaf-128">**Akamai Dynamic Site Accelerator** – další informace viz [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="4caaf-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="4caaf-129">Nastavení CDN</span><span class="sxs-lookup"><span data-stu-id="4caaf-129">CDN setup</span></span>

<span data-ttu-id="4caaf-130">Proces nastavení CDN se skládá z následujících obecných kroků:</span><span class="sxs-lookup"><span data-stu-id="4caaf-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="4caaf-131">Přidejte hostitele front-endu.</span><span class="sxs-lookup"><span data-stu-id="4caaf-131">Add a front-end host.</span></span>
1. <span data-ttu-id="4caaf-132">Nakonfigurujte back-endový fond.</span><span class="sxs-lookup"><span data-stu-id="4caaf-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="4caaf-133">Nastavte pravidla pro směrování a ukládání do mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="4caaf-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="4caaf-134">Přidání hostitele front-endu</span><span class="sxs-lookup"><span data-stu-id="4caaf-134">Add a front-end host</span></span>

<span data-ttu-id="4caaf-135">Je možné použít libovolnou službu CDN, ale v příkladu v tomto tématu se použije služba Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="4caaf-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="4caaf-136">Informace, jak nastavit službu Azure Front Door Service, naleznete v tématu [Rychlý start: Vytvoření služby Front Door pro vysoce dostoupnou globální webovou aplikaci](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="4caaf-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="4caaf-137">Konfigurace backendového fondu ve službě Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="4caaf-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="4caaf-138">Chcete-li konfigurovat backendový fond ve službě Azure Front Door Service, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="4caaf-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="4caaf-139">Přidejte **&lt;název-klienta-prostředí-elektronického-obchodování&gt;.commerce.dynamics.com** do backendového fondu jako vlastního hostitele s prázdným záhlavím.</span><span class="sxs-lookup"><span data-stu-id="4caaf-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="4caaf-140">V části **Vyrovnávání zátěže** ponechte výchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="4caaf-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="4caaf-141">Následující ilustrace znázorňuje dialogové okno **Přidat backend** služby Azure Front Door Service s vloženým názvem hostitele backendu.</span><span class="sxs-lookup"><span data-stu-id="4caaf-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Dialogové okno Přidat back-endový fond](./media/CDN_BackendPool.png)

<span data-ttu-id="4caaf-143">Následující ilustrace znázorňuje dialogové okno **Přidat backendový pool** služby Azure Front Door Service s výchozími hodnotami vyrovnávání zatížení.</span><span class="sxs-lookup"><span data-stu-id="4caaf-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Pokračování dialogového okna Přidat back-endový fond](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="4caaf-145">Nastavení pravidel ve službě Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="4caaf-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="4caaf-146">Chcete-li nastavit pravidlo směrování ve službě Azure Front Door Service, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="4caaf-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="4caaf-147">Přidejte pravidlo směrování.</span><span class="sxs-lookup"><span data-stu-id="4caaf-147">Add a routing rule.</span></span>
1. <span data-ttu-id="4caaf-148">Do pole **Název** zadejte **výchozí**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="4caaf-149">V poli **Přijatý protokol** vyberte možnost **HTTP a HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="4caaf-150">Do pole **Hostitelé front-endu** zadejte **název-klienta-elektronického-obchodování-dynamics.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="4caaf-151">V části **Vzory, které se mají vyhledat** zadejte do horního pole položku **/\***.</span><span class="sxs-lookup"><span data-stu-id="4caaf-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="4caaf-152">V části **Podrobnostipostupu** nastavte možnost **Typ postupu** na hodnotu **Vpřed**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="4caaf-153">V poli **Back-endový fond** vyberte **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="4caaf-154">Ve skupině polí **Předávací protokol** vyberte možnost **Požadavek na shodu**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="4caaf-155">Nastavte možnost **Přepis adresy URL** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="4caaf-156">Nastavte možnost **Použití mezipaměti** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="4caaf-157">Chcete-li nastavit pravidlo použití mezipaměti ve službě Azure Front Door Service, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="4caaf-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="4caaf-158">Přidejte pravidlo použití mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="4caaf-158">Add a caching rule.</span></span>
1. <span data-ttu-id="4caaf-159">Do pole **Název** zadejte **statické objekty**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="4caaf-160">V poli **Přijatý protokol** vyberte možnost **HTTP a HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="4caaf-161">Do pole **Hostitelé front-endu** zadejte **název-klienta-elektronického-obchodování-dynamics.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="4caaf-162">V části **Vzory, které se mají vyhledat** zadejte do horního pole **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="4caaf-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="4caaf-163">V části **Podrobnostipostupu** nastavte možnost **Typ postupu** na hodnotu **Vpřed**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="4caaf-164">V poli **Back-endový fond** vyberte **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="4caaf-165">Ve skupině polí **Předávací protokol** vyberte možnost **Požadavek na shodu**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="4caaf-166">Nastavte možnost **Přepis adresy URL** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="4caaf-167">Nastavte možnost **Použití mezipaměti** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="4caaf-168">V poli **Chování při ukládání řetězců dotazů do mezipaměti** vyberte možnost **Ukládat do mezipaměti každou jedinečnou adresu URL**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="4caaf-169">Ve skupině polí **Dynamická komprese** vyberte možnost **Povoleno**.</span><span class="sxs-lookup"><span data-stu-id="4caaf-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="4caaf-170">Následující ilustrace znázorňuje dialogové okno **Přidat pravidlo** služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="4caaf-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogové okno Přidat pravidlo](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="4caaf-172">Pokud je doména, kterou budete používat, již aktivní a živá, vytvořte lístek podpory z dlaždice **Podpora** v [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) a získejte pomoc při dalších krocích.</span><span class="sxs-lookup"><span data-stu-id="4caaf-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="4caaf-173">Další informace viz [Získejte podporu pro aplikace Finance and Operations nebo Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="4caaf-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="4caaf-174">Pokud je vaše doména nová a nejedná se o dříve existující živou doménu, můžete svou vlastní doménu přidat do konfigurace služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="4caaf-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="4caaf-175">To umožní, aby se webový provoz přesměroval na váš web prostřednictvím instance Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="4caaf-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="4caaf-176">Chcete-li přidat vlastní doménu (například `www.fabrikam.com`), je nutné pro doménu nakonfigurovat kanonický název (CNAME).</span><span class="sxs-lookup"><span data-stu-id="4caaf-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="4caaf-177">Následující ilustrace znázorňuje dialogové okno **Konfigurace CNAME** služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="4caaf-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogové okno Konfigurace CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="4caaf-179">Službu Azure Front Door Service můžete použít ke správě certifikátu, nebo můžete pro vlastní doménu použít vlastní certifikát.</span><span class="sxs-lookup"><span data-stu-id="4caaf-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="4caaf-180">Následující ilustrace znázorňuje dialogové okno **HTTPS vlastní domény** služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="4caaf-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogové okno HTTPS vlastní domény](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="4caaf-182">Podrobné pokyny pro přidání vlastní domény do vašich Azure Front Door najdete na stránce [Přidejte do Front Door vlastní doménu](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="4caaf-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="4caaf-183">Vaše síť CDN by měla být správně nakonfigurována, aby ji bylo možné používat s webem Commerce.</span><span class="sxs-lookup"><span data-stu-id="4caaf-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4caaf-184">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4caaf-184">Additional resources</span></span>

[<span data-ttu-id="4caaf-185">Možnosti implementace sítě pro doručování obsahu</span><span class="sxs-lookup"><span data-stu-id="4caaf-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
