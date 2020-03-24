---
title: Konfigurace samoobsluhy pro zaměstnance
description: V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092653"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="d636e-103">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="d636e-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d636e-104">V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d636e-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="d636e-105">Dlaždice Plán zaměstnaneckých výhod směruje uživatele na plány zaměstnaneckých výhod, k nimž mají nárok se zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="d636e-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="d636e-106">Nastavení centrální dlaždice role</span><span class="sxs-lookup"><span data-stu-id="d636e-106">Set up a role center tile</span></span>

1. <span data-ttu-id="d636e-107">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="d636e-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d636e-108">Vyberte kartu **Nastavení prostřední dlaždice role** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d636e-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d636e-109">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="d636e-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d636e-110">Pole</span><span class="sxs-lookup"><span data-stu-id="d636e-110">Field</span></span> | <span data-ttu-id="d636e-111">Popis</span><span class="sxs-lookup"><span data-stu-id="d636e-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d636e-112">ID dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-112">Tile ID</span></span> | <span data-ttu-id="d636e-113">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="d636e-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d636e-114">Text popisku dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-114">Tile label text</span></span> | <span data-ttu-id="d636e-115">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="d636e-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d636e-116">Popis</span><span class="sxs-lookup"><span data-stu-id="d636e-116">Description</span></span> | <span data-ttu-id="d636e-117">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="d636e-117">A description of the tile.</span></span> |
   | <span data-ttu-id="d636e-118">Internetová adresa</span><span class="sxs-lookup"><span data-stu-id="d636e-118">Internet address</span></span> | <span data-ttu-id="d636e-119">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d636e-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d636e-120">Velikost dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-120">Tile size</span></span> | <span data-ttu-id="d636e-121">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="d636e-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d636e-122">Cíl</span><span class="sxs-lookup"><span data-stu-id="d636e-122">Target</span></span> | <span data-ttu-id="d636e-123">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="d636e-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d636e-124">Obrázek pozadí dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-124">Tile background image</span></span> | <span data-ttu-id="d636e-125">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="d636e-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d636e-126">Spuštění</span><span class="sxs-lookup"><span data-stu-id="d636e-126">Start</span></span> | <span data-ttu-id="d636e-127">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d636e-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d636e-128">End</span><span class="sxs-lookup"><span data-stu-id="d636e-128">End</span></span> | <span data-ttu-id="d636e-129">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d636e-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d636e-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d636e-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="d636e-131">Nastavení dlaždice plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d636e-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="d636e-132">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="d636e-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d636e-133">Vyberte kartu **Nastavení dlaždice plánu zaměstnaneckých výhod** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d636e-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d636e-134">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="d636e-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d636e-135">Pole</span><span class="sxs-lookup"><span data-stu-id="d636e-135">Field</span></span> | <span data-ttu-id="d636e-136">Popis</span><span class="sxs-lookup"><span data-stu-id="d636e-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d636e-137">ID dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-137">Tile ID</span></span> | <span data-ttu-id="d636e-138">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="d636e-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d636e-139">Text popisku dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-139">Tile label text</span></span> | <span data-ttu-id="d636e-140">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="d636e-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d636e-141">Popis</span><span class="sxs-lookup"><span data-stu-id="d636e-141">Description</span></span> | <span data-ttu-id="d636e-142">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="d636e-142">A description of the tile.</span></span> |
   | <span data-ttu-id="d636e-143">Internetová adresa</span><span class="sxs-lookup"><span data-stu-id="d636e-143">Internet address</span></span> | <span data-ttu-id="d636e-144">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d636e-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d636e-145">Velikost dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-145">Tile size</span></span> | <span data-ttu-id="d636e-146">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="d636e-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d636e-147">Cíl</span><span class="sxs-lookup"><span data-stu-id="d636e-147">Target</span></span> | <span data-ttu-id="d636e-148">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="d636e-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d636e-149">Obrázek pozadí dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-149">Tile background image</span></span> | <span data-ttu-id="d636e-150">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="d636e-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d636e-151">Spuštění</span><span class="sxs-lookup"><span data-stu-id="d636e-151">Start</span></span> | <span data-ttu-id="d636e-152">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d636e-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d636e-153">End</span><span class="sxs-lookup"><span data-stu-id="d636e-153">End</span></span> | <span data-ttu-id="d636e-154">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d636e-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d636e-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d636e-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="d636e-156">Nastavení dlaždice plánu flexibilního kreditu</span><span class="sxs-lookup"><span data-stu-id="d636e-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="d636e-157">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="d636e-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d636e-158">Vyberte kartu **Nastavení dlaždice plánu flexibilního kreditu** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d636e-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d636e-159">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="d636e-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d636e-160">Pole</span><span class="sxs-lookup"><span data-stu-id="d636e-160">Field</span></span> | <span data-ttu-id="d636e-161">Popis</span><span class="sxs-lookup"><span data-stu-id="d636e-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d636e-162">ID dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-162">Tile ID</span></span> | <span data-ttu-id="d636e-163">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="d636e-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d636e-164">Text popisku dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-164">Tile label text</span></span> | <span data-ttu-id="d636e-165">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="d636e-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d636e-166">Popis</span><span class="sxs-lookup"><span data-stu-id="d636e-166">Description</span></span> | <span data-ttu-id="d636e-167">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="d636e-167">A description of the tile.</span></span> |
   | <span data-ttu-id="d636e-168">Internetová adresa</span><span class="sxs-lookup"><span data-stu-id="d636e-168">Internet address</span></span> | <span data-ttu-id="d636e-169">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d636e-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d636e-170">Velikost dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-170">Tile size</span></span> | <span data-ttu-id="d636e-171">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="d636e-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d636e-172">Cíl</span><span class="sxs-lookup"><span data-stu-id="d636e-172">Target</span></span> | <span data-ttu-id="d636e-173">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="d636e-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d636e-174">Obrázek pozadí dlaždice</span><span class="sxs-lookup"><span data-stu-id="d636e-174">Tile background image</span></span> | <span data-ttu-id="d636e-175">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="d636e-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d636e-176">Spuštění</span><span class="sxs-lookup"><span data-stu-id="d636e-176">Start</span></span> | <span data-ttu-id="d636e-177">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d636e-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d636e-178">End</span><span class="sxs-lookup"><span data-stu-id="d636e-178">End</span></span> | <span data-ttu-id="d636e-179">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d636e-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d636e-180">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d636e-180">Select **Save**.</span></span>
