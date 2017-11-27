---
title: "Obsah kompenzací a zaměstnaneckých výhod v Power BI"
description: "Toto téma popisuje Finance and Operations - Obsah kompenzací a zaměstnaneckých výhod v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f403416921d2eede9d0071a13af09e1103f91692
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="compensation-and-benefits-power-bi-content"></a>Obsah kompenzací a zaměstnaneckých výhod v Power BI

[!include[banner](../includes/banner.md)]


Toto téma popisuje Finance and Operations - Obsah kompenzací a zaměstnaneckých výhod v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu.

<a name="accessing-the-content-pack"></a>Přístup k balíčku obsahu
--------------------------

Balíček obsahu kompenzací a zaměstnaneckých výhod naleznete v knihovně sdíleného majetku ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení balíčku obsahu a připojení k datům aplikace Microsoft Dynamics 365 for Finance and Operations naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům z aplikace Finance and Operations zobrazí sestavy dat vaší organizace. Pokud jste aplikaci Microsoft Power BI nikdy předtím nepoužívali, vyhledejte si další informace v tématu [Řízená výuka pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí balíčku obsahu, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                     | Obsah                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Analýza kompenzací a zaměstnaneckých výhod | Zaměstnanci s hodinovou a stálou mzdou podle společnosti, průměrná hodinová mzda, průměrná stálá mzda, zaměstnanci podle typu zaměstnání a přihlášení k plánu |
| Zaměstnanecké výhody          | Přihlášení zaměstnance podle vybrané zaměstnanecké výhody                                                                                               |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data aplikace Finance and Operations se používají k naplnění sestav v balíčku obsahu kompenzací a zaměstnaneckých výhod. Následující tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                            | Obsah                                                                                                   | Vztahy s jinými entitami                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pracovní síla\_Kalendářní odsazení         | Posuny kalendáře pro řez sestav                                                                          | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Pracovní síla\_Společnost                | Společnosti, podle kterých se filtrují sestavy                                                                             | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Pracovní síla\_Kompenzace           | Mzdová sazba a frekvence v čase                                                                           | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Pracovní síla\_AktuálníKompenzace    | Mzdová sazba a frekvence k aktuálnímu datu                                                              | Workforce\_Company Workforce\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Pracovní síla\_AktuálníPozice        | Pozice k aktuálnímu datu, ekvivalent k plnému úvazku, otevřené pozice a dlouhodobě otevřené pozice | Pracovní síla\_Pracovní síla dle úkolu\_Pozice                                                                                                                                                                                                                                                                                               |
| Pracovní síla\_Aktuální pracovník          | Pracovníci k aktuálnímu datu, věk a počet zaměstnanců                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit                                            |
| Pracovní síla\_Datum                   | Dny, týdny, měsíce a roky                                                                             | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Pracovní síla\_Demografie           | Datum narození, pohlaví, etnický původ a rodinný stav                                                   | Pracovní síla\_Pracovní síla Aktuální pracovníci\_Pracovní síla Pracovníci s ukončeným poměrem\_TrendPracovníků                                                                                                                                                                                                                                                       |
| Pracovní síla\_Zaměstnání             | Počáteční datum, koncové datum a datum přechodu                                                                  | Pracovní síla\_Pracovní síla Aktuální pracovník\_Pracovní síla Pracovník s ukončeným poměrem\_TrendPracovníků                                                                                                                                                                                                                                                       |
| Pracovní síla\_ZeměpisnáPoloha     | Město, okres, PSČ a stát nebo kraj                                                           | Pracovní síla\_Pracovní síla Aktuální pracovník\_Pracovní síla Pracovník s ukončeným poměrem\_TrendPracovníků                                                                                                                                                                                                                                                       |
| Pracovní síla\_Pracovní místo                    | Funkce, typ a název                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PastPositionAssignment | Důvod přiřazení, počáteční datum, koncové datum a práce                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Pracovní síla\_Výkonnost            | Ohodnocení, popis a model ohodnocení                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Position               | Oddělení, FTE, pozice, typ pozice a název                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | Pozice během času, FTE a práce                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | Křestní jméno, příjmení a celé jméno                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Skill                  | Dovednosti, typ dovedností a ohodnocení                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Workforce\_TerminatedWorker       | Propuštění pracovníci, datum ukončení, název, pozice a práce                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Pracovní síla\_Zaměstnanecké výhody          | Datum začátku platnosti, možnost zaměstnaneckých výhod, plán zaměstnaneckých výhod a typ výhod                                             | Pracovní síla\_Pracovní síla AktuálníPracovník\_Pracovní síla PracovníkSUkončenýmPoměrem\_TrendPracovníků                                                                                                                                                                                                                                                       |
| Pracovní síla\_JménoPracovníka             | Křestní jméno, příjmení a celé jméno                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerTitle            | Název a datum služebního věku                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| PracovníSíla\_TrendPracovníků             | Pracovníci během času, počet zaměstnanců, společnost a pozice                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v balíčku obsahu. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor CompensationandBenefits.pbix z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření balíčku obsahu. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





