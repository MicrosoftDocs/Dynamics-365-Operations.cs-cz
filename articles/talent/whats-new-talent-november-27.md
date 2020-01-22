---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (27. listopadu 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897481"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (27. listopadu 2018)

**Sestavení 8.1.2064**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.


## <a name="changes"></a>Změny

### <a name="unable-to-create-a-note-in-case-management"></a>Nelze vytvořit poznámku ve správě případu

Byla provedena změna kvůli problému při pokusu o úpravu nebo vytvoření poznámky v protokolu případů ve správě případu.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Překlep ve slově na kartě analýzy v pracovním prostoru kompenzace 

Byla provedena oprava pravopisu u Ethnic Origin v grafu analýzy kompenzace v pracovním prostoru kompenzace.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Pracovní prostor samoobsluhy pro zaměstnance se nezobrazuje, když není uživatel přiřazen k pracovníkovi 

Byla provedena změna, když je zvolen pracovní prostor **Samoobsluha pro zaměstnance** jako počáteční stránka při spuštění pro uživatele, který není přiřazen k pracovníkovi. V takovém případě se zobrazí výchozí řídicí panel.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Pracovní volno a absence - chyba: Odkaz na objekt není nastaven na instanci objektu.

Pro pracovní volno a absence byly provedeny změny za účelem opravy této chyby po schválení záznamů pracovního volna a absence v seznamu **Pracovní položky přiřazené mně**.

### <a name="unable-to-recall-an-image-workflow"></a>Nelze vyvolat workflow obrázku

Po vyvolání workflow obrázku bude workflow nastaveno na zrušené a stávající požadavek lze odstranit v pracovním prostoru samoobsluhy pro zaměstnance.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Opětovně přijatí zaměstnanci nebo dodavatelé se zobrazují po jejich skončení několikrát 

V této aktualizaci se ukončení zaměstnanci, kteří jsou opět přijati, zobrazí v ukončeném seznamu pouze jednou. 

## <a name="known-issue"></a>Známý problém

- **Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě. 
- **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**. Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici. (Tento problém bude opraven v další aktualizaci Platform Update.)
