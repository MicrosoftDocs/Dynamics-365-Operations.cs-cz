---
title: Identifikace a vyřešení konfliktů v dělení zodpovědnosti
description: Toto téma vysvětluje, jak identifikovat a vyřešit konflikty v dělení zodpovědnosti.
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70fe3bb707f2f204cda92ec979fe9fe1a3b96bac
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143597"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifikace a vyřešení konfliktů v dělení zodpovědnosti

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak identifikovat a vyřešit konflikty v dělení zodpovědnosti. Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli. Tento koncept se nazývá dělení zodpovědnosti. Pokud definice role zabezpečení nebo přiřazení role uživatele porušuje pravidla, konflikt je zaznamenán. Všechny konflikty musí vyřešit správce. Chcete-li zjistit a vyřešit konflikty, postupujte následujícím způsobem. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Ověření, zda přiřazení rolí uživatelů vyhovují novým pravidlům pro dělení zodpovědnosti
1. Přejděte na **Podokno navigace > Moduly > Správa systému > Zabezpečení > Dělení zodpovědnosti > Ověřit plnění přiřazení role uživatele**.
2. Vyberte **OK**. Oznámení zobrazí výsledky ověření. Dojde-li ke konfliktu, můžete otevřít stránku **Uživatelé** a změnit přiřazení role uživatele. Konflikty jsou také zaznamenávány na stránce **Konflikty dělení zodpovědnosti**. Ke spuštění procesu ověření jako dávkové úlohy vyberte **Dávkové zpracování** a poté nastavte ostatní parametry dávky. Po dokončení dávkové úlohy můžete zkontrolovat konflikty na stránce **Konflikty dělení zodpovědnosti**.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Zobrazení a vyřešení konfliktních přiřazení rolí uživatelů
1. Přejděte do nabídky **Podokno navigace > Správa systému > Zabezpečení > Dělení zodpovědnosti > Konflikty dělení zodpovědnosti.** Vyberte konflikt a zvolte některé z následujících tlačítek: **Odepřít přiřazení - Odepře přiřazení uživatele k další roli zabezpečení**. Pokud odmítnete automatické přiřazení role, uživatel bude označen jako vyloučený z role. Vyloučenému uživateli není udělen přístup, který je přidružený k roli, a uživatel nemůže být přiřazen k roli, dokud správce vyloučení neodstraní. Povolit přiřazení **Přepíše** konflikt a povolí přiřazení uživatele k oběma rolím zabezpečení. Pokud přepíšete konflikt, je nutné zadat důvod do pole **Důvod pro přepsání**.  
2. Zavřete stránku.
3. Přejděte do nabídky **Podokno navigace > Správa systému > Zabezpečení > Dělení zodpovědnosti > Nevyřešené konflikty dělení zodpovědnosti.** Vyberte konflikt a zvolte některé z následujících tlačítek: **Odepřít přiřazení - Odepře přiřazení uživatele k další roli zabezpečení**. Pokud odmítnete automatické přiřazení role, uživatel bude označen jako vyloučený z role. Vyloučenému uživateli není udělen přístup, který je přidružený k roli, a uživatel nemůže být přiřazen k roli, dokud správce vyloučení neodstraní. Povolit přiřazení **Přepíše** konflikt a povolí přiřazení uživatele k oběma rolím zabezpečení. Pokud přepíšete konflikt, je nutné zadat důvod do pole **Důvod pro přepsání**.    
4. Zavřete stránku.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Ověření, zda existující role vyhovují novým pravidlům pro dělení zodpovědnosti
1. Přejděte do nabídky **Podokno navigace > Správa systému > Zabezpečení > Dělení zodpovědnosti > Pravidla dělení zodpovědnosti.** Vyberte pravidlo.  
2. Zvolte **Ověřit zodpovědnosti a role**. Pokud jakákoli stávající role porušila vybrané pravidlo, zobrazí se zpráva obsahující název role a názvy konfliktních zodpovědností. Správce musí určit snížení rizika zabezpečení nebo upravit roli tak, aby neporušovala pravidla dělení zodpovědnosti. Pokud vybrané pravidlo není porušeno žádnou rolí, zpráva zobrazí informaci, že všechny role jsou kompatibilní.  

