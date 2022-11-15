---
title: Konfigurace CPOS tak, aby používal vlastní aplikaci Azure AD
description: Tento článek vysvětluje, jak nakonfigurovat Cloud POS (CPOS), aby používal vlastní aplikaci Azure Active Directory (Azure AD).
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746253"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>Konfigurace CPOS tak, aby používal vlastní aplikaci Azure AD

[!include [banner](includes/banner.md)]

Ve výchozím nastavení Cloud POS (CPOS) v Microsoft Dynamics 365 Commerce odkazuje na registrovanou aplikaci Microsoft první strany v Azure Active Directory (Azure AD). Proto můžete používat CPOS, aniž byste museli provádět jakékoli změny v Azure AD. Možná však budete chtít nasměrovat svou instanci CPOS na vlastní aplikaci Azure AD, kterou ovládáte. Tento článek vysvětluje, jak nakonfigurovat CPOS, aby používal vlastní aplikaci Azure AD.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Nastavte si vlastní aplikace maloobchodního serveru v Azure AD

Chcete-li vytvořit a nakonfigurovat vlastní aplikaci maloobchodního serveru v Azure AD, postupujte následovně.

1. Přihlaste se do [centra pro správu Azure Active Directory](https://aad.portal.azure.com) pomocí uživatelského účtu Azure AD. Uživatelský účet nemusí mít oprávnění správce.
1. Vyberte **Azure Active Directory**.
1. Vyberte **Registrace aplikací** a poté vyberte **Nová registrace** k otevření dialogového okna **Zaregistrovat aplikaci**.
1. Nastavte následující pole:

    - **Název** - Zadejte vlastní název aplikace. Například zadejte **Vlastní maloobchodní server**.
    - **Typy účtů podpory** – Vyberte výchozí možnost, **Účty pouze v tomto organizačním adresáři (pouze Microsoft – jeden tenant)**.
    - **Adresa URI pro přesměrování** – Toto pole je volitelné. Ponechte prázdné.
    - **ID stromu služby** – Toto pole je volitelné. Ponechte prázdné.
    
1. Vyberte **Registrovat**. Zobrazí se konfigurační stránka pro nově zaregistrovanou aplikaci.
1. V části **Přehled \> Základy** vyberte **Přidat identifikátor URI ID aplikace** a poté vyberte **Nastavit** vedle **URI ID aplikace**. Poznamenejte si navrhovanou hodnotu a poté vyberte **Uložit**, abyste tuto hodnotu přijali. 
1. Vyberte **Přidat rozsah** a poté nastavte následující pole:

    - **Název rozsahu** – Zadejte vlastní rozsahu. Například zadejte **Legacy.Access.Full**.
    - **Kdo může souhlasit** – Určete, zda mohou souhlas udělit správci i uživatelé nebo pouze správci na základě zásad zabezpečení vaší organizace.
    - **Zobrazovaný název pro souhlas správce** – Zadejte zobrazovaný název. Například zadejte **Přístup k maloobchodnímu serveru**.
    - **Popis souhlasu správce** – Zadejte popis. Například zadejte **Uděluje přístup k API maloobchodního serveru**.

1. Vyberte **Přidat rozsah** k dokončení procesu vytváření rozsahu.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Nastavení vlastní aplikace CPOS v Azure AD

> [!IMPORTANT]
> Pokud upgradujete stávající vlastní aplikaci CPOS Azure AD, která byla vytvořena před verzí Commerce 10.0.21, postupujte podle kroků v [Upgradujte stávající vlastní aplikaci CPOS Azure AD vytvořenou před komerční verzí 10.0.21](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021).

Chcete-li vytvořit a nakonfigurovat vlastní aplikaci CPOS v Azure AD, postupujte následovně.

1. Přihlaste se do [centra pro správu Azure Active Directory](https://aad.portal.azure.com) pomocí uživatelského účtu Azure AD. Uživatelský účet nemusí mít oprávnění správce.
1. Vyberte **Azure Active Directory**.
1. Vyberte **Registrace aplikací** a poté vyberte **Nová registrace** k otevření dialogového okna **Zaregistrovat aplikaci**.
1. Nastavte následující pole:

    - **Název** – Zadejte název aplikace. Například zadejte **Vlastní Cloud POS**.
    - **Typy účtů podpory** – Vyberte výchozí možnost, **Účty pouze v tomto organizačním adresáři (pouze Microsoft – jeden tenant)**.
    - **URI pro přesměrování** – Vyberte **Jednostránková aplikace (SPA)** v rozevíracím seznamu a poté zadejte URI CPOS.
    - **ID stromu služby** – Toto pole je volitelné. Ponechte prázdné.

1. Vyberte **Registrovat**. Zobrazí se konfigurační stránka pro nově zaregistrovanou aplikaci.
1. V části **Manifest** nastavte parametry **oauth2AllowIdTokenImplicitFlow** a **oauth2AllowImplicitFlow** na **true** a poté vyberte **Uložit**.
1. V části **Konfigurace tokenu** postupujte takto a přidejte dvě deklarace identity:

    1. Vyberte **Přidat volitelnou deklaraci identity**. Nastavte pole **Typ tokenu** a **ID** a poté vyberte deklaraci identity **sid**. Vyberte **přidat**.
    1. Vyberte **Přidat volitelnou deklaraci identity**. Nastavte pole **Typ tokenu** a **Přístup** a poté vyberte deklaraci identity **sid**. Vyberte **přidat**.

1. V části **Oprávnění API** vyberte **Přidat oprávnění**.
1. Na kartě **API, která používá moje organizace** vyhledejte aplikaci maloobchodního serveru, které jste vytvořili v části [Nastavení vlastní aplikace maloobchodního serveru v Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad). Poté vyberte **Přidat oprávnění**.
1. V části **Přehled** si poznamenejte hodnotu v poli **ID aplikace (klienta)**.

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>Upgradujte stávající vlastní aplikaci CPOS Azure AD vytvořenou před verzí Commerce 10.0.21

Chcete-li upgradovat stávající vlastní aplikaci CPOS Azure AD vytvořenou před verzí Commerce 10.0.21, postupujte následovně. 

1. V portálu Azure otevřete vlastní aplikaci CPOS Azure AD.
1. Vyberte kartu **Ověřování**.
1. Zkopírujte a uložte původní URI přesměrování z typu **Web** pro pozdější použití a poté jej odstraňte.
1. Vyberte **Přidat platformu** a poté vyberte **Jednostránková aplikace (SPA)**.
1. Přidejte původní URI webového přesměrování zkopírované výše do platformy SPA.
1. V části **Konfigurace tokenu** postupujte takto a přidejte dvě deklarace identity:
    1. Vyberte **Přidat volitelnou deklaraci identity**. Nastavte pole **Typ tokenu** a **ID** a poté vyberte deklaraci identity **sid**. Vyberte **přidat**.
    1. Vyberte **Přidat volitelnou deklaraci identity**. Nastavte pole **Typ tokenu** a **Přístup** a poté vyberte deklaraci identity **sid**. Vyberte **přidat**.

## <a name="update-the-cpos-configuration-file"></a>Aktualizace konfiguračního souboru CPOS

Otevřete soubor CPOS config.json a proveďte v něm následující aktualizace.

1. Nahraďte hodnotu klíče **AADClientId** za hodnotu **ID aplikace (klienta)** vlastní aplikace CPOS, kterou jste vytvořili v části [Nastavení vlastní aplikaci CPOS v Azure AD](#set-up-a-custom-cpos-app-in-azure-ad).
1. Nahraďte hodnotu klíče **AADRetailServerResourceId** za hodnotu **URI ID aplikace** vlastní aplikace maloobchodního serveru, kterou jste vytvořili v části [Nastavení vlastní aplikace maloobchodního serveru v Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad).

CPOS použije oba parametry při odesílání požadavků do Azure AD k získání bezpečnostního tokenu.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Aktualizace nastavení poskytovatelů identity v Commerce headquarters

Dále musíte aktualizovat nastavení poskytovatelů identity v Commerce headquarters.

1. V Commerce headquarters otevřete stránku **Sdílené parametry Commerce**.
1. Na kartě **Poskytovatelé identity** v části **Poskytovatelé identity** vyberte řádek, kde je pole **Typ** nastaveno na **Azure Active Directory** a pole **Vydavatel** ukazuje na klienta Azure AD. Toto nastavení deklaruje, že budete pracovat s podřízenými mřížkami, které obsahují data související s poskytovatelem identity, který odpovídá vašemu tenantovi Azure AD.
1. V části **Předávající strany** vyberte **Přidat** při přidání řádku.
1. Nastavte následující pole:

    - **ClientId** – Zadejte hodnotu **ID aplikace (klienta)** vlastní aplikace CPOS, kterou jste vytvořili v části [Nastavení vlastní aplikaci CPOS v Azure AD](#set-up-a-custom-cpos-app-in-azure-ad).
    - **Type** – Vyberte **Veřejný**.
    - **UserType** – Vyberte **Pracovník**.

1. Vyberte řádek, který jste přidali. Část **ID zdrojů serveru** pod částí **Předávající strany** zobrazuje ID aplikace maloobchodního serveru, ke kterým má aplikace, kterou jste vybrali v mřížce **Předávající strany**, přístup.
1. V části **ID prostředků serveru** vyberte **Přidat** pro přidání řádku.
1. Do pole **Id prostředku serveru** zadejte hodnotu **URI ID aplikace** vlastní aplikace maloobchodního serveru, kterou jste vytvořili v části [Nastavení vlastní aplikace maloobchodního serveru v Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad).

    > [!IMPORTANT]
    > Všechna pole uvedená v předchozích krocích rozlišují velká a malá písmena. Hodnoty, které zadáte, se musí přesně shodovat s hodnotami, které jsou nakonfigurovány v centru pro správu Azure AD.

1. Přejděte na Maloobchod a velkoobchod **IT pro maloobchod a velkoobchod \> Plán distribuce** a spusťte úlohu **1110** (**Globální konfigurace**).

Nyní můžete aktivovat zařízení CPOS pomocí svých vlastní aplikace Azure AD.

## <a name="additional-resources"></a>Další prostředky

[Aktivace zařízení pokladního místa (POS)](dev-itpro/retail-device-activation.md)

[Správa účtů aktivace a ověření zařízení](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
