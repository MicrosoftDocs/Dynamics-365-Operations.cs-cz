---
title: Zpracování deníku přidělení hlavní knihy
description: Toto téma vysvětluje, jak zpracovat požadavek přidělení v aplikaci Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186065"
---
# <a name="process-ledger-allocation-journal"></a>Zpracování deníku přidělení hlavní knihy

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak zpracovat požadavek na přidělení. Použijte stránku Požadavek na přidělení procesu k vytvoření deníku přidělování, který lze před zaúčtováním do hlavní knihy zkontrolovat a schválit nebo přímo zaúčtovat do hlavní knihy. Předtím, než budete moci vytvořit deník přidělení, je nejprve nutné mít aktivní alespoň jedno pravidlo přidělení hlavní knihy. Tento úkol využívá ukázkovou společnost USMF.

1. V navigačním podokně přejděte na **Moduly > Hlavní kniha > Přidělení > Zpracovat požadavek na přidělení**.
2. V poli **Pravidlo** vyberte požadovaný záznam v rozevírací nabídce.
3. Do pole **K datu** zadejte datum.

    - Pole **K datu** je velmi důležité, když je hlavní kniha zdrojem dat pro pravidlo. Toto datum určuje, jaké zůstatky hlavní knihy budou zahrnuty do přidělení.  
    - V poli **Nulový zdroj** vyberte **Zastavit**. To zastaví proces přidělování a zobrazí zprávu informující o tom, že je vybrána nulová zdrojová částka.  

4. V poli **Možnosti návrhu** vyberte **Pouze návrh**. Vyberte **Pouze návrh** pro kontrolu a volitelné schválení výsledku v Denících přidělení před zaúčtováním přidělení do hlavní knihy.  
5. Zadejte datum do pole Datum zaúčtování do hlavní knihy.
6. Vyberte **OK**.
7. V navigačním podokně přejděte na **Moduly > Hlavní kniha > Přidělení > Deníky přidělení**.
8. Vybrat **řádky**.
9. Zvolte **Zaúčtovat**.
10. Zvolte **Zaúčtovat**.
