---
title: Zálohy zákazníků
description: Toto téma vysvětluje, jak nastavit a zpracovat zálohy zákazníků (známé také jako vklady zákazníků).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019413"
---
# <a name="customer-prepayments"></a><span data-ttu-id="70dfe-103">Zálohy zákazníků</span><span class="sxs-lookup"><span data-stu-id="70dfe-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70dfe-104">Zálohy zákazníka se používají, když obdržíte platbu od zákazníka, ale neexistuje žádná faktura, proti které lze platbu uhradit.</span><span class="sxs-lookup"><span data-stu-id="70dfe-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="70dfe-105">Tyto typy plateb se také označují jako vklady zákazníků.</span><span class="sxs-lookup"><span data-stu-id="70dfe-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="70dfe-106">Proces nastavení a práce se zálohami zákazníkům se skládá z následujících základních kroků.</span><span class="sxs-lookup"><span data-stu-id="70dfe-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="70dfe-107">Vytvořte účetní profil zákazníka pro platby záloh.</span><span class="sxs-lookup"><span data-stu-id="70dfe-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="70dfe-108">Nastavte parametr **Účetní profil se zálohovým dokladem deníku**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="70dfe-109">Vytvořte deník plateb od zákazníka a zaškrtněte políčko **Zálohový doklad deníku** na každém řádku.</span><span class="sxs-lookup"><span data-stu-id="70dfe-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="70dfe-110">Zaúčtovat deník plateb odběratele</span><span class="sxs-lookup"><span data-stu-id="70dfe-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="70dfe-111">Po vygenerování faktury vyrovnejte zálohovou platbu pomocí stránky **Vypořádat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="70dfe-112">Vytvoření účetního profilu zákazníka pro platby záloh</span><span class="sxs-lookup"><span data-stu-id="70dfe-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="70dfe-113">Obvykle, když přijmete zálohy nebo vklady od svých zákazníků před dodáním zboží nebo služeb nebo předtím, než ve vašem systému bude existovat faktura, budete chtít zaznamenat hotovost jako závazek namísto majetku v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="70dfe-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="70dfe-114">Požadavky na zaznamenávání těchto částek do hlavní knihy se však mohou lišit v závislosti na vaší zemi nebo oblasti.</span><span class="sxs-lookup"><span data-stu-id="70dfe-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="70dfe-115">Nezapomeňte se proto poradit se svými účetními ohledně veškerých platných místních předpisů.</span><span class="sxs-lookup"><span data-stu-id="70dfe-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="70dfe-116">Obecně platí, že proces vytváření profilu účtování, který lze použít pro platby předem, je stejný jako proces vytváření dalších profilů účtování.</span><span class="sxs-lookup"><span data-stu-id="70dfe-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="70dfe-117">Primárním rozdílem je hlavní účet, který vyberete v poli **Souhrnný účet**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="70dfe-118">Další informace naleznete v tématu [Účetní profily zákazníka](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="70dfe-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="70dfe-119">Definování parametrů záloh pro zákazníka</span><span class="sxs-lookup"><span data-stu-id="70dfe-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="70dfe-120">Existují dva hlavní parametry závazků, které musíte vzít v úvahu při konfiguraci systému pro platby záloh zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="70dfe-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="70dfe-121">Při konfiguraci parametrů postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="70dfe-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="70dfe-122">Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="70dfe-123">Volitelné: Na kartě **Hlavní kniha a DPH** na pevné záložce **Platba** nastavte možnost **Daň z prodeje u zálohového dokladu deníku** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="70dfe-124">V poli **Profil zaúčtování s poukazem na zálohový doklad deníku** vyberte profil účtování zákazníka, který se má použít při zaúčtování záloh zákazníků.</span><span class="sxs-lookup"><span data-stu-id="70dfe-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="70dfe-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="70dfe-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="70dfe-126">Vytvoření zálohových poukazů zákazníka</span><span class="sxs-lookup"><span data-stu-id="70dfe-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="70dfe-127">Při vytváření deníku plateb pro zákazníka musíte pro každou platbu předem nastavit možnost **Zálohový doklad deníku** na **Ano** na stránce **Deník plateb zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="70dfe-128">Pokud chcete zálohu zákazníka, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="70dfe-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="70dfe-129">Přejděte na **Pohledávky \> Platby \> Deník plateb zákazníkovi**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="70dfe-130">Zvolte **Nový** pro vytvoření deníku.</span><span class="sxs-lookup"><span data-stu-id="70dfe-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="70dfe-131">V poli **Název** vyberte název deníku, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="70dfe-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="70dfe-132">Pokud jste v předchozím postupu nastavili **Daň z obratu na zálohovém dokladu deníku** na **Ano**, musíte vybrat název deníku, kde he vybrán parametr **Částka zahrnuje daň z obratu**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="70dfe-133">Volitelné: Do pole **Popis** zadejte podrobný popis.</span><span class="sxs-lookup"><span data-stu-id="70dfe-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="70dfe-134">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-134">Select **Lines**.</span></span>
6. <span data-ttu-id="70dfe-135">Pokud prázdný řádek neexistuje, vyberte **Nový** pro vytvoření řádku.</span><span class="sxs-lookup"><span data-stu-id="70dfe-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="70dfe-136">Do pole **Datum** zadejte datum, kdy má být záloha zaúčtována.</span><span class="sxs-lookup"><span data-stu-id="70dfe-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="70dfe-137">V poli **Účet** vyberte zákazníka pro zálohu.</span><span class="sxs-lookup"><span data-stu-id="70dfe-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="70dfe-138">Volitelné: Do pole **Popis** zadejte podrobný popis transakce.</span><span class="sxs-lookup"><span data-stu-id="70dfe-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="70dfe-139">V poli **Kredit** zadejte částku zálohy.</span><span class="sxs-lookup"><span data-stu-id="70dfe-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="70dfe-140">V poli **Typ účtu pro protiúčet** vyberte účet pro vyrovnání platby.</span><span class="sxs-lookup"><span data-stu-id="70dfe-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="70dfe-141">Vyberte například banku nebo hlavní účet, na který chcete platbu zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="70dfe-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="70dfe-142">V poli **Metoda platby** vyberte metodu platby zákazníka.</span><span class="sxs-lookup"><span data-stu-id="70dfe-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="70dfe-143">Na kartě **Způsob platby** nastavte možnost **zálohový doklad deníku** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="70dfe-144">Opakujte kroky 7 až 13 pro každou další platbu předem, která musí být zaúčtována.</span><span class="sxs-lookup"><span data-stu-id="70dfe-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="70dfe-145">Vyberte **Zaúčtovat** pro dokončení deníku.</span><span class="sxs-lookup"><span data-stu-id="70dfe-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="70dfe-146">Vyrovnání záloh s fakturami</span><span class="sxs-lookup"><span data-stu-id="70dfe-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="70dfe-147">V pracovním prostoru **Platby zákazníkům** můžete snadno vyhledávat a vypořádávat platby, které nebyly zcela vypořádány.</span><span class="sxs-lookup"><span data-stu-id="70dfe-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="70dfe-148">V řídicím panelu **Domů** vyberte dlaždici **Platby zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="70dfe-149">V sekci **Zákaznické transakce** na kartě **Platby nejsou vypořádány** vyhledejte a vyberte platbu k vypořádání.</span><span class="sxs-lookup"><span data-stu-id="70dfe-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="70dfe-150">Vyberte **Vyrovnat transakce**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="70dfe-151">Zaškrtněte políčko **Označit** pro fakturu a platbu, která bude vypořádána.</span><span class="sxs-lookup"><span data-stu-id="70dfe-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="70dfe-152">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="70dfe-152">Select **Post**.</span></span>

<span data-ttu-id="70dfe-153">Další informace o tom, jak vypořádat otevřené transakce, najdete v části [Přehled vyrovnání](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="70dfe-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
