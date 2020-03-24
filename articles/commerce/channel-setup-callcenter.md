---
title: Nastavení kanálu kontaktního střediska
description: Toto téma popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: 14cee020cc8aead627180343c82bf23534ae83c4
ms.sourcegitcommit: 0681a00d60c9f8cc8f7b9888b8c5ddf07279fc04
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3131724"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="3c74f-103">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3c74f-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3c74f-104">Toto téma popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3c74f-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3c74f-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3c74f-105">Overview</span></span>


<span data-ttu-id="3c74f-106">V aplikaci Dynamics 365 Commerce je kontaktní středisko typu maloobchodní sítě, které lze definovat v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="3c74f-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="3c74f-107">Definování kanálu pro entity kontaktního střediska umožňuje systému zařadit specifická data a zpracovat výchozí hodnoty do prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="3c74f-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="3c74f-108">Zatímco společnost může definovat více kanálů kontaktních center ve službě Commerce, je důležité si uvědomit, že jednotliví uživatelé mohou být spojeni pouze s jedním kanálem kontaktního centra.</span><span class="sxs-lookup"><span data-stu-id="3c74f-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="3c74f-109">Před vytvořením nového kanálu kontaktního centra se ujistěte, že jste splnili [Požadavky pro zřízení kanálů](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="3c74f-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="3c74f-110">Vytvořit a konfigurovat nový kanál kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3c74f-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="3c74f-111">Chcete-li vytvořit a konfigurovat nový kanál kontaktního střediska, postupujte dle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="3c74f-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="3c74f-112">V navigačním podokně přejděte na **Retail and Commerce \> Kanály \> Kontaktní střediska \> Všechna kontaktních střediska**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="3c74f-113">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3c74f-114">Do pole **Název** zadejte název nového kanálu.</span><span class="sxs-lookup"><span data-stu-id="3c74f-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="3c74f-115">Vyberte patřičnou **Právnickou osobu** z rozevírací nabídky.</span><span class="sxs-lookup"><span data-stu-id="3c74f-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="3c74f-116">Vyberte odpovídající umístění **Skladu** z rozevírací nabídky.</span><span class="sxs-lookup"><span data-stu-id="3c74f-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="3c74f-117">Toto místo bude použito jako výchozí v prodejních objednávkách vytvořených pro tento kanál kontaktního centra, pokud nebyla na úrovni odběratele nebo položky definována jiná výchozí nastavení.</span><span class="sxs-lookup"><span data-stu-id="3c74f-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="3c74f-118">Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="3c74f-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="3c74f-119">Tato data slouží k pomoci při vytváření nových záznamů odběratelů při automatickém vyplňování výchozího nastavení.</span><span class="sxs-lookup"><span data-stu-id="3c74f-119">This data is used to assist in auto-populating defaults when new customer records are created.</span></span> <span data-ttu-id="3c74f-120">Při vytváření objednávek kontaktních středisek není vhodné vytvářet objednávky pro výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="3c74f-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="3c74f-121">V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.</span><span class="sxs-lookup"><span data-stu-id="3c74f-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="3c74f-122">Při vytváření a zpracování objednávek kontaktních středisek se pomocí profilu e-mailového oznámení spouští automatické e-mailové výstrahy pro zákazníky s informacemi o stavu jejich objednávky.</span><span class="sxs-lookup"><span data-stu-id="3c74f-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="3c74f-123">Zadejte informační kód **Přepisu ceny**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="3c74f-124">Je možné, že pro vás bude nutné vytvořit informační kód.</span><span class="sxs-lookup"><span data-stu-id="3c74f-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="3c74f-125">Tento informační kód poskytuje sadu kódů důvodů, z nichž si uživatel bude při použití funkce přepsání ceny v objednávce kontaktního centra vycházet.</span><span class="sxs-lookup"><span data-stu-id="3c74f-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="3c74f-126">Zadejte informační kód **Kód blokování**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="3c74f-127">Je možné, že pro vás bude nutné vytvořit informační kód.</span><span class="sxs-lookup"><span data-stu-id="3c74f-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="3c74f-128">Tento informační kód poskytuje sadu vlitelných kódů důvodů, z nichž si uživatel bude vybírat při odesílání blokované objednávky.</span><span class="sxs-lookup"><span data-stu-id="3c74f-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="3c74f-129">Zadejte informační kód **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="3c74f-130">Je možné, že pro vás bude nutné vytvořit informační kód.</span><span class="sxs-lookup"><span data-stu-id="3c74f-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="3c74f-131">Tento informační kód obsahuje sadu kódů důvodů, z nichž může uživatel vybírat při použití funkce kredit objednávek v centru volání k poskytování různých refundací odběrateli z důvodů služeb pro zákazníky.</span><span class="sxs-lookup"><span data-stu-id="3c74f-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="3c74f-132">Volitelné: nastavení finančních dimenzí na pevné záložce **Finanční dimenze**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="3c74f-133">Dimenze zadané v tomto poli budou výchozí pro každou prodejní objednávku vytvořenou v tomto kanálu kontaktního centra.</span><span class="sxs-lookup"><span data-stu-id="3c74f-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="3c74f-134">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-134">Click **Save**.</span></span>

<span data-ttu-id="3c74f-135">V následujícím obrázku je znázorněno vytvoření nového kanálu kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3c74f-135">The following image shows the creation of a new call center channel.</span></span>

![Nový kanál kontaktního střediska](media/channel-setup-callcenter-1.png)

<span data-ttu-id="3c74f-137">Následující obrázek znázorňuje příklad kanálu kontaktního centra.</span><span class="sxs-lookup"><span data-stu-id="3c74f-137">The following image shows an example call center channel.</span></span>

![Příklad kanálu kontaktního střediska](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="3c74f-139">Nastavení dodatečného kanálu</span><span class="sxs-lookup"><span data-stu-id="3c74f-139">Additional channel setup</span></span>

<span data-ttu-id="3c74f-140">Další úkoly požadované pro nastavení kanálu kontaktního střediska zahrnují nastavení způsobů plateb a způsobů dodání.</span><span class="sxs-lookup"><span data-stu-id="3c74f-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="3c74f-141">Následující obrázek znázorňuje možnosti nastavení **Režimy dodávek** a **Způsobů platby** na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Další akce nastavení kanálu kontaktního střediska](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="3c74f-143">Nastavení metod platby</span><span class="sxs-lookup"><span data-stu-id="3c74f-143">Set up payment methods</span></span>

<span data-ttu-id="3c74f-144">Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="3c74f-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="3c74f-145">Uživatelé budou muset vybírat z předdefinovaných metod platby a propojit je s kanálem kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3c74f-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="3c74f-146">Před nastavením metod platby na kontaktních střediscích nejprve nastavte hlavní metody platby v **Retail and Commerce \> Nastavení kanállu \> Metody platby \> Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="3c74f-147">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="3c74f-148">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3c74f-149">V navigačním podokně vyberte způsob platby z dostupných předdefinovaných plateb.</span><span class="sxs-lookup"><span data-stu-id="3c74f-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="3c74f-150">Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.</span><span class="sxs-lookup"><span data-stu-id="3c74f-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="3c74f-151">V případě kreditních karet, dárkových poukazů nebo věrnostních karet je vyžadována další instalace výběrem funkce **Nastavení karty**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="3c74f-152">Konfigurace správných účtů pro zaúčtování pro typ platby v části **Zaúčtování**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="3c74f-153">V podokně akcí klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="3c74f-154">Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="3c74f-154">The following image shows an example of a cash payment method.</span></span>

![Příklad způsobů platby](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="3c74f-156">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="3c74f-156">Set up modes of delivery</span></span>

<span data-ttu-id="3c74f-157">Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="3c74f-158">Chcete-li změnit nebo přidat způsob dodání, který má být přidružen k kanálu kontaktního střediska, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3c74f-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="3c74f-159">Ve formuláři způsoby dodání na základě kontaktního střediska vyberte **Spravovat způsoby dodání**</span><span class="sxs-lookup"><span data-stu-id="3c74f-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="3c74f-160">V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.</span><span class="sxs-lookup"><span data-stu-id="3c74f-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="3c74f-161">V oddílu **Maloobchodní kanály** klikněte na **Přidat řádek**, chcete-li přidat kanál kontaktního centra.</span><span class="sxs-lookup"><span data-stu-id="3c74f-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="3c74f-162">Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.</span><span class="sxs-lookup"><span data-stu-id="3c74f-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="3c74f-163">Zajistěte, aby byl způsob dodání konfigurován daty na pevné záložce **Produkty** a **Adresy**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="3c74f-164">Nejsou-li pro způsob dodání platné žádné produkty nebo dodací adresy, při výběru objednávky dojde k chybám.</span><span class="sxs-lookup"><span data-stu-id="3c74f-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="3c74f-165">Po provedení změn v režimu kontaktní středisko pro konfiguraci dodání je nutné spustit úlohu **Zpracovat způsoby dodání** a rozbalit tak matici změn.</span><span class="sxs-lookup"><span data-stu-id="3c74f-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="3c74f-166">Tato úloha se nachází v **Maloobchodní a velkoobchodní prodej \> IT pro maloobchod a velkoobchod \> Zpracovat způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="3c74f-167">Na následujícím obrázku je znázorněn příklad způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="3c74f-167">The following image shows an example of a mode of delivery.</span></span>

![Nastavit způsoby dodání](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="3c74f-169">Nastavení uživatele kanálu</span><span class="sxs-lookup"><span data-stu-id="3c74f-169">Set up channel users</span></span>

<span data-ttu-id="3c74f-170">Chcete-li vytvořit prodejní objednávku, která je propojena s kanálem kontaktního centra z programu Commerce Headquarters, musí být uživatel vytvářející prodejní objednávku propojen s kanálem kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3c74f-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="3c74f-171">Uživatel nemůže ručně propojit prodejní objednávku vytvořenou v rámci služby Commerce Headquarters s kanálem kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3c74f-171">The user can not manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="3c74f-172">Odkaz je systematický a je založen na uživateli a vztahu uživatele k kanálu kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3c74f-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="3c74f-173">Uživatel může být propojen pouze s jedním kanálem kontaktního centra.</span><span class="sxs-lookup"><span data-stu-id="3c74f-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="3c74f-174">V podokně akcí vyberte kartu **Kanál** a poté vyberte možnost **Uživatelé kanálu**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="3c74f-175">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3c74f-176">Vyberte existující **ID uživatele** z rozevíracího seznamu výběrů, chcete-li tohoto uživatele propojit s kanálem kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3c74f-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="3c74f-177">Po dokončení nastavení uživatele kanálu a uživatel vytvoří novou prodejní objednávku v Commerce Headquarters, bude prodejní objednávka propojena s přiřazeným kanálem kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3c74f-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="3c74f-178">Všechny konfigurace tohoto kanálu budou systematicky použity pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="3c74f-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="3c74f-179">Uživatel může potvrdit, se kterým kanálem kontaktního střediska je prodejní objednávka propojena, a to zobrazením odkazu názvu kanálu v záhlaví prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="3c74f-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="3c74f-180">Nastavení cenových skupin</span><span class="sxs-lookup"><span data-stu-id="3c74f-180">Set up price groups</span></span>

<span data-ttu-id="3c74f-181">Cenové skupiny jsou volitelné, ale pokud jsou používány, mohou kontrolovat, které prodejní ceny budou nabídnuty odběratelům, kteří dodávají objednávky do kanálu kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="3c74f-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="3c74f-182">Pokud pro odběratele nebyla nakonfigurována cenová skupina nebo pokud nejsou použity cenové skupiny katalogu pro prodejní objednávku (pomocí pole **ID zdrojového kódu** v záhlaví objednávky kontaktního centra), použije se pro vyhledání cen položek Cenová skupina kanálů.</span><span class="sxs-lookup"><span data-stu-id="3c74f-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="3c74f-183">Pokud v kanálu kontaktního střediska nebyla nalezena Cenová skupina, použijí se výchozí hlavní ceny zboží.</span><span class="sxs-lookup"><span data-stu-id="3c74f-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="3c74f-184">Chcete-li nastavit cenovou skupinu, postupujte podle následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="3c74f-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="3c74f-185">V podokně akcí klikněte na kartu **Kanál** a poté vyberte možnost **Cenové skupiny**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="3c74f-186">V podokně akcí klikněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="3c74f-187">V rozevíracím seznamu vyberte **Maloobchodní cenovou skupinu**.</span><span class="sxs-lookup"><span data-stu-id="3c74f-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c74f-188">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3c74f-188">Additional resources</span></span>

[<span data-ttu-id="3c74f-189">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="3c74f-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="3c74f-190">Funkce prodeje kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3c74f-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="3c74f-191">Nastavení možností zpracování objednávky kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3c74f-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="3c74f-192">Katalogy kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="3c74f-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="3c74f-193">Nastavení a práce s výstrahami u podvodů</span><span class="sxs-lookup"><span data-stu-id="3c74f-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="3c74f-194">Nastavení programů kontinuity pro kontaktní střediska</span><span class="sxs-lookup"><span data-stu-id="3c74f-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
