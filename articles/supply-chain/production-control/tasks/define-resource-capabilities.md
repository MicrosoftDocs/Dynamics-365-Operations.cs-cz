--- 
title: "Definování schopností prostředku"
description: "Schopnosti prostředku popisují, jaké mají provozní prostředky možnosti."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 99c230c0e6a580f77d863b6f0be298615966c479
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="define-resource-capabilities"></a>Definování schopností prostředku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Schopnosti prostředku popisují, jaké mají provozní prostředky možnosti. Při plánování jsou požadavky jednotlivých úloh a operací porovnávány s možnostmi dostupných prostředků. Tento Průvodce úkolem vám pomůže vytvořit schopnosti prostředku a přiřadit je k prostředku. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.


## <a name="create-a-resource-capability"></a>Vytvořit schopnosti prostředku
1. Přejděte na Schopnosti prostředku.
2. Klepněte na možnost Nový.
3. V poli Schopnost zadejte ID schopnosti prostředku.
    * Pro danou operaci použijte ID možnosti a určete tak, že zdroje musí mít tyto možnosti pro provedení operace.  
4. Do pole Popis zadejte popis schopností.

## <a name="assign-capability-to-a-resource"></a>Přiřadit schopnost k prostředku
1. Klepněte na možnost Přidat.
2. V poli Prostředek zadejte ID prostředku.
    * Schopnost zdrojů může být přiřazena k jednomu nebo více zdrojům.  
3. Do pole Vypršení platnosti zadejte datum.
    * Toto pole lze použít k určení toho, že zdroj má možnosti jen po omezenou dobu.  
4. V poli Priorita zadejte číslo.
    * Při plánování prací a operací můžete určit, zda chcete vybrat zdroje podle priority. Pokud tuto možnost vyberte, a více než jeden zdroj může provádět úlohy nebo operace do požadovaného data, zdroj, který má prioritu nejnižší s ohledem na požadovanou funkci, bude vybrán.  
5. Do pole Úroveň zadejte číslo.
    * Pokud zadáte, že úloha nebo operace vyžaduje určitou možnost, můžete také určit minimální potřebné úrovně. použijte úroveň schopností k odlišení zdrojů, které lze použít ve stejné úloze, ale s různou rychlostí, silnými stránkami, velikostmi a tak dále.  


