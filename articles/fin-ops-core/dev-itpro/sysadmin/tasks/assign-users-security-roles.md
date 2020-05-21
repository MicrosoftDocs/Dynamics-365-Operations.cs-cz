---
title: Přiřazení uživatelů k rolím zabezpečení
description: Pro přístup k aplikacím Finance and Operations musí být uživateli přiřazeni k rolím zabezpečení.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0421ad6c932f2c91de51169bda6c98f53d3bc65
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346438"
---
# <a name="assign-users-to-security-roles"></a>Přiřazení uživatelů k rolím zabezpečení

[!include [banner](../../includes/banner.md)]

Chcete-li v aplikacích Finance and Operations použít cokoli jiného než společné funkce, musí být uživatelům přiřazeny k role zabezpečení. Uživatele můžete k rolím přiřadit automaticky, na základě pravidel a obchodních údajů, vyloučit uživatele z automatického přiřazování rolí nebo přidat uživatele do rolí ručně.

## <a name="automatically-assign-users-to-roles"></a>Automatické přiřazení uživatelů k rolím
Tento postup vysvětluje způsob, jakým správce systému může automaticky přiřadit uživatele k rolím automaticky na základě obchodních dat. 
1. Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.
2. Ve stromovém zobrazení vyberte „Vedoucí účetní“. Vyberte roli, pro kterou chcete konfigurovat pravidlo. V tomto příkladu vyberte vedoucí účetní. 
3. Výběrem možnosti **Přidat pravidlo** otevřete nabídku dialogového okna.
4. V seznamu **Vybrat dotaz** najděte a vyberte požadovaný záznam. Vyberte dotaz, který chcete použít pro toto pravidlo.  
5. V seznamu **Název pravidla členství** klikněte na odkaz ve vybraném řádku.
6. Vyberte **Upravit dotaz**. Podle potřeby upravte dotaz.  
7. Vyberte **OK**.
8. Vyberte **Spustit automatické přiřazení role**.
9. Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé** (nejlépe na kartě samostatného prohlížeče).
10. Zkontrolujte role přiřazené různým uživatelům a potvrďte, že dotaz na přiřazení role byl správný. V případě potřeby je upravte a spusťte znovu.

## <a name="exclude-users-from-automatic-role-assignment"></a>Vyloučení uživatelů z automatického přiřazení k roli
1. Zavřete stránku.
2. Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.
3. Ve stromovém zobrazení vyberte „Vedoucí účetní“. Vyberte požadovanou roli. V tomto příkladu vyberte vedoucí účetní.  
4. V nabídce **role přiřazené uživatelům** vyberte možnost **Ručně přiřadit nebo vyloučit uživatele.**
5. V seznamu **Přiřadit nebo nebo vyloučit uživatele z role** vyberte vybraný řádek. Vyberte uživatele.  
6. V **podokně akcí** vyberte možnost **Vyloučit z role**.
7. Kliknutím na **Vyloučit z role** vyloučíte vybrané uživatele z role. Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko **Vynulovat stav**. Při odebírání vyloučení obnovením stavu uživatele se role uživatele automaticky přiřadí. Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen. Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.  

## <a name="manually-assign-users-to-roles"></a>Ruční přiřazení uživatelů k rolím
Uživatelé, kteří jsou ručně přiřazeni k rolím zabezpečení, musí být také ručně odebráni správcem. Tito uživatelé nejsou z rolí odstraněni pravidly pro automatické přiřazování rolí.

1. Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.
2. Ve stromu vyberte roli a v nabídce **Role přiřazené uživatelům** vyberte možnost **Ručně přiřadit nebo vyloučit uživatele.**
4. V poli **Přiřadit uživatele k roli nebo je vyloučit z role** jsou uvedeni uživatelé, jimž nebyla role přiřazena, s **režimem přiřazení** nastaveným na **Žádný**. Vyberte jednoho nebo více uživatelů, kterým má být role přiřazena.
5. V **podokně akcí** vyberte možnost **Přiřadit k roli**. **Režim přiřazení** se aktualizuje na **Ruční** a uživatelům je nyní přiřazena nová role.
