---
title: Sestavy maloobchodních cen
description: Tento článek obsahuje přehled funkce sestavy cen, kterou lze použít k zobrazení nadcházejících cenových změn u roztříděných produktů.
author: ShalabhjainMSFT
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 09350d15660978126d36199a3b4e93f6be5fe157
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269020"
---
# <a name="retail-price-reports"></a>Sestavy maloobchodních cen

[!include [banner](includes/banner.md)]


S cílem poskytnout konkurenční ceny pro své zákazníky maloobchodní prodejci často mění ceny produktů. Manažeři obchodu vyžadují možnost snadný přístup k nedávným nebo nadcházejícím cenovým změnám, aby mohly plánovat požadovaným zdrojům aktualizace cenových štítků zobrazených na policích obchodu. S verzí 10.0 aplikace Retail může manažer obchodu otevřít sestavu **Cena** přechodem na **Všechny obchody \> Obchod \> Sestava cen** a zobrazením aktualizovaných cen pro produkty přidružené k obchodu. 

Pro povolení sestavy cen musí být zapnut parametr **Povolit sestavu cen pro obchod**. Tento parametr se nachází na kartě **Parametry velkoobchodu \> Slevy \> Různé**. Otevření stránky **Sestava cen** zobrazí dialogové okno s různými konfiguracemi. Dostupné konfigurace jsou uvedené níže.

| Konfigurace | popis |
|---|---|
| Od data / Do data| Rozsah dat, pro který se má vygenerovat sestava cen. Doba trvání je nyní omezena na 7 dnů. |
| Kanál| Obchod, pro který se má vygenerovat sestava cen. |
| Zobrazit produkty s dostupnými zásobami| Nastavení na **Ano** zobrazí ceny pouze pro ty produkty, které mají momentálně dostupné fyzické zásoby v obchodě. |
| Zobrazení cen pro varianty | Nastavení na **Ano** zobrazí ceny variant spolu s hlavními produkty. Tuto možnost je třeba **zapnout**, pokud máte ceny specifické pro varianty, protože počet řádků strmě roste. V budoucích verzích povolíme ceny založené na dimenzích, aby manažer obchodu mohl vybrat dimenze, pro které by se měly ceny zobrazovat. |
| Zobrazení produktů se změnami cen | Nastavení na **Ano** zobrazí ceny pouze pro ta data, kdy byla cena změněna. Cena pro *jeden den před* datem vybraným v možnosti **Od data** se zobrazí vždy, aby manažer ochodu mohl snadno určit produkty, u kterých se nezměnily ceny po celou zvolenou dobu. Rovněž mohou zobrazit aktuální cenu. |

Po vygenerování sestavy lze stáhnout soubor aplikace Excel pro všechny další potřeby filtrování. Sestavu cen lze také použít ke kontrole historických cen produktů pro minulá data.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
