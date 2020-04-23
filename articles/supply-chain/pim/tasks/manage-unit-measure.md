---
title: Správa měrných jednotek
description: Tento postup popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7f7e2220a8eca9f9bf45216491f606ef0a2eb18
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203517"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="efe81-103">Správa měrných jednotek</span><span class="sxs-lookup"><span data-stu-id="efe81-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efe81-104">Tento postup popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek.</span><span class="sxs-lookup"><span data-stu-id="efe81-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="efe81-105">Tento postup můžete projít pomocí ukázkových dat společnosti nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="efe81-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="efe81-106">Přejděte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Údržba uvolněného produktu**.</span><span class="sxs-lookup"><span data-stu-id="efe81-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="efe81-107">Klikněte na možnost **Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="efe81-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="efe81-108">Vytvoření měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="efe81-108">Create a unit of measure</span></span>
1. <span data-ttu-id="efe81-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="efe81-109">Click **New**.</span></span>
2. <span data-ttu-id="efe81-110">Do pole **Jednotka** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="efe81-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="efe81-111">Zadejte ID nebo symbol pro použití při odkazování na měrnou jednotku.</span><span class="sxs-lookup"><span data-stu-id="efe81-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="efe81-112">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="efe81-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="efe81-113">Zadejte popisný název měrné jednotky v systémovém jazyce.</span><span class="sxs-lookup"><span data-stu-id="efe81-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="efe81-114">V poli **Třída jednotek** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="efe81-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="efe81-115">Třída jednotek určuje, do jakého logického seskupení, například do oblasti, hmotnosti nebo množství, měrná jednotka patří.</span><span class="sxs-lookup"><span data-stu-id="efe81-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="efe81-116">V poli **Desetinná přesnost** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="efe81-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="efe81-117">Určete počet desetinných míst, na který má být převedená měrná jednotka zaokrouhlena při dokončení výpočtu pro měrnou jednotku.</span><span class="sxs-lookup"><span data-stu-id="efe81-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="efe81-118">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="efe81-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="efe81-119">Definování překladů jednotek</span><span class="sxs-lookup"><span data-stu-id="efe81-119">Define unit translations</span></span>
1. <span data-ttu-id="efe81-120">V **podokně akcí** klikněte na možnost **Texty jednotek**.</span><span class="sxs-lookup"><span data-stu-id="efe81-120">On the **Action pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="efe81-121">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="efe81-121">Click **New**.</span></span> <span data-ttu-id="efe81-122">Text jednotky použijte k vytvoření překladu ID nebo symbolu představujícího měrnou jednotku pro použití u externích dokumentů v jazycích odběratele nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efe81-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="efe81-123">V poli **Jazyk** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="efe81-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="efe81-124">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="efe81-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="efe81-125">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="efe81-125">Click **Save**.</span></span>
6. <span data-ttu-id="efe81-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="efe81-126">Close the page.</span></span>
7. <span data-ttu-id="efe81-127">V **podokně akcí** klikněte na možnost **Popisy přeložené jednotky**.</span><span class="sxs-lookup"><span data-stu-id="efe81-127">On the **Action pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="efe81-128">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="efe81-128">Click **New**.</span></span> <span data-ttu-id="efe81-129">Definujte popisy měrné jednotky pro daný jazyk.</span><span class="sxs-lookup"><span data-stu-id="efe81-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="efe81-130">V poli **Jazyk** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="efe81-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="efe81-131">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="efe81-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="efe81-132">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="efe81-132">Click **Save**.</span></span>
12. <span data-ttu-id="efe81-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="efe81-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="efe81-134">Definování pravidel pro převod jednotek</span><span class="sxs-lookup"><span data-stu-id="efe81-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="efe81-135">V **podokně akcí** klikněte na možnost **Převody jednotek**.</span><span class="sxs-lookup"><span data-stu-id="efe81-135">On the **Action pane**, click **Unit conversions**.</span></span> <span data-ttu-id="efe81-136">Definujte pravidla pro převod měrné jednotky do a z jiných měrných jednotek ve vybrané třídě jednotky.</span><span class="sxs-lookup"><span data-stu-id="efe81-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="efe81-137">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="efe81-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="efe81-138">Do pole **Koeficient** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="efe81-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="efe81-139">Koeficient převodu mezi hodnotou Z jednotky a Do jednotky.</span><span class="sxs-lookup"><span data-stu-id="efe81-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="efe81-140">Například koeficient převodu centimetrů na metry je 100, protože v jednom metru je 100 centimetrů.</span><span class="sxs-lookup"><span data-stu-id="efe81-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="efe81-141">V poli **Do jednotky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="efe81-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="efe81-142">Vyberte možnost v poli **Zaokrouhlení**.</span><span class="sxs-lookup"><span data-stu-id="efe81-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="efe81-143">Definujte, jak má být převedená hodnota zaokrouhlena.</span><span class="sxs-lookup"><span data-stu-id="efe81-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="efe81-144">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="efe81-144">Click **OK**.</span></span>
7. <span data-ttu-id="efe81-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="efe81-145">Close the page.</span></span>

