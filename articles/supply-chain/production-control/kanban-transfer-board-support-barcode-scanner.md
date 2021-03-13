---
title: Rozvrh převodů kanbanu podporuje skenery čárových kódů
description: Rozvrh převodů kanbanu podporuje vstup ze skeneru skrze widget pro skener čárového kódu, který umožňuje vybrat, zahájit, dokončit a vyprázdnit kanbanovou úlohu.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aedfe7ef96d62401b1d0de0f2cd035036c68e51a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007059"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="423d5-103">Rozvrh převodů kanbanu podporuje skenery čárových kódů</span><span class="sxs-lookup"><span data-stu-id="423d5-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="423d5-104">Rozvrh převodů kanbanu podporuje vstup ze skeneru skrze widget pro skener čárového kódu, který umožňuje vybrat, zahájit, dokončit a vyprázdnit kanbanovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="423d5-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="423d5-105">Režimy registrace</span><span class="sxs-lookup"><span data-stu-id="423d5-105">Registration modes</span></span>
------------------

<span data-ttu-id="423d5-106">Na pevné záložce **Registrace skeneru** můžete vybrat režim registrace, který řídí akci při skenování čísla kanbanové karty ne ručně skenujete číslo v poli Číslo kanbanové karty.</span><span class="sxs-lookup"><span data-stu-id="423d5-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="423d5-107">Nastavit režim registrace</span><span class="sxs-lookup"><span data-stu-id="423d5-107">Set registration mode</span></span> | <span data-ttu-id="423d5-108">Popis</span><span class="sxs-lookup"><span data-stu-id="423d5-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="423d5-109">Počátek</span><span class="sxs-lookup"><span data-stu-id="423d5-109">Start</span></span>                 | <span data-ttu-id="423d5-110">Registrovat úlohu převodu kanbanu jako probíhající.</span><span class="sxs-lookup"><span data-stu-id="423d5-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="423d5-111">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="423d5-111">Complete</span></span>              | <span data-ttu-id="423d5-112">Registrovat úlohu převodu kanbanu jako dokončenou.</span><span class="sxs-lookup"><span data-stu-id="423d5-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="423d5-113">Prázdné</span><span class="sxs-lookup"><span data-stu-id="423d5-113">Empty</span></span>                 | <span data-ttu-id="423d5-114">Registrovat manipulační jednotku materiálu odkazovanou kanbanovou kartou jako prázdnou.</span><span class="sxs-lookup"><span data-stu-id="423d5-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="423d5-115">Vybrat</span><span class="sxs-lookup"><span data-stu-id="423d5-115">Select</span></span>                | <span data-ttu-id="423d5-116">Registrovat číslo kanbanové karty a automaticky vybrat odkazovanou úlohu ze seznamu kanbanu.</span><span class="sxs-lookup"><span data-stu-id="423d5-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="423d5-117">Režim registrace – Nastavit</span><span class="sxs-lookup"><span data-stu-id="423d5-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="423d5-118">Pokud používáte čtečku čárových kódů pro výběr úlohy, režim zobrazení kanbanové desky se změní.</span><span class="sxs-lookup"><span data-stu-id="423d5-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="423d5-119">V tomto režimu platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="423d5-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="423d5-120">Zobrazí se pouze skenovaná kanbanová úloha.</span><span class="sxs-lookup"><span data-stu-id="423d5-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="423d5-121">Podrobnosti o vybrané úloze jsou uvedeny na pevné záložce **Podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="423d5-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="423d5-122">Pevná záložka **Zprávy** zobrazuje zprávy pouze pro vybranou úlohu.</span><span class="sxs-lookup"><span data-stu-id="423d5-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="423d5-123">Stav úlohy lze změnit pomocí funkce, která je k dispozici v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="423d5-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="423d5-124">Rozvrh převodů kanbanu bude i nadále popisovat pouze jednu úlohu během této doby.</span><span class="sxs-lookup"><span data-stu-id="423d5-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="423d5-125">Informace v seznamu úloh lze aktualizovat ručně klepnutím na **Aktualizovat** (Shift + F5) v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="423d5-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="423d5-126">Po aktualizaci údajů jsou znovu zobrazeny úplné výsledky filtru úlohy.</span><span class="sxs-lookup"><span data-stu-id="423d5-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="423d5-127">Stav úlohy a možné akce</span><span class="sxs-lookup"><span data-stu-id="423d5-127">Job status and possible actions</span></span>
<span data-ttu-id="423d5-128">Stav vybrané úlohy a stav doložené úlohy pro kanbany události určuje, zda může úlohu dále zpracovat.</span><span class="sxs-lookup"><span data-stu-id="423d5-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="423d5-129">V následující tabulce jsou uvedeny informace o těchto stavech a úkolech:</span><span class="sxs-lookup"><span data-stu-id="423d5-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="423d5-130">Stavy, které jsou k dispozici pro úlohy nebo manipulační jednotky, na které odkazují úlohy.</span><span class="sxs-lookup"><span data-stu-id="423d5-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="423d5-131">Jednotlivé úkoly, které mohou provádět úlohu.</span><span class="sxs-lookup"><span data-stu-id="423d5-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="423d5-132">Typ práce</span><span class="sxs-lookup"><span data-stu-id="423d5-132">Job type</span></span></th>
<th><span data-ttu-id="423d5-133">Stav úlohy nebo stav manipulační jednotky</span><span class="sxs-lookup"><span data-stu-id="423d5-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="423d5-134">Aktualizovat výdejku</span><span class="sxs-lookup"><span data-stu-id="423d5-134">Update picking list</span></span></th>
<th><span data-ttu-id="423d5-135">Počátek</span><span class="sxs-lookup"><span data-stu-id="423d5-135">Start</span></span></th>
<th><span data-ttu-id="423d5-136">Aktualizovat registraci</span><span class="sxs-lookup"><span data-stu-id="423d5-136">Update registration</span></span></th>
<th><span data-ttu-id="423d5-137">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="423d5-137">Complete</span></span></th>
<th><span data-ttu-id="423d5-138">Prázdné</span><span class="sxs-lookup"><span data-stu-id="423d5-138">Empty</span></span></th>
<th><span data-ttu-id="423d5-139">Vytvořit kanbanové události</span><span class="sxs-lookup"><span data-stu-id="423d5-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="423d5-140">Převést</span><span class="sxs-lookup"><span data-stu-id="423d5-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="423d5-141">Neplánováno</span><span class="sxs-lookup"><span data-stu-id="423d5-141">Not planned</span></span></li>
<li><span data-ttu-id="423d5-142">Žádné doložené nebo doložené úlohy jsou dokončeny</span><span class="sxs-lookup"><span data-stu-id="423d5-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="423d5-143">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-143">Yes</span></span></td>
<td><span data-ttu-id="423d5-144">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-144">Yes</span></span></td>
<td><span data-ttu-id="423d5-145">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-145">Yes</span></span></td>
<td><span data-ttu-id="423d5-146">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-146">Yes</span></span></td>
<td><span data-ttu-id="423d5-147">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-147">No</span></span></td>
<td><span data-ttu-id="423d5-148">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="423d5-149">Převést</span><span class="sxs-lookup"><span data-stu-id="423d5-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="423d5-150">Neplánováno</span><span class="sxs-lookup"><span data-stu-id="423d5-150">Not planned</span></span></li>
<li><span data-ttu-id="423d5-151">Doložené úlohy nejsou dokončeny</span><span class="sxs-lookup"><span data-stu-id="423d5-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="423d5-152">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-152">Yes</span></span></td>
<td><span data-ttu-id="423d5-153">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-153">No</span></span></td>
<td><span data-ttu-id="423d5-154">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-154">Yes</span></span></td>
<td><span data-ttu-id="423d5-155">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-155">No</span></span></td>
<td><span data-ttu-id="423d5-156">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-156">No</span></span></td>
<td><span data-ttu-id="423d5-157">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="423d5-158">Převést</span><span class="sxs-lookup"><span data-stu-id="423d5-158">Transfer</span></span></td>
<td><span data-ttu-id="423d5-159">Probíhá</span><span class="sxs-lookup"><span data-stu-id="423d5-159">In progress</span></span></td>
<td><span data-ttu-id="423d5-160">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-160">Yes</span></span></td>
<td><span data-ttu-id="423d5-161">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-161">No</span></span></td>
<td><span data-ttu-id="423d5-162">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-162">Yes</span></span></td>
<td><span data-ttu-id="423d5-163">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-163">Yes</span></span></td>
<td><span data-ttu-id="423d5-164">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-164">No</span></span></td>
<td><span data-ttu-id="423d5-165">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="423d5-166">Převést</span><span class="sxs-lookup"><span data-stu-id="423d5-166">Transfer</span></span></td>
<td><span data-ttu-id="423d5-167">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="423d5-167">Completed</span></span></td>
<td><span data-ttu-id="423d5-168">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-168">No</span></span></td>
<td><span data-ttu-id="423d5-169">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-169">No</span></span></td>
<td><span data-ttu-id="423d5-170">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-170">No</span></span></td>
<td><span data-ttu-id="423d5-171">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-171">No</span></span></td>
<td><span data-ttu-id="423d5-172">Ano</span><span class="sxs-lookup"><span data-stu-id="423d5-172">Yes</span></span></td>
<td><span data-ttu-id="423d5-173">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="423d5-174">Převod nebo průběh</span><span class="sxs-lookup"><span data-stu-id="423d5-174">Transfer or process</span></span></td>
<td><span data-ttu-id="423d5-175">Prázdné</span><span class="sxs-lookup"><span data-stu-id="423d5-175">Empty</span></span></td>
<td><span data-ttu-id="423d5-176">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-176">No</span></span></td>
<td><span data-ttu-id="423d5-177">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-177">No</span></span></td>
<td><span data-ttu-id="423d5-178">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-178">No</span></span></td>
<td><span data-ttu-id="423d5-179">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-179">No</span></span></td>
<td><span data-ttu-id="423d5-180">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-180">No</span></span></td>
<td><span data-ttu-id="423d5-181">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="423d5-182">Převod nebo průběh</span><span class="sxs-lookup"><span data-stu-id="423d5-182">Transfer or process</span></span></td>
<td><span data-ttu-id="423d5-183">Kanbanová karta nebyla nalezena</span><span class="sxs-lookup"><span data-stu-id="423d5-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="423d5-184">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-184">No</span></span></td>
<td><span data-ttu-id="423d5-185">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-185">No</span></span></td>
<td><span data-ttu-id="423d5-186">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-186">No</span></span></td>
<td><span data-ttu-id="423d5-187">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-187">No</span></span></td>
<td><span data-ttu-id="423d5-188">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-188">No</span></span></td>
<td><span data-ttu-id="423d5-189">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="423d5-190">Převod nebo průběh</span><span class="sxs-lookup"><span data-stu-id="423d5-190">Transfer or process</span></span></td>
<td><span data-ttu-id="423d5-191">Kanbanová karta je nalezena, ale není přiřazena ke kanbanu</span><span class="sxs-lookup"><span data-stu-id="423d5-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="423d5-192">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-192">No</span></span></td>
<td><span data-ttu-id="423d5-193">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-193">No</span></span></td>
<td><span data-ttu-id="423d5-194">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-194">No</span></span></td>
<td><span data-ttu-id="423d5-195">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-195">No</span></span></td>
<td><span data-ttu-id="423d5-196">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-196">No</span></span></td>
<td><span data-ttu-id="423d5-197">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="423d5-198">Proces</span><span class="sxs-lookup"><span data-stu-id="423d5-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="423d5-199">Neplánováno</span><span class="sxs-lookup"><span data-stu-id="423d5-199">Not planned</span></span></li>
<li><span data-ttu-id="423d5-200">Připraveno</span><span class="sxs-lookup"><span data-stu-id="423d5-200">Prepared</span></span></li>
<li><span data-ttu-id="423d5-201">Probíhá</span><span class="sxs-lookup"><span data-stu-id="423d5-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="423d5-202">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-202">No</span></span></td>
<td><span data-ttu-id="423d5-203">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-203">No</span></span></td>
<td><span data-ttu-id="423d5-204">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-204">No</span></span></td>
<td><span data-ttu-id="423d5-205">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-205">No</span></span></td>
<td><span data-ttu-id="423d5-206">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-206">No</span></span></td>
<td><span data-ttu-id="423d5-207">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="423d5-208">Proces</span><span class="sxs-lookup"><span data-stu-id="423d5-208">Process</span></span></td>
<td><span data-ttu-id="423d5-209">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="423d5-209">Completed</span></span></td>
<td><span data-ttu-id="423d5-210">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-210">No</span></span></td>
<td><span data-ttu-id="423d5-211">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-211">No</span></span></td>
<td><span data-ttu-id="423d5-212">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-212">No</span></span></td>
<td><span data-ttu-id="423d5-213">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-213">No</span></span></td>
<td><span data-ttu-id="423d5-214">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-214">No</span></span></td>
<td><span data-ttu-id="423d5-215">Č.</span><span class="sxs-lookup"><span data-stu-id="423d5-215">No</span></span></td>
</tr>
</tbody>
</table>





