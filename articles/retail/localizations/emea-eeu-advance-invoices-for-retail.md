---
title: Zálohové faktury pro Retail pro východní Evropu
description: Toto téma vysvětluje, jak nastavit oznámení zálohách v maloobchodu pro východní Evropu.
author: epopov
manager: annbe
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0dd49d6fc3294342ebc13d16eb871d0b20229b0c
ms.sourcegitcommit: 2cf5498098e7a5ade1c16eac6df26bc98e4565cd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2019
ms.locfileid: "760700"
---
# <a name="advance-invoices-for-retail-for-eastern-europe"></a><span data-ttu-id="8fd3f-103">Zálohové faktury pro Retail pro východní Evropu</span><span class="sxs-lookup"><span data-stu-id="8fd3f-103">Advance invoices for Retail for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fd3f-104">Informace v tomto tématu platí pro východoevropskou lokalizaci a souvisí s maloobchodem.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-104">The information in this topic applies to the Eastern European localization and is specific to the retail industry.</span></span>

<span data-ttu-id="8fd3f-105">Pro Polsko, Maďarsko a Českou republiku platí, že při přijetí zálohy od odběratele pomocí pokladního místa (POS), musí být záloha zaregistrována pro daňové účely a musí být generován a vytištěn zálohový doklad obsahující částku zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-105">For Poland, Hungary, and Czech Republic, when a prepayment is received from a customer via Point of Sale (POS), the prepayment must be registered for tax purposes, and it's required to generate and print an advance invoice document that includes the prepayment amount.</span></span> <span data-ttu-id="8fd3f-106">Kromě toho pro Polsko platí, že musí být transakce zálohové faktury zaúčtovány v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-106">Additionally, for Poland, advance invoice transactions must be posted in the general ledger.</span></span>

<span data-ttu-id="8fd3f-107">Po konečném zaúčtování faktury faktury prodejní objednávky by měl konečný doklad obsahovat zálohovou fakturu a měly by být uvedeny všechny zálohy.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-107">When the invoice for the sales order is finally posted, the final document should include the advance invoice, and any prepayments should be indicated.</span></span>

<span data-ttu-id="8fd3f-108">Pokud prodejní objednávky generujete z modulu Pohledávky, musíte ručně generovat zálohové faktury pomocí kroků uvedených v části [Zálohové faktury pro východní Evropu](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span><span class="sxs-lookup"><span data-stu-id="8fd3f-108">If you generate sales orders from Accounts receivable, you must manually generate advance invoices by using the procedure in [Advance invoices for Eastern Europe](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span></span> <span data-ttu-id="8fd3f-109">Pokud generujete prodejní objednávky prostřednictvím POS systém vytvoří a zaúčtuje zálohové faktury za vás.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-109">If you generate sales orders via POS, the system generates and posts the advance invoices for you.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="8fd3f-110">Podporované scénáře</span><span class="sxs-lookup"><span data-stu-id="8fd3f-110">Supported scenarios</span></span>

<span data-ttu-id="8fd3f-111">Podporovány jsou následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="8fd3f-111">The following scenarios are supported:</span></span>

- <span data-ttu-id="8fd3f-112">Vytvořte a zaúčtujte zálohovou fakturu.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-112">Create and post an advance invoice.</span></span>
- <span data-ttu-id="8fd3f-113">Změňte částku vkladu.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-113">Modify a deposit amount.</span></span> <span data-ttu-id="8fd3f-114">Pokud se zákazník rozhodne zvýšit výši vkladu, bude vystavena další zálohová faktura.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-114">If a customer decides to increase the amount of a deposit, an additional advance invoice is issued.</span></span> <span data-ttu-id="8fd3f-115">Pro všechny ostatní změny částky vkladu (pokud je například zakázka odběratele upravena) je vytvořen dobropis pro zálohovou fakturu, která již byla vygenerována a je generována a zaúčtována nová zálohová faktura pro opravenou částku.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-115">For all other changes to the deposit amount (for example, if a customer order is edited), a credit note is created for the advance invoice that was previously generated, and a new advance invoice is generated and posted for the corrected amount.</span></span>
- <span data-ttu-id="8fd3f-116">Zrušte prodejní objednávku, ke které jsou připojené zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-116">Cancel a sales order that has linked advance invoices.</span></span> <span data-ttu-id="8fd3f-117">V takovém případě je vytvořen dobropis zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-117">In this case, a credit note is created for the advance invoice.</span></span>
- <span data-ttu-id="8fd3f-118">Zaúčtujte fakturu prodejní objednávky, ke které jsou připojené zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-118">Post a sales order invoice that has linked advance invoices.</span></span> <span data-ttu-id="8fd3f-119">Zálohová faktura, která je spojena s prodejní objednávkou, je stornována na množství na prodejní faktuře.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-119">The advance invoice that is linked to a sales order is reversed for the amount of the sales invoice.</span></span> <span data-ttu-id="8fd3f-120">Transakce zálohové faktury jsou vypořádány s transakcemi storna zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-120">The advance invoice transactions are settled with advance invoice reversal transactions.</span></span>

## <a name="set-up-advance-invoices"></a><span data-ttu-id="8fd3f-121">Nastavení zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="8fd3f-121">Set up advance invoices</span></span>

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a><span data-ttu-id="8fd3f-122">Zapnutí funkce vytváření zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="8fd3f-122">Turn on the functionality for creating advance invoices</span></span>

1. <span data-ttu-id="8fd3f-123">Přejděte na možnost **Maloobchod \> Nastavení centrály \> Parametry \> Parametry maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-123">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span>
2. <span data-ttu-id="8fd3f-124">Na kartě **Objednávky odběratele** na pevné záložce **Objednávka** nastavte možnost **Vytvořit zálohovou fakturu pro vklad** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-124">On the **Customer orders** tab, on the **Order** FastTab, set the **Create advance invoice for deposit** option to **Yes**.</span></span>

### <a name="define-the-parameters-for-posting-advance-invoices"></a><span data-ttu-id="8fd3f-125">Definování parametrů zaúčtování zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="8fd3f-125">Define the parameters for posting advance invoices</span></span>

1. <span data-ttu-id="8fd3f-126">Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-126">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="8fd3f-127">Na kartě **Aktualizace** na pevné záložce **Zálohová faktura** nastavte pole **Profil zaúčtování**, **Skupina daně z prodeje** a **Skupina daně z prodeje** položky.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-127">On the **Updates** tab, on the **Advance invoice** FastTab, set the **Posting profile**, **Sales tax group**, and **Item sales tax group** fields.</span></span> <span data-ttu-id="8fd3f-128">Pokud jsou tato pole nastavena správně, zálohová faktura se zaúčtuje.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-128">If these fields are set correctly, the advance invoice will be posted.</span></span> <span data-ttu-id="8fd3f-129">Jestliže tato pole nejsou nastavena, faktury nebudou zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-129">If these fields aren't set, advance invoices won't be posted.</span></span>

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a><span data-ttu-id="8fd3f-130">Vypnutí zaúčtování DPH na zálohovém dokladu deníku</span><span class="sxs-lookup"><span data-stu-id="8fd3f-130">Turn off posting of the Sales tax on prepayment journal voucher</span></span>

<span data-ttu-id="8fd3f-131">Pokud je zapnuto zaúčtování zálohových faktur, nesmí být zaúčtována DPH na zálohovém dokladu deníku.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-131">The Sales tax on prepayment journal voucher must not be posted if advance invoice posting is turned on.</span></span> <span data-ttu-id="8fd3f-132">Chcete-li ověřit, že tento požadavek je splněn, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-132">To verify that this requirement is met, follow these steps.</span></span>

1. <span data-ttu-id="8fd3f-133">Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-133">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="8fd3f-134">Na kartě **Hlavní kniha a DPH** se na pevné záložce **Platba** ujistěte, že jsou následující pole prázdná nebo nastavená na **Ne**:</span><span class="sxs-lookup"><span data-stu-id="8fd3f-134">On the **Ledger and sales tax** tab, on the **Payment** FastTab, make sure that the following fields are blank or set to **No**:</span></span>

    - <span data-ttu-id="8fd3f-135">DPH na zálohovém dokladu deníku</span><span class="sxs-lookup"><span data-stu-id="8fd3f-135">Sales tax on prepayment journal voucher</span></span>
    - <span data-ttu-id="8fd3f-136">Účetní profil se zálohovým dokladem deníku</span><span class="sxs-lookup"><span data-stu-id="8fd3f-136">Posting profile with prepayment journal voucher</span></span>
    - <span data-ttu-id="8fd3f-137">Skupina daně pro zálohy</span><span class="sxs-lookup"><span data-stu-id="8fd3f-137">Tax group for prepayment</span></span>
    - <span data-ttu-id="8fd3f-138">Skupina DPH u položky</span><span class="sxs-lookup"><span data-stu-id="8fd3f-138">Item Sales tax group</span></span>

## <a name="print-advance-invoices"></a><span data-ttu-id="8fd3f-139">Tisk zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="8fd3f-139">Print advance invoices</span></span>

<span data-ttu-id="8fd3f-140">Zálohové faktury můžete tisknout z POS na tiskárně Microsoft Windows, která je připojena k hardwarové stanici.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-140">You can print advance invoices from POS on a Microsoft Windows printer that is connected to the hardware station.</span></span> <span data-ttu-id="8fd3f-141">Existují dvě možnosti tisku zálohové faktury z POS:</span><span class="sxs-lookup"><span data-stu-id="8fd3f-141">There are two options for printing an advance invoice from POS:</span></span>

- <span data-ttu-id="8fd3f-142">**Tisk zálohové faktury po uzavření transakce v POS.**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-142">**Print an advance invoice after a transaction is concluded in POS.**</span></span> <span data-ttu-id="8fd3f-143">Tato možnost se objeví automaticky, pokud byla vygenerovaná zálohová faktura a správně nastavena tiskárna systému Windows.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-143">This option occurs automatically if an advance invoice was generated and a Windows printer was correctly set up.</span></span> <span data-ttu-id="8fd3f-144">V takovém případě se vytiskne pouze poslední zálohová faktura, která je propojena s objednávkou odběratele.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-144">In this case, only the last advance invoice that is linked to the customer order is printed.</span></span>
- <span data-ttu-id="8fd3f-145">**Znovu vytisknout zálohovou fakturu z deníku transakce.**</span><span class="sxs-lookup"><span data-stu-id="8fd3f-145">**Reprint an advance invoice from the transaction journal.**</span></span> <span data-ttu-id="8fd3f-146">Vyberte **zobrazit deník** pro otevření deníku transakcí, vyhledejte objednávku odběratele a poté vyberte **Tisk zálohové faktury**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-146">Select **Show journal** to open the transactions journal, find the customer order, and then select **Print Advance invoice**.</span></span> <span data-ttu-id="8fd3f-147">V takovém případě se vytisknou všechny zálohové faktury, které jsou propojeny s objednávkou odběratele.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-147">In this case, all advance invoices that are linked to the customer order are printed.</span></span>

### <a name="set-up-a-windows-printer"></a><span data-ttu-id="8fd3f-148">Nastavení tiskárny Windows</span><span class="sxs-lookup"><span data-stu-id="8fd3f-148">Set up a Windows printer</span></span>

<span data-ttu-id="8fd3f-149">Tento postup slouží k povolení tisku dokumentů z POS na tiskárně Windows, která je připojena k hardwarové stanici dokumentů.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-149">Follow these steps to enable documents to be printed from POS on a Windows printer that is connected to the hardware station.</span></span>

1. <span data-ttu-id="8fd3f-150">Přejděte na **Maloobchod \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-150">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
2. <span data-ttu-id="8fd3f-151">Vyberte hardwarový profil vztahující se k obchodu, kde se používá tiskárna.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-151">Select a hardware profile that is related to the store where the printer is used.</span></span>
3. <span data-ttu-id="8fd3f-152">Aktualizujte nastavení v části **Tiskárna** nebo **Tiskárna 2**:</span><span class="sxs-lookup"><span data-stu-id="8fd3f-152">In either the **Printer** section or the **Printer 2** section, update the settings:</span></span>

    - <span data-ttu-id="8fd3f-153">V polo **Tiskárna** vyberte **Ovladač systému Windows**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-153">In the **Printer** field, select **Windows driver**.</span></span>
    - <span data-ttu-id="8fd3f-154">Do pole **Název zařízení** zadejte název tiskárny.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-154">In the **Device name** field, enter the name of the printer.</span></span>

4. <span data-ttu-id="8fd3f-155">Přejděte do nabídky **Maloobchodní prodej \> Maloobchodní IT \> Distribuční plán**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-155">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="8fd3f-156">Vyberte úlohu **1090** a klikněte na tlačítko **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="8fd3f-156">Select job **1090**, and then select **Run now**.</span></span>
