---
title: Kusovníky majetku
description: Toto téma popisuje kusovníky majetku ve správě majetku.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f42646ae865cd530203c997fd10c8ccd59e7fa2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423950"
---
# <a name="asset-boms"></a><span data-ttu-id="7beae-103">Kusovníky majetku</span><span class="sxs-lookup"><span data-stu-id="7beae-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7beae-104">Toto téma popisuje kusovníky majetku ve správě majetku.</span><span class="sxs-lookup"><span data-stu-id="7beae-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="7beae-105">Stránka **Kusovník majetku** zobrazuje seznam všech položek (náhradních dílů a jiných položek), které jsou použity v majetku po celou dobu jeho životnosti.</span><span class="sxs-lookup"><span data-stu-id="7beae-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="7beae-106">Při vytváření nového majetku byste měli zvážit nastavení kusovníku majetku jako součásti postupu nastavení.</span><span class="sxs-lookup"><span data-stu-id="7beae-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="7beae-107">Tímto způsobem můžete sledovat historii položek majetku od data vytvoření.</span><span class="sxs-lookup"><span data-stu-id="7beae-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="7beae-108">Po dokončení úlohy údržby a registraci spotřeby položky na pracovním příkazu můžete sledovat spotřebu náhradních dílů a dalších položek, které jsou u majetku použity.</span><span class="sxs-lookup"><span data-stu-id="7beae-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="7beae-109">Tato funkce umožňuje uchovávat kompletní záznam spotřeby položky pro všechny majetky.</span><span class="sxs-lookup"><span data-stu-id="7beae-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="7beae-110">Pomocí tohoto záznamu můžete například sledovat, zda je určitý náhradní díl často vyměňován, nebo sledovat náhradní díly nebo jiné položky, které jsou u majetku aktuálně použity.</span><span class="sxs-lookup"><span data-stu-id="7beae-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="7beae-111">Na pracovním příkazu může spotřeba položky zahrnovat jak náhradní díly, tak i další položky, jako jsou maziva, šrouby a těsnění.</span><span class="sxs-lookup"><span data-stu-id="7beae-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="7beae-112">Kusovník majetku může být automaticky aktualizován na základě nastavení správy majetku.</span><span class="sxs-lookup"><span data-stu-id="7beae-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="7beae-113">Pokud byl stav životního cyklu pracovního příkazu vytvořen pro zpracování dokončených pracovních příkazů a pokud je možnost **Aktualizovat kusovník majetku** stav životního cyklu pracovního příkazu nastaven na **Ano** na stránce **Stav životního cyklu pracovního příkazu**, budou všechny položky použité na pracovním příkazu automaticky aktualizovány na stránce **Kusovník majetku**, když je pracovní příkaz aktualizován do tohoto stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="7beae-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="7beae-114">Můžete také ručně aktualizovat kusovník majetku vytvořením nových řádků položek na stránce **Kusovník majetku**.</span><span class="sxs-lookup"><span data-stu-id="7beae-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="7beae-115">Na stránce **Kusovník majetku** můžete sledovat historii náhradních dílů pro majetek po registraci spotřeby položky na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="7beae-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="7beae-116">Chcete-li použít tuto funkci, musíte vybrat skupiny položek, které by měly být použity pro registraci náhradních dílů na stránce **Skupiny položek náhradních dílů**.</span><span class="sxs-lookup"><span data-stu-id="7beae-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="7beae-117">Chcete-li použít funkci kusovníku majetku, musíte nejprve nastavit požadované skupiny položek náhradních dílů.</span><span class="sxs-lookup"><span data-stu-id="7beae-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="7beae-118">Pokud pak chcete, aby byl kusovník majetku po dokončení pracovního příkazu automaticky aktualizován, můžete nastavit stav životního cyklu pracovního příkazu pro zpracování této aktualizace.</span><span class="sxs-lookup"><span data-stu-id="7beae-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="7beae-119">Nastavení skupin položek náhradních dílů</span><span class="sxs-lookup"><span data-stu-id="7beae-119">Set up spare parts item groups</span></span>

<span data-ttu-id="7beae-120">Nastavení historie náhradních dílů je založeno na skupinách položek vytvořených v modulu **Řízení zásob a skladu**.</span><span class="sxs-lookup"><span data-stu-id="7beae-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="7beae-121">Ve správě majetku nastavíte skupiny položek tak, aby bylo možné sledovat historii náhradních dílů pro položky ve vybraných skupinách položek.</span><span class="sxs-lookup"><span data-stu-id="7beae-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="7beae-122">Vyberte **Sráva majetku** \> **Nastavení** \> **Majetek** \> **Skupiny položek náhradních dílů**.</span><span class="sxs-lookup"><span data-stu-id="7beae-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="7beae-123">Vyberte **Nová**, chcete-li nastavit skupinu položek.</span><span class="sxs-lookup"><span data-stu-id="7beae-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="7beae-124">V poli **Skupina položky** vyberte skupinu.</span><span class="sxs-lookup"><span data-stu-id="7beae-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="7beae-125">Název skupiny se automaticky vyplní do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="7beae-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="7beae-126">Zobrazení a aktualizace kusovníků majetku</span><span class="sxs-lookup"><span data-stu-id="7beae-126">View and update asset BOMs</span></span>

<span data-ttu-id="7beae-127">Po zaúčtování spotřeby položky na pracovním příkazu můžete zobrazit registrovanou spotřebu položky na stránce **Kusovník majetku**.</span><span class="sxs-lookup"><span data-stu-id="7beae-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="7beae-128">Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Aktivní majetek**.</span><span class="sxs-lookup"><span data-stu-id="7beae-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="7beae-129">Vyberte majetek v seznamu a pak vyberte **Kusovník majetku**.</span><span class="sxs-lookup"><span data-stu-id="7beae-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7beae-130">Chcete-li zobrazit všechny registrace spotřeby položek u veškerého majetku, vyberte **Správa majetku** \> **Dotazy** \> **Majetek** \> **Kusovník majetku**.</span><span class="sxs-lookup"><span data-stu-id="7beae-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="7beae-131">Vyberte **Aktualizovat kusovník majetku**.</span><span class="sxs-lookup"><span data-stu-id="7beae-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="7beae-132">Do aktualizace můžete přidat majetek, typy majetku a zdroje podle potřeby volbou možnosti **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="7beae-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="7beae-133">Vyberte **OK** a spusťte aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="7beae-133">Select **OK** to start the update.</span></span> <span data-ttu-id="7beae-134">Funkci aktualizace můžete také nastavit jako dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="7beae-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="7beae-135">Pokud chcete zobrazit více informací vztahujících se k položkám, můžete přidat dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="7beae-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="7beae-136">Vyberte **Zásoby** \> **Zobrazení dimenzí** a pak zaškrtněte políčka u dimenzí, které chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="7beae-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="7beae-137">Chcete-li zachovat toto nastavení pro všechen majetek na stránce **Kusovník majetku**, nastavte možnost **Uložit nastavení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7beae-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="7beae-138">Chcete-li získat přehled o tom, kde se ve správě majetku používá položka na vybraném řádku, ve vztahu k majetku, výchozím typům práce, náhradním dílům a pracovním příkazům, vyberte **Položka, kde se používá**.</span><span class="sxs-lookup"><span data-stu-id="7beae-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="7beae-139">Pokud chcete zobrazit pouze řádky aktivních položek, vyberte **Zobrazit** \> **Aktuální**.</span><span class="sxs-lookup"><span data-stu-id="7beae-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="7beae-140">Chcete-li zobrazit všechny řádky položek, včetně řádků, kde je datum vypršení platnosti dřívější než aktuální datum, vyberte **Zobrazit** \> **Vše**.</span><span class="sxs-lookup"><span data-stu-id="7beae-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="7beae-141">Po dokončení pracovního příkazu, pokud vypršela platnost některých položek nebo náhradních dílů, které souvisejí se souvisejícím majetkem nebo byly nahrazeny jinými položkami nebo náhradními díly, doporučujeme odpovídajícím způsobem aktualizovat kusovník majetku.</span><span class="sxs-lookup"><span data-stu-id="7beae-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="7beae-142">Vytvoření nového řádku položky v kusovníku majetku</span><span class="sxs-lookup"><span data-stu-id="7beae-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="7beae-143">Pro majetek můžete ručně vytvořit řádky položky.</span><span class="sxs-lookup"><span data-stu-id="7beae-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="7beae-144">Na stránce **Kusovník majetku** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="7beae-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="7beae-145">V poli **Majetek** vyberte majetek, pro který chcete přidat řádek položky.</span><span class="sxs-lookup"><span data-stu-id="7beae-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="7beae-146">Do pole **Číslo řádku** zadejte pořadové číslo řádku.</span><span class="sxs-lookup"><span data-stu-id="7beae-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="7beae-147">V poli **Platnost** zadejte počáteční datum pro položku.</span><span class="sxs-lookup"><span data-stu-id="7beae-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="7beae-148">Pokud platnost položky vyprší, zadejte do pole **Vypršení platnosti** koncové datum.</span><span class="sxs-lookup"><span data-stu-id="7beae-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="7beae-149">V poli **Číslo položky** vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="7beae-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="7beae-150">Název se automaticky vyplní do pole **Název produktu**.</span><span class="sxs-lookup"><span data-stu-id="7beae-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="7beae-151">Poté v poli **Množství** zadejte množství, které se používá.</span><span class="sxs-lookup"><span data-stu-id="7beae-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="7beae-152">Pole **Jednotka** je aktualizováno automaticky.</span><span class="sxs-lookup"><span data-stu-id="7beae-152">The **Unit** field is automatically updated.</span></span>
