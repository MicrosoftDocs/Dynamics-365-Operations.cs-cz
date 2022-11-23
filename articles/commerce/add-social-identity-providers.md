---
title: Přidání poskytovatelů identity sociálních sítí
description: Tento článek popisuje, jak přidat poskytovatele identity sociálních sítí do portálu Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785223"
---
# <a name="add-social-identity-providers"></a>Přidání poskytovatelů identity sociálních sítí

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak přidat poskytovatele identity sociálních sítí do portálu Microsoft Azure.

Zprostředkovatelé sociální identity umožňují uživatelům používat účty sociálních sítí k ověřování. Přidání ověření zprostředkovatele sociální identity je volitelné v Dynamics 365 Commerce. 

Pokud není přidáno ověřování zprostředkovatele sociální identity, budou výchozí profily Azure Active Directory (Azure AD) B2C hlavními profily pro vaše uživatele. Uživatelé budou moci vybrat vlastní uživatelské jméno (jejich upřednostňovaná e-mailová adresa) a nastavit heslo. Azure AD B2C bude uživatele ověřovat přímo. 

Je-li přidáno ověřování zprostředkovatele sociální identity a uživatel si zvolí jednoho ze nabízených zprostředkovatelů sociální identity, bude v klientu Azure AD B2C vytvořena entita. Azure AD B2C poté ověří přihlašovací údaje uživatele pomocí zprostředkovatele sociální identity.

> [!NOTE]
> Přihlášení zprostředkovatele identity vytvoří záznam v klientovi B2C, ale v jiném formátu než místní účty, protože pro ověření bude volat externí odkaz na zprostředkovatele sociální identity. Uživatel může použít stejnou e-mailovou adresu v rámci zprostředkovatelů sociální identity, což znamená, že uživatelské jméno e-mailu použité pro ověření nemusí být jedinečné pro klienta. Azure AD B2C pouze vynutí, aby uživatelé měli jedinečnou e-mailovou adresu v místních účtech B2C.

Před přidáním zprostředkovatele sociální identity pro ověřování je nutné přejít na portál zprostředkovatele identity a nastavit aplikaci zprostředkovatele identity tak, jak je uvedeno v dokumentaci k Azure AD B2C. Níže je uveden seznam odkazů na dokumentaci.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (jeden klient)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Účet Microsoft](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Přidání a nastavení zprostředkovatele sociální identity

> [!NOTE]
> Přidání poskytovatelů identity ze sociálních sítí je volitelný krok při nastavování nájemce typu business-to-consumer (B2C) v Microsoft Dynamics 365 Commerce.

Chcete-li přidat a nastavit zprostředkovatele sociální identity, postupujte podle následujících kroků.  

1. V portálu Azure přejděte k **Zprostředkovatelé identity**.
1. Vyberte **přidat**. Zobrazí se obrazovka **Přidání zprostředkovatele identity**.
1. V části **Název** zadejte název, který se zobrazí uživatelům na vaší obrazovce pro přihlášení.
1. V části **Typ zprostředkovatele identity** vyberte zprostředkovatele identity ze seznamu.
1. Vyberte **OK**.
1. Volbou **Nastavit tohoto zprostředkovatele identity** přistoupíte na obrazovku **Nastavení zprostředkovatele sociální identity**.
1. V poli **ID klienta** zadejte ID klienta, které jste získali z nastavení aplikace zprostředkovatele identity.
1. V poli **Tajný klíč klienta** zadejte tajný klíč klienta, které jste získali z nastavení aplikace zprostředkovatele identity.
1. Připojte tok uživatele pro zásady přihlášení a registrace:
1. Přejděte na **Azure AD B2C – toky uživatelů (zásady) \> {vaše zásada pro přihlášení a registraci} \> Zprostředkovatelé identity**.
1. Chcete-li připojit zásadu toku uživatele pro přihlášení/registraci, vyberte každého zprostředkovatele identity, kterého jste pro svůj účet nastavili. Chcete-li toky otestovat, vyberte možnost **Spustit tok uživatele** pro každého zprostředkovatele identity. Na nové kartě se zobrazí stránka pro přihlášení s oblastí výběru nového zprostředkovatele identity.

Následující obrázek znázorňuje příklad obrazovek **Přidání zprostředkovatele identity** a **Nastavení zprostředkovatele** sociální identity v Azure AD B2C.

![Přidání poskytovatele sociální identity do aplikace.](./media/B2CImage_14.png)

Následující obrázek znázorňuje příklad, jak vybrat zprostředkovatele identity na stránce **Zprostředkovatelé identity** v Azure AD B2C.

![Výběr jednotlivých zprostředkovatelů sociální identity a povolení vaší zásady.](./media/B2CImage_16.png)

Následující obrázek znázorňuje příklad výchozí přihlašovací obrazovky se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity.

> [!NOTE]
> Pokud používáte vlastní stránky integrované v Commerce pro vaše toky uživatelů, bude nutné přidat tlačítka pro zprostředkovatele sociální identity pomocí funkcí rozšiřitelnosti knihovny modulů Commerce. Navíc při nastavování aplikací u konkrétního zprostředkovatele sociální identity mohou v některých případech řetězce adresy URL nebo konfigurace rozlišovat velká a malá písmena. Další informace najdete v pokynech pro připojení zprostředkovatele sociální identity.
 
![Příklad výchozí obrazovky pro přihlášení se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu nastavení tenanta B2C v Commerce, pokračujte na [Aktualizace Commerce headquarters na nové informace Azure AD B2C](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure](create-link-aad-b2c-tenant.md)

[Vytvoření aplikace B2C](create-b2c-app.md)

[Vytvoření zásad toku uživatele](create-user-flow-policies.md)

[Aktualizace Commerce Headquarters o nové informace Azure AD B2C](update-hq-aad-b2c-info.md)

[Konfigurace klienta B2C v konfigurátoru webů Commerce](config-b2c-tenant-site-builder.md)

[Doplňkové informace o B2C](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
