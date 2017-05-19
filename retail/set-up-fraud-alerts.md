---
title: "Nastavit upozornění na podvod"
description: "Toto téma vysvětluje, jak nastavit pravidla výstrahy pro zástupce z oddělení služeb zákazníkům zaměřené na potenciálně podvodné informace při zpracování objednávek. Můžete definovat zvláštní kódy, které jsou automaticky nebo ručně použity k blokování podezřelých objednávek."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ddcf68b9d9d35d63cb092225d468dd4a6a3d4446
ms.contentlocale: cs-cz
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-fraud-alerts"></a>Nastavit upozornění na podvod

[!include[banner](includes/banner.md)]


Toto téma vysvětluje, jak nastavit pravidla výstrahy pro zástupce z oddělení služeb zákazníkům zaměřené na potenciálně podvodné informace při zpracování objednávek. Můžete definovat zvláštní kódy, které jsou automaticky nebo ručně použity k blokování podezřelých objednávek. 

Před nastavením a použitím pravidel pro zjišťování podvodů musíte povolit zjišťování podvodů a definovat základní hodnoty zjišťování podvodů v parametrech kontaktních středisek. Existují dva typy pravidel podvodů:

-   **Statická pravidla** používají určitou hodnotu, jako je například telefonní číslo, které má být zakázáno.
-   **Dynamická pravidla** mohou být složena z proměnných a podmínek.

Než vytvoříte dynamické pravidlo, je nutné vytvořit proměnné a podmínky, které definují, koho se pravidla týkají, a kdy se pravidla mají použít. Chcete například vytvořit pravidlo, které vyžaduje, aby jakákoli prodejní objednávka, kterou odběratel 1202 vystaví v ceně 1 000,00 nebo více jednotek, byla blokována, dokud se neověří platba odběratele. V tomto případu je proměnná odběratel 1202 a celková objednávka 1 000,00 jednotek. Podmínka určuje, že pokud odběratel 1202 vystaví objednávku a celková částka na objednávce je rovna nebo více než 1 000,00, prodejní objednávku je nutné blokovat, dokud lze ověřit platby odběratele.




