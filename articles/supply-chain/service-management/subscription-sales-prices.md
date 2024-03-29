---
title: Prodejní cena předplatného
description: Při vytváření předplatného je prodejní cena odvozena od nastavení prodejní ceny vytvořené ve formuláři Prodejní cena (předplatné).
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae15c49483a4967edfd23fc0ab6b614fe282afea
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676600"
---
# <a name="subscription-sales-prices"></a>Prodejní cena předplatného

[!include [banner](../includes/banner.md)]

Při vytváření předplatného je prodejní cena odvozena od nastavení prodejní ceny vytvořené ve formuláři **Prodejní cena (předplatné)**.

Ve formuláři **Prodejní cena (předplatné)** můžete vytvořit prodejní ceny pro konkrétní předplatné nebo můžete vytvořit obecněji platné prodejní ceny. Aby byla prodejní cena u předplatného použita, musí být kód období a měna předplatného a prodejní stejný jako kód období a měna prodejní ceny.

Jestliže jsou kód období a měna pro předplatné i pro prodejní cenu identické, jsou prodejní ceny předplatného vybírány na základě priorit uvedených v následující tabulce. Prázdná buňka v tabulce označuje prázdné pole a X označuje, že je hodnota rovna hodnotě předplatného, ze které je transakce generována.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Priorita </p></th>
<th><p><strong>Kategorie</strong></p></th>
<th><p><strong>ID projektu</strong></p></th>
<th><p><strong>Předplatné</strong></p></th>
<th><p><strong>Měna prodeje</strong></p></th>
<th><p><strong>Kód období</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>

Pokud je vytvořen poplatek předplatného, je jako prodejní cena předplatného vybrána prodejní cena s nejvyšší úrovní podrobností, jak je uvedeno v předchozí tabulce.

## <a name="update-and-index-subscription-sales-prices"></a>Aktualizace a indexování prodejních cen předplatného

Prodejní cenu předplatného můžete aktualizovat aktualizováním základní ceny nebo indexu. Aktualizovat lze o procentuální hodnotu nebo na novou hodnotu.

## <a name="subscription-fee-sales-prices"></a>Prodejní ceny poplatků předplatného

Při vytváření poplatku odběru je prodejní cena založena na nastavení prodejní ceny předplatného. Můžete buď použít základní cenu z nastavení ceny předplatného, nebo vytvořit indexované prodejní ceny.

## <a name="example"></a>Příklad

Chcete nastavit prodejní ceny předplatného na 500 EUR pro nový projekt 9030. Ve formuláři **prodejní cena (předplatné)** vytvoříte řádek prodejní ceny předplatného podle návodu v následující tabulce.

<table>
<colgroup>
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
<th><p>Platné od</p></th>
<th><p>Kategorie</p></th>
<th><p>Project</p></th>
<th><p>Předplatné</p></th>
<th><p>Kód období</p></th>
<th><p>Prodejní měna</p></th>
<th><p>Prodejní cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Měsíc</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Pole **Kategorie** a **Předplatné** jsou prázdná.

Potom vytvoříte následující předplatná.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Předplatné servisu</p></th>
<th><p>Project</p></th>
<th><p>Skupina předplatného</p></th>
<th><p>Kategorie</p></th>
<th><p>Měna</p></th>
<th><p>Kód období</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Předpl.1</p></td>
<td><p>Kateg.předpl.1</p></td>
<td><p>EUR</p></td>
<td><p>Měsíčně</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Předpl.1</p></td>
<td><p>Kateg.předpl.2</p></td>
<td><p>EUR</p></td>
<td><p>Měsíčně</p></td>
</tr>
</tbody>
</table>


Nyní vytvoříte poplatky předplatného pro obě předplatné ve skupině předplatného Předpl.1:

1.  Klikněte na uzel **Řízení služeb** \> **Nastavení** \> **Servisní zakázky** \> **Skupiny předplatného**.

2.  Ve formuláři **skupiny předplatného** klepněte na možnost **funkce** \> **Vytvořit poplatek předplatného**.

3.  Ve formuláři **Vytvořit poplatek za předplatné** zadejte příslušné informace do polí. Další informace o transakcích poplatků naleznete v tématu [Vytvoření transakcí poplatku za předplatné](create-subscription-fee-transactions.md)..

Pro obě předplatná jsou vytvořeny poplatky předplatného s prodejní cenou 500 EUR, jak je uvedeno v následující tabulce.

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
<th><p>Datum projektu</p></th>
<th><p>Předplatné servisu</p></th>
<th><p>Project</p></th>
<th><p>Kategorie</p></th>
<th><p>Datum zahájení</p></th>
<th><p>Koncové datum</p></th>
<th><p>Prodejní měna</p></th>
<th><p>Prodejní cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Kateg.předpl.1</p></td>
<td><p>1. 1. 2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Kateg.předpl.2</p></td>
<td><p>1. 1. 2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Později se rozhodnete, že budete chtít zadat prodejní ceny pro kategorii Kateg.předpl.1 pro projekt 9030. Proto vytvoříte nový řádek prodejní ceny s prodejní cenou 550 EUR pro kombinaci projektu 9030 a kategorie poplatků Kateg.předpl.1. Pro projekt 9030 nyní existují dva řádky prodejní ceny předplatného, jak ukazuje následující tabulka.

<table>
<colgroup>
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
<th><p>Platné od</p></th>
<th><p>Kategorie</p></th>
<th><p>Project</p></th>
<th><p>Předplatné</p></th>
<th><p>Kód období</p></th>
<th><p>Měna</p></th>
<th><p>Prodejní cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Měsíc</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2007</p></td>
<td><p>Kateg.předpl.1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Měsíc</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>

Opakováním výše uvedeného postupu vytvoříte poplatky předplatného pro obě předplatné ve skupině předplatného Předpl.1. Následující tabulka ukazuje transakce, které jsou vytvořeny pro každé předplatné připojené ke skupině předplatného:

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
<th><p>Datum projektu</p></th>
<th><p>Předplatné</p></th>
<th><p>Project</p></th>
<th><p>Kategorie</p></th>
<th><p>Datum zahájení</p></th>
<th><p>Datum ukončení</p></th>
<th><p>Prodejní měna</p></th>
<th><p>Prodejní cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-07-2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Kateg.předpl.1</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28-07-2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Kateg.předpl.2</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>

V první transakci pro předplatné 00020\_13 je prodejní cena 550 EUR odvozena od prodejní ceny předplatného nastavené pro kombinaci konkrétního projektu a kategorie. Ve druhé transakci pro předplatné 00021\_135 se jako prodejní cena předplatného projektu používá prodejní cena 500 EUR, protože není nastavena cena pro kombinaci projektu 9030 a kategorie Kateg.předpl.2.

## <a name="see-also"></a>Viz také

[Aktualizace a indexování prodejních cen předplatného](update-and-index-subscription-sales-prices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
