---
title: Nastavení online kanálu
description: Toto téma popisuje, jak vytvořit nový online kanál v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002420"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="ccfcd-103">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="ccfcd-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ccfcd-104">Toto téma popisuje, jak vytvořit nový online kanál v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ccfcd-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="ccfcd-105">Overview</span></span>

<span data-ttu-id="ccfcd-106">Dynamics 365 Commerce podporuje více maloobchodních sítí.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="ccfcd-107">Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody).</span><span class="sxs-lookup"><span data-stu-id="ccfcd-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="ccfcd-108">Online obchody nabízí zákazníkům možnost nákupu produktů prodejce online i v maloobchodě.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="ccfcd-109">Chcete-li vytvořit online obchod v rámci služby Commerce, musíte nejprve vytvořit online kanál.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="ccfcd-110">Před vytvořením nového online kanálu se ujistěte, že jste splnili [Požadavky pro zřízení kanálů](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="ccfcd-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="ccfcd-111">Vytvořit a konfigurovat nový online kanál</span><span class="sxs-lookup"><span data-stu-id="ccfcd-111">Create and configure a new online channel</span></span>

<span data-ttu-id="ccfcd-112">Chcete-li vytvořit a konfigurovat nový online kanál, postupujte dle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="ccfcd-113">V navigačním podokně přejděte na **Moduly \> Kanály \> Online obchody**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="ccfcd-114">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ccfcd-115">Do pole **Název** zadejte název nového kanálu.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="ccfcd-116">V rozevíracím seznamu **Právnícká osoba** zadejte příslušnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="ccfcd-117">Do rozevíracího seznamu **Sklad** zadejte příslušný sklad.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="ccfcd-118">V poli **Uložené časové pásmo** vyberte příslušné časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="ccfcd-119">V poli **Měna** vyberte příslušnou měnu.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="ccfcd-120">Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="ccfcd-121">V poli **Adresář odběratele** zadejte platný adresář.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="ccfcd-122">V poli **Funkční profil** vyberte funkční profil, pokud je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="ccfcd-123">V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="ccfcd-124">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ccfcd-125">V následujícím obrázku je znázorněno vytvoření nového online kanálu.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-125">The following image shows the creation of a new online channel.</span></span>

![Nvý online kanál](media/channel-setup-online-1.png)

<span data-ttu-id="ccfcd-127">Následující obrázek znázorňuje příklad online kanálu.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-127">The following image shows an example online channel.</span></span>

![Příklad online kanálu](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="ccfcd-129">Nastavit jazyky</span><span class="sxs-lookup"><span data-stu-id="ccfcd-129">Set up languages</span></span>

<span data-ttu-id="ccfcd-130">Pokud váš web e-Commerce bude podporovat více jazyků, rozbalte část **Jazyky** a podle potřeby přidejte další jazyky.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="ccfcd-131">Nastavit účet platby</span><span class="sxs-lookup"><span data-stu-id="ccfcd-131">Set up payment account</span></span>

<span data-ttu-id="ccfcd-132">V části **Platební účet** můžete přidat poskytovatele plateb třetí strany.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="ccfcd-133">Informace o nastavení platebního konektoru Adyen naleznete v tématu [Platební konektor Dynamics 365 pro Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="ccfcd-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="ccfcd-134">Nastavení dodatečného kanálu</span><span class="sxs-lookup"><span data-stu-id="ccfcd-134">Additional channel set up</span></span>

<span data-ttu-id="ccfcd-135">Další úkoly požadované pro nastavení online kanálu zahrnují nastavení způsobů plateb, způsobů dodání a přiřazení skupiny plnění.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="ccfcd-136">Následující obrázek znázorňuje možnosti nastavení **Režimy dodávek**, **Způsobů platby** a **Přiřazení skupiny plnění** na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Další akce nastavení online kanálu](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="ccfcd-138">Nastavení metod platby</span><span class="sxs-lookup"><span data-stu-id="ccfcd-138">Set up payment methods</span></span>

<span data-ttu-id="ccfcd-139">Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="ccfcd-140">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="ccfcd-141">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ccfcd-142">V navigačním podokně vyberte požadovaný způsob platby.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="ccfcd-143">V části **Obecné** zadejte **Název operace** a nakonfigurujte další požadovaná nastavení.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="ccfcd-144">Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="ccfcd-145">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ccfcd-146">Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-146">The following image shows an example of a cash payment method.</span></span>

![Příklad způsobů platby](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="ccfcd-148">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="ccfcd-148">Set up modes of delivery</span></span>

<span data-ttu-id="ccfcd-149">Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="ccfcd-150">Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="ccfcd-151">V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="ccfcd-152">V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="ccfcd-153">V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="ccfcd-154">Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="ccfcd-155">Na následujícím obrázku je znázorněn příklad způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-155">The following image shows an example of a mode of delivery.</span></span>

![Nastavit způsoby dodání](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="ccfcd-157">Nastavení přiřazení skupiny plnění</span><span class="sxs-lookup"><span data-stu-id="ccfcd-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="ccfcd-158">Chcete-li nastavit přiřazení skupiny plnění, postupujte podle následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="ccfcd-159">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="ccfcd-160">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ccfcd-161">V rozevíracím seznamu **Skupina plnění** vyberte skupinu plnění.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="ccfcd-162">V rozevíracím sezamu **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="ccfcd-163">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ccfcd-164">Následující obrázek znázorňuje příklad nastavení přiřazení skupiny plnění.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Nastavení Přiřazení skupiny plnění](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="ccfcd-166">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ccfcd-166">Additional resources</span></span>

[<span data-ttu-id="ccfcd-167">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="ccfcd-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ccfcd-168">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="ccfcd-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ccfcd-169">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="ccfcd-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="ccfcd-170">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="ccfcd-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="ccfcd-171">Platební konektor Dynamics 365 pro Adyen</span><span class="sxs-lookup"><span data-stu-id="ccfcd-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
