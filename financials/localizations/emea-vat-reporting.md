---
title: "DPH, vykazování pro Evropu"
description: "Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-01-11 13 - 48 - 01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266844
ms.assetid: 06798e29-6140-489e-9b4e-66b45b26be2b
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 84a639b25c64821e00ca4397f42f69298953e599
ms.lasthandoff: 03/31/2017


---

# <a name="vat-reporting-for-europe"></a>DPH, vykazování pro Evropu

Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země.

Toto téma obsahuje obecný přístup k nastavení a generování výkazu DPH. Tento přístup je společné pro uživatele v právnických osobách, které v těchto zemích a oblastech:

-   Rakousko
-   Belgie
-   Česká republika
-   Estonsko
-   Finsko
-   Německo
-   Lotyšsko
-   Litva
-   Nizozemsko
-   Švédsko

## <a name="vat-statement-overview"></a>Přehled výkazu DPH
Výkaz DPH je založen na částky DPH transakce. Proces generování výkazu DPH je součástí procesu platby DPH, které je implementováno pomocí funkce DPH vyrovnání a post. Tato funkce vypočítá DPH splatné za dané období. Výpočet vyrovnání zahrnuje zaúčtovanou DPH pro vybrané období vyrovnání transakcí DPH. Postup pro výpočet dat pro výkaz DPH je založena na vztahu mezi kódy DPH a kódy, kde odpovídají kódy vykazování DPH na DPH výkazů polí (nebo značky v souboru XML) vykazování DPH. Pro každý kód DPH by měla být kódy vykazování DPH nastavit pro každý typ transakce, například zdanitelné prodeje zdanitelné nákupy zdanitelného dovozu. Tento typ transakce, které jsou popsány v [kódy DPH pro vykazování DPH](#Sales tax codes for VAT reporting) oddílu dále v tomto tématu.

Pro každý kód vykazování prodejní daně se určí konkrétní sestavu rozložení. Ve stejnou dobu kódy DPH souvisejí s konkrétní finanční úřad prostřednictvím období vyrovnání DPH. Pro každý finanční úřad stanovit rozložení sestavy. Tedy pouze kódy vykazování DPH na stejné rozložení sestavy, která je nastavena pro finanční úřad v období vyrovnání DPH pro kód DPH lze vybrat v nastavení sestavy kódu DPH. DPH transakce generované při účtování objednávky nebo deníku, obsahuje kód DPH, DPH zdroj, směr DPH a částky transakcí (částku základu daně a výše daně v zúčtovací měně, DPH měně a měně transakce). V závislosti na kombinaci atributů transakce DPH, částky transakce tvoří celkové částky určené pro kódy DPH kódy vykazování DPH. Následující obrázek znázorňuje vztah data.

![Diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>Nastavení výkazu DPH
Generovat výkaz DPH nastavte následující.

### <a name="sales-tax-authorities-for-vat-reporting"></a>Finančnímu úřadu pro vykazování DPH

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Dříve než můžete vytvořit kódy vykazování DPH, je nutné vybrat správnou sestavu rozložení pro finanční úřad. Na **finančnímu úřadu** stránky v **Obecné** vyberte **rozložení**. Toto rozložení bude použit, když vytváříte kódy vykazování DPH.

### <a name="sales-tax-reporting-codes"></a>Kódy vykazování DPH

Kódy vykazování DPH jsou pole kódy DPH výkazu nebo značky názvy ve formátu XML. Tyto kódy se používají k agregaci a přípravě částky v sestavě. Při konfiguraci elektronické podobě sestavy výkazu DPH budou použity názvy částek výsledku. Můžete vytvářet a Udržovat kódy vykazování DPH **kódy vykazování DPH** stránky. Každý kód je nutné přiřadit rozložení sestavy. Jakmile vytvoříte kódy vykazování DPH, můžete použít kódy v **nastavení sestavy** oddílu na **kódy DPH** stránky. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Kódy DPH pro vykazování DPH

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).-->Základní částky a daňové částky prodejní daně, který může být agregovaný transakce na vykazování kódů ve výkazu DPH (značky XML nebo deklarace polí). Můžete to nastavit přiřazením vykazování kódů různých typů transakcí pro kódy DPH na DPH **kódy DPH** stránky. Následující tabulka popisuje typy transakcí v nastavení sestavy pro kódy DPH. Výpočet zahrnuje transakce pro všechny typy zdrojů s výjimkou DPH.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transaction type</strong></td>
<td><strong>Popis transakce a částky, které mají být počítány na typ transakce</strong></td>
</tr>
<tr class="even">
<td><strong>Zdanitelné prodeje</strong></td>
<td>Součet <strong>daně základní částky</strong> daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období /</li>
<li>Prodej je domácí (<strong>daně směr</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Nezdanitelných prodejů</strong></td>
<td>Součet <strong>daně základní částky</strong> daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je export (<strong>daně směr</strong> je <strong>Prodej bez daně</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax payable</strong></td>
<td>Součet <strong>daně částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je domácí (<strong>daně směr</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable sales credit note</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je domácí (<strong>daně směr</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Prodejní dobropis osvobozený od Fax</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je export (<strong>daně směr</strong> je <strong>Prodej bez daně</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on sales credit note</strong></td>
<td>Součet <strong>daně částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je domácí (<strong>daně směr</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable purchases</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>daně směr</strong> je <strong>pohledávky DPH</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free purchase</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je import (<strong>daně směr</strong> je <strong>bezcelní nákupní</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax receivable</strong></td>
<td>Součet <strong>daně částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>daně směr</strong> je <strong>pohledávky DPH</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable purchase credit note</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>daně směr</strong> je <strong>pohledávky DPH</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tax exempt purchase credit note</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je import (<strong>daně směr</strong> je <strong>bezcelní nákupní</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on purchase credit note</strong></td>
<td>Součet <strong>daně částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>daně směr</strong> je <strong>pohledávky DPH</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Daňové směr</strong> je <strong>spotřební daň</strong></li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import</strong></td>
<td>Stornované součtem <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Daňové směr</strong> je <strong>spotřební daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import credit note</strong></td>
<td>Součet <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
e<li><strong>Daňové směr</strong> je <strong>spotřební daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import credit note</strong></td>
<td>Stornované součtem <strong>daně základní částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Směr daně je <strong>spotřební daň</strong>.</li>
d<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Use tax</strong></td>
<td>Součet <strong>daně částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Daňové směr</strong> je <strong>spotřební daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset use tax</strong></td>
<td>Stornované součtem <strong>daně částky</strong> z daňových transakcí, které splňují následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Daňové směr</strong> je <strong>spotřební daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>daně</strong>&gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Pro výše uvedené tabulce se předpokládá, že jsou splněna tato kritéria: 
> -   Částka základu daně je částka transakce z **v zúčtovací měně původu** pole.
> -   Částka DPH je částka přechod z **skutečná částka prodejní daně v zúčtovací měně** pole.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurace modelu ER a formát sestavy

Elektronické hlášení (ER) můžete použít ke konfiguraci výkazy a sestavy a export různých formátů elektronických dat bez nutnosti změny kódu X ++. Další informace:

-   [Přehled elektronického výkaznictví](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Požadavky na lokalizaci – vytvoření konfigurace pravidel](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>Countryspecific prostředky pro výkazy DPH
Výkaz DPH pro každou zemi musí splňovat požadavky právních předpisů této země. Existuje předdefinované obecné modely a formáty výkazů DPH pro země uvedené v následující tabulce.


| Země        | Doplňkové informace                                                          |
|----------------|---------------------------------------------------------------------------------|
| Rakousko        |  [Podrobnosti výkazu DPH pro Rakousko](emea-aut-vat-statement-details.md)         |
| Belgie        |                                                                                 |
| Česká republika |  [Podrobnosti výkazu DPH pro Českou republiku](emea-cze-vat-statement-details.md)   |
| Estonsko        |  [Podrobnosti výkazu DPH pro Estonsko](emea-est-vat-statement-details.md) |
| Finsko        |                                                                                 |
| Německo        |                                                                                 |
| Itálie          | [Podrobnosti výkazu DPH pro Itálii](emea-ita-vat-statements-details.md)            |
| Lotyšsko         | [Podrobnosti výkazu DPH pro Lotyšsko](emea-lva-vat-statement-details.md)           |
| Litva      | [Podrobnosti výkazu DPH pro Litvu](emea-ltu-vat-statement-details.md)         |
| Nizozemsko    |                                                                                 |
| Švédsko         |                                                                                 |




