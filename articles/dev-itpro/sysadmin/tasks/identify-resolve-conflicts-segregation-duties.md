--- 
title: "Identifikace a vyřešení konfliktů v dělení zodpovědnosti"
description: "Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifikace a vyřešení konfliktů v dělení zodpovědnosti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli. Tento koncept se nazývá dělení zodpovědnosti. Pokud definice role zabezpečení nebo přiřazení role uživatele porušuje pravidla, konflikt je zaznamenán. Všechny konflikty musí vyřešit správce. Chcete-li zjistit a vyřešit konflikty, postupujte následujícím způsobem. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Ověření, zda přiřazení rolí uživatelů vyhovují novým pravidlům pro dělení zodpovědnosti
1. Přejděte do nabídky Správa systému > Zabezpečení > Dělení zodpovědnosti > Ověřit plnění přiřazení role uživatele.
2. Klikněte na tlačítko OK.
    * Oznámení zobrazí výsledky ověření.     Dojde-li ke konfliktu, můžete otevřít stránku Uživatelé a změnit přiřazení role uživatele. Konflikty jsou také zaznamenávány na stránce Konflikty dělení zodpovědnosti.     Ke spuštění procesu ověření jako dávkové úlohy vyberte Dávkového zpracování a poté nastavte ostatní parametry dávky. Po dokončení dávkové úlohy můžete zkontrolovat konflikty na stránce Konflikty dělení zodpovědnosti.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Zobrazení a vyřešení konfliktních přiřazení rolí uživatelů
1. Přejděte do nabídky Správa systému > Zabezpečení > Dělení zodpovědnosti > Konflikty dělení zodpovědnosti.
    * Vyberte konflikt a klikněte na některé z následujících tlačítek:     Odepřít přiřazení - Odepře přiřazení uživatele k další roli zabezpečení. Pokud odmítnete automatické přiřazení role, uživatel bude označen jako vyloučený z role. Vyloučenému uživateli není udělen přístup, který je přidružený k roli, a uživatel nemůže být přiřazen k roli, dokud správce vyloučení neodstraní.     Povolit přiřazení: Přepíše konflikt a povolí přiřazení uživatele k oběma rolím zabezpečení. Pokud přepíšete konflikt, je nutné zadat důvod do pole Důvod pro přepsání.  
2. Zavřete stránku.
3. Přejděte do nabídky Správa systému > Zabezpečení > Dělení zodpovědnosti > Nevyřešené konflikty dělení zodpovědnosti.
    * Vyberte konflikt a klikněte na některé z následujících tlačítek:     Odepřít přiřazení - Odepře přiřazení uživatele k další roli zabezpečení. Pokud odmítnete automatické přiřazení role, uživatel bude označen jako vyloučený z role. Vyloučenému uživateli není udělen přístup, který je přidružený k roli, a uživatel nemůže být přiřazen k roli, dokud správce vyloučení neodstraní.     Povolit přiřazení: Přepíše konflikt a povolí přiřazení uživatele k oběma rolím zabezpečení. Pokud přepíšete konflikt, je nutné zadat důvod do pole Důvod pro přepsání.    
4. Zavřete stránku.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Ověření, zda existující role vyhovují novým pravidlům pro dělení zodpovědnosti
1. Přejděte do nabídky Správa systému > Zabezpečení > Dělení zodpovědnosti > Pravidla dělení zodpovědnosti.
    * Vyberte pravidlo.  
2. Klikněte na možnost Ověřit zodpovědnosti a role.
    * Pokud jakákoli stávající role porušila vybrané pravidlo, zobrazí se zpráva obsahující název role a názvy konfliktních zodpovědností. Správce musí určit snížení rizika zabezpečení nebo upravit roli tak, aby neporušovala pravidla dělení zodpovědnosti.     Pokud vybrané pravidlo není porušeno žádnou rolí, zpráva zobrazí informaci, že všechny role jsou kompatibilní.  


