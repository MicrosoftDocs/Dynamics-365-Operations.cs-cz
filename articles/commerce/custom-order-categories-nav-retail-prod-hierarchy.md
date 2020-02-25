---
title: Změna pořadí řazení pro maloobchodní entity
description: Toto téma vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje v aplikaci Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021830"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="7935c-103">Změna pořadí řazení pro maloobchodní entity</span><span class="sxs-lookup"><span data-stu-id="7935c-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7935c-104">Maloobchodní prodejci považují vyhledání produktu za primární nástrojem pro interakci se zákazníkem ve všech kanálech.</span><span class="sxs-lookup"><span data-stu-id="7935c-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="7935c-105">Různé funkce mohou zákazníkům pomoci snadno objevit produkty.</span><span class="sxs-lookup"><span data-stu-id="7935c-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="7935c-106">Mohou například procházet kategorie, vyhledávat a filtrovat.</span><span class="sxs-lookup"><span data-stu-id="7935c-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="7935c-107">Toto téma vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje.</span><span class="sxs-lookup"><span data-stu-id="7935c-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="7935c-108">Dále je zde vysvětleno, jak změnit pořadí řazení.</span><span class="sxs-lookup"><span data-stu-id="7935c-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="7935c-109">Přehled</span><span class="sxs-lookup"><span data-stu-id="7935c-109">Overview</span></span>

<span data-ttu-id="7935c-110">Podpora třídění různých entit souvisejících s podporou prodeje byla vylepšena.</span><span class="sxs-lookup"><span data-stu-id="7935c-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="7935c-111">Tato podpora je nyní lépe sladěna se stávajícími scénáři odběratele, které dříve vyžadovaly rozšíření od implementačních partnerů.</span><span class="sxs-lookup"><span data-stu-id="7935c-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="7935c-112">Ve verzích Retail starších než 10.0.5 bylo pořadí řazení kategorií v navigační hierarchii abecední.</span><span class="sxs-lookup"><span data-stu-id="7935c-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="7935c-113">Nová funkce vlastního pořadí řazení umožňuje manažerům podpory prodeje konfigurovat pořadí řazení pro různé entity související s podporou prodeje napříč všemi klienty koncových uživatelů.</span><span class="sxs-lookup"><span data-stu-id="7935c-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="7935c-114">Mezi tyto klienty patří centrála (HQ) a kontaktní střediska.</span><span class="sxs-lookup"><span data-stu-id="7935c-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="7935c-115">Konfigurace pořadí zobrazení pro kategorie v hierarchii produktů</span><span class="sxs-lookup"><span data-stu-id="7935c-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="7935c-116">Před provedením tohoto postupu je nutné, aby byla v prostředí nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="7935c-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="7935c-117">Přejděte na **Retail and Commerce \> Produkty a kategorie \> Hierarchie produktů Commerce**.</span><span class="sxs-lookup"><span data-stu-id="7935c-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="7935c-118">Klikněte na možnost **Upravit hierarchii kategorií**.</span><span class="sxs-lookup"><span data-stu-id="7935c-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="7935c-119">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="7935c-119">Click **Edit**.</span></span>
4. <span data-ttu-id="7935c-120">Ve stromovém zobrazení rozbalte **VŠE \> Akční sporty**.</span><span class="sxs-lookup"><span data-stu-id="7935c-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="7935c-121">Ve stromovém zobrazení rozbalte **VŠE \> Týmové sporty**.</span><span class="sxs-lookup"><span data-stu-id="7935c-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="7935c-122">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="7935c-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="7935c-123">(Číslo může být záporné.)</span><span class="sxs-lookup"><span data-stu-id="7935c-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="7935c-124">Zopakujte kroky 4 až 6 pro všechny další kategorie, u kterých chcete změnit pořadí.</span><span class="sxs-lookup"><span data-stu-id="7935c-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="7935c-125">Pořadí zobrazení hierarchie navigace kanálu se odrazí v centrále pro hierarchii produktů commerce a uvolněné produkty podle kategorie.</span><span class="sxs-lookup"><span data-stu-id="7935c-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Vlastní řazení hierarchie produktů se zápornými hodnotami](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vlastní řazení uvolněných produktů podle kategorie na základě hierarchie produktů](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="7935c-128">Konfigurace pořadí zobrazení pro kategorie v hierarchii navigace kanálů</span><span class="sxs-lookup"><span data-stu-id="7935c-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="7935c-129">Před provedením tohoto postupu je nutné, aby byla v prostředí nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="7935c-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="7935c-130">Přejděte na **Retail and Commerce \> Produkty a kategorie \> Navigační kategorie kanálu**.</span><span class="sxs-lookup"><span data-stu-id="7935c-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="7935c-131">V seznamu vyberte hierarchii navigace **Móda**.</span><span class="sxs-lookup"><span data-stu-id="7935c-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="7935c-132">Klikněte na možnost **Upravit hierarchii kategorií**.</span><span class="sxs-lookup"><span data-stu-id="7935c-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="7935c-133">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="7935c-133">Click **Edit**.</span></span>
5. <span data-ttu-id="7935c-134">Ve stromové struktuře vyberte **Móda \> Dámské oděvy \> Dámské boty**.</span><span class="sxs-lookup"><span data-stu-id="7935c-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="7935c-135">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="7935c-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="7935c-136">Ve stromové struktuře vyberte **Móda \> Dámské oděvy \> Halenky**.</span><span class="sxs-lookup"><span data-stu-id="7935c-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="7935c-137">Obdobně můžete definovat pořadí řazení pro dílčí kategorie.</span><span class="sxs-lookup"><span data-stu-id="7935c-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="7935c-138">Ve stromové struktuře vyberte **Móda \> Pánské oděvy \> Košile pro volný čas**.</span><span class="sxs-lookup"><span data-stu-id="7935c-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="7935c-139">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="7935c-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="7935c-140">Ve stromové struktuře vyberte **Móda \> Pánské oděvy \> Kabáty a bundy**.</span><span class="sxs-lookup"><span data-stu-id="7935c-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="7935c-141">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="7935c-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="7935c-142">Zopakujte kroky pro všechny další kategorie, u kterých chcete změnit pořadí.</span><span class="sxs-lookup"><span data-stu-id="7935c-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="7935c-143">Pořadí zobrazení hierarchie navigace kanálu se odráží v centrále, katalogu a kanálech.</span><span class="sxs-lookup"><span data-stu-id="7935c-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Vlastní řazení hierarchie navigace kanálu](./media/ChannelNavCustomSorted.png)

![Vlastní řazení hierarchie navigace katalogu na základě hierarchie navigace kanálu](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS s vlastním řazením kategorií](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="7935c-147">Ve výchozím nastavení je funkce vlastního řazení vypnutá.</span><span class="sxs-lookup"><span data-stu-id="7935c-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="7935c-148">Informace o zapnutí této funkce a dalších funkcí naleznete v tématu [Správa funkcí](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="7935c-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
