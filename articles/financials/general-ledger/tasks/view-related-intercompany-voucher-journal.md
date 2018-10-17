--- 
title: "Zobrazení souvisejícího mezipodnikového dokladu z deníku"
description: "Související doklad zobrazí doklad společností protiúčtu při zaúčtování mezipodnikové transakce z deníku hlavní knihy."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, SysDataAreaSelectLookup, LedgerTransVoucher, LedgerTransRelatedVouchers
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: fe2590b43a4399c3935906c8ab67a91883bbf094
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="view-related-intercompany-voucher-from-journal"></a><span data-ttu-id="be7b7-103">Zobrazení souvisejícího mezipodnikového dokladu z deníku</span><span class="sxs-lookup"><span data-stu-id="be7b7-103">View related intercompany voucher from journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be7b7-104">Související doklad zobrazí doklad společností protiúčtu při zaúčtování mezipodnikové transakce z deníku hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="be7b7-104">The related voucher window shows the voucher from the offset company when posting an intercompany transaction from the general journal.</span></span>


## <a name="post-an-intercompany-journal"></a><span data-ttu-id="be7b7-105">Zaúčtování mezipodnikového deníku</span><span class="sxs-lookup"><span data-stu-id="be7b7-105">Post an intercompany journal</span></span>
1. <span data-ttu-id="be7b7-106">Přejděte na možnost Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="be7b7-106">Go to General journals.</span></span>
2. <span data-ttu-id="be7b7-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be7b7-107">Click New.</span></span>
3. <span data-ttu-id="be7b7-108">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="be7b7-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="be7b7-109">V poli Název zadejte nebo vyberte název mezipodnikového deníku.</span><span class="sxs-lookup"><span data-stu-id="be7b7-109">In the Name field, enter or select the intercompany journal name.</span></span>
5. <span data-ttu-id="be7b7-110">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="be7b7-110">Click Lines.</span></span>
6. <span data-ttu-id="be7b7-111">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="be7b7-111">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="be7b7-112">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="be7b7-112">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="be7b7-113">V poli Popis zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be7b7-113">In the Description field, enter or select a value.</span></span>
9. <span data-ttu-id="be7b7-114">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="be7b7-114">In the Description field, type a value.</span></span>
10. <span data-ttu-id="be7b7-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be7b7-115">Close the page.</span></span>
11. <span data-ttu-id="be7b7-116">Do pole Má dáti zadejte čísl.</span><span class="sxs-lookup"><span data-stu-id="be7b7-116">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="be7b7-117">V poli Společnost protiúčtu vyberte nebo zadejte společnost protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="be7b7-117">In the Offset company field, type or select the offset company.</span></span>
13. <span data-ttu-id="be7b7-118">V poli Společnost protiúčtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be7b7-118">In the Offset company field, enter or select a value.</span></span>
14. <span data-ttu-id="be7b7-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be7b7-119">Close the page.</span></span>
15. <span data-ttu-id="be7b7-120">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="be7b7-120">In the Offset account field, specify the desired values.</span></span>
16. <span data-ttu-id="be7b7-121">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="be7b7-121">Click Post.</span></span>

## <a name="view-related-intercompany-voucher"></a><span data-ttu-id="be7b7-122">Zobrazení souvisejícího mezipodnikového dokladu</span><span class="sxs-lookup"><span data-stu-id="be7b7-122">View related intercompany voucher</span></span>
1. <span data-ttu-id="be7b7-123">Klikněte na možnost Doklad.</span><span class="sxs-lookup"><span data-stu-id="be7b7-123">Click Voucher.</span></span>
2. <span data-ttu-id="be7b7-124">Klikněte na možnost Související doklady.</span><span class="sxs-lookup"><span data-stu-id="be7b7-124">Click Related vouchers.</span></span>
3. <span data-ttu-id="be7b7-125">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="be7b7-125">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="be7b7-126">Klikněte na možnost Doklad.</span><span class="sxs-lookup"><span data-stu-id="be7b7-126">Click Voucher.</span></span>


