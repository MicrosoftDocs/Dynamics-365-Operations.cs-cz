---
title: Vytvoření aplikace B2C
description: Tento článek popisuje, jak vytvořit aplikaci business-to-consumer (B2C) v portálu Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785226"
---
# <a name="create-a-b2c-application"></a>Vytvoření aplikace B2C

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit aplikaci business-to-consumer (B2C) v portálu Microsoft Azure.

Po vytvoření tenanta B2C vytvoříte aplikaci B2C s novým tenantem Azure Active Directory (Azure AD) pro interakci s Commerce.

Chcete-li vytvořit aplikaci B2C, postupujte následovně.

1. V portálu Azure vyberte **Registrace aplikací** a poté vyberte možnost **Nová registrace**.
1. V poli **Název** zadejte název aplikace Azure AD B2C.
1. V sekci **Podporované typy účtů** vyberte **Účty u libovolného zprostředkovatele identity nebo organizačního adresáře (pro ověřování uživatelů pomocí toků uživatelů)**.
1. Jako **Identifikátor URI přesměrování** zadejte své vyhrazené adresy URL odpovědí jako typ **Web**. Viz [Adresy URL pro odpovědi](#reply-urls) níže, kde najdete informace o adresách URL odpovědí a jak je naformátovat. Chcete-li povolit přesměrování, je nutné zadat URI pro přesměrování / adresu URL odpovědi z Azure AD B2C zpět na váš web, když se uživatel autentizuje. Adresu URL odpovědi lze přidat během procesu registrace nebo ji lze přidat později výběrem odkazu **Přidat URI přesměrování** z nabídky **Přehled** v části **Přehled** aplikace B2C.
1. Pro **Oprávnění** vyberte **Udělit souhlas správce oprávněním openid a offline_access**.
1. Vyberte **Registrovat**.
1. Vyberte nově vytvořenou aplikaci a přejděte do nabídky **Ověřování**. 
1. Pokud je zadána adresa URL odpovědi, v části **Toky implicitního udělení oprávnění a hybridní toky** vyberte možnost **Přístupové tokeny** i **Tokeny ID** pro jejich povolení pro aplikaci a poté vyberte **Uložit**. Pokud nebyla při registraci zadána adresa URL odpovědi, lze ji také přidat na tuto stránku výběrem **Přidat platformu**, výběrem **Web** a poté zadáním URI přesměrování aplikace. Část **Toky implicitního udělení oprávnění a hybridní toky** pak bude k dispozici pro výběr možnosti **Přístupové tokeny** i **Tokeny ID**.
1. Přejděte do nabídky **Přehled** portálu Azure Portal a zkopírujte **ID aplikace (klienta)**. Poznamenejte si toto ID pro pozdější kroky instalace (později zmiňováno jako **GUID klienta**).

Další informace o registraci aplikací v Azure AD B2C viz [Nové prostředí registrace aplikací pro Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Adresy URL pro odpovědi

Adresy URL pro odpovědi jsou důležité, protože poskytují seznam povolených návratových domén, když váš web volá Azure AD B2C pro ověření uživatele. To umožňuje vrátit ověřeného uživatele zpět do domény, ze které se přihlásí (doména vašeho webu). 

V poli **Adresa URL odpovědi** na obrazovce **Azure AD B2C – aplikace \> Nová aplikace** je nutné přidat samostatné řádky pro doménu vašeho webu a (po zřízení vašeho prostředí) adresu URL generovanou řešením Commerce. Tyto adresy URL musí vždy používat platný formát adresy URL a musí to být pouze základní adresy URL (bez koncového lomítka nebo cesty). Řetězec ``/_msdyn365/authresp`` pak musí být přidán k základní adrese URL, jako v následujících příkladech.

- ``https://www.fabrikam.com/_msdyn365/authresp``(Doména by se měla zcela shodovat s doménou elektronického obchodu. Pokud máte více domén, musíte přidat tuto adresu URL pro každou doménu.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu nastavení B2C tenanta v Commerce, pokračujte na [Vytvoření zásad toku uživatele](create-user-flow-policies.md).

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure](create-link-aad-b2c-tenant.md)

[Vytvoření zásad toku uživatele](create-user-flow-policies.md)

[Přidání zprostředkovatelů sociální identity (volitelné)](add-social-identity-providers.md)

[Aktualizace Commerce Headquarters o nové informace Azure AD B2C](update-hq-aad-b2c-info.md)

[Konfigurace klienta B2C v konfigurátoru webů Commerce](config-b2c-tenant-site-builder.md)

[Doplňkové informace o B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
