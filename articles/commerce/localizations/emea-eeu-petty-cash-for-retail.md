---
title: Správa pokladní hotovosti pro Commerce pro východní Evropu
description: Toto téma popisuje, jak nastavit a používat funkce správy hotovosti v aplikaci Commerce pro východní Evropu.
author: epopov
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 9305e7143bc0a978569d51544a1ae65ee57b3243
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798815"
---
# <a name="petty-cash-management-for-commerce-for-eastern-europe"></a><span data-ttu-id="c4e2e-103">Správa pokladní hotovosti pro Commerce pro východní Evropu</span><span class="sxs-lookup"><span data-stu-id="c4e2e-103">Petty cash management for Commerce for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4e2e-104">Tento článek obsahuje informace o východoevropské lokalizaci specifické pro oblast obchodu.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-104">This article contains information about Eastern European localization specific for the commerce industry.</span></span>

<span data-ttu-id="c4e2e-105">V souladu s požadavky na účtování ve východní Evropě můžete nastavit operace pro pokladní účty pro automatizaci procesů pro příjemky, pokladní doklady a výpisy hotovosti.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-105">In accordance with the Eastern Europe accounting requirements, you can set up operations for cash accounts to automate the processes for receipts, cash documents and cash reports.</span></span> <span data-ttu-id="c4e2e-106">Více informací naleznete v části [(EEUR) Nastavení parametrů pro správu hotovosti](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span><span class="sxs-lookup"><span data-stu-id="c4e2e-106">For more information, go to [(EEUR) Set up parameters for cash management](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span></span>

<span data-ttu-id="c4e2e-107">Maloobchodní prodejci mohou přijímat různé typy plateb za výrobky a služby, které prodávají.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-107">Retailers can accept various types of payment in exchange for the products and services that they sell.</span></span> <span data-ttu-id="c4e2e-108">I když jsou hotovostní platby nejčastěji používaným typem platby, maloobchodní prodejci mohou také přijímat platby ve formě šeků, karet nebo kuponů.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-108">Although cash is the most common form of payment, retailers can also receive payment in the form of checks, cards, or vouchers.</span></span> <span data-ttu-id="c4e2e-109">V maloobchodním pokladním místě (POS) jsou hotovost, doklady o platbě kartou a ostatní platby zpracovány n pokladně.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-109">In Retail point of sale (POS), cash, credit card receipts, and other payments are processed through a cash office.</span></span>

<span data-ttu-id="c4e2e-110">Pomocí správy hotovosti v aplikaci Commerce můžete provádět následující akce:</span><span class="sxs-lookup"><span data-stu-id="c4e2e-110">You can do the following by using Cash management in Commerce:</span></span>

- <span data-ttu-id="c4e2e-111">Vytvoření pokladního účtu pro vybraný způsob platby pro každý obchod.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-111">Create a cash account for the selected payment method for each store.</span></span>
- <span data-ttu-id="c4e2e-112">Použít deníky hotovosti k zaúčtování hotovostních transakcí a plateb zákazníků přijímaných v Retail POS.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-112">Use cash journals to post cash transactions and customer payments that are received at a retail POS.</span></span>
- <span data-ttu-id="c4e2e-113">Sdružení transakcí v řádku výkazu při zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-113">Aggregate transactions in a statement line when you post a statement.</span></span> <span data-ttu-id="c4e2e-114">Můžete sdružovat odvody do trezoru, odvody do banky, transakce dokladu, odebírat transakce odvodu, transakce s plovoucí položkou, příjmové transakce, výdajové transakce, platby odběratelů, prodejní transakce a návratové transakce.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-114">You can aggregate safe drops, bank drops, voucher transactions, remove tender transactions, float entry transactions, income transactions, expense transactions, customer payments, sales transactions, and return transactions.</span></span>

<span data-ttu-id="c4e2e-115">Všechny transakce, které se uskutečňují v POS, jsou zaúčtovány pomocí deníku hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-115">All transactions that take place in POS are posted using a ledger journal.</span></span> <span data-ttu-id="c4e2e-116">Pokladní deníky plateb, deníky plateb odběratelů a hlavní deníky můžete používat k vytvoření a zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-116">You can use cash payment journals, customer payment journals, and general journals to create and post the statements.</span></span> <span data-ttu-id="c4e2e-117">Více informací naleznete v části [Vytvoření, výpočet a zaúčtování výkazů pro maloobchod](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span><span class="sxs-lookup"><span data-stu-id="c4e2e-117">For more information, go to [Create, calculate, and post statements for a retail store](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span></span>

<span data-ttu-id="c4e2e-118">Na stránce **Zaúčtované výkazy** v podokně akcí můžete provést následující:</span><span class="sxs-lookup"><span data-stu-id="c4e2e-118">On the **Posted statements** page, on the Action Pane, you can do the following:</span></span>

- <span data-ttu-id="c4e2e-119">Přejděte na **Dotazy \> Deník plateb v hotovosti** pro přístup k deníkům plateb v hotovosti souvisejícím s výkazem.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-119">Go to **Inquiries \> Cash payment journal** to access the cash payment journals that are related to the statement.</span></span>
- <span data-ttu-id="c4e2e-120">Přejděte na **Dotazy \> Hlavní deník** pro přístup k deníkům hlavní knihy, které se vztahují k výkazu jinému, než jsou platby odběratele a platby v hotovosti.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-120">Go to **Inquiries \> General journal** to access the ledger journals that are related to the statement, other than customer payments and cash payments.</span></span>

## <a name="set-up-for-cash-management-for-pos"></a><span data-ttu-id="c4e2e-121">Nastavení správy hotovosti pro POS</span><span class="sxs-lookup"><span data-stu-id="c4e2e-121">Set up for cash management for POS</span></span>

<span data-ttu-id="c4e2e-122">Následující postup nastavení je nutné dokončit před použitím řízení hotovosti:</span><span class="sxs-lookup"><span data-stu-id="c4e2e-122">You must complete the following setup procedure before you use cash management:</span></span>

- <span data-ttu-id="c4e2e-123">Nastavení metody platby pro každý typ platby, kterou přijímá prodejce na stránce **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-123">Set up a payment method for each payment type that the retailer accepts on the **Payment methods** page.</span></span> <span data-ttu-id="c4e2e-124">Pro zaúčtování transakcí v POS můžete použít různé metody platby.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-124">You can use different payment methods for posting transactions in POS.</span></span> <span data-ttu-id="c4e2e-125">Další informace o metodách platby naleznete v tématu [Metody platby](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).</span><span class="sxs-lookup"><span data-stu-id="c4e2e-125">For more information about payment methods, see [Payment methods](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).</span></span>
- <span data-ttu-id="c4e2e-126">Nastavení parametrů pro hotovostní operace.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-126">Set up parameters for cash operations.</span></span>
- <span data-ttu-id="c4e2e-127">Nastavení metody platby pro platby v hotovosti v obchodě.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-127">Set up a payment method for cash payments in a store.</span></span>

### <a name="set-up-parameters-for-cash-operations"></a><span data-ttu-id="c4e2e-128">Nastavení parametrů pro hotovostní operace</span><span class="sxs-lookup"><span data-stu-id="c4e2e-128">Set up parameters for cash operations</span></span>

<span data-ttu-id="c4e2e-129">Můžete nastavit parametry pro vytvoření a zaúčtování hotovostních transakcí v Commerce.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-129">You can set up parameters to create and post cash transactions in Commerce.</span></span> <span data-ttu-id="c4e2e-130">K zaúčtování transakcí v POS můžete použít pokladní deníky a deníky plateb odběratelů nebo hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-130">You can use cash payment journals, customer payment journals, or general journals to post sales transactions and payment transactions in the POS.</span></span> <span data-ttu-id="c4e2e-131">Lze seskupit transakce, které mají stejné vlastnosti při zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-131">You can aggregate transactions that have the same properties when you post a statement.</span></span>

1. <span data-ttu-id="c4e2e-132">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="c4e2e-133">V levém podokně klikněte na **Zaúčtování**.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-133">In the left pane, click **Posting**.</span></span>
2. <span data-ttu-id="c4e2e-134">V oblasti **Zaúčtování** na pevné záložce **Agregace** nastavte možnost **Úhrada – odebrat/plovoucí** na **Ano** pro agregaci odebrání transakcí úhrad nebo transakcí plovoucí položky, které jsou přidruženy k řádku výkazu při zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-134">In the **Posting** area, on the **Aggregation** FastTab, set **Tender remove/float** to **Yes** to aggregate the remove tender transactions or float entry transactions that are associated with a statement line when you post the statement.</span></span> <span data-ttu-id="c4e2e-135">Transakce odebrání úhrady je vytvořena při výběru hotovosti ze zásuvky s hotovostí POS.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-135">A remove tender transaction is created when you withdraw cash from the POS cash drawer.</span></span> <span data-ttu-id="c4e2e-136">Transakce plovoucí položky je vytvořena při vložení hotovosti do zásuvky s hotovostí POS.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-136">A float entry transaction is created when you deposit cash in the POS cash drawer.</span></span>
3. <span data-ttu-id="c4e2e-137">Aktivujte jednotlivé parametry uvedené níže pro seskupení transakcí, které jsou přidruženy k řádku výkazu při zaúčtování výkazu:</span><span class="sxs-lookup"><span data-stu-id="c4e2e-137">Activate the individual parameters listed below to aggregate the transactions that are associated with a statement line when you post the statement:</span></span>

    - <span data-ttu-id="c4e2e-138">**Odvod do banky** – Souhrnné bankovní transakce.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-138">**Bank drop** – Aggregate bank transactions.</span></span>
    - <span data-ttu-id="c4e2e-139">**Odvod do trezoru** – Souhrnné transakce trezoru.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-139">**Safe drop** – Aggregate safe transactions.</span></span>
    - <span data-ttu-id="c4e2e-140">**Transakce příjmů/výdajů** – Souhrnné transakce příjmů nebo transakce výdajů.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-140">**Income/Expense transactions** – Aggregate income transactions or expense transactions.</span></span>
    - <span data-ttu-id="c4e2e-141">**Transakce dokladu** – Souhrnné transakce dokladu.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-141">**Voucher transactions** – Aggregate voucher transactions.</span></span>
    - <span data-ttu-id="c4e2e-142">**Platby odběratele** – Souhrnné platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-142">**Customer payments** – Aggregate customer payments.</span></span>
    - <span data-ttu-id="c4e2e-143">**Prodeje a vrácení** – Souhrnné transakce prodeje a vrácení.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-143">**Sales and returns** – Aggregate sales and returns transactions.</span></span>

4. <span data-ttu-id="c4e2e-144">Na pevné záložce **Platby** zvolte výchozí název deníku pro následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="c4e2e-144">On the **Payments** FastTab, select a default journal name for the following options:</span></span>

    - <span data-ttu-id="c4e2e-145">**Deník plateb odběratele** - Tento deník se používá k zaúčtování plateb odběratele.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-145">**Customer payment journal** – This journal is used to post customer payments.</span></span>
    - <span data-ttu-id="c4e2e-146">**Deník plateb v hotovosti** - Tento deník se používá k zaúčtování plateb v hotovosti.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-146">**Cash payment journal** – This journal is used to post cash payments.</span></span>
    - <span data-ttu-id="c4e2e-147">**Hlavní deník** – Tento deník se používá k zaúčtování jiných transakcí než hotovostních plateb a plateb odběratele.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-147">**General journal** – This journal is used to post transactions other than cash payments and customer payments.</span></span>

### <a name="set-up-a-payment-method-for-cash-payments-in-a-store"></a><span data-ttu-id="c4e2e-148">Nastavení metody platby pro platby v hotovosti v obchodě</span><span class="sxs-lookup"><span data-stu-id="c4e2e-148">Set up a payment method for cash payments in a store</span></span>

<span data-ttu-id="c4e2e-149">Následující postup slouží k nastavení metody platby pro platby v hotovosti v obchodě.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-149">Use the following procedure to set up a payment method for cash payments in a store.</span></span>

1. <span data-ttu-id="c4e2e-150">Přejděte na **Retail a Commerce \> Kanály \> Obchody \> Všechny obchody**.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-150">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
2. <span data-ttu-id="c4e2e-151">Na stránce se seznamem **Všechny obchody** vyberte obchod, pro který chcete nastavit platební metodu.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-151">On the **All stores** list page, select the store to set up a payment method for.</span></span>
3. <span data-ttu-id="c4e2e-152">Na panelu akcí na kartě **Nastavení** ve skupině **Nastavení** klikněte na možnost **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-152">On the Action Pane, on the **Set up** tab, in the **Set up** group, click **Payment methods**.</span></span>
4. <span data-ttu-id="c4e2e-153">Na stránce **Metody platby** vytvořte nebo vyberte metodu platby.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-153">On the **Payment method** page, create or select a payment method.</span></span>
5. <span data-ttu-id="c4e2e-154">Na pevné záložce **Zaúčtování** ve skupině polí **Účet** v poli **Typ účtu** vyberte **Pokladní účet**.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-154">On the **Posting** FastTab, in the **Account** field group, in the **Account type** field, select **Cash account**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4e2e-155">Můžete vybrat **Pokladní účet** v poli **Typ účtu** pouze tehdy, pokud zvolíte **Normální** nebo **Úhrady odebrat/plovoucí** v poli **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-155">You can select **Cash account** in the **Account type** field only if you select **Normal** or **Tender remove/float** in the **Function** field.</span></span>

6. <span data-ttu-id="c4e2e-156">V poli **Číslo účtu** vyberte číslo hotovostního účtu pro metodu platby.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-156">In the **Account number** field, select a cash account number for the payment method.</span></span>
7. <span data-ttu-id="c4e2e-157">Ve skupině polí **Úhrada - odebrat/plovoucí** v poli **Protiúčet** vyberte protiúčet pro zaúčtování odebrané úhrady nebo transakce odvodu pro metodu platby.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-157">In the **Tender remove/float** field group, in the **Offset account** field, select the offset account to post remove tender or float entry transactions for the payment method.</span></span>

> [!NOTE]
> <span data-ttu-id="c4e2e-158">Je nutné nastavit protiúčty jak pro metodu platby pro úhrady hotovosti, tak pro odebrání úhrady nebo metodu platby plovoucí položky pro obchod.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-158">You must set up offset accounts for both the cash tender payment method and the remove tender or float entry payment method for a store.</span></span> <span data-ttu-id="c4e2e-159">Tím se vytvoří vyrovnané položky hlavní knihy pro odebrání úhrady nebo transakce plovoucí položky.</span><span class="sxs-lookup"><span data-stu-id="c4e2e-159">This creates balanced general ledger entries for remove tender or float entry transactions.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]