---
title: Přesun, nahrazení a instalace majetku
description: Toto téma vysvětluje, jak přesunout, nahradit a nainstalovat majetek v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0e6306698d351d33cae627e3741ad9a2eb6d893
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783137"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="0ab2f-103">Přesun, nahrazení a instalace majetku</span><span class="sxs-lookup"><span data-stu-id="0ab2f-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0ab2f-104">Toto téma vysvětluje, jak přesunout, nahradit a nainstalovat majetek v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="0ab2f-105">Můžete vytvořit jednotlivý majetek, který nemá žádné vztahy k jiným majetkům, nebo můžete vytvořit strukturu majetku, která zahrnuje nadřazený majetek (majetek nejvyšší úrovně) a související podřízený majetek (dílčí majetek).</span><span class="sxs-lookup"><span data-stu-id="0ab2f-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="0ab2f-106">V modulu Správa majetku existují tři přístupy k přesunu a změně umístění majetku:</span><span class="sxs-lookup"><span data-stu-id="0ab2f-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="0ab2f-107">**Přesunout** – Přesun majetku buď do jiné struktury majetku nebo do jiného umístění ve stejné struktuře majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="0ab2f-108">**Nahradit** – Dočasně odstraňte majetek ze struktury majetku, aby mohl být opraven nebo obnoven, a poté znovu přidejte obnovený majetek zpět do struktury majetku později.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="0ab2f-109">Můžete také trvale nahradit použitý majetek novým majetkem.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="0ab2f-110">**Instalovat** – Instalace nadřazeného majetku a souvisejícího podřízeného majetku na funkční místo.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="0ab2f-111">Majetek, který přesunete, nahradíte nebo nainstalujete, může souviset s jiným funkčním místem.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="0ab2f-112">V takovém případě může majetek využívat finanční dimenze funkčního místa.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="0ab2f-113">Na stránce **Typy funkčních míst** nastavte zpracování finančních dimenzí na funkčních místech.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="0ab2f-114">Přesun majetku</span><span class="sxs-lookup"><span data-stu-id="0ab2f-114">Move asset</span></span>

<span data-ttu-id="0ab2f-115">Použijte funkci **Přesunout majetek** – pro přesun majetku buď do jiné struktury majetku nebo do jiného umístění ve stejné struktuře majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="0ab2f-116">Majetek můžete také přesunout mimo strukturu majetku tak, aby se stal samostatným majetkem, který nemá žádné vztahy se strukturou.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="0ab2f-117">Tuto funkci nepoužívejte, pokud je majetek opraven nebo dočasně nahrazen.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="0ab2f-118">Místo toho použijte funkci **Nahradit majetek**, která je popsána dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="0ab2f-119">Zvolte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="0ab2f-120">V seznamu vyberte majetek, který chcete přesunout.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-120">In the list, select the asset to move.</span></span> <span data-ttu-id="0ab2f-121">Pokud má majetek podřízený majetek, přesunete také tento majetek.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="0ab2f-122">Zvolte **Přesunout majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="0ab2f-123">Chcete-li majetek přesunout tak, aby se stal součástí struktury majetku, vyberte nový nadřazený majetek v poli **Nadřazený majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="0ab2f-124">Pokud přesouváte podřízený majetek a chcete jej nastavit jako samostatný majetek, který nemá žádné vztahy ke struktuře, ponechejte pole **Nadřazený majetek** prázdné.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="0ab2f-125">Ve výchozím nastavení je pole **Začátek platnosti** automaticky nastaveno na aktuální datum a čas.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="0ab2f-126">Můžete však vybrat jiné datum a čas, od kterého je přesun majetku platný.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="0ab2f-127">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="0ab2f-128">Nahrazení majetku</span><span class="sxs-lookup"><span data-stu-id="0ab2f-128">Replace asset</span></span>

<span data-ttu-id="0ab2f-129">Použijte funkci **Nahradit majetek** v souvislosti s opravami, obnovou nebo trvalým nahrazením opotřebeného majetku novým majetkem.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="0ab2f-130">Tato funkce se používá k nahrazení podřízeného majetku ve struktuře majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="0ab2f-131">Pro nadřazený majetek (to znamená majetek, který momentálně nemá nadřazený majetek) se tato náhrada provádí na funkčním místě.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="0ab2f-132">Další informace o tom, jak nahradit nadřazený majetek na funkčním místě, naleznete v tématu [Instalace majetku na funkčních místech](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="0ab2f-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0ab2f-133">Pokud dílna souvisí s výrobním oddělením, můžete vytvořit funkční místa, jako **Oprava**, **Odpad** a **Sklad** pro zpracování oprav a nahrazení majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="0ab2f-134">Zvolte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="0ab2f-135">V seznamu vyberte podřízený majetek, který chcete nahradit.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="0ab2f-136">Pokud má majetek podřízený majetek, nahradíte také tento majetek.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="0ab2f-137">Vyberte **Nahradit majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="0ab2f-138">Pole **Změna struktury** zobrazuje poslední datum a čas, kdy byl vybraný majetek a související podřízený majetek přesunut ve struktuře majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="0ab2f-139">V části **Vybraný majetek** vyberte v poli **Cílové funkční místo** funkční umístění, do kterého chcete majetek přesunout.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="0ab2f-140">Vyberte například místo **Oprava** nebo **Odpad**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="0ab2f-141">V části **Nadřazený majetek** zobrazí pole **Začátek platnosti** datum a čas, kdy byl nadřazený majetek a související podřízený majetek instalován nebo přesunut na aktuální funkční místo.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="0ab2f-142">V části **Nový majetek** v poli **Majetek** vyberte majetek, který chcete vložit jako dočasnou nebo trvalou náhradu vybraného majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="0ab2f-143">Tento majetek může být aktuálně umístěn na jiné funkční místo, jako například **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="0ab2f-144">V části **Platnost od** je pole **Začátek platnosti** automaticky nastaveno na aktuální datum a čas ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="0ab2f-145">Můžete však vybrat jiné datum a čas, od kterého je nahrazení majetku platné.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="0ab2f-146">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="0ab2f-147">Instalace majetku</span><span class="sxs-lookup"><span data-stu-id="0ab2f-147">Install asset</span></span>

<span data-ttu-id="0ab2f-148">K instalaci struktury majetku do funkčního místa použijte funkci **Nainstalovat majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="0ab2f-149">Vždy vyberte nadřazený majetek.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-149">Always select a parent asset.</span></span> <span data-ttu-id="0ab2f-150">Nadřazený majetek a související podřízený majetek budou přesunuty do vybraného funkčního místa.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="0ab2f-151">Zvolte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="0ab2f-152">V seznamu vyberte nadřazený majetek, který chcete nainstalovat do jiného funkčního místa.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="0ab2f-153">Vyberte **Instalovat majetek**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-153">Select **Install asset**.</span></span>

    <span data-ttu-id="0ab2f-154">Část **Atributy** zobrazuje atributy majetku, které jsou nastaveny u nadřazeného majetku.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="0ab2f-155">V poli **Funkční místo** zvolte nové místo.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="0ab2f-156">Ve výchozím nastavení je pole **Začátek platnosti** automaticky nastaveno na aktuální datum a čas.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="0ab2f-157">Můžete však vybrat jiné datum a čas, od kterého je instalace ve struktuře majetku platná.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="0ab2f-158">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ab2f-158">Select **OK**.</span></span>
