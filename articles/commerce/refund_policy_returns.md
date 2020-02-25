---
title: Vytvoření a aktualizace zásady vrácení a refundace pro kanál
description: Toto téma vysvětluje, jak nastavit zásady vrácení a refundace pro kanál.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 66bb9bbd338561315f2f69ae4aff86a67513b190
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3021942"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="3e106-103">Vytvoření a aktualizace zásady vrácení a refundace pro kanál</span><span class="sxs-lookup"><span data-stu-id="3e106-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]


## <a name="overview"></a><span data-ttu-id="3e106-104">Přehled</span><span class="sxs-lookup"><span data-stu-id="3e106-104">Overview</span></span>

<span data-ttu-id="3e106-105">Zásada vrácení se změnami kanálu v Dynamics 365 Commerce umožňuje prodejcům nastavit vynucení, na kterých lze úhrady plateb povolit pro zpracování vrácení na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="3e106-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="3e106-106">Toto téma vysvětluje postup nastavení zásad vrácení a refundace pro kanál.</span><span class="sxs-lookup"><span data-stu-id="3e106-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="3e106-107">Rozsah zásady je aktuálně omezen na nastavení nabídek plateb, které lze povolit pro kanál.</span><span class="sxs-lookup"><span data-stu-id="3e106-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="3e106-108">Seznam povolených položek vychází z metod plateb, které byly použity při nákupu.</span><span class="sxs-lookup"><span data-stu-id="3e106-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="3e106-109">Například:</span><span class="sxs-lookup"><span data-stu-id="3e106-109">For example:</span></span>

- <span data-ttu-id="3e106-110">Pokud byl nákup proveden pomocí dárkového poukazu, platí zásady obchodu pro zpracování refundací pouze na nový dárkový poukaz nebo pro poskytnutí dobropisu obchodu.</span><span class="sxs-lookup"><span data-stu-id="3e106-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="3e106-111">Pokud je prodej uskutečněn s použitím hotovosti, jsou možnosti refundace hotovostní, dárkové poukazy a účet odběratele, ale ne kreditní karta.</span><span class="sxs-lookup"><span data-stu-id="3e106-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="3e106-112">Povolit zásady vracení</span><span class="sxs-lookup"><span data-stu-id="3e106-112">Enable return policy</span></span>

<span data-ttu-id="3e106-113">Chcete-li povolit funkci zásad vrácení v rámci prodejního kanálu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3e106-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="3e106-114">Přejděte do pracovního prostoru **Správa funkcí** v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3e106-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="3e106-115">Vyhledejte v seznamu názvů funkcí funkci **Povolit zásady vracení kanálů**.</span><span class="sxs-lookup"><span data-stu-id="3e106-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="3e106-116">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="3e106-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="3e106-117">Konfigurace zásad vracení</span><span class="sxs-lookup"><span data-stu-id="3e106-117">Configure return policy</span></span>

<span data-ttu-id="3e106-118">Chcete-li konfigurovat zásady vracení pro maloobchodní prodejnu nebo online maloobchodní kanál, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3e106-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="3e106-119">Přejděte na **Maloobchodní a velkoobchodní prodej** \> **Nastavení kanálu** \> **Vracení** \> **Zásady vracení v rámci kanálu**.</span><span class="sxs-lookup"><span data-stu-id="3e106-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="3e106-120">Vyberte **Nová** pro vytvoření nové šablony zásad vracení.</span><span class="sxs-lookup"><span data-stu-id="3e106-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="3e106-121">Chcete-li použít existující šablonu, vyberte ji v levém podokně.</span><span class="sxs-lookup"><span data-stu-id="3e106-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="3e106-122">Pro nové šablony přidejte název a popis, který vám pomůže určit zásadu při jejím použití v prodejním kanálu.</span><span class="sxs-lookup"><span data-stu-id="3e106-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="3e106-123">![Přidat nové zásady vrácení](media/Return-policy-page1.png "Přidání nové zásady vracení")</span><span class="sxs-lookup"><span data-stu-id="3e106-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="3e106-124">V části **Povolené způsoby platby refundace** definujte **povolené** nabídky výplat vratek, které jsou specifické pro jednotlivé způsoby platby.</span><span class="sxs-lookup"><span data-stu-id="3e106-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="3e106-125">![Přidat způsoby platby](media/Return-policy-page2.PNG "Nastavit povolené metody platby podle typu platby")</span><span class="sxs-lookup"><span data-stu-id="3e106-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="3e106-126">Způsoby platby jsou odvozeny ze způsobů platby nastavených pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="3e106-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="3e106-127">Přidání povoleného typu úhrady vratky pro každý ze seznamu způsobu platby zajistí, že vrácení může být provedeno na povolený typ úhrady vratky.</span><span class="sxs-lookup"><span data-stu-id="3e106-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="3e106-128">Přiřaďte šablonu zásad vracení s obchody, kde bude použita.</span><span class="sxs-lookup"><span data-stu-id="3e106-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="3e106-129">Na kartě **Maloobchodní kanály** vyberte **Přidat** a přidružte dostupné kanály.</span><span class="sxs-lookup"><span data-stu-id="3e106-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="3e106-130">V dialogovém okně **Vybrat uzly organizace** vyberte obchody, oblasti a organizace, ke kterým má být daná šablona přidružena.</span><span class="sxs-lookup"><span data-stu-id="3e106-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="3e106-131">Ke každému obchodu lze přidružit pouze jednu šablonu zásad vracení.</span><span class="sxs-lookup"><span data-stu-id="3e106-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="3e106-132">Pomocí tlačítek se šipkami vyberte obchody, regiony nebo organizace.</span><span class="sxs-lookup"><span data-stu-id="3e106-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="3e106-133">Datum začátku platnosti zásady bude datem, kdy jsou zásady použity pro kanály a spouštěné úlohy kanálu.</span><span class="sxs-lookup"><span data-stu-id="3e106-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="3e106-134">![Dialogové okno Vybrat organizační uzly](media/Return-policy-page3.PNG "Dialogové okno Vybrat organizační uzly")</span><span class="sxs-lookup"><span data-stu-id="3e106-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="3e106-135">Na stránce **Plán distribuce** spusťte úlohu **1070** pro zpřístupnění zásad vracení prodejního kanálu v POS.</span><span class="sxs-lookup"><span data-stu-id="3e106-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="3e106-136">Náhled zásad vrácení kanálů v POS</span><span class="sxs-lookup"><span data-stu-id="3e106-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="3e106-137">Chcete-li zobrazit povolené typy úhrad vratek v POS, postupujte podle kroků v jednom z následujících příkladů.</span><span class="sxs-lookup"><span data-stu-id="3e106-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="3e106-138">Přihlaste se k POS jako pokladník nebo manažer.</span><span class="sxs-lookup"><span data-stu-id="3e106-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="3e106-139">V části **Směna a pokladna** vyberte **Zobrazit deník**.</span><span class="sxs-lookup"><span data-stu-id="3e106-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="3e106-140">Vyberte transakci, která je součástí vrácení.</span><span class="sxs-lookup"><span data-stu-id="3e106-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="3e106-141">Vyberte položky k refundaci a vyberte způsob platby.</span><span class="sxs-lookup"><span data-stu-id="3e106-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="3e106-142">Pokud je vybraná úhrada plateb v seznamu povolených typů úhrad vratek, může pokladní dokončit transakci.</span><span class="sxs-lookup"><span data-stu-id="3e106-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="3e106-143">Není-li vybraná úhrada plateb povolena, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="3e106-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="3e106-144">Chcete-li zobrazit seznam všech povolených typů úhrady vratek, vyberte **Dlužná částka**.</span><span class="sxs-lookup"><span data-stu-id="3e106-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="3e106-145">- nebo -</span><span class="sxs-lookup"><span data-stu-id="3e106-145">-or-</span></span>

1. <span data-ttu-id="3e106-146">Přihlaste se k POS jako pokladník nebo manažer.</span><span class="sxs-lookup"><span data-stu-id="3e106-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="3e106-147">Vyberte **Transakce vrácení** a zadejte ID účtenky pomocí kontroly čárového kódu nebo ručním zadáním.</span><span class="sxs-lookup"><span data-stu-id="3e106-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="3e106-148">Vyberte transakci, která je součástí vrácení.</span><span class="sxs-lookup"><span data-stu-id="3e106-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="3e106-149">Vyberte položky k refundaci a vyberte způsob platby.</span><span class="sxs-lookup"><span data-stu-id="3e106-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="3e106-150">Pokud je vybraná úhrada plateb v seznamu povolených typů úhrad vratek, může pokladní dokončit transakci.</span><span class="sxs-lookup"><span data-stu-id="3e106-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="3e106-151">Není-li vybraná úhrada plateb povolena, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="3e106-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="3e106-152">Chcete-li zobrazit seznam všech povolených typů úhrady vratek, vyberte **Dlužná částka**.</span><span class="sxs-lookup"><span data-stu-id="3e106-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="3e106-153">![Nepovolena refundace](media/Return-policy-page6.png "Typ refundace není povolen.")</span><span class="sxs-lookup"><span data-stu-id="3e106-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="3e106-154">![Seznam způsobů platby](media/Return-policy-page5.PNG "Typy refundace nejsou povoleny")</span><span class="sxs-lookup"><span data-stu-id="3e106-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
