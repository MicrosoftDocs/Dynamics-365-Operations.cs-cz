---
title: Nastavení dopravců
description: Toto téma popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1ec19288f01ceb0bb3021cf549af1c38746785c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233576"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="d6e94-103">Nastavení dopravců</span><span class="sxs-lookup"><span data-stu-id="d6e94-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6e94-104">Toto téma popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice.</span><span class="sxs-lookup"><span data-stu-id="d6e94-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="d6e94-105">Koordinátor přepravy potom může přiřadit dopravce k příchozímu nebo odchozímu vytížení.</span><span class="sxs-lookup"><span data-stu-id="d6e94-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="d6e94-106">Vytvoření nového dopravce</span><span class="sxs-lookup"><span data-stu-id="d6e94-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="d6e94-107">Přejděte na **Navigační > podokno Moduly > Správa přepravy > Nastavení > Dopravci > Dopravci.**</span><span class="sxs-lookup"><span data-stu-id="d6e94-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="d6e94-108">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="d6e94-109">Zadejte hodnotu do pole **Dopravce dodávky**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="d6e94-110">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d6e94-111">V poli **Režim** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="d6e94-112">Zadání obecných informací pro dopravce</span><span class="sxs-lookup"><span data-stu-id="d6e94-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="d6e94-113">Přepněte rozšíření oddílu **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="d6e94-114">Zaškrtněte nebo zrušte zaškrtnutí políčka **Aktivovat dopravce**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="d6e94-115">V poli **Účet dodavatele** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="d6e94-116">Vyberte účet dodavatele, ke kterému chcete přiřadit dopravce.</span><span class="sxs-lookup"><span data-stu-id="d6e94-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="d6e94-117">V poli **Typ úhrady přepravy** vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="d6e94-118">Vyberte **Ručně**, pokud chcete použít stránku Úhrada přepravy, nebo vyberte **EDI** a nechte aktualizovat úhrady pomocí služby Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="d6e94-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="d6e94-119">Zaškrtněte nebo zrušte zaškrtnutí políčka **Aktivovat hodnocení dopravce**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="d6e94-120">Vytvoření nezbytných služeb pro dopravce</span><span class="sxs-lookup"><span data-stu-id="d6e94-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="d6e94-121">Přepněte rozšíření oddílu **Služby**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="d6e94-122">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-122">Select **New**.</span></span>
3. <span data-ttu-id="d6e94-123">Zadejte hodnotu do pole **Služba dopravce**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="d6e94-124">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d6e94-125">V poli **Metoda přepravy** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="d6e94-126">Nastavení adresy pro dopravce (volitelné)</span><span class="sxs-lookup"><span data-stu-id="d6e94-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="d6e94-127">Přepněte rozšíření oddílu **Adresy**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="d6e94-128">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-128">Select **New**.</span></span>
3. <span data-ttu-id="d6e94-129">Zadejte hodnotu do pole **Název nebo popis**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="d6e94-130">V poli **Země/oblast** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="d6e94-131">V poli **PSČ** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="d6e94-132">Zadejte hodnotu do pole **Ulice**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="d6e94-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="d6e94-134">Nastavení profilu hodnocení pro dopravce</span><span class="sxs-lookup"><span data-stu-id="d6e94-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="d6e94-135">Rozbalte oddíl **Profily sazeb**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="d6e94-136">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-136">Select **New**.</span></span>
3. <span data-ttu-id="d6e94-137">Zadejte hodnotu do pole **Profil sazeb**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="d6e94-138">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d6e94-139">V poli **Pracoviště** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="d6e94-140">V poli **Sklad** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="d6e94-141">V poli **Výpočet přepravních sazeb** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="d6e94-142">Vyberte modul sazeb, který je v souladu se smlouvou, které máte s dopravcem.</span><span class="sxs-lookup"><span data-stu-id="d6e94-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="d6e94-143">V poli **Hlavní sazba** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="d6e94-144">V poli **Modul mezioperačního času** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="d6e94-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="d6e94-145">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d6e94-145">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]