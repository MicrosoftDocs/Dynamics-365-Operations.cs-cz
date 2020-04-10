---
title: Hromadné uzavření finančního období
description: Toto téma ukazuje, jak pozdržet nebo trvale uzavřít období nebo více než jednu právnickou osobu současně.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144975"
---
# <a name="mass-financial-period-close"></a>Hromadné uzavření finančního období

[!include [banner](../../includes/banner.md)]

Toto téma ukazuje, jak pozdržet nebo trvale uzavřít období nebo více než jednu právnickou osobu současně. Úkol navíc ukáže, jak omezit skupinu uživatelů, kteří provádějí zaúčtování do konkrétních modulů.

1. V navigačním podokně přejděte na **Moduly > Hlavní kniha > Uzavření období > Kalendáře hlavní knihy**. Všimněte si, že zobrazený seznam právnických osob je závislý na fiskálním kalendáři vybraném na stránce. Zobrazí se pouze právnické osoby používající vybraný fiskální kalendář.
2. Vyberte možnost **Upravit**.
3. Vyberte období, u kterého chcete změnit stav.
4. Vyberte právnické osoby, u kterých chcete aktualizovat stav. Zaškrtnutím políčka v levé horní části mřížky můžete rychle vybrat všechny právnické osoby.  
5. Vyberte možnost **Aktualizovat přístup k modulu** a definujte přístup k vybranému modulu pro zaúčtování. Stav modulu může být také aktualizovaný postupně úpravou záznamů v mřížce. Tlačítko je užitečné, když chcete rychle aktualizovat více záznamů právnické osoby.  
6. V modulu **Aplikace** vyberte nebo zadejte modul, jehož stav chcete aktualizovat. Klepněte na tlačítko **Vybrat**.
7. V poli **Úroveň přístupu** vyberte **Vše**, **Žádná** nebo konkrétní skupinu uživatelů. Klepněte na tlačítko **Vybrat**. Pokud je období otevřené, vše naznačuje tomu, že všichni uživatelé s přístupem k úpravám mohou zaúčtovávat do modulu. Hodnota Žádné označuje, že uživatelé nemůžou zaúčtovávat do modulu, když je období otevřené. Určité uživatelské skupiny určují, že pouze uživatelé ve skupině mohou zaúčtovávat do modulu, pokud je období otevřené.  
8. Vyberte **Aktualizovat**.
9. Vyberte jiné období k aktualizaci stavu.
10. Vyberte právnické osoby, u kterých chcete aktualizovat stav období.
11. Vyberte **Stav aktualizace období** a nastavte stav na **Blokováno**, **Otevřeno** nebo **Trvale uzavřeno**. **Otevřeno** naznačuje, že období lze zaúčtovat, pokud má uživatel přístup. Hodnota **Blokováno** znamená, že období nelze zaúčtovat, ale můžete ho znovu otevřít. **Trvale uzavřeno** znamená, že je období uzavřeno a nikdy je nelze otevřít. Úpravy nelze zaúčtovat. Nedoporučujeme nastavit období na **Trvale uzavřeno**, dokud nejsou dokončeny všechny úpravy a audity.  
12. Vyberte **Aktualizovat**.

