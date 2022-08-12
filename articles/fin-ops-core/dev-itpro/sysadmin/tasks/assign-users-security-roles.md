---
title: Přiřadit uživatelů k rolím zabezpečení
description: Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k finančním a provozním aplikacím.
author: Peakerbl
ms.date: 02/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5e69a79f123daff3f85d0100647615ad818288e
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103861"
---
# <a name="manage-users-and-security-roles"></a>Správa uživatelů a rolí zabezpečení

[!include [banner](../../includes/banner.md)]

Chcete-li ve finančních a provozních aplikacích použít cokoli jiného než společné funkce, musejí být uživatelé přiřazeni k rolím zabezpečení. Uživatele můžete k rolím přiřadit automaticky, na základě pravidel a obchodních údajů, vyloučit uživatele z automatického přiřazování rolí nebo přidat uživatele do rolí ručně.

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
Tento postup vysvětluje, jak vyloučit uživatele z automatického přidělování rolí.

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

## <a name="manually-remove-users-from-roles"></a>Ruční odebrání uživatele z rolí
Uživatelé, kteří jsou ručně přiřazeni k rolím zabezpečení, musí být také ručně odebráni správcem. Tito uživatelé nejsou z rolí odstraněni pravidly pro automatické přiřazování rolí.

1. Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.
2. Chcete-li odebrat jednoho uživatele, postupujte takto:
   1. Ve stromu vyberte roli. 
   2. V oblasti **Uživatelé přiřazení k roli** vyberte uživatele, který má být odebrán.
   3. Vyberte položku **Odstranit** a uživatel je poté odebrán z role.
3. Chcete-li odebrat více uživatelů, postupujte takto:
   1. Ve stromu vyberte roli. 
   2. V oblasti **Uživatelé přiřazení k roli** vyberte možnost **Ručně přiřadit nebo vyloučit uživatele**.
   3. Na stránce **Přiřadit uživatele k roli nebo je vyloučit z role** mají uživatelé, jimž nebyla žádná role přiřazena, ve sloupci **Režim přiřazení** hodnotu **Žádný**. Vyberte uživatele, kteří mají být vyloučeni z role.
   4. V **podokně akcí** vyberte možnost **Vyloučit z role**. Sloupec **Režim přiřazení** se nyní aktualizuje na **Ruční** a uživatelé jsou odebráni z role.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

