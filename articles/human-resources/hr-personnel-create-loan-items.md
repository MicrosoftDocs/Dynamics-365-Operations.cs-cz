---
title: Vytvořit položky výpůjček
description: Položky výpůjčky jsou záznamy, které vám pomohou sledovat fyzické položky, jako například telefony nebo počítače, které vaše společnost poskytuje pro zaměstnance.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b93f68790a72af28130d80ed189538f9c5c87ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467090"
---
# <a name="create-loan-items"></a><span data-ttu-id="5cd39-103">Vytvořit položky výpůjček</span><span class="sxs-lookup"><span data-stu-id="5cd39-103">Create loan items</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="5cd39-104">Položky výpůjčky jsou záznamy, které vám pomohou sledovat fyzické položky, jako například telefony nebo počítače, které vaše společnost poskytuje pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5cd39-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="5cd39-105">Každá fyzická položka musí mít odpovídající položku výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="5cd39-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="5cd39-106">Každý záznam zapůjčené položky by měl obsahovat popis zapůjčené věci, kdo je za zapůjčení odpovědný a počet dní, které jsou pro půjčku stanoveny.</span><span class="sxs-lookup"><span data-stu-id="5cd39-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="5cd39-107">Můžete vytvořit více položek výpůjčky, například klíčů, přístupových karet nebo stejnokrojů současně.</span><span class="sxs-lookup"><span data-stu-id="5cd39-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="5cd39-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="5cd39-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="5cd39-109">Vytvoření typů výpůjčky</span><span class="sxs-lookup"><span data-stu-id="5cd39-109">Create Loan types</span></span>
1. <span data-ttu-id="5cd39-110">Přejděte na Lidské zdroje > Pracovníci > Položky výpůjčky > Typy výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="5cd39-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="5cd39-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5cd39-111">Click New.</span></span>
3. <span data-ttu-id="5cd39-112">Zadejte hodnotu do pole Typ výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="5cd39-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="5cd39-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="5cd39-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5cd39-114">Zadejte počet dní, který mohou být zapůjčené položky podle tohoto typu půjčky po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="5cd39-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="5cd39-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5cd39-115">Click Save.</span></span>
7. <span data-ttu-id="5cd39-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5cd39-116">Close the page.</span></span>
8. <span data-ttu-id="5cd39-117">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="5cd39-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="5cd39-118">Vytvoření položek výpůjčky</span><span class="sxs-lookup"><span data-stu-id="5cd39-118">Create Loan items</span></span>
1. <span data-ttu-id="5cd39-119">Přejděte na Lidské zdroje > Pracovníci > Položky výpůjčky > Položky výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="5cd39-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="5cd39-120">Klikněte na Vytvořit položky výpůjček.</span><span class="sxs-lookup"><span data-stu-id="5cd39-120">Click Create loan items.</span></span>
3. <span data-ttu-id="5cd39-121">Do pole Množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="5cd39-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="5cd39-122">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="5cd39-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5cd39-123">V poli Typ výpůjčky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5cd39-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5cd39-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5cd39-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="5cd39-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5cd39-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5cd39-126">Zadejte počet dnů, po které může být položka zapůjčena.</span><span class="sxs-lookup"><span data-stu-id="5cd39-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="5cd39-127">Výchozí hodnota pole Plánovaný návrat na stránce Vypůjčené vybavení se vypočítá jako součet aktuálního data a tohoto čísla.</span><span class="sxs-lookup"><span data-stu-id="5cd39-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="5cd39-128">V poli Zodpovědná osoba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5cd39-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5cd39-129">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="5cd39-129">Click Select.</span></span>
11. <span data-ttu-id="5cd39-130">Zadejte číslo do pole Počáteční hodnota.</span><span class="sxs-lookup"><span data-stu-id="5cd39-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="5cd39-131">V poli Interval zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="5cd39-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="5cd39-132">Zadejte hodnotu do pole Formát.</span><span class="sxs-lookup"><span data-stu-id="5cd39-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="5cd39-133">Pokud má například počáteční číslo položky výpůjčky hodnotu 10, zadejte do pole Formát dva číselné symboly.</span><span class="sxs-lookup"><span data-stu-id="5cd39-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="5cd39-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5cd39-134">Click OK.</span></span>
15. <span data-ttu-id="5cd39-135">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="5cd39-135">Refresh the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]