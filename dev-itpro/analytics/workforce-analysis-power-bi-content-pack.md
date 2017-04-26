---
title: "Obsah pracovní síly metriky Power BI"
description: "Toto téma popisuje 365 Dynamics pro operace - obsah pracovníků metriky Power BI. Popisuje, jak přístup k sestavám, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d03692e39c51cc4eb0fe23ba263e52de2bf3c3da
ms.lasthandoff: 03/31/2017


---

# <a name="workforce-metrics-power-bi-content"></a>Obsah pracovní síly metriky Power BI

[!include[banner](../includes/banner.md)]


Toto téma popisuje 365 Dynamics pro operace - obsah pracovníků metriky Power BI. Popisuje, jak přístup k sestavám, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu pack.

<a name="accessing-the-content-pack"></a>Přístup k obsahu pack
--------------------------

Obsahu pack pracovníků metriky můžete najít v knihovně Sdílené datové zdroje v Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení obsahu pack a připojit k vaší 365 Microsoft Dynamics pro datové operace, viz [obsahu Power BI od společnosti Microsoft a partnerů LCS](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí obsahu pack
Po připojení obsahu pack do aplikace Dynamics 365 pro operace data, sestavy zobrazit data organizace. Pokud jste dosud nepoužívali Microsoft Power BI před, bližší informace na [s asistencí výukové stránky pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí obsahu pack mají grafy a tabulky, které obsahují další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                                           | Obsah                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Počet osob analýzy společnosti, oddělení, umístění | Počet osob ve společnosti, počtu zaměstnanců podle oddělení, počtu zaměstnanců podle umístění a celkový počet osob                                                                                                                           |
| Úloha kroku Správce analýzy počet osob            | Počet osob podle projektu, počtu zaměstnanců o krok, počet osob, vedoucí a celkový počet osob                                                                                                                                      |
| Analýza trendů počet osob                         | Počet osob tento rok versus minulý rok společnost a postupné počtu zaměstnanců v posledních 12 měsících                                                                                                                        |
| Demografické údaje zaměstnanců                           | Počet osob podle věku a pohlaví, počet osob podle etnického původu, počtu zaměstnanců podle stavu veterána, počet osob, rodinný stav, počet studentů na plný úvazek, průměrná držby, průměrné stáří a poměr žena muže zaměstnancům |
| Analýzu pozice                                | Otevřené pozice podle oddělení, pozice otevřené vyplněné, aktivní aktivní pozice a pozice podle oddělení                                                                                                   |
| Otěr analýzy                               | Otěr letos a Loni otěr, průměrná držby lidí opouští, průměrné stáří osoby opouštějící a podle důvodu ukončení zaměstnancům                                                                   |
| Lidé podle oddělení                             | Zaměstnanci s osobní číslo oddělení, pozice a přiřazení počátečního a koncového data                                                                                                                       |
| Služební věk analýzy                               | Průměr let podle seznamu společností a služebního věku                                                                                                                                                              |
| Výročí a let               | Zaměstnanci podle let služby a výročí                                                                                                                                                                    |

Můžete filtrovat grafy a dlaždice v těchto sestavách a Připnutí grafů a dlaždice pro řídicí panel. Další informace o filtru a pin v Power BI, viz [vytvoření a konfigurace řídicího panelu A](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Dynamics 365 pro datové operace se používá k naplnění sestavy v obsahu pack metriky pracovníků. Následující tabulka zobrazuje entity, aby byla na základě obsahu pack.

| Celek                            | Obsah                                                                                                   | Vztahy s jinými subjekty                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sil\_CalendarOffset         | Kalendář posuny na řezu sestavy                                                                          | Pracovní síly\_sil PastPositionAssignment\_PositionTrend Workorce\_WorkerTrend sil\_TerminatedWorker                                                                                                                                                                                                                     |
| Sil\_společnosti                | Chcete-li filtrovat zprávy společnosti                                                                             | Pracovní síly\_sil CurrentCompensation\_CurrentWorker sil\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Sil\_vyrovnání           | Mzdová sazba a frekvence v čase                                                                           | Pracovní síly\_sil CurrentCompensation\_CurrentWorker sil\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Sil\_CurrentCompensation    | Mzdová sazba a frekvence k aktuálnímu datu                                                              | Pracovní síly\_zaměstnanců společnosti\_pracovníků kompenzace\_demografické údaje zaměstnanců\_pracovních sil\_pozice                                                                                                                                                                                                                            |
| Sil\_CurrentPosition        | Pozice aktuálního data, ekvivalent plného úvazku (FTE), otevřené pozice a otevřít naplní pozice | Sil\_pracovních sil\_pozice                                                                                                                                                                                                                                                                                               |
| Sil\_CurrentWorker          | Pracovníků k aktuálnímu datu, věku a počtu zaměstnanců                                                         | Pracovní síly\_zaměstnanců společnosti\_kompenzace zaměstnanců\_GeographicLocation sil\_výkonu pracovníků\_WorkerName sil\_ReportsToWorkerName sil\_WorkerTitle sil\_demografické údaje zaměstnanců\_pracovních sil\_pracovních sil\_umístěte pracovní síly\_WorkerBenefit                                            |
| Sil\_datum                   | Dny, týdny, měsíce a roky                                                                             | Pracovní síly\_sil PastPositionAssignment\_PositionTrend sil\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Sil\_demografické údaje           | Datum narození, pohlaví, etnického původu a rodinného stavu                                                   | Sil\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Sil\_zaměstnání             | Počáteční datum, koncové datum a datum přechodu                                                                  | Sil\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Sil\_GeographicLocation     | Město, kraj, poštovní kód a Okres                                                           | Sil\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Sil\_práce                    | Funkce, typ a název                                                                                  | Sil\_CurrentPosition sil\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Sil\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| Sil\_PastPositionAssignment | Důvod přiřazení, počáteční datum, koncové datum a úlohy                                                           | Sil\_CalendarOffset sil\_datum pracovní síly\_pracovních sil\_pozice                                                                                                                                                                                                                                                     |
| Sil\_výkon            | Model hodnocení, hodnocení a popis                                                                      | Sil\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Sil\_PersonSkill            | Úroveň a dovednosti                                                                                            | Sil\_dovednosti                                                                                                                                                                                                                                                                                                                 |
| Sil\_PersonSkillAnalysis    | Certifikovaný, úroveň a dovednosti                                                                                | Sil\_dovedností pracovníků\_WorkerName                                                                                                                                                                                                                                                                                           |
| Sil\_pozice               | Oddělení, FTE, pozice, typ pozice a názvu                                                        | Sil\_CurrentPosition sil\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Sil\_PositionTrend          | Nad čas, FTE a pracovní pozice                                                                          | Sil\_CalendarOffset sil\_datum pracovní síly\_pracovních sil\_pozice                                                                                                                                                                                                                                                     |
| Sil\_ReportsToWorkerName    | Jméno, příjmení a celé jméno                                                                       | Sil\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Sil\_dovednosti                  | Dovednosti, typ dovednosti a hodnocení                                                                              | Sil\_sil PersonSkill\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| Sil\_TerminatedWorker       | Pracovníků, datum ukončení, název, umístění a úloha ukončena                                             | Pracovní síly\_zaměstnanců společnosti\_kompenzace zaměstnanců\_GeographicLocation sil\_výkonu pracovníků\_WorkerName sil\_ReportsToWorkerName sil\_CalendarOffset sil\_datum pracovní síly\_WorkerTitle sil\_demografické údaje zaměstnanců\_zaměstnání pracovníků\_pracovních sil\_umístění zaměstnanců\_WorkerBenefit |
| Sil\_WorkerBenefit          | Zadejte datum začátku platnosti, možnost zaměstnaneckých výhod, plán zaměstnaneckých výhod a výhod                                             | Sil\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Sil\_WorkerName             | Jméno, příjmení a celé jméno                                                                       | Pracovní síly\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend sil\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| Sil\_WorkerTitle            | Datum název a služebního věku                                                                                   | Sil\_sil CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Nad čas, počet osob, společnosti a postavení zaměstnanců                                                        | Pracovní síly\_zaměstnanců společnosti\_kompenzace zaměstnanců\_GeographicLocation sil\_výkonu pracovníků\_WorkerName sil\_ReportsToWorkerName sil\_CalendarOffset sil\_datum pracovní síly\_WorkerTitle sil\_demografické údaje zaměstnanců\_zaměstnání pracovníků\_pracovních sil\_WorkerBenefit                     |

Tyto entity byly použity k vytvoření vypočítaných rozměrů v datovém modelu. Tyto vypočtena opatření se poté použije pro výpočet klíčových ukazatelů výkonu (KPI) a sestavy, které jsou použity v obsahu pack. Pokud chcete zahrnout další výpočty v sestavách a řídicího panelu, můžete stáhnout a upravit soubor CompensationandBenefits.pbix z LCS. Tento soubor je výchozí datový model, který byl použit k vytvoření obsahu pack. Poté, co jste provedli změny, můžete vytvořit obsahu pack organizační a řídicí panel, který obsahuje informace, které jste přidali.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





