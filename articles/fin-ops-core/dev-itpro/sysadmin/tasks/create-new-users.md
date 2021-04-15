---
title: Vytvoření nových uživatelů
description: Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b994473b4535c255f87551a6d97e197516fc2a9c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745830"
---
# <a name="create-new-users"></a>Vytvoření nových uživatelů

[!include [banner](../../includes/banner.md)]

Než budete mít přístup do aplikací Finance and Operations, musíte být nejprve přidáni na stránku **Uživatelé** (**Správa systému \> Uživatelé \> Uživatelé**). Mezi uživatele patří interní zaměstnanci vaší organizace nebo externí zákazníci a prodejci. Uživatele lze importovat nebo přidávat ručně. Všichni uživatelé musí mít správnou licenci pro použití v souladu s předpisy.

Informace o tom, jak nakupovat a licencovat pro aplikace Finance and Operations, najdete v části [Průvodce licencováním Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Přiřazení licence uživateli
Správci systému mohou [přiřazovat licence uživatelům](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) v [centru správy Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Přidání externího uživatele do Azure AD a přiřazení licence 
Externí uživatelé musí být zastoupeni ve vašem adresáři klienta (Azure Active Directory (Azure AD)), aby jim mohly být přiřazeny licence. Tito externí uživatelé by měli být přidáni do klienta v Azure AD jako uživatelé typu Host a poté jim přiřazovat příslušné licence. Požadavek na aplikace Finance and Operations je, že společnost hostujícího uživatele musí používat Azure AD. Další informace naleznete v tématu [Přidání uživatelů spolupráce B2B Azure Active Directory na portálu Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Import nových uživatelů ze služby Azure AD 
1. Přejděte do nabídky **Správa systému** \> **Uživatel** \> **Uživatelé**.
2. V podokně akcí klikněte na možnost **Import uživatele**.
3. Vyberte uživatele pro import. Seznam obsahuje uživatele Azure AD, kteří aktuálně nejsou uživateli v tomto prostředí.
4. Vybrat **Importovat uživatele**.
5. Vyberte **Zavřít**.

> [!NOTE]
> Hodnota pro pole **Společnost** bude nastaveno na základě aktuální relační společnosti pro správce. Po importu musíte podle potřeby přiřadit role a organizace. Další informace viz [Přiřadit uživatelům role zabezpečení](assign-users-security-roles.md). Podmíněně může být také požadováno přidružení uživatele k **Osobě** a aktualizovat možnosti uživatele, například jazyk.

## <a name="manually-add-a-new-user"></a>Ruční přidání nového uživatele
1. Přejděte do nabídky **Správa systému** \> **Uživatelé** \> **Uživatelé**.
2. V podokně akcí zvolte **Nový**.
3. Do pole **ID uživatele** zadejte jedinečný identifikátor uživatele.   
4. Do pole **Jméno uživatele** zadejte jméno uživatele.  
5. V poli **Poskytovatel**:
 - Pro interní uživatele použijte výchozí hodnotu. Například váš klient Azure AD s předponou https://sts.windows.net/.  
 - Pro ty, kdo nejsou uživateli Azure AD, jako jsou účty Service-2-Service, zadejte základní textovou hodnotu. Například: NA. Tato hodnota pomůže vyhnout se nesprávným voláním ověřování, které by mohly vést k chybám, pokud se použije platná hodnota poskytovatele identity.  
 - Pro externí nebo hostující uživatele přidejte jejich jméno klienta Azure AD za https://sts.windows.net/.
6. Do pole **E-mail** zadejte celou e-mailovou adresu/hlavní jméno uživatele.  
7. V poli **Společnost** vyberte výchozí spouštěcí společnost pro uživatele. 
8. Zvolte **Uložit**.

Hodnoty pro poskytovatele identity a telemetrické ID budou aktualizovány na základě volání [Microsoft graf](https://docs.microsoft.com/graph/overview), když je záznam uživatele uložen. ID telemetrie je založeno na uživatelském ID objektu / identifikátoru zabezpečení (SID) v Azure AD.

> [!NOTE]
> Po přidání uživatele musíte podle potřeby přiřadit role a organizace. Další informace viz [Přiřadit uživatelům role zabezpečení](assign-users-security-roles.md). Podmíněně může být také požadováno přidružení uživatele k **Osobě** a aktualizovat **možnosti uživatele**, například jazyk.

## <a name="change-a-user-id"></a>Změňte ID uživatele
Chcete-li změnit ID uživatele, musíte klíč v databázi přejmenovat. Když změníte ID uživatele pomocí tohoto postupu, všechna související nastavení uživatele se upraví tak, aby používala nové ID uživatele. Například informace o použití v tabulce **SysLastValue** je aktualizována, aby odkazovala na nové ID uživatele.

> [!NOTE]
> ID uživatele je primárním klíčem tabulky s informacemi o uživateli. Přejmenování primárního klíče může stávajícím uživatelům nějakou dobu trvat, protože všechny odkazy na klíč jsou také aktualizovány v databázi. 

1. Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.
2. Vyberte uživatele v seznamu a vyberte **Možnosti\> Informace o záznamu**.
3. Vyberte **Přejmenovat**.
4. Zadejte novou a jedinečnou hodnotu ID uživatele a vyberte **OK**. 
5. Potvrďte výběrem tlačítka **Ano**.

## <a name="additional-resources"></a>Další prostředky

Další možnosti implementace uživatelů B2B najdete v tématu [Export uživatele B2B do Azure AD](../implement-b2b.md).

Informace o předkonfigurovaných systémových účtech najdete v části [Předkonfigurované systémové účty](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]