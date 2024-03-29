---
title: Obsah kompetencí a rozvoje zaměstnance v Power BI
description: Tento článek popisuje obsah kompetencí a rozvoje zaměstnanců v Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.openlocfilehash: 1ddc117c83e551374bc8da6872429e3bb9eeee58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280951"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Obsah kompetencí a rozvoje zaměstnance v Power BI

[!include [banner](../includes/banner.md)]

Tento článek popisuje obsah kompetencí a rozvoje zaměstnanců v Power BI. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům zobrazí sestavy dat vaší organizace. Pokud jste aplikaci Microsoft Power BI nikdy předtím nepoužívali, vyhledejte si další informace v tématu [Řízená výuka pro Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí balíčku obsahu, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                            | Obsah                                               |
|-----------------------------------|--------------------------------------------------------|
| Analýza kompetence a rozvoje | Typy dovedností člena týmu a dovednosti členů týmu podle typu |
| Profil dovedností                     | Profil dovedností vybraného zaměstnance                |
| Analýza dovedností                    | Dovednosti podle typu a hodnocení                              |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Sestavy v balíčku obsahu Kompetence a rozvoj zaměstnance se vyplní pomocí dat aplikace Finance. Následující tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                            | Obsah                                                                                                   | Vztahy s jinými entitami |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Posuny kalendáře pro řez sestav                                                                          | |
| Pracovní síla\_Společnost                | Společnosti, podle kterých se filtrují sestavy                                                                             | |
| Pracovní síla\_Kompenzace           | Mzdová sazba a frekvence v čase                                                                           | |
| Pracovní síla\_AktuálníKompenzace    | Mzdová sazba a frekvence k aktuálnímu datu                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Pracovní síla\_AktuálníPozice        | Pozice k aktuálnímu datu, ekvivalent k plnému úvazku, otevřené pozice a dlouhodobě otevřené pozice | Pracovní síla\_Pracovní síla dle úkolu\_Pozice |
| Pracovní síla\_Aktuální pracovník          | Pracovníci k aktuálnímu datu, věk a počet zaměstnanců                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Pracovní síla\_Datum                   | Dny, týdny, měsíce a roky                                                                             | |
| Pracovní síla\_Demografie           | Datum narození, pohlaví, etnický původ a rodinný stav                                                   | |
| Pracovní síla\_Zaměstnání             | Počáteční datum, koncové datum a datum přechodu                                                                  | |
| Pracovní síla\_ZeměpisnáPoloha     | Město, okres, PSČ a stát nebo kraj                                                           | |
| Pracovní síla\_Pracovní místo                    | Funkce, typ a název                                                                                  | |
| Workforce\_JobPreferredSkill      | Důležitost, hodnocení, dovednost a úroveň dovedností                                                                 | Workforce\_Skill, Workforce\_Job |
| Pracovní síla\_ÚkolNaDřívějšíPozici | Důvod přiřazení, počáteční datum, koncové datum a práce                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Pracovní síla\_Výkonnost            | Ohodnocení, popis a model ohodnocení                                                                      | |
| Pracovní síla\_DovednostOsoby            | Úroveň, datum úrovně a dovednost                                                                               | Pracovní síla\_Dovednost |
| Pracovní síla\_AnalýzaDovednostíOsoby    | Certifikace, úroveň, datum úrovně a dovednost                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Oddělení, FTE, pozice, typ pozice a název                                                        | |
| Workforce\_PositionTrend          | Pozice během času, FTE a práce                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Křestní jméno, příjmení a celé jméno                                                                       | |
| Pracovní síla\_Dovednost                  | Dovednosti, typ dovedností a ohodnocení                                                                              | |
| Pracovní síla\_Pracovník s ukončeným poměrem       | Propuštění pracovníci, datum ukončení, název, pozice a práce                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Pracovní síla\_JménoPracovníka             | Křestní jméno, příjmení a celé jméno                                                                       | |
| PracovníSíla\_TitulPracovníka            | Název a datum služebního věku                                                                                   | |
| PracovníSíla\_TrendPracovníků             | Pracovníci během času, počet zaměstnanců, společnost a pozice                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
