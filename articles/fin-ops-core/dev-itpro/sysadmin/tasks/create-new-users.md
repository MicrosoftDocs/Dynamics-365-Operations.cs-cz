---
title: Vytvoření nových uživatelů
description: Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
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
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180937"
---
# <a name="create-new-users"></a>Vytvoření nových uživatelů

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Přiřazení uživatele k licenci (pouze nové typy licencí)
Pro zákazníky, kteří se nacházejí v jednom z nových typů licencí, které byly přidány v říjnu 2019, je nutné, aby byli uživatelé přiřazeni k licenci. Uživatelé, kteří jsou přiřazeni k licenci, jsou automaticky přidáni jako uživatelé systému, kteří při prvním přihlášení nemají žádné role. Uživatelé, kteří nejsou přidruženi k licenci, obdrží zprávu s upozorněním.

Správci systému mohou [přiřazovat licence uživatelům](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) v [centru správy Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Přidat nového uživatele
1. Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.
2. V podokně akcí zvolte **Nový**.
3. Do pole **ID uživatele** zadejte jedinečný identifikátor uživatele. ID uživatele je povinné.  
4. Do pole **Jméno uživatele** zadejte jméno uživatele.  
5. Do pole **Doména** zadejte doménu daného uživatele.  
6. Do pole **Alias** zadejte alias uživatele.  
7. V poli **Společnost** zvolte požadovanou společnost. 
8. Na pevné záložce **Role uživatele** vyberte možnost **Přiřadit role** a [přiřaďte je uživatelům k rolím zabezpečení](assign-users-security-roles.md)
9. Vyberte **OK**.
10. Zvolte **Uložit**.

## <a name="import-users"></a>Importovat uživatele
1. V podokně akcí klikněte na možnost **Import uživatele**.
2. Označte na seznamu vybraný řádek.
3. Vybrat **Importovat uživatele**.
4. Vyberte **Zavřít**.

