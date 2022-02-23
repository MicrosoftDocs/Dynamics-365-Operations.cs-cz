---
title: Nastavení klienta B2C v Commerce
description: Tohle téma popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: af2ec75328b6377c5d92656d011d21576417a63f
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517373"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Nastavení klienta B2C v Commerce

[!include [banner](includes/banner.md)]

Tohle téma popisuje, jak nastavíte své klienty Azure Active Directory (Azure AD) business-to-consumer (B2C) pro ověření webu uživatele v aplikaci Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Dynamics 365 Commerce používá Azure AD B2C pro podporu toků přihlašovacích údajů a ověřování uživatele. Uživatel se může registrovat, přihlásit a obnovit své heslo pomocí těchto toků. Azure AD B2C ukládá citlivé informace o ověřování uživatele, například jeho uživatelské jméno a heslo. Záznam uživatele v klientovi B2C uloží buď záznam místního účtu B2C nebo záznam zprostředkovatele sociální identity B2C. Tyto záznamy B2C budou odkazovat zpět na záznam odběratele v prostředí Commerce.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Vytvoření nebo připojení ke stávajícími klientovi AAD B2C v portálu Azure

1. Přihlaste se do [portálu Azure](https://portal.azure.com/).
1. Z nabídky portálu Azure vyberte možnost **Vytvořit prostředek**. Ujistěte se, že používáte předplatné a adresář, který bude připojen k vašemu prostředí Commerce.

    ![Vytvoření prostředku na portálu Azure](./media/B2CImage_1.png)

1. Přejděte na **Identita \> Azure Active Directory B2C**.
1. Na stránce **Vytvoření nového klienta B2C nebo připojení k existujícímu klientovi** použijte jednu z následujících možností, které nejlépe vyhovují potřebám vaší společnosti:

    - **Vytvořit nového klienta Azure AD B2C**: Touto možností vytvoříte nového klienta AAD B2C.
        1. Vyberte **Vytvořit nového klienta Azure AD B2C**.
        1. Pro **Název organizace** zadejte název organizace.
        1. Pro **Počáteční název domény** zadejte počáteční název domény.
        1. Pro **Země nebo oblast** vyberte zemi nebo oblast.
        1. Volbou **Vytvořit** vytvoříte klienta.

     ![Vytvoření nového klienta Azure AD](./media/B2CImage_2.png)

     - **Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**: Tuto možnost použijte, pokud již existuje klient Azure AD B2C, který chcete propojit.
        1. Vyberte **Propojit existujícího klienta Azure AD B2C s mým předplatným Azure**.
        1. Pro **Klient Azure AD B2C** vyberte příslušného klienta B2C. Pokud se v oblasti výběru zobrazí zpráva „Nebyly nalezeni žádní oprávnění klienti B2C“, nemáte žádného existující oprávněného klienta B2C a budete muset vytvořit nového.
        1. Pro **Skupina prostředků** vyberte možnost **Vytvořit novou**. Zadejte **Název** pro skupinu prostředků, která bude obsahovat klienta, vyberte **Umístění skupiny prostředků** a pak vyberte možnost **Vytvořit**.

    ![Propojení existujícího klienta Azure AD B2C s předplatným Azure](./media/B2CImage_3.png)

1. Po vytvoření nového adresáře Azure AD B2C (což může chvíli trvat) se na řídicím panelu zobrazí odkaz na nový adresář. Tento odkaz vás přesměruje na stránku „Vítá vás Azure Active Directory B2C“.

    ![Odkaz na nový adresář AAD](./media/B2CImage_4.png)

> [!NOTE]
> Pokud máte více předplatných v rámci účtu Azure nebo jste zřídili klienta B2C bez propojení s aktivním předplatným, banner **Řešení potíží** vás nasměruje k propojení klienta a předplatného. Vyberte zprávu řešení potíží a podle pokynů vyřešte problém s předplatným.

Na následujícím obrázku je znázorněn příklad banneru **Řešení potíží** v Azure AD B2C.

![Upozornění, že adresář nemá žádné aktivní předplatné](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>Vytvoření aplikace B2C

Po vytvoření klienta B2C vytvoříte aplikaci B2C s klientem pro interakci s akcemi Commerce.

Chcete-li vytvořit aplikaci B2C, postupujte následovně.

1. Na portálu Azure vyberte možnost **Aplikace (starší verze)** a pak vyberte možnost **Přidat**.
1. V poli **Název** zadejte název požadované aplikace AAD B2C.
1. V části **Webová aplikace/webové rozhraní API** vyberte pro **Zahrnout webovou aplikaci/webové rozhraní API** možnost **Ano**.
1. Pro **Povolit implicitní tok** vyberte možnost **Ano** (výchozí hodnota).
1. Pro **Adresa URL odpovědi** zadejte vyhrazené adresy URL pro odpovědi. Viz [Adresy URL pro odpovědi](#reply-urls) níže, kde najdete informace o adresách URL odpovědí a jak je naformátovat.
1. Pro **Zahrnout nativního klienta** vyberte možnost **Ne** (výchozí hodnota).
1. Vyberte **Vytvořit**.

### <a name="reply-urls"></a>Adresy URL pro odpovědi

Adresy URL pro odpovědi jsou důležité, protože poskytují seznam povolených návratových domén, když váš web volá Azure AD B2C pro ověření uživatele. To umožňuje vrátit ověřeného uživatele zpět do domény, ze které se přihlásí (doména vašeho webu). 

V poli **Adresa URL odpovědi** na obrazovce **Azure AD B2C – aplikace \> Nová aplikace** je nutné přidat samostatné řádky pro doménu vašeho webu a (po zřízení vašeho prostředí) adresu URL generovanou řešením Commerce. Tyto adresy URL musí vždy používat platný formát adresy URL a musí to být pouze základní adresy URL (bez koncového lomítka nebo cesty). Řetězec ``/_msdyn365/authresp`` pak musí být přidán k základní adrese URL, jako v následujících příkladech.

- ``https://www.fabrikam.com/_msdyn365/authresp``(Doména by se měla zcela shodovat s doménou elektronického obchodu. Pokud máte více domén, musíte přidat tuto adresu URL pro každou doménu.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Vytvoření zásad toku uživatele

Toky uživatelů představují zásady, které Azure AD B2C používá k zajištění bezpečného přihlášení, registraci, úpravy profilu a obnově zapomenutého hesla. Dynamics 365 Commerce používá tyto toky k provádění akcí zásad pro interakci s klientem Azure AD B2C. Pokud uživatel pracuje s těmito zásadami, je přesměrován na klienta Azure AD B2C, kde může provádět akce.

Azure AD B2C poskytuje tři základní typy toků uživatele:
- Registrace a přihlášení
- Úprava profilu
- Obnovení hesla

Můžete zvolit, zda chcete použít výchozí toky uživatelů, které poskytuje Azure AD, čímž se zobrazí stránka hostovaná v AAD B2C. Alternativně můžete vytvořit stránku HTML, která určí vzhled a chování těchto toků uživatelů. 

Chcete-li přizpůsobit stránky zásad uživatelů pro Dynamics 365 Commerce, prostudujte si téma [Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md). Další informace naleznete v tématu [Přizpůsobení rozhraní uživatelských prostředí v Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Vytvoření zásady toku uživatele pro registraci a přihlášení

Chcete-li vytvořit zásadu toku uživatele pro registraci a přihlášení, postupujte podle následujících kroků.

1. Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.
1. Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.
1. Na kartě **Doporučené** vyberte možnost **Registrace a přihlášení**.
1. V položce **Název** zadejte název zásady. Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).
1. V části **Zprostředkovatelé identity** zaškrtněte příslušné políčko.
1. V části **Vícefaktorové ověřování** vyberte vhodnou volbu pro vaši společnost. 
1. V části **Atributy a deklarace identit uživatelů** vyberte možnosti pro získání atributů nebo deklarací identit pro vrácení (podle potřeby). Commerce vyžaduje následující výchozí možnosti:

    | **Získat atribut** | **Vrátit deklaraci identity** |
    | ---------------------- | ----------------- |
    | E-mailová adresa          | E-mailové adresy   |
    | Křestní jméno             | Křestní jméno        |
    |                        | Poskytovatel identity |
    | Příjmení                | Příjmení           |
    |                        | ID objektu uživatele  |

1. Vyberte **Vytvořit**.

Následující obrázek je příkladem toku uživatele pro registraci a přihlášení Azure AD B2C.

![Nastavení zásady registrace a přihlášení](./media/B2CImage_11.png)

Následující obrázek znázorňuje možnost **Spustit tok uživatele** v toku uživatele pro registraci a přihlášení Azure AD B2C.

![Možnost Spustit tok uživatele v toku zásady](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Vytvoření zásady toku uživatele pro úpravu profilu

Chcete-li vytvořit zásadu toku uživatele pro úpravu profilu, postupujte podle následujících kroků.

1. Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.
1. Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.
1. Na kartě **Doporučené** vyberte možnost **Úprava profilu**.
1. V části **Název** zadejte tok uživatele pro úpravu profilu. Tento název se pak zobrazí s použitím předpony, kterou přiřadí portál (například „B2C_1_“).
1. V části **Zprostředkovatelé identity** vyberte možnost **Přihlášení k místnímu účtu**.
1. V části **Atributy uživatele** zaškrtněte některé z následujících políček:
    - **E-mailové adresy** (pouze **Vrátit deklaraci identity**)
    - **Křestní jméno** (**Získat atribut** a **Vrátit deklaraci identity**)
    - **Zprostředkovatel identity** (pouze **Vrátit deklaraci identity**)
    - **Příjmení** (**Získat atribut** a **Vrátit deklaraci identity**)
    - **ID objektu uživatele** (pouze **Vrátit deklaraci identity**)
1. Vyberte **Vytvořit**.

Na následujícím obrázku je znázorněn příklad toku uživatele pro upravu profilu Azure AD B2C.

![Vytvoření toku uživatele pro úpravu profilu](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Vytvoření zásady toku uživatele pro resetování hesla

Chcete-li vytvořit zásadu toku uživatele pro resetování hesla, postupujte podle následujících kroků.

1. Na portálu Azure vyberte možnost **Toky uživatelů (zásady)** v levém navigačním podokně.
1. Na stránce **Azure AD B2C – toky uživatelů (zásady)** vyberte možnost **Nový tok uživatele**.
1. Na kartě **Doporučené** vyberte možnost **Resetování hesla**.
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

## <a name="add-social-identity-providers-optional"></a>Přidání zprostředkovatelů sociální identity (volitelné)

Zprostředkovatelé sociální identity umožňují uživatelům používat účty sociálních sítí k ověřování. Přidání ověření zprostředkovatele sociální identity je volitelné v Dynamics 365 Commerce. 

Pokud není přidáno ověřování zprostředkovatele sociální identity, budou výchozí profily Azure AD B2C hlavními profily pro vaše uživatele. Uživatelé budou moci vybrat vlastní uživatelské jméno (jejich upřednostňovaná e-mailová adresa) a nastavit heslo. Azure AD B2C bude uživatele ověřovat přímo. 

Je-li přidáno ověřování zprostředkovatele sociální identity a uživatel si zvolí jednoho ze nabízených zprostředkovatelů sociální identity, bude v klientu Azure AD B2C vytvořena entita. Azure AD B2C poté ověří přihlašovací údaje uživatele pomocí zprostředkovatele sociální identity.

> [!NOTE]
> Přihlášení zprostředkovatele identity vytvoří záznam v klientovi B2C, ale v jiném formátu než místní účty, protože pro ověření bude volat externí odkaz na zprostředkovatele sociální identity. Uživatel může použít stejnou e-mailovou adresu v rámci zprostředkovatelů sociální identity, což znamená, že uživatelské jméno e-mailu použité pro ověření nemusí být jedinečné pro klienta. Azure AD B2C pouze vynutí, aby uživatelé měli jedinečnou e-mailovou adresu v místních účtech B2C.

Před přidáním zprostředkovatele sociální identity pro ověřování je nutné přejít na portál zprostředkovatele identity a nastavit aplikaci zprostředkovatele identity tak, jak je uvedeno v dokumentaci k Azure AD B2C. Níže je uveden seznam odkazů na dokumentaci.

- [Amazon](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (jeden klient)](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Účet Microsoft](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Přidání a nastavení zprostředkovatele sociální identity

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
1. Chcete-li připojit zásadu toku uživatele pro přihlášení/registraci, vyberte každého zprostředkovatele identity, kterého jste pro svůj účet nastavili. Chcete-li je otestovat, vyberte možnost **Spustit tok uživatele** pro každého zprostředkovatele identity. Na nové kartě se zobrazí stránka pro přihlášení s oblastí výběru nového zprostředkovatele identity.

Následující obrázek znázorňuje příklad obrazovek **Přidání zprostředkovatele identity** a **Nastavení zprostředkovatele** sociální identity v Azure AD B2C.

![Přidání poskytovatele sociální identity do aplikace](./media/B2CImage_14.png)

Následující obrázek znázorňuje příklad, jak vybrat zprostředkovatele identity na stránce **Zprostředkovatelé identity** v Azure AD B2C.

![Výběr jednotlivých zprostředkovatelů sociální identity a povolení vaší zásady](./media/B2CImage_16.png)

Následující obrázek znázorňuje příklad výchozí přihlašovací obrazovky se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity.

![Příklad výchozí obrazovky pro přihlášení se zobrazeným tlačítkem pro přihlášení zprostředkovatele sociální identity](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Aktualizace Commerce Headquarters o nové informace Azure AD B2C

Po dokončení výše uvedených kroků pro zřízení Azure AD B2C musí být aplikace Azure AD B2C registrována ve vašem prostředí Dynamics 365 Commerce.

Chcete-li aktualizovat Headquarters o nové informace Azure AD B2C, postupujte takto.

1. V Commerce přejděte na **Sdílené parametry Commerce** a vyberte **Zprostředkovatelé identity** v levé nabídce.
1. V části **Zprostředkovatelé identity** postupujte takto:
    1. V poli **Vystavitel** zadejte adresu URL vystavitele zprostředkovatele identity. Chcete-li najít adresu URL svého vystavitele, viz [Získání adresy URL vystavitele](#obtain-issuer-url) níže.
    1. Do pole **Název** zadejte název záznamu vystavitele.
    1. Do pole **Typ** zadejte **Azure AD B2C (id_token)**.
1. V části **Předávající strany** s výše vybranou položkou zprostředkovatele identity B2C postupujte takto:
    1. V poli **ID klienta** zadejte ID aplikace B2C. To lze nalézt v poli **ID aplikace** na stránce vlastností aplikace B2C.
    1. Do pole **Typ** zadejte **Veřejné**.
    1. Do pole **Typ uživatele** zadejte **Zákazník**.
1. V podokně akcí vyberte **Uložit**.
1. Ve vyhledávacím poli Commerce Search vyhledejte **Plán distribuce**.
1. V levé navigační nabídce stránky **Plán distribuce** vyberte úlohu **1110 Globální konfigurace**.
1. V podokně akcí zvolte **Spustit**.

### <a name="obtain-issuer-url"></a>Získání adresy URL vystavitele

Chcete-li získat adresu URL vystavitele svého zprostředkovatele identity, postupujte takto.

1. V následujícím formátu vytvořte adresu URL metadat s použitím vašeho klienta a zásady B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Příklad: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Do adresního řádku prohlížeče zadejte adresu URL metadat.
1. V metadatech zkopírujte adresu URL vystavitele zprostředkovatele identity (hodnota pro **„vystavitel“**).
    - Příklad: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurace klienta B2C v konfigurátoru webů Commerce

Po dokončení nastavení klienta Azure AD B2C musíte nakonfigurovat klienta B2C v konfigurátoru webů Commerce. Kroky konfigurace zahrnují získání informací o aplikaci B2C z portálu Azure, zadání informací o aplikaci B2C do konfigurátru webů a následné přidružení aplikace B2C k vašemu webu a kanálu.

### <a name="collect-the-required-application-information"></a>Získání požadovaných informací o aplikaci

Chcete-li získat požadované informace o aplikaci, postupujte podle následujících kroků.

1. V portálu Azure přejděte na **Domovská stránka \> Azure AD B2C – aplikace**.
1. Pro získání podrobností o aplikaci vyberte svou aplikaci a v levém navigačním podokně vyberte **Vlastnosti**.
1. Z pole **ID aplikace** získejte ID aplikace B2C vytvořené ve vašem klientovi B2C. Později bude zadáno jako **GUID klienta** v konfigurátoru webů.
1. V poli **AdresaURL odpovědi** získejte adresu URL odpovědi.
1. Přejděte na **Domovská stránka \> Azure AD B2C – toky uživatelů (zásady)** a získejte názvy jednotlivých zásad toku uživatelů.

Na následujícím obrázku je znázorněn příklad stránky **Azure AD B2C – aplikace**.

![Přechod k aplikaci B2C ve vašem klientovi](./media/B2CImage_19.png)

Na následujícím obrázku je znázorněn příklad stránky **Vlastnosti** aplikace v Azure AD B2C. 

![Kopírování ID aplikace z vlastností aplikace B2C](./media/B2CImage_21.png)

Následující obrázek znázorňuje příklad zásad toku uživatelů na stránce **Azure AD B2C – toky uživatelů (zásady)**.

![Získání názvů jednotlivých toků zásad B2C](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>Zadání informací o aplikaci klienta AAD B2C do platformy Commerce

Před přidružením klienta B2C ke svým webům je nutné zadat podrobnosti o klientovi Azure AD B2C do konfigurátoru webů Commerce.

Chcete-li do platformy Commerce přidat informace o aplikaci klienta AAD B2C, postupujte podle následujících kroků.

1. Přihlaste se jako správce ke konfigurátoru webů Commerce pro vaše prostředí.
1. V levém navigačním podokně vyberte **Nastavení klienta**, čímž jej rozbalíte.
1. V části **Nastavení klienta** vyberte **Nastavení B2C**. 
1. V hlavním okně vedle položky **Aplikace B2C** vyberte možnost **Spravovat**. (Pokud se klient zobrazí v seznamu aplikací B2C, pak již byl přidán správcem. Ověřte, že položky v kroku 6 odpovídají vaší aplikaci B2C.)
1. Vyberte **Přidat aplikaci B2C**.
1. Ve zobrazeném formuláři zadejte následující požadované položky s použitím hodnot z klienta a aplikace B2C. Pole, která nejsou vyžadována (bez hvězdičky), mohou být ponechána prázdná.

    - **Název aplikace**: název aplikace B2C, například „Fabrikam B2C“.
    - **Název klienta**: Název klienta B2C (použijte například "fabrikam", pokud se doména pro klienta B2C zobrazuje jako "fabrikam.onmicrosoft.com"). 
    - **ID zásady zapomenutého hesla**: ID zásady toku uživatele pro zapomenuté heslo, například „B2C_1_ResetovaniHesla“.
    - **ID zásady registrace a přihlášení**: ID zásady toku uživatele pro registraci a přihlášení, například „B2C_1_registrace_prihlaseni“.
    - **GUID klienta**: ID aplikace B2C, například „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.
    - **ID zásady úpravy profilu**: ID zásady toku uživatele pro úpravu profilu, například „B2C_1A_UpravaProfilu“.

1. Vyberte **OK**. Nyní by se měl zobrazit název vaší aplikace B2C v seznamu.
1. Klepnutím na tlačítko **Uložit** uložte změny.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Přidružení aplikace B2C k webu a kanálu

> [!WARNING]
> Pokud je váš web již přidružen k aplikaci B2C, změna na jinou aplikaci B2C odstraní aktuální odkazy vytvořené pro uživatele, které jsou již zaregistrováni v tomto prostředí. V případě změny nebudou mít uživatelé k dispozici žádná pověření přidružená k aktuálně přiřazené aplikaci B2C. 
> 
> Aplikaci B2C aktualizujte pouze v případě, že aplikaci B2C kanálu zřizujete poprvé, nebo pokud čekáte, že se uživatelé znovu zaregistrují s novými pověřeními pro tento kanál pomocí nové aplikace B2C. Buďte opatrní při přiřazování kanálů k aplikacím B2C a pojmenovávejte aplikace srozumitelně. Není-li kanál přidružen k aplikaci B2C v níže uvedených krocích, uživatelé přihlašující se k tomuto kanálu pro váš web budou zadáni do aplikace B2C, která se zobrazí jako **výchozí** v seznamu aplikací B2C v umístění **Nastavení klienta \> Nastavení B2C**.

Chcete-li přidružit aplikaci B2C k webu a kanálu, postupujte takto.

1. Přejděte na svůj web konfigurátoru webů Commerce.
1. V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.
1. Pod položkou **Nastavení webu** vyberte možnost **Kanály**.
1. V hlavním okně v části **Kanály** vyberte svůj kanál.
1. V podokně vlastností kanálu vpravo vyberte název svojí aplikace B2C z rozevírací nabídky **Vybrat aplikaci B2C**.
1. Vyberte možnost **Zavřít** a pak vyberte možnost **Uložit a publikovat**.

## <a name="additional-b2c-information"></a>Doplňkové informace o B2C

### <a name="customer-migration"></a>Migrace zákazníků

Pokud uvažujete o migraci záznamů zákazníků z předchozí platformy zprotředkovatele identity, spolupracujte s týmem Dynamics 365 Commerce, abyste zkontrolovali potřeby zákazníka ohledně migrace.

Další dokumentaci Azure AD B2C ohledně migrace zákazníků najdete v tématu [Migrace uživatelů do Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Vlastní zásady

Další informace o přizpůsobení interakcí a toků zásad Azure AD B2C nad rámec toho, co je nabídnuto standardními zásadami B2C, naleznete v tématu [Vlastní zásady v Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundární správce

Nepovinný sekundární účet správce lze přidat do oddílu **Uživatelé** v klientovi B2C. Může se jednat o přímý nebo obecný účet. Potřebujete-li sdílet účet v prostředcích týmu, je možné také vytvořit běžný účet. Vzhledem k citlivosti dat uložených v Azure AD B2C je třeba společný účet pečlivě monitorovat dle bezpečnostních postupů společnosti.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md) Přidružení webu Dynamics 365 Commerce k online kanálu

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Konfigurace více klientů B2C v prostředí Commerce](configure-multi-B2C-tenants.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)
