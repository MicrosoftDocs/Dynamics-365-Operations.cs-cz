---
title: Účetní profil dodavatele
description: Účetní profil dodavatele řídí zaúčtování transakcí dodavatelů do hlavní knihy
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3f62df7ec5627556561db950d54ff4347d2b4d6
ms.sourcegitcommit: ce84a1faeda6013ef6a90038d811a72f375b604e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2019
ms.locfileid: "1625888"
---
# <a name="vendor-posting-profiles"></a>Účetní profil dodavatele

[!include [banner](../includes/banner.md)]

Účetní profil dodavatele řídí zaúčtování transakcí dodavatelů do hlavní knihy

<a name="vendor-posting-profiles"></a>Účetní profil dodavatele
-----------------------

Účetní profily dodavatelů umožňují přiřazení účtů hlavní knihy a nastavení dokumentů ke všem dodavatelům, skupině dodavatelů nebo jednomu dodavateli. Toto nastavení se použije při vytváření nákupních objednávek, faktur dodavatele a plateb v hotovosti. U některých transakcí je možné vybrat účetní profil, který se odlišuje od účetních profilů nastavených pro transakce na této stránce a má před nimi přednost. Výchozí účetní profil je definován na záložce s náhledem **Hlavní kniha a DPH** na stránce **Parametry závazků**. Výchozí účetní profil je poté následně automaticky zahrnut do záhlaví nových dokumentů, kde jej můžete změnit na jiný účetní profil v případě potřeby.

Můžete také přiřadit definice účtování k typům účtování transakcí na stránce **Definice účtování transakce**. Definice účtování určují zaúčtování transakcí dodavatelů do hlavní knihy místo účetních profilů.

## <a name="creating-a-posting-profile"></a>Vytvoření účetního profilu
### <a name="setup"></a>**Nastavení**

Určete účty hlavní knihy, které jsou použity při zaúčtování transakcí s vybraným účetním profilem. Vyberte kód účtu a je-li to možné, i číslo účtu nebo skupiny vybraného účetního profilu. V procesu zaúčtování bude nejvhodnější účetní profil pro každou transakci nalezen vyhledáním nejspecifičtější kombinace kódu účtu, čísla účtu nebo kombinace skupiny a čísla s následující prioritou.

| Hodnota pole **Kód účtu** | Hodnota pole **Číslo účtu/skupiny**        | Priorita hledání |
|------------------------------|---------------------------------------------|-----------------|
| **Tabulka**                    | Konkrétní účet dodavatele                     | 1               |
| **Seskupit**                    | Skupina dodavatelů, která je přiřazena dodavateli | 2               |
| **Vše**                      | Formulář                                       | 3               |

Pokud chcete, aby všechny transakce dodavatele měly shodný účetní profil, nastavte pouze jeden účetní profil s hodnotou **Vše** v poli **Kód účtu**. Zadejte následující hodnoty pro nastavení účetního profilu.

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
<td>Zadejte kód účetního profilu. Můžete například vytvořit dva účetní profily a získat jeden účet pro rozvahy dodavatele v národní měně a jiný účet pro rozvahy v měně cizí. Jeden účet byste měli nazvat "národní" a druhý "cizí".</td>
</tr>
<tr class="even">
<td><strong>Popis</strong></td>
<td>Zadejte popis účetního profilu.</td>
</tr>
<tr class="odd">
<td><strong>Kód účtu</strong></td>
<td>Zadejte, zda se účetní profil týká specifického dodavatele, skupiny dodavatelů nebo všech dodavatelů:
<ul>
<li><strong>Tabulka</strong> – Účetní profil platí pro jednoho dodavatele. Vyberte účet dodavatele v poli <strong>Číslo účtu/skupiny</strong>.</li>
<li><strong>Skupina</strong> – Účetní profil platí pro skupinu dodavatelů. Vyberte skupinu dodavatelů v poli <strong>Číslo účtu/skupiny</strong>.</li>
<li><strong>Vše</strong> – Účetní profil platí pro všechny dodavatele. Pole <strong>Číslo účtu/skupiny</strong> ponechejte prázdné.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Číslo účtu/skupiny</strong></td>
<td>Pokud vyberete možnost <strong>Tabulka</strong> v poli <strong>Kód účtu</strong>, zvolte číslo účtu dodavatele přiřazeného k účetnímu profilu. Pokud vyberete možnost <strong>Skupina</strong>, zvolte skupinu dodavatelů. Pokud je vybrána možnost <strong>Vše</strong>, ponechte toto pole prázdné.</td>
</tr>
<tr class="odd">
<td><strong>Součtový účet</strong></td>
<td>Vyberte účet hlavní knihy, který se má použít jako součtový účet pro dodavatele, se kterým účetní profil souvisí. Bude označen parametr <strong>Nepovolit ruční zadávání</strong> pro tento hlavní účet. Pokud následně tento účet odeberete z účetního profilu, ověřte nastavení možnost i<strong>Nepovolit ruční zadávání</strong> na stránce <strong>Hlavní účty</strong>. 
<p><strong>Poznámka:</strong> Je-li na stránce <strong>Parametry hlavní knihy</strong> vybrána možnost <strong>Použít definice účtování</strong>, použije se místo souhrnného účtu definici účtování transakce pro faktury dodavatele.</p>
</td>
</tr>
<tr class="even">
<td><strong>Účet vyrovnání</strong></td>
<td>Vyberte účet hlavní knihy likvidity použitý pro prognózy cash-flow. Toto pole je k dispozici, pouze když je povolena prognóza cashflow.</td>
</tr>
<tr class="odd">
<td><strong>Zálohy DPH</strong></td>
<td>Vyberte účet pro zálohy na platby DPH.
<p><strong>Poznámka:</strong> Účetní profil používaný při označení platby jako zálohy je vybrán v poli <strong>Účetní profil</strong> s polem <strong>Zálohový doklad deníku</strong> v oblasti <strong>Hlavní kniha a DPH</strong> na stránce <strong>Parametry závazků</strong>.</p>
</td>
</tr>
<tr class="even">
<td><strong>Doručení</strong></td>
<td>Vyberte účet hlavní knihy, do kterého jsou zaúčtovány informace o neschválených fakturách dodavatele. Informace jsou zaznamenány do deníku registrů faktur. Uživatel například zadá zcela základní informace o fakturách dodavatele, když byly přijaty do registru faktur. Když je registr faktur zaúčtován, transakce jsou zaúčtovány na účet, který je zadán zde, a do pole <strong>Protiúčet</strong>. Když jsou faktury schváleny, dluh je přenesen z účtu doručení do souhrnného účtu dodavatele.</td>
</tr>
<tr class="odd">
<td><strong>Protiúčet</strong></td>
<td>Vyberte účet hlavní knihy, který je používán pro vyrovnání neschválených faktur dodavatele, které jsou aktualizovány pomocí registru faktur. Protiúčet plní funkci protiúčtu pro transakce, které jsou zaúčtovány na účty doručení. Proto bude účet obsahovat nákupy dodavatele, které dosud nebyly schváleny.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tabulka omezení**

Pro transakce s vybraným účetním profilem určete, zda transakce budou vyrovnány automaticky, zda bude vypočten úrok a zda budou vydány upomínky. Můžete také vybrat účet, který se použije při uzavření transakcí s vybraným účetním profilem.

Zadání následujících hodnot pro nastavení účetního profilu

| Pole          | Popis                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vyrovnání** | Tuto možnost vyberte, chcete-li povolit automatické vyrovnání transakcí, které mají tento účetní profil. Není-li toto políčko zaškrtnuto, je nutné vyrovnat transakce ručně s použitím stránky **Vyrovnat otevřené transakce**. |
| Tlačítko **Zrušit**     | Tuto možnost vyberte, chcete-li mít možnost zrušit transakce, které mají tento účetní profil.                                                                                                               |
| **Zavřít**      | Vyberte jiný účetní profil, na který se chcete přepnout při uzavření transakcí s tímto účetním profilem. Transakce je považována za uzavřenou, když byla plně vyrovnána.                                       |
