---
title: "Organizační obsah školení Power BI"
description: "Toto téma popisuje 365 Dynamics pro operace - obsah organizační školení Power BI. Tento článek vysvětluje, jak získat přístup k obsahu pack a popisuje datový model a subjekty, které byly použity k sestavení obsahu pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organizační obsah školení Power BI

[!include[banner](../includes/banner.md)]


Toto téma popisuje 365 Dynamics pro operace - obsah organizační školení Power BI. Tento článek vysvětluje, jak získat přístup k obsahu pack a popisuje datový model a subjekty, které byly použity k sestavení obsahu pack.

<a name="accessing-the-content-pack"></a>Přístup k obsahu pack
--------------------------

Obsahu pack organizační školení můžete najít v knihovně Sdílené datové zdroje v Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení obsahu pack a připojit k vaší 365 Microsoft Dynamics pro datové operace, viz [obsahu Power BI od společnosti Microsoft a partnerů LCS](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí obsahu pack
Po připojení obsahu pack do aplikace Dynamics 365 pro operace data, sestavy zobrazit data organizace. Pokud jste dosud nepoužívali Microsoft Power BI před, bližší informace na [s asistencí výukové stránky pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí obsahu pack mají grafy a tabulky, které obsahují další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava          | Obsah                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurz analýza | Registrace podle umístění, Účastníci kurzu podle stavu a seznam registrací |
| Typy kurzů    | Typy kurzů podle dovednosti                                                       |

Můžete filtrovat grafy a dlaždice v těchto sestavách a Připnutí grafů a dlaždice pro řídicí panel. Další informace o filtru a pin v Power BI, viz [vytvoření a konfigurace řídicího panelu A](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Dynamics 365 pro datové operace se používá k naplnění sestavy v obsahu pack organizační školení. Následující tabulka zobrazuje entity, aby byla na základě obsahu pack.

| Celek                    | Obsah                                                         | Vztahy s jinými subjekty                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Školení\_CalendarOffset  | Kalendář posuny na řezu sestavy                                | Školení\_vzdělávání CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_společnosti         | Chcete-li filtrovat zprávy společnosti                                   | Školení\_vzdělávání CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_kurzu          | Kurzu, popis, Instruktor název, umístění, místnosti a stav | Školení\_vzdělávání CourseAgenda\_CourseAttendees vzdělávání\_CourseSkill                                                                                                                             |
| Školení\_CourseAgenda    | Agenda kurzu a počáteční a koncové časy                          | Školení\_školení společnosti\_CalendarOffset vzdělávání\_datum školení\_kurzu                                                                                                                         |
| Školení\_CourseAttendees | Datum název, stav, úlohy a registrace                         | Školení\_školení společnosti\_CalendarOffset vzdělávání\_datum školení\_demografické údaje školení\_zaměstnanost, vzdělávání\_kurzu školení\_vzdělávání WorkerName\_WorkerTitle vzdělávání\_projektu vzdělávání\_pozice |
| Školení\_CourseSkill     | Úrovni, typ dovednosti a dovednosti                                     | Školení\_kurzu                                                                                                                                                                                   |
| Školení\_datum            | Dny, týdny, měsíce a roky                                   | Školení\_vzdělávání CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_demografické údaje    | Datum narození, pohlaví, etnického původu a rodinného stavu         | Školení\_vzdělávání CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_zaměstnání      | Počáteční datum, koncové datum a datum přechodu                        | Školení\_vzdělávání CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_práce             | Funkce, typ a název                                        | Školení\_vzdělávání CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_pozice        | Umístění, název a ekvivalent plného úvazku (FTE)                  | Školení\_vzdělávání CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_WorkerName      | Jméno, příjmení a celé jméno                             | Školení\_CourseAttendees                                                                                                                                                                          |
| Školení\_WorkerTitle     | Datum název a služebního věku                                         | Školení\_CourseAttendees                                                                                                                                                                          |

Tyto entity byly použity k vytvoření vypočítaných rozměrů v datovém modelu. Tyto vypočtena opatření se poté použije pro výpočet klíčových ukazatelů výkonu (KPI) a sestavy, které jsou použity v obsahu pack. Pokud chcete zahrnout další výpočty v sestavách a řídicího panelu, můžete stáhnout a upravit soubor Training.pbix z LCS. Tento soubor je výchozí datový model, který byl použit k vytvoření obsahu pack. Poté, co jste provedli změny, můžete vytvořit obsahu pack organizační a řídicí panel, který obsahuje informace, které jste přidali.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





