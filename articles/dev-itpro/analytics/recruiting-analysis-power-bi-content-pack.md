---
title: Obsah náboru v Power BI
description: Toto téma popisuje obsah náboru v Power BI. Vysvětluje přístup k sestavám a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2d8c0e0e52a8dba2a1ea5bf330cdea01e3cfb60d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544973"
---
# <a name="recruiting-power-bi-content"></a>Obsah náboru v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje obsah **náboru** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah **Nábor** v Power BI se zobrazí v pracovním prostoru **Řízení náboru**.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Sestavy a vizuální informace v pracovním prostoru řízení náboru
Pracovní prostor **Řízení náboru obsahuje** kartu **Analýza**. Tato karta zahrnuje obsah Power BI pro nábor. Obsah je tvořen kartou Přehled a dalšími kartami, které obsahují podrobnosti. Následující tabulka obsahuje popis daných sestav na jednotlivých kartách.

| Sestava               | Obsah |
|----------------------|----------|
| Přehled náboru | Uvádí souhrn dalších sestav |
| Analýza uchazeče   | Celkový počet uchazečů, uchazečů podle práce, zdrojů uchazeče, uchazečů podle pohlaví a uchazečů podle umístění |
| Stav uchazeče     | Uchazeč podle typu a stavu a stav uchazeče |
| Analýza náboru  | Poměr čistého náboru, průměrný počet dnů náboru procento chybných náborů, nákladů na nábor, počtu náborových projektů, žádostí o přijetí do zaměstnání a počet žadatelů vs. volných míst podle náborového projektu |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Následující tabulka zobrazuje entity, na kterých je balíček obsahu **Nábor** Power BI založen.

| Celek               | Obsah                                                         | Vztahy s jinými entitami |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Uchazeč            | Uchazeči, přijatí uchazeči, čistý poměr náboru a náklady          | Jméno uchazeče, Společnost, Posun v kalendáři, Datum, Zeměpisná poloha, Demografické údaje, Pracovní místo, Média, Projekt náboru |
| Jméno uchazeče       | Křestní jméno, příjmení a celé jméno uchazeče                   | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Posuny kalendáře      | Posuny kalendáře pro řez sestav                                | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Společnost              | Společnosti, podle kterých se filtrují sestavy                                   | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Datum                 | Dny, týdny, měsíce a roky                                   | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Demografické údaje         | Datum narození, pohlaví, etnický původ a rodinný stav         | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Zaměstnaný uchazeč   | Uchazeč, výkon, datum zahájení a typ žadatele           | Společnost, Posun v kalendáři, Datum, Zeměpisná poloha, Jméno uchazeče, Zaměstnání, Výkon, Demografické údaje, Pracovní místo, Média, Projekt náboru |
| Zaměstnání           | Počáteční datum, koncové datum a datum přechodu                        | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Geografické umístění  | Město, okres, PSČ a stát nebo kraj                 | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Práce                  | Funkce, typ a název                                        | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Média                | Zdroj uchazečů                                             | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Výkonnost          | Ohodnocení, popis a model ohodnocení                            | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Náborový projekt  | Popis projektu, stavu projektu a volných míst                | Uchazeč, zaměstnaný uchazeč, uchazeč s výpovědí |
| Uchazeč po výpovědi | Vyřazení uchazeči, důvod, výkon a datum vyřazení | Společnost, Posun v kalendáři, Datum, Zeměpisná poloha, Demografické údaje, Pracovní místo, Média, Projekt náboru, Jméno uchazeče |
