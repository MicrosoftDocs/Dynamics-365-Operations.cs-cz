---
title: Vytvoření zásad toku uživatele
description: Tento článek popisuje, jak vytvořit zásady toku uživatelů v portálu Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785230"
---
# <a name="create-user-flow-policies"></a>Vytvoření zásad toku uživatele

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit zásady toku uživatelů v portálu Microsoft Azure.

Toky uživatelů představují zásady, které Azure Active Directory (Azure AD) business-to-consumer (B2C) používá k zajištění bezpečného přihlášení, registraci, úpravy profilu a obnově zapomenutého hesla. Dynamics 365 Commerce používá tyto toky k provádění akcí zásad pro interakci s klientem Azure AD B2C. Pokud uživatel pracuje s těmito zásadami, je přesměrován na klienta Azure AD B2C, kde může provádět akce.

Azure AD B2C poskytuje tři základní typy toků uživatele:
- Registrace a přihlášení
- Úprava profilu
- Obnovení hesla

Můžete zvolit, zda chcete použít výchozí toky uživatelů, které poskytuje Azure AD, čímž se zobrazí stránka hostovaná v Azure AD B2C. Alternativně můžete vytvořit stránku HTML, která určí vzhled a chování těchto toků uživatelů. 

Chcete-li přizpůsobit stránky zásad uživatelů se stránkami integrovanými v Dynamics 365 Commerce, prostudujte si téma [Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md). Další informace naleznete v tématu [Přizpůsobení rozhraní uživatelských prostředí v Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Vytvoření zásady toku uživatele pro registraci a přihlášení

Chcete-li vytvořit zásadu toku uživatele pro registraci a přihlášení, postupujte podle následujících kroků.

1. Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.
1. Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.
1. Vyberte zásadu **Registrace a přihlášení** a poté vyberte **doporučenou** verzi.
1. V položce **Název** zadejte název zásady. Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).
1. V části **Poskytovatelé identity** v části **Místní účty** vyberte **E-mailová registrace**. E-mailová autentizace se používá ve většině běžných scénářů pro Commerce. Pokud také používáte ověřování poskytovatele identity sociální sítě, lze v tuto chvíli vybrat i tyto.
1. V části **Vícefaktorové ověřování** vyberte vhodnou volbu pro vaši společnost. 
1. V části **Atributy a deklarace identit uživatelů** vyberte možnosti pro získání atributů nebo deklarací identit pro vrácení (podle potřeby). Vyberte **Zobrazit více…** pro získání úplného seznamu vlastností a možností nároků. Commerce vyžaduje následující výchozí možnosti:

    | **Získat atribut** | **Vrátit deklaraci identity** |
    | ---------------------- | ----------------- |
    | E-mailová adresa          | E-mailové adresy   |
    | Křestní jméno             | Křestní jméno        |
    |                        | Poskytovatel identity |
    | Příjmení                | Příjmení           |
    |                        | ID objektu uživatele  |

1. Vyberte **Vytvořit**.

Následující obrázek je příkladem toku uživatele pro registraci a přihlášení Azure AD B2C.

![Nastavení zásady registrace a přihlášení.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Vytvoření zásady toku uživatele pro úpravu profilu

Chcete-li vytvořit zásadu toku uživatele pro úpravu profilu, postupujte podle následujících kroků.

1. Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.
1. Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.
1. Vyberte **Úprava profilu** a potom vyberte **doporučenou** verzi.
1. V části **Název** zadejte tok uživatele pro úpravu profilu. Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).
1. V části **Poskytovatelé identity** v části **Místní účty** vyberte **E-mailové přihlášení**.
1. V části **Atributy uživatele** zaškrtněte některé z následujících políček:
    
    | **Získat atribut** | **Vrátit deklaraci identity** |
    | ---------------------- | ----------------- |
    |                        | E-mailové adresy   |
    | Křestní jméno             | Křestní jméno        |
    |                        | Poskytovatel identity |
    | Příjmení                | Příjmení           |
    |                        | ID objektu uživatele  |
    
1. Vyberte **Vytvořit**.

Na následujícím obrázku je znázorněn příklad toku uživatele pro upravu profilu Azure AD B2C.

![Příklad uživatelského toku úpravy profilu Azure AD B2C](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Vytvoření zásady toku uživatele pro resetování hesla

Chcete-li vytvořit zásadu toku uživatele pro resetování hesla, postupujte podle následujících kroků.

1. Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.
1. Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.
1. Vyberte **Resetování hesla** a potom vyberte **doporučenou** verzi.
1. V poli **Název** zadejte název toku uživatele pro resetování hesla.
1. V části **Zprostředkovatelé identity** vyberte možnost **Resetovat heslo pomocí e-mailové adresy**.
1. Vyberte **Vytvořit**.
1. V části **Deklarace identity aplikace** zaškrtněte některé z následujících políček:
    - **E-mailové adresy**
    - **Křestní jméno**
    - **Příjmení**
    - **ID objektu uživatele**
1. Vyberte **Vytvořit**.

Následující obrázek znázorňuje, kde nastavit možnost **Resetovat heslo pomocí e-mailové adresy** v toku uživatele pro resetování hesla Azure AD B2C.

![Nastavení možnosti „Resetovat heslo pomocí e-mailové adresy“ v zásadě pro resetování hesla](./media/B2CImage_13.png)

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu nastavení B2C tenanta v Commerce, pokračujte na [Přidání poskytovatelů identity sociálních sítí](add-social-identity-providers.md).

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Vytvoření nebo připojení ke stávajícímu tenantovi Azure AD B2C v portálu Azure](create-link-aad-b2c-tenant.md)

[Vytvoření aplikace B2C](create-b2c-app.md)

[Přidání zprostředkovatelů sociální identity (volitelné)](add-social-identity-providers.md)

[Aktualizace Commerce Headquarters o nové informace Azure AD B2C](update-hq-aad-b2c-info.md)

[Konfigurace klienta B2C v konfigurátoru webů Commerce](config-b2c-tenant-site-builder.md)

[Doplňkové informace o B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
