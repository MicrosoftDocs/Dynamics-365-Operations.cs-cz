---
title: Přehled prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Toto téma poskytuje přehled o prostředí vyhodnocení Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3a16b771dc352ac30957f108da1f8e3727136207
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338320"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Přehled prostředí vyhodnocení aplikace Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled o prostředí vyhodnocení Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Prostředí vyhodnocení Commerce nejsou obecně dostupná a jsou poskytována partnerům a zákazníkům na základě žádosti. Podrobnější informace získáte od kontaktu společnosti Microsoft.

Prostředí vyhodnocení Commerce je volitelné komplexní prostředí Dynamics 365 Commerce, které partnerům a potenciálním zákazníkům umožňuje vyzkoušet produkt Commerce.

Vyhodnocovací prostředí jsou částečně předkonfigurována, aby se snížily požadované kroky po poskytnutí.

Kromě menších omezení, která neovlivňují funkce nebo funkčnost, poskytuje prostředí vyhodnocení Commerce kompletní zkušenost s tímto produktem a mohou je používat zákazníci a partneři k implementaci pro vyhodnocení produktu, poskytnutí zpětné vazby a analýze přizpůsobení nebo nedostatků.

## <a name="limitations-of-the-commerce-evaluation-environment"></a>Omezení prostředí vyhodnocení Commerce

I když prostředí vyhodnocení Commerce nabízí úplnou sadu funkcí a funkčnosti Commerce, existuje několik menších omezení:

- Přestože prostředí vyhodnocení Commerce nemá žádná zeměpisná omezení, součásti prostředí, jako například aplikace Retail Cloud Scale Unit (rcsu) a e-commerce, by se měly zřizovat pouze ve Spojených státech.
- Použití prostředí vyhodnocení Commerce je omezeno na 30 dní od data, kdy je zřízeno prostředí e-Commerce.
- Prostředí vyhodnocení Commerce je možné úspěšně nasadit a inicializovat pouze v prostředí, ve kterém je použita ukázková topologie, kde jsou všechny součásti prostředí nasazeny na jednom virtuálním počítači (VM) hostovaném v cloudu. Hlavní omezení této topologie je počet uživatelů, které může prostředí současně podporovat.

## <a name="get-started"></a>Začínáme

Chcete-li zřizovat prostředí vyhodnocení Commerce, získáte informace v části [Zřízení prostředí vyhodnocení Commerce](provisioning-guide.md).

## <a name="additional-resources"></a>Další prostředky

[Zřízení prostředí vyhodnocení Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace prostředí vyhodnocení Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce](cpe-optional-features.md)

[Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
