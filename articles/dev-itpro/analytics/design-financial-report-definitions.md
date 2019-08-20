---
title: Definice sestavy v návrháři finanční sestavy
description: Tento článek obsahuje informace o definicích sestavy. Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Definice sestavy také poskytuje možnosti a nastavení pro přizpůsobení sestavy.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848334"
---
# <a name="report-definitions-in-financial-report-designer"></a>Definice sestavy v návrháři finanční sestavy

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o definicích sestavy. Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Definice sestavy také poskytuje možnosti a nastavení pro přizpůsobení sestavy. 

Definice sestavy představuje součást sestavy (nebo stavební blok), který využívá definici řádku, definici sloupce a volitelně definici stromu výkaznictví pro vytvoření sestavy. Definice sestavy nabízí také další možnosti a nastavení, které můžete použít pro přizpůsobení sestavy. Po vytvoření definic řádků a sloupců je nutno je zkombinovat do definice sestavy. V tomto okamžiku můžete také definovat další aspekty definic, například úroveň podrobností a datum sestavy. Poté můžete sestavu uložit a vygenerovat. Finanční výkaznictví nabízí následující úrovně podrobností:

- Finanční
- Finanční a účetní
- Finanční, účetní a transakční

V závislosti na tom, jak jsou data v systému Microsoft Dynamics ERP uložena, však v sestavách nemusejí být dostupné podrobnosti transakcí.

## <a name="create-a-report-definition"></a>Vytvoření definice sestavy
1. V Návrháři sestav v nabídce **Soubor** klikněte na tlačítko **Nový** a vyberte možnost **Definice sestavy**.
2. Zadejte příslušné informace na kartách **Sestava**, **Výstup a distribuce**, **Záhlaví a zápatí** a **Nastavení**.

## <a name="contents-of-a-report-definition"></a>Obsah definice sestavy
Následující tabulka popisuje karty v definici sestavy a způsob použití těchto informací.

<table>
<thead>
<tr>
<th>TAB</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sestava</td>
<td>Umožňuje vytvořit sestavu, konfigurovat sestavu nebo změnit existující sestavu.</td>
</tr>
<tr>
<td>Výstup a distribuce</td>
<td>Umožňuje změnit typ výstupu a cílové umístění sestavy.</td>
</tr>
<tr>
<td>Záhlaví a zápatí</td>
<td>Umožňuje definovat a naformátovat záhlaví a zápatí sestavy. Například můžete přidat text a obrázky pro záhlaví nebo zápatí. Finanční výkaznictví podporuje soubory BMP, JPG a PNG jako obrázky. Můžete také přidat kódy automatického textu a vložit tak další informace, například název společnosti, název sestavy nebo číslo stránky.</td>
</tr>
<tr>
<td>Nastavení</td>
<td>Zadejte nastavení definice sestavy, například následující nastavení:
<ul>
<li>Formátování a částky ze zaokrouhlení</li>
<li>Formát sestavy podrobností</li>
<li>Formátování organizačního stromu</li>
<li>Generování sestavy výjimek</li>
<li>Určit převod měny</li>
<li>Podrobnosti o mezisoučtu a filtrování podrobností účtů.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Další zdroje

[Finanční výkaznictví](financial-reporting-intro.md)
