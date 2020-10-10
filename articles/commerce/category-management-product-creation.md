---
title: Správa kategorií produktů a produktů
description: Toto téma popisuje, jak obchodní manažeři mohou použít kategorie maloobchodní produktů ke správě vztahů mezi hierarchií produktů Commerce a podrobnostmi uvolněného produktu.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9d47a866703b830e84e3f2e37a02d9d58f73987b
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895418"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="d788e-103">Správa kategorií produktů a produktů</span><span class="sxs-lookup"><span data-stu-id="d788e-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="d788e-104">Toto téma popisuje rozšířený způsob správy kategorií produktů a produktů v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d788e-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d788e-105">Tato zlepšení umožní obchodním manažerům zobrazit společnou strukturu vlastností produktu sdílenou mezi hierarchií produktů a podrobnostmi uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="d788e-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="d788e-106">Další informace o správě v kategoriích produktu získáte tak, že v pracovním prostoru **Správa kategorie a produktu** vyberete dlaždici **Hierarchie produktů Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d788e-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="d788e-107">Všimněte si vylepšené struktury rozšířené stránky **Hierarchie produktů Commerce**, která se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="d788e-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="d788e-108">V předchozích verzích aplikace byly vlastnosti produktu rozděleny na *základní vlastnosti základních* a *vlastností maloobchodních produktů*, podle rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="d788e-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="d788e-109">Vlastnosti maloobchodních produktů jsou *globální* v rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="d788e-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="d788e-110">Jinými slovy, pro danou vlastnost produktu se stejná hodnota sdílí mezi všemi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="d788e-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="d788e-111">Naproti tomu, vlastnosti základních produktů jsou *specifické pro právnickou osobu*.</span><span class="sxs-lookup"><span data-stu-id="d788e-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="d788e-112">Jinými slovy, pro danou vlastnost základního produktu se může hodnota lišit napříč právnickými osobami, v závislosti na obchodních požadavcích každého právního subjektu.</span><span class="sxs-lookup"><span data-stu-id="d788e-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="d788e-113">V rozšířené struktuře kategorie produktů jsou vlastnosti produktu logicky odděleny podle jejich použitelnosti v rámci skupiny tak, aby odrážely strukturu formuláře podrobností uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="d788e-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Seskupení polí podle jejich rozsahu použitelnosti](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="d788e-115">Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d788e-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="d788e-116">Abyste mohli spravovat vlastnosti ve všech právnických osobách, vyberte **zobrazit pro všechny právnické osoby** (nebo **upravit pro všechny právnické osoby**).</span><span class="sxs-lookup"><span data-stu-id="d788e-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Zobrazit nebo upravit pro všechny právnické osoby](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="d788e-118">Abyste mohli spravovat vlastnosti pro určitou právnickou osobu, vyberte **zobrazit pro určité právnické osoby** (nebo **upravit pro specifickou právnickou osobu**).</span><span class="sxs-lookup"><span data-stu-id="d788e-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Zobrazit nebo upravit pro specifickou právnickou osobu](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="d788e-120">Dále pak ve vylepšené kategorii produktů může ve srovnání s předchozími verzemi v nové struktuře kategorií maloobchodních produktů obchodní manažer také definovat výchozí hodnoty pro další sadu vlastností produktů na individuální úrovni kategorií.</span><span class="sxs-lookup"><span data-stu-id="d788e-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="d788e-121">Po vytvoření produktů se tyto výchozí hodnoty vlastností produktu dědí podle produktu na základě jejich přidružení k jednotlivé kategorii z hierarchie produktů.</span><span class="sxs-lookup"><span data-stu-id="d788e-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="d788e-122">Tyto zděděné vlastnosti produktu lze upravit pro každý produkt za účelem splnění jednotlivých obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="d788e-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="d788e-123">Výběr vlastností pro aktualizaci produktů ze stránky hierarchie produktů Commerce</span><span class="sxs-lookup"><span data-stu-id="d788e-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="d788e-124">Tuto novou rozšířenou strukturu vlastností produktu můžete použít pro výběr aktualizovaných vlastností produktu, které je třeba odeslat k přiřazeným produktům.</span><span class="sxs-lookup"><span data-stu-id="d788e-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="d788e-125">Na stránce **Hierarchie produktů Commerce** v podokně akcí vyberte **kategorie**a poté vyberte **aktualizovat produkty** k otevření dialogového okna **Aktualizace produktů**.</span><span class="sxs-lookup"><span data-stu-id="d788e-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialogové okno Aktualizovat produkty](media/NewUpdateProductsEnhancedView.PNG)
