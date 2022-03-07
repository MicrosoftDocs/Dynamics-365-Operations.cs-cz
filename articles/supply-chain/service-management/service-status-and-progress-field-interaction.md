---
title: Interakce stavu služby a pole postupu
description: Ve formuláři Servisní zakázky je v poli Pokrok v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli Stav je uveden stav jednotlivých řádků servisní zakázky.
author: kamaybac
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0758c370fd1548770d596115b18f133071f3bbc0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566088"
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
