---
title: Příklad dnů snížení
description: Příklad dnů snížení
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 97fb032d02df1dbedaeccec14496cb1d63e8cf70
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567936"
---
# <a name="reduction-days-example"></a>Příklad dnů snížení

[!include [banner](../includes/banner.md)]

Vytvořili jste transakci předplatného pro předplatné zákaznické údržby podle popisu v následující tabulce.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
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
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]