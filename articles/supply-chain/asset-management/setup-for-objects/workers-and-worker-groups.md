---
title: Pracovníci údržby a skupiny pracovníků
description: Toto téma vysvětluje, jak nastavit pracovníky údržby skupiny pracovníků v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c85fc24cdf0b3cd1a188ccf0f477ffbfa5fab960
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783114"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="ef97d-103">Pracovníci údržby a skupiny pracovníků</span><span class="sxs-lookup"><span data-stu-id="ef97d-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ef97d-104">Toto téma vysvětluje, jak nastavit pracovníky údržby skupiny pracovníků v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="ef97d-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="ef97d-105">V modulu Správa majetku můžete pracovníky údržby připojit k funkčním místům.</span><span class="sxs-lookup"><span data-stu-id="ef97d-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="ef97d-106">(Další informace o funkčních umístěních naleznete v tématu [Tvorba funkčních míst](../functional-locations/create-functional-locations.md).) Tato funkce může být užitečná například v případě, že plánujete úlohu údržby stroje, který je umístěn na funkčním místě 01, a chcete práci přidělit pracovníkům údržby ze stejného místa.</span><span class="sxs-lookup"><span data-stu-id="ef97d-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="ef97d-107">Můžete také vytvořit skupiny pracovníků údržby a přidružit k nim pracovníky údržby.</span><span class="sxs-lookup"><span data-stu-id="ef97d-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="ef97d-108">Tato funkce je užitečná, když provádíte jednoduché plánování pracovních zakázek a chcete naplánovat skupinu údržbářských pracovníků na pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="ef97d-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="ef97d-109">Pracovníky údržby a údržbářské skupiny můžete použít k nastavení preferovaných pracovníků údržby a zodpovědných pracovníků údržby.</span><span class="sxs-lookup"><span data-stu-id="ef97d-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="ef97d-110">Vytvořit pracovníky</span><span class="sxs-lookup"><span data-stu-id="ef97d-110">Create workers</span></span>

1. <span data-ttu-id="ef97d-111">Vyberte **Správa majetku** \> **Nastavení** \> **Pracovníci** \> **Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="ef97d-112">Vyberte **Nový** pro přidání pracovníka na seznam.</span><span class="sxs-lookup"><span data-stu-id="ef97d-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="ef97d-113">V poli **Pracovník** vyberte pracovníka.</span><span class="sxs-lookup"><span data-stu-id="ef97d-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="ef97d-114">Nastavením možnosti **Aktivní** na **Ano** naplánujete pracovníka na pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="ef97d-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="ef97d-115">Na pevné záložce **Obecné** jsou pole **Prostředek** a **Popis** automaticky vyplněna, pokud byl zdroj vybrán pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="ef97d-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="ef97d-116">Pole **Kalendář** je také vyplněno automaticky, pokud jste pracovníka nastavili jako zdroj a přidělili k danému zdroji kalendář na stránce **Prostředky** (**Správa organizace** \> **Prostředky** \> **Prostředky**).</span><span class="sxs-lookup"><span data-stu-id="ef97d-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="ef97d-117">Na pevné záložce **Skupiny** vyberte **Přidat** a pak vyberte skupinu pracovníků údržby pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="ef97d-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="ef97d-118">Pracovník může být přiřazen k více než jedné skupině.</span><span class="sxs-lookup"><span data-stu-id="ef97d-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="ef97d-119">Ve standardním nastavení je příslušnost pracovníka ke skupině účinná od data přidání skupiny a nikdy nevyprší.</span><span class="sxs-lookup"><span data-stu-id="ef97d-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="ef97d-120">Toto datum je zobrazeno v poli **Účinnost**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="ef97d-121">Chcete-li zobrazit pole **Účinnost** vyberte **Zobrazit** \> **Vše**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="ef97d-122">Pokud má být přidružení pracovníka ke skupině omezeno na určité období, definujte období pomocí **Účinnost** a **Vypršení platnosti**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="ef97d-123">Na pevné záložce **Funkční místa** vyberte **Přidat** a pak vyberte funkční místo pro pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="ef97d-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="ef97d-124">Zadejte také, které místo je primárním funkčním místem pracovníka.</span><span class="sxs-lookup"><span data-stu-id="ef97d-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef97d-125">Po přidání funkčních umístění pracovníkovi se veškerý aktivní majetek, který se vztahuje k těmto funkčním místům, zobrazí v různých položkách nabídky, jako je například **Můj aktivní majetek** a **Moje aktivní funkční místa**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="ef97d-126">Zobrazí se také ve vyhledávání majetku, které se zobrazí při vytvoření nového majetku, požadavku na údržbu nebo pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="ef97d-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="ef97d-127">Pole na pevné záložce **Podrobnosti** zobrazí počet skupin údržby a funkčních míst, ke kterým se vybraný pracovník údržby vztahuje.</span><span class="sxs-lookup"><span data-stu-id="ef97d-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="ef97d-128">Vytvořit skupiny pracovníků</span><span class="sxs-lookup"><span data-stu-id="ef97d-128">Create worker groups</span></span>

1. <span data-ttu-id="ef97d-129">Vyberte **Správa majetku** \> **Nastavení** \> **Pracovníci** \> **Skupiny pracovníků údržby**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="ef97d-130">Vyberte **Nový** pro přidání skupiny pracovníků na seznam.</span><span class="sxs-lookup"><span data-stu-id="ef97d-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="ef97d-131">Do pole **Skupina pracovníků údržby** zadejte ID skupiny.</span><span class="sxs-lookup"><span data-stu-id="ef97d-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="ef97d-132">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="ef97d-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="ef97d-133">Na pevné záložce **Pracovníci** vyberte **Přidat** a pak vyberte skupinu pracovníků údržby pro skupinu pracovníků.</span><span class="sxs-lookup"><span data-stu-id="ef97d-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="ef97d-134">Informace o polích **Účinnost** a **Vypršení platnosti** najdete v kroku 6 v předchozí proceduře.</span><span class="sxs-lookup"><span data-stu-id="ef97d-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="ef97d-135">Pokud má skupina prostředků souviset s vybranou skupinou údržbářských pracovníků, vyberte možnost **Kopírovat ze skupiny prostředků**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="ef97d-136">V poli **Skupina** vyberte skupinu zdrojů, ze které chcete kopírovat nastavení kalendáře.</span><span class="sxs-lookup"><span data-stu-id="ef97d-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="ef97d-137">Potom v poli **Skupina pracovníků** vyberte skupinu pracovníků, ke které chcete zkopírovat nastavení kalendáře skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="ef97d-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="ef97d-138">Tento krok je relevantní pouze v případě, že chcete, aby pracovníci údržby používali kalendář, který se vztahuje k prostředku (pracovnímu středisku) během plánování pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="ef97d-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="ef97d-139">Pole na pevné záložce **Podrobnosti** zobrazí počet pracovníků údržby a funkčních míst, které byly vytvořeny ve zvolené skupině pracovníků údržby.</span><span class="sxs-lookup"><span data-stu-id="ef97d-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
