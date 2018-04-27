--- 
title: "Úprava vztahů podřízenosti pro určitou pozici"
description: "Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4d8c82998e6b19adbd67b6b5ea3d68d2fbd08d8b
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="02a17-103">Úprava vztahů podřízenosti pro určitou pozici</span><span class="sxs-lookup"><span data-stu-id="02a17-103">Modify reporting relationships for a position</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02a17-104">Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="02a17-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="02a17-105">Vztah sestav lze použít pro směrování dokumentů prostřednictvím workflowu.</span><span class="sxs-lookup"><span data-stu-id="02a17-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="02a17-106">Procedura také ukazuje postup přiřazení zaměstnance k dalším hierarchiím.</span><span class="sxs-lookup"><span data-stu-id="02a17-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="02a17-107">Například zaměstnanec může být součástí projektového týmu s neformálním vykazováním vztahů k vedoucímu projektu.</span><span class="sxs-lookup"><span data-stu-id="02a17-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="02a17-108">Další vztahy vykazování lze definovat na pozici pro různé scénáře projektu nebo matice.</span><span class="sxs-lookup"><span data-stu-id="02a17-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="02a17-109">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="02a17-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="02a17-110">Přejděte k nabídce Lidské zdroje > Pozice > Pozice.</span><span class="sxs-lookup"><span data-stu-id="02a17-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="02a17-111">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="02a17-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="02a17-112">Můžete například filtrovat v poli Pozice pomocí hodnoty „000091“.</span><span class="sxs-lookup"><span data-stu-id="02a17-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="02a17-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="02a17-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="02a17-114">Rozbalte pole Sestavy pro umístění oddílu.</span><span class="sxs-lookup"><span data-stu-id="02a17-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="02a17-115">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="02a17-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="02a17-116">V poli Nadřízená pozice zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02a17-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="02a17-117">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="02a17-117">Click Create.</span></span>
8. <span data-ttu-id="02a17-118">Rozbalte nebo sbalte oddíl Vztahy.</span><span class="sxs-lookup"><span data-stu-id="02a17-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="02a17-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="02a17-119">Click Add.</span></span>
10. <span data-ttu-id="02a17-120">Zaškrtněte políčko po levé straně mřížky.</span><span class="sxs-lookup"><span data-stu-id="02a17-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="02a17-121">V poli Název hierarchie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02a17-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="02a17-122">Příklad: Projekt</span><span class="sxs-lookup"><span data-stu-id="02a17-122">Example: Project</span></span>  
12. <span data-ttu-id="02a17-123">V poli Nadřízená pozice zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02a17-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="02a17-124">Příklad: 000437</span><span class="sxs-lookup"><span data-stu-id="02a17-124">Example:  000437</span></span>
13. <span data-ttu-id="02a17-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="02a17-125">Click Save.</span></span>


