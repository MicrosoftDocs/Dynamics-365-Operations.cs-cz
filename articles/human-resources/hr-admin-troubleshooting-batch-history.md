---
title: Optimalizace výkonu pomocí úloh automatického vyčištění
description: V tomto článku je vysvětleno, jak vyřešit některé problémy s aplikací Microsoft Dynamics 365 Human Resources vyčištěním historie dávkových úloh.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 0372833c11e0919fa03d57ea258e81a89ab9ff31
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803938"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="529cc-103">Optimalizace výkonu pomocí úkolů automatického čištění</span><span class="sxs-lookup"><span data-stu-id="529cc-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="529cc-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="529cc-104">**Issue**</span></span>

<span data-ttu-id="529cc-105">Microsoft Dynamics 365 Human Resources může zaznamenat problémy s výkonem, pokud se historie dávkových úloh příliš zvětší.</span><span class="sxs-lookup"><span data-stu-id="529cc-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="529cc-106">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="529cc-106">**Cause**</span></span>

<span data-ttu-id="529cc-107">Dávkové úlohy, které běží často, mohou vést k neudržitelnému nárůstu historie dávkových úloh.</span><span class="sxs-lookup"><span data-stu-id="529cc-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="529cc-108">To může způsobit problémy s výkonem.</span><span class="sxs-lookup"><span data-stu-id="529cc-108">This can cause performance issues.</span></span> 

<span data-ttu-id="529cc-109">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="529cc-109">**Resolution**</span></span>

<span data-ttu-id="529cc-110">Naplánování automatického úkolu vyčištění historie dávkových úloh</span><span class="sxs-lookup"><span data-stu-id="529cc-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="529cc-111">Doporučujeme nastavit úlohu tak, aby se spouštěla týdně, ale v závislosti na daném prostředí může být nutné spustit vyčištění častěji nebo méně často.</span><span class="sxs-lookup"><span data-stu-id="529cc-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="529cc-112">Následující postup obsahuje naše doporučená nastavení, ale lze je podle potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="529cc-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="529cc-113">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="529cc-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="529cc-114">Na panelu **Hledat** zadejte **Vyčištění historie dávkových úloh**.</span><span class="sxs-lookup"><span data-stu-id="529cc-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Vyhledejte vymazání historie dávkové úlohy](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="529cc-116">V části **Limit historie (dny)** zadejte **30**.</span><span class="sxs-lookup"><span data-stu-id="529cc-116">In **History limit (days)**, enter **30**.</span></span>

   ![Nastavení limitu historie na 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="529cc-118">Vyberte možnost **Spustit na pozadí** a vyberte **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="529cc-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Nastavení opakování](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="529cc-120">Ve skupinovém rámečku **definovat opakování** nastavte **Počáteční datum** a **Počáteční čas** mimo pracovní dobu nebo víkend a vyberte možnost **žáDNé DATUM UKONčENí**.</span><span class="sxs-lookup"><span data-stu-id="529cc-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Definování počátečního data a času opakování](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="529cc-122">Ve skupinovém rámečku **VZOREC OPAKOVáNí** vyberte **Dny** a nastavte **OPAKOVAT PO ZADANéM INTERVALU** na **7**.</span><span class="sxs-lookup"><span data-stu-id="529cc-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Nastavení čištění na týdenní opakování](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="529cc-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="529cc-124">Select **OK**.</span></span>

8. <span data-ttu-id="529cc-125">V případě potřeby změňte všechny ostatní parametry v podnabídce **Spustit na pozadí** a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="529cc-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]