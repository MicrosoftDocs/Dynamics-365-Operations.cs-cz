---
title: Vytvoření hierarchie navigace sítě
description: Toto téma popisuje, jak vytvořit hierarchie navigace kanálu v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89e24496d35ea0a02bd985f76d7579e1914d9290
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972975"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="8057e-103">Vytvoření hierarchie navigace sítě</span><span class="sxs-lookup"><span data-stu-id="8057e-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8057e-104">Toto téma popisuje, jak vytvořit hierarchie navigace kanálu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8057e-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8057e-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="8057e-105">Overview</span></span>

<span data-ttu-id="8057e-106">Hierarchie navigace kanálů se používá k seskupení a uspořádání produktů do kategorií, aby je bylo možné procházet online nebo v prodejních místech (POS).</span><span class="sxs-lookup"><span data-stu-id="8057e-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="8057e-107">Vytvoření hierarchie navigace sítě</span><span class="sxs-lookup"><span data-stu-id="8057e-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="8057e-108">Chcete-li vytvořit hierarchii navigace kanálu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="8057e-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="8057e-109">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Kategorie navigace kanálů**.</span><span class="sxs-lookup"><span data-stu-id="8057e-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="8057e-110">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8057e-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8057e-111">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="8057e-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="8057e-112">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8057e-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="8057e-113">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="8057e-113">Select **Create**.</span></span>
1. <span data-ttu-id="8057e-114">V podokně akcí vyberte **Nový uzel kategorie** k vytvoření kořenového uzlu.</span><span class="sxs-lookup"><span data-stu-id="8057e-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="8057e-115">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="8057e-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="8057e-116">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8057e-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="8057e-117">Do pole **Popisný název** zadejte popisný název produktu.</span><span class="sxs-lookup"><span data-stu-id="8057e-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="8057e-118">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8057e-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8057e-119">Následující obrázek znázorňuje příklad kořenového uzlu.</span><span class="sxs-lookup"><span data-stu-id="8057e-119">The following image shows a example root node.</span></span>

![Ukázkový kořenový uzel](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="8057e-121">Vytvoření uzlů navigačních kategorií</span><span class="sxs-lookup"><span data-stu-id="8057e-121">Create navigation category nodes</span></span>

<span data-ttu-id="8057e-122">Chcete-li vytvořit další uzly navigační kategorie, které budou představovat kategorie produktů v kanálu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8057e-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="8057e-123">V navigačním podokně vyberte nadřazený uzel, ke kterému chcete přidat kategorii.</span><span class="sxs-lookup"><span data-stu-id="8057e-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="8057e-124">V podokně akcí vyberte možnost **Nový uzel kategorií**.</span><span class="sxs-lookup"><span data-stu-id="8057e-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="8057e-125">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="8057e-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="8057e-126">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8057e-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="8057e-127">Do pole **Popisný název** zadejte popisný název produktu.</span><span class="sxs-lookup"><span data-stu-id="8057e-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="8057e-128">V poli **Pořadí zobrazení** zadejte pořadí zobrazení (volitelné).</span><span class="sxs-lookup"><span data-stu-id="8057e-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="8057e-129">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8057e-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8057e-130">Následující obrázek znázorňuje příklad dokončené navigační hierarchie kanálů.</span><span class="sxs-lookup"><span data-stu-id="8057e-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Vzorová hierarchie kanálu](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="8057e-132">Přidat produkty do uzlů kategorií</span><span class="sxs-lookup"><span data-stu-id="8057e-132">Add products to category nodes</span></span>

<span data-ttu-id="8057e-133">Chcete-li přidat produkty do uzlů kategorií, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8057e-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="8057e-134">Vyberte uzel kategorií.</span><span class="sxs-lookup"><span data-stu-id="8057e-134">Select a category node.</span></span>
1. <span data-ttu-id="8057e-135">Ve volbě **Produkty** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8057e-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="8057e-136">Vyhledejte nové produkty, které chcete přidat pomocí čísla produktu nebo názvu produktu, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8057e-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="8057e-137">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8057e-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="8057e-138">Přidání produktů do uzlu v hierarchii navigace kanálu není dostatečné, aby se produkty na vybraném kanálu zobrazily, ale tyto produkty musí být také roztříděny do produktu.</span><span class="sxs-lookup"><span data-stu-id="8057e-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="8057e-139">Následující obrázek znázorňuje příklad uzlu s přidanými produkty.</span><span class="sxs-lookup"><span data-stu-id="8057e-139">The following image shows an example node with products added.</span></span>

![Produkty přidané do uzlu kategorií](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="8057e-141">Přidat skupiny atributů produktů do uzlů kategorií</span><span class="sxs-lookup"><span data-stu-id="8057e-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="8057e-142">Skupiny atributů je nutné vytvořit před jejich přidáním do uzlu v hierarchii navigace kanálu.</span><span class="sxs-lookup"><span data-stu-id="8057e-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="8057e-143">Přidání produktu skupiny atributů do uzlu kategorií provedete následovně.</span><span class="sxs-lookup"><span data-stu-id="8057e-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="8057e-144">Vyberte uzel kategorií.</span><span class="sxs-lookup"><span data-stu-id="8057e-144">Select a category node.</span></span>
1. <span data-ttu-id="8057e-145">Ve **Skupině atributů produktu** vyberte možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8057e-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="8057e-146">Vyhledejte skupiny atributů, které chcete přidat, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8057e-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="8057e-147">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8057e-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8057e-148">Následující obrázek znázorňuje příklad uzlu s přidanými skupinami atributů produktů.</span><span class="sxs-lookup"><span data-stu-id="8057e-148">The following image shows a sample node with product attribute groups added.</span></span>

![Skupiny atributů produktu v uzlu](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="8057e-150">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8057e-150">Additional resources</span></span>

[<span data-ttu-id="8057e-151">Nastavení sortimentu</span><span class="sxs-lookup"><span data-stu-id="8057e-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="8057e-152">Správa atributů a skupin atributů</span><span class="sxs-lookup"><span data-stu-id="8057e-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)
