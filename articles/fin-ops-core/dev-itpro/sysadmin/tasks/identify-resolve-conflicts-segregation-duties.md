---
title: Identifikace a vyřešení konfliktů v dělení zodpovědnosti
description: Toto téma vysvětluje, jak identifikovat a vyřešit konflikty v dělení zodpovědnosti.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826361"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifikace a vyřešení konfliktů v dělení zodpovědnosti

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak identifikovat a vyřešit konflikty v dělení zodpovědnosti. Můžete nastavit pravidla k oddělení zodpovědností, které musí být prováděny různými uživateli. Tento koncept se nazývá dělení zodpovědnosti. Pokud definice role zabezpečení nebo přiřazení role uživatele porušuje pravidla, konflikt je zaznamenán. Všechny konflikty musí vyřešit správce. Chcete-li zjistit a vyřešit konflikty, postupujte následujícím způsobem.

Po přidání pravidla ověřte, zda jsou všechny existující role kompatibilní. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Ověření, zda existující role a zodpovědnosti vyhovují novým pravidlům pro dělení zodpovědnosti
1. Přejděte do nabídky **Správa systému** > **Zabezpečení** > **Dělení zodpovědnosti** > **Pravidla dělení zodpovědnosti**.
3. Zvolte **Ověřit zodpovědnosti a role**. Pokud jakákoli role porušila pravidla, zobrazí se zpráva obsahující název pravidla, roli a názvy konfliktních zodpovědností. Konfliktní role musí být upraveny pomocí **Konfigurace zabezpečení** a nemůže zahrnovat konfliktní zodpovědnosti. Pokud vybrané pravidlo není porušeno žádnou rolí, zpráva zobrazí informaci, že všechny role jsou kompatibilní.   

> [!NOTE]
> Ověření se provádí pouze pro vybrané pravidlo. Je důležité ověřit dodržování předpisů pro každé pravidlo.   

Když vytvoříte nebo upravíte roli, pravidla pro oddělení povinností se automaticky vynucují. Roli nemůžete přiřadit konfliktní povinnosti.

Dále ověřte, zda jsou všechna existující přiřazení rolí kompatibilní.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Ověření, zda přiřazení rolí uživatelů vyhovují novým pravidlům pro dělení zodpovědnosti
1. Přejděte do nabídky **Správa systému > Zabezpečení > Dělení zodpovědnosti > Ověřit plnění přiřazení role uživatele**.
2. Vyberte **OK**. Oznámení zobrazí výsledky ověření. Konflikty jsou zaznamenávány na stránce **Nevyřešené konflikty dělení zodpovědnosti**.   

Když přiřadíte uživatele rolím, pravidla pro dělení zodpovědnosti se automaticky vynucují. Pokud se pokusíte přiřadit uživatele k rolím, které obsahují konfliktní povinnosti, zobrazí se chybová zpráva. Poté musíte konflikt vyřešit odmítnutím nebo povolením dalšího přiřazení role. Další role bude přidělena po povolení přiřazení. 

> [!NOTE]
> Konflikty nejsou aktuálně ověřeny pro uživatele, kterým jsou přiřazeny role na základě skupin domén služby Active Directory.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Zobrazení a vyřešení konfliktních přiřazení rolí uživatelů
1. Přejděte do nabídky **Správa systému** > **Zabezpečení** > **Dělení zodpovědnosti** > **Nevyřešené konflikty dělení zodpovědnosti**. 
2. Vyberte konflikt a vyberte některou z následujících akcí: 

  - **Odepřít přiřazení** – Odepře přiřazení uživatele k další roli zabezpečení. Pokud odmítnete automatické přiřazení role, uživatel bude označen jako vyloučený z role. Vyloučenému uživateli není udělen přístup, který je přidružený k roli, a uživatel nemůže být přiřazen k roli, dokud správce vyloučení neodstraní. 
-  **Povolit přiřazení** Přepíše konflikt a povolí přiřazení uživatele k další roli zabezpečení. Pokud přepíšete konflikt, je nutné zadat důvod do pole **Důvod pro přepsání**. Všechna přepsaná přiřazení rolí lze zobrazit na stránce **Rozdělení konfliktů povinností**.  

> [!NOTE]
> Pokud je u stejného uživatele uvedeno několik konfliktů, vyberte záznam uživatele a vyhodnoťte přiřazené role na stránce **Uživatelé**. Abyste se tomuto konfliktu vyhnuli, ověřte každé pravidlo po jeho přidání nebo úpravě.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]