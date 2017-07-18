---
title: "Obsah finanční výkonnosti Power BI"
description: "Toto téma popisuje obsah Power BI pro finanční výkonnost. Popisuje příslušné sestavy a řídicí panel a obsahuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu."
author: kweekley
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b20f526d20d357750777d0f9bda26e4d9d55b335
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="financial-performance-power-bi-content"></a>Obsah finanční výkonnosti Power BI

[!include[banner](../includes/banner.md)]

Toto téma popisuje obsah Microsoft Power BI **Finanční výkonnost**. Popisuje příslušné sestavy a řídicí panel a obsahuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Obsah Power BI **Finanční výkonnost** najdete ve službě Microsoft Dynamics Lifecycle Services LCS (LCS) a na adrese PowerBI.com.

### <a name="available-from-lcs"></a>K dispozici ve službě LCS
Obsah Power BI **Finanční výkonnost**, který je k dispozici v LCS, podporuje následující verze:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, aktualizace z července 2017
- Microsoft Dynamics 365 for Operations verze 1611 

Obsah Power BI najdete v knihovně sdíleného majetku ve službě LCS. Další informace o stažení balíčku obsahu a jeho implementaci ve vaší organizaci najdete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

### <a name="available-from-powerbicom"></a>Dostupné na adrese PowerBI.com
Verze obsahu Power BI **Finanční výkonnost** dostupná na adrese PowerBI.com podporuje verze aplikace Microsoft Dynamics AX 7.0 a 7.0.1. Další informace o připojení a načtení dat aplikace Dynamics AX najdete v tématu [Přístup k obsahu Power BI   webu PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Nastavení hlavního účtu
Protože pro organizace je žádoucí, aby se závazky a částky výnosů zobrazovaly ve výkazech jako kladné částky, je důležité správně nastavit hlavní účty. Aby se tyto hlavní účty zobrazovaly jako kladné částky, musí být typ hlavního účtu nastaven na **Pasiva** nebo **Výnos**. Při použití těchto typů účtů se při vykazování pomocí nástroje Power BI změní znaménka a částky se zobrazí jako kladné.

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Řídicí panely a výkazy, které jsou součástí obsahu Power BI
Řídicí panel obsahuje souhrnné dlaždice dat, která jsou založena na základních sestavách. Každá dlaždice obsahuje souhrnné informace pro aktuální rok v rámci všech společností v organizaci. Následuje několik příkladů dlaždic:

- Hotovost
- Celkové výnosy tento rok
- Celkové výdaje tento rok
- Čistý příjem tento rok
- Rychlý poměr
- Celkové výdaje tento rok podle kategorie účtů
- Aktuální poměr
- Dluh k celkovým aktivům
- Skutečné vs. předpokládané výnosy
- Fakturované výnosy tento rok
- Poměr provozních výdajů tento rok
- Zisková marže tento rok
- Skutečné vs rozpočtové výdaje – všechny společnosti

Každá z těchto dlaždic je podložena příslušnou sestavou. Tyto sestavy obsahují grafy a tabulky, které obsahují další informace. Následující tabulka obsahuje popis daných sestav.

| Sestava                      | Informace, které sestava obsahuje |
|-----------------------------|--------------------------------------|
| Analýza hotovosti               | Hotovost podle právnické osoby, hotovost podle čtvrtletí, hotovost celkem a hotovost podle účtu<blockquote>[!NOTE]<br>Informace o hotovosti ve čtvrtletí nezahrnuje u součtu za první čtvrtletí počáteční zůstatky. Zobrazuje celkové nové transakce, které jsou zaúčtovány v každém čtvrtletí.</blockquote> |
| Analýza aktuálního poměru      | Aktuální poměr podle právnické osoby, aktuální poměr podle čtvrtletí a zůstatky pro aktuální aktiva a aktuální pasiva |
| Analýza rychlého poměru        | Rychlý poměr podle právnické osoby, rychlý poměr podle čtvrtletí, zůstatky pro hotovost, pohledávky a aktuální pasiva |
| Analýza nákladů prodaného zboží | Náklady prodaného zboží podle právnické osoby, náklady prodaného zboží pro tento rok a poslední rok podle čtvrtletí, náklady prodaného zboží pro prodej podle právnické osoby, celkové náklady prodaného zboží a podíl nákladů prodaného zboží k prodeji |
| Analýza pracovního kapitálu    | Pracovní kapitál podle právnické osoby, pracovní kapitál podle čtvrtletí, aktuální aktiva, aktuální pasiva a celkový pracovní kapitál |
| Analýza aktiv a dluhu     | Návratnost celkového majetku a dluhy celkového majetku podle právnické osoby, dluhy celkového majetku a návratnost celkového majetku podle čtvrtletí do současnosti, aktiva a pasiva |
| Analýza ziskové marže      | Aktuální a rozpočtová zisková marže podle právnické osoby, zisková marže podle čtvrtletí, podíl ziskové marže a zisková marže |
| Analýza čistého příjmu         | Aktuální a rozpočtový čistý příjem podle právnické osoby, čistý příjem tento rok a minulý rok a podíl výdajů a čistého příjmu |
| Analýza zisků           | Aktuální a rozpočtový zisk před započtením úroku a daní (EBIT) podle právnické osoby, EBIT tento rok a minulý rok, podíl výdajů a výnosů a aktuální a rozpočtové výdaje pro výnosy |
| Analýza výnosů            | Celkové výnosy, aktuální a rozpočtové celkové výnosy podle právnické osoby, celkové výnosy tento rok a minulý rok, odchylka rozpočtu výnosů podle právnické osoby a celkové výnosy za toto období a poslední období |
| Analýza výdajů            | Celkové výdaje, aktuální a rozpočtové celkové výdaje podle právnické osoby, aktuální a rozpočtové výdaje podle čtvrtletí, celkové výdaje podle kategorie účtů a poměr provozních výdajů |
| Analýza fakturovaných výnosů     | Celkové pohledávky, celkové pohledávky podle právnické osoby, celkové pohledávky podle čtvrtletí a zůstatky pro účty pohledávek<blockquote>[!NOTE]<br>Informace nezahrnují počáteční zůstatky u účtů hlavní knihy pohledávek. Zobrazuje se zde součet nových transakcí, které jsou zaúčtovány na účty pohledávek.</blockquote> |

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Následující entity byly použity jako základ obsahu Power BI **Finanční výkonnost**:

**Agregované datové entity**

- **GeneralLedgerActivities** – Tato entita agreguje zůstatky hlavní knihy podle kategorie účtů.
- **BudgetActivities** – Tato entita agreguje zůstatky rozpočtu podle kategorie účtů.

**Datové entity**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Hlavní knihy
- ChartofAccounts

Tyto entity byly použity k vytvoření vypočítaných hodnot v datovém modelu. Vypočtené hodnoty se poté použijí pro výpočet klíčových ukazatelů výkonu a sestav, které se používají v obsahu. Ve výchozím nastavení obsahuje obsah data za poslední tři roky a za jeden budoucí rok. Pokud budete chtít zahrnout další výpočty do svých sestav a řídicího panelu, můžete upravit [sešit aplikace Microsoft Excel](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Tento sešit představuje výchozí datový model, který byl použit k vytvoření obsahu. Po dokončení změn můžete vytvořit organizační balíček obsahu a řídicí panel, který bude obsahovat vámi přidané informace.

