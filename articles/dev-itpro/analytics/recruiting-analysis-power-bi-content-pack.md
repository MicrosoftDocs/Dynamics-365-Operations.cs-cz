---
title: "Obsah Power BI pro nábor"
description: "Toto téma popisuje obsah Power BI pro nábor. Vysvětluje přístup k sestavám a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu."
author: jcart1106
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 22138ab34243aa5f8c74f785ce3aaf68b27b9622
ms.contentlocale: cs-cz
ms.lasthandoff: 12/01/2017

---

# <a name="recruiting-power-bi-content"></a>Obsah Power BI pro nábor

[!include[banner](../includes/banner.md)]

Toto téma popisuje obsah **Nábor** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah Power BI **Nábor** se zobrazí v pracovním prostoru **Řízení náboru**. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Sestavy a vizuální informace v pracovním prostoru řízení náboru
Pracovní prostor **Řízení náboru** obsahuje kartu **Analýza**. Tato karta zahrnuje obsah Power BI Embedded pro nábor. Obsah je tvořen kartou Přehled a dalšími kartami, které obsahují podrobnosti. Následující tabulka obsahuje popis daných sestav na jednotlivých kartách.

| Sestava               | Obsah |
|----------------------|----------|
| Přehled náboru | Uvádí souhrn dalších sestav |
| Analýza uchazeče   | Celkový počet uchazečů, uchazečů podle práce, zdrojů uchazeče, uchazečů podle pohlaví a uchazečů podle umístění |
| Stav uchazeče     | Uchazeč podle typu a stavu a stav uchazeče |
| Analýza náboru  | Poměr čistého náboru, průměrný počet dnů náboru procento chybných náborů, nákladů na nábor, počtu náborových projektů, žádostí o přijetí do zaměstnání a počet žadatelů vs. volných míst podle náborového projektu |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Následující tabulka zobrazuje entity, na kterých je obsah **Nábor** v Power BI založen.

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

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v obsahu. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor Recruiting.pbix z aplikace Microsoft Dynamics Lifecycle Services (LCS). Tento soubor představuje výchozí datový model, který byl použit k vytvoření obsahu. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

