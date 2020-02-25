---
title: Často kladené dotazy k prostředí Preview aplikace Dynamics 365 Commerce
description: V tomto tématu jsou odpovědi na časté otázky týkající se prostředí náhledu Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 061a160380e500ea52afbc35f0a95fe84d971bcf
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024745"
---
# <a name="dynamics-365-commerce-preview-environment-faq"></a>Často kladené dotazy k prostředí Preview aplikace Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

V tomto tématu jsou odpovědi na časté otázky týkající se prostředí náhledu Microsoft Dynamics 365 Commerce.

**Mohu přenést pozvánku pro prostředí náhledu Commerce do jiného klienta?**

Ano. Pro přenosy pozvánek můžete použít [formulář převodu náhledu produktu Commerce](https://aka.ms/Dynamics365CommercePreviewTransferForm).

**Jak dlouho trvá přenos pozvánky?**

Přenos v průměru trvá přibližně tři až pět pracovních dnů. Mohou však platit výjimky.

**Pracuje prostředí náhledu Commerce s projekty Dynamics 365 Finance nebo Dynamics 365 Supply Chain?**

Č. Prostředí náhledu Commerce je pracuje pouze s projekty Dynamics 365 Retail.

**Můžeme použít prostředí náhledu Commerce jako úložiště elektronického obchodu pro zákazníky, kteří aktuálně implementují program Retail?**

Č. Prostředí náhledu Commerce je pouze prostředí pro hodnocení. Pokud požadujete prostředí pro zákazníka, který implementuje program Retail, kontaktujte společnost Microsoft.

**Je možné použít prostředí náhledu Commerce ke zřizování funkcí elektronického obchodování nad rámec existující aplikace nebo prostředí, které implementuje program Retail?**

Č. Prostředí náhledu Commerce je momentálně k dispozici pouze v nových prostředích, která byla nasazena v projektech maloobchodních skladových jednotek (SKU), které mají ukázková data z verze 10.0.6.

**Jaké náklady jsou zahrnuty v nasazení náhledu prostředí Commerce v Microsoft Azure prostřednictvím Microsoft Dynamics Lifecycle Services (LCS)?**

Jedinou komponentou, která je hostována ve vašem předplatném, je maloobchod. Další komponenty jako Retail Cloud Scale Unit (RCSU) a e-Commerce budou hostovány v předplatných společnosti Microsoft. K odhadu těchto nákladů [můžete použít kalkulačku cen Azure](https://azure.microsoft.com/pricing/calculator/).

**Které oblasti Azure jsou aktuálně podporovány v prostředí náhledu Commerce?**

Prostředí náhledu Commerce je možné nasadit pouze v severoamerické zeměpisné oblasti.

**Existuje virtuální pevný disk (VHD) s možností stažení, který má kompletní možnost virtuálního počítače OneBox (VM)?**

Dynamics 365 Retail Cloud Scale Unit (rcsu) a e-Commerce jsou kompletní software jako služba (SaaS) a musí být hostovány v cloudu.

**Jak dlouho je možné používat prostředí náhledu Commerce?**

Použití prostředí náhledu Commerce je omezeno na 30 dní od data zřízení prostředí e-Commerce.

**Lze prodloužit časový limit pro prostředí náhledu Commerce?**

Ano. Můžete se obrátit na tým podpory pomocí [formuláře rozšíření pro náhled Commerce](https://aka.ms/Dynamics365CommercePreviewExtensionForm).

**Lze vytvořit více požadavků pro prostředí náhledu Commerce?**

Pro každý přijatý požadavek přidělíme kvótu jednoho prostředí pro náhled Commerce. Potřebujete-li více než jedno prostředí náhledu, obraťte se na společnost Microsoft. Kontaktní informace naleznete v následující části.

## <a name="dynamics-365-commerce-preview-environment-contact-information"></a>Kontaktní údaje pro náhled prostředí Dynamics 365 Commerce

Chcete-li kontaktovat Microsoft s otázkami nebo požadavky v souvislosti s prostředím náhledu Commerce, navštivte [skupinu Microsoft Dynamics 365 Commerce Preview ve službě Yammer](https://aka.ms/Dynamics365CommercePreviewYammer) a požádejte o pomoc.

Pokud se při pokusu o přístup ke skupině Yammer vyskytnou problémy, můžete kontaktovat společnost Microsoft e-mailem na adrese <Dynamics365Commerce@microsoft.com>. Tato e-mailová adresa není aktivně monitorována. Proto očekávejte prodlevu v odpovědi.

## <a name="additional-resources"></a>Další zdroje

[Přehled prostředí Preview aplikace Dynamics 365 Commerce](cpe-overview.md)

[Zřízení prostředí Preview aplikace Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace prostředí Preview aplikace Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurace volitelných funkcí pro prostředí Preview aplikace Dynamics 365 Commerce](cpe-optional-features.md)
