---
title: Vytvoření nové hierarchie produktu
description: Toto téma popisuje, jak vytvořit novou hierarchii produktů v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410708"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="75be3-103">Vytvoření nové hierarchie produktu</span><span class="sxs-lookup"><span data-stu-id="75be3-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="75be3-104">Toto téma popisuje, jak vytvořit novou hierarchii produktů v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="75be3-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="75be3-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="75be3-105">Overview</span></span>

<span data-ttu-id="75be3-106">Dynamics 365 Commerce podporuje více maloobchodních sítí.</span><span class="sxs-lookup"><span data-stu-id="75be3-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="75be3-107">Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody).</span><span class="sxs-lookup"><span data-stu-id="75be3-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="75be3-108">Každý kanál maloobchodu může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="75be3-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="75be3-109">Všechny tyto prvky je třeba nastavit pro maloobchod před vytvořením kanálu maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="75be3-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="75be3-110">Hierarchie produktů Commerce se používá, chcete-li definovat celkovou hierarchii produktů pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="75be3-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="75be3-111">Hierarchii produktů Commerce lze použít pro výrobní události, tvorbu cen a promoakce, sestavy a plánování sortimentu.</span><span class="sxs-lookup"><span data-stu-id="75be3-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="75be3-112">Organizaci může být přiřazen pouze jedna hierarchie produktů Commerce.</span><span class="sxs-lookup"><span data-stu-id="75be3-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="75be3-113">Vytvoření a konfigurace hierarchie produktu</span><span class="sxs-lookup"><span data-stu-id="75be3-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="75be3-114">Chcete-li vytvořit a konfigurovat novou hierarchii produktů Commerce, postupujte dle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="75be3-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="75be3-115">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Hierarchie produktů Commerce**.</span><span class="sxs-lookup"><span data-stu-id="75be3-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="75be3-116">Pokud dosud žádná hierachie neexistuje, vyberte v **Podokně akcí** možnost **Nový** a vytvořte kořenový adresář hierarchie.</span><span class="sxs-lookup"><span data-stu-id="75be3-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="75be3-117">V **Obecné**:</span><span class="sxs-lookup"><span data-stu-id="75be3-117">Under **General**:</span></span>
    1. <span data-ttu-id="75be3-118">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="75be3-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="75be3-119">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="75be3-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="75be3-120">Do pole **Popisný název** zadejte popisný název produktu.</span><span class="sxs-lookup"><span data-stu-id="75be3-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="75be3-121">Nastavte **Aktivní** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="75be3-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="75be3-122">Přidání uzlů hierarchie</span><span class="sxs-lookup"><span data-stu-id="75be3-122">Add hierarchy nodes</span></span>

<span data-ttu-id="75be3-123">Chcete-li přidat uzly hierarchie, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="75be3-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="75be3-124">V podokně akcí vyberte možnost **Upravit hierarchii kategorií**.</span><span class="sxs-lookup"><span data-stu-id="75be3-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="75be3-125">Vyberte nadřazený uzel, do kterého chcete přidat nový uzel, a poté vyberte **Nový uzel kategorie**.</span><span class="sxs-lookup"><span data-stu-id="75be3-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="75be3-126">V části **Obecné** zadejte **název**, **popis**, **popisný název** a **klíčová slova**.</span><span class="sxs-lookup"><span data-stu-id="75be3-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="75be3-127">V **Obecné**:</span><span class="sxs-lookup"><span data-stu-id="75be3-127">Under **General**:</span></span>
    1. <span data-ttu-id="75be3-128">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="75be3-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="75be3-129">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="75be3-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="75be3-130">Do pole **Popisný název** zadejte popisný název produktu.</span><span class="sxs-lookup"><span data-stu-id="75be3-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="75be3-131">Do pole **klíčová slova** zadejte příslušná klíčová slova.</span><span class="sxs-lookup"><span data-stu-id="75be3-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="75be3-132">V poli **Pořadí zobrazení** zadejte číslo pořadí zobrazení (volitelné).</span><span class="sxs-lookup"><span data-stu-id="75be3-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="75be3-133">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="75be3-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="75be3-134">Zopakováním výše uvedených kroků přidejte další uzly.</span><span class="sxs-lookup"><span data-stu-id="75be3-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="75be3-135">V následujícím obrázku je znázorněno vytvoření nového uzlu hierarchie produktů.</span><span class="sxs-lookup"><span data-stu-id="75be3-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Vytvoření hierarchie produktu](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="75be3-137">Další nastavení</span><span class="sxs-lookup"><span data-stu-id="75be3-137">Other settings</span></span>

<span data-ttu-id="75be3-138">Skupiny atributů kategorií lze podle potřeby přiřadit ke každé skupině.</span><span class="sxs-lookup"><span data-stu-id="75be3-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="75be3-139">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="75be3-139">Additional resources</span></span>

[<span data-ttu-id="75be3-140">hierarchie obchodu</span><span class="sxs-lookup"><span data-stu-id="75be3-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="75be3-141">Správa kategorií produktů a produktů</span><span class="sxs-lookup"><span data-stu-id="75be3-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="75be3-142">Změna pořadí řazení pro entity podpory prodeje</span><span class="sxs-lookup"><span data-stu-id="75be3-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
