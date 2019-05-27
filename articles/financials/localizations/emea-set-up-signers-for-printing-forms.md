---
title: Nastavení podepisujících uživatelů pro tiskové formuláře
description: Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku můžete nastavit podepisující osoby a tituly pro odběratele a dodavatele, kteří tisknou dokumenty, jako jsou faktury a platební příkazy.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 263464
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c3b97de064d7e151c6136d77d993ff4323055bc8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537643"
---
# <a name="set-up-signers-for-print-forms"></a>Nastavení podepisujících uživatelů pro tiskové formuláře

[!include [banner](../includes/banner.md)]

Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku můžete nastavit podepisující osoby a tituly pro odběratele a dodavatele, kteří tisknou dokumenty, jako jsou faktury a platební příkazy.

<a name="set-up-default-values"></a>Nastavení výchozích hodnot
---------------------

K nastavení podepisujících dokumentů, které společnost tiskne, použijte stránku **Úředníci**. Pro firmu i pro zákazníky nebo dodavatele můžete nastavit podepisující osoby a jejich jména, v závislosti na typu dokumentu. Následující tabulka popisuje karty na stránce **Úředníci**.

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
<td>Přidání pozic a souvisejících informací pro podepisující osoby (ředitel a hlavní účetní), který může podepisovat tištěné doklady všech typů.</td>
</tr>
<tr class="even">
<td>Hlavní kniha</td>
<td>Přidejte pozici a související informace o uživatelích, kteří mohou podepsat následující interní finanční dokumenty, které souvisí s cashflow:
<ul>
<li>Pokladní doklady</li>
<li>Sestava záloh</li>
<li>Stránka pokladní knihy</li>
<li>Výpis inventury</li>
<li>Časově rozlišené položky<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Prodejní objednávky</td>
<td>Přidejte pozice a související informace o uživatelích, kteří mohou podepsat následující odchozí primární dokumenty, které souvisí s cashflow:
<ul>
<li>Faktura pro platbu</em></li>
<li>Faktura</li>
<li>Faktura<em></li>
<li>Faktura – dobropis</li>
<li>Dílčí faktura – dobropis</em></li>
<li>Faktura daňové transakce (zákazník)<em></li>
</ul></td>
</tr>
<tr class="even">
<td>Nákupní objednávky</td>
<td>Přidejte pozice a související informace o uživatelích, kteří mohou podepsat následující příchozí primární dokumenty, které souvisí s dodavateli:
<ul>
<li>Faktura</li>
<li>Faktura</em></li>
<li>Faktura – dobropis</li>
<li>Dílčí faktura – dobropis<em></li>
<li>Faktura pro platbu</em></li>
<li>Faktura daňové transakce (dodavatel)<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Řízení skladových položek</td>
<td>Přidejte pozice a informace týkající se u uživatelů, kteří mohou podepsat následující skladové doklady, když je zákazníkovi vydán hmotný majetek nebo když je převzat od dodavatele.
<ul>
<li>Výdejní list pro prodejní objednávku (M-15)</em></li>
<li>Refund. doklad/Příjemka</li>
<li>Výdejní list pro převodní příkaz (M-15)*</li>
</ul></td>
</tr>
</tbody>
</table>

\* Tento typ dokumentu je k dispozici pouze pro právnické osoby, které mají primární adresu v Rusku. Následující tabulka popisuje pole na stránce **Úředníci**.

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
<td>Vyberte název pozice autora podpisu.</td>
</tr>
<tr class="even">
<td>Jméno</td>
<td>Vyberte jméno autora podpisu. Jména v seznamu pocházejí z tabulky Kontakty nebo tabulky Zaměstnanci v závislosti na typu podepisující osoby (tj. v závislosti na tom, zda je zaškrtnuto políčko <strong>Naši</strong>). Není-li jméno podepisující osoby v seznamu, ručně zadejte celé jméno podepisující osoby.</td>
</tr>
<tr class="odd">
<td>Pracovní titul</td>
<td>Vyberte titul autora podpisu. Není-li titul podepisující osoby v seznamu, ručně ho zadejte.</td>
</tr>
<tr class="even">
<td>Kód účtu</td>
<td>Vyberte, zda mohou podepisující podepsat všechny dokumenty pro vybraný typ dokumentu nebo pouze doklady pro určitého odběratele nebo dodavatele.</td>
</tr>
<tr class="odd">
<td>Odkaz na účet</td>
<td>Vyberte účet odběratele nebo dodavatele, vztahující se ke kódu vybraného účtu. Toto pole je k dispozici pouze, pokud vyberete <strong>Záznam</strong> v poli <strong>Kód účtu</strong>.</td>
</tr>
<tr class="even">
<td>Naše</td>
<td>Zaškrtnuté políčko označuje, že jde o interní pozici</td>
</tr>
<tr class="odd">
<td>Spojení se skladem</td>
<td>Vyberte, zda je podepisující je přiřazen všem skladům nebo jen určitému. Existují tyto možnosti:
<ul>
<li><strong>Všechny</strong> – podepisující je přiřazen všem skladům.</li>
<li><strong>Záznam</strong> – podepisující je přiřazen jen určitému skladu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sklad</td>
<td>Vyberte kód skladu, který odpovídá skladu, jemuž je podepisující přiřazen. Toto pole je k dispozici pouze, pokud vyberete <strong>Záznam</strong> v poli <strong>Přidružení ke skladu</strong>.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Nastavení kódu číselného pořadí pro státní úředníky
Můžete přiřadit kód číselné řady pro úředníky v části **Číselné řady** stránky **Právnické osoby**. Vyberte kód číselné řady reference **ID relace úředních osob**.

## <a name="modify-signers-in-primary-documents"></a>Změna podepisujících osob v primárních dokumentech
Funkce Úředníci zobrazuje výchozí předdefinované podepisující z tabulky úředníků. Na stránce **Zaúčtování faktury** na kartě **Úředníci** můžete změnit jméno podepisující osoby a název primárního dokladu pro následující typy dokumentů:

-   Faktura odběratele
-   Faktury dodavatele
-   Převodní příkaz expedice
-   Pokladní doklad

**Poznámka:** Po zaúčtování dokumentu nelze úředníky upravit.



