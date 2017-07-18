---
title: "Publikování řádek deníku a dokumentů z Excelu"
description: "Toto téma popisuje, jak zadávat a publikovat řádky pro hlavní deníky z aplikace Microsoft Excel. Obsahuje informace o různých šablonách, které můžete používat, v závislosti na typu transakcí, které zadáváte."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1fed8d162a37736883365fa765a059e5beff06be
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Publikování řádek deníku a dokumentů z Excelu

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak zadávat a publikovat řádky pro hlavní deníky z aplikace Microsoft Excel. Obsahuje informace o různých šablonách, které můžete používat, v závislosti na typu transakcí, které zadáváte.

Uživatelé mohou zadávat a publikovat řádky pro finanční deníky z aplikace Microsoft Excel. Poté, co uživatel vytvoří deník v tlačítku **Otevřené řádky v aplikaci Excel** se zobrazí šablony, které jsou k dispozici. Šablony jsou určeny pro podporu konkrétních scénářů, avšak ne všechny kombinace typu účtu jsou podporovány v deníku. Následující tabulka zobrazuje šablony, které jsou k dispozici, a typy účtů, které podporují.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Šablona**             | **Typy podporovaných účtů**                                                                                             | **Jak získat přístup k šabloně**                                                          |
| Řádky deníku hlavní knihy     | K dispozici je podpora pro Účet: Hlavní kniha, Zákazník, Dodavatel, Bankovní protiúčet: hlavní kniha, Odběratel, Dodavatel, Bankovní mezipodnikové.       | Hlavní deník                                                                         |
| Registr faktur         | Nepodporuje se Účet: Protiúčet dodavatele: mezipodnikový účet hlavní knihy.                                                    | Registr faktur AP                                                                     |
| Deník faktur          | Podporuje se Účet: Protiúčet dodavatele: mezipodnikový účet hlavní knihy.                                                      | Deník faktur závazků                                                                      |
| Faktury dodavatele           |                                                                                                                         | Faktury dodavatele                                                                          |
| Deník faktur odběratele | Podporuje se Účet: Protiúčet odběratele: mezipodnikový účet hlavní knihy.                                                     | Hlavní deník                                                                         |
| Volné faktury        |                                                                                                                         | Na stránce **Textová faktura** klikněte na **Otevřít v aplikaci Excel** (ikona Microsoft Office). |
| Deník dlouhodobého majetku     | Majetek do hlavní knihy, banky, zákazníka nebo dodavatele. Hodnota Mezipodnikové není podporována.                                               | Deník dlouhodobého majetku                                                                     |
| Platební deník dodavatelů   | Podporuje se Účet: Protiúčet dodavatele: mezipodnikový bankovní účet.                                                 | Platební deník dodavatelů                                                                  |
| Deník plateb odběratele | Podporuje se Účet: Protiúčet odběratele: mezipodnikový bankovní účet.                                               | Deník plateb odběratele                                                                |
| Deník výdajů projektu  | K dispozici je podpora pro Projekt: Hlavní kniha, Zákazník, Protiúčet dodavatele: hlavní kniha, Odběratel, Dodavatel, Bankovní mezipodnikové. | Hlavní deník výdajů (v rámci řízení a účetnictví projektu)                       |

Když jsou řádky publikovány, jsou ověřeny pro zajištění, zda jsou v souladu s pravidly, které jsou nastaveny ve finančních denících. Po publikování řádků uživatelé mohou upravit nebo zaúčtovat doklady z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. 

Chcete-li přidat finanční dimenze do šablony, jsou nutné další změny. Další informace viz [Přidání dimenzí do šablony aplikace Microsoft Excel](/dynamics365/unified-operations/dev-itpro/financial/add-dimensions-excel-templates). Po přidání dimenzí do entity jsou k dispozici v návrháři aplikace Excel a lze je přidat do šablony.






