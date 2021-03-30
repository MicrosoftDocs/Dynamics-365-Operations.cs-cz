---
title: Definování finančních dimenzí
description: Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf0136f216e5aa04cfae35afdb02d79893a6d39c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240731"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="896b7-103">Definování finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="896b7-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="896b7-104">Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="896b7-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="896b7-105">Průvodce používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="896b7-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="896b7-106">Vytvoření finanční dimenze zálohované entitou</span><span class="sxs-lookup"><span data-stu-id="896b7-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="896b7-107">Přejděte do části **Navigační podokno > Moduly > Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze**.</span><span class="sxs-lookup"><span data-stu-id="896b7-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="896b7-108">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="896b7-108">Click **New**.</span></span>
3. <span data-ttu-id="896b7-109">V poli **Formulář hodnot uživatele** vyberte systémem definovanou entitu jako základ finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="896b7-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="896b7-110">V poli **Název dimenze** zadejte hodnotu pro popis finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="896b7-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="896b7-111">Název může být jiný než entita definovaná systémem, nesmí však obsahovat mezery ani speciální znaky.</span><span class="sxs-lookup"><span data-stu-id="896b7-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="896b7-112">Klepněte na tlačítko **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="896b7-112">Click **Activate**.</span></span> <span data-ttu-id="896b7-113">Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere.</span><span class="sxs-lookup"><span data-stu-id="896b7-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="896b7-114">Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.</span><span class="sxs-lookup"><span data-stu-id="896b7-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="896b7-115">Klikněte na **Zavřít** na aktivační zprávě.</span><span class="sxs-lookup"><span data-stu-id="896b7-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="896b7-116">Klepněte na tlačítko **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="896b7-116">Click **Activate**.</span></span> <span data-ttu-id="896b7-117">Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.</span><span class="sxs-lookup"><span data-stu-id="896b7-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="896b7-118">V **Podokně akcí** klikněte na možnost **Hodnoty dimenze**.</span><span class="sxs-lookup"><span data-stu-id="896b7-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="896b7-119">Některé hodnoty dimenze jsou konkrétní pro společnosti.</span><span class="sxs-lookup"><span data-stu-id="896b7-119">Some dimension values are company specific.</span></span> <span data-ttu-id="896b7-120">Zda jsou konkrétní pro společnost můžete ověřit, bude-li název společnosti zobrazen v seznamu hodnot dimenzí.</span><span class="sxs-lookup"><span data-stu-id="896b7-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="896b7-121">Vytvoření vlastní finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="896b7-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="896b7-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="896b7-122">Close the page.</span></span>
2. <span data-ttu-id="896b7-123">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="896b7-123">Click **New**.</span></span>
3. <span data-ttu-id="896b7-124">V poli **Použít hodnoty od** vyberte **Vlastní dimenze**.</span><span class="sxs-lookup"><span data-stu-id="896b7-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="896b7-125">V poli **Název dimenze** zadejte hodnotu pro popis finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="896b7-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="896b7-126">Název nemůže obsahovat mezery ani speciální znaky.</span><span class="sxs-lookup"><span data-stu-id="896b7-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="896b7-127">Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="896b7-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="896b7-128">Můžete zadat znaky, které zůstávají pro každou hodnotu dimenze stejné, například písmena nebo pomlčky.</span><span class="sxs-lookup"><span data-stu-id="896b7-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="896b7-129">Můžete také zadat znaky čísel (#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena.</span><span class="sxs-lookup"><span data-stu-id="896b7-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="896b7-130">Použijte znak čísla (#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno.</span><span class="sxs-lookup"><span data-stu-id="896b7-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="896b7-131">Příklad: K omezení hodnoty dimenze na písmena CC a tři čísla zadejte jako masku formátu CC-###.</span><span class="sxs-lookup"><span data-stu-id="896b7-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="896b7-132">Klepněte na tlačítko **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="896b7-132">Click **Activate**.</span></span> <span data-ttu-id="896b7-133">Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere.</span><span class="sxs-lookup"><span data-stu-id="896b7-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="896b7-134">Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.</span><span class="sxs-lookup"><span data-stu-id="896b7-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="896b7-135">Klepněte na tlačítko **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="896b7-135">Click **Activate**.</span></span> <span data-ttu-id="896b7-136">Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.</span><span class="sxs-lookup"><span data-stu-id="896b7-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="896b7-137">V **Podokně akcí** klikněte na možnost **Hodnoty dimenze**.</span><span class="sxs-lookup"><span data-stu-id="896b7-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="896b7-138">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="896b7-138">Click **New**.</span></span>
9. <span data-ttu-id="896b7-139">V poli **Hodnota dimenze** zadejte název pro popis vaší finanční hodnoty.</span><span class="sxs-lookup"><span data-stu-id="896b7-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="896b7-140">V poli **Popis** zadejte popis, který popisuje vaši hodnotu finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="896b7-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]