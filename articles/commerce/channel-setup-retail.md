---
title: Nastavení maloobchodního kanálu
description: Toto téma popisuje, jak vytvořit nový maloobchodní kanál v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937527"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="61210-103">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="61210-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61210-104">Toto téma popisuje, jak vytvořit nový maloobchodní kanál v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="61210-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="61210-105">Dynamics 365 Commerce podporuje více maloobchodních sítí.</span><span class="sxs-lookup"><span data-stu-id="61210-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="61210-106">Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody).</span><span class="sxs-lookup"><span data-stu-id="61210-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="61210-107">Každý kanál maloobchodu může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="61210-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="61210-108">Všechny tyto prvky je třeba nastavit pro maloobchod před vytvořením kanálu maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="61210-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="61210-109">Před vytvořením maloobchodního kanálu se ujistěte, že splňujete [předpoklady kanálu](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="61210-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="61210-110">Vytvořit a konfigurovat nový maloobchodní kanál</span><span class="sxs-lookup"><span data-stu-id="61210-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="61210-111">V navigačním podokně přejděte na **Moduly \> Kanály \> Obchody \> Všechny obchody**.</span><span class="sxs-lookup"><span data-stu-id="61210-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="61210-112">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="61210-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61210-113">Do pole **Název** zadejte název nového kanálu.</span><span class="sxs-lookup"><span data-stu-id="61210-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="61210-114">V poli **Číslo obchodu** zadejte jedinečné číslo obchodu.</span><span class="sxs-lookup"><span data-stu-id="61210-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="61210-115">Číslo může být alfanumerické s maximálně 10 znaky.</span><span class="sxs-lookup"><span data-stu-id="61210-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="61210-116">V rozevíracím seznamu **Právnícká osoba** zadejte příslušnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="61210-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="61210-117">Do rozevíracího seznamu **Sklad** zadejte příslušný sklad.</span><span class="sxs-lookup"><span data-stu-id="61210-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="61210-118">V poli **Uložené časové pásmo** vyberte příslušné časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="61210-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="61210-119">V rozevíracím seznamu **Skupina DPH** vyberte pro obchod příslušnou skupinu DPH.</span><span class="sxs-lookup"><span data-stu-id="61210-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="61210-120">V poli **Měna** vyberte příslušnou měnu.</span><span class="sxs-lookup"><span data-stu-id="61210-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="61210-121">V poli **Adresář odběratele** zadejte platný adresář.</span><span class="sxs-lookup"><span data-stu-id="61210-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="61210-122">Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="61210-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="61210-123">V poli **Funkční profil** vyberte funkční profil, pokud je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="61210-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="61210-124">V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.</span><span class="sxs-lookup"><span data-stu-id="61210-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="61210-125">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="61210-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="61210-126">V následujícím obrázku je znázorněno vytvoření nového maloobchodního kanálu.</span><span class="sxs-lookup"><span data-stu-id="61210-126">The following image shows the creation of a new retail channel.</span></span>

![Nový maloobchodní kanál](media/channel-setup-retail-1.png)

<span data-ttu-id="61210-128">Následující obrázek znázorňuje příklad maloobchodního kanálu.</span><span class="sxs-lookup"><span data-stu-id="61210-128">The following image shows an example retail channel.</span></span>

![Příklad maloobchodního kanálu](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="61210-130">Další nastavení</span><span class="sxs-lookup"><span data-stu-id="61210-130">Other settings</span></span>

<span data-ttu-id="61210-131">Existuje řada dalších volitelných nastavení, která lze nastavit v sekcích **Výkaz/uzávěrka** a **Různé** podle potřeb maloobchodního obchodu.</span><span class="sxs-lookup"><span data-stu-id="61210-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="61210-132">Kromě toho viz [Rozložení obrazovky pokladního místa (POS)](pos-screen-layouts.md) pro informace o nastavení výchozího rozvržení obrazovky v části **Rozložení obrazovky** a [Konfigurace a instalace Retail Hardware Station](retail-hardware-station-configuration-installation.md) pro informace o nastavení v části **Hardwarové stanice**.</span><span class="sxs-lookup"><span data-stu-id="61210-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="61210-133">Následující obrázek znázorňuje příklad konfigurace nastavení maloobchodního kanálu.</span><span class="sxs-lookup"><span data-stu-id="61210-133">The following image shows an example retail channel setup configuration.</span></span>

![Příklad konfigurace maloobchodní sítě](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="61210-135">Nastavení dodatečného kanálu</span><span class="sxs-lookup"><span data-stu-id="61210-135">Additional channel set up</span></span>

<span data-ttu-id="61210-136">Existují další položky, které je třeba nastavit pro kanál, který lze najít v podokně Akce v sekci **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="61210-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="61210-137">Další úkoly požadované pro nastavení online kanálu zahrnují nastavení způsobů plateb, výkazu hotovosti, způsobů dodání, účtu příjmů/výdajů a přiřazení skupiny plnění a trezorů.</span><span class="sxs-lookup"><span data-stu-id="61210-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="61210-138">Následující obrázek ukazuje další možnosti nastavení maloobchodních kanálů na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="61210-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Nastavení kanálu](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="61210-140">Nastavení metod platby</span><span class="sxs-lookup"><span data-stu-id="61210-140">Set up payment methods</span></span>

<span data-ttu-id="61210-141">Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="61210-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="61210-142">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="61210-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="61210-143">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="61210-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61210-144">V navigačním podokně vyberte požadovaný způsob platby.</span><span class="sxs-lookup"><span data-stu-id="61210-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="61210-145">V části **Obecné** zadejte **Název operace** a nakonfigurujte další požadovaná nastavení.</span><span class="sxs-lookup"><span data-stu-id="61210-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="61210-146">Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.</span><span class="sxs-lookup"><span data-stu-id="61210-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="61210-147">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="61210-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="61210-148">Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="61210-148">The following image shows an example of a cash payment method.</span></span>

![Příklad způsobů platby](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="61210-150">Nastavení výkazu hotovosti</span><span class="sxs-lookup"><span data-stu-id="61210-150">Set up cash declaration</span></span>

1. <span data-ttu-id="61210-151">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Výkaz hotovosti**.</span><span class="sxs-lookup"><span data-stu-id="61210-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="61210-152">V podokně akcí vyberte **Nový** a poté vytvořte všechny použitelné nominální hodnoty pro **Mince** a **Bankovky**.</span><span class="sxs-lookup"><span data-stu-id="61210-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="61210-153">Na následujícím obrázku je znázorněn příklad výkazu hotovosti.</span><span class="sxs-lookup"><span data-stu-id="61210-153">The following image shows an example of a cash declaration.</span></span>

![Nastavení výkazu hotovosti](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="61210-155">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="61210-155">Set up modes of delivery</span></span>

<span data-ttu-id="61210-156">Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v Podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="61210-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="61210-157">Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="61210-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="61210-158">V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="61210-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="61210-159">V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.</span><span class="sxs-lookup"><span data-stu-id="61210-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="61210-160">V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál.</span><span class="sxs-lookup"><span data-stu-id="61210-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="61210-161">Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.</span><span class="sxs-lookup"><span data-stu-id="61210-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="61210-162">Na následujícím obrázku je znázorněn příklad způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="61210-162">The following image shows an example of a mode of delivery.</span></span>

![Nastavit způsoby dodání](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="61210-164">Nastavit účet příjmů/výdajů</span><span class="sxs-lookup"><span data-stu-id="61210-164">Set up income/expense account</span></span>

<span data-ttu-id="61210-165">Chcete-li nastavit účet příjmů/výdajů, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="61210-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="61210-166">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Účet příjmů/výdajů**.</span><span class="sxs-lookup"><span data-stu-id="61210-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="61210-167">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="61210-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61210-168">V položce **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="61210-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="61210-169">V položce **Vyhledat název** zadejte název pro vyhledání.</span><span class="sxs-lookup"><span data-stu-id="61210-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="61210-170">V položce **Typ účtu** zadejte typ účtu.</span><span class="sxs-lookup"><span data-stu-id="61210-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="61210-171">V případě potřeby zadejte text pro **Řádek zprávy 1**, **Řádek zprávy 2**, **Text stvrzenky 1** a **Text stvrzenky 2**.</span><span class="sxs-lookup"><span data-stu-id="61210-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="61210-172">V položce **Zaúčtování** zadejte informace o zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="61210-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="61210-173">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="61210-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="61210-174">Následující obrázek znázorňuje příklad účtu příjmů/výdajů.</span><span class="sxs-lookup"><span data-stu-id="61210-174">The following image shows an example of an income/expense account.</span></span>

![Nastavit účty příjmů/výdajů](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="61210-176">Nastavení sekcí</span><span class="sxs-lookup"><span data-stu-id="61210-176">Set up sections</span></span>

<span data-ttu-id="61210-177">Chcete-li nastavit sekce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="61210-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="61210-178">V podokně akcí vyberte kartu **Nastavení** a poté klikněte na možnost **Sekce**.</span><span class="sxs-lookup"><span data-stu-id="61210-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="61210-179">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="61210-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61210-180">V položce **Číslo sekce** zadejte číslo sekce.</span><span class="sxs-lookup"><span data-stu-id="61210-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="61210-181">V položce **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="61210-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="61210-182">V položce **Velikost sekce** zadejte velikost sekce.</span><span class="sxs-lookup"><span data-stu-id="61210-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="61210-183">Konfigurujte další nastavení pro **Obecné** a **Prodejní statistiky** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="61210-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="61210-184">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="61210-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="61210-185">Nastavení přiřazení skupiny plnění</span><span class="sxs-lookup"><span data-stu-id="61210-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="61210-186">Chcete-li nastavit přiřazení skupiny plnění, postupujte podle následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="61210-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="61210-187">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.</span><span class="sxs-lookup"><span data-stu-id="61210-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="61210-188">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="61210-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61210-189">V rozevíracím seznamu **Skupina plnění** vyberte skupinu plnění.</span><span class="sxs-lookup"><span data-stu-id="61210-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="61210-190">V rozevíracím sezamu **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="61210-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="61210-191">V podokně akcí vyberte **Uložit**</span><span class="sxs-lookup"><span data-stu-id="61210-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="61210-192">Následující obrázek znázorňuje příklad nastavení přiřazení skupiny plnění.</span><span class="sxs-lookup"><span data-stu-id="61210-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Nastavení Přiřazení skupiny plnění](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="61210-194">Nastavit trezory</span><span class="sxs-lookup"><span data-stu-id="61210-194">Set up safes</span></span>

<span data-ttu-id="61210-195">Chcete-li nastavit trezory, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="61210-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="61210-196">V podokně akcí vyberte kartu **Nastavení** a poté klikněte na možnost **Trezory**.</span><span class="sxs-lookup"><span data-stu-id="61210-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="61210-197">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="61210-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61210-198">Zadejte název trezoru.</span><span class="sxs-lookup"><span data-stu-id="61210-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="61210-199">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="61210-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="61210-200">Zajištění jedinečných ID transakce</span><span class="sxs-lookup"><span data-stu-id="61210-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="61210-201">Počínaje verzí Commerce 10.0.18 jsou ID transakcí generovaná pro prodejní místo (POS) sekvenčně a zahrnují následující části:</span><span class="sxs-lookup"><span data-stu-id="61210-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="61210-202">Pevná část, což je zřetězení ID obchodu a ID terminálu.</span><span class="sxs-lookup"><span data-stu-id="61210-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="61210-203">Sekvenční část, což je číselná řada.</span><span class="sxs-lookup"><span data-stu-id="61210-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="61210-204">Konkrétně jde o formát *{store}-{terminal}-{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="61210-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="61210-205">Protože ID transakcí lze generovat v offline a online režimu, došlo k generování duplicitních ID transakcí.</span><span class="sxs-lookup"><span data-stu-id="61210-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="61210-206">Eliminace duplicitních ID transakcí vyžaduje mnoho manuálního opravování dat.</span><span class="sxs-lookup"><span data-stu-id="61210-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="61210-207">S verzí Commerce 10.0.19 byl aktualizován formát ID transakce, aby se odstranila sekvenční část, a místo toho se používá 13místné číslo generované výpočtem času v milisekundách od roku 1970.</span><span class="sxs-lookup"><span data-stu-id="61210-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="61210-208">S touto změnou je nový formát ID transakce *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="61210-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="61210-209">Tato aktualizace dělá ID transakce nesekvenční a zajišťuje, že ID transakcí jsou vždy jedinečná.</span><span class="sxs-lookup"><span data-stu-id="61210-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="61210-210">Transakční ID jsou určena pouze pro interní použití systému, takže se nevyžaduje, aby byla sekvenční.</span><span class="sxs-lookup"><span data-stu-id="61210-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="61210-211">Mnoho zemí však vyžaduje, aby identifikační čísla účtenek byla sekvenční.</span><span class="sxs-lookup"><span data-stu-id="61210-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="61210-212">Novou funkci formátu ID transakce lze povolit z pracovního prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="61210-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="61210-213">Chcete-li povolit použití nových ID transakcí, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="61210-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="61210-214">V centru Commerce přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="61210-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="61210-215">Filtrujte modul „retail a commerce“.</span><span class="sxs-lookup"><span data-stu-id="61210-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="61210-216">Vyhledejte název funkce **Aktivovat nové ID transakce, aby se zabránilo duplicitním ID transakcí**.</span><span class="sxs-lookup"><span data-stu-id="61210-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="61210-217">Vyberte funkci a poté v pravém podokně vyberte možnost **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="61210-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="61210-218">Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="61210-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="61210-219">Spusťte úlohy **Konfigurace kanálu 1070** a **Záznamník úloh 1170 POS** k synchronizaci povolené funkce s obchody.</span><span class="sxs-lookup"><span data-stu-id="61210-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="61210-220">Po odeslání změn do obchodů musí být POS terminály uzavřeny a znovu otevřeny, aby bylo možné použít nový formát ID transakce.</span><span class="sxs-lookup"><span data-stu-id="61210-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="61210-221">Jakmile bude povolena nová funkce formátu ID transakce, nebudete ji moci deaktivovat.</span><span class="sxs-lookup"><span data-stu-id="61210-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="61210-222">Pokud je třeba ji deaktivovat, kontaktujte podporu Commerce.</span><span class="sxs-lookup"><span data-stu-id="61210-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61210-223">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="61210-223">Additional resources</span></span>

[<span data-ttu-id="61210-224">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="61210-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="61210-225">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="61210-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="61210-226">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="61210-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="61210-227">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="61210-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
