--- 
title: "Vklad platby odběratele"
description: "Vložení platby odběratele."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 73f5e34054bee5c7b81ca6d4b3e4b3d2339a6b86
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="dc7f6-103">Vklad platby odběratele</span><span class="sxs-lookup"><span data-stu-id="dc7f6-103">Deposit customer payments</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc7f6-104">Vložení platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-104">Deposit customer payments.</span></span> <span data-ttu-id="dc7f6-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="dc7f6-106">Přejděte na Pohledávky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="dc7f6-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-107">Click New.</span></span>
3. <span data-ttu-id="dc7f6-108">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dc7f6-109">Vyberte deník platby.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="dc7f6-110">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-110">Click Lines.</span></span>
6. <span data-ttu-id="dc7f6-111">V poli Účet vyberte odběratele, od kterého jste platbu zaznamenali.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="dc7f6-112">V poli Dobropis zadejte částku platby.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="dc7f6-113">Můžete určit, že chcete částku ponechat prázdnou a nechat systém vypočítat ji pomocí výběru faktur, které byly zaplaceny.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="dc7f6-114">Zadejte hodnotu do pole Odkaz na platbu.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="dc7f6-115">Platební odkaz může být číslo šeku pro platbu, kterou zadáváte.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="dc7f6-116">Platební reference je vyžadována, pokud označíte zahrnutí platby na vkladové složence.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="dc7f6-117">Zaškrtněte pole Použít vklad. složenku.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="dc7f6-118">Má-li být platba zahrnuta do zálohy, toto nastavení změňte na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="dc7f6-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-119">Click New.</span></span>
11. <span data-ttu-id="dc7f6-120">V poli Účet vyberte odběratele pro další platbu.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="dc7f6-121">Do pole Dobropis zadejte výši úhrady.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="dc7f6-122">Zadejte hodnotu do pole Odkaz na platbu.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="dc7f6-123">Zaškrtněte pole Použít vklad. složenku.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="dc7f6-124">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-124">Click Post.</span></span>
    * <span data-ttu-id="dc7f6-125">Předtím, než lze generovat vkladové složenky, musí být zaúčtována platba.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="dc7f6-126">Tím je zajištěno, že platby se nezmění po vygenerování vkladové složenky.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="dc7f6-127">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-127">Click Functions.</span></span>
17. <span data-ttu-id="dc7f6-128">Klikněte na Vkladová složenka.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="dc7f6-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-129">Click OK.</span></span>
    * <span data-ttu-id="dc7f6-130">První stránka slouží k vytvoření vkladové složenky.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="dc7f6-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-131">Click OK.</span></span>
    * <span data-ttu-id="dc7f6-132">Druhý krok je tisk vkladové složenky, ale tento krok není nutný.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


