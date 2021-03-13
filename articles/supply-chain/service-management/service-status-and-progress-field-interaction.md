---
title: Interakce stavu služby a pole postupu
description: Ve formuláři Servisní zakázky je v poli Pokrok v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli Stav je uveden stav jednotlivých řádků servisní zakázky.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 314ca8c325205bd8f489daf46498e9586603eaf3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010440"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="0e684-103">Interakce stavu služby a pole postupu</span><span class="sxs-lookup"><span data-stu-id="0e684-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0e684-104">Ve formuláři **Servisní zakázky** je v poli **Postup** v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli **Stav** je uveden stav jednotlivých řádků servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="0e684-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e684-105">Postup</span><span class="sxs-lookup"><span data-stu-id="0e684-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="0e684-106">Řádek 1 - stav</span><span class="sxs-lookup"><span data-stu-id="0e684-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="0e684-107">Řádek 2 - stav</span><span class="sxs-lookup"><span data-stu-id="0e684-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="0e684-108">Řádek 3 - stav</span><span class="sxs-lookup"><span data-stu-id="0e684-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e684-109"><strong>Zpracovává se.</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-110"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-111"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-112"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e684-113"><strong>Zpracovává se.</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-114"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-115"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-116"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e684-117"><strong>Zpracovává se.</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-118"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-119"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-120"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e684-121"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-122"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-123"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-124"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e684-125"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-126"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-127"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-128"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e684-129"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-130"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-131"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="0e684-132"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="0e684-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e684-133">Pokud mají všechny řádky stav **Vytvořeno**, bude servisní zakázka ve stavu zpracování. Pokud mají některé řádky stav nebo , bude servisní zakázka nadále ve stavu **Zrušeno** nebo **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="0e684-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="0e684-134">Pokud jsou všechny řádky servisní zakázky označeny hodnotou **Zaúčtováno**, bude průběžným stavem zakázky stav **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="0e684-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="0e684-135">Pokud mají některé řádky stav **Zaúčtováno** a jiné stav **Zrušeno**, bude průběžným stavem nadále stav **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="0e684-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


