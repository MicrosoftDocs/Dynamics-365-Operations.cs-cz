---
title: Přehled instalace a konfigurace skladové aplikace
description: Toto téma popisuje, jak nainstalovat a nakonfigurovat aplikaci Dynamics 365 Supply Chain Management – Sklady.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: b8eb8dee88d8664391d2dcf485dff9dee4722cac
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251493"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Přehled instalace a konfigurace skladové aplikace

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Toto téma popisuje způsob konfigurace skladu pro nasazení v cloudu. Postup konfigurace skladu pro místní nasazení naleznete v tématu [Sklady pro místní nasazení](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Toto téma popisuje, jak nainstalovat a nakonfigurovat aplikaci Dynamics 365 Supply Chain Management – Sklady.

Aplikace Warehousing je k dispozici v obchodě Google Play a v systému Windows Store. Pro aktuální verzi aplikace Dynamics 365 Supply Chain Management je tato aplikace k dispozici jako samostatná komponenta, což znamená samostatné nasazení na zařízeních pro úlohy skladu. Abyste mohli aplikaci v prostředí Finance and Operations použít, je nutné stáhnout aplikaci do každého zařízení a nakonfigurovat ho pro připojení k prostředí Supply Chain Management. Toto téma popisuje, jak nainstalovat aplikace na vašem zařízení. Také vysvětluje, jak nakonfigurovat aplikaci pro připojení k prostředí Supply Chain Management.

## <a name="prerequisites"></a>Předpoklady
Aplikace je k dispozici v operačních systémech Android a Windows. Chcete-li použít tuto aplikaci, musíte mít jeden z následujících podporovaných operačních systémů nainstalovaných v zařízení. Je také nutné mít jednu z následujících podporovaných verzí. Pomocí informací v následující tabulce určete, zda je vaše hardwarové a softwarové prostředí připraveno pro podporu instalace.

| Platforma                    | Verze                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (všechny verze)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, verze 1611 <br>- nebo - <br>Microsoft Dynamics AX verze 7.0/7.0.1 a Microsoft Dynamics AX aktualizace Platform Update 2 s opravou hotfix KB 3210014 |

## <a name="get-the-app"></a>Získat aplikaci
-   Windows (UWP)
     - [Finance and Operations – Sklady v obchodě Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations – Warehousing v obchodě Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery byla vyřazena, což znamená, že aplikace Warehousing již nebude k dispozici ke stažení z tohoto umístění.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Vytvoření aplikace webové služby v Azure Active Directory
Pokud chcete povolit interakci aplikace s konkrétním serverem Supply Chain Management, je nutné zaregistrovat aplikaci webové služby v Azure Active Directory pro klienta Supply Chain Management. Z bezpečnostních důvodů doporučujeme vytvořit webovou aplikaci služby pro každé zařízení, které používáte. Chcete-li vytvořit aplikaci webové služby v Azure Active Directory (Azure AD), proveďte následující kroky:

1.  Přejděte ve webovém prohlížeči na <https://portal.azure.com>.
2.  Zadejte jméno a heslo pro uživatele, kteří mají přístup k předplatnému Azure.
3.  Na portálu Azure v levém navigačním podokně klikněte na **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Ujistěte se, že instance služby Active Directory je ta, kterou používá aplikace Supply Chain Management.
5.  V seznamu klikněte na **Registrace aplikací**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  V horním podokně klikněte na **Nová registrace**. Spustí se **Průvodce registrací aplikace**.
7.  Zadejte název aplikace a vyberte **Pouze účty v tomto organizačním adresáři**. Klikněte na možnost **Registrovat**.  [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Otevře se vaše nová registrace aplikace. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Zapamatujte si **ID aplikace**, budete ho potřebovat později. Na **ID aplikace** se bude později odkazovat jako na **ID klienta**.
10. Klikněte na **Certifikát a tajné kódy** v podokně **Spravovat**. Klikněte **Nový tajný klíč klienta**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)
11. Vytvořte klíč zadáním popisu klíče a trvání v části **Hesla**. Klikněte na **Přidat** a zkopírujte klíč. Tento klíč bude později označován jako **tajný klíč klienta**. [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Vytvoření a konfigurace uživatelských účtů v aplikaci Supply Chain Management
Aby mohla aplikace Supply Chain Management používat vaši aplikaci Azure AD, je nutné provést následující kroky konfigurace:

1.  Vytvořte uživatele, který odpovídá pověření uživatele aplikace Warehousing.
    1.  Přejděte do nabídky **Správa systému** &gt; **Společné** &gt; **Uživatelé**.
    2.  Vytvořte nového uživatele.
    3.  Přiřaďte uživatele mobilního zařízení skladu, jak je znázorněno na následujícím snímku obrazovky. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Přidružte aplikaci služby Azure Active Directory k uživateli aplikace Sklady.
    1.  V aplikaci Supply Chain Management přejděte na **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
    2.  Vytvořit nový řádek.
    3.  Zadejte **ID klienta** (získané v poslední části), zadejte jeho název a vyberte dříve vytvořeného uživatele. Doporučujeme označit všechna zařízení, abyste jim v případě ztráty mohli z této stránky snadno odebrat přístup k aplikaci Supply Chain Management. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurace aplikace
Aplikaci je třeba nakonfigurovat v zařízení, aby se připojovala k serveru Supply Chain Management prostřednictvím aplikace Azure AD. To lze provést následovně:

1.  V aplikaci přejděte na **Nastavení připojení**.
2.  Zrušte zaškrtnutí políčka **Demo režim**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Zadejte následující informace: 
    + **ID klienta služby Azure Active Directory** – ID klienta získáte v kroku 9 v postupu „Vytvoření aplikace webové služby ve službě Active Directory“. 
    + **Tajný klíč klienta služby Azure Active Directory** – Tajný klíč získáte v kroku 11 v postupu „Vytvoření aplikace webové služby ve službě Active Directory“. 
    + **Prostředek služby Azure Active Directory** - Prostředek Azure AD určuje adresu URL aplikace Supply Chain Management. **Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). 
    + **Klient služby Azure Active Directory** - klient adresáře Azure AD, který se používá se serverem Supply Chain Management: `https://login.windows.net/your-AD-tenant-ID`. Například: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Poznámka:**: na konci tohoto pole nepoužívejte znak lomítka (/). 
    + **Společnost** – Zadejte právnickou osobu v aplikaci Supply Chain Management, ke které se má aplikace připojovat. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vyberte tlačítko **Zpět** tlačítko v levém horním rohu aplikace. Aplikace se nyní připojí k vašemu serveru Supply Chain Management a zobrazí se přihlašovací obrazovka pro pracovníka skladu. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Další informace o způsobu nastavení aplikace Warehousing pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení naleznete v tématu [Skenování čárových kódů pomocí fotoaparátu v aplikaci Dynamics 365 for Finance and Operations – Warehousing](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Odebrání přístupu k zařízení
Ztraceným nebo narušeným zařízením je nutné odebrat přístup k aplikaci Supply Chain Management. Následující kroky popisují doporučený postup odebrání přístupu.

1.  Přejděte do nabídky **Správa systému** &gt; **Nastavení** &gt; **Aplikace Azure Active Directory**.
2.  Odstraň řádek, který odpovídá zařízení, kterému chcete odebrat přístup. Pamatujte, že **ID klienta** se používá pro odebrané zařízení, budete ho potřebovat později.
3.  Přihlaste se do portálu Azure na <https://portal.azure.com>.
4.  Klikněte na ikonu **Active Directory** v levé nabídce a ujistěte se, že jste ve správném adresáři.
5.  V seznamu klikněte na **AppRegistrace aplikací** a klikněte na aplikaci, kterou chcete konfigurovat. Zobrazí se stránka **Nastavení** s informacemi o konfiguraci.
6.  Ujistěte se, že **ID klienta** aplikace je stejné jako v kroku 2 v této části.
7.  Klepněte na tlačítko **Odstranit** v horním podokně.
8.  V potvrzující zprávě, která se otevře, klikněte na tlačítko **Ano**.
