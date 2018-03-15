---
title: "Omezení tabulek definovaná uživatelem nebo systémem"
description: "Tento článek popisuje dva typy omezení tabulky pro komponenty v modelu konfigurace produktu - definované uživatelem a systémem. Omezení tabulky představují matice povolených kombinací atributů, kde každý řádek určuje jednu sadu možných hodnot atributů."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 4da560ca3cce5a28edd2a00506f825d5d88ef0f3
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="718e0-104">Omezení tabulek definovaná uživatelem nebo systémem</span><span class="sxs-lookup"><span data-stu-id="718e0-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="718e0-105">Tento článek popisuje dva typy omezení tabulky pro komponenty v modelu konfigurace produktu - definované uživatelem a systémem.</span><span class="sxs-lookup"><span data-stu-id="718e0-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="718e0-106">Omezení tabulky představují matice povolených kombinací atributů, kde každý řádek určuje jednu sadu možných hodnot atributů.</span><span class="sxs-lookup"><span data-stu-id="718e0-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="718e0-107">Omezení tabulek představují matice kombinací atributů, které jsou povoleny pro komponenty v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="718e0-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="718e0-108">Každý řádek v tabulce definuje jednu sadu možných hodnoty atributů.</span><span class="sxs-lookup"><span data-stu-id="718e0-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="718e0-109">V modelu konfigurace produktu můžete deklarovat dva typy omezení:</span><span class="sxs-lookup"><span data-stu-id="718e0-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="718e0-110">**Omezení výrazu** – vytvoření výrazu, který definuje vztahy mezi atributy, aby bylo zaručeno, že lze vybrat pouze kompatibilní hodnoty během konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="718e0-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="718e0-111">**Omezení tabulky** – vytvoření tabulky, která definuje všechny kombinace povolené pro zadanou sadu atributů.</span><span class="sxs-lookup"><span data-stu-id="718e0-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="718e0-112">Jsou k dispozici dva typy omezení tabulky: omezení tabulky definované uživatelem a omezení tabulky definované systémem.</span><span class="sxs-lookup"><span data-stu-id="718e0-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="718e0-113">Tento článek popisuje omezení tabulky definovaná uživatelem a systémem pro komponenty v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="718e0-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="718e0-114">Omezení tabulky definované uživatelem</span><span class="sxs-lookup"><span data-stu-id="718e0-114">User-defined table constraints</span></span>
<span data-ttu-id="718e0-115">Omezení tabulky definované uživatelem je typ matice, který se používá k popisu kombinací hodnot atributů, které jsou definovány pomocí typů atributů.</span><span class="sxs-lookup"><span data-stu-id="718e0-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="718e0-116">Například pokud se vyrobí reproduktory, můžete v omezení tabulky definované uživatelem použít sloupce pro povrchovou úpravu skříně a přední mřížku.</span><span class="sxs-lookup"><span data-stu-id="718e0-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="718e0-117">Typ atributu pro povrchovou úpravu skříně má čtyři hodnoty a typ atributu pro přední mřížku má tři hodnoty.</span><span class="sxs-lookup"><span data-stu-id="718e0-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="718e0-118">Takže pokud omezení nejsou použita, je k dispozici 4 x 3 = 12 možných kombinací.</span><span class="sxs-lookup"><span data-stu-id="718e0-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="718e0-119">Avšak v tomto příkladu je dovoleno pouze šest kombinací, jak je vidět v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="718e0-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="718e0-120">Tyto informace se zobrazí na kartě **Povolené kombinace** na stránce **Upravit omezení tabulky**.</span><span class="sxs-lookup"><span data-stu-id="718e0-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="718e0-121">Povrch skříňky</span><span class="sxs-lookup"><span data-stu-id="718e0-121">Cabinet finish</span></span> | <span data-ttu-id="718e0-122">Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="718e0-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="718e0-123">Černá</span><span class="sxs-lookup"><span data-stu-id="718e0-123">Black</span></span>          | <span data-ttu-id="718e0-124">Černá</span><span class="sxs-lookup"><span data-stu-id="718e0-124">Black</span></span>       |
| <span data-ttu-id="718e0-125">Černá</span><span class="sxs-lookup"><span data-stu-id="718e0-125">Black</span></span>          | <span data-ttu-id="718e0-126">Kov</span><span class="sxs-lookup"><span data-stu-id="718e0-126">Metal</span></span>       |
| <span data-ttu-id="718e0-127">Dub</span><span class="sxs-lookup"><span data-stu-id="718e0-127">Oak</span></span>            | <span data-ttu-id="718e0-128">Černá</span><span class="sxs-lookup"><span data-stu-id="718e0-128">Black</span></span>       |
| <span data-ttu-id="718e0-129">Palisandr</span><span class="sxs-lookup"><span data-stu-id="718e0-129">Rosewood</span></span>       | <span data-ttu-id="718e0-130">Bílá</span><span class="sxs-lookup"><span data-stu-id="718e0-130">White</span></span>       |
| <span data-ttu-id="718e0-131">Bílá</span><span class="sxs-lookup"><span data-stu-id="718e0-131">White</span></span>          | <span data-ttu-id="718e0-132">Černá</span><span class="sxs-lookup"><span data-stu-id="718e0-132">Black</span></span>       |
| <span data-ttu-id="718e0-133">Bílá</span><span class="sxs-lookup"><span data-stu-id="718e0-133">White</span></span>          | <span data-ttu-id="718e0-134">Bílá</span><span class="sxs-lookup"><span data-stu-id="718e0-134">White</span></span>       |

<span data-ttu-id="718e0-135">Omezení tabulky definovaná uživatelem jsou definována vstupem statické tabulky, který pracuje stejně jako omezení výrazu.</span><span class="sxs-lookup"><span data-stu-id="718e0-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="718e0-136">Při použití omezení tabulky definovaného uživatelem přináší výhodu v tom, že se tabulky často snadněji vytváří a udržují (a jsou také přehlednější) než dlouhá omezení výrazu.</span><span class="sxs-lookup"><span data-stu-id="718e0-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="718e0-137">Omezení tabulek definovaná systémem</span><span class="sxs-lookup"><span data-stu-id="718e0-137">System-defined table constraints</span></span>
<span data-ttu-id="718e0-138">Omezení tabulky definované systémem vytvoří dynamické mapování mezi typem atributu a polem v tabulce.</span><span class="sxs-lookup"><span data-stu-id="718e0-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="718e0-139">Pokud je v modelu konfigurace produktu zahrnuto omezení tabulky definované systémem, mapování zaručuje, že se v tabulce zobrazí data místo hodnot typů atributů.</span><span class="sxs-lookup"><span data-stu-id="718e0-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="718e0-140">Výsledkem je dynamické omezení, protože obsah tabulky lze upravit (například z jiných modulů).</span><span class="sxs-lookup"><span data-stu-id="718e0-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="718e0-141">Při vytváření omezení tabulky definovaného systémem vyberte tabulku, volitelně můžete definovat dotaz a potom můžete přidružit typy atributů k polím ve vybrané tabulce.</span><span class="sxs-lookup"><span data-stu-id="718e0-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="718e0-142">Typy polí musí odpovídat typům atributů.</span><span class="sxs-lookup"><span data-stu-id="718e0-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="718e0-143">Aby mohlo mít omezení tabulky vliv na model konfigurace produktu, je nutno zahrnout omezení tabulky do omezení v jedné z komponent modelu.</span><span class="sxs-lookup"><span data-stu-id="718e0-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="718e0-144">Je třeba vytvořit nové omezení, vybrat typ omezení tabulky a poté vybrat definici omezení tabulky, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="718e0-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="718e0-145">Nakonec je nutno všechna pole v omezení tabulky namapovat na atributy v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="718e0-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="718e0-146">Viz také</span><span class="sxs-lookup"><span data-stu-id="718e0-146">See also</span></span>
--------

[<span data-ttu-id="718e0-147">Základní koncepty v modelech konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="718e0-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)




