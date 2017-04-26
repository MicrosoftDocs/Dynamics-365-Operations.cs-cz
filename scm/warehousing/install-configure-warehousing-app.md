---
title: "Nainstalujte a nakonfigurujte Microsoft Dynamics 365 pro operace & #8211; Skladování"
description: "Toto téma popisuje, jak nainstalovat a nakonfigurovat Microsoft Dynamics 365 pro operace - skladování."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-18 14 - 23 - 32
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Nainstalujte a nakonfigurujte Microsoft Dynamics 365 pro operace & #8211; Skladování

Toto téma popisuje, jak nainstalovat a nakonfigurovat Microsoft Dynamics 365 pro operace - skladování.

Dynamics 365 pro operace - skladu je k dispozici aplikace na Google Play Store a Windows Store. Pro aktuální verzi aplikace Microsoft Dynamics 365 pro operace tato app je k dispozici jako samostatné komponenty, což znamená samostatné nasazení na zařízeních pro činnosti skladu. Pomocí aplikace pro prostředí operací ve vašem Dynamics 365, je nutné stáhnout app na každé zařízení a nakonfigurovat jej pro připojení k vaší 365 Dynamics pro operace prostředí. Toto téma popisuje, jak nainstalovat aplikace na vašem zařízení. Také vysvětluje, jak nakonfigurovat aplikace pro připojení k vaší 365 Dynamics pro operace prostředí.

## <a name="prerequisites"></a>Předpoklady
Aplikace je k dispozici v operačních systémech Android a Windows. Chcete-li použít tuto aplikaci, musí mít jeden z následujících podporovaných operačních systémech nainstalovaných zařízení. Také musí mít jeden z následujících podporovaných verzích 365 Dynamics pro operace. Pomocí informací v následující tabulce pro vyhodnocení, zda je připraven pro podporu instalace prostředí hardwaru a softwaru.

| Platforma                    | Verze                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (všechny verze)                                                                                                                                                   |
| Dynamics 365 pro operace | 365 Microsoft Dynamics pro operace 1611 - nebo - klienta Dynamics AX verze 7.0/7.0.1 a platformu Microsoft Dynamics AX aktualizovat 2 s opravou hotfix KB 3210014 |

## <a name="get-the-app"></a>Získání aplikace
-   Windows (UWP) - [Dynamics 365 pro operace - skladování na Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 pro operace - uskladnění v úložišti služby Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Vytvoření aplikace webové služby ve službě Active Directory
Povolit aplikace pro interakci s konkrétní 365 Dynamics pro operace serveru, musíte zaregistrovat aplikace webové služby ve službě Active Directory Azure pro 365 Dynamics pro operace klienta. Z bezpečnostních důvodů doporučujeme vytvořit webovou aplikaci služby pro každé zařízení, které používáte. Chcete-li vytvořit webovou aplikaci služby ve službě Active Directory Azure (Azure AD), proveďte následující kroky:

1.  Ve webovém prohlížeči přejděte na <https://manage.windowsazure.com>.
2.  Zadejte jméno a heslo pro uživatele, kteří mají přístup k předplatnému Azure.
3.  V portálu Azure v levém navigačním podokně klepněte na **služby Active Directory**. [](./media/wh-01-active-directory-example.png)[![c-01aktivní adresář příklad](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  V mřížce vyberte instanci služby Active Directory používaný Dynamics 365 pro operace.
5.  Na horním panelu nástrojů, klepněte na tlačítko **aplikace**. [![c-02aktivní adresář aplikace](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  V dolním podokně klepněte na **přidat**. **Přidat aplikaci** spuštění průvodce.
7.  Zadejte název aplikace a vyberte **webové aplikace nebo webové rozhraní API**. [![Wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Zadejte URL přihlášení, což je adresa URL aplikace v klienta, kořenové adresy URL operace. Adresa URL přihlášení není aktuálně používán aktivně při ověřování aplikace, ale je povinné pole. Zadejte stejnou adresu URL v poli ID identifikátoru URI. [![c-04-ad přidat – vlastnosti](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Přejděte **konfigurace** kartu. [![c-05-ad konfigurace app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Přejděte dolů, dokud se nezobrazí **oprávnění pro ostatní aplikace** oddílu. Klepněte na tlačítko **přidat aplikaci**. [![Wh-06-AD-App-Add-Permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Vyberte **aplikaci Microsoft Dynamics ERP** v seznamu. Klepněte **dokončit kontrolu** tlačítko v pravém horním rohu stránky. [![Wh-07-ad výběr oprávnění](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. V **delegovat oprávnění** seznam, zaškrtněte všechna políčka. Click **Save**. [![Wh-08-ad delegát oprávnění](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Poznamenejte si následující informace:
    -   **ID klienta** - při posouvání nahoru na stránku, zobrazí se **ID klienta** zobrazí.
    -   **Klíč** - v **klíče** oddílu, vytvořte klíč vyberte dobu trvání a zkopírovat klíč. Tento klíč bude později označována jako **tajný klíč klienta**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Vytvoření a konfigurace uživatelských účtů v 365 Dynamics pro operace
Aby 365 Dynamics pro operace, které používají aplikace Azure AD, je nutné dokončit následující kroky konfigurace:

1.  Vytvoření nového uživatelského účtu ve službě Active Directory Azure pro 365 Dynamics pro operace klienta. Účelem tohoto uživatelského účtu je pro přístup k určité vlastní službě uskladnění app, která zpřístupňuje 365 Dynamics pro operace serveru. Po dokončení tohoto kroku, budete mít WMDP uživatelská pověření, která se skládá z e-mailovou adresu WMDP a WMDP heslo. Další informace o základní kroky pro přidání uživatelů do Azure AD a 365 Dynamics pro operace, naleznete v tomto kurzu: [přihlásit 365 Microsoft Dynamics pro operace odběru](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Vytvořte Dynamics 365 pro operace uživatele, který odpovídá uskladnění app uživatelská pověření.
    1.  V 365 Dynamics pro operace, přejděte na **Správa systému**&gt;**běžné**&gt;**uživatelů**.
    2.  Vytvořte nového uživatele.
    3.  Přiřadíte uživatele mobilního zařízení skladu, jak je znázorněno v následující snímek obrazovky. [![Wh-09-Add-User-Security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Přidružení aplikace služby Active Directory Azure skladu app uživateli.
    1.  V 365 Dynamics pro operace, přejděte na **Správa systému**&gt;**nastavení**&gt;**Azure Active Directory aplikace**.
    2.  Vytvořit nový řádek.
    3.  Zadejte **ID klienta** (získané v poslední části), zadejte jeho název a vyberte dříve vytvořený uživatelem. Doporučujeme označit všechna zařízení, takže můžete snadno odebrat přístup k 365 Dynamics pro operace z této stránky v případě, že dojde ke ztrátě. [![Wh 10-ad aplikace formulář](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurace aplikace
Aplikace je třeba nakonfigurovat zařízení pro připojení k 365 Dynamics Server operace prostřednictvím aplikace Azure AD. Chcete-li to provést, proveďte následující kroky.

1.  V aplikaci, přejděte na **nastavení připojení**.
2.  Vymazat **Demo režim** pole. [![Wh-11-App-Connection-Settings-Demo-Mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Zadejte následující informace:- **ID klienta služby Azure Active directory** -klient je získat ID v kroku 13 "Vytvoření aplikace webové služby ve službě Active Directory". - **Tajný klíč klienta azure Active directory** -tajný klíč klienta je získaný v kroku 13 "Vytvoření aplikace webové služby ve službě Active Directory". - **Prostředků azure Active directory** -zdroj adresáře Azure AD znázorňuje Dynamics 365 pro operace kořenová adresa URL. **Poznámka:**: na konci tohoto pole znak lomítka (/). - **Azure Active directory klienta** -adresář klienta Azure AD používá pro Dynamics 365 server operace: https://login.windows.net/&lt;e AD-nájemce ID&gt;. Příklad: https://login.windows.net/contosooperations.onmicrosoft.com. **Poznámka:**: na konci tohoto pole znak lomítka (/). - **Společnost** -právnická osoba zadejte do Dynamics 365 pro operace, které chcete, aby aplikace pro připojení. [![c-12-app--nastavení připojení](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vyberte **zpět** tlačítko v levém horním aplikace. Aplikace se nyní připojí k vaší 365 Dynamics pro operace serveru a zobrazí přihlašovací obrazovka pro pracovníka skladu. [![c 13 přihlašovací obrazovka](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Odebrání přístupu k zařízení
V případě ztracených nebo narušený zařízení je nutné odebrat přístup k Dynamics 365 pro provoz zařízení. Následující kroky popisují doporučený postup odebrání přístupu.

1.  V 365 Dynamics pro operace, přejděte na **Správa systému**&gt;**nastavení**&gt;**Azure Active Directory aplikace**.
2.  Odstraníte řádek, který odpovídá zařízení, které chcete odebrat přístup. Poznamenejte si **ID klienta** pro odebrané zařízení.
3.  Přihlásit na portál Azure klasické na <https://manage.windowsazure.com>.
4.  Klepněte **služby Active Directory** ikonu v levé nabídce a potom klepněte na požadovaný adresář.
5.  V horní nabídce klepněte na příkaz **aplikace**a klepněte na aplikaci, kterou chcete konfigurovat. **Rychlý Start** bude stránka zobrazena pomocí jednotného přihlášení a další informace o konfiguraci.
6.  Klepněte **konfigurace** kartu, přejděte dolů a zajistit, aby **ID klienta** aplikace je stejný jako v kroku 2 v této části.
7.  Klepněte **odstranit** tlačítko na panelu příkazů.
8.  Klepněte na tlačítko **Ano** v potvrzovací zprávě.



