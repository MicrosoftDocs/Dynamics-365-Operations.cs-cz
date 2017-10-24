---
title: "Obsah zaměstnaneckých výhod v Power BI"
description: "Toto téma popisuje obsah zaměstnaneckých výhod v Power BI. Vysvětluje přístup k obsaženým sestavám a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
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
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e650047473136d1aaf455e96f9d7c63a426563f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="benefits-power-bi-content"></a>Obsah zaměstnaneckých výhod v Power BI

[!include[banner](../includes/banner.md)]

Toto téma popisuje obsah **zaměstnaneckých výhod** v Microsoft Power BI. Vysvětluje přístup k obsaženým sestavám a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah **Zaměstnanecké výhody** v Power BI se zobrazuje v pracovním prostoru **Správa zaměstnaneckých výhod**, pokud používáte jeden z následujících produktů:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017)
- Aplikace Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI
Sestavy, které jsou součástí obsahu **Zaměstnanecké výhody**, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                       | Obsah                                                                                       |
|------------------------------|------------------------------------------------------------------------------------------------|
| Přehled registrací k zaměstnaneckým výhodám  | Nejvíce a nejméně registrované plány, registrace podle skupiny zaměstnanců a vybrané možnosti zaměstnaneckých výhod |
| Zaměstnanecké výhody            | Přihlášení zaměstnance podle vybrané zaměstnanecké výhody                                                        |
                                                                                             
Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Rozšíření obsahu v Power BI
Pomocí balíčků obsahu, které jsou k dispozici ve službě Microsoft Dynamics Lifecycle Services (LCS) můžete poskytovat skvělou analýzu osobám, které nejsou přihlášeny k aplikaci Finance and Operations. Tyto balíčky obsahu můžete upravit tak, aby zahrnovaly jiné sestavy nebo vizuály, a potom publikovat balíčky obsahu na svého klienta Power BI.com pro analýzu.

Obsah **Zaměstnanecké výhody** v Power BI naleznete v knihovně sdíleného majetku ve službě LCS. Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

>[!NOTE]
>Soubory .pbix dostupné ve službě Lifecycle Services platí pouze pro aplikaci Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Následující data se používají k vyplňování sestav v obsahu **Zaměstnanecké výhody** Power BI. Tato tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                   | Obsah                                                                                                   | Vztahy s jinými entitami |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Posuny kalendáře          | Posuny kalendáře pro řez sestav                                                                          | Přiřazení k minulé pozici, trend pozice, trend zaměstnance, ukončený zaměstnanec |
| Společnost                  | Společnosti, podle kterých se filtrují sestavy                                                                             | Aktuální kompenzace, aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Kompenzace             | Mzdová sazba a frekvence v čase                                                                           | Aktuální kompenzace, aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Aktuální kompenzace     | Mzdová sazba a frekvence k aktuálnímu datu                                                              | Společnost, kompenzace, demografické údaje, práce, pozice |
| Aktuální pozice         | Pozice k aktuálnímu datu, ekvivalent k plnému úvazku, otevřené pozice a dlouhodobě otevřené pozice | Práce, pozice |
| Aktuální zaměstnanec         | Pracovníci k aktuálnímu datu, věk a počet zaměstnanců                                                         | Společnost, kompenzace, geografické umístění, jméno zaměstnance, nadřízený, pracovní zařazení, demografické údaje, práce, zaměstnání, pozice, zaměstnanecké výhody |
| Datum                     | Dny, týdny, měsíce a roky                                                                             | Přiřazení k minulé pozici, trend pozice, ukončený zaměstnanec, trend zaměstnance |
| Demografické údaje             | Datum narození, pohlaví, etnický původ a rodinný stav                                                   | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Zaměstnání               | Počáteční datum, koncové datum a datum přechodu                                                                  | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Geografické umístění      | Město, okres, PSČ a stát nebo kraj                                                           | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Práce                      | Funkce, typ a název                                                                                  | Aktuální pozice, aktuální zaměstnanec |
| Minulá pozice | Důvod přiřazení, počáteční datum, koncové datum a práce                                                           | Posun kalendáře, datum, práce, pozice |
| Pozice                 | Oddělení, FTE, pozice, typ pozice a název                                                        | Aktuální pozice, aktuální zaměstnanec |
| Trend pozice           | Pozice během času, FTE a práce                                                                          | Posun kalendáře, datum, práce, pozice |
| Nadřízená pozice               | Křestní jméno, příjmení a celé jméno                                                                       | Aktuální pracovník, ukončený zaměstnanec, trend zaměstnance |
| Ukončený zaměstnanec      | Ukončení zaměstnanci, datum ukončení, název, pozice a práce                                           | Společnost, kompenzace, geografické umístění, jméno zaměstnance, nadřízený, posun kalendáře, datum, pracovní zařazení, demografické údaje, práce, zaměstnání, pozice, zaměstnanecké výhody |
| Zam. výhody                 | Datum začátku platnosti, možnost zaměstnaneckých výhod, plán zaměstnaneckých výhod a typ výhod                                             | Aktuální jméno, ukončený zaměstnanec, trend zaměstnance |
| Jméno zaměstnance            | Křestní jméno, příjmení a celé jméno                                                                       | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Titul zaměstnance           | Název a datum služebního věku                                                                                   | Aktuální zaměstnanec, ukončený zaměstnanec, trend zaměstnance |
| Trend zaměstnance           | Pracovníci během času, počet zaměstnanců, společnost a pozice                                                        | Společnost, kompenzace, geografické umístění, jméno zaměstnance, nadřízený, posun kalendáře, datum, pracovní zařazení, demografické údaje, práce, zaměstnání, zaměstnanecké výhody |

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v obsahu. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor .pbix z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření obsahu. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

