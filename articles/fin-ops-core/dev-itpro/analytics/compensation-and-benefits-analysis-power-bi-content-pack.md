---
title: Obsah kompenzací a zaměstnaneckých výhod v Power BI
description: Tento článek popisuje obsah kompenzací a zaměstnaneckých výhod v Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bed0e8ffbd23c6793c037bade218f637105734b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908612"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Obsah kompenzací a zaměstnaneckých výhod v Power BI

[!include [banner](../includes/banner.md)]

Tento článek popisuje obsah kompenzací a zaměstnaneckých výhod v Power BI. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům zobrazí sestavy dat vaší organizace. Pokud jste aplikaci Microsoft Power BI nikdy předtím nepoužívali, vyhledejte si další informace v tématu [Řízená výuka pro Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí balíčku obsahu, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                     | Obsah                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Analýza kompenzací a zaměstnaneckých výhod | Zaměstnanci s hodinovou a stálou mzdou podle společnosti, průměrná hodinová mzda, průměrná stálá mzda, zaměstnanci podle typu zaměstnání a přihlášení k plánu |
| Zaměstnanecké výhody          | Přihlášení zaměstnance podle vybrané zaměstnanecké výhody                                                                                               |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data aplikace se používají k naplnění sestav v balíčku obsahu kompenzací a zaměstnaneckých výhod. Následující tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                            | Obsah                                                                                                   | Vztahy s jinými entitami |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Pracovní síla\_Kalendářní odsazení         | Posuny kalendáře pro řez sestav                                                                          | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker |
| Pracovní síla\_Společnost                | Společnosti, podle kterých se filtrují sestavy                                                                             | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_Kompenzace           | Mzdová sazba a frekvence v čase                                                                           | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_AktuálníKompenzace    | Mzdová sazba a frekvence k aktuálnímu datu                                                              | Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Pracovní síla\_AktuálníPozice        | Pozice k aktuálnímu datu, ekvivalent k plnému úvazku, otevřené pozice a dlouhodobě otevřené pozice | Workforce\_Job, Workforce\_Position |
| Pracovní síla\_Aktuální pracovník          | Pracovníci k aktuálnímu datu, věk a počet zaměstnanců                                                         | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit |
| Pracovní síla\_Datum                   | Dny, týdny, měsíce a roky                                                                             | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_Demografie           | Datum narození, pohlaví, etnický původ a rodinný stav                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_Zaměstnání             | Počáteční datum, koncové datum a datum přechodu                                                                  | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_ZeměpisnáPoloha     | Město, okres, PSČ a stát nebo kraj                                                           | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_Pracovní místo                    | Funkce, typ a název                                                                                  | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Pracovní síla\_ÚkolNaDřívějšíPozici | Důvod přiřazení, počáteční datum, koncové datum a práce                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Pracovní síla\_Výkonnost            | Ohodnocení, popis a model ohodnocení                                                                      | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Position               | Oddělení, FTE, pozice, typ pozice a název                                                        | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | Pozice během času, FTE a práce                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Křestní jméno, příjmení a celé jméno                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_Dovednost                  | Dovednosti, typ dovedností a ohodnocení                                                                              | |
| Workforce\_TerminatedWorker       | Propuštění pracovníci, datum ukončení, název, pozice a práce                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit |
| Pracovní síla\_Zaměstnanecké výhody          | Datum začátku platnosti, možnost zaměstnaneckých výhod, plán zaměstnaneckých výhod a typ výhod                                             | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Pracovní síla\_JménoPracovníka             | Křestní jméno, příjmení a celé jméno                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| PracovníSíla\_TitulPracovníka            | Název a datum služebního věku                                                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTrend            | Pracovníci během času, počet zaměstnanců, společnost a pozice                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]