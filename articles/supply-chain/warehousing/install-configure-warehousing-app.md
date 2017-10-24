---
title: "Instalace a konfigurace aplikace Microsoft Dynamics 365 for Finance and Operations – Warehousing"
description: "Toto téma popisuje, jak nainstalovat a nakonfigurovat Microsoft Dynamics 365 for Finance and Operations – Warehousing."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 31e77b27d4bf95c997817b3a053b33119562adf8
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Instalace a konfigurace aplikace Microsoft Dynamics 365 for Finance and Operations – Warehousing

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak nainstalovat a nakonfigurovat Microsoft Dynamics 365 for Finance and Operations – Warehousing.

Finance and Operations – Warehousing je aplikace, která je k dispozici v obchodech Google Play a Windows Store. Pro aktuální verzi aplikace Finance and Operations je tato aplikace k dispozici jako samostatná komponenta, což znamená samostatné nasazení na zařízeních pro úlohy skladu. Abyste mohli aplikaci v prostředí Finance and Operations použít, je nutné stáhnout aplikaci do každého zařízení a nakonfigurovat ho pro připojení k prostředí Finance and Operations. Toto téma popisuje, jak nainstalovat aplikace na vašem zařízení. Také vysvětluje, jak nakonfigurovat aplikaci pro připojení k prostředí Finance and Operations.

## <a name="prerequisites"></a>Požadavky
Aplikace je k dispozici v operačních systémech Android a Windows. Chcete-li použít tuto aplikaci, musíte mít jeden z následujících podporovaných operačních systémů nainstalovaných v zařízení. Také musíte mít jednu z následujících podporovaných verzí aplikace Finance and Operations. Pomocí informací v následující tabulce určete, zda je vaše hardwarové a softwarové prostředí připraveno pro podporu instalace.

| Platforma                    | Verze                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (všechny verze)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operations verze 1611 <br>- nebo - <br>Microsoft Dynamics Dynamics AX verze 7.0/7.0.1 a platforma Microsoft Dynamics AX s aktualizací 2 a opravou hotfix KB 3210014 |

## <a name="get-the-app"></a>Získat aplikaci
-   Windows (UWP): [Finance and Operations – Warehousing v obchodě Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operations – Warehousing v obchodě Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations – Warehousing v galerii Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>Vytvoření aplikace webové služby ve službě Active Directory
Pokud chcete povolit interakci aplikace s konkrétním serverem Finance and Operations, je nutné zaregistrovat aplikaci webové služby v adresáři Azure Active Directory pro klienta Finance and Operations. Z bezpečnostních důvodů doporučujeme vytvořit webovou aplikaci služby pro každé zařízení, které používáte. Chcete-li vytvořit webovou aplikaci služby ve službě Active Directory Azure (Azure AD), proveďte následující kroky:

1.  Ve webovém prohlížeči přejděte na <https://manage.windowsazure.com>.
2.  Zadejte jméno a heslo pro uživatele, kteří mají přístup k předplatnému Azure.
3.  V portálu Azure v levém navigačním podokně klepněte na **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  V mřížce vyberte instanci služby Active Directory používanou aplikací Finance and Operations.
5.  Na horním panelu nástrojů klepněte na tlačítko **Aplikace**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  V dolním podokně klikněte na **Přidat**. Spustí se průvodce **Přidat aplikaci**.
7.  Zadejte název aplikace a vyberte **Webová aplikace nebo webové rozhraní API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Zadejte přihlašovací adresu URL, tedy adresu URL webové aplikace. Tato adresa URL je stejná jako adresa URL nasazení, ale na konci je uveden řetězec oauth. Zadejte URI ID aplikace. Tato hodnota je povinná, ale není nutná pro ověření. Zajistěte, aby URI ID aplikace byl jen nepravý, například https://contosooperations/wmapp, protože při použití URL nasazení může dojít k potížím s přihlašováním do jiných aplikací AAD, například doplňku aplikace Excel. [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  Přejděte na kartu **Konfigurovat**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Přejděte dolů, dokud se nezobrazí oddíl **Oprávnění pro ostatní aplikace**. Klikněte na **Přidat aplikaci**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. V seznamu vyberte **Microsoft Dynamics ERP**. Klepněte na tlačítko **Dokončit kontrolu** v pravém horním rohu stránky. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. V seznamu **Delegovat oprávnění** zaškrtněte všechna políčka. Klikněte na možnost **Uložit**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Poznamenejte si následující informace:
    -   **ID klienta** - při posouvání nahoru na stránku se zobrazí **ID klienta**.
    -   **Klíč** - v oddílu **klíče** vytvořte klíč výběrem doby trvání a zkopírováním klíče. Tento klíč bude později označován jako **tajný klíč klienta**.

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Vytvoření a konfigurace uživatelských účtů v aplikaci Finance and Operations
Aby mohla aplikace Finance and Operations používat vaši aplikaci Azure AD, je nutné provést následující kroky konfigurace:

1.  Ve službě Azure Active Directory pro aplikaci Finance and Operations vytvořte nový uživatelský účet. Účelem tohoto uživatelského účtu je zajištění přístupu ke konkrétní vlastní službě aplikace Warehousing, kterou zpřístupňuje server Finance and Operations. Po dokončení tohoto kroku budete mít uživatelská pověření WMDP, která sestávají z e-mailové adresy WMDP a hesla WMDP. Další informace o základních krocích přidání uživatelů do Azure AD a Finance and Operations najdete v tomto kurzu: [Přihlášení k předplatnému aplikace Finance and Operations](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Vytvořte uživatele aplikace Finance and Operations, který odpovídá pověření uživatele aplikace Warehousing.
    1.  V aplikaci Finance and Operations vyberte položky **Správa systému** &gt; **Společné** &gt; **Uživatelé**.
    2.  Vytvořte nového uživatele.
    3.  Přiřaďte uživatele mobilního zařízení skladu, jak je znázorněno na následujícím snímku obrazovky. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Přidružte aplikaci služby Active Directory Azure uživateli aplikace Warehousing.
    1.  V aplikaci Finance and Operations vyberte položky **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
    2.  Vytvořit nový řádek.
    3.  Zadejte **ID klienta** (získané v poslední části), zadejte jeho název a vyberte dříve vytvořeného uživatele. Doporučujeme označit všechna zařízení, abyste jim v případě ztráty mohli z této stránky snadno odebrat přístup k aplikaci Finance and Operations. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurace aplikace
Aplikaci je třeba nakonfigurovat v zařízení, aby se připojovala k serveru Finance and Operations prostřednictvím aplikace Azure AD. To lze provést následovně:

1.  V aplikaci přejděte na **Nastavení připojení**.
2.  Zrušte zaškrtnutí políčka **Demo režim**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Zadejte následující informace: 
    + **ID klienta služby Azure Active Directory** – ID klienta získáte v kroku 13 v postupu „Vytvoření aplikace webové služby ve službě Active Directory“. 
    + **Tajný klíč klienta služby Azure Active Directory** – Tajný klíč získáte v kroku 13 v postupu „Vytvoření aplikace webové služby ve službě Active Directory“. 
    + **Prostředek služby Azure Active Directory** – Prostředek určuje kořenovou adresu URL aplikace Finance and Operations. **Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). 
    + **Nájemce služby Azure Active Directory** – Jedná se o klienta služby Azure AD Directory používaného se serverem Finance and Operations: https://login.windows.net/vase-ID-klienta-AD. Příklad: https://login.windows.net/contosooperations.onmicrosoft.com.
    <br>**Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). 
    + **Společnost** – Zadejte právnickou osobu v aplikaci Finance and Operations, ke které se má aplikace připojovat. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vyberte tlačítko **Zpět** tlačítko v levém horním rohu aplikace. Aplikace se nyní připojí k vašemu serveru Finance and Operations a zobrazí se přihlašovací obrazovka pro pracovníka skladu. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Odebrání přístupu k zařízení
Ztraceným nebo narušeným zařízením je nutné odebrat přístup k aplikaci Finance and Operations. Následující kroky popisují doporučený postup odebrání přístupu.

1.  V aplikaci Finance and Operations vyberte položky **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
2.  Odstraň řádek, který odpovídá zařízení, kterému chcete odebrat přístup. Poznamenejte si **ID klienta** pro odebrané zařízení.
3.  Přihlaste se na portál Azure classic na stránkách <https://manage.windowsazure.com>.
4.  Klepněte na ikonu **Active Directory** v levé nabídce a potom klepněte na požadovaný adresář.
5.  V horní nabídce klepněte na příkaz **Aplikace** a klepněte na aplikaci, kterou chcete konfigurovat. Stránka **Rychlý Start** bude zobrazena pomocí jednotného přihlášení a dalších informací o konfiguraci.
6.  Klepněte na kartu **konfigurace** kartu, přejděte dolů a ujistěte se, za je **ID klienta** aplikace stejné jako v kroku 2 v této části.
7.  Klepněte na tlačítko **Odstranit** na panelu nástrojů.
8.  V potvrzující zprávě, která se otevře, klikněte na tlačítko **Ano**.





