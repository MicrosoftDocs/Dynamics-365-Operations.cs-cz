---
title: "Výchozí protiúčty pro deníky pro faktury dodavatele a pro deníky pro schvalování faktur"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 40631521def2905ae4d0be053c9267e6487c8029
ms.lasthandoff: 03/31/2017


---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Výchozí protiúčty pro deníky pro faktury dodavatele a pro deníky pro schvalování faktur

[!include[banner](../includes/banner.md)]




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
<td><strong>Záhlaví deníku</strong> – Nastavte výchozí protiúčet pro deník, který má být použit jako výchozí položka na stránkách pro doklad deníku. Poznámka: není možné zadat výchozí protiúčty pro záhlaví deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</td>
<td>Položky deníku v deníku</td>
<td>Výchozí protiúčet pro deník se používá jako výchozí položka na stránkách pro doklad deníku.</td>
<td>Tato možnost slouží k urychlení zadávání dat, pokud většina položek v deníku má stejný protiúčet.</td>
</tr>
</tbody>
</table>





