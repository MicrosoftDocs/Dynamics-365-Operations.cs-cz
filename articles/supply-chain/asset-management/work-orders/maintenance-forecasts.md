---
title: Prognózy údržby
description: Toto téma popisuje prognózy údržby v modulu Správa majetku.
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
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024492"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="61d25-103">Prognózy údržby</span><span class="sxs-lookup"><span data-stu-id="61d25-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="61d25-104">Při vytváření pracovního příkazu vytváříte úlohy pracovních příkazů se souvisejícími položkami majetku a typy práce údržby.</span><span class="sxs-lookup"><span data-stu-id="61d25-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="61d25-105">Pokud vyberete typ práce údržby obsahující prognózy údržby, budou prognózy automaticky zkopírovány do tohoto pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="61d25-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="61d25-106">Řádky prognózy můžete přidávat nebo odstraňovat v rámci pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="61d25-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="61d25-107">Nastavení stavu životního cyklu pracovního příkazu, související typ projektu a pravidla fáze související s typem projektu určují, zda lze přidávat nebo upravovat řádky prognózy.</span><span class="sxs-lookup"><span data-stu-id="61d25-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="61d25-108">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="61d25-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="61d25-109">V seznamu vyberte požadovaný pracovní příkaz a klepněte na možnost **Prognóza**.</span><span class="sxs-lookup"><span data-stu-id="61d25-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="61d25-110">V části **Prognóza údržby pracovního příkazu** jsou zobrazeny řádky prognózy z typu práce údržby vybrané na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="61d25-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="61d25-111">Přidat hodiny prognózy do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="61d25-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="61d25-112">Vyberte úlohu pracovního příkazu, do níž chcete přidat prognózu.</span><span class="sxs-lookup"><span data-stu-id="61d25-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="61d25-113">Na záložce s náhledem **Hodiny** kliknutím na tlačítko **Přidat** vytvořte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="61d25-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="61d25-114">V poli **Kategorie** vyberte kategorii.</span><span class="sxs-lookup"><span data-stu-id="61d25-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="61d25-115">Do pole **Hodiny** zadejte počet prognózovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="61d25-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="61d25-116">V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.</span><span class="sxs-lookup"><span data-stu-id="61d25-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="61d25-117">Přidání prognózy položek do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="61d25-117">Add items forecast to a work order</span></span>

<span data-ttu-id="61d25-118">Existují tři způsoby přidání položek do prognózy údržby pracovního příkazu: můžete vytvořit řádky pro položky (náhradní díly), které nejsou zahrnuty do seznamu náhradních dílů nebo kusovníku majetku, můžete vybrat náhradní díly ze seznamu schválených náhradních dílů a vybrat položky z kusovníku majetku.</span><span class="sxs-lookup"><span data-stu-id="61d25-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="61d25-119">Vyberte úlohu pracovního příkazu, do níž chcete přidat prognózu.</span><span class="sxs-lookup"><span data-stu-id="61d25-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="61d25-120">Vyberte záložku s náhledem **Položky**.</span><span class="sxs-lookup"><span data-stu-id="61d25-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="61d25-121">Chcete-li vytvořit nový řádek pro náhradní díl, který není v seznamu náhradních dílů nebo v seznamu kusovníků majetku, klepněte na možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="61d25-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="61d25-122">V poli **Číslo položky** vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="61d25-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="61d25-123">Vložte množství do pole **Prodejní množství** a vyberte jednotku množství v poli **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="61d25-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="61d25-124">Do příslušných polí vložte nákladovou cenu a měnu a vyberte **Vlastnost řádku**.</span><span class="sxs-lookup"><span data-stu-id="61d25-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="61d25-125">Chcete-li změnit seznam dimenzí zobrazený na řádcích položek, klepněte na volby **Zásoby** > **Zobrazit dimenze**, vyberte dimenze a na přepínacím tlačítku **Uložit nastavení** vyberte možnost „Ano“.</span><span class="sxs-lookup"><span data-stu-id="61d25-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="61d25-126">Chcete-li do prognózy údržby přidat schválený náhradní díl, klikněte na možnost **Přidat náhradní díly**, v případě potřeby vyberte náhradní díl, upravte související informace a klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="61d25-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="61d25-127">Chcete-li do prognózy přidat položky kusovníku majetku, klikněte na možnost **Přidat položkykusovníku**, vyberte položku, upravte související informace a klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="61d25-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="61d25-128">Klikněte na možnost **Kde byla položka použita,** chcete-li získat přehled o tom, kde se ve Správě majetku používá položka na vybraném řádku ve vztahu k majetku, výchozím typům práce údržby, náhradním dílům a pracovním příkazům.</span><span class="sxs-lookup"><span data-stu-id="61d25-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="61d25-129">Přidání prognózy výdajů do pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="61d25-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="61d25-130">Tohle téma popisuje, jak přidat prognózu výdajů do pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="61d25-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="61d25-131">Na levé straně formuláře vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.</span><span class="sxs-lookup"><span data-stu-id="61d25-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="61d25-132">Vyberte záložku s náhledem **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="61d25-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="61d25-133">Kliknutím na **Přidat** vytvořte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="61d25-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="61d25-134">V poli **Kategorie** vyberte kategorii.</span><span class="sxs-lookup"><span data-stu-id="61d25-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="61d25-135">Poté zadejte množství v poli **Množství**.</span><span class="sxs-lookup"><span data-stu-id="61d25-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="61d25-136">Do příslušných polí zadejte nákladovou cenu, prodejní měnu a prodejní cenu.</span><span class="sxs-lookup"><span data-stu-id="61d25-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="61d25-137">V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.</span><span class="sxs-lookup"><span data-stu-id="61d25-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="61d25-138">Na záložce s náhledem **Součty prognóz údržby** můžete zobrazit přehled počtu řádků vytvořených na jednotlivých kartách, pro vybranou úlohu pracovního příkazu a pro daný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="61d25-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="61d25-139">Můžete také zobrazit součet prognózovaných pracovních hodin pro úlohu pracovního příkazu a pro daný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="61d25-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Obrázek č. 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="61d25-141">Automatická aktualizace prognóz pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="61d25-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="61d25-142">V modulu Správa majetku můžete automaticky aktualizovat všechny změny prognóz pracovních příkazů ohledně hodinových nákladů, nákladů na položky a výdajů, které byly aktualizovány v jiných modulech.</span><span class="sxs-lookup"><span data-stu-id="61d25-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="61d25-143">Je to proto, aby v prognózách pracovního příkazu byly vždy nejnovější nákladové ceny.</span><span class="sxs-lookup"><span data-stu-id="61d25-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="61d25-144">Je také možné provést podobné aktualizace pro [prognózy typů práce údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="61d25-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="61d25-145">Klikněte na položky **Správa majetku** > **Pravidelně** > **Prognóza** > **Aktualizovat prognózu pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="61d25-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="61d25-146">V rozevíracím dialogovém okně **Aktualizovat prognózu pracovního příkazu** můžete přidat výběr týkající se konkrétních pracovních příkazů nebo úloh pracovních příkazů, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="61d25-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="61d25-147">Kliknutím na tlačítko **Filtr** proveďte tento výběr.</span><span class="sxs-lookup"><span data-stu-id="61d25-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="61d25-148">Pokud je to nutné, na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="61d25-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="61d25-149">Kliknutím na tlačítko **OK** spustíte aktualizaci prognózy.</span><span class="sxs-lookup"><span data-stu-id="61d25-149">Click **OK** to start the forecast update.</span></span>


![Obrázek č. 2](media/07-work-orders.png)

