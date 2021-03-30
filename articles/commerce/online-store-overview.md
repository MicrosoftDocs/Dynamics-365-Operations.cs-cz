---
title: Přehled webu elektronického obchodu
description: Toto téma poskytuje přehled podpory pro weby elektronického obchodování v Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53bce671d6aca35335a3b3ef557a94fa60da1edc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251180"
---
# <a name="e-commerce-site-overview"></a>Přehled webu elektronického obchodu

[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled podpory pro weby elektronického obchodování v Microsoft Dynamics 365 Commerce. Obsahuje informace, jak jsou inicializovány a spravovány online obchody elektronického obchodování v Dynamics 365 Commerce. Obsahuje také odkazy na další informace o online obchodech a informace, jak zřídit a nakonfigurovat web elektronického obchodu. Ačkoli toto téma pokrývá mnoho základních informací, nepokrývá vše, co je nutné k vytvoření produkčního webu elektronického obchodování. Pokročilejší témata najdete v dokumentaci k Dynamics 365 Commerce.

## <a name="online-store-channel"></a>Kanál online obchodu

Než bude možné vytvořit web v aplikaci Dynamics 365 Commerce musí být vytvořen alespoň jeden kanál online obchodu. Další informace viz [Nastavení online kanálu](channel-setup-online.md). 

V aplikaci Dynamics 365 Commerce můžete pomocí kanálu online obchodu vytvořit produkty, ceny, jazyky, způsoby plateb, způsoby dodání, centra plnění a další aspekty online prostředí, které by měly být k dispozici vašim zákazníkům.

Než budete moci začít s Dynamics 365 Commerce, je třeba nastavit jeden kanál online obchodu. Jediný web elektronického obchodování však může poskytnout online prostředí pro více online obchodů. Pokud je například pro podporu různých zeměpisných oblastí nastaveno více online obchodů, lze použít jednu sadu stránek elektronického obchodu k poskytnutí jedinečných prostředí, které jsou definovány jednotlivými obchody. Další informace o konfiguraci webu pro podporu více online obchodů naleznete v tématu [Pidružení online webu ke kanálu](associate-site-online-store.md).

Jakmile je online obchod nastaven, může být přidružen k webu Dynamics 365 Commerce, který bude sloužit jako online výkladní skříň. Další informace o online obchodech a jejich nastavení naleznete v tématu [Vyváření online obchodů](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Nasazení nového klienta elektronického obchodu

Během inicializace webu elektronického obchodu se zobrazí výzva k zadání názvu domény. Další informace o doménách v Commerce najdete v části [Konfigurace názvu domény](configure-your-domain-name.md) a [Domény v Dynamics 365 Commerce](domains-commerce.md). Nasazení nového klienta elektronického obchodování pomocí [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), postupujte podle pokynů v části [Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md). Poté, co je váš klient elektronického obchodu nastaven v LCS, je vytvořen odkaz na konfigurátor webů Commerce. Potom můžete použít konfigurátor webů Commerce k inicializaci a konfiguraci webů elektronického obchodu.

## <a name="initialize-your-e-commerce-site"></a>Inicializace webu elektronického obchodu

Když spustíte konfigurátor webů Commerce z LCS, zobrazí se stránka **Weby** (Sites). Tato stránka obsahuje dva předem konfigurované weby, **výchozí** (default) a **fabrikam**, jak je znázorněno v příkladu na následujícím obrázku.

![Stránka Weby v konfigurátoru webů Commerce](media/e-commerce-site-01.png)

Když vyberete jeden z těchto webů, budete vyzváni k výběru názvu domény, výchozího kanálu online obchodu, podporovaného jazyka pro vybraný kanál a cesty. Pokud je použit pouze jeden kanál, můžete cestu nechat prázdnou. Více kanálů nebo jazyků online obchodu lze nakonfigurovat později v konfigurátoru webů Commerce. Každý další kanál nebo jazyk bude vyžadovat jedinečnou cestu. Například máte dva online kanály, které jsou přidruženy k jednomu webu, a název domény pro tento web je `www.fabrikam.com`. V tomto případě může být cesta pro jeden kanál výchozí hodnota, která neobsahuje žádnou cestu (`https://www.fabrikam.com`) a druhý kanál lze nastavit na novou cestu, například **web2**, který bude mít adresu URL `https://www.fabrikam.com/site2`. Následující obrázek ukazuje příklad dialogového okna inicializace webu v konfigurátoru webů Commerce.

![Dialogové okno inicializace konfigurátoru webů Commerce](media/e-commerce-site-02.png)

Stránka **Weby** také obsahuje tlačítko **Nový web**. Dialogové okno, které se zobrazí, když vyberete toto tlačítko, se podobá dialogovému oknu inicializace webu, ale slouží k vytvoření nového webu. Nové weby jsou prázdné. Nezahrnují stejné výchozí šablony, fragmenty, stránky a obrázky, které obsahují **výchozí** a **fabrikam** weby. Dle potřeby však můžete otevřít lístek podpory a požádat o přidání kopie výchozího obsahu na nový prázdný web. Další informace najdete v části [Vytvoření webu elektronického obchodu](create-ecommerce-site.md).

Po inicializaci nového webu se zobrazí **domovská** stránka konfigurátoru webů Commerce. Tato stránka obsahuje odkazy na běžné akce a průvodce, jak je znázorněno v příkladu na následujícím obrázku.

![Odkazy na domovské stránce v konfigurátoru webů Commerce](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Změna kanálů online obchodu nebo přidání kanálů online obchodu na web elektronického obchodu

Po vytvoření webu elektronického obchodu můžete změnit kanál, ke kterému je přidružen, podle pokynů v části [Přidružení webu elektronického obchodu k online kanálu](associate-site-online-store.md). Příklad na následujícím obrázku ukazuje, jak lze na stránce **Kanály** změnit číslo provozní jednotky kanálu (OUN) (**Nastavení webu \> Kanály**). Po provedení změny nezapomeňte vybrat **Uložit a publikovat**. Tímto způsobem zajistíte publikování změny.

![Stránka Kanály v konfigurátoru webů Commerce](media/e-commerce-site-04.png)

Nové kanály můžete přidat volbou **Přidat kanál**. Chcete-li do kanálu přidat nové jazyky, vyberte daný kanál a poté vyberte **Přidat národní prostředí** v zobrazeném dialogovém okně kanálu. Než se v dialogovém okně mohou objevit národní prostředí, musí být předem nakonfigurována pro kanál online obchodu v centrále Commerce.

![Dialogové okno Kanál konfigurátoru webů Commerce](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Vytvoření klienta Azure B2C

Dynamics 365 Commerce používá Azure Active Directory (Azure AD) B2C pro podporu toků přihlašovacích údajů a ověřování uživatele. Informace, jak vytvořit klienta Azure B2C, najdete v tématu [Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md), [Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md) a [Konfigurace více klientů B2C v prostředí Commerce](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Přehled výchozích webových stránek

**Výchozí** a **fabrikam** weby obsahují předkonfigurované šablony, fragmenty a stránky, které vám pomohou začít. Další informace naleznete v následujících tématech:

- [Přehled domovské stránky](quick-tour-home-page.md)
- [Přehled stránky s podrobnostmi o produktu](quick-tour-pdp.md)
- [Přehled stránek košíku a pokladny](quick-tour-cart-checkout.md)
- [Přehled stránek správy účtů](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Správa nastavení webu

Další informace o správě nastavení vašeho webu naleznete v následujících tématech:

- [Správa uživatelů a rolí elektronického obchodu](manage-ecommerce-users-roles.md)
- [Zvažování optimalizace webového vyhledávače (SEO) pro váš web](/search-engine-optimization-considerations.md)
- [Správa zásad zabezpečení obsahu (CSP)](manage-csp.md)
- [Volba motivu webu](select-site-theme.md)

## <a name="manage-site-content"></a>Správa obsahu webu

Další informace o správě obsahu webu naleznete v následujících tématech:

- [Glosář modelu stránky](page-elements-overview.md)
- [Stavy dokumentu a životního cyklu](document-states-overview.md)
- [Šablony a rozložení](templates-layouts-overview.md)
- [Práce s fragmenty](work-with-fragments.md)
- [Práce s moduly](work-with-modules.md)
- [Přehled správy digitálních aktiv](dam-overview.md)
- [Přehled knihovny modulů](starter-kit-overview.md)

## <a name="additional-resources"></a>Další prostředky

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Nasazení nového webu elektronického obchodu](deploy-ecommerce-site.md)

[Přiřazení online webu ke kanálu](associate-site-online-store.md)

[Konfigurace názvu domény](configure-your-domain-name.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]