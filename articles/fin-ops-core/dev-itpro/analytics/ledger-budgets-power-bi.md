---
title: Obsah porovnání skutečnosti a rozpočtu v Power BI
description: Toto téma popisuje obsah Power BI pro porovnání skutečné situace s rozpočtem. Vysvětluje, jak přistupovat k sestavám, a poskytuje informace o datovém modelu.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 908b96af5b3d67f265953648edd6aa7ec31556a4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093841"
---
# <a name="actual-vs-budget-power-bi-content"></a>Obsah porovnání skutečnosti a rozpočtu v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje obsah **porovnání skutečné situace s rozpočtem** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **skutečnost a rozpočet** v Power BI byl vytvořen pro uživatele, kteří odpovídají za sledování a porovnávání skutečných výsledků s rozpočtem v rámci organizace. Obsah **Skutečnost a rozpočet** v Power BI usnadňuje kontrolu odchylek rozpočtu. Můžete analyzovat rozpočet pro aktuální rok podle kategorie účtu, kódu rozpočtu, hlavního účtu, popisu hlavního účtu nebo fiskálního období a získat užitečné informace o příčinách odchylek.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Sestavy z obsahu **Skutečnost a rozpočet** v Power BI se zobrazují v pracovních prostorech **Rozpočty hlavní knihy a prognózy** a **CFO**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI
Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu **Skutečnost a rozpočet** v Power BI.

| Sestava                      | Metrika                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Výdaje - Skutečné a rozpočtové | <ul><li>Celkové výdaje za tento rok</li><li>Celkové výdaje v rozpočtu za tento rok</li></ul>  |
| Výnosy - Skutečné a rozpočtové  | <ul><li>Celkové výnosy za tento rok</li><li>Celkové výnosy v rozpočtu za tento rok</li><ul>     |
| Výdaj                     | <ul><li>Celkové výdaje za tento rok</li><li>Cílová výše výdajů podle rozpočtu</li><ul> |
| Výnosy                     | <ul><li>Celkové výnosy za tento rok</li><li>Cílová výše výnosů podle rozpočtu</li><ul>   |
| Čistý příjem                  | <ul><li>Čistý příjem za tento rok</li><li>Cílová výše čistého příjmu podle rozpočtu</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

| Celek                    | Obsah                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Aktivity hlavní knihy | Částky transakcí pro hlavní knihu                                       |
| Aktivity rozpočtu         | Částky transakcí pro registr rozpočtu                                      |
| Hlavní účty             | Hlavní účty pro filtrování sestav                                               |
| Fiskální kalendáře          | Fiskální kalendáře pro filtrování sestav                                            |
| Hlavní knihy                   | Hlavní knihy, které lze použít k filtrování sestavy u aktuální hlavní knihy              |
| Kódy rozpočtu              | Kódy rozpočtu pro filtrování sestav                                                |
| Právnické osoby            | Právnické osoby, které lze použít k filtrování sestavy u aktuální právnické osoby |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]