---
title: Instalace a připojení aplikace skladu
description: Tento článek vysvětluje, jak nainstalovat aplikaci skladu na každém z vašich mobilních zařízení a nakonfigurovat ji tak, aby se připojovala k vašemu prostředí Microsoft Dynamics 365 Supply Chain Management. Každé zařízení můžete nakonfigurovat ručně nebo můžete importovat nastavení připojení prostřednictvím souboru nebo naskenováním QR kódu.
author: Mirzaab
ms.date: 05/25/2020
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
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8ed770e45aa7f9909b98a92b493dd2931c6a3981
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885747"
---
# <a name="install-and-connect-the-warehouse-app"></a>Instalace a připojení aplikace skladu

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tento článek popisuje, jak nakonfigurovat starou aplikaci skladu (která je nyní zastaralá). Pokud hledáte informace o tom, jak konfigurovat novou mobilní aplikaci Řízení skladu, pročtěte si téma [Instalace a připojení mobilní aplikace Řízení skladu](install-configure-warehouse-management-app.md).

> [!NOTE]
> Tento článek popisuje způsob konfigurace skladové aplikace pro nasazení v cloudu. Postup konfigurace skladové aplikace pro místní nasazení naleznete v tématu [Sklady pro místní nasazení](../../fin-ops-core/dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Aplikace skladu je k dispozici v obchodech Google Play a Microsoft Store. Poskytuje se jako samostatná komponenta. Proto ji musíte stáhnout do každého zařízení a poté ji nakonfigurovat pro připojení k prostředí Microsoft Dynamics 365 Supply Chain Management.

Tento článek vysvětluje, jak nainstalovat aplikaci skladu na každém z vašich mobilních zařízení a nakonfigurovat ji tak, aby se připojovala k vašemu prostředí Supply Chain Management. Každé zařízení můžete nakonfigurovat ručně nebo můžete importovat nastavení připojení prostřednictvím souboru nebo naskenováním QR kódu.

## <a name="system-requirements"></a>Systémové požadavky

Aplikace skladu je k dispozici pro operační systémy Android a Windows. Chcete-li použít nejnovější verzi aplikaci, musíte mít jeden z následujících podporovaných operačních systémů nainstalovaných v mobilním zařízení.

- Windows 10 (Universal Windows Platform \[UWP\]) Podzim, aktualizace tvůrců 1709 (sestavení 10.0.16299) nebo novější
- Android 4.4 nebo novější

> [!NOTE]
> Pokud musíte podporovat starší zařízení Windows, která nemohou spouštět nejnovější verzi systému Windows, můžete si stále stáhnout verzi 1.6.3.0 aplikace skladu z obchodu Microsoft Store. Tato verze bude spuštěna v systému Windows 10 (UWP) Listopad, Update 1511 (sestavení 10.0.10586) nebo novější. Mějte však na paměti, že tato verze aplikace skladu nepodporuje hromadné nasazení nastavení připojení. Proto musíte [ručně nakonfigurovat připojení](#config-manually) na každém zařízení, na kterém běží tato verze aplikace.

## <a name="get-the-warehouse-app"></a>Získání aplikace skladu

Ke stažení aplikace použijte jeden z následujících odkazů:

- **Windows (UWP):** [Dynamics 365 for Finance and Operations - Sklady v obchodě Microsoft Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Sklady - Dynamics 365 v obchodě Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

U menších nasazení můžete chtít nainstalovat aplikaci z příslušného úložiště na každém zařízení a poté ručně nakonfigurovat připojení k prostředím, která používáte. Ve verzi 1.7.0.0 a novější aplikace skladu však můžete také automatizovat nasazení anebo konfiguraci aplikace. Tento přístup může být vhodný, pokud spravujete mnoho zařízení a používáte řešení pro správu mobilních zařízení a správu mobilních aplikací, například [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Informace o tom, jak používat Intune k přidávání aplikací, naleznete v části [Přidání aplikací do Microsoft Intune](/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Vytvoření aplikace webové služby v Azure Active Directory

Pokud chcete povolit interakci aplikace skladu s konkrétním serverem Supply Chain Management, je nutné zaregistrovat aplikaci webové služby pro klienta Supply Chain Management v Azure Active Directory (Azure AD). Následující postup ukazuje jeden způsob, jak dokončit tento úkol. Podrobné informace a alternativy naleznete v odkazech po postupu.

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

1. Otevře se vaše nová registrace aplikace. Poznamenejte si hodnotu v poli **ID aplikace (klienta)**, protože ji budete potřebovat později. Na toto ID se budeme dále v tomto článku odkazovat jako na *ID klienta*.

    ![ID aplikace (klienta).](media/app-connect-azure-app-id.png "ID aplikace (klienta)")

1. V seznamu **Spravovat** zvolte **Certifikát a tajné klíče**. Poté vyberte jedno z následujících tlačítek v závislosti na tom, jak chcete nakonfigurovat aplikaci pro ověřování. (Pro více informací viz [Ověření pomocí certifikátu nebo tajného klíče klienta](#authenticate) dále v tomto článku.)

    - **Odeslat certifikát** – Odešlete certifikát, který chcete použít jako tajný klíč. Tento přístup doporučujeme, protože je bezpečnější a lze jej také zcela automatizovat. Pokud provozujete aplikaci skladu na zařízeních Windows, poznamenejte si hodnota **Kryptografický otisk**, která se zobrazí po odeslání certifikátu. Tuto hodnotu budete potřebovat při konfiguraci certifikátu na zařízeních Windows.
    - **Nový tajný klíč klienta** – Vytvořte klíč zadáním popisu klíče a jeho délky trvání do části **Hesla** a poté vyberte **Přidat**. Vytvořte kopii klíče a bezpečně ji uložte.

    ![Certifikát a tajné klíče.](media/app-connect-azure-authentication.png "Certifikát a tajné klíče")

Další informace o nastavení aplikací webových služeb v Azure AD naleznete v následujících zdrojích:

- Pokyny, které ukazují, jak používat Windows PowerShell k nastavení aplikací webových služeb v Azure AD naleznete v části [Postup: Použití Azure PowerShell k vytvoření hlavní služby s certifikátem](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Úplné podrobnosti o tom, jak ručně vytvořit aplikaci webové služby Azure AD naleznete v následujících článcích:

    - [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](/azure/active-directory/develop/quickstart-register-app)
    - [Postup: Použití portálu k vytvoření aplikace Azure AD a hlavní služby, které mají přístup ke zdrojům](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Vytvoření a konfigurace uživatelských účtů v aplikaci Supply Chain Management

Chcete-li povolit Supply Chain Management pro použití vaší aplikace Azure AD, postupujte takto.

1. Vytvořte uživatele, který odpovídá pověření uživatele pro aplikaci skladu:

    1. V aplikaci Supply Chain Management přejděte na **Správa systému \> Uživatelé \> Uživatelé**.
    1. Vytvořte uživatele.
    1. Přiřaďte uživatele skladového mobilního zařízení.

    ![Přiřaďte uživatele skladového mobilního zařízení.](media/app-connect-app-users.png "Přiřazení uživatele skladového mobilního zařízení")

1. Přidružte aplikaci Azure AD k uživateli aplikace skladu:

    1. Přejděte na **Správa systému \> Nastavení \> Aplikace Azure Active Directory**.
    1. Vytvořte řádek.
    1. Zadejte ID klienta, které jste si poznamenali v předchozí části, pojmenujte ho a vyberte právě vytvořeného uživatele. Doporučujeme označit všechna vaše zařízení. Pokud je ztratíte, můžete z této stránky snadno odebrat přístup k aplikaci Supply Chain Management.

    ![Aplikace Azure Active Directory.](media/app-connect-aad-apps.png "Aplikace služby Azure Active Directory")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Ověření pomocí certifikátu nebo tajného klíče klienta

Ověřování pomocí Azure AD poskytuje bezpečný způsob připojení mobilního zařízení k Supply Chain Management. Ověřovat můžete pomocí tajného klíče klienta nebo certifikátu. Pokud importujete nastavení připojení, doporučujeme použít certifikát místo tajného klíče klienta. Protože tajný klíč klienta musí být vždy bezpečně uložen, nemůžete ho importovat ze souboru nastavení připojení nebo z QR kódu, jak je popsáno dále v tomto článku.

Certifikáty mohou být použity jako tajné klíče k prokázání identity aplikace, když je požadován token. Veřejná část certifikátu je nahrána do registrace aplikace na portálu Azure, zatímco úplný certifikát musí být nasazen na každém zařízení, na kterém je aplikace skladu nainstalovaná. Vaše organizace odpovídá za správu certifikátu z hlediska rotace atd. Můžete použít certifikáty s vlastním podpisem, ale vždy byste měli používat neexportovatelné certifikáty.

Certifikát musíte zpřístupnit lokálně na každém zařízení, na kterém spouštíte aplikaci skladu. Informace o tom, jak spravovat certifikáty pro zařízení řízená aplikací Intune, pokud používáte Intune, naleznete v části [Použití certifikátů pro ověření v Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Konfigurace aplikace importem nastavení připojení

Chcete-li usnadnit údržbu a nasazení aplikace na mnoha mobilních zařízeních, můžete importovat nastavení připojení namísto jejich ručního zadávání do každého zařízení. Tato část vysvětluje, jak vytvořit a importovat nastavení.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Vytvoření souboru nastavení připojení nebo QR kódu

Nastavení připojení můžete importovat ze souboru nebo z QR kódu. Pro oba přístupy musíte nejprve vytvořit soubor nastavení, který používá formát a syntaxi JavaScript Object Notation (JSON). Soubor musí zahrnovat seznam připojení, který obsahuje jednotlivá připojení, která je třeba přidat. Následující tabulka shrnuje parametry, které musíte zadat v souboru nastavení připojení.

| Parametr | popis |
| --- | --- |
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

Obvykle použijete nástroj nebo skript pro správu zařízení k distribuci souborů nastavení připojení do každého spravovaného zařízení. Pokud použijete výchozí název a umístění při uložení souboru nastavení připojení na každém zařízení, aplikace skladu jej automaticky importuje, a to i při prvním spuštění po instalaci aplikace. Pokud pro soubor používáte vlastní název nebo umístění, musí uživatel aplikace při prvním spuštění zadat hodnoty. Aplikace však bude i nadále používat zadaný název a umístění.

Při každém spuštění aplikace se znovu importuje nastavení připojení ze svého předchozího umístění a určí, zda došlo ke změnám. Aplikace aktualizuje pouze připojení, která mají stejné názvy jako připojení v souboru nastavení připojení. Uživatelem vytvořená připojení, která používají jiné názvy, nebudou aktualizována.

Připojení nelze odstranit pomocí souboru nastavení připojení.

Jak již bylo zmíněno, výchozí název souboru je *connection.json*. Výchozí umístění souboru závisí na tom, zda používáte zařízení se systémem Windows nebo Android:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Cesty se obvykle vytvoří automaticky po prvním spuštění aplikace. Můžete je však vytvořit ručně, pokud musíte před instalací přenést soubor nastavení připojení do zařízení.

> [!NOTE]
> Pokud je aplikace odinstalována, bude odstraněna výchozí cesta a její obsah.

### <a name="import-the-connection-settings"></a>Import nastavení připojení

Chcete-li importovat nastavení připojení ze souboru nebo z QR kódu, postupujte takto.

1. Otevřete aplikaci skladu na svém mobilním zařízení.
1. Přejděte na **Nastavení připojení**.
1. Nastavte možnost **Použít ukázkový režim** na _Ne_.

    ![Použití možnosti ukázkového režimu.](media/app-connect-app-demo-mode.png "Použití možnosti ukázkového režimu")

1. Vyberte **Zvolit soubor** nebo **Naskenovat QR kód**, v závislosti na tom, jak chcete nastavení importovat:

    - Pokud importujete nastavení připojení ze souboru, aplikace již mohla soubor najít, pokud byl při uložení použit výchozí název a výchozí umístění. Jinak vyberte **Zvolit soubor**, vyhledejte soubor na místním zařízení a vyberte ho. Pokud vyberete vlastní umístění, aplikace ho uloží a při příštím použití ho automaticky použije.
    - Pokud importujete nastavení připojení skenováním QR kódu, vyberte **Skenovat QR kód**. Aplikace vás vyzve k povolení pro použití fotoaparátu zařízení. Po udělení povolení se fotoaparát spustí, takže ho můžete použít ke skenování. V závislosti na kvalitě fotoaparátu zařízení a složitosti QR kódu může být obtížné získat správný sken. V takovém případě zkuste snížit složitost QR kódu generováním pouze jednoho připojení na QR kód. (V současné době můžete ke skenování QR kódu použít pouze fotoaparát zařízení.)

    ![Import nastavení připojení.](media/app-connect-app-select-file.png "Import nastavení připojení")

1. Po úspěšném načtení nastavení připojení vyberte **Zpět** (šipka vlevo) v levém horním rohu stránky.

    ![Nastavení připojení načteno.](media/app-connect-app-settings-loaded.png "Nastavení připojení načteno")

1. Pokud používáte Android zařízení a k ověření certifikát, zařízení vás vyzve k výběru certifikátu.

    ![Výzva k výběru k certifikátu na zařízení Android.](media/app-connect-app-choose-cert.png "Výzva k výběru k certifikátu na zařízení Android")

1. Aplikace se připojí k serveru Supply Chain Management a zobrazí přihlašovací stránku.

    ![Přihlašovací stránka.](media/app-connect-sign-in.png "Přihlašovací stránka")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Ruční konfigurace aplikace

Aplikaci můžete nakonfigurovat na zařízení ručně, aby se připojovala k serveru Supply Chain Management prostřednictvím aplikace Azure AD.

1. Otevřete aplikaci skladu na svém mobilním zařízení.
1. Přejděte na **Nastavení připojení**.
1. Nastavte možnost **Použít ukázkový režim** na _Ne_.

    ![Ukázkový režim vypnutý.](media/app-connect-app-select-file.png "Ukázkový režim vypnutý")

1. Klepněte na pole **Vybrat připojení** pro rozbalení nastavení, která jsou vyžadována pro ruční zadání podrobností o připojení.

    ![Pole pro ruční připojení.](media/app-connect-manual-connect.png "Pole pro ruční připojení")

1. Zadejte následující informace:

    - **Použít tajný klíč klienta** - Nastavte tuto možnost na _Ano_ k použití tajného klíče klienta k ověření pomocí Supply Chain Management. Nastavte možnost na _Ne_ pro použití certifikátu k ověření. (Více informací naleznete v části [Vytvoření aplikace webových služeb v Azure Active Directory](#create-service) .)
    - **Název připojení** - Zadejte název nového připojení. Toto jméno se objeví v poli **Vybrat připojení** při příštím otevření nastavení připojení. Název, který zadáte, musí být jedinečný: (Jinými slovy, musí se lišit od všech ostatních názvů připojení, které jsou uloženy v zařízení, jsou-li tam uloženy jiné názvy připojení.)
    - **ID klienta Active Directory** – Zadejte ID klienta, které jste si poznamenali při nastavování Azure AD v části Vytvoření aplikaci webové služby v [Azure Active Directory](#create-service).
    - **Tajný klíč klienta Active Directory** - Toto pole je k dispozici, pouze pokud je možnost **Použít tajný klíč klienta** nastavena na _Ano_. Zadejte tajný klíč klienta, které jste si poznamenali při nastavování Azure AD v části [Vytvoření aplikaci webové služby v Azure Active Directory](#create-service).
    - **Kryptografický otisk certifikátu Active Directory** - Toto pole je k dispozici pro zařízení Windows, pouze pokud je možnost **Použít tajný klíč klienta** nastavena na _Ne_. Zadejte kryptografický otisk certifikátu, které jste si poznamenali při nastavování Azure AD v části [Vytvoření aplikaci webové služby v Azure Active Directory](#create-service).
    - **Zdroj Active Directory** - Určete kořenovou adresu URL aplikace Supply Chain Management.

        > [!NOTE]
        > Neukončujte tuto hodnotu lomítkem (/).

    - **Tenant Active Directory** – Zadejte název domény Azure AD, kterou používáte se serverem Supply Chain Management. Tato hodnota má tvar `https://login.windows.net/<your-Azure-AD-domain-name>`. Zde je příklad: `https://login.windows.net/contosooperations.onmicrosoft.com`. Další informace o tom, jak najít název domény Azure AD najdete v části [Vyhledání důležitých ID pro uživatele](/partner-center/find-ids-and-domain-names).

        > [!NOTE]
        > Neukončujte tuto hodnotu lomítkem (/).

    - **Společnost** – Zadejte právnickou osobu v aplikaci Supply Chain Management, ke které se má aplikace připojovat.

1. Zvolte tlačítko **Uložit** v pravém horním rohu stránky.
1. Pokud používáte Android zařízení a k ověření certifikát, zařízení vás vyzve k výběru certifikátu.
1. Aplikace se připojí k serveru Supply Chain Management a zobrazí přihlašovací stránku.

## <a name="remove-access-for-a-device"></a>Odebrání přístupu k zařízení

Ztraceným nebo narušeným zařízením je nutné odebrat přístup k aplikaci Supply Chain Management. Následující kroky popisují doporučený postup odebrání přístupu.

1. Přejděte na **Správa systému \> Nastavení \> Aplikace Azure Active Directory**.
1. Odstraň řádek, který odpovídá zařízení, kterému chcete odebrat přístup. Poznamenejte si ID klienta, které se používá pro odebrané zařízení, protože ho budete potřebovat později.

    Pokud jste zaregistrovali pouze jedno ID klienta a více zařízení používá stejné ID klienta, musíte do těchto zařízení odeslat nová nastavení připojení. Jinak ztratí přístup.

1. Přihlaste se do portálu Azure na [https://portal.azure.com](https://portal.azure.com/).
1. V levém navigačním podokně vyberte možnost **Active Directory** a ujistěte se, že jste ve správném adresáři.
1. V seznamu **Spravovat** zvolte **Registrace aplikací** a zvolte aplikaci, kterou chcete konfigurovat. Zobrazí se stránka **Nastavení** s informacemi o konfiguraci.
1. Ujistěte se, že ID klienta aplikace odpovídá ID klienta, které jste si poznamenali v kroku 2.
1. Na panelu nástrojů vyberte **Odstranit**.
1. V zobrazené zprávě s potvrzením vyberte **Ano**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
