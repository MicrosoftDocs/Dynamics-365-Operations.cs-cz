---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (15. listopadu 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b90d4230fe1e666aba4075670f6df206e8df7ce9
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "857305"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (15. listopadu 2018)

[!include [banner](includes/banner.md)]

**Sestavení 8.1.2045**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="other-changesfixes"></a>Další změny/opravy

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Nelze změnit aktuální pozici zaměstnance na budoucí otevřenou pozici

Byla provedena změna, která povoluje převody pozic, když je pozice dostupná pouze v budoucnu. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Při vytvoření nového zaměstnance se nezobrazuje pozice

Byly provedeny změny za účelem všech otevřených pozic, které jsou dostupné pro přiřazení při náboru nového zaměstnance v aplikaci Talent. To zahrnuje historické pozice nebo pozice s budoucí datem. Pozice se zobrazí nyní správně na základě počátečního data zaměstnání. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Datum ukončení se zobrazuje na základě nastavení uživatele

Byla provedena změna seznamu bývalých zaměstnanců, aby byly vysvětleny posuny časových zón u časových zón preferovaných zaměstnanci při zobrazení data ukončení.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Odkazy na pracovní položky přiřazené mně nezobrazují správné informace

Při této změně navigace k podrobnostem jednotlivých pracovních položek v seznamu zobrazí správné informace pro vybranou položku. K tomuto problému dochází pouze u rozšířených možností zabezpečení.


## <a name="known-issue"></a>Známý problém

- **Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě. 
- **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**. Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici. (Tento problém bude opraven v další aktualizaci Platform Update.)
