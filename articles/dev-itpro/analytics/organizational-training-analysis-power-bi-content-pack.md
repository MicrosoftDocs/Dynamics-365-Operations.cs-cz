---
title: "Obsah organizačních školení Power BI"
description: "Toto téma popisuje aplikaci Finance and Operations - Organizační obsah školení Power BI."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 18567a3241fce02e17df368f544e545fad93e1d9
ms.contentlocale: cs-cz
ms.lasthandoff: 03/23/2018

---

# <a name="organizational-training-power-bi-content"></a>Obsah organizačních školení Power BI

[!INCLUDE [banner](../includes/banner.md)]

Toto téma popisuje aplikaci Finance and Operations - Organizační obsah školení Power BI. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům z aplikace Finance and Operations zobrazí sestavy dat vaší organizace. Pokud jste aplikaci Microsoft Power BI nikdy předtím nepoužívali, vyhledejte si další informace v tématu [Řízená výuka pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí balíčku obsahu, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava          | Obsah                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analýza kurzu | Registrace podle umístění, účastníci kurzu podle stavu a seznam registrací |
| Typy kurzů    | Typy kurzů podle dovednosti                                                       |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data aplikace Finance and Operations se používají k naplnění sestav v balíčku obsahu organizačního školení. Následující tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                    | Obsah                                                         | Vztahy s jinými entitami                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Školení\_CalendarOffset  | Posuny kalendáře pro řez sestav                                | Školení\_Školení CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_Společnost         | Společnosti, podle kterých se filtrují sestavy                                   | Školení\_Školení CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_Kurz          | Kurz, popis, jméno školitele, umístění, místnosti a stav | Školení\_Školení CourseAgenda\_Školení CourseAttendees\_CourseSkill                                                                                                                             |
| Školení\_CourseAgenda    | Agenda kurzu a počáteční a koncové časy                          | Školení\_Školení společnosti\_CalendarOffset Školení\_Datum školení\_Kurz                                                                                                                         |
| Školení\_CourseAttendees | Název, stav, práce a datum registrace                         | Školení\_Školení společnosti\_CalendarOffset Školení\_Datum školení\_Demografické údaje školení\_Školení k zaměstnání\_Školicí kurz\_Školení WorkerName\_WorkerTitle Školení\_Školení k práci\_Pozice |
| Školení\_CourseSkill     | Dovednost, typ dovednosti a úroveň                                     | Školení\_Kurz                                                                                                                                                                                   |
| Školení\_Datum            | Dny, týdny, měsíce a roky                                   | Školení\_Školení CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_Demografické údaje    | Datum narození, pohlaví, etnický původ a rodinný stav         | Školení\_Školení CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_Zaměstnání      | Počáteční datum, koncové datum a datum přechodu                        | Školení\_Školení CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_Práce             | Funkce, typ a název                                        | Školení\_Školení CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_Pozice        | Pozice, titul a ekvivalent plného úvazku (FTE)                  | Školení\_Školení CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Školení\_WorkerName      | Křestní jméno, příjmení a celé jméno                             | Školení\_CourseAttendees                                                                                                                                                                          |
| Školení\_WorkerTitle     | Název a datum služebního věku                                         | Školení\_CourseAttendees                                                                                                                                                                          |





