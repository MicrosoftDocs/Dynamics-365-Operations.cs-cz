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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6871765a450295a3f308ec7e706f1b126071585f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986040"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="28fe8-103">Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="28fe8-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28fe8-104">Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="28fe8-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="28fe8-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="28fe8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="28fe8-106">Nové názvosloví čísel produktů je přiřazeno skupině dimenzí produktu Barva a Velikost.</span><span class="sxs-lookup"><span data-stu-id="28fe8-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="28fe8-107">Tento úkol obvykle provádí návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="28fe8-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="28fe8-108">Vytvoření názvosloví čísla produktu</span><span class="sxs-lookup"><span data-stu-id="28fe8-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="28fe8-109">Zvolte **Definice modelu varianty produktu** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-109">Select **Product variant model definition** .</span></span>
2. <span data-ttu-id="28fe8-110">Zvolte **Názvosloví produktu** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-110">Select **Product nomenclature** .</span></span>
3. <span data-ttu-id="28fe8-111">Zvolte **Nové** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-111">Select **New** .</span></span>
4. <span data-ttu-id="28fe8-112">V poli **Název** zadejte název názvosloví, který pomáhá identifikovat cílovou skupinu dimenzí produktu, například `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="28fe8-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="28fe8-113">Zadejte hodnotu do pole **Popis** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="28fe8-114">Vyberte **přidat** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-114">Select **Add** .</span></span>
7. <span data-ttu-id="28fe8-115">Zvolte **Číslo základního produktu** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="28fe8-116">Vyberte **přidat** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-116">Select **Add** .</span></span>
9. <span data-ttu-id="28fe8-117">Zvolte **Textová konstanta** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-117">Select **Text constant** .</span></span>
10. <span data-ttu-id="28fe8-118">Zadejte hodnotu do pole **Text** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="28fe8-119">Vyberte **přidat** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-119">Select **Add** .</span></span>
12. <span data-ttu-id="28fe8-120">Vyberte **Barva** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-120">Select **Color** .</span></span>
13. <span data-ttu-id="28fe8-121">Vyberte **přidat** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-121">Select **Add** .</span></span>
14. <span data-ttu-id="28fe8-122">Zvolte **Textová konstanta** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-122">Select **Text constant** .</span></span>
15. <span data-ttu-id="28fe8-123">Zadejte hodnotu do pole **Text** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="28fe8-124">Vyberte **přidat** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-124">Select **Add** .</span></span>
17. <span data-ttu-id="28fe8-125">Vyberte **Velikost** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-125">Select **Size** .</span></span>
18. <span data-ttu-id="28fe8-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="28fe8-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="28fe8-127">Přiřazení názvosloví základnímu produktu</span><span class="sxs-lookup"><span data-stu-id="28fe8-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="28fe8-128">Vyberte **Skupiny dimenzí produktů** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-128">Select **Product dimension groups** .</span></span>
2. <span data-ttu-id="28fe8-129">Vyberte **skupinu dimenzí produktu SizeCol** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="28fe8-130">Vyberte možnost **Upravit** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-130">Select **Edit** .</span></span>
4. <span data-ttu-id="28fe8-131">Vyberte možnost **Ano** v poli **Použít názvosloví** .</span><span class="sxs-lookup"><span data-stu-id="28fe8-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="28fe8-132">V poli **Názvosloví čísla varianty produktu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="28fe8-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="28fe8-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="28fe8-133">Close the page.</span></span>

