---
title: Použití přidání produktu do nastavení košíku
description: Tohle téma se zabývá nastavením „Přidat produkt do košíku“ a popisuje, jak je použít v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c1d29b84d79ab503580478a1553514ddf992ca46
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2021
ms.locfileid: "6637970"
---
# <a name="apply-add-product-to-cart-settings"></a>Použití přidání produktu do nastavení košíku

[!include [banner](includes/banner.md)]

Tohle téma se zabývá nastavením **Přidat produkt do košíku** a popisuje, jak je použít v řešení Microsoft Dynamics 365 Commerce.

Když je produkt přidán do košíku na webu elektronického obchodování Dynamics 365 Commerce, jsou podporovány různé pracovní postupy. Uživatel webu může být například přenesen na stránku košíku. Alternativně může uživatel zůstat na aktuální stránce, ale může obdržet oznámení, které potvrzuje, že byl produkt přidán do košíku.

Pro podporu různých pracovních postupů, pole **Přidat produkt do košíku** je k dispozici v **Nastavení \> Rozšíření** v nástroji pro vytváření webů Commerce. Vyberte jednu z následujících možností nastavení pro implementaci odpovídajícího pracovního postupu:

- **Přejít na stránku nákupního košíku** – Když uživatelé přidají položku do košíku, jsou přesměrováni na stránku nákupního košíku.
- **Zobrazit oznámení** – Když uživatelé přidají položku do košíku, zobrazí se jim potvrzovací oznámení a poté mohou nadále procházet stránku podrobností o produktu (PDP).
- **Zobrazit minikošík** – Když uživatelé přidají položku do košíku, zobrazí se obsah minikošíku. Uživatelé mohou zkontrolovat všechny položky v košíku a mohou pokračovat k pokladně, pokud jsou připraveni.
- **Zobrazit oznámení pomocí modulu Oznámení** – Když uživatelé přidají položku do košíku, modul oznámení se používá k zobrazení potvrzovacího oznámení. Aby tato možnost nastavení fungovala, musí být do záhlaví stránky přidán modul oznámení.
- **Nepřecházet na stránku nákupního košíku** – Když uživatelé přidají položku do košíku, zůstanou na aktuální stránce.

Následující obrázek ukazuje příklad možností nastavení **Přidat produkt do košíku** v nástroji pro tvorbu webů.

![Příklad možností nastavení Přidat produkt do košíku v nástroji pro tvorbu webů](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - Nastavení webu **Přidat produkt do nákupního košíku** jsou k dispozici od verze Dynamics 365 Commerce 10.0.11. Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json. Informace o aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Možnost nastavení **Zobrazit minikošík** je k dispozici od verze Dynamics 365 Commerce 10.0.20. Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json. Informace o aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Následující ilustrace ukazuje příklad potvrzovacího oznámení „přidáno do košíku“ na webu Fabrikam.

![Příklad potvrzovacího oznámení „přidáno do košíku“ na webu Fabrikam](./media/ecommerce-addtocart-notifications.PNG)

Následující ilustrace ukazuje příklad potvrzovacího oznámení „přidáno do košíku“ na webu Adventure Works.

![Příklad potvrzovacího oznámení „přidáno do košíku“ na webu Adventure Works](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Modul volby obchodu](store-selector.md)
