---
title: Hierarchie maloobchodu
description: Tento článek popisuje hierarchie maloobchodu v aplikaci Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
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
ms.openlocfilehash: 198c8da336f3e225c5d6da2eb02c86581dc9b4d6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568015"
---
# <a name="retail-hierarchies"></a><span data-ttu-id="4eba4-103">Hierarchie maloobchodu</span><span class="sxs-lookup"><span data-stu-id="4eba4-103">Retail hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4eba4-104">Tento článek popisuje hierarchie maloobchodu v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="4eba4-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="4eba4-105">Můžete vytvořit hierarchii kategorií maloobchodu a uspořádat produkty, které prodáváte prostřednictvím prodejních kanálů.</span><span class="sxs-lookup"><span data-stu-id="4eba4-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="4eba4-106">Hierarchie maloobchodních produktů můžete použít k uspořádání produktů do kategorií nebo k jejich seskupení.</span><span class="sxs-lookup"><span data-stu-id="4eba4-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="4eba4-107">Potom můžete tyto produkty použít k vytvoření sortimentu produktů a věrnostních programů pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="4eba4-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="4eba4-108">Lze také přiřadit atributy a vlastnosti produktu, přiřadit cenové struktury, zahrnout produkty do promoakcí produktů a použít produkty k vykazování.</span><span class="sxs-lookup"><span data-stu-id="4eba4-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="4eba4-109">Můžete vytvořit jednu hierarchii kategorií maloobchodu představující všechny produkty a kategorie v rámci organizace a potom tuto hierarchii kategorií můžete použít pro více účelů.</span><span class="sxs-lookup"><span data-stu-id="4eba4-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="4eba4-110">Alternativně můžete vytvořit více hierarchií kategorií maloobchodu pro zvláštní účely, jako je propagace produktu.</span><span class="sxs-lookup"><span data-stu-id="4eba4-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="4eba4-111">Při vytváření hierarchie maloobchodních produktů je nutné přiřadit typ kategorie hierarchie k identifikaci účelu hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="4eba4-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="4eba4-112">Například pouze hierarchie produktů, kterým je přiřazen typ **Hierarchie navigace maloobchodu**, jsou odkazovány při procházení produktů podle kategorie online nebo na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="4eba4-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="4eba4-113">Typy hierarchie maloobchodu</span><span class="sxs-lookup"><span data-stu-id="4eba4-113">Retail hierarchy types</span></span>

<span data-ttu-id="4eba4-114">V následující tabulce jsou uvedeny dostupné typy hierarchií kategorií maloobchodu a obecný účel každého typu.</span><span class="sxs-lookup"><span data-stu-id="4eba4-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="4eba4-115">Typ hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="4eba4-115">Category hierarchy type</span></span>       | <span data-ttu-id="4eba4-116">Účel</span><span class="sxs-lookup"><span data-stu-id="4eba4-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="4eba4-117">Hierarchie maloobchodních produktů</span><span class="sxs-lookup"><span data-stu-id="4eba4-117">Retail product hierarchy</span></span>      | <span data-ttu-id="4eba4-118">Použijte tento typ hierarchie, chcete-li definovat celkovou hierarchii produktů pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="4eba4-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="4eba4-119">Tento typ hierarchie lze použít pro výrobní události, tvorbu cen a promoakce, sestavy a plánování sortimentu.</span><span class="sxs-lookup"><span data-stu-id="4eba4-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="4eba4-120">Tento typ hierarchie může být přiřazen pouze jedné hierarchii maloobchodních produktů.</span><span class="sxs-lookup"><span data-stu-id="4eba4-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="4eba4-121">Hierarchie doplňkového maloobchodu</span><span class="sxs-lookup"><span data-stu-id="4eba4-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="4eba4-122">Použijte tento typ hierarchie pro jakékoli další hierarchie kategorií maloobchodu, které chcete vytvořit.</span><span class="sxs-lookup"><span data-stu-id="4eba4-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="4eba4-123">Například na jaře máte promoakci na plavky.</span><span class="sxs-lookup"><span data-stu-id="4eba4-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="4eba4-124">Proto zahrnete plavky do samostatnou hierarchie kategorií a použijete propagační cenové kalkulace pro různé kategorie produktu.</span><span class="sxs-lookup"><span data-stu-id="4eba4-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="4eba4-125">Hierarchie navigace maloobchodu</span><span class="sxs-lookup"><span data-stu-id="4eba4-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="4eba4-126">Použijte tento typu hierarchie pro seskupení a uspořádání produktů do kategorií, aby je bylo možné procházet online nebo v POS.</span><span class="sxs-lookup"><span data-stu-id="4eba4-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="4eba4-127">Pomocí hierarchie kategorií maloobchodu k vytvoření struktury produktů můžete nastavit a spravovat atributy a vlastnosti produktů na úrovni kategorie.</span><span class="sxs-lookup"><span data-stu-id="4eba4-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="4eba4-128">Tyto atributy a vlastnosti zahrnují nastavení pro dimenze produktu a nastavení POS.</span><span class="sxs-lookup"><span data-stu-id="4eba4-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="4eba4-129">Všechny produkty, které přiřadíte k těmto kategoriím, automaticky zdědí atributy a vlastnosti, které definujete.</span><span class="sxs-lookup"><span data-stu-id="4eba4-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="4eba4-130">Můžete také zkopírovat nastavení vlastností pro jakýkoli produkt do více produktů ve vybrané kategorii současně.</span><span class="sxs-lookup"><span data-stu-id="4eba4-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
