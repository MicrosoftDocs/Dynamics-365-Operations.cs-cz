---
title: Interakce stavu služby a pole postupu
description: Ve formuláři Servisní zakázky je v poli Pokrok v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli Stav je uveden stav jednotlivých řádků servisní zakázky.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677639"
---
# <a name="service-status-and-progress-field-interaction"></a>Interakce stavu služby a pole postupu

[!include [banner](../includes/banner.md)]

Ve formuláři **Servisní zakázky** je v poli **Postup** v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli **Stav** je uveden stav jednotlivých řádků servisní zakázky.

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Postup</p></th>
<th><p>Řádek 1 - stav</p></th>
<th><p>Řádek 2 - stav</p></th>
<th><p>Řádek 3 - stav</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Zpracovává se.</strong></p></td>
<td><p><strong>Vytvořeno</strong></p></td>
<td><p><strong>Vytvořeno</strong></p></td>
<td><p><strong>Vytvořeno</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Zpracovává se.</strong></p></td>
<td><p><strong>Zrušeno</strong></p></td>
<td><p><strong>Vytvořeno</strong></p></td>
<td><p><strong>Vytvořeno</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Zpracovává se.</strong></p></td>
<td><p><strong>Vytvořeno</strong></p></td>
<td><p><strong>Zrušeno</strong></p></td>
<td><p><strong>Zaúčtováno</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Zrušeno</strong></p></td>
<td><p><strong>Zrušeno</strong></p></td>
<td><p><strong>Zrušeno</strong></p></td>
<td><p><strong>Zrušeno</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Zaúčtováno</strong></p></td>
<td><p><strong>Zaúčtováno</strong></p></td>
<td><p><strong>Zaúčtováno</strong></p></td>
<td><p><strong>Zaúčtováno</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Zaúčtováno</strong></p></td>
<td><p><strong>Zaúčtováno</strong></p></td>
<td><p><strong>Zrušeno</strong></p></td>
<td><p><strong>Zrušeno</strong></p></td>
</tr>
</tbody>
</table>

Pokud mají všechny řádky stav **Vytvořeno**, bude servisní zakázka ve stavu zpracování. Pokud mají některé řádky stav nebo , bude servisní zakázka nadále ve stavu **Zrušeno** nebo **Zaúčtováno**.

Pokud jsou všechny řádky servisní zakázky označeny hodnotou **Zaúčtováno**, bude průběžným stavem zakázky stav **Zaúčtováno**. Pokud mají některé řádky stav **Zaúčtováno** a jiné stav **Zrušeno**, bude průběžným stavem nadále stav **Zaúčtováno**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
