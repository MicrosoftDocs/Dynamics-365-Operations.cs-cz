---
title: Vytvoření nového rozvržení skladu
description: Toto téma popisuje, jak nastavit informace o umístění ve skladu.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07fee1787cc2719bafbe2bb6d54849edda14018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000027"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="829b0-103">Vytvoření nového rozvržení skladu</span><span class="sxs-lookup"><span data-stu-id="829b0-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="829b0-104">Toto téma popisuje, jak nastavit informace o umístění ve skladu.</span><span class="sxs-lookup"><span data-stu-id="829b0-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="829b0-105">To platí pouze pro sklady vytvořené pomocí "základních funkcí skladu" v modulu Řízení zásob, ne pro sklady, které jsou vytvořeny v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="829b0-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="829b0-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="829b0-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="829b0-107">Nastavte výchozí kapacitu skladového místa</span><span class="sxs-lookup"><span data-stu-id="829b0-107">Set the default location capacity</span></span>
1. <span data-ttu-id="829b0-108">V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Parametry řízení zásob a skladu**.</span><span class="sxs-lookup"><span data-stu-id="829b0-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="829b0-109">Vyberte karu **Umístění**.</span><span class="sxs-lookup"><span data-stu-id="829b0-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="829b0-110">V poli **Standardní šířka** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="829b0-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="829b0-111">V poli **Standardní hloubka** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="829b0-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="829b0-112">V poli **Standardní výška** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="829b0-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="829b0-113">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="829b0-113">Select **Save**.</span></span>
7. <span data-ttu-id="829b0-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="829b0-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="829b0-115">Definujte formát názvu skladového místa</span><span class="sxs-lookup"><span data-stu-id="829b0-115">Define the location name format</span></span>
1. <span data-ttu-id="829b0-116">V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Rozdělení zásob > Sklady**.</span><span class="sxs-lookup"><span data-stu-id="829b0-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="829b0-117">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="829b0-117">Select **New**.</span></span>
3. <span data-ttu-id="829b0-118">Zadejte hodnotu do pole **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="829b0-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="829b0-119">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="829b0-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="829b0-120">V poli **Pracoviště** vyberte požadovaný záznam ve vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="829b0-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="829b0-121">Přepněte rozšíření oddílu **Názvy umístění**.</span><span class="sxs-lookup"><span data-stu-id="829b0-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="829b0-122">Možnosti v tomto oddílu definují výchozí formát pro názvy umístění.</span><span class="sxs-lookup"><span data-stu-id="829b0-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="829b0-123">V našem příkladu použijeme čísla uličky, stojanu a police.</span><span class="sxs-lookup"><span data-stu-id="829b0-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="829b0-124">Nastavte možnost **Včetně uličky** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="829b0-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="829b0-125">Nastavte možnost **Včetně stojanu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="829b0-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="829b0-126">V poli **Formát** zadejte hodnotu pro stojan.</span><span class="sxs-lookup"><span data-stu-id="829b0-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="829b0-127">Nastavte možnost **Včetně police** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="829b0-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="829b0-128">V poli **Formát** zadejte pro polici hodnotu.</span><span class="sxs-lookup"><span data-stu-id="829b0-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="829b0-129">Definujte umístění ve skladu</span><span class="sxs-lookup"><span data-stu-id="829b0-129">Define warehouse locations</span></span>
1. <span data-ttu-id="829b0-130">V podokně akcí zvolte **Sklady**.</span><span class="sxs-lookup"><span data-stu-id="829b0-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="829b0-131">Zvolte **Průvodce skladovým místem**.</span><span class="sxs-lookup"><span data-stu-id="829b0-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="829b0-132">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="829b0-132">Select **Next**.</span></span>
4. <span data-ttu-id="829b0-133">Zrušte výběr možnosti **Výstupní překladiště**</span><span class="sxs-lookup"><span data-stu-id="829b0-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="829b0-134">Zrušte výběr možnosti **Hromadné umístění**</span><span class="sxs-lookup"><span data-stu-id="829b0-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="829b0-135">Vyberte **Další**, dokud nepřejdete na možnost **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="829b0-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="829b0-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="829b0-136">Close the page.</span></span>
8. <span data-ttu-id="829b0-137">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="829b0-137">Refresh the page.</span></span>

