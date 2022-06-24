---
title: Obsah rozvoje zaměstnanců v Power BI
description: Tento článek popisuje obsah rozvoje zaměstnanců v Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 67fd3b5907cb52dc1f10d754e12316e21876e888
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850980"
---
# <a name="employee-development-power-bi-content"></a>Obsah rozvoje zaměstnanců v Power BI

[!include [banner](../includes/banner.md)]

Tento článek popisuje obsah **rozvoje zaměstnanců** v Microsoft Power BI.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI
Sestavy, které jsou součástí obsahu **Rozvoj zaměstnanců** v Power BI, obsahují grafy a tabulky s dalšími informacemi. Následující tabulka obsahuje popis daných sestav.

| Sestava                        | Obsah |
|-------------------------------|----------|
| Přehled rozvoje zaměstnanců | Souhrn dalších sestav |
| Analýza dovedností zaměstnanců       | Typy dovedností zaměstnanců a dovednosti zaměstnanců podle typu |
| Analýza úrovní dovedností zaměstnanců | Úrovně dovedností zaměstnanců podle oddělení, zaměstnanci podle úrovní a typů dovedností a nejnižší a nejvyšší úrovně podle dovednosti |
| Profil dovedností                 | Profil dovedností vybraného zaměstnance |
| Analýza dovedností                | Dovednosti podle typu a hodnocení |
| Analýza hodnocení výkonnosti   | Zaměstnanci s nejnižším a nejvyšším hodnocením podle druhu práce, hodnocení zaměstnanců podle oddělení, zaměstnanci podle typu pozice a hodnocení a nejvyšší a nejnižší hodnocení podle umístění |
| Analýza výkonnosti zaměstnanců | Hodnocení zaměstnanců u vybraného hodnocení podle manažera |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

| Celek                   | Obsah                                                                                                   | Vztahy s jinými entitami |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Posuny kalendáře          | Posuny kalendáře pro řez sestav                                                                          | Přiřazení k minulé pozici, trend pozice, trend zaměstnance, ukončený zaměstnanec |
| Společnost                  | Společnosti, podle kterých se filtrují sestavy                                                                             | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Aktuální pozice         | Pozice k aktuálnímu datu, ekvivalent k plnému úvazku, otevřené pozice a dlouhodobě otevřené pozice | Práce, pozice |
| Aktuální zaměstnanec         | Pracovníci k aktuálnímu datu, věk a počet zaměstnanců                                                         | Společnost, geografické umístění, jméno zaměstnance, nadřízený, pracovní zařazení, demografické údaje, práce, zaměstnání, pozice |
| Datum                     | Dny, týdny, měsíce a roky                                                                             | Přiřazení k minulé pozici, trend pozice, ukončený zaměstnanec, trend zaměstnance |
| Demografické údaje             | Datum narození, pohlaví, etnický původ a rodinný stav                                                   | Aktuální zaměstnanec, ukončený pracovní poměr, trend zaměstnance |
| Zaměstnání               | Počáteční datum, koncové datum a datum přechodu                                                                  | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Geografické umístění      | Město, okres, PSČ a stát nebo kraj                                                           | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Práce                      | Funkce, typ a název                                                                                  | Aktuální pozice, aktuální zaměstnanec |
| Minulá pozice | Důvod přiřazení, počáteční datum, koncové datum a práce                                                           | Posun kalendáře, datum, práce, pozice |
| Pozice                 | Oddělení, FTE, pozice, typ pozice a název                                                        | Aktuální pozice, aktuální zaměstnanec |
| Trend pozice           | Pozice během času, FTE a práce                                                                          | Posun kalendáře, datum, práce, pozice |
| Nadřízená pozice               | Křestní jméno, příjmení a celé jméno                                                                       | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Ukončený pracovní poměr      | Propuštění pracovníci, datum ukončení, název, pozice a práce                                             | Společnost, geografické umístění, jméno zaměstnance, nadřízený, posun kalendáře, datum, pracovní zařazení, demografické údaje, práce, zaměstnání, pozice |
| Jméno zaměstnance            | Křestní jméno, příjmení a celé jméno                                                                       | Aktuální pracovník, ukončený zaměstnanec, trend zaměstnance |
| Titul zaměstnance           | Název a datum služebního věku                                                                                   | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Trend zaměstnance           | Pracovníci během času, počet zaměstnanců, společnost a pozice                                                        | Společnost, geografické umístění, jméno zaměstnance, nadřízený, posun kalendáře, datum, pracovní zařazení, demografické údaje, práce, zaměstnání |
| Práce                      | Funkce, typ a název                                                                                  | Aktuální zaměstnanec, aktuální pozice, trend zaměstnance, upřednostňované dovednosti, minulá pozice, trend pozice, ukončený pracovní poměr |
| Upřednostňovaná dovednost      | Důležitost, hodnocení, dovednost a úroveň dovedností                                                                 | Práce |
| Analýza dovedností zaměstnanců  | Certifikace, úroveň, datum úrovně a dovednost                                                                    | Jméno zaměstnance, dovednost |
| Výkonnost              | Ohodnocení, popis a model ohodnocení                                                                      | Aktuální zaměstnanec, aktuální pozice, trend zaměstnance, upřednostňované dovednosti, minulá pozice, trend pozice, ukončený pracovní poměr |
| Dovednost                    | Dovednosti, typ dovedností a ohodnocení                                                                              | Analýza dovedností zaměstnanců, upřednostňovaná dovednost |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]