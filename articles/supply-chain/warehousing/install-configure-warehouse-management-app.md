---
title: Instalace a připojení mobilní aplikace Warehouse Management
description: Toto téma vysvětluje, jak nainstalovat aplikaci Warehouse Management Mobile App z vašich mobilních zařízení a nakonfigurovat ji tak, aby se připojovala k vašemu prostředí Microsoft Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e93aff4914314ea99798415a0bacc7b844169bc2
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384604"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Instalace a připojení mobilní aplikace Warehouse Management

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Toto téma popisuje způsob konfigurace nové mobilní aplikace skladové aplikace Řízení skladu. Pokud hledáte informace o tom, jak nakonfigurovat starou aplikaci skladu (nyní zastaralou), přečtěte si téma [Instalace a připojení aplikace skladu](../../supply-chain/warehousing/install-configure-warehousing-app.md).

Toto téma vysvětluje, jak stáhnout a nainstalovat mobilní aplikaci Řízení skladu na každém z vašich mobilních zařízení, a jak konfigurovat její připojování k prostředí Supply Chain Management. Každé zařízení můžete nakonfigurovat ručně nebo můžete importovat nastavení připojení prostřednictvím souboru nebo naskenováním QR kódu.

## <a name="system-requirements"></a>Systémové požadavky

Warehouse Management Mobile App je k dispozici pro operační systémy Windows i Google Android. Chcete-li použít tuto aplikaci, musíte mít jeden z následujících podporovaných operačních systémů nainstalovaných v zařízení.

- Windows 10 (Universal Windows Platform \[UWP\]) říjen 2018 aktualizace 1809 (sestavení 10.0.17763) nebo novější
- Android 4.4 nebo novější

## <a name="turn-on-the-feature"></a>Zapnutí funkce

Než můžete použít aplikaci, musíte ve svém systému zapnout související funkci. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Uživatelská nastavení, ikony a názvy kroků pro novou aplikaci skladu*

## <a name="get-the-warehouse-management-mobile-app"></a>Získání mobilní aplikace pro správu skladu

U menších nasazení budete obvykle chtít instalovat aplikaci na každém zařízení z příslušného úložiště a poté ručně konfigurovat připojení k prostředím, která používáte.

U větších nasazení můžete automatizovat nasazení anebo konfiguraci, což může být pohodlnější, pokud spravujete mnoho zařízení. Můžete například použít řešení pro správu mobilních zařízení a mobilních aplikací, jako je [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Informace o tom, jak používat Intune k přidávání aplikací, naleznete v části [Přidání aplikací do Microsoft Intune](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Nainstalujte si aplikaci z obchodu s aplikacemi

Nejjednodušší způsob instalace aplikace na jednom zařízení je instalace z obchodu s aplikacemi, který vždy poskytuje nejnovější obecně dostupnou verzi. Microsoft Intune může také načítat aplikace z obchodů s aplikacemi. K instalaci aplikace z obchodu s aplikacemi použijte jeden z následujících odkazů:

- **Windows (UWP):** [Řízení skladu v Microsoft Storu](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Řízení skladu v obchodě Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Stažení aplikace z Microsoft App Center

Jako alternativu k instalaci z obchodu s aplikacemi si místo toho můžete aplikaci stáhnout z Microsoft App Center. App Center poskytuje instalovatelné balíčky, které můžete zkušebně načíst. Kromě aktuální verze vám App Center také umožňuje stáhnout předchozí verze a může poskytnout verze preview s chystanými funkcemi, které si můžete vyzkoušet. Chcete-li stáhnout aktuální, předchozí nebo preview verzi mobilní aplikace Řízení skladu z Microsoft App Center, použijte jeden z následujících odkazů:

- **Windows (UWP):** [Řízení skladu (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Pokyny k instalaci staženého balíčku na zařízení Windows a nastavení požadovaných certifikátů naleznete v tématu [Instalace sestavení z App Center](/appcenter/distribution/installation).

- **Android:** [Řízení skladu (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Jestliže si stáhnete verzi preview, je k její instalaci zapotřebí několik dalších kroků. Podrobnosti viz [Testování aplikací Android](/appcenter/distribution/testers/testing-android).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Vytvoření aplikace webové služby v Azure Active Directory

Pokud chcete povolit interakci aplikace Warehouse Management Mobile App s konkrétním serverem Supply Chain Management, je nutné zaregistrovat aplikaci webové služby pro klienta Supply Chain Management v Azure Active Directory (Azure AD). Následující postup ukazuje jeden způsob, jak dokončit tento úkol. Podrobné informace a alternativy naleznete v odkazech po postupu.

1. Přejděte ve webovém prohlížeči na [https://portal.azure.com](https://portal.azure.com/).
1. Zadejte jméno a heslo uživatele, kteří mají přístup k předplatnému Azure.
1. Na portálu Azure v levém navigačním podokně vyberte **Azure Active Directory**.

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Ujistěte se, že pracujete s instancí Azure AD, kterou používá Supply Chain Management.
1. V seznamu **Spravovat** zvolte **Registrace aplikací**.

    ![Registrace aplikací.](media/app-connect-azure-register.png "Registrace aplikací")

1. Na panelu nástrojů vyberte **Nová registrace** a otevřete průvodce **Zaregistrovat aplikaci**.
1. Zadejte název aplikace, vyberte možnost **Pouze účty v tomto organizačním adresáři** a poté zvolte **Registrovat**.

    ![Průvodce registrací aplikace.](media/app-connect-azure-register-wizard.png "Průvodce registrací aplikace")

1. Otevře se vaše nová registrace aplikace. Poznamenejte si hodnotu v poli **ID aplikace (klienta)**, protože ji budete potřebovat později. Na toto ID se budeme dále v tomto tématu odkazovat jako na *ID klienta*.

    ![ID aplikace (klienta).](media/app-connect-azure-app-id.png "ID aplikace (klienta)")

1. V seznamu **Spravovat** zvolte **Certifikát a tajné klíče**. Poté vyberte jedno z následujících tlačítek v závislosti na tom, jak chcete nakonfigurovat aplikaci pro ověřování. (Pro více informací viz [Ověření pomocí certifikátu nebo tajného klíče klienta](#authenticate) dále v tomto tématu.)

    - **Odeslat certifikát** – Odešlete certifikát, který chcete použít jako tajný klíč. Tento přístup doporučujeme, protože je bezpečnější a lze jej také zcela automatizovat. Pokud provozujete Warehouse Management mobile app na zařízeních Windows, poznamenejte si hodnota **Kryptografický otisk**, která se zobrazí po odeslání certifikátu. Tuto hodnotu budete potřebovat při konfiguraci certifikátu na zařízeních Windows.
    - **Nový tajný klíč klienta** – Vytvořte klíč zadáním popisu klíče a jeho délky trvání do části **Hesla** a poté vyberte **Přidat**. Vytvořte kopii klíče a bezpečně ji uložte.

    ![Certifikát a tajné klíče.](media/app-connect-azure-authentication.png "Certifikát a tajné klíče")

Další informace o nastavení aplikací webových služeb v Azure AD naleznete v následujících zdrojích:

- Pokyny, které ukazují, jak používat Windows PowerShell k nastavení aplikací webových služeb v Azure AD naleznete v části [Postup: Použití Azure PowerShell k vytvoření hlavní služby s certifikátem](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Úplné podrobnosti o tom, jak ručně vytvořit aplikaci webové služby Azure AD naleznete v následujících tématech:

    - [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](/azure/active-directory/develop/quickstart-register-app)
    - [Postup: Použití portálu k vytvoření aplikace Azure AD a hlavní služby, které mají přístup ke zdrojům](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Vytvoření a konfigurace uživatelských účtů v aplikaci Supply Chain Management

Chcete-li povolit Supply Chain Management pro použití vaší aplikace Azure AD, postupujte takto.

1. Vytvořte uživatele, který odpovídá pověření uživatele pro Warehouse Management mobile app:

    1. V aplikaci Supply Chain Management přejděte na **Správa systému \> Uživatelé \> Uživatelé**.
    1. Vytvořte uživatele.
    1. Přiřaďte uživatele skladového mobilního zařízení.

    ![Přiřaďte uživatele skladového mobilního zařízení.](media/app-connect-app-users.png "Přiřazení uživatele skladového mobilního zařízení")

1. Přidružte aplikaci Azure AD k uživateli Warehouse Management mobile app:

    1. Přejděte na **Správa systému \> Nastavení \> Aplikace Azure Active Directory**.
    1. Vytvořte řádek.
    1. Zadejte ID klienta, které jste si poznamenali v předchozí části, pojmenujte ho a vyberte právě vytvořeného uživatele. Doporučujeme označit všechna vaše zařízení. Pokud zařízení ztratíte, můžete z této stránky snadno odebrat přístup k aplikaci Supply Chain Management.

    ![Aplikace Azure Active Directory.](media/app-connect-aad-apps.png "Aplikace služby Azure Active Directory")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Ověření pomocí certifikátu nebo tajného klíče klienta

Ověřování pomocí Azure AD poskytuje bezpečný způsob připojení mobilního zařízení k Supply Chain Management. Ověřovat můžete pomocí tajného klíče klienta nebo certifikátu. Pokud importujete nastavení připojení, doporučujeme použít certifikát místo tajného klíče klienta. Protože tajný klíč klienta musí být vždy bezpečně uložen, nemůžete ho importovat ze souboru nastavení připojení nebo z QR kódu, jak je popsáno dále v tomto tématu.

Certifikáty mohou být použity jako tajné klíče k prokázání identity aplikace, když je požadován token. Veřejná část certifikátu je nahrána do registrace aplikace na portálu Azure, zatímco úplný certifikát musí být nasazen na každém zařízení, na kterém je Warehouse Management mobile app nainstalovaná. Vaše organizace odpovídá za správu certifikátu z hlediska rotace atd. Můžete použít certifikáty s vlastním podpisem, ale vždy byste měli používat neexportovatelné certifikáty.

Certifikát musíte zpřístupnit lokálně na každém zařízení, na kterém spouštíte Warehouse Management mobile app. Informace o tom, jak spravovat certifikáty pro zařízení řízená aplikací Intune, pokud používáte Intune, naleznete v části [Použití certifikátů pro ověření v Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Konfigurace aplikace importem nastavení připojení

Chcete-li usnadnit údržbu a nasazení aplikace na mnoha mobilních zařízeních, můžete importovat nastavení připojení namísto jejich ručního zadávání do každého zařízení. Tato část vysvětluje, jak vytvořit a importovat nastavení.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Vytvoření souboru nastavení připojení nebo QR kódu

Nastavení připojení můžete importovat ze souboru nebo z QR kódu. Pro oba přístupy musíte nejprve vytvořit soubor nastavení, který používá formát a syntaxi JavaScript Object Notation (JSON). Soubor musí zahrnovat seznam připojení, který obsahuje jednotlivá připojení, která je třeba přidat. Následující tabulka shrnuje parametry, které musíte zadat v souboru nastavení připojení.

| Parametr | popis |
|---|---|
| ConnectionName | Zadejte název nastavení připojení. Maximální délka je 20 znaků. Protože je tato hodnota jedinečným identifikátorem nastavení připojení, ujistěte se, že je v seznamu jedinečná. Pokud v zařízení již existuje připojení se stejným názvem, bude toto nastavení přepsáno z importovaného souboru. |
| ActiveDirectoryClientAppId | Určete ID klienta, které jste si poznamenali při nastavování Azure AD v části [Vytvoření aplikaci webové služby v Azure Active Directory](#create-service). |
| ActiveDirectoryResource | Zadejte kořenovou adresu URL aplikace Supply Chain Management. |
| ActiveDirectoryTenant | Určete název domény Azure AD, kterou používáte se serverem Supply Chain Management. Tato hodnota má tvar `https://login.windows.net/<your-Azure-AD-domain-name>`. Zde je příklad: `https://login.windows.net/contosooperations.onmicrosoft.com`. Další informace o tom, jak najít název domény Azure AD najdete v části [Vyhledání důležitých ID pro uživatele](/partner-center/find-ids-and-domain-names). |
| Společnost | Zadejte právnickou osobu v aplikaci Supply Chain Management, ke které se má aplikace připojovat. |
| Typ připojení | (Volitelné) Určete, zda by nastavení připojení mělo používat certifikát nebo tajný klíč klienta pro připojení k prostředí. Platné hodnoty jsou *"certificate"* a *"clientsecret"*. Výchozí hodnota je *"certificate"*.<p>**Poznámka:** Tajné klíče klienta nelze importovat.</p> |
| IsEditable | (Volitelné) Určete, zda by měl mít uživatel aplikace možnost upravit nastavení připojení. Platné hodnoty jsou *"true"* a *"false"*. Výchozí hodnota je *"true"*. |
| IsDefault | (Volitelné) Určete, zda je připojení výchozím připojením. Připojení, které je nastaveno jako výchozí připojení, bude při otevření aplikace automaticky předvybráno. Jako výchozí připojení lze nastavit pouze jedno připojení. Platné hodnoty jsou *"true"* a *"false"*. Výchozí hodnota je *"false"*. |
| CertificateThumbprint | (Volitelné) U zařízení Windows můžete zadat pro připojení kryptografický otisk certifikátu. Pro Android zařízení musí uživatel aplikace vybrat certifikát při prvním použití připojení. |

Následující příklad ukazuje platný soubor nastavení připojení, který obsahuje dvě připojení. Jak vidíte, seznam připojení (pojmenovaný *"ConnectionList"* v souboru) je objekt s polem, které ukládá každé připojení jako objekt. Každý objekt musí být uzavřen ve složených závorkách ({}) a oddělen čárkami a pole musí být uzavřeno v hranatých závorkách (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Můžete buď uložit informace jako soubor JSON, nebo vygenerovat QR kód, který má stejný obsah. Pokud informace uložíte jako soubor, doporučujeme ho uložit pomocí výchozího názvu, *connection.json*, zejména pokud ho uložíte ve výchozím umístění na každém mobilním zařízení.

### <a name="save-the-connection-settings-file-on-each-device"></a>Uložení souboru nastavení připojení na každém zařízení

Obvykle použijete nástroj nebo skript pro správu zařízení k distribuci souborů nastavení připojení do každého spravovaného zařízení. Pokud použijete výchozí název a umístění při uložení souboru nastavení připojení na každém zařízení, Warehouse Management mobile app jej automaticky importuje, a to i při prvním spuštění po instalaci aplikace. Pokud pro soubor používáte vlastní název nebo umístění, musí uživatel aplikace při prvním spuštění zadat hodnoty. Aplikace však bude i nadále používat zadaný název a umístění.

Při každém spuštění aplikace se znovu importuje nastavení připojení ze svého předchozího umístění a určí, zda došlo ke změnám. Aplikace aktualizuje pouze připojení, která mají stejné názvy jako připojení v souboru nastavení připojení. Uživatelem vytvořená připojení, která používají jiné názvy, nebudou aktualizována.

Připojení nelze odstranit pomocí souboru nastavení připojení.

Jak již bylo zmíněno, výchozí název souboru je *connection.json*. Výchozí umístění souboru závisí na tom, zda používáte zařízení se systémem Windows nebo Android:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Cesty se obvykle vytvoří automaticky po prvním spuštění aplikace. Můžete je však vytvořit ručně, pokud musíte před instalací přenést soubor nastavení připojení do zařízení.

> [!NOTE]
> Pokud je aplikace odinstalována, bude odstraněna výchozí cesta a její obsah.

### <a name="import-the-connection-settings"></a>Import nastavení připojení

Chcete-li importovat nastavení připojení ze souboru nebo z QR kódu, postupujte takto.

1. Spusťte na svém mobilním zařízení mobilní aplikaci Warehouse Management mobile app. Při prvním spuštění aplikace se zobrazí uvítací zpráva. Vyberte **Vybrat připojení**.

    ![Uvítací zpráva.](media/app-configure-welcome-screen.png "Uvítací zpráva")

1. Pokud importujete nastavení připojení ze souboru, aplikace již mohla soubor najít, pokud byl při uložení použit výchozí název a výchozí umístění. V takovém případě přeskočte na krok 4. Jinak vyberte **Nastavení připojení** a poté pokračujte krokem 3.

    ![Nastavení připojení.](media/app-configure-set-up-connection.png "Nastavení připojení")

1. V dialogovém okně **Nastavení připojení** vyberte **Přidat ze souboru** nebo **Přidat z QR kódu**, podle toho, jak chcete importovat nastavení:

    - Pokud importujete nastavení připojení ze souboru, vyberte **Přidat ze souboru**, přejděte na soubor v místním zařízení a vyberte jej. Pokud vyberete vlastní umístění, aplikace ho uloží a při příštím použití ho automaticky použije.
    - Pokud importujete nastavení připojení skenováním QR kódu, vyberte **Přidat z QR kódu**. Aplikace vás vyzve k povolení pro použití fotoaparátu zařízení. Po udělení povolení se fotoaparát spustí, takže ho můžete použít ke skenování. V závislosti na kvalitě fotoaparátu zařízení a složitosti QR kódu může být obtížné získat správný sken. V takovém případě zkuste snížit složitost QR kódu generováním pouze jednoho připojení na QR kód. (V současné době můžete ke skenování QR kódu použít pouze fotoaparát zařízení.)

    ![Nabídka nastavení připojení.](media/app-configure-connection-setup-flyout.png "Nabídka nastavení připojení")

1. Po úspěšném načtení nastavení připojení se zobrazí vybrané připojení.

    ![Nastavení připojení načteno.](media/app-configure-select-connection.png "Nastavení připojení načteno")

1. Pokud používáte Android zařízení a k ověření certifikát, zařízení vás vyzve k výběru certifikátu.

    ![Výzva k výběru certifikátu na zařízení Android.](media/app-configure-select-certificate.png "Výzva k výběru certifikátu na zařízení Android")

1. Aplikace se připojí k serveru Supply Chain Management a zobrazí přihlašovací stránku.

    ![Přihlašovací stránka.](media/app-configure-sign-in-page.png "Přihlašovací stránka")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Ruční konfigurace aplikace

Pokud nemáte soubor nebo QR kód, můžete aplikaci na zařízení nakonfigurovat ručně, aby se připojovala k serveru Supply Chain Management prostřednictvím aplikace Azure AD.

1. Spusťte na svém mobilním zařízení mobilní aplikaci Warehouse Management mobile app.
1. Pokud je aplikace spuštěna v **demo režimu**, vyberte **Nastavení připojení**. Pokud se při spuštění aplikace zobrazí stránka **Přihlásit**, vyberte **Změnit připojení**.
1. Vyberte **Nastavit připojení**.

    ![Nastavení připojení.](media/app-configure-set-up-connection.png "Nastavení připojení")

1. Vyberte **Zadat ručně**.

    ![Nabídka nastavení připojení.](media/app-configure-connection-setup-flyout.png "Nabídka nastavení připojení")

    Zobrazí se stránka **Nové připojení** a ukazuje nastavení, která jsou vyžadována pro ruční zadání podrobností o připojení.

    ![Pole pro ruční připojení.](media/app-configure-input-manually.png "Pole pro ruční připojení")

1. Zadejte následující informace:

    - **Použít tajný klíč klienta** - Nastavte tuto možnost na _Ano_ k použití tajného klíče klienta k ověření pomocí Supply Chain Management. Nastavte možnost na _Ne_ pro použití certifikátu k ověření. (Další informace viz [Vytvoření aplikace webové služby v Azure Active Directory](#create-service) dříve v tomto tématu.)
    - **Název připojení** - Zadejte název nového připojení. Toto jméno se objeví v poli **Vybrat připojení** při příštím otevření nastavení připojení. Název, který zadáte, musí být jedinečný: (Jinými slovy, musí se lišit od všech ostatních názvů připojení, které jsou uloženy v zařízení, jsou-li tam uloženy jiné názvy připojení.)
    - **ID klienta Active Directory** – Zadejte ID klienta, které jste si poznamenali při nastavování Azure AD v části Vytvoření aplikaci webové služby v [Azure Active Directory](#create-service).
    - **Tajný klíč klienta Active Directory** - Toto pole je k dispozici, pouze pokud je možnost **Použít tajný klíč klienta** nastavena na _Ano_. Zadejte tajný klíč klienta, které jste si poznamenali při nastavování Azure AD v části [Vytvoření aplikaci webové služby v Azure Active Directory](#create-service).
    - **Kryptografický otisk certifikátu Active Directory** - Toto pole je k dispozici jenom pro zařízení Windows, pouze pokud je možnost **Použít tajný klíč klienta** nastavena na _Ne_. Zadejte kryptografický otisk certifikátu, které jste si poznamenali při nastavování Azure AD v části [Vytvoření aplikaci webové služby v Azure Active Directory](#create-service).
    - **Zdroj Active Directory** - Určete kořenovou adresu URL aplikace Supply Chain Management.

        > [!IMPORTANT]
        > Neukončujte tuto hodnotu lomítkem (/).

    - **Tenant Active Directory** – Zadejte název domény Azure AD, kterou používáte se serverem Supply Chain Management. Tato hodnota má tvar `https://login.windows.net/<your-Azure-AD-domain-name>`. Zde je příklad: `https://login.windows.net/contosooperations.onmicrosoft.com`. Další informace o tom, jak najít název domény Azure AD najdete v části [Vyhledání důležitých ID pro uživatele](/partner-center/find-ids-and-domain-names).

        > [!IMPORTANT]
        > Neukončujte tuto hodnotu lomítkem (/).

    - **Společnost** – Zadejte právnickou osobu (společnost) v aplikaci Supply Chain Management, ke které se má aplikace připojovat.

1. Zvolte tlačítko **Uložit** v pravém horním rohu stránky.
1. Pokud používáte Android zařízení a k ověření certifikát, zařízení vás vyzve k výběru certifikátu.
1. Aplikace se připojí k serveru Supply Chain Management a zobrazí přihlašovací stránku.

## <a name="remove-access-for-a-device"></a>Odebrání přístupu k zařízení

Ztraceným nebo narušeným zařízením je nutné odebrat přístup k aplikaci Supply Chain Management. Následující kroky popisují doporučený postup odebrání přístupu.

1. Přejděte na **Správa systému \> Nastavení \> Aplikace Azure Active Directory**.
1. Odstraň řádek, který odpovídá zařízení, kterému chcete odebrat přístup. Poznamenejte si ID klienta, které se používá pro zařízení, protože ho budete potřebovat později.

    Pokud jste zaregistrovali pouze jedno ID klienta a více zařízení používá stejné ID klienta, musíte do těchto zařízení odeslat nová nastavení připojení. Jinak ztratí přístup.

1. Přihlaste se do portálu Azure na [https://portal.azure.com](https://portal.azure.com/).
1. V levém navigačním podokně vyberte možnost **Active Directory** a ujistěte se, že jste ve správném adresáři.
1. V seznamu **Spravovat** zvolte **Registrace aplikací** a zvolte aplikaci, kterou chcete konfigurovat. Zobrazí se stránka **Nastavení** s informacemi o konfiguraci.
1. Ujistěte se, že ID klienta aplikace odpovídá ID klienta, které jste si poznamenali v kroku 2.
1. Na panelu nástrojů vyberte **Odstranit**.
1. V zobrazené zprávě s potvrzením vyberte **Ano**.

## <a name="additional-resources"></a>Další prostředky

- [Uživatelská nastavení mobilního zařízení](mobile-device-user-settings.md)
- [Přiřaďte ikony kroků a názvy pro mobilní aplikaci Warehouse Management](step-icons-titles.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
