---
title: Konfigurace názvu domény
description: Tento článek vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 298ce84008e60cc82a494320b6a41f35338508c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278617"
---
# <a name="configure-your-domain-name"></a>Konfigurace názvu domény


[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>Přidání domén při inicializaci elektronického obchodu

Chcete-li přidružit domény k prostředí elektronického obchodu Dynamics 365 Commerce, inicializujte elektronický obchod způsobem popsaným v tématu [Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md). Během inicializace budete požádáni o poskytnutí informací, které budou použity k zajištění prostředí elektronického obchodu. V poli **Podporované názvy hostitelů** přidejte všechny domény, které chcete používat s tímto prostředím. Více domén je třeba oddělit středníkem. Tímto způsobem jsou domény konfigurovány ve všech požadovaných součástech elektronického obchodu a jsou připraveny k použití při přepnutí provozu ze sítě CDN (Content Delivery Network) nebo z webového serveru a ukazují na front-endy elektronického obchodu.

## <a name="add-domains-after-e-commerce-initialization"></a>Přidání domén po inicializaci elektronického obchodu

Chcete-li po inicializaci elektronického obchodu přidružit nové domény k prostředí elektronického obchodu, je nutné odeslat požadavek na službu.

## <a name="additional-resources"></a>Další prostředky

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Konfigurace několika klientů B2C v prostředí Commerce](configure-multi-B2C-tenants.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
