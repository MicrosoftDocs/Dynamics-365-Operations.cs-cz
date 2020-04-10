---
title: Workflow správy výdajů
description: Toto téma vysvětluje, jak můžete použít systém workflow v aplikaci Microsoft Dynamics 365 Finance pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153964"
---
# <a name="expense-management-workflow"></a>Workflow správy výdajů

[!include [banner](../includes/banner.md)]

Můžete použít systém workflow pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů. Můžete nastavit workflow, které používá k určení osoby schvalující sestavy výdajů následující kritéria:

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
