---
title: Nastavení online kanálu
description: Toto téma popisuje, jak vytvořit nový online kanál v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 0d803b23f9de9daf624537d1d1ef30f17dc05fea
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533314"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="9e961-103">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="9e961-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9e961-104">Toto téma popisuje, jak vytvořit nový online kanál v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9e961-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9e961-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="9e961-105">Overview</span></span>

<span data-ttu-id="9e961-106">Dynamics 365 Commerce podporuje více maloobchodních sítí.</span><span class="sxs-lookup"><span data-stu-id="9e961-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="9e961-107">Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody).</span><span class="sxs-lookup"><span data-stu-id="9e961-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="9e961-108">Online obchody nabízí zákazníkům možnost nákupu produktů prodejce online i v maloobchodě.</span><span class="sxs-lookup"><span data-stu-id="9e961-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="9e961-109">Chcete-li vytvořit online obchod v rámci služby Commerce, musíte nejprve vytvořit online kanál.</span><span class="sxs-lookup"><span data-stu-id="9e961-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="9e961-110">Před vytvořením nového online kanálu se ujistěte, že jste splnili [Požadavky pro zřízení kanálů](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="9e961-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="9e961-111">Než bude možné vytvořit nový web, musí být v aplikaci Commerce vytvořen alespoň jeden online obchod.</span><span class="sxs-lookup"><span data-stu-id="9e961-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="9e961-112">Další informace najdete v části [Vytvoření webu elektronického obchodu](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9e961-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="9e961-113">Vytvořit a konfigurovat nový online kanál</span><span class="sxs-lookup"><span data-stu-id="9e961-113">Create and configure a new online channel</span></span>

<span data-ttu-id="9e961-114">Chcete-li vytvořit a konfigurovat nový online kanál, postupujte dle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="9e961-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="9e961-115">V navigačním podokně přejděte na **Moduly \> Kanály \> Online obchody**.</span><span class="sxs-lookup"><span data-stu-id="9e961-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="9e961-116">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="9e961-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9e961-117">Do pole **Název** zadejte název nového kanálu.</span><span class="sxs-lookup"><span data-stu-id="9e961-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="9e961-118">V rozevíracím seznamu **Právnícká osoba** zadejte příslušnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="9e961-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="9e961-119">Do rozevíracího seznamu **Sklad** zadejte příslušný sklad.</span><span class="sxs-lookup"><span data-stu-id="9e961-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="9e961-120">V poli **Uložené časové pásmo** vyberte příslušné časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="9e961-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="9e961-121">V poli **Měna** vyberte příslušnou měnu.</span><span class="sxs-lookup"><span data-stu-id="9e961-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="9e961-122">Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="9e961-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="9e961-123">V poli **Adresář odběratele** zadejte platný adresář.</span><span class="sxs-lookup"><span data-stu-id="9e961-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="9e961-124">V poli **Funkční profil** vyberte funkční profil, pokud je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="9e961-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="9e961-125">V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.</span><span class="sxs-lookup"><span data-stu-id="9e961-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="9e961-126">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9e961-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9e961-127">V následujícím obrázku je znázorněno vytvoření nového online kanálu.</span><span class="sxs-lookup"><span data-stu-id="9e961-127">The following image shows the creation of a new online channel.</span></span>

![Nvý online kanál](media/channel-setup-online-1.png)

<span data-ttu-id="9e961-129">Následující obrázek znázorňuje příklad online kanálu.</span><span class="sxs-lookup"><span data-stu-id="9e961-129">The following image shows an example online channel.</span></span>

![Příklad online kanálu](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="9e961-131">Nastavit jazyky</span><span class="sxs-lookup"><span data-stu-id="9e961-131">Set up languages</span></span>

<span data-ttu-id="9e961-132">Pokud váš web e-Commerce bude podporovat více jazyků, rozbalte část **Jazyky** a podle potřeby přidejte další jazyky.</span><span class="sxs-lookup"><span data-stu-id="9e961-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="9e961-133">Nastavit účet platby</span><span class="sxs-lookup"><span data-stu-id="9e961-133">Set up payment account</span></span>

<span data-ttu-id="9e961-134">V části **Platební účet** můžete přidat poskytovatele plateb třetí strany.</span><span class="sxs-lookup"><span data-stu-id="9e961-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="9e961-135">Informace o nastavení platebního konektoru Adyen naleznete v tématu [Platební konektor Dynamics 365 pro Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="9e961-135">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="9e961-136">Nastavení dodatečného kanálu</span><span class="sxs-lookup"><span data-stu-id="9e961-136">Additional channel set up</span></span>

<span data-ttu-id="9e961-137">Další úkoly požadované pro nastavení online kanálu zahrnují nastavení způsobů plateb, způsobů dodání a přiřazení skupiny plnění.</span><span class="sxs-lookup"><span data-stu-id="9e961-137">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="9e961-138">Následující obrázek znázorňuje možnosti nastavení **Režimy dodávek**, **Způsobů platby** a **Přiřazení skupiny plnění** na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="9e961-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Další akce nastavení online kanálu](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="9e961-140">Nastavení metod platby</span><span class="sxs-lookup"><span data-stu-id="9e961-140">Set up payment methods</span></span>

<span data-ttu-id="9e961-141">Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9e961-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="9e961-142">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="9e961-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="9e961-143">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="9e961-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9e961-144">V navigačním podokně vyberte požadovaný způsob platby.</span><span class="sxs-lookup"><span data-stu-id="9e961-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="9e961-145">V části **Obecné** zadejte **Název operace** a nakonfigurujte další požadovaná nastavení.</span><span class="sxs-lookup"><span data-stu-id="9e961-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="9e961-146">Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.</span><span class="sxs-lookup"><span data-stu-id="9e961-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="9e961-147">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9e961-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9e961-148">Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="9e961-148">The following image shows an example of a cash payment method.</span></span>

![Příklad způsobů platby](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="9e961-150">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="9e961-150">Set up modes of delivery</span></span>

<span data-ttu-id="9e961-151">Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.</span><span class="sxs-lookup"><span data-stu-id="9e961-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="9e961-152">Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="9e961-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="9e961-153">V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="9e961-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="9e961-154">V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.</span><span class="sxs-lookup"><span data-stu-id="9e961-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="9e961-155">V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál.</span><span class="sxs-lookup"><span data-stu-id="9e961-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="9e961-156">Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.</span><span class="sxs-lookup"><span data-stu-id="9e961-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="9e961-157">Na následujícím obrázku je znázorněn příklad způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="9e961-157">The following image shows an example of a mode of delivery.</span></span>

![Nastavit způsoby dodání](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="9e961-159">Nastavení přiřazení skupiny plnění</span><span class="sxs-lookup"><span data-stu-id="9e961-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="9e961-160">Chcete-li nastavit přiřazení skupiny plnění, postupujte podle následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="9e961-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="9e961-161">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.</span><span class="sxs-lookup"><span data-stu-id="9e961-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="9e961-162">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="9e961-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9e961-163">V rozevíracím seznamu **Skupina plnění** vyberte skupinu plnění.</span><span class="sxs-lookup"><span data-stu-id="9e961-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="9e961-164">V rozevíracím sezamu **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="9e961-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="9e961-165">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9e961-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9e961-166">Následující obrázek znázorňuje příklad nastavení přiřazení skupiny plnění.</span><span class="sxs-lookup"><span data-stu-id="9e961-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Nastavení Přiřazení skupiny plnění](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="9e961-168">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9e961-168">Additional resources</span></span>

[<span data-ttu-id="9e961-169">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="9e961-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9e961-170">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="9e961-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="9e961-171">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="9e961-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="9e961-172">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="9e961-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="9e961-173">Platební konektor Dynamics 365 pro Adyen</span><span class="sxs-lookup"><span data-stu-id="9e961-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
