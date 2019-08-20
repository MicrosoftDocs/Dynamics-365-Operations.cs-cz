---
title: Přiřazení uživatelů k rolím zabezpečení
description: Pro přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations Enterprise edition musí být uživateli přiřazeni k rolím zabezpečení.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851352"
---
# <a name="assign-users-to-security-roles"></a>Přiřazení uživatelů k rolím zabezpečení

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pro přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations Enterprise edition musí být uživateli přiřazeni k rolím zabezpečení. Tento postup vysvětluje způsob, jakým správce systému může přiřadit uživatele k rolím automaticky na základě obchodních dat. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="automatically-assign-users-to-roles"></a>Automatické přiřazení uživatelů k rolím
1. Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.
2. Ve stromovém zobrazení vyberte „Vedoucí účetní“. Vyberte roli, pro kterou chcete konfigurovat pravidlo. V tomto příkladu vyberte vedoucí účetní. 
3. Kliknutím na možnost **Přidat pravidlo** otevřete dialogové okno.
4. V seznamu **Vybrat dotaz** najděte a vyberte požadovaný záznam. Vyberte dotaz, který chcete použít pro toto pravidlo.  
5. V seznamu **Název pravidla členství** klikněte na odkaz ve vybraném řádku.
6. Klikněte na **Upravit dotaz**. Podle potřeby upravte dotaz.  
7. Klikněte na tlačítko **OK**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Vyloučení uživatelů z automatického přiřazení k roli
1. Zavřete stránku.
2. Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.
3. Ve stromovém zobrazení vyberte „Vedoucí účetní“. Vyberte požadovanou roli. V tomto příkladu vyberte vedoucí účetní.  
4. V nabídce **role přiřazené uživatelům** vyberte možnost **Ručně přiřadit nebo vyloučit uživatele.**
5. V seznamu **Přiřadit nebo nebo vyloučit uživatele z role** vyberte vybraný řádek. Vyberte uživatele.  
6. V **podokně akcí** vyberte možnost **Vyloučit z role**.
    
    Kliknutím na **Vyloučit z role** vyloučíte vybrané uživatele z role. Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko **Vynulovat stav**. Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí. Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen. Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.  
