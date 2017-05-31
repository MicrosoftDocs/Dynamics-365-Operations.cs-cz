---
title: "Účetní profil dodavatele"
description: "Účetní profil dodavatele řídí zaúčtování transakcí dodavatelů do hlavní knihy"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2dbb8874323631a9bddb226834adf87d014c1c2f
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-posting-profiles"></a>Účetní profil dodavatele

[!include[banner](../includes/banner.md)]


Účetní profil dodavatele řídí zaúčtování transakcí dodavatelů do hlavní knihy

<a name="vendor-posting-profiles"></a>Účetní profil dodavatele
-----------------------

Účetní profily dodavatelů umožňují přiřazení účtů hlavní knihy a nastavení dokumentů ke všem dodavatelům, skupině dodavatelů nebo jednomu dodavateli. Toto nastavení se použije při vytváření nákupních objednávek, faktur dodavatele a plateb v hotovosti. U některých transakcí je možné vybrat účetní profil, který se odlišuje od účetních profilů nastavených pro transakce na této stránce a má před nimi přednost. Výchozí účetní profil je definován v pevné záložce Hlavní kniha a DPH na straně Parametry závazků. Výchozí účetní profil je poté následně automaticky zahrnut do záhlaví nových dokumentů, kde jej můžete změnit na jiný účetní profil v případě potřeby.

Můžete také přiřadit definice účtování k typům účtování transakcí na stránce Definice účtování transakce. Definice účtování určují zaúčtování transakcí dodavatelů do hlavní knihy místo účetních profilů.

## <a name="creating-a-posting-profile"></a>Vytvoření účetního profilu
### <a name="setup"></a>**Nastavení**

Určete účty hlavní knihy, které jsou použity při zaúčtování transakcí s vybraným účetním profilem. Vyberte kód účtu a je-li to možné, i číslo účtu nebo skupiny vybraného účetního profilu. V procesu zaúčtování bude nejvhodnější účetní profil pro každou transakci nalezen vyhledáním nejspecifičtější kombinace kódu účtu, čísla účtu nebo kombinace skupiny a čísla s následující prioritou:

| Hodnota pole **Kód účtu** | Hodnota pole **Číslo účtu/skupiny**        | Priorita hledání |
|------------------------------|---------------------------------------------|-----------------|
| **Tabulka**                    | Konkrétní účet dodavatele                     | 1               |
| **Skupina**                    | skupina dodavatelů, která je přiřazena dodavateli | 2               |
| **Vše**                      | Prázdné                                       | 3               |

Pokud chcete, aby všechny transakce dodavatele měly shodný účetní profil, nastavte pouze jeden účetní profil s hodnotou Vše v poli Kód účtu. Zadejte následující hodnoty pro nastavení účetního profilu:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
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
<li><strong>Tabulka</strong> – Účetní profil platí pro jednoho dodavatele. Vyberte účet dodavatele v poli Číslo účtu/skupiny.</li>
<li><strong>Skupina</strong> – Účetní profil platí pro skupinu dodavatelů. Vyberte skupinu dodavatelů v poli Číslo účtu/skupiny.</li>
<li><strong>Vše</strong> – Účetní profil platí pro všechny dodavatele. Pole Číslo účtu/skupiny ponechejte prázdné.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Číslo účtu/skupiny</strong></td>
<td>Pokud vyberete možnost Tabulka v poli Kód účtu, zvolte číslo účtu dodavatele přiřazeného k účetnímu profilu. Pokud vyberete možnost Skupina, zvolte skupinu dodavatelů. Pokud je vybrána možnost Vše, ponechte toto pole prázdné.</td>
</tr>
<tr class="odd">
<td><strong>Součtový účet</strong></td>
<td>Vyberte účet hlavní knihy, který se má použít jako součtový účet pro dodavatele, se kterým účetní profil souvisí.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Poznámka:</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Je-li na stránce Parametry hlavní knihy vybráno přepínání definic účtování, použije se místo souhrnného účtu definici účtování transakce pro faktury dodavatele.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Účet vyrovnání</strong></td>
<td>Vyberte účet hlavní knihy likvidity použitý pro prognózy cash-flow. Toto pole je k dispozici, pouze když je povolena prognóza cashflow.</td>
</tr>
<tr class="odd">
<td><strong>Zálohy DPH</strong></td>
<td>Vyberte účet pro zálohy na platby DPH.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Poznámka:</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Účetní profil používaný při označení platby jako zálohy vybrán v poli Účetní profil se zálohovým dokladem deníku v hlavní knize a oblasti DPH na stránce Parametry závazků.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Doručení</strong></td>
<td>Vyberte účet hlavní knihy, do kterého jsou zaúčtovány informace o neschválených fakturách dodavatele. Informace jsou zaznamenány do deníku registrů faktur. Uživatel například zadá zcela základní informace o fakturách dodavatele, když byly přijaty do registru faktur. Když je registr faktur zaúčtován, transakce jsou zaúčtovány na účet, který je zadán zde, a do pole Protiúčet. Když jsou faktury schváleny, dluh je přenesen z účtu doručení do souhrnného účtu dodavatele.</td>
</tr>
<tr class="odd">
<td><strong>Protiúčet</strong></td>
<td>Vyberte účet hlavní knihy, který je používán pro vyrovnání neschválených faktur dodavatele, které jsou aktualizovány pomocí registru faktur. Protiúčet plní funkci protiúčtu pro transakce, které jsou zaúčtovány na účty doručení. Proto bude účet obsahovat nákupy dodavatele, které dosud nebyly schváleny.</td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a>**Tabulka omezení**

Pro transakce s vybraným účetním profilem určete, zda transakce budou vyrovnány automaticky, zda bude vypočten úrok a zda budou vydány upomínky. Můžete také vybrat účet, který se použije při uzavření transakcí s vybraným účetním profilem.

Zadejte následující hodnoty pro nastavení účetního profilu:

| Pole          | Popis                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vyrovnání** | Tuto možnost vyberte, chcete-li povolit automatické vyrovnání transakcí, které mají tento účetní profil. Není-li toto políčko zaškrtnuto, je nutné vyrovnat transakce ručně s použitím stránky Vyrovnat otevřené transakce. |
| Tlačítko **Zrušit**     | Tuto možnost vyberte, chcete-li mít možnost zrušit transakce, které mají tento účetní profil.                                                                                                               |
| **Zavřít**      | Vyberte jiný účetní profil, na který se chcete přepnout při uzavření transakcí s tímto účetním profilem. Transakce je považována za uzavřenou, když byla plně vyrovnána.                                       |






