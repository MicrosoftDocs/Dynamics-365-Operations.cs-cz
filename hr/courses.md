---
title: "Nastavení školení"
description: "Správci lidských zdrojů a vedoucí pracovníci mohou funkce kurzů používat ke správě informací o školeních nabízených pracovníkům."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: aa97950a22572fb4c934687b550c13dcc8acce0d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-training-courses"></a>Nastavení školení

[!include[banner](includes/banner.md)]


Správci lidských zdrojů a vedoucí pracovníci mohou funkce kurzů používat ke správě informací o školeních nabízených pracovníkům.

 <a name="set-up-prerequisites"></a> Nastavení předpokladů
---------------------

Před vytvořením kurzů je nutné znát a nastavit následující informace.
-   **Typy kurzů**

Tyto informace jsou volitelné informace, které lze určit pro kurzy. Pokud víte, že budete zadávat tyto údaje pro kurzy, nastavte je před vytvořením záznamů kurzu.
-   **Skupiny učeben**
-   **Skupiny kurzů**
-   **Místo konání kurzu**
-   **Učebny**
-   **Instruktoři**

## <a name="course-types"></a>Typy kurzů
Typy kurzů slouží k rozdělení kurzů podle struktury nebo obsahu kurzu. Na stránce **Typy kurzů** můžete vytvořit typy kurzů. Musíte vybrat typ kurzu, když vytváříte záznam kurzu.

## <a name="course-setup-type"></a>Typ nastavení kurzu
V následující tabulce jsou uvedeny tři typy nastavení kurzů. Typy nastavení určují strukturu kurzu.

<table>
<thead>
<tr class="header">
<th>Typ nastavení</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standardní</strong></td>
<td>Vyberte tento typ pro kurzy, které nemají denní agendu. Toto je výchozí typ nastavení, když vytváříte nový kurz.</td>
</tr>
<tr class="even">
<td><strong>Pořad jednání</strong></td>
<td>Tento typ vyberte pro naplánování podrobností pro jednotlivé dny vícedenního kurzu.</td>
</tr>
<tr class="odd">
<td><strong>Agenda + relace</strong></td>
<td>Vyberte tento typ pro složitější kurzy. Agendu kurzu lze například rozdělit do běhů a relací.
<ul>
<li><strong>Běhy </strong> – Běhy jsou konkrétní témata kurzu.</li>
<li><strong>Relace</strong> – Relace rozdělují běhy a mohou identifikovat specifické procesy nebo postupy, které se vztahují k jednotlivým běhům.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Úkoly kurzu
U každého kurzu můžete provést následující úlohy.
-   Registrovat účastníky
-   Nastavit uzávěrku registrace
-   Definovat minimální a maximální počet účastníků
-   Přiřadit místo konání kurzu a učebnu
-   Doporučit hotely účastníkům kurzu
-   Vytvořit popis kurzu, který je poté možné zveřejnit na portálu Samoobsluha pro zaměstnance

  >**Poznámka:** kurzu můžete odstranit pouze v případě, že jej nikdo zaregistroval. 
    
## <a name="course-statuses"></a>Stavy kurzu
V následující tabulce jsou uvedeny možné stavy kurzu a akce, které lze provádět, je-li kurz nachází ve specifickém stavu.

<table>
<thead>
<tr class="header">
<th>Stav</th>
<th>Akce</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Vytvořeno</strong></td>
<td><ul>
<li>Zadávání a úprava informací o kurzu.</li>
<li>Změňte stav kurzu na <strong>Otevřen</strong>, aby se pracovníci mohli do kurzu registrovat.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Otevřít</strong></td>
<td><ul>
<li>Zaregistrujte účastníky na kurz.</li>
<li>Odeberte účastníky z kurzu.</li>
<li>Potvrďte účastníky kurzu.</li>
<li>Změňte stav kurzu na <strong>Uzavřeno</strong> nebo <strong>Zrušeno</strong>.</li>
<li>Naplánujte dotazníky pro účastníky, jejichž stav je <strong>Potvrzeno</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Zavřeno</strong></td>
<td>Kurz můžete znovu otevřít.</td>
</tr>
<tr class="even">
<td><strong>Zrušeno</strong></td>
<td>Kurz můžete znovu otevřít.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Účastníci kurzu
Účastníky kurzu jsou pracovníci, uchazeči nebo kontaktní osoby, kteří se účastní školicího kurzu nebo události. Účastníky můžete registrovat pouze pro otevřené kurzy. Maximální a minimální počty účastníků, které lze do kurzu registrovat, jsou uvedeny na pevné záložce **Obecné** na stránce **Kurzy**.

<a name="workflow"></a>Workflow
--------

Zaměstnanci, kteří registrovat do kurzu až **zaměstnance samoobslužném** stránka může mít jejich registraci směrovány pomocí pracovního postupu pro schválení.  Pracovní postup lze přiřadit ke kurzu na **Obecné** s náhledem na **kurzy** stránky.






