---
title: Konfigurace samoobsluhy pro zaměstnance
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008365"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="50575-102">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="50575-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="50575-103">V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="50575-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="50575-104">Dlaždice Plán zaměstnaneckých výhod směruje uživatele na plány zaměstnaneckých výhod, k nimž mají nárok se zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="50575-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="50575-105">Nastavení centrální dlaždice role</span><span class="sxs-lookup"><span data-stu-id="50575-105">Set up a role center tile</span></span>

1. <span data-ttu-id="50575-106">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="50575-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="50575-107">Vyberte kartu **Nastavení prostřední dlaždice role** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="50575-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="50575-108">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="50575-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="50575-109">Pole</span><span class="sxs-lookup"><span data-stu-id="50575-109">Field</span></span> | <span data-ttu-id="50575-110">Popis</span><span class="sxs-lookup"><span data-stu-id="50575-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="50575-111">ID dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-111">Tile ID</span></span> | <span data-ttu-id="50575-112">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="50575-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="50575-113">Text popisku dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-113">Tile label text</span></span> | <span data-ttu-id="50575-114">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="50575-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="50575-115">Popis</span><span class="sxs-lookup"><span data-stu-id="50575-115">Description</span></span> | <span data-ttu-id="50575-116">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="50575-116">A description of the tile.</span></span> |
   | <span data-ttu-id="50575-117">Internetová adresa</span><span class="sxs-lookup"><span data-stu-id="50575-117">Internet address</span></span> | <span data-ttu-id="50575-118">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="50575-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="50575-119">Velikost dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-119">Tile size</span></span> | <span data-ttu-id="50575-120">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="50575-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="50575-121">Cíl</span><span class="sxs-lookup"><span data-stu-id="50575-121">Target</span></span> | <span data-ttu-id="50575-122">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="50575-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="50575-123">Obrázek pozadí dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-123">Tile background image</span></span> | <span data-ttu-id="50575-124">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="50575-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="50575-125">Spuštění</span><span class="sxs-lookup"><span data-stu-id="50575-125">Start</span></span> | <span data-ttu-id="50575-126">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="50575-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="50575-127">End</span><span class="sxs-lookup"><span data-stu-id="50575-127">End</span></span> | <span data-ttu-id="50575-128">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="50575-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="50575-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="50575-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="50575-130">Nastavení dlaždice plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="50575-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="50575-131">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="50575-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="50575-132">Vyberte kartu **Nastavení dlaždice plánu zaměstnaneckých výhod** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="50575-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="50575-133">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="50575-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="50575-134">Pole</span><span class="sxs-lookup"><span data-stu-id="50575-134">Field</span></span> | <span data-ttu-id="50575-135">Popis</span><span class="sxs-lookup"><span data-stu-id="50575-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="50575-136">ID dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-136">Tile ID</span></span> | <span data-ttu-id="50575-137">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="50575-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="50575-138">Text popisku dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-138">Tile label text</span></span> | <span data-ttu-id="50575-139">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="50575-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="50575-140">Popis</span><span class="sxs-lookup"><span data-stu-id="50575-140">Description</span></span> | <span data-ttu-id="50575-141">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="50575-141">A description of the tile.</span></span> |
   | <span data-ttu-id="50575-142">Internetová adresa</span><span class="sxs-lookup"><span data-stu-id="50575-142">Internet address</span></span> | <span data-ttu-id="50575-143">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="50575-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="50575-144">Velikost dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-144">Tile size</span></span> | <span data-ttu-id="50575-145">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="50575-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="50575-146">Cíl</span><span class="sxs-lookup"><span data-stu-id="50575-146">Target</span></span> | <span data-ttu-id="50575-147">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="50575-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="50575-148">Obrázek pozadí dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-148">Tile background image</span></span> | <span data-ttu-id="50575-149">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="50575-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="50575-150">Spuštění</span><span class="sxs-lookup"><span data-stu-id="50575-150">Start</span></span> | <span data-ttu-id="50575-151">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="50575-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="50575-152">End</span><span class="sxs-lookup"><span data-stu-id="50575-152">End</span></span> | <span data-ttu-id="50575-153">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="50575-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="50575-154">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="50575-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="50575-155">Nastavení dlaždice plánu flexibilního kreditu</span><span class="sxs-lookup"><span data-stu-id="50575-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="50575-156">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="50575-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="50575-157">Vyberte kartu **Nastavení dlaždice plánu flexibilního kreditu** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="50575-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="50575-158">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="50575-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="50575-159">Pole</span><span class="sxs-lookup"><span data-stu-id="50575-159">Field</span></span> | <span data-ttu-id="50575-160">Popis</span><span class="sxs-lookup"><span data-stu-id="50575-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="50575-161">ID dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-161">Tile ID</span></span> | <span data-ttu-id="50575-162">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="50575-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="50575-163">Text popisku dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-163">Tile label text</span></span> | <span data-ttu-id="50575-164">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="50575-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="50575-165">Popis</span><span class="sxs-lookup"><span data-stu-id="50575-165">Description</span></span> | <span data-ttu-id="50575-166">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="50575-166">A description of the tile.</span></span> |
   | <span data-ttu-id="50575-167">Internetová adresa</span><span class="sxs-lookup"><span data-stu-id="50575-167">Internet address</span></span> | <span data-ttu-id="50575-168">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="50575-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="50575-169">Velikost dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-169">Tile size</span></span> | <span data-ttu-id="50575-170">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="50575-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="50575-171">Cíl</span><span class="sxs-lookup"><span data-stu-id="50575-171">Target</span></span> | <span data-ttu-id="50575-172">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="50575-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="50575-173">Obrázek pozadí dlaždice</span><span class="sxs-lookup"><span data-stu-id="50575-173">Tile background image</span></span> | <span data-ttu-id="50575-174">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="50575-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="50575-175">Spuštění</span><span class="sxs-lookup"><span data-stu-id="50575-175">Start</span></span> | <span data-ttu-id="50575-176">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="50575-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="50575-177">End</span><span class="sxs-lookup"><span data-stu-id="50575-177">End</span></span> | <span data-ttu-id="50575-178">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="50575-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="50575-179">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="50575-179">Select **Save**.</span></span>
