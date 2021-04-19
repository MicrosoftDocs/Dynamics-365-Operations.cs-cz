---
title: Správa poruch
description: Tohle téma popisuje správu poruch v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c87bfa057fd2808551674f2acb9d654ad47e9a42
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825655"
---
# <a name="fault-management"></a><span data-ttu-id="a5dd4-103">Správa poruch</span><span class="sxs-lookup"><span data-stu-id="a5dd4-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a5dd4-104">V modulu Správa majetku můžete pomocí Návrháře poruch nastavit příznaky poruch, oblasti poruch a typy poruch na typech majetku.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="a5dd4-105">Tímto způsobem lze spravovat poruchy zjištěné u majetku.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="a5dd4-106">Kromě toho mohou být v rámci pracovního příkazu registrovány příčiny poruch a návrhy na jejich opravu.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="a5dd4-107">Proces registrace a správy poruch sestává z těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="a5dd4-108">Vytvořte seznam příznaků poruch, oblastí poruch a typů poruch, které mohou nastat u vašich typů majetku.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="a5dd4-109">V Návrháři poruch nastavte příznaky, oblasti poruch a typy poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="a5dd4-110">Zde jsou uvedeny některé příklady, které vám pomohou pochopit rozdíly mezi příznaky poruch, oblastmi poruch a typy poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="a5dd4-111">**Příznaky poruch:**</span><span class="sxs-lookup"><span data-stu-id="a5dd4-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="a5dd4-112">Nevyrovnané elektrické napětí</span><span class="sxs-lookup"><span data-stu-id="a5dd4-112">Unbalanced voltages</span></span>
- <span data-ttu-id="a5dd4-113">Krátký obvod</span><span class="sxs-lookup"><span data-stu-id="a5dd4-113">Short circuit</span></span>
- <span data-ttu-id="a5dd4-114">Hluk</span><span class="sxs-lookup"><span data-stu-id="a5dd4-114">Noise</span></span>
- <span data-ttu-id="a5dd4-115">Únik kapaliny</span><span class="sxs-lookup"><span data-stu-id="a5dd4-115">Leak</span></span>
- <span data-ttu-id="a5dd4-116">Vibrace</span><span class="sxs-lookup"><span data-stu-id="a5dd4-116">Vibrations</span></span>

<span data-ttu-id="a5dd4-117">**Oblasti poruch:**</span><span class="sxs-lookup"><span data-stu-id="a5dd4-117">**Fault areas:**</span></span>

- <span data-ttu-id="a5dd4-118">Elektrická</span><span class="sxs-lookup"><span data-stu-id="a5dd4-118">Electrical</span></span>
- <span data-ttu-id="a5dd4-119">Mechanická</span><span class="sxs-lookup"><span data-stu-id="a5dd4-119">Mechanical</span></span>
- <span data-ttu-id="a5dd4-120">Hydraulická</span><span class="sxs-lookup"><span data-stu-id="a5dd4-120">Hydraulic</span></span>
- <span data-ttu-id="a5dd4-121">Pneumatická</span><span class="sxs-lookup"><span data-stu-id="a5dd4-121">Pneumatic</span></span>

<span data-ttu-id="a5dd4-122">**Typy poruch:**</span><span class="sxs-lookup"><span data-stu-id="a5dd4-122">**Fault types:**</span></span>

- <span data-ttu-id="a5dd4-123">Chybné hlavní vinutí statoru</span><span class="sxs-lookup"><span data-stu-id="a5dd4-123">Faulty main stator winding</span></span>
- <span data-ttu-id="a5dd4-124">Vadná dioda</span><span class="sxs-lookup"><span data-stu-id="a5dd4-124">Faulty diode</span></span>
- <span data-ttu-id="a5dd4-125">Znečištěné vinutí</span><span class="sxs-lookup"><span data-stu-id="a5dd4-125">Dirty windings</span></span>
- <span data-ttu-id="a5dd4-126">Chybný generátor</span><span class="sxs-lookup"><span data-stu-id="a5dd4-126">Defective generator</span></span>
- <span data-ttu-id="a5dd4-127">Vadný senzor</span><span class="sxs-lookup"><span data-stu-id="a5dd4-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="a5dd4-128">Vytvoření příznaků poruch</span><span class="sxs-lookup"><span data-stu-id="a5dd4-128">Create fault symptoms</span></span>

<span data-ttu-id="a5dd4-129">Pomocí následujících kroků vytvořte seznam příznaků, které lze použít v Návrháři poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="a5dd4-130">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Příznaky poruch**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="a5dd4-131">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a5dd4-132">Do pole **Příznak poruchy** zadejte název příznaku poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="a5dd4-133">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a5dd4-134">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="a5dd4-135">Vytvoření oblastí poruch</span><span class="sxs-lookup"><span data-stu-id="a5dd4-135">Create fault areas</span></span>

<span data-ttu-id="a5dd4-136">Pomocí následujících kroků vytvořte oblasti poruch, které lze použít v Návrháři poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="a5dd4-137">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Oblasti poruch**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="a5dd4-138">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a5dd4-139">Do pole **Oblast poruchy** zadejte název oblasti poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="a5dd4-140">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a5dd4-141">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="a5dd4-142">Vytvoření typů poruch</span><span class="sxs-lookup"><span data-stu-id="a5dd4-142">Create fault types</span></span>

<span data-ttu-id="a5dd4-143">Pomocí následujících kroků vytvořte seznam typů poruch, které lze použít v Návrháři poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="a5dd4-144">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Typy poruch**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="a5dd4-145">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a5dd4-146">Do pole **Typ poruchy** zadejte název typu poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="a5dd4-147">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a5dd4-148">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="a5dd4-149">Nastavení Návrháře poruch</span><span class="sxs-lookup"><span data-stu-id="a5dd4-149">Set up the fault designer</span></span>

<span data-ttu-id="a5dd4-150">V Návrháři poruch se nastavují údaje o poruchách pro typy majetku.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="a5dd4-151">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Návrhář poruch**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="a5dd4-152">V levém podokně vyberte typ majetku, pro který chcete nastavit záznam poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="a5dd4-153">Na záložce s náhledem **Příznak poruchy** vyberte možnost **Přidat řádek** a poté v poli **Příznak poruchy** vyberte příznak poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="a5dd4-154">Na záložce s náhledem **Oblast poruchy** vyberte možnost **Přidat řádek** a poté v poli **Oblast poruchy** vyberte oblast poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="a5dd4-155">Na záložce s náhledem **Typ poruchy** vyberte možnost **Přidat řádek** a poté v poli **Typ poruchy** vyberte typ poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="a5dd4-156">Chcete-li rychle vytvořit kombinace všech existujících příznaků, oblastí a typů poruch pro vybraný typ majetku, vyberte možnost **Vytvořit kombinace poruch**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="a5dd4-157">Tato funkce je užitečná v případě, že jste přidali mnoho příznaků, oblastí a typů poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="a5dd4-158">Je jednodušší odstranit řádky pro všechny kombinace, které nesouvisejí s typem majetku, než vytvářet nové řádky ručně.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a5dd4-159">Chcete-li zkopírovat nastavení příznaků, oblastí a typů poruch z jednoho typu majetku na vybraný typ majetku, vyberte možnost **Kopírovat z typu majetku**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="a5dd4-160">Klepnutím na tlačítko **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-160">Select **Save** to save your changes.</span></span>

![Stránka návrháře chyb](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="a5dd4-162">Vytvoření příčin poruch</span><span class="sxs-lookup"><span data-stu-id="a5dd4-162">Create fault causes</span></span>

<span data-ttu-id="a5dd4-163">Chcete-li vytvořit seznam známých příčin poruch, které lze přidat na pracovní příkaz nebo požadavek na údržbu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="a5dd4-164">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Příčiny poruch**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="a5dd4-165">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a5dd4-166">Do pole **Příčina poruchy** zadejte název příčiny poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="a5dd4-167">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a5dd4-168">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="a5dd4-169">Vytvoření náprav poruch</span><span class="sxs-lookup"><span data-stu-id="a5dd4-169">Create fault remedies</span></span>

<span data-ttu-id="a5dd4-170">Chcete-li vytvořit seznam navrhovaných náprav a oprav, které lze přidat na pracovní příkaz nebo požadavek na údržbu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="a5dd4-171">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Náprava poruch**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="a5dd4-172">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a5dd4-173">Do pole **Náprava poruchy** zadejte název nápravy poruchy.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="a5dd4-174">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a5dd4-175">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="a5dd4-176">Podle potřeby můžete změnit názvy příznaků, oblastí, typů, příčin a náprav poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="a5dd4-177">Změny názvu se automaticky projeví v souvisejících registracích poruch.</span><span class="sxs-lookup"><span data-stu-id="a5dd4-177">The name changes are automatically reflected in the related fault registrations.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]