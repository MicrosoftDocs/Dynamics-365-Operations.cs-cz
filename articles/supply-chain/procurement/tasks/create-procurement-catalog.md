--- 
title: "Vytvoření zásobovacího katalogu"
description: "Tento postup popisuje způsob vytváření zásobovacího katalogu."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="48905-103">Vytvoření zásobovacího katalogu</span><span class="sxs-lookup"><span data-stu-id="48905-103">Create a procurement catalog</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48905-104">Tento postup popisuje způsob vytváření zásobovacího katalogu.</span><span class="sxs-lookup"><span data-stu-id="48905-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="48905-105">Tento úkol by obvykle prováděl zásobovací pracovník.</span><span class="sxs-lookup"><span data-stu-id="48905-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="48905-106">Zjistíte také, jak mohou zaměstnanci používat katalog při vytváření požadavku.</span><span class="sxs-lookup"><span data-stu-id="48905-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="48905-107">Před vytvořením katalogu musí existovat ve vašem systému hierarchie kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="48905-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="48905-108">Hierarchii zdědí nový katalog spolu se všemi produkty, které jsou v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="48905-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="48905-109">Tento postup lze použít u ukázkových dat společnosti USMF, kde je k dispozici hierarchie kategorie zásobování společně s příklady použitými v krocích postupu.</span><span class="sxs-lookup"><span data-stu-id="48905-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="48905-110">Ujistěte se, že existuje hierarchie kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="48905-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="48905-111">Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="48905-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="48905-112">U společnosti s demonstračními daty USMF je k dispozici hierarchie kategorie zásobování a produkty byly přidány do kategorie Kancelářské počítače.</span><span class="sxs-lookup"><span data-stu-id="48905-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="48905-113">Pokud tento postup používáte jako průvodce úkolem, možná bude třeba průvodce odemknout, aby bylo možné kategorii procházet.</span><span class="sxs-lookup"><span data-stu-id="48905-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="48905-114">Pokud hierarchii není k dispozici, vytvoříte ji klepnutím na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="48905-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="48905-115">To je možné pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="48905-115">This can only be done once.</span></span>  
2. <span data-ttu-id="48905-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="48905-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="48905-117">Vytvoření katalogu</span><span class="sxs-lookup"><span data-stu-id="48905-117">Create a catalog</span></span>
1. <span data-ttu-id="48905-118">Přejděte do nabídky Zásobování a zdroje > Katalogy > Katalogy zásobování.</span><span class="sxs-lookup"><span data-stu-id="48905-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="48905-119">Kliknutím na možnost Nový zásobovací katalog otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="48905-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="48905-120">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="48905-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="48905-121">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="48905-121">Click OK.</span></span>
5. <span data-ttu-id="48905-122">Ve stromovém zobrazení rozbalte KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI.</span><span class="sxs-lookup"><span data-stu-id="48905-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="48905-123">Ve stromu rozbalte KANCELÁŘSKÉ POČÍTAČE.</span><span class="sxs-lookup"><span data-stu-id="48905-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="48905-124">Ve stromu vyberte Počítače.</span><span class="sxs-lookup"><span data-stu-id="48905-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="48905-125">V seznamu jsou zobrazeny produkty z kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="48905-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="48905-126">Pokud chcete přidat produkt do kategorie, je nutné to provést na stránce Hierarchie kategorií zásobování nebo Podrobnosti o zboží.</span><span class="sxs-lookup"><span data-stu-id="48905-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="48905-127">Výchozí typ aktualizace určuje, zda jsou nové produkty přidané do hierarchie kategorie zásobování okamžitě viditelné v katalogu.</span><span class="sxs-lookup"><span data-stu-id="48905-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="48905-128">Pokud je typ aktualizace nastaven na Dynamický, změny se projeví okamžitě.</span><span class="sxs-lookup"><span data-stu-id="48905-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="48905-129">Pokud je typem aktualizace Statický, nové produkty jsou viditelné pouze uživatelům, kteří používají katalog po jeho opětovném publikování.</span><span class="sxs-lookup"><span data-stu-id="48905-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="48905-130">Akce Publikovat je k dispozici v podokně Akce v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="48905-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="48905-131">Pokud jsou produkty odebrány z hierarchie kategorie zásobování, změny se projeví okamžitě bez ohledu na hodnotu v poli Výchozí typ aktualizace.</span><span class="sxs-lookup"><span data-stu-id="48905-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="48905-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="48905-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="48905-133">Klikněte na Skrýt.</span><span class="sxs-lookup"><span data-stu-id="48905-133">Click Hide.</span></span>
10. <span data-ttu-id="48905-134">V podokně akcí klikněte na možnost Navigace v kategorii.</span><span class="sxs-lookup"><span data-stu-id="48905-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="48905-135">Klikněte na Zakázat.</span><span class="sxs-lookup"><span data-stu-id="48905-135">Click Disable.</span></span>
12. <span data-ttu-id="48905-136">V podokně akcí klikněte na možnost Navigace v kategorii.</span><span class="sxs-lookup"><span data-stu-id="48905-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="48905-137">Klikněte na tlačítko Povolit.</span><span class="sxs-lookup"><span data-stu-id="48905-137">Click Enable.</span></span>
14. <span data-ttu-id="48905-138">Klikněte na Aktivovat katalog.</span><span class="sxs-lookup"><span data-stu-id="48905-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="48905-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="48905-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="48905-140">Zviditelnění katalogu</span><span class="sxs-lookup"><span data-stu-id="48905-140">Make the catalog visible</span></span>
1. <span data-ttu-id="48905-141">Přejděte na Zásobování a zdroje > Nastavení > Zásady > Zásady nákupu.</span><span class="sxs-lookup"><span data-stu-id="48905-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="48905-142">Vyberte USMF – zásady zásobování.</span><span class="sxs-lookup"><span data-stu-id="48905-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="48905-143">Je třeba vybrat zásady nákupu pro právnickou osobu, u které je pracovník propojený s profilem uživatele oprávněn objednávat produkty.</span><span class="sxs-lookup"><span data-stu-id="48905-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="48905-144">V rámci ukázkových dat USMF je Administrátor je propojen s pracovníkem se jménem Julia Funderburk, která standardně objednává produkty v USMF.</span><span class="sxs-lookup"><span data-stu-id="48905-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="48905-145">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="48905-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="48905-146">Výběr katalog, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="48905-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="48905-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="48905-147">Click OK.</span></span>
6. <span data-ttu-id="48905-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="48905-148">Close the page.</span></span>
7. <span data-ttu-id="48905-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="48905-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="48905-150">Použití katalogu</span><span class="sxs-lookup"><span data-stu-id="48905-150">Use the catalog</span></span>
1. <span data-ttu-id="48905-151">Přejděte do nabídky Zásobování a zdroje > Nákupní žádanky > Všechny nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="48905-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="48905-152">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="48905-152">Click New.</span></span>
3. <span data-ttu-id="48905-153">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="48905-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="48905-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="48905-154">Click OK.</span></span>
5. <span data-ttu-id="48905-155">Klikněte na možnost Přidat produkty.</span><span class="sxs-lookup"><span data-stu-id="48905-155">Click Add products.</span></span>
6. <span data-ttu-id="48905-156">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="48905-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48905-157">Pro filtrování produktů můžete použít hierarchii kategorií vlevo nebo filtr v horní části seznamu.</span><span class="sxs-lookup"><span data-stu-id="48905-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="48905-158">Klikněte na možnost Přidat na řádky.</span><span class="sxs-lookup"><span data-stu-id="48905-158">Click Add to lines.</span></span>
8. <span data-ttu-id="48905-159">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="48905-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="48905-160">Klikněte na možnost Přidat na řádky.</span><span class="sxs-lookup"><span data-stu-id="48905-160">Click Add to lines.</span></span>
10. <span data-ttu-id="48905-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="48905-161">Click OK.</span></span>


