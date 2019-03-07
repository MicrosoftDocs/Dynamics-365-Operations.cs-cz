---
title: Automatizace faktur dodavatele
description: Toto téma popisuje funkce, které jsou k dispozici pro celkovou automatizaci dodavatelských faktur, a to dokonce i faktur, které obsahují přílohy.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ea483a82b8215f0e6d8f420c007da349313daa5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "324507"
---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="efa3b-103">Automatizace faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="efa3b-103">Vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efa3b-104">Toto téma popisuje funkce, které jsou k dispozici pro celkovou automatizaci dodavatelských faktur, a to dokonce i faktur, které obsahují přílohy.</span><span class="sxs-lookup"><span data-stu-id="efa3b-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="efa3b-105">Organizace, které chtějí usnadnit své procesy v oblasti závazků (AP), často identifikují zpracování faktury jako jeden z hlavních procesních oblastí, které by měly být efektivnější.</span><span class="sxs-lookup"><span data-stu-id="efa3b-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="efa3b-106">V mnoha případech organizace svěřují zpracování papírových faktur nezávislým poskytovatelům služeb optického rozpoznávání znaků (OCR).</span><span class="sxs-lookup"><span data-stu-id="efa3b-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="efa3b-107">Poté obdrží strojově čitelná metadata faktury spolu s naskenovaným obrázkem jednotlivých faktur.</span><span class="sxs-lookup"><span data-stu-id="efa3b-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="efa3b-108">Na pomoc s automatizací je pak k dispozici řešení na poslední chvíli, které umožňuje spotřebu těchto artefaktů ve fakturačním systému.</span><span class="sxs-lookup"><span data-stu-id="efa3b-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="efa3b-109">Microsoft Dynamics 365 for Finance and Operations umožňuje nyní vydání této automatizace na poslední chvíli prostřednictvím řešení automatizace faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-109">Microsoft Dynamics 365 for Finance and Operations now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="efa3b-110">Kontext řešení</span><span class="sxs-lookup"><span data-stu-id="efa3b-110">Solution context</span></span>

<span data-ttu-id="efa3b-111">Automatické řešení faktur má standardní rozhraní, které přijímá metadata faktury pro hlavičku faktury a řádky faktury, a také přílohy použitelné u faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="efa3b-112">Jakýkoli externí systém, který dokáže generovat artefakty vyhovující tomuto rozhraní, bude moci odesílat informační kanál do aplikace Finance and Operations k automatickému zpracování faktur a příloh.</span><span class="sxs-lookup"><span data-stu-id="efa3b-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="efa3b-113">Následující obrázek znázorňuje scénář integrace vzorku, kde se společnost Contoso stala partnerem poskytovatele služeb OCR ke zpracování faktur dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="efa3b-114">Dodavatelé společnosti Contoso odesílají faktury poskytovateli služeb e-mailem.</span><span class="sxs-lookup"><span data-stu-id="efa3b-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="efa3b-115">Prostřednictvím zpracování OCR poskytovatel služby generuje metadata faktury (záhlaví a řádky) a naskenovanou kopii faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="efa3b-116">Vrstva integrace pak transformuje tyto artefakty tak, aby je bylo možné používat v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="efa3b-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![Vzorový scénář integrace](media/vendor_invoice_automation_01.png)

<span data-ttu-id="efa3b-118">Předchozí scénář umožňuje několik variant v případě, že je nutná integrace faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="efa3b-119">Migrace dat představuje jiný příklad použití tohoto rozhraní k vytvoření faktur a příloh faktur v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="efa3b-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="efa3b-120">Komponenty řešení</span><span class="sxs-lookup"><span data-stu-id="efa3b-120">Solution components</span></span>

<span data-ttu-id="efa3b-121">Řešení obsahuje následující součásti:</span><span class="sxs-lookup"><span data-stu-id="efa3b-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="efa3b-122">Datové entity pro záhlaví faktury, řádky faktury a přílohy faktury</span><span class="sxs-lookup"><span data-stu-id="efa3b-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="efa3b-123">Zpracování výjimek u faktur</span><span class="sxs-lookup"><span data-stu-id="efa3b-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="efa3b-124">Prohlížeč příloh faktur vedle sebe</span><span class="sxs-lookup"><span data-stu-id="efa3b-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="efa3b-125">Zbývající část tohoto tématu obsahuje podrobné popisy těchto komponent řešení.</span><span class="sxs-lookup"><span data-stu-id="efa3b-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="efa3b-126">Datové entity</span><span class="sxs-lookup"><span data-stu-id="efa3b-126">Data entities</span></span>

<span data-ttu-id="efa3b-127">Datový balík je jednotka práce, které musí být odeslána do modulu Finance and Operations, aby bylo možné vytvořit záhlaví faktury, řádky faktury a přílohy faktur.</span><span class="sxs-lookup"><span data-stu-id="efa3b-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="efa3b-128">Následující datové entity se používají pro artefakty tvořících datový balíček:</span><span class="sxs-lookup"><span data-stu-id="efa3b-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="efa3b-129">Záhlaví faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="efa3b-129">Vendor invoice header</span></span>
+ <span data-ttu-id="efa3b-130">Řádek dodavatelské faktury</span><span class="sxs-lookup"><span data-stu-id="efa3b-130">Vendor invoice line</span></span>
+ <span data-ttu-id="efa3b-131">Příloha dokumentu faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="efa3b-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="efa3b-132">Příloha dokumentu faktury dodavatele je nová datová entita, která je zavedena jako součást této funkce.</span><span class="sxs-lookup"><span data-stu-id="efa3b-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="efa3b-133">Entita v záhlaví faktury dodavatele byla upravena tak, aby podporovala přílohy.</span><span class="sxs-lookup"><span data-stu-id="efa3b-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="efa3b-134">Entita řádku faktury dodavatele pro tuto funkci nebyla změněna.</span><span class="sxs-lookup"><span data-stu-id="efa3b-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="efa3b-135">Toto téma neposkytuje podrobnou definici datového balíku.</span><span class="sxs-lookup"><span data-stu-id="efa3b-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="efa3b-136">Také nevysvětluje, jak vytvářet datové balíčky.</span><span class="sxs-lookup"><span data-stu-id="efa3b-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="efa3b-137">Tyto informace lze najít v tématu [Systém datových entit a balíčků](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="efa3b-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="efa3b-138">Chcete-li rychle generovat testovací data, která zahrnují faktury a přílohy, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="efa3b-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="efa3b-139">Přihlaste se k instanci aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="efa3b-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="efa3b-140">Přejděte na **Závazky** > **Faktury** > **Otevřít faktury dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="efa3b-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="efa3b-141">Vytvořte faktury, které mají řádky a přílohy.</span><span class="sxs-lookup"><span data-stu-id="efa3b-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efa3b-142">Přílohy musí být přílohy záhlaví.</span><span class="sxs-lookup"><span data-stu-id="efa3b-142">The attachments must be header attachments.</span></span> <span data-ttu-id="efa3b-143">V současné době entita přílohy dokumentu dodavatelské faktury nepodporuje přílohy řádků.</span><span class="sxs-lookup"><span data-stu-id="efa3b-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="efa3b-144">Otevřete pracovní prostor **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="efa3b-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="efa3b-145">Vytvořte úlohu exportu, která obsahuje záhlaví faktury dodavatele, řádku faktury dodavatele a entity příloh dokumentu faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="efa3b-146">Exportujte data.</span><span class="sxs-lookup"><span data-stu-id="efa3b-146">Export the data.</span></span>
1. <span data-ttu-id="efa3b-147">Stáhněte exportovaná data jako balíček.</span><span class="sxs-lookup"><span data-stu-id="efa3b-147">Download the exported data as a package.</span></span> <span data-ttu-id="efa3b-148">Nyní můžete balíček použít k importu dat do cílových instancí pro účely testování.</span><span class="sxs-lookup"><span data-stu-id="efa3b-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="efa3b-149">Určení právnické osoby faktury</span><span class="sxs-lookup"><span data-stu-id="efa3b-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="efa3b-150">Faktury importované pomocí datových balíčků lze přidružit k právnické osobě, ke které patří, dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="efa3b-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="efa3b-151">Úloha importu, která fakturu zpracovává, ji importuje do stejné společnosti, ve které byla úloha naplánována v pracovním prostoru **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="efa3b-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="efa3b-152">Jinými slovy společnost úlohy určuje společnost, do které faktura patří.</span><span class="sxs-lookup"><span data-stu-id="efa3b-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="efa3b-153">Při odeslání datového balíčku obsahujícího faktury do aplikace Finance and Operations může volající (tedy aplikace integrace běžící mimo Finance and Operations) explicitně zmínit ID společnosti v požadavku HTTP</span><span class="sxs-lookup"><span data-stu-id="efa3b-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="efa3b-154">V tomto případě bude kontext společnosti, ve kterém je úloha zpracování spuštěná v modulu Finance and Operations, přepsán a faktury jsou importovány do společnosti, která byla předána v požadavku HTTP.</span><span class="sxs-lookup"><span data-stu-id="efa3b-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="efa3b-155">Toto chování je standardní chování správy dat.</span><span class="sxs-lookup"><span data-stu-id="efa3b-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="efa3b-156">Je zde vysvětleno v kontextu faktur jenom pro úplnost.</span><span class="sxs-lookup"><span data-stu-id="efa3b-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="efa3b-157">Zpracování výjimky</span><span class="sxs-lookup"><span data-stu-id="efa3b-157">Exception processing</span></span>

<span data-ttu-id="efa3b-158">V situacích, kdy faktury dodavatele přecházejí do aplikace Finance and Operations prostřednictvím integrace, musí existovat jednoduchý způsob zpracování výjimek nebo neúspěšných faktur členem týmu modulu Závazky a k vytvoření čekajících faktur mimo neúspěšné faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="efa3b-159">Toto zpracování výjimek pro faktury dodavatele je nyní součástí modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="efa3b-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="efa3b-160">Stránka seznamu výjimek</span><span class="sxs-lookup"><span data-stu-id="efa3b-160">Exceptions list page</span></span>

<span data-ttu-id="efa3b-161">Stránka s novým seznamem výjimek faktur je k dispozici zde: **Závazky** > **Faktury** > **Selhání importu** > **Dodavatelské faktury, které se nepodařilo importovat**.</span><span class="sxs-lookup"><span data-stu-id="efa3b-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="efa3b-162">Na této stránce se zobrazují všechny záznamy v záhlaví dodavatelské faktury z tabulky fázování entity dat záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="efa3b-163">Všimněte si, že můžete zobrazit stejné záznamy z pracovního prostoru **Správa dat**, kde můžete provést stejné akce, které jsou k dispozici ve funkci zpracování výjimky.</span><span class="sxs-lookup"><span data-stu-id="efa3b-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="efa3b-164">Uživatelské rozhraní, které funkce zpracování výjimek poskytuje, je však optimalizováno pro funkčního uživatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Stránka seznamu výjimek](media/vendor_invoice_automation_02.png)

<span data-ttu-id="efa3b-166">Tato stránka seznamu zahrnuje následující pole, která se dodávají prostřednictvím kanálu:</span><span class="sxs-lookup"><span data-stu-id="efa3b-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="efa3b-167">**Společnost** – Společnost, které faktura náleží</span><span class="sxs-lookup"><span data-stu-id="efa3b-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="efa3b-168">**Chybová zpráva** – chybová zpráva, kterou vydává systém správy platformy k vysvětlení, proč nelze vytvořit fakturu</span><span class="sxs-lookup"><span data-stu-id="efa3b-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="efa3b-169">**Číslo** – číslo faktury</span><span class="sxs-lookup"><span data-stu-id="efa3b-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="efa3b-170">**Účet faktury**</span><span class="sxs-lookup"><span data-stu-id="efa3b-170">**Invoice account**</span></span>
+ <span data-ttu-id="efa3b-171">**Název** – Název dodavatele</span><span class="sxs-lookup"><span data-stu-id="efa3b-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="efa3b-172">**Účet dodavatele**</span><span class="sxs-lookup"><span data-stu-id="efa3b-172">**Vendor account**</span></span>
+ <span data-ttu-id="efa3b-173">**Nákupní objednávka** – Číslo nákupní objednávky pro vybranou fakturu</span><span class="sxs-lookup"><span data-stu-id="efa3b-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="efa3b-174">**Datum zaúčtování**</span><span class="sxs-lookup"><span data-stu-id="efa3b-174">**Posting date**</span></span>
+ <span data-ttu-id="efa3b-175">**Datum fakturace**</span><span class="sxs-lookup"><span data-stu-id="efa3b-175">**Invoice date**</span></span>
+ <span data-ttu-id="efa3b-176">**Popis faktury**</span><span class="sxs-lookup"><span data-stu-id="efa3b-176">**Invoice description**</span></span>
+ <span data-ttu-id="efa3b-177">**Měna**</span><span class="sxs-lookup"><span data-stu-id="efa3b-177">**Currency**</span></span>
+ <span data-ttu-id="efa3b-178">**Protokol**</span><span class="sxs-lookup"><span data-stu-id="efa3b-178">**Log**</span></span>
+ <span data-ttu-id="efa3b-179">**Reference na řádek** –Identifikátor, který pochází z externího systému</span><span class="sxs-lookup"><span data-stu-id="efa3b-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="efa3b-180">Odkaz na řádek není ID faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="efa3b-181">Tato stránka seznamu dále obsahuje podokno náhledu, které lze použít následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="efa3b-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="efa3b-182">Zobrazte celou chybovou zprávu, abyste nemuseli rozbalovat sloupec **Chybová zpráva** v mřížce.</span><span class="sxs-lookup"><span data-stu-id="efa3b-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="efa3b-183">Zobrazte celý seznam příloh faktury, pokud existují.</span><span class="sxs-lookup"><span data-stu-id="efa3b-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="efa3b-184">Stránka seznamu podporuje následující akce:</span><span class="sxs-lookup"><span data-stu-id="efa3b-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="efa3b-185">**Upravit** – otevřete záznam o výjimce v režimu úprav, abyste mohli opravit problémy.</span><span class="sxs-lookup"><span data-stu-id="efa3b-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="efa3b-186">**Možnosti** – přejděte ke standardním možnostem, které jsou k dispozici na stránkách seznamů.</span><span class="sxs-lookup"><span data-stu-id="efa3b-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="efa3b-187">Můžete použít možnost **Přidat do pracovního prostoru** pro připnutí stránky se seznamem výjimek jako seznamu nebo dlaždice.</span><span class="sxs-lookup"><span data-stu-id="efa3b-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="efa3b-188">Stránka podrobností o výjimce</span><span class="sxs-lookup"><span data-stu-id="efa3b-188">Exception details page</span></span>

<span data-ttu-id="efa3b-189">Při spuštění režimu úprav se zobrazí stránka podrobností výjimky pro fakturu s problémy.</span><span class="sxs-lookup"><span data-stu-id="efa3b-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="efa3b-190">Pokud existují nějaké přílohy, faktura a výchozí příloha se zobrazí vedle sebe na stránce Podrobnosti o výjimce.</span><span class="sxs-lookup"><span data-stu-id="efa3b-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Stránka podrobností o výjimce](media/vendor_invoice_automation_03.png)

<span data-ttu-id="efa3b-192">V předcházejícím ilustračním příkladu nebyly žádné řádky pro záhlaví faktury dodavatele, která byla dodána.</span><span class="sxs-lookup"><span data-stu-id="efa3b-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="efa3b-193">Oddíl pro řádky je tedy prázdný.</span><span class="sxs-lookup"><span data-stu-id="efa3b-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="efa3b-194">Stránka podrobností o výjimce podporuje následující operace:</span><span class="sxs-lookup"><span data-stu-id="efa3b-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="efa3b-195">**Vytvořit čekající fakturu** – po opravě problémů na faktuře v rámci zpracování výjimky můžete klepnutím na toto tlačítko vytvořit čekající fakturu.</span><span class="sxs-lookup"><span data-stu-id="efa3b-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="efa3b-196">Dojde k vytvoření čekajících faktur na pozadí (jako asynchronní operace).</span><span class="sxs-lookup"><span data-stu-id="efa3b-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="efa3b-197">Sdílené služby vs. zpracování výjimek organizace</span><span class="sxs-lookup"><span data-stu-id="efa3b-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="efa3b-198">Stránka seznamu výjimek podporuje standardní konstrukty zabezpečení, které pracovní prostor **Správa dat** podporuje pro zpracování záznamů fázování.</span><span class="sxs-lookup"><span data-stu-id="efa3b-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="efa3b-199">Úlohu importu faktury můžete zabezpečit následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="efa3b-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="efa3b-200">Podle role uživatele</span><span class="sxs-lookup"><span data-stu-id="efa3b-200">By user role</span></span>
+ <span data-ttu-id="efa3b-201">Podle uživatelů</span><span class="sxs-lookup"><span data-stu-id="efa3b-201">By user</span></span>
+ <span data-ttu-id="efa3b-202">Podle právnické osoby</span><span class="sxs-lookup"><span data-stu-id="efa3b-202">By legal entity</span></span>

![Úloha importu, která je zabezpečena pomocí role uživatele a právnické osoby](media/vendor_invoice_automation_04.png)

<span data-ttu-id="efa3b-204">Pokud je pro úlohu importu faktury nakonfigurované zabezpečení, stránka seznamu výjimek toto nastavení ocení.</span><span class="sxs-lookup"><span data-stu-id="efa3b-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="efa3b-205">Uživatelé budou moci zobrazit pouze záznamy výjimky faktury, které jim toto nastavení umožňuje zobrazit.</span><span class="sxs-lookup"><span data-stu-id="efa3b-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="efa3b-206">Společnost Contoso se například rozhodla pro zpracování výjimek faktury podle právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="efa3b-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="efa3b-207">Proto je nastavení u úlohy importu faktury nakonfigurováno tak, aby uživatel u právnické osoby A mohl zobrazit pouze výjimky faktury v právnické osobě A, zatímco uživatel v právnické osobě B může zobrazit pouze výjimky faktury v právnické osobě B. Toto nastavení umožňuje dělení zodpovědností pro správu výjimek faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="efa3b-208">Společnost Contoso by se také mohla rozhodnout, že nevynutí žádné zabezpečení, takže stejní uživatelé mohou zpracovávat výjimky faktury pro všechny právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="efa3b-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="efa3b-209">Toto nastavení umožňuje scénář sdílených služeb pro správu výjimek faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="efa3b-210">Prohlížeč příloh faktur vedle sebe</span><span class="sxs-lookup"><span data-stu-id="efa3b-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="efa3b-211">Na pomoc se snadným zobrazením příloh pro faktury dodavatele obsahují následující stránky, které se používají v procesu fakturace, prohlížeč formátu připojení:</span><span class="sxs-lookup"><span data-stu-id="efa3b-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="efa3b-212">**Ošetření výjimek**</span><span class="sxs-lookup"><span data-stu-id="efa3b-212">**Exception handling**</span></span>
+ <span data-ttu-id="efa3b-213">Stránka **Nevyřízené faktury dodavatele** (k dispozici také v procesu kontroly faktury)</span><span class="sxs-lookup"><span data-stu-id="efa3b-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="efa3b-214">Stránka s dotazem **Deník faktur** (pro zaúčtované faktury)</span><span class="sxs-lookup"><span data-stu-id="efa3b-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="efa3b-215">Tady jsou hlavní funkce, které poskytuje prohlížeč příloh:</span><span class="sxs-lookup"><span data-stu-id="efa3b-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="efa3b-216">Zobrazte všechny typy příloh, které Správa dokumentů podporuje (soubory, obrázky, adresy URL a poznámky).</span><span class="sxs-lookup"><span data-stu-id="efa3b-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="efa3b-217">Zobrazte vícestránkové soubory TIFF.</span><span class="sxs-lookup"><span data-stu-id="efa3b-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="efa3b-218">U souborů obrázků proveďte následující akce:</span><span class="sxs-lookup"><span data-stu-id="efa3b-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="efa3b-219">Zvýrazněte části obrázku.</span><span class="sxs-lookup"><span data-stu-id="efa3b-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="efa3b-220">Zablokujte části obrázku.</span><span class="sxs-lookup"><span data-stu-id="efa3b-220">Block parts of the image.</span></span>
  + <span data-ttu-id="efa3b-221">Přidejte poznámky do obrázku.</span><span class="sxs-lookup"><span data-stu-id="efa3b-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="efa3b-222">Přibližte nebo oddalte obrázek.</span><span class="sxs-lookup"><span data-stu-id="efa3b-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="efa3b-223">Naklopte obrázek.</span><span class="sxs-lookup"><span data-stu-id="efa3b-223">Pan the image.</span></span>
  + <span data-ttu-id="efa3b-224">Vraťte a opakujte akce.</span><span class="sxs-lookup"><span data-stu-id="efa3b-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="efa3b-225">Přizpůsobte velikost obrázku.</span><span class="sxs-lookup"><span data-stu-id="efa3b-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="efa3b-226">Tyto akce jsou k dispozici pouze pro soubory obrázků (JPEG, TIFF, PNG a tak dále).</span><span class="sxs-lookup"><span data-stu-id="efa3b-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="efa3b-227">Jakékoli změny provedené u obrázku pomocí těchto akcí jsou uloženy do souboru s obrázkem.</span><span class="sxs-lookup"><span data-stu-id="efa3b-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="efa3b-228">V současné době prohlížeč příloh neobsahuje správy verzí nebo schopnosti auditu.</span><span class="sxs-lookup"><span data-stu-id="efa3b-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="efa3b-229">Výchozí příloha</span><span class="sxs-lookup"><span data-stu-id="efa3b-229">Default attachment</span></span>

<span data-ttu-id="efa3b-230">Pokud faktura dodavatele má více než jednu přílohu, můžete nastavit jeden z dokumentů jako výchozí přílohu na stránce **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="efa3b-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="efa3b-231">Možnost **Je výchozí příloha** je novou možností, která byla přidaná v rámci této funkce.</span><span class="sxs-lookup"><span data-stu-id="efa3b-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="efa3b-232">Tato možnost je také vystavena v datové entitě Příloha dokumentu faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="efa3b-233">Proto lze výchozí přílohu nastavit pomocí integrace.</span><span class="sxs-lookup"><span data-stu-id="efa3b-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="efa3b-234">Jako výchozí přílohu lze nastavit pouze jeden dokument.</span><span class="sxs-lookup"><span data-stu-id="efa3b-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="efa3b-235">Po nastavení dokumentu jako výchozí přílohy se dokument automaticky zobrazí v prohlížeči příloh při otevření faktury.</span><span class="sxs-lookup"><span data-stu-id="efa3b-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="efa3b-236">Pokud jako výchozí přílohu nenastavíte žádný dokument, v prohlížeči se při otevření faktury automaticky nezobrazí žádná příloha.</span><span class="sxs-lookup"><span data-stu-id="efa3b-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="efa3b-237">Zobrazit přílohy faktur</span><span class="sxs-lookup"><span data-stu-id="efa3b-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="efa3b-238">Na stránkách **Zpracování výjimek**, **Čekající faktura** a **Deník faktur** je k dispozici nové tlačítko, které umožňuje zobrazit nebo skrýt prohlížeč příloh.</span><span class="sxs-lookup"><span data-stu-id="efa3b-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="efa3b-239">Zabezpečení</span><span class="sxs-lookup"><span data-stu-id="efa3b-239">Security</span></span>

<span data-ttu-id="efa3b-240">Pomocí rolí zabezpečení jsou v rámci zabezpečení založeného na rolích řízeny následující akce:</span><span class="sxs-lookup"><span data-stu-id="efa3b-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="efa3b-241">Zvýraznění</span><span class="sxs-lookup"><span data-stu-id="efa3b-241">Highlighting</span></span>
+ <span data-ttu-id="efa3b-242">Blokovat</span><span class="sxs-lookup"><span data-stu-id="efa3b-242">Block</span></span>
+ <span data-ttu-id="efa3b-243">Poznámky</span><span class="sxs-lookup"><span data-stu-id="efa3b-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="efa3b-244">Stránka Čekající faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="efa3b-244">Pending vendor invoices page</span></span>

<span data-ttu-id="efa3b-245">Následující oprávnění poskytují přístup jen ke čtení nebo přístup pro čtení a zápis k prohlížeči příloh pro zvýrazněný blok a akce anotací:</span><span class="sxs-lookup"><span data-stu-id="efa3b-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="efa3b-246">**Spravovat obrázek faktury dodavatele** – toto oprávnění poskytuje přístup pro čtení a zápis.</span><span class="sxs-lookup"><span data-stu-id="efa3b-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="efa3b-247">**Zobrazit obrázek faktury dodavatele** – toto oprávnění poskytuje přístup pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="efa3b-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="efa3b-248">Následující funkční oprávnění poskytují přístup jen pro čtení a zápis k prohlížeči příloh pro tyto akce:</span><span class="sxs-lookup"><span data-stu-id="efa3b-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="efa3b-249">**Spravovat faktury dodavatele** – Tomuto funkčnímu oprávnění je přiděleno oprávnění Spravovat obrázek faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="efa3b-250">**Dotaz na stav faktury dodavatele** – Tomuto funkčnímu oprávnění je přiděleno oprávnění Zobrazit obrázek faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="efa3b-251">Následující role poskytují přístup jen pro čtení a zápis k prohlížeči příloh pro tyto akce:</span><span class="sxs-lookup"><span data-stu-id="efa3b-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="efa3b-252">**Úředník závazků** a **Manažer závazků** – Těmto rolím je přiřazeno funkční oprávnění Spravovat faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="efa3b-253">**Úředník závazků**, **Manažer závazků**, **Úředník centralizovaných plateb závazků** a **Úředník plateb závazků** – Těmto rolím je přiřazeno funkční oprávnění Dotázat se na stav faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="efa3b-254">Stránka podrobností o výjimce faktury</span><span class="sxs-lookup"><span data-stu-id="efa3b-254">Invoice exception details page</span></span>

<span data-ttu-id="efa3b-255">Následující oprávnění poskytují přístup jen ke čtení nebo přístup pro čtení a zápis k prohlížeči příloh pro zvýrazněný blok a akce anotací.</span><span class="sxs-lookup"><span data-stu-id="efa3b-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="efa3b-256">Role, které jsou uvedeny v této části, poskytují z výroby přístup k obrázkům faktury v prohlížeči příloh jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="efa3b-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="efa3b-257">Pokud role musí mít také přístup pro zápis do obrázků, můžete této roli udělit přístup pro zápis pomocí oprávnění a funkčního oprávnění, které jsou zde popsány.</span><span class="sxs-lookup"><span data-stu-id="efa3b-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="efa3b-258">**Udržovat obrázek entity záhlaví faktury dodavatele** – toto oprávnění poskytuje přístup pro čtení a zápis k obrázkům faktury v prohlížeči příloh.</span><span class="sxs-lookup"><span data-stu-id="efa3b-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="efa3b-259">**Zobrazit obrázek entity záhlaví faktury dodavatele** – toto oprávnění poskytuje přístup pouze pro čtení k obrázkům faktury v prohlížeči příloh.</span><span class="sxs-lookup"><span data-stu-id="efa3b-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="efa3b-260">Následující funkční oprávnění poskytují přístup jen pro čtení k prohlížeči příloh pro tyto akce:</span><span class="sxs-lookup"><span data-stu-id="efa3b-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="efa3b-261">**Spravovat faktury dodavatele** – Tomuto funkčnímu oprávnění je přiděleno oprávnění entity záhlaví Spravovat fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="efa3b-262">Následující role poskytují přístup jen pro čtení k prohlížeči příloh pro tyto akce:</span><span class="sxs-lookup"><span data-stu-id="efa3b-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="efa3b-263">**Úředník závazků** a **Manažer závazků** – Těmto rolím je přiřazeno funkční oprávnění Spravovat faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="efa3b-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="efa3b-264">Pokud role uživatele poskytuje práva pro úpravy na jakékoli stránce, bude mít ve výchozím nastavení uživatel také oprávnění pro úpravy v prohlížeči úprav pro akce zvýraznění, blokování a poznámky.</span><span class="sxs-lookup"><span data-stu-id="efa3b-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="efa3b-265">Pokud však existují scénáře, ve kterých by měla mít konkrétní role oprávnění pro úpravy na stránce, ale ne v prohlížeči příloh, příslušná oprávnění v předchozím seznamu lze použít k vyřešení případu použití.</span><span class="sxs-lookup"><span data-stu-id="efa3b-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
