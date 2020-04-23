---
title: Skupiny pracovních příkazů
description: V tomto tématu je popsán postup při práci se skupinami pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: debff2d6ec9c9e3ba711f62ffefab0546dbd2346
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208862"
---
# <a name="work-order-pools"></a><span data-ttu-id="6052e-103">Skupiny pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="6052e-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="6052e-104">Skupiny pracovních příkazů lze použít k seskupení pracovních příkazů, které mají něco společného.</span><span class="sxs-lookup"><span data-stu-id="6052e-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="6052e-105">Zde je několik příkladů akcí, které lze vytvořit z následujících skupin pracovních příkazů:</span><span class="sxs-lookup"><span data-stu-id="6052e-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="6052e-106">Pracovní skupiny, např. skupina údržby A nebo skupina údržby B</span><span class="sxs-lookup"><span data-stu-id="6052e-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="6052e-107">Profesionální dovednosti, např. elektrikáři nebo instalatéři</span><span class="sxs-lookup"><span data-stu-id="6052e-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="6052e-108">Fyzická umístění</span><span class="sxs-lookup"><span data-stu-id="6052e-108">Physical locations</span></span>  

- <span data-ttu-id="6052e-109">Časové plány, například týdny nebo jiná období</span><span class="sxs-lookup"><span data-stu-id="6052e-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="6052e-110">Podle potřeby lze do více skupin pracovních příkazů vložit jednu pracovní objednávku.</span><span class="sxs-lookup"><span data-stu-id="6052e-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="6052e-111">Vytvoření fondu pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="6052e-111">Create a work order pool</span></span>

<span data-ttu-id="6052e-112">Na stránce se seznamem **Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů** můžete získat přehled o vašich skupinách pracovních příkazů a vytvořit nové skupiny.</span><span class="sxs-lookup"><span data-stu-id="6052e-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="6052e-113">Vyberte **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="6052e-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="6052e-114">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="6052e-114">Select **New**.</span></span>

3. <span data-ttu-id="6052e-115">V poli **Fond** zadejte identifikátor fondu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6052e-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="6052e-116">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="6052e-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="6052e-117">Natavením možnosti **Ano** na přepínacím tlačítku **Aktivní** označíte, že skupina pracovních objednávek je aktivní.</span><span class="sxs-lookup"><span data-stu-id="6052e-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="6052e-118">Nastavte možnost **Ano** na přepínacím tlačítku **Odstranit vztahy pracovních příkazů**, chcete-li automaticky odebrat pracovní příkazy ze skupiny pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="6052e-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="6052e-119">V poli **Odstranit stav životního cyklu** vyberte stav životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="6052e-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="6052e-120">Například stav životního cyklu pracovního příkazu pro dokončení pracovního příkazu může být nastaven tak, aby automaticky odstranil vztahy ke skupinám pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="6052e-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="6052e-121">Do skupiny pracovních příkazů můžete ihned přidávat pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="6052e-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="6052e-122">Na pevné záložce **Pracovní příkazy** vyberte tlačítko **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="6052e-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="6052e-123">V poli **Pracovní příkaz** vyberte pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="6052e-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="6052e-124">Související pole se automaticky aktualizují.</span><span class="sxs-lookup"><span data-stu-id="6052e-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="6052e-125">Opakováním kroků 8 až 9 přidejte další pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="6052e-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="6052e-126">Pokud mají být přidané pracovní příkazy prováděny v určitém pořadí, můžete v poli **Pořadí řazení** zadat čísla **1**, **2**, **3** atd. a určit tak pořadí.</span><span class="sxs-lookup"><span data-stu-id="6052e-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="6052e-127">Chcete-li zobrazit seznam všech pracovních příkazů, které jsou zahrnuty ve fondu pracovních příkazů, na kartě **Fond pracovních příkazů** ve skupině **Zobrazit související fond pracovních příkazů** vyberte možnost **Pracovní příkazy**, pro kterou chcete otevřít stránku se seznamem **Všechny pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="6052e-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="6052e-128">Chcete-li vypočítat a zobrazit vytížení kapacity pro plán údržby, neplánované pracovní příkazy a plánované pracovní příkazy, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Zobrazit související fond pracovních příkazů** vyberte **Vytížení kapacity** k otevření dialogového okna **Vypočítat vytížení kapacity**.</span><span class="sxs-lookup"><span data-stu-id="6052e-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="6052e-129">Chcete-li vypočítat a zobrazit prognózy položek (náhradní díly a další požadované položky), které souvisí splánem údržby, neplánovanými pracovními příkazy a plánovanými pracovními příkazy, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Zobrazit související fond pracovních příkazů** vyberte **Prognóza položky** k otevření dialogového okna **Vypočítat prognózu položky**.</span><span class="sxs-lookup"><span data-stu-id="6052e-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="6052e-130">Chcete-li zobrazit seznam nákupních žádanek, které souvisí s pracovními příkazy ve fondu pracovních příkazů, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Nákup** vyberte možnost **Nákupní žádanka pracovního příkazu** k otevření stránky se seznamem **Nákupní žádanka pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="6052e-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="6052e-131">Chcete-li zobrazit seznam nákupních objednávek, které souvisí s pracovními příkazy ve fondu pracovních příkazů, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Nákup** vyberte možnost **Nákupní objednávka pracovního příkazu** k otevření stránky se seznamem **Nákupní objednávka pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="6052e-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="6052e-132">Není-li pro vaše plánování práce dále relevantní fond pracovních příkazů, nastavte možnost **Aktivní** daného fondu na **Ne** v zobrazení seznamu na stránce **Fond pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="6052e-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="6052e-133">Chcete-li odstranit všechny řádky pracovního příkazu, nastavte možnost **Odstranit vztahy pracovního příkazu** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6052e-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="6052e-134">Tato možnost je užitečná například tehdy, chcete-li vytvořit prázdný fond, který lze použít později pro další pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="6052e-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="6052e-135">Až budete později připravení použít fond pracovního příkazu k vytvoření nových vztahů pracovního příkazu, nezapomeňte nastavit možnost **Odstranit vztahy pracovního příkazu** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="6052e-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="6052e-136">Na následujícím obrázku je uveden příklad stránky se seznamem **Fond pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="6052e-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Obrázek č. 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="6052e-138">Přidání pracovního příkazu do skupiny pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="6052e-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="6052e-139">Jak je popsáno v předchozí části, můžete při vytvoření skupiny přidat do skupiny pracovních příkazů pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="6052e-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="6052e-140">Můžete také přidat pracovní příkazy do fondu pracovních příkazů na stránce se seznamem **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="6052e-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="6052e-141">Vyberte pracovní příkaz v seznamu a pak v podokně akcí na kartě **Pracovní příkaz** ve skupině **Údržba** vyberte **Fond pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="6052e-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="6052e-142">V seznamu vyberte požadovaný pracovní příkaz a klepněte na možnost **Skupina pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="6052e-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="6052e-143">V dialogovém okně **Spravovat fond pracovních příkazů** v poli **Přidat/odebrat** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="6052e-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="6052e-144">Vyberte fond pracovních příkazů v poli **Fond**.</span><span class="sxs-lookup"><span data-stu-id="6052e-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="6052e-145">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="6052e-145">Select **OK**.</span></span>

6. <span data-ttu-id="6052e-146">Chcete-li vložit pracovní příkaz, který jste přidali v určitém pořadí ve fondu pracovních příkazů, vyberte stránku se seznamem **Všechny fondy pracovních příkazů** nebo **Aktivní fondy pracovních příkazů**, vyberte požadovaný fond a poté vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="6052e-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="6052e-147">Pak na stránce **Fond pracovních příkazů** na pevné záložce **Pracovní příkazy** použijte pole **Pořadí řazení** k nastavení pořadí pracovních příkazů zahrnutých ve fondu.</span><span class="sxs-lookup"><span data-stu-id="6052e-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="6052e-148">Chcete-li vybraný pracovní příkaz odebrat z fondu pracovních příkazů, vyberte v kroku 3 možnost **Odebrat**.</span><span class="sxs-lookup"><span data-stu-id="6052e-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

