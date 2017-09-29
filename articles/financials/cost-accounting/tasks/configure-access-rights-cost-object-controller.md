--- 
title: "Konfigurace přístupových práv pro kontrolora objektu nákladů"
description: "Pomocí tohoto postupu proveďte konfiguraci přístupových práv pro kontroloru objektu nákladů."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b0647e1ec55d23607d07f38105e42af498ad1174
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="d978a-103">Konfigurace přístupových práv pro kontrolora objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="d978a-103">Configure access rights for a cost object controller</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d978a-104">Pomocí tohoto postupu proveďte konfiguraci přístupových práv pro kontroloru objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d978a-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="d978a-105">Tento záznam používá v ukázkových datech společnost USP2.</span><span class="sxs-lookup"><span data-stu-id="d978a-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="d978a-106">Přiřazení role kontrolora objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="d978a-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="d978a-107">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="d978a-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="d978a-108">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="d978a-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d978a-109">Můžete například filtrovat v poli Uživatelské jméno pomocí hodnoty „alicia“.</span><span class="sxs-lookup"><span data-stu-id="d978a-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="d978a-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d978a-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d978a-111">Klikněte na možnost Přiřadit role.</span><span class="sxs-lookup"><span data-stu-id="d978a-111">Click Assign roles.</span></span>
5. <span data-ttu-id="d978a-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d978a-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d978a-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d978a-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="d978a-114">Povolení zabezpečení přístupového seznamu</span><span class="sxs-lookup"><span data-stu-id="d978a-114">Enable access list security</span></span>
1. <span data-ttu-id="d978a-115">Přejděte na Nákladové účetnictví > Dimenze > Hierarchie dimenzí.</span><span class="sxs-lookup"><span data-stu-id="d978a-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="d978a-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d978a-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d978a-117">Vyberte organizaci.</span><span class="sxs-lookup"><span data-stu-id="d978a-117">Select Organization.</span></span>  
3. <span data-ttu-id="d978a-118">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="d978a-118">Click Edit.</span></span>
4. <span data-ttu-id="d978a-119">V poli Hierarchie přístupového seznamu vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="d978a-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="d978a-120">Klikněte na Zobrazit hierarchii.</span><span class="sxs-lookup"><span data-stu-id="d978a-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="d978a-121">Přiřazení přístupových práv uživateli</span><span class="sxs-lookup"><span data-stu-id="d978a-121">Assign access rights to user</span></span>
1. <span data-ttu-id="d978a-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d978a-122">Click New.</span></span>
2. <span data-ttu-id="d978a-123">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d978a-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="d978a-124">V poli ID uživatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d978a-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="d978a-125">Vyberte správce.</span><span class="sxs-lookup"><span data-stu-id="d978a-125">Select Admin.</span></span>  
4. <span data-ttu-id="d978a-126">Ve stromovém zobrazení vyberte 'Organization\CEO\CFO\FIM'.</span><span class="sxs-lookup"><span data-stu-id="d978a-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="d978a-127">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d978a-127">Click New.</span></span>
6. <span data-ttu-id="d978a-128">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d978a-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="d978a-129">V poli ID uživatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d978a-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="d978a-130">Vyberte Alicia.</span><span class="sxs-lookup"><span data-stu-id="d978a-130">Select Alicia.</span></span>  
8. <span data-ttu-id="d978a-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d978a-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="d978a-132">Povolení přístupových práv v nákladovém účetnictví</span><span class="sxs-lookup"><span data-stu-id="d978a-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="d978a-133">Přejděte na Nákladové účetnictví > Nastavení > Parametry.</span><span class="sxs-lookup"><span data-stu-id="d978a-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="d978a-134">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="d978a-134">Click the General tab.</span></span>
3. <span data-ttu-id="d978a-135">Zvolte parametr Ano v poli Povolit přístup k zobrazení pro členy dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d978a-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="d978a-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d978a-136">Click Save.</span></span>
5. <span data-ttu-id="d978a-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d978a-137">Close the page.</span></span>
6. <span data-ttu-id="d978a-138">Přejděte na Nákladové účetnictví > Nastavení > Konfigurace pracovního prostoru pro řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="d978a-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="d978a-139">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="d978a-139">Click Edit.</span></span>
8. <span data-ttu-id="d978a-140">Vyberte možnost Ano v poli Publikováno.</span><span class="sxs-lookup"><span data-stu-id="d978a-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="d978a-141">Pokud vyberete Ano, uživatel s přiřazenou některou z následujících čtyř rolí si může zobrazit sestavy v pracovním prostoru řízení nákladů: manažer nákladového účetnictví, nákladový účetní, úředník na pozici nákladového účetního nebo kontrolor objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d978a-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="d978a-142">Pokud vyberete Ne, pouze uživatel s přiřazenou některou z následujících rolí si může zobrazit sestavy: manažer nákladového účetnictví, nákladový účetní a úředník na pozici nákladového účetního.</span><span class="sxs-lookup"><span data-stu-id="d978a-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="d978a-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d978a-143">Click Save.</span></span>


