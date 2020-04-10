---
title: Nastavení hierarchie kategorií zásobování
description: Tento postup popisuje vytvoření nových uzlů v hierarchii kategorií zásobování a konfiguraci kategorie zásobování pro použití v procesu zásobování.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7010fb702d16dc276bfee397066ccf95bf5d25a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147266"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="e4b4e-103">Nastavení hierarchie kategorií zásobování</span><span class="sxs-lookup"><span data-stu-id="e4b4e-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4b4e-104">Tento postup popisuje vytvoření nových uzlů v hierarchii kategorií zásobování a konfiguraci kategorie zásobování pro použití v procesu zásobování.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="e4b4e-105">Tyto úkoly obvykle provádějí vedoucí nákupu.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="e4b4e-106">Před zahájením tohoto postupu musí existovat hierarchie kategorií typu Zásobování.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="e4b4e-107">Používáte-li ukázková data společnosti, můžete tento postup provést se společností USMF.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="e4b4e-108">Přidání nové kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="e4b4e-108">Add a new procurement category</span></span>
1. <span data-ttu-id="e4b4e-109">Přejděte na **navigační podokno > Moduly > Zásobování a zdroje > Zásilka > Kategorie zásobování**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="e4b4e-110">V podokně akcí vyberte možnost **Upravit hierarchii kategorií**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="e4b4e-111">Aktuální hierarchie kategorií zásobování se zobrazí v levé části stránky.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="e4b4e-112">Chystáte se upravit hierarchii.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="e4b4e-113">V podokně akcí vyberte možnost **Nový uzel kategorií**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="e4b4e-114">Systém vybere ve výchozím nastavení nejvyšší uzel.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-114">The system selects the top node by default.</span></span> <span data-ttu-id="e4b4e-115">Používáte-li tento postup jako úkol průvodce, lze kliknout na tlačítko Odemknout a vybrat jiný nadřazený uzel pro vložení nového uzlu.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="e4b4e-116">Po skončení znovu zamkněte průvodce úkolem a pak klikněte na uzel Nová kategorie.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="e4b4e-117">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="e4b4e-118">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="e4b4e-119">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="e4b4e-120">Popisný název je volitelný.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-120">The friendly name is optional.</span></span> <span data-ttu-id="e4b4e-121">Zobrazí se ve vyhledávání kategorií společně s názvem kategorie.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="e4b4e-122">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="e4b4e-123">Přidání produktů do nové kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="e4b4e-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="e4b4e-124">Přejděte do nabídky **Zásobování a zdroje > Zásilka > Kategorie zásobování**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="e4b4e-125">Vyberte uzel, který jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-125">Select the node you just added.</span></span> <span data-ttu-id="e4b4e-126">Pokud tento postup používáte jako průvodce úkolem, možná bude třeba průvodce odemknout, aby bylo možné uzel vybrat.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="e4b4e-127">Rozbalte oddíl **Produkty**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="e4b4e-128">Kliknutím na tlačítko **Přidat** přidružte produkty ke kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="e4b4e-129">Vyberte produkty, které chcete přidat do kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="e4b4e-130">Výběrem šipky přidáte produkty do tabulky **Vybrané**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="e4b4e-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4b4e-131">Select **OK**.</span></span>
