---
title: " Nastavení pravidel a parametrů pro cross docking a metodu buyer's push"
description: Tato procedura ukazuje postup vytváření pravidel doplnění.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecc3e1ce842e8d3b693b5e81ed665e9f3c00bfb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021848"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Nastavení pravidel a parametrů pro cross docking a metodu buyer's push

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura ukazuje postup vytváření pravidel doplnění. Pravidla doplnění lze použít k řízení distribuce produktů do obchodů při použití metod cross docking a buyer´s push. Pravidla doplnění lze nastavit pro obchody a skupiny obchodů. Hmotnost definovaná pro jednotlivé řádky v pravidle bude určovat, jak bude množství produktů distribuováno mezi obchody při použití pravidel doplnění jako distribuční metody pro metodu cross docking a buyer´s push. Tato procedura používá ukázkovou společnost USRT.

1. Přejděte na Pravidla doplnění.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Pravidlo doplnění.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klikněte na položku Uložit.
6. Klepněte na možnost Přidat.
7. Označte v seznamu vybraný řádek.
    * Můžete vybrat Hierarchie doplnění nebo Kanál pro typ. Hodnota určuje, zda výběr v položce Název bude hierarchie kanálů nebo konkrétní kanál.  V tomto příkladu ponechejte nastavení Hierarchie doplnění.  
8. Vyberte hodnotu v poli Název.
    * Výchozí hodnota hmotnosti se převezme od hmotnosti definované ve skladu.  Tuto hmotnost lze použít pro Pravidlo doplnění nebo můžete zadat novou hmotnost do pole Hmotnost.  
9. Zadejte číslo do pole Hmotnost.
10. Klepněte na možnost Přidat.
11. Označte v seznamu vybraný řádek.
12. V poli Typ vyberte možnost „Kanál“.
13. V poli Název zadejte nebo vyberte hodnotu.
14. Zadejte číslo do pole Hmotnost.
15. Klikněte na položku Uložit.
