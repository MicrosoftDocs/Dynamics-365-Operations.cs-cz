---
title: Rozúčtováních a záznamy v dílčí hlavní knize pro volné faktury
description: Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výnosy, daně a náklady zaúčtovány na volných fakturách. Každá částka, která musí být zaúčtována, když je volná faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d1546e8537110daec5d6655f68d3328a58ca1cb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571181"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a>Rozúčtováních a záznamy v dílčí hlavní knize pro volné faktury

[!include [banner](../includes/banner.md)]

Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výnosy, daně a náklady zaúčtovány na volných fakturách. Každá částka, která musí být zaúčtována, když je volná faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.

<a name="accounting-distributions"></a>Rozúčtování
------------------------

Na stránce Volné faktury můžete použít následující tlačítka k zobrazení a případné změně rozúčtování pro každou částku na volné faktuře.

-   **Distribuovat částky**—Zobrazení a změna rozúčtování pro každý řádek a také všechny podřízené řádky, jako jsou například daně a poplatky. Lze také zobrazit a změnit rozúčtování pro podřízený řádek přímo na stránce Transakcí DPH nebo na stránce Transakce nákladů.
    -   Změna částek v záhlaví volných faktur, například náklady nebo měnové zaokrouhlení částky.
    -   Změna částek na řádcích volné faktury.
-   **Zobrazit distribuce** – Zobrazení rozúčtování pro všechny řádky v dokumentu. V tomto zobrazení nelze měnit rozúčtování.
    -   Zobrazení záhlaví a částek řádku.

## <a name="distributing-amounts"></a>Distribuce částek
Při vkládání volné faktury budou jednotlivé částky rozděleny následujícím způsobem.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ peněžní částky</th>
<th>Odkud se zobrazuje hlavní účet</th>
<th>Pořadí priority, které určuje, jaká výchozí finanční dimenze je zobrazena</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Řádek volné faktury</td>
<td>Hlavní kniha na řádku volné faktury.</td>
<td><ol>
<li>Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</li>
<li>Pokud hlavní účet není účtem přidělení, použijte výchozí šablonu finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="even">
<td>Řádek volné faktury pro kombinaci čísla dlouhodobého majetku a oceňovacího modelu
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Poznámka </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hlavní účet na řádku volné faktury bude účet vyřazení dlouhodobého majetku.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Hlavní kniha na řádku volné faktury.</td>
<td><ol>
<li>Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Částka slevy na volné faktuře</td>
<td>Pole Hlavní účet pro slevy odběratele na stránce strany Platební slevy.</td>
<td><ol>
<li>Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</li>
<li>Pokud hlavní účet není účtem přidělení, použijte výchozí šablonu finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="even">
<td>Částka DPH na volné faktuře</td>
<td>Pole Splatná DPH na stránce Skupiny zaúčtování hlavní knihy.</td>
<td><ol>
<li>Použijte finanční dimenze, které jsou definovány v částce řádku na volné faktuře nebo distribucí pro částky řádku nákladů.</li>
<li>Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Částka na řádku nákladů na volné faktuře</td>
<td>Pole Účet Dal na stránce Kódy nákladů.</td>
<td><ol>
<li>Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</li>
<li>Pokud hlavní účet není účtem přidělení, použijte výchozí šablonu finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Distribuce daní
Dokud daně nejsou vypočítány, nelze pro ně vytvořit rozúčtování. Při výpočtu DPH je třeba ve formuláři Volná faktura provést jeden z následujících úkolů:
-   Zobrazit DPH.
-   Zobrazit celkový součet faktury.
-   Zobrazit cashflow.
-   Zobrazit rozúčtování pro všechny volné faktury.
-   Zobrazit dílčí hlavní knihu.

## <a name="subledger-journals-for-free-text-invoices"></a> Dílčí hlavní knihy pro volné faktury
Před zaúčtováním volné faktury můžete zobrazit celý účetní zápis faktury, který zahrnuje pohledávky a závazky, abyste ověřili, zda je faktura zaúčtována na správné účty. Toto zobrazení celkového zápisu do účetnictví se nazývá dílčí hlavní kniha. Pokud zobrazíte náhled dříve, než zapíšete fakturu dodavatele do deníku, a položka dílčí hlavní knihy není správná, nelze položku dílčí hlavní knihy změnit. Namísto toho je nutné změnit rozúčtování nebo účetní profil. Rozúčtování slouží k definování jedné strany účetní položky, má dáti nebo dal. Vyrovnání účetní položky dílčí hlavní knihy je vytvořeno z účetních profilů, jako je například účet odběratele nebo daň.



