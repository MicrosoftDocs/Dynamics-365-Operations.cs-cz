---
title: "Obsah Power BI kompetencí a rozvoje zaměstnance"
description: "Toto téma popisuje obsah Power BI kompetencí a rozvoje zaměstnanců v aplikaci Finance and Operations. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: f5b3c180f0a9d60fa5d4d8398daf79a14da2d6f4
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Obsah Power BI kompetencí a rozvoje zaměstnance

[!include[banner](../includes/banner.md)]


Toto téma popisuje obsah Power BI kompetencí a rozvoje zaměstnanců v aplikaci Finance and Operations. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu.

<a name="accessing-the-content-pack"></a>Přístup k balíčku obsahu
--------------------------

Sadu kompetencí zaměstnance a obsahu rozvoje najdete v sadě obsahu rozvoje ve sdílené knihovně aktiv služby Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení balíčku obsahu a připojení k datům aplikace Microsoft Dynamics 365 for Finance and Operations naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům z aplikace Finance and Operations zobrazí sestavy dat vaší organizace. Pokud jste aplikaci Microsoft Power BI nikdy předtím nepoužívali, vyhledejte si další informace v tématu [Řízená výuka pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí balíčku obsahu, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                            | Obsah                                               |
|-----------------------------------|--------------------------------------------------------|
| Analýza kompetence a rozvoje | Typy dovedností člena týmu a dovednosti členů týmu podle typu |
| Profil dovedností                     | Profil dovedností vybraného zaměstnance                |
| Analýza dovedností                    | Dovednosti podle typu a hodnocení                              |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Sestavy v balíčku obsahu Kompetence a rozvoj zaměstnance se vyplní pomocí dat aplikace Finance and Operations. Následující tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                            | Obsah                                                                                                   | Vztahy s jinými entitami                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Posuny kalendáře pro řez sestav                                                                          |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_Společnost                | Společnosti, podle kterých se filtrují sestavy                                                                             |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_Kompenzace           | Mzdová sazba a frekvence v čase                                                                           |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_AktuálníKompenzace    | Mzdová sazba a frekvence k aktuálnímu datu                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Pracovní síla\_AktuálníPozice        | Pozice k aktuálnímu datu, ekvivalent k plnému úvazku, otevřené pozice a dlouhodobě otevřené pozice | Pracovní síla\_Pracovní síla dle úkolu\_Pozice                                                                                                                                                                                                                                                                      |
| Pracovní síla\_Aktuální pracovník          | Pracovníci k aktuálnímu datu, věk a počet zaměstnanců                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Pracovní síla\_Datum                   | Dny, týdny, měsíce a roky                                                                             |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_Demografie           | Datum narození, pohlaví, etnický původ a rodinný stav                                                   |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_Zaměstnání             | Počáteční datum, koncové datum a datum přechodu                                                                  |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_ZeměpisnáPoloha     | Město, okres, PSČ a stát nebo kraj                                                           |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_Pracovní místo                    | Funkce, typ a název                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | Důležitost, hodnocení, dovednost a úroveň dovedností                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Pracovní síla\_ÚkolNaDřívějšíPozici | Důvod přiřazení, počáteční datum, koncové datum a práce                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Pracovní síla\_Výkonnost            | Ohodnocení, popis a model ohodnocení                                                                      |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_DovednostOsoby            | Úroveň, datum úrovně a dovednost                                                                               | Pracovní síla\_Dovednost                                                                                                                                                                                                                                                                                        |
| Pracovní síla\_AnalýzaDovednostíOsoby    | Certifikace, úroveň, datum úrovně a dovednost                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | Oddělení, FTE, pozice, typ pozice a název                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | Pozice během času, FTE a práce                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | Křestní jméno, příjmení a celé jméno                                                                       |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_Dovednost                  | Dovednosti, typ dovedností a ohodnocení                                                                              |                                                                                                                                                                                                                                                                                                         |
| Pracovní síla\_Pracovník s ukončeným poměrem       | Propuštění pracovníci, datum ukončení, název, pozice a práce                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Pracovní síla\_JménoPracovníka             | Křestní jméno, příjmení a celé jméno                                                                       |                                                                                                                                                                                                                                                                                                         |
| PracovníSíla\_TitulPracovníka            | Název a datum služebního věku                                                                                   |                                                                                                                                                                                                                                                                                                         |
| PracovníSíla\_TrendPracovníků             | Pracovníci během času, počet zaměstnanců, společnost a pozice                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v balíčku obsahu. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor CompetenciesandDevelopment.pbix z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření balíčku obsahu. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





