---
title: "Správa kategorií produktů"
description: "Toto téma popisuje, jak obchodní manažeři mohou použít kategorie maloobchodní produktů ke správě vztahů mezi hierarchií maloobchodních produktů a podrobnostmi uvolněného produktu."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: cs-cz
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="268fa-103">Rozšířená správa kategorií a produktů</span><span class="sxs-lookup"><span data-stu-id="268fa-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="268fa-104">Toto téma popisuje rozšířený způsob správy kategorií maloobchodních produktů a produktů v aplikaci Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="268fa-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="268fa-105">Tato zlepšení umožní obchodním manažerům zobrazit společnou strukturu vlastností produktu mezi hierarchií maloobchodních produktů a podrobnostmi uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="268fa-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="268fa-106">Pro další informace o správě kategorií maloobchodních produktů přejděte na položku **Hierarchie maloobchodních produktů** z pracovního prostoru **Správa kategorií a produktů** a všimněte si rozšířené struktury stránky **Kategorie maloobchodních produktů**.</span><span class="sxs-lookup"><span data-stu-id="268fa-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Pracovní prostor správy kategorií a produktů](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="268fa-108">V předchozích verzích byly vlastnosti produktu rozděleny do **vlastností základních produktů** a **vlastností maloobchodních produktů**, podle rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="268fa-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="268fa-109">**Vlastnosti maloobchodních produktů** byly *globální* podle rozsahu použitelnosti, což znamená, že pro dané **vlastnosti maloobchodních produktů** se sdílela stejná hodnota napříč všemi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="268fa-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="268fa-110">**Vlastnosti základních produktů** jsou *specifické pro právnickou osobu*.</span><span class="sxs-lookup"><span data-stu-id="268fa-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="268fa-111">Jinými slovy, pro danou **vlastnost základního produktu** se může hodnota lišit napříč právnickými osobami, v závislosti na obchodních požadavcích.</span><span class="sxs-lookup"><span data-stu-id="268fa-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="268fa-112">V rozšířené struktuře kategorie maloobchodních produktů jsou vlastnosti produktu logicky odděleny podle jejich použitelnosti v rámci skupiny tak, aby odrážely strukturu formuláře podrobností uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="268fa-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Seskupení polí podle jejich rozsahu použitelnosti](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="268fa-114">Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="268fa-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="268fa-115">To provedete výběrem možnosti **Zobrazit/upravit pro všechny právnické osoby** nebo **Zobrazit/upravit pro konkrétní právnickou osobu**.</span><span class="sxs-lookup"><span data-stu-id="268fa-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Přepnutí zobrazení mezi jednotlivými a všemi právnickými osobami](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Přepnutí zobrazení mezi jednotlivými a všemi právnickými osobami](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="268fa-118">Ve srovnání s předchozími verzemi může v nové struktuře kategorií maloobchodních produktů obchodní manažer také definovat výchozí hodnoty pro další sadu vlastností produktů na individuální úrovni kategorií.</span><span class="sxs-lookup"><span data-stu-id="268fa-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="268fa-119">V čase vytvoření produktu se tyto výchozí hodnoty vlastností produktu dědí podle produktu na základě jejich přidružení k jednotlivé kategorii z hierarchie maloobchodních produktů.</span><span class="sxs-lookup"><span data-stu-id="268fa-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="268fa-120">Tyto zděděné vlastnosti produktu lze upravit pro každý produkt za účelem splnění jednotlivých obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="268fa-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="268fa-121">Vyberte vlastnosti, abyste aktualizovali produkty z formuláře kategorií maloobchodních produktů</span><span class="sxs-lookup"><span data-stu-id="268fa-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="268fa-122">Tuto novou rozšířenou strukturu vlastností produktu můžete použít pro výběr aktualizovaných vlastností produktu, které je třeba odeslat k přiřazeným produktům.</span><span class="sxs-lookup"><span data-stu-id="268fa-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Nové rozšířené zobrazení možnosti Aktualizovat produkty](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="268fa-124">Obchodní manažeři mohou upravit tyto zděděné vlastnosti produktů pro každý produkt za účelem splnění jednotlivých obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="268fa-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


