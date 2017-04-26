---
title: "O přijetí obsahu Power BI"
description: "Toto téma popisuje 365 Dynamics pro operace - obsah náborového Power BI. Popisuje, jak přístup k sestavám, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>O přijetí obsahu Power BI

[!include[banner](../includes/banner.md)]


Toto téma popisuje 365 Dynamics pro operace - obsah náborového Power BI. Popisuje, jak přístup k sestavám, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu pack.

<a name="accessing-the-content-pack"></a>Přístup k obsahu pack
--------------------------

Sada obsahu pro nábor můžete najít v knihovně Sdílené datové zdroje v Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení obsahu pack a připojit k vaší 365 Microsoft Dynamics pro datové operace, viz [obsahu Power BI od společnosti Microsoft a partnerů LCS](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí obsahu pack
Po připojení obsahu pack do aplikace Dynamics 365 pro operace data, sestavy zobrazit data organizace. Pokud jste dosud nepoužívali Microsoft Power BI před, bližší informace na [s asistencí výukové stránky pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí obsahu pack mají grafy a tabulky, které obsahují další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                       | Obsah                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Analýza žadatele           | Žadatel projektu, zdroje žadatele, žadatel podle umístění a celkový počet uchazečů           |
| Stav žadatele             | Žadatel podle typu a stavu a stav žadatele                                                    |
| Demografické údaje žadatele       | Žadatelů podle věku a pohlaví a úroveň vzdělání a stav žadatele                             |
| O přijetí analýzy          | Pronájem poměr netto, průměrný počet dní, které chcete najmout, procento chybných hires a náklady náboru                    |
| Analýza projektu náboru | Počet náborových projektů, otvory podle náborového projektu a žadatelů podle náborového projektu |

Můžete filtrovat grafy a dlaždice v těchto sestavách a Připnutí grafů a dlaždice pro řídicí panel. Další informace o filtru a pin v Power BI, viz [vytvoření a konfigurace řídicího panelu A](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Dynamics 365 pro datové operace se používá k naplnění sestavy v obsahu pack nábor. Následující tabulka zobrazuje entity, aby byla na základě obsahu pack.

| Celek                          | Obsah                                                         | Vztahy s jinými subjekty                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nábor\_žadatele           | Žadatelé, přijaté uchazeče, poměr čistého nájmu a náklady          | Nábor\_nábor ApplicantName\_společnosti o přijetí\_CalendarOffset Recuriting\_datum přijetí\_GeographicLocation o přijetí\_demografické údaje o přijetí\_projektu náboru\_Media nábor\_RecruitmentProject                                |
| Nábor\_ApplicantName       | Žadatel jméno, příjmení a celé jméno                   | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_CalendarOffset      | Kalendář posuny na řezu sestavy                                | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_společnosti             | Chcete-li filtrovat zprávy společnosti                                   | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_datum                | Dny, týdny, měsíce a roky                                   | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_demografické údaje        | Datum narození, pohlaví, etnického původu a rodinného stavu         | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_EmployedApplicant   | Žadatel, výkon, datum zahájení a typu žadatele           | Nábor\_společnosti o přijetí\_nábor CalendarOffset\_datum přijetí\_nábor GeographicLocation\_ApplicantName o přijetí\_přijetí zaměstnání\_nábor výkon\_projektu náboru\_Media nábor\_RecruitmentProject          |
| Nábor\_zaměstnání          | Počáteční datum, koncové datum a datum přechodu                        | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_GeographicLocation  | Město, kraj, poštovní kód a Okres                 | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_práce                 | Funkce, typ a název                                        | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_Media               | Zdroje uchazečů                                             | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_výkon         | Model hodnocení, hodnocení a popis                            | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_RecruitmentProject  | Popis projektu, stav projektu a otvory                | Nábor\_žadatele náboru\_přijetí EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Nábor\_TerminatedApplicant | Ukončeno žadatelů, důvodem je výkon a datum ukončení | Nábor\_společnosti o přijetí\_CalendarOffset o přijetí\_datum přijetí\_nábor GeographicLocation\_nábor výkon\_demografické údaje o přijetí\_přijetí zaměstnání\_Media nábor\_nábor RecruitmentProject\_ApplicantName |

Tyto entity byly použity k vytvoření výpočtové míry. Tyto vypočtena opatření se poté použije pro výpočet klíčových ukazatelů výkonu (KPI) a sestavy, které jsou použity v obsahu pack. Pokud chcete zahrnout další výpočty v sestavách a řídicího panelu, můžete stáhnout a upravit soubor Recruiting.pbix z LCS. Tento soubor je výchozí datový model, který byl použit k vytvoření obsahu pack. Poté, co jste provedli změny, můžete vytvořit obsahu pack organizační a řídicí panel, který obsahuje informace, které jste přidali.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





