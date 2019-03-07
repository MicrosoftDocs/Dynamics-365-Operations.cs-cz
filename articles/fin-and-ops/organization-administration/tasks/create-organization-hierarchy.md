---
title: Vytvoření organizační hierarchie
description: Následující postup použijte k vytvoření organizační hierarchie.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 203a586b06a13a7c67f246384152d17627e22041
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "308798"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="51871-103">Vytvoření organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="51871-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51871-104">Následující postup použijte k vytvoření organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="51871-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="51871-105">Organizační hierarchii můžete použít k zobrazení a tvorbě sestav vašeho podnikání z různých perspektiv.</span><span class="sxs-lookup"><span data-stu-id="51871-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="51871-106">Můžete například nastavit jednu hierarchii pro daňové, právní nebo statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="51871-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="51871-107">Potom můžete nastavit jinou hierarchii pro finanční informace sestavy, které nejsou vyžadovány zákonem, ale které se používají pro interní výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="51871-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="51871-108">Dříve než vytvoříte organizační hierarchií, musíte vytvořit organizace.</span><span class="sxs-lookup"><span data-stu-id="51871-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="51871-109">Další informace naleznete v úloze "Vytvoření právnické osoby" nebo "Vytvoření provozní jednotky".</span><span class="sxs-lookup"><span data-stu-id="51871-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="51871-110">Můžete také vytvořit oddělení nebo týmy.</span><span class="sxs-lookup"><span data-stu-id="51871-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="51871-111">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="51871-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="51871-112">Vytvořit hierarchii</span><span class="sxs-lookup"><span data-stu-id="51871-112">Create a hierarchy</span></span>
1. <span data-ttu-id="51871-113">Přejděte do nabídky Správa organizace > Organizace > Organization hierarchies.</span><span class="sxs-lookup"><span data-stu-id="51871-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="51871-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="51871-114">Click New.</span></span>
3. <span data-ttu-id="51871-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="51871-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="51871-116">Klikněte na Přiřadit účel.</span><span class="sxs-lookup"><span data-stu-id="51871-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="51871-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="51871-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="51871-118">Vyberte účel, který chcete přiřadit k hierarchii organizace.</span><span class="sxs-lookup"><span data-stu-id="51871-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="51871-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="51871-119">Click Add.</span></span>
7. <span data-ttu-id="51871-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="51871-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="51871-121">Vyhledejte hierarchii, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="51871-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="51871-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="51871-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="51871-123">Přidání organizací do hierarchie</span><span class="sxs-lookup"><span data-stu-id="51871-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="51871-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="51871-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="51871-125">Vyberte svoji hierarchii.</span><span class="sxs-lookup"><span data-stu-id="51871-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="51871-126">Klikněte na Zobrazit hierarchii.</span><span class="sxs-lookup"><span data-stu-id="51871-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="51871-127">Podle potřeby přidejte organizace.</span><span class="sxs-lookup"><span data-stu-id="51871-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="51871-128">Pokud chcete přidat organizaci, klepněte na tlačítko Upravit a Vložit a přidejte tak organizaci.</span><span class="sxs-lookup"><span data-stu-id="51871-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="51871-129">Po dokončení provádění změn můžete uložit návrh a publikovat změny.</span><span class="sxs-lookup"><span data-stu-id="51871-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  

