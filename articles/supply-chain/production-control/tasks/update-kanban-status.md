---
title: Aktualizace stavu kanbanu
description: Pokud dojde omylem k vyprázdnění kanbanu nebo přijatý kanban musí být prázdný, je nutné aktualizovat stav kanbanu.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 741a2a29e6b222c722e94db4e07dee6c8f4014030364753e3352fa30594dac0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715667"
---
# <a name="update-kanban-status"></a>Aktualizace stavu kanbanu

[!include [banner](../../includes/banner.md)]

Pokud dojde omylem k vyprázdnění kanbanu nebo přijatý kanban musí být prázdný, je nutné aktualizovat stav kanbanu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro vedoucího dílny.


## <a name="find-the-kanban"></a>Vyhledejte kanban.
1. Přejděte na Řízení výroby > Kanban > Kanbany.
2. Otevřete filtr sloupce Stav manipulační jednotky.
3. Klikněte na tlačítko Vymazat.
    * To obnoví hodnoty filtrů.  
4. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole Číslo karty pomocí hodnoty „000149“.

## <a name="change-emptied-status-to-received-status"></a>Změna stavu Vyprázdněno na Přijato
1. Klikněte na Stornovat prázdnou manipulační jednotku.
2. Klikněte na tlačítko OK.
    * Všimněte si, že stav manipulační jednotky je Přijato.  

## <a name="change-received-status-to-emptied-status"></a>Změna stavu Přijato na Vyprázdněno
1. Klikněte na Prázdný kanban.
2. Označte v seznamu vybraný řádek.
    * Všimněte si, že stav manipulační jednotky je Vyprázdněno.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]