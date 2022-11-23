---
title: Doplňkové informace o B2C
description: Tento článek poskytuje další informace o tom, jak nastavit nájemce typu business-to-consumer (B2C) v Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785220"
---
# <a name="additional-b2c-information"></a>Doplňkové informace o B2C

[!include [banner](includes/banner.md)]

Tento článek poskytuje další informace o tom, jak nastavit nájemce typu business-to-consumer (B2C) v Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Migrace zákazníků

Pokud uvažujete o migraci záznamů zákazníků z předchozí platformy zprotředkovatele identity, spolupracujte s týmem Dynamics 365 Commerce, abyste zkontrolovali potřeby zákazníka ohledně migrace.

Další dokumentaci Azure AD B2C ohledně migrace zákazníků najdete v tématu [Migrace uživatelů do Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Vlastní zásady

Další informace o přizpůsobení interakcí a toků zásad Azure AD B2C nad rámec toho, co je nabídnuto standardními zásadami B2C, naleznete v tématu [Vlastní zásady v Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundární správce

Nepovinný sekundární účet správce lze přidat do oddílu **Uživatelé** v klientovi B2C. Může se jednat o přímý nebo obecný účet. Potřebujete-li sdílet účet v prostředcích týmu, je možné také vytvořit běžný účet. Vzhledem k citlivosti dat uložených v Azure AD B2C je třeba společný účet pečlivě monitorovat dle bezpečnostních postupů společnosti.

### <a name="set-up-a-custom-sign-in-domain"></a>Nastavte si vlastní přihlašovací doménu

Azure AD B2C vám umožňuje nastavit vlastní přihlašovací doménu pro klienta Azure AD B2C. Pokyny viz [Povolit vlastní domény pro Azure Active Directory B2C](/azure/active-directory-b2c/custom-domain). 

Pokud používáte vlastní přihlašovací doménu, doména musí být zadána do nástroje Commerce Site Builder.

Chcete-li zadat vlastní doménu přihlašování v nástroji pro tvorbu webu, postupujte následovně.

1. Vyberte Přepínač webů v pravém horním rohu nástroje pro tvorbu webu a poté vyberte **Spravovat weby**.
1. V levém navigačním podokně vyberte **Nastavení klienta \> Nastavení ověřování webu**.
1. V sekci **Ověřovací profily webu** vyberte **Spravovat**.
1. V plovoucím panelu vpravo vyberte tlačítko **Upravit** (symbol tužky) vedle profilu ověřování webu, pro který chcete zadat vlastní doménu.
1. V dialogovém okně **Upravit profil ověřování webu** v **Přihlaste se do vlastní domény** zadejte svou vlastní přihlašovací doménu (například 'login.fabrikam.com').

> [!WARNING]
> Při aktualizaci na vlastní doménu pro klienta Azure AD B2C změna ovlivní podrobnosti o vydavateli vygenerovaného tokenu klienta. Podrobnosti o vydavateli pak budou zahrnovat vlastní doménu namísto výchozí domény, kterou poskytuje Azure AD B2C. Rozdílná konfiguace **Vydavatel** v Commerce headquarters (**Maloobchod a obchod \> Nastavení ústředí \> Parametry \> Sdílené parametry obchodu \> Poskytovatelé identity**) změní interakci systému s uživateli webu a případně vytvoří nový záznam zákazníka, pokud se uživatel ověřuje proti novému vydavateli. Jakékoli změny vlastní domény by měly být důkladně otestovány před přechodem na vlastní doménu v živém prostředí Azure AD B2C.

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure](create-link-aad-b2c-tenant.md)

[Vytvoření aplikace B2C](create-b2c-app.md)

[Vytvoření zásad toku uživatele](create-user-flow-policies.md)

[Přidání zprostředkovatelů sociální identity (volitelné)](add-social-identity-providers.md)

[Aktualizace Commerce Headquarters o nové informace Azure AD B2C](update-hq-aad-b2c-info.md)

[Konfigurace klienta B2C v konfigurátoru webů Commerce](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
