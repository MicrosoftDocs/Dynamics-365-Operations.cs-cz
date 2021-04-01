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
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bb35770f32c21a685b21a41dc7c369ee01fe3891
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243290"
---
# <a name="country-of-origin"></a><span data-ttu-id="9055a-105">Země/oblast původu</span><span class="sxs-lookup"><span data-stu-id="9055a-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9055a-106">Mnoho organizací vydává certifikáty svým dodavatelům, aby zajistily, že produkty splňují specifické certifikační standardy.</span><span class="sxs-lookup"><span data-stu-id="9055a-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="9055a-107">Tyto certifikáty často závisí na zemi původu.</span><span class="sxs-lookup"><span data-stu-id="9055a-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="9055a-108">Funkce země původu, která vám umožňuje propojit produkt s jeho zemí původu a sledovat jeho certifikace produktu.</span><span class="sxs-lookup"><span data-stu-id="9055a-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="9055a-109">Zapnutí funkci země původu</span><span class="sxs-lookup"><span data-stu-id="9055a-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="9055a-110">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="9055a-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9055a-111">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="9055a-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9055a-112">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="9055a-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9055a-113">**Modul**: *Řízení informací o produktech*</span><span class="sxs-lookup"><span data-stu-id="9055a-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="9055a-114">**Název funkce:** *Funkce správy země původu*</span><span class="sxs-lookup"><span data-stu-id="9055a-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="9055a-115">Nakonfigurujte zdrojové a cílové země</span><span class="sxs-lookup"><span data-stu-id="9055a-115">Configure source and destination countries</span></span>

<span data-ttu-id="9055a-116">Před vydáním certifikátu pro produkt musíte produkt propojit s cílovou zemí a zemí původu.</span><span class="sxs-lookup"><span data-stu-id="9055a-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="9055a-117">Přejděte na **Správa informací o produktu \> Založit \> Shoda výrobků \> Země původu \> Pravidla země původu**.</span><span class="sxs-lookup"><span data-stu-id="9055a-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="9055a-118">Vyberte existující nastavení země, které chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nové nastavení země.</span><span class="sxs-lookup"><span data-stu-id="9055a-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="9055a-119">Nastavte následující hodnoty pro vybranou nebo novou zemi.</span><span class="sxs-lookup"><span data-stu-id="9055a-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="9055a-120">Pole</span><span class="sxs-lookup"><span data-stu-id="9055a-120">Field</span></span> | <span data-ttu-id="9055a-121">popis</span><span class="sxs-lookup"><span data-stu-id="9055a-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="9055a-122">Č. položky</span><span class="sxs-lookup"><span data-stu-id="9055a-122">Item number</span></span> | <span data-ttu-id="9055a-123">Vyberte číslo položky produktu.</span><span class="sxs-lookup"><span data-stu-id="9055a-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="9055a-124">Cílová země</span><span class="sxs-lookup"><span data-stu-id="9055a-124">Destination country</span></span> | <span data-ttu-id="9055a-125">Vyberte zemi, do které odesíláte produkt.</span><span class="sxs-lookup"><span data-stu-id="9055a-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="9055a-126">Země původu</span><span class="sxs-lookup"><span data-stu-id="9055a-126">Origin country</span></span> | <span data-ttu-id="9055a-127">Vyberte zemi, ze které odesíláte produkt.</span><span class="sxs-lookup"><span data-stu-id="9055a-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="9055a-128">Účelem tohoto nastavení je pomoci vám vygenerovat sestavu kusovníku (BOM), kde můžete zahrnout zemi původu pro každou část, pro kterou jsou zdrojové a cílové země určeny.</span><span class="sxs-lookup"><span data-stu-id="9055a-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="9055a-129">Tato zpráva vám pomůže získat ucelený obrázek o tom, odkud vaše součásti pocházejí a kam směřují.</span><span class="sxs-lookup"><span data-stu-id="9055a-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="9055a-130">Sledujte certifikáty dodavatelů</span><span class="sxs-lookup"><span data-stu-id="9055a-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="9055a-131">Můžete použít stránku **Osvědčení prodejců země původu** pro sledování certifikátů, které vydáváte prodejcům.</span><span class="sxs-lookup"><span data-stu-id="9055a-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="9055a-132">Musíte se rozhodnout, které certifikáty vydáváte a jakým způsobem je budete hlásit zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="9055a-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="9055a-133">Tato funkce pomáhá sledovat vaše certifikáty.</span><span class="sxs-lookup"><span data-stu-id="9055a-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="9055a-134">Umožňuje také zvolit, zda se příslušná čísla certifikátů budou zobrazovat na fakturách, dodacích listech nebo potvrzeních objednávek.</span><span class="sxs-lookup"><span data-stu-id="9055a-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="9055a-135">Chcete-li nastavit informace certifikátů, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="9055a-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="9055a-136">Přejděte na **Správa informací o produktu \> Založit \> Shoda výrobků \> Země původu \> Certifikáty dodavatelů země původu**.</span><span class="sxs-lookup"><span data-stu-id="9055a-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="9055a-137">Vyberte existující nastavení certifikátu, které chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nové nastavení certifikátu.</span><span class="sxs-lookup"><span data-stu-id="9055a-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="9055a-138">Proveďte následující nastavení pro vybraný nebo nový certifikát.</span><span class="sxs-lookup"><span data-stu-id="9055a-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="9055a-139">Pole</span><span class="sxs-lookup"><span data-stu-id="9055a-139">Field</span></span> | <span data-ttu-id="9055a-140">popis</span><span class="sxs-lookup"><span data-stu-id="9055a-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="9055a-141">Účet dodavatele</span><span class="sxs-lookup"><span data-stu-id="9055a-141">Vendor account</span></span> | <span data-ttu-id="9055a-142">Vyberte dodavatele, kterému jste certifikát vydali.</span><span class="sxs-lookup"><span data-stu-id="9055a-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="9055a-143">Č. položky</span><span class="sxs-lookup"><span data-stu-id="9055a-143">Item number</span></span> | <span data-ttu-id="9055a-144">Vyberte položku, které jste certifikát vydali.</span><span class="sxs-lookup"><span data-stu-id="9055a-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="9055a-145">Země / oblast</span><span class="sxs-lookup"><span data-stu-id="9055a-145">Country/region</span></span> | <span data-ttu-id="9055a-146">Cílová země nebo region, kde musíte tento certifikát použít.</span><span class="sxs-lookup"><span data-stu-id="9055a-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="9055a-147">Číslo certifikátu</span><span class="sxs-lookup"><span data-stu-id="9055a-147">Certificate number</span></span> | <span data-ttu-id="9055a-148">Zadejte identifikační číslo certifikátu, který jste vydali.</span><span class="sxs-lookup"><span data-stu-id="9055a-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="9055a-149">Platný</span><span class="sxs-lookup"><span data-stu-id="9055a-149">Effective</span></span> | <span data-ttu-id="9055a-150">Vyberte první datum, kdy je aktuální certifikát platný.</span><span class="sxs-lookup"><span data-stu-id="9055a-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="9055a-151">Vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="9055a-151">Expiration</span></span> | <span data-ttu-id="9055a-152">Vyberte poslední datum, kdy je aktuální certifikát platný.</span><span class="sxs-lookup"><span data-stu-id="9055a-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="9055a-153">Vytisknout na fakturu</span><span class="sxs-lookup"><span data-stu-id="9055a-153">Print on invoice</span></span> | <span data-ttu-id="9055a-154">Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na fakturách, které jsou adresovány konkrétní zemi během zadaného časového období.</span><span class="sxs-lookup"><span data-stu-id="9055a-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="9055a-155">Vytisknout na dodacím listu</span><span class="sxs-lookup"><span data-stu-id="9055a-155">Print on packing slip</span></span> | <span data-ttu-id="9055a-156">Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na dodacích listech, které jsou adresovány konkrétní zemi během zadaného časového období.</span><span class="sxs-lookup"><span data-stu-id="9055a-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="9055a-157">Vytisknout na prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="9055a-157">Print on sales order</span></span> | <span data-ttu-id="9055a-158">Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na prodejních objednávkách, které jsou adresovány konkrétní zemi během zadaného časového období.</span><span class="sxs-lookup"><span data-stu-id="9055a-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="9055a-159">Uveďte zemi původu do hlášení kusovníku</span><span class="sxs-lookup"><span data-stu-id="9055a-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="9055a-160">Při generování sestavy kusovníku můžete pro každou část, pro kterou jste určili zdrojovou a cílovou zemi, zadat zemi původu na stránce **Pravidla země původu**.</span><span class="sxs-lookup"><span data-stu-id="9055a-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="9055a-161">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="9055a-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9055a-162">Vyberte nebo vytvořte produkt a otevřete jeho stránku **Podrobnosti o uvolněném produktu**.</span><span class="sxs-lookup"><span data-stu-id="9055a-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="9055a-163">V podokně akcí na kartě **Analyzovat** ve skupině **BOM** zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="9055a-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="9055a-164">Na stránce, která se zobrazí, v podokně akcí vyberte **BOM \> Tisk**.</span><span class="sxs-lookup"><span data-stu-id="9055a-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="9055a-165">V dialogovém okně **Řádky kusovníku** nastavte pole **Cílová země** na cílovou zemi, kterou chcete zobrazit v sestavě.</span><span class="sxs-lookup"><span data-stu-id="9055a-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="9055a-166">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9055a-166">Select **OK**.</span></span>

<span data-ttu-id="9055a-167">Je vygenerována a zobrazena sestava, která zobrazuje informace o zemi původu každé části.</span><span class="sxs-lookup"><span data-stu-id="9055a-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="9055a-168">Následuje příklad sestavy.</span><span class="sxs-lookup"><span data-stu-id="9055a-168">Here is an example of the report.</span></span>

<span data-ttu-id="9055a-169">![Sestava země původu](media/country-of-origin-report.png "Sestava země původu")</span><span class="sxs-lookup"><span data-stu-id="9055a-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]