---
title: Registrace a odebrání zaměstnaneckých výhod pracovníků
description: Tento postup ukazuje, jak jeden pracovník může být registrován do jedné nebo více zaměstnaneckých výhod, a také jak více pracovníků může být registrováno k zaměstnanecké výhodě.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92da6d24f3fc4282de5673a8155b6ab6316e55aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190412"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="47153-103">Registrace a odebrání zaměstnaneckých výhod pracovníků</span><span class="sxs-lookup"><span data-stu-id="47153-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47153-104">Tento postup ukazuje, jak jeden pracovník může být registrován do jedné nebo více zaměstnaneckých výhod, a také jak více pracovníků může být registrováno k zaměstnanecké výhodě.</span><span class="sxs-lookup"><span data-stu-id="47153-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="47153-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="47153-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="47153-106">Přihlásit jednoho pracovníka k zaměstnaneckým výhodám</span><span class="sxs-lookup"><span data-stu-id="47153-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="47153-107">Přejděte k nabídce Lidské zdroje > Pracovníci > Zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="47153-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="47153-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="47153-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="47153-109">Klikněte na možnost Zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="47153-109">Click Benefits.</span></span>
4. <span data-ttu-id="47153-110">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="47153-110">Click New.</span></span>
5. <span data-ttu-id="47153-111">V poli Zaměstnanecká výhody zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="47153-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="47153-112">Do pole Počáteční datum pokrytí zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="47153-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="47153-113">Do pole Koncové datum pokrytí zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="47153-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="47153-114">Pokud potřebujete přidat příjemce do zaměstnaneckých výhod, rozbalte oddíl příjemců.</span><span class="sxs-lookup"><span data-stu-id="47153-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="47153-115">Můžete také podle potřeby přidat závislé prvky z této stránky do zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="47153-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="47153-116">Na této stránce můžete také upravit podrobnosti o přihlášení k zaměstnanecké výhodě nebo přihlášení odstranit.</span><span class="sxs-lookup"><span data-stu-id="47153-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="47153-117">Po dokončení požadovaných změn v přihlášení k zaměstnanecké výhodě zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47153-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="47153-118">Přihlásit více pracovníků k zaměstnanecké výhodě</span><span class="sxs-lookup"><span data-stu-id="47153-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="47153-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47153-119">Close the page.</span></span>
2. <span data-ttu-id="47153-120">Přejděte k nabídce Lidské zdroje > Pracovníci > Zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="47153-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="47153-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="47153-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="47153-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="47153-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="47153-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="47153-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="47153-124">Klikněte na možnost Přihlášení k zaměstnaneckým výhodám.</span><span class="sxs-lookup"><span data-stu-id="47153-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="47153-125">V poli Zaměstnanecká výhody zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="47153-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="47153-126">Do pole Počáteční datum pokrytí zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="47153-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="47153-127">Do pole Koncové datum pokrytí zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="47153-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="47153-128">Klikněte na možnost Přihlásit.</span><span class="sxs-lookup"><span data-stu-id="47153-128">Click Enroll.</span></span>
11. <span data-ttu-id="47153-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47153-129">Close the page.</span></span>
12. <span data-ttu-id="47153-130">Přejděte na Lidské zdroje > Výhody > Přihlášení > Výsledky přihlášení k zaměstnanecké výhodě</span><span class="sxs-lookup"><span data-stu-id="47153-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="47153-131">Najděte záznam výsledků zaměstnanecké výhody, který hledáte.</span><span class="sxs-lookup"><span data-stu-id="47153-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="47153-132">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="47153-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="47153-133">Na této stránce můžete zobrazit, kterým zaměstnancům byly zapsány zaměstnanecké výhody a také všechny zaměstnance, kteří nebyli přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="47153-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

