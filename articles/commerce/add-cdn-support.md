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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646032"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="442fb-103">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="442fb-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="442fb-104">V tomto tématu je popsán postup při přidání sítě pro doručování obsahu (CDN) do prostředí Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="442fb-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="442fb-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="442fb-105">Overview</span></span>

<span data-ttu-id="442fb-106">Pokud zřídíte prostředí elektronického obchodu v řešení Dynamics 365 Commerce, můžete jej nakonfigurovat tak, aby spolupracovalo se službou CDN.</span><span class="sxs-lookup"><span data-stu-id="442fb-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="442fb-107">Vaši vlastní doménu lze povolit během procesu zřízení pro vaše prostředí elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="442fb-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="442fb-108">Další možností je k jejímu nastavení použít servisní požadavek až po dokončení procesu zřízení.</span><span class="sxs-lookup"><span data-stu-id="442fb-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="442fb-109">Proces zřízení pro prostředí elektronického obchodu generuje název hostitele, který je přidružen k prostředí.</span><span class="sxs-lookup"><span data-stu-id="442fb-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="442fb-110">Tento název hostitele má následující formát, kde \<*e-commerce-tenant-name*\> je název vašeho prostředí:</span><span class="sxs-lookup"><span data-stu-id="442fb-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="442fb-111">&lt;název-klienta-prostředí-elektronického-obchodu&gt;commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="442fb-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="442fb-112">Název hostitele nebo koncový bod, který je generován během procesu zřízení, podporuje certifikát SSL (Secure Sockets Layer) pouze pro \*commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="442fb-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="442fb-113">Nepodporuje protokol SSL pro vlastní domény.</span><span class="sxs-lookup"><span data-stu-id="442fb-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="442fb-114">V takovém případě je nutné ukončit protokol SSL pro vlastní domény v síti CDN a předat komunikaci ze sítě CDN názvu hostitele nebo koncovému bodu, který vytvořilo řešení Commerce.</span><span class="sxs-lookup"><span data-stu-id="442fb-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="442fb-115">Kromě toho, *statické objekty* (soubory JavaScript nebo \[CSS\]) z řešení Commerce jsou dále obsluhovány z koncového bodu vygenerovaného řešením Commerce (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="442fb-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="442fb-116">Statické objekty mohou být uloženy do mezipaměti pouze v případě, že název hostitele nebo koncový bod, který řešení Commerce vygenerovalo, se nachází za CDN.</span><span class="sxs-lookup"><span data-stu-id="442fb-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="442fb-117">Nastavit formát SSL</span><span class="sxs-lookup"><span data-stu-id="442fb-117">Set up SSL</span></span>

<span data-ttu-id="442fb-118">Chcete-li zaručit, že je konfigurován protokol SSL a že jsou statické objekty uloženy do mezipaměti, je nutné nakonfigurovat síť CDN tak, aby byla přidružena k názvu hostitele, který řešení Commerce vygenerovalo pro vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="442fb-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="442fb-119">Je také nutné uložit do mezipaměti následující vzor výhradně pro statické objekty:</span><span class="sxs-lookup"><span data-stu-id="442fb-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="442fb-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="442fb-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="442fb-121">Po zřízení vašeho prostředí Commerce s vlastní doménou, která je k dispozici, nebo po zadání vlastní domény pro dané prostředí pomocí požadavku na službu nasměrujte vlastní doménu na název hostitele nebo koncový bod vytvoření řešením Commerce.</span><span class="sxs-lookup"><span data-stu-id="442fb-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="442fb-122">Jak bylo uvedeno dříve, vygenerovaný název hostitele nebo koncový bod podporuje certifikát SSL pouze pro \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="442fb-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="442fb-123">Nepodporuje protokol SSL pro vlastní domény.</span><span class="sxs-lookup"><span data-stu-id="442fb-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="442fb-124">Služby CDN</span><span class="sxs-lookup"><span data-stu-id="442fb-124">CDN services</span></span>

<span data-ttu-id="442fb-125">Jakoukoli službu CDN lze používat v prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="442fb-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="442fb-126">Zde jsou dva příklady:</span><span class="sxs-lookup"><span data-stu-id="442fb-126">Here are two examples:</span></span>

- <span data-ttu-id="442fb-127">**Microsoft Azure Front Door Service** – řešení Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="442fb-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="442fb-128">Další informace o řešení Azure Front Door Service naleznete [v dokumentaci k Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="442fb-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="442fb-129">**Akamai Dynamic Site Accelerator** – další informace viz [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="442fb-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="442fb-130">Nastavení CDN</span><span class="sxs-lookup"><span data-stu-id="442fb-130">CDN setup</span></span>

<span data-ttu-id="442fb-131">Proces nastavení CDN se skládá z následujících obecných kroků:</span><span class="sxs-lookup"><span data-stu-id="442fb-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="442fb-132">Přidejte hostitele front-endu.</span><span class="sxs-lookup"><span data-stu-id="442fb-132">Add a front-end host.</span></span>
1. <span data-ttu-id="442fb-133">Nakonfigurujte back-endový fond.</span><span class="sxs-lookup"><span data-stu-id="442fb-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="442fb-134">Nastavte pravidla pro směrování a ukládání do mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="442fb-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="442fb-135">Přidání hostitele front-endu</span><span class="sxs-lookup"><span data-stu-id="442fb-135">Add a front-end host</span></span>

<span data-ttu-id="442fb-136">Je možné použít libovolnou službu CDN, ale v příkladu v tomto tématu se použije služba Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="442fb-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="442fb-137">Informace, jak nastavit službu Azure Front Door Service, naleznete v tématu [Rychlý start: Vytvoření služby Front Door pro vysoce dostoupnou globální webovou aplikaci](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="442fb-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="442fb-138">Konfigurace backendového fondu ve službě Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="442fb-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="442fb-139">Chcete-li konfigurovat backendový fond ve službě Azure Front Door Service, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="442fb-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="442fb-140">Přidejte **&lt;název-klienta-prostředí-elektronického-obchodování&gt;.commerce.dynamics.com** do backendového fondu jako vlastního hostitele s prázdným záhlavím.</span><span class="sxs-lookup"><span data-stu-id="442fb-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="442fb-141">V části **Vyrovnávání zátěže** ponechte výchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="442fb-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="442fb-142">Následující ilustrace znázorňuje dialogové okno **Přidat backend** služby Azure Front Door Service s vloženým názvem hostitele backendu.</span><span class="sxs-lookup"><span data-stu-id="442fb-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Dialogové okno Přidat back-endový fond](./media/CDN_BackendPool.png)

<span data-ttu-id="442fb-144">Následující ilustrace znázorňuje dialogové okno **Přidat backendový pool** služby Azure Front Door Service s výchozími hodnotami vyrovnávání zatížení.</span><span class="sxs-lookup"><span data-stu-id="442fb-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Pokračování dialogového okna Přidat back-endový fond](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="442fb-146">Nastavení pravidel ve službě Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="442fb-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="442fb-147">Chcete-li nastavit pravidlo směrování ve službě Azure Front Door Service, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="442fb-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="442fb-148">Přidejte pravidlo směrování.</span><span class="sxs-lookup"><span data-stu-id="442fb-148">Add a routing rule.</span></span>
1. <span data-ttu-id="442fb-149">Do pole **Název** zadejte **výchozí**.</span><span class="sxs-lookup"><span data-stu-id="442fb-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="442fb-150">V poli **Přijatý protokol** vyberte možnost **HTTP a HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="442fb-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="442fb-151">Do pole **Hostitelé front-endu** zadejte **název-klienta-elektronického-obchodování-dynamics.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="442fb-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="442fb-152">V části **Vzory, které se mají vyhledat** zadejte do horního pole položku **/\***.</span><span class="sxs-lookup"><span data-stu-id="442fb-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="442fb-153">V části **Podrobnostipostupu** nastavte možnost **Typ postupu** na hodnotu **Vpřed**.</span><span class="sxs-lookup"><span data-stu-id="442fb-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="442fb-154">V poli **Back-endový fond** vyberte **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="442fb-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="442fb-155">Ve skupině polí **Předávací protokol** vyberte možnost **Požadavek na shodu**.</span><span class="sxs-lookup"><span data-stu-id="442fb-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="442fb-156">Nastavte možnost **Přepis adresy URL** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="442fb-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="442fb-157">Nastavte možnost **Použití mezipaměti** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="442fb-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="442fb-158">Chcete-li nastavit pravidlo použití mezipaměti ve službě Azure Front Door Service, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="442fb-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="442fb-159">Přidejte pravidlo použití mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="442fb-159">Add a caching rule.</span></span>
1. <span data-ttu-id="442fb-160">Do pole **Název** zadejte **statické objekty**.</span><span class="sxs-lookup"><span data-stu-id="442fb-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="442fb-161">V poli **Přijatý protokol** vyberte možnost **HTTP a HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="442fb-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="442fb-162">Do pole **Hostitelé front-endu** zadejte **název-klienta-elektronického-obchodování-dynamics.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="442fb-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="442fb-163">V části **Vzory, které se mají vyhledat** zadejte do horního pole **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="442fb-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="442fb-164">V části **Podrobnostipostupu** nastavte možnost **Typ postupu** na hodnotu **Vpřed**.</span><span class="sxs-lookup"><span data-stu-id="442fb-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="442fb-165">V poli **Back-endový fond** vyberte **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="442fb-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="442fb-166">Ve skupině polí **Předávací protokol** vyberte možnost **Požadavek na shodu**.</span><span class="sxs-lookup"><span data-stu-id="442fb-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="442fb-167">Nastavte možnost **Přepis adresy URL** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="442fb-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="442fb-168">Nastavte možnost **Použití mezipaměti** na hodnotu **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="442fb-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="442fb-169">V poli **Chování při ukládání řetězců dotazů do mezipaměti** vyberte možnost **Ukládat do mezipaměti každou jedinečnou adresu URL**.</span><span class="sxs-lookup"><span data-stu-id="442fb-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="442fb-170">Ve skupině polí **Dynamická komprese** vyberte možnost **Povoleno**.</span><span class="sxs-lookup"><span data-stu-id="442fb-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="442fb-171">Následující ilustrace znázorňuje dialogové okno **Přidat pravidlo** služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="442fb-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogové okno Přidat pravidlo](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="442fb-173">Pokud je doména, kterou budete používat, již aktivní a živá, vytvořte lístek podpory z dlaždice **Podpora** v [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) a získejte pomoc při dalších krocích.</span><span class="sxs-lookup"><span data-stu-id="442fb-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="442fb-174">Další informace viz [Získejte podporu pro aplikace Finance and Operations nebo Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="442fb-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="442fb-175">Pokud je vaše doména nová a nejedná se o dříve existující živou doménu, můžete svou vlastní doménu přidat do konfigurace služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="442fb-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="442fb-176">To umožní, aby se webový provoz přesměroval na váš web prostřednictvím instance Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="442fb-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="442fb-177">Chcete-li přidat vlastní doménu (například `www.fabrikam.com`), je nutné pro doménu nakonfigurovat kanonický název (CNAME).</span><span class="sxs-lookup"><span data-stu-id="442fb-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="442fb-178">Následující ilustrace znázorňuje dialogové okno **Konfigurace CNAME** služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="442fb-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogové okno Konfigurace CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="442fb-180">Službu Azure Front Door Service můžete použít ke správě certifikátu, nebo můžete pro vlastní doménu použít vlastní certifikát.</span><span class="sxs-lookup"><span data-stu-id="442fb-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="442fb-181">Následující ilustrace znázorňuje dialogové okno **HTTPS vlastní domény** služby Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="442fb-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogové okno HTTPS vlastní domény](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="442fb-183">Podrobné pokyny pro přidání vlastní domény do vašich Azure Front Door najdete na stránce [Přidejte do Front Door vlastní doménu](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="442fb-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="442fb-184">Vaše síť CDN by měla být správně nakonfigurována, aby ji bylo možné používat s webem Commerce.</span><span class="sxs-lookup"><span data-stu-id="442fb-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="442fb-185">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="442fb-185">Additional resources</span></span>

[<span data-ttu-id="442fb-186">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="442fb-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="442fb-187">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="442fb-187">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="442fb-188">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="442fb-188">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="442fb-189">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="442fb-189">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="442fb-190">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="442fb-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="442fb-191">Nahrání souborů pro hromadné přesmerování adres URL</span><span class="sxs-lookup"><span data-stu-id="442fb-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="442fb-192">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="442fb-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="442fb-193">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="442fb-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="442fb-194">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="442fb-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="442fb-195">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="442fb-195">Enable location-based store detection</span></span>](enable-store-detection.md)
