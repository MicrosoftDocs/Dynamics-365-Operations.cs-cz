---
title: Změna pořadí řazení pro maloobchodní entity
description: Toto téma vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54929f924bd9c2b59dec453cf580e0b2bc149d38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799462"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="d27e3-103">Změna pořadí řazení pro maloobchodní entity</span><span class="sxs-lookup"><span data-stu-id="d27e3-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d27e3-104">Maloobchodní prodejci považují vyhledání produktu za primární nástrojem pro interakci se zákazníkem ve všech kanálech.</span><span class="sxs-lookup"><span data-stu-id="d27e3-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="d27e3-105">Různé funkce mohou zákazníkům pomoci snadno objevit produkty.</span><span class="sxs-lookup"><span data-stu-id="d27e3-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="d27e3-106">Mohou například procházet kategorie, vyhledávat a filtrovat.</span><span class="sxs-lookup"><span data-stu-id="d27e3-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="d27e3-107">Toto téma vysvětluje koncepty, které se vztahují k řízení pořadí zobrazení pro různé entity související s podporou prodeje.</span><span class="sxs-lookup"><span data-stu-id="d27e3-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="d27e3-108">Dále je zde vysvětleno, jak změnit pořadí řazení.</span><span class="sxs-lookup"><span data-stu-id="d27e3-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="d27e3-109">Přehled</span><span class="sxs-lookup"><span data-stu-id="d27e3-109">Overview</span></span>

<span data-ttu-id="d27e3-110">Podpora třídění různých entit souvisejících s podporou prodeje byla vylepšena.</span><span class="sxs-lookup"><span data-stu-id="d27e3-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="d27e3-111">Tato podpora je nyní lépe sladěna se stávajícími scénáři odběratele, které dříve vyžadovaly rozšíření od implementačních partnerů.</span><span class="sxs-lookup"><span data-stu-id="d27e3-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="d27e3-112">Ve verzích Retail starších než 10.0.5 bylo pořadí řazení kategorií v navigační hierarchii abecední.</span><span class="sxs-lookup"><span data-stu-id="d27e3-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="d27e3-113">Nová funkce vlastního pořadí řazení umožňuje manažerům podpory prodeje konfigurovat pořadí řazení pro různé entity související s podporou prodeje napříč všemi klienty koncových uživatelů.</span><span class="sxs-lookup"><span data-stu-id="d27e3-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="d27e3-114">Mezi tyto klienty patří centrála (HQ) a kontaktní střediska.</span><span class="sxs-lookup"><span data-stu-id="d27e3-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="d27e3-115">Konfigurace pořadí zobrazení pro kategorie v hierarchii produktů</span><span class="sxs-lookup"><span data-stu-id="d27e3-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="d27e3-116">Před provedením tohoto postupu je nutné, aby byla v prostředí nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="d27e3-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="d27e3-117">Přejděte na **Retail and Commerce \> Produkty a kategorie \> Hierarchie produktů Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="d27e3-118">Klikněte na možnost **Upravit hierarchii kategorií**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="d27e3-119">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-119">Click **Edit**.</span></span>
4. <span data-ttu-id="d27e3-120">Ve stromovém zobrazení rozbalte **VŠE \> Akční sporty**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="d27e3-121">Ve stromovém zobrazení rozbalte **VŠE \> Týmové sporty**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="d27e3-122">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="d27e3-123">(Číslo může být záporné.)</span><span class="sxs-lookup"><span data-stu-id="d27e3-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="d27e3-124">Zopakujte kroky 4 až 6 pro všechny další kategorie, u kterých chcete změnit pořadí.</span><span class="sxs-lookup"><span data-stu-id="d27e3-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="d27e3-125">Pořadí zobrazení hierarchie navigace kanálu se odrazí v centrále pro hierarchii produktů commerce a uvolněné produkty podle kategorie.</span><span class="sxs-lookup"><span data-stu-id="d27e3-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Vlastní řazení hierarchie produktů se zápornými hodnotami](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vlastní řazení uvolněných produktů podle kategorie na základě hierarchie produktů](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="d27e3-128">Konfigurace pořadí zobrazení pro kategorie v hierarchii navigace kanálů</span><span class="sxs-lookup"><span data-stu-id="d27e3-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="d27e3-129">Před provedením tohoto postupu je nutné, aby byla v prostředí nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="d27e3-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="d27e3-130">Přejděte na **Retail and Commerce \> Produkty a kategorie \> Navigační kategorie kanálu**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="d27e3-131">V seznamu vyberte hierarchii navigace **Móda**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="d27e3-132">Klikněte na možnost **Upravit hierarchii kategorií**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="d27e3-133">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-133">Click **Edit**.</span></span>
5. <span data-ttu-id="d27e3-134">Ve stromové struktuře vyberte **Móda \> Dámské oděvy \> Dámské boty**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="d27e3-135">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="d27e3-136">Ve stromové struktuře vyberte **Móda \> Dámské oděvy \> Halenky**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="d27e3-137">Obdobně můžete definovat pořadí řazení pro dílčí kategorie.</span><span class="sxs-lookup"><span data-stu-id="d27e3-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="d27e3-138">Ve stromové struktuře vyberte **Móda \> Pánské oděvy \> Košile pro volný čas**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="d27e3-139">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="d27e3-140">Ve stromové struktuře vyberte **Móda \> Pánské oděvy \> Kabáty a bundy**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="d27e3-141">Zadejte číslo do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="d27e3-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="d27e3-142">Zopakujte kroky pro všechny další kategorie, u kterých chcete změnit pořadí.</span><span class="sxs-lookup"><span data-stu-id="d27e3-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="d27e3-143">Pořadí zobrazení hierarchie navigace kanálu se odráží v centrále, katalogu a kanálech.</span><span class="sxs-lookup"><span data-stu-id="d27e3-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Vlastní řazení hierarchie navigace kanálu](./media/ChannelNavCustomSorted.png)

![Vlastní řazení hierarchie navigace katalogu na základě hierarchie navigace kanálu](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS s vlastním řazením kategorií](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="d27e3-147">Ve výchozím nastavení je funkce vlastního řazení vypnutá.</span><span class="sxs-lookup"><span data-stu-id="d27e3-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="d27e3-148">Informace o zapnutí této funkce a dalších funkcí naleznete v tématu [Správa funkcí](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="d27e3-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]