---
title: Země/oblast původu
description: Mnoho organizací vydává certifikáty svým dodavatelům, aby zajistily, že produkty splňují specifické certifikační standardy. Tyto certifikáty často závisí na zemi původu. Toto téma obsahuje informace o funkci země původu, která vám umožňuje propojit produkt s jeho zemí původu a sledovat jeho certifikace produktu.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596210"
---
# <a name="country-of-origin"></a><span data-ttu-id="8ee5a-105">Země/oblast původu</span><span class="sxs-lookup"><span data-stu-id="8ee5a-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ee5a-106">Mnoho organizací vydává certifikáty svým dodavatelům, aby zajistily, že produkty splňují specifické certifikační standardy.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="8ee5a-107">Tyto certifikáty často závisí na zemi původu.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="8ee5a-108">Funkce země původu, která vám umožňuje propojit produkt s jeho zemí původu a sledovat jeho certifikace produktu.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="8ee5a-109">Nakonfigurujte zdrojové a cílové země</span><span class="sxs-lookup"><span data-stu-id="8ee5a-109">Configure source and destination countries</span></span>

<span data-ttu-id="8ee5a-110">Před vydáním certifikátu pro produkt musíte produkt propojit s cílovou zemí a zemí původu.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="8ee5a-111">Přejděte na **Správa informací o produktu \> Založit \> Shoda výrobků \> Země původu \> Pravidla země původu**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="8ee5a-112">Vyberte existující nastavení země, které chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nové nastavení země.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="8ee5a-113">Nastavte následující hodnoty pro vybranou nebo novou zemi.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="8ee5a-114">Pole</span><span class="sxs-lookup"><span data-stu-id="8ee5a-114">Field</span></span> | <span data-ttu-id="8ee5a-115">popis</span><span class="sxs-lookup"><span data-stu-id="8ee5a-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="8ee5a-116">Č. položky</span><span class="sxs-lookup"><span data-stu-id="8ee5a-116">Item number</span></span> | <span data-ttu-id="8ee5a-117">Vyberte číslo položky produktu.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="8ee5a-118">Cílová země</span><span class="sxs-lookup"><span data-stu-id="8ee5a-118">Destination country</span></span> | <span data-ttu-id="8ee5a-119">Vyberte zemi, do které odesíláte produkt.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="8ee5a-120">Země původu</span><span class="sxs-lookup"><span data-stu-id="8ee5a-120">Origin country</span></span> | <span data-ttu-id="8ee5a-121">Vyberte zemi, ze které odesíláte produkt.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="8ee5a-122">Účelem tohoto nastavení je pomoci vám vygenerovat sestavu kusovníku (BOM), kde můžete zahrnout zemi původu pro každou část, pro kterou jsou zdrojové a cílové země určeny.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="8ee5a-123">Tato zpráva vám pomůže získat ucelený obrázek o tom, odkud vaše součásti pocházejí a kam směřují.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="8ee5a-124">Sledujte certifikáty dodavatelů</span><span class="sxs-lookup"><span data-stu-id="8ee5a-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="8ee5a-125">Můžete použít stránku **Osvědčení prodejců země původu** pro sledování certifikátů, které vydáváte prodejcům.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="8ee5a-126">Musíte se rozhodnout, které certifikáty vydáváte a jakým způsobem je budete hlásit zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="8ee5a-127">Tato funkce pomáhá sledovat vaše certifikáty.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="8ee5a-128">Umožňuje také zvolit, zda se příslušná čísla certifikátů budou zobrazovat na fakturách, dodacích listech nebo potvrzeních objednávek.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="8ee5a-129">Chcete-li nastavit informace certifikátů, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="8ee5a-130">Přejděte na **Správa informací o produktu \> Založit \> Shoda výrobků \> Země původu \> Certifikáty dodavatelů země původu**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="8ee5a-131">Vyberte existující nastavení certifikátu, které chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nové nastavení certifikátu.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="8ee5a-132">Proveďte následující nastavení pro vybraný nebo nový certifikát.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="8ee5a-133">Pole</span><span class="sxs-lookup"><span data-stu-id="8ee5a-133">Field</span></span> | <span data-ttu-id="8ee5a-134">popis</span><span class="sxs-lookup"><span data-stu-id="8ee5a-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="8ee5a-135">Účet dodavatele</span><span class="sxs-lookup"><span data-stu-id="8ee5a-135">Vendor account</span></span> | <span data-ttu-id="8ee5a-136">Vyberte dodavatele, kterému jste certifikát vydali.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="8ee5a-137">Č. položky</span><span class="sxs-lookup"><span data-stu-id="8ee5a-137">Item number</span></span> | <span data-ttu-id="8ee5a-138">Vyberte položku, které jste certifikát vydali.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="8ee5a-139">Země / oblast</span><span class="sxs-lookup"><span data-stu-id="8ee5a-139">Country/region</span></span> | <span data-ttu-id="8ee5a-140">Cílová země nebo region, kde musíte tento certifikát použít.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="8ee5a-141">Číslo certifikátu</span><span class="sxs-lookup"><span data-stu-id="8ee5a-141">Certificate number</span></span> | <span data-ttu-id="8ee5a-142">Zadejte identifikační číslo certifikátu, který jste vydali.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="8ee5a-143">Platný</span><span class="sxs-lookup"><span data-stu-id="8ee5a-143">Effective</span></span> | <span data-ttu-id="8ee5a-144">Vyberte první datum, kdy je aktuální certifikát platný.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="8ee5a-145">Vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="8ee5a-145">Expiration</span></span> | <span data-ttu-id="8ee5a-146">Vyberte poslední datum, kdy je aktuální certifikát platný.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="8ee5a-147">Vytisknout na fakturu</span><span class="sxs-lookup"><span data-stu-id="8ee5a-147">Print on invoice</span></span> | <span data-ttu-id="8ee5a-148">Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na fakturách, které jsou adresovány konkrétní zemi během zadaného časového období.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="8ee5a-149">Vytisknout na dodacím listu</span><span class="sxs-lookup"><span data-stu-id="8ee5a-149">Print on packing slip</span></span> | <span data-ttu-id="8ee5a-150">Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na dodacích listech, které jsou adresovány konkrétní zemi během zadaného časového období.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="8ee5a-151">Vytisknout na prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="8ee5a-151">Print on sales order</span></span> | <span data-ttu-id="8ee5a-152">Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na prodejních objednávkách, které jsou adresovány konkrétní zemi během zadaného časového období.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="8ee5a-153">Uveďte zemi původu do hlášení kusovníku</span><span class="sxs-lookup"><span data-stu-id="8ee5a-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="8ee5a-154">Při generování sestavy kusovníku můžete pro každou část, pro kterou jste určili zdrojovou a cílovou zemi, zadat zemi původu na stránce **Pravidla země původu**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="8ee5a-155">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8ee5a-156">Vyberte nebo vytvořte produkt a otevřete jeho stránku **Podrobnosti o uvolněném produktu**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="8ee5a-157">V podokně akcí na kartě **Analyzovat** ve skupině **BOM** zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="8ee5a-158">Na stránce, která se zobrazí, v podokně akcí vyberte **BOM \> Tisk**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="8ee5a-159">V dialogovém okně **Řádky kusovníku** nastavte pole **Cílová země** na cílovou zemi, kterou chcete zobrazit v sestavě.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="8ee5a-160">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-160">Select **OK**.</span></span>

<span data-ttu-id="8ee5a-161">Je vygenerována a zobrazena sestava, která zobrazuje informace o zemi původu každé části.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="8ee5a-162">Následuje příklad sestavy.</span><span class="sxs-lookup"><span data-stu-id="8ee5a-162">Here is an example of the report.</span></span>

<span data-ttu-id="8ee5a-163">![Sestava země původu](media/country-of-origin-report.png "Sestava země původu")</span><span class="sxs-lookup"><span data-stu-id="8ee5a-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
