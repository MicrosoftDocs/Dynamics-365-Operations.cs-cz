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
# <a name="enable-location-based-store-detection"></a>Povolení zjišťování obchodu na základě polohy

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Zjišťování obchodu na základě polohy umožňuje poskytovat zákazníkům relevantní obsah webu na základě jejich umístění. Je-li zapnuto zjišťování obchodu na základě polohy, služba vykreslování Commerce používá informace o zemi nebo oblasti z IP adresy webového prohlížeče zákazníka k nasměrování zákazníka na nejvhodnější geografickou konfiguraci webu, která je k dispozici.

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Pokud zapnete funkci zjišťování obchodu na základě polohy, budou informace z prohlížeče zákazníka odeslány do služby zjišťování polohy Microsoft. Tyto informace pak slouží k poskytnutí obsahu zákazníkovi, který je relevantní pro jeho umístění. Informace, které jsou odeslány z prohlížeče zákazníka, a informace na základě umístění, které jsou vráceny zákazníkovi, podléhají zásadám ochrany osobních údajů a souborů cookie.

## <a name="turn-on-location-based-store-detection"></a>Zapnutí zjišťování obchodu na základě polohy

Chcete-li zapnout zjišťování obchodu na základě polohy, postupujte podle následujících kroků.

1. Ve nástroji pro tvorbu obsahu přejděte ke svému webu.
1. V navigačním podokně nalevo vyberte položku **Správa webu**.
1. Vyberte **Nastavení webu**.
1. Nastavte možnost **Povolit zjišťování obchodu na základě polohy** na hodnotu **Zapnuto**.

## <a name="additional-resources"></a>Další zdroje

[Přehled online obchodu](online-store-overview.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Nasazení nového webu elektronického obchodu](deploy-ecommerce-site.md)

[Přiřazení online webu ke kanálu](associate-site-online-store.md)

[Konfigurace názvu domény](configure-your-domain-name.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)
