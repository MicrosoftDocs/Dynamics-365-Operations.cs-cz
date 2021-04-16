---
title: Vyrovnání postdatovaného šeku od odběratele
description: Postdatovaný šek můžete vyrovnat poté, co byl schválen bankou.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f714e41f47a31bce16424de18878d2f5acb5028d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834541"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="2c073-103">Vyrovnání postdatovaného šeku od odběratele</span><span class="sxs-lookup"><span data-stu-id="2c073-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c073-104">Postdatovaný šek můžete vyrovnat poté, co byl schválen bankou.</span><span class="sxs-lookup"><span data-stu-id="2c073-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="2c073-105">Tato finanční transakce rovněž schválí překlenovací transakci účtu pro postdatovaný šek.</span><span class="sxs-lookup"><span data-stu-id="2c073-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="2c073-106">Před zahájením tohoto úkolu je nutné dokončit následující úkoly.</span><span class="sxs-lookup"><span data-stu-id="2c073-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="2c073-107">Nastavení postdatovaných šeků</span><span class="sxs-lookup"><span data-stu-id="2c073-107">Set up postdated checks</span></span>

2) <span data-ttu-id="2c073-108">Registrace a zaúčtování postdatovaného šeku pro odběratele</span><span class="sxs-lookup"><span data-stu-id="2c073-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="2c073-109">Role tohoto průvodce úkolem je Pokladník.</span><span class="sxs-lookup"><span data-stu-id="2c073-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="2c073-110">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="2c073-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="2c073-111">Přejděte do nabídky Kredit a inkasa > Dotazy a sestavy > Platby > Postdatované šeky odběratele.</span><span class="sxs-lookup"><span data-stu-id="2c073-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="2c073-112">Klikněte na možnost Vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="2c073-112">Click Settle.</span></span>
3. <span data-ttu-id="2c073-113">Klikněte na možnost Vyrovnat položky clearingu.</span><span class="sxs-lookup"><span data-stu-id="2c073-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="2c073-114">Vyrovnejte účet odběratele pro transakci šeku.</span><span class="sxs-lookup"><span data-stu-id="2c073-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="2c073-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2c073-115">Close the page.</span></span>
5. <span data-ttu-id="2c073-116">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="2c073-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="2c073-117">Vyberte možnost v poli Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="2c073-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="2c073-118">Zaškrtněte políčko Zobrazit pouze uživatelem vytvořené položky nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="2c073-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="2c073-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2c073-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="2c073-120">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="2c073-120">Click Lines.</span></span>
10. <span data-ttu-id="2c073-121">Klikněte na možnost Doklad.</span><span class="sxs-lookup"><span data-stu-id="2c073-121">Click Voucher.</span></span>
11. <span data-ttu-id="2c073-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2c073-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]