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
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 03e46a7f8d110bd9ef3b353b150116bbf8a70ad5
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478109"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="b2820-103">Vytvoření a aktualizace zásady vrácení a refundace pro kanál</span><span class="sxs-lookup"><span data-stu-id="b2820-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2820-104">Zásada vrácení se změnami kanálu v Dynamics 365 Commerce umožňuje prodejcům nastavit vynucení, na kterých lze úhrady plateb povolit pro zpracování vrácení na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="b2820-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="b2820-105">Toto téma vysvětluje postup nastavení zásad vrácení a refundace pro kanál.</span><span class="sxs-lookup"><span data-stu-id="b2820-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="b2820-106">Rozsah zásady je aktuálně omezen na nastavení nabídek plateb, které lze povolit pro kanál.</span><span class="sxs-lookup"><span data-stu-id="b2820-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="b2820-107">Seznam povolených položek vychází z metod plateb, které byly použity při nákupu.</span><span class="sxs-lookup"><span data-stu-id="b2820-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="b2820-108">Například:</span><span class="sxs-lookup"><span data-stu-id="b2820-108">For example:</span></span>

- <span data-ttu-id="b2820-109">Pokud byl nákup proveden pomocí dárkového poukazu, platí zásady obchodu pro zpracování refundací pouze na nový dárkový poukaz nebo pro poskytnutí dobropisu obchodu.</span><span class="sxs-lookup"><span data-stu-id="b2820-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="b2820-110">Pokud je prodej uskutečněn s použitím hotovosti, jsou možnosti refundace hotovostní, dárkové poukazy a účet odběratele, ale ne kreditní karta.</span><span class="sxs-lookup"><span data-stu-id="b2820-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="b2820-111">Povolit zásady vracení</span><span class="sxs-lookup"><span data-stu-id="b2820-111">Enable return policy</span></span>

<span data-ttu-id="b2820-112">Chcete-li povolit funkci zásad vrácení v rámci prodejního kanálu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="b2820-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="b2820-113">Přejděte do pracovního prostoru **Správa funkcí** v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2820-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="b2820-114">Vyhledejte v seznamu názvů funkcí funkci **Povolit zásady vracení kanálů**.</span><span class="sxs-lookup"><span data-stu-id="b2820-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="b2820-115">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="b2820-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="b2820-116">Konfigurace zásad vracení</span><span class="sxs-lookup"><span data-stu-id="b2820-116">Configure return policy</span></span>

<span data-ttu-id="b2820-117">Chcete-li konfigurovat zásady vracení pro maloobchodní prodejnu nebo online maloobchodní kanál, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b2820-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="b2820-118">Přejděte na **Maloobchodní a velkoobchodní prodej** \> **Nastavení kanálu** \> **Vracení** \> **Zásady vracení v rámci kanálu**.</span><span class="sxs-lookup"><span data-stu-id="b2820-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="b2820-119">Vyberte **Nová** pro vytvoření nové šablony zásad vracení.</span><span class="sxs-lookup"><span data-stu-id="b2820-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="b2820-120">Chcete-li použít existující šablonu, vyberte ji v levém podokně.</span><span class="sxs-lookup"><span data-stu-id="b2820-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="b2820-121">Pro nové šablony přidejte název a popis, který vám pomůže určit zásadu při jejím použití v prodejním kanálu.</span><span class="sxs-lookup"><span data-stu-id="b2820-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="b2820-122">![Přidat nové zásady vrácení](media/Return-policy-page1.png "Přidání nové zásady vracení")</span><span class="sxs-lookup"><span data-stu-id="b2820-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="b2820-123">V části **Povolené způsoby platby refundace** definujte **povolené** nabídky výplat vratek, které jsou specifické pro jednotlivé způsoby platby.</span><span class="sxs-lookup"><span data-stu-id="b2820-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="b2820-124">![Přidat způsoby platby](media/Return-policy-page2.PNG "Nastavit povolené metody platby podle typu platby")</span><span class="sxs-lookup"><span data-stu-id="b2820-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="b2820-125">Způsoby platby jsou odvozeny ze způsobů platby nastavených pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="b2820-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="b2820-126">Přidání povoleného typu úhrady vratky pro každý ze seznamu způsobu platby zajistí, že vrácení může být provedeno na povolený typ úhrady vratky.</span><span class="sxs-lookup"><span data-stu-id="b2820-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="b2820-127">Přiřaďte šablonu zásad vracení s obchody, kde bude použita.</span><span class="sxs-lookup"><span data-stu-id="b2820-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="b2820-128">Na kartě **Maloobchodní kanály** vyberte **Přidat** a přidružte dostupné kanály.</span><span class="sxs-lookup"><span data-stu-id="b2820-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="b2820-129">V dialogovém okně **Vybrat uzly organizace** vyberte obchody, oblasti a organizace, ke kterým má být daná šablona přidružena.</span><span class="sxs-lookup"><span data-stu-id="b2820-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="b2820-130">Ke každému obchodu lze přidružit pouze jednu šablonu zásad vracení.</span><span class="sxs-lookup"><span data-stu-id="b2820-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="b2820-131">Pomocí tlačítek se šipkami vyberte obchody, regiony nebo organizace.</span><span class="sxs-lookup"><span data-stu-id="b2820-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="b2820-132">Datum začátku platnosti zásady bude datem, kdy jsou zásady použity pro kanály a spouštěné úlohy kanálu.</span><span class="sxs-lookup"><span data-stu-id="b2820-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="b2820-133">![Dialogové okno Vybrat organizační uzly](media/Return-policy-page3.PNG "Dialogové okno Vybrat organizační uzly")</span><span class="sxs-lookup"><span data-stu-id="b2820-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="b2820-134">Na stránce **Plán distribuce** spusťte úlohu **1070** pro zpřístupnění zásad vracení prodejního kanálu v POS.</span><span class="sxs-lookup"><span data-stu-id="b2820-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="b2820-135">Náhled zásad vrácení kanálů v POS</span><span class="sxs-lookup"><span data-stu-id="b2820-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="b2820-136">Chcete-li zobrazit povolené typy úhrad vratek v POS, postupujte podle kroků v jednom z následujících příkladů.</span><span class="sxs-lookup"><span data-stu-id="b2820-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="b2820-137">Přihlaste se k POS jako pokladník nebo manažer.</span><span class="sxs-lookup"><span data-stu-id="b2820-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="b2820-138">V části **Směna a pokladna** vyberte **Zobrazit deník**.</span><span class="sxs-lookup"><span data-stu-id="b2820-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="b2820-139">Vyberte transakci, která je součástí vrácení.</span><span class="sxs-lookup"><span data-stu-id="b2820-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="b2820-140">Vyberte položky k refundaci a vyberte způsob platby.</span><span class="sxs-lookup"><span data-stu-id="b2820-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="b2820-141">Pokud je vybraná úhrada plateb v seznamu povolených typů úhrad vratek, může pokladní dokončit transakci.</span><span class="sxs-lookup"><span data-stu-id="b2820-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="b2820-142">Není-li vybraná úhrada plateb povolena, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="b2820-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="b2820-143">Chcete-li zobrazit seznam všech povolených typů úhrady vratek, vyberte **Dlužná částka**.</span><span class="sxs-lookup"><span data-stu-id="b2820-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="b2820-144">- nebo -</span><span class="sxs-lookup"><span data-stu-id="b2820-144">-or-</span></span>

1. <span data-ttu-id="b2820-145">Přihlaste se k POS jako pokladník nebo manažer.</span><span class="sxs-lookup"><span data-stu-id="b2820-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="b2820-146">Vyberte **Transakce vrácení** a zadejte ID účtenky pomocí kontroly čárového kódu nebo ručním zadáním.</span><span class="sxs-lookup"><span data-stu-id="b2820-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="b2820-147">Vyberte transakci, která je součástí vrácení.</span><span class="sxs-lookup"><span data-stu-id="b2820-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="b2820-148">Vyberte položky k refundaci a vyberte způsob platby.</span><span class="sxs-lookup"><span data-stu-id="b2820-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="b2820-149">Pokud je vybraná úhrada plateb v seznamu povolených typů úhrad vratek, může pokladní dokončit transakci.</span><span class="sxs-lookup"><span data-stu-id="b2820-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="b2820-150">Není-li vybraná úhrada plateb povolena, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="b2820-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="b2820-151">Chcete-li zobrazit seznam všech povolených typů úhrady vratek, vyberte **Dlužná částka**.</span><span class="sxs-lookup"><span data-stu-id="b2820-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="b2820-152">![Nepovolena refundace](media/Return-policy-page6.png "Typ refundace není povolen.")</span><span class="sxs-lookup"><span data-stu-id="b2820-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="b2820-153">![Seznam způsobů platby](media/Return-policy-page5.PNG "Typy refundace nejsou povoleny")</span><span class="sxs-lookup"><span data-stu-id="b2820-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
