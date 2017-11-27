---
title: "Správa a vytvoření kategorií produktů"
description: "Toto téma popisuje vylepšení provedená pro správu kategorií maloobchodního produktu. Tato zlepšení umožní obchodním manažerům udržovat korelaci mezi hierarchií maloobchodních produktů a podrobnostmi o uvolněném produktu."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Retail
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 98250062892e0c5f665616dc3944181a3ff8599a
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="bc625-104">Správa a vytvoření kategorií produktů</span><span class="sxs-lookup"><span data-stu-id="bc625-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="bc625-105">Vylepšení provedená pro správu kategorií maloobchodního produktu umožní obchodním manažerům udržovat korelaci mezi hierarchií maloobchodních produktů a podrobnostmi o uvolněném produktu.</span><span class="sxs-lookup"><span data-stu-id="bc625-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="bc625-106">Chcete-li zobrazit tato vylepšení, zvolte v pracovním prostoru **Správa kategorií a produktů** možnost **Hierarchie maloobchodních produktů** a otevřete stránku **Nová struktura kategorií maloobchodních produktů**.</span><span class="sxs-lookup"><span data-stu-id="bc625-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="bc625-107">V předchozích verzích byly vlastnosti produktu rozděleny do vlastností základních produktů a vlastností maloobchodních produktů, podle rozsahu použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="bc625-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="bc625-108">Vlastnosti maloobchodních produktů byly *globální*.</span><span class="sxs-lookup"><span data-stu-id="bc625-108">Retail product properties were *global*.</span></span> <span data-ttu-id="bc625-109">Jinými slovy, pro danou vlastnost produktu se stejná hodnota sdílí mezi všemi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="bc625-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="bc625-110">Vlastnosti základních produktů byly *specifické pro právnickou osobu*.</span><span class="sxs-lookup"><span data-stu-id="bc625-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="bc625-111">Jinými slovy, daná vlastnost produktu se může lišit napříč právnickými osobami, v závislosti na obchodních požadavcích.</span><span class="sxs-lookup"><span data-stu-id="bc625-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="bc625-112">Pomocí těchto vylepšení vlastností produktů v kategorii maloobchodních produktů pokračujeme v oddělování polí, podle jejich použitelnosti v rámci skupiny tak, aby odrážela strukturu formuláře podrobností uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="bc625-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="bc625-113">Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="bc625-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="bc625-114">Pouze vyberte podle potřeby buď **Zobrazit/upravit pro všechny právnické osoby** nebo **Zobrazit/upravit pro konkrétní právnickou osobu**.</span><span class="sxs-lookup"><span data-stu-id="bc625-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="bc625-115">Obchodní manažeři mohou také definovat výchozí hodnoty pro další sadu vlastností produktu na úrovni jednotlivé kategorie.</span><span class="sxs-lookup"><span data-stu-id="bc625-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="bc625-116">Tyto hodnoty vlastností produkt dědí na základě jejich přidružení k kategorii v době vytvoření produktu.</span><span class="sxs-lookup"><span data-stu-id="bc625-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="bc625-117">Vyberte vlastnosti, abyste aktualizovali produkty z formuláře kategorií maloobchodních produktů</span><span class="sxs-lookup"><span data-stu-id="bc625-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="bc625-118">Abyste vybrali, které vlastnosti aktualizovaných produktů mají být odeslány k přidruženým produktům, můžete použít vlastnosti logického seskupování.</span><span class="sxs-lookup"><span data-stu-id="bc625-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="bc625-119">Obchodní manažeři mohou upravit tyto zděděné vlastnosti produktů pro každý produkt za účelem splnění jednotlivých obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="bc625-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

