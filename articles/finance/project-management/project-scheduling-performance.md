---
title: Výkon plánování prostředků projektů
description: Tohle téma poskytuje informace, jak zlepšit výkon plánování prostředků u velkého počtu projektů.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760499"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="babf3-103">Výkon plánování prostředků projektů</span><span class="sxs-lookup"><span data-stu-id="babf3-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="babf3-104">Problémy s výkonem související s plánováním prostředků mohou nastat, když počet projektů dosáhne tisíců.</span><span class="sxs-lookup"><span data-stu-id="babf3-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="babf3-105">K vylepšení výkonu plánování prostředků je k dispozici funkce, která uživatelům umožňuje zkrátit čas potřebný ke spuštění formuláře dostupnosti prostředků.</span><span class="sxs-lookup"><span data-stu-id="babf3-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="babf3-106">Konkrétně odebere proces synchronizace pro shrnutí kapacity prostředků a použije tabulku **ResProjectResource** k urychlení vyhledávání prostředků.</span><span class="sxs-lookup"><span data-stu-id="babf3-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="babf3-107">Všimněte si, že tabulka **ResRollup** již nebude použita.</span><span class="sxs-lookup"><span data-stu-id="babf3-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="babf3-108">Pokud existuje závislost buď na procesu synchronizace pro shrutí kapacity prostředků, nebo na tabulce **ResProjectResource**, nepoužívejte tuto funkci.</span><span class="sxs-lookup"><span data-stu-id="babf3-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="babf3-109">Povolení zvýšení výkonnosti plánování prostředků</span><span class="sxs-lookup"><span data-stu-id="babf3-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="babf3-110">Chcete-li povolit vylepšení výkonnosti plánování prostředků, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="babf3-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="babf3-111">Přejděte na **Správa funkcí** > **Vše** a v seznamu funkcí vyhledejte **Povolit funkci vylepšení výkonosti plánování prostředků projektu**.</span><span class="sxs-lookup"><span data-stu-id="babf3-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="babf3-112">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="babf3-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="babf3-113">Pokud nemůžete najít funkci v seznamu, volbou **Zkontrolovat aktualizace** aktualizujte seznam.</span><span class="sxs-lookup"><span data-stu-id="babf3-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="babf3-114">Aktualizujte prohlížeč a poté přejděte na **Řízení a účetnictví projektu** > **Periodické** > **Prostředky projektu** > **Synchronizovat kapacitu kalendářů prostředků ve všech společnostech**.</span><span class="sxs-lookup"><span data-stu-id="babf3-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="babf3-115">Nastavením **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data.</span><span class="sxs-lookup"><span data-stu-id="babf3-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="babf3-116">Pokud chcete generovat přírůstková data, nastavte tuto volbu na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="babf3-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="babf3-117">V poli **Kód období** vyberte období, ve kterém mají být data generována.</span><span class="sxs-lookup"><span data-stu-id="babf3-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="babf3-118">Pokud vyberete kód období, není nutné definovat počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="babf3-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="babf3-119">Pokud ponecháte pole **Kód období** prázdné, vyberte konkrétní počáteční a koncové datum pro generování dat.</span><span class="sxs-lookup"><span data-stu-id="babf3-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="babf3-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="babf3-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="babf3-121">Dojde k distribuci obecných dat do tabulky **ResCalendarCapacity** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="babf3-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="babf3-122">Data v této dávkové úloze jsou potřebná k výpočtu kapacity prostředků prostřednictvím přidruženého kalendáře.</span><span class="sxs-lookup"><span data-stu-id="babf3-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="babf3-123">Přejděte na **Řízení a účetnictví projektu** > **Periodické** > **Prostředky projektu** > **Naplnit prostředky projektu ve všech společnostech** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="babf3-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="babf3-124">Toto je skript pro aktualizaci dat pro obecná data v tabulkách **ResProjectResource**, **ResCalendarDateTimeRange** a **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="babf3-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="babf3-125">Hodnoty pro pole **PSAPRojSchedRole.RootActivity** se také aktualizují.</span><span class="sxs-lookup"><span data-stu-id="babf3-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="babf3-126">Pokud to není spuštěno, obdržíte varování, když se pokusíte provést operace plánování prostředků.</span><span class="sxs-lookup"><span data-stu-id="babf3-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="babf3-127">Zapnutí zvýšení výkonnosti plánování prostředků</span><span class="sxs-lookup"><span data-stu-id="babf3-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="babf3-128">Přejděte na **Správa funkcí** > **Vše** a hledejte **Povolit funkci vylepšení výkonosti plánování prostředků projektu**.</span><span class="sxs-lookup"><span data-stu-id="babf3-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="babf3-129">Vyberte funkci a poté vyberte tlačítko **Zakázat**.</span><span class="sxs-lookup"><span data-stu-id="babf3-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="babf3-130">Aktualizujte svůj prohlížeč.</span><span class="sxs-lookup"><span data-stu-id="babf3-130">Refresh your browser.</span></span>
4. <span data-ttu-id="babf3-131">Přejděte na **Řízení a účetnictví projektů** > **Periodicky** > **Synchronizace kapacity** > **Synchronizace shrnutí kapacity pro prostředek**.</span><span class="sxs-lookup"><span data-stu-id="babf3-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="babf3-132">Na stránce **Synchronizace shrnutí kapacity** nastavením **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data.</span><span class="sxs-lookup"><span data-stu-id="babf3-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="babf3-133">Pokud chcete generovat přírůstková data, nastavte tuto volbu na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="babf3-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="babf3-134">V poli **Kód období** vyberte období, ve kterém mají být data generována.</span><span class="sxs-lookup"><span data-stu-id="babf3-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="babf3-135">Pokud vyberete kód období, není nutné definovat počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="babf3-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="babf3-136">Pokud ponecháte pole **Kód období** prázdné, vyberte konkrétní počáteční a koncové datum pro generování dat.</span><span class="sxs-lookup"><span data-stu-id="babf3-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="babf3-137">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="babf3-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="babf3-138">Dojde k distribuci obecných dat do tabulky **ResRollup** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="babf3-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="babf3-139">Tato dávková úloha je nutná pro všechn zobrazení **Dostupnost prostředků**.</span><span class="sxs-lookup"><span data-stu-id="babf3-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="babf3-140">Pokud tato dávková úloha není spuštěna, data **ResRollup** budou generována za chodu, což může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="babf3-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
