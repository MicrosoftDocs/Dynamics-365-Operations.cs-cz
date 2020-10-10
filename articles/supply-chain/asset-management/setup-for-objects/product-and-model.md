---
title: Výrobci a modely majetku
description: Toto téma vysvětluje, jak nastavit výrobce majetku a související modely v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2dfcebcbab77cba1795a8b559a3a4244abd00e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889402"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="c973b-103">Výrobci a modely majetku</span><span class="sxs-lookup"><span data-stu-id="c973b-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c973b-104">Toto téma vysvětluje, jak nastavit výrobce majetku a související modely v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="c973b-105">Modely mohou souviset s typy majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="c973b-106">Nastavení vztahů produktů a modelů</span><span class="sxs-lookup"><span data-stu-id="c973b-106">Set up product-model relations</span></span>

1. <span data-ttu-id="c973b-107">Vyberte **Správa majetku** \> **Nastavení** \> **Majetek** \> **Výrobce a model**.</span><span class="sxs-lookup"><span data-stu-id="c973b-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="c973b-108">Zvolte **Nový** pro vytvoření nového produktu</span><span class="sxs-lookup"><span data-stu-id="c973b-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="c973b-109">Do pole **Výrobce** zadejte název výrobce majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="c973b-110">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c973b-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c973b-111">Na záložce **Modely** vyberte **Přidat**, chcete-li vytvořit model majetku, který by měl souviset s výrobcem majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="c973b-112">Do pole **Model** zadejte název model majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="c973b-113">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c973b-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="c973b-114">V poli **Typ majetku** vyberte typ majetku, ke kterému by se měl vztahovat model výrobce.</span><span class="sxs-lookup"><span data-stu-id="c973b-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c973b-115">Ve vyhledání **Typ majetku** můžete také nastavit vztahy pro typy majetku, výrobce a modely.</span><span class="sxs-lookup"><span data-stu-id="c973b-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="c973b-116">Další informace naleznete v tématu [Typy majetku](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="c973b-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="c973b-117">Na záložce **Podrobnosti** zobrazuje pole **Modely** počet modelů majetku nastavených pro vybraného výrobce majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="c973b-118">Pole **Majetek** zobrazuje množství majetku, který používá vybraného výrobce.</span><span class="sxs-lookup"><span data-stu-id="c973b-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="c973b-119">Pole **Majetek** zobrazuje počet objektů, které používají model výrobce.</span><span class="sxs-lookup"><span data-stu-id="c973b-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="c973b-120">Typ majetku nemůže mít žádné vztahy s modely výrobců majetku, může se vztahovat k jednomu modelu výrobce majetku nebo se může vztahovat k více modelům výrobců majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="c973b-121">Pokud typ majetku souvisí alespoň s jedním modelem výrobce, mohou být na těchto stránkách správy majetku vybrány pouze kombinace nastavené ve vyhledávání **Model výrobce**, kde může být nastavena kombinace typu majetku, výrobce a modelu.</span><span class="sxs-lookup"><span data-stu-id="c973b-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="c973b-122">Tyto stránky zahrnují řádky **Všechen majetek**, **Úrovně služby Majetek**, **Výchozí typy úloh** a **Rozpočet údržby**.</span><span class="sxs-lookup"><span data-stu-id="c973b-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="c973b-123">Pokud některé typy majetku nesouvisejí s žádným modelem výrobce, na stránkách se zobrazí pouze ty typy majetku a modely výrobců, které také nemají žádný vztah k typům majetku.</span><span class="sxs-lookup"><span data-stu-id="c973b-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="c973b-124">Výběr výrobce a modelu na objektu</span><span class="sxs-lookup"><span data-stu-id="c973b-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="c973b-125">Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="c973b-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="c973b-126">Ve sloupci **Majetek** vyberte odkaz na majetek.</span><span class="sxs-lookup"><span data-stu-id="c973b-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="c973b-127">Zobrazí se stránka **Podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="c973b-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="c973b-128">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="c973b-128">Select **Edit**.</span></span>
4. <span data-ttu-id="c973b-129">Na záložce **Obecné** vyberte hodnoty v polích **Výrobce** a **Model**.</span><span class="sxs-lookup"><span data-stu-id="c973b-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
