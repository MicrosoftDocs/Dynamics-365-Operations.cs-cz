---
title: Záporné storno
description: Záporné storno je praxe používání záporných čísel ke stornování původních účetních položek deníku.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 1219713
ms.search.region: Czech Republic, Germany, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ee8f3f5c850ad0ae519c83a689d12b9a1471712
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407620"
---
# <a name="storno-accounting"></a>Záporné storno

[!include [banner](../includes/banner.md)]

Záporné storno je praxe používání záporných čísel ke stornování původních účetních položek deníku.

*Záporné storno* je praxe používání záporných debetních nebo kreditních částek ke stornování původních účetních položek deníku. Vzhledem k tomu, že účetní obvykle zapisují položky záporného storna červeně, tento účetní standard se také označuje jako *červené storno*. Pomocí záporného storna můžete zrušit dokument s nesprávnými částkami, po zrušení byste však vždy měli zadat správnou částku dokumentu.

## <a name="example"></a>Příklad
Účetní zaúčtuje fakturu dodavatele s částkou 120 USD. Během procesu platby se zjistí, že účetní omylem zadal 120 USD, namísto 102 USD. Účetní teď musí vytvořit storno původního dokumentu a následně vytvořit správnou fakturu na 102 USD. Další informace naleznete v tématu  [Přehled faktur dodavatele](../accounts-payable/vendor-invoices-overview.md). Následující tabulka uvádí obecné záznamy pro Storno.

| **ID dokumentu** | **Účet** | **Má Dáti** | **Dal** | **Poznámka**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Faktura0001     | Nákupní vratka   | 120       |            | Původní faktura (nesprávná) |
| Faktura0001     | Účet dodavatele  |           | 120        | Původní faktura (nesprávná) |
|                 |             |           |            |                              |
| Storno0001      | Nákupní vratka   | -120     |            | Storno                       |
| Storno0001      | Účet dodavatele  |           | -120      | Storno                       |
|                 |             |           |            |                              |
| Faktura0002     | Nákupní vratka   | 102       |            | Správná faktura              |
| Faktura0002     | Účet dodavatele  |           | 102        | Správná faktura              |

V tomto příkladu výpis zůstatku ukazuje následující.

| Účet    | Má Dáti | Kreditní | Rozvaha |
|------------|-------|--------|---------|
| Nákupní vratka  | 102   | 0      | 102     |
| Účet dodavatele | 0     | 102    | -102    |

## <a name="differences-between-storno-and-reverse-entries"></a>Rozdíly mezi stornem a opačnými zápisy
Existují dva způsoby opravy účetních položek – opačný zápis a storno. Při použití opačného zápisu je vytvořena kopie původního obecného zápisu se zpětným zápisem debetního a kreditního účtu, přičemž u částek bude stejné znaménko. Používáte-li storno, systém vytvoří kopii původní obecné položky, ale částky budou zapsány se záporným znaménkem. Následující tabulka uvádí obecné záznamy pro Storno.

| **ID dokumentu** | **Účet** | **Má Dáti** | **Dal** | **Poznámka**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Faktura0001     | Nákupní vratka   | 120       |            | Původní faktura (nesprávná) |
| Faktura0001     | Účet dodavatele  |           | 120        | Původní faktura (nesprávná) |
|                 |             |           |            |                              |
| Reverse0001     | Nákupní vratka   |           | 120        | Stornovat                      |
| Reverse0001     | Účet dodavatele  | 120       |            | Stornovat                      |
|                 |             |           |            |                              |
| Faktura0002     | Nákupní vratka   | 102       |            | Správná faktura              |
| Faktura0002     | Účet dodavatele  |           | 102        | Správná faktura              |

V tomto příkladu výpis zůstatku ukazuje následující.

| Účet    | Má Dáti | Kreditní | Rozvaha |
|------------|-------|--------|---------|
| Nákupní vratka  | 222   | 120    | 102     |
| Účet dodavatele | 120   | 222    | -102    |

Všimněte si, že jsou zůstatky záporného účtování a storna stejné. Existuje rozdíl mezi debetním a kreditním obratem, protože opačný zápis způsobuje redundantní obrat debetu a kreditu. Opačný zápis se používá v zemích/oblastech, kde se obrat používá jen zřídka. Jiné země nebo oblasti používají záporné storno.

## <a name="partial-storno"></a>Částečná storno
*Částečné storno* je účetní praxe používání záporných debetních nebo kreditních částek ke stornování původních účetních položek deníku. Některé země nebo oblasti umožňují používání částečného storna. Účetní například zaúčtuje fakturu dodavatele s částkou 120 USD. Během procesu platby je zjištěno, že účetní omylem zadal nesprávnou číselnou řadu. Původní faktura na 102 USD obsahovala chybu v číselné řadě.Pomocí částečného storna by měl účetní vytvořit storno na 18 USD. Následující tabulka uvádí obecné záznamy pro částečné storno.

| **ID dokumentu** | **Účet** | **Má Dáti** | **Kreditní** | **Poznámka**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Faktura0001     | Nákupní vratka   | 120       |            | Původní faktura (nesprávná) |
| Faktura0001     | Účet dodavatele  |           | 120        | Původní faktura (nesprávná) |
|                 |             |           |            |                              |
| Storno0001      | Nákupní vratka   | 18. \-      |            | Částečná storno               |
| Storno0001      | Účet dodavatele  |           | 18. \-       | Částečná storno               |

V tomto příkladu výpis zůstatku ukazuje následující.

| Účet    | Má Dáti | Kreditní | Rozvaha |
|------------|-------|--------|---------|
| Nákupní vratka  | 102   | 0      | 102     |
| Účet dodavatele | 0     | 102    | -102    |

Částečné storno může vytvořit problém ve formuláři Tisk předlohy.Pokud existuje rozdíl mezi datem původního dokladu a datem storna, může být obtížné získat přesnou částku měny. V důsledku toho je částečné storno povoleno pouze pro určité dokumenty. Dynamics 365 Finance poskytuje funkci částečného storna pro dokumenty a země/oblasti, kde je povoleno.

## <a name="how-to-enter-stornoon-journal-lines"></a>Jak zadat storno na řádcích deníku
Zadejte částku Má dáti nebo Dal se záporným znaménkem v řádku deníku k vytvoření položky storna. Pole **Oprava** je nastaveno během procesu zaúčtování. 

## <a name="how-storno-is-displayed"></a>Zobrazení storna
Finance zpracovává záporné částky deníku speciálním způsobem. Položka hlavního deníku, transakce odběratele, transakce dodavatele a jiné transakce poskytují funkce storna, jak je uvedeno níže.

<table>
<thead>
<tr class="row-1">
<th class="column-1" rowspan="2">Uživatelský vstup na řádku deníku</th>
<th class="column-2" colspan="2">Princip úložiště</th>
<th class="column-4" colspan="2">Pravidlo zobrazení</th>
<th class="column-6" colspan="3">Dopad na sestavu výpisu</th>
</tr>
<tr class="row-1">
<th class="column-2">Pole Oprava</th>
<th class="column-3">Pole Částka</th>
<th class="column-4">Částka v měně transakce</th>
<th class="column-5">Množství</th>
<th class="column-6">Sloupec Má dáti</th>
<th class="column-7">Sloupec Dal</th>
<th class="column-8">Sloupec Zůstatek</th>
</tr>
</thead>
<tbody>
<tr class="row-2">
<td class="column-1"> Má Dáti</td>
<td class="column-2">Žádný</td>
<td class="column-3">0. &gt;</td>
<td class="column-4" align="right">Množství</td>
<td class="column-5" align="right">Množství</td>
<td class="column-6">Zvýšení</td>
<td class="column-7"></td>
<td class="column-8">Zvýšení</td>
</tr>
<tr class="row-3">
<td class="column-1"> Kreditní</td>
<td class="column-2">Žádný</td>
<td class="column-3">0. &lt;</td>
<td class="column-4" align="right">-Částka</td>
<td class="column-5" align="right">Množství</td>
<td class="column-6"></td>
<td class="column-7">Zvýšení</td>
<td class="column-8">Snížení</td>
</tr>
<tr class="row-4">
<td class="column-1">-Má Dáti</td>
<td class="column-2">Ano</td>
<td class="column-3">0. &gt;</td>
<td class="column-4" align="right">+Částka</td>
<td class="column-5" align="right">-Částka</td>
<td class="column-6">Snížení</td>
<td class="column-7"></td>
<td class="column-8">Zvýšení</td>
</tr>
<tr class="row-5">
<td class="column-1">-Kredit</td>
<td class="column-2">Ano</td>
<td class="column-3">0. &lt;</td>
<td class="column-4" align="right">-Částka</td>
<td class="column-5" align="right">-Částka</td>
<td class="column-6"></td>
<td class="column-7">Snížení</td>
<td class="column-8">Snížení</td>
</tr>
</tbody>
</table>

Můžete upravit zobrazení storna pro formuláře, tabulky, sloupce a pole. Například můžete vypnout zobrazení znaménka nebo změnit odsazení pro záporné částky. Můžete také použít pole **oprava** se všemi nastaveními zobrazení, pokud má pole **Oprava** zadanou hodnotu "Ano", po které následuje položka Storno.

![Částky storna položky deníku](./media/journal-storno.png)

## <a name="how-documents-create-storno"></a>Jak dokumenty vytvářejí storno
Některé dokumenty vytvářejí transakce zrušení. Následující přecenění cizí měny pro hlavní knihu, závazky a dokumenty pohledávek stornují nerealizovaé zisky a ztráty. Další informace naleznete v tématu [přecenění cizí měny v hlavní knize](../general-ledger/foreign-currency-revaluation-general-ledger.md) nebo [přecenění cizí měny pro závazky a pohledávky](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md). Po vytvoření transakce zrušení budou vytvořeny nové transakce s nerealizovanými zisky a ztrátami. Transakce zrušení jsou vytvořeny také pro zásoby. Další informace naleznete v tématu  [Uzávěrka zásob](../../supply-chain/cost-management/inventory-close.md). Existují dokumenty, které umožňují zrušení dříve zaúčtovaného dokladu. Uživatel může například vytvořit dobropis ke zrušení dříve vytvořené faktury. Dokumenty používají specifické parametry pro vytváření zpětných transakcí nebo transakcí storna. Například přecenění cizí měny vytvoří transakce zpětného zápisu nebo storna na základě parametru opravy hlavní knihy. Dobropis odběratele vytvoří zpětné transakce nebo transakce storna na základě parametru opravy dobropisu závazků.

