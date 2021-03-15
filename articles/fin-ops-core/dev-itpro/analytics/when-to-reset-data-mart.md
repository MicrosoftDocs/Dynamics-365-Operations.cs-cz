---
title: Kdy resetovat datové tržiště
description: V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093205"
---
# <a name="when-to-reset-a-data-mart"></a>Kdy resetovat datové tržiště

Resetování datového tržiště může být časově náročné. V závislosti na okolnostech nemusí být tato akce řešením, které je potřeba. V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Kdy potřebujete provést reset datového tržiště?
Před resetováním datového tržiště zvažte následující otázky. Odpověď ano na jednu nebo více otázek může znamenat, že vaše organizace může mít prospěch z resetování datového tržiště.

- Databáze aplikace byla obnovena, ale nebyla obnovena databáze datového tržiště.
- Zobrazují se nesprávné údaje za účetní období, které není výsledkem problému s návrhem sestavy.
- Zobrazují se nesprávné údaje za účetní období a záznamy jsou uvedeny v části Pokusy o integraci na stránce **Stav integrace** v Návrháři sestav (spusťte Návrháře sestav a vyberte **Nástroje> Stav integrace**).
- Otevřeli jste incident podpory a technik podpory vám nařídil resetovat datové tržiště jako součást kroku odstraňování problémů.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Když není vhodné resetovat datové tržiště?
Existují okolnosti, kdy nedoporučujeme resetovat datové tržiště. Mezi ně patří následující. 

- Kdykoli důvod není uveden v tomto tématu.
- Máte problémy s výkonem spojené se synchronizací dat. Za těchto okolností pravděpodobně obnovení datového tržiště nepomůže.
- Pokud máte opakující se vzor pro resetování z některého z následujících důvodů: 
  - **Chybějící data** - Nejprve odstraňte problémy s návrhem sestavy a problémy s časováním synchronizace dat, například zjistíte, že mapa faktů se nespustila, protože byla zveřejněna chybějící data.
  - **Zaseknutý stav integrace** - Pokud je integrace pomalá nebo se zdá být zaseknutá, je nepravděpodobné, že resetování datového tržiště problém vyřeší.
  - **Pokusy o resetování byly neúspěšné** - Pokud bylo provedeno několik pokusů o dokončení resetu a byly neúspěšné z důvodu chybějících dat, doporučujeme zahájit incident podpory a spolupracovat s technikem podpory na analýze vaší situace před dalším pokusem o resetování datového trhu.
  - **Zastaralé záznamy** - Zastaralé záznamy samy o sobě nutně neospravedlňují resetování datového tržiště. Pokud máte velkou datovou sadu, proces resetování bude nějakou dobu trvat, ale je nepravděpodobné, že by vedl ke zlepšení.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Co resetování datového tržiště nedělá  
- Reset se spustí až po dokončení stávajících úkolů. Tím je zajištěno, že nebudou vložena stará data. V tomto okamžiku se může zobrazit zpráva jako: „Obnovení datového tržiště nebylo možné zpracovat kvůli aktivní úloze. Prosím zkuste to znovu později."
- Reset deaktivuje integrační úlohy a vymaže všechna data datového tržiště. Integrace je znovu povolena.

> [!NOTE]
> Následující body specifikují dvě věci, které resetování datového tržiště *nebude* dělat. <br>
> - Resetování nevymaže návrhy sestav. <br>
> - Resetování nevymaže firemní ani uživatelská data, pokud není vybráno.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]