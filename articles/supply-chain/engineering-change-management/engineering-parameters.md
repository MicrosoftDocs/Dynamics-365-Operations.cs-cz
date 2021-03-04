---
title: Parametry správy technické změny
description: Toto téma vysvětluje, jak konfigurovat funkce správy technických změn pro Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 0cf0e56a8aece98379aa0f181d7b7ff665767544
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424266"
---
# <a name="engineering-change-management-parameters"></a>Parametry správy technické změny

[!include [banner](../includes/banner.md)]

Na stránce **Parametry řízení technických změn** jsou uvedeny parametry nastavení, které mění výchozí chování související se strukturou vydání produktu a procesy správy technických změn.

## <a name="open-the-engineering-change-management-parameters-page"></a>Otevřete stránku parametrů správy technických změn

Chcete-li otevřít stránku **Parametry řízení technických změn**, přejděte na **Řízení technických změn \> Založit \> Parametry řízení technických změn**. Poté můžete nastavit pole, jak je popsáno ve zbývajících částech tohoto tématu.

## <a name="release-control-tab"></a>Karta Uvolnit kontrolu

Následující tabulka popisuje pole, která jsou k dispozici na kartě **Uvolnit kontrolu** na stránce **Parametry řízení technických změn**. Tato pole ovlivňují proces struktury vydání produktu.

| Pole | popis |
|---|---|
| Pravidlo čísla položky | Vyberte, jak má být definováno číslo položky, když je produkt vydán právnické osobě. Vyberte *Číslo technického produktu*, pokud by se číslo produktu v přijímající právnické osobě mělo shodovat s číslem produktu v technické společnosti. Vyberte *Pořadí čísel místních položek*, pokud má produkt přijmout další číslo v pořadí čísel pro čísla produktů v přijímajícím právnickém subjektu. |
| Pravidlo názvu kusovníku | Vyberte, jak je definován název kusovníku (BOM) při přijetí (vydání) produktu v právnické osobě. Vyberte některou z možností *Název technického zpracování* nebo *Číslo přijímající položky*. |
| Pravidlo názvu postupu | Vyberte, jak je by měl být definován název trasy, když je přijata (vydána) trasa produktu v právnické osobě. Vyberte některou z možností *Název technického zpracování* nebo *Číslo přijímající položky*. |
| Spustit kontrolu kusovníku | Vyberte, zda bude kontrola kusovníku spuštěna při přijetí (vydání) produktu v právnické osobě. |
| Chování uvolnění neaktivního kusovníku | Vyberte, zda může být produkt vydán, pokud má neaktivní kusovník. Vyberte *Akceptovat*, *Pouze varování* nebo *Nepovoleno*. |
| Chování uvolnění neaktivního postupu | Vyberte, zda může být produkt vydán, pokud má neaktivní trasu. Vyberte *Akceptovat*, *Pouze varování* nebo *Nepovoleno*.|
| Přijetí produktu | Vyberte, zda je před uvolněním produktu v právnické osobě vyžadován další krok pro přijetí. Vyberte *Ručně* pro přidání kroku přijetí. V tomto případě se na stránce **Otevřít verze produktů** zobrazí produkty. Vyberte *Automaticky* k zobrazení produktu přímo na stránce **Uvolněné produkty** v cílové právnické osobě bezprostředně poté, co je produkt uvolněn spolu se strukturou vydání produktu. |

## <a name="engineering-change-management-tab"></a>Karta Správa technických změn

Následující tabulka popisuje pole, která jsou k dispozici na kartě **Správa technických změn** na stránce **Parametry řízení technických změn**. Tato nastavení ovlivňují proces správy technických změn.

| Pole | popis |
|---|---|
| Kategorie | Výchozí kategorie, která se použije při vytvoření požadavku na technickou změnu. |
| Priorita | Výchozí priorita, která se použije při vytvoření požadavku na technickou změnu. |
| Pravidlo závažnosti | Vyberte, jak by měla být stanovena závažnost objednávky technické změny. Vyberte *ruční*, pokud se očekává, že uživatel zadá hodnotu do pole **Závažnost**. Výběrem volby *Vypočítat* nechte systém vypočítat hodnotu pole **Závažnost**, když v podokně akcí objednávky technických změn vyberete **Vypočítat závažnost**. V takovém případě systém použije pravidla závažnosti, která jsou definována na stránce **Sada pravidel závažnosti**. Vyberte *Vypočítat automaticky*, aby se hodnota pole **Závažnost** vypočítala automaticky a vyplnila podle sad pravidel závažnosti. |
| Znovu uvolnit dotčené produkty | Toto pole je použitelné, když znovu vydáváte produkty prostřednictvím příkazu k technické změně. Můžete vybrat, zda mají být v dialogovém okně **Zprávy** navrženy všechny produkty nebo pouze dotčené produkty. |
| Úrovně kusovníku pro uvolnění | Hloubka úrovně kusovníku, který se má uvolnit. Pokud má kusovník více úrovní (tj. pokud je hlubší) než zde zadaná hodnota, budou uvolněny pouze úrovně do zadané hodnoty. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]