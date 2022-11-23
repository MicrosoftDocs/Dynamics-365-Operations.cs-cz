---
title: Aktualizace Commerce Headquarters o nové informace Azure AD B2C
description: Tento článek popisuje, jak aktualizovat Microsoft Dynamics 365 Commerce headquarters na nové údaje Azure Active Directory (Azure AD) business-to-consumer (B2C).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785234"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Aktualizace Commerce Headquarters o nové informace Azure AD B2C

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak aktualizovat Microsoft Dynamics 365 Commerce headquarters na nové údaje Azure Active Directory (Azure AD) business-to-consumer (B2C).

Po dokončení výše uvedených kroků pro zřízení Azure AD B2C musí být aplikace Azure AD B2C registrována ve vašem prostředí Dynamics 365 Commerce.

Chcete-li aktualizovat Headquarters o nové informace Azure AD B2C, postupujte takto.

1. V Commerce přejděte na **Sdílené parametry Commerce** a vyberte **Zprostředkovatelé identity** v levé nabídce.
1. V části **Zprostředkovatelé identity** postupujte takto:
    1. V poli **Vystavitel** zadejte řetězec vystavitele zprostředkovatele identity. Chcete-li najít řetězec vydavatele, postupujte dle části [Získání řetězce vydavatele pro nastavení centrály](#obtain-issuer-string-for-headquarters-setup) uvedené níže.
    1. Do pole **Název** zadejte název záznamu vystavitele.
    1. Do pole **Typ** zadejte **Azure AD B2C (id_token)**.
1. V části **Předávající strany** s výše vybranou položkou zprostředkovatele identity B2C postupujte takto:
    1. V poli **ClientID** zadejte své ID aplikace B2C, které najdete v poli **ID aplikace** na stránce vlastností vaší aplikace B2C.
    1. Do pole **Typ** zadejte **Veřejné**.
    1. Do pole **Typ uživatele** zadejte **Zákazník**.
1. V podokně akcí vyberte **Uložit**.
1. Ve vyhledávacím poli Commerce Search vyhledejte **Plán distribuce**.
1. V levé navigační nabídce stránky **Plán distribuce** vyberte úlohu **1110 Globální konfigurace**.
1. V podokně akcí zvolte **Spustit**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Získání řetězce vydavatele pro nastavení centrály

Chcete-li získat řetězec vystavitele svého zprostředkovatele identity, postupujte takto.

1. Na stránce Azure AD B2C na webu Azure Portal přejděte na tok uživatelů **Registrace a přihlášení**.
1. Vyberte **Rozložení stránky** v levé navigační nabídce, v sekci **Název rozložení** vyberte **Jednotná stránka pro registraci nebo přihlášení** a potom vyberte **Spustit tok uživatele**.
1. Ujistěte se, že je vaše aplikace nastavena podle zamýšlené aplikace Azure AD B2C vytvořené výše a poté v záhlaví **Spustit tok uživatele** vyberte odkaz na tok uživatele, který obsahuje řetězec ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Nevybírejte příkaz **Spustit uživatelský tok**.) Otevře se nová karta zobrazující metadata pro zásadu shromažďování řetězce vydavatele.
1. Na stránce metadat zobrazené na kartě prohlížeče zkopírujte řetězec vydavatele poskytovatele identity (hodnota **issuer** začínající na „https://“ a končící řetězcem „/v2.0/“), který vypadá podobně jako následující příklad.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**NEBO**: Chcete-li vytvořit stejnou adresu URL metadat ručně, proveďte následující kroky.

1. V následujícím formátu vytvořte adresu URL metadat s použitím vašeho klienta a zásady B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Příklad: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Do adresního řádku prohlížeče zadejte adresu URL metadat.
1. V metadatech zkopírujte adresu URL vystavitele zprostředkovatele identity (hodnota pro **„vystavitel“**).
    - Příklad: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu nastavení tenanta B2C v Commerce, pokračujte na [Konfigurace tenanta B2C v tvůrci webů Commerce](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure](create-link-aad-b2c-tenant.md)

[Vytvoření aplikace B2C](create-b2c-app.md)

[Vytvoření zásad toku uživatele](create-user-flow-policies.md)

[Přidání zprostředkovatelů sociální identity (volitelné)](add-social-identity-providers.md)

[Konfigurace klienta B2C v konfigurátoru webů Commerce](config-b2c-tenant-site-builder.md)

[Doplňkové informace o B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
