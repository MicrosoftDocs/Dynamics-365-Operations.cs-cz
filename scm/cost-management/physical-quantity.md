---
title: "Hodnoty objektu zásob"
description: "Tento článek obsahuje informace o výpočtu hodnot objektu zásob."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Hodnoty objektu zásob

Tento článek obsahuje informace o výpočtu hodnot objektu zásob. 

Nová funkce nazvaná ** fyzické množství ** umožňuje zobrazit hodnoty určitého objektu zásob. Nákladový objekt představuje úroveň entity, kde bude probíhat účtování zásob. Další informace o nákladových objektech naleznete v tématu [Nákladové objekty](cost-object.md). Pokud chcete zobrazit hodnoty konkrétního objektu zásob, klikněte na tlačítko **Fyzické množství** na stránce **Objekt nákladů**. Toto je postup, jak se počítá hodnota objektu zásob: Objekt zásob.Hodnota = Nákladový objekt.Průměrné náklady na jednotku x Objekt zásob.Množství Následující příklad ukazuje způsob výpočtu hodnoty objektu zásob a nákladového objektu. U položky A jsou registrovány dvě události příjemky produktu:

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
<td>A.</td>
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



<a name="see-also"></a>Viz také
--------

[Nákladové objekty](cost-object.md)

[Položky nákladů](cost-entries.md)

[Co je nového a co se změnilo v aplikaci Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

