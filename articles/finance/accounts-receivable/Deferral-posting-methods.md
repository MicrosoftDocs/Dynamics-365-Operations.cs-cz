---
title: Metody odloženého zaúčtování
description: Tento článek popisuje rozdíly mezi metodami odloženého zaúčtování pro odložení výnosů a nákladů ve Fakturaci předplatného.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019091"
---
# <a name="deferral-posting-methods"></a>Metody odloženého zaúčtování

Tento článek popisuje rozdíly mezi metodami odloženého zaúčtování pro odložení výnosů a nákladů ve Fakturaci předplatného.

Na stránce **Parametry časového rozlišení výnosů a výdajů** jsou možnosti pro metody odloženého účtování **Rozvaha** a **Zisk a ztráta**. Příklad v tomto článku vám pomůže vysvětlit rozdíly mezi těmito dvěma metodami a důvody, proč byste mohli použít jednu nebo druhou metodu.

Metoda **Rozvaha** používá pouze dva účty. Proto je zapotřebí méně nastavení. Metoda **Zisk a ztráta** má dva další účty, **Počáteční uznání** a **Ofsetové uznání** pro výnosy, slevy a náklady v závislosti na typu transakce. Tyto účty jsou zřízeny na stránce **Výchozí hodnoty odkladu** (**Fakturace předplatného \> Časové rozlišení výnosů a nákladů \> Nastavení**). Přestože je příklad zaměřen na výnosy příštích období, stejný koncept lze použít pro odložené slevy a náklady příštích období.

## <a name="example"></a>Příklad

Prodejní faktura 1 má celkem 3000 USD a má odložené příjmy. Následující tabulky ukazují distribuce při zaúčtování této prodejní faktury.

**Metoda Rozvaha**

| Typ | Účet | Debet | Kredit|
|---|---|---|---|
| Debet | Pohledávky | 3,000.00 | |
| Kredit | Odložené výnosy | | 3,000.00 |

**Metoda Zisk a ztráta**

| Typ | Účet | Debet | Kredit |
|---|---|---|---|
| Debet | Pohledávky | 3,000.00 | |
| Debet | Ofsetové uznání výnosů | 3,000.00 | |
| Kredit | Odložené výnosy | | 3,000.00 |
| Kredit | Počáteční uznání výnosů | | 3,000.00 |

Prodejní faktura 2 má celkem 2000 USD a nemá odložené příjmy.

| Typ | Účet | Částka |
|---|---|---|
| Debet | Pohledávky | 3,000.00 |
| Kredit | Výnosy | 3,000.00 |

**Součty metody Rozvaha pro prodejní fakturu 1 a 2 dohromady**

| Účet | Debet | Kredit |
|---|---|---|
| Pohledávky | 5,000.00 | |
| Výnosy | | 2,000.00 |
| Odložené výnosy | | 3,000.00 |

Když se použije metoda **Rozvaha**, není tak snadné vidět hrubý příjem za období. Některé výnosy jsou zaúčtovány na účet **Odložené výnosy**. Mějte na paměti, že vzhledem k tomu, že výnosy jsou vykazovány v každém období, existuje několik debetů a kreditů na účtu **Odložené výnosy**. Hrubý výnos za dané období bude smíchán s kredity a debety uznání výnosů.

**Součty metody Zisk a ztráta pro prodejní fakturu 1 a 2 dohromady**

| Účet | Debet | Kredit |
|---|---|---|
| Pohledávky | 5,000.00 | |
| Výnosy | | 5,000.00 |
| Protiúčet výnosů | 3,000.00 | |
| Odložené výnosy | | 3,000.00 |

Veškeré výnosy jdou na účet zisku a ztrát **Výnosů**. Poté se výnosy příštích období přesunou z výkazu zisku a ztrát do rozvahy. Můžete snadno vidět hrubý příjem, protože vše je zaúčtováno na účtu **Výnosy**. Část těchto hrubých příjmů je však odložena. Proto se přesune ná účet **Odložené výnosy** a později uzná.

V metodě **Zisk a ztráta** se můžete podívat na účet **Výnosy** a **Protiúčet výosů** a zobrazit hrubé výnosy 5000 USD a čistý příjem (bez odložených výnosů) 2000 USD. Přestože může metoda **Zisk a ztráta** usnadnit hlášení, existuje více účtů k nastavení.
