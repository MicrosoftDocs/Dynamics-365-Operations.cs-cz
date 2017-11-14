---
title: "Obsah metriky pracovní síly Power BI"
description: "Toto téma popisuje obsah Power BI Metriky zaměstnanců. Vysvětluje přístup k sestavám a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a5b680b406f9be3e80b43259993a3e441391ec60
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-metrics-power-bi-content"></a>Obsah metriky pracovní síly Power BI

[!include[banner](../includes/banner.md)]

Toto téma popisuje obsah Power BI **Metriky zaměstnanců**. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah **Metriky zaměstnanců** v Power BI se zobrazuje v pracovním prostoru **Správa pracovníků**, pokud používáte jeden z následujících produktů:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017)
- Aplikace Microsoft Dynamics 365 for Talent

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
V následující tabulce jsou uvedeny metriky, které jsou zobrazeny pro každou sestavu.

| Sestava                                           | Metrika                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nastavení osob                                   | Souhrn dalších sestav                                                                                                                           |
| Analýza počtu osob ve společnosti, oddělení, umístění | Počet osob ve společnosti, počet osob podle oddělení, počet osob podle umístění a celkový počet osob                                                                                                                           |
| Úloha analýzy počtu osob, krok, manažer            | Počet osob podle úkolu, počet osob podle kroku, počet osob podle manažera a celkový počet osob                                                                                                                                      |
| Analýza trendů počtu osob                         | Počet osob tento rok versus minulý rok podle společnosti a postupný počet zaměstnanců za posledních 12 měsíců                                                                                                                        |
| Analýza FTE                                     | Celkový ekvivalent plného úvazku (FTE), celkem přiřazené FTE, FTE podle oddělení, FTE za posledních 12 měsíců, a FTE podle úlohy |
| Demografické složení pracovní síly                           | Počet osob podle věku a pohlaví, počet osob podle etnického původu, počet zaměstnanců podle stavu veterána, počet osob podle rodinného stavu, počet studentů na plný úvazek, průměrná doba služby, průměrný věk, poměr počtu žen k počtu mužů mezi zaměstnanci a jazyky, jakými zaměstnanci hovoří |
| Analýza pozice                                | Otevřené pozice podle oddělení, pozice otevřené k vyplnění, aktivní-neaktivní pozice a pozice podle oddělení                                                                                                   |
| Analýza úbytku pracovních sil                               | Přirozené úbytky v tomto roce oproti minulého roku, odcházející zaměstnanci podle pohlaví a věku, průměrné funkční období odcházejících zaměstnanců, zaměstnanci, kteří odešli tento měsíc a zaměstnanci, kteří odcházejí, podle důvodů                                                                   |
| Lidé podle oddělení                             | Zaměstnanci s osobním čísemo podle oddělení, pozice a přiřazení počátečního a koncového data                                                                                                                       |
| Analýza odsloužené doby                               | Průměrné funkční období, průměrný počet let ve společnosti a seznam podle služebního věku                                                                                                                                                              |
| Výročí zaměstnanců                           | Výročí tento měsíc, výročí příští měsíc, zaměstnanci podle odsloužených let a výročí, roky ve službě podle oddělení                                                                                                                                                                    |
| Narozeniny zaměstnance                               | Narozeniny tento měsíc, narozeniny další měsíc, narozeniny zaměstnanců a narozeniny podle oddělení a měsíce                                                                                                                                                                    |
| Projekty hromadného zařazení                               | Celkový počet projektů hromadného zařazení, projekty hromadného zařazení podle stavu, projekty hromadného zařazení podle oddělení a vlastníka, projekty hromadného zařazení podle úlohy a projekty hromadného zařazení                                                                                                                                                                    |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Rozšíření obsahu v Power BI
Pomocí balíčků obsahu, které jsou k dispozici ve službě Microsoft Dynamics Lifecycle Services (LCS) můžete poskytovat skvělou analýzu osobám, které nejsou přihlášeny k aplikaci Finance and Operations. Tyto balíčky obsahu můžete upravit tak, aby zahrnovaly jiné sestavy nebo vizuály, a potom publikovat balíčky obsahu na svého klienta Power BI.com pro analýzu.

Obsah **Metriky zaměstnanců** v Power BI najdete v knihovně sdíleného majetku ve službě LCS. Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

Nezapomeňte si stáhnout obsah **Metriky zaměstnanců** v Power BI, který se vztahuje k vámi používané verzi aplikace Microsoft Dynamics 365.

>[!NOTE]
>Soubory .pbix dostupné ve službě Lifecycle Services platí pouze pro aplikaci Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Následující tabulka zobrazuje entity, na kterých je obsah založen.

| Celek                   | Obsah                                                                            | Vztahy s jinými entitami |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Posuny kalendáře          | Posuny kalendáře pro řez sestav                                                   | Přiřazení k minulé pozici, trend pozice, trend zaměstnance, ukončený zaměstnanec |
| Společnost                  | Společnosti, podle kterých se filtrují sestavy                                                      | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Aktuální pozice         | Pozice k aktuálnímu datu, FTE, otevřené pozice a dlouhodobě otevřené pozice | Práce, pozice |
| Aktuální zaměstnanec         | Pracovníci k aktuálnímu datu, věk a počet zaměstnanců                                  | Společnost, geografické umístění, jméno zaměstnance, nadřízený, pracovní zařazení, demografické údaje, práce, zaměstnání, pozice |
| Datum                     | Dny, týdny, měsíce a roky                                                      | Přiřazení k minulé pozici, trend pozice, ukončený zaměstnanec, trend zaměstnance |
| Demografické údaje             | Datum narození, pohlaví, etnický původ a rodinný stav                            | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Zaměstnání               | Počáteční datum, koncové datum a datum přechodu                                           | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Geografické umístění      | Město, okres, PSČ a stát nebo kraj                                    | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Práce                      | Funkce, typ a název                                                           | Aktuální pozice, aktuální zaměstnanec |
| Minulá pozice | Důvod přiřazení, počáteční datum, koncové datum a práce                                    | Posun kalendáře, datum, práce, pozice |
| Pozice                 | Oddělení, FTE, pozice, typ pozice a název                                 | Aktuální pozice, aktuální zaměstnanec |
| Trend pozice           | Pozice během času, FTE a práce                                                   | Posun kalendáře, datum, práce, pozice |
| Nadřízená pozice               | Křestní jméno, příjmení a celé jméno                                                | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Ukončený pracovní poměr      | Propuštění pracovníci, datum ukončení, název, pozice a práce                      | Společnost, geografické umístění, jméno zaměstnance, nadřízený, posun kalendáře, datum, pracovní zařazení, demografické údaje, práce, zaměstnání, pozice |
| Jméno zaměstnance            | Křestní jméno, příjmení a celé jméno                                                | Aktuální pracovník, ukončený zaměstnanec, trend zaměstnance |
| Titul zaměstnance           | Název a datum služebního věku                                                            | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Trend zaměstnance           | Pracovníci během času, počet zaměstnanců, společnost a pozice                                 | Společnost, geografické umístění, jméno zaměstnance, nadřízený, posun kalendáře, datum, pracovní zařazení, demografické údaje, práce, zaměstnání |
| Projekt hromadného zařazení        | Počet projektů hromadného zařazení, vlastník projektu a stav projektu                     | Společnost, řádek Hromadné zařazení |
| Řádek hromadné zařazení           | Oddělení, typ zaměstnání a pozice                                           | Datum, pozice, projekt hromadného zařazení |

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se použijí k výpočtu klíčových ukazatelů výkonu a sestav, které se používají v obsahu Power BI. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor .pbix z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření obsahu Power BI. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.
