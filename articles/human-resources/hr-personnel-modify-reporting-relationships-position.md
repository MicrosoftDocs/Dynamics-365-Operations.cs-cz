---
title: Úprava vztahů podřízenosti pro určitou pozici
description: Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3285222b11905999f0eadb846ac785342c16aa38
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008384"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="e531f-103">Úprava vztahů podřízenosti pro určitou pozici</span><span class="sxs-lookup"><span data-stu-id="e531f-103">Modify reporting relationships for a position</span></span>



<span data-ttu-id="e531f-104">Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="e531f-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="e531f-105">Vztah sestav lze použít pro směrování dokumentů prostřednictvím workflowu.</span><span class="sxs-lookup"><span data-stu-id="e531f-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="e531f-106">Procedura také ukazuje postup přiřazení zaměstnance k dalším hierarchiím.</span><span class="sxs-lookup"><span data-stu-id="e531f-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="e531f-107">Například zaměstnanec může být součástí projektového týmu s neformálním vykazováním vztahů k vedoucímu projektu.</span><span class="sxs-lookup"><span data-stu-id="e531f-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="e531f-108">Další vztahy vykazování lze definovat na pozici pro různé scénáře projektu nebo matice.</span><span class="sxs-lookup"><span data-stu-id="e531f-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="e531f-109">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e531f-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e531f-110">Přejděte k nabídce Lidské zdroje > Pozice > Pozice.</span><span class="sxs-lookup"><span data-stu-id="e531f-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="e531f-111">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="e531f-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e531f-112">Můžete například filtrovat v poli Pozice pomocí hodnoty „000091“.</span><span class="sxs-lookup"><span data-stu-id="e531f-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="e531f-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e531f-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e531f-114">Rozbalte pole Sestavy pro umístění oddílu.</span><span class="sxs-lookup"><span data-stu-id="e531f-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="e531f-115">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e531f-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="e531f-116">V poli Nadřízená pozice zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e531f-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="e531f-117">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="e531f-117">Click Create.</span></span>
8. <span data-ttu-id="e531f-118">Rozbalte nebo sbalte oddíl Vztahy.</span><span class="sxs-lookup"><span data-stu-id="e531f-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="e531f-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e531f-119">Click Add.</span></span>
10. <span data-ttu-id="e531f-120">Zaškrtněte políčko po levé straně mřížky.</span><span class="sxs-lookup"><span data-stu-id="e531f-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="e531f-121">V poli Název hierarchie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e531f-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="e531f-122">Příklad: Projekt</span><span class="sxs-lookup"><span data-stu-id="e531f-122">Example: Project</span></span>  
12. <span data-ttu-id="e531f-123">V poli Nadřízená pozice zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e531f-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="e531f-124">Příklad: 000437</span><span class="sxs-lookup"><span data-stu-id="e531f-124">Example:  000437</span></span>
13. <span data-ttu-id="e531f-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e531f-125">Click Save.</span></span>

