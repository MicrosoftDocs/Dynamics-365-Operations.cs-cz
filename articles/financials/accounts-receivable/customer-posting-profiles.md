---
title: Účetní profily odběratele
description: Účetní profily odběratele řídí zaúčtování transakcí odběratelů do hlavní knihy
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 956dca24c2cfa7e22d718ff84b338bc4ba030394
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "322345"
---
# <a name="customer-posting-profiles"></a>Účetní profily odběratele

[!include [banner](../includes/banner.md)]

Účetní profily odběratele řídí zaúčtování transakcí odběratelů do hlavní knihy

<a name="customer-posting-profiles"></a>Účetní profily odběratele
-------------------------

Účetní profily odběratelů umožňují přiřazení účtů hlavní knihy a nastavení dokumentů ke všem odběratelům, skupině odběratelů nebo jednomu odběrateli. Toto nastavení se použije při vytváření prodejních objednávek, volných faktur, hotovostních plateb, upomínek a oznámení úroků. U některých transakcí je možné vybrat účetní profil, který se odlišuje od účetních profilů nastavených pro transakce na této stránce a má před nimi přednost. 

Výchozí účetní profil je definován v pevné záložce Hlavní kniha a DPH na straně Parametry pohledávek. Výchozí účetní profil je poté následně automaticky zahrnut do záhlaví nových dokumentů, kde jej můžete změnit na jiný účetní profil v případě potřeby.

Můžete také přiřadit definice účtování k typům účtování transakcí na stránce Definice účtování transakce. Definice účtování řídí účtování transakcí odběratelů do hlavní knihy místo účetních profilů.

## <a name="creating-a-posting-profile"></a>Vytvoření účetního profilu
Určete účty hlavní knihy, které jsou použity při zaúčtování transakcí s vybraným účetním profilem. Vyberte kód účtu a je-li to možné, i číslo účtu nebo skupiny vybraného účetního profilu. V procesu zaúčtování bude nejvhodnější účetní profil pro každou transakci nalezen vyhledáním nejspecifičtější kombinace kódu účtu, čísla účtu nebo kombinace skupiny a čísla s následující prioritou:

| Hodnota pole **Kód účtu** | Hodnota pole **Číslo účtu/skupiny**            | Priorita hledání |
|------------------------------|-------------------------------------------------|-----------------|
| **Tabulka**                    | Specifický účet odběratele                       | 1               |
| **Skupina**                    | Skupina odběratelů, která je přiřazena odběrateli | 2               |
| **Vše**                      | Prázdné                                           | 3               |

Pokud chcete, aby všechny transakce odběratele měly shodný účetní profil, nastavte pouze jeden účetní profil s hodnotou Vše v poli Kód účtu. Zadejte následující hodnoty pro nastavení účetního profilu:

<table>
<thead>
<tr class="header">
<th>Pole</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Účetní profil</strong></td>
<td>Zadejte kód účetního profilu. Můžete například vytvořit dva účetní profily a získat jeden účet pro rozvahy odběratele v národní měně a jiný účet pro rozvahy v měně cizí. Jeden účet byste měli nazvat "národní" a druhý "cizí".</td>
</tr>
<tr class="even">
<td><strong>Popis</strong></td>
<td>Zadejte popis účetního profilu. Používá se jen k lepší identifikace účetního profilu při jeho zobrazení na této stránce.</td>
</tr>
<tr class="odd">
<td><strong>Kód účtu</strong></td>
<td>Uveďte, zda účetní profil platí pro jednotlivého odběratele, skupinu odběratelů nebo všechny odběratele:
<ul>
<li><strong>Tabulka</strong> – Účetní profil platí pro jednoho odběratele. Vyberte účet odběratele v poli Číslo účtu/skupiny.</li>
<li><strong>Skupina</strong> – Účetní profil platí pro skupinu odběratelů. Vyberte skupinu odběratelů v poli Číslo účtu/skupiny.</li>
<li><strong>Vše</strong> – Účetní profil platí pro všechny odběratele. Pole Číslo účtu/skupiny ponechejte prázdné.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Číslo účtu/skupiny</strong></td>
<td>Pokud vyberete možnost Tabulka v poli Kód účtu, zvolte číslo účtu odběratele přiřazeného k účetnímu profilu. Pokud je vybrána možnost Skupina, vyberte skupinu odběratelů. Pokud je vybrána možnost Vše, ponechte toto pole prázdné.</td>
</tr>
<tr class="odd">
<td><strong>Součtový účet</strong></td>
<td>Vyberte účet hlavní knihy, který se má použít jako součtový účet odběratele přiřazených k danému účetnímu profilu.</td>
</tr>
<tr class="even">
<td><strong>Účet vyrovnání</strong></td>
<td>Vyberte účet hlavní knihy likvidity použitý pro prognózy cash-flow. Toto pole se zobrazí pouze v případě, že jsou prognózy cashflow povoleny.</td>
</tr>
<tr class="odd">
<td><strong>Zálohy DPH</strong></td>
<td>Vyberte účet pro zálohové platby daně z prodeje.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Poznámka" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Poznámka</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Na stránce Parametry pohledávek určete účetní profil, který má být použit při označení platby jako zálohy.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Závazky pro účet slevy</strong></td>
<td>Vyberte účet hlavní knihy pro závazky slevy.</td>
</tr>
<tr class="odd">
<td><strong>Posloupnost upomínek</strong></td>
<td>Vyberte identifikátor posloupnosti upomínek, který má být použit pro odběratele, kterým je přiřazen účetní profil.</td>
</tr>
<tr class="even">
<td><strong>Kód úroku</strong></td>
<td>Vyberte kód úroku, který má být použit pro výpočet úroku pro odběratele, kterým je přiřazen účetní profil.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Tabulka omezení**

Pro transakce s vybraným účetním profilem určete, zda transakce budou vyrovnány automaticky, zda bude vypočten úrok a zda budou vydány upomínky. Můžete také vybrat účet, který se použije při uzavření transakcí s vybraným účetním profilem.

Zadejte následující hodnoty pro nastavení účetního profilu:

| Pole                 | Popis                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vyrovnání**        | Tento přepínač vyberte, chcete-li povolit automatické vyrovnání transakcí, které mají tento účetní profil. Není-li tento přepínač zaškrtnutý, je nutné vyrovnat transakce ručně s použitím stránky Vyrovnat otevřené transakce nebo Zadat platby odběratele. |
| **Zájmy**          | Tento přepínač vyberte, pokud by měl být úrok vypočítán z neuhrazených zůstatků pro účty odběratele s tímto profilem. Pokud není tento přepínač zaškrtnut, úrok se u těchto odběratelů nevypočítá.                                           |
| **Upomínka** | Tento přepínač vyberte, pokud by měly být upomínky generovány pro účty odběratele s tímto profilem. Pokud není tento přepínač zaškrtnut, upomínky nebudou u těchto odběratelů generovány.                                                 |
| **Zavřít**             | Vyberte jiný účetní profil, na který se chcete přepnout při uzavření transakcí s tímto účetním profilem. Transakce je považována za uzavřenou, když byla plně vyrovnána.                                                                           |



Další informace naleznete v tématu [Přehled plateb odběratele](../cash-bank-management/tasks/customer-payment-overview.md).

