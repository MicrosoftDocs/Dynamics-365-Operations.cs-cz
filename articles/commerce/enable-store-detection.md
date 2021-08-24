---
title: Povolení zjišťování obchodu na základě polohy
description: Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98aa781a42b1c82cc00c8a680007b7200e9c7413fb8e3a67b0c723ff62c1d8e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749869"
---
# <a name="enable-location-based-store-detection"></a>Povolení zjišťování obchodu na základě polohy

[!include [banner](includes/banner.md)]

Tohle téma popisuje, jak zapnout zjišťování obchodu na základě polohy pro web Dynamics 365 Commerce.

Zjišťování obchodu na základě polohy umožňuje poskytovat zákazníkům relevantní obsah webu na základě jejich umístění. Je-li zapnuto zjišťování obchodu na základě polohy, služba vykreslování Commerce používá informace o zemi nebo oblasti z IP adresy webového prohlížeče zákazníka k nasměrování zákazníka na nejvhodnější geografickou konfiguraci webu, která je k dispozici.

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Pokud zapnete funkci zjišťování obchodu na základě polohy, budou informace z prohlížeče zákazníka odeslány do služby zjišťování polohy Microsoft. Tyto informace pak slouží k poskytnutí obsahu zákazníkovi, který je relevantní pro jeho umístění. Informace, které jsou odeslány z prohlížeče zákazníka, a informace na základě umístění, které jsou vráceny zákazníkovi, podléhají zásadám ochrany osobních údajů a souborů cookie.

## <a name="turn-on-location-based-store-detection"></a>Zapnutí zjišťování obchodu na základě polohy

Chcete-li zapnout zjišťování obchodu na základě polohy, postupujte podle následujících kroků.

1. Ve nástroji pro tvorbu obsahu přejděte ke svému webu.
1. V navigačním podokně nalevo vyberte položku **Správa webu**.
1. Vyberte **Nastavení webu**.
1. Nastavte možnost **Povolit zjišťování obchodu na základě polohy** na hodnotu **Zapnuto**.

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

[Přidání podpory pro síť CDN](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
