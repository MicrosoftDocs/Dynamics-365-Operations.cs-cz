---
title: "Interakce stavu služby a pole postupu"
description: "Ve formuláři Servisní zakázky je v poli Pokrok v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli Stav je uveden stav jednotlivých řádků servisní zakázky."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 51ef39266e8de00488954918568d00a297a9b50a
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---


# <a name="service-status-and-progress-field-interaction"></a>Interakce stavu služby a pole postupu 

[!include [banner](../includes/banner.md)]


Ve formuláři **Servisní zakázky** je v poli **Postup** v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli **Stav** je uveden stav jednotlivých řádků servisní zakázky.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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

  



