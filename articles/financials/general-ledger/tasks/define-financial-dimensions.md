--- 
title: "Definování finančních dimenzí"
description: "Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 147702c1036c0ada41719c27a033dd646de811f4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="1e129-103">Definování finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="1e129-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e129-104">Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="1e129-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="1e129-105">Průvodce používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="1e129-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="1e129-106">Vytvoření finanční dimenze zálohované entitou</span><span class="sxs-lookup"><span data-stu-id="1e129-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="1e129-107">Přejděte do části Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="1e129-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="1e129-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1e129-108">Click New.</span></span>
3. <span data-ttu-id="1e129-109">V poli Hodnoty uživatele od vyberte systémem definovanou entitu jako základ finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="1e129-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="1e129-110">V poli Název dimenze zadejte hodnotu pro popis finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="1e129-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="1e129-111">Název může být jiný než entita definovaná systémem, nesmí však obsahovat mezery ani speciální znaky.</span><span class="sxs-lookup"><span data-stu-id="1e129-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="1e129-112">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1e129-112">Click Activate.</span></span>
    * <span data-ttu-id="1e129-113">Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere.</span><span class="sxs-lookup"><span data-stu-id="1e129-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="1e129-114">Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.</span><span class="sxs-lookup"><span data-stu-id="1e129-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="1e129-115">Klepněte na Zavřít na aktivační zprávě.</span><span class="sxs-lookup"><span data-stu-id="1e129-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="1e129-116">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1e129-116">Click Activate.</span></span>
    * <span data-ttu-id="1e129-117">Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.</span><span class="sxs-lookup"><span data-stu-id="1e129-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="1e129-118">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="1e129-118">Click Dimension values.</span></span>
    * <span data-ttu-id="1e129-119">Některé hodnoty dimenze jsou konkrétní pro společnosti.</span><span class="sxs-lookup"><span data-stu-id="1e129-119">Some dimension values are company specific.</span></span> <span data-ttu-id="1e129-120">Zda jsou konkrétní pro společnost můžete ověřit, bude-li název společnosti zobrazen v seznamu hodnot dimenzí.</span><span class="sxs-lookup"><span data-stu-id="1e129-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="1e129-121">Vytvoření vlastní finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="1e129-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="1e129-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1e129-122">Close the page.</span></span>
2. <span data-ttu-id="1e129-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1e129-123">Click New.</span></span>
3. <span data-ttu-id="1e129-124">Vyberte možnost <Custom dimension> v poli Použít hodnoty od.</span><span class="sxs-lookup"><span data-stu-id="1e129-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="1e129-125">V poli Název dimenze zadejte hodnotu pro popis finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="1e129-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="1e129-126">Název nemůže obsahovat mezery ani speciální znaky.</span><span class="sxs-lookup"><span data-stu-id="1e129-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="1e129-127">Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="1e129-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="1e129-128">Můžete zadat znaky, které zůstávají pro každou hodnotu dimenze stejné, například písmena nebo pomlčky.</span><span class="sxs-lookup"><span data-stu-id="1e129-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="1e129-129">Můžete také zadat znaky čísel (#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena.</span><span class="sxs-lookup"><span data-stu-id="1e129-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="1e129-130">Použijte znak čísla (#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno.</span><span class="sxs-lookup"><span data-stu-id="1e129-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="1e129-131">Příklad: K omezení hodnoty dimenze na písmena CC a tři čísla zadejte jako masku formátu CC-###.</span><span class="sxs-lookup"><span data-stu-id="1e129-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="1e129-132">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1e129-132">Click Activate.</span></span>
    * <span data-ttu-id="1e129-133">Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere.</span><span class="sxs-lookup"><span data-stu-id="1e129-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="1e129-134">Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.</span><span class="sxs-lookup"><span data-stu-id="1e129-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="1e129-135">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1e129-135">Click Activate.</span></span>
    * <span data-ttu-id="1e129-136">Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.</span><span class="sxs-lookup"><span data-stu-id="1e129-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="1e129-137">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="1e129-137">Click Dimension values.</span></span>
8. <span data-ttu-id="1e129-138">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1e129-138">Click New.</span></span>
9. <span data-ttu-id="1e129-139">V poli hodnota dimenze zadejte název pro popis vaší finanční hodnoty.</span><span class="sxs-lookup"><span data-stu-id="1e129-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="1e129-140">V poli Popis zadejte popis, který popisuje vaši hodnotu finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="1e129-140">In the Description field, type a description that describes your financial dimension value.</span></span>


