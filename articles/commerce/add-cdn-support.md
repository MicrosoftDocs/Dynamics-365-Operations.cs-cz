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
ms.openlocfilehash: 1d9482a45cb8f2ea52e7f58d55e30cfe56694d04
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985947"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Přidání podpory pro síť CDN


[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při přidání sítě pro doručování obsahu (CDN) do prostředí Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Pokud zřídíte prostředí elektronického obchodu v řešení Dynamics 365 Commerce, můžete jej nakonfigurovat tak, aby spolupracovalo se službou CDN. 

Vaši vlastní doménu lze povolit během procesu zřízení pro vaše prostředí elektronického obchodu. Další možností je k jejímu nastavení použít servisní požadavek až po dokončení procesu zřízení. Proces zřízení pro prostředí elektronického obchodu generuje název hostitele, který je přidružen k prostředí. Tento název hostitele má následující formát, kde \<*e-commerce-tenant-name*\> je název vašeho prostředí:

&lt;název-klienta-prostředí-elektronického-obchodu&gt;commerce.dynamics.com

Název hostitele nebo koncový bod, který je generován během procesu zřízení, podporuje certifikát SSL (Secure Sockets Layer) pouze pro \*commerce.dynamics.com. Nepodporuje protokol SSL pro vlastní domény. V takovém případě je nutné ukončit protokol SSL pro vlastní domény v síti CDN a předat komunikaci ze sítě CDN názvu hostitele nebo koncovému bodu, který vytvořilo řešení Commerce. 

Kromě toho, *statické objekty* (soubory JavaScript nebo \[CSS\]) z řešení Commerce jsou dále obsluhovány z koncového bodu vygenerovaného řešením Commerce (\*.commerce.dynamics.com). Statické objekty mohou být uloženy do mezipaměti pouze v případě, že název hostitele nebo koncový bod, který řešení Commerce vygenerovalo, se nachází za CDN.

## <a name="set-up-ssl"></a>Nastavit formát SSL

Chcete-li zaručit, že je konfigurován protokol SSL a že jsou statické objekty uloženy do mezipaměti, je nutné nakonfigurovat síť CDN tak, aby byla přidružena k názvu hostitele, který řešení Commerce vygenerovalo pro vaše prostředí. Je také nutné uložit do mezipaměti následující vzor výhradně pro statické objekty: 

/\_msdyn365/\_scnr/\*

Po zřízení vašeho prostředí Commerce s vlastní doménou, která je k dispozici, nebo po zadání vlastní domény pro dané prostředí pomocí požadavku na službu nasměrujte vlastní doménu na název hostitele nebo koncový bod vytvoření řešením Commerce.

Jak bylo uvedeno dříve, vygenerovaný název hostitele nebo koncový bod podporuje certifikát SSL pouze pro \*.commerce.dynamics.com. Nepodporuje protokol SSL pro vlastní domény.

## <a name="cdn-services"></a>Služby CDN

Jakoukoli službu CDN lze používat v prostředí Commerce. Zde jsou dva příklady:

- **Microsoft Azure Front Door Service** – řešení Azure CDN. Další informace o řešení Azure Front Door Service naleznete [v dokumentaci k Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – další informace viz [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>Nastavení CDN

Proces nastavení CDN se skládá z následujících obecných kroků:

1. Přidejte hostitele front-endu.
1. Nakonfigurujte back-endový fond.
1. Nastavte pravidla pro směrování a ukládání do mezipaměti.

### <a name="add-a-front-end-host"></a>Přidání hostitele front-endu

Je možné použít libovolnou službu CDN, ale v příkladu v tomto tématu se použije služba Azure Front Door Service. 

Informace, jak nastavit službu Azure Front Door Service, naleznete v tématu [Rychlý start: Vytvoření služby Front Door pro vysoce dostoupnou globální webovou aplikaci](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigurace backendového fondu ve službě Azure Front Door Service

Chcete-li konfigurovat backendový fond ve službě Azure Front Door Service, postupujte následovně.

1. Přidejte **&lt;název-klienta-prostředí-elektronického-obchodování&gt;.commerce.dynamics.com** do backendového fondu jako vlastního hostitele s prázdným záhlavím.
1. V části **Vyrovnávání zátěže** ponechte výchozí hodnoty.

Následující ilustrace znázorňuje dialogové okno **Přidat backend** služby Azure Front Door Service s vloženým názvem hostitele backendu.

![Dialogové okno Přidat back-endový fond](./media/CDN_BackendPool.png)

Následující ilustrace znázorňuje dialogové okno **Přidat backendový pool** služby Azure Front Door Service s výchozími hodnotami vyrovnávání zatížení.

![Pokračování dialogového okna Přidat back-endový fond](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Nastavení pravidel ve službě Azure Front Door Service

Chcete-li nastavit pravidlo směrování ve službě Azure Front Door Service, postupujte takto.

1. Přidejte pravidlo směrování.
1. Do pole **Název** zadejte **výchozí**.
1. V poli **Přijatý protokol** vyberte možnost **HTTP a HTTPS**.
1. Do pole **Hostitelé front-endu** zadejte **název-klienta-elektronického-obchodování-dynamics.azurefd.net**.
1. V části **Vzory, které se mají vyhledat** zadejte do horního pole položku **/\** _.
1. V části _*Podrobnosti postupu** nastavte možnost **Typ postupu** na hodnotu **Vpřed**.
1. V poli **Back-endový fond** vyberte **ecom-backend**.
1. Ve skupině polí **Předávací protokol** vyberte možnost **Požadavek na shodu**. 
1. Nastavte možnost **Přepis adresy URL** na hodnotu **Zakázáno**.
1. Nastavte možnost **Použití mezipaměti** na hodnotu **Zakázáno**.

Chcete-li nastavit pravidlo použití mezipaměti ve službě Azure Front Door Service, postupujte takto.

1. Přidejte pravidlo použití mezipaměti.
1. Do pole **Název** zadejte **statické objekty**.
1. V poli **Přijatý protokol** vyberte možnost **HTTP a HTTPS**.
1. Do pole **Hostitelé front-endu** zadejte **název-klienta-elektronického-obchodování-dynamics.azurefd.net**.
1. V části **Vzory, které se mají vyhledat** zadejte do horního pole **/\_msdyn365/\_scnr/\** _.
1. V části _*Podrobnosti postupu** nastavte možnost **Typ postupu** na hodnotu **Vpřed**.
1. V poli **Back-endový fond** vyberte **ecom-backend**.
1. Ve skupině polí **Předávací protokol** vyberte možnost **Požadavek na shodu**.
1. Nastavte možnost **Přepis adresy URL** na hodnotu **Zakázáno**.
1. Nastavte možnost **Použití mezipaměti** na hodnotu **Zakázáno**.
1. V poli **Chování při ukládání řetězců dotazů do mezipaměti** vyberte možnost **Ukládat do mezipaměti každou jedinečnou adresu URL**.
1. Ve skupině polí **Dynamická komprese** vyberte možnost **Povoleno**.

Následující ilustrace znázorňuje dialogové okno **Přidat pravidlo** služby Azure Front Door Service.

![Dialogové okno Přidat pravidlo](./media/CDN_CachingRule.png)

> [!WARNING]
> Pokud je doména, kterou budete používat, již aktivní a živá, vytvořte lístek podpory z dlaždice **Podpora** v [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) a získejte pomoc při dalších krocích. Další informace viz [Získejte podporu pro aplikace Finance and Operations nebo Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Pokud je vaše doména nová a nejedná se o dříve existující živou doménu, můžete svou vlastní doménu přidat do konfigurace služby Azure Front Door Service. To umožní, aby se webový provoz přesměroval na váš web prostřednictvím instance Azure Front Door. Chcete-li přidat vlastní doménu (například `www.fabrikam.com`), je nutné pro doménu nakonfigurovat kanonický název (CNAME).

Následující ilustrace znázorňuje dialogové okno **Konfigurace CNAME** služby Azure Front Door Service.

![Dialogové okno Konfigurace CNAME](./media/CNAME_Configuration.png)

Službu Azure Front Door Service můžete použít ke správě certifikátu, nebo můžete pro vlastní doménu použít vlastní certifikát.

Následující ilustrace znázorňuje dialogové okno **HTTPS vlastní domény** služby Azure Front Door Service.

![Dialogové okno HTTPS vlastní domény](./media/Custom_Domain_HTTPS.png)

Podrobné pokyny pro přidání vlastní domény do vašich Azure Front Door najdete na stránce [Přidejte do Front Door vlastní doménu](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).

Vaše síť CDN by měla být správně nakonfigurována, aby ji bylo možné používat s webem Commerce.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Konfigurace několika klientů B2C v prostředí Commerce](configure-multi-B2C-tenants.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)
