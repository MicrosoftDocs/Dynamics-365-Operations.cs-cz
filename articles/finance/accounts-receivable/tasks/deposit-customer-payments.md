---
title: Vklad platby odběratele
description: Vložení platby odběratele.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bf44570a0eaceab94765b100bdd8b4d507a0f54
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822364"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="13720-103">Vklad platby odběratele</span><span class="sxs-lookup"><span data-stu-id="13720-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13720-104">Vložení platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="13720-104">Deposit customer payments.</span></span> <span data-ttu-id="13720-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="13720-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="13720-106">Přejděte na **Podokno navigace Moduly > Pohledávky > Platby > Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="13720-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="13720-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="13720-107">Select **New**.</span></span>
3. <span data-ttu-id="13720-108">V poli **Název** vyberte **CustPay** v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="13720-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="13720-109">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="13720-109">Select **Lines**.</span></span>
5. <span data-ttu-id="13720-110">V poli **Účet** vyberte odběratele, od kterého jste platbu zaznamenali.</span><span class="sxs-lookup"><span data-stu-id="13720-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="13720-111">V poli **Kredit** zadejte částku platby.</span><span class="sxs-lookup"><span data-stu-id="13720-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="13720-112">Můžete určit, že chcete částku ponechat prázdnou a nechat systém vypočítat ji pomocí výběru faktur, které byly zaplaceny.</span><span class="sxs-lookup"><span data-stu-id="13720-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="13720-113">Zadejte hodnotu do pole **Odkaz na platbu**.</span><span class="sxs-lookup"><span data-stu-id="13720-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="13720-114">Platební odkaz může být číslo šeku pro platbu, kterou zadáváte.</span><span class="sxs-lookup"><span data-stu-id="13720-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="13720-115">Platební reference je vyžadována, pokud označíte zahrnutí platby na vkladové složence.</span><span class="sxs-lookup"><span data-stu-id="13720-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="13720-116">Zaškrtněte pole Použít vklad. složenku.</span><span class="sxs-lookup"><span data-stu-id="13720-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="13720-117">Má-li být platba zahrnuta do zálohy, toto nastavení změňte na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="13720-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="13720-118">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="13720-118">Select **New**.</span></span>
10. <span data-ttu-id="13720-119">V poli **Účet** vyberte odběratele pro další platbu.</span><span class="sxs-lookup"><span data-stu-id="13720-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="13720-120">Do pole **Kredit** zadejte výši úhrady.</span><span class="sxs-lookup"><span data-stu-id="13720-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="13720-121">Zadejte hodnotu do pole **Odkaz na platbu**.</span><span class="sxs-lookup"><span data-stu-id="13720-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="13720-122">Zaškrtněte pole **Použít vklad. složenku**.</span><span class="sxs-lookup"><span data-stu-id="13720-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="13720-123">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="13720-123">Select **Post**.</span></span> <span data-ttu-id="13720-124">Předtím, než lze generovat vkladové složenky, musí být zaúčtována platba.</span><span class="sxs-lookup"><span data-stu-id="13720-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="13720-125">Tím je zajištěno, že platby se nezmění po vygenerování vkladové složenky.</span><span class="sxs-lookup"><span data-stu-id="13720-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="13720-126">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="13720-126">Select **Functions**.</span></span>
16. <span data-ttu-id="13720-127">Zvolte **Vkladová složenka**.</span><span class="sxs-lookup"><span data-stu-id="13720-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="13720-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="13720-128">Select **OK**.</span></span> <span data-ttu-id="13720-129">První stránka slouží k vytvoření vkladové složenky.</span><span class="sxs-lookup"><span data-stu-id="13720-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="13720-130">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="13720-130">Select **OK**.</span></span> <span data-ttu-id="13720-131">Druhý krok je tisk vkladové složenky, ale tento krok není nutný.</span><span class="sxs-lookup"><span data-stu-id="13720-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]