---
title: Vytvoření rozpočtů údržby
description: Toto téma vysvětluje, jak vytvořit rozpočet údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 593a03e3317de5759427dfc61093530c4b7ef7e9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253487"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="61917-103">Vytvoření rozpočtů údržby</span><span class="sxs-lookup"><span data-stu-id="61917-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="61917-104">Rozpočty údržby se používají k poskytnutí přehledu o očekávaných nákladech pro preventivní údržbu.</span><span class="sxs-lookup"><span data-stu-id="61917-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="61917-105">Řádky rozpočtu jsou vypočítány na základě řádků plánu údržby, které mají očekávané počáteční datum během rozpočtového období.</span><span class="sxs-lookup"><span data-stu-id="61917-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="61917-106">Rozpočty údržby jsou založeny na typech nákladů, které se používají ve správě majetku: **Preventivní** **Opravný** a **Investice**.</span><span class="sxs-lookup"><span data-stu-id="61917-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="61917-107">Rozpočtové náklady na údržbu investic jsou zahrnuty pro aktivní majetek, který má datum náhrady během rozpočtového období a související náhradní hodnotu.</span><span class="sxs-lookup"><span data-stu-id="61917-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="61917-108">Rozpočtové náklady na opravnou údržbu jsou zahrnuty v případě, že do výpočtu rozpočtu bude zahrnuto dřívější opravné datum.</span><span class="sxs-lookup"><span data-stu-id="61917-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="61917-109">V takovém případě se opravné náklady z předchozího období vypočítávají pro stejné budoucí období, pro které počítáte rozpočet údržby.</span><span class="sxs-lookup"><span data-stu-id="61917-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="61917-110">Vytvoření rozpočtu údržby</span><span class="sxs-lookup"><span data-stu-id="61917-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="61917-111">Vyberte **Správa majetku** \> **Dotazy** \> **Rozpočet údržby** \> **Rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="61917-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="61917-112">Zvolte **Vytvořit rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="61917-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="61917-113">Do pole **Rozpočet údržby** zadejte ID rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="61917-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="61917-114">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="61917-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="61917-115">Na záložce s náhledem **Období** zadejte do polí **Od data** a **Do data** počáteční a koncová data rozpočtového období.</span><span class="sxs-lookup"><span data-stu-id="61917-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="61917-116">Chcete-li zahrnout opravné rozpočtové náklady, které jsou vypočteny na základě skutečných nákladů z předchozího období, zadejte do pole **Opravné od data** počáteční datum období, ze kterého by tyto náklady měly být zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="61917-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="61917-117">V závislosti na úrovni podrobností, které jsou v rozpočtu požadovány, nastavte na pěti záložkách s náhledem **Seskupit podle** příslušné možnosti.</span><span class="sxs-lookup"><span data-stu-id="61917-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="61917-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="61917-118">Select **OK**.</span></span>
8. <span data-ttu-id="61917-119">Vyberte **Řádky rozpočtu** pro otevření stránky **Řádky rozpočtu údržby**, kde můžete zobrazit všechny řádky rozpočtu, které byly vytvořeny pro dané období.</span><span class="sxs-lookup"><span data-stu-id="61917-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="61917-120">Chcete-li rozpočet schválit, vyberte jej na stránce **Rozpočty údržby** a poté vyberte **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="61917-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="61917-121">Poté v dialogovém okně **Schválit rozpočet** vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="61917-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="61917-122">Vaše jméno je zadáno v poli **Schválil/a** na stránce **Rozpočty údržby**.</span><span class="sxs-lookup"><span data-stu-id="61917-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="61917-123">Po schválení rozpočtu údržby nelze přepočítat nebo upravit související řádky na stránce **Řádky rozpočtu údržby**, pokud jste nejprve neodebrali schválení.</span><span class="sxs-lookup"><span data-stu-id="61917-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="61917-124">Chcete-li odstranit schválení rozpočtu údržby, vyberte jej na stránce **Rozpočty údržby** a poté vyberte **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="61917-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="61917-125">Poté v dialogovém okně **Schválit rozpočet** vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="61917-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Rozpočty údržby](media/01-maintenance-budgets.png)

<span data-ttu-id="61917-127">Nový rozpočet údržby můžete také vytvořit zkopírováním existujícího rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="61917-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="61917-128">Na stránce **Rozpočty údržby** vyberte rozpočet, který chcete kopírovat, a poté vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="61917-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="61917-129">Tento přístup je užitečný, pokud jste například vytvořili rozpočet na jeden měsíc a chcete jej zkopírovat do dalších měsíců.</span><span class="sxs-lookup"><span data-stu-id="61917-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="61917-130">Rozpočet údržby vypočítá pouze rozpočtové náklady založené na řádcích rozvrhu údržby.</span><span class="sxs-lookup"><span data-stu-id="61917-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="61917-131">Chcete-li vypočítat skutečné náklady pro stejné období, můžete provést výpočet na stránce **Kontrola nákladů majetku**.</span><span class="sxs-lookup"><span data-stu-id="61917-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]