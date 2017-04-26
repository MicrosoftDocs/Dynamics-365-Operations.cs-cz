---
title: "Podpora převodu kanbanu pro skenery čárového kódu"
description: "Rozvrh převodů kanbanu podporuje vstup ze skeneru skrze widget pro skener čárového kódu, který umožňuje vybrat, zahájit, dokončit a vyprázdnit kanbanovou úlohu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f393efaf011de103fc172af625816eef5915c642
ms.lasthandoff: 03/31/2017


---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>Podpora převodu kanbanu pro skenery čárového kódu

[!include[banner](../includes/banner.md)]


Rozvrh převodů kanbanu podporuje vstup ze skeneru skrze widget pro skener čárového kódu, který umožňuje vybrat, zahájit, dokončit a vyprázdnit kanbanovou úlohu.

<a name="registration-modes"></a>Režimy registrace
------------------

Na pevné záložce **Registrace skeneru** můžete vybrat režim registrace, který řídí akci při skenování čísla kanbanové karty ne ručně skenujete číslo v poli Číslo kanbanové karty.
| Nastavit režim registrace | Popis                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Počátek                 | Registrovat úlohu převodu kanbanu jako probíhající.                                                 |
| Dokončeno              | Registrovat úlohu převodu kanbanu jako dokončenou.                                                   |
| Prázdné                 | Registrovat manipulační jednotku materiálu odkazovanou kanbanovou kartou jako prázdnou.              |
| Vybrat                | Registrovat číslo kanbanové karty a automaticky vybrat odkazovanou úlohu ze seznamu kanbanu. |

 
<a name="registration-mode-select"></a>Režim registrace – Nastavit
------------------------

Při použití čtecího zařízení čárového kódu vyberte úlohy, režim zobrazení změn kanban Rada. V tomto režimu platí následující podmínky:

-   Zobrazí se pouze skenovaná kanbanová úloha.
-   Podrobnosti o vybrané úloze jsou uvedeny na pevné záložce **Podrobnosti**.
-   Pevná záložka **Zprávy** zobrazuje zprávy pouze pro vybranou úlohu.
-   Stav úlohy lze změnit pomocí funkce, která je k dispozici v podokně akcí. Rozvrh převodů kanbanu bude i nadále popisovat pouze jednu úlohu během této doby.
-   Informace v seznamu úloh můžete aktualizovat ručně klepnutím na **aktualizace** (Shift + F5) v podokně akcí. Po aktualizaci údajů jsou znovu zobrazeny úplné výsledky filtru úlohy.

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
<td>Č.</td>
<td>Ano</td>
</tr>
<tr class="even">
<td>Převést</td>
<td><ul>
<li>Neplánováno</li>
<li>Doložené úlohy nejsou dokončeny</li>
</ul></td>
<td>Ano</td>
<td>Č.</td>
<td>Ano</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
</tr>
<tr class="odd">
<td>Převést</td>
<td>Probíhá</td>
<td>Ano</td>
<td>Č.</td>
<td>Ano</td>
<td>Ano</td>
<td>Č.</td>
<td>Č.</td>
</tr>
<tr class="even">
<td>Převést</td>
<td>Dokončeno</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Ano</td>
<td>Č.</td>
</tr>
<tr class="odd">
<td>Převod nebo průběh</td>
<td>Prázdné</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
</tr>
<tr class="even">
<td>Převod nebo průběh</td>
<td>Kanbanová karta nebyla nalezena</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
</tr>
<tr class="odd">
<td>Převod nebo průběh</td>
<td>Kanbanová karta je nalezena, ale není přiřazena ke kanbanu</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
</tr>
<tr class="even">
<td>Proces</td>
<td><ul>
<li>Neplánováno</li>
<li>Připraveno</li>
<li>Probíhá</li>
</ul></td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
</tr>
<tr class="odd">
<td>Proces</td>
<td>Dokončeno</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
<td>Č.</td>
</tr>
</tbody>
</table>






