---
title: "Obsah Power BI pro nábor"
description: "Toto téma popisuje obsah Power BI pro aplikaci Dynamics 365 for Operations - Recruiting. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu."
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

# <a name="recruiting-power-bi-content"></a>Obsah Power BI pro nábor

[!include[banner](../includes/banner.md)]


Toto téma popisuje obsah Power BI pro aplikaci Dynamics 365 for Operations - Recruiting. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu.

<a name="accessing-the-content-pack"></a>Přístup k balíčku obsahu
--------------------------

Balíček obsahu metrik pro nábor naleznete v knihovně sdíleného majetku ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení balíčku obsahu a připojení k datům aplikace Microsoft Dynamics 365 for Operations naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům z aplikace Dynamics 365 for Operations zobrazí sestavy data vaší organizace. Pokud jste aplikaci Microsoft Power BI nikdy předtím nepoužívali, vyhledejte si další informace v tématu [Řízená výuka pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sestavy, které jsou součástí balíčku obsahu, mají grafy a tabulky obsahující další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                       | Obsah                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Analýza uchazeče           | Uchazeči podle práce, zdrojů uchazeče, uchazeči podle umístění a celkový počet uchazečů           |
| Stav uchazeče             | Uchazeč podle typu a stavu a stav uchazeče                                                    |
| Demografické údaje uchazeče       | Uchazeči podle věku a pohlaví a úroveň vzdělání a stav uchazeče                             |
| Analýza náboru          | Čistý poměr náborů, průměrný počet dní pro nábor, procento chybných náborů a náklady na nábor                    |
| Analýza náborového projektu | Počet náborových projektů, volná místa podle náborového projektu a uchazeči podle náborového projektu |

Grafy a dlaždice v těchto sestavách můžete filtrovat a ukotvit je na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data aplikace Dynamics 365 for Operations se používají k naplnění sestav v balíčku obsahu metrik náboru. Následující tabulka zobrazuje entity, na kterých je balíček obsahu založen.

| Celek                          | Obsah                                                         | Vztahy s jinými entitami                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nábor\_Uchazeč           | Uchazeči, přijatí uchazeči, čistý poměr náboru a náklady          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Křestní jméno, příjmení a celé jméno uchazeče                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Posuny kalendáře pro řez sestav                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Společnosti, podle kterých se filtrují sestavy                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Dny, týdny, měsíce a roky                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Datum narození, pohlaví, etnický původ a rodinný stav         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Uchazeč, výkon, datum zahájení a typ žadatele           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Počáteční datum, koncové datum a datum přechodu                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | Město, okres, PSČ a stát nebo kraj                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Funkce, typ a název                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Zdroj uchazečů                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Ohodnocení, popis a model ohodnocení                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Popis projektu, stavu projektu a volných míst                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Vyřazení uchazeči, důvod, výkon a datum vyřazení | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v balíčku obsahu. Pokud chcete zahrnout další výpočty do sestav a řídicího panelu, můžete stáhnout a upravit soubor Recruiting.pbix z LCS. Tento soubor představuje výchozí datový model, který byl použit k vytvoření balíčku obsahu. Po provedení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





