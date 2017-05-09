---
title: "Obsah finanční výkonnosti Power BI"
description: "V tomto tématu je vysvětleno, jak využívat balíček obsahu pro finanční výkonnost z aplikace Microsoft Dynamics 365 for Operations pro aplikaci Microsoft Power BI. Popisuje se zde také způsob použití řídicího panelu a sestav, které jsou obsaženy v balíčku obsahu, a uvádí se informace o modelování dat a entitách, které se používaly k vytváření balíčku obsahu."
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

# <a name="financial-performance-power-bi-content"></a>Obsah finanční výkonnosti Power BI

[!include[banner](../includes/banner.md)]


V tomto tématu je vysvětleno, jak využívat balíček obsahu pro finanční výkonnost z aplikace Microsoft Dynamics 365 for Operations pro aplikaci Microsoft Power BI. Popisuje se zde také způsob použití řídicího panelu a sestav, které jsou obsaženy v balíčku obsahu, a uvádí se informace o modelování dat a entitách, které se používaly k vytváření balíčku obsahu.

<a name="accessing-the-content-pack"></a>Přístup k balíčku obsahu
--------------------------

K dispozici jsou dvě verze obsahu balíčku výkonnosti. Jedna verze je k dispozici ve službě Microsoft Dynamics Lifecycle Services (LCS) a druhý je k dispozici na PowerBI.com.

-   **Verze, která je k dispozici z LCS:** Balíček obsahu finančního výkonu, který je k dispozici z LCS, podporuje 1611 Microsoft Dynamics 365 for Operations verze 1611. Obsah balíčku můžete najít v knihovně sdíleného majetku v LCS. Další informace o stažení balíčku obsahu a připojení k datům aplikace Microsoft Dynamics 365 for Operations naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md).
-   **Verze, která je k dispozici z webu PowerBI.com:** Balíček obsahu finančního výkonu, který je k dispozici na webu PowerBI.com, podporuje Microsoft Dynamics AX versions 7.0 a 7.0.1. Další informace o připojení a načtení dat aplikace Microsoft Dynamics 365 for Operations naleznete v tématu [Přístup k obsahu Power BI z webu PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Nastavení hlavního účtu
Vzhledem k tomu, že organizace má závazky a částky výnosů, které se zobrazují jako kladné částky v sestavách, je důležité nastavení hlavních účtů v aplikaci Dynamics 365 for Operations. Aby se tyto hlavní účty zobrazovaly jako kladné částky, musí být typ hlavního účtu nastaven na **Pasiva** nebo **Výnos**. Pokud jsou použity tyto typy účtů, vykazování pomocí nástroje Microsoft Power BI změní znaménka a zobrazí částky jako kladné částky.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Řídicí panely a sestavy, které jsou součástí balíčku obsahu
Po připojení balíčku obsahu k datům z aplikace Dynamics 365 for Operations se na řídicím panelu a v sestavách zobrazí vaše finanční data. Pokud jste aplikaci Power BI předtím nepoužívali, můžete si o ní více přečíst zde: [Řízená výuka pro Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Řídicí panel obsahuje souhrnné dlaždice dat, která jsou založena na základních sestavách. Každá dlaždice obsahuje souhrnné informace pro aktuální rok v rámci všech společností v organizaci. Následuje několik příkladů dlaždic:

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

Každá z těchto dlaždic je podložena příslušnou sestavou. Tyto sestavy obsahují grafy a tabulky, které obsahují další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                      | Informace, které sestava obsahuje                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analýza hotovosti               | Hotovost podle právnické osoby, hotovost podle čtvrtletí, celková hotovost a hotovost podle účtu **Poznámka:** **Sestava hotovosti podle čtvrtletí** neobsahuje počáteční zůstatky v celkovém součtu za první čtvrtletí. Zobrazuje celkové nové transakce, které jsou zaúčtovány v každém čtvrtletí.                                                                                |
| Analýza aktuálního poměru      | Aktuální poměr podle právnické osoby, aktuální poměr podle čtvrtletí a zůstatky pro aktuální aktiva a aktuální pasiva                                                                                                                                                                                                                              |
| Analýza rychlého poměru        | Rychlý poměr podle právnické osoby, rychlý poměr podle čtvrtletí, zůstatky pro hotovost, pohledávky a aktuální pasiva                                                                                                                                                                                                                      |
| Analýza nákladů prodaného zboží | Náklady prodaného zboží podle právnické osoby, náklady prodaného zboží pro tento rok a poslední rok podle čtvrtletí, náklady prodaného zboží pro prodej podle právnické osoby, celkové náklady prodaného zboží a podíl nákladů prodaného zboží k prodeji                                                                                                                                                                                   |
| Analýza pracovního kapitálu    | Pracovní kapitál podle právnické osoby, pracovní kapitál podle čtvrtletí, aktuální aktiva, aktuální pasiva a celkový pracovní kapitál                                                                                                                                                                                                                   |
| Analýza aktiv a dluhu     | Návratnost celkového majetku a dluhy celkového majetku podle právnické osoby, dluhy celkového majetku a návratnost celkového majetku podle čtvrtletí do současnosti, aktiva a pasiva                                                                                                                                                                                     |
| Analýza ziskové marže      | Aktuální a rozpočtová zisková marže podle právnické osoby, zisková marže podle čtvrtletí, podíl ziskové marže a zisková marže                                                                                                                                                                                                                       |
| Analýza čistého příjmu         | Aktuální a rozpočtový čistý příjem podle právnické osoby, čistý příjem tento rok a minulý rok a podíl výdajů a čistého příjmu                                                                                                                                                                                                                       |
| Analýza zisků           | Aktuální a rozpočtový zisk před započtením úroku a daní (EBIT) podle právnické osoby, EBIT tento rok a minulý rok, podíl výdajů a výnosů a aktuální a rozpočtové výdaje pro výnosy                                                                                                                                                          |
| Analýza výnosů            | Celkové výnosy, aktuální a rozpočtové celkové výnosy podle právnické osoby, celkové výnosy tento rok a minulý rok, odchylka rozpočtu výnosů podle právnické osoby a celkové výnosy za toto období a poslední období                                                                                                                                                 |
| Analýza výdajů            | Celkové výdaje, aktuální a rozpočtové celkové výdaje podle právnické osoby, aktuální a rozpočtové výdaje podle čtvrtletí, celkové výdaje podle kategorie účtů a poměr provozních výdajů                                                                                                                                                                 |
| Analýza fakturovaných výnosů     | Celkové pohledávky, celkové pohledávky podle právnické osoby, součet pohledávek podle čtvrtletí a zůstatky pro účty pohledávek **Poznámka:** Sestavy nezahrnují počáteční zůstatky pro účty hlavní knihy pohledávek. Zobrazuje se součet nových transakcí, které jsou zaúčtovány na účty pohledávek. |

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data, která slouží k vyplnění řídicího panelu a sestav v balíčku obsahu pro finanční výkonnost, pocházejí z aplikace Dynamics 365 for Operations. Následující entity byly použity jako základ balíčku obsahu: **Agregované datové entity**

-   **GeneralLedgerActivities** – Tato entita agreguje zůstatky hlavní knihy podle kategorie účtů.
-   **BudgetActivities** – Tato entita agreguje zůstatky rozpočtu podle kategorie účtů.

**Datové entity**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Hlavní knihy
-   ChartofAccounts

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Tyto vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v balíčku obsahu. Ve výchozím nastavení obsahuje balíček obsahu data za poslední tři roky a za jeden budoucí rok. Pokud budete chtít zahrnout další výpočty do svých sestav a řídicího panelu, můžete upravit [sešit aplikace Microsoft Excel](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Tento sešit představuje výchozí datový model, který byl použit k vytvoření balíčku obsahu. Po dokončení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)





