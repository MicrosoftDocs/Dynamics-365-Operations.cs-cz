---
title: "Nastavení programu trvání pro kontaktní středisko"
description: "Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00504b62237ac4f121d603d5144ffa4e71956cc3
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Nastavení programu trvání pro kontaktní středisko

[!include[banner](includes/banner.md)]


Tento článek popisuje, jak lze nastavit program trvání pro kontaktní středisko.

V rámci programu trvání, který je znám také jako program opakování objednávky, mohou odběratelé přijímat pravidelné dodávky produktu podle předem určeného plánu. Jednotlivé dodávky mohou obsahovat různé produkty, stejně jako v případě klub „kniha měsíce“ nebo je možné opakovaně odesílat stejný výrobek. K nastavení programu trvání je třeba dokončit následující úlohy.

1.  Nastavte parametry programu trvání na stránce **Parametry kontaktního střediska**.
2.  Vytvořte program trvání, který určuje podrobnosti, jako je platební kalendář, časové období dodávky a zda probíhá účtování předem. Je také nutné přidat seznam produktů, které spadají do programu trvání. Každý výrobek obdrží číslo ID události přiřazené postupně, počínaje 1. ID události určí pořadí, ve kterém jsou výrobky odesílány.
    -   Pokud zákazníci obdrží různé produkty v rámci jednotlivých dodávek, produkty jsou odeslány v postupném pořadí podle jejich ID události a počínaje aktuální událostí.
    -   Pokud odběratelé přijímají stejný produkt v rámci každé dodávky, bude seznam obsahovat pouze jeden produkt, který má jedno ID události. Stejná událost se děje opakovaně. Můžete zadat počet opakování každé události.

3.  Vytvořte nadřazený produkt, který představuje program trvání vytvořený v úkolu 2. Pokud přidáte tento produkt do prodejní objednávky, otevře se stránka **Trvání**. Tuto stránku můžete poté použít k vytvoření samotné trvalé objednávky. Nadřazený produkt neurčuje jednotlivé produkty, které odběratel obdrží v jednotlivých dodávkách.

Poté, co jste nastavili program trvání podle pokynů výše, můžete vytvořit trvalou objednávku pro odběratele. Je také třeba provádět následující úlohy údržby.

-   **Aktualizujte aktuální období trvalé události** – nastavte dávkovou úlohu, která systém informuje o tom, jaké je aktuální období události.
-   **Vytvořte podřízené trvalé objednávky** – vytvořte podřízené objednávky z nadřazených trvalých objednávek.
-   **Zpracujte trvalé platby** – zpracování fakturace a oznámení pro platby, které jsou přidruženy k prodejním trvalým objednávkám.
-   **Rozšiřte řádky trvání** (je-li vyžadováno) – zvyšte počet opakování povolených u trvalé události. Opakování dodávky lze poté překročit přes limit, který byl nastaven v poli **Prahová hodnota opakování trvalé položky** v parametrech kontaktního střediska.
-   **Proveďte aktualizaci trvání** (je-li vyžadováno) – synchronizujte změny mezi programem trvání a nadřazenými trvalými prodejními objednávkami.
-   **Zavřete nadřazené řádky trvání a objednávky** – zavřete trvalé objednávky.





