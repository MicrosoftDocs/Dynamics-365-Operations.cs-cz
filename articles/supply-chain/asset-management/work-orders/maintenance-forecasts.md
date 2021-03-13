---
title: Prognózy údržby
description: Toto téma popisuje prognózy údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c60834a1f818b142a0f2f022d66fe1f42edeb536
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020854"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="00a39-103">Prognózy údržby</span><span class="sxs-lookup"><span data-stu-id="00a39-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="00a39-104">Při vytváření pracovního příkazu vytváříte úlohy pracovních příkazů se souvisejícími položkami majetku a typy práce údržby.</span><span class="sxs-lookup"><span data-stu-id="00a39-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="00a39-105">Pokud vyberete typ práce údržby obsahující prognózy údržby, budou prognózy automaticky zkopírovány do tohoto pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="00a39-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="00a39-106">Měli byste být schopni přidat řádky prognózy do pracovního příkazu nebo je z něho odstranit.</span><span class="sxs-lookup"><span data-stu-id="00a39-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="00a39-107">Nastavení stavu životního cyklu pracovního příkazu, související typ projektu a pravidla fáze související s typem projektu určují, zda lze přidávat nebo upravovat řádky prognózy.</span><span class="sxs-lookup"><span data-stu-id="00a39-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="00a39-108">Další informace o stavech životního cyklu pracovního příkazu a souvisejících fázích projektu naleznete v tématu [Prognózy, pracovní příkazy a projekty](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="00a39-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="00a39-109">Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="00a39-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="00a39-110">Vyberte pracovní příkaz v seznamu a pak v podokně akcí na kartě **Pracovní příkaz** ve skupině **Projekt** vyberte **Prognóza**.</span><span class="sxs-lookup"><span data-stu-id="00a39-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="00a39-111">Stránka **Prognóza údržby pracovního příkazu** ukazuje řádky prognózy z typu práce údržby vybrané v pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="00a39-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="00a39-112">Přidání prognózy hodin do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="00a39-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="00a39-113">Na stránce **Prognóza údržby pracovního příkazu** vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.</span><span class="sxs-lookup"><span data-stu-id="00a39-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="00a39-114">Na záložce s náhledem **Hodiny** výběrem tlačítka **Přidat** vytvořte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="00a39-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="00a39-115">V poli **Kategorie** vyberte kategorii.</span><span class="sxs-lookup"><span data-stu-id="00a39-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="00a39-116">Do pole **Hodiny** zadejte počet prognózovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="00a39-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="00a39-117">V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.</span><span class="sxs-lookup"><span data-stu-id="00a39-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="00a39-118">Přidání prognózy položek do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="00a39-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="00a39-119">Existují tři způsoby přidání položek do prognózy údržby pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="00a39-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="00a39-120">Existují tři způsoby přidání položek do prognózy údržby pracovního příkazu: můžete vytvořit řádky pro položky (náhradní díly) nebo kusovníky (BOM) majetku, které nejsou zahrnuty do seznamu náhradních dílů nebo kusovníku majetku, můžete vybrat náhradní díly ze seznamu schválených náhradních dílů a vybrat položky z kusovníku majetku.</span><span class="sxs-lookup"><span data-stu-id="00a39-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="00a39-121">Na stránce **Prognóza údržby pracovního příkazu** vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.</span><span class="sxs-lookup"><span data-stu-id="00a39-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="00a39-122">Na pevné záložce **Položky** přidejte do prognózy údržby položky pomocí odpovídající metody.</span><span class="sxs-lookup"><span data-stu-id="00a39-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="00a39-123">Chcete-li vytvořit nový řádek pro náhradní díl, který není v seznamu náhradních dílů nebo v seznamu kusovníků majetku, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="00a39-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="00a39-124">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="00a39-124">Select **Add**.</span></span>
2. <span data-ttu-id="00a39-125">V poli **Číslo položky** vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="00a39-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="00a39-126">Do pole **Množství prodeje** zadejte množství.</span><span class="sxs-lookup"><span data-stu-id="00a39-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="00a39-127">V poli **Jednotka** vyberte měrnou jednotku pro množství.</span><span class="sxs-lookup"><span data-stu-id="00a39-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="00a39-128">V poli **Cena nákladů** a **Měna** zadejte příslušné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="00a39-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="00a39-129">V poli **Vlastnost řádku** vyberte vlastnost řádku.</span><span class="sxs-lookup"><span data-stu-id="00a39-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="00a39-130">Chcete-li změnit seznam dimenzí zobrazený na řádcích položek, vyberte **Zásoby** > **Zobrazit dimenze**, vyberte dimenze a pak nastavte možnost **Uložit nastavení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="00a39-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="00a39-131">Chcete-li přidat náhradní díl ze seznamu schválených náhradních dílů, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="00a39-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="00a39-132">Vyberte možnost **Přidat náhradní díly**.</span><span class="sxs-lookup"><span data-stu-id="00a39-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="00a39-133">Vyberte náhradní díl a upravte související informace podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="00a39-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="00a39-134">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="00a39-134">Select **OK**.</span></span>

<span data-ttu-id="00a39-135">Chcete-li přidat položku z kusovníku majetku, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="00a39-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="00a39-136">Vyberte **Přidat položky kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="00a39-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="00a39-137">Vyberte položku a upravte související informace podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="00a39-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="00a39-138">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="00a39-138">Select **OK**.</span></span>

<span data-ttu-id="00a39-139">Chcete-li získat přehled o tom, kde se ve správě majetku používá položka na vybraném řádku, ve vztahu k majetku, výchozím typům práce, náhradním dílům a pracovním příkazům, vyberte **Položka, kde se používá**.</span><span class="sxs-lookup"><span data-stu-id="00a39-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="00a39-140">Další informace o tomto přehledu naleznete v tématu [Položka, kde se používá](../controlling-and-reporting/item-where-used.md)se používá.</span><span class="sxs-lookup"><span data-stu-id="00a39-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="00a39-141">Přidání prognózy výdajů do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="00a39-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="00a39-142">Na stránce **Prognóza údržby pracovního příkazu** vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.</span><span class="sxs-lookup"><span data-stu-id="00a39-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="00a39-143">Na pevné záložce **Výdaje** výběrem tlačítka **Přidat** vytvořte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="00a39-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="00a39-144">V poli **Kategorie** vyberte kategorii.</span><span class="sxs-lookup"><span data-stu-id="00a39-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="00a39-145">Poté zadejte množství v poli **Množství**.</span><span class="sxs-lookup"><span data-stu-id="00a39-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="00a39-146">Do polí **Nákladová cena**, **Prodejní měna** a **Prodejní cena** zadejte příslušné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="00a39-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="00a39-147">V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.</span><span class="sxs-lookup"><span data-stu-id="00a39-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="00a39-148">Na pevné záložce **Součty prognóz údržby** můžete zobrazit přehled počtu řádků vytvořených na jednotlivých kartách, pro vybranou úlohu pracovního příkazu a pro daný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="00a39-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="00a39-149">Zobrazuje také součet prognózovaných pracovních hodin pro úlohu pracovního příkazu a pro daný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="00a39-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="00a39-150">Na následujícím obrázku je uveden příklad stránky **Prognóza údržby pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="00a39-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Obrázek č. 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="00a39-152">Automatická aktualizace prognóz pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="00a39-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="00a39-153">Pokud jsou hodinové náklad,y náklady na položku a výdaje aktualizovány v ostatních modulech aplikace Microsoft Dynamics 365 for Finance and Operations, můžete automaticky aktualizovat změny prognóz pracovních příkazů ve správě majetku, aby se tyto změny projevily.</span><span class="sxs-lookup"><span data-stu-id="00a39-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="00a39-154">To pomáhá zajistit, aby v prognózách pracovního příkazu byly vždy nejnovější nákladové ceny.</span><span class="sxs-lookup"><span data-stu-id="00a39-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="00a39-155">Je také možné provést podobné aktualizace pro [prognózy typů práce údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="00a39-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="00a39-156">Vyberte položky **Správa majetku** > **Pravidelně** > **Prognóza** > **Aktualizovat prognózu pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="00a39-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="00a39-157">V dialogovém okně **Aktualizovat prognózu pracovního příkazu** na pevné záložce **Záznamy k zahrnutí** můžete přidat výběry týkající se konkrétních pracovních příkazů nebo úloh pracovních příkazů podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="00a39-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="00a39-158">Kliknutím na tlačítko **Filtr** proveďte příslušné výběry.</span><span class="sxs-lookup"><span data-stu-id="00a39-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="00a39-159">Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="00a39-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="00a39-160">Kliknutím na tlačítko **OK** spustíte aktualizaci prognózy.</span><span class="sxs-lookup"><span data-stu-id="00a39-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="00a39-161">Na následujícím obrázku je uveden příklad stránky **Aktualizovat prognózu údržby pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="00a39-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Obrázek č. 2](media/07-work-orders.png)
