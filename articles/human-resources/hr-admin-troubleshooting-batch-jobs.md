---
title: Optimalizace výkonu plánováním dávkových úloh po pracovní době
description: V tomto tématu se vysvětluje, jak řešit některé problémy s aplikací Microsoft Dynamics 365 Human Resources plánováním dlouho běžících dávkových úloh po pracovní době.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500498"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="164db-103">Optimalizace výkonu plánováním dávkových úloh po pracovní době</span><span class="sxs-lookup"><span data-stu-id="164db-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="164db-104">Výdej</span><span class="sxs-lookup"><span data-stu-id="164db-104">Issue</span></span>

<span data-ttu-id="164db-105">Pokud jsou dávkové úlohy, jež běží dlouho, spouštěny během běžné pracovní doby, může mít Microsoft Dynamics 365 Human Resources problémy s výkonem.</span><span class="sxs-lookup"><span data-stu-id="164db-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="164db-106">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="164db-106">Resolution</span></span>

<span data-ttu-id="164db-107">Následující dávkové úlohy plánujte na dobu po pracovní době.</span><span class="sxs-lookup"><span data-stu-id="164db-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="164db-108">Doporučujeme také přezkoumat frekvenci dávkových úloh, které se spouští často.</span><span class="sxs-lookup"><span data-stu-id="164db-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="164db-109">Pokud je to možné, snižte frekvenci opakování dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="164db-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="164db-110">V mnoha případech je dostatečná výchozí frekvence.</span><span class="sxs-lookup"><span data-stu-id="164db-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="164db-111">Následující dávkové úlohy by měly být spouštěny v noci nebo po pracovní době.</span><span class="sxs-lookup"><span data-stu-id="164db-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="164db-112">U těchto opakujících se dávkových úloh zkontrolujte časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="164db-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="164db-113">Některé dávkové úlohy mohou používat tichomořský standardní čas (PST).</span><span class="sxs-lookup"><span data-stu-id="164db-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="164db-114">Dávková úloha</span><span class="sxs-lookup"><span data-stu-id="164db-114">Batch job</span></span> | <span data-ttu-id="164db-115">Výchozí výskyt</span><span class="sxs-lookup"><span data-stu-id="164db-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="164db-116">Vymazání historie dávkových úloh</span><span class="sxs-lookup"><span data-stu-id="164db-116">Batch job history cleanup</span></span> | <span data-ttu-id="164db-117">1krát za měsíc</span><span class="sxs-lookup"><span data-stu-id="164db-117">1 time per month</span></span> |
| <span data-ttu-id="164db-118">Exportovat vyčištění fázování</span><span class="sxs-lookup"><span data-stu-id="164db-118">Export staging cleanup</span></span> | <span data-ttu-id="164db-119">1krát denně</span><span class="sxs-lookup"><span data-stu-id="164db-119">1 time per day</span></span> |
| <span data-ttu-id="164db-120">Synchronizace zmeškaného požadavku integrace Common Data Service</span><span class="sxs-lookup"><span data-stu-id="164db-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="164db-121">1krát denně</span><span class="sxs-lookup"><span data-stu-id="164db-121">1 time per day</span></span> |
| <span data-ttu-id="164db-122">Systémová úloha komprese databáze, jež musí běžet pravidelně mimo pracovní dobu</span><span class="sxs-lookup"><span data-stu-id="164db-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="164db-123">1krát denně</span><span class="sxs-lookup"><span data-stu-id="164db-123">1 time per day</span></span> |
| <span data-ttu-id="164db-124">Systémová úloha sestavení nového indexu databáze, jež musí běžet pravidelně mimo pracovní dobu</span><span class="sxs-lookup"><span data-stu-id="164db-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="164db-125">1krát denně</span><span class="sxs-lookup"><span data-stu-id="164db-125">1 time per day</span></span> |

1. <span data-ttu-id="164db-126">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="164db-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="164db-127">Pomocí **vyhledávací** lišty vyhledejte jednu z výše uvedených dávkových úloh.</span><span class="sxs-lookup"><span data-stu-id="164db-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="164db-128">Vyberte možnost **Spustit na pozadí** a vyberte **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="164db-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Nastavení opakování](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="164db-130">V části **Definovat opakování** nastavte **Počáteční datum** a **Počáteční čas** mimo pracovní dobu nebo víkend.</span><span class="sxs-lookup"><span data-stu-id="164db-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="164db-131">Vyberte **Bez koncového data**.</span><span class="sxs-lookup"><span data-stu-id="164db-131">Select **No end date**.</span></span> 

   ![Definování počátečního data a času opakování](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="164db-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="164db-133">Select **OK**.</span></span>

6. <span data-ttu-id="164db-134">V případě potřeby změňte všechny ostatní parametry v podnabídce **Spustit na pozadí** a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="164db-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="164db-135">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="164db-135">Additional resources</span></span>

[<span data-ttu-id="164db-136">Optimalizace výkonu pomocí úloh automatického vyčištění</span><span class="sxs-lookup"><span data-stu-id="164db-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
