---
title: Intrastat - přehled
description: Toto téma obsahuje informace o vykazování Intrastat pro obchodování se zbožím a v některých případech mezi zeměmi/oblastmi Evropské unie (EU). Poskytuje přehled o procesu vykazování a popisuje požadované nastavení a požadavky.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8447cb644e7fe0a5ed55fd08091f42a57341f790
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212960"
---
# <a name="intrastat-overview"></a><span data-ttu-id="0e23d-104">Intrastat - přehled</span><span class="sxs-lookup"><span data-stu-id="0e23d-104">Intrastat overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e23d-105">Toto téma obsahuje informace o vykazování Intrastat pro obchodování se zbožím a v některých případech mezi zeměmi/oblastmi Evropské unie (EU).</span><span class="sxs-lookup"><span data-stu-id="0e23d-105">This topic provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="0e23d-106">Poskytuje přehled o procesu vykazování a popisuje požadované nastavení a požadavky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="0e23d-107">Intrastat je systém pro shromažďování informací a generování statistik o obchodování se zbožím mezi zeměmi/oblastmi Evropské unie (EU).</span><span class="sxs-lookup"><span data-stu-id="0e23d-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="0e23d-108">Vykazování v systému Intrastat je požadováno vždy, když produkt překročí hranice jiné země nebo oblasti v rámci EU.</span><span class="sxs-lookup"><span data-stu-id="0e23d-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="0e23d-109">V některých zemích či oblastech platí povinnost vykazování v systému Intrastat také pro služby.</span><span class="sxs-lookup"><span data-stu-id="0e23d-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="0e23d-110">V sestavách v systému Intrastat lze shromažďovat povinné i volitelné prvky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="0e23d-111">Následující prvky jsou povinné: identifikátor pro daň z přidané hodnoty (DPH) strany zodpovědné za poskytnutí informací, referenční období, tok (doručení nebo odeslání), číselný kód zboží, členský stát partnera (členský stát dodání při příjmu a členský stát pro cíl výdeje), hodnota zboží, množství zboží (čisté hmotnosti a doplňující jednotka) a druh transakce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="0e23d-112">Země či oblasti mohou za různých podmínek shromažďovat také volitelné prvky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="0e23d-113">Mezi volitelné prvky patří země/oblast původu, dodací podmínky, způsob dopravy, podrobnější kód zboží než CN8, oblast původu pro výdej a oblast určení na příjmu, statistická hodnota, popis zboží a přístav/letiště nakládky a vykládky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="0e23d-114">Přehled procesu vykazování v systému Intrastat</span><span class="sxs-lookup"><span data-stu-id="0e23d-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="0e23d-115">V následujících částech je popsán celkový tok informací, které se používají k vykazování v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="0e23d-116">1. Zadání transakce, která překračuje hranice jiné země nebo oblasti EU</span><span class="sxs-lookup"><span data-stu-id="0e23d-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="0e23d-117">Faktura odběratele, faktura s volným textem, nákupní faktura, faktura projektu, dodací list odběratele, příjemka produktu dodavatele nebo převodní příkaz je převeden do deníku systému Intrastat pouze v případě, že je typ země/oblast cíle (na výdeji) nebo místo určení (na příjmu) **EU**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="0e23d-118">Tato funkce byla v aplikaci Microsoft Dynamics 365 for Operations (verze 1611) rozšířena a umožňuje zadat adresy nakládky pro intrakomunitární transakce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="0e23d-119">Pokud se liší adresa přepravních dokladů dodavatele od obchodní adresy (nebo obchodní adresy zákazníka pro objednávku vratky), bude hlášení Intrastat pracovat s těmito informacemi.</span><span class="sxs-lookup"><span data-stu-id="0e23d-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="0e23d-120">Při vytvoření prodejní objednávky, faktury s volným textem, nákupní objednávky, faktury dodavatele, faktury projektu nebo převodního příkazu mají některá pole, která souvisejí se zahraničním obchodem, výchozí hodnoty v záhlaví dokumentu nebo na řádku.</span><span class="sxs-lookup"><span data-stu-id="0e23d-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="0e23d-121">Výchozí kód transakce je převzat z odpovídajícího pole na stránce **Parametry zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="0e23d-122">Výchozí kód komodity, země/oblast původu a stát/provincie původu jsou převzaty z položky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="0e23d-123">Výchozí hodnoty lze změnit a také můžete vyplnit další informace související se zahraničním obchodem: statistickou proceduru, způsob přepravy a přístav.</span><span class="sxs-lookup"><span data-stu-id="0e23d-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="0e23d-124">2. Použití deníku v systému Intrastat k vygenerování informací o obchodu mezi zeměmi/oblastmi EU</span><span class="sxs-lookup"><span data-stu-id="0e23d-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="0e23d-125">Každý měsíc generujete pro statistické účely informace o obchodu mezi zeměmi/oblastmi EU.</span><span class="sxs-lookup"><span data-stu-id="0e23d-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="0e23d-126">Můžete převést transakce z faktury s volným textem, faktury odběratele, dodacího listu odběratele, faktury dodavatele, dodacího listu dodavatele, faktury projektu nebo převodního příkazu podle kritérií převodu, která jsou nastavena na stránce **Parametry zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="0e23d-127">Případně můžete zadat transakci ručně.</span><span class="sxs-lookup"><span data-stu-id="0e23d-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="0e23d-128">Je-li nutné upravit některé údaje, můžete převedené transakce v deníku systému Intrastat ručně aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="0e23d-129">Za určitých podmínek, které jsou nastaveny na stránce **Komprese pro systém Intrastat**, můžete transakce v deníku systému Intrastat komprimovat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="0e23d-130">U některých zemí či oblastí lze aplikovat práh malé transakce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="0e23d-131">Transakce pod tuto prahovou hodnotu tak můžete vykazovat pod určeným kódem komodity.</span><span class="sxs-lookup"><span data-stu-id="0e23d-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="0e23d-132">Kód komodity lze upravit na příslušných řádcích deníku systému Intrastat na základě nastavení **Minimální limit** na stránce **Parametry zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="0e23d-133">Tyto transakce je možné také komprimovat podle nastavení **Komprese pro systém Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="0e23d-134">Úplnost transakce v deníku systému Intrastat můžete ověřit na základě nastavení **Zkontrolovat nastavení** na stránce **Parametry zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="0e23d-135">Úplnost dat v odpovídajících polích může být ověřena: země/oblast, stát nebo provincie, hmotnost, kód komodity, kód transakce, dodatečná jednotka, přístav, původ, podmínky dodání, způsob přepravy a číslo osvobození od daně.</span><span class="sxs-lookup"><span data-stu-id="0e23d-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="0e23d-136">Nedokončené transakce budou označeny jako neplatné.</span><span class="sxs-lookup"><span data-stu-id="0e23d-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="0e23d-137">3. Použití deníku v systému Intrastat k vykázání informací o obchodu mezi zeměmi/oblastmi EU</span><span class="sxs-lookup"><span data-stu-id="0e23d-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="0e23d-138">Každý měsíc vykazujete pro statistické účely informace o obchodu mezi zeměmi/oblastmi EU.</span><span class="sxs-lookup"><span data-stu-id="0e23d-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="0e23d-139">Můžete vytisknout sestavy systému Intrastat na základě nastavení **Mapování formátu sestavy** na stránce **Parametry zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="0e23d-140">Také můžete vytvořit elektronický soubor na základě nastavení **Mapování formátu souboru** na stránce **Parametry zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="0e23d-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="0e23d-141">Další informace o souhrnném hlášení Intrastat, včetně požadovaných předpokladů naleznete na stránce souhrnného hlášení Intrastat:</span><span class="sxs-lookup"><span data-stu-id="0e23d-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="0e23d-142">Generování prohlášení Intrastat EU,</span><span class="sxs-lookup"><span data-stu-id="0e23d-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="0e23d-143">Přenos transakcí do systému Intrastat,</span><span class="sxs-lookup"><span data-stu-id="0e23d-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="0e23d-144">Zadání adresy nakládky pro interní transakci.</span><span class="sxs-lookup"><span data-stu-id="0e23d-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0e23d-145">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="0e23d-145">Prerequisites</span></span>
<span data-ttu-id="0e23d-146">V následující tabulce jsou uvedeny předpoklady pro vykazování v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e23d-147">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="0e23d-147">Prerequisite</span></span></th>
<th><span data-ttu-id="0e23d-148">Popis</span><span class="sxs-lookup"><span data-stu-id="0e23d-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e23d-149">Nastavení adresy</span><span class="sxs-lookup"><span data-stu-id="0e23d-149">Address setup</span></span></td>
<td><span data-ttu-id="0e23d-150">Nastavte kód země nebo oblasti používaný Mezinárodní organizací pro normalizaci (ISO).</span><span class="sxs-lookup"><span data-stu-id="0e23d-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-151">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="0e23d-151">Legal entity</span></span></td>
<td><span data-ttu-id="0e23d-152">Nastavte číslo osvobození od daně pro import či export, rozšíření DIČ pobočky pro import/export a kód systému Intrastat, který je přiřazen k právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="0e23d-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e23d-153">Hierarchie kategorií produktů (prodejní hierarchie, hierarchie zásobování)</span><span class="sxs-lookup"><span data-stu-id="0e23d-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="0e23d-154">Na kartě <strong>Kódy komodit</strong> na stránce <strong>Hierarchie kategorií</strong> přiřaďte kódy komodit v systému Intrastat k uzlům kategorií.</span><span class="sxs-lookup"><span data-stu-id="0e23d-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="0e23d-155">Když přiřadíte kód komodity k nadřazenému uzlu kategorie, lze kód použít pro všechny podřízené uzly kategorií.</span><span class="sxs-lookup"><span data-stu-id="0e23d-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="0e23d-156">Vybrané kódy komodit budou dostupné v zobrazení <strong>Vybrané</strong>, pokud daný kód komodity vyberete v podrobnostech o uvolněném produktu, na prodejní objednávce, na nákupní objednávce a na řádcích převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="0e23d-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the released product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-157">Podrobnosti o uvolněném produktu</span><span class="sxs-lookup"><span data-stu-id="0e23d-157">Released product details</span></span></td>
<td><span data-ttu-id="0e23d-158">Pro uvolněné produkty nastavte tato data zahraničního obchodu:</span><span class="sxs-lookup"><span data-stu-id="0e23d-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="0e23d-159"><strong>Kód komodity</strong> – vyberte buď seznam vybraných komodit získaný z kategorie přiřazené produktu, nebo celý seznam kódů komodit v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="0e23d-160"><strong>Statistické procento nákladů</strong></span><span class="sxs-lookup"><span data-stu-id="0e23d-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="0e23d-161"><strong>Země/oblast původu</strong> – vyberte výchozí zemi nebo oblast, kde bylo zboží zcela získáno nebo vyrobeno.</span><span class="sxs-lookup"><span data-stu-id="0e23d-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="0e23d-162"><strong>Stát/provincie původu/určení</strong> – vyberte výchozí stát/provincii určení a stát/provincii původu zásilky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="0e23d-163"><strong>Čistá hmotnost v kg</strong></span><span class="sxs-lookup"><span data-stu-id="0e23d-163"><strong>Net weight in kg</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e23d-164">Zákazníci</span><span class="sxs-lookup"><span data-stu-id="0e23d-164">Customers</span></span></td>
<td><span data-ttu-id="0e23d-165">Nastavte dodací adresu odběratele v zemi/regionu EU.</span><span class="sxs-lookup"><span data-stu-id="0e23d-165">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-166">Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="0e23d-166">Vendors</span></span></td>
<td><span data-ttu-id="0e23d-167">Nastavte adresu dodavatele v zemi/regionu EU.</span><span class="sxs-lookup"><span data-stu-id="0e23d-167">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e23d-168">Vedlejší náklady</span><span class="sxs-lookup"><span data-stu-id="0e23d-168">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="0e23d-169">Nastavte, zda se má kód vedlejších nákladů zahrnout do fakturované částky, statistické částky, nebo do obou částek.</span><span class="sxs-lookup"><span data-stu-id="0e23d-169">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="0e23d-170">Na stránce <strong>Kódy nákladů</strong> na kartě <strong>Zahraniční obchod</strong> kartu povolte, aby <strong>Hodnota faktury Intrastat</strong> zahrnovala částku nákladů v hodnotě faktury a aby <strong>Statistická hodnota Intrastat</strong> zahrnovala částku nákladů ve statistické hodnotě.</span><span class="sxs-lookup"><span data-stu-id="0e23d-170">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-171">Elektronické výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0e23d-171">Electronic reporting</span></span></td>
<td><span data-ttu-id="0e23d-172">Upravte konfiguraci elektronického vykazování tak, aby se data ze systému Intrastat exportovala do elektronického souboru v takovém formátu, který je vyžadován příslušnými orgány, a aby se tato data zobrazovala v uživatelsky přívětivém a čitelném formátu (například v aplikaci Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="0e23d-172">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-173">Sklady</span><span class="sxs-lookup"><span data-stu-id="0e23d-173">Warehousing</span></span></td>
<td><span data-ttu-id="0e23d-174">Přidružte účty dodavatele ke kódům skladu pro vyplnění čísla osvobození od daně při převodu převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="0e23d-174">Associate vendor accounts with warehouse codes for filling tax exempt number when transferring Transfer order.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="0e23d-175">Nastavení</span><span class="sxs-lookup"><span data-stu-id="0e23d-175">Setup</span></span>
<span data-ttu-id="0e23d-176">V následujících částech je popsáno nastavení, které je nutné pro vykazování v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-176">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="0e23d-177">Nastavení všech požadovaných seznamů souvisejících se systémem Intrastat</span><span class="sxs-lookup"><span data-stu-id="0e23d-177">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e23d-178">Seznam</span><span class="sxs-lookup"><span data-stu-id="0e23d-178">List</span></span></th>
<th><span data-ttu-id="0e23d-179">Doplňkové informace</span><span class="sxs-lookup"><span data-stu-id="0e23d-179">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e23d-180">Kódy komodit</span><span class="sxs-lookup"><span data-stu-id="0e23d-180">Commodity codes</span></span></td>
<td><span data-ttu-id="0e23d-181">Nastavte hierarchii kategorií typu <strong>Kód komodity</strong> a zadejte všechny kódy komodit podle seznamu kombinované nomenklatury.</span><span class="sxs-lookup"><span data-stu-id="0e23d-181">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="0e23d-182">Pro každou komoditu nastavte tyto informace:</span><span class="sxs-lookup"><span data-stu-id="0e23d-182">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="0e23d-183">Název komodity a kód komodity</span><span class="sxs-lookup"><span data-stu-id="0e23d-183">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="0e23d-184">Popisný název a/nebo přeložený název</span><span class="sxs-lookup"><span data-stu-id="0e23d-184">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="0e23d-185">Nastavení pro vykazování dalších (doplňkových) jednotek na kartě <strong>Zahraniční obchod</strong>. Dodatečné jednotky můžete vybrat v seznamu jednotek.</span><span class="sxs-lookup"><span data-stu-id="0e23d-185">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab. You can select the additional unit in the unit list.</span></span> <span data-ttu-id="0e23d-186">Můžete také určit, zda musí být společně se zvolenou dodatečnou jednotkou uvedena také hmotnost komodit.</span><span class="sxs-lookup"><span data-stu-id="0e23d-186">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-187">Kódy transakce</span><span class="sxs-lookup"><span data-stu-id="0e23d-187">Transaction codes</span></span></td>
<td><span data-ttu-id="0e23d-188">Podle požadavků vaší země nebo oblasti nastavte druh transakce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-188">Set up the nature of the transaction according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="0e23d-189">Pro každý kód transakce, který nastavíte, je nutné nastavit pravidla pro výpočet fakturované částky a statistické částky pro převodní příkazy a prodejní nebo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-189">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="0e23d-190">U převodních příkazů můžete nastavit některé z následujících pravidel pro výpočet částky faktury a statistických částek:</span><span class="sxs-lookup"><span data-stu-id="0e23d-190">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="0e23d-191"><strong>Prázdné</strong> – částka bude mít hodnotu 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="0e23d-191"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="0e23d-192"><strong>Částka finančních nákladů</strong> – částka se bude rovnat finančním nákladům.</span><span class="sxs-lookup"><span data-stu-id="0e23d-192"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="0e23d-193"><strong>Celkové náklady</strong> – částka se bude rovnat celkovým nákladům transakce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-193"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="0e23d-194"><strong>Ruční</strong> – částka se bude rovnat ručně zadané částce na řádku převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="0e23d-194"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="0e23d-195">U prodejních a nákupních objednávek můžete nastavit některé z následujících pravidel pro výpočet fakturovaných částek a statistických částek:</span><span class="sxs-lookup"><span data-stu-id="0e23d-195">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="0e23d-196"><strong>Prázdné</strong> – částka bude mít hodnotu 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="0e23d-196"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="0e23d-197"><strong>Fakturovaná částka</strong> – částka se bude rovnat částce fakturované pro komoditu.</span><span class="sxs-lookup"><span data-stu-id="0e23d-197"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="0e23d-198"><strong>Základní částka</strong> – částka se bude rovnat fakturované částce před uplatněním slevy.</span><span class="sxs-lookup"><span data-stu-id="0e23d-198"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e23d-199">Způsoby přepravy</span><span class="sxs-lookup"><span data-stu-id="0e23d-199">Transport methods</span></span></td>
<td><span data-ttu-id="0e23d-200">Podle požadavků vaší země nebo oblasti nastavte režim přepravy.</span><span class="sxs-lookup"><span data-stu-id="0e23d-200">Set up the transport mode according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="0e23d-201">Pro každý způsob dodání můžete na kartě <strong>Zahraniční obchod</strong> nastavit výchozí způsob přepravy.</span><span class="sxs-lookup"><span data-stu-id="0e23d-201">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-202">Přístavy</span><span class="sxs-lookup"><span data-stu-id="0e23d-202">Ports</span></span></td>
<td><span data-ttu-id="0e23d-203">Pokud je tato informace vaší zemí nebo oblastí shromažďována, nastavte přístav/letiště nakládky/vykládky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-203">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e23d-204">Statistické procedury</span><span class="sxs-lookup"><span data-stu-id="0e23d-204">Statistics procedures</span></span></td>
<td><span data-ttu-id="0e23d-205">Pokud je tato informace vaší zemí nebo oblastí shromažďována, nastavte statistickou proceduru.</span><span class="sxs-lookup"><span data-stu-id="0e23d-205">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="0e23d-206">Nastavení pravidel pro kompresi transakcí v systému Intrastat</span><span class="sxs-lookup"><span data-stu-id="0e23d-206">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="0e23d-207">Na stránce **Komprese pro systém Intrastat** můžete vybrat pole, která mají být použita pro kompresi.</span><span class="sxs-lookup"><span data-stu-id="0e23d-207">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="0e23d-208">Všechny transakce se stejnou kombinací hodnoty pro pole vybraná v deníku systému Intrastat budou při spuštění funkce komprese v deníku systému Intrastat komprimovány do jedné transakce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-208">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="0e23d-209">Nastavit parametry zahraničního obchodu</span><span class="sxs-lookup"><span data-stu-id="0e23d-209">Set up foreign trade parameters</span></span>

<span data-ttu-id="0e23d-210">Stránka **Parametry zahraničního obchodu** slouží k nastavení parametrů uvedených v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-210">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e23d-211">Karta</span><span class="sxs-lookup"><span data-stu-id="0e23d-211">Tab</span></span></th>
<th><span data-ttu-id="0e23d-212">Parametry</span><span class="sxs-lookup"><span data-stu-id="0e23d-212">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e23d-213">Obecné</span><span class="sxs-lookup"><span data-stu-id="0e23d-213">General</span></span></td>
<td><ul>
<li><span data-ttu-id="0e23d-214"><strong>Obecné</strong> – zadejte tyto informace:</span><span class="sxs-lookup"><span data-stu-id="0e23d-214"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="0e23d-215">Výchozí kódy transakce pro prodejní objednávky, nákupní objednávky, dobropisy a převodní příkazy.</span><span class="sxs-lookup"><span data-stu-id="0e23d-215">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="0e23d-216">Kód transakce, který je nastaven pro dobropisy, slouží také jako kód vrácení fyzického zboží a používá se pro odchylky fyzických vratek vůči opravám dobropisů.</span><span class="sxs-lookup"><span data-stu-id="0e23d-216">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span> <span data-ttu-id="0e23d-217">Vrácení fyzického zboží se vykazuje v převodu Intrastat jiným směrem.</span><span class="sxs-lookup"><span data-stu-id="0e23d-217">Returns of physical goods are reported in Intrastat transfer with a different direction.</span></span> <span data-ttu-id="0e23d-218">Vrácení při doručení je vykázáno jako odeslání a vrácení při odeslání je vykázáno jako doručení.</span><span class="sxs-lookup"><span data-stu-id="0e23d-218">The return of arrival is reported as dispatch and the return of dispatch is reported as arrival.</span></span></li>
<li><span data-ttu-id="0e23d-219">Zaměstnanec, který je zodpovědný za přípravu sestav v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-219">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="0e23d-220"><strong>Minimální limit</strong> – určete nastavení pro aktualizaci transakcí, které jsou pod prahovou hodnotu:</span><span class="sxs-lookup"><span data-stu-id="0e23d-220"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="0e23d-221">Prahové částka a hmotnost</span><span class="sxs-lookup"><span data-stu-id="0e23d-221">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="0e23d-222">Kód komodity, který se použije pro transakce spadající pod prahovou hodnotu</span><span class="sxs-lookup"><span data-stu-id="0e23d-222">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="0e23d-223"><strong>Přenos</strong> – určete kritéria pro přenos transakcí do deníku systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-223"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="0e23d-224">Můžete nastavit, aby se transakce přenášely pouze v případě, že budou položky splňovat všechna tato kritéria:</span><span class="sxs-lookup"><span data-stu-id="0e23d-224">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="0e23d-225">Nejedná se o servisní položky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-225">The items aren&#39;t service items.</span></span></li>
<li><span data-ttu-id="0e23d-226">Položky mají kód komodity.</span><span class="sxs-lookup"><span data-stu-id="0e23d-226">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="0e23d-227">Položky mají hmotnost.</span><span class="sxs-lookup"><span data-stu-id="0e23d-227">The items have a weight.</span></span></li>
<li><span data-ttu-id="0e23d-228">Položky mají dodatečné jednotky.</span><span class="sxs-lookup"><span data-stu-id="0e23d-228">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="0e23d-229"><strong>Zkontrolovat nastavení</strong> – určete pravidla pro ověření úplnosti dat v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-229"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="0e23d-230">Můžete vybrat data, která budou ověřována.</span><span class="sxs-lookup"><span data-stu-id="0e23d-230">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="0e23d-231"><strong>Pravidla zaokrouhlování</strong> – upravte následující nastavení pro zaokrouhlování částek a hmotností v sestavách v systému Intrastat:</span><span class="sxs-lookup"><span data-stu-id="0e23d-231"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="0e23d-232">Pravidlo zaokrouhlování (přesnost)</span><span class="sxs-lookup"><span data-stu-id="0e23d-232">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="0e23d-233">Metoda zaokrouhlování: nahoru, dolů nebo normální</span><span class="sxs-lookup"><span data-stu-id="0e23d-233">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="0e23d-234">Počet desetinných míst pro částky a hmotnosti</span><span class="sxs-lookup"><span data-stu-id="0e23d-234">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="0e23d-235">Pokyny pro zaokrouhlování hmotnosti, které jsou nižší než 1 kilogram (kg): nahoru na 1 kg, normální nebo bez zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="0e23d-235">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="0e23d-236"><strong>Elektronické výkaznictví</strong> – určete odkazy na konfigurace elektronického vykazování, abyste mohli vygenerovat elektronický soubor a sestavu.</span><span class="sxs-lookup"><span data-stu-id="0e23d-236"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="0e23d-237"><strong>Hierarchie kódů komodit</strong> – zadejte hierarchie kategorií typu <strong>Kód komodity</strong>, který představuje kód komodity CN8 v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-237"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
  <li> <span data-ttu-id="0e23d-238"><strong>Typ směnného kurzu</strong> – Volitelně můžete zadat směnný kurz, který se bude používat pro vykazování prodejů Intrastat a prodejních a nákupních transakcí v cizích měnách.</span><span class="sxs-lookup"><span data-stu-id="0e23d-238"><strong>Exchange rate type</strong> – Optionally, specify an exchange rate to be used to report Intrastat sales and purchase transactions in foreign currencies.</span></span> <span data-ttu-id="0e23d-239">Používá se, pokud je cena jiná než cena použitá při zaúčtování transakce.</span><span class="sxs-lookup"><span data-stu-id="0e23d-239">This is used if the rate is different than the one applied when posting the transaction.</span></span></li>  
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-240">Kontaktní informace o zástupci</span><span class="sxs-lookup"><span data-stu-id="0e23d-240">Agent contact information</span></span></td>
<td><span data-ttu-id="0e23d-241">Zadejte jméno zástupce, jeho adresu, číslo osvobození od daně, telefonní číslo a číslo faxu.</span><span class="sxs-lookup"><span data-stu-id="0e23d-241">Specify the agent&#39;s name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e23d-242">Vlastnosti země/oblasti</span><span class="sxs-lookup"><span data-stu-id="0e23d-242">Country/region properties</span></span></td>
<td><span data-ttu-id="0e23d-243">Nastavte zemi/oblast aktuální právnické osoby na hodnotu <strong>Domácí</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e23d-243">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="0e23d-244">Nastavte zemi/oblasti zemí či oblastí EU, které se účastní obchodu v rámci EU, s aktuální právnickou osobou na hodnotu <strong>EU</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e23d-244">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="0e23d-245">Pro každou zemi/oblast určete také kód země/oblasti pro účely zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="0e23d-245">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e23d-246">Číselná řada</span><span class="sxs-lookup"><span data-stu-id="0e23d-246">Number sequence</span></span></td>
<td><span data-ttu-id="0e23d-247">Zadejte číselnou řadu pro deník systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e23d-247">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]