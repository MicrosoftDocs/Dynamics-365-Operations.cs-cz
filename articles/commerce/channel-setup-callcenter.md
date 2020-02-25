---
title: Nastavení kanálu kontaktního střediska
description: Toto téma popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002443"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="97b37-103">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="97b37-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="97b37-104">Toto téma popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97b37-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97b37-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="97b37-105">Overview</span></span>

<span data-ttu-id="97b37-106">V aplikaci Dynamics 365 Commerce je kontaktní středisko typu maloobchodní sítě, které lze definovat v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="97b37-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="97b37-107">Definování kanálu pro entity kontaktního střediska umožňuje systému zařadit specifická data a zpracovat výchozí hodnoty do prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="97b37-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="97b37-108">Společnost může definovat ve více kanálů kontaktního střediska v aplikaci Commerce.</span><span class="sxs-lookup"><span data-stu-id="97b37-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="97b37-109">Před vytvořením nového kanálu kontaktního centra se ujistěte, že jste splnili [Požadavky pro zřízení kanálů](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="97b37-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="97b37-110">Vytvořit a konfigurovat nový kanál kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="97b37-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="97b37-111">Chcete-li vytvořit a konfigurovat nový kanál kontaktního střediska, postupujte dle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="97b37-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="97b37-112">V navigačním podokně přejděte na **Moduly \> Kanály \> Kontaktní střediska \> Všechna kontaktní střediska**.</span><span class="sxs-lookup"><span data-stu-id="97b37-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="97b37-113">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="97b37-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="97b37-114">Do pole **Název** zadejte název nového kanálu.</span><span class="sxs-lookup"><span data-stu-id="97b37-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="97b37-115">Vyberte patřičnou **Právnickou osobu** z rozevírací nabídky.</span><span class="sxs-lookup"><span data-stu-id="97b37-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="97b37-116">Vyberte odpovídající umístění **Skladu** z rozevírací nabídky.</span><span class="sxs-lookup"><span data-stu-id="97b37-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="97b37-117">Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="97b37-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="97b37-118">V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.</span><span class="sxs-lookup"><span data-stu-id="97b37-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="97b37-119">Zadejte informační kód **Přepisu ceny**.</span><span class="sxs-lookup"><span data-stu-id="97b37-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="97b37-120">Poznámka: je možné, že pro vás bude nutné vytvořit informační kód.</span><span class="sxs-lookup"><span data-stu-id="97b37-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="97b37-121">Zadejte informační kód **Kód blokování**.</span><span class="sxs-lookup"><span data-stu-id="97b37-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="97b37-122">Poznámka: je možné, že pro vás bude nutné vytvořit informační kód.</span><span class="sxs-lookup"><span data-stu-id="97b37-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="97b37-123">Zadejte informační kód **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="97b37-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="97b37-124">Poznámka: je možné, že pro vás bude nutné vytvořit informační kód.</span><span class="sxs-lookup"><span data-stu-id="97b37-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="97b37-125">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="97b37-125">Select **Save**.</span></span>

<span data-ttu-id="97b37-126">V následujícím obrázku je znázorněno vytvoření nového kanálu kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="97b37-126">The following image shows the creation of a new call center channel.</span></span>

![Nový kanál kontaktního střediska](media/channel-setup-callcenter-1.png)

<span data-ttu-id="97b37-128">Následující obrázek znázorňuje příklad kanálu kontaktního centra.</span><span class="sxs-lookup"><span data-stu-id="97b37-128">The following image shows an example call center channel.</span></span>

![Příklad kanálu kontaktního střediska](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="97b37-130">Nastavení dodatečného kanálu</span><span class="sxs-lookup"><span data-stu-id="97b37-130">Additional channel setup</span></span>

<span data-ttu-id="97b37-131">Další úkoly požadované pro nastavení kanálu kontaktního střediska zahrnují nastavení způsobů plateb a způsobů dodání.</span><span class="sxs-lookup"><span data-stu-id="97b37-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="97b37-132">Následující obrázek znázorňuje možnosti nastavení **Režimy dodávek** a **Způsobů platby** na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="97b37-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Další akce nastavení kanálu kontaktního střediska](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="97b37-134">Nastavení metod platby</span><span class="sxs-lookup"><span data-stu-id="97b37-134">Set up payment methods</span></span>

<span data-ttu-id="97b37-135">Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="97b37-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="97b37-136">V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="97b37-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="97b37-137">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="97b37-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="97b37-138">V navigačním podokně vyberte požadovaný způsob platby.</span><span class="sxs-lookup"><span data-stu-id="97b37-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="97b37-139">V části **Obecné** zadejte **Název operace** a nakonfigurujte další požadovaná nastavení.</span><span class="sxs-lookup"><span data-stu-id="97b37-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="97b37-140">Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.</span><span class="sxs-lookup"><span data-stu-id="97b37-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="97b37-141">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="97b37-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="97b37-142">Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="97b37-142">The following image shows an example of a cash payment method.</span></span>

![Příklad způsobů platby](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="97b37-144">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="97b37-144">Set up modes of delivery</span></span>

<span data-ttu-id="97b37-145">Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.</span><span class="sxs-lookup"><span data-stu-id="97b37-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="97b37-146">Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="97b37-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="97b37-147">V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="97b37-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="97b37-148">V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.</span><span class="sxs-lookup"><span data-stu-id="97b37-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="97b37-149">V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál.</span><span class="sxs-lookup"><span data-stu-id="97b37-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="97b37-150">Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.</span><span class="sxs-lookup"><span data-stu-id="97b37-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="97b37-151">Na následujícím obrázku je znázorněn příklad způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="97b37-151">The following image shows an example of a mode of delivery.</span></span>

![Nastavit způsoby dodání](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="97b37-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="97b37-153">Additional resources</span></span>

[<span data-ttu-id="97b37-154">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="97b37-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="97b37-155">Funkce prodeje kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="97b37-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="97b37-156">Nastavení možností zpracování objednávky kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="97b37-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="97b37-157">Katalogy kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="97b37-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="97b37-158">Nastavení a práce s výstrahami u podvodů</span><span class="sxs-lookup"><span data-stu-id="97b37-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="97b37-159">Nastavení programů kontinuity pro kontaktní střediska</span><span class="sxs-lookup"><span data-stu-id="97b37-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
