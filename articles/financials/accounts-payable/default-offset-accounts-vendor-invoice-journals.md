---
title: Výchozí protiúčty pro deníky faktur dodavatele a deníky schvalování faktur
description: Toto téma vám pomůže s rozhodnutím, kam chcete přiřadit výchozí účty pro deníky faktur.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cf772a0f0f9f99519322be1f37f961dc0ab2500
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509099"
---
# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Výchozí protiúčty pro deníky faktur dodavatele a deníky schvalování faktur

[!include [banner](../includes/banner.md)]

Výchozí protiúčty se používají v následující stránkách deníku faktury dodavatele:

-   Deník faktur
-   Deník schválených faktur

Podle následující tabulky se rozhodněte, kam chcete přiřadit výchozí účty pro deníky faktur.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Zde nastavte výchozí účty</th>
<th>Kde jsou zadávány výchozí účty</th>
<th>Jaký má tato možnost vliv na zpracování</th>
<th>Kdy použít tuto možnost</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Skupina dodavatelů</strong> – nastavte kódů na výchozí protiúčty pro skupiny dodavatelů na stránce <strong>Výchozí nastavení účtu</strong>, kterou lze otevřít ze stránky <strong>Skupiny dodavatelů</strong>.</td>
<td><ul>
<li>Účet dodavatele</li>
<li>Položky deníku pro účty dodavatele ve skupině dodavatelů, nejsou-li účty uvedeny pro účty dodavatelů</li>
</ul></td>
<td>Výchozí protiúčty pro skupiny dodavatelů se zobrazí jako na výchozí protiúčty pro dodavatele na stránce <strong>Výchozí nastavení účtu</strong>. Můžete otevřít tuto stránku na stránce se seznamem <strong>Všichni dodavatelé</strong>.</td>
<td>Tuto možnost použijte, pokud obvykle platíte za stejné typy věcí ze stejné skupiny dodavatelů během času.</td>
</tr>
<tr class="even">
<td><strong>Účet dodavatele</strong> – nastavte kódů na výchozí účty pro účty dodavatelů na stránce <strong>Výchozí nastavení účtu</strong>, kterou lze otevřít ze stránky <strong>Dodavatelé</strong>.</td>
<td>Položky deníku pro účet dodavatele</td>
<td>Výchozí protiúčty pro účty dodavatele jsou zobrazeny jako výchozí protiúčty pro položky deníku pro účet dodavatele.</td>
<td>Tuto možnost použijte, pokud obvykle platíte za stejné typy věcí od stejných dodavatelů během času.</td>
</tr>
<tr class="odd">
<td><strong>Názvy deníků</strong> – nastavte výchozí protiúčty pro deníky na stránce <strong>Názvy deníků</strong>. Vyberte možnost <strong>Pevný protiúčet</strong>. Poznámka: není možné zadat výchozí protiúčty pro názvy deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</td>
<td><ul>
<li>Záhlaví deínku používajícího název deníku</li>
<li>Položky deníku v denících, které používají název deníku</li>
</ul></td>
<td>Pokud je vybrána možnost <strong>Pevný protiúčet</strong> na stránce <strong>Názvy deníků</strong>, bude protiúčet pro název deníku mít přednost před výchozím protiúčtem pro dodavatele nebo skupinu dodavatelů.</td>
<td>Tato možnost slouží k nastavení deníků pro specifické výdaje a náklady, které jsou účtovány na konkrétní účty, bez ohledu na to, kdo je dodavatelem nebo které skupiny dodavatelů je součástí.</td>
</tr>
<tr class="even">
<td><strong>Názvy deníků</strong> – nastavte výchozí protiúčty pro deníky na stránce <strong>Názvy deníků</strong>. Zrušte výběr možnosti <strong>Pevný protiúčet</strong>. Poznámka: není možné zadat výchozí protiúčty pro názvy deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</td>
<td><ul>
<li>Záhlaví deníku</li>
<li>Položky deníku v denících, které používají název deníku</li>
</ul></td>
<td>Tyto výchozí položky se používají na stránkách pro záhlaví deníku a protiúčet na stránce pro záhlaví deníku se používá jako výchozí položka na stránkách pro doklad deníku. Výchozí účty na stránce <strong>Názvy deníku </strong>se používají pouze v případě, že nejsou nastaveny výchozí účty pro účet dodavatele.</td>
<td>Tato možnost slouží k vytvoření výchozích účtů, které použijete, pokud protiúčet dodavatele není přiřazen.</td>
</tr>
<tr class="odd">
<td><strong>Záhlaví deníku</strong> – Nastavte výchozí protiúčet pro deník, který má být použit jako výchozí položka na stránkách pro doklad deníku. Mějte na paměti, že není možné zadat výchozí protiúčty pro záhlaví deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</td>
<td>Položky deníku v deníku</td>
<td>Výchozí protiúčet pro deník se používá jako výchozí položka na stránkách pro doklad deníku.</td>
<td>Tato možnost slouží k urychlení zadávání dat, pokud většina položek v deníku má stejný protiúčet.</td>
</tr>
</tbody>
</table>





