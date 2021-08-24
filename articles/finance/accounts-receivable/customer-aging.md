---
title: Sestava sledování prodlení odběratele
description: Sestava sledování prodlení odběratele zobrazuje zůstatky splatné odběrateli, které jsou seřazeny podle časového intervalu nebo období pro sledování splatnosti.
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c1e3b724c95aa91192c77d5f3b8be4f93f0357f5f2f940c198bc8da47933fa0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769076"
---
# <a name="customer-aging-report"></a>Sestava sledování prodlení odběratele 

Sestava **sledování prodlení odběratele** zobrazuje zůstatky splatné odběrateli, které jsou seřazeny podle časového intervalu nebo období pro sledování splatnosti.

Při generování této sestavy se zobrazují následující výchozí parametry. Parametry sestavy slouží k filtrování dat, která se zobrazí v sestavě. Další informace naleznete v tématu [Nastavení kolekcí](set-up-collections.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Pole</p></th>
<th><p>popis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Účtovací klasifikace</strong></p></td>
<td><p>Vyberte jednu nebo více účtovacích klasifikací, které chcete zahrnout do sestavy.</p>
<div class="alert">

**Poznámka:** Tento ovládací prvek je k dispozici pouze v případě, že je zvolen konfigurační klíč pro <STRONG>veřejný sektor</STRONG>.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Zahrnout transakce bez účtovací klasifikace</strong></p></td>
<td><p>Pokud je toto políčko zaškrtnuto, zobrazí se v sestavě všechny transakce, které nemají přiřazenou účtovací klasifikaci.</p>
<div class="alert">

**Poznámka:** Tento ovládací prvek je k dispozici pouze v případě, že je zvolen konfigurační klíč pro <STRONG>veřejný sektor</STRONG>.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Sledování splatnosti k</strong></p></td>
<td><p>Zadejte datum použité v aktuálním intervalu prodlení.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Zůstatek k</strong></p></td>
<td><p>Zadejte datum, k němuž chcete zobrazit zůstatky odběratelů. Označuje se také jako datum přerušení transakcí.</p></td>
</tr>
<tr class="even">
<td><p><strong>Datum zahájení</strong></p></td>
<td><p>Zadejte datum ležící v intervalu prvního období nebo období pro sledování splatnosti, které má být zahrnuto do sestavy.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Kritéria</strong></p></td>
<td><p>Vyberte typ kalendářního data, na kterém má být sestava založena.</p>
<ul>
<li><p><strong>Datum transakce</strong> – datum zaúčtování transakcí. Může to být například datum faktury, které je základem pro výpočet data splatnosti.</p></li>
<li><p><strong>Datum splatnosti</strong> – datum splatnosti transakcí na základě platebních podmínek.</p></li>
<li><p><strong>Datum dokladu</strong> – uživatelem definované datum dokladu, které je základem pro výpočet data splatnosti.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Definice období pro sledování splatnosti</strong></p></td>
<td><p>Vyberte definici období pro sledování splatnosti. Pokud vyberete definici období pro sledování splatnosti, pole <strong>Interval</strong> se nepoužije.</p>
<p>V tištěné sestavě nelze použít definice období pro sledování splatnosti, které mají více než šest období pro sledování splatnosti.</p>
<div class="alert">

**Poznámka:** Období pro sledování splatnosti můžete nastavit na stránce <STRONG>Definice období pro sledování splatnosti</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Tisk popisu období pro sledování splatnosti</strong></p></td>
<td><p>Chcete-li zahrnout popisy období pro sledování splatnosti do záhlaví sloupce každého období pro sledování splatnosti, zaškrtněte políčko <strong>Ano</strong>. Vyberte <strong>Ne</strong>, pokud chcete sestavu vytisknout bez záhlaví sloupců.</p></td>
</tr>
<tr class="even">
<td><p><strong>Interval</strong></p></td>
<td><p>Zadáním počtu jednotek dnů nebo měsíců v každém období definujte použité období. Chcete-li například zobrazit informace o sledování splatnosti podle týdne, zadejte do tohoto pole hodnotu 7 a vyberte možnost <strong>Den</strong> v poli <strong>Den/měsíc</strong>.</p>
<div class="alert">

**Poznámka:** Informace zadané v tomto poli se použijí jen tehdy, když nebyla vybrána definice období pro sledování splatnosti. V opačném případě je směr tisku definován v definici období pro sledování splatnosti.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Den/měs.</strong></p></td>
<td><p>V poli <strong>Interval</strong> vyberte jednotku <strong>Den</strong> nebo <strong>Měsíc</strong>, která se použije k definování období.</p></td>
</tr>
<tr class="even">
<td><p><strong>Pokyn pro tisk</strong></p></td>
<td><p>Vyberte, zda chcete vypočítat zůstatky a vytisknout sestavu sledování prodlení za minulá nebo budoucí období. Kalendářní data se vyhodnocují vzhledem k datu, které je vybráno v poli <strong>Zůstatek ke dni</strong>. Výběrem položky <strong>Vzad</strong> zobrazíte informace o minulých obdobích. Výběrem položky <strong>Vpřed</strong> zobrazíte informace o budoucích obdobích.</p>
<div class="alert">
  
<STRONG>Poznámka:</STRONG> Informace zadané v tomto poli se použijí jen tehdy, když nebyla vybrána definice období pro sledování splatnosti.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Podrobnosti</strong></p></td>
<td><p>Zaškrtnutím tohoto políčka vypíšete transakce, které jsou zahrnuté do zůstatků zobrazených v sestavě.</p></td>
</tr>
<tr class="even">
<td><p><strong>Zahrnout částky v měně transakce</strong></p></td>
<td><p>Zaškrtnutím tohoto políčka zahrnete částky v měně transakce navíc k částkám v zúčtovací měně. Pokud toto políčko není zaškrtnuto, zobrazí se v sestavě jen částky v zúčtovací měně.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Záporné zůstatek</strong></p></td>
<td><p>Zaškrtnutím tohoto políčka zahrnete účty odběratelů se zápornými zůstatky.</p></td>
</tr>
<tr class="even">
<td><p><strong>Vyloučit účty s nulovým zůstatkem</strong></p></td>
<td><p>Zaškrtnutím tohoto políčka vyloučíte účty odběratelů s nulovým zůstatkem.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Umístění platby</strong></p></td>
<td><p>Zaškrtnutím tohoto políčka zobrazíte platby, které nebyly vyrovnány. Zobrazují se v prvním sloupci sestavy.</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]