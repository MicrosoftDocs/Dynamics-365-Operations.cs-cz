---
title: Služba výpočtu daně (Preview)
description: Toto téma vysvětluje celkový rozsah a funkce služby výpočtu daní.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818217"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="ed7a4-103">Služba výpočtu daně (Preview)</span><span class="sxs-lookup"><span data-stu-id="ed7a4-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ed7a4-104">Služba výpočtu daně je hyperškálovatelná multiklientová služba, která umožňuje globálnímu daňovému modulu automatizovat a zjednodušit proces stanovení a výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="ed7a4-105">Daňový modul je plně konfigurovatelný.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="ed7a4-106">Mezi prvky, které lze konfigurovat, patří mimo jiné model zdanitelných dat, daňový kód, matice použitelnosti daně a vzorec výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="ed7a4-107">Daňový modul běží na platformě základních služeb Microsoft Azure a nabízí moderní technologie a exponenciální škálovatelnost.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="ed7a4-108">Služba výpočtu daní je integrována s Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ed7a4-109">Kromě toho se také integruje s Dynamics 365 Project Operations, Dynamics 365 Commerce a dalšími aplikacemi prvních stran a jiných výrobců.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="ed7a4-110">Služba výpočtu daně je daňový modul založený na technologiích Microsoftu, který nabízí exponenciální škálovatelnost.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="ed7a4-111">Pomůže vám provést následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="ed7a4-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="ed7a4-112">Konfigurujte službu výpočtu daně prostřednictvím služby Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="ed7a4-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="ed7a4-113">RCS je vylepšená verze návrháře elektronických zpráv (ER) a je k dispozici jako samostatná služba.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="ed7a4-114">Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové kódy a sazby.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="ed7a4-115">Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové identifikační číslo (DIČ).</span><span class="sxs-lookup"><span data-stu-id="ed7a4-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="ed7a4-116">Nakonfigurujte návrháře výpočtu daně tak, aby definoval vzorce a podmínky.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="ed7a4-117">Sdílejte řešení stanovení a výpočtu daně mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="ed7a4-118">Chcete-li použít službu výpočtu daně, nainstalujte doplněk služby výpočtu daně ze svého projektu ve službách Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ed7a4-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ed7a4-119">Poté dokončete nastavení v RCS a povolte službu výpočtu daně v aplikacích Finance a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="ed7a4-120">Více informací najdete v tématu [Začínáme s daňovou službou](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="ed7a4-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="ed7a4-121">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="ed7a4-121">Availability</span></span>

<span data-ttu-id="ed7a4-122">Služba výpočtu daně je k dispozici pouze v prostředích sandbox a pro vybrané zákazníky, a to prostřednictvím programu Public Preview.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="ed7a4-123">Nakonec bude obecně k dispozici všem zákazníkům a v produkčních prostředích.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="ed7a4-124">Nové funkce budou i nadále dodávány ve službě výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="ed7a4-125">Nezapomeňte proto často zkontrolovat nejaktuálnější dokumentaci, abyste se dozvěděli o pokrytí a rozsahu podporovaných funkcí.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="ed7a4-126">Služba výpočtu daně je nasazena v následujících geografických oblastech Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="ed7a4-127">Bude také nasazena do dalších geografických oblastí Azure, a to na základě potřeb zákazníků:</span><span class="sxs-lookup"><span data-stu-id="ed7a4-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="ed7a4-128">Spojené státy americké</span><span class="sxs-lookup"><span data-stu-id="ed7a4-128">United States</span></span>
- <span data-ttu-id="ed7a4-129">Evropa</span><span class="sxs-lookup"><span data-stu-id="ed7a4-129">Europe</span></span>
- <span data-ttu-id="ed7a4-130">Francie</span><span class="sxs-lookup"><span data-stu-id="ed7a4-130">France</span></span>
- <span data-ttu-id="ed7a4-131">Spojené království</span><span class="sxs-lookup"><span data-stu-id="ed7a4-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="ed7a4-132">Služba výpočtu daně nepodporuje místní nasazení Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="ed7a4-133">Nepodporuje také dřívější verze, například Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="ed7a4-134">Zvýrazněné funkce</span><span class="sxs-lookup"><span data-stu-id="ed7a4-134">Feature highlights</span></span>

- <span data-ttu-id="ed7a4-135">Konfigurovatelná matice daní, která automaticky určuje a vypočítá daň</span><span class="sxs-lookup"><span data-stu-id="ed7a4-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="ed7a4-136">Podpora více DIČ pro daň z přidané hodnoty (DPH)</span><span class="sxs-lookup"><span data-stu-id="ed7a4-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="ed7a4-137">Podpora převodních příkazů pro stanovení a výpočet daně</span><span class="sxs-lookup"><span data-stu-id="ed7a4-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="ed7a4-138">Podpora převodních příkazů pro určení více DIČ pro DPH</span><span class="sxs-lookup"><span data-stu-id="ed7a4-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="ed7a4-139">Podporované transakce</span><span class="sxs-lookup"><span data-stu-id="ed7a4-139">Supported transactions</span></span>

<span data-ttu-id="ed7a4-140">Služba výpočtu daně může být povolena podle právnické osoby a transakce.</span><span class="sxs-lookup"><span data-stu-id="ed7a4-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="ed7a4-141">Podporovány jsou následující transakce:</span><span class="sxs-lookup"><span data-stu-id="ed7a4-141">The following transactions are supported:</span></span>

- <span data-ttu-id="ed7a4-142">Proces prodeje</span><span class="sxs-lookup"><span data-stu-id="ed7a4-142">Sales process</span></span>

    - <span data-ttu-id="ed7a4-143">Prodejní nabídka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-143">Sales quotation</span></span>
    - <span data-ttu-id="ed7a4-144">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-144">Sales order</span></span>
    - <span data-ttu-id="ed7a4-145">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="ed7a4-145">Confirmation</span></span>
    - <span data-ttu-id="ed7a4-146">Výdejka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-146">Picking list</span></span>
    - <span data-ttu-id="ed7a4-147">Dodací list</span><span class="sxs-lookup"><span data-stu-id="ed7a4-147">Packing slip</span></span>
    - <span data-ttu-id="ed7a4-148">Prodejní faktura</span><span class="sxs-lookup"><span data-stu-id="ed7a4-148">Sales invoice</span></span>
    - <span data-ttu-id="ed7a4-149">Dobropis</span><span class="sxs-lookup"><span data-stu-id="ed7a4-149">Credit note</span></span>
    - <span data-ttu-id="ed7a4-150">Vratka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-150">Return order</span></span>
    - <span data-ttu-id="ed7a4-151">Záhlaví – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ed7a4-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ed7a4-152">Řádek - vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ed7a4-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="ed7a4-153">Proces nákupu</span><span class="sxs-lookup"><span data-stu-id="ed7a4-153">Purchase process</span></span>

    - <span data-ttu-id="ed7a4-154">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-154">Purchase order</span></span>
    - <span data-ttu-id="ed7a4-155">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="ed7a4-155">Confirmation</span></span>
    - <span data-ttu-id="ed7a4-156">Příjemka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-156">Receipts list</span></span>
    - <span data-ttu-id="ed7a4-157">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="ed7a4-157">Product receipt</span></span>
    - <span data-ttu-id="ed7a4-158">Nákupní faktura</span><span class="sxs-lookup"><span data-stu-id="ed7a4-158">Purchase invoice</span></span>
    - <span data-ttu-id="ed7a4-159">Záhlaví – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ed7a4-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ed7a4-160">Řádek - vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ed7a4-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="ed7a4-161">Dobropis</span><span class="sxs-lookup"><span data-stu-id="ed7a4-161">Credit note</span></span>
    - <span data-ttu-id="ed7a4-162">Vratka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-162">Return order</span></span>
    - <span data-ttu-id="ed7a4-163">Nákupní žádanka</span><span class="sxs-lookup"><span data-stu-id="ed7a4-163">Purchase requisition</span></span>
    - <span data-ttu-id="ed7a4-164">Řádek nákupní žádanky – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ed7a4-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="ed7a4-165">Požadavek na nabídku</span><span class="sxs-lookup"><span data-stu-id="ed7a4-165">Request for quotation</span></span>
    - <span data-ttu-id="ed7a4-166">Záhlaví požadavku na nabídku – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ed7a4-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="ed7a4-167">Řádek požadavku na nabídku – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="ed7a4-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="ed7a4-168">Proces zásob</span><span class="sxs-lookup"><span data-stu-id="ed7a4-168">Inventory process</span></span>

    - <span data-ttu-id="ed7a4-169">Převodní příkaz – expedice</span><span class="sxs-lookup"><span data-stu-id="ed7a4-169">Transfer order – ship</span></span>
    - <span data-ttu-id="ed7a4-170">Převodní příkaz – příjem</span><span class="sxs-lookup"><span data-stu-id="ed7a4-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="ed7a4-171">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="ed7a4-171">Related resources</span></span>

[<span data-ttu-id="ed7a4-172">Začínáme s daňovou službou</span><span class="sxs-lookup"><span data-stu-id="ed7a4-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="ed7a4-173">Vícenásobné daňové identifikační číslo</span><span class="sxs-lookup"><span data-stu-id="ed7a4-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="ed7a4-174">Podpora daňové funkce u převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="ed7a4-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="ed7a4-175">Jak vytvořit rozšíření v daňové službě</span><span class="sxs-lookup"><span data-stu-id="ed7a4-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
