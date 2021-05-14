---
title: Vlna není způsobilá k vyčištění
description: Vlna není způsobilá k vyčištění
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924320"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="88b05-103">Vlna není způsobilá k vyčištění</span><span class="sxs-lookup"><span data-stu-id="88b05-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="88b05-104">Kód chyby: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="88b05-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="88b05-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="88b05-105">Symptoms</span></span>

<span data-ttu-id="88b05-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="88b05-106">The system shows the following error message:</span></span>

> <span data-ttu-id="88b05-107">Vlna %1 není pro vyčištění způsobilá.</span><span class="sxs-lookup"><span data-stu-id="88b05-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="88b05-108">Data vln nelze vyčistit.</span><span class="sxs-lookup"><span data-stu-id="88b05-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="88b05-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="88b05-109">Cause</span></span>

<span data-ttu-id="88b05-110">Vlna se aktuálně zpracovává, jak naznačuje jedna z následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="88b05-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="88b05-111">Pole **Stav vlny** je nastaveno na hodnotu *Zpracování*.</span><span class="sxs-lookup"><span data-stu-id="88b05-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="88b05-112">Když vyberete možnost **Dávková úloha** ve skupině **Vlna** na kartě **Vlna** podokna akcí, pole **Stav** není nastaveno na hodnotu *Ukončeno*, *Chyba* nebo *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="88b05-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="88b05-113">Proto je aktuálně spuštěna dávková úloha.</span><span class="sxs-lookup"><span data-stu-id="88b05-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="88b05-114">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="88b05-114">Resolution</span></span>

<span data-ttu-id="88b05-115">V podokně akcí na kartě **Vlna** ve skupině **Vlna** vyberte možnost **Dávková úloha** a poté proveďte jeden z těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="88b05-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="88b05-116">Pokud je pole **Stav** nastaveno na hodnotu *Zpracování*: V podoknu akcí na kartě **Dávková úloha** ve skupině **Dávková úloha** vyberte možnost **Zobrazení úkolů**.</span><span class="sxs-lookup"><span data-stu-id="88b05-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="88b05-117">Průběh můžete sledovat pomocí obnovení stránky **Dávkové úkoly**.</span><span class="sxs-lookup"><span data-stu-id="88b05-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="88b05-118">Pokud není pole **Stav** nastaveno na hodnotu *Zpracování*: V podoknu akcí na kartě **Dávková úloha** ve skupině **Funkce** vyberte možnost **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="88b05-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="88b05-119">V poli **Vyberte nový stav** vyberte možnost *Čekání*.</span><span class="sxs-lookup"><span data-stu-id="88b05-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="88b05-120">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="88b05-120">Then select **OK**.</span></span>
