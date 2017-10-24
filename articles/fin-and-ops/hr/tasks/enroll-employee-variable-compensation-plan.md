--- 
title: "Přihlášení zaměstnance k plánu variabilní kompenzace"
description: "Manažer kompenzací a zaměstnaneckých výhod může přihlásit zaměstnance do plánů variabilní kompenzace a vypočítat tak hotovostní a bezhotovostní odměny pro zaměstnance."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb162e22276fc19cf11999380d551b29ba6a6d45
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="3cca9-103">Přihlášení zaměstnance k plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="3cca9-103">Enroll an employee in a variable compensation plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3cca9-104">Manažer kompenzací a zaměstnaneckých výhod může přihlásit zaměstnance do plánů variabilní kompenzace a vypočítat tak hotovostní a bezhotovostní odměny pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="3cca9-104">The Compensation and Benefits manager can enrol employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="3cca9-105">Tento postup předpokládá, že byl vytvořen plán variabilní kompenzace, ve kterém je v poli Povolit přihlášení nastavena hodnota Ano, a že byla vytvořena pravidla způsobilosti pro tento plán variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="3cca9-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="3cca9-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="3cca9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3cca9-107">Tento postup zahájíte tak, že přejděte na Lidské zdroje > Pracovníci > Zaměstnanci > Kompenzace > Zápis variabilního plánu</span><span class="sxs-lookup"><span data-stu-id="3cca9-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="3cca9-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="3cca9-108">Click New.</span></span>
2. <span data-ttu-id="3cca9-109">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="3cca9-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3cca9-110">Vyhledávání plánu bude filtrováno a zobrazí pouze plány variabilní kompenzace, pro které je zaměstnanec způsobilý podle pravidel způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="3cca9-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="3cca9-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="3cca9-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3cca9-112">Přepněte rozšíření oddílu Obecné.</span><span class="sxs-lookup"><span data-stu-id="3cca9-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="3cca9-113">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="3cca9-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="3cca9-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="3cca9-114">Click Save.</span></span>
7. <span data-ttu-id="3cca9-115">Přepněte rozšíření oddílu Přepsání.</span><span class="sxs-lookup"><span data-stu-id="3cca9-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="3cca9-116">V případě potřeby lze nastavit datum pravidla zařazení tak, aby přepsalo datum zařazení zaměstnance v případě, že je u pravidla zařazení pro vybraný variabilní plán vybrána možnost Procento.</span><span class="sxs-lookup"><span data-stu-id="3cca9-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="3cca9-117">Pokud variabilní plán je plánem využívajícím procentuální část základu, je možné pro zaměstnance přepsat procentuální odměnu.</span><span class="sxs-lookup"><span data-stu-id="3cca9-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="3cca9-118">Pokud plán variabilní kompenzace je plánem využívajícím počet jednotek, je možné pro zaměstnance přepsat počet jednotek.</span><span class="sxs-lookup"><span data-stu-id="3cca9-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="3cca9-119">Pokud by měla být zaměstnanci dána prostá částka představující jejich odměnu, tuto částku můžete nastavit zde.</span><span class="sxs-lookup"><span data-stu-id="3cca9-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="3cca9-120">Přepněte rozšíření oddílu Organizační přepsání.</span><span class="sxs-lookup"><span data-stu-id="3cca9-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="3cca9-121">Je-li třeba zohlednit výkon zaměstnance, je možné přepsat výkon v ostatních odděleních nebo oddělení jiném, než které je přiřazeno pro pozici zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="3cca9-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="3cca9-122">Sloupec Procento musí dohromady dát číslo 100.</span><span class="sxs-lookup"><span data-stu-id="3cca9-122">The Percent column should total 100.</span></span>  


