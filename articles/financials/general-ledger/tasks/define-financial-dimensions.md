---
title: Definování finančních dimenzí
description: Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a30872daeeeb6d7d2accb07e9fdbdc84bb8dc5e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846456"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="0d4a7-103">Definování finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="0d4a7-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d4a7-104">Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="0d4a7-105">Průvodce používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="0d4a7-106">Vytvoření finanční dimenze zálohované entitou</span><span class="sxs-lookup"><span data-stu-id="0d4a7-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="0d4a7-107">Přejděte do části Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="0d4a7-108">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-108">Click New.</span></span>
3. <span data-ttu-id="0d4a7-109">V poli formuláře Hodnoty uživatele vyberte systémem definovanou entitu jako základ finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-109">In the User values form field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="0d4a7-110">V poli Název dimenze zadejte hodnotu pro popis finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="0d4a7-111">Název může být jiný než entita definovaná systémem, nesmí však obsahovat mezery ani speciální znaky.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="0d4a7-112">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-112">Click Activate.</span></span>
    * <span data-ttu-id="0d4a7-113">Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="0d4a7-114">Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="0d4a7-115">Klepněte na Zavřít na aktivační zprávě.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="0d4a7-116">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-116">Click Activate.</span></span>
    * <span data-ttu-id="0d4a7-117">Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="0d4a7-118">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-118">Click Dimension values.</span></span>
    * <span data-ttu-id="0d4a7-119">Některé hodnoty dimenze jsou konkrétní pro společnosti.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-119">Some dimension values are company specific.</span></span> <span data-ttu-id="0d4a7-120">Zda jsou konkrétní pro společnost můžete ověřit, bude-li název společnosti zobrazen v seznamu hodnot dimenzí.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="0d4a7-121">Vytvoření vlastní finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="0d4a7-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="0d4a7-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-122">Close the page.</span></span>
2. <span data-ttu-id="0d4a7-123">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-123">Click New.</span></span>
3. <span data-ttu-id="0d4a7-124">V poli Použít hodnoty od vyberte Vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-124">In the Use values from field, select Custom dimension.</span></span>
4. <span data-ttu-id="0d4a7-125">V poli Název dimenze zadejte hodnotu pro popis finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="0d4a7-126">Název nemůže obsahovat mezery ani speciální znaky.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="0d4a7-127">Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="0d4a7-128">Můžete zadat znaky, které zůstávají pro každou hodnotu dimenze stejné, například písmena nebo pomlčky.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="0d4a7-129">Můžete také zadat znaky čísel (#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="0d4a7-130">Použijte znak čísla (#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="0d4a7-131">Příklad: K omezení hodnoty dimenze na písmena CC a tři čísla zadejte jako masku formátu CC-###.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="0d4a7-132">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-132">Click Activate.</span></span>
    * <span data-ttu-id="0d4a7-133">Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="0d4a7-134">Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="0d4a7-135">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-135">Click Activate.</span></span>
    * <span data-ttu-id="0d4a7-136">Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="0d4a7-137">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-137">Click Dimension values.</span></span>
8. <span data-ttu-id="0d4a7-138">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-138">Click New.</span></span>
9. <span data-ttu-id="0d4a7-139">V poli hodnota dimenze zadejte název pro popis vaší finanční hodnoty.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="0d4a7-140">V poli Popis zadejte popis, který popisuje vaši hodnotu finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-140">In the Description field, type a description that describes your financial dimension value.</span></span>

