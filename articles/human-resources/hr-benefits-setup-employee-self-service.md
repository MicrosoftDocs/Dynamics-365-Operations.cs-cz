---
title: Konfigurace samoobsluhy pro zaměstnance
description: V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32981812eac3c08e1409fe5470b550e421f5d6c9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111778"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="af018-103">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="af018-103">Configure employee self service</span></span>

<span data-ttu-id="af018-104">V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="af018-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="af018-105">Dlaždice Plán zaměstnaneckých výhod směruje uživatele na plány zaměstnaneckých výhod, na něž mají nárok.</span><span class="sxs-lookup"><span data-stu-id="af018-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="af018-106">Nastavení dlaždice plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="af018-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="af018-107">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="af018-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="af018-108">Vyberte kartu **Nastavení dlaždice plánu zaměstnaneckých výhod** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="af018-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="af018-109">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="af018-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="af018-110">Pole</span><span class="sxs-lookup"><span data-stu-id="af018-110">Field</span></span> | <span data-ttu-id="af018-111">Popis</span><span class="sxs-lookup"><span data-stu-id="af018-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="af018-112">**ID dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-112">**Tile ID**</span></span> | <span data-ttu-id="af018-113">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="af018-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="af018-114">**Text popisku dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-114">**Tile label text**</span></span> | <span data-ttu-id="af018-115">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="af018-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="af018-116">**Popis**</span><span class="sxs-lookup"><span data-stu-id="af018-116">**Description**</span></span> | <span data-ttu-id="af018-117">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="af018-117">A description of the tile.</span></span> |
   | <span data-ttu-id="af018-118">**Internetová adresa**</span><span class="sxs-lookup"><span data-stu-id="af018-118">**Internet address**</span></span> | <span data-ttu-id="af018-119">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="af018-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="af018-120">**Velikost dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-120">**Tile size**</span></span> | <span data-ttu-id="af018-121">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="af018-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="af018-122">**Cíl**</span><span class="sxs-lookup"><span data-stu-id="af018-122">**Target**</span></span> | <span data-ttu-id="af018-123">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="af018-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="af018-124">**Obrázek pozadí dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-124">**Tile background image**</span></span> | <span data-ttu-id="af018-125">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="af018-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="af018-126">**Spuštění**</span><span class="sxs-lookup"><span data-stu-id="af018-126">**Start**</span></span> | <span data-ttu-id="af018-127">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="af018-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="af018-128">**End**</span><span class="sxs-lookup"><span data-stu-id="af018-128">**End**</span></span> | <span data-ttu-id="af018-129">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="af018-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="af018-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="af018-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="af018-131">Nastavení dlaždice plánu flexibilního kreditu</span><span class="sxs-lookup"><span data-stu-id="af018-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="af018-132">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="af018-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="af018-133">Vyberte kartu **Nastavení dlaždice plánu flexibilního kreditu** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="af018-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="af018-134">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="af018-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="af018-135">Pole</span><span class="sxs-lookup"><span data-stu-id="af018-135">Field</span></span> | <span data-ttu-id="af018-136">Popis</span><span class="sxs-lookup"><span data-stu-id="af018-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="af018-137">**ID dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-137">**Tile ID**</span></span> | <span data-ttu-id="af018-138">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="af018-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="af018-139">**Text popisku dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-139">**Tile label text**</span></span> | <span data-ttu-id="af018-140">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="af018-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="af018-141">**Popis**</span><span class="sxs-lookup"><span data-stu-id="af018-141">**Description**</span></span> | <span data-ttu-id="af018-142">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="af018-142">A description of the tile.</span></span> |
   | <span data-ttu-id="af018-143">**Internetová adresa**</span><span class="sxs-lookup"><span data-stu-id="af018-143">**Internet address**</span></span> | <span data-ttu-id="af018-144">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="af018-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="af018-145">**Velikost dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-145">**Tile size**</span></span> | <span data-ttu-id="af018-146">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="af018-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="af018-147">**Cíl**</span><span class="sxs-lookup"><span data-stu-id="af018-147">**Target**</span></span> | <span data-ttu-id="af018-148">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="af018-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="af018-149">**Obrázek pozadí dlaždice**</span><span class="sxs-lookup"><span data-stu-id="af018-149">**Tile background image**</span></span> | <span data-ttu-id="af018-150">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="af018-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="af018-151">**Spuštění**</span><span class="sxs-lookup"><span data-stu-id="af018-151">**Start**</span></span> | <span data-ttu-id="af018-152">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="af018-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="af018-153">**End**</span><span class="sxs-lookup"><span data-stu-id="af018-153">**End**</span></span> | <span data-ttu-id="af018-154">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="af018-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="af018-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="af018-155">Select **Save**.</span></span>
