---
title: "Nastavit podepisující osoby pro tisk formuláře"
description: "Pro právnické osoby do České republiky, Estonska, Maďarska, Litvy, Lotyšska, Polska a Ruska nastavením podepisující osoby a tituly pro odběratele a dodavatele, které vytisknout dokumenty jako jsou faktury a platební příkazy."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 263464
ms.assetid: 7213914a-ecb6-4711-99fe-4e11867aaf4d
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 45d2facde1e5502f4a5863863554a486916c26cd
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-signers-for-print-forms"></a>Nastavit podepisující osoby pro tisk formuláře

[!include[banner](../includes/banner.md)]


Pro právnické osoby do České republiky, Estonska, Maďarska, Litvy, Lotyšska, Polska a Ruska nastavením podepisující osoby a tituly pro odběratele a dodavatele, které vytisknout dokumenty jako jsou faktury a platební příkazy.

<a name="set-up-default-values"></a>Nastavení výchozích hodnot
---------------------

Zřídit podepsaných dokumentů, které společnost vytiskne, použít **úředníci** stránky. Pro firmu i pro zákazníky nebo dodavatele, v závislosti na typu dokumentu můžete nastavit podepisující osoby a jejich názvy. Následující tabulka popisuje karty **úředníci** stránky.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Karta</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Obecné</td>
<td>Přidání polohy a související informace pro podepisující osoby (ředitel a hlavní účetní) který lze podepsat dokumenty všech typů.</td>
</tr>
<tr class="even">
<td>Hlavní kniha</td>
<td>Přidáte pozici a související informace o uživatelů, kteří mohou podepsat následující interní finanční dokumenty, které souvisí s cashflow:
<ul>
<li>Pokladní doklady</li>
<li>Sestava záloh</li>
<li>Stránka pokladní knihy</li>
<li>Výpis inventury</li>
<li>* Časově rozlišených položek</li>
</ul></td>
</tr>
<tr class="odd">
<td>Prodejní objednávky</td>
<td>Přidáte umístění a informace týkající se u uživatelů, kteří mohou podepsat následující odchozí primární dokumenty, které se vztahují k zákazníkům:
<ul>
<li>Faktura pro platbu *</li>
<li>Faktura</li>
<li>Dílčí faktura *</li>
<li>Faktura – dobropis</li>
<li>Faktura – Dal – Poznámka: *</li>
<li>Faktura daňové transakce (klient) *</li>
</ul></td>
</tr>
<tr class="even">
<td>Nákupní objednávky</td>
<td>Přidáte umístění a informace týkající se u uživatelů, kteří mohou podepsat následující příchozí primární dokumenty, které souvisejí s dodavateli:
<ul>
<li>Faktura</li>
<li>Dílčí faktura *</li>
<li>Faktura – dobropis</li>
<li>Faktura – Dal – Poznámka: *</li>
<li>Faktura pro platbu *</li>
<li>Faktura daňové transakce (dodavatel) *</li>
</ul></td>
</tr>
<tr class="odd">
<td>Řízení skladových položek</td>
<td>Přidáte umístění a informace týkající se u uživatelů, kteří mohou podepsat následující doklady skladu jsou vydané odběrateli nebo přijaté od dodavatele hmotných aktiv:
<ul>
<li>Výdejní list pro prodejní objednávky (M-15) *</li>
<li>RMB. list/potvrzení objednávky</li>
<li>Výdejní list pro převodní příkaz (M-15) *</li>
</ul></td>
</tr>
</tbody>
</table>

\*Tento typ dokumentu je k dispozici pouze pro právnické osoby, které mají svou primární adresu v Rusku. Následující tabulka popisuje pole na **úředníci** stránky.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pozice</td>
<td>Vyberte zaúčtovat podepisující osoby.</td>
</tr>
<tr class="even">
<td>Jméno</td>
<td>Vyberte název autora podpisu. Názvy v seznamu pocházet z tabulky Kontakty nebo tabulce Zaměstnanci v závislosti na typu podepisující osoba (, v závislosti na tom, zda <strong>našich</strong> je zaškrtnuto políčko). Není-li jméno podepisující osoby v seznamu, ručně zadejte celé jméno podepisující osoby.</td>
</tr>
<tr class="odd">
<td>Funkce</td>
<td>Vyberte úlohu podepisující osoby. Není-li podepisující osoby v seznamu, zadejte ručně podepisující osoby.</td>
</tr>
<tr class="even">
<td>Kód účtu</td>
<td>Vyberte, zda podepisující mohou podepsat všechny dokumenty pro vybraný typ dokumentu nebo pouze doklady pro určitého odběratele nebo dodavatele.</td>
</tr>
<tr class="odd">
<td>Odkaz na účet</td>
<td>Vyberte účet odběratele nebo dodavatele, vztahující se ke kódu vybraného účtu. Toto pole je dostupné pouze pokud vyberete <strong>záznam</strong> v <strong>kód účtu</strong> pole.</td>
</tr>
<tr class="even">
<td>Naše</td>
<td>Zaškrtnuté políčko označuje, že je interní pozice.</td>
</tr>
<tr class="odd">
<td>Spojení se skladem</td>
<td>Vyberte, zda podepisující je přiřazena všechny sklady nebo pouze určitý sklad. Existují tyto možnosti:
<ul>
<li><strong>Všechny</strong> – podepisující je přiřazena všechny sklady.</li>
<li><strong>Záznam</strong> – podepisující je přiřazen určitý sklad.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sklad</td>
<td>Vyberte sklad, který je přiřazen podepisující odpovídající kód skladu. Toto pole je dostupné pouze pokud vyberete <strong>záznam</strong> v <strong>spojení se skladem</strong> pole.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Nastavit kód číselné řady pro úředníky
Můžete přiřadit kód číselné řady pro úředníky **číselné řady** oddílu **právnické osoby** stránky. Vyberte kód číselné řady pro **ID relace úředních osob** odkaz.

## <a name="modify-signers-in-primary-documents"></a>Změna podepisující osoby v primárních dokumentů
Úředníci funkce zobrazuje výchozí předdefinované podepsaných z tabulky úředníků. Na **zaúčtování faktury** na stránky **úředníci** kartu, můžete změnit jméno podepisující osoby a název primárního dokladu pro následující typy dokumentů:

-   Faktura odběratele
-   Faktury dodavatele
-   Převodní příkaz expedice
-   Pokladní doklad

**Poznámka:** po zaúčtování dokumentu nelze upravit, úředníci.




