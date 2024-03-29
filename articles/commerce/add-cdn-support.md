---
title: Přidání podpory sítě pro doručování obsahu (CDN)
description: V tomto článku je popsán postup při přidání sítě pro doručování obsahu (CDN) do prostředí Microsoft Dynamics 365 Commerce.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 84839c1e370dccd19462de5c4a3dc120df15df09
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275805"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Přidání podpory sítě pro doručování obsahu (CDN)

[!include [banner](includes/banner.md)]

V tomto článku je popsán postup při přidání sítě pro doručování obsahu (CDN) do prostředí Microsoft Dynamics 365 Commerce.

Pokud zřídíte prostředí elektronického obchodu v řešení Dynamics 365 Commerce, můžete jej nakonfigurovat tak, aby spolupracovalo se službou CDN. 

Vaši vlastní doménu lze povolit během procesu zřízení pro vaše prostředí elektronického obchodu. Další možností je k jejímu nastavení použít servisní požadavek až po dokončení procesu zřízení. Proces zřízení pro prostředí elektronického obchodu generuje název hostitele, který je přidružen k prostředí. Tento název hostitele má následující formát, kde \<*e-commerce-tenant-name*\> je název vašeho prostředí:

&lt;název-klienta-prostředí-elektronického-obchodu&gt;commerce.dynamics.com

Název hostitele nebo koncový bod, který je generován během procesu zřízení, podporuje certifikát SSL (Secure Sockets Layer) pouze pro \*commerce.dynamics.com. Nepodporuje protokol SSL pro vlastní domény. V takovém případě je nutné ukončit protokol SSL pro vlastní domény v síti CDN a předat komunikaci ze sítě CDN názvu hostitele nebo koncovému bodu, který vytvořilo řešení Commerce. 

Kromě toho, *statické objekty* (soubory JavaScript nebo \[CSS\]) z řešení Commerce jsou dále obsluhovány z koncového bodu vygenerovaného řešením Commerce (\*.commerce.dynamics.com). Statické objekty mohou být uloženy do mezipaměti pouze v případě, že název hostitele nebo koncový bod, který řešení Commerce vygenerovalo, se nachází za CDN.

## <a name="set-up-ssl"></a>Nastavit SSL

Po zřízení vašeho prostředí Commerce s vlastní doménou, která je zadána, nebo po zadání vlastní domény pro dané prostředí pomocí požadavku na službu musíte spolupracovat s týmem pro zaškolení Commerce pro plánování změn DNS.

Jak bylo uvedeno dříve, vygenerovaný název hostitele nebo koncový bod podporuje certifikát SSL pouze pro \*.commerce.dynamics.com. Nepodporuje protokol SSL pro vlastní domény.

## <a name="cdn-services"></a>Služby CDN

Jakoukoli službu CDN lze používat v prostředí Commerce. Zde jsou dva příklady:

- **Microsoft Azure Front Door Service** – řešení Azure CDN. Další informace o řešení Azure Front Door Service naleznete [v dokumentaci k Azure Front Door Service](/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – další informace viz [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>Nastavení CDN

Proces nastavení CDN se skládá z následujících obecných kroků:

1. Přidejte hostitele front-endu.
1. Nakonfigurujte back-endový fond.
1. Nastavení pravidel směrování.

### <a name="add-a-front-end-host"></a>Přidání hostitele front-endu

Je možné použít libovolnou službu CDN, ale v příkladu v tomto článku se použije služba Azure Front Door Service. 

Informace, jak nastavit službu Azure Front Door Service, naleznete v tématu [Rychlý start: Vytvoření služby Front Door pro vysoce dostoupnou globální webovou aplikaci](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigurace backendového fondu ve službě Azure Front Door Service

Chcete-li konfigurovat backendový fond ve službě Azure Front Door Service, postupujte následovně.

1. Přidejte **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** do back-endového fondu jako vlastního hostitele, který má záhlaví hostitele back-endu, které je stejné jako **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.
1. V části **Vyrovnávání zátěže** ponechte výchozí hodnoty.
1. Zakažte kontroly stavu back-endového fondu.

Následující ilustrace znázorňuje dialogové okno **Přidat backend** služby Azure Front Door Service s vloženým názvem hostitele backendu.

![Dialogové okno Přidat back-endový fond.](./media/CDN_BackendPool.png)

Následující ilustrace znázorňuje dialogové okno **Přidat backendový pool** služby Azure Front Door Service s výchozími hodnotami vyrovnávání zatížení.

![Pokračování dialogového okna Přidat back-endový fond.](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Nezapomeňte zakázat **Sondy stavu** při nastavování vlastní služby Azure Front Door Service pro Commerce.


### <a name="set-up-rules-in-azure-front-door-service"></a>Nastavení pravidel ve službě Azure Front Door Service

Chcete-li nastavit pravidlo směrování ve službě Azure Front Door Service, postupujte takto.

1. Přidejte pravidlo směrování.
1. Do pole **Název** zadejte **výchozí**.
1. V poli **Přijatý protokol** vyberte možnost **HTTP a HTTPS**.
1. Do pole **Hostitelé front-endu** zadejte **název-klienta-elektronického-obchodování-dynamics.azurefd.net**.
1. V části **Vzory, které se mají vyhledat** zadejte do horního pole položku **/\***.
1. V části **Podrobnostipostupu** nastavte možnost **Typ postupu** na hodnotu **Vpřed**.
1. V poli **Back-endový fond** vyberte **ecom-backend**.
1. Ve skupině polí **Předávací protokol** vyberte možnost **Požadavek na shodu**. 
1. Nastavte možnost **Přepis adresy URL** na hodnotu **Zakázáno**.
1. Nastavte možnost **Použití mezipaměti** na hodnotu **Zakázáno**.


> [!WARNING]
> Pokud je doména, kterou budete používat, již aktivní a živá, vytvořte lístek podpory z dlaždice **Podpora** v [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) a získejte pomoc při dalších krocích. Další informace získáte v článku [Získání podpory pro finanční a provozní aplikace nebo Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Pokud je vaše doména nová a nejedná se o dříve existující živou doménu, můžete svou vlastní doménu přidat do konfigurace služby Azure Front Door Service. To umožní, aby se webový provoz přesměroval na váš web prostřednictvím instance Azure Front Door. Chcete-li přidat vlastní doménu (například `www.fabrikam.com`), je nutné pro doménu nakonfigurovat kanonický název (CNAME).

Následující ilustrace znázorňuje dialogové okno **Konfigurace CNAME** služby Azure Front Door Service.

![Dialogové okno Konfigurace CNAME.](./media/CNAME_Configuration.png)

Službu Azure Front Door Service můžete použít ke správě certifikátu, nebo můžete pro vlastní doménu použít vlastní certifikát.

Následující ilustrace znázorňuje dialogové okno **HTTPS vlastní domény** služby Azure Front Door Service.

![Dialogové okno HTTPS vlastní domény.](./media/Custom_Domain_HTTPS.png)

Podrobné pokyny pro přidání vlastní domény do vašich Azure Front Door najdete na stránce [Přidejte do Front Door vlastní doménu](/azure/frontdoor/front-door-custom-domain).

Vaše síť CDN by měla být správně nakonfigurována, aby ji bylo možné používat s webem Commerce.

## <a name="additional-resources"></a>Další prostředky

[Možnosti implementace sítě pro doručování obsahu](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
