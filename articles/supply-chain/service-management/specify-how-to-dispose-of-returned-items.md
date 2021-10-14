---
title: Určení způsobu nakládání s vrácenými položkami
description: Určení způsobu nakládání s vrácenými položkami
author: kamaybac
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e609c1c285b34a5416a2058809b2fc4fafb73fca
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571322"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Určení způsobu nakládání s vrácenými položkami

[!include [banner](../includes/banner.md)]

Při zpracování vratky je třeba zadáním kódu důvodu vrácení identifikovat příčinu vrácení produktu. Také je nutné zadáním dispozičního kódu a dispoziční akce určit, jak má být naloženo s vráceným produktem.

Dispoziční kód lze použít při vytvoření vratky, registraci doručené položky nebo aktualizaci dodacího listu pro položku a ukončení karanténního příkazu.

Můžete definovat libovolné dispoziční kódy, které si vyžaduje podpora obchodních procesů. V následující tabulce je uvedena sada kódů, které jsou obvykle přidruženy k vyřazení vrácené položky.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Typ dispozice</p></th>
<th><p>Běžný kód</p></th>
<th><p>popis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Vyřazení</p></td>
<td><p>SC</p></td>
<td><p>Likvidace nebo zničení</p></td>
</tr>
<tr class="even">
<td><p>Vyřazení</p></td>
<td><p>DC</p></td>
<td><p>Dar charitě</p></td>
</tr>
<tr class="odd">
<td><p>Vyřazení</p></td>
<td><p>TD</p></td>
<td><p>Vyřazení třetí strany</p></td>
</tr>
<tr class="even">
<td><p>Vyřazení</p></td>
<td><p>SL</p></td>
<td><p>Konečný zůstatek</p></td>
</tr>
<tr class="odd">
<td><p>Vyřazení</p></td>
<td><p>TS</p></td>
<td><p>Prodej třetí strany (sekundární trhy)</p></td>
</tr>
<tr class="even">
<td><p>Oprava nebo úprava</p></td>
<td><p>RW</p></td>
<td><p>Přepracování</p></td>
</tr>
<tr class="odd">
<td><p>Oprava nebo úprava</p></td>
<td><p>RF</p></td>
<td><p>Přepracování</p></td>
</tr>
<tr class="even">
<td><p>Oprava nebo úprava</p></td>
<td><p>MD</p></td>
<td><p>Změna</p></td>
</tr>
<tr class="odd">
<td><p>Oprava nebo úprava</p></td>
<td><p>RP</p></td>
<td><p>Oprava</p></td>
</tr>
<tr class="even">
<td><p>Oprava nebo úprava</p></td>
<td><p>RV</p></td>
<td><p>Návrat dodavateli</p></td>
</tr>
<tr class="odd">
<td><p>Ostatní</p></td>
<td><p>AI</p></td>
<td><p>Použít jako</p></td>
</tr>
<tr class="even">
<td><p>Jiná</p></td>
<td><p>RS</p></td>
<td><p>Opětovný prodej</p></td>
</tr>
<tr class="odd">
<td><p>Jiná</p></td>
<td><p>EX</p></td>
<td><p>Směna</p></td>
</tr>
<tr class="even">
<td><p>Jiná</p></td>
<td><p>MS</p></td>
<td><p>Různé</p></td>
</tr>
</tbody>
</table>


Pro každý kód dispozice, který definujete, je nutné vybrat dispoziční akci. Dispoziční akce určují fyzické a finanční důsledky dispozičních kódů. Dispoziční akce například určuje fyzické zpracování vráceného zboží, finanční dopad vráceného zboží a informaci o tom, zda má být odběrateli zasláno náhradní zboží. Můžete definovat neomezený počet dispozičních kódů podle vašich obchodních potřeb, ale existuje pouze šest předdefinovaných dispozičních akcí, které lze vybírat. Následující tabulka obsahuje dispoziční akce a jejich definice.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Dispoziční akce</p></th>
<th><p>popis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Kreditní</strong></p></td>
<td><p>Vrácení zboží do skladové zásoby a vrácení peněz odběrateli.</p></td>
</tr>
<tr class="even">
<td><p><strong>Pouze Dal</strong></p></td>
<td><p>Vrácení peněz odběrateli bez vyžadování či očekávání návratu zboží.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Odpad</strong></p></td>
<td><p>Likvidace zboží a vrácení peněz odběrateli.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nahradit a připsat na stranu Dal</strong></p></td>
<td><p>Vrácení zboží do skladové zásoby, vytvoření náhradní objednávky a vrácení peněz odběrateli.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nahradit a vyřadit</strong></p></td>
<td><p>Likvidace zboží, vytvoření náhradní objednávky a vrácení peněz odběrateli.</p></td>
</tr>
<tr class="even">
<td><p><strong>Vrátit odběrateli</strong></p></td>
<td><p>Odmítnutí vráceného zboží a jeho vrácení zákazníkovi.</p></td>
</tr>
</tbody>
</table>

## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Vyberte dispoziční kód pro karanténní příkaz.

1. Přejděte na **Řízení zásob** \> **Periodicky** \> **Správa kvality** \> **Karanténní příkazy**.
1. Pro stávající karanténní příkaz vyberte akci v poli **Dispoziční kód** na kartě **Přehled**.

## <a name="see-also"></a>Viz také

[Karanténní příkaz (formulář)](/dynamicsax-2012//quarantine-order-form)

[Dispoziční kódy (formulář)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
