---
title: Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu
description: Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a15d1f4ecbf85e22bfadc1dd680d24bc56d807f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007534"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="dc6db-103">Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="dc6db-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc6db-104">Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="dc6db-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="dc6db-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="dc6db-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dc6db-106">Nové názvosloví čísel produktů je přiřazeno skupině dimenzí produktu Barva a Velikost.</span><span class="sxs-lookup"><span data-stu-id="dc6db-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="dc6db-107">Tento úkol obvykle provádí návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="dc6db-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="dc6db-108">Vytvoření názvosloví čísla produktu</span><span class="sxs-lookup"><span data-stu-id="dc6db-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="dc6db-109">Zvolte **Definice modelu varianty produktu**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="dc6db-110">Zvolte **Názvosloví produktu**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="dc6db-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-111">Select **New**.</span></span>
4. <span data-ttu-id="dc6db-112">V poli **Název** zadejte název názvosloví, který pomáhá identifikovat cílovou skupinu dimenzí produktu, například `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="dc6db-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="dc6db-113">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="dc6db-114">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-114">Select **Add**.</span></span>
7. <span data-ttu-id="dc6db-115">Zvolte **Číslo základního produktu**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="dc6db-116">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-116">Select **Add**.</span></span>
9. <span data-ttu-id="dc6db-117">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="dc6db-118">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="dc6db-119">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-119">Select **Add**.</span></span>
12. <span data-ttu-id="dc6db-120">Vyberte **Barva**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-120">Select **Color**.</span></span>
13. <span data-ttu-id="dc6db-121">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-121">Select **Add**.</span></span>
14. <span data-ttu-id="dc6db-122">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="dc6db-123">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="dc6db-124">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-124">Select **Add**.</span></span>
17. <span data-ttu-id="dc6db-125">Vyberte **Velikost**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-125">Select **Size**.</span></span>
18. <span data-ttu-id="dc6db-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dc6db-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="dc6db-127">Přiřazení názvosloví základnímu produktu</span><span class="sxs-lookup"><span data-stu-id="dc6db-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="dc6db-128">Vyberte **Skupiny dimenzí produktů**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="dc6db-129">Vyberte **skupinu dimenzí produktu SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="dc6db-130">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-130">Select **Edit**.</span></span>
4. <span data-ttu-id="dc6db-131">Vyberte možnost **Ano** v poli **Použít názvosloví**.</span><span class="sxs-lookup"><span data-stu-id="dc6db-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="dc6db-132">V poli **Názvosloví čísla varianty produktu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc6db-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="dc6db-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dc6db-133">Close the page.</span></span>

