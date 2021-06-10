---
title: Přihlášení zaměstnance k plánu fixní kompenzace
description: Manažer kompenzací a zaměstnaneckých výhod může přiřadit zaměstnance k plánům fixní kompenzace a spravovat tak jejich základní mzdy.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5f0862c86234495c89b2a6ad947cc78e687de37
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054229"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="eb78d-103">Přihlášení zaměstnance k plánu fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="eb78d-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eb78d-104">Manažer kompenzací a zaměstnaneckých výhod může přiřadit zaměstnance k plánům fixní kompenzace a spravovat tak jejich základní mzdy.</span><span class="sxs-lookup"><span data-stu-id="eb78d-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="eb78d-105">Tento postup předpokládá, že fixní plán byl vytvořen a je aktivní, a že byla nastavena pravidla způsobilosti pro daný plán.</span><span class="sxs-lookup"><span data-stu-id="eb78d-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="eb78d-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="eb78d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eb78d-107">Postup zahájíte tak, že přejděte na Lidské zdroje > Pracovníci > Zaměstnanci > Kompenzace > Fixní plán</span><span class="sxs-lookup"><span data-stu-id="eb78d-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="eb78d-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="eb78d-108">Click New.</span></span>
2. <span data-ttu-id="eb78d-109">V poli Akce vyberte u možnosti Akce fixní kompenzace typ Zařadit nebo znovu zařadit a popište změnu v kompenzacích zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="eb78d-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="eb78d-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eb78d-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="eb78d-111">V poli Pozice kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eb78d-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="eb78d-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eb78d-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="eb78d-113">Uvedená úroveň pochází z úrovně kompenzace pro úlohu na dané pozici.</span><span class="sxs-lookup"><span data-stu-id="eb78d-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="eb78d-114">Úroveň musí být nastavena na stav Úloha předtím, než ji bude možné přiřadit zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="eb78d-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="eb78d-115">V poli Plán vyberte plán fixní kompenzace pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="eb78d-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="eb78d-116">Vyhledávání plánu je filtrováno a zobrazí pouze plány, pro které je zaměstnanec způsobilý podle pravidel způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="eb78d-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="eb78d-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eb78d-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb78d-118">Výchozí nastavení pro Datum zahájení platnosti a Datum konce platnosti vychází z počátečního a koncového data pro přiřazení pozice pracovníka.</span><span class="sxs-lookup"><span data-stu-id="eb78d-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="eb78d-119">Tato data lze změnit podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="eb78d-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="eb78d-120">Je-li Plán fixní kompenzace plánem kroku, vyberte krok obsahující správné mzdové sazby pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="eb78d-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="eb78d-121">Je-li Plán fixní kompenzace plánem stupně nebo pásma, zadejte mzdovou sazbu pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="eb78d-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="eb78d-122">Mzdová sazba bude ověřena podle nastavení tolerance pro plán a minimálních a maximálních referenčních bodů pro úroveň kompenzace pozice.</span><span class="sxs-lookup"><span data-stu-id="eb78d-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="eb78d-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eb78d-123">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]