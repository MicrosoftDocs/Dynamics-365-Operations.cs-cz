---
title: Nastavení klienta B2C v Commerce
description: Tento článek popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785120"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Nastavení klienta B2C v Commerce

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Dynamics 365 Commerce.

Dynamics 365 Commerce používá Azure AD B2C pro podporu toků přihlašovacích údajů a ověřování uživatele. Uživatel se může registrovat, přihlásit a obnovit své heslo pomocí těchto toků. Azure AD B2C ukládá citlivé informace o ověřování uživatele, například jeho uživatelské jméno a heslo. Záznam uživatele v klientovi B2C uloží buď záznam místního účtu B2C nebo záznam zprostředkovatele sociální identity B2C. Tyto záznamy B2C budou odkazovat zpět na záznam odběratele v prostředí Commerce.

> [!WARNING] 
> Azure AD B2C vyřadí staré (starší) toky uživatelů od 1. srpna 2021. Proto byste měli naplánovat migraci toků uživatelů do nové doporučené verze. Nová verze poskytuje paritu funkcí a nové funkce. Knihovna modulů pro Commerce verze 10.0.15 nebo vyšší by měla být použita s doporučenými toky uživatelů B2C. Další informace naleznete v tématu [Toky uživatelů v Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Prostředí vyhodnocení Commerce přicházejí s předinstalovaným klientem Azure AD B2C pro demonstrační účely. Načtení vlastního klienta Azure AD B2C pomocí níže uvedených kroků není potřeba pro prostředí vyhodnocení.

> [!TIP]
> Můžete dále chránit uživatele svých stránek a zvýšit bezpečnost svých klientů Azure AD B2C pomocí Ochrany identity a podmíněný přístup k Azure AD. Chcete-li zkontrolovat možnosti, které mají k dispozici klienti Azure AD B2C Premium P1 a Premium P2, viz [Ochrana identity a podmíněný přístup k Azure AD B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Předpoklady prostředí Dynamics

Než začnete, ujistěte se, že vaše prostředí Dynamics 365 Commerce a kanál elektronického obchodování jsou odpovídajícím způsobem konfigurovány splněním následujících předpokladů.

- Nastavte hodnotu operací POS **AllowAnonymousAccess** na "1" v centrále Commerce:
    1. Jděte na **Operace POS**.
    1. Klikněte pravým tlačítkem myši na mřížku a vyberte **Přizpůsobit**.
    1. Vyberte **Přidat pole**.
    1. V seznamu dostupných sloupců vyberte sloupec **AllowAnonymousAccess** pro přidání.
    1. Vyberte **Aktualizovat**.
    1. Pro operaci **612** „Přidání zákazníka“ změňte **AllowAnonymousAccess** na „1.“
    1. Spusťte úlohu **1090 (Registry)**.
- Nastavte atribut **Ruční** zákaznického účtu číselné sekvence na **Ne** v centrále Commerce:
    1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry závazků**.
    1. Vyberte **číselné sekvence**.
    1. Na řádku **Zákaznický účet** dvakrát klikněte na hodnotu **Kód číselné sekvence**.
    1. Na záložce s náhledem **Obecné** číselné sekvence nastavte **Ruční** na **Ne**.

Po nasazení vašeho prostředí Dynamics 365 Commerce se také doporučuje [inicializovat zdrojová data](enable-configure-retail-functionality.md) v prostředí.

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu nastavení B2C tenanta v Commerce, pokračujte na [Vytvoření nebo propojení existujícího tenanta Azure AD B2C v Azure Portal](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Další prostředky

[Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure](create-link-aad-b2c-tenant.md)

[Vytvoření aplikace B2C](create-b2c-app.md)

[Vytvoření zásad toku uživatele](create-user-flow-policies.md)

[Přidání zprostředkovatelů sociální identity (volitelné)](add-social-identity-providers.md)

[Aktualizace Commerce Headquarters o nové informace Azure AD B2C](update-hq-aad-b2c-info.md)

[Konfigurace klienta B2C v konfigurátoru webů Commerce](config-b2c-tenant-site-builder.md)

[Doplňkové informace o B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
