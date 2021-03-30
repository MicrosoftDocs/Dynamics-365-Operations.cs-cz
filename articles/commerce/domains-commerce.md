---
title: Domény v Dynamics 365 Commerce
description: Tohle téma popisuje, jak se zachází s doménami v Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: bafa49cc570ddf7e0ff9c3dcb1b6902fb341b790
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225782"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="1625c-103">Domény v Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1625c-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1625c-104">Tohle téma popisuje, jak se zachází s doménami v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1625c-105">Domény jsou webové adresy používané k navigaci na weby Dynamics 365 Commerce ve webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="1625c-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="1625c-106">Správu své domény provádíte u vybraného poskytovatele serveru DNS (Domain Name Server).</span><span class="sxs-lookup"><span data-stu-id="1625c-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="1625c-107">Na domény se odkazuje v rámci konfigurátoru webů Dynamics 365 Commerce za účelem koordinace přístupu na web, když je publikován.</span><span class="sxs-lookup"><span data-stu-id="1625c-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="1625c-108">Toto téma popisuje, jak se s doménami zachází a jak se na ně odkazuje během celého životního cyklu vývoje a spuštění webu Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="1625c-109">Zřizování a podporované názvy hostitelů</span><span class="sxs-lookup"><span data-stu-id="1625c-109">Provisioning and supported host names</span></span>

<span data-ttu-id="1625c-110">Při zřizování prostředí elektronického obchodu v [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), pole **Podporované názvy hostitelů** na obrazovce zřizování elektronického obchodu se používá k zadání domén, které budou přidruženy k nasazenému prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="1625c-111">Tyto domény budou názvy zákaznických serverů DNS (Domain Name Server), na kterých budou hostovány weby elektronických obchodů.</span><span class="sxs-lookup"><span data-stu-id="1625c-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="1625c-112">Zadání domény v této fázi nepřesměruje provoz domény na Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="1625c-113">Provoz domény bude směrován pouze do koncového bodu Commerce, když se aktualizuje záznam DNS CNAME, aby se s doménou použil koncový bod Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="1625c-114">Do pole **Podporované názvy hostitelů** můžete zadat více domén oddělených středníky.</span><span class="sxs-lookup"><span data-stu-id="1625c-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="1625c-115">Následující obrázek ukazuje obrazovku pro zřízení elektronického obchodu LCS se zvýrazněným polem **Podporované názvy hostitelů**.</span><span class="sxs-lookup"><span data-stu-id="1625c-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![Obrazovka pro zřízení elektronického obchodu LCS se zvýrazněným polem **Podporované názvy hostitelů**](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="1625c-117">Pokud již došlo ke zřízení, můžete vytvořit požadavek na službu a přidat do prostředí další domény.</span><span class="sxs-lookup"><span data-stu-id="1625c-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="1625c-118">Chcete-li vytvořit požadavek na službu v LCS, přejděte ve svém prostředí na **Podpora \> Problémy s podporou** a vyberte **Odeslat incident**.</span><span class="sxs-lookup"><span data-stu-id="1625c-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="1625c-119">Adresy URL generované řešením Commerce</span><span class="sxs-lookup"><span data-stu-id="1625c-119">Commerce-generated URLs</span></span>

<span data-ttu-id="1625c-120">Při zřizování prostředí elektronického obchodu Dynamics 365 Commerce vygeneruje Commerce adresu URL, která bude pracovní adresou prostředí.</span><span class="sxs-lookup"><span data-stu-id="1625c-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="1625c-121">Tuto adresu URL obsahuje odkaz na web elektronického obchodu zobrazeném v LCS po zřízení prostředí.</span><span class="sxs-lookup"><span data-stu-id="1625c-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="1625c-122">Adresa URL generovaná řešením Comerce je ve formátu `https://<e-commerce tenant name>.commerce.dynamics.com`, kde název klienta elektronického obchodu je název zadaný v LCS pro prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="1625c-123">Můžete také použít názvy hostitelů výrobního webu v prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="1625c-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="1625c-124">Tato možnost je ideální, když budete kopírovat web z prostředí sandbox do produkčního prostředí.</span><span class="sxs-lookup"><span data-stu-id="1625c-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="1625c-125">Nastavení webu</span><span class="sxs-lookup"><span data-stu-id="1625c-125">Site setup</span></span>

<span data-ttu-id="1625c-126">Po zřízení prostředí elektronického obchodu musíte nastavit svůj web v konfigurátoru webů Commerce a přidružit jej k pracovní adrese URL.</span><span class="sxs-lookup"><span data-stu-id="1625c-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="1625c-127">Při prvním nastavení webu v konfigurátoru webů se zobrazí dialogové okno **Nastavte svůj web**.</span><span class="sxs-lookup"><span data-stu-id="1625c-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="1625c-128">Následující obrázek ukazuje dialogové okno **Nastavte svůj web** pro web s názvem „výchozí“ při prvním přístupu na web v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="1625c-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![Dialogové okno **Nastavte svůj web**](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="1625c-130">Pole **Vyberte doménu** umožňuje přidružit jeden z podporovaných názvů hostitelů poskytnutých pro váš web v LCS k vašemu webu v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="1625c-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="1625c-131">Pole **Cesta** může zůstat prázdné nebo lze přidat další řetězec cesty, který se projeví ve vaší pracovní adrese URL.</span><span class="sxs-lookup"><span data-stu-id="1625c-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="1625c-132">Při nevyplnění pole **Cesta** dojde k přidružení základní adresy URL generované řešením Commerce k webu nastavovaném v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="1625c-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="1625c-133">Cesty musí být pro každý pár web/doména jedinečná.</span><span class="sxs-lookup"><span data-stu-id="1625c-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="1625c-134">V rámci vybraného webu a domény může pouze jeden web v prostředí použít prázdnou cestu nebo být přidružen k jedinečnému řetězci cesty.</span><span class="sxs-lookup"><span data-stu-id="1625c-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="1625c-135">Libovolný řetězec přidaný do pole **Cesta** během nastavení webu se stane dílčí cestou základní adresy URL generované řešením Commerce, která se používá k přístupu na web ve webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="1625c-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="1625c-136">Cesta je také známá jako **Cesta pro párování** při přidávání kanálu do sekce konfigurace **Nastavení webu \> Kanály** v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="1625c-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="1625c-137">Například pokud máte web v konfigurátoru webů s názvem „fabrikam“ v klientu elektronického obchodu s názvem „xyz“ a pokud nastavíte web s prázdnou cestou, měli byste přístup k publikovanému obsahu webu ve webovém prohlížeči přímým přechodem na základní adresu URL generovanou řešením Commerce:</span><span class="sxs-lookup"><span data-stu-id="1625c-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="1625c-138">Alternativně, pokud byste během nastavení stejného webu přidali cestu „fabrikam“, měli byste přístup k publikovanému obsahu webu ve webovém prohlížeči pomocí následující adresy URL:</span><span class="sxs-lookup"><span data-stu-id="1625c-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="1625c-139">Stránky a adresy URL</span><span class="sxs-lookup"><span data-stu-id="1625c-139">Pages and URLs</span></span>

<span data-ttu-id="1625c-140">Jakmile má váš web nastavenu cestu, všechny adresy URL přidružené ke stránkám v konfigurátoru webů budou vycházet z funkční adresy URL (adresa generovaná řešením Commerce nebo adresa generovaná řešením Commerce plus cesta) pro daný web.</span><span class="sxs-lookup"><span data-stu-id="1625c-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="1625c-141">Vytvoření nové adresy URL v konfigurátoru webů (**URLS /> + Nová**) výběrem stránky ze seznamu v dialogovém okně **Nová adresa URL** a zadání cesty URL pro tuto stránku přidruží tuto adresu URL k vybrané stránce.</span><span class="sxs-lookup"><span data-stu-id="1625c-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="1625c-142">Hodnota cesty URL se poté připojí k pracovní adrese URL webu pro přístup na stránku a je označena jako `./<URL path>` v seznamu adres URL na stránce **Adresy URL** v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="1625c-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="1625c-143">Následující obrázek ukazuje dialogové okno **Nová adresa URL** v konfigurátoru webů se zvýrazněnou ukázkovou adresou URL.</span><span class="sxs-lookup"><span data-stu-id="1625c-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![Dialogové okno **Nová adresa URL** v konfigurátoru webů](./media/Domains_PageSetup2a.png)

<span data-ttu-id="1625c-145">Následující obrázek ukazuje stránku **Adresy URL** v konfigurátoru webů se zvýrazněnou adresou URL v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1625c-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![Možnost Spustit tok uživatele v toku zásady](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="1625c-147">Domény v konfigurátoru webů</span><span class="sxs-lookup"><span data-stu-id="1625c-147">Domains in site builder</span></span>

<span data-ttu-id="1625c-148">Podporované hodnoty názvů hostitelů jsou k dispozici k přidružení jako doména při nastavování webu.</span><span class="sxs-lookup"><span data-stu-id="1625c-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="1625c-149">Když vyberete hodnotu podporovaného názvu hostitele jako doménu, uvidíte vybranou doménu odkazovanou v celém konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="1625c-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="1625c-150">Tato doména je pouze odkazem v prostředí Commerce, živý provoz pro tuto doménu ještě nebude přeposlán do Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1625c-151">Pokud při práci s weby v konfigurátoru webů máte dva weby nastavené se dvěma různými doménami, můžete připojit atribut **?domain=** k vaší pracovní adrese URL pro přístup k publikovanému obsahu webu v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="1625c-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="1625c-152">Například bylo zřízeno prostředí „xyz“ a v konfigurátoru webů byly vytvořeny a přidruženy dva weby: jeden s doménou `www.fabrikam.com` a druhý s doménou `www.constoso.com`.</span><span class="sxs-lookup"><span data-stu-id="1625c-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="1625c-153">Každý web byl nastaven s prázdnou cestou.</span><span class="sxs-lookup"><span data-stu-id="1625c-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="1625c-154">K těmto dvěma webům je pak možné přistupovat ve webovém prohlížeči pomocí atributu **?doména=**:</span><span class="sxs-lookup"><span data-stu-id="1625c-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="1625c-155">Pokud není řetězec dotazu na doménu zadán v prostředí s více doménami, použije Commerce první doménu, kterou jste zadali.</span><span class="sxs-lookup"><span data-stu-id="1625c-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="1625c-156">Například pokud byla cesta „fabrikam“ poprvé zadána během nastavení webu, adresu URL `https://xyz.commerce.dynamics.com` lze použít pro přístup k publikovanému obsahu webu pro `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="1625c-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="1625c-157">Přesměrování provozu ve výrobě</span><span class="sxs-lookup"><span data-stu-id="1625c-157">Traffic forwarding in production</span></span>

<span data-ttu-id="1625c-158">Můžete simulovat více domén pomocí parametrů řetězce dotazu na doménu na samotném koncovém bodě commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="1625c-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="1625c-159">Ale pokud potřebujete začít fungovat ve výrobě, musíte přesměrovat provoz pro vlastní doménu na koncový bod `<e-commerce tenant name>.commerce.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="1625c-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="1625c-160">Koncový bod `<e-commerce tenant name>.commerce.dynamics.com` nepodporuje vlastní domény Secure Sockets Layers (SSL), takže musíte nastavit vlastní domény pomocí služby front door nebo sítě pro doručování obsahu (CDN).</span><span class="sxs-lookup"><span data-stu-id="1625c-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="1625c-161">Chcete-li nastavit vlastní domény pomocí služby front door nebo CDN, máte dvě možnosti:</span><span class="sxs-lookup"><span data-stu-id="1625c-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="1625c-162">Nastavit službu front door, jako je Azure Front Door, pro zpracování front-endu provozu a připojení k vašemu prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="1625c-163">To poskytuje větší kontrolu nad správou domén a certifikátů a podrobnější zásady zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="1625c-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="1625c-164">Použít instanci Azure Front Door poskytnutou řešením Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="1625c-165">To vyžaduje koordinační akci s týmem Dynamics 365 Commerce pro ověření domény a získání certifikátů SSL pro vaši doménu výroby.</span><span class="sxs-lookup"><span data-stu-id="1625c-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="1625c-166">Informace, jak přímo nastavit službu CDN, najdete v části [Přidání podpory pro síť pro doručování obsahu (CDN)](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="1625c-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="1625c-167">Chcete-li použít instanci Azure Front Door poskytnutou řešením Commerce, musíte vytvořit požadavek na službu pomoci s instalací CDN od týmu pro zprovoznění řešení Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="1625c-168">Budete muset zadat název vaší společnosti, doménu výroby, ID prostředí a název klienta elektronického obchodu výroby.</span><span class="sxs-lookup"><span data-stu-id="1625c-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="1625c-169">Budete muset potvrdit, zda se jedná o existující doménu (použitou se pro aktuálně aktivní web) nebo o novou doménu.</span><span class="sxs-lookup"><span data-stu-id="1625c-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="1625c-170">U nové domény lze ověření domény a certifikátu SSL dosáhnout v jediném kroku.</span><span class="sxs-lookup"><span data-stu-id="1625c-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="1625c-171">Pro doménu obsluhující existující webovou stránku je k vytvoření ověření domény a certifikátu SSL vyžadován vícestupňový proces.</span><span class="sxs-lookup"><span data-stu-id="1625c-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="1625c-172">Tento proces má smlouvu o rozsahu služeb (SLA) na 7 dní pro zprovoznění domény, protože zahrnuje několik postupných kroků.</span><span class="sxs-lookup"><span data-stu-id="1625c-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="1625c-173">Chcete-li vytvořit požadavek na službu v LCS, přejděte ve svém prostředí na **Podpora \> Problémy s podporou** a vyberte **Odeslat incident**.</span><span class="sxs-lookup"><span data-stu-id="1625c-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="1625c-174">Vlastní domény s SSL jsou podporovány pouze v provozních prostředích.</span><span class="sxs-lookup"><span data-stu-id="1625c-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="1625c-175">V neprovozních prostředích, jako je prostředí sandbox a testování přijetí uživatele (UAT), použijte URL generovanou řešením Commerce pro přístup k publikovanému obsahu ve webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="1625c-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="1625c-176">Proces certifikátu SSL</span><span class="sxs-lookup"><span data-stu-id="1625c-176">SSL certificate process</span></span>

<span data-ttu-id="1625c-177">Když je podána žádost o službu, tým Commerce s vámi koordinuje následující kroky.</span><span class="sxs-lookup"><span data-stu-id="1625c-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="1625c-178">Pro nové domény:</span><span class="sxs-lookup"><span data-stu-id="1625c-178">For new domains:</span></span>
- <span data-ttu-id="1625c-179">Tým Commerce nastaví instanci Azure Front Door (hostovaná v Commerce).</span><span class="sxs-lookup"><span data-stu-id="1625c-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="1625c-180">Tým Commerce poté poskytne záznam CNAME k ukázání na vaší vlastní doménu.</span><span class="sxs-lookup"><span data-stu-id="1625c-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="1625c-181">Po aktualizaci záznamu CNAME bude instance Azure Front Door hostovaná v Commerce moci ověřit vlastnictví domény a získat certifikát SSL.</span><span class="sxs-lookup"><span data-stu-id="1625c-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="1625c-182">Pro existující/aktivní domény:</span><span class="sxs-lookup"><span data-stu-id="1625c-182">For existing/active domains:</span></span>
- <span data-ttu-id="1625c-183">Tým Commerce vám dá pokyn, abyste přidali záznam CNAME `afdverify.<custom-domain>`, který poskytnete poskytovateli DNS vaší domény.</span><span class="sxs-lookup"><span data-stu-id="1625c-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="1625c-184">Po dokončení tým Commerce přidá doménu do instance Azure Front Door a poskytne další záznamy DNS TXT, které se mají přidat do DNS pro doménu.</span><span class="sxs-lookup"><span data-stu-id="1625c-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="1625c-185">Po dokončení záznamů TXT tým Commerce dokončí aktualizace Azure Front Door pro doménu, která nastaví certifikát SSL.</span><span class="sxs-lookup"><span data-stu-id="1625c-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="1625c-186">Vrcholové domény</span><span class="sxs-lookup"><span data-stu-id="1625c-186">Apex domains</span></span>

<span data-ttu-id="1625c-187">Instance Azure Front Door poskytnutá řešením Commerce nepodporuje vrcholové domény (kořenové domény, které neobsahují subdomény).</span><span class="sxs-lookup"><span data-stu-id="1625c-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="1625c-188">Vrcholové domény vyžadují k rozlišení IP adresu a instance Commerce Azure Front Door existuje pouze s virtuálními koncovými body.</span><span class="sxs-lookup"><span data-stu-id="1625c-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="1625c-189">Chcete-li použít vrcholovou doménu, máte dvě možnosti:</span><span class="sxs-lookup"><span data-stu-id="1625c-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="1625c-190">**Možnost 1** – Použijte poskytovatele DNS k přesměrování vrcholové domény na doménu „www“.</span><span class="sxs-lookup"><span data-stu-id="1625c-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="1625c-191">Například fabrikam.com přesměruje na `www.fabrikam.com`, kde `www.fabrikam.com` je záznam CNAME, který odkazuje na instanci Azure Front Door hostovanou řešením Commerce.</span><span class="sxs-lookup"><span data-stu-id="1625c-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="1625c-192">**Možnost 2** – Vytvořte vlastní instanci CDN / front door pro hostování vrcholové domény.</span><span class="sxs-lookup"><span data-stu-id="1625c-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="1625c-193">Pokud používáte Azure Front Door, musíte také nastavit Azure DNS ve stejném předplatném.</span><span class="sxs-lookup"><span data-stu-id="1625c-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="1625c-194">Vrcholová doména hostovaná na Azure DNS může odkazovat na vaše Azure Front Door jako aliasový záznam.</span><span class="sxs-lookup"><span data-stu-id="1625c-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="1625c-195">Toto je jediné řešení, protože vrcholové domény musí vždy ukazovat na IP adresu.</span><span class="sxs-lookup"><span data-stu-id="1625c-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="1625c-196">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="1625c-196">Additional resources</span></span>

  [<span data-ttu-id="1625c-197">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="1625c-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="1625c-198">Nastavení kanálu online obchodu</span><span class="sxs-lookup"><span data-stu-id="1625c-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="1625c-199">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="1625c-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="1625c-200">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="1625c-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="1625c-201">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="1625c-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="1625c-202">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="1625c-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="1625c-203">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="1625c-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="1625c-204">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="1625c-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="1625c-205">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="1625c-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="1625c-206">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="1625c-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="1625c-207">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="1625c-207">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]