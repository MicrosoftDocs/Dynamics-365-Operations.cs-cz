---
title: Konvence odepisování dlouhodobého majetku
description: Toto téma popisuje konvence odpisů pro dlouhodobý majetek.
author: moaamer
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e151d20fbfb9aa8fca9afc5be4f112b3de13cc7
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719798"
---
# <a name="fixed-asset-depreciation-conventions"></a>Konvence odepisování dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Toto téma popisuje konvence odpisů pro dlouhodobý majetek. Konvence odpisů se používají k určení, kdy a jak se vypočítá odpisu pro rok pořízení dlouhodobého majetku a v roce, kdy došlo k vyřazení dlouhodobého majetku.

Konvence odepisování lze přiřadit nastavení knihy skupiny dlouhodobého majetku. Chcete-li zobrazit nebo přiřadit způsob odpisu, v oblasti nastavení dlouhodobého majetku, vyberte skupinu **Dlouhodobý majetek**. Zvolte tlačítko **Knihy**. V tomto případě se konvence odepisování, které jsou přiřazeny, používají jako výchozí hodnoty při vytváření knih dlouhodobého majetku. Lze také nastavit konvence odpisu v knize jednotlivou položku dlouhodobého majetku. To provedete volbou **Knihy** v oblasti nastavení dlouhodobého majetku a volbou tlačítka **Skupiny dlouhodobého majetku**.

| Způsob odpisu   | Popis |
|---------------------------|-------------|
| Žádný                      | Majetek se začíná odepisovat datem <strong>uvedení do užívání</strong>. |
| Pololetí                 | Půlroční odpis je odepsán pro první rok a poslední rok odpisu majetku. Celý rok odpisu je odepsán pro každý rok během doby vratky. |
| Celý měsíc                | Majetek, který má datum <strong>uvedení do užívání</strong>, které se vyskytne kdykoli v průběhu počátečního měsíce odepisování na prvním dnem v měsíci. Pro účely odpisování se majetek považuje za vyřazený v poslední den předchozího měsíce. Konkrétní den měsíce, kdy byl odepsán, se nebere v potaz. |
| Polovina čtvrtletí               | Pro výpočet odpočtu na odpisu pro rok, kdy uvedete majetek do servisu vynásobte odpisy za celý rok procentuální hodnotou za čtvrtletí, kdy byl majetek uveden do provozu, jak je uvedeno v následující tabulce.<table><thead><tr><th>Čtvrtletí</th><th>Procento</th></tr></thead><tbody><tr><td>První</td><td>87.5</td></tr><tr><td>Druhý</td><td>62.5</td></tr><tr><td>Třetí</td><td>37.5</td></tr><tr><td>Čtvrtý</td><td>12.5</td></tr></tbody></table>Polovina čtvrtletí odpisů je převzata ve čtvrtletí, kdy byl majetek vyřazen (nebo čvrtletí, kdy byl plně odepsán). |
| Polovina měsíce (1. den v měsíci)  | Majetek, který má datum <strong>uvedeno do užívání</strong> v první polovině měsíce (dny 1 až 15) se začíná odepisovat prvním dnem v měsíci data <strong>uvedení do užívání</strong>. Majetek, který má datum <strong>uvedeno do užívání</strong> ve druhé polovině měsíce (dny 16 až konec měsíce) se začíná odepisovat prvním dnem v měsíci po datu <strong>uvedení do užívání</strong>. Majetek, který se v vyřadí v první polovině měsíce (den 1 až 15), je považován za vyřazený pro účely odpisů k poslednímu dni v předchozím měsíci. Majetek, který se v vyřadí ve druhé polovině měsíce (den 16 až konec měsíce), je považován za vyřazený pro účely odpisů k poslednímu dni měsíce vyřazení. |
| Polovina měsíce (15. den v měsíci) | Pro výpočet odpočtu na odpisu v roce, kdy majetek uvedete do užívání, vynásobte odpisy za celý rok zlomkem. Čitatel (číslo nahoře) v tomto zlomku činí počet celých měsíců v roce uvedení majetku do užívání plus 1/2 neboli 0,5. Jmenovatel (dolní číslo) je 12. Pokud majetek vyřadíte před koncem období zotavení, použijte stejnou metodu pro výpočet odpočtu odpisu v roce disponování. |
| Pololetí (počátek roku) | Majetek, který má datum <strong>uvedeno do užívání</strong> v první polovině roku, se začíná odepisovat k prvnímu dni v roce (celý rok). Majetek, který má datum <strong>uvedeno do užívání</strong> ve druhé polovině roku, se začíná odepisovat odprostřed roku. |
| Pololetí (příští rok)     | Majetek, který má datum <strong>uvedeno do užívání</strong> v první polovině roku, se začíná odepisovat k prvnímu dni v roce (celý rok). Majetek, který má datum <strong>uvedeno do užívání</strong> ve druhé polovině roku, se začíná odepisovat k prvnímu dni v následujícím roce. Majetek, který se vyřadí v první polovině roku, je považován za vyřazený pro účely odpisů k poslednímu dni v předchozím roce. Všechny odpisy zaúčtované v aktuálním roce musí být stornovány nebo upraveny. Majetek, který se vyřadí ve druhé polovině roku, je považován za vyřazený pro účely odpisů k poslednímu dni v roce vyřazení. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
