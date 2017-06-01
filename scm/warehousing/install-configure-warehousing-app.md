---
title: "Instalace a konfigurace aplikace Microsoft Dynamics 365 for Operations – Warehousing"
description: "Toto téma popisuje, jak nainstalovat a nakonfigurovat Microsoft Dynamics 365 for Operations - Warehousing."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46b4809ae89f90295766e95ce78a8f019de0cdae
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Instalace a konfigurace aplikace Microsoft Dynamics 365 for Operations – Warehousing

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak nainstalovat a nakonfigurovat Microsoft Dynamics 365 for Operations - Warehousing.

Dynamics 365 for Operations - Warehousing je aplikace, která je k dispozici v Google Play Store a Windows Store. Pro aktuální verzi aplikace Microsoft Dynamics 365 pro operace je tato aplikace k dispozici jako samostatná komponenty, což znamená samostatné nasazení na zařízeních pro činnosti skladu. Pomocí aplikace pro prostředí operací v prostředí Dynamics 365 for Operations je nutné stáhnout aplikaci na každé zařízení a nakonfigurovat jej pro připojení k prostředí Dynamics 365 for Operations. Toto téma popisuje, jak nainstalovat aplikace na vašem zařízení. Také vysvětluje, jak nakonfigurovat aplikace pro připojení k prostředí Dynamics 365 for Operations.

## <a name="prerequisites"></a>Předpoklady
Aplikace je k dispozici v operačních systémech Android a Windows. Chcete-li použít tuto aplikaci, musíte mít jeden z následujících podporovaných operačních systémů nainstalovaných v zařízení. Také musíte mít jednu z následujících podporovaných verzí Dynamics 365 for Operations. Pomocí informací v následující tabulce určete, zda je vaše hardwarové a softwarové prostředí připraveno pro podporu instalace.

| Platforma                    | Verze                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (všechny verze)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations verze 1611 nebo klient Microsoft Dynamics Dynamics AX version 7.0/7.0.1 a aktualizace Microsoft Dynamics AX platform 2 s opravou hotfix KB 3210014 |

## <a name="get-the-app"></a>Získat aplikaci
-   Windows (UWP) - [Dynamics 365 for Operations - Warehousing ve Windows Storu](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Warehousing v Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Vytvoření aplikace webové služby ve službě Active Directory
Pokud chcete povolit interakci aplikace s konkrétním serverem Dynamics 365 for Operations, musíte zaregistrovat aplikaci webové služby do klienta Azure Active Directory pro Dynamics 365 for Operations. Z bezpečnostních důvodů doporučujeme vytvořit webovou aplikaci služby pro každé zařízení, které používáte. Chcete-li vytvořit webovou aplikaci služby ve službě Active Directory Azure (Azure AD), proveďte následující kroky:

1.  Ve webovém prohlížeči přejděte na <https://manage.windowsazure.com>.
2.  Zadejte jméno a heslo pro uživatele, kteří mají přístup k předplatnému Azure.
3.  V portálu Azure v levém navigačním podokně klepněte na **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  V mřížce vyberte instanci služby Active Directory používanou aplikací Dynamics 365 for Operations.
5.  Na horním panelu nástrojů klepněte na tlačítko **Aplikace**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  V dolním podokně klikněte na **Přidat**. Spustí se průvodce **Přidat aplikaci**.
7.  Zadejte název aplikace a vyberte **Webová aplikace nebo webové rozhraní API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Zadejte URL přihlášení, což je adresa URL aplikace v klientovi, kořenová adresa URL operace. Adresa URL přihlášení není aktuálně aktivně používána při ověřování aplikace, ale je to povinné pole. Zadejte stejnou adresu URL do pole App ID URI. [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Přejděte na kartu **Konfigurace**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Přejděte dolů, dokud se nezobrazí oddíl **Oprávnění pro ostatní aplikace**. Klikněte na **Přidat aplikaci**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. V seznamu vyberte **Microsoft Dynamics ERP**. Klepněte na tlačítko **Dokončit kontrolu** v pravém horním rohu stránky. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. V seznamu **Delegovat oprávnění** zaškrtněte všechna políčka. Klikněte na možnost **Uložit**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Poznamenejte si následující informace:
    -   **ID klienta** - při posouvání nahoru na stránku se zobrazí **ID klienta**.
    -   **Klíč** - v oddílu **klíče** vytvořte klíč výběrem doby trvání a zkopírováním klíče. Tento klíč bude později označován jako **tajný klíč klienta**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Vytvoření a konfigurace uživatelských účtů v Dynamics 365 for Operations
Pro povolení aplikaci Dynamics 365 for Operations používat vaši aplikaci Azure AD je nutné dokončit následující kroky konfigurace:

1.  Ve službě Azure Active Directory pro aplikaci Dynamics 365 for Operations vytvořte nový uživatelský účet. Účelem tohoto uživatelského účtu je přístup ke konkrétní vlastní službě aplikace Warehousing, kterou zpřístupňuje server Dynamics 365 for Operations. Po dokončení tohoto kroku budete mít uživatelská pověření WMDP, která sestávají z e-mailové adresy WMDP a hesla WMDP. Další informace o základních krocích přidání uživatelů do Azure AD a Dynamics 365 for Operations naleznete v tomto kurzu: [přihlášení k předplatnému Microsoft Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Vytvořte uživatele Dynamics 365 for Operations, který odpovídá pověření uživatele aplikace Warehousing.
    1.  V aplikaci Dynamics 365 for Operations přejděte na **Správa systému** &gt; **Společné** &gt; **Uživatelé**.
    2.  Vytvořte nového uživatele.
    3.  Přiřaďte uživatele mobilního zařízení skladu, jak je znázorněno na následujícím snímku obrazovky. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Přidružte aplikaci služby Active Directory Azure uživateli aplikace Warehousing.
    1.  V Dynamics 365 for Operations přejděte na **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
    2.  Vytvořit nový řádek.
    3.  Zadejte **ID klienta** (získané v poslední části), zadejte jeho název a vyberte dříve vytvořeného uživatele. Doporučujeme označit všechna zařízení, takže můžete snadno odebrat přístup k Dynamics 365 for Operations z této stránky v případě, že dojde ke ztrátě. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurace aplikace
Aplikaci je třeba nakonfigurovat na zařízení, aby se připojovala k serveru Dynamics 365 for Operations prostřednictvím Azure AD. To lze provést následovně:

1.  V aplikaci přejděte na **Nastavení připojení**.
2.  Zrušte zaškrtnutí políčka **Demo režim**. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Zadejte následující informace:- **ID klienta služby Azure Active Directory** - ID klienta je získáno v kroku 13 "Vytvoření aplikace webové služby ve službě Active Directory". - **Tajné ID klienta služby Azure Active Directory** - tajné ID klienta je získáno v kroku 13 "Vytvoření aplikace webové služby ve službě Active Directory". - **Prostředek Azure Active directory** -zdroj adresáře Azure AD znázorňuje kořenovou adresu URL Dynamics 365 for Operations. **Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). - **Klient Azure Active directory** - Klient Azure AD Directory používaný se serverem Dynamics 365 for Operations: https://login.windows.net/&lt;your-AD-tenant-ID&gt;. Příklad: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). - **Společnost** - zadejte právnickou osobu do Dynamics 365 for Operations, ke které se má aplikace připojovat. [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vyberte tlačítko **Zpět** tlačítko v levém horním rohu aplikace. Aplikace se nyní připojí k vašemu serveru Dynamics 365 for Operations a zobrazí se přihlašovací obrazovka pro pracovníka skladu. [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Odebrání přístupu k zařízení
V případě ztracených nebo narušených zařízení je nutné odebrat přístup k Dynamics 365 for Operations pro zařízení. Následující kroky popisují doporučený postup odebrání přístupu.

1.  V Dynamics 365 for Operations přejděte na **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
2.  Odstraň řádek, který odpovídá zařízení, kterému chcete odebrat přístup. Poznamenejte si **ID klienta** pro odebrané zařízení.
3.  Přihlaste se na portál Azure classic na stránkách <https://manage.windowsazure.com>.
4.  Klepněte na ikonu **Active Directory** v levé nabídce a potom klepněte na požadovaný adresář.
5.  V horní nabídce klepněte na příkaz **Aplikace**a klepněte na aplikaci, kterou chcete konfigurovat. Stránka **Rychlý Start** bude zobrazena pomocí jednotného přihlášení a dalších informací o konfiguraci.
6.  Klepněte na kartu **konfigurace** kartu, přejděte dolů a ujistěte se, za je **ID klienta** aplikace stejné jako v kroku 2 v této části.
7.  Klepněte na tlačítko **Odstranit** na panelu nástrojů.
8.  V potvrzující zprávě, která se otevře, klikněte na tlačítko **Ano**.





