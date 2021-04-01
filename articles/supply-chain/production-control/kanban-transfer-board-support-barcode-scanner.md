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
ms.openlocfilehash: 8b6d65430d09c293fd5bca032b8b0e88c971d5a9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246086"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="4c44a-103">Rozvrh převodů kanbanu podporuje skenery čárových kódů</span><span class="sxs-lookup"><span data-stu-id="4c44a-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c44a-104">Rozvrh převodů kanbanu podporuje vstup ze skeneru skrze widget pro skener čárového kódu, který umožňuje vybrat, zahájit, dokončit a vyprázdnit kanbanovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="4c44a-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="4c44a-105">Režimy registrace</span><span class="sxs-lookup"><span data-stu-id="4c44a-105">Registration modes</span></span>
------------------

<span data-ttu-id="4c44a-106">Na pevné záložce **Registrace skeneru** můžete vybrat režim registrace, který řídí akci při skenování čísla kanbanové karty ne ručně skenujete číslo v poli Číslo kanbanové karty.</span><span class="sxs-lookup"><span data-stu-id="4c44a-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="4c44a-107">Nastavit režim registrace</span><span class="sxs-lookup"><span data-stu-id="4c44a-107">Set registration mode</span></span> | <span data-ttu-id="4c44a-108">Popis</span><span class="sxs-lookup"><span data-stu-id="4c44a-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c44a-109">Počátek</span><span class="sxs-lookup"><span data-stu-id="4c44a-109">Start</span></span>                 | <span data-ttu-id="4c44a-110">Registrovat úlohu převodu kanbanu jako probíhající.</span><span class="sxs-lookup"><span data-stu-id="4c44a-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="4c44a-111">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="4c44a-111">Complete</span></span>              | <span data-ttu-id="4c44a-112">Registrovat úlohu převodu kanbanu jako dokončenou.</span><span class="sxs-lookup"><span data-stu-id="4c44a-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="4c44a-113">Prázdné</span><span class="sxs-lookup"><span data-stu-id="4c44a-113">Empty</span></span>                 | <span data-ttu-id="4c44a-114">Registrovat manipulační jednotku materiálu odkazovanou kanbanovou kartou jako prázdnou.</span><span class="sxs-lookup"><span data-stu-id="4c44a-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="4c44a-115">Vybrat</span><span class="sxs-lookup"><span data-stu-id="4c44a-115">Select</span></span>                | <span data-ttu-id="4c44a-116">Registrovat číslo kanbanové karty a automaticky vybrat odkazovanou úlohu ze seznamu kanbanu.</span><span class="sxs-lookup"><span data-stu-id="4c44a-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="4c44a-117">Režim registrace – Nastavit</span><span class="sxs-lookup"><span data-stu-id="4c44a-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="4c44a-118">Pokud používáte čtečku čárových kódů pro výběr úlohy, režim zobrazení kanbanové desky se změní.</span><span class="sxs-lookup"><span data-stu-id="4c44a-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="4c44a-119">V tomto režimu platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="4c44a-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="4c44a-120">Zobrazí se pouze skenovaná kanbanová úloha.</span><span class="sxs-lookup"><span data-stu-id="4c44a-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="4c44a-121">Podrobnosti o vybrané úloze jsou uvedeny na pevné záložce **Podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="4c44a-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="4c44a-122">Pevná záložka **Zprávy** zobrazuje zprávy pouze pro vybranou úlohu.</span><span class="sxs-lookup"><span data-stu-id="4c44a-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="4c44a-123">Stav úlohy lze změnit pomocí funkce, která je k dispozici v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="4c44a-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="4c44a-124">Rozvrh převodů kanbanu bude i nadále popisovat pouze jednu úlohu během této doby.</span><span class="sxs-lookup"><span data-stu-id="4c44a-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="4c44a-125">Informace v seznamu úloh lze aktualizovat ručně klepnutím na **Aktualizovat** (Shift + F5) v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="4c44a-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="4c44a-126">Po aktualizaci údajů jsou znovu zobrazeny úplné výsledky filtru úlohy.</span><span class="sxs-lookup"><span data-stu-id="4c44a-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="4c44a-127">Stav úlohy a možné akce</span><span class="sxs-lookup"><span data-stu-id="4c44a-127">Job status and possible actions</span></span>
<span data-ttu-id="4c44a-128">Stav vybrané úlohy a stav doložené úlohy pro kanbany události určuje, zda může úlohu dále zpracovat.</span><span class="sxs-lookup"><span data-stu-id="4c44a-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="4c44a-129">V následující tabulce jsou uvedeny informace o těchto stavech a úkolech:</span><span class="sxs-lookup"><span data-stu-id="4c44a-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="4c44a-130">Stavy, které jsou k dispozici pro úlohy nebo manipulační jednotky, na které odkazují úlohy.</span><span class="sxs-lookup"><span data-stu-id="4c44a-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="4c44a-131">Jednotlivé úkoly, které mohou provádět úlohu.</span><span class="sxs-lookup"><span data-stu-id="4c44a-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="4c44a-132">Typ práce</span><span class="sxs-lookup"><span data-stu-id="4c44a-132">Job type</span></span></th>
<th><span data-ttu-id="4c44a-133">Stav úlohy nebo stav manipulační jednotky</span><span class="sxs-lookup"><span data-stu-id="4c44a-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="4c44a-134">Aktualizovat výdejku</span><span class="sxs-lookup"><span data-stu-id="4c44a-134">Update picking list</span></span></th>
<th><span data-ttu-id="4c44a-135">Počátek</span><span class="sxs-lookup"><span data-stu-id="4c44a-135">Start</span></span></th>
<th><span data-ttu-id="4c44a-136">Aktualizovat registraci</span><span class="sxs-lookup"><span data-stu-id="4c44a-136">Update registration</span></span></th>
<th><span data-ttu-id="4c44a-137">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="4c44a-137">Complete</span></span></th>
<th><span data-ttu-id="4c44a-138">Prázdné</span><span class="sxs-lookup"><span data-stu-id="4c44a-138">Empty</span></span></th>
<th><span data-ttu-id="4c44a-139">Vytvořit kanbanové události</span><span class="sxs-lookup"><span data-stu-id="4c44a-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c44a-140">Převést</span><span class="sxs-lookup"><span data-stu-id="4c44a-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="4c44a-141">Neplánováno</span><span class="sxs-lookup"><span data-stu-id="4c44a-141">Not planned</span></span></li>
<li><span data-ttu-id="4c44a-142">Žádné doložené nebo doložené úlohy jsou dokončeny</span><span class="sxs-lookup"><span data-stu-id="4c44a-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="4c44a-143">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-143">Yes</span></span></td>
<td><span data-ttu-id="4c44a-144">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-144">Yes</span></span></td>
<td><span data-ttu-id="4c44a-145">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-145">Yes</span></span></td>
<td><span data-ttu-id="4c44a-146">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-146">Yes</span></span></td>
<td><span data-ttu-id="4c44a-147">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-147">No</span></span></td>
<td><span data-ttu-id="4c44a-148">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c44a-149">Převést</span><span class="sxs-lookup"><span data-stu-id="4c44a-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="4c44a-150">Neplánováno</span><span class="sxs-lookup"><span data-stu-id="4c44a-150">Not planned</span></span></li>
<li><span data-ttu-id="4c44a-151">Doložené úlohy nejsou dokončeny</span><span class="sxs-lookup"><span data-stu-id="4c44a-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="4c44a-152">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-152">Yes</span></span></td>
<td><span data-ttu-id="4c44a-153">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-153">No</span></span></td>
<td><span data-ttu-id="4c44a-154">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-154">Yes</span></span></td>
<td><span data-ttu-id="4c44a-155">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-155">No</span></span></td>
<td><span data-ttu-id="4c44a-156">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-156">No</span></span></td>
<td><span data-ttu-id="4c44a-157">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c44a-158">Převést</span><span class="sxs-lookup"><span data-stu-id="4c44a-158">Transfer</span></span></td>
<td><span data-ttu-id="4c44a-159">Probíhá</span><span class="sxs-lookup"><span data-stu-id="4c44a-159">In progress</span></span></td>
<td><span data-ttu-id="4c44a-160">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-160">Yes</span></span></td>
<td><span data-ttu-id="4c44a-161">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-161">No</span></span></td>
<td><span data-ttu-id="4c44a-162">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-162">Yes</span></span></td>
<td><span data-ttu-id="4c44a-163">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-163">Yes</span></span></td>
<td><span data-ttu-id="4c44a-164">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-164">No</span></span></td>
<td><span data-ttu-id="4c44a-165">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c44a-166">Převést</span><span class="sxs-lookup"><span data-stu-id="4c44a-166">Transfer</span></span></td>
<td><span data-ttu-id="4c44a-167">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="4c44a-167">Completed</span></span></td>
<td><span data-ttu-id="4c44a-168">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-168">No</span></span></td>
<td><span data-ttu-id="4c44a-169">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-169">No</span></span></td>
<td><span data-ttu-id="4c44a-170">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-170">No</span></span></td>
<td><span data-ttu-id="4c44a-171">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-171">No</span></span></td>
<td><span data-ttu-id="4c44a-172">Ano</span><span class="sxs-lookup"><span data-stu-id="4c44a-172">Yes</span></span></td>
<td><span data-ttu-id="4c44a-173">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c44a-174">Převod nebo průběh</span><span class="sxs-lookup"><span data-stu-id="4c44a-174">Transfer or process</span></span></td>
<td><span data-ttu-id="4c44a-175">Prázdné</span><span class="sxs-lookup"><span data-stu-id="4c44a-175">Empty</span></span></td>
<td><span data-ttu-id="4c44a-176">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-176">No</span></span></td>
<td><span data-ttu-id="4c44a-177">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-177">No</span></span></td>
<td><span data-ttu-id="4c44a-178">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-178">No</span></span></td>
<td><span data-ttu-id="4c44a-179">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-179">No</span></span></td>
<td><span data-ttu-id="4c44a-180">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-180">No</span></span></td>
<td><span data-ttu-id="4c44a-181">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c44a-182">Převod nebo průběh</span><span class="sxs-lookup"><span data-stu-id="4c44a-182">Transfer or process</span></span></td>
<td><span data-ttu-id="4c44a-183">Kanbanová karta nebyla nalezena</span><span class="sxs-lookup"><span data-stu-id="4c44a-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="4c44a-184">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-184">No</span></span></td>
<td><span data-ttu-id="4c44a-185">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-185">No</span></span></td>
<td><span data-ttu-id="4c44a-186">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-186">No</span></span></td>
<td><span data-ttu-id="4c44a-187">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-187">No</span></span></td>
<td><span data-ttu-id="4c44a-188">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-188">No</span></span></td>
<td><span data-ttu-id="4c44a-189">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c44a-190">Převod nebo průběh</span><span class="sxs-lookup"><span data-stu-id="4c44a-190">Transfer or process</span></span></td>
<td><span data-ttu-id="4c44a-191">Kanbanová karta je nalezena, ale není přiřazena ke kanbanu</span><span class="sxs-lookup"><span data-stu-id="4c44a-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="4c44a-192">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-192">No</span></span></td>
<td><span data-ttu-id="4c44a-193">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-193">No</span></span></td>
<td><span data-ttu-id="4c44a-194">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-194">No</span></span></td>
<td><span data-ttu-id="4c44a-195">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-195">No</span></span></td>
<td><span data-ttu-id="4c44a-196">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-196">No</span></span></td>
<td><span data-ttu-id="4c44a-197">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c44a-198">Proces</span><span class="sxs-lookup"><span data-stu-id="4c44a-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="4c44a-199">Neplánováno</span><span class="sxs-lookup"><span data-stu-id="4c44a-199">Not planned</span></span></li>
<li><span data-ttu-id="4c44a-200">Připraveno</span><span class="sxs-lookup"><span data-stu-id="4c44a-200">Prepared</span></span></li>
<li><span data-ttu-id="4c44a-201">Probíhá</span><span class="sxs-lookup"><span data-stu-id="4c44a-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="4c44a-202">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-202">No</span></span></td>
<td><span data-ttu-id="4c44a-203">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-203">No</span></span></td>
<td><span data-ttu-id="4c44a-204">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-204">No</span></span></td>
<td><span data-ttu-id="4c44a-205">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-205">No</span></span></td>
<td><span data-ttu-id="4c44a-206">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-206">No</span></span></td>
<td><span data-ttu-id="4c44a-207">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c44a-208">Proces</span><span class="sxs-lookup"><span data-stu-id="4c44a-208">Process</span></span></td>
<td><span data-ttu-id="4c44a-209">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="4c44a-209">Completed</span></span></td>
<td><span data-ttu-id="4c44a-210">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-210">No</span></span></td>
<td><span data-ttu-id="4c44a-211">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-211">No</span></span></td>
<td><span data-ttu-id="4c44a-212">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-212">No</span></span></td>
<td><span data-ttu-id="4c44a-213">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-213">No</span></span></td>
<td><span data-ttu-id="4c44a-214">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-214">No</span></span></td>
<td><span data-ttu-id="4c44a-215">Č.</span><span class="sxs-lookup"><span data-stu-id="4c44a-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]