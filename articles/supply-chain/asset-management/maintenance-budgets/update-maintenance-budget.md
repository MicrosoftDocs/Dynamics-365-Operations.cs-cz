---
title: Aktualizace rozpočtů údržby
description: Toto téma vysvětluje, jak aktualizovat rozpočet údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 01620e1cca17d3c2b08b3abcdf9a4482693f0409
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809823"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="04bdc-103">Aktualizace rozpočtů údržby</span><span class="sxs-lookup"><span data-stu-id="04bdc-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="04bdc-104">Na stránce **Řádky rozpočtu údržby** jsou zobrazeny všechny řádky rozpočtu, které byly vytvořeny pro rozpočet vybraný na stránce **Rozpočty údržby**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="04bdc-105">(Další informace naleznete v tématu [Vytvoření rozpočtů údržby](create-maintenance-budget.md).) Řádky rozpočtu údržby lze přepočítat a upravit, dokud není schválen rozpočet údržby.</span><span class="sxs-lookup"><span data-stu-id="04bdc-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="04bdc-106">Po uplynutí rozpočtového období a zaúčtování nákladů do Správy majetku lze také aktualizovat řádky rozpočtu skutečnými náklady.</span><span class="sxs-lookup"><span data-stu-id="04bdc-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="04bdc-107">Přepočítání rozpočtu údržby</span><span class="sxs-lookup"><span data-stu-id="04bdc-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="04bdc-108">Rozpočet údržby lze přepočítat na stránce **Řádky údržby rozpočtu**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="04bdc-109">Při přepočtu rozpočtu údržby budou stávající řádky rozpočtu odstraněny a bude proveden nový výpočet.</span><span class="sxs-lookup"><span data-stu-id="04bdc-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="04bdc-110">Na stránce **Řádky údržby rozpočtu** vyberte možnost **Přepočítat**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="04bdc-111">V dialogovém okně **Přepočítat rozpočet** proveďte požadované změny nového výpočtu a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="04bdc-112">Nové řádky rozpočtu jsou vytvořeny podle hodnot, které jste nastavili.</span><span class="sxs-lookup"><span data-stu-id="04bdc-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="04bdc-113">Upravit řádky rozpočtu</span><span class="sxs-lookup"><span data-stu-id="04bdc-113">Adjust budget lines</span></span>

<span data-ttu-id="04bdc-114">Namísto přepočítání celého rozpočtu údržby můžete upravit vybrané řádky, které se vztahují k rozpočtovým nákladům.</span><span class="sxs-lookup"><span data-stu-id="04bdc-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="04bdc-115">Na stránce **Řádků rozpočtu údržby** vyberte řádky, pro které chcete aktualizovat rozpočtové náklady.</span><span class="sxs-lookup"><span data-stu-id="04bdc-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="04bdc-116">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="04bdc-117">Chcete-li přidat částku do vybraných řádků, zaškrtněte políčko **Přidat náklady** a poté zadejte hodnotu do pole **Přidat hodnotu**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="04bdc-118">Chcete-li vynásobit rozpočtové náklady na vybraných řádcích rozpočtu podle koeficientu, zaškrtněte políčko **Vynásobit náklady** a zadejte koeficient do pole **Hodnota násobku**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="04bdc-119">Zadáte-li například **1,2** do pole **Hodnota násobku**, budou rozpočtové náklady na vybraných řádcích zvýšeny o 20 procent.</span><span class="sxs-lookup"><span data-stu-id="04bdc-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="04bdc-120">Zadáte-li **0,7**, snížíte rozpočtové náklady na vybrané řádky o 30 procent.</span><span class="sxs-lookup"><span data-stu-id="04bdc-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="04bdc-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-121">Select **OK**.</span></span>

<span data-ttu-id="04bdc-122">Vybrané řádky rozpočtu se aktualizují podle hodnot, které jste nastavili v kroku 3 nebo 4.</span><span class="sxs-lookup"><span data-stu-id="04bdc-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="04bdc-123">Aktualizovat skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04bdc-123">Update actual costs</span></span>

<span data-ttu-id="04bdc-124">Po uplynutí dat v řádcích rozpočtu a zaúčtování skutečných nákladů do Správy majetku lze také aktualizovat rozpočet údržby skutečnými náklady.</span><span class="sxs-lookup"><span data-stu-id="04bdc-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="04bdc-125">Na stránce **Řádky údržby rozpočtu** vyberte možnost **Aktualizovat náklady**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="04bdc-126">V dialogovém okně **Vypočítat skutečné náklady** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="04bdc-127">Pole **Skutečné náklady** v řádcích rozpočtu se aktualizují v případě, že byly zaúčtovány skutečné náklady.</span><span class="sxs-lookup"><span data-stu-id="04bdc-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="04bdc-128">Nové řádky rozpočtu mohou být generovány, pokud byly vytvořeny nové typy majetku od vytvoření rozpočtu a pokud byly tyto typy majetku použity pro majetek, pro který byly vytvořeny pracovní příkazy a pro které byly zaúčtovány související náklady.</span><span class="sxs-lookup"><span data-stu-id="04bdc-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="04bdc-129">Nové řádky rozpočtu zobrazují pouze skutečné náklady, protože pro ně nebyly vypočítány žádné rozpočtové náklady.</span><span class="sxs-lookup"><span data-stu-id="04bdc-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="04bdc-130">Chcete-li zobrazit přehled skutečných nákladů rozdělených na preventivní, opravné a investiční náklady, můžete provést výpočet pro stejné období na stránce **Řízení nákladů majetku**.</span><span class="sxs-lookup"><span data-stu-id="04bdc-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="04bdc-131">Přidat řádky rozpočtu ručně</span><span class="sxs-lookup"><span data-stu-id="04bdc-131">Manually add budget lines</span></span>

<span data-ttu-id="04bdc-132">Na stránce **Řádky údržby rozpočtu** můžete ručně přidat nový řádek rozpočtu výběrem možnosti **Nový** a výběrem možnosti na řádku.</span><span class="sxs-lookup"><span data-stu-id="04bdc-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="04bdc-133">Zde je několik příkladů situací, kdy může být tento přístup užitečný:</span><span class="sxs-lookup"><span data-stu-id="04bdc-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="04bdc-134">Víte, že renovace některého majetku je aktuálně ve fázi plánování, ale související úlohy ještě nebyly vytvořeny ve správě majetku.</span><span class="sxs-lookup"><span data-stu-id="04bdc-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="04bdc-135">Chcete však, aby byly rozpočtové náklady pro tyto úlohy zahrnuty do rozpočtu údržby.</span><span class="sxs-lookup"><span data-stu-id="04bdc-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="04bdc-136">Od tvorby rozpočtu údržby byl vytvořen nový majetek nebo nové typy majetku, ale plány údržby dosud nebyly nastaveny pro tento majetek nebo typy majetku.</span><span class="sxs-lookup"><span data-stu-id="04bdc-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="04bdc-137">Chcete však, aby byly rozpočtové náklady pro tyto typy majetku zahrnuty do rozpočtu údržby.</span><span class="sxs-lookup"><span data-stu-id="04bdc-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]