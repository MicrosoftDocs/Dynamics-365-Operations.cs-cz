---
title: Interakce stavu služby a pole postupu
description: Ve formuláři Servisní zakázky je v poli Pokrok v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli Stav je uveden stav jednotlivých řádků servisní zakázky.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd7b5160149a38dd62535901c1225bf704f404d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570779"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="e68eb-103">Interakce stavu služby a pole postupu</span><span class="sxs-lookup"><span data-stu-id="e68eb-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e68eb-104">Ve formuláři **Servisní zakázky** je v poli **Postup** v záhlaví servisní zakázky uveden stav celé servisní zakázky a v poli **Stav** je uveden stav jednotlivých řádků servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e68eb-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e68eb-105">Postup</span><span class="sxs-lookup"><span data-stu-id="e68eb-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="e68eb-106">Řádek 1 - stav</span><span class="sxs-lookup"><span data-stu-id="e68eb-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="e68eb-107">Řádek 2 - stav</span><span class="sxs-lookup"><span data-stu-id="e68eb-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="e68eb-108">Řádek 3 - stav</span><span class="sxs-lookup"><span data-stu-id="e68eb-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e68eb-109"><strong>Zpracovává se.</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-110"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-111"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-112"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e68eb-113"><strong>Zpracovává se.</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-114"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-115"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-116"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e68eb-117"><strong>Zpracovává se.</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-118"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-119"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-120"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e68eb-121"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-122"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-123"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-124"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e68eb-125"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-126"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-127"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-128"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e68eb-129"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-130"><strong>Zaúčtováno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-131"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e68eb-132"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="e68eb-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e68eb-133">Pokud mají všechny řádky stav **Vytvořeno**, bude servisní zakázka ve stavu zpracování. Pokud mají některé řádky stav nebo , bude servisní zakázka nadále ve stavu **Zrušeno** nebo **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="e68eb-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="e68eb-134">Pokud jsou všechny řádky servisní zakázky označeny hodnotou **Zaúčtováno**, bude průběžným stavem zakázky stav **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="e68eb-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="e68eb-135">Pokud mají některé řádky stav **Zaúčtováno** a jiné stav **Zrušeno**, bude průběžným stavem nadále stav **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="e68eb-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


