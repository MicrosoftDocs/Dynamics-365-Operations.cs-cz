---
title: "Pravidla zásad auditu"
description: "Zásady auditu můžete použit pro vyhodnocení sestav výdajů, faktur dodavatele a nákupních objednávek, abyste se ujistili, že jsou v souladu s pravidly zásad, které jste vytvořili. Všechna pravidla, která jsou přidružena k zásadě auditu, jsou spouštěna v dávkovém režimu podle určeného plánu.  Každé pravidlo zásad je instancí typu pravidla zásad. Pro každý typ pravidla zásad může být aktivní pouze jedno pravidlo zásad současně."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c3fac2117fbc580e0c40d840a037f3073d66b4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="audit-policy-rules"></a>Pravidla zásad auditu

[!include[banner](../includes/banner.md)]


Zásady auditu můžete použit pro vyhodnocení sestav výdajů, faktur dodavatele a nákupních objednávek, abyste se ujistili, že jsou v souladu s pravidly zásad, které jste vytvořili. Všechna pravidla, která jsou přidružena k zásadě auditu, jsou spouštěna v dávkovém režimu podle určeného plánu.  Každé pravidlo zásad je instancí typu pravidla zásad. Pro každý typ pravidla zásad může být aktivní pouze jedno pravidlo zásad současně. 

<a name="queries-and-query-types"></a>Dotazy a typy dotazů
-----------------------

Když vytvoříte pravidlo zásad auditu, nejprve vyberte typ pravidla zásad. Typ pravidla zásad určuje dotaz pro strom aplikačních objektů (AOT), který bude použit jako výchozí bod při vytvoření pravidla zásad. Určuje také typ dotazu pro pravidla zásad. Dotaz určuje zdrojový dokument, pro který je pravidlo zásad vyhodnoceno. Určuje také pole ve zdrojovém dokumentu, který určuje právnickou osobu a data použité při výběru dokumentů pro audit. Typ dotazu řídí výchozí pole na stránce s dotazy a na stránce pravidel zásad auditu. V následující tabulce jsou uvedeny typy dotazů dostupné pro pravidla zásad auditu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ dotazu</th>
<th>Účel</th>
<th>Více informací</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Podmíněné</td>
<td>Vyhodnoťte atributy zdrojového dokumentu proti zadaným hodnotám.</td>
<td></td>
</tr>
<tr class="even">
<td>Agregovat</td>
<td>Vyhodnoťte více zdrojových dokumentů nebo řádků zdrojového dokumentu proti pravidlu zásad sečtením číselné hodnoty.</td>
<td></td>
</tr>
<tr class="odd">
<td>Vzorkování</td>
<td>Vyberte náhodně zadané procento zdrojových dokumentů pro vyhodnocení narušení zásad.</td>
<td>Pokud vyberete tuto možnost, použijte stránku Pravidla zásad auditu a zadejte procento dokumentů, které chcete náhodně vybrat pro audit.</td>
</tr>
<tr class="even">
<td>Duplicitní</td>
<td>Vyhodnoťte zdrojové dokumenty a určete, zda obsahují duplicitní záznamy v určených polích.</td>
<td>Když vyberete tuto možnost, použijte stránku Pravidla zásad auditu a zadejte počet dní, které chcete přidat na začátek rozsahu dat pro výběr dokumentu při vyhodnocení duplicitních záznamů dokumentů.</td>
</tr>
<tr class="odd">
<td>Vyhledávání seznamu</td>
<td>Vyhodnocení zdrojových dokumentů pro dané entity.</td>
<td>Kořenový dokument dotazu definuje dokument, u kterého bude proveden audit. Dotaz musí být dotaz seznamu, který obsahuje odkaz na tabulku dirpartytable. Tuto možnost lze použít pouze u dotazů AOT:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (zaměstnanci sledovaní v sestavě výdajů)</li>
<li><span class="ui">AuditPolicyPurchList</span> (dodavatelé sledovaní v nákupní objednávce)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Dodavatelé sledovaní ve fakturách dodavatele)</li>
</ul>
Pokud vyberete tuto možnost, zadejte sledované entity na stránce Pravidlo zásad auditu.</td>
</tr>
<tr class="even">
<td>Vyhledávání klíčových slov</td>
<td>Vyhodnocení zdrojových dokumentů a určení toho, zda obsahují určitá slova.</td>
<td>Pokud vyberete tuto možnost, zadejte vyhledávaná slova na stránce Pravidlo zásad auditu. Stránka Pravidlo zásad auditu obsahuje také volby, které vám umožňují určit tabulky a pole k vyhodnocení zadaných slov.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Společné parametry
Všechna pravidla zásad pro určitou zásadu auditu sdílí stejné parametry dávky a stejný rozsah data pro výběr dokumentu. Tyto parametry jsou zadány pro zásady na stránce Další možnosti.



<a name="see-also"></a>Viz také
--------

[Porušení a případy zásad auditu](audit-policy-violations-cases.md)
[Definování zásad auditu pro zdrojové dokumenty](tasks/define-audit-policies-source-documents.md)



