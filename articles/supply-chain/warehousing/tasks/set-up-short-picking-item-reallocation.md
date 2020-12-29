---
title: Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění
description: Toto téma ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424168"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="24735-103">Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění</span><span class="sxs-lookup"><span data-stu-id="24735-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24735-104">Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován.</span><span class="sxs-lookup"><span data-stu-id="24735-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="24735-105">Proces opětovného přidělení řídí **Výjimka práce** a používá jej skladový **pracovník**.</span><span class="sxs-lookup"><span data-stu-id="24735-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="24735-106">Procesy opětovného přidělení mohou být automatické, ruční nebo obojí:</span><span class="sxs-lookup"><span data-stu-id="24735-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="24735-107">Automatické opětovné přidělení – k určení, zda je zboží k dispozici na jiném místě, se používají směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="24735-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="24735-108">Je-li to možné, práce se aktualizuje a uživatel skladu je přesměrován na alternativní umístění.</span><span class="sxs-lookup"><span data-stu-id="24735-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="24735-109">Manuální opětovné přidělení – umožňuje uživateli skladu vybrat si z jednoho nebo více skladových míst s nerezervovaným množstvím zboží.</span><span class="sxs-lookup"><span data-stu-id="24735-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="24735-110">Automatický a ruční – pokud není systém schopen provést automatické opětovné přidělení a jsou k dispozici skladová místa s nerezervovaným množstvím, bude uživatel vyzván k výběru skladového místa.</span><span class="sxs-lookup"><span data-stu-id="24735-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="24735-111">Nastavit pracovní výjimky</span><span class="sxs-lookup"><span data-stu-id="24735-111">Set up work exceptions</span></span>
<span data-ttu-id="24735-112">Je možné definovat několik pracovních výjimek práce s jinými zásadami opakovaného přidělení zboží umožňujícími zaměstnanci skladu výběr na základě potřeb dodávky, kterou zpracovávají.</span><span class="sxs-lookup"><span data-stu-id="24735-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="24735-113">K vytvoření této procedury jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="24735-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="24735-114">V **navigačním podokně** přejděte na **Řízení skladu > Nastavení > Práce > Výjimky práce**.</span><span class="sxs-lookup"><span data-stu-id="24735-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="24735-115">Klepněte na možnost **Nový**</span><span class="sxs-lookup"><span data-stu-id="24735-115">Click **New**</span></span> 
3. <span data-ttu-id="24735-116">Zadejte hodnotu do pole **Kód výjimky práce**.</span><span class="sxs-lookup"><span data-stu-id="24735-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="24735-117">Toto bude název této výjimky.</span><span class="sxs-lookup"><span data-stu-id="24735-117">This will be the title of this exception .</span></span> <span data-ttu-id="24735-118">Například Návod ke krátkodobému vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="24735-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="24735-119">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="24735-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="24735-120">Toto bude stručný popis použití této výjimky.</span><span class="sxs-lookup"><span data-stu-id="24735-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="24735-121">Například Krátkodobé vyskladnění – položka není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="24735-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="24735-122">V poli **Typ výjimky** vyberte hodnotu **Krátkodobě vyskladnit**.</span><span class="sxs-lookup"><span data-stu-id="24735-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="24735-123">Zaškrtněte políčko **Upravit zásoby**.</span><span class="sxs-lookup"><span data-stu-id="24735-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="24735-124">Je-li vybrána tato možnost, budou zásoby v místě krátkodobého vyskladnění automaticky upraveny na 0.</span><span class="sxs-lookup"><span data-stu-id="24735-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="24735-125">V poli **Výchozí kód typu úpravy** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="24735-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="24735-126">Například v USMF můžete vybrat **Odebrat Res Adj Out** . Každý kód typu úpravy obsahuje čtyři vlastnosti: název, popis, název skladového deníku a volbu **Odebrat rezervace**.</span><span class="sxs-lookup"><span data-stu-id="24735-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="24735-127">Je-li volba **Odebrat rezervace** vybrána, budou rezervace v řádku objednávky krátkodobého výdeje odstraněny.</span><span class="sxs-lookup"><span data-stu-id="24735-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="24735-128">V poli **Opakované přidělení zboží** zadejte hodnotu, například Ruční.</span><span class="sxs-lookup"><span data-stu-id="24735-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="24735-129">Pokud vyberete Ruční nebo Automatické a ruční, pracovník skladu musí mít povoleno použití ručního přerozdělení.</span><span class="sxs-lookup"><span data-stu-id="24735-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="24735-130">Nastavení pracovníka k použití ručního opakované přidělení zboží</span><span class="sxs-lookup"><span data-stu-id="24735-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="24735-131">K vytvoření této procedury jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="24735-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="24735-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="24735-132">Close the page.</span></span>
2. <span data-ttu-id="24735-133">V **Navigačním podokně** přejděte na **Řízení skladu > Nastavení > Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="24735-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="24735-134">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="24735-134">Click **Edit**.</span></span>
4. <span data-ttu-id="24735-135">Vyberte ze seznamu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="24735-135">In the list, select worker.</span></span> <span data-ttu-id="24735-136">Příklad: Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="24735-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="24735-137">Rozbalte pevnou záložku **Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="24735-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="24735-138">V seznamu vyberte **ID uživatele**.</span><span class="sxs-lookup"><span data-stu-id="24735-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="24735-139">Například 24.</span><span class="sxs-lookup"><span data-stu-id="24735-139">For example, 24.</span></span>
7. <span data-ttu-id="24735-140">Rozbalte pevnou záložku **Práce**.</span><span class="sxs-lookup"><span data-stu-id="24735-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="24735-141">Vyberte možnost **Ano** v poli **Povolit ruční opakované přidělení zboží**.</span><span class="sxs-lookup"><span data-stu-id="24735-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
