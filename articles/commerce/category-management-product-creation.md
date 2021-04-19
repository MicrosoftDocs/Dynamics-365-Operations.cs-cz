---
title: Správa kategorií produktů a produktů
description: Toto téma popisuje, jak obchodní manažeři mohou použít kategorie maloobchodní produktů ke správě vztahů mezi hierarchií produktů Commerce a podrobnostmi uvolněného produktu.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 678561856fbb5514ff954363a767091edac6dee2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794366"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="99079-103">Správa kategorií produktů a produktů</span><span class="sxs-lookup"><span data-stu-id="99079-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="99079-104">Toto téma popisuje rozšířený způsob správy kategorií produktů a produktů v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="99079-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="99079-105">Tato zlepšení umožní obchodním manažerům zobrazit společnou strukturu vlastností produktu sdílenou mezi hierarchií produktů a podrobnostmi uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="99079-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="99079-106">Další informace o správě v kategoriích produktu získáte tak, že v pracovním prostoru **Správa kategorie a produktu** vyberete dlaždici **Hierarchie produktů Commerce**.</span><span class="sxs-lookup"><span data-stu-id="99079-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="99079-107">Všimněte si vylepšené struktury rozšířené stránky **Hierarchie produktů Commerce**, která se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="99079-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="99079-108">V předchozích verzích aplikace byly vlastnosti produktu rozděleny na *základní vlastnosti základních* a *vlastností maloobchodních produktů*, podle rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="99079-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="99079-109">Vlastnosti maloobchodních produktů jsou *globální* v rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="99079-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="99079-110">Jinými slovy, pro danou vlastnost produktu se stejná hodnota sdílí mezi všemi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="99079-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="99079-111">Naproti tomu, vlastnosti základních produktů jsou *specifické pro právnickou osobu*.</span><span class="sxs-lookup"><span data-stu-id="99079-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="99079-112">Jinými slovy, pro danou vlastnost základního produktu se může hodnota lišit napříč právnickými osobami, v závislosti na obchodních požadavcích každého právního subjektu.</span><span class="sxs-lookup"><span data-stu-id="99079-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="99079-113">V rozšířené struktuře kategorie produktů jsou vlastnosti produktu logicky odděleny podle jejich použitelnosti v rámci skupiny tak, aby odrážely strukturu formuláře podrobností uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="99079-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Seskupení polí podle jejich rozsahu použitelnosti](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="99079-115">Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="99079-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="99079-116">Abyste mohli spravovat vlastnosti ve všech právnických osobách, vyberte **zobrazit pro všechny právnické osoby** (nebo **upravit pro všechny právnické osoby**).</span><span class="sxs-lookup"><span data-stu-id="99079-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Zobrazit nebo upravit pro všechny právnické osoby](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="99079-118">Abyste mohli spravovat vlastnosti pro určitou právnickou osobu, vyberte **zobrazit pro určité právnické osoby** (nebo **upravit pro specifickou právnickou osobu**).</span><span class="sxs-lookup"><span data-stu-id="99079-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Zobrazit nebo upravit pro specifickou právnickou osobu](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="99079-120">Dále pak ve vylepšené kategorii produktů může ve srovnání s předchozími verzemi v nové struktuře kategorií maloobchodních produktů obchodní manažer také definovat výchozí hodnoty pro další sadu vlastností produktů na individuální úrovni kategorií.</span><span class="sxs-lookup"><span data-stu-id="99079-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="99079-121">Po vytvoření produktů se tyto výchozí hodnoty vlastností produktu dědí podle produktu na základě jejich přidružení k jednotlivé kategorii z hierarchie produktů.</span><span class="sxs-lookup"><span data-stu-id="99079-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="99079-122">Tyto zděděné vlastnosti produktu lze upravit pro každý produkt za účelem splnění jednotlivých obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="99079-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="99079-123">Výběr vlastností pro aktualizaci produktů ze stránky hierarchie produktů Commerce</span><span class="sxs-lookup"><span data-stu-id="99079-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="99079-124">Tuto novou rozšířenou strukturu vlastností produktu můžete použít pro výběr aktualizovaných vlastností produktu, které je třeba odeslat k přiřazeným produktům.</span><span class="sxs-lookup"><span data-stu-id="99079-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="99079-125">Na stránce **Hierarchie produktů Commerce** v podokně akcí vyberte **kategorie** a poté vyberte **aktualizovat produkty** k otevření dialogového okna **Aktualizace produktů**.</span><span class="sxs-lookup"><span data-stu-id="99079-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialogové okno Aktualizovat produkty](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]