---
title: Konfigurace názvu domény
description: Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f73c034563fb1cc6b05091b4c47e2a788d1a8b6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945529"
---
# <a name="configure-your-domain-name"></a>Konfigurace názvu domény

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>Přidání domén při inicializaci elektronického obchodu

Chcete-li přidružit domény k prostředí elektronického obchodu, inicializujte elektronický obchod způsobem popsaným v tématu [Nasazení nového webu elektronického obchodu](deploy-ecommerce-site.md). Během inicializace budete požádáni o poskytnutí informací, které budou použity k zajištění prostředí elektronického obchodu. V poli **Podporované názvy hostitelů** přidejte všechny domény, které chcete používat s tímto prostředím. Více domén je třeba oddělit středníkem. Tímto způsobem jsou domény konfigurovány ve všech požadovaných součástech elektronického obchodu a jsou připraveny k použití při přepnutí provozu ze sítě CDN (Content Delivery Network) nebo z webového serveru a ukazují na front-endy elektronického obchodu.

## <a name="add-domains-after-e-commerce-initialization"></a>Přidání domén po inicializaci elektronického obchodu

Chcete-li po inicializaci elektronického obchodu přidružit nové domény k prostředí elektronického obchodu, je nutné odeslat požadavek na službu.

## <a name="additional-resources"></a>Další zdroje

[Nasazení nového webu elektronického obchodu](deploy-ecommerce-site.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přiřazení online webu ke kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)
