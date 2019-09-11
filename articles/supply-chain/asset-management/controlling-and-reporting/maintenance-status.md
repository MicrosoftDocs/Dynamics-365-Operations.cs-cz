---
title: Stav údržby
description: Toto téma vysvětluje, jak vypočítat stav údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918342"
---
# <a name="maintenance-status"></a><span data-ttu-id="b5346-103">Stav údržby</span><span class="sxs-lookup"><span data-stu-id="b5346-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b5346-104">V modulu Správa majetku můžete výpočtem získat přehled nových, aktivních a dokončených požadavků na údržbu, pracovních příkazů a aktivit prostojů údržby za určité období.</span><span class="sxs-lookup"><span data-stu-id="b5346-104">In Asset Management, you can make a calculation to see an overview of new, active, and completed maintenance requests, work orders, and maintenance downtime activities for a specific period.</span></span> <span data-ttu-id="b5346-105">Můžete také zobrazit počet provedených odhadů podmínek pro stejné období.</span><span class="sxs-lookup"><span data-stu-id="b5346-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="b5346-106">Pomocí tohoto výpočtu získáte přehled o pracovním vytížení, které se týká příchozích a dokončených požadavků na údržbu a pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="b5346-106">Use this calculation to get an overview of workload regarding incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="b5346-107">Výpočet stavu údržby</span><span class="sxs-lookup"><span data-stu-id="b5346-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="b5346-108">Klikněte na možnosti **Správa majetku** > **Dotazy** > **Stav údržby**.</span><span class="sxs-lookup"><span data-stu-id="b5346-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="b5346-109">V dialogovém okně **Stavvýpočtu** vyberte období, pro které chcete provést výpočet v polích **Od data** a **Do data**.</span><span class="sxs-lookup"><span data-stu-id="b5346-109">In the **Calculate status** dialog, select the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="b5346-110">V poli **Úroveň** určete, jak detailní mají být řádky údržby v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="b5346-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> <span data-ttu-id="b5346-111">Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky údržby pro funkční místo, a proto lze stav na řádku navýšit z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="b5346-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="b5346-112">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky údržby na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="b5346-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="b5346-113">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5346-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="b5346-114">Ve skupině podoken akcí **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="b5346-114">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="b5346-115">Vybraná tlačítka podokna akcí jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="b5346-115">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="b5346-116">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="b5346-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="b5346-117">Nezapomeňte tlačítkem **Aktualizovat** aktualizovat výpočet při každé změně aktivací nebo deaktivací tlačítek **Skupiny pole...** nebo provedením výpočtu pro nové období.</span><span class="sxs-lookup"><span data-stu-id="b5346-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="b5346-118">Klikněte na možnost **Stav**, chcete-li vytvořit nový výpočet stavu údržby.</span><span class="sxs-lookup"><span data-stu-id="b5346-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="b5346-119">Výsledky zobrazené v sekci **Stav údržby** zahrnují pouze požadavky na údržbu a pracovní příkazy, které mají skutečný počáteční datum a čas.</span><span class="sxs-lookup"><span data-stu-id="b5346-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="b5346-120">Pole koncového data a času mohou být prázdná.</span><span class="sxs-lookup"><span data-stu-id="b5346-120">End date and time may be blank.</span></span>

<span data-ttu-id="b5346-121">*Příklad 1:*</span><span class="sxs-lookup"><span data-stu-id="b5346-121">*Example 1:*</span></span>

<span data-ttu-id="b5346-122">Na níže uvedeném obrázku jsou aktivovány tlačítka **Rok** a **Měsíc**.</span><span class="sxs-lookup"><span data-stu-id="b5346-122">In the figure below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="b5346-123">Zde získáte obecný přehled o měsíčním pracovním vytížení a propustnosti, které souvisejí s požadavky na údržbu a pracovními příkazy.</span><span class="sxs-lookup"><span data-stu-id="b5346-123">Here, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Obrázek č. 1](media/13-controlling-and-reporting.png)

<span data-ttu-id="b5346-125">*Příklad 2:*</span><span class="sxs-lookup"><span data-stu-id="b5346-125">*Example 2:*</span></span>

<span data-ttu-id="b5346-126">Na níže uvedeném obrázku byly přidány informace o funkčních místech.</span><span class="sxs-lookup"><span data-stu-id="b5346-126">In the figure below, information about functional locations has been added.</span></span> <span data-ttu-id="b5346-127">Nyní je možné porovnat pracovní vytížení a propustnost mezi funkčními místy, která mohou představovat geografická umístění, továrny nebo pracovní oblasti.</span><span class="sxs-lookup"><span data-stu-id="b5346-127">Now, it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Obrázek č. 2](media/14-controlling-and-reporting.png)

