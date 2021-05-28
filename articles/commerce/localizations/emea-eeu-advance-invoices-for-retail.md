---
title: Zálohové faktury pro Commerce pro východní Evropu
description: Toto téma vysvětluje, jak nastavit oznámení zálohách v Commerce pro východní Evropu.
author: epopov
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7771dfb9d9aa6dc87ef9eaee078c45ea66a5e143
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020289"
---
# <a name="advance-invoices-for-commerce-for-eastern-europe"></a><span data-ttu-id="f099a-103">Zálohové faktury pro Commerce pro východní Evropu</span><span class="sxs-lookup"><span data-stu-id="f099a-103">Advance invoices for Commerce for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f099a-104">Informace v tomto tématu platí pro východoevropskou lokalizaci a souvisí s obchodem.</span><span class="sxs-lookup"><span data-stu-id="f099a-104">The information in this topic applies to the Eastern European localization and is specific to the commerce industry.</span></span>

<span data-ttu-id="f099a-105">Pro Polsko, Maďarsko a Českou republiku platí, že při přijetí zálohy od odběratele pomocí pokladního místa (POS), musí být záloha zaregistrována pro daňové účely a musí být generován a vytištěn zálohový doklad obsahující částku zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="f099a-105">For Poland, Hungary, and Czech Republic, when a prepayment is received from a customer via Point of Sale (POS), the prepayment must be registered for tax purposes, and it's required to generate and print an advance invoice document that includes the prepayment amount.</span></span> <span data-ttu-id="f099a-106">Kromě toho pro Polsko platí, že musí být transakce zálohové faktury zaúčtovány v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="f099a-106">Additionally, for Poland, advance invoice transactions must be posted in the general ledger.</span></span>

<span data-ttu-id="f099a-107">Po konečném zaúčtování faktury faktury prodejní objednávky by měl konečný doklad obsahovat zálohovou fakturu a měly by být uvedeny všechny zálohy.</span><span class="sxs-lookup"><span data-stu-id="f099a-107">When the invoice for the sales order is finally posted, the final document should include the advance invoice, and any prepayments should be indicated.</span></span>

<span data-ttu-id="f099a-108">Pokud prodejní objednávky generujete z modulu Pohledávky, musíte ručně generovat zálohové faktury pomocí kroků uvedených v části [Zálohové faktury pro východní Evropu](/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span><span class="sxs-lookup"><span data-stu-id="f099a-108">If you generate sales orders from Accounts receivable, you must manually generate advance invoices by using the procedure in [Advance invoices for Eastern Europe](/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span></span> <span data-ttu-id="f099a-109">Pokud generujete prodejní objednávky prostřednictvím POS systém vytvoří a zaúčtuje zálohové faktury za vás.</span><span class="sxs-lookup"><span data-stu-id="f099a-109">If you generate sales orders via POS, the system generates and posts the advance invoices for you.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="f099a-110">Podporované scénáře</span><span class="sxs-lookup"><span data-stu-id="f099a-110">Supported scenarios</span></span>

<span data-ttu-id="f099a-111">Podporovány jsou následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="f099a-111">The following scenarios are supported:</span></span>

- <span data-ttu-id="f099a-112">Vytvořte a zaúčtujte zálohovou fakturu.</span><span class="sxs-lookup"><span data-stu-id="f099a-112">Create and post an advance invoice.</span></span>
- <span data-ttu-id="f099a-113">Změňte částku vkladu.</span><span class="sxs-lookup"><span data-stu-id="f099a-113">Modify a deposit amount.</span></span> <span data-ttu-id="f099a-114">Pokud se zákazník rozhodne zvýšit výši vkladu, bude vystavena další zálohová faktura.</span><span class="sxs-lookup"><span data-stu-id="f099a-114">If a customer decides to increase the amount of a deposit, an additional advance invoice is issued.</span></span> <span data-ttu-id="f099a-115">Pro všechny ostatní změny částky vkladu (pokud je například zakázka odběratele upravena) je vytvořen dobropis pro zálohovou fakturu, která již byla vygenerována a je generována a zaúčtována nová zálohová faktura pro opravenou částku.</span><span class="sxs-lookup"><span data-stu-id="f099a-115">For all other changes to the deposit amount (for example, if a customer order is edited), a credit note is created for the advance invoice that was previously generated, and a new advance invoice is generated and posted for the corrected amount.</span></span>
- <span data-ttu-id="f099a-116">Zrušte prodejní objednávku, ke které jsou připojené zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="f099a-116">Cancel a sales order that has linked advance invoices.</span></span> <span data-ttu-id="f099a-117">V takovém případě je vytvořen dobropis zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="f099a-117">In this case, a credit note is created for the advance invoice.</span></span>
- <span data-ttu-id="f099a-118">Zaúčtujte fakturu prodejní objednávky, ke které jsou připojené zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="f099a-118">Post a sales order invoice that has linked advance invoices.</span></span> <span data-ttu-id="f099a-119">Zálohová faktura, která je spojena s prodejní objednávkou, je stornována na množství na prodejní faktuře.</span><span class="sxs-lookup"><span data-stu-id="f099a-119">The advance invoice that is linked to a sales order is reversed for the amount of the sales invoice.</span></span> <span data-ttu-id="f099a-120">Transakce zálohové faktury jsou vypořádány s transakcemi storna zálohové faktury.</span><span class="sxs-lookup"><span data-stu-id="f099a-120">The advance invoice transactions are settled with advance invoice reversal transactions.</span></span>

## <a name="set-up-advance-invoices"></a><span data-ttu-id="f099a-121">Nastavení zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="f099a-121">Set up advance invoices</span></span>

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a><span data-ttu-id="f099a-122">Zapnutí funkce vytváření zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="f099a-122">Turn on the functionality for creating advance invoices</span></span>

1. <span data-ttu-id="f099a-123">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**.</span><span class="sxs-lookup"><span data-stu-id="f099a-123">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span>
2. <span data-ttu-id="f099a-124">Na kartě **Objednávky odběratele** na pevné záložce **Objednávka** nastavte možnost **Vytvořit zálohovou fakturu pro vklad** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f099a-124">On the **Customer orders** tab, on the **Order** FastTab, set the **Create advance invoice for deposit** option to **Yes**.</span></span>

### <a name="define-the-parameters-for-posting-advance-invoices"></a><span data-ttu-id="f099a-125">Definování parametrů zaúčtování zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="f099a-125">Define the parameters for posting advance invoices</span></span>

1. <span data-ttu-id="f099a-126">Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="f099a-126">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="f099a-127">Na kartě **Aktualizace** na pevné záložce **Zálohová faktura** nastavte pole **Profil zaúčtování**, **Skupina daně z prodeje** a **Skupina daně z prodeje** položky.</span><span class="sxs-lookup"><span data-stu-id="f099a-127">On the **Updates** tab, on the **Advance invoice** FastTab, set the **Posting profile**, **Sales tax group**, and **Item sales tax group** fields.</span></span> <span data-ttu-id="f099a-128">Pokud jsou tato pole nastavena správně, zálohová faktura se zaúčtuje.</span><span class="sxs-lookup"><span data-stu-id="f099a-128">If these fields are set correctly, the advance invoice will be posted.</span></span> <span data-ttu-id="f099a-129">Jestliže tato pole nejsou nastavena, faktury nebudou zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="f099a-129">If these fields aren't set, advance invoices won't be posted.</span></span>

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a><span data-ttu-id="f099a-130">Vypnutí zaúčtování DPH na zálohovém dokladu deníku</span><span class="sxs-lookup"><span data-stu-id="f099a-130">Turn off posting of the Sales tax on prepayment journal voucher</span></span>

<span data-ttu-id="f099a-131">Pokud je zapnuto zaúčtování zálohových faktur, nesmí být zaúčtována DPH na zálohovém dokladu deníku.</span><span class="sxs-lookup"><span data-stu-id="f099a-131">The Sales tax on prepayment journal voucher must not be posted if advance invoice posting is turned on.</span></span> <span data-ttu-id="f099a-132">Chcete-li ověřit, že tento požadavek je splněn, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f099a-132">To verify that this requirement is met, follow these steps.</span></span>

1. <span data-ttu-id="f099a-133">Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="f099a-133">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="f099a-134">Na kartě **Hlavní kniha a DPH** se na pevné záložce **Platba** ujistěte, že jsou následující pole prázdná nebo nastavená na **Ne**:</span><span class="sxs-lookup"><span data-stu-id="f099a-134">On the **Ledger and sales tax** tab, on the **Payment** FastTab, make sure that the following fields are blank or set to **No**:</span></span>

    - <span data-ttu-id="f099a-135">DPH na zálohovém dokladu deníku</span><span class="sxs-lookup"><span data-stu-id="f099a-135">Sales tax on prepayment journal voucher</span></span>
    - <span data-ttu-id="f099a-136">Účetní profil se zálohovým dokladem deníku</span><span class="sxs-lookup"><span data-stu-id="f099a-136">Posting profile with prepayment journal voucher</span></span>
    - <span data-ttu-id="f099a-137">Skupina daně pro zálohy</span><span class="sxs-lookup"><span data-stu-id="f099a-137">Tax group for prepayment</span></span>
    - <span data-ttu-id="f099a-138">Skupina DPH u položky</span><span class="sxs-lookup"><span data-stu-id="f099a-138">Item Sales tax group</span></span>

## <a name="print-advance-invoices"></a><span data-ttu-id="f099a-139">Tisk zálohových faktur</span><span class="sxs-lookup"><span data-stu-id="f099a-139">Print advance invoices</span></span>

<span data-ttu-id="f099a-140">Zálohové faktury můžete tisknout z POS na tiskárně Microsoft Windows, která je připojena k hardwarové stanici.</span><span class="sxs-lookup"><span data-stu-id="f099a-140">You can print advance invoices from POS on a Microsoft Windows printer that is connected to the hardware station.</span></span> <span data-ttu-id="f099a-141">Existují dvě možnosti tisku zálohové faktury z POS:</span><span class="sxs-lookup"><span data-stu-id="f099a-141">There are two options for printing an advance invoice from POS:</span></span>

- <span data-ttu-id="f099a-142">**Tisk zálohové faktury po uzavření transakce v POS.**</span><span class="sxs-lookup"><span data-stu-id="f099a-142">**Print an advance invoice after a transaction is concluded in POS.**</span></span> <span data-ttu-id="f099a-143">Tato možnost se objeví automaticky, pokud byla vygenerovaná zálohová faktura a správně nastavena tiskárna systému Windows.</span><span class="sxs-lookup"><span data-stu-id="f099a-143">This option occurs automatically if an advance invoice was generated and a Windows printer was correctly set up.</span></span> <span data-ttu-id="f099a-144">V takovém případě se vytiskne pouze poslední zálohová faktura, která je propojena s objednávkou odběratele.</span><span class="sxs-lookup"><span data-stu-id="f099a-144">In this case, only the last advance invoice that is linked to the customer order is printed.</span></span>
- <span data-ttu-id="f099a-145">**Znovu vytisknout zálohovou fakturu z deníku transakce.**</span><span class="sxs-lookup"><span data-stu-id="f099a-145">**Reprint an advance invoice from the transaction journal.**</span></span> <span data-ttu-id="f099a-146">Vyberte **zobrazit deník** pro otevření deníku transakcí, vyhledejte objednávku odběratele a poté vyberte **Tisk zálohové faktury**.</span><span class="sxs-lookup"><span data-stu-id="f099a-146">Select **Show journal** to open the transactions journal, find the customer order, and then select **Print Advance invoice**.</span></span> <span data-ttu-id="f099a-147">V takovém případě se vytisknou všechny zálohové faktury, které jsou propojeny s objednávkou odběratele.</span><span class="sxs-lookup"><span data-stu-id="f099a-147">In this case, all advance invoices that are linked to the customer order are printed.</span></span>

### <a name="set-up-a-windows-printer"></a><span data-ttu-id="f099a-148">Nastavení tiskárny Windows</span><span class="sxs-lookup"><span data-stu-id="f099a-148">Set up a Windows printer</span></span>

<span data-ttu-id="f099a-149">Tento postup slouží k povolení tisku dokumentů z POS na tiskárně Windows, která je připojena k hardwarové stanici dokumentů.</span><span class="sxs-lookup"><span data-stu-id="f099a-149">Follow these steps to enable documents to be printed from POS on a Windows printer that is connected to the hardware station.</span></span>

1. <span data-ttu-id="f099a-150">Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**.</span><span class="sxs-lookup"><span data-stu-id="f099a-150">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
2. <span data-ttu-id="f099a-151">Vyberte hardwarový profil vztahující se k obchodu, kde se používá tiskárna.</span><span class="sxs-lookup"><span data-stu-id="f099a-151">Select a hardware profile that is related to the store where the printer is used.</span></span>
3. <span data-ttu-id="f099a-152">Aktualizujte nastavení v části **Tiskárna** nebo **Tiskárna 2**:</span><span class="sxs-lookup"><span data-stu-id="f099a-152">In either the **Printer** section or the **Printer 2** section, update the settings:</span></span>

    - <span data-ttu-id="f099a-153">V polo **Tiskárna** vyberte **Ovladač systému Windows**.</span><span class="sxs-lookup"><span data-stu-id="f099a-153">In the **Printer** field, select **Windows driver**.</span></span>
    - <span data-ttu-id="f099a-154">Do pole **Název zařízení** zadejte název tiskárny.</span><span class="sxs-lookup"><span data-stu-id="f099a-154">In the **Device name** field, enter the name of the printer.</span></span>

4. <span data-ttu-id="f099a-155">Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="f099a-155">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="f099a-156">Vyberte úlohu **1090** a klikněte na tlačítko **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="f099a-156">Select job **1090**, and then select **Run now**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]