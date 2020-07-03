---
title: Vytvoření nových uživatelů
description: Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435577"
---
# <a name="create-new-users"></a>Vytvoření nových uživatelů

[!include [banner](../../includes/banner.md)]

Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Přiřazení uživatele k licenci (pouze nové typy licencí)
Pro zákazníky, kteří se nacházejí v jednom z nových typů licencí, které byly přidány v říjnu 2019, je nutné, aby byli uživatelé přiřazeni k licenci. Uživatelé, kteří jsou přiřazeni k licenci, jsou automaticky přidáni jako uživatelé systému, kteří při prvním přihlášení nemají žádné role.

Správci systému mohou [přiřazovat licence uživatelům](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) v [centru správy Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Přiřazení externího uživatele k licenci (pouze nové typy licencí)
Uživatelé, kteří jsou externí vůči klientovi, do kterého bylo prostředí nasazeno, je třeba reprezentovat v adresáři hostitelského klienta (Azure Active Directory (Azure AD)), aby jim mohly být přiřazeny licence. Tito externí uživatelé by měli být přidáni do klienta v Azure AD jako uživatelé typu Host a poté jim přiřazovat příslušné licence. Další informace naleznete v tématu [Přidání uživatelů spolupráce B2B Azure Active Directory na portálu Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Přidat nového uživatele
1. Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.
2. V podokně akcí zvolte **Nový**.
3. Do pole **ID uživatele** zadejte jedinečný identifikátor uživatele. ID uživatele je povinné.  
4. Do pole **Jméno uživatele** zadejte jméno uživatele.  
5. Do pole **Doména** zadejte doménu daného uživatele.  
6. Do pole **Alias** zadejte alias uživatele.  
7. V poli **Společnost** zvolte požadovanou společnost. 
8. Na pevné kartě **Role uživatele** vyberte možnost **Přiřadit role**, chcete-li uživatelům přiřadit role zabezpečení. Další informace viz [Přiřadit uživatelům role zabezpečení](assign-users-security-roles.md).
9. Vyberte **OK**.
10. Zvolte **Uložit**.

## <a name="import-users"></a>Importovat uživatele
1. Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.
2. V podokně akcí klikněte na možnost **Import uživatele**.
3. Označte na seznamu vybraný řádek.
4. Vybrat **Importovat uživatele**.
5. Vyberte **Zavřít**.

