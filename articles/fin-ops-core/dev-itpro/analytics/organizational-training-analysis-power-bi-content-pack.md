---
title: Obsah školení organizace v Power BI
description: Toto téma popisuje obsah Finance and Operations – Školení organizace Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cd48c12ea3ea31904c437f678888a51e5381cfcfbeef0e1c709858b0c6cb857d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763541"
---
# <a name="organizational-training-power-bi-content"></a>Obsah školení organizace v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje obsah Finance and Operations – Školení organizace Power BI.

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům zobrazí sestavy dat vaší organizace. Pokud jste aplikaci Microsoft Power BI nikdy předtím nepoužívali, vyhledejte si další informace v tématu [Řízená výuka pro Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí balíčku obsahu, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava          | Obsah                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analýza kurzu | Registrace podle umístění, účastníci kurzu podle stavu a seznam registrací |
| Typy kurzů    | Typy kurzů podle dovednosti                                                       |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data aplikace se používají k naplnění sestav v balíčku obsahu organizačního školení. Následující tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                    | Obsah                                                         | Vztahy s jinými entitami |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Školení\_CalendarOffset  | Posuny kalendáře pro řez sestav                                | Training\_CourseAgenda, Training\_CourseAttendees |
| Školení\_Společnost         | Společnosti, podle kterých se filtrují sestavy                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Školení\_Kurz          | Kurz, popis, jméno školitele, umístění, místnosti a stav | Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill |
| Školení\_CourseAgenda    | Agenda kurzu a počáteční a koncové časy                          | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course |
| Školení\_CourseAttendees | Název, stav, práce a datum registrace                         | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position |
| Školení\_CourseSkill     | Dovednost, typ dovednosti a úroveň                                     | Školení\_Kurz |
| Školení\_Datum            | Dny, týdny, měsíce a roky                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Školení\_Demografické údaje    | Datum narození, pohlaví, etnický původ a rodinný stav         | Training\_CourseAgenda, Training\_CourseAttendees |
| Školení\_Zaměstnání      | Počáteční datum, koncové datum a datum přechodu                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Školení\_Práce             | Funkce, typ a název                                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Školení\_Pozice        | Pozice, titul a ekvivalent plného úvazku (FTE)                  | Training\_CourseAgenda, Training\_CourseAttendees |
| Školení\_WorkerName      | Křestní jméno, příjmení a celé jméno                             | Školení\_CourseAttendees |
| Školení\_WorkerTitle     | Název a datum služebního věku                                         | Školení\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]