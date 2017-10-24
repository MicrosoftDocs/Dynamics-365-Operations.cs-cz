--- 
title: "Vytvoření schémat časového rozlišení"
description: "Tento průvodce úkoly vás provede vytvořením schématu časového rozlišení."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="2b3ef-103">Vytvoření schémat časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="2b3ef-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b3ef-104">Tento průvodce úkoly vás provede vytvořením schématu časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="2b3ef-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2b3ef-106">Přejděte do hlavní knihy > Nastavení deníku > Schémata časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="2b3ef-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-107">Click New.</span></span>
3. <span data-ttu-id="2b3ef-108">Zadejte hodnotu do pole Identifikace časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="2b3ef-109">Do pole Popis schématu časového rozlišení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="2b3ef-110">Zadejte požadované hodnoty do pole Má dáti.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="2b3ef-111">Definovaný hlavní účet nahradí hlavní účet Má dáti v řádku dokladu deníku také bude použit pro stornování časově rozlišených položek na základě transakcí časového rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="2b3ef-112">Zadejte požadované hodnoty do pole Dal.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="2b3ef-113">Definovaný hlavní účet nahradí kreditní hlavní účet řádku dokladu deníku a také bude použit pro stornování časově rozlišených položek podle transakcí časového rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="2b3ef-114">V poli Doklad vyberte způsob určení dokladu, když jsou transakce zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="2b3ef-115">V poli Popis zadejte hodnotu k popisu transakcí, které mají být zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="2b3ef-116">V poli Frekvence období vyberte, jak často by transakce měla být zaznamenána.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="2b3ef-117">Do pole Počet výskytů podle období zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="2b3ef-118">V poli Zaúčtovat transakce vyberte, kdy transakce mají být zaúčtovány – například měsíčně.</span><span class="sxs-lookup"><span data-stu-id="2b3ef-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


