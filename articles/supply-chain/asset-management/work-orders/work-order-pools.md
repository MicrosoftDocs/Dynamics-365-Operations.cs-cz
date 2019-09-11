---
title: Skupiny pracovních příkazů
description: V tomto tématu je popsán postup při práci se skupinami pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875547"
---
# <a name="work-order-pools"></a><span data-ttu-id="e6373-103">Skupiny pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="e6373-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e6373-104">Skupiny pracovních příkazů lze použít k seskupení pracovních příkazů, které mají něco společného.</span><span class="sxs-lookup"><span data-stu-id="e6373-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="e6373-105">Můžete například vytvořit skupiny pracovních příkazů pro</span><span class="sxs-lookup"><span data-stu-id="e6373-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="e6373-106">Pracovní skupiny, např. skupina údržby A, skupina údržby B</span><span class="sxs-lookup"><span data-stu-id="e6373-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="e6373-107">profesionální dovednosti, např. elektrikáři nebo instalatéři</span><span class="sxs-lookup"><span data-stu-id="e6373-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="e6373-108">fyzická umístění</span><span class="sxs-lookup"><span data-stu-id="e6373-108">physical locations</span></span>  

- <span data-ttu-id="e6373-109">časové plány, například týdny nebo jiná období</span><span class="sxs-lookup"><span data-stu-id="e6373-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="e6373-110">V případě potřeby lze vložit jeden pracovní příkaz do mnoha skupin pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="e6373-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="e6373-111">Vytvořit skupinu pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="e6373-111">Create work order pool</span></span>

<span data-ttu-id="e6373-112">Ve **Všech skupinách pracovních příkazů** nebo **Aktivních skupinách pracovních příkazů** můžete získat přehled o vašich skupinách pracovních příkazů a vytvořit nové skupiny.</span><span class="sxs-lookup"><span data-stu-id="e6373-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="e6373-113">Klikněte na **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="e6373-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="e6373-114">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e6373-114">Click **New**.</span></span>

3. <span data-ttu-id="e6373-115">Zadejte ID skupiny pracovních příkazů do pole **Skupina** a název do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="e6373-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="e6373-116">Výběrem možnosti Ano na přepínacím tlačítku **Aktivní** označíte, že skupina pracovních objednávek je aktivní.</span><span class="sxs-lookup"><span data-stu-id="e6373-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="e6373-117">Výběrem možnosti Ano na přepínacím tlačítku **Odebrat vztahy pracovních příkazů**, chcete-li automaticky odebrat pracovní příkazy ze skupiny pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="e6373-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="e6373-118">V poli **Odstranit stav životního cyklu** vyberte stav životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="e6373-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="e6373-119">Například stav životního cyklu pracovního příkazu pro dokončení pracovního příkazu může být nastaven tak, aby automaticky odstranil vztahy ke skupinám pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="e6373-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="e6373-120">Do skupiny pracovních příkazů můžete ihned přidávat pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="e6373-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="e6373-121">Na pevné záložce **Pracovní příkazy** klikněte na tlačítko **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="e6373-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="e6373-122">V poli **Pracovní příkaz** vyberte pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="e6373-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="e6373-123">Související pole se automaticky aktualizují.</span><span class="sxs-lookup"><span data-stu-id="e6373-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="e6373-124">Chcete-li přidat další pracovní příkazy, zopakujte kroky 7–8.</span><span class="sxs-lookup"><span data-stu-id="e6373-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="e6373-125">V poli **Pořadí řazení** lze určit, zda mají být pracovní příkazy prováděny v určitém pořadí.</span><span class="sxs-lookup"><span data-stu-id="e6373-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="e6373-126">Vložením čísel 1, 2, 3 atd. určete specifickou posloupnost pro vybrané pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="e6373-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="e6373-127">Chcete-li zobrazit seznam všech pracovních příkazů zahrnutých ve fondu pracovních příkazů, klikněte na tlačítko **Pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="e6373-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="e6373-128">Klikněte na tlačítko **Vytížení kapacity** pro otevření **Vytížení kapacity**, chcete-li vypočítat a zobrazit vytížení kapacity pro rozvrh údržby, nenaplánované pracovní příkazy a naplánované pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="e6373-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="e6373-129">Klikněte na tlačítko **Prognóza položek** pro otevření **Prognózy položek**, chcete-li vypočítat a zobrazit prognózu položek pro položky (náhradní díly a další požadované položky) související s rozvrhem údržby, nenaplánovanými pracovními příkazy a naplánovanými pracovními příkazy.</span><span class="sxs-lookup"><span data-stu-id="e6373-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="e6373-130">Klikněte na tlačítko **Nákupní žádanka pracovního příkazu** pro otevření **Nákupní žádanky pracovního příkazu**, chcete-li zobrazit seznam nákupních žádanek souvisejících s pracovními příkazy ve skupině pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="e6373-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="e6373-131">Klikněte na tlačítko **Nákupní pracovní příkaz** pro otevření **Nákupního pracovního příkazu**, chcete-li zobrazit seznam pracovních příkazů souvisejících s pracovními příkazy ve skupině pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="e6373-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="e6373-132">Není-li pro plánování práce relevantní skupina pracovních příkazů, nastavte zaškrtávací políčko **Aktivní** dané skupiny na Ne v zobrazení seznamu **Skupina pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="e6373-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="e6373-133">Zaškrtněte políčko **Odstranit vztahy pracovního příkazu**, chcete-li odstranit všechny řádky pracovního příkazu, například pro vytvoření prázdné skupiny, kterou lze později použít pro jiné pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="e6373-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="e6373-134">Nezapomeňte zrušit zaškrtnutí políčka **Odstranit vztahy pracovního příkazu**, pokud chcete použít skupinu pracovních příkazů k vytvoření nových vztahů pracovních příkazů později.</span><span class="sxs-lookup"><span data-stu-id="e6373-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Obrázek č. 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="e6373-136">Přidání pracovních příkazů do skupiny pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="e6373-136">Add work order to a work order pool</span></span>

<span data-ttu-id="e6373-137">Jak je popsáno výše, můžete při vytvoření skupiny přidat do skupiny pracovních příkazů pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="e6373-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="e6373-138">Pracovní příkaz lze rovněž přidat do skupiny pracovních příkazů ze seznamu **Všechny pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="e6373-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="e6373-139">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="e6373-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e6373-140">V seznamu vyberte požadovaný pracovní příkaz a klepněte na možnost **Skupina pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="e6373-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="e6373-141">V poli **Přidat nebo odebrat** vyberte možnost „Přidat“.</span><span class="sxs-lookup"><span data-stu-id="e6373-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="e6373-142">Vyberte skupinu pracovních příkazů v poli **Skupina**.</span><span class="sxs-lookup"><span data-stu-id="e6373-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="e6373-143">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6373-143">Click **OK**.</span></span>

6. <span data-ttu-id="e6373-144">Po přidání pracovního příkazu do skupiny pracovních příkazů, pokud chcete umístit pracovní příkaz do skupiny v určitém pořadí: otevřete jednu ze stránek se seznamem skupin pracovních příkazů, vyberte skupinu a klikněte na tlačítko **Upravit** a upravte pořadí řazení pro pracovní příkazy ve skupině ve formuláři **Skupina pracovních příkazů** > pevná záložka **Pracovní příkazy** > pole **Pořadí řazení**.</span><span class="sxs-lookup"><span data-stu-id="e6373-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="e6373-145">Chcete-li vybraný pracovní příkaz odebrat ze skupiny pracovních příkazů, vyberte v kroku 3 možnost „Odebrat“.</span><span class="sxs-lookup"><span data-stu-id="e6373-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

