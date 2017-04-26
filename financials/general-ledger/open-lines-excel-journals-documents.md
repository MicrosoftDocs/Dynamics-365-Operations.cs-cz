---
title: "Řádky deníku a dokumentů z aplikace Excel publikovat"
description: "Toto téma vysvětluje, jak zadat a publikovat řádků pro finanční deníky z aplikace Microsoft Excel. Obsahuje informace o různých šablon, které můžete použít v závislosti na typu transakce, které zadáváte."
author: twheeloc
manager: AnnBe
ms.date: 2016-03-08 17 - 50 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Řádky deníku a dokumentů z aplikace Excel publikovat

Toto téma vysvětluje, jak zadat a publikovat řádků pro finanční deníky z aplikace Microsoft Excel. Obsahuje informace o různých šablon, které můžete použít v závislosti na typu transakce, které zadáváte.

Zadávání a publikovat řádků pro finanční deníky z aplikace Microsoft Excel. Poté, co uživatel vytvoří deník, **otevřené řádky v aplikaci Excel** tlačítko zobrazí šablony, které jsou k dispozici. Šablony jsou určeny pro podporu konkrétní scénáře, avšak ne všechny kombinace typu účtu je podporována v deníku. Následující tabulka zobrazuje šablony, které jsou k dispozici a typy účtů, které podporují.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Typy podporovaných účtů**                                                                                             | **Jak získat přístup k šabloně**                                                          |
| Řádky deníku hlavní knihy     | Účet: Zboží, Zákazník, Dodavatel, bankovní protiúčet: hlavní knihy, odběratele, dodavatele, bankovního mezipodnikové je podporována.       | Hlavní deník                                                                         |
| Registr faktur         | Účtu: Protiúčet dodavatel: mezipodnikové hlavní knihy není podporován.                                                    | Registr faktur AP                                                                     |
| Deník faktur          | Účty: Protiúčet dodavatele: podporuje mezipodnikové hlavní knihy.                                                      | Deník faktur závazků                                                                      |
| Faktury dodavatele           |                                                                                                                         | Faktury dodavatele                                                                          |
| Deník faktur odběratele | Účtu: Protiúčet zákazník: podporuje mezipodnikové hlavní knihy.                                                     | Hlavní deník                                                                         |
| Volné faktury        |                                                                                                                         | Na **faktury s volným textem** klepněte na tlačítko **otevřít v aplikaci Excel** (na ikonu Microsoft Office). |
| Deník dlouhodobého majetku     | Majetku do hlavní knihy, banky, zákazníka nebo dodavatele. Mezipodnikové, není podporována.                                               | Deník dlouhodobého majetku                                                                     |
| Platební deník dodavatelů   | Účtu: Protiúčet dodavatel: knihy, vnitropodnikové banky je podporována.                                                 | Platební deník dodavatelů                                                                  |
| Deník plateb odběratele | Účtu: Protiúčet zákazník: knihy, vnitropodnikové banky je podporována.                                               | Deník plateb odběratele                                                                |
| Deník výdajů projektu  | Účet: Projektu, hlavní knihy, odběratele, Protiúčet dodavatele: projektu, hlavní knihy, odběratele, dodavatele mezipodnikovou je podporována. | Deník výdajů (v rámci řízení a účetnictví projektu)                       |

Při řádky jsou publikovány, jsou ověřena a ujistěte se, zda jsou v souladu s pravidly, které jsou nastaveny ve finančních denících. Po publikování řádky, uživatelé mohou upravit nebo doklady zaúčtovat z 365 Microsoft Dynamics pro operace. 

Chcete-li přidat šablonu finanční dimenze, jsou nutné další změny. Další informace naleznete v tématu [přidání dimenzí do šablony aplikace Microsoft Excel](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Po přidání dimenze entity, jsou k dispozici v návrháři aplikace Excel a lze přidat do šablony.




