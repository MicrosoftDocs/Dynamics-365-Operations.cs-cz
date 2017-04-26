---
title: "Obsah finančního výkonu Power BI"
description: "Toto téma popisuje 365 Dynamics Microsoft finanční výsledky operací obsahu Pack pro Microsoft Power BI. Popisuje řídicích panelů a sestav, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Obsah finančního výkonu Power BI

[!include[banner](../includes/banner.md)]


Toto téma popisuje 365 Dynamics Microsoft finanční výsledky operací obsahu Pack pro Microsoft Power BI. Popisuje řídicích panelů a sestav, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu pack.

<a name="accessing-the-content-pack"></a>Přístup k obsahu pack
--------------------------

K dispozici jsou dvě verze obsahu pack finanční výsledky. Jedna verze je k dispozici z Microsoft Dynamics Lifecycle Services (LCS) a druhý je k dispozici na PowerBI.com.

-   **Verze, která je k dispozici z LCS:** finanční výsledky obsahu pack, která je k dispozici z LCS podporuje verzi operace 1611 Microsoft Dynamics 365. Obsahu pack můžete najít v knihovně Sdílené majetku v LCS. Další informace o stažení obsahu pack a připojit k vaší 365 Microsoft Dynamics pro datové operace, viz [obsahu Power BI od společnosti Microsoft a partnerů LCS](power-bi-content-microsoft-partners.md).
-   **Verze, která je k dispozici z PowerBI.com:** finanční výsledky obsahu pack, která je k dispozici z PowerBI.com podporuje aplikace Microsoft Dynamics AX verze 7.0 a 7.0.1. Další informace o tom, jak připojit a načíst vaše 365 Dynamics pro datové operace, viz [obsahu Power BI přístup z PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Nastavení hlavního účtu
Vzhledem k tomu, že organizace má závazky a částky výnosů jako kladné částky v sestavách, je důležité nastavení hlavních účtů v 365 Dynamics pro operace. Tyto hlavní účty jsou zobrazeny jako kladné částky, musí být typ hlavního účtu nastavena na **odpovědnosti** nebo **výnosů**. Pokud jsou použity tyto typy účtů, sestav pomocí nástroje Microsoft Power BI se reverzní příznaky a zobrazit jako kladné částky.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Řídicích panelů a sestav, které jsou součástí obsahu pack
Po připojení balíčku obsahu k datům z aplikace Dynamics 365 for Operations se na řídicím panelu a v sestavách zobrazí vaše finanční data. Pokud jste dosud nepoužívali BI napájení před, bližší informace na [s asistencí výukové stránky pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Řídicí panel obsahuje souhrnné dlaždice dat, která jsou založena na základních sestavách. Každá dlaždice obsahuje souhrnné informace pro aktuální rok v rámci všech společností v organizaci. Zde jsou některé z dlaždic:

-   Hotovost
-   Celkové výnosy tento rok
-   Celkové výdaje tento rok
-   Čistý příjem tento rok
-   Rychlý poměr
-   Celkové výdaje tento rok podle kategorie účtů
-   Aktuální poměr
-   Dluh k celkovým aktivům
-   Skutečné vs. předpokládané výnosy
-   Fakturované výnosy tento rok
-   Poměr provozních výdajů tento rok
-   Zisková marže tento rok
-   Skutečné vs rozpočtové výdaje – všechny společnosti

Každý kámen je zálohován podpůrných sestav. Tyto sestavy obsahují grafy a tabulky, které obsahují další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                      | Informace, které sestava obsahuje                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analýza hotovosti               | Právnickou osobou, hotovosti podle čtvrtletí, celkovou hotovost a hotovostní účet hotovosti **Poznámka:****hotovosti podle čtvrtletí** sestava neobsahuje počáteční zůstatky v celkovém součtu za první čtvrtletí. Zobrazuje celkové nové transakce, které jsou zaúčtovány v každém čtvrtletí.                                                                                |
| Analýza aktuálního poměru      | Aktuální poměr podle právnické osoby, aktuální poměr podle čtvrtletí a zůstatky pro aktuální aktiva a aktuální pasiva                                                                                                                                                                                                                              |
| Analýza rychlého poměru        | Rychlý poměr právnickou osobou, Rychlý poměr podle čtvrtletí a zůstatky hotovosti, účty pohledávek a aktuální závazky                                                                                                                                                                                                                      |
| Analýza nákladů prodaného zboží | Náklady prodaného zboží podle právnické osoby, náklady prodaného zboží pro tento rok a poslední rok podle čtvrtletí, náklady prodaného zboží pro prodej podle právnické osoby, celkové náklady prodaného zboží a podíl nákladů prodaného zboží k prodeji                                                                                                                                                                                   |
| Analýza pracovního kapitálu    | Pracovní kapitál podle právnické osoby, pracovní kapitál podle čtvrtletí, aktuální aktiva, aktuální pasiva a celkový pracovní kapitál                                                                                                                                                                                                                   |
| Analýza aktiv a dluhu     | Návratnost celkového majetku a dluhy celkového majetku podle právnické osoby, dluhy celkového majetku a návratnost celkového majetku podle čtvrtletí do současnosti, aktiva a pasiva                                                                                                                                                                                     |
| Analýza ziskové marže      | Aktuální a rozpočtová zisková marže podle právnické osoby, zisková marže podle čtvrtletí, podíl ziskové marže a zisková marže                                                                                                                                                                                                                       |
| Analýza čistého příjmu         | Aktuální a rozpočtový čistý příjem podle právnické osoby, čistý příjem tento rok a minulý rok a podíl výdajů a čistého příjmu                                                                                                                                                                                                                       |
| Analýza zisků           | Aktuální a rozpočtový zisk před započtením úroku a daní (EBIT) podle právnické osoby, EBIT tento rok a minulý rok, podíl výdajů a výnosů a aktuální a rozpočtové výdaje pro výnosy                                                                                                                                                          |
| Analýza výnosů            | Celkové výnosy, aktuální a rozpočtové celkové výnosy podle právnické osoby, celkové výnosy tento rok a minulý rok, odchylka rozpočtu výnosů podle právnické osoby a celkové výnosy za toto období a poslední období                                                                                                                                                 |
| Analýza výdajů            | Celkové výdaje, aktuální a rozpočtové celkové výdaje podle právnické osoby, aktuální a rozpočtové výdaje podle čtvrtletí, celkové výdaje podle kategorie účtů a poměr provozních výdajů                                                                                                                                                                 |
| Analýza fakturovaných výnosů     | Celkové pohledávky, celkové pohledávky právnickou osobou, součet pohledávek podle čtvrtletí a zůstatky pro účty pohledávek **Poznámka:** zprávy nechcete zahrnout počáteční zůstatky pro účty hlavní knihy pohledávek. Zobrazují celkové nové transakce, které jsou zaúčtovány na účty pohledávek. |

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data, která naplní řídicích panelů a sestav v obsahu pack finanční výkonnosti je Dynamics 365 pro datové operace. Tyto entity byly použity jako základ obsahu pack: **agregovat data entity**

-   **GeneralLedgerActivities** – tato entita agreguje zůstatky hlavní knihy podle kategorie účtů.
-   **BudgetActivities** – tato entita agreguje zůstatky rozpočtu podle kategorie účtů.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Hlavní knihy
-   ChartofAccounts

Tyto entity byly použity k vytvoření vypočítaných rozměrů v datovém modelu. Vypočítané rozměry jsou použity pro výpočet klíčových ukazatelů výkonu (KPI) a sestavy, které jsou použity v obsahu pack. Ve výchozím nastavení obsahuje balíček obsahu data za poslední tři roky a za jeden budoucí rok. Pokud budete chtít zahrnout další výpočty do svých sestav a řídicího panelu, můžete upravit [sešit aplikace Microsoft Excel](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Tento sešit představuje výchozí datový model, který byl použit k vytvoření balíčku obsahu. Po dokončení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)





