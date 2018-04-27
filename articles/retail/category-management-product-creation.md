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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2246024d7d70947690173f3d0768292abe43efd7
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="c407d-103">Správa kategorií a produktů maloobchodu</span><span class="sxs-lookup"><span data-stu-id="c407d-103">Manage Retail product categories and products</span></span>

[!INCLUDE [banner](./includes/banner.md)]

<span data-ttu-id="c407d-104">Toto téma popisuje rozšířený způsob správy kategorií maloobchodních produktů a produktů v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="c407d-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="c407d-105">Tato zlepšení umožní obchodním manažerům zobrazit společnou strukturu vlastností produktu sdílenou mezi hierarchií maloobchodních produktů a podrobnostmi uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="c407d-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="c407d-106">Další informace o správě v kategoriích maloobchodního produktu získáte tak, že v pracovním prostoru **Správa kategorie a produktu** vyberete dlaždici **Maloobchodní hierarchie produktů**.</span><span class="sxs-lookup"><span data-stu-id="c407d-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="c407d-107">Všimněte si vylepšené struktury rozšířené stránky **maloobchodní hierarchie produktů**, která se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="c407d-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="c407d-108">V předchozích verzích aplikace Retail byly vlastnosti produktu rozděleny na *základní vlastnosti základních* a *vlastností maloobchodních produktů*, podle rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="c407d-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="c407d-109">Vlastnosti maloobchodních produktů jsou *globální* v rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="c407d-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="c407d-110">Jinými slovy, pro danou vlastnost maloobchodního produktu se stejná hodnota sdílí mezi všemi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="c407d-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="c407d-111">Naproti tomu, vlastnosti základních produktů jsou *specifické pro právnickou osobu*.</span><span class="sxs-lookup"><span data-stu-id="c407d-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="c407d-112">Jinými slovy, pro danou vlastnost základního produktu se může hodnota lišit napříč právnickými osobami, v závislosti na obchodních požadavcích každého právního subjektu.</span><span class="sxs-lookup"><span data-stu-id="c407d-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="c407d-113">V rozšířené struktuře kategorie maloobchodních produktů jsou vlastnosti produktu logicky odděleny podle jejich použitelnosti v rámci skupiny tak, aby odrážely strukturu formuláře podrobností uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="c407d-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Seskupení polí podle jejich rozsahu použitelnosti](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="c407d-115">Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="c407d-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="c407d-116">Abyste mohli spravovat vlastnosti ve všech právnických osobách, vyberte **zobrazit pro všechny právnické osoby** (nebo **upravit pro všechny právnické osoby**).</span><span class="sxs-lookup"><span data-stu-id="c407d-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Zobrazit nebo upravit pro všechny právnické osoby](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="c407d-118">Abyste mohli spravovat vlastnosti pro určitou právnickou osobu, vyberte **zobrazit pro určité právnické osoby** (nebo **upravit pro specifickou právnickou osobu**).</span><span class="sxs-lookup"><span data-stu-id="c407d-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Zobrazit nebo upravit pro specifickou právnickou osobu](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="c407d-120">Dále pak ve vylepšené kategorii maloobchodních produktů může ve srovnání s předchozími verzemi v nové struktuře kategorií maloobchodních produktů obchodní manažer také definovat výchozí hodnoty pro další sadu vlastností produktů na individuální úrovni kategorií.</span><span class="sxs-lookup"><span data-stu-id="c407d-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="c407d-121">Po vytvoření produktů se tyto výchozí hodnoty vlastností produktu dědí podle produktu na základě jejich přidružení k jednotlivé kategorii z hierarchie maloobchodních produktů.</span><span class="sxs-lookup"><span data-stu-id="c407d-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="c407d-122">Tyto zděděné vlastnosti produktu lze upravit pro každý produkt za účelem splnění jednotlivých obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="c407d-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="c407d-123">Výběr vlastností pro aktualizaci produktů ze stránky hierarchie maloobchodních produktů</span><span class="sxs-lookup"><span data-stu-id="c407d-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="c407d-124">Tuto novou rozšířenou strukturu vlastností produktu můžete použít pro výběr aktualizovaných vlastností produktu, které je třeba odeslat k přiřazeným produktům.</span><span class="sxs-lookup"><span data-stu-id="c407d-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="c407d-125">Na stránce **maloobchodní hierarchie produktů** v podokně akcí vyberte **kategorie**a poté vyberte **aktualizovat produkty** k otevření dialogového okna **Aktualizace produktů**.</span><span class="sxs-lookup"><span data-stu-id="c407d-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialogové okno Aktualizovat produkty](media/NewUpdateProductsEnhancedView.PNG)


