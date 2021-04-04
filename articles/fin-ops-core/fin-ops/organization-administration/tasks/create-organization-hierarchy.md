---
title: Vytvoření organizační hierarchie
description: Následující postup použijte k vytvoření organizační hierarchie.
author: sericks007
manager: AnnBe
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d61d6eee3b55087d633a8416fbed3a6192e82b2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560572"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="31c13-103">Vytvoření organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="31c13-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31c13-104">Následující postup použijte k vytvoření organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="31c13-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="31c13-105">Organizační hierarchii můžete použít k zobrazení a tvorbě sestav vašeho podnikání z různých perspektiv.</span><span class="sxs-lookup"><span data-stu-id="31c13-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="31c13-106">Můžete například nastavit jednu hierarchii pro daňové, právní nebo statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="31c13-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="31c13-107">Potom můžete nastavit jinou hierarchii pro finanční informace sestavy, které nejsou vyžadovány zákonem, ale které se používají pro interní výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="31c13-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="31c13-108">Dříve než vytvoříte organizační hierarchií, musíte vytvořit organizace.</span><span class="sxs-lookup"><span data-stu-id="31c13-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="31c13-109">Další informace naleznete v úloze "Vytvoření právnické osoby" nebo "Vytvoření provozní jednotky".</span><span class="sxs-lookup"><span data-stu-id="31c13-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="31c13-110">Můžete také vytvořit oddělení nebo týmy.</span><span class="sxs-lookup"><span data-stu-id="31c13-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="31c13-111">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="31c13-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="31c13-112">Vytvořit hierarchii</span><span class="sxs-lookup"><span data-stu-id="31c13-112">Create a hierarchy</span></span>
1. <span data-ttu-id="31c13-113">Přejděte na **Navigační podokno > Moduly > Správa organizace > Organizace > Organizační hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="31c13-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="31c13-114">V **podokně akcí** klikněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="31c13-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="31c13-115">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="31c13-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="31c13-116">V sekci **Účel** klikněte na **Přiřadit účel**.</span><span class="sxs-lookup"><span data-stu-id="31c13-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="31c13-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="31c13-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="31c13-118">Vyberte účel, který chcete přiřadit k hierarchii organizace.</span><span class="sxs-lookup"><span data-stu-id="31c13-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="31c13-119">V části **Přiřazené hierarchie** klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="31c13-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="31c13-120">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="31c13-120">In the list, mark the selected row.</span></span> <span data-ttu-id="31c13-121">Vyhledejte hierarchii, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="31c13-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="31c13-122">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="31c13-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="31c13-123">Přidání organizací do hierarchie</span><span class="sxs-lookup"><span data-stu-id="31c13-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="31c13-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="31c13-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="31c13-125">Vyberte svoji hierarchii.</span><span class="sxs-lookup"><span data-stu-id="31c13-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="31c13-126">V sekci **Přiřazené hierarchie** klikněte na **Zobrazit hierarchii**.</span><span class="sxs-lookup"><span data-stu-id="31c13-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="31c13-127">Podle potřeby přidejte organizace.</span><span class="sxs-lookup"><span data-stu-id="31c13-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="31c13-128">Pokud chcete přidat organizaci, klikněte na tlačítko **Upravit** a pak **Vložit** a přidejte organizaci.</span><span class="sxs-lookup"><span data-stu-id="31c13-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="31c13-129">Po dokončení provádění změn můžete **uložit** návrh a **publikovat** změny.</span><span class="sxs-lookup"><span data-stu-id="31c13-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]