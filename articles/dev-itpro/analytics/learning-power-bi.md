---
title: "Obsah Power BI pro výuku"
description: "Toto téma popisuje obsah Power BI pro výuku."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0ee0cc2e22609d1a87e7d2b6dcd031606191f879
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="learning-power-bi-content"></a>Obsah Power BI pro výuku

[!include [banner](../includes/banner.md)]

Toto téma popisuje obsah **Výuka** v Microsoft Power BI.

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



