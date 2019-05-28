---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (11. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a89ba455acbed9724da6826ac4d41c6a481490
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517492"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (11. ledna 2019)

[!include [banner](includes/banner.md)]

**Sestavení 8.1.2100**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="changes"></a>Změny

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Ověření požadavků na dovolenou prostřednictvím předpovědi dostupného zůstatku
Změny provedené v této verzi umožní zaměstnancům vyžádat si budoucí dovolenou bez odečtení od aktuálního zůstatku. Použijí se standardní workflow pro všechny budoucí žádosti. Další informace naleznete v tématu [Časové rozlišení volna na základě odpracovaných hodin](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Zobrazení předpovídaného zůstatku dovolené v modulu ESS a People
Tato funkce umožňuje zobrazení zůstatků za období dovolené budoucími manažery lidských zdrojů, vedoucími a zaměstnanci. Zaměstnanci mohou zobrazit budoucí zůstatky v pracovním prostoru **Samoobsluha zaměstnanců** a personalisté mají přístup ke stejnými informacím pomocí pracovní plochy **Lidé**.

### <a name="notifications-for-changing-leave-balances"></a>Upozornění na změnu zůstatků dovolené
Zůstatky dovolené zobrazí aktuální zůstatek zaměstnance. Budoucí zůstatky jsou dostupné v pracovních prostorech **Samoobslužný portál zaměstnanců** a **Lidé** po zadání hodnoty "K datu" pro výpočet předpovídaného zůstatku.

Byla přidána navigace k zobrazení předpovídaných zůstatků v následujících oblastech:
  - Karta **Pracovní volno** v pracovním prostoru **samoobslužný servis zaměstnance**.
  - Karta **Dovolená a absence** v pracovním prostoru **Správa samoobslužného prostoru**.
  - Stránka **Dovolená a absence** v pracovním prostoru **Lidé**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Povolení desetinných míst pro plány variabilní kompenzace (platební plány)
Odměny a plány variabilního odměňování mají další flexibilitu pro částky a přepisy hodnot s desetinnými místy.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Po uložení plánu nelze změnit data registrací variabilního odměňování
Tato změna umožňuje aktualizace koncového data plánu (rozšířené nebo s ukončenou platností) po uložení plánu. Je možné stále aktivovat nebo deaktivovat plány nezávisle na počátečním a koncovém datu.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Mzdové informace, které jsou k dispozici při přiřazení role zabezpečení Správce mezd
Role správce mezd byla aktualizována tak, aby měla přístup k informacím o mzdám během procesu žádosti.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Samoobsluha pro zaměstnance | rozbalení hierarchie pozic z dlaždic se nedaří získat nadřazený uzel
Byly provedeny změny pro účely odstranění chyby, která nastala při přidávání hierarchie pozice do nového pracovního prostoru a navigaci v rámci organizační struktury.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Používá se nová zpráva o ověření při použití pořadí čísel pracovníků
Byla provedena změna k objasnění, jaký je problém při náboru zaměstnanci v případě, že se používá nové číslo personálu.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Samoobslužný pracovní prostor zaměstnance vybraný jako počáteční stránka spuštění
Když je jako počáteční stránka pro spuštění uživatele vybrán pracovní prostor **Samoobsluha zaměstnance** a tento uživatel nemá přiřazenou roli zaměstnance, systém se přesměruje na výchozí řídicí panel.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Kód důvodu výpovědi aktualizuje záznam o přiřazení pozice
Kód důvodu výpovědi bude nyní aktualizovat přiřazení pozice při výpovědi pro zaměstnance a ukončení pozice. 
