---
title: Zpracování deníku přidělení hlavní knihy
description: Tento článek vysvětluje, jak zpracovat požadavek přidělení v aplikaci Dynamics 365 Finance.
author: aprilolson
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779385"
---
# <a name="process-ledger-allocation-journal"></a>Zpracování deníku přidělení hlavní knihy

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak zpracovat požadavek na přidělení. Použijte stránku **Požadavek na přidělení procesu** k vytvoření deníku přidělování, který lze před zaúčtováním do hlavní knihy zkontrolovat a schválit nebo přímo zaúčtovat do hlavní knihy. Předtím, než budete moci vytvořit deník přidělení, je nejprve nutné mít aktivní alespoň jedno pravidlo přidělení hlavní knihy. Tento úkol využívá ukázkovou společnost USMF.

1. V navigačním podokně přejděte na **Hlavní kniha > Přidělení > Zpracovat požadavek na přidělení**.
2. V poli **Pravidlo** vyberte požadovaný záznam v rozevírací nabídce.
3. Do pole **K datu** zadejte datum.

    - Pole **K datu** je velmi důležité, když je hlavní kniha zdrojem dat pro pravidlo. Toto datum určuje, jaké zůstatky hlavní knihy budou zahrnuty do přidělení.  
    - V poli **Nulový zdroj** vyberte **Zastavit**. To zastaví proces přidělování a zobrazí zprávu informující o tom, že je vybrána nulová zdrojová částka.  

4. V poli **Možnosti návrhu** vyberte **Pouze návrh**. Vyberte **Pouze návrh** pro kontrolu a volitelné schválení výsledku v **Denících přidělení** před zaúčtováním přidělení do hlavní knihy.  
5. Zadejte datum do pole **Datum zaúčtování do hlavní knihy**.
6. Vyberte **OK**.
7. V navigačním podokně přejděte na **Moduly > Hlavní kniha > Přidělení > Deníky přidělení**.
8. Vybrat **řádky**.
9. Zvolte **Zaúčtovat**.
10. Zvolte **Zaúčtovat**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
