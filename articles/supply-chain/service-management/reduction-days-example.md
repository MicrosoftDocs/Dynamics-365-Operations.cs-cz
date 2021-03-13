---
title: Příklad dnů snížení
description: Příklad dnů snížení
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 509d1a9e2abd79938376209d8feab1b935394833
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010515"
---
# <a name="reduction-days-example"></a>Příklad dnů snížení 

[!include [banner](../includes/banner.md)]


Vytvořili jste transakci předplatného pro předplatné zákaznické údržby podle popisu v následující tabulce.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Od data</p></th>
<th><p>Do data</p></th>
<th><p>Předplatné</p></th>
<th><p>Typ předplatného</p></th>
<th><p>Project</p></th>
<th><p>Kategorie</p></th>
<th><p>Prodejní měna</p></th>
<th><p>Prodejní cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01. března 2011</p></td>
<td><p>31. března 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Řádné</strong></p></td>
<td><p>9013</p></td>
<td><p>Dílčí kategorie 2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Zákazník ohlásí, že nevyžaduje disponibilitu služeb po dobu dvou dnů (10. a 11. března). Souhlasíte se snížením předplatného o tyto dva dny.

Vytvoříte novou transakci typu **Dny omezení** podle popisu v následující tabulce.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Od data</p></th>
<th><p>Do data</p></th>
<th><p>Předplatné</p></th>
<th><p>Typ předplatného</p></th>
<th><p>Project</p></th>
<th><p>Kategorie</p></th>
<th><p>Prodejní měna</p></th>
<th><p>Prodejní cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10. března 2011</p></td>
<td><p>11. března 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Dny omezení</strong></p></td>
<td><p>9013</p></td>
<td><p>Dílčí kategorie 2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Při fakturaci transakcí pro březen 2011 je prodejní cena 200 EUR snížena o částku 12,90 EUR. Fakturovatelná částka pro transakci předplatného je tedy 187,10 EUR a obě transakce budou fakturovány celkovou částkou 187,10 EUR.

## <a name="see-also"></a>Viz také

[Snížení počtu dnů u poplatků za odběr](reduce-the-days-on-subscription-fees.md)

  


