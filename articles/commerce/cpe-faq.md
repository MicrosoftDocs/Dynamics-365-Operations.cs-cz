---
title: Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce
description: V tomto tématu jsou odpovědi na časté otázky týkající se prostředí vyhodnocení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b8d7d7364087dacf3b4479ab008609ecffeaacb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000968"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

V tomto tématu jsou odpovědi na časté otázky týkající se prostředí vyhodnocení Microsoft Dynamics 365 Commerce.

**Můžeme použít prostředí vyhodnocení Commerce jako úložiště elektronického obchodu pro zákazníky, kteří aktuálně implementují program Retail?**

Č. Prostředí vyhodnocení obchodu je pouze pro hodnocení. Pokud požadujete prostředí pro zákazníka, který implementuje program Retail, kontaktujte společnost Microsoft.

**Je možné použít prostředí vyhodnocení Commerce ke zřizování funkcí elektronického obchodování nad rámec existující aplikace nebo prostředí, které implementuje program Retail?**

Ne (většinou). Komponenty vyhodnocení obchodu jsou k dispozici pouze v prostředích, která odpovídají konfiguracím specifikovaným v příručce pro předpoklady a zajišťování. Požadovaná základní ukázková data navíc nebudou dostupná v prostředích, která byla nasazena s počátečním vydáním starším než 10.0.8. 

**Jaké náklady jsou zahrnuty v nasazení prostředí vyhodnocení Commerce v Microsoft Azure prostřednictvím Microsoft Dynamics Lifecycle Services (LCS)?**

Tradiční demo prostředí ústředí Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce (virtuální stroj \[VM \]) bude hostována ve vašem předplatném služby Azure. K odhadu těchto nákladů [můžete použít kalkulačku cen Azure](https://azure.microsoft.com/pricing/calculator/).

Ostatní komponenty, jako je Commerce Scale Unit, Tvůrce webu Commerce a váš web elektronického obchodu, budou k dispozici jako software jako služba (SaaS) a budou hostovány společností Microsoft.

**Které oblasti Azure jsou aktuálně podporovány v prostředí vyhodnocení Commerce?**

Prostředí vyhodnocení Commerce je možné nasadit pouze v severoamerické zeměpisné oblasti.

**Existuje virtuální pevný disk (VHD) s možností stažení, který má kompletní možnost virtuálního počítače OneBox (VM)?**

Dynamics 365 Commerce a Commerce Scale Unit jsou kompletní software jako služba (SaaS) a musí být hostovány v cloudu.

**Jak dlouho je možné používat prostředí vyhodnocení Commerce?**

Prostředí vyhodnocení Commerce má lhůtu 30 dnů ode dne, kdy jsou poskytovány komponenty SaaS, jako je Commerce Scale Unit, Tvůrce webu Commerce a váš web e-Commerce.

**Lze prodloužit časový limit pro prostředí vyhodnocení Commerce?**

Prodloužení lhůty je výjimkou z normy a posuzuje se případ od případu. Měli byste se obrátit na svého partnera společnosti Microsoft s žádostí o pomoc.

## <a name="additional-resources"></a>Další prostředky

[Přehled prostředí vyhodnocení Dynamics 365 Commerce](cpe-overview.md)

[Zřízení prostředí vyhodnocení Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace prostředí vyhodnocení Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce](cpe-optional-features.md)
