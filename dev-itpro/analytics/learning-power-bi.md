---
title: "Obsah Power BI pro výuku"
description: "Toto téma popisuje obsah Power BI pro výuku. Vysvětluje přístup k sestavám a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a3f28d21a7e73d3ad462c5cc37198dd2b6f5f8af
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="learning-power-bi-content"></a>Obsah Power BI pro výuku

[!include[banner](../includes/banner.md)]

Toto téma popisuje obsah **Výuka** v Microsoft Power BI. Vysvětluje, jak získat přístup k obsahu, a popisuje datový model a entity, které byly k sestavení obsahu použity.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Pokud používáte aktualizaci aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition z července 2017, najdete obsah Power BI **Výuka** v knihovně sdíleného majetku ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI

Sestavy, které jsou součástí obsahu **Výuka**, obsahují grafy a tabulky s dalšími informacemi. Následující tabulka obsahuje popis daných sestav.

| Sestava                | Obsah |
|-----------------------|----------|
| Přehled výuky     | Souhrn dalších sestav |
| Analýza kurzu       | Registrace podle umístění, účastníci podle stavu, kurzy podle typu u každé společnosti a účast na kurzu podle práce |
| Analýza registrace | Seznam registrací |
| Typy kurzů          | Typy kurzů podle dovednosti |
| Analýza instruktora   | Poměr kurzů k počtu instruktorů, počet instruktorů, počet kurzů od instruktora, počet kurzů na instruktora a program kurzu od instruktora |
| Kurzy, které jsou k dispozici       | Seznam kurzů |
| Formát kurzů        | Agenda kurzu |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Tato data se používají k vyplňování sestav v obsahu Power BI **Výuka**. Tato tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek           | Obsah                                                         | Vztahy s jinými entitami |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Posuny kalendáře  | Posuny kalendáře pro řez sestav                                | Program kurzu, účastníci kurzu |
| Společnost          | Společnosti, podle kterých se filtrují sestavy                                   | Program kurzu, účastníci kurzu |
| Kurz           | Kurz, popis, jméno školitele, umístění, místnosti a stav | Program kurzu, účastníci kurzu, dovednost kurzu |
| Program kurzu    | Agenda kurzu a počáteční a koncové časy                          | Společnost, posun kalendáře, datum, kurz |
| Účastníci kurzu | Název, stav, práce a datum registrace                         | Společnost, posun kalendáře, datum, kurz, demografické údaje, práce, kurz, jméno zaměstnance, titul zaměstnance, zaměstnání, pozice |
| Dovednost kurzu     | Dovednost, typ dovednosti a úroveň                                     | Kurz |
| Datum             | Dny, týdny, měsíce a roky                                   | Program kurzu, účastníci kurzu |
| Demografické údaje     | Datum narození, pohlaví, etnický původ a rodinný stav         | Program kurzu, účastníci kurzu |
| Zaměstnání       | Počáteční datum, koncové datum a datum přechodu                        | Program kurzu, účastníci kurzu |
| Práce              | Funkce, typ a název                                        | Program kurzu, účastníci kurzu |
| Pozice         | Pozice, titul a ekvivalent plného úvazku (FTE)                  | Program kurzu, účastníci kurzu |
| Jméno zaměstnance    | Křestní jméno, příjmení a celé jméno                             | Účastníci kurzu |
| Titul zaměstnance   | Název a datum služebního věku                                         | Účastníci kurzu |

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v obsahu. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor .pbix z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření obsahu. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

