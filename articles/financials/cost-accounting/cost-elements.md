---
title: Dimenze prvku nákladů
description: Coby jeden ze základních pilířů v nákladovém účetnictví se dimenze prvků nákladů používají pro kategorizaci a sledování, kam jsou náklady převáděny.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 037d4971fe0a5a9d08f0ed20d2482b8feb9aa4f2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841602"
---
# <a name="cost-element-dimensions"></a>Dimenze prvku nákladů

[!include [banner](../includes/banner.md)]

Coby jeden ze základních pilířů v nákladovém účetnictví se dimenze prvků nákladů používají pro kategorizaci a sledování, kam jsou náklady převáděny. 

Prvek nákladů odpovídá příslušné položce nákladů v účtové osnově. V zásadě může jít o libovolný typ prvku v nejnižší úrovni společnosti, kde může docházet k toku nákladů. Prvky nákladů jako koncept se pohybují od účtů hlavní knihy po všechny prostředky související s náklady. V současné době nákladové účetnictví podporuje účty hlavní knihy.

## <a name="two-types-of-cost-elements"></a>Dva typy prvků nákladů
Existují dva typy prvků nákladů: primární prvky nákladů a sekundární prvky nákladů. Následující tabulka popisuje rozdíly mezi oběma typy.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Primární prvky nákladů</strong></td>
<td><strong>Prvky druhotných nákladů</strong></td>
</tr>
<tr class="even">
<td>Primární prvky nákladů představují tok nákladů z finančního účetnictví do nákladového účetnictví. Struktura prvku nákladů odpovídá ziskům a ztrátám účetní struktury v hlavní knize, kde prvek nákladů může odpovídat hlavnímu účtu. Ne všechny hlavní účty musejí být nutně prezentovány jako prvky nákladů závisející na obchodních potřebách. Příklady primárních prvků nákladů zahrnují:
<ul>
<li>Náklady prodaného zboží</li>
<li>Nepřímé náklady na materiál</li>
<li>Osobní náklady</li>
<li>Náklady na energii</li>
</ul></td>
<td>Sekundární prvky nákladů představují tok nákladů interně, protože tyto náklady vznikají a používají se pouze v nákladovém účetnictví. Používají se pokud chcete zajistit, že lze sledovat zdroje nákladů. Tyto prvky nákladů se používají při přidělování nákladů a výpočtech režijních nákladů. Příklady sekundárních prvků nákladů zahrnují:
<ul>
<li>Výrobní náklady</li>
<li>Výroba, materiál a režie marketingu</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Dimenze prvku nákladů a členy dimenze prvku nákladů
Prvky náklady se označují jako *dimenze prvků nákladů* . Hodnoty jednotlivých dimenzí se nazývají *členy dimenze prvku nákladů*. V USA máme například strukturu účtové osnovy (COA), která je základem pro statutární vykazování. Tato COA slouží jako dimenze prvku nákladů. Účty, které jsou primární prvky nákladů, jsou představovány jako členy dimenze prvku nákladů v nákladovém účetnictví. Následující obrázek znázorňuje příklad hlavního účtu jako dimenze prvku nákladů s jeho aktuálními hlavními účty jako členy dimenze prvku nákladů. 

[![Dimenze prvku nákladů](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Import členů dimenze prvků nákladů pomocí datových konektorů
K usnadnění nastavení členů dimenze prvku nákladů v nákladovém účetnictví můžete použít datové konektory, které jsou předem připravené nebo vytvořené na míru, abyste získali zpět primární prvky nákladů z jednoho nebo více zdrojových systémů.

## <a name="implementation-considerations"></a>Na co myslet při implementaci
Jelikož prvky nákladů představují nejnižší úroveň podrobností o nákladech, měli byste se ujistit, že všechny požadované prvky nákladů pro manažerské vykazování jsou zahrnuty při implementací struktury prvků nákladů. Může být obtížné najít vhodný počet prvků nákladů pro řízení nákladů. Tisíce prvků nákladů pravděpodobně ztíží řízení jednotlivých prvků nákladů. Jako alternativní postup lze seskupit prvky nákladů a správu řízení nákladů v agregační úrovni.



