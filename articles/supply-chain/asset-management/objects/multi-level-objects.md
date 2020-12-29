---
title: Víceúrovňový majetek
description: Toto téma vysvětluje, jak vytvořit a odstranit víceúrovňové majetky.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423949"
---
# <a name="multi-level-assets"></a><span data-ttu-id="39e26-103">Víceúrovňový majetek</span><span class="sxs-lookup"><span data-stu-id="39e26-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="39e26-104">Toto téma vysvětluje, jak vytvořit a odstranit víceúrovňové majetky.</span><span class="sxs-lookup"><span data-stu-id="39e26-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="39e26-105">Majetek a související dílčí majetek můžete vytvořit v hierarchické stromové struktuře.</span><span class="sxs-lookup"><span data-stu-id="39e26-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="39e26-106">Tímto způsobem můžete znázornit vztahy a závislosti mezi majetky.</span><span class="sxs-lookup"><span data-stu-id="39e26-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="39e26-107">Úlohy údržby mohou souviset se všemi úrovněmi stromové struktury.</span><span class="sxs-lookup"><span data-stu-id="39e26-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="39e26-108">Statistiky lze vytvořit také pro jednotlivou úroveň nebo jako součet všech úrovní dílčích majetků.</span><span class="sxs-lookup"><span data-stu-id="39e26-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="39e26-109">Na stránce se seznamem **Všechen majetek** (**Správa majetku** \> **Obecné** \> **Majetek** \> **Všechen majetek**), sloupec **Majetek** zobrazuje seznam majetku v hierarchickém pořadí.</span><span class="sxs-lookup"><span data-stu-id="39e26-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="39e26-110">Sloupec **Nadřazený** zobrazuje související nadřazený majetek.</span><span class="sxs-lookup"><span data-stu-id="39e26-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="39e26-111">Pokud již byl majetek a dílčí majetek vytvořen, zobrazí se v části **Strom majetku** v podokně **Související informace** majetek ve stromové struktuře.</span><span class="sxs-lookup"><span data-stu-id="39e26-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="39e26-112">Informace o způsobu vytvoření majetku naleznete v tématu [Vytvoření majetku](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="39e26-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="39e26-113">Chcete-li vytvořit dílčí majetek, vyberte nadřazený majetek v poli **Nadřazený** na záložce s náhledem **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="39e26-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="39e26-114">Kopírování majetku nebo struktury majetku</span><span class="sxs-lookup"><span data-stu-id="39e26-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="39e26-115">Pokud má vaše společnost několik podobných struktur majetku, můžete je rychle vytvořit pomocí funkce Kopírovat ve správě majetku.</span><span class="sxs-lookup"><span data-stu-id="39e26-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="39e26-116">Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="39e26-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="39e26-117">Na stránce se seznamem **Všechen majetek** vyberte majetek, který chcete kopírovat.</span><span class="sxs-lookup"><span data-stu-id="39e26-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="39e26-118">Chcete-li například zkopírovat celou strukturu majetku včetně dílčích majetků, vyberte nadřazený majetek.</span><span class="sxs-lookup"><span data-stu-id="39e26-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="39e26-119">Vyberte **Kopírovat majetek**.</span><span class="sxs-lookup"><span data-stu-id="39e26-119">Select **Copy asset**.</span></span> <span data-ttu-id="39e26-120">V části **Kopírovat z** je pole **Majetek** nastaveno na majetek, který jste vybrali na stránce se seznamem.</span><span class="sxs-lookup"><span data-stu-id="39e26-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="39e26-121">V části **Kopírovat do** zadejte do pole **Majetek** název nového majetku.</span><span class="sxs-lookup"><span data-stu-id="39e26-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="39e26-122">Pokud má být vytvářený majetek součástí existující struktury majetku, vyberte v části **Nadřazený majetek** v poli **Majetek** ID nadřazeného majetku.</span><span class="sxs-lookup"><span data-stu-id="39e26-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="39e26-123">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="39e26-123">Select **OK**.</span></span> <span data-ttu-id="39e26-124">Nová struktura majetku je zobrazena na stránce seznam **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="39e26-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="39e26-125">Všechny atributy majetku, plány údržby a pořadí údržby související s majetkem, který jste zkopírovali, budou převedeny do nového majetku nebo struktury majetku.</span><span class="sxs-lookup"><span data-stu-id="39e26-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="39e26-126">Při kopírování struktury majetku mají dílčí majetky v nové struktuře stejný název jako dílčí majetky, které jste zkopírovali.</span><span class="sxs-lookup"><span data-stu-id="39e26-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="39e26-127">Po dokončení procesu kopírování můžete snadno změnit název a další nastavení majetku.</span><span class="sxs-lookup"><span data-stu-id="39e26-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="39e26-128">Vyberte majetek na stránce se seznamem **Všechen majetek** a zvolte tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="39e26-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="39e26-129">Když kopírujete majetek nebo strukturu majetku, stav životního cyklu nového majetku se obnoví do stavu, který jste definovali jako počáteční stav životního cyklu pro majetek.</span><span class="sxs-lookup"><span data-stu-id="39e26-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="39e26-130">Funkční místo je resetováno na výchozí funkční místo.</span><span class="sxs-lookup"><span data-stu-id="39e26-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="39e26-131">Odstranění majetku nebo struktury majetku</span><span class="sxs-lookup"><span data-stu-id="39e26-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="39e26-132">Pokud má majetek související dílčí majetek, můžete jej odstranit pouze v případě, že na některém z těchto majetků nejsou registrovány žádné požadavky na údržbu, úlohy pracovního příkazu, chybné registrace nebo vyhodnocení podmínek.</span><span class="sxs-lookup"><span data-stu-id="39e26-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="39e26-133">Na stránce se seznamem **Všechen majetek** vyberte majetek, který chcete odstranit.</span><span class="sxs-lookup"><span data-stu-id="39e26-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="39e26-134">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="39e26-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="39e26-135">Pokud nemůžete odstranit majetek pomocí tohoto postupu, dalším způsobem odstranění je nastavení stavu životního cyklu majetku pro tento účel.</span><span class="sxs-lookup"><span data-stu-id="39e26-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="39e26-136">Můžete například nastavit stav životního cyklu **Zlikvidováno** nebo **Odstraněno** na stránce **Stavy životního cyklu majetku**.</span><span class="sxs-lookup"><span data-stu-id="39e26-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
