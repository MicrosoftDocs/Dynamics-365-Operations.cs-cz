---
title: Publikování řádek deníku a dokumentů z Excelu
description: Tento článek popisuje, jak zadávat a publikovat řádky pro hlavní deníky z aplikace Microsoft Excel. Obsahuje informace o různých šablonách, které můžete používat, v závislosti na typu transakcí, které zadáváte.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb3e7a420f7f048ba93b6fadf5491e312e7ce33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872463"
---
# <a name="publish-journal-lines-and-documents-from-excel"></a>Publikování řádek deníku a dokumentů z Excelu

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak zadávat a publikovat řádky pro hlavní deníky z aplikace Microsoft Excel. Obsahuje informace o různých šablonách, které můžete používat, v závislosti na typu transakcí, které zadáváte.

Uživatelé mohou zadávat a publikovat řádky pro finanční deníky z aplikace Microsoft Excel. Poté, co uživatel vytvoří deník v tlačítku **Otevřené řádky v aplikaci Excel** se zobrazí šablony, které jsou k dispozici. Šablony jsou určeny pro podporu konkrétních scénářů, avšak ne všechny kombinace typu účtu jsou podporovány v deníku. Následující tabulka zobrazuje šablony, které jsou k dispozici, a typy účtů, které podporují.

| Šablona             | Typy podporovaných účtů | Jak získat přístup k šabloně                                                          |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Řádky deníku hlavní knihy     | K dispozici je podpora pro Účet: Hlavní kniha, Zákazník, Dodavatel, Bankovní protiúčet: hlavní kniha, Odběratel, Dodavatel, Bankovní mezipodnikové.       | Hlavní deník                                                                         |
| Registr faktur         | Nepodporuje se Účet: Protiúčet dodavatele: mezipodnikový účet hlavní knihy.                                                    | Registr faktur AP                                                                     |
| Deník faktur          | Podporuje se Účet: Protiúčet dodavatele: mezipodnikový účet hlavní knihy.                                                      | Deník faktur závazků                                                                      |
| Faktury dodavatele           |                                                                                                                         | Faktury dodavatele                                                                          |
| Deník faktur odběratele | Podporuje se Účet: Protiúčet odběratele: mezipodnikový účet hlavní knihy.                                                     | Hlavní deník                                                                         |
| Volné faktury        |                                                                                                                         | Na stránce **Volná faktura** klikněte na **Otevřít v aplikaci Excel** (ikona Microsoft Office). |
| Deník dlouhodobého majetku     | Majetek do hlavní knihy, banky, zákazníka nebo dodavatele. Hodnota Mezipodnikové není podporována.                                               | Deník dlouhodobého majetku                                                                     |
| Platební deník dodavatelů   | Podporuje se Účet: Protiúčet dodavatele: mezipodnikový bankovní účet.                                                 | Platební deník dodavatelů                                                                  |
| Deník plateb odběratele | Podporuje se Účet: Protiúčet odběratele: mezipodnikový bankovní účet.                                               | Deník plateb odběratele                                                                |
| Deník výdajů projektu  | K dispozici je podpora pro Projekt: Hlavní kniha, Zákazník, Protiúčet dodavatele: hlavní kniha, Odběratel, Dodavatel, Bankovní mezipodnikové. | Hlavní deník výdajů (v rámci řízení a účetnictví projektu)                       |

Když jsou řádky publikovány, jsou ověřeny pro zajištění, zda jsou v souladu s pravidly, které jsou nastaveny ve finančních denících. Po publikování řádků uživatelé mohou upravit nebo zaúčtovat doklady z aplikace Dynamics 365 Finance. 

Chcete-li přidat finanční dimenze do šablony, jsou nutné další změny. Další informace viz [Přidání dimenzí do šablony aplikace Microsoft Excel](../../fin-ops-core/dev-itpro/financial/add-dimensions-excel-templates.md). Po přidání dimenzí do entity jsou k dispozici v návrháři aplikace Excel a lze je přidat do šablony.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
