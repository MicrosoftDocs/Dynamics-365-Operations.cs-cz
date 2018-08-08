--- 
title: "Stanovení platebních poplatků odběratele"
description: "Vytvořte poplatky pro platbu pro úhrady odběratelů."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1b223d99c19b559dd428159fc65cd68566c2b221
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="cfc5b-103">Stanovení platebních poplatků odběratele</span><span class="sxs-lookup"><span data-stu-id="cfc5b-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cfc5b-104">Vytvořte poplatky pro platbu pro úhrady odběratelů.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="cfc5b-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cfc5b-106">Přejděte do nabídky Pohledávky > Nastavení platby > Platební poplatek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="cfc5b-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-107">Click New.</span></span>
3. <span data-ttu-id="cfc5b-108">V poli ID poplatku zadejte ID poplatku.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="cfc5b-109">ID poplatku se zobrazí na denících platby, takže je zadejte dostatečně popisné, aby bylo možné pochopit, jaký poplatek je vyměřen.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="cfc5b-110">Do pole Název zadejte název poplatku.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="cfc5b-111">Do pole Popis poplatku zadejte popis poplatku.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="cfc5b-112">Určete, zda poplatek bude účtován z účtu hlavní knihy nebo odběratele.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="cfc5b-113">Pokud je odběrateli stanoven poplatek, vyberte Odběratel.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="cfc5b-114">Pokud bude poplatek vyměřen pro vaši organizaci v rámci výdajů, vyberte Hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="cfc5b-115">Pro tento úkol vyberte Odběratele.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="cfc5b-116">Vyberte typ deníku, který lze použít pro tento platební poplatek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="cfc5b-117">Pokud se tyto poplatky používají pro platby odběratelů, typu deníku bude pravděpodobně Platba odběratele.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="cfc5b-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-118">Click Save.</span></span>
9. <span data-ttu-id="cfc5b-119">Klikněte na Nastavení platebního poplatku.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="cfc5b-120">Nastavení platebního poplatku se používá ke stanovení kritérií pro dobu, kdy se platebního poplatek hodnotí.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="cfc5b-121">Můžete například definovat, že bude poplatek vypočítán, pokud je bankovní účet USMF OPER, a způsob platby je šek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="cfc5b-122">Zaškrtněte buď Tabulka, Skupina nebo Vše a definujte tak, jaké bankovní účty, budou oceněny pro tento poplatek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="cfc5b-123">Pokud vyberete možnost Vše, všechny bankovní účty mohou hodnotit tento poplatek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="cfc5b-124">Pokud vyberete Tabulka, může být pro tento poplatek hodnocen pouze vybraný bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="cfc5b-125">Jestliže vyberete Skupina, pouze bankovní účty ve vybrané bankovní skupině mohou být vyhodnoceny pro tento poplatek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="cfc5b-126">Vyberte bankovní účet nebo bankovní skupinu.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="cfc5b-127">Pokud vyberete Tabulka, zobrazí se vyhledávání bankovních účtů.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="cfc5b-128">Pokud vyberete Skupina, zobrazí se vyhledávání bankovních skupin.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="cfc5b-129">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="cfc5b-130">Vyberte metodu platby, pro kterou se vyhodnotí tento poplatek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="cfc5b-131">Můžete například vyhodnotit poplatek pro vaše odběratele, jestliže odešlou platby jako šek, nikoli jako elektronickou platbu.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="cfc5b-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="cfc5b-133">V případě potřeby zadejte měnu platby.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="cfc5b-134">Měna platby se používá jako další kritérium pro to, zda budou poplatky posouzeny.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="cfc5b-135">Například může vaše banka účtovat dodatečný poplatek pro plateb přijaté v měně USD, protože obvykle provádí pouze transakce v měně EUR.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="cfc5b-136">Určete, zda poplatek budou procenta, částka nebo interval.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="cfc5b-137">Zadejte procento nebo částku poplatku.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="cfc5b-138">Je-li v poli Procento/Částka vybrána možnost Procento, pak hodnota zadaná zde bude procento.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="cfc5b-139">Je-li v poli Procento/Částka vybrána možnost Částka, pak hodnota zadaná zde bude částka.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="cfc5b-140">Je-li v poli Procento/Částka vybrána možnost Interval, použijte kartu Interval pro definování úrovní.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="cfc5b-141">V poli Měna poplatku vyberte měny poplatku.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="cfc5b-142">Toto je měna, v níž bude vytvořen poplatek.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="cfc5b-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cfc5b-143">Click Save.</span></span>


