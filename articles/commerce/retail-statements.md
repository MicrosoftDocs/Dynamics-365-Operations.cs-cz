---
title: Výkazy maloobchodu
description: Toto téma popisuje způsob vytváření a zaúčtování výkazů.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 4409811d2ef60174a316db10307dc7af4697398c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021898"
---
# <a name="retail-statements"></a><span data-ttu-id="2f3d6-103">Příkazy maloobchodu</span><span class="sxs-lookup"><span data-stu-id="2f3d6-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f3d6-104">V aplikaci Dynamics 365 Commerce proces zaúčtování výkazů slouží k zaúčtování transakcí, které se mohou vyskytovat v Cloudovém pokladním místě (POS) nebo v Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="2f3d6-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="2f3d6-105">Proces zaúčtování výkazu používá plán distribuce k vyžádání sady transakcí Retail POS do klienta centrály (HQ).</span><span class="sxs-lookup"><span data-stu-id="2f3d6-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="2f3d6-106">Parametry, které jsou definovány na stránkách **Parametry velkoobchodu** a **Obchody** se používají k výběru transakcí, které budou převedeny na jednotlivé výkazy.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="2f3d6-107">Proces zaúčtování je znázorněn na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="2f3d6-108">V tomto procesu jsou transakce, které jsou zaznamenány v POS, předávány klientovi pomocí modulu Velkoobchodní plánovač.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="2f3d6-109">Po přijetí transakcí klientem můžete vytvářet, kalkulovat a zaúčtovávat výkazy transakce pro daný obchod.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="2f3d6-110">[![Proces zaúčtování výpisu](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="2f3d6-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="2f3d6-111">Vytváření a zaúčtovávání výkazů</span><span class="sxs-lookup"><span data-stu-id="2f3d6-111">Creating and posting statements</span></span>

<span data-ttu-id="2f3d6-112">Výkaz můžete vytvářet ručně nebo pomocí dávkových procesů, které jste nastavili ke spuštění v pravidelných intervalech během dne.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="2f3d6-113">V obou případech následující postup slouží k vytvoření a zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="2f3d6-114">Vytvoření výkazu</span><span class="sxs-lookup"><span data-stu-id="2f3d6-114">Create the statement</span></span>

<span data-ttu-id="2f3d6-115">Tento krok identifikuje obchod, pro který je výkaz ručně vytvořen.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="2f3d6-116">Pokud konfigurujete dávkové zpracování, můžete vytvořit automaticky výkazy pro všechny obchody podle určeného plánu.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="2f3d6-117">Výpočet výkazu</span><span class="sxs-lookup"><span data-stu-id="2f3d6-117">Calculate the statement</span></span>

<span data-ttu-id="2f3d6-118">V tomto kroku jsou vybrány řádky transakcí na základě kritérií, která jsou definovaná pro jednotlivé obchody na stránkách **Parametry velkoobchodu** a **Obchody**.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="2f3d6-119">Na těchto stránkách definujete kritéria a určujete způsob výpočtu transakce.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="2f3d6-120">Chcete-li zobrazit seznam transakcí, které jsou zahrnuty do výkazu, dříve než začnete počítat výkaz, použijte stránku **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="2f3d6-121">Výpočet výkazu používá tyto výkazy úhrad z registračních pokladen jako spočítanou částku.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="2f3d6-122">Případně můžete zadat spočítanou částku ručně.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="2f3d6-123">Výkaz ukazuje rozdíl mezi prodejní částkou transakce a skutečně spočítanou částkou u všech metod platby.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="2f3d6-124">Výkaz je zaúčtován tehdy, když rozdílová částka je menší než maximální vybraný rozdílu v zaúčtování definovaný pro obchod.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="2f3d6-125">Proces výpočtu výkazu používá globální číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="2f3d6-126">Při výpočtu výkazu výpočet zahrnuje následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="2f3d6-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="2f3d6-127">Pro vybraný rozsah dat označte transakce, které nebyly zahrnuty do předchozího výpočtu výkazu pro vybrané období.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="2f3d6-128">Proveďte výpočet celkových částek, které byly uhrazeny ve vybraných transakcích.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="2f3d6-129">Výsledky jsou zobrazeny v řádcích výkazu v závislosti na metodě výkazu:</span><span class="sxs-lookup"><span data-stu-id="2f3d6-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="2f3d6-130">Je-li metoda výkazu **Součet**, bude vytvořen řádek pro každý způsob platby ve vybraných transakcích.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="2f3d6-131">Je-li metoda výkazu **Zaměstnanci**, bude vytvořen řádek pro každý způsob platby v transakcích provedených vybraným zaměstnancem.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="2f3d6-132">Je-li metoda výkazu **Terminál POS**, bude vytvořen řádek pro každý způsob platby v transakcích provedených vybranou pokladnou.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="2f3d6-133">Je-li metoda výkazu **Směna**, bude vytvořen řádek pro každý způsob platby v transakcích provedených během směny.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="2f3d6-134">Pokud je na stránce **Obchody** zaškrtnuto políčko **Rozdělit podle způsobu výpisu**, vytvoří se samostatný výpis na základě hodnoty vybrané v poli **Způsob výpisu**.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="2f3d6-135">Pokud otevírací doba obchodu přesahuje po půlnoci, můžete nakonfigurovat zaúčtování výkazů podle konce pracovního dne namísto podle konce kalendářního dne.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="2f3d6-136">Na stránce **Obchody** na pevné záložce **Výpis/uzávěrka** v poli **Konec pracovního dne** zadejte čas, kdy musí být zaznamenána poslední transakce, aby byla zahrnuta do výkazu pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="2f3d6-137">Zaškrtnutím políčka **Zaúčtovat jako pracovní den** budete účtovat transakce v rámci stejného pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="2f3d6-138">Při zaúčtování výkazu, transakcí které jsou zaznamenány do stejného pracovního dne lze vložit do stejné prodejní objednávky, i když se některé transakce objeví před půlnocí a jiné po půlnoci.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="2f3d6-139">Příklad: Zaúčtování výkazu pro pracovní den, který zasahuje do dvou kalendářních dní</span><span class="sxs-lookup"><span data-stu-id="2f3d6-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="2f3d6-140">Obchod je otevřen v 8:00 až 3:00 a je zaškrtnuto políčko **Zaúčtovat jako pracovní den** v konfiguraci obchodu.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="2f3d6-141">31. května obchod eviduje transakce mezi 8:00 a půlnocí.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="2f3d6-142">Obchod zaznamená také transakce, které se uskutečnily v době mezi 12:01 až 3:00 1. června.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="2f3d6-143">Při zaúčtování výkazu obchodu při ukončení pracovního dne, dojde k vygenerování prodejní objednávky obsahující všechny transakce, které byly zapsány v pracovní době mezi 8.00 a 3.00 dopoledne, přestože k transakcím došlo během dvou dnů, 31. května i 1. června.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="2f3d6-144">Pokud je stejný obchod nakonfigurován bez zaškrtnutého políčka **Zaúčtovat pracovní den** pro stejný obchod, jsou generovány samostatné prodejní objednávky, když obchod zaúčtovává výkazy při ukončení pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="2f3d6-145">Jedna prodejní objednávka obsahuje transakce, které byly zaznamenány během pracovní doby od 8.00 do půlnoci 31. května, a druhá prodejní objednávka obsahuje transakce, které byly zaznamenány v pracovní době mezi 12:01 a 3:00 1. června.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="2f3d6-146">Před vytvořením výkazů zavřete směny v určeném období.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="2f3d6-147">Zaúčtování výkazu</span><span class="sxs-lookup"><span data-stu-id="2f3d6-147">Post the statement</span></span>

<span data-ttu-id="2f3d6-148">Při zaúčtování výkazu prodejní objednávky a faktury jsou vytvořeny pro prodej ve výkazu.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="2f3d6-149">Prodej cash and carry jsou agregován na jedné prodejní objednávce a fakturován pro výchozího odběratele, který je přiřazen k obchodu.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="2f3d6-150">Prodeje, pro které byl přidání zákazník do transakce v POS, generují samostatné prodejní objednávky a faktury, jednu pro každého jedinečného odběratele.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="2f3d6-151">Pro platby ve výkazu jsou automaticky vytvořeny deníky plateb a zásoby jsou automaticky aktualizovány pro obchod POS.</span><span class="sxs-lookup"><span data-stu-id="2f3d6-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>
