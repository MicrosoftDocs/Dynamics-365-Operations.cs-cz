---
title: Instalace a konfigurace Microsoft Dynamics 365 for Finance and Operations &#8211; Sklady
description: Toto téma popisuje, jak nainstalovat a nakonfigurovat aplikaci Microsoft Dynamics 365 for Finance and Operations – Sklady.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5e99351d79cb5898c6d5565d3d3197a8fe860df
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "316112"
---
# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Instalace a konfigurace Microsoft Dynamics 365 for Finance and Operations &#8211; Sklady

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Toto téma popisuje způsob konfigurace skladu pro nasazení v cloudu. Postup konfigurace skladu pro místní nasazení naleznete v tématu [Sklady pro místní nasazení](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Toto téma popisuje, jak nainstalovat a nakonfigurovat aplikaci Microsoft Dynamics 365 for Finance and Operations – Sklady.

Finance and Operations – Warehousing je aplikace, která je k dispozici v obchodech Google Play a Windows Store. Pro aktuální verzi aplikace Finance and Operations je tato aplikace k dispozici jako samostatná komponenta, což znamená samostatné nasazení na zařízeních pro úlohy skladu. Abyste mohli aplikaci v prostředí Finance and Operations použít, je nutné stáhnout aplikaci do každého zařízení a nakonfigurovat ho pro připojení k prostředí Finance and Operations. Toto téma popisuje, jak nainstalovat aplikace na vašem zařízení. Také vysvětluje, jak nakonfigurovat aplikaci pro připojení k prostředí Finance and Operations.

## <a name="prerequisites"></a>Předpoklady
Aplikace je k dispozici v operačních systémech Android a Windows. Chcete-li použít tuto aplikaci, musíte mít jeden z následujících podporovaných operačních systémů nainstalovaných v zařízení. Také musíte mít jednu z následujících podporovaných verzí aplikace Finance and Operations. Pomocí informací v následující tabulce určete, zda je vaše hardwarové a softwarové prostředí připraveno pro podporu instalace.

| Platforma                    | Verze                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (všechny verze)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, verze 1611 <br>- nebo - <br>Microsoft Dynamics AX verze 7.0/7.0.1 a Microsoft Dynamics AX aktualizace Platform Update 2 s opravou hotfix KB 3210014 |

## <a name="get-the-app"></a>Získat aplikaci
-   Windows (UWP)
     - [Finance and Operations – Sklady v obchodě Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations – Warehousing v obchodě Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery byla vyřazena, což znamená, že aplikace Finance and Operations - Sklady již nebude k dispozici ke stažení z tohoto umístění.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Vytvoření aplikace webové služby v Azure Active Directory
Pokud chcete povolit interakci aplikace s konkrétním serverem Finance and Operations, je nutné zaregistrovat aplikaci webové služby v Azure Active Directory pro klienta Finance and Operations. Z bezpečnostních důvodů doporučujeme vytvořit webovou aplikaci služby pro každé zařízení, které používáte. Chcete-li vytvořit aplikaci webové služby v Azure Active Directory (Azure AD), proveďte následující kroky:

1.  Přejděte ve webovém prohlížeči na <https://portal.azure.com>.
2.  Zadejte jméno a heslo pro uživatele, kteří mají přístup k předplatnému Azure.
3.  Na portálu Azure v levém navigačním podokně klikněte na **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Ujistěte se, že instance služby Active Directory je ta, kterou používá aplikace Finance and Operations.
5.  V seznamu klikněte na **Registrace aplikací**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  V horním podokně klikněte na **Registrace nové aplikace**. Spustí se průvodce **Přidat aplikaci**.
7.  Zadejte název aplikace a vyberte **Webová aplikace/webové rozhraní API**. Zadejte přihlašovací adresu URL, tedy adresu URL webové aplikace. Tato adresa URL je stejná jako adresa URL nasazení, ale na konci je uveden řetězec oauth. Klepněte na volbu **Nový**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Vyberte novou aplikaci v seznamu. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Zapamatujte si **ID aplikace**, budete ho potřebovat později. Na **ID aplikace** se bude později odkazovat jako na **ID klienta**.
10. Klikněte na **Klíče** v podokně **Nastavení**. Vytvořte klíč zadáním popisu klíče a trvání v části **Hesla**. 
11. Klikněte na **Uložit** a zkopírujte klíč. Tento klíč bude později označován jako **tajný klíč klienta**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Vytvoření a konfigurace uživatelských účtů v aplikaci Finance and Operations
Aby mohla aplikace Finance and Operations používat vaši aplikaci Azure AD, je nutné provést následující kroky konfigurace:

1.  Vytvořte uživatele aplikace Finance and Operations, který odpovídá pověření uživatele aplikace Warehousing.
    1.  V aplikaci Finance and Operations vyberte položky **Správa systému** &gt; **Společné** &gt; **Uživatelé**.
    2.  Vytvořte nového uživatele.
    3.  Přiřaďte uživatele mobilního zařízení skladu, jak je znázorněno na následujícím snímku obrazovky. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Přidružte aplikaci služby Azure Active Directory k uživateli aplikace Sklady.
    1.  V aplikaci Finance and Operations přejděte na **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
    2.  Vytvořit nový řádek.
    3.  Zadejte **ID klienta** (získané v poslední části), zadejte jeho název a vyberte dříve vytvořeného uživatele. Doporučujeme označit všechna zařízení, abyste jim v případě ztráty mohli z této stránky snadno odebrat přístup k aplikaci Finance and Operations. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurace aplikace
Aplikaci je třeba nakonfigurovat v zařízení, aby se připojovala k serveru Finance and Operations prostřednictvím aplikace Azure AD. To lze provést následovně:

1.  V aplikaci přejděte na **Nastavení připojení**.
2.  Zrušte zaškrtnutí políčka **Demo režim**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Zadejte následující informace: 
    + **ID klienta služby Azure Active Directory** – ID klienta získáte v kroku 9 v postupu „Vytvoření aplikace webové služby ve službě Active Directory“. 
    + **Tajný klíč klienta služby Azure Active Directory** – Tajný klíč získáte v kroku 11 v postupu „Vytvoření aplikace webové služby ve službě Active Directory“. 
    + **Prostředek služby Azure Active Directory** – Prostředek Azure AD určuje kořenovou adresu URL aplikace Finance and Operations. **Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). 
    + **Klient služby Azure Active Directory** – Jedná se o klienta služby Azure AD používaného se serverem Finance and Operations: `https://login.windows.net/your-AD-tenant-ID`. Například: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). 
    + **Společnost** – Zadejte právnickou osobu v aplikaci Finance and Operations, ke které se má aplikace připojovat. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vyberte tlačítko **Zpět** tlačítko v levém horním rohu aplikace. Aplikace se nyní připojí k vašemu serveru Finance and Operations a zobrazí se přihlašovací obrazovka pro pracovníka skladu. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Další informace o způsobu nastavení Dynamics 365 for Finance and Operations – Sklady pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení naleznete v tématu [Skenování čárových kódů pomocí fotoaparátu v aplikaci Dynamics 365 for Finance and Operations – Sklady](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Odebrání přístupu k zařízení
Ztraceným nebo narušeným zařízením je nutné odebrat přístup k aplikaci Finance and Operations. Následující kroky popisují doporučený postup odebrání přístupu.

1.  V aplikaci Finance and Operations přejděte na **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
2.  Odstraň řádek, který odpovídá zařízení, kterému chcete odebrat přístup. Pamatujte, že **ID klienta** se používá pro odebrané zařízení, budete ho potřebovat později.
3.  Přihlaste se do portálu Azure na <https://portal.azure.com>.
4.  Klikněte na ikonu **Active Directory** v levé nabídce a ujistěte se, že jste ve správném adresáři.
5.  V seznamu klikněte na **AppRegistrace aplikací** a klikněte na aplikaci, kterou chcete konfigurovat. Zobrazí se stránka **Nastavení** s informacemi o konfiguraci.
6.  Ujistěte se, že **ID klienta** aplikace je stejné jako v kroku 2 v této části.
7.  Klepněte na tlačítko **Odstranit** v horním podokně.
8.  V potvrzující zprávě, která se otevře, klikněte na tlačítko **Ano**.
