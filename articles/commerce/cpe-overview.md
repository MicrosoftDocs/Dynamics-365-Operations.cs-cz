---
title: Přehled prostředí Preview aplikace Dynamics 365 Commerce
description: Toto téma poskytuje přehled o prostředí náhledu v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024676"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a>Přehled prostředí Preview aplikace Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled o prostředí náhledu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Prostředí náhledu produktu Commerce je volitelné komplexní prostředí pro zobrazení náhledu produktu Dynamics 365 Commerce, které potenciálním zákazníkům umožňuje vyzkoušet produkt Commerce před jeho veřejným vydáním.

Kromě menších omezení, která neovlivňují funkce nebo funkčnost, poskytuje prostředí náhledu produktu Commerce kompletní zkušenost s tímto produktem a mohou je používat zákazníci a partneři k implementaci pro vyhodnocení produktu, poskytnutí zpětné vazby a analýze přizpůsobení nebo nedostatků.

## <a name="limitations-of-the-commerce-preview-environment"></a>Omezení prostředí náhledu Commerce

I když prostředí náhledu Commerce nabízí úplnou sadu funkcí a funkčnosti Commerce, existuje několik menších omezení:

- Přestože prostředí náhledu Commerce nemá žádná zeměpisná omezení, součásti prostředí, jako například aplikace Retail Cloud Scale Unit (rcsu) a e-commerce, lze zřizovat pouze ve Spojených státech.
- Použití prostředí náhledu Commerce je omezeno na 30 dní od data, kdy je zřízeno prostředí e-Commerce.
- Prostředí náhledu Commerce je možné úspěšně nasadit a inicializovat pouze v prostředí, ve kterém je použita ukázková topologie, kde jsou všechny součásti prostředí nasazeny na jednom virtuálním počítači (VM). Hlavní omezení této topologie OneBox VM je počet uživatelů, které může prostředí náhledu současně podporovat.
- Prostředí náhledu Commerce je možné posoudit pouze do doby, kdy bude produkt Commerce dostupný široké veřejnosti. Nová ukázková prostředí budou k dispozici po vydání pro širokou veřejnost.

## <a name="get-started"></a>Začínáme

Chcete-li zřizovat prostředí pro náhled Commerce, získáte informace v části [Zřízení prostředí náhledu Commerce](provisioning-guide.md).

## <a name="additional-resources"></a>Další zdroje

[Zřízení prostředí Preview aplikace Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace prostředí Preview aplikace Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurace volitelných funkcí pro prostředí Preview aplikace Dynamics 365 Commerce](cpe-optional-features.md)

[Často kladené dotazy k prostředí Preview aplikace Dynamics 365 Commerce](cpe-faq.md)
