---
title: Projekty hromadného zařazení
description: Projekty hromadného zařazení umožňují odborníkům z oblasti lidských zdrojů vytvářet více pozic a efektivně zařazovat zaměstnance na tyto pozice.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 209449fe8541f0f6a474b0125cbe6b3c0287b6e9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008324"
---
# <a name="mass-hire-projects"></a>Projekty hromadného zařazení



Projekty hromadného zařazení umožňují odborníkům z oblasti lidských zdrojů vytvářet více pozic a efektivně zařazovat zaměstnance na tyto pozice.

## <a name="overview"></a>Přehled

Projekty hromadného zařazení používejte pokud zařazujete několik zaměstnanců zároveň, například při zařazování ke splnění sezónní poptávky. Vytvoření projektu hromadného zařazování zaměstnanců je užitečné, protože lze vytvořit současně záznamy pozice, záznamy pracovníků a přiřazení pracovníků k pozicím. Při vytváření pozic pro projekt hromadného zařazování zaměstnanců můžete zadat následující informace:

- Počet pozic, které chcete vytvořit
- Typ pracovníka, který budete nabírat na pozice
- Oddělení a úloha související s danými pozicemi
- Odpovídající hodnota pozice na plný úvazek

## <a name="example"></a>Příklad

V létě obvykle probíhá nábor na 15-20 studentů na částečný úvazek pro vyplnění stáží ve vaší společnosti. Tento rok chcete najmout pět účetních, pět osob pro zpracování objednávek a pět pokladníků. Namísto vytváření jednotlivých pozic a pracovních záznamů samostatně vytvoříte jeden projekt hromadného zařazení s názvem "LetníVýpomoc". Počáteční a koncové datum projektu koreluje s počátečním a koncovým datem trvání pozice pro pozice, které jste vytvořili pro projekt hromadného náboru.

Na stránce **Projekty hromadného zařazení** vyberte "LetníVýpomoc" a klepněte na tlačítko **Otevřít projekt**. V části Otevřít projekt masového zařazení klikněte na možnost **Vytváření pozic** a zadejte informace o pozici účetního. Můžete určit, že pět účetních pozic by mělo být vytvořeno s využitím vždy stejných informací, a klepněte na tlačítko OK. Tento postup opakujte pro osoby vyřizující objednávky a pozice pokladníka.

Po výběru studentů, které chcete zařadit kvůli stáži zadejte informace o každém studentovi do pole **Podrobnosti pozice** u pozice, pro kterou je zařazujete. Po zadání všech podrobností o pozici vyberte pozici na stránce Projekty hromadného zařazení a klepněte na **Zařazení**. Záznam pozice bude vytvořen pro jednotlivé pozice, a bude vytvořen záznam pracovníka a přiřazen ke správné pozici pro každou osobu, kterou zařazujete.

## <a name="mass-hire-project-statuses"></a>Stavy projektu hromadného zařazení

Projekt masového zařazení může mít jeden z následujících stavů.

- Vytvořeno
- Otevřené
- Uzavřené

Na stránce **Projekt hromadného zařazení** klepněte na **Otevřít projekt** nebo **Zavřít projekt** a změňte tak stav projektu hromadného zařazování zaměstnanců. Následující tabulka uvádí, co lze s projektem provádět podle toho, v jakém stavu se nachází.

<table>
<thead>
<tr>
<th>Stav</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vytvořeno</td>
<td>Informace lze vytvořit a upravovat, avšak v projektu nelze vytvořit pozice. Jedná se o výchozí stav pro nové projekty.</td>
</tr>
<tr>
<td>Otevřené</td>
<td>Můžete upravit podrobnosti projektu, vytvořit pozice pro projekt hromadného zařazení a najmout osoby pro pozici. Jedná se o stav aktivních projektů.</td>
</tr>
<tr>
<td>Uzavřené</td>
<td>Nelze přidat pozice do projektu. Otevřete projekt hromadného zařazování, kde můžete přiřadit další pozice. Jedná se o stav dokončených projektů.
<blockquote>[!NOTE] Před uzavřením projektu hromadného zařazování je nutné, aby všechny pozice v projektu měly stav Vytvořeno nebo Uzavřeno.</blockquote>
</td>
</tr>
</tbody>
</table>