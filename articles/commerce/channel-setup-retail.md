---
title: Nastavení maloobchodního kanálu
description: Toto téma popisuje, jak vytvořit nový maloobchodní kanál v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113821"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="d0468-103">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="d0468-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d0468-104">Toto téma popisuje, jak vytvořit nový maloobchodní kanál v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d0468-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d0468-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d0468-105">Overview</span></span>

<span data-ttu-id="d0468-106">Dynamics 365 Commerce podporuje více maloobchodních sítí.</span><span class="sxs-lookup"><span data-stu-id="d0468-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="d0468-107">Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody).</span><span class="sxs-lookup"><span data-stu-id="d0468-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="d0468-108">Každý kanál maloobchodu může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d0468-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="d0468-109">Všechny tyto prvky je třeba nastavit pro maloobchod před vytvořením kanálu maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="d0468-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="d0468-110">Před vytvořením maloobchodního kanálu se ujistěte, že splňujete [předpoklady kanálu](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d0468-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="d0468-111">Vytvořit a konfigurovat nový maloobchodní kanál</span><span class="sxs-lookup"><span data-stu-id="d0468-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="d0468-112">V navigačním podokně přejděte na **Moduly \> Kanály \> Obchody \> Všechny obchody**.</span><span class="sxs-lookup"><span data-stu-id="d0468-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="d0468-113">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0468-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d0468-114">Do pole **Název** zadejte název nového kanálu.</span><span class="sxs-lookup"><span data-stu-id="d0468-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="d0468-115">V poli **Číslo obchodu** zadejte jedinečné číslo obchodu.</span><span class="sxs-lookup"><span data-stu-id="d0468-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="d0468-116">Číslo může být alfanumerické s maximálně 10 znaky.</span><span class="sxs-lookup"><span data-stu-id="d0468-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="d0468-117">V rozevíracím seznamu **Právnícká osoba** zadejte příslušnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d0468-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="d0468-118">Do rozevíracího seznamu **Sklad** zadejte příslušný sklad.</span><span class="sxs-lookup"><span data-stu-id="d0468-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="d0468-119">V poli **Uložené časové pásmo** vyberte příslušné časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="d0468-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="d0468-120">V rozevíracím seznamu **Skupina DPH** vyberte pro obchod příslušnou skupinu DPH.</span><span class="sxs-lookup"><span data-stu-id="d0468-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="d0468-121">V poli **Měna** vyberte příslušnou měnu.</span><span class="sxs-lookup"><span data-stu-id="d0468-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="d0468-122">V poli **Adresář odběratele** zadejte platný adresář.</span><span class="sxs-lookup"><span data-stu-id="d0468-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="d0468-123">Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="d0468-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="d0468-124">V poli **Funkční profil** vyberte funkční profil, pokud je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d0468-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="d0468-125">V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.</span><span class="sxs-lookup"><span data-stu-id="d0468-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="d0468-126">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0468-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d0468-127">V následujícím obrázku je znázorněno vytvoření nového maloobchodního kanálu.</span><span class="sxs-lookup"><span data-stu-id="d0468-127">The following image shows the creation of a new retail channel.</span></span>

![Nový maloobchodní kanál](media/channel-setup-retail-1.png)

<span data-ttu-id="d0468-129">Následující obrázek znázorňuje příklad maloobchodního kanálu.</span><span class="sxs-lookup"><span data-stu-id="d0468-129">The following image shows an example retail channel.</span></span>

![Příklad maloobchodního kanálu](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="d0468-131">Další nastavení</span><span class="sxs-lookup"><span data-stu-id="d0468-131">Other settings</span></span>

<span data-ttu-id="d0468-132">Existuje řada dalších volitelných nastavení, která lze nastavit v sekcích **Výkaz/uzávěrka** a **Různé** podle potřeb maloobchodního obchodu.</span><span class="sxs-lookup"><span data-stu-id="d0468-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="d0468-133">Kromě toho viz [Rozložení obrazovky pokladního místa (POS)](pos-screen-layouts.md) pro informace o nastavení výchozího rozvržení obrazovky v části **Rozložení obrazovky** a [Konfigurace a instalace Retail Hardware Station](retail-hardware-station-configuration-installation.md) pro informace o nastavení v části **Hardwarové stanice**.</span><span class="sxs-lookup"><span data-stu-id="d0468-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="d0468-134">Následující obrázek znázorňuje příklad konfigurace nastavení maloobchodního kanálu.</span><span class="sxs-lookup"><span data-stu-id="d0468-134">The following image shows an example retail channel setup configuration.</span></span>

![Příklad konfigurace maloobchodní sítě](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="d0468-136">Nastavení dodatečného kanálu</span><span class="sxs-lookup"><span data-stu-id="d0468-136">Additional channel set up</span></span>

<span data-ttu-id="d0468-137">Existují další položky, které je třeba nastavit pro kanál, který lze najít v **Podokně akcí** v sekci **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="d0468-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="d0468-138">Další úkoly požadované pro nastavení online kanálu zahrnují nastavení způsobů plateb, výkazu hotovosti, způsobů dodání, účtu příjmů/výdajů a přiřazení skupiny plnění a trezorů.</span><span class="sxs-lookup"><span data-stu-id="d0468-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="d0468-139">Následující obrázek ukazuje další možnosti nastavení maloobchodních kanálů na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="d0468-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Nastavení kanálu](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="d0468-141">Nastavení metod platby</span><span class="sxs-lookup"><span data-stu-id="d0468-141">Set up payment methods</span></span>

<span data-ttu-id="d0468-142">Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="d0468-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="d0468-143">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="d0468-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="d0468-144">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0468-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d0468-145">V navigačním podokně vyberte požadovaný způsob platby.</span><span class="sxs-lookup"><span data-stu-id="d0468-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="d0468-146">V části **Obecné** zadejte **Název operace** a nakonfigurujte další požadovaná nastavení.</span><span class="sxs-lookup"><span data-stu-id="d0468-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="d0468-147">Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.</span><span class="sxs-lookup"><span data-stu-id="d0468-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="d0468-148">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0468-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d0468-149">Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="d0468-149">The following image shows an example of a cash payment method.</span></span>

![Příklad způsobů platby](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="d0468-151">Nastavení výkazu hotovosti</span><span class="sxs-lookup"><span data-stu-id="d0468-151">Set up cash declaration</span></span>

1. <span data-ttu-id="d0468-152">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Výkaz hotovosti**.</span><span class="sxs-lookup"><span data-stu-id="d0468-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="d0468-153">V podokně akcí vyberte **Nový** a poté vytvořte všechny použitelné nominální hodnoty pro **Mince** a **Bankovky**.</span><span class="sxs-lookup"><span data-stu-id="d0468-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="d0468-154">Na následujícím obrázku je znázorněn příklad výkazu hotovosti.</span><span class="sxs-lookup"><span data-stu-id="d0468-154">The following image shows an example of a cash declaration.</span></span>

![Nastavení výkazu hotovosti](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="d0468-156">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="d0468-156">Set up modes of delivery</span></span>

<span data-ttu-id="d0468-157">Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.</span><span class="sxs-lookup"><span data-stu-id="d0468-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="d0468-158">Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d0468-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="d0468-159">V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="d0468-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="d0468-160">V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.</span><span class="sxs-lookup"><span data-stu-id="d0468-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="d0468-161">V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál.</span><span class="sxs-lookup"><span data-stu-id="d0468-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="d0468-162">Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.</span><span class="sxs-lookup"><span data-stu-id="d0468-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="d0468-163">Na následujícím obrázku je znázorněn příklad způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="d0468-163">The following image shows an example of a mode of delivery.</span></span>

![Nastavit způsoby dodání](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="d0468-165">Nastavit účet příjmů/výdajů</span><span class="sxs-lookup"><span data-stu-id="d0468-165">Set up income/expense account</span></span>

<span data-ttu-id="d0468-166">Chcete-li nastavit účet příjmů/výdajů, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d0468-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="d0468-167">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Účet příjmů/výdajů**.</span><span class="sxs-lookup"><span data-stu-id="d0468-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="d0468-168">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0468-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d0468-169">V položce **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="d0468-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="d0468-170">V položce **Vyhledat název** zadejte název pro vyhledání.</span><span class="sxs-lookup"><span data-stu-id="d0468-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="d0468-171">V položce **Typ účtu** zadejte typ účtu.</span><span class="sxs-lookup"><span data-stu-id="d0468-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="d0468-172">V případě potřeby zadejte text pro **Řádek zprávy 1**, **Řádek zprávy 2**, **Text stvrzenky 1** a **Text stvrzenky 2**.</span><span class="sxs-lookup"><span data-stu-id="d0468-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="d0468-173">V položce **Zaúčtování** zadejte informace o zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="d0468-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="d0468-174">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0468-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d0468-175">Následující obrázek znázorňuje příklad účtu příjmů/výdajů.</span><span class="sxs-lookup"><span data-stu-id="d0468-175">The following image shows an example of an income/expense account.</span></span>

![Nastavit účty příjmů/výdajů](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="d0468-177">Nastavení sekcí</span><span class="sxs-lookup"><span data-stu-id="d0468-177">Set up sections</span></span>

<span data-ttu-id="d0468-178">Chcete-li nastavit sekce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d0468-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="d0468-179">V podokně akcí vyberte kartu **Nastavení** a poté klikněte na možnost **Sekce**.</span><span class="sxs-lookup"><span data-stu-id="d0468-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="d0468-180">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0468-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d0468-181">V položce **Číslo sekce** zadejte číslo sekce.</span><span class="sxs-lookup"><span data-stu-id="d0468-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="d0468-182">V položce **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="d0468-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="d0468-183">V položce **Velikost sekce** zadejte velikost sekce.</span><span class="sxs-lookup"><span data-stu-id="d0468-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="d0468-184">Konfigurujte další nastavení pro **Obecné** a **Prodejní statistiky** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="d0468-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="d0468-185">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0468-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="d0468-186">Nastavení přiřazení skupiny plnění</span><span class="sxs-lookup"><span data-stu-id="d0468-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="d0468-187">Chcete-li nastavit přiřazení skupiny plnění, postupujte podle následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="d0468-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="d0468-188">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.</span><span class="sxs-lookup"><span data-stu-id="d0468-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="d0468-189">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0468-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d0468-190">V rozevíracím seznamu **Skupina plnění** vyberte skupinu plnění.</span><span class="sxs-lookup"><span data-stu-id="d0468-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="d0468-191">V rozevíracím sezamu **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="d0468-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="d0468-192">V podokně akcí vyberte **Uložit**</span><span class="sxs-lookup"><span data-stu-id="d0468-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="d0468-193">Následující obrázek znázorňuje příklad nastavení přiřazení skupiny plnění.</span><span class="sxs-lookup"><span data-stu-id="d0468-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Nastavení Přiřazení skupiny plnění](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="d0468-195">Nastavit trezory</span><span class="sxs-lookup"><span data-stu-id="d0468-195">Set up safes</span></span>

<span data-ttu-id="d0468-196">Chcete-li nastavit trezory, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d0468-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="d0468-197">V podokně akcí vyberte kartu **Nastavení** a poté klikněte na možnost **Trezory**.</span><span class="sxs-lookup"><span data-stu-id="d0468-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="d0468-198">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0468-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d0468-199">Zadejte název trezoru.</span><span class="sxs-lookup"><span data-stu-id="d0468-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="d0468-200">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0468-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0468-201">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d0468-201">Additional resources</span></span>

[<span data-ttu-id="d0468-202">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="d0468-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d0468-203">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="d0468-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d0468-204">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="d0468-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="d0468-205">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="d0468-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

