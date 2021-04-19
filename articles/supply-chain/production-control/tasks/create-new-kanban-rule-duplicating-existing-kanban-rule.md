---
title: Vytvoření nového kanbanového pravidla duplikováním existujícího kanbanového pravidla
description: Tento postup se zaměřuje na vytváření kopií existujícího kanbanového pravidla.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d80bf0318234f858e51fb461894238894e01717c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829059"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="d7849-103">Vytvoření nového kanbanového pravidla duplikováním existujícího kanbanového pravidla</span><span class="sxs-lookup"><span data-stu-id="d7849-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7849-104">Tento postup se zaměřuje na vytváření kopií existujícího kanbanového pravidla.</span><span class="sxs-lookup"><span data-stu-id="d7849-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="d7849-105">To je užitečné, pokud chcete vytvořit nová kanbanová pravidla, která jsou založena na existujících kanbanových pravidlech.</span><span class="sxs-lookup"><span data-stu-id="d7849-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="d7849-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d7849-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d7849-107">Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu změněného výrobního toku nebo nového pravidla doplnění.</span><span class="sxs-lookup"><span data-stu-id="d7849-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="d7849-108">Vyberte kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="d7849-108">Select a kanban rule</span></span>
1. <span data-ttu-id="d7849-109">Otevřete Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="d7849-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="d7849-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d7849-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d7849-111">Vyberte kanbanové pravidlo 000017 produktu M0006.</span><span class="sxs-lookup"><span data-stu-id="d7849-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="d7849-112">Duplikujte kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="d7849-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="d7849-113">Klepněte na Duplicitní kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="d7849-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="d7849-114">Při duplikování kanbanového pravidla je možné změnit typ, data, aktivity a výběr produktu.</span><span class="sxs-lookup"><span data-stu-id="d7849-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="d7849-115">Změňte produkt pro tuto proceduru v dalším kroku.</span><span class="sxs-lookup"><span data-stu-id="d7849-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="d7849-116">V poli Produkt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d7849-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="d7849-117">Vyberte volbu „M0007“.</span><span class="sxs-lookup"><span data-stu-id="d7849-117">Select M0007.</span></span>  
3. <span data-ttu-id="d7849-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d7849-118">Click OK.</span></span>
    * <span data-ttu-id="d7849-119">Všimněte si, že je vytvořeno duplicitní kanbanové pravidlo 000017.</span><span class="sxs-lookup"><span data-stu-id="d7849-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]