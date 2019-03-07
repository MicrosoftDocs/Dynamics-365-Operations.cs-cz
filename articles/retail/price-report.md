---
title: Sestavy maloobchodních cen
description: Toto téma obsahuje přehled funkce sestavy cen, kterou lze použít k zobrazení nadcházejících cenových změn u roztříděných produktů.
author: shajain
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 6db6d1c6b6eb1d69b40fe75d97eeb71564986707
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "353050"
---
# <a name="retail-price-reports"></a>Sestavy maloobchodních cen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]


S cílem poskytnout konkurenční ceny pro své zákazníky maloobchodní prodejci často mění ceny produktů. Manažeři obchodu vyžadují možnost snadný přístup k nedávným nebo nadcházejícím cenovým změnám, aby mohly plánovat požadovaným zdrojům aktualizace cenových štítků zobrazených na policích obchodu. S verzí 10.0 aplikace Dynamics 365 for Retail může manažer obchodu otevřít sestavu **Cena** přechodem na **Všechny maloobchody \> Obchod \> Sestava cen** a zobrazením aktualizovaných cen pro produkty přidružené k obchodu. 

Pro povolení sestavy cen musí být zapnut parametr **Povolit sestavu cen pro maloobchod**. Tento parametr se nachází na kartě **Parametry maloobchodu \> Slevy \> Různé**. Otevření stránky **Sestava cen** zobrazí dialogové okno s různými konfiguracemi. Dostupné konfigurace jsou uvedené níže.

| Konfigurace | popis |
|---|---|
| Od data / Do data| Rozsah dat, pro který se má vygenerovat sestava cen. Doba trvání je nyní omezena na 7 dnů. |
| Kanál| Maloobchod, pro který se má vygenerovat sestava cen. |
| Zobrazení produktů s dostupnými zásobami| Nastavení na **Ano** zobrazí ceny pouze pro ty produkty, které mají momentálně dostupné fyzické zásoby v obchodě. |
| Zobrazení cen pro varianty | Nastavení na **Ano** zobrazí ceny variant spolu s hlavními produkty. Tuto možnost je třeba **zapnout**, pokud máte ceny specifické pro varianty, protože počet řádků strmě roste. V budoucích verzích povolíme ceny založené na dimenzích, aby manažer obchodu mohl vybrat dimenze, pro které by se měly ceny zobrazovat. |
| Zobrazení produktů se změnami cen | Nastavení na **Ano** zobrazí ceny pouze pro ta data, kdy byla cena změněna. Cena pro *jeden den před* datem vybraným v možnosti **Od data** se zobrazí vždy, aby manažer ochodu mohl snadno určit produkty, u kterých se nezměnily ceny po celou zvolenou dobu. Rovněž mohou zobrazit aktuální cenu. |

Po vygenerování sestavy lze stáhnout soubor aplikace Excel pro všechny další potřeby filtrování. Sestavu cen lze také použít ke kontrole historických cen produktů pro minulá data.
