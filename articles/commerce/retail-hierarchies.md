---
title: Hierarchie Commerce
description: Tento článek popisuje hierarchie v aplikaci Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895274"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="55efc-103">Hierarchie Commerce</span><span class="sxs-lookup"><span data-stu-id="55efc-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="55efc-104">Tento článek popisuje hierarchie v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="55efc-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="55efc-105">Můžete vytvořit hierarchii kategorií a uspořádat produkty, které prodáváte prostřednictvím prodejních kanálů.</span><span class="sxs-lookup"><span data-stu-id="55efc-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="55efc-106">Hierarchie produktů můžete použít k uspořádání produktů do kategorií nebo k jejich seskupení.</span><span class="sxs-lookup"><span data-stu-id="55efc-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="55efc-107">Potom můžete tyto produkty použít k vytvoření sortimentu produktů a věrnostních programů pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="55efc-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="55efc-108">Lze také přiřadit atributy a vlastnosti produktu, přiřadit cenové struktury, zahrnout produkty do promoakcí produktů a použít produkty k vykazování.</span><span class="sxs-lookup"><span data-stu-id="55efc-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="55efc-109">Můžete vytvořit jednu hierarchii kategorie představující všechny produkty a kategorie v rámci organizace a potom tuto hierarchii kategorií použít pro více účelů.</span><span class="sxs-lookup"><span data-stu-id="55efc-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="55efc-110">Alternativně můžete vytvořit více hierarchií kategorií pro zvláštní účely, jako je propagace výrobku.</span><span class="sxs-lookup"><span data-stu-id="55efc-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="55efc-111">Při vytváření hierarchie produktů je nutné přiřadit typ kategorie hierarchie k identifikaci účelu hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="55efc-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="55efc-112">Například pouze hierarchie produktů, kterým je přiřazen typ **Hierarchie navigace velkoobchodu**, jsou odkazovány při procházení produktů podle kategorie online nebo na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="55efc-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="55efc-113">Typy hierarchie</span><span class="sxs-lookup"><span data-stu-id="55efc-113">Hierarchy types</span></span>

<span data-ttu-id="55efc-114">V následující tabulce jsou uvedeny dostupné typy hierarchií kategorie a obecný účel každého typu.</span><span class="sxs-lookup"><span data-stu-id="55efc-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="55efc-115">Typ hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="55efc-115">Category hierarchy type</span></span>       | <span data-ttu-id="55efc-116">Účel</span><span class="sxs-lookup"><span data-stu-id="55efc-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="55efc-117">Hierarchie výrobků</span><span class="sxs-lookup"><span data-stu-id="55efc-117">Product hierarchy</span></span>      | <span data-ttu-id="55efc-118">Použijte tento typ hierarchie, chcete-li definovat celkovou hierarchii produktů pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="55efc-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="55efc-119">Tento typ hierarchie lze použít pro výrobní události, tvorbu cen a promoakce, sestavy a plánování sortimentu.</span><span class="sxs-lookup"><span data-stu-id="55efc-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="55efc-120">Tento typ hierarchie může být přiřazen pouze jedné hierarchii produktů.</span><span class="sxs-lookup"><span data-stu-id="55efc-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="55efc-121">Doplňková hierarchie</span><span class="sxs-lookup"><span data-stu-id="55efc-121">Supplemental hierarchy</span></span> | <span data-ttu-id="55efc-122">Použijte tento typ hierarchie pro jakékoli další hierarchie kategorií, které chcete vytvořit.</span><span class="sxs-lookup"><span data-stu-id="55efc-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="55efc-123">Například na jaře máte promoakci na plavky.</span><span class="sxs-lookup"><span data-stu-id="55efc-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="55efc-124">Proto zahrnete plavky do samostatnou hierarchie kategorií a použijete propagační cenové kalkulace pro různé kategorie produktu.</span><span class="sxs-lookup"><span data-stu-id="55efc-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="55efc-125">Hierarchie navigace</span><span class="sxs-lookup"><span data-stu-id="55efc-125">Navigation hierarchy</span></span>   | <span data-ttu-id="55efc-126">Použijte tento typu hierarchie pro seskupení a uspořádání produktů do kategorií, aby je bylo možné procházet online nebo v POS.</span><span class="sxs-lookup"><span data-stu-id="55efc-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="55efc-127">Pomocí hierarchie kategorií k vytvoření struktury produktů můžete nastavit a spravovat atributy a vlastnosti produktů na úrovni kategorie.</span><span class="sxs-lookup"><span data-stu-id="55efc-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="55efc-128">Tyto atributy a vlastnosti zahrnují nastavení pro dimenze produktu a nastavení POS.</span><span class="sxs-lookup"><span data-stu-id="55efc-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="55efc-129">Všechny produkty, které přiřadíte k těmto kategoriím, automaticky zdědí atributy a vlastnosti, které definujete.</span><span class="sxs-lookup"><span data-stu-id="55efc-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="55efc-130">Můžete také zkopírovat nastavení vlastností pro jakýkoli produkt do více produktů ve vybrané kategorii současně.</span><span class="sxs-lookup"><span data-stu-id="55efc-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
