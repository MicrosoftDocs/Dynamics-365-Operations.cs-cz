---
title: Obsah učení v Power BI
description: Toto téma popisuje obsah učení v Power BI.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8f97d4f59765840e215710e666079df3d4ecb878
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005772"
---
# <a name="learning-power-bi-content"></a>Obsah učení v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje obsah **učení** v Microsoft Power BI.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI

Sestavy, které jsou součástí obsahu **učení** v Power BI, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                | Obsah |
|-----------------------|----------|
| Přehled výuky     | Souhrn dalších sestav |
| Analýza kurzu       | Registrace podle umístění, účastníci podle stavu, kurzy podle typu u každé společnosti a účast na kurzu podle práce |
| Analýza registrace | Seznam registrací |
| Typy kurzů          | Typy kurzů podle dovednosti |
| Analýza instruktora   | Poměr kurzů k počtu instruktorů, počet instruktorů, počet kurzů od instruktora, počet kurzů na instruktora a program kurzu od instruktora |
| Kurzy, které jsou k dispozici       | Seznam kurzů |
| Formát kurzů        | Agenda kurzu |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Následující data se používají k vyplňování sestav v obsahu **učení** v Power BI. Tato tabulka zobrazuje entity, na kterých je balíček obsahu založen.

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
