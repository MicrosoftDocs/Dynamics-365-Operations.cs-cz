---
title: Hodnoty objektu zásob
description: Tento článek obsahuje informace o výpočtu hodnot objektu zásob.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 543253714b3cf318ad5f6092b190e777772f956f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910130"
---
# <a name="inventory-object-values"></a>Hodnoty objektu zásob

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o výpočtu hodnot objektu zásob. 

Nová funkce **„fyzické množství“** umožňuje zobrazit hodnoty určitého objektu zásob. 

Nákladový objekt představuje úroveň entity, kde bude probíhat účtování zásob. Další informace o nákladových objektech naleznete v tématu [Nákladové objekty](cost-object.md). 

Pokud chcete zobrazit hodnoty konkrétního objektu zásob, klikněte na tlačítko **Fyzické množství** na stránce **Objekt nákladů**. Zde je způsob výpočtu hodnoty objektu zásob: 

Objekt zásob.Hodnota = Objektu nákladů.Průměrné náklady na jednotku x Objekt zásob.Množství 

Následující příklad ukazuje způsob výpočtu hodnot objektu zásob a objektu nákladů. U položky A jsou registrovány dvě události příjemky produktu:

-   Příjemka produktu 1: Množství = 100 kusů., Množství = 1 000,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky = B1
-   Příjemka produktu 2: Množství = 50 kusů., Množství = 800,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky = B2

Následující tabulka zobrazuje výsledek výpočtu nákladového objektu. Výsledky lze zobrazit na stránce **Nákladový objekt**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ objektu</th>
<th>Číslo zboží</th>
<th>Lokalita</th>
<th>Množství</th>
<th>Skladová jednotka</th>
<th>Hodnota</th>
<th>Průměrné náklady na jednotku</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Objekt nákladů</td>
<td>O</td>
<td>1</td>
<td>150</td>
<td>Ks</td>
<td><p>1 800,00 Kč</p></td>
<td><p>12,00 Kč</p></td>
</tr>
</tbody>
</table>

Následující tabulka zobrazuje výsledek výpočtu objektu zásob. Výsledky lze zobrazit kliknutím na možnost **Fyzické množství** na stránce **Nákladový objekt**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ objektu</th>
<th>Číslo zboží</th>
<th>Lokalita</th>
<th>Sklad</th>
<th>Č. dávky</th>
<th>Množství</th>
<th>Skladová jednotka</th>
<th>Hodnota</th>
<th>Průměrné náklady na jednotku</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Objekt zásob</td>
<td>O</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Ks</td>
<td><p>1 200,00 Kč.</p></td>
<td><p>12,00 Kč</p></td>
</tr>
<tr class="even">
<td>Objekt zásob</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Ks</td>
<td><p>600,00 Kč</p></td>
<td><p>12,00 Kč</p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Další zdroje
--------

[Nákladové objekty](cost-object.md)

[Položky nákladů](cost-entries.md)

[Co je nového a co se změnilo](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]