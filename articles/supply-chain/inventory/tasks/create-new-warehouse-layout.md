---
title: Vytvoření nového rozvržení skladu
description: Toto téma popisuje, jak nastavit informace o umístění ve skladu.
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a329df85c339c90e4bdc620c8a63837ebc19a7c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833970"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="3df6c-103">Vytvoření nového rozvržení skladu</span><span class="sxs-lookup"><span data-stu-id="3df6c-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3df6c-104">Toto téma popisuje, jak nastavit informace o umístění ve skladu.</span><span class="sxs-lookup"><span data-stu-id="3df6c-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="3df6c-105">To platí pouze pro sklady vytvořené pomocí "základních funkcí skladu" v modulu Řízení zásob, ne pro sklady, které jsou vytvořeny v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="3df6c-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="3df6c-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="3df6c-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="3df6c-107">Nastavte výchozí kapacitu skladového místa</span><span class="sxs-lookup"><span data-stu-id="3df6c-107">Set the default location capacity</span></span>
1. <span data-ttu-id="3df6c-108">V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Parametry řízení zásob a skladu**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="3df6c-109">Vyberte karu **Umístění**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="3df6c-110">V poli **Standardní šířka** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="3df6c-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="3df6c-111">V poli **Standardní hloubka** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="3df6c-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="3df6c-112">V poli **Standardní výška** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="3df6c-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="3df6c-113">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-113">Select **Save**.</span></span>
7. <span data-ttu-id="3df6c-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3df6c-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="3df6c-115">Definujte formát názvu skladového místa</span><span class="sxs-lookup"><span data-stu-id="3df6c-115">Define the location name format</span></span>
1. <span data-ttu-id="3df6c-116">V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Rozdělení zásob > Sklady**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="3df6c-117">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-117">Select **New**.</span></span>
3. <span data-ttu-id="3df6c-118">Zadejte hodnotu do pole **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="3df6c-119">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="3df6c-120">V poli **Pracoviště** vyberte požadovaný záznam ve vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="3df6c-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="3df6c-121">Přepněte rozšíření oddílu **Názvy umístění**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="3df6c-122">Možnosti v tomto oddílu definují výchozí formát pro názvy umístění.</span><span class="sxs-lookup"><span data-stu-id="3df6c-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="3df6c-123">V našem příkladu použijeme čísla uličky, stojanu a police.</span><span class="sxs-lookup"><span data-stu-id="3df6c-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="3df6c-124">Nastavte možnost **Včetně uličky** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="3df6c-125">Nastavte možnost **Včetně stojanu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="3df6c-126">V poli **Formát** zadejte hodnotu pro stojan.</span><span class="sxs-lookup"><span data-stu-id="3df6c-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="3df6c-127">Nastavte možnost **Včetně police** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="3df6c-128">V poli **Formát** zadejte pro polici hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3df6c-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="3df6c-129">Definujte umístění ve skladu</span><span class="sxs-lookup"><span data-stu-id="3df6c-129">Define warehouse locations</span></span>
1. <span data-ttu-id="3df6c-130">V podokně akcí zvolte **Sklady**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="3df6c-131">Zvolte **Průvodce skladovým místem**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="3df6c-132">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-132">Select **Next**.</span></span>
4. <span data-ttu-id="3df6c-133">Zrušte výběr možnosti **Výstupní překladiště**</span><span class="sxs-lookup"><span data-stu-id="3df6c-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="3df6c-134">Zrušte výběr možnosti **Hromadné umístění**</span><span class="sxs-lookup"><span data-stu-id="3df6c-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="3df6c-135">Vyberte **Další**, dokud nepřejdete na možnost **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="3df6c-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="3df6c-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3df6c-136">Close the page.</span></span>
8. <span data-ttu-id="3df6c-137">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="3df6c-137">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]