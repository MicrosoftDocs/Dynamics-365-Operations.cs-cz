---
title: Výpočet daně (Preview)
description: Toto téma vysvětluje celkový rozsah a funkce výpočtu daně.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021925"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="ad00b-103">Výpočet daně (Preview)</span><span class="sxs-lookup"><span data-stu-id="ad00b-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ad00b-104">Výpočet daně je hyperškálovatelná multiklientová služba, která umožňuje globálnímu daňovému modulu automatizovat a zjednodušit proces stanovení a výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="ad00b-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="ad00b-105">Daňový modul je plně konfigurovatelný.</span><span class="sxs-lookup"><span data-stu-id="ad00b-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="ad00b-106">Mezi prvky, které lze konfigurovat, patří mimo jiné model zdanitelných dat, daňový kód, matice použitelnosti daně a vzorec výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="ad00b-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="ad00b-107">Daňový modul běží na platformě základních služeb Microsoft Azure a nabízí moderní technologie a exponenciální škálovatelnost.</span><span class="sxs-lookup"><span data-stu-id="ad00b-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="ad00b-108">Výpočet daně je integrován s Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad00b-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ad00b-109">Kromě toho se také integruje s Dynamics 365 Project Operations, Dynamics 365 Commerce a dalšími aplikacemi prvních stran a jiných výrobců.</span><span class="sxs-lookup"><span data-stu-id="ad00b-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="ad00b-110">Výpočet daně je daňový modul založený na mikroslužbách, který nabízí exponenciální škálovatelnost.</span><span class="sxs-lookup"><span data-stu-id="ad00b-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="ad00b-111">Pomůže vám provést následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="ad00b-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="ad00b-112">Konfigurujte výpočet daně prostřednictvím služby Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="ad00b-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="ad00b-113">RCS je vylepšená verze návrháře elektronických zpráv (ER) a je k dispozici jako samostatná služba.</span><span class="sxs-lookup"><span data-stu-id="ad00b-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="ad00b-114">Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové kódy a sazby.</span><span class="sxs-lookup"><span data-stu-id="ad00b-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="ad00b-115">Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové identifikační číslo (DIČ).</span><span class="sxs-lookup"><span data-stu-id="ad00b-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="ad00b-116">Nakonfigurujte návrháře výpočtu daně tak, aby definoval vzorce a podmínky.</span><span class="sxs-lookup"><span data-stu-id="ad00b-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="ad00b-117">Sdílejte řešení stanovení a výpočtu daně mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="ad00b-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="ad00b-118">Chcete-li použít službu výpočtu daně, nainstalujte doplněk služby výpočtu daně ze svého projektu ve službách Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ad00b-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ad00b-119">Poté dokončete nastavení v RCS a povolte službu výpočtu daně v aplikacích Finance a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad00b-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="ad00b-120">Více informací najdete v tématu [Začínáme s daňovou službou](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="ad00b-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="ad00b-121">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="ad00b-121">Availability</span></span>

<span data-ttu-id="ad00b-122">Výpočet daně je k dispozici pouze v prostředích sandbox a pro vybrané zákazníky, a to prostřednictvím programu Public Preview.</span><span class="sxs-lookup"><span data-stu-id="ad00b-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="ad00b-123">Nakonec bude obecně k dispozici všem zákazníkům a v produkčních prostředích.</span><span class="sxs-lookup"><span data-stu-id="ad00b-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="ad00b-124">Budou dodávány nové funkce, proto nezapomeňte často zkontrolovat nejaktuálnější dokumentaci, abyste se dozvěděli o pokrytí a rozsahu podporovaných funkcí.</span><span class="sxs-lookup"><span data-stu-id="ad00b-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="ad00b-125">Výpočet daně je nasazen v následujících geografických oblastech Azure.</span><span class="sxs-lookup"><span data-stu-id="ad00b-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="ad00b-126">Bude také nasazena do dalších geografických oblastí Azure, a to na základě potřeb zákazníků:</span><span class="sxs-lookup"><span data-stu-id="ad00b-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="ad00b-127">Spojené státy americké</span><span class="sxs-lookup"><span data-stu-id="ad00b-127">United States</span></span>
- <span data-ttu-id="ad00b-128">Evropa</span><span class="sxs-lookup"><span data-stu-id="ad00b-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="ad00b-129">Výpočet daně nepodporuje místní nasazení Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ad00b-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="ad00b-130">Nepodporuje také dřívější verze, například Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="ad00b-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="ad00b-131">Zvýrazněné funkce</span><span class="sxs-lookup"><span data-stu-id="ad00b-131">Feature highlights</span></span>

- <span data-ttu-id="ad00b-132">Konfigurovatelná matice daní, která automaticky určuje a vypočítá daň</span><span class="sxs-lookup"><span data-stu-id="ad00b-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="ad00b-133">Podpora více DIČ</span><span class="sxs-lookup"><span data-stu-id="ad00b-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="ad00b-134">Podpora převodních příkazů pro stanovení a výpočet daně</span><span class="sxs-lookup"><span data-stu-id="ad00b-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="ad00b-135">Podpora převodních příkazů pro určení více DIČ</span><span class="sxs-lookup"><span data-stu-id="ad00b-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="ad00b-136">Podporované transakce</span><span class="sxs-lookup"><span data-stu-id="ad00b-136">Supported transactions</span></span>

<span data-ttu-id="ad00b-137">Výpočet daně může být povolen podle právnické osoby a transakce.</span><span class="sxs-lookup"><span data-stu-id="ad00b-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="ad00b-138">Podporovány jsou následující transakce:</span><span class="sxs-lookup"><span data-stu-id="ad00b-138">The following transactions are supported:</span></span>

- <span data-ttu-id="ad00b-139">Proces prodeje</span><span class="sxs-lookup"><span data-stu-id="ad00b-139">Sales process</span></span>

    - <span data-ttu-id="ad00b-140">Prodejní nabídka</span><span class="sxs-lookup"><span data-stu-id="ad00b-140">Sales quotation</span></span>
    - <span data-ttu-id="ad00b-141">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="ad00b-141">Sales order</span></span>
    - <span data-ttu-id="ad00b-142">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="ad00b-142">Confirmation</span></span>
    - <span data-ttu-id="ad00b-143">Výdejka</span><span class="sxs-lookup"><span data-stu-id="ad00b-143">Picking list</span></span>
    - <span data-ttu-id="ad00b-144">Dodací list</span><span class="sxs-lookup"><span data-stu-id="ad00b-144">Packing slip</span></span>
    - <span data-ttu-id="ad00b-145">Prodejní faktura</span><span class="sxs-lookup"><span data-stu-id="ad00b-145">Sales invoice</span></span>
    - <span data-ttu-id="ad00b-146">Dobropis</span><span class="sxs-lookup"><span data-stu-id="ad00b-146">Credit note</span></span>
    - <span data-ttu-id="ad00b-147">Vratka</span><span class="sxs-lookup"><span data-stu-id="ad00b-147">Return order</span></span>
    - <span data-ttu-id="ad00b-148">Záhlaví – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ad00b-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ad00b-149">Řádek - vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ad00b-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="ad00b-150">Proces nákupu</span><span class="sxs-lookup"><span data-stu-id="ad00b-150">Purchase process</span></span>

    - <span data-ttu-id="ad00b-151">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="ad00b-151">Purchase order</span></span>
    - <span data-ttu-id="ad00b-152">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="ad00b-152">Confirmation</span></span>
    - <span data-ttu-id="ad00b-153">Příjemka</span><span class="sxs-lookup"><span data-stu-id="ad00b-153">Receipts list</span></span>
    - <span data-ttu-id="ad00b-154">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="ad00b-154">Product receipt</span></span>
    - <span data-ttu-id="ad00b-155">Nákupní faktura</span><span class="sxs-lookup"><span data-stu-id="ad00b-155">Purchase invoice</span></span>
    - <span data-ttu-id="ad00b-156">Záhlaví – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ad00b-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ad00b-157">Řádek - vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ad00b-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="ad00b-158">Dobropis</span><span class="sxs-lookup"><span data-stu-id="ad00b-158">Credit note</span></span>
    - <span data-ttu-id="ad00b-159">Vratka</span><span class="sxs-lookup"><span data-stu-id="ad00b-159">Return order</span></span>
    - <span data-ttu-id="ad00b-160">Nákupní žádanka</span><span class="sxs-lookup"><span data-stu-id="ad00b-160">Purchase requisition</span></span>
    - <span data-ttu-id="ad00b-161">Řádek nákupní žádanky – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ad00b-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="ad00b-162">Požadavek na nabídku</span><span class="sxs-lookup"><span data-stu-id="ad00b-162">Request for quotation</span></span>
    - <span data-ttu-id="ad00b-163">Záhlaví požadavku na nabídku – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ad00b-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="ad00b-164">Řádek požadavku na nabídku – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ad00b-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="ad00b-165">Proces zásob</span><span class="sxs-lookup"><span data-stu-id="ad00b-165">Inventory process</span></span>

    - <span data-ttu-id="ad00b-166">Převodní příkaz – expedice</span><span class="sxs-lookup"><span data-stu-id="ad00b-166">Transfer order – ship</span></span>
    - <span data-ttu-id="ad00b-167">Převodní příkaz – příjem</span><span class="sxs-lookup"><span data-stu-id="ad00b-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="ad00b-168">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="ad00b-168">Related resources</span></span>

[<span data-ttu-id="ad00b-169">Začínáme s daňovou službou</span><span class="sxs-lookup"><span data-stu-id="ad00b-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="ad00b-170">Vícenásobné daňové identifikační číslo</span><span class="sxs-lookup"><span data-stu-id="ad00b-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="ad00b-171">Podpora daňové funkce u převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="ad00b-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="ad00b-172">Jak vytvořit rozšíření v daňové službě</span><span class="sxs-lookup"><span data-stu-id="ad00b-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)