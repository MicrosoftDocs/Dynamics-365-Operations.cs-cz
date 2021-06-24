---
title: Výpočet daně (Preview)
description: Toto téma vysvětluje celkový rozsah a funkce výpočtu daně.
author: wangchen
ms.date: 06/03/2021
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184094"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="c9a7b-103">Výpočet daně (Preview)</span><span class="sxs-lookup"><span data-stu-id="c9a7b-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c9a7b-104">Výpočet daně je hyperškálovatelná multiklientová služba, která umožňuje globálnímu daňovému modulu automatizovat a zjednodušit proces stanovení a výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="c9a7b-105">Daňový modul je plně konfigurovatelný.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="c9a7b-106">Mezi prvky, které lze konfigurovat, patří mimo jiné model zdanitelných dat, daňový kód, matice použitelnosti daně a vzorec výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="c9a7b-107">Daňový modul běží na platformě základních služeb Microsoft Azure a nabízí moderní technologie a exponenciální škálovatelnost.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="c9a7b-108">Výpočet daně je integrován s Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c9a7b-109">Kromě toho se také integruje s Dynamics 365 Project Operations, Dynamics 365 Commerce a dalšími aplikacemi prvních stran a jiných výrobců.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9a7b-110">Když povolíte službu Výpočet daně, některé operace se souvisejícími daty mohou být prováděny v jiném datovém centru než v datovém centru, které udržuje vaše data služby.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="c9a7b-111">Zkontrolujte [Smluvní podmínky](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) před povolením služby Výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="c9a7b-112">Ochrana vašich osobních údajů je pro nás důležitá.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-112">Your privacy is important to us.</span></span> <span data-ttu-id="c9a7b-113">Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="c9a7b-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="c9a7b-114">Výpočet daně je daňový modul založený na mikroslužbách, který nabízí exponenciální škálovatelnost.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="c9a7b-115">Pomůže vám provést následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="c9a7b-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="c9a7b-116">Konfigurujte výpočet daně prostřednictvím služby Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="c9a7b-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="c9a7b-117">RCS je vylepšená verze návrháře elektronických zpráv (ER) a je k dispozici jako samostatná služba.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="c9a7b-118">Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové kódy a sazby.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="c9a7b-119">Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové identifikační číslo (DIČ).</span><span class="sxs-lookup"><span data-stu-id="c9a7b-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="c9a7b-120">Nakonfigurujte návrháře výpočtu daně tak, aby definoval vzorce a podmínky.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="c9a7b-121">Sdílejte řešení stanovení a výpočtu daně mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="c9a7b-122">Chcete-li použít službu výpočtu daně, nainstalujte doplněk služby výpočtu daně ze svého projektu ve službách Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c9a7b-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c9a7b-123">Poté dokončete nastavení v RCS a povolte službu výpočtu daně v aplikacích Finance a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="c9a7b-124">Více informací najdete v tématu [Začínáme s daňovou službou](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="c9a7b-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="c9a7b-125">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="c9a7b-125">Availability</span></span>

<span data-ttu-id="c9a7b-126">Výpočet daně je k dispozici pouze v prostředích sandbox a pro vybrané zákazníky, a to prostřednictvím programu Public Preview.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="c9a7b-127">Nakonec bude obecně k dispozici všem zákazníkům a v produkčních prostředích.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="c9a7b-128">Budou dodávány nové funkce, proto nezapomeňte často zkontrolovat nejaktuálnější dokumentaci, abyste se dozvěděli o pokrytí a rozsahu podporovaných funkcí.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="c9a7b-129">Výpočet daně je nasazen v následujících geografických oblastech Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="c9a7b-130">Bude také nasazena do dalších geografických oblastí Azure, a to na základě potřeb zákazníků:</span><span class="sxs-lookup"><span data-stu-id="c9a7b-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="c9a7b-131">Spojené státy americké</span><span class="sxs-lookup"><span data-stu-id="c9a7b-131">United States</span></span>
- <span data-ttu-id="c9a7b-132">Evropa</span><span class="sxs-lookup"><span data-stu-id="c9a7b-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="c9a7b-133">Výpočet daně nepodporuje místní nasazení Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="c9a7b-134">Nepodporuje také dřívější verze, například Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="c9a7b-135">Zvýrazněné funkce</span><span class="sxs-lookup"><span data-stu-id="c9a7b-135">Feature highlights</span></span>

- <span data-ttu-id="c9a7b-136">Konfigurovatelná matice daní, která automaticky určuje a vypočítá daň</span><span class="sxs-lookup"><span data-stu-id="c9a7b-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="c9a7b-137">Podpora více DIČ</span><span class="sxs-lookup"><span data-stu-id="c9a7b-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="c9a7b-138">Podpora převodních příkazů pro stanovení a výpočet daně</span><span class="sxs-lookup"><span data-stu-id="c9a7b-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="c9a7b-139">Podpora převodních příkazů pro určení více DIČ</span><span class="sxs-lookup"><span data-stu-id="c9a7b-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="c9a7b-140">Podporované transakce</span><span class="sxs-lookup"><span data-stu-id="c9a7b-140">Supported transactions</span></span>

<span data-ttu-id="c9a7b-141">Výpočet daně může být povolen podle právnické osoby a transakce.</span><span class="sxs-lookup"><span data-stu-id="c9a7b-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="c9a7b-142">Podporovány jsou následující transakce:</span><span class="sxs-lookup"><span data-stu-id="c9a7b-142">The following transactions are supported:</span></span>

- <span data-ttu-id="c9a7b-143">Proces prodeje</span><span class="sxs-lookup"><span data-stu-id="c9a7b-143">Sales process</span></span>

    - <span data-ttu-id="c9a7b-144">Prodejní nabídka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-144">Sales quotation</span></span>
    - <span data-ttu-id="c9a7b-145">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-145">Sales order</span></span>
    - <span data-ttu-id="c9a7b-146">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="c9a7b-146">Confirmation</span></span>
    - <span data-ttu-id="c9a7b-147">Výdejka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-147">Picking list</span></span>
    - <span data-ttu-id="c9a7b-148">Dodací list</span><span class="sxs-lookup"><span data-stu-id="c9a7b-148">Packing slip</span></span>
    - <span data-ttu-id="c9a7b-149">Prodejní faktura</span><span class="sxs-lookup"><span data-stu-id="c9a7b-149">Sales invoice</span></span>
    - <span data-ttu-id="c9a7b-150">Dobropis</span><span class="sxs-lookup"><span data-stu-id="c9a7b-150">Credit note</span></span>
    - <span data-ttu-id="c9a7b-151">Vratka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-151">Return order</span></span>
    - <span data-ttu-id="c9a7b-152">Záhlaví – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="c9a7b-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="c9a7b-153">Řádek - vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="c9a7b-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="c9a7b-154">Proces nákupu</span><span class="sxs-lookup"><span data-stu-id="c9a7b-154">Purchase process</span></span>

    - <span data-ttu-id="c9a7b-155">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-155">Purchase order</span></span>
    - <span data-ttu-id="c9a7b-156">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="c9a7b-156">Confirmation</span></span>
    - <span data-ttu-id="c9a7b-157">Příjemka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-157">Receipts list</span></span>
    - <span data-ttu-id="c9a7b-158">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="c9a7b-158">Product receipt</span></span>
    - <span data-ttu-id="c9a7b-159">Nákupní faktura</span><span class="sxs-lookup"><span data-stu-id="c9a7b-159">Purchase invoice</span></span>
    - <span data-ttu-id="c9a7b-160">Záhlaví – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="c9a7b-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="c9a7b-161">Řádek - vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="c9a7b-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="c9a7b-162">Dobropis</span><span class="sxs-lookup"><span data-stu-id="c9a7b-162">Credit note</span></span>
    - <span data-ttu-id="c9a7b-163">Vratka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-163">Return order</span></span>
    - <span data-ttu-id="c9a7b-164">Nákupní žádanka</span><span class="sxs-lookup"><span data-stu-id="c9a7b-164">Purchase requisition</span></span>
    - <span data-ttu-id="c9a7b-165">Řádek nákupní žádanky – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="c9a7b-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="c9a7b-166">Požadavek na nabídku</span><span class="sxs-lookup"><span data-stu-id="c9a7b-166">Request for quotation</span></span>
    - <span data-ttu-id="c9a7b-167">Záhlaví požadavku na nabídku – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="c9a7b-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="c9a7b-168">Řádek požadavku na nabídku – vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="c9a7b-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="c9a7b-169">Proces zásob</span><span class="sxs-lookup"><span data-stu-id="c9a7b-169">Inventory process</span></span>

    - <span data-ttu-id="c9a7b-170">Převodní příkaz – expedice</span><span class="sxs-lookup"><span data-stu-id="c9a7b-170">Transfer order – ship</span></span>
    - <span data-ttu-id="c9a7b-171">Převodní příkaz – příjem</span><span class="sxs-lookup"><span data-stu-id="c9a7b-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="c9a7b-172">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="c9a7b-172">Related resources</span></span>

[<span data-ttu-id="c9a7b-173">Začínáme s daňovou službou</span><span class="sxs-lookup"><span data-stu-id="c9a7b-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="c9a7b-174">Vícenásobné daňové identifikační číslo</span><span class="sxs-lookup"><span data-stu-id="c9a7b-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="c9a7b-175">Podpora daňové funkce u převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="c9a7b-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="c9a7b-176">Jak vytvořit rozšíření v daňové službě</span><span class="sxs-lookup"><span data-stu-id="c9a7b-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
