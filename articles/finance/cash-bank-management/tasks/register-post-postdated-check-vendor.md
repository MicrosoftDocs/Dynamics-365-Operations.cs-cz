---
title: Registrace a zaúčtování postdatovaného šeku pro dodavatele
description: Můžete si zaregistrovat podrobnosti postdatovaného šeku před vydáním šeku na dodavatele pomocí účetního dokladu.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb7f9935b20d042551b0ce77fd6bdbf55e9f9669
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834661"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="b0b09-103">Registrace a zaúčtování postdatovaného šeku pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="b0b09-103">Register and post a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0b09-104">Můžete si zaregistrovat podrobnosti postdatovaného šeku před vydáním šeku na dodavatele pomocí účetního dokladu.</span><span class="sxs-lookup"><span data-stu-id="b0b09-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="b0b09-105">Také můžete postdatovaný šek zaúčtovat a generovat finanční transakce.</span><span class="sxs-lookup"><span data-stu-id="b0b09-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="b0b09-106">Než můžete zaregistrovat a zaúčtovat postdatovaný šek od dodavatele, proveďte následující úkol:</span><span class="sxs-lookup"><span data-stu-id="b0b09-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="b0b09-107">Nastavte postdatované šeky na stránce Pokladna a banka.</span><span class="sxs-lookup"><span data-stu-id="b0b09-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="b0b09-108">Role tohoto průvodce úkolem je Pokladník.</span><span class="sxs-lookup"><span data-stu-id="b0b09-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="b0b09-109">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="b0b09-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b0b09-110">Přejděte na Závazky > Platby > Deník plateb</span><span class="sxs-lookup"><span data-stu-id="b0b09-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="b0b09-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0b09-111">Click New.</span></span>
3. <span data-ttu-id="b0b09-112">Zadejte text „VendPay“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b0b09-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="b0b09-113">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="b0b09-113">Click Lines.</span></span>
5. <span data-ttu-id="b0b09-114">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="b0b09-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="b0b09-115">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b0b09-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b0b09-116">Do pole Má dáti zadejte čísl.</span><span class="sxs-lookup"><span data-stu-id="b0b09-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="b0b09-117">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0b09-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b0b09-118">Volba způsobu platby pro postdatovaný šek</span><span class="sxs-lookup"><span data-stu-id="b0b09-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="b0b09-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b0b09-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b0b09-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0b09-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b0b09-121">Klikněte na kartu Postdatované šeky.</span><span class="sxs-lookup"><span data-stu-id="b0b09-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="b0b09-122">Zadejte hodnotu do pole Číslo šeku.</span><span class="sxs-lookup"><span data-stu-id="b0b09-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="b0b09-123">Zadejte nebo upravte číslo postdatovaného šeku.</span><span class="sxs-lookup"><span data-stu-id="b0b09-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="b0b09-124">Zadejte hodnotu do pole Název vydávající banky.</span><span class="sxs-lookup"><span data-stu-id="b0b09-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="b0b09-125">zadejte bankovní údaje pro vydávající banku.</span><span class="sxs-lookup"><span data-stu-id="b0b09-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="b0b09-126">Klikněte na kartu Seznam.</span><span class="sxs-lookup"><span data-stu-id="b0b09-126">Click the List tab.</span></span>
15. <span data-ttu-id="b0b09-127">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="b0b09-127">Click Post.</span></span>
16. <span data-ttu-id="b0b09-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0b09-128">Close the page.</span></span>
17. <span data-ttu-id="b0b09-129">Klikněte na kartu Postdatované šeky.</span><span class="sxs-lookup"><span data-stu-id="b0b09-129">Click the Postdated checks tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]