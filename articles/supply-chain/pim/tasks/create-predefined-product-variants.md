---
title: Vytváření předdefinovaných variant produktů
description: Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270473"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="a15d9-103">Předdefinované varianty produktů</span><span class="sxs-lookup"><span data-stu-id="a15d9-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="a15d9-104">Příklad scénáře: Vytváření předdefinovaných variant produktů</span><span class="sxs-lookup"><span data-stu-id="a15d9-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="a15d9-105">Tento příklad scénáře vám ukáže, jak vytvořit varianty produktu pro základní produkt za pomoci kombinací dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="a15d9-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="a15d9-106">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="a15d9-106">Make demo data available</span></span>

<span data-ttu-id="a15d9-107">Pokud chcete provést tento scénář pomocí zde navržených hodnot, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu *USMF*.</span><span class="sxs-lookup"><span data-stu-id="a15d9-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="a15d9-108">Krok 1: Vytvoření základního produktu</span><span class="sxs-lookup"><span data-stu-id="a15d9-108">Step 1: Create a product master</span></span>

<span data-ttu-id="a15d9-109">Vytvoření základního produktu:</span><span class="sxs-lookup"><span data-stu-id="a15d9-109">To create a product master:</span></span>

1. <span data-ttu-id="a15d9-110">Přejděte do nabídky **Řízení informací o produktech > Produkty > Základní produkty**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="a15d9-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-111">Select **New**.</span></span>
1. <span data-ttu-id="a15d9-112">Pokud pole **Číslo produktu** již nezobrazuje číslo, pak zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a15d9-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="a15d9-113">Tento krok je vyžadován, jen pokud nebyla nastavena žádná číselná řada pro toto pole.</span><span class="sxs-lookup"><span data-stu-id="a15d9-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="a15d9-114">Do pole **Název produktu** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="a15d9-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="a15d9-115">V poli **Skupina dimenzí produktu** vyberte skupinu dimenze produktu *SizeCol* (velikost a barva).</span><span class="sxs-lookup"><span data-stu-id="a15d9-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="a15d9-116">Vyberte **OK** k vytvoření a otevření nového hlavního produktu.</span><span class="sxs-lookup"><span data-stu-id="a15d9-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="a15d9-117">Krok 2: Přidání dimenzí produktu</span><span class="sxs-lookup"><span data-stu-id="a15d9-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="a15d9-118">Tento příklad ukazuje, jak zadávat dimenze produktu ručně.</span><span class="sxs-lookup"><span data-stu-id="a15d9-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="a15d9-119">Rovněž je možné vybrat velikost, barvu nebo skupinu stylů, která obsahuje hodnoty dimenze produktu, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="a15d9-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="a15d9-120">Přidání dimenzí produktu:</span><span class="sxs-lookup"><span data-stu-id="a15d9-120">To add product dimensions:</span></span>

1. <span data-ttu-id="a15d9-121">Když je nový hlavní produkt stále otevřený, vyberte **Rozměry produktu** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="a15d9-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="a15d9-122">Otevřete kartu **Velikost** a vyberte **Nový** na panelu nástrojů pro přidání řádku do mřížky.</span><span class="sxs-lookup"><span data-stu-id="a15d9-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="a15d9-123">Proveďte následující nastavení pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="a15d9-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="a15d9-124">**Velikost:** Vyberte hodnotu velikosti.</span><span class="sxs-lookup"><span data-stu-id="a15d9-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="a15d9-125">**Název**: Zadejte název velikosti.</span><span class="sxs-lookup"><span data-stu-id="a15d9-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="a15d9-126">Vyberte **Nový** na panelu nástrojů a přidejte do mřížky druhou velikost s novou hodnotou **Velikost** a **Název**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="a15d9-127">Otevřete kartu **Barvy** a vyberte **Nový** na panelu nástrojů pro přidání řádku do mřížky.</span><span class="sxs-lookup"><span data-stu-id="a15d9-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="a15d9-128">Proveďte následující nastavení pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="a15d9-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="a15d9-129">**Barva:** Vyberte hodnotu barvy.</span><span class="sxs-lookup"><span data-stu-id="a15d9-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="a15d9-130">**Název**: Zadejte název barvy.</span><span class="sxs-lookup"><span data-stu-id="a15d9-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="a15d9-131">Vyberte **Nový** na panelu nástrojů a přidejte do mřížky druhou barvu s novou hodnotou **Barva** a **Název**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="a15d9-132">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-132">Select **Save**.</span></span>
1. <span data-ttu-id="a15d9-133">Zavřete stránku a vraťte se k novému hlavnímu produktu.</span><span class="sxs-lookup"><span data-stu-id="a15d9-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="a15d9-134">Krok 3: Vytvoření variant produktů</span><span class="sxs-lookup"><span data-stu-id="a15d9-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="a15d9-135">Tato část popisuje, jak generovat varianty produktu, když funkce *Vylepšení stránky s návrhy variant* není povolena.</span><span class="sxs-lookup"><span data-stu-id="a15d9-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="a15d9-136">V další části najdete podrobnosti o tom, jak generovat varianty produktu, když je tato funkce k dispozici.</span><span class="sxs-lookup"><span data-stu-id="a15d9-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="a15d9-137">Vytvoření variant produktů:</span><span class="sxs-lookup"><span data-stu-id="a15d9-137">To generate product variants:</span></span>

1. <span data-ttu-id="a15d9-138">Když je nový hlavní produkt stále otevřený, vyberte **Varianty produktu** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="a15d9-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="a15d9-139">V podokně Akce vyberte možnost **Návrhy variant**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="a15d9-140">Systém generuje seznam všech možných kombinací velikostí a barev, které jste pro produkt definovali.</span><span class="sxs-lookup"><span data-stu-id="a15d9-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="a15d9-141">Vyberte **Vybrat vše** na panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="a15d9-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="a15d9-142">V tomto příkladu vyberte všechny možné varianty.</span><span class="sxs-lookup"><span data-stu-id="a15d9-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="a15d9-143">Pokud chcete použít pouze podmnožinu možných kombinací dimenzí produktu, zaškrtněte podle potřeby pouze požadovaná zaškrtávací políčka.</span><span class="sxs-lookup"><span data-stu-id="a15d9-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="a15d9-144">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-144">Select **Create**.</span></span>
1. <span data-ttu-id="a15d9-145">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="a15d9-146">Vylepšené návrhy variant</span><span class="sxs-lookup"><span data-stu-id="a15d9-146">Improved variant suggestions</span></span>

<span data-ttu-id="a15d9-147">Funkce *Vylepšení stránky s návrhy variant* vylepšuje stránku **Návrhy variant** věnovanou problémům s výkonem a použitelností pro společnosti, které mají vysoký počet kombinací dimenzí produktů.</span><span class="sxs-lookup"><span data-stu-id="a15d9-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="a15d9-148">Vylepšený proces výběru hodnot dimenzí produktu, pro které se generují návrhy variant, umožňuje rychlejší a snazší identifikaci a vydání příslušné sady variant produktu.</span><span class="sxs-lookup"><span data-stu-id="a15d9-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="a15d9-149">Tato funkce přidává následující vylepšení:</span><span class="sxs-lookup"><span data-stu-id="a15d9-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="a15d9-150">**Odložené generování návrhů variant:** Stránka **Návrhy variant** již nezobrazuje návrhy při prvním otevření.</span><span class="sxs-lookup"><span data-stu-id="a15d9-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="a15d9-151">Místo toho musíte explicitně zvolit, které hodnoty budete potřebovat, a poté vybrat tlačítko **Navrhnout** pro generování kombinací.</span><span class="sxs-lookup"><span data-stu-id="a15d9-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="a15d9-152">Díky tomu je proces viditelnější a interaktivnější.</span><span class="sxs-lookup"><span data-stu-id="a15d9-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="a15d9-153">**Výběr hodnot rozměrů:** Když máte mnoho hodnot dimenzí, obvykle vás zajímá generování návrhů variant, které obsahují jen několik z nich (například při zavádění nové sady barev nebo stylů).</span><span class="sxs-lookup"><span data-stu-id="a15d9-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="a15d9-154">Díky vylepšenému designu můžete vybrat hodnoty dimenzí, pro které chcete generovat návrhy variant produktu.</span><span class="sxs-lookup"><span data-stu-id="a15d9-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="a15d9-155">To značně zvyšuje relevanci navrhovaných variant a zlepšuje výkon systému i produktivitu uživatelů.</span><span class="sxs-lookup"><span data-stu-id="a15d9-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="a15d9-156">Zapněte funkci vylepšení stránky s návrhy variant</span><span class="sxs-lookup"><span data-stu-id="a15d9-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="a15d9-157">Než můžete použít funkci *Vylepšení stránky s návrhy variant*, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="a15d9-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a15d9-158">Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="a15d9-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="a15d9-159">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="a15d9-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a15d9-160">**Modul**: *Řízení informací o produktech*</span><span class="sxs-lookup"><span data-stu-id="a15d9-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="a15d9-161">**Název funkce:** *Vylepšení stránky s návrhy variant*</span><span class="sxs-lookup"><span data-stu-id="a15d9-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="a15d9-162">Práce s vylepšenými návrhy variant</span><span class="sxs-lookup"><span data-stu-id="a15d9-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="a15d9-163">Vytváření návrhů variant produktu, když je funkce *Vylepšení stránky s návrhy variant* zapnutá:</span><span class="sxs-lookup"><span data-stu-id="a15d9-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="a15d9-164">Otevřete nebo vytvořte hlavní produkt a přidejte do něj požadované dimenze produktu, jak je popsáno v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="a15d9-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="a15d9-165">Když je hlavní produkt otevřený, vyberte **Varianty produktu** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="a15d9-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="a15d9-166">V podokně Akce vyberte možnost **Návrhy variant**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="a15d9-167">Vyberte hodnoty, které chcete použít pro každou dimenzi.</span><span class="sxs-lookup"><span data-stu-id="a15d9-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="a15d9-168">Na horním panelu nástrojů vyberte **Navrhnout**.</span><span class="sxs-lookup"><span data-stu-id="a15d9-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="a15d9-169">Systém generuje seznam všech možných kombinací velikostí a barev, které jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="a15d9-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="a15d9-170">Na rychlé kartě **Navrhované varianty** zaškrtněte políčko pro každou kombinaci dimenze produktu, kterou chcete použít, nebo vyberte **Vybrat vše** na panelu nástrojů a vyberte je všechny.</span><span class="sxs-lookup"><span data-stu-id="a15d9-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="a15d9-171">Vybrat **Vytvořit** k přidání variant do aktuálního hlavního produktu.</span><span class="sxs-lookup"><span data-stu-id="a15d9-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
