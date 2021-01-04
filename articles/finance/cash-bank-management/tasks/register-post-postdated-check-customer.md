---
title: Registrace a zaúčtování postdatovaného šeku pro odběratele
description: Podrobnosti postdatovaného šeku přijatého od zákazníka můžete zaregistrovat.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11089584e150a1a302eb969a5fb61cb9d1900901
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441193"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="822b9-103">Registrace a zaúčtování postdatovaného šeku pro odběratele</span><span class="sxs-lookup"><span data-stu-id="822b9-103">Register and post a postdated check for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="822b9-104">Podrobnosti postdatovaného šeku přijatého od zákazníka můžete zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="822b9-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="822b9-105">Také můžete postdatovaný šek zaúčtovat a generovat finanční transakce.</span><span class="sxs-lookup"><span data-stu-id="822b9-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="822b9-106">Dokončete následující úlohy před registrací a zaúčtováním postdatovaného šeku přijatého od odběratele:   \* Nastavte postdatované šeky na stránce Pokladna a banka \* Nastavte metodu platby pro postdatované šeky   Role tohoto postupu je Pokladník.</span><span class="sxs-lookup"><span data-stu-id="822b9-106">Complete the following tasks before you register and post a postdated check received from a customer:   \* Set up postdated check in the Cash and bank management page \* Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="822b9-107">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="822b9-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="822b9-108">Přejděte na Pohledávky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="822b9-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="822b9-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="822b9-109">Click New.</span></span>
3. <span data-ttu-id="822b9-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="822b9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="822b9-111">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="822b9-111">Click Lines.</span></span>
5. <span data-ttu-id="822b9-112">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="822b9-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="822b9-113">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="822b9-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="822b9-114">V poli Dobropis zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="822b9-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="822b9-115">Zadejte částku uvedenou na postdatovaném šeku.</span><span class="sxs-lookup"><span data-stu-id="822b9-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="822b9-116">Klikněte na kartu Platba.</span><span class="sxs-lookup"><span data-stu-id="822b9-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="822b9-117">V poli Způsob platby zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="822b9-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="822b9-118">Zvolte způsob platby pro postdatovaný šek.</span><span class="sxs-lookup"><span data-stu-id="822b9-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="822b9-119">Klikněte na kartu Postdatované šeky.</span><span class="sxs-lookup"><span data-stu-id="822b9-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="822b9-120">Zadejte datum do pole Datum splatnosti.</span><span class="sxs-lookup"><span data-stu-id="822b9-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="822b9-121">Zadejte datum, do kterého má být platba za postdatovaný šek provedena.</span><span class="sxs-lookup"><span data-stu-id="822b9-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="822b9-122">Zadejte hodnotu do pole Pobočka vydávající banky.</span><span class="sxs-lookup"><span data-stu-id="822b9-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="822b9-123">Zadejte bankovní údaje postdatovaného šeku.</span><span class="sxs-lookup"><span data-stu-id="822b9-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="822b9-124">Zadejte hodnotu do pole Číslo šeku.</span><span class="sxs-lookup"><span data-stu-id="822b9-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="822b9-125">Zadejte hodnotu do pole Název vydávající banky.</span><span class="sxs-lookup"><span data-stu-id="822b9-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="822b9-126">Zadejte bankovní údaje postdatovaného šeku.</span><span class="sxs-lookup"><span data-stu-id="822b9-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="822b9-127">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="822b9-127">Click Post.</span></span>
16. <span data-ttu-id="822b9-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="822b9-128">Close the page.</span></span>

