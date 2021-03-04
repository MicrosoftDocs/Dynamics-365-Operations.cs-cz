---
title: Nastavení vlastních stránek pro přihlášení uživatelů
description: V tomto tématu je popsán způsob vytváření vlastních stránek v řešení Microsoft Dynamics 365 Commerce, které zpracovávají přizpůsobená přihlášení uživatelů klientů B2C (business-to-consumer) služby Azure Active Directory (Azure AD).
author: brianshook
manager: annbe
ms.date: 09/15/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5d9f2febc912b35897b063019146d219cadea1fa
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517225"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Nastavení vlastních stránek pro přihlášení uživatelů


[!include [banner](includes/banner.md)]

V tomto tématu je popsán způsob vytváření vlastních stránek v řešení Microsoft Dynamics 365 Commerce, které zpracovávají přizpůsobená přihlášení uživatelů klientů B2C (business-to-consumer) služby Azure Active Directory (Azure AD).

## <a name="overview"></a>Přehled

Chcete-li použít vlastní stránky, které jsou vytvořeny v řešení Dynamics 365 Commerce pro zpracování toků přihlášení uživatelů, je nutné nastavit zásady Azure AD, které budou odkazovány v prostředí Commerce. Pomocí aplikace Azure AD B2C můžete konfigurovat následující zásady Azure AD B2C: „Registrace a přihlášení“, „Úprava profilu“ a „Resetování hesla“. Na název klienta a zásad Azure AD B2C lze poté odkazovat během procesu zřizování prováděného pro prostředí Commerce pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).

Vlastní stránky Commerce lze sestavit pomocí modulu přihlášení, registrace, úpravy profilu účtu nebo obnovy hesla. V konfiguracích zásad Azure AD B2C na portálu Azure by pak měly být odkazovány adresy URL publikované pro tyto vlastní stránky.

## <a name="set-up-b2c-policies"></a>Nastavení zásad B2C

Po nastavení klienta Azure AD B2C a jeho přidružení k prostředí Commerce přejděte na stránku **Azure AD B2C** na portálu Azure a pak v nabídce v části **Zásady** vyberte možnost **Toky uživatelů (zásady)**.

![Příkaz Toky uživatelů (zásady) v nabídce](./media/B2C_CustomPage_PoliciesMenu.png)

Nyní můžete nakonfigurovat toky přihlášení uživatelů „Registrace a přihlášení“ a „Resetování hesla“.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigurace zásady „Registrace a přihlášení“

Chcete-li konfigurovat zásadu „Registrace a přihlášení“, postupujte podle následujících kroků.

1. Vyberte možnost **Nový tok uživatele** a poté na kartě **Doporučené** vyberte zásadu **Registrace a přihlášení**.
1. Zadejte název zásady (například **B2C\_1\_Registrace_a_prihlaseni**).
1. V části **Poskytovatelé identit** vyberte poskytovatele identit, kteří mají být použiti pro zásadu. Musí být vybrána alespoň možnost **Registrace e-mailu**.
1. Ve sloupci **Shromáždit atribut** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno** a **Příjmení**.
1. Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Poskytovatelé identit**, **Příjmení** a **ID objektu uživatele**.

    ![Vybrané atributy a deklarace identity](./media/B2C_SignInSignUp_Attributes.png)

1. Zvolte **OK** pro vytvoření zásady.
1. Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.
1. Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.

    ![Stránka vlastností pro novou zásadu](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Název zásady bude plně odkazován v prostředí Commerce. (Předpona **B2C\_1\_** bude zahrnuta do odkazu.) Zásady nelze po vytvoření přejmenovat. Pokud nahrazujete existující zásady pro vaše prostředí Commerce, můžete odstranit původní zásady a vytvořit novou zásadu se stejným názvem. Je-li však prostředí již zřízeno, můžete název nové zásady odeslat prostřednictvím požadavku na službu.

K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek. Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.

### <a name="configure-the-profile-editing-policy"></a>Konfigurace zásady „Úprava profilu“

Chcete-li konfigurovat zásadu „Úprava profilu“ , postupujte takto.

1. Vyberte možnost **Nový tok uživatele** a poté na kartě **Doporučené** vyberte zásadu **Úprava profilu**.
1. Zadejte název zásady (například **B2C\_1\_Uprava_profilu**).
1. V části **Poskytovatelé identit** vyberte poskytovatele identit, kteří mají být použiti pro zásadu. Je nutné vybrat alespoň **Přihlášení k místnímu účtu**.
1. Ve sloupci **Shromáždit atribut** zaškrtněte políčka **E-mailová adresa** a **Příjmení**.
1. Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Poskytovatelé identit**, **Příjmení** a **ID objektu uživatele**.
1. Zvolte **OK** pro vytvoření zásady.
1. Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.
1. Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.

K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek. Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.

### <a name="configure-the-password-reset-policy"></a>Konfigurace zásady „Resetování hesla“

Chcete-li konfigurovat zásadu „Resetování hesla“ , postupujte takto.

1. Vyberte možnost **Nový tok uživatele** a poté na kartě **Preview** vyberte zásadu **Resetování hesla v1.1**.

    ![Zásada Resetování hesla v1.1 vybraná na kartě Preview](./media/B2C_ForgetPassword_Menu.png)

1. Zadejte název zásady (například **B2C\_1\_Zapomenute_heslo**).
1. V části **Poskytovatelé identit** vyberte možnost **Resetovat heslo pomocí e-mailové adresy**.
1. Ve sloupci **Vrátit deklaraci identity** zaškrtněte políčka **E-mailová adresa**, **Křestní jméno**, **Příjmení** a **ID objektu uživatele**.

    ![Vybrané deklarace identity](./media/B2C_ForgetPassword_Attributes.png)

1. Zvolte **OK** pro vytvoření zásady.
1. Poklepejte na název nové zásady a poté v navigačním podokně vyberte možnost **Vlastnosti**.
1. Nastavte možnost **Povolit JavaScript s vynucením rozložení stránky (Preview)** na **Zapnuto**.

K této zásadě se vrátíte a dokončíte nastavení po vytvoření vlastních stránek. Nyní se uzavřením zásady vraťte na stránku **Toky uživatelů (zásady)** na portálu Azure.

## <a name="build-the-custom-pages"></a>Vytvoření vlastních stránek

Chcete-li vytvořit vlastní stránky pro zpracování přihlášení uživatelů, postupujte podle následujících kroků.

1. Ve vývojových nástrojech Commerce přejděte na web.
1. Vytvořte následujících pět šablon a pět stránek:

    - Šablona a stránka **Přihlášení**, které používají modul přihlášení.
    - Šablona a stránka **Registrace**, které používají modul registrace.
    - Šablona a stránka **Resetování hesla**, které používají modul pro resetování hesla.
    - Šablona a stránka **Ověření resetování hesla**, které používají modul pro ověření resetování hesla.
    - Šablona a stránka **Úprava profilu**, které používají modul úpravy profilu účtu.

Při vytváření stránek postupujte podle následujících pokynů:

- Pro každou stránku nebo modul použijte rozložení a styl, které nejlépe vyhovují vašim obchodním požadavkům.
- Publikujte všechny stránky a adresy URL, které jsou potřeba při nastavení Azure AD B2C.
- Po publikování stránek a adres URL shromážděte adresy URL, které je nutné použít pro konfigurace zásad Azure AD B2C. Přípona **?preloadscripts=true** bude přidána do každé adresy URL při jejím použití.

> [!IMPORTANT]
> Opakovaně nepoužívejte univerzální záhlaví a zápatí s relativními odkazy. Vzhledem k tomu, že tyto stránky budou hostovány v doméně Azure AD B2C při jejich použití, měly by být pro všechny odkazy použity pouze absolutní adresy URL.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Konfigurace zásad Azure AD B2C s informacemi o vlastní stránce 

Na portálu Azure přejděte zpět na stránku **Azure AD B2C** a poté v nabídce v části **Zásady** vyberte možnost **Toky uživatelů (zásady)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Aktualizace zásady „Registrace a přihlášení“ o informace o vlastní stránce

Chcete-li aktualizovat zásadu „Registrace a přihlášení“ o informace o vlastní stránce, postupujte takto.

1. V zásadě **Registrace a přihlášení**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.
1. Vyberte rozložení **Jednotná stránka pro registraci nebo přihlášení**.
1. Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.
1. Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro přihlášení. Zahrňte příponu **?preloadscripts=true**. Zadejte například ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.
1. Vyberte rozložení **Stránka pro registraci místního účtu**.
1. Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.
1. Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro registraci. Zahrňte příponu **?preloadscripts=true**. Zadejte například ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.
1. V části **Atributy uživatele** postupujte takto:

    1. Pro atributy **E-mailová adresa**, **Křestní jméno** a **Příjmení** vyberte v poli **Vyžaduje ověření** hodnotu **Ne**.
    1. Pro atributy **Křestní jméno** a **Příjmení** vyberte v poli **Volitelné** hodnotu **Ne**.

    ![Konfigurace zásady Stránka pro registraci místního účtu](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Aktualizace zásady „Úprava profilu“ o informace o vlastní stránce

Chcete-li aktualizovat zásadu „Editace profilu“ o informace o vlastní stránce, postupujte takto.

1. V zásadě **Úprava profilu**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.
1. Vyberte rozložení **Stránka Úprava profilu**.
1. Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.
1. Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL profilu. Zahrňte příponu **?preloadscripts=true**. Zadejte například ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.
1. V části **Atributy uživatele** postupujte takto:

    1. Pro atributy **E-mailová adresa** a **Křestní jméno** vyberte v poli **Vyžaduje ověření** hodnotu **Ne**.
    1. Pro atributy **Křestní jméno** a **Příjmení** vyberte v poli **Volitelné** hodnotu **Ne**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Aktualizace zásady „Resetování hesla“ o informace o vlastní stránce

Chcete-li aktualizovat zásadu „Resetování hesla“ o informace o vlastní stránce, postupujte takto.

1. V zásadě **Resetování hesla**, kterou jste již konfigurovali, vyberte v navigačním podokně možnost **Rozložení stránek**.
1. Vyberte rozložení **Stránka Nové heslo**.
1. Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.
1. Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro resetování hesla. Zahrňte příponu **?preloadscripts=true**. Zadejte například ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.
1. Vyberte rozložení **Stránk Ověření účtu**.
1. Nastavte volbu **Použít obsah vlastní stránky** na hodnotu **Ano**.
1. Do pole **Identifikátor URI vlastní stránky** zadejte úplnou adresu URL pro ověření. Zahrňte příponu **?preloadscripts=true**. Zadejte například ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. V poli **Verze rozložení stránky (Preview)** vyberte **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Přizpůsobení výchozích textových řetězců pro popisky a popisy

V knihovně modulů jsou moduly přihlášení předvyplněny výchozími textovými řetězci pro popisky a popisy. Tyto řetězce můžete upravit v sadě SDK (Software Development Kit) tak, že aktualizujete hodnoty v souboru global.json pro modul přihlášení.

Například výchozí text odkazu zapomenutého hesla je **Zapomenuté heslo?**. Tento výchozí text je zobrazen na přihlašovací stránce.

![Výchozí text odkazu zapomenutého hesla na přihlašovací stránce](./media/B2C_SignUp_ModuleFace.png)

V souboru global.json pro modul přihlášení v knihovně modulů je však možné upravit text na **Zapomněli jste heslo?**, jak je znázorněno na následujícím obrázku.

![Aktualizovaný text odkazu v souboru global.json v modulu přihlášení](./media/B2C_CustomizingStringsForModule.png)

Po aktualizaci souboru global.json a publikování změn se nový text odkazu zobrazí v modulu přihlášení, a to jak v řešení Commerce, tak na aktivní přihlašovací stránce.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)

[Konfigurace několika klientů B2C v prostředí Commerce](configure-multi-B2C-tenants.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]