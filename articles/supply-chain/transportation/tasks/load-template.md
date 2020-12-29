---
title: Šablony vytížení
description: Toto téma popisuje způsob nastavení šablony nákladů a jak přiřadit šablonu nákladu do nového nákladu.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646368"
---
# <a name="load-templates"></a><span data-ttu-id="1480f-103">Šablony vytížení</span><span class="sxs-lookup"><span data-stu-id="1480f-103">Load templates</span></span>

<span data-ttu-id="1480f-104">Při vytváření nového vytížení můžete přiřadit šablonu vytížení.</span><span class="sxs-lookup"><span data-stu-id="1480f-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="1480f-105">Šablona vytížení obsahuje informace o vybavení a měrných jednotkách, jako je výška, šířka, hloubka a objem nákladu.</span><span class="sxs-lookup"><span data-stu-id="1480f-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="1480f-106">Toto téma popisuje způsob nastavení šablony nákladů a jak přiřadit šablonu nákladu do nového nákladu.</span><span class="sxs-lookup"><span data-stu-id="1480f-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="1480f-107">Nastavení šablony vytížení</span><span class="sxs-lookup"><span data-stu-id="1480f-107">Set up a load template</span></span>

1. <span data-ttu-id="1480f-108">Přejděte na **Řízení dopravy \> Nastavení \> Sestavení vytížení \> Šablona vytížení**.</span><span class="sxs-lookup"><span data-stu-id="1480f-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="1480f-109">V podokně akcí vyberte **Nová** pro přidání nové šablony nebo **Upravit** pro úpravu existující šablony.</span><span class="sxs-lookup"><span data-stu-id="1480f-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="1480f-110">V řádku pro novou nebo stávající šablonu nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="1480f-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="1480f-111">**ID šablony vytížení** - Zadejte jedinečný identifikátor (ID) pro šablonu vytížení.</span><span class="sxs-lookup"><span data-stu-id="1480f-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="1480f-112">**Vybavení** - Vyberte vybavení, které by mělo být použito k přepravě nákladu.</span><span class="sxs-lookup"><span data-stu-id="1480f-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="1480f-113">**Výška nákladu**, **Šířka nákladu** a **Hloubka nákladu** - Zadejte rozměry nákladu.</span><span class="sxs-lookup"><span data-stu-id="1480f-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="1480f-114">**Maximální povolený objem nákladu** a **Maximální povolená hmotnost nákladu** - Zadejte maximální povolený objem a hmotnost nákladu.</span><span class="sxs-lookup"><span data-stu-id="1480f-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="1480f-115">**Maximální povolená hrubá hmotnost** - Zadejte maximální povolenou hrubou hmotnost nákladu.</span><span class="sxs-lookup"><span data-stu-id="1480f-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="1480f-116">Hrubá hmotnost nákladu zahrnuje hmotnosti obalu a nákladovou hmotnost.</span><span class="sxs-lookup"><span data-stu-id="1480f-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="1480f-117">**Maximální počet kusů nákladu** - Zadejte maximální počet kusů, které může náklad obsahovat.</span><span class="sxs-lookup"><span data-stu-id="1480f-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="1480f-118">**Složení nákladu na zemi** - Zaškrtnutím tohoto políčka použijete nakládku na zemi.</span><span class="sxs-lookup"><span data-stu-id="1480f-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="1480f-119">Ve scénáři nákladu na zemi jsou krabice seřazeny od podlahy ke stropu, od stěny ke stěně uvnitř kontejneru pro využití maximální kapacity.</span><span class="sxs-lookup"><span data-stu-id="1480f-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="1480f-120">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1480f-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="1480f-121">Přiřazení šablony nákladu k novému nákladu</span><span class="sxs-lookup"><span data-stu-id="1480f-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="1480f-122">Přejděte do **Správa přepravy \> Plánování \> Pracovní plocha plánování vytížení**.</span><span class="sxs-lookup"><span data-stu-id="1480f-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="1480f-123">V horní části stránky vyberte jednu z následujících karet v závislosti na typu zdrojového dokumentu, pro který vytváříte náklad: **Dodávky**, **Řádky prodeje**, **Řádky převodu** nebo **Řádky nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="1480f-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="1480f-124">Vyberte konkrétní dokument, pro který chcete naplánovat náklad.</span><span class="sxs-lookup"><span data-stu-id="1480f-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="1480f-125">V podokně Akce na kartě **Nabídka a poptávka** vyberte ve skupině **Přidat** možnost **Do nového vytížení**.</span><span class="sxs-lookup"><span data-stu-id="1480f-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="1480f-126">V dialogovém okně **Šablona vytížení** zvolte v poli **ID šablony vytížení** šablonu, kterou použijete.</span><span class="sxs-lookup"><span data-stu-id="1480f-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="1480f-127">Zvolte **OK** pro použití šablony.</span><span class="sxs-lookup"><span data-stu-id="1480f-127">Select **OK** to apply the template.</span></span>
