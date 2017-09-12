--- 
title: "Vytvořit položky výpůjček"
description: "Položky výpůjčky jsou záznamy, které vám pomohou sledovat fyzické položky, jako například telefony nebo počítače, které vaše společnost poskytuje pro zaměstnance."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="60a44-103">Vytvořit položky výpůjček</span><span class="sxs-lookup"><span data-stu-id="60a44-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60a44-104">Položky výpůjčky jsou záznamy, které vám pomohou sledovat fyzické položky, jako například telefony nebo počítače, které vaše společnost poskytuje pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="60a44-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="60a44-105">Každá fyzická položka musí mít odpovídající položku výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="60a44-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="60a44-106">Každý záznam zapůjčené položky by měl obsahovat popis zapůjčené věci, kdo je za zapůjčení odpovědný a počet dní, které jsou pro půjčku stanoveny.</span><span class="sxs-lookup"><span data-stu-id="60a44-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="60a44-107">Můžete vytvořit více položek výpůjčky, například klíčů, přístupových karet nebo stejnokrojů současně.</span><span class="sxs-lookup"><span data-stu-id="60a44-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="60a44-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="60a44-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="60a44-109">Vytvoření typů výpůjčky</span><span class="sxs-lookup"><span data-stu-id="60a44-109">Create Loan types</span></span>
1. <span data-ttu-id="60a44-110">Přejděte na Lidské zdroje > Pracovníci > Položky výpůjčky > Typy výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="60a44-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="60a44-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="60a44-111">Click New.</span></span>
3. <span data-ttu-id="60a44-112">Zadejte hodnotu do pole Typ výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="60a44-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="60a44-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="60a44-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="60a44-114">Zadejte počet dní, který mohou být zapůjčené položky podle tohoto typu půjčky po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="60a44-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="60a44-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="60a44-115">Click Save.</span></span>
7. <span data-ttu-id="60a44-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="60a44-116">Close the page.</span></span>
8. <span data-ttu-id="60a44-117">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="60a44-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="60a44-118">Vytvoření položek výpůjčky</span><span class="sxs-lookup"><span data-stu-id="60a44-118">Create Loan items</span></span>
1. <span data-ttu-id="60a44-119">Přejděte na Lidské zdroje > Pracovníci > Položky výpůjčky > Položky výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="60a44-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="60a44-120">Klikněte na Vytvořit položky výpůjček.</span><span class="sxs-lookup"><span data-stu-id="60a44-120">Click Create loan items.</span></span>
3. <span data-ttu-id="60a44-121">Do množství</span><span class="sxs-lookup"><span data-stu-id="60a44-121">In the Qty.</span></span> <span data-ttu-id="60a44-122">zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="60a44-122">field, enter a number.</span></span>
4. <span data-ttu-id="60a44-123">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="60a44-123">In the Description field, type a value.</span></span>
5. <span data-ttu-id="60a44-124">V poli Typ výpůjčky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="60a44-124">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="60a44-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="60a44-125">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="60a44-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="60a44-126">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="60a44-127">Zadejte počet dnů, po které může být položka zapůjčena.</span><span class="sxs-lookup"><span data-stu-id="60a44-127">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="60a44-128">Výchozí hodnota pole Plánovaný návrat na stránce Vypůjčené vybavení se vypočítá jako součet aktuálního data a tohoto čísla.</span><span class="sxs-lookup"><span data-stu-id="60a44-128">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="60a44-129">V poli Zodpovědná osoba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="60a44-129">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="60a44-130">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="60a44-130">Click Select.</span></span>
11. <span data-ttu-id="60a44-131">Zadejte číslo do pole Počáteční hodnota.</span><span class="sxs-lookup"><span data-stu-id="60a44-131">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="60a44-132">V poli Interval zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="60a44-132">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="60a44-133">Zadejte hodnotu do pole Formát.</span><span class="sxs-lookup"><span data-stu-id="60a44-133">In the Format field, type a value.</span></span>
    * <span data-ttu-id="60a44-134">Pokud má například počáteční číslo položky výpůjčky hodnotu 10, zadejte do pole Formát dva číselné symboly.</span><span class="sxs-lookup"><span data-stu-id="60a44-134">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="60a44-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="60a44-135">Click OK.</span></span>
15. <span data-ttu-id="60a44-136">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="60a44-136">Refresh the page.</span></span>


