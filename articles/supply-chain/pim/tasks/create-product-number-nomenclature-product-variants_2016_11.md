---
title: Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu
description: Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921004"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="d900f-103">Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="d900f-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d900f-104">Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu.</span><span class="sxs-lookup"><span data-stu-id="d900f-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="d900f-105">Tato procedura také ukazuje, jak lze vytvářet názvosloví konfigurace komponenty modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="d900f-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="d900f-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d900f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d900f-107">Základnímu produktu D0004 je přiřazeno nové názvosloví čísla produktu.</span><span class="sxs-lookup"><span data-stu-id="d900f-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="d900f-108">Tento úkol obvykle provádí návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="d900f-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="d900f-109">Vytvoření názvosloví čísla produktu</span><span class="sxs-lookup"><span data-stu-id="d900f-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="d900f-110">Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Nomenklatura produktu**.</span><span class="sxs-lookup"><span data-stu-id="d900f-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="d900f-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d900f-111">Select **New**.</span></span>
1. <span data-ttu-id="d900f-112">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="d900f-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="d900f-113">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="d900f-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="d900f-114">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-114">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-115">Zvolte **Číslo základního produktu**.</span><span class="sxs-lookup"><span data-stu-id="d900f-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="d900f-116">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-116">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-117">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d900f-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="d900f-118">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-119">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="d900f-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d900f-120">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-120">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-121">Vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="d900f-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="d900f-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d900f-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="d900f-123">Přiřazení názvosloví čísla produktu základnímu produktu</span><span class="sxs-lookup"><span data-stu-id="d900f-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="d900f-124">Přejděte do nabídky **Řízení informací o produktech \> Produkty \> Základní produkty**.</span><span class="sxs-lookup"><span data-stu-id="d900f-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="d900f-125">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="d900f-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d900f-126">Můžete například filtrovat pole **Číslo produktu** pomocí hodnoty „D“.</span><span class="sxs-lookup"><span data-stu-id="d900f-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="d900f-127">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d900f-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="d900f-128">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="d900f-128">Select **Edit**.</span></span>
1. <span data-ttu-id="d900f-129">Vyberte možnost *Ano* v poli **Použít názvosloví**.</span><span class="sxs-lookup"><span data-stu-id="d900f-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="d900f-130">V poli **Názvosloví čísla varianty produktu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d900f-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="d900f-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d900f-131">Close the page.</span></span>
1. <span data-ttu-id="d900f-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d900f-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="d900f-133">Vytvoření názvosloví pro komponentu modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="d900f-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="d900f-134">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="d900f-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="d900f-135">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d900f-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="d900f-136">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d900f-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="d900f-137">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="d900f-137">Select **Edit**.</span></span>
1. <span data-ttu-id="d900f-138">Vyberte možnost *Ano* v poli **Použít konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="d900f-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="d900f-139">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-139">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-140">Vyberte **Hodnota atributu**.</span><span class="sxs-lookup"><span data-stu-id="d900f-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d900f-141">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-142">V poli **Atribut** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d900f-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d900f-143">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-143">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-144">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d900f-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="d900f-145">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-146">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="d900f-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d900f-147">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-147">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-148">Vyberte **Hodnota atributu**.</span><span class="sxs-lookup"><span data-stu-id="d900f-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d900f-149">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-150">V poli **Atribut** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d900f-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d900f-151">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-151">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-152">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d900f-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="d900f-153">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-154">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="d900f-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d900f-155">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-155">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-156">Vyberte **Hodnota atributu**.</span><span class="sxs-lookup"><span data-stu-id="d900f-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d900f-157">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-158">V poli **Atribut** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d900f-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d900f-159">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-159">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-160">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d900f-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="d900f-161">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-162">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="d900f-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d900f-163">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-163">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-164">Vyberte **Hodnota atributu**.</span><span class="sxs-lookup"><span data-stu-id="d900f-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d900f-165">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-166">V poli **Atribut** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d900f-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d900f-167">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-167">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-168">Zvolte **Textová konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d900f-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="d900f-169">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-170">Zadejte hodnotu do pole **Text**.</span><span class="sxs-lookup"><span data-stu-id="d900f-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d900f-171">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d900f-171">Select **Add**.</span></span>
1. <span data-ttu-id="d900f-172">Vyberte **Hodnota číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="d900f-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="d900f-173">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d900f-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d900f-174">V poli **Číselná řada** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d900f-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="d900f-175">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d900f-175">Close the page.</span></span>
1. <span data-ttu-id="d900f-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d900f-176">Close the page.</span></span>
1. <span data-ttu-id="d900f-177">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d900f-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]