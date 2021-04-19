---
title: Nastavení programů kontinuity pro kontaktní střediska
description: Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e7f90e919133fd7443083261a325b285b3abb75b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791023"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>Nastavení programů kontinuity pro kontaktní střediska

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko.

V rámci programu trvání, který je znám také jako program opakování objednávky, mohou odběratelé přijímat pravidelné dodávky produktu podle předem určeného plánu. Jednotlivé dodávky mohou obsahovat různé produkty, stejně jako v případě klub „kniha měsíce“ nebo je možné opakovaně odesílat stejný výrobek. K nastavení programu trvání je třeba dokončit následující úlohy.

1. Nastavte parametry programu trvání na stránce **Parametry kontaktního střediska**.
2. Vytvořte program trvání, který určuje podrobnosti, jako je platební kalendář, časové období dodávky a zda probíhá účtování předem. Je také nutné přidat seznam produktů, které spadají do programu trvání. Každý výrobek obdrží číslo ID události přiřazené postupně, počínaje 1. ID události určí pořadí, ve kterém jsou výrobky odesílány.

    - Pokud zákazníci obdrží různé produkty v rámci jednotlivých dodávek, produkty jsou odeslány v postupném pořadí podle jejich ID události a počínaje aktuální událostí.
    - Pokud odběratelé přijímají stejný produkt v rámci každé dodávky, bude seznam obsahovat pouze jeden produkt, který má jedno ID události. Stejná událost se děje opakovaně. Můžete zadat počet opakování každé události.

3. Vytvořte nadřazený produkt, který představuje program trvání vytvořený v úkolu 2. Pokud přidáte tento produkt do prodejní objednávky, otevře se stránka **Trvání**. Tuto stránku můžete poté použít k vytvoření samotné trvalé objednávky. Nadřazený produkt neurčuje jednotlivé produkty, které odběratel obdrží v jednotlivých dodávkách.

Poté, co jste nastavili program trvání podle pokynů výše, můžete vytvořit trvalou objednávku pro odběratele. Je také třeba provádět následující úlohy údržby.

- **Aktualizujte aktuální období trvalé události** – nastavte dávkovou úlohu, která systém informuje o tom, jaké je aktuální období události.
- **Vytvořte podřízené trvalé objednávky** – vytvořte podřízené objednávky z nadřazených trvalých objednávek.
- **Zpracujte trvalé platby** – zpracování fakturace a oznámení pro platby, které jsou přidruženy k prodejním trvalým objednávkám.
- **Rozšiřte řádky trvání** (je-li vyžadováno) – zvyšte počet opakování povolených u trvalé události. Opakování dodávky lze poté překročit přes limit, který byl nastaven v poli **Prahová hodnota opakování trvalé položky** v parametrech kontaktního střediska.
- **Proveďte aktualizaci trvání** (je-li vyžadováno) – synchronizujte změny mezi programem trvání a nadřazenými trvalými prodejními objednávkami.
- **Zavřete nadřazené řádky trvání a objednávky** – zavřete trvalé objednávky.


[!INCLUDE[footer-include](../includes/footer-banner.md)]