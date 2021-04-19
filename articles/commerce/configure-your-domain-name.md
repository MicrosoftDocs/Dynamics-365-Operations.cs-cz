---
title: Konfigurace názvu domény
description: Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796044"
---
# <a name="configure-your-domain-name"></a>Konfigurace názvu domény


[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365. 

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