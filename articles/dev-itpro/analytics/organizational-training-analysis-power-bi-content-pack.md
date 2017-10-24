---
title: "Organizační obsah školení Power BI"
description: "Toto téma popisuje aplikaci Finance and Operations - Organizační obsah školení Power BI. Vysvětluje přístup k sestavám balíčku obsahu a poskytuje popis datového modelu a entit, které byly použity k sestavení obsahu."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e49d9af8b8bd8d5edb977c49742861199c6964fd
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="organizational-training-power-bi-content"></a>Organizační obsah školení Power BI

[!include[banner](../includes/banner.md)]


Toto téma popisuje aplikaci Finance and Operations - Organizační obsah školení Power BI. Vysvětluje přístup k sestavám balíčku obsahu a poskytuje popis datového modelu a entit, které byly použity k sestavení obsahu.

<a name="accessing-the-content-pack"></a>Přístup k balíčku obsahu
--------------------------

Balíček obsahu organizačního školení naleznete v knihovně sdíleného majetku ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení balíčku obsahu a připojení k datům aplikace Microsoft Dynamics 365 for Finance and Operations naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md).

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

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v balíčku obsahu. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor Training.pbix z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření balíčku obsahu. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





