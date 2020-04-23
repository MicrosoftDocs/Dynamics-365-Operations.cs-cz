---
title: Správa poruch
description: Tohle téma popisuje správu poruch v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6665e80342af1baa7176aee92693b77e83b368f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205913"
---
# <a name="fault-management"></a><span data-ttu-id="f8381-103">Správa poruch</span><span class="sxs-lookup"><span data-stu-id="f8381-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f8381-104">V modulu Správa majetku můžete pomocí Návrháře poruch nastavit příznaky poruch, oblasti poruch a typy poruch na typech majetku.</span><span class="sxs-lookup"><span data-stu-id="f8381-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="f8381-105">Tímto způsobem lze spravovat poruchy zjištěné u majetku.</span><span class="sxs-lookup"><span data-stu-id="f8381-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="f8381-106">Kromě toho mohou být v rámci pracovního příkazu registrovány příčiny poruch a návrhy na jejich opravu.</span><span class="sxs-lookup"><span data-stu-id="f8381-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="f8381-107">Proces registrace a správy poruch sestává z těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="f8381-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="f8381-108">Vytvořte seznam příznaků poruch, oblastí poruch a typů poruch, které mohou nastat u vašich typů majetku.</span><span class="sxs-lookup"><span data-stu-id="f8381-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="f8381-109">V Návrháři poruch nastavte příznaky, oblasti poruch a typy poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="f8381-110">Zde jsou uvedeny některé příklady, které vám pomohou pochopit rozdíly mezi příznaky poruch, oblastmi poruch a typy poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="f8381-111">**Příznaky poruch:**</span><span class="sxs-lookup"><span data-stu-id="f8381-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="f8381-112">Nevyrovnané elektrické napětí</span><span class="sxs-lookup"><span data-stu-id="f8381-112">Unbalanced voltages</span></span>
- <span data-ttu-id="f8381-113">Krátký obvod</span><span class="sxs-lookup"><span data-stu-id="f8381-113">Short circuit</span></span>
- <span data-ttu-id="f8381-114">Hluk</span><span class="sxs-lookup"><span data-stu-id="f8381-114">Noise</span></span>
- <span data-ttu-id="f8381-115">Únik kapaliny</span><span class="sxs-lookup"><span data-stu-id="f8381-115">Leak</span></span>
- <span data-ttu-id="f8381-116">Vibrace</span><span class="sxs-lookup"><span data-stu-id="f8381-116">Vibrations</span></span>

<span data-ttu-id="f8381-117">**Oblasti poruch:**</span><span class="sxs-lookup"><span data-stu-id="f8381-117">**Fault areas:**</span></span>

- <span data-ttu-id="f8381-118">Elektrická</span><span class="sxs-lookup"><span data-stu-id="f8381-118">Electrical</span></span>
- <span data-ttu-id="f8381-119">Mechanická</span><span class="sxs-lookup"><span data-stu-id="f8381-119">Mechanical</span></span>
- <span data-ttu-id="f8381-120">Hydraulická</span><span class="sxs-lookup"><span data-stu-id="f8381-120">Hydraulic</span></span>
- <span data-ttu-id="f8381-121">Pneumatická</span><span class="sxs-lookup"><span data-stu-id="f8381-121">Pneumatic</span></span>

<span data-ttu-id="f8381-122">**Typy poruch:**</span><span class="sxs-lookup"><span data-stu-id="f8381-122">**Fault types:**</span></span>

- <span data-ttu-id="f8381-123">Chybné hlavní vinutí statoru</span><span class="sxs-lookup"><span data-stu-id="f8381-123">Faulty main stator winding</span></span>
- <span data-ttu-id="f8381-124">Vadná dioda</span><span class="sxs-lookup"><span data-stu-id="f8381-124">Faulty diode</span></span>
- <span data-ttu-id="f8381-125">Znečištěné vinutí</span><span class="sxs-lookup"><span data-stu-id="f8381-125">Dirty windings</span></span>
- <span data-ttu-id="f8381-126">Chybný generátor</span><span class="sxs-lookup"><span data-stu-id="f8381-126">Defective generator</span></span>
- <span data-ttu-id="f8381-127">Vadný senzor</span><span class="sxs-lookup"><span data-stu-id="f8381-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="f8381-128">Vytvoření příznaků poruch</span><span class="sxs-lookup"><span data-stu-id="f8381-128">Create fault symptoms</span></span>

<span data-ttu-id="f8381-129">Pomocí následujících kroků vytvořte seznam příznaků, které lze použít v Návrháři poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f8381-130">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Příznaky poruch**.</span><span class="sxs-lookup"><span data-stu-id="f8381-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="f8381-131">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="f8381-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f8381-132">Do pole **Příznak poruchy** zadejte název příznaku poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="f8381-133">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f8381-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f8381-134">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f8381-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="f8381-135">Vytvoření oblastí poruch</span><span class="sxs-lookup"><span data-stu-id="f8381-135">Create fault areas</span></span>

<span data-ttu-id="f8381-136">Pomocí následujících kroků vytvořte oblasti poruch, které lze použít v Návrháři poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f8381-137">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Oblasti poruch**.</span><span class="sxs-lookup"><span data-stu-id="f8381-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="f8381-138">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="f8381-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f8381-139">Do pole **Oblast poruchy** zadejte název oblasti poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="f8381-140">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f8381-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f8381-141">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f8381-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="f8381-142">Vytvoření typů poruch</span><span class="sxs-lookup"><span data-stu-id="f8381-142">Create fault types</span></span>

<span data-ttu-id="f8381-143">Pomocí následujících kroků vytvořte seznam typů poruch, které lze použít v Návrháři poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f8381-144">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Typy poruch**.</span><span class="sxs-lookup"><span data-stu-id="f8381-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="f8381-145">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="f8381-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f8381-146">Do pole **Typ poruchy** zadejte název typu poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="f8381-147">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f8381-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f8381-148">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f8381-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="f8381-149">Nastavení Návrháře poruch</span><span class="sxs-lookup"><span data-stu-id="f8381-149">Set up the fault designer</span></span>

<span data-ttu-id="f8381-150">V Návrháři poruch se nastavují údaje o poruchách pro typy majetku.</span><span class="sxs-lookup"><span data-stu-id="f8381-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="f8381-151">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Návrhář poruch**.</span><span class="sxs-lookup"><span data-stu-id="f8381-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="f8381-152">V levém podokně vyberte typ majetku, pro který chcete nastavit záznam poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="f8381-153">Na záložce s náhledem **Příznak poruchy** vyberte možnost **Přidat řádek** a poté v poli **Příznak poruchy** vyberte příznak poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="f8381-154">Na záložce s náhledem **Oblast poruchy** vyberte možnost **Přidat řádek** a poté v poli **Oblast poruchy** vyberte oblast poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="f8381-155">Na záložce s náhledem **Typ poruchy** vyberte možnost **Přidat řádek** a poté v poli **Typ poruchy** vyberte typ poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="f8381-156">Chcete-li rychle vytvořit kombinace všech existujících příznaků, oblastí a typů poruch pro vybraný typ majetku, vyberte možnost **Vytvořit kombinace poruch**.</span><span class="sxs-lookup"><span data-stu-id="f8381-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="f8381-157">Tato funkce je užitečná v případě, že jste přidali mnoho příznaků, oblastí a typů poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="f8381-158">Je jednodušší odstranit řádky pro všechny kombinace, které nesouvisejí s typem majetku, než vytvářet nové řádky ručně.</span><span class="sxs-lookup"><span data-stu-id="f8381-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8381-159">Chcete-li zkopírovat nastavení příznaků, oblastí a typů poruch z jednoho typu majetku na vybraný typ majetku, vyberte možnost **Kopírovat z typu majetku**.</span><span class="sxs-lookup"><span data-stu-id="f8381-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="f8381-160">Klepnutím na tlačítko **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="f8381-160">Select **Save** to save your changes.</span></span>

![Stránka návrháře chyb](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="f8381-162">Vytvoření příčin poruch</span><span class="sxs-lookup"><span data-stu-id="f8381-162">Create fault causes</span></span>

<span data-ttu-id="f8381-163">Chcete-li vytvořit seznam známých příčin poruch, které lze přidat na pracovní příkaz nebo požadavek na údržbu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="f8381-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="f8381-164">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Příčiny poruch**.</span><span class="sxs-lookup"><span data-stu-id="f8381-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="f8381-165">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="f8381-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f8381-166">Do pole **Příčina poruchy** zadejte název příčiny poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="f8381-167">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f8381-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f8381-168">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f8381-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="f8381-169">Vytvoření náprav poruch</span><span class="sxs-lookup"><span data-stu-id="f8381-169">Create fault remedies</span></span>

<span data-ttu-id="f8381-170">Chcete-li vytvořit seznam navrhovaných náprav a oprav, které lze přidat na pracovní příkaz nebo požadavek na údržbu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="f8381-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="f8381-171">Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Náprava poruch**.</span><span class="sxs-lookup"><span data-stu-id="f8381-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="f8381-172">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="f8381-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f8381-173">Do pole **Náprava poruchy** zadejte název nápravy poruchy.</span><span class="sxs-lookup"><span data-stu-id="f8381-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="f8381-174">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f8381-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f8381-175">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f8381-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f8381-176">Podle potřeby můžete změnit názvy příznaků, oblastí, typů, příčin a náprav poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="f8381-177">Změny názvu se automaticky projeví v souvisejících registracích poruch.</span><span class="sxs-lookup"><span data-stu-id="f8381-177">The name changes are automatically reflected in the related fault registrations.</span></span>
