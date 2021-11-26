---
title: Podpora desky převodů kanbanu pro čtečky čárového kódu
description: Rozvrh převodů kanbanu podporuje vstup ze skeneru skrze widget pro skener čárového kódu, který umožňuje vybrat, zahájit, dokončit a vyprázdnit kanbanovou úlohu.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b18aad4dcdbf8c2d18960ae306556c3ea679d622
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566804"
---
# <a name="kanban-transfer-board-support-for-bar-code-scanners"></a>Podpora desky převodů kanbanu pro čtečky čárového kódu

[!include [banner](../includes/banner.md)]

Rozvrh převodů kanbanu podporuje vstup ze skeneru skrze widget pro skener čárového kódu, který umožňuje vybrat, zahájit, dokončit a vyprázdnit kanbanovou úlohu.

## <a name="registration-modes"></a>Režimy registrace

Na pevné záložce **Registrace skeneru** můžete vybrat režim registrace, který řídí akci při skenování čísla kanbanové karty ne ručně skenujete číslo v poli Číslo kanbanové karty.

| Nastavit režim registrace | Popis                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Počátek                 | Registrovat úlohu převodu kanbanu jako probíhající.                                                 |
| Dokončeno              | Registrovat úlohu převodu kanbanu jako dokončenou.                                                   |
| Prázdné                 | Registrovat manipulační jednotku materiálu odkazovanou kanbanovou kartou jako prázdnou.              |
| Vybrat                | Registrovat číslo kanbanové karty a automaticky vybrat odkazovanou úlohu ze seznamu kanbanu. |

 
## <a name="registration-mode-select"></a>Režim registrace – Nastavit

Pokud používáte čtečku čárových kódů pro výběr úlohy, režim zobrazení kanbanové desky se změní. V tomto režimu platí následující podmínky:

-   Zobrazí se pouze skenovaná kanbanová úloha.
-   Podrobnosti o vybrané úloze jsou uvedeny na pevné záložce **Podrobnosti**.
-   Pevná záložka **Zprávy** zobrazuje zprávy pouze pro vybranou úlohu.
-   Stav úlohy lze změnit pomocí funkce, která je k dispozici v podokně akcí. Rozvrh převodů kanbanu bude i nadále popisovat pouze jednu úlohu během této doby.
-   Informace v seznamu úloh lze aktualizovat ručně klepnutím na **Aktualizovat** (Shift + F5) v podokně akcí. Po aktualizaci údajů jsou znovu zobrazeny úplné výsledky filtru úlohy.

## <a name="job-status-and-possible-actions"></a>Stav úlohy a možné akce
Stav vybrané úlohy a stav doložené úlohy pro kanbany události určuje, zda může úlohu dále zpracovat. V následující tabulce jsou uvedeny informace o těchto stavech a úkolech:
-   Stavy, které jsou k dispozici pro úlohy nebo manipulační jednotky, na které odkazují úlohy.
-   Jednotlivé úkoly, které mohou provádět úlohu.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ práce</th>
<th>Stav úlohy nebo stav manipulační jednotky</th>
<th>Aktualizovat výdejku</th>
<th>Počátek</th>
<th>Aktualizovat registraci</th>
<th>Dokončeno</th>
<th>Prázdné</th>
<th>Vytvořit kanbanové události</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Převést</td>
<td><ul>
<li>Neplánováno</li>
<li>Žádné doložené nebo doložené úlohy jsou dokončeny</li>
</ul></td>
<td>Ano</td>
<td>Ano</td>
<td>Ano</td>
<td>Ano</td>
<td>Ne</td>
<td>Ano</td>
</tr>
<tr class="even">
<td>Převést</td>
<td><ul>
<li>Neplánováno</li>
<li>Doložené úlohy nejsou dokončeny</li>
</ul></td>
<td>Ano</td>
<td>Ne</td>
<td>Ano</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Převést</td>
<td>Probíhá</td>
<td>Ano</td>
<td>Ne</td>
<td>Ano</td>
<td>Ano</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="even">
<td>Převést</td>
<td>Dokončeno</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ano</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Převod nebo průběh</td>
<td>Prázdné</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="even">
<td>Převod nebo průběh</td>
<td>Kanbanová karta nebyla nalezena</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Převod nebo průběh</td>
<td>Kanbanová karta je nalezena, ale není přiřazena ke kanbanu</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="even">
<td>Proces</td>
<td><ul>
<li>Neplánováno</li>
<li>Připraveno</li>
<li>Probíhá</li>
</ul></td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Proces</td>
<td>Dokončeno</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]