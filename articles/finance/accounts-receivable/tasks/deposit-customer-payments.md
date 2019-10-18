---
title: Vklad platby odběratele
description: Vložení platby odběratele.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595d1b609ae83af8f1581caeff9ef7d3892a6207
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176831"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="5434b-103">Vklad platby odběratele</span><span class="sxs-lookup"><span data-stu-id="5434b-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5434b-104">Vložení platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="5434b-104">Deposit customer payments.</span></span> <span data-ttu-id="5434b-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="5434b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="5434b-106">Přejděte na **Podokno navigace Moduly > Pohledávky > Platby > Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="5434b-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="5434b-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="5434b-107">Select **New**.</span></span>
3. <span data-ttu-id="5434b-108">V poli **Název** vyberte **CustPay** v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="5434b-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="5434b-109">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="5434b-109">Select **Lines**.</span></span>
5. <span data-ttu-id="5434b-110">V poli **Účet** vyberte odběratele, od kterého jste platbu zaznamenali.</span><span class="sxs-lookup"><span data-stu-id="5434b-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="5434b-111">V poli **Kredit** zadejte částku platby.</span><span class="sxs-lookup"><span data-stu-id="5434b-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="5434b-112">Můžete určit, že chcete částku ponechat prázdnou a nechat systém vypočítat ji pomocí výběru faktur, které byly zaplaceny.</span><span class="sxs-lookup"><span data-stu-id="5434b-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="5434b-113">Zadejte hodnotu do pole **Odkaz na platbu**.</span><span class="sxs-lookup"><span data-stu-id="5434b-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="5434b-114">Platební odkaz může být číslo šeku pro platbu, kterou zadáváte.</span><span class="sxs-lookup"><span data-stu-id="5434b-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="5434b-115">Platební reference je vyžadována, pokud označíte zahrnutí platby na vkladové složence.</span><span class="sxs-lookup"><span data-stu-id="5434b-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="5434b-116">Zaškrtněte pole Použít vklad. složenku.</span><span class="sxs-lookup"><span data-stu-id="5434b-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="5434b-117">Má-li být platba zahrnuta do zálohy, toto nastavení změňte na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="5434b-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="5434b-118">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="5434b-118">Select **New**.</span></span>
10. <span data-ttu-id="5434b-119">V poli **Účet** vyberte odběratele pro další platbu.</span><span class="sxs-lookup"><span data-stu-id="5434b-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="5434b-120">Do pole **Kredit** zadejte výši úhrady.</span><span class="sxs-lookup"><span data-stu-id="5434b-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="5434b-121">Zadejte hodnotu do pole **Odkaz na platbu**.</span><span class="sxs-lookup"><span data-stu-id="5434b-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="5434b-122">Zaškrtněte pole **Použít vklad. složenku**.</span><span class="sxs-lookup"><span data-stu-id="5434b-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="5434b-123">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="5434b-123">Select **Post**.</span></span> <span data-ttu-id="5434b-124">Předtím, než lze generovat vkladové složenky, musí být zaúčtována platba.</span><span class="sxs-lookup"><span data-stu-id="5434b-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="5434b-125">Tím je zajištěno, že platby se nezmění po vygenerování vkladové složenky.</span><span class="sxs-lookup"><span data-stu-id="5434b-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="5434b-126">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="5434b-126">Select **Functions**.</span></span>
16. <span data-ttu-id="5434b-127">Zvolte **Vkladová složenka**.</span><span class="sxs-lookup"><span data-stu-id="5434b-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="5434b-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="5434b-128">Select **OK**.</span></span> <span data-ttu-id="5434b-129">První stránka slouží k vytvoření vkladové složenky.</span><span class="sxs-lookup"><span data-stu-id="5434b-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="5434b-130">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="5434b-130">Select **OK**.</span></span> <span data-ttu-id="5434b-131">Druhý krok je tisk vkladové složenky, ale tento krok není nutný.</span><span class="sxs-lookup"><span data-stu-id="5434b-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

