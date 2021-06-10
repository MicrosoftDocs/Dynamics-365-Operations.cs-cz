---
title: Přiřaďte ikony kroků a názvy pro mobilní aplikaci Warehouse Management
description: Toto téma popisuje, jak přiřadit ikony a názvy kroků pro nové nebo přizpůsobené toky úloh pro mobilní aplikaci Warehouse Management.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049357"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="ff7e6-103">Přiřaďte ikony kroků a názvy pro mobilní aplikaci Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="ff7e6-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff7e6-104">Toto téma popisuje, jak přiřadit ikony a názvy kroků pro nové nebo přizpůsobené toky úloh pro mobilní aplikaci Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ff7e6-105">Následující ilustrace ukazují, jak se ikony kroků a názvy zobrazují v mobilní aplikaci Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ff7e6-106">![Příklad ikony kroku a názvu kroku v mobilní aplikaci Warehouse Management](media/step-icon-example.png "Příklad ikony kroku a názvu kroku v mobilní aplikaci Warehouse Management")</span><span class="sxs-lookup"><span data-stu-id="ff7e6-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="ff7e6-107">Zapnutí funkce ve vašem systému</span><span class="sxs-lookup"><span data-stu-id="ff7e6-107">Turn on this feature in your system</span></span>

<span data-ttu-id="ff7e6-108">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ff7e6-109">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ff7e6-110">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="ff7e6-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ff7e6-111">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="ff7e6-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ff7e6-112">**Název funkce:** *Uživatelská nastavení, ikony a názvy kroků pro novou aplikaci skladu*</span><span class="sxs-lookup"><span data-stu-id="ff7e6-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="ff7e6-113">Standardní ID kroku, třídy a ikony</span><span class="sxs-lookup"><span data-stu-id="ff7e6-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="ff7e6-114">Každý krok v toku úlohy je identifikován ID kroku a každé ID kroku má odpovídající třídu kroku.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="ff7e6-115">Ikona a název kroku jsou specifikovány v každé třídě kroků.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="ff7e6-116">ID kroku a třídy kroků</span><span class="sxs-lookup"><span data-stu-id="ff7e6-116">Step IDs and step classes</span></span>

<span data-ttu-id="ff7e6-117">V následující tabulce je uvedeno každé ID kroku, které je aktuálně k dispozici, a jeho odpovídající třída kroku.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="ff7e6-118">Název kroku primárního vstupního pole se používá jako ID kroku.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="ff7e6-119">Příklad, který ukazuje, jak se tyto ID a třídy kroků používají, najdete v implementaci metody `WHSMobileAppStepInfoBuilder.stepId()` v [Příklad: Přiřaďte ikony kroků a názvy pro vlastní tok](#example) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="ff7e6-120">ID kroku</span><span class="sxs-lookup"><span data-stu-id="ff7e6-120">Step ID</span></span> | <span data-ttu-id="ff7e6-121">Třída kroků</span><span class="sxs-lookup"><span data-stu-id="ff7e6-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="ff7e6-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-122">BatchDisposition</span></span> | <span data-ttu-id="ff7e6-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="ff7e6-124">Dopravce</span><span class="sxs-lookup"><span data-stu-id="ff7e6-124">Carrier</span></span> | <span data-ttu-id="ff7e6-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="ff7e6-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="ff7e6-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-126">CatchWeight</span></span> | <span data-ttu-id="ff7e6-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff7e6-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="ff7e6-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff7e6-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff7e6-130">CatchWeightTag</span></span> | <span data-ttu-id="ff7e6-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff7e6-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ff7e6-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="ff7e6-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="ff7e6-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="ff7e6-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="ff7e6-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="ff7e6-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="ff7e6-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="ff7e6-136">CheckDigit</span></span> | <span data-ttu-id="ff7e6-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="ff7e6-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="ff7e6-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-138">ClusterId</span></span> | <span data-ttu-id="ff7e6-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="ff7e6-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="ff7e6-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ff7e6-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-142">ClusterPosition</span></span> | <span data-ttu-id="ff7e6-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="ff7e6-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-144">ConfigId</span></span> | <span data-ttu-id="ff7e6-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="ff7e6-146">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="ff7e6-146">Confirmation</span></span> | <span data-ttu-id="ff7e6-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="ff7e6-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="ff7e6-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="ff7e6-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="ff7e6-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="ff7e6-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="ff7e6-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="ff7e6-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ff7e6-154">ContainerType</span></span> | <span data-ttu-id="ff7e6-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="ff7e6-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="ff7e6-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ff7e6-156">CountingReasonCode</span></span> | <span data-ttu-id="ff7e6-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ff7e6-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="ff7e6-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="ff7e6-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="ff7e6-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="ff7e6-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="ff7e6-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="ff7e6-160">CycleCountQty1</span></span> | <span data-ttu-id="ff7e6-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff7e6-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="ff7e6-162">CycleCountQty2</span></span> | <span data-ttu-id="ff7e6-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff7e6-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="ff7e6-164">CycleCountQty3</span></span> | <span data-ttu-id="ff7e6-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff7e6-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="ff7e6-166">CycleCountQty4</span></span> | <span data-ttu-id="ff7e6-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff7e6-168">Dispozice</span><span class="sxs-lookup"><span data-stu-id="ff7e6-168">Disposition</span></span> | <span data-ttu-id="ff7e6-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="ff7e6-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="ff7e6-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="ff7e6-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-172">DriverCheckInId</span></span> | <span data-ttu-id="ff7e6-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="ff7e6-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="ff7e6-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="ff7e6-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-176">DriverCheckOutId</span></span> | <span data-ttu-id="ff7e6-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="ff7e6-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="ff7e6-178">ExpDate</span></span> | <span data-ttu-id="ff7e6-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="ff7e6-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="ff7e6-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-180">FromBatchDisposition</span></span> | <span data-ttu-id="ff7e6-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="ff7e6-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="ff7e6-182">FromInventoryStatus</span></span> | <span data-ttu-id="ff7e6-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="ff7e6-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="ff7e6-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-184">FullQty</span></span> | <span data-ttu-id="ff7e6-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="ff7e6-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-186">InboundPut</span></span> | <span data-ttu-id="ff7e6-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="ff7e6-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-188">InventBatchId</span></span> | <span data-ttu-id="ff7e6-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="ff7e6-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="ff7e6-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-190">InventColorId</span></span> | <span data-ttu-id="ff7e6-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="ff7e6-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-192">InventLocation</span></span> | <span data-ttu-id="ff7e6-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="ff7e6-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-194">InventLocationId</span></span> | <span data-ttu-id="ff7e6-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="ff7e6-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="ff7e6-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-196">InventSerialId</span></span> | <span data-ttu-id="ff7e6-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="ff7e6-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-198">InventSizeId</span></span> | <span data-ttu-id="ff7e6-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="ff7e6-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-200">InventStatusId</span></span> | <span data-ttu-id="ff7e6-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="ff7e6-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="ff7e6-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-202">InventStyleId</span></span> | <span data-ttu-id="ff7e6-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="ff7e6-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-204">InventVersionId</span></span> | <span data-ttu-id="ff7e6-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="ff7e6-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-206">ItemId</span></span> | <span data-ttu-id="ff7e6-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="ff7e6-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="ff7e6-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-208">ITMContainerID</span></span> | <span data-ttu-id="ff7e6-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="ff7e6-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-210">ITMShipmentID</span></span> | <span data-ttu-id="ff7e6-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="ff7e6-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-212">KanbanCardId</span></span> | <span data-ttu-id="ff7e6-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="ff7e6-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ff7e6-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="ff7e6-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="ff7e6-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-216">KanbanOrCardId</span></span> | <span data-ttu-id="ff7e6-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="ff7e6-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ff7e6-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-218">LicensePlateId</span></span> | <span data-ttu-id="ff7e6-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="ff7e6-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="ff7e6-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-220">LoadId</span></span> | <span data-ttu-id="ff7e6-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="ff7e6-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="ff7e6-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="ff7e6-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-224">LocOrLP</span></span> | <span data-ttu-id="ff7e6-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="ff7e6-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="ff7e6-226">LocOrLP_From</span></span> | <span data-ttu-id="ff7e6-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="ff7e6-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="ff7e6-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="ff7e6-228">LocOrLP_To</span></span> | <span data-ttu-id="ff7e6-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="ff7e6-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="ff7e6-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ff7e6-230">LocOrLPCheck</span></span> | <span data-ttu-id="ff7e6-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ff7e6-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="ff7e6-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-232">LocVerification</span></span> | <span data-ttu-id="ff7e6-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="ff7e6-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ff7e6-234">LPAdjustIn</span></span> | <span data-ttu-id="ff7e6-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ff7e6-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="ff7e6-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-236">LPBreakChildLP</span></span> | <span data-ttu-id="ff7e6-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="ff7e6-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-238">LPBreakParentLP</span></span> | <span data-ttu-id="ff7e6-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="ff7e6-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-240">LPBuildChildLP</span></span> | <span data-ttu-id="ff7e6-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="ff7e6-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-242">LPBuildParentLP</span></span> | <span data-ttu-id="ff7e6-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="ff7e6-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-244">LPVerification</span></span> | <span data-ttu-id="ff7e6-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="ff7e6-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-246">MergeContainerId</span></span> | <span data-ttu-id="ff7e6-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="ff7e6-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-248">MixedLPLineNum</span></span> | <span data-ttu-id="ff7e6-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="ff7e6-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="ff7e6-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="ff7e6-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="ff7e6-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="ff7e6-252">MovementConfirmCancel</span></span> | <span data-ttu-id="ff7e6-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="ff7e6-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="ff7e6-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-254">NewCaptureWeight</span></span> | <span data-ttu-id="ff7e6-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff7e6-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-256">NewQty</span></span> | <span data-ttu-id="ff7e6-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="ff7e6-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff7e6-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="ff7e6-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff7e6-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ff7e6-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-260">OutboundPut</span></span> | <span data-ttu-id="ff7e6-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="ff7e6-262">Odchozí hmotnost</span><span class="sxs-lookup"><span data-stu-id="ff7e6-262">OutboundWeight</span></span> | <span data-ttu-id="ff7e6-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff7e6-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-264">OverridePutNewLocation</span></span> | <span data-ttu-id="ff7e6-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="ff7e6-266">Potvrzení PieceByPiece</span><span class="sxs-lookup"><span data-stu-id="ff7e6-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="ff7e6-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ff7e6-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-268">POLineNum</span></span> | <span data-ttu-id="ff7e6-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="ff7e6-270">Číslo nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="ff7e6-270">PONum</span></span> | <span data-ttu-id="ff7e6-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="ff7e6-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="ff7e6-272">PositionFull</span></span> | <span data-ttu-id="ff7e6-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="ff7e6-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="ff7e6-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-274">PositionFullQty</span></span> | <span data-ttu-id="ff7e6-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="ff7e6-276">Obsah</span><span class="sxs-lookup"><span data-stu-id="ff7e6-276">Potency</span></span> | <span data-ttu-id="ff7e6-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="ff7e6-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="ff7e6-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="ff7e6-278">PrinterName</span></span> | <span data-ttu-id="ff7e6-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="ff7e6-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="ff7e6-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-280">ProdId</span></span> | <span data-ttu-id="ff7e6-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="ff7e6-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="ff7e6-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="ff7e6-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-284">ProductConfirmation</span></span> | <span data-ttu-id="ff7e6-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="ff7e6-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="ff7e6-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="ff7e6-288">Vložit</span><span class="sxs-lookup"><span data-stu-id="ff7e6-288">Put</span></span> | <span data-ttu-id="ff7e6-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="ff7e6-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-290">PutawayClusterId</span></span> | <span data-ttu-id="ff7e6-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="ff7e6-292">Množství</span><span class="sxs-lookup"><span data-stu-id="ff7e6-292">Qty</span></span> | <span data-ttu-id="ff7e6-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="ff7e6-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ff7e6-294">QtyAdjust</span></span> | <span data-ttu-id="ff7e6-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ff7e6-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ff7e6-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="ff7e6-296">QtyShort</span></span> | <span data-ttu-id="ff7e6-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="ff7e6-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="ff7e6-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ff7e6-298">QtyToConsume</span></span> | <span data-ttu-id="ff7e6-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ff7e6-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="ff7e6-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="ff7e6-300">QtyToPick</span></span> | <span data-ttu-id="ff7e6-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="ff7e6-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="ff7e6-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-302">QtyToPut</span></span> | <span data-ttu-id="ff7e6-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="ff7e6-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ff7e6-304">QtyToScrap</span></span> | <span data-ttu-id="ff7e6-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ff7e6-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="ff7e6-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-306">QtyVerification</span></span> | <span data-ttu-id="ff7e6-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ff7e6-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="ff7e6-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="ff7e6-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ff7e6-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ff7e6-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="ff7e6-310">ReasonString</span></span> | <span data-ttu-id="ff7e6-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="ff7e6-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="ff7e6-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-312">RecvLocationId</span></span> | <span data-ttu-id="ff7e6-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="ff7e6-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-314">RemoveContainerId</span></span> | <span data-ttu-id="ff7e6-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="ff7e6-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="ff7e6-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="ff7e6-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-318">RMANum</span></span> | <span data-ttu-id="ff7e6-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="ff7e6-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ff7e6-320">ShortPickReason</span></span> | <span data-ttu-id="ff7e6-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ff7e6-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="ff7e6-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-322">SortConOrLP</span></span> | <span data-ttu-id="ff7e6-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="ff7e6-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-324">SortLicensePlateId</span></span> | <span data-ttu-id="ff7e6-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="ff7e6-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-326">SortPositionId</span></span> | <span data-ttu-id="ff7e6-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="ff7e6-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-328">SortVerification</span></span> | <span data-ttu-id="ff7e6-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="ff7e6-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="ff7e6-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-330">StartLocationId</span></span> | <span data-ttu-id="ff7e6-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="ff7e6-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="ff7e6-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="ff7e6-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-334">TargetLicensePlateId</span></span> | <span data-ttu-id="ff7e6-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="ff7e6-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-336">TOLineNum</span></span> | <span data-ttu-id="ff7e6-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="ff7e6-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-338">ToLocation</span></span> | <span data-ttu-id="ff7e6-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="ff7e6-340">Do čísla</span><span class="sxs-lookup"><span data-stu-id="ff7e6-340">TONum</span></span> | <span data-ttu-id="ff7e6-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="ff7e6-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="ff7e6-342">ToWarehouse</span></span> | <span data-ttu-id="ff7e6-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="ff7e6-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="ff7e6-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-344">TransportLoadId</span></span> | <span data-ttu-id="ff7e6-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="ff7e6-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-346">WaveLabelId</span></span> | <span data-ttu-id="ff7e6-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="ff7e6-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-348">WaveLblQty</span></span> | <span data-ttu-id="ff7e6-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="ff7e6-350">Váha</span><span class="sxs-lookup"><span data-stu-id="ff7e6-350">Weight</span></span> | <span data-ttu-id="ff7e6-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="ff7e6-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ff7e6-352">WeightToConsume</span></span> | <span data-ttu-id="ff7e6-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ff7e6-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="ff7e6-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ff7e6-354">WHSAdjustmentType</span></span> | <span data-ttu-id="ff7e6-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ff7e6-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="ff7e6-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ff7e6-356">WHSReceivingException</span></span> | <span data-ttu-id="ff7e6-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ff7e6-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="ff7e6-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="ff7e6-358">WHSWorkException</span></span> | <span data-ttu-id="ff7e6-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="ff7e6-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="ff7e6-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="ff7e6-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="ff7e6-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-362">WMSLocationId</span></span> | <span data-ttu-id="ff7e6-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="ff7e6-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-364">WorkId</span></span> | <span data-ttu-id="ff7e6-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="ff7e6-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ff7e6-366">WorkIdToCancel</span></span> | <span data-ttu-id="ff7e6-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ff7e6-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="ff7e6-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ff7e6-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="ff7e6-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ff7e6-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="ff7e6-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-370">WorkPoolId</span></span> | <span data-ttu-id="ff7e6-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="ff7e6-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-372">ZoneId</span></span> | <span data-ttu-id="ff7e6-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="ff7e6-374">Ikony dostupných kroků</span><span class="sxs-lookup"><span data-stu-id="ff7e6-374">Available step icons</span></span>

<span data-ttu-id="ff7e6-375">Systém obsahuje kolekci ikon standardních kroků, které můžete také použít pro vlastní kroky.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="ff7e6-376">Momentálně nemůžete nahrát vlastní ikony kroků.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="ff7e6-377">Proto musíte vždy vybrat jednu ze standardních ikon kroků.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="ff7e6-378">Následující tabulka ukazuje každou ikonu standardního kroku, která je aktuálně k dispozici, a její název.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Ikona O kroku"><br><span data-ttu-id="ff7e6-380">O prognóze</span><span class="sxs-lookup"><span data-stu-id="ff7e6-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Přidat registrační značku nebo ikonu kroku položky"><br><span data-ttu-id="ff7e6-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="ff7e6-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Ikona kroku dávkové dispozice"><br><span data-ttu-id="ff7e6-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Ikona kroku dopravce"><br><span data-ttu-id="ff7e6-386">Dopravce</span><span class="sxs-lookup"><span data-stu-id="ff7e6-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Ikona kroku značky skutečné hmotnosti"><br><span data-ttu-id="ff7e6-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff7e6-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Ikona kroku hmotnosti značky skutečné hmotnosti"><br><span data-ttu-id="ff7e6-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Ikona kroku kontrolní číslice"><br><span data-ttu-id="ff7e6-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="ff7e6-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Ikona kroku ID přihlášení nebo odhlášení"><br><span data-ttu-id="ff7e6-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Ikona kroku podřízené registrační značky"><br><span data-ttu-id="ff7e6-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Ikona kroku ID clusteru"><br><span data-ttu-id="ff7e6-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Ikona kroku pozice clusteru"><br><span data-ttu-id="ff7e6-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Ikona kroku ID konfigurace"><br><span data-ttu-id="ff7e6-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Ikona kroku nakonfigurovaného pole"><br><span data-ttu-id="ff7e6-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="ff7e6-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Ikona kroku kon. nebo reg. zn."><br><span data-ttu-id="ff7e6-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Ikona kroku Konsolidace z ID registrační značky"><br><span data-ttu-id="ff7e6-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Ikona kroku Konsolidace do ID registrační značky"><br><span data-ttu-id="ff7e6-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Ikona kroku typu kontejneru"><br><span data-ttu-id="ff7e6-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ff7e6-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Ikona kroku inventura"><br><span data-ttu-id="ff7e6-414">Inventura</span><span class="sxs-lookup"><span data-stu-id="ff7e6-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Ikona kroku kód důvodu inventury"><br><span data-ttu-id="ff7e6-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ff7e6-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Ikona kroku kódu země původu"><br><span data-ttu-id="ff7e6-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="ff7e6-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Ikona kroku dispozice"><br><span data-ttu-id="ff7e6-420">Dispozice</span><span class="sxs-lookup"><span data-stu-id="ff7e6-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Ikona kroku hotovo"><br><span data-ttu-id="ff7e6-422">Hotovo</span><span class="sxs-lookup"><span data-stu-id="ff7e6-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Ikona kroku potvrzení přihlášení ovladače"><br><span data-ttu-id="ff7e6-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Ikona kroku ID přihlášení ovladače"><br><span data-ttu-id="ff7e6-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Ikona kroku ID odhlášení ovladače"><br><span data-ttu-id="ff7e6-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Ikona kroku data vypršení platnosti"><br><span data-ttu-id="ff7e6-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="ff7e6-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Ikona kroku pole"><br><span data-ttu-id="ff7e6-432">Pole</span><span class="sxs-lookup"><span data-stu-id="ff7e6-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Ikona kroku z dávkové dispozice"><br><span data-ttu-id="ff7e6-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Ikona kroku ze stavu inventáře"><br><span data-ttu-id="ff7e6-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="ff7e6-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Ikona kroku atributu ID"><br><span data-ttu-id="ff7e6-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="ff7e6-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Ikona kroku ID dávky zásob"><br><span data-ttu-id="ff7e6-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Ikona kroku ID barvy zásob"><br><span data-ttu-id="ff7e6-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Ikona kroku umístění zásob"><br><span data-ttu-id="ff7e6-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Ikona kroku ID sériových zásob"><br><span data-ttu-id="ff7e6-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Ikona kroku ID velikosti zásob"><br><span data-ttu-id="ff7e6-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Ikona kroku ID stavu zásob"><br><span data-ttu-id="ff7e6-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Ikona kroku ID stylu zásob"><br><span data-ttu-id="ff7e6-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Ikona kroku ID verze zásob"><br><span data-ttu-id="ff7e6-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Ikona kroku ID položky"><br><span data-ttu-id="ff7e6-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Ikona kroku ID kontejneru ITM"><br><span data-ttu-id="ff7e6-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Ikona kroku ID zásilky ITM"><br><span data-ttu-id="ff7e6-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Ikona kroku ID karty Kanban"><br><span data-ttu-id="ff7e6-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Ikona kroku ID kanbanu nebo karty"><br><span data-ttu-id="ff7e6-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Ikona kroku ID registrační značky"><br><span data-ttu-id="ff7e6-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Ikona kroku ID nákladu"><br><span data-ttu-id="ff7e6-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Ikona ktoku umístění registrační značky místa"><br><span data-ttu-id="ff7e6-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ff7e6-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Ikona kroku umístění nebo registrační značky"><br><span data-ttu-id="ff7e6-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Ikona kroku kontrola umístění nebo registrační značky"><br><span data-ttu-id="ff7e6-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ff7e6-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Ikona kroku z umístění nebo registrační značky"><br><span data-ttu-id="ff7e6-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="ff7e6-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Ikona kroku do umístění nebo registrační značky"><br><span data-ttu-id="ff7e6-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="ff7e6-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Ikona dokončeného kroku dlouhého procesu"><br><span data-ttu-id="ff7e6-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="ff7e6-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Ikona kroku přešení reg. zn. nadřazené reg. zn."><br><span data-ttu-id="ff7e6-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Ikona kroku ID sloučení kontejneru"><br><span data-ttu-id="ff7e6-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Ikona kroku číslo řádku smíšené registrační značky"><br><span data-ttu-id="ff7e6-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Ikona kroku odchozí hmotnosti"><br><span data-ttu-id="ff7e6-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ff7e6-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Ikona kroku vlastníka"><br><span data-ttu-id="ff7e6-490">Vlastník</span><span class="sxs-lookup"><span data-stu-id="ff7e6-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Ikona kroku nadřazené registrační značky"><br><span data-ttu-id="ff7e6-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="ff7e6-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Potvrďte prosím ikonu kroku"><br><span data-ttu-id="ff7e6-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="ff7e6-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Ikona kroku čísla řádku nákupní objednávky"><br><span data-ttu-id="ff7e6-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Ikona kroku čísla nákupní objednávky"><br><span data-ttu-id="ff7e6-498">Číslo nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="ff7e6-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Ikona kroku plné pozice"><br><span data-ttu-id="ff7e6-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="ff7e6-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Ikona kroku koncentrace"><br><span data-ttu-id="ff7e6-502">Obsah</span><span class="sxs-lookup"><span data-stu-id="ff7e6-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Ikona kroku názvu tiskárny"><br><span data-ttu-id="ff7e6-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="ff7e6-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Ikona kroku ID prod."><br><span data-ttu-id="ff7e6-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Ikona kroku potvrzení produktu"><br><span data-ttu-id="ff7e6-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Ikona kroku vložit"><br><span data-ttu-id="ff7e6-510">Vložit</span><span class="sxs-lookup"><span data-stu-id="ff7e6-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Ikona kroku IDseskupení vyskladnění"><br><span data-ttu-id="ff7e6-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Ikona kroku množství"><br><span data-ttu-id="ff7e6-514">Množství</span><span class="sxs-lookup"><span data-stu-id="ff7e6-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Ikona kroku úpravy množství"><br><span data-ttu-id="ff7e6-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ff7e6-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Ikona krátkého kroku množství"><br><span data-ttu-id="ff7e6-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="ff7e6-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Ikona kroku množství ke spotřebě"><br><span data-ttu-id="ff7e6-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ff7e6-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Ikona kroku množství k vložení"><br><span data-ttu-id="ff7e6-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="ff7e6-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Ikona kroku množství k likvidaci"><br><span data-ttu-id="ff7e6-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ff7e6-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Ikona kroku potvrzení množství"><br><span data-ttu-id="ff7e6-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Ikona kroku Nahlásit dokončení úlohy"><br><span data-ttu-id="ff7e6-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="ff7e6-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Ikona kroku ID místa příjmu"><br><span data-ttu-id="ff7e6-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Ikona kroku ID odebrání kontejneru"><br><span data-ttu-id="ff7e6-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Ikona kroku čísla RMA"><br><span data-ttu-id="ff7e6-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Ikona kroku výběr objednávky"><br><span data-ttu-id="ff7e6-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="ff7e6-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Ikona kroku důvod krátkého výdeje"><br><span data-ttu-id="ff7e6-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ff7e6-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Ikona kroku ID pozice třídění"><br><span data-ttu-id="ff7e6-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Ikona kroku ID cílové registrační značky"><br><span data-ttu-id="ff7e6-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Ikona ktoku čísla řádku příjmu"><br><span data-ttu-id="ff7e6-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Ikona kroku umístění příjmu"><br><span data-ttu-id="ff7e6-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="ff7e6-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Ikona kroku čísla příjmu"><br><span data-ttu-id="ff7e6-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="ff7e6-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Ikona kroku skladu příjmu"><br><span data-ttu-id="ff7e6-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="ff7e6-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Ikona kroku ID dopravy nákladu"><br><span data-ttu-id="ff7e6-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Ikona kroku ID dávky dodavatele"><br><span data-ttu-id="ff7e6-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Ikona kroku ID štítku vlny"><br><span data-ttu-id="ff7e6-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Ikona kroku množství štítku vlny"><br><span data-ttu-id="ff7e6-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ff7e6-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Ikona kroku hmotnosti"><br><span data-ttu-id="ff7e6-560">Váha</span><span class="sxs-lookup"><span data-stu-id="ff7e6-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Ikona kroku hmostnosti ke spotřebě"><br><span data-ttu-id="ff7e6-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ff7e6-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Ikona kroku typu úpravy WHS"><br><span data-ttu-id="ff7e6-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ff7e6-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Ikona kroku výjimky přijetí WHS"><br><span data-ttu-id="ff7e6-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ff7e6-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Ikona kroku ID umístění WMS"><br><span data-ttu-id="ff7e6-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Ikona kroku ID práce"><br><span data-ttu-id="ff7e6-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Ikona kroku ID práce ke zrušení"><br><span data-ttu-id="ff7e6-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ff7e6-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Ikona kroku ID registrační značky práce"><br><span data-ttu-id="ff7e6-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff7e6-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Ikona kroku ID seskupení výdeje registrační značky práce"><br><span data-ttu-id="ff7e6-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ff7e6-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Ikona kroku ID fondu práce"><br><span data-ttu-id="ff7e6-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Ikona kroku ID zóny"><br><span data-ttu-id="ff7e6-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="ff7e6-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="ff7e6-581">Příklad: Přiřaďte ikony kroků a názvy pro vlastní tok</span><span class="sxs-lookup"><span data-stu-id="ff7e6-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="ff7e6-582">Tento příklad vysvětluje, jak nastavit ikony a názvy kroků pro vlastní tok úkolů.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="ff7e6-583">Scénář je postaven na příkladu vlastního toku úloh, který je podrobněji představen a prozkoumán v následujícím příspěvku na blogu: [Přizpůsobení mobilní aplikace Warehousing](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="ff7e6-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="ff7e6-584">Tok úloh funguje následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="ff7e6-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="ff7e6-585">Aplikace zobrazuje stránku, která pracovníka vyzve k poskytnutí ID kontejneru (například skenováním čárového kódu).</span><span class="sxs-lookup"><span data-stu-id="ff7e6-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="ff7e6-586">Pokud je ID kontejneru platné, aplikace otevře novou stránku, která pracovníka vyzve k zadání hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="ff7e6-587">(Pokud ID kontejneru není platné, pracovník se vrátí na první stránku.)</span><span class="sxs-lookup"><span data-stu-id="ff7e6-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="ff7e6-588">Když pracovník zadá platnou hmotnost, systém váhu uloží a vrátí pracovníka na první stránku.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="ff7e6-589">Následující obrázek znázorňuje tento tok úloh.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="ff7e6-590">![Vývojový diagram úkolu](media/step-icons-example-task-flow.png "Vývojový diagram úkolu")</span><span class="sxs-lookup"><span data-stu-id="ff7e6-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="ff7e6-591">Vytvořte třídu kroků pro vstupní stránku kontejneru</span><span class="sxs-lookup"><span data-stu-id="ff7e6-591">Create a step class for the container input page</span></span>

<span data-ttu-id="ff7e6-592">Na vstupní stránce kontejneru může pracovník skenovat nebo zadat ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="ff7e6-593">![Stránka vstupu do kontejneru](media/step-icons-example-container-input.png "Stránka vstupu do kontejneru")</span><span class="sxs-lookup"><span data-stu-id="ff7e6-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="ff7e6-594">Na vstupní stránce kontejneru je název ovládacího prvku vstupního pole `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="ff7e6-595">Protože tento název ovládacího prvku není v [seznamu ID kroků](#step-ids-classes), nenajdete existující krok, který je na něm založen.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="ff7e6-596">Proto musíte vytvořit třídu kroku, která představuje krok.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="ff7e6-597">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="ff7e6-598">Identifikátor ikony kroku je uložen v členu třídy `defaultStepIcon` a název kroku je uložen v členu třídy `defaultStepTitle`.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="ff7e6-599">Chcete-li přiřadit ikonu kroku, nastavte `defaultStepIcon` na jedno z ID ikon, které jsou uvedeny v sekci [Dostupné ikony kroků](#step-icons) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="ff7e6-600">Pro zadání hmotnosti použijte standardní nebo vlastní ikonu a název kroku</span><span class="sxs-lookup"><span data-stu-id="ff7e6-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="ff7e6-601">Stránka pro zadání hmotnosti umožňuje pracovníkovi zadat hmotnost.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="ff7e6-602">![Stránka pro zadání hmotnosti](media/step-icons-example-weight-input.png "Stránka pro zadání hmotnosti")</span><span class="sxs-lookup"><span data-stu-id="ff7e6-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="ff7e6-603">Na stránce pro zadávání hmotnosti je název ovládacího prvku vstupního pole `Weight`, které je v [seznamu ID kroků](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="ff7e6-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="ff7e6-604">Pokud tedy ikona a název kroku, které jsou definovány v třídě `WHSMobileAppStepWeight`, jsou pro vás přijatelné, pro tento krok nemusíte nic měnit.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="ff7e6-605">Pokud však v tomto kroku dáváte přednost použití jiné ikony nebo názvu, můžete přepsat buď metodu `stepId()` nebo `stepInfo()` ve třídě tvůrce.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="ff7e6-606">Každý tok úloh má svůj vlastní nástroj pro vytváření informací o krocích.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="ff7e6-607">Přepsat metodu stepId ()</span><span class="sxs-lookup"><span data-stu-id="ff7e6-607">Override the stepId() method</span></span>

<span data-ttu-id="ff7e6-608">Následující příklad ukazuje jeden způsob, kterým můžete upravit třídu tvůrce přepsáním metody `stepId()`.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="ff7e6-609">Potom vytvoříte třídu kroků pro krok `NewWeight`.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="ff7e6-610">Kód by měl vypadat jako kód pro příklad `ContainerId`, který byl uveden dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="ff7e6-611">Přepsat metodu stepInfo()</span><span class="sxs-lookup"><span data-stu-id="ff7e6-611">Override the stepInfo() method</span></span>

<span data-ttu-id="ff7e6-612">Následující příklad ukazuje jeden způsob, kterým můžete upravit třídu tvůrce přepsáním metody `stepInfo()`.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="ff7e6-613">Potom vytvoříte objekt `WHSMobileAppStepInfo` a přímo nastavíte ikonu a/nebo název.</span><span class="sxs-lookup"><span data-stu-id="ff7e6-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff7e6-614">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ff7e6-614">Additional resources</span></span>

- [<span data-ttu-id="ff7e6-615">Instalace a připojení mobilní aplikace Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="ff7e6-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="ff7e6-616">Uživatelská nastavení mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="ff7e6-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
