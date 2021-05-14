---
title: Kódy Motor Freight Classification (NMFC)
description: Toto téma popisuje, jak pracovat s kódy National Motor Freight Classification (NMFC) v Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941875"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="a925a-103">Kódy Motor Freight Classification (NMFC)</span><span class="sxs-lookup"><span data-stu-id="a925a-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a925a-104">Kódy National Motor Freight Classification (NMFC) vám pomohou klasifikovat položky, které lze odeslat.</span><span class="sxs-lookup"><span data-stu-id="a925a-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="a925a-105">Kód NMFC je označení, které se používá ke seskupení komodit.</span><span class="sxs-lookup"><span data-stu-id="a925a-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="a925a-106">Umožňuje přepravním společnostem vyhodnotit zboží k odeslání klasifikací položek na základě úvah, jako je vhodnost kamionu, problémy s nakládáním, problémy s manipulací a rychle se kazící zboží.</span><span class="sxs-lookup"><span data-stu-id="a925a-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="a925a-107">Komodity jsou seskupeny do jedné z 18 nákladních tříd pomocí řady čísel od 50 do 500.</span><span class="sxs-lookup"><span data-stu-id="a925a-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="a925a-108">Třída, do které je komodita seskupena, je založena na vyhodnocení čtyř přepravních charakteristik: hustoty, skladovatelnosti, manipulace a odpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="a925a-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="a925a-109">Společně tyto vlastnosti zajišťují přepravitelnost komodity.</span><span class="sxs-lookup"><span data-stu-id="a925a-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="a925a-110">Kód NMFC je přidružen ke každé přepravní položce menší než nákladní vozidlo (LTL).</span><span class="sxs-lookup"><span data-stu-id="a925a-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="a925a-111">Například notebooku může být přiřazen NMFC, který je klasifikován na 2,5, zatímco elektrickým kabelům může být přiřazen NMFC, který je klasifikován na 65.</span><span class="sxs-lookup"><span data-stu-id="a925a-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="a925a-112">Tato funkce může pracovníkům pomoci použít kódy NMFC ke klasifikaci přepravních položek LTL.</span><span class="sxs-lookup"><span data-stu-id="a925a-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="a925a-113">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="a925a-113">Here are some examples:</span></span>

- <span data-ttu-id="a925a-114">Pokud vaše společnost uvede na nákladním listu (BOL) popis nákladu, bude mít přepravce určitou představu o tom, co je náklad.</span><span class="sxs-lookup"><span data-stu-id="a925a-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="a925a-115">Nákladní doprava je důležitá klasifikace, protože mnoho přepravních společností zakládá celý svůj obchodní model na typech nákladu, který přepravují.</span><span class="sxs-lookup"><span data-stu-id="a925a-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="a925a-116">Tato klasifikace může být pro vaši společnost zásadní, protože se používá k určení nákladů na danou zátěž.</span><span class="sxs-lookup"><span data-stu-id="a925a-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="a925a-117">Vaše společnost může identifikovat ziskovost logistické a přepravní společnosti LTL.</span><span class="sxs-lookup"><span data-stu-id="a925a-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="a925a-118">Toto téma popisuje, jak pracovat s k=ody NMFC v aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a925a-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a925a-119">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="a925a-119">Prerequisites</span></span>

<span data-ttu-id="a925a-120">Před vytvořením kódů NMFC musíte nastavit všechny třídy nákladní dopravy LTL, které k nim musí být namapovány.</span><span class="sxs-lookup"><span data-stu-id="a925a-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="a925a-121">Nákladní třídy LTL představují kategorie položek, zatímco kódy NMFC se vztahují ke konkrétním komoditám v každé z 18 nákladních tříd.</span><span class="sxs-lookup"><span data-stu-id="a925a-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="a925a-122">Další informace o tom, jak pracovat s třídami LTL, najdete v části [Třídy menší než nákladní vůz (LTL)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="a925a-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="a925a-123">Vytvoření kódu NMFC</span><span class="sxs-lookup"><span data-stu-id="a925a-123">Create an NMFC code</span></span>

<span data-ttu-id="a925a-124">Kód NMFC vytvoříte takto.</span><span class="sxs-lookup"><span data-stu-id="a925a-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="a925a-125">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="a925a-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="a925a-126">Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Kódy NMFC**.</span><span class="sxs-lookup"><span data-stu-id="a925a-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="a925a-127">Přejděte do nabídky **Správa přepravy \> Nastavení \> Přepravní normy \> Kódy NMFC**.</span><span class="sxs-lookup"><span data-stu-id="a925a-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="a925a-128">Vyberte **Nový** pro vytvoření NMFC kódu.</span><span class="sxs-lookup"><span data-stu-id="a925a-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="a925a-129">Poté nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="a925a-129">Then set the following fields:</span></span>

    - <span data-ttu-id="a925a-130">**NMFC kód** - Zadejte kód NMFC pro typ komodity.</span><span class="sxs-lookup"><span data-stu-id="a925a-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="a925a-131">**Název** - Zadejte název NMFC kódu.</span><span class="sxs-lookup"><span data-stu-id="a925a-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="a925a-132">**Třída LTL** - Vyberte třídu LTL, která je přidružena k kódu NMFC.</span><span class="sxs-lookup"><span data-stu-id="a925a-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="a925a-133">**Manipulační jednotka BOL** - Definujte výchozí typ zpracování zásilky.</span><span class="sxs-lookup"><span data-stu-id="a925a-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="a925a-134">Příklad: Nastavení kódů NMFC</span><span class="sxs-lookup"><span data-stu-id="a925a-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="a925a-135">Následující příklad ukazuje, jak nastavit dva různé kódy NMFC, které lze použít s různými produkty.</span><span class="sxs-lookup"><span data-stu-id="a925a-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="a925a-136">Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Kódy NMFC**.</span><span class="sxs-lookup"><span data-stu-id="a925a-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="a925a-137">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a925a-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a925a-138">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a925a-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a925a-139">**NMFC kód:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="a925a-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="a925a-140">**Název:** *Počítače*</span><span class="sxs-lookup"><span data-stu-id="a925a-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="a925a-141">**Třída LTL:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="a925a-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="a925a-142">**Manipulační jednotka BOL:** *Jednotka*</span><span class="sxs-lookup"><span data-stu-id="a925a-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="a925a-143">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a925a-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a925a-144">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a925a-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a925a-145">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a925a-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a925a-146">**NMFC kód:** *125*</span><span class="sxs-lookup"><span data-stu-id="a925a-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="a925a-147">**Název:** *Telefony*</span><span class="sxs-lookup"><span data-stu-id="a925a-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="a925a-148">**Třída LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="a925a-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="a925a-149">**Manipulační jednotka BOL:** *Jednotka*</span><span class="sxs-lookup"><span data-stu-id="a925a-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="a925a-150">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a925a-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a925a-151">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a925a-151">Additional resources</span></span>

- [<span data-ttu-id="a925a-152">Méně než třídy nákladu (LTL)</span><span class="sxs-lookup"><span data-stu-id="a925a-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="a925a-153">Vytvoření přepravního dokladu</span><span class="sxs-lookup"><span data-stu-id="a925a-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
