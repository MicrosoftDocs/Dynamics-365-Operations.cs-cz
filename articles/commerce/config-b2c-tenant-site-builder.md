---
title: Konfigurace klienta B2C v konfigurátoru webů Commerce
description: Tento článek popisuje, jak nakonfigurovat tenanta business-to-consumer (B2C) v tvůrci webu Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785231"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurace klienta B2C v konfigurátoru webů Commerce

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nakonfigurovat tenanta business-to-consumer (B2C) v tvůrci webu Microsoft Dynamics 365 Commerce.

Po dokončení nastavení klienta Azure AD B2C musíte nakonfigurovat klienta B2C v konfigurátoru webů Commerce. Kroky konfigurace zahrnují získání informací o aplikaci B2C z portálu Azure, zadání informací o aplikaci B2C do konfigurátru webů a následné přidružení aplikace B2C k vašemu webu a kanálu.

### <a name="collect-the-required-application-information"></a>Získání požadovaných informací o aplikaci

Chcete-li získat požadované informace o aplikaci, postupujte podle následujících kroků.

1. V portálu Azure přejděte na **Domovská stránka \> Azure AD B2C – Registrace aplikací**.
1. Pro získání podrobností o aplikaci vyberte svou aplikaci a v levém navigačním podokně vyberte **Přehled**.
1. Z reference **ID aplikace (klienta)** získejte ID aplikace B2C vytvořené ve vašem klientovi B2C. Později bude zadáno jako **GUID klienta** v konfigurátoru webů.
1. Vyberte **Identifikátory URI přesměrování** a shromážděte adresu URL odpovědi zobrazenou pro váš web (adresu URL odpovědi zadanou při nastavení).
1. Přejděte na **Domovská stránka \> Azure AD B2C – toky uživatelů (zásady)** a shromážděte celé názvy jednotlivých zásad toku uživatelů.

Na následujícím obrázku je znázorněn příklad stránky přehledu **Azure AD B2C – Registrace aplikací**.

![Azure AD B2C – Stránka s přehledem registrací aplikací se zvýrazněným ID aplikace (klienta)](./media/ClientGUID_Application_AzurePortal.png)

Následující obrázek znázorňuje příklad zásad toku uživatelů na stránce **Azure AD B2C – toky uživatelů (zásady)**.

![Získání názvů jednotlivých toků zásad B2C.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Zadání informací o aplikaci klienta Azure AD B2C do platformy Commerce

Před přidružením klienta B2C ke svým webům je nutné zadat podrobnosti o klientovi Azure AD B2C do konfigurátoru webů Commerce.

Chcete-li do platformy Commerce přidat informace o aplikaci klienta Azure AD B2C, postupujte podle následujících kroků.

1. Přihlaste se jako správce ke konfigurátoru webů Commerce pro vaše prostředí.
1. V levém navigačním podokně vyberte **Nastavení klienta**, čímž jej rozbalíte.
1. V **Nastavení klienta** vyberte **Nastavení ověřování webu**. 
1. V hlavním okně vedle **Ověřovací profily webu** vyberte **Spravovat**. (Pokud se klient zobrazí v seznamu profilů ověřování webu, pak již byl přidán správcem. Ověřte, že položky v kroku 6 odpovídají vašemu plánovanému nastavení B2C. Nový profil lze také vytvořit pomocí klientů nebo aplikací Azure AD B2C, aby se zohlednily drobné rozdíly, jako jsou různá ID uživatelských zásad).
1. Zvolit **Přidat profil ověřování webu**.
1. Ve zobrazeném formuláři zadejte následující požadované položky s použitím hodnot z klienta a aplikace B2C. Pole, která nejsou vyžadována (bez hvězdičky), mohou být ponechána prázdná.

    - **Název aplikace**: název aplikace B2C, například „Fabrikam B2C“.
    - **Název klienta**: Název klienta B2C (použijte například "fabrikam", pokud se doména pro klienta B2C zobrazuje jako "fabrikam.onmicrosoft.com"). 
    - **ID zásady zapomenutého hesla**: ID zásady toku uživatele pro zapomenuté heslo, například „B2C_1_ResetovaniHesla“.
    - **ID zásady registrace a přihlášení**: ID zásady toku uživatele pro registraci a přihlášení, například „B2C_1_registrace_prihlaseni“.
    - **GUID klienta**: ID aplikace B2C, například „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.
    - **ID zásady úpravy profilu**: ID zásady toku uživatele pro úpravu profilu, například „B2C_1A_UpravaProfilu“.

1. Vyberte **OK**. Nyní by se měl zobrazit název vaší aplikace B2C v seznamu.
1. Klepnutím na tlačítko **Uložit** uložte změny.

Volitelné pole **Přihlaste se do vlastní domény** by mělo být použito pouze v případě, že nastavujete vlastní doménu pro klienta Azure AD B2C. Pro další podrobnosti a úvahy týkající se použití pole **Přihlaste se do vlastní domény** viz [Další informace o B2C](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Přidružení aplikace B2C k webu a kanálu

> [!WARNING]
> - Pokud je váš web již přidružen k aplikaci B2C, změna na jinou aplikaci B2C odstraní aktuální odkazy vytvořené pro uživatele, které jsou již zaregistrováni v tomto prostředí. V případě změny nebudou mít uživatelé k dispozici žádná pověření přidružená k aktuálně přiřazené aplikaci B2C. 
> - Aplikaci B2C aktualizujte pouze v případě, že aplikaci B2C kanálu zřizujete poprvé, nebo pokud čekáte, že se uživatelé znovu zaregistrují s novými pověřeními pro tento kanál pomocí nové aplikace B2C. Buďte opatrní při přiřazování kanálů k aplikacím B2C a pojmenovávejte aplikace srozumitelně. Není-li kanál přidružen k aplikaci B2C v níže uvedených krocích, uživatelé přihlašující se k tomuto kanálu pro váš web budou zadáni do aplikace B2C, která se zobrazí jako **výchozí** v seznamu aplikací B2C v umístění **Nastavení klienta \> Nastavení B2C**.

Chcete-li přidružit aplikaci B2C k webu a kanálu, postupujte takto.

1. Přejděte na svůj web konfigurátoru webů Commerce.
1. V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.
1. Pod položkou **Nastavení webu** vyberte možnost **Kanály**.
1. V hlavním okně v části **Kanály** vyberte svůj kanál.
1. V podokně vlastností kanálu vpravo vyberte název svojí aplikace B2C z rozevírací nabídky **Vybrat aplikaci B2C**.
1. Vyberte možnost **Zavřít** a pak vyberte možnost **Uložit a publikovat**.

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu nastavení B2C tenanta v Commerce, pokračujte na [Další informace B2C](additional-b2c-info.md).

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure](create-link-aad-b2c-tenant.md)

[Vytvoření aplikace B2C](create-b2c-app.md)

[Vytvoření zásad toku uživatele](create-user-flow-policies.md)

[Přidání zprostředkovatelů sociální identity (volitelné)](add-social-identity-providers.md)

[Aktualizace Commerce Headquarters o nové informace Azure AD B2C](update-hq-aad-b2c-info.md)

[Doplňkové informace o B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
