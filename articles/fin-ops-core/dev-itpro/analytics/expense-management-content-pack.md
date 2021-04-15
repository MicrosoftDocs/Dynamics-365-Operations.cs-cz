---
title: Obsah správy výdajů v Power BI
description: Toto téma popisuje, co je součástí balíčku obsahu správy výdajů v Power BI.
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: aadf43d478eb4bf5af20df02dcc6399a7a2e71a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743500"
---
# <a name="expense-management-power-bi-content"></a>Obsah správy výdajů v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je součástí balíčku obsahu správy výdajů v Power BI. 

## <a name="overview"></a>Přehled
Dva balíčky obashu Power BI jsou k dispozici pro použití s modulem Správa výdajů ve verzi 8.1 a vyšší. 
- Pro zaměstnance, kteří předkládají vyúčtování výdajů, je určen osobní řídicí panel. 

  Řídicí panel je přizpůsoben tak, aby poskytoval základní informace jednotlivcům o neodeslaných a odeslaných částkách, a také historie a postřehy o historii výdajových transakcí. Osobní řídicí panel je jedna stránka obsahující nejdůležitější informace pro uživatele.

- Existuje řídicí panel správce určený pro úředníky a manažery závazků. Řídicí panel je šitý na míru vykazování a sledování celkových výdajů zaměstnance. Poskytuje klíčové výdajové metriky, jako jsou nepředložené výdaje, ujeté kilometry a průměrné částky z vyúčtování výdajů. Používá transakční data a poskytuje agregované zobrazení správy výdajů napříč všemi společnostmi. Také poskytuje rozdělení podle zaměstnanců, s možností přidat data finanční dimenze. Obsah analytiky vyúčtování správy obsahuje: 
  - Stránku přehledu s klíčovými metrikami ohledně částek výdajů a přehled konceptů, procesu a vyplněná vyúčtování výdajů. 
  - Stránk statistiky zaměstnance k zobrazení podrobných informací o zaměstnanci podle času, typu nákladů a statistické skupiny. 
  - Stránka porovnání zaměstnance k porovnání více zaměstnanců v čase. 

Všechny částky jsou zobrazeny v měně společnosti. Jsou zobrazeny údaje pro všechny společnosti, ale podle potřeby můžete přidat filtr společnosti. 

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah Expense Admin Dashboard.pbix a Expense Personal Dashboard.pbix Power BI můžete vyhledat v knihovně sdíleného majetku ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI LCS od společnosti Microsoft a vašich partnerů](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).
Obsah je k dispozici z pracovního prostoru Správa výdajů jako vložený obsah Power BI. Libovolný vlastník výdaje může přistupovat k osobním výdajů pro sebe, ale pouze úředníci a manažeři závazků mají přístup k obsahu pro správu, aby mohli prohlížet výdajová data všech uživatelů.

## <a name="refreshing-the-power-bi-content"></a>Aktualizace obsahu Power BI
Obsah Power BI správy výdajů vyžaduje aktualizaci měření TrvBiExpenseMeasurement a BudgetActivityMeasure z úložiště Entity. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsah zahrnuje sadu stránek sestav. Každá stránka obsahuje sadu metrik, které jsou zobrazovány jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizací v obsahu Power BI.

**Analýza osobních výdajů**

| Stránka sestavy | Vizualizace                             |
|-------------|-------------------------------------------|
| Moje výdaje | Částka za ujeté kilometry                         |
|             | Zpracovávaná vyúčtování výdajů                |
|             | Č. z neodeslaných výdajů               |
|             | Osobní výdaje k zaplacení              |
|             | Neodeslaná částka                        |
|             | Odeslaná částka                          |
|             | Částka čekající na úhradu             |
|             | Vyúčtování výdajů s částkami a stavem   |
|             | Odeslaná, ale neschválená vyúčtování výdajů  |
|             | Výdaje podle typu nákladů                     |
|             | Výdaje podle obchodníka                      |
|             | Výdaje podle zpracovaných výdajů            |
|             | Výdaje podle projektu                       |
|             | Celková částka transakce v čase        |

**Spravovat analýzy výdajů**

| Stránka sestavy         | Vizualizace                           |           
|---------------------|-----------------------------------------|
| Přehled výdajů    | Rámcová částka výdajů                   |
|                     | Počet rámcových řádků výdajů           |
|                     | Rámcové řádky výdajů                     |
|                     | Porušení zásad vyúčtování výdajů        |
|                     | Neuhrazená částka                      |
|                     | Odeslaná, ale neschválená vyúčtování výdajů       |
|                     | Schválené výdaje                       |
|                     | Celková částka výdajů                    |
|                     | Souhrny vyúčtování výdajů                |
|                     | Výdaje podle typu nákladů                   |
|                     | Výdaje podle obchodníka                    |
|                     | Výdaje zaplacené zaměstnanci                   |
|                     | Výdaje vs. projekt                     |
| Porovnání zaměstnanců | Částky výdajů                         |
|                     | Částky výdajů v čase podle zaměstnance   |
| Statistika zaměstnance | Vyúčtování výdajů podle typu nákladů            |
|                     | Osobní výdaje                       |
|                     | Vyúčtování výdajů podle skupin statistiky     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]