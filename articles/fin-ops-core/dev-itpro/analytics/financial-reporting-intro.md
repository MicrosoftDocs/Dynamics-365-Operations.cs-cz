---
title: Finanční výkaznictví
description: Finanční výkaznictví je nástroj, pomocí kterého mohou pracovníci v oblasti financí a obchodu vytvářet, spravovat, nasazovat a kontrolovat finanční výkazy.
author: aprilolson
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 68813,  ""intro-internal
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.form: FinanicalReportingSetup
ms.openlocfilehash: e7a31f44acafc7703f6d82ad0271fde0d0bb7906
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280054"
---
# <a name="financial-reporting"></a>Finanční výkaznictví

[!include [banner](../includes/banner.md)]

Finanční výkaznictví v aplikaci je nástroj, který finanční a obchodní profesionálové mohou používat k vytváření, správě, nasazení a zobrazování finančních výkazů. Obchází omezení tradičních sestav a pomáhá efektivně navrhnout různé typy sestav.

Finanční výkaznictví zahrnuje podporu dimenzí. Proto jsou segmenty účtu nebo dimenze okamžitě k dispozici. Žádné další nástroje nebo konfigurační kroky nejsou požadovány.

## <a name="financial-reporting-setup"></a>Nastavení finančního výkaznictví
Stránka **Nastavení finančního výkaznictví** obsahuje seznam všech finančních dimenzí v systému. **Hlavní kniha** \> **Nastavení hlavní knihy** \> **Nastavení finančního výkaznictví**.

Stránka **Nastavení finančního výkaznictví** má dvě části, které určují data vykazovaná ve finančním výkaznictví:

- **Karta Dimenze** – Vzhledem k tomu, že různé společnosti používají různé dimenze a účetní struktury, nelze určit pořadí, ve kterém uživatelé potřebují zobrazit všechny finanční dimenze v sestavách. Tato stránka vám umožní nastavit pořadí, ve kterém si přejete zobrazovat finanční dimenze při tvorbě a zobrazení sestavy ve finančním výkaznictví.
- **Karta Atributy** je místem, kde můžete zvolit, zda chcete použít možnosti **Dodavatelé** a **Odběratelé** jako atributy pro účely filtrování a návrhu sestav. Vykazování na úrovni dodavatele a odběratele bude užitečné pouze tehdy, pokud nezadáte do jednoho dokladu při zaúčtování transakcí více dodavatelů a odběratelů. Výběr dodavatele anebo odběratele přidá další čas pro integraci.

## <a name="financial-reporting-components"></a>Součásti finančního výkaznictví
Následující součásti finančního výkaznictví umožňují snadné vytváření, zobrazování a plánování sestav.

| Součást        | Funkce | Doplňkové informace |
|------------------|-----------|------------------------|
| Návrhář sestav  | Vytváření stavebních bloků sestav, které v kombinaci definují a generují sestavy. Průvodce sestavou provádí méně zkušené uživatele procesem návrhu. Pokročilí uživatelé mohou vytvořit nové stavební bloky sestav nebo upravit existující stavební bloky podle svých potřeb. | |
| Plánování sestav | Naplánujte jednu sestavu nebo skupinu sestav tak, aby se generovala v pravidelných intervalech. | [Generování finančních sestav](generate-financial-report.md) |

## <a name="features"></a>Funkce
<table>
<thead>
<tr>
<th>Funkce</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Flexibilita navrhování sestav</td>
<td>Návrhář sestav zahrnuje následující možnosti vykazování při navrhování sestavy:
<ul>
<li>ukládat kombinace dimenzí a znovu používat dimenze pro více sestav;</li>
<li>řídit způsob formátování a zobrazování popisů dimenzí;</li>
<li>Rozpoznejte účty nebo dimenzí, které byly vynechány ve stavebních blocích sestavy.</li>
<li>Formátování záhlaví pro klouzavé prognózy.</li>
</ul>
</td>
</tr>
<tr>
<td>Spolupráce při vytváření finančních sestav</td>
<td>Následující funkce pomáhají spravovat generování a distribuci sestav:
<ul>
<li>plánování automatického generování sestav s denní, týdenní, měsíční nebo roční pravidelností;</li>
<li>export do formátu jen pro čtení XPS, který poskytuje lepší zabezpečení dokumentů s digitálními podpisy;</li>
<li>Export do listu aplikace Microsoft Excel.</li>
<li>pokud chcete sdílet sestavy, můžete vytvářet e-mailové zprávy, které obsahují odkazy na sestavy.</li>
</ul>
</td>
</tr>
<tr>
<td>Prohlížení interaktivních sestav</td>
<td>Interaktivní funkce umožňují provádět následující úlohy:
<ul>
<li>Změna data sestavy pro sestavu, kterou prohlížíte.</li>
<li>Změna měny sestavy, kterou prohlížíte.</li>
<li>Zobrazení sestavy v souhrnném zobrazení nebo podrobném zobrazení.</li>
<li>Přidání filtrů dimenze pro omezení obsahu sestavy na specifickou dimenzi nebo kombinaci dimenzí.</li>
<li>Přidání filtrů atributu pro omezení obsahu sestavy na specifický atribut nebo kombinaci atributů.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Další zdroje
[Generování finančních sestav](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
