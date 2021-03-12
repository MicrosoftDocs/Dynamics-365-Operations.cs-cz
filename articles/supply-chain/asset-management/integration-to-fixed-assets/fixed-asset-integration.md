---
title: Integrace správy majetku s dlouhodobým majetkem
description: V tomto tématu je vysvětleno, jak integrovat moduly Správa majetku a Dlouhodobý majetek tak, aby bylo možné propojit dlouhodobý majetek s objekty údržby.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 879950b9aeb345fcd59dfe73d3963a44607c7ac2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994222"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="941e6-103">Integrace správy majetku s dlouhodobým majetkem</span><span class="sxs-lookup"><span data-stu-id="941e6-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="941e6-104">Integrací modulů **Správa majetku** a **Dlouhodobý majetek** můžete propojit dlouhodobý majetek s objekty údržby.</span><span class="sxs-lookup"><span data-stu-id="941e6-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="941e6-105">Uživatelé modulu Dlouhodobý majetek pak mohou vytvořit objekt údržby z nového nebo existujícího dlouhodobého majetku a uživatelé modulu Správa majetku mohou k existujícímu dlouhodobému majetku přidružit objekt údržby.</span><span class="sxs-lookup"><span data-stu-id="941e6-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="941e6-106">Tato funkce rovněž usnadňuje uživatelům modulu Dlouhodobý majetek zobrazení nákladů, které byly zaúčtovány z pracovních příkazů pro související objekty údržby.</span><span class="sxs-lookup"><span data-stu-id="941e6-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="941e6-107">V tomto tématu *objekty údržby* odkazují na majetek z modulu **Správa majetku** a *dlouhodobý majetek* na majetek z modulu **Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="941e6-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="941e6-108">Nastavení výchozího umístění pro nové objekty údržby vytvořené z dlouhodobého majetku (volitelné)</span><span class="sxs-lookup"><span data-stu-id="941e6-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="941e6-109">Tato volitelná konfigurace vám umožňuje nastavit výchozí umístění pro nové objekty údržby vytvořené z dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="941e6-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="941e6-110">Tuto konfiguraci obvykle provedete pouze jednou, pokud ji vůbec provedete.</span><span class="sxs-lookup"><span data-stu-id="941e6-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="941e6-111">Konfiguraci provedete následovně:</span><span class="sxs-lookup"><span data-stu-id="941e6-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="941e6-112">Přejděte do nabídky **Správa majetku \> Nastavení \> Parametry správy skladu**.</span><span class="sxs-lookup"><span data-stu-id="941e6-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="941e6-113">Na kartě **Dlouhodobý majetek** v poli **Funkční místo** vyberte výchozí umístění.</span><span class="sxs-lookup"><span data-stu-id="941e6-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="941e6-114">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="941e6-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="941e6-115">Práce s integrovanými objekty údržby a dlouhodobým majetkem</span><span class="sxs-lookup"><span data-stu-id="941e6-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="941e6-116">Tato část obsahuje kolekci postupů, které představují různé způsoby práce s integrovanými funkcemi správy majetku a dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="941e6-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="941e6-117">Přidružení existujícího objektu údržby k dlouhodobému majetku</span><span class="sxs-lookup"><span data-stu-id="941e6-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="941e6-118">Chcete-li přidružit existující objektu údržby k dlouhodobému majetku, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="941e6-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="941e6-119">Přejděte na **Správa majetku \> Majetek \> Všechen majetek** (nebo **Aktivní majetek**).</span><span class="sxs-lookup"><span data-stu-id="941e6-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="941e6-120">Vyberte majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-120">Select an asset.</span></span>
1. <span data-ttu-id="941e6-121">Na záložce s náhledem **Dlouhodobý majetek** v poli **Číslo dlouhodobého majetku** vyberte existující dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="941e6-122">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="941e6-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="941e6-123">Zobrazení dlouhodobého majetku, který je přidružen k vybranému objektu údržby</span><span class="sxs-lookup"><span data-stu-id="941e6-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="941e6-124">Chcete-li zobrazit dlouhodobý majetek, který je přidružen k vybranému objektu údržby, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="941e6-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="941e6-125">Přejděte na **Správa majetku \> Majetek \> Všechen majetek** (nebo **Aktivní majetek**).</span><span class="sxs-lookup"><span data-stu-id="941e6-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="941e6-126">Vyberte majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-126">Select an asset.</span></span>
1. <span data-ttu-id="941e6-127">Na záložce s náhledem **Dlouhodobý majetek** v poli **Číslo dlouhodobého majetku** vyberte odkaz.</span><span class="sxs-lookup"><span data-stu-id="941e6-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="941e6-128">Otevře se stránka **Dlouhodobý majetek** pro vybraný majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="941e6-129">(Tato stránka se obvykle nachází v umístění **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.)</span><span class="sxs-lookup"><span data-stu-id="941e6-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="941e6-130">Zobrazení objektu údržby, který je přidružen k vybranému dlouhodobému majetku</span><span class="sxs-lookup"><span data-stu-id="941e6-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="941e6-131">Chcete-li zobrazit objekt údržby, který je přidružen k vybranému dlouhodobému majetku, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="941e6-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="941e6-132">Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="941e6-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="941e6-133">Vyberte majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-133">Select an asset.</span></span>
1. <span data-ttu-id="941e6-134">V podokně akcí na kartě **Správa majetku** ve skupině **Zobrazit** vyberte **Objekt údržby**.</span><span class="sxs-lookup"><span data-stu-id="941e6-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="941e6-135">Otevře se stránka **Správa majetku** pro objekt údržby, který je přidružen k vybranému dlouhodobému majetku.</span><span class="sxs-lookup"><span data-stu-id="941e6-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="941e6-136">(Tato stránka je obvykle k dispozici v umístění **Správa majetku \> Majetek \> Všechen majetek**.)</span><span class="sxs-lookup"><span data-stu-id="941e6-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="941e6-137">Zobrazení nákladů na údržbu přidružených k dlouhodobému majetku</span><span class="sxs-lookup"><span data-stu-id="941e6-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="941e6-138">Pracovní příkazy správy majetku mohou být zaúčtovány pro objekty údržby a každý z těchto pracovních příkazů obvykle obsahuje náklady.</span><span class="sxs-lookup"><span data-stu-id="941e6-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="941e6-139">Když je dlouhodobý majetek přidružen k objektu údržby, přímo z dlouhodobého majetku můžete zobrazit související náklady.</span><span class="sxs-lookup"><span data-stu-id="941e6-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="941e6-140">Chcete-li zobrazit náklady na údržbu přidružené k dlouhodobému majetku, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="941e6-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="941e6-141">Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="941e6-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="941e6-142">Vyberte majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-142">Select an asset.</span></span>
1. <span data-ttu-id="941e6-143">V podokně akcí na kartě **Správa majetku** ve skupině **Zobrazit** vyberte **Náklady na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="941e6-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="941e6-144">Otevře se stránka **Náklady na údržbu** a zobrazí související náklady.</span><span class="sxs-lookup"><span data-stu-id="941e6-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="941e6-145">Vytvoření nového objektu údržby pro existující dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="941e6-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="941e6-146">Chcete-li vytvořit nový objekt údržby pro existující dlouhodobý majetek, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="941e6-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="941e6-147">Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="941e6-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="941e6-148">Vyberte majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-148">Select an asset.</span></span>
1. <span data-ttu-id="941e6-149">V podokně akcí na kartě **Správa majetku** ve skupině **Nový** vyberte **Vytvořit objekt údržby**.</span><span class="sxs-lookup"><span data-stu-id="941e6-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="941e6-150">(Není-li tato možnost dostupná, je možné, že objekt údržby již byl přidružen k vybranému dlouhodobému majetku.)</span><span class="sxs-lookup"><span data-stu-id="941e6-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="941e6-151">Dokončete tvorbu majetku způsobem popsaným v tématu [Vytvoření majetku](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="941e6-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="941e6-152">Vytvoření nového dlouhodobého majetku a přidání nového objektu údržby pro něj</span><span class="sxs-lookup"><span data-stu-id="941e6-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="941e6-153">Chcete-li vytvořit nový dlouhodobý majetek a přidat pro něj nový objekt údržby, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="941e6-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="941e6-154">Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="941e6-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="941e6-155">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="941e6-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="941e6-156">Dokončete tvorbu dlouhodobého majetku způsobem popsaným v tématu [Vytvoření dlouhodobého majetku](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="941e6-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="941e6-157">V podokně akcí na kartě **Správa majetku** ve skupině **Nový** vyberte **Vytvořit objekt údržby**.</span><span class="sxs-lookup"><span data-stu-id="941e6-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="941e6-158">Dokončete tvorbu majetku způsobem popsaným v tématu [Vytvoření majetku](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="941e6-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="941e6-159">Odebrání přidružení mezi dlouhodobým majetkem a objektem údržby</span><span class="sxs-lookup"><span data-stu-id="941e6-159">Remove the association between two assets</span></span>

<span data-ttu-id="941e6-160">V některých případech může být nutné zrušit přidružení objektu údržby k dlouhodobému majetku.</span><span class="sxs-lookup"><span data-stu-id="941e6-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="941e6-161">Chcete- li například [vytvořit nový objekt údržby](#new-maintenance-from-fixed) z dlouhodobého majetku, musíte nejprve odebrat existující přidružení.</span><span class="sxs-lookup"><span data-stu-id="941e6-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="941e6-162">Chcete-li odebrat existující přidružení mezi objektem údržby a dlouhodobým majetkem, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="941e6-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="941e6-163">Přejděte na **Správa majetku \> Majetek \> Všechen majetek** (nebo **Aktivní majetek**).</span><span class="sxs-lookup"><span data-stu-id="941e6-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="941e6-164">Vyhledejte a otevřete dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="941e6-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="941e6-165">Na záložce s náhledem **Dlouhodobý majetek** vymažte hodnotu z pole **Funkční místo**.</span><span class="sxs-lookup"><span data-stu-id="941e6-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="941e6-166">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="941e6-166">On the Action Pane, select **Save**.</span></span>
