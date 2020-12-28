---
title: Konfigurace samoobsluhy pro zaměstnance
description: V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: d1534e37e83e22dd9860de54165c062935db3798
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417682"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="95148-103">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="95148-103">Configure employee self service</span></span>

<span data-ttu-id="95148-104">V Microsoft Dynamics 365 Human Resources můžete konfigurovat dlaždice pro navigaci nejvyšší úrovní v samoobsluze pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="95148-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="95148-105">Dlaždice Plán zaměstnaneckých výhod směruje uživatele na plány zaměstnaneckých výhod, na něž mají nárok.</span><span class="sxs-lookup"><span data-stu-id="95148-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="95148-106">Nastavení dlaždice plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="95148-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="95148-107">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="95148-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="95148-108">Vyberte kartu **Nastavení dlaždice plánu zaměstnaneckých výhod** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="95148-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="95148-109">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="95148-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="95148-110">Pole</span><span class="sxs-lookup"><span data-stu-id="95148-110">Field</span></span> | <span data-ttu-id="95148-111">Popis</span><span class="sxs-lookup"><span data-stu-id="95148-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="95148-112">**ID dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-112">**Tile ID**</span></span> | <span data-ttu-id="95148-113">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="95148-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="95148-114">**Text popisku dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-114">**Tile label text**</span></span> | <span data-ttu-id="95148-115">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="95148-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="95148-116">**Popis**</span><span class="sxs-lookup"><span data-stu-id="95148-116">**Description**</span></span> | <span data-ttu-id="95148-117">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="95148-117">A description of the tile.</span></span> |
   | <span data-ttu-id="95148-118">**Internetová adresa**</span><span class="sxs-lookup"><span data-stu-id="95148-118">**Internet address**</span></span> | <span data-ttu-id="95148-119">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="95148-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="95148-120">**Velikost dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-120">**Tile size**</span></span> | <span data-ttu-id="95148-121">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="95148-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="95148-122">**Cíl**</span><span class="sxs-lookup"><span data-stu-id="95148-122">**Target**</span></span> | <span data-ttu-id="95148-123">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="95148-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="95148-124">**Obrázek pozadí dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-124">**Tile background image**</span></span> | <span data-ttu-id="95148-125">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="95148-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="95148-126">**Spuštění**</span><span class="sxs-lookup"><span data-stu-id="95148-126">**Start**</span></span> | <span data-ttu-id="95148-127">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="95148-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="95148-128">**End**</span><span class="sxs-lookup"><span data-stu-id="95148-128">**End**</span></span> | <span data-ttu-id="95148-129">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="95148-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="95148-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="95148-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="95148-131">Nastavení dlaždice plánu flexibilního kreditu</span><span class="sxs-lookup"><span data-stu-id="95148-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="95148-132">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry samoobsluhy zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="95148-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="95148-133">Vyberte kartu **Nastavení dlaždice plánu flexibilního kreditu** a poté vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="95148-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="95148-134">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="95148-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="95148-135">Pole</span><span class="sxs-lookup"><span data-stu-id="95148-135">Field</span></span> | <span data-ttu-id="95148-136">Popis</span><span class="sxs-lookup"><span data-stu-id="95148-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="95148-137">**ID dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-137">**Tile ID**</span></span> | <span data-ttu-id="95148-138">Jedinečný identifikátor pro dlaždici.</span><span class="sxs-lookup"><span data-stu-id="95148-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="95148-139">**Text popisku dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-139">**Tile label text**</span></span> | <span data-ttu-id="95148-140">Text, který se zobrazí v samoobsluze dlaždice.</span><span class="sxs-lookup"><span data-stu-id="95148-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="95148-141">**Popis**</span><span class="sxs-lookup"><span data-stu-id="95148-141">**Description**</span></span> | <span data-ttu-id="95148-142">Popis dlaždice.</span><span class="sxs-lookup"><span data-stu-id="95148-142">A description of the tile.</span></span> |
   | <span data-ttu-id="95148-143">**Internetová adresa**</span><span class="sxs-lookup"><span data-stu-id="95148-143">**Internet address**</span></span> | <span data-ttu-id="95148-144">Zadejte adresu URL samoobsluhy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="95148-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="95148-145">**Velikost dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-145">**Tile size**</span></span> | <span data-ttu-id="95148-146">Velikost dlaždice: malá, střední nebo velká.</span><span class="sxs-lookup"><span data-stu-id="95148-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="95148-147">**Cíl**</span><span class="sxs-lookup"><span data-stu-id="95148-147">**Target**</span></span> | <span data-ttu-id="95148-148">Určuje, zda se má stránka otevřít v novém okně nebo v aktuálním okně.</span><span class="sxs-lookup"><span data-stu-id="95148-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="95148-149">**Obrázek pozadí dlaždice**</span><span class="sxs-lookup"><span data-stu-id="95148-149">**Tile background image**</span></span> | <span data-ttu-id="95148-150">Adresa URL obrázku, který má být použit pro dlaždici (volitelné)</span><span class="sxs-lookup"><span data-stu-id="95148-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="95148-151">**Spuštění**</span><span class="sxs-lookup"><span data-stu-id="95148-151">**Start**</span></span> | <span data-ttu-id="95148-152">Počáteční datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="95148-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="95148-153">**End**</span><span class="sxs-lookup"><span data-stu-id="95148-153">**End**</span></span> | <span data-ttu-id="95148-154">Koncové datum a čas, kdy má být dlaždice k dispozici.</span><span class="sxs-lookup"><span data-stu-id="95148-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="95148-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="95148-155">Select **Save**.</span></span>
