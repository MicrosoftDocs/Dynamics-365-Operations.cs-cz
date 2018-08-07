---
title: "Nákupní objednávky pro projekt"
description: "Tento článek popisuje různé metody, které slouží k vytváření nákupních objednávek pro určitý projekt. Použitá metodu závisí na účelu nákupní objednávky a kdy jsou zakoupené položky spotřebovány a účtovány v projektu."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: dae65394a2180ccbf3317a41b635ba97034e541b
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="purchase-orders-for-a-project"></a>Nákupní objednávky pro projekt

[!include [banner](../includes/banner.md)]

Tento článek popisuje různé metody, které slouží k vytváření nákupních objednávek pro určitý projekt. Použitá metodu závisí na účelu nákupní objednávky a kdy jsou zakoupené položky spotřebovány a účtovány v projektu.

V aplikaci Microsoft Dynamics 365 for Finance and Operations můžete použít několik způsobů pro vytvoření nákupních objednávek pro určitý projekt. Použitá metodu závisí na účelu nákupní objednávky, kdy jsou zakoupené položky spotřebovány, a kdy jsou zakoupené položky účtovány v projektu.

### <a name="methods-for-creating-a-purchase-order"></a>Způsoby vytvoření nákupní objednávky

Jednu z následujících metod můžete použít k vytvoření nákupní objednávky v modulu Řízení a účetnictví projektu. Účel nákupní objednávky určuje, kdy je nákupní objednávka spotřebována a tedy kdy lze na projektu účtovat poplatky za položky.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metoda</th>
<th>Účel</th>
<th>Spotřeba položek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vytvoření nákupní objednávky přímo z projektu.</td>
<td>Tuto metodu použijte pro nákup zboží od externího dodavatele pro účely spotřeby na projektu. Nákupní objednávku lze vytvořit dvěma způsoby.
<ul>
<li>Ze samotného projektu. V tomto případě je projekt pro nákupní objednávku již definován.</li>
<li>Přechodem k nákupní objednávce projektu. Je nezbytné vybrat jak dodavatele, tak projekt, pro který se má nákupní objednávka vytvořit.</li>
</ul></td>
<td>Položky jsou spotřebovány při aktualizaci faktury dodavatele.</td>
</tr>
<tr class="even">
<td>Vytvořte nákupní objednávku z prodejní objednávky.</td>
<td>Tato metoda se použije, pokud se mají nakoupit položky při vytváření prodejní objednávky z projektu.</td>
<td>Položky jsou spotřebovány, když se prodejní objednávka fakturuje odběrateli.</td>
</tr>
<tr class="odd">
<td>Vytvořte nákupní objednávku z požadavku na položku.</td>
<td>Tato metoda se použije, pokud se mají nakoupit položky při vytváření požadavku na položku z projektu.</td>
<td>Položky jsou spotřebovány, když se aktualizuje dodací list požadavku na položku.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Při aktualizaci faktury nebo dodacího listu dodavatele budete požádáni, abyste aktualizovali dodací list v požadavku na položku.

Další informace naleznete v tématu [Přijetí položek na nákupní objednávce z požadavku na položku](tasks/receive-items-purchase-order-item-requirement.md).


