---
title: "Vykazování DPH pro Evropu"
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

# <a name="vat-reporting-for-europe"></a>Vykazování DPH pro Evropu

Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země.

Toto téma obsahuje obecný přístup k nastavení a generování výkazu DPH. Tento přístup je společný pro uživatele v právnických osobách v těchto zemích a oblastech:

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
Výkaz DPH je založený na částkách daňových transakcí. Proces generování výkazu DPH je součástí procesu platby DPH, který je implementován pomocí funkce vypořádání a zaúčtování DPH. Tato funkce se používá k výpočtu DPH splatné pro dané období. Výpočet vyrovnání zahrnuje zaúčtovanou DPH pro vybrané období vyrovnání daňových transakcí. Postup pro výpočet dat pro výkaz DPH je založen na vztahu mezi kódy DPH a kódy vykazování DPH, kde kódy vykazování daně odpovídají polím s výkazy DPH. Pro každý kód DPH by měly být nastaveny kódy vykazování DPH pro každý typ transakce, například zdanitelné prodeje zdanitelné nákupy, zdanitelný import. Tento typ transakcí je popsán v části [Kódy DPH pro vykazování DPH](#Sales tax codes for VAT reporting) dále v tomto tématu.

Pro každý kód vykazování by mělo být určeno konkrétní rozložení sestavy. Ve stejnou dobu jsou kódy DPH propojeny s konkrétním finančním úřadem prostřednictvím období vyrovnání DPH. Pro každý finanční úřad pro vykazování DPH by mělo být určeno konkrétní rozložení sestavy. Tedy pouze kódy vykazování DPH se stejným rozložením sestavy, která je nastavena pro finanční úřad k odvedení DPH v období vyrovnání DPH pro kód DPH lze vybrat v nastavení sestavy kódu DPH. Transakce DPH generované při účtování objednávky nebo deníku obsahují kód DPH, zdroj DPH, směr DPH a částky transakcí (částka základu daně a výše daně v zúčtovací měně, měně DPH a měně transakce). V závislosti na kombinaci atributů transakce DPH, částky transakce tvoří celkové částky určené pro kódy vykazování DPH určené pro kódy DPH. Následující obrázek znázorňuje vztah mezi daty.

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>Nastavení výkazu DPH
Chcete-li generovat výkazy DPH, je nutné vytvořit následující nastavení:

### <a name="sales-tax-authorities-for-vat-reporting"></a>Nastavení daňových úřadů pro vykazování DPH

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Dříve než můžete vytvořit kódy vykazování DPH, je nutné vybrat správnou sestavu rozložení pro finanční úřad. Na stránce **Finanční úřady** v části **Obecné** vyberte **Rozložení sestavy**. Toto rozložení bude použito, když nastavujete kódy vykazování DPH.

### <a name="sales-tax-reporting-codes"></a>Kódy vykazování DPH

Kódy vykazování DPH jsou pole kódy DPH výkazu nebo značky názvy ve formátu XML. Tyto kódy se používají k agregaci a přípravě částky v sestavě. Při konfiguraci elektronického formátu vykazování ve výkazu DPH budou použity názvy částek výsledku. Můžete vytvářet a udržovat kódy vykazování DPH na stránce **Kódy vykazování DPH**. Každý kód je nutné přiřadit rozložení sestavy. Jakmile vytvoříte kódy vykazování DPH, můžete použít kódy v části **Nastavení sestavy** na stránce **Kódy DPH**. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Kódy vykazování DPH

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).--> Základní částky a daňové částky prodejní daně mohou být agregovány v kódech vykazování ve výkazu DPH (značky XML nebo deklarace polí). Můžete to nastavit přiřazením vykazování kódů různých typů transakcí pro kódy DPH na DPH **kódy DPH** stránky. Následující tabulka popisuje typy transakcí v nastavení sestavy pro kódy DPH. Výpočet zahrnuje transakce pro všechny typy zdrojů s výjimkou DPH.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Typ transakce</strong></td>
<td><strong>Popis transakcí a částek pro výpočet v typu transakce</strong></td>
</tr>
<tr class="even">
<td><strong>Zdanitelné prodeje</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období/</li>
<li>Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Prodej bez daně</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DPH na výstupu</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Zdanitelný prodejní dobropis</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Prodejní dobropis osvobozený od daně</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>DPH na prodejním dobropisu</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Zdanitelné nákupy</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Nákup bez daně</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DPH na vstupu</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Zdanitelný nákupní dobropis</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Nákupní dobropis osvobozený od daně</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>DPH na nákupním dobropisu</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Zdanitelný import</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Směr daně</strong> je <strong>Použít daň</strong></li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Protiúčet zdanitelného dovozu</strong></td>
<td>Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Směr daně</strong> je <strong>Použít daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Zdanitelný dovozní dobropis</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
e<li><strong>Směr daně</strong> je <strong>Použít daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Protiúčet zdanitelných dovozních dobropisů</strong></td>
<td>Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li>Směr daně je <strong>Importní DPH</strong>.</li>
d<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Importní DPH</strong></td>
<td>Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Směr daně</strong> je <strong>Použít daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Zapsat importní DPH na protiúčet</strong></td>
<td>Stornovaný součet <strong>Částek daně</strong> daňových transakcí, který splňuje následující podmínky:
<ul>
<li>Datum transakce je ve vybraném období.</li>
<li><strong>Směr daně</strong> je <strong>Použít daň</strong>.</li>
<li>Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Pro výše uvedenou tabulku se předpokládá, že jsou splněna tato kritéria: 
> -   Částka základu daně je částka transakce z pole **Původ v zúčtovací měně**.
> -   Částka základu daně je částka transakce z pole **Částka daně skutečných prodejů**.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurace modelu ER a formátu výkazu

Elektronické hlášení (ER) můžete použít ke konfiguraci výkazů a sestav a k exportu různých formátů elektronických dat bez nutnosti změny kódu X ++. Další informace:

-   [Přehled elektronického výkaznictví](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Požadavky na lokalizaci – vytvoření konfigurace GER](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>Prostředky pro výkazy DPH specifické podle zemí
Výkaz DPH pro každou zemi musí splňovat požadavky právních předpisů této země. Existují předdefinované obecné modely a formáty výkazů DPH pro země uvedené v následující tabulce.


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



