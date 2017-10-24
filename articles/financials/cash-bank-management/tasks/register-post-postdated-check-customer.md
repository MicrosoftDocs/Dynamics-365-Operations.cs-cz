--- 
title: "Registrace a zaúčtování postdatovaného šeku pro odběratele"
description: "Podrobnosti postdatovaného šeku přijatého od zákazníka můžete zaregistrovat."
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="d1424-103">Registrace a zaúčtování postdatovaného šeku pro odběratele</span><span class="sxs-lookup"><span data-stu-id="d1424-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1424-104">Podrobnosti postdatovaného šeku přijatého od zákazníka můžete zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="d1424-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="d1424-105">Také můžete postdatovaný šek zaúčtovat a generovat finanční transakce.</span><span class="sxs-lookup"><span data-stu-id="d1424-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="d1424-106">Dokončete následující úlohy před registrací a zaúčtováním postdatovaného šeku přijatého od odběratele:  • Nastavte postdatované šeky na stránce Pokladna a banka • Nastavte metodu platby pro postdatované šeky.   Role tohoto postupu je Pokladník</span><span class="sxs-lookup"><span data-stu-id="d1424-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="d1424-107">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="d1424-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="d1424-108">Přejděte na Pohledávky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="d1424-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="d1424-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d1424-109">Click New.</span></span>
3. <span data-ttu-id="d1424-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d1424-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d1424-111">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="d1424-111">Click Lines.</span></span>
5. <span data-ttu-id="d1424-112">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d1424-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="d1424-113">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="d1424-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="d1424-114">V poli Dobropis zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="d1424-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="d1424-115">Zadejte částku uvedenou na postdatovaném šeku.</span><span class="sxs-lookup"><span data-stu-id="d1424-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="d1424-116">Klikněte na kartu Platba.</span><span class="sxs-lookup"><span data-stu-id="d1424-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="d1424-117">V poli Způsob platby zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d1424-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="d1424-118">Volba způsobu platby pro postdatovaný šek</span><span class="sxs-lookup"><span data-stu-id="d1424-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="d1424-119">Klikněte na kartu Postdatované šeky.</span><span class="sxs-lookup"><span data-stu-id="d1424-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="d1424-120">Zadejte datum do pole Datum splatnosti.</span><span class="sxs-lookup"><span data-stu-id="d1424-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="d1424-121">Zadejte datum, do kterého má být platba za postdatovaný šek provedena.</span><span class="sxs-lookup"><span data-stu-id="d1424-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="d1424-122">Zadejte hodnotu do pole Pobočka vydávající banky.</span><span class="sxs-lookup"><span data-stu-id="d1424-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="d1424-123">Zadejte bankovní údaje postdatovaného šeku.</span><span class="sxs-lookup"><span data-stu-id="d1424-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="d1424-124">Zadejte hodnotu do pole Číslo šeku.</span><span class="sxs-lookup"><span data-stu-id="d1424-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="d1424-125">Zadejte hodnotu do pole Název vydávající banky.</span><span class="sxs-lookup"><span data-stu-id="d1424-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="d1424-126">Zadejte bankovní údaje postdatovaného šeku.</span><span class="sxs-lookup"><span data-stu-id="d1424-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="d1424-127">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="d1424-127">Click Post.</span></span>
16. <span data-ttu-id="d1424-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d1424-128">Close the page.</span></span>


