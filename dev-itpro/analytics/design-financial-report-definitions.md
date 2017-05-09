---
title: "Definice sestavy v návrháři finanční sestavy"
description: "Tento článek obsahuje informace o definicích sestavy. Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Definice sestavy také poskytuje možnosti a nastavení pro přizpůsobení sestavy."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 58 - 18
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81ac503410e51672c2f97a76d37d4c567832912f
ms.lasthandoff: 03/29/2017


---

# <a name="report-definitions-in-financial-report-designer"></a>Definice sestavy v návrháři finanční sestavy

Tento článek obsahuje informace o definicích sestavy. Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Definice sestavy také poskytuje možnosti a nastavení pro přizpůsobení sestavy. 

Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Definice sestavy také nabízí možnosti a nastavení, které můžete použít pro přizpůsobení sestavy. Po definování definic řádků a sloupců je musíte zkombinovat do definice sestavy. V tomto okamžiku můžete také definovat další aspekty definic, například úroveň podrobností a datum sestavy. Poté můžete sestavu uložit a vygenerovat. Finanční výkaznictví nabízí následující úrovně podrobností:

-   Finanční
-   Finanční a účetní
-   Finanční, účetní a transakční

V závislosti na tom, jakým způsobem jsou data uložena v systému Microsoft Dynamics ERP, však nemusí být detaily transakcí k dispozici v sestavách.

## <a name="create-a-report-definition"></a>Vytvoření definice sestavy
1.  V Návrháři sestav v nabídce **Soubor** klikněte na tlačítko **Nový** a vyberte možnost **Definice sestavy**.
2.  Zadejte příslušné informace na kartách **Sestava**, **Výstup a distribuce**, **Záhlaví a zápatí** a **Nastavení**.

## <a name="contents-of-a-report-definition"></a>Obsah definice sestavy
V následující tabulce jsou popsány karty v definici sestavy a způsob použití zadaných informací.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Karta</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sestava</td>
<td>Umožňuje vytvořit sestavu, nakonfigurovat sestavu nebo upravit existující sestavu.</td>
</tr>
<tr class="even">
<td>Výstup a distribuce</td>
<td>Umožňuje změnit typ výstupu a místo určení sestavy.</td>
</tr>
<tr class="odd">
<td>Záhlaví a zápatí</td>
<td>Umožňuje definovat a formátovat záhlaví a zápatí sestavy. Například můžete přidat text a obrázky pro záhlaví nebo zápatí. Finanční výkaznictví podporuje soubory BMP, JPG a PNG jako obrázky. Můžete také přidat kódy automatického textu a vložit tak další informace, například název společnosti, název sestavy nebo číslo stránky.</td>
</tr>
<tr class="even">
<td>Nastavení</td>
<td>Umožňuje určit nastavení definice sestavy, například následující nastavení:
<ul>
<li>Formátování a zaokrouhlování částek</li>
<li>Formátování sestav s podrobnostmi</li>
<li>Formátování stromů výkaznictví</li>
<li>Generování sestavy výjimek</li>
<li>Určení převodu měny</li>
<li>Mezisoučty a filtrování podrobností účtu</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví v aplikaci Microsoft Dynamics 365 for Operations](financial-reporting-intro.md)


