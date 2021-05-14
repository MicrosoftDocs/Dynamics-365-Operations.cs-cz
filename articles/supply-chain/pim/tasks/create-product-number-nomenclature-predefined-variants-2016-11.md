---
title: Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu
description: Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920650"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="8dc17-103">Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="8dc17-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8dc17-104">Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="8dc17-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="8dc17-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="8dc17-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8dc17-106">Nové názvosloví čísel produktů je přiřazeno skupině dimenzí produktu Barva a Velikost.</span><span class="sxs-lookup"><span data-stu-id="8dc17-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="8dc17-107">Tento úkol obvykle provádí návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="8dc17-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="8dc17-108">Vytvoření názvosloví čísla produktu</span><span class="sxs-lookup"><span data-stu-id="8dc17-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="8dc17-109">Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Nomenklatura produktu**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="8dc17-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-110">Select **New**.</span></span>
1. <span data-ttu-id="8dc17-111">V poli **Název** zadejte název názvosloví, který pomáhá identifikovat cílovou skupinu dimenzí produktu, například `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="8dc17-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="8dc17-112">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="8dc17-113">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-113">Select **Add**.</span></span>
1. <span data-ttu-id="8dc17-114">Zvolte **Číslo základního produktu**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="8dc17-115">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-115">Select **Add**.</span></span>
1. <span data-ttu-id="8dc17-116">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="8dc17-117">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="8dc17-118">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-118">Select **Add**.</span></span>
1. <span data-ttu-id="8dc17-119">Vyberte **Barva**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-119">Select **Color**.</span></span>
1. <span data-ttu-id="8dc17-120">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-120">Select **Add**.</span></span>
1. <span data-ttu-id="8dc17-121">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="8dc17-122">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="8dc17-123">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-123">Select **Add**.</span></span>
1. <span data-ttu-id="8dc17-124">Vyberte **Velikost**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-124">Select **Size**.</span></span>
1. <span data-ttu-id="8dc17-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8dc17-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="8dc17-126">Přiřazení názvosloví základnímu produktu</span><span class="sxs-lookup"><span data-stu-id="8dc17-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="8dc17-127">Vyberte **Skupiny dimenzí produktů**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="8dc17-128">Vyberte **skupinu dimenzí produktu SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="8dc17-129">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-129">Select **Edit**.</span></span>
4. <span data-ttu-id="8dc17-130">Vyberte možnost **Ano** v poli **Použít názvosloví**.</span><span class="sxs-lookup"><span data-stu-id="8dc17-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="8dc17-131">V poli **Názvosloví čísla varianty produktu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8dc17-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="8dc17-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8dc17-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]