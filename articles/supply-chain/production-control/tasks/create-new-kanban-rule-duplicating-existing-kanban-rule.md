---
title: Vytvoření nového kanbanového pravidla duplikováním existujícího kanbanového pravidla
description: Tento postup se zaměřuje na vytváření kopií existujícího kanbanového pravidla.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f72dbca0debf9e6a03ee700a979d4f4c110f819
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "350336"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="6d454-103">Vytvoření nového kanbanového pravidla duplikováním existujícího kanbanového pravidla</span><span class="sxs-lookup"><span data-stu-id="6d454-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d454-104">Tento postup se zaměřuje na vytváření kopií existujícího kanbanového pravidla.</span><span class="sxs-lookup"><span data-stu-id="6d454-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="6d454-105">To je užitečné, pokud chcete vytvořit nová kanbanová pravidla, která jsou založena na existujících kanbanových pravidlech.</span><span class="sxs-lookup"><span data-stu-id="6d454-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="6d454-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="6d454-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6d454-107">Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu změněného výrobního toku nebo nového pravidla doplnění.</span><span class="sxs-lookup"><span data-stu-id="6d454-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="6d454-108">Vyberte kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="6d454-108">Select a kanban rule</span></span>
1. <span data-ttu-id="6d454-109">Otevřete Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="6d454-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="6d454-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6d454-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6d454-111">Vyberte kanbanové pravidlo 000017 produktu M0006.</span><span class="sxs-lookup"><span data-stu-id="6d454-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="6d454-112">Duplikujte kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="6d454-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="6d454-113">Klepněte na Duplicitní kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="6d454-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="6d454-114">Při duplikování kanbanového pravidla je možné změnit typ, data, aktivity a výběr produktu.</span><span class="sxs-lookup"><span data-stu-id="6d454-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="6d454-115">Změňte produkt pro tuto proceduru v dalším kroku.</span><span class="sxs-lookup"><span data-stu-id="6d454-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="6d454-116">V poli Produkt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6d454-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="6d454-117">Vyberte volbu „M0007“.</span><span class="sxs-lookup"><span data-stu-id="6d454-117">Select M0007.</span></span>  
3. <span data-ttu-id="6d454-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6d454-118">Click OK.</span></span>
    * <span data-ttu-id="6d454-119">Všimněte si, že je vytvořeno duplicitní kanbanové pravidlo 000017.</span><span class="sxs-lookup"><span data-stu-id="6d454-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

