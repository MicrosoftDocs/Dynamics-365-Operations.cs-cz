---
title: "Workflow výdajů"
description: "Toto téma vysvětluje, jak můžete použít systém workflow v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d60d2f462a1fd27d4655e68aab7f96fb28a34b77
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="expense-workflow"></a>Workflow výdajů

[!include[banner](../includes/banner.md)]

Můžete použít systém workflow v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů. Můžete nastavit workflow, které používá k určení osoby schvalující sestavy výdajů následující kritéria:

- Hierarchie nadřízenosti zaměstnanců a předdefinované schvalovací limity
- Víceúrovňové schválení, které podporuje prozatímního schvalovatele a výsledného schvalovatele
- Finanční dimenze a odpovědnost za projekt
- Přiřazení pro určité uživatele či skupiny uživatelů

Schválení workflowu lze vytvořit pro vyúčtování výdajů, cestovní žádanky, hotovostní zálohy a vratky daně z přidané hodnoty (DPH).

**Příklad**

Následující proces je příkladem workflowu správy výdajů pro vyúčtování výdajů.

1. Zaměstnanec vytvoří a uloží vyúčtování výdajů.
2. Zaměstnanec odešle vyúčtování výdajů ke schválení. Schvalovatel je určen na základě pravidel definovaných při nastavení workflowu.
3. Schvalovatel obdrží oznámení o tom, že vyúčtování výdajů je připraveno ke schválení. Schvalovatel zkontroluje vyúčtování výdajů a ověří, zda jsou splněny následující podmínky:

    - Výdaje neporušují žádné zásady výdajů. Pokud výdaje porušují nějakou zásadu, schvalující ověří, že vyúčtování výdajů obsahuje platné obchodní odůvodnění.
    - Elektronické příjemky jsou připojeny k sestavě výdajů.

4. Schvalovatel schválí vyúčtování výdajů.
5. Vyúčtování výdajů je přiřazeno koordinátoru závazků k zaúčtování.
6. V závislosti na tom, zda je nakonfigurováno automatické zaúčtování, dojde k jednomu z následujících kroků:

    - Pokud je nakonfigurováno automatické zaúčtování, vyúčtování výdajů se zpracovává pro platbu a stav vyúčtování výdajů se zaktualizuje.
    - Pokud není automatické zaúčtování nakonfigurováno, koordinátor závazků ověří, že všechny originály příjemek byly odeslány a že jsou příjemky ve shodě s výdaji na vyúčtování výdajů. Všechny kódy daně, které jsou zadány ve vyúčtování výdajů, musí být ověřeny ohledně správnosti.

Po ověření těchto požadavků dojde k zaúčtování výdajů.

Po zaúčtování výdajů se autorizuje platba za výdaje a zaměstnanci je vyplacena úhrada.

