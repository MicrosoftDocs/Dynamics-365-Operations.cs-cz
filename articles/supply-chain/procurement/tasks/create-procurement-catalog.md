---
title: Vytvoření zásobovacího katalogu
description: Toto téma vysvětluje postup při vytváření zásobovacího katalogu.
author: RichardLuan
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaf8b8d8b369aa704344d6984a0f111af6e4285b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016470"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="73a1f-103">Vytvoření zásobovacího katalogu</span><span class="sxs-lookup"><span data-stu-id="73a1f-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73a1f-104">Toto téma vysvětluje postup při vytváření zásobovacího katalogu.</span><span class="sxs-lookup"><span data-stu-id="73a1f-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="73a1f-105">Tento úkol by obvykle prováděl zásobovací pracovník.</span><span class="sxs-lookup"><span data-stu-id="73a1f-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="73a1f-106">Zjistíte také, jak mohou zaměstnanci používat katalog při vytváření požadavku.</span><span class="sxs-lookup"><span data-stu-id="73a1f-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="73a1f-107">Před vytvořením katalogu musí existovat ve vašem systému hierarchie kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="73a1f-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="73a1f-108">Hierarchii zdědí nový katalog spolu se všemi produkty, které jsou v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="73a1f-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="73a1f-109">Tento postup lze použít u ukázkových dat společnosti USMF, kde je k dispozici hierarchie kategorie zásobování společně s příklady použitými v krocích postupu.</span><span class="sxs-lookup"><span data-stu-id="73a1f-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="73a1f-110">Ujistěte se, že existuje hierarchie kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="73a1f-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="73a1f-111">Přejděte na **navigační podokno > Moduly > Zásobování a zdroje > Kategorie zásobování**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="73a1f-112">U společnosti s demonstračními daty USMF je k dispozici hierarchie kategorie zásobování a produkty byly přidány do kategorie **Kancelářské počítače**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="73a1f-113">Pokud tento postup používáte jako průvodce úkolem, možná bude třeba průvodce odemknout, aby bylo možné kategorii procházet.</span><span class="sxs-lookup"><span data-stu-id="73a1f-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="73a1f-114">Pokud hierarchii není k dispozici, vytvoříte ji klepnutím na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="73a1f-115">To je možné pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="73a1f-115">This can only be done once.</span></span>  
2. <span data-ttu-id="73a1f-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="73a1f-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="73a1f-117">Vytvoření katalogu</span><span class="sxs-lookup"><span data-stu-id="73a1f-117">Create a catalog</span></span>
1. <span data-ttu-id="73a1f-118">Přejděte na **navigační podokno > Moduly > Zásobování a zdroje > > Katalogy > Katalogy zásobování**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="73a1f-119">Výběrem možnosti **Nový zásobovací katalog** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="73a1f-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="73a1f-120">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="73a1f-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-121">Select **OK**.</span></span>
5. <span data-ttu-id="73a1f-122">Ve stromovém zobrazení rozbalte **KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="73a1f-123">Ve stromu rozbalte **KANCELÁŘSKÉ POČÍTAČE**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="73a1f-124">Ve stromu vyberte **Počítače**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="73a1f-125">V seznamu jsou zobrazeny produkty z kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="73a1f-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="73a1f-126">Pokud chcete přidat produkt do kategorie, je nutné to provést na stránce **Hierarchie kategorií zásobování** nebo **Podrobnosti o zboží**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="73a1f-127">**Výchozí** typ aktualizace určuje, zda jsou nové produkty přidané do hierarchie kategorie zásobování okamžitě viditelné v katalogu.</span><span class="sxs-lookup"><span data-stu-id="73a1f-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="73a1f-128">Pokud je typ aktualizace nastaven na **Dynamický**, změny se projeví okamžitě.</span><span class="sxs-lookup"><span data-stu-id="73a1f-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="73a1f-129">Pokud je typem aktualizace **Statický**, nové produkty jsou viditelné pouze uživatelům, kteří používají katalog po jeho opětovném publikování.</span><span class="sxs-lookup"><span data-stu-id="73a1f-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="73a1f-130">Akce **Publikovat** je k dispozici v podokně Akce v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="73a1f-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="73a1f-131">Pokud jsou produkty odebrány z hierarchie kategorie zásobování, změny se projeví okamžitě bez ohledu na hodnotu v poli **Výchozí** typ aktualizace.</span><span class="sxs-lookup"><span data-stu-id="73a1f-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="73a1f-132">V podokně akcí vyberte **Navigace v kategorii** a ujistěte se, že je vybrána možnost **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="73a1f-133">Vyberte **Aktivovat katalog**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="73a1f-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="73a1f-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="73a1f-135">Zviditelnění katalogu</span><span class="sxs-lookup"><span data-stu-id="73a1f-135">Make the catalog visible</span></span>
1. <span data-ttu-id="73a1f-136">Přejděte na **navigační podokno > Moduly > Zásobování a nákup > Nastavení > Zásady > Zásady nákupu**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="73a1f-137">Vyberte **USMF – zásady zásobování**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="73a1f-138">Je třeba vybrat zásady nákupu pro právnickou osobu, u které je pracovník propojený s profilem uživatele oprávněn objednávat produkty.</span><span class="sxs-lookup"><span data-stu-id="73a1f-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="73a1f-139">V rámci ukázkových dat USMF je Administrátor je propojen s pracovníkem se jménem **Julia Funderburk**, která standardně objednává produkty v USMF.</span><span class="sxs-lookup"><span data-stu-id="73a1f-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="73a1f-140">Výběr katalog, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="73a1f-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="73a1f-141">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="73a1f-142">Použití katalogu</span><span class="sxs-lookup"><span data-stu-id="73a1f-142">Use the catalog</span></span>
1. <span data-ttu-id="73a1f-143">Přejděte na **navigační podokno > Moduly > Zásobování a zdroje > Nákupní žádanky > Všechny nákupní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="73a1f-144">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-144">Select **New**.</span></span>
3. <span data-ttu-id="73a1f-145">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="73a1f-146">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-146">Select **OK**.</span></span>
5. <span data-ttu-id="73a1f-147">Vyberte **Přidat produkty**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-147">Select **Add products**.</span></span>
6. <span data-ttu-id="73a1f-148">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="73a1f-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="73a1f-149">Pro filtrování produktů můžete použít hierarchii kategorií vlevo nebo filtr v horní části seznamu.</span><span class="sxs-lookup"><span data-stu-id="73a1f-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="73a1f-150">Vyberte **Přidat na řádky**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="73a1f-151">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="73a1f-151">Select **OK**.</span></span>

