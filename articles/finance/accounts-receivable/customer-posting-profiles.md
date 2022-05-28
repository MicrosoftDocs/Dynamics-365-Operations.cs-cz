---
title: Účetní profily odběratele
description: Toto téma popisuje účetní profily odběratele, které účtování řídí účtování transakcí odběratelů do hlavní knihy.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ed5ab24e37c75222080bd242aa72a39ecb476bf
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734625"
---
# <a name="customer-posting-profiles"></a>Účetní profily odběratele

[!include [banner](../includes/banner.md)]

Toto téma popisuje účetní profily odběratele, které účtování řídí účtování transakcí odběratelů do hlavní knihy.

## <a name="customer-posting-profiles"></a>Účetní profily odběratele

Účetní profily odběratelů umožňují přiřazení účtů hlavní knihy a nastavení dokumentů ke všem odběratelům, skupině odběratelů nebo jednomu odběrateli. Toto nastavení se použije při vytváření faktur prodejních objednávek, volných faktur, faktur projektu, platebních deníků, upomínek a oznámení úroků. 

Výchozí účetní profil je definován v kartě **Hlavní kniha a DPH** na straně **Parametry pohledávek**. Poté je automaticky zahrnut do záhlaví nových dokumentů. Zde jej můžete změnit, pokud je vyžadován jiný účetní profil. 

Organizace, které přijímají platby předem od zákazníků, často konfigurují druhý účetní profil pro platby předem a propojí ho v parametrech jako výchozí profil pro platby předem. Další informace naleznete v tématu [Platby odběratelů předem](customer-prepayments.md).

Můžete také přiřadit definice účtování k typům účtování transakcí na stránce **Definice účtování transakce**. Definice účtování se používají místo účetních profilů k řízení účtování transakcí odběratelů do hlavní knihy. Další informace získáte v části [Definice účtování](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Vytvoření účetního profilu
Určete účty hlavní knihy, které jsou použity při zaúčtování transakcí s vybraným účetním profilem. Vyberte kód účtu a je-li to možné, i číslo účtu nebo skupiny vybraného účetního profilu. V procesu zaúčtování bude nejvhodnější účetní profil pro každou transakci nalezen vyhledáním nejspecifičtější kombinace kódu účtu, čísla účtu nebo kombinace skupiny a čísla s následující prioritou:

| Hodnota pole Kód účtu | Hodnota pole Číslo účtu/skupiny                | Priorita hledání |
|--------------------------|-------------------------------------------------|-----------------|
| Tabulka                    | Specifický účet odběratele                       | 1               |
| Seskupit                    | Skupina odběratelů, která je přiřazena odběrateli | 2               |
| Vše                      | Prázdné                                           | 3               |

Pokud chcete, aby všechny transakce odběratele měly shodný účetní profil, nastavte pouze jeden účetní profil s hodnotou **Vše** v poli **Kód účtu**. Zadejte následující hodnoty pro nastavení účetního profilu.

<table>
<thead>
<tr>
<th>Pole</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Účetní profil</td>
<td>Zadejte kód účetního profilu. Můžete například vytvořit dva účetní profily a získat jeden účet pro rozvahy odběratele v národní měně a jiný účet pro rozvahy v měně cizí. Jeden účet byste měli nazvat "národní" a druhý "cizí".</td>
</tr>
<tr>
<td>Popis</td>
<td>Zadejte popis účetního profilu. Používá se jen k lepší identifikace účetního profilu při jeho zobrazení na této stránce.</td>
</tr>
<tr>
<td>Kód účtu</td>
<td>Uveďte, zda účetní profil platí pro jednotlivého odběratele, skupinu odběratelů nebo všechny odběratele:
<ul>
<li><b>Tabulka</b> – Účetní profil platí pro jednoho odběratele. Vyberte účet odběratele v poli <b>Číslo účtu/skupiny</b>.</li>
<li><b>Skupina</b> – Účetní profil platí pro skupinu odběratelů. Vyberte skupinu odběratelů v poli <b>Číslo účtu/skupiny</b>.</li>
<li><b>Vše</b> – Účetní profil platí pro všechny odběratele. Pole <b>Číslo účtu/skupiny</b> ponechejte prázdné.</li>
</ul>
</td>
</tr>
<tr>
<td>Číslo účtu/skupiny</td>
<td>Pokud vyberete možnost <b>Tabulka</b> v poli <b>Kód účtu</b>, zvolte číslo účtu odběratele přiřazeného k účetnímu profilu. Pokud je vybrána možnost <b>Skupina</b>, vyberte skupinu odběratelů. Pokud je vybrána možnost <b>Vše</b>, ponechte toto pole prázdné.</td>
</tr>
<tr>
<td>Součtový účet</td>
<td>Vyberte účet hlavní knihy, který se má použít jako obchodní účet pohledávek odběratelů přiřazených k danému účetnímu profilu. Tento účet je účtem pro typ účtování <b>Rovnováha odběratele</b>.</td>
</tr>
<tr>
<td>Účet likvidity pro platby</td>
<td>Vyberte účet hlavní knihy likvidity použitý pro prognózy cash-flow. Toto pole se zobrazí pouze v případě, že jsou prognózy cashflow povoleny.</td>
</tr>
<tr>
<td>Zálohy DPH</td>
<td><p>Vyberte účet pro zálohové platby daně z prodeje.</p>
<p><strong>Poznámka:</strong> Na stránce <b>Parametry pohledávek</b> určete účetní profil, který má být použit při označení platby jako zálohy.</p>
</td>
</tr>
<tr>
<td>Závazky pro účet slevy</td>
<td>Vyberte účet hlavní knihy pro závazky slevy.</td>
</tr>
<tr>
<td>Posloupnost upomínek</td>
<td>Vyberte identifikátor posloupnosti upomínek, který má být použit pro odběratele, kterým je přiřazen účetní profil.</td>
</tr>
<tr>
<td>Kód úroku</td>
<td>Vyberte kód úroku, který má být použit pro výpočet úroku pro odběratele, kterým je přiřazen účetní profil.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Příklady účtování

Následující tabulka ukazuje příklady výchozích typů účtování s ukázkovými hlavními účty a popisy. Sloupec **Má dáti / dal** označuje, zda lze účtovat transakce obvykle Má dáti nebo Dal nebo v některých případech obojí. Sloupec **Clearingový účet** označuje, že typ účtování je clearingový účet. To znamená, že částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce. 

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Má dáti/Dal | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Zůstatek odběratele | 130100 | Obchod s pohledávkou | Materiál | Oboje | Ne | Zadejte účet do pole **Součtový účet**.|
| Žádné | 110110 | Bankovní účet | Materiál | Oboje | Ne | Zadejte hlavní účet do pole **Účet likvidity pro platby**. Tento účet se nepoužívá k účtování. Používá se pouze pro předpovídání peněžních toků. |
| Zálohy DPH | 202900 | Vyúčtování DPH | Pasiva | Oboje | Ano | Vyberte účet pro zálohové platby daně z prodeje. |
| Závazky pro účet slevy | 250600 | Odložené výnosy a slevy | Pasiva | Oboje | Ano | Vyberte účet hlavní knihy pro závazky slev.|     

### <a name="table-restrictions"></a>Tabulka omezení

Pro transakce s vybraným účetním profilem určete, zda transakce budou vyrovnány automaticky, zda bude vypočten úrok a zda budou vydány upomínky. Můžete také vybrat účet, který se použije při uzavření transakcí s vybraným účetním profilem.

Zadejte následující hodnoty pro nastavení účetního profilu:

| Pole                 | Popis                                           |
|-----------------------|-------------------------------------------------------|
| Vyrovnání        | Tento přepínač vyberte, chcete-li povolit automatické vyrovnání transakcí, které mají tento účetní profil. Není-li tento přepínač zaškrtnutý, je nutné vyrovnat transakce ručně s použitím stránky **Vyrovnat otevřené transakce** nebo **Zadat platby odběratele**. |
| Zájmy          | Tento přepínač vyberte, pokud by měl být úrok vypočítán z neuhrazených zůstatků pro účty odběratele s tímto profilem. Pokud není tento přepínač zaškrtnut, úrok se u těchto odběratelů nevypočítá.                                           |
| Upomínka | Tento přepínač vyberte, pokud by měly být upomínky generovány pro účty odběratele s tímto profilem. Pokud není tento přepínač zaškrtnut, upomínky nebudou u těchto odběratelů generovány.                                                 |
| Zavřít             | Vyberte jiný účetní profil, na který se chcete přepnout při uzavření transakcí s tímto účetním profilem. Transakce je považována za uzavřenou, když byla plně vyrovnána.             |



Další informace naleznete v tématu [Přehled plateb odběratele](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
