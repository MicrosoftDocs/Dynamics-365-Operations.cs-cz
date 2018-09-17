--- 
title: "Přiřadit uživatelů k rolím zabezpečení"
description: "Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations, edice Enterprise."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="assign-users-to-security-roles"></a>Přiřadit uživatelů k rolím zabezpečení

[!include [task guide banner](../../includes/task-guide-banner.md)]

Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations, edice Enterprise. Tento postup vysvětluje způsob, jakým správce systému může přiřadit uživatele k rolím automaticky na základě obchodních dat. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="automatically-assign-users-to-roles"></a>Automatické přiřazení uživatelů k rolím
1. Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.
2. Ve stromovém zobrazení vyberte „Vedoucí účetní“.
    * Vyberte roli, pro kterou chcete konfigurovat pravidlo. V tomto příkladu vyberte vedoucí účetní.  
3. Klepnutím na možnost Přidat pravidlo otevřete dialogové okno.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte dotaz, který chcete použít pro toto pravidlo.  
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na možnost Upravit dotaz.
    * Podle potřeby upravte dotaz.  
7. Klikněte na tlačítko OK.

## <a name="exclude-users-from-automatic-role-assignment"></a>Vyloučení uživatelů z automatického přiřazení k roli
1. Zavřete stránku.
2. Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.
3. Ve stromovém zobrazení vyberte „Vedoucí účetní“.
    * Vyberte požadovanou roli. V tomto příkladu vyberte vedoucí účetní.  
4. Klikněte na Ručně přiřadit nebo vyloučit uživatele.
5. Označte v seznamu vybraný řádek.
    * Vyberte uživatele.  
6. Klikněte na Vyloučit z role.
    * Kliknutím na Vyloučit z role vyloučíte vybrané uživatele z role. Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko Vynulovat stav. Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí. Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen. Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.  


