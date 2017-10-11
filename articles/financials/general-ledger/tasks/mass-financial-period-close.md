--- 
title: "Hromadné uzavření finančního období"
description: "Tento postup ukazuje, jak pozdržet nebo trvale uzavřít období nebo více než jednu právnickou osobu současně."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b176adc2cbd23647b98cf55e94829e1ea9637c95
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="mass-financial-period-close"></a>Hromadné uzavření finančního období

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak pozdržet nebo trvale uzavřít období nebo více než jednu právnickou osobu současně. Úkol navíc ukáže, jak omezit skupinu uživatelů, kteří provádějí zaúčtování do konkrétních modulů.

1. Přejděte do části Hlavní kniha > Uzávěrka období > Kalendáře hlavní knihy.
    * Všimněte si, že zobrazený seznam právnických osob je závislý na fiskálním kalendáři vybraném na stránce. Zobrazí se pouze právnické osoby používající vybraný fiskální kalendář.  
2. Klikněte na položku Upravit.
3. Vyberte období, u kterého chcete změnit stav.
4. Vyberte právnické osoby, u kterých chcete aktualizovat stav.
    * Zaškrtnutím políčka v levé horní části mřížky můžete rychle vybrat všechny právnické osoby.  
5. Vyberte možnost Aktualizovat přístup k modulu a definujte přístup k vybranému modulu pro zaúčtování.
    * Stav modulu může být také aktualizovaný postupně úpravou záznamů v mřížce. Tlačítko je užitečné, když chcete rychle aktualizovat více záznamů právnické osoby.  
6. V poli Modul aplikace vyberte nebo zadejte modul, jehož stav chcete aktualizovat. Klepněte na tlačítko Vybrat.
7. V poli Úroveň přístupu vyberte Vše, Žádná nebo konkrétní skupinu uživatelů. Klepněte na tlačítko Vybrat.
    * Pokud je období otevřené, vše naznačuje tomu, že všichni uživatelé s přístupem k úpravám mohou zaúčtovávat do modulu. Hodnota Žádné označuje, že uživatelé nemůžou zaúčtovávat do modulu, když je období otevřené. Určité uživatelské skupiny určují, že pouze uživatelé ve skupině mohou zaúčtovávat do modulu, pokud je období otevřené.  
8. Klepněte na položku Aktualizovat.
9. Vyberte jiné období k aktualizaci stavu.
10. Vyberte právnické osoby, u kterých chcete aktualizovat stav období.
11. Vyberte stav aktualizace období a nastavte stav na Blokováno, Otevřeno nebo Trvale uzavřeno.
    * Otevření naznačuje, že období lze zaúčtovat, pokud má uživatel přístup. Hodnota Blokováno znamená, že období nelze zaúčtovat, ale můžete ho znovu otevřít. Trvale uzavřené znamená, že je období uzavřeno a nikdy je nelze otevřít. Úpravy nelze zaúčtovat. Nedoporučujeme nastavit období na Trvale uzavřeno, dokud nejsou dokončeny všechny úpravy a audity.  
12. Klepněte na položku Aktualizovat.

