---
title: Poradce při potížích s importem souboru bankovního výpisu
description: Je důležité, aby se soubor s bankovním výpisem z banky shodoval s rozvržením podporovaným v aplikaci Microsoft Dynamics 365 Finance. Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně. Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky. Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem. V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188552"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="f6967-107">Poradce při potížích s importem souboru bankovního výpisu</span><span class="sxs-lookup"><span data-stu-id="f6967-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6967-108">Je důležité, aby se soubor s bankovním výpisem z banky shodoval s rozvržením podporovaným v aplikaci Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f6967-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="f6967-109">Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně.</span><span class="sxs-lookup"><span data-stu-id="f6967-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="f6967-110">Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky.</span><span class="sxs-lookup"><span data-stu-id="f6967-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="f6967-111">Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem.</span><span class="sxs-lookup"><span data-stu-id="f6967-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="f6967-112">V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží.</span><span class="sxs-lookup"><span data-stu-id="f6967-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="f6967-113">Kde se stala chyba?</span><span class="sxs-lookup"><span data-stu-id="f6967-113">What is the error?</span></span>

<span data-ttu-id="f6967-114">Při pokusu o import souboru s bankovním výpisem přejděte při hledání chyby k historii úlohy řízení dat a podrobnostem o jejím provedení.</span><span class="sxs-lookup"><span data-stu-id="f6967-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="f6967-115">Chyba může pomoci tím, že bude ukazovat na řádek výkazu, rozvahy nebo výpisu.</span><span class="sxs-lookup"><span data-stu-id="f6967-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="f6967-116">Obvykle však neposkytuje dostatek informací k identifikaci pole nebo prvku, který problém způsobil.</span><span class="sxs-lookup"><span data-stu-id="f6967-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="f6967-117">Importované bankovní výpisy se mohou překrývat pouze pro jeden bod v čase.</span><span class="sxs-lookup"><span data-stu-id="f6967-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="f6967-118">Například pokud výpis končí 1. ledna 2021 v 0:00, počáteční datum dalšího výpisu může být 1. ledna 2021 v 0:00.</span><span class="sxs-lookup"><span data-stu-id="f6967-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="f6967-119">Jaký je rozdíl?</span><span class="sxs-lookup"><span data-stu-id="f6967-119">What are the differences?</span></span>
<span data-ttu-id="f6967-120">Srovnejte definici rozvržení bankovního souboru s definicí importu v aplikaci Finance a poznamenejte si všechny rozdíly v polích a prvcích.</span><span class="sxs-lookup"><span data-stu-id="f6967-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="f6967-121">Porovnejte soubor bankovního výpisu s příslušným vzorovým souborem aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="f6967-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="f6967-122">V souborech ISO20022 by mělo být možné snadno zjistit rozdíly.</span><span class="sxs-lookup"><span data-stu-id="f6967-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="f6967-123">Rozdíly v časových pásmech u importovaných bankovních výpisů</span><span class="sxs-lookup"><span data-stu-id="f6967-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="f6967-124">Hodnoty data a času v importním souboru se mohou lišit od hodnot data a času zobrazených ve Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6967-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="f6967-125">Chcete-li zabránit této nesrovnalosti, zadejte prioritu časového pásma na stránce **Konfigurovat zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="f6967-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="f6967-126">Informace o zadání předvoleb pro časové pásmo najdete v tématu [Nastavení procesu importu pokročilého odsouhlasení banky](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="f6967-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="f6967-127">Transformace</span><span class="sxs-lookup"><span data-stu-id="f6967-127">Transformations</span></span>
<span data-ttu-id="f6967-128">Obvykle je nutné provést změny v jedné ze tří transformací.</span><span class="sxs-lookup"><span data-stu-id="f6967-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="f6967-129">Každá transformace je sestavena pro konkrétní standard.</span><span class="sxs-lookup"><span data-stu-id="f6967-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="f6967-130">Název prostředku</span><span class="sxs-lookup"><span data-stu-id="f6967-130">Resource name</span></span>                                         | <span data-ttu-id="f6967-131">Název souboru</span><span class="sxs-lookup"><span data-stu-id="f6967-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="f6967-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f6967-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="f6967-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f6967-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="f6967-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="f6967-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="f6967-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="f6967-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="f6967-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f6967-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="f6967-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f6967-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="f6967-138">Ladění transformací</span><span class="sxs-lookup"><span data-stu-id="f6967-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="f6967-139">Úprava souboru BAI2 a MT940</span><span class="sxs-lookup"><span data-stu-id="f6967-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="f6967-140">BAI2 a MT940 jsou textové soubory a vyžadují provedení úprav, než bude možné použít ladění dokumentů XSLT (Extensible Stylesheet Language Transformations).</span><span class="sxs-lookup"><span data-stu-id="f6967-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="f6967-141">Program tyto úpravy provede při importu souboru.</span><span class="sxs-lookup"><span data-stu-id="f6967-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="f6967-142">Vytvořit soubor XML a zkopírujte do něj následující text.</span><span class="sxs-lookup"><span data-stu-id="f6967-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="f6967-143">Zkopírujte obsah souboru s bankovním výpisem a vložte jej do souboru XML tak, aby nahradil text **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="f6967-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="f6967-144">Ladění souboru XSLT</span><span class="sxs-lookup"><span data-stu-id="f6967-144">Debug the XSLT</span></span>

<span data-ttu-id="f6967-145">Další informace naleznete v tématu <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f6967-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="f6967-146">Spusťte aplikaci Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f6967-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="f6967-147">Vytvořte aplikační konzoli.</span><span class="sxs-lookup"><span data-stu-id="f6967-147">Create a console application.</span></span>
3.  <span data-ttu-id="f6967-148">Otevřete odpovídající soubor XSLT.</span><span class="sxs-lookup"><span data-stu-id="f6967-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="f6967-149">Klepněte na XLST a na stránku s jeho vlastnostmi.</span><span class="sxs-lookup"><span data-stu-id="f6967-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="f6967-150">jako vstup nastavte umístění souboru s bankovním výpisem.</span><span class="sxs-lookup"><span data-stu-id="f6967-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="f6967-151">Zadejte název souboru a jeho umístění pro výstup.</span><span class="sxs-lookup"><span data-stu-id="f6967-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="f6967-152">Nastavte požadované zlomové body.</span><span class="sxs-lookup"><span data-stu-id="f6967-152">Set the required break points.</span></span>
8.  <span data-ttu-id="f6967-153">V nabídce klepněte na **XML** &gt; **Spustit ladění XSLT**.</span><span class="sxs-lookup"><span data-stu-id="f6967-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="f6967-154">Formátování výstupu XSLT</span><span class="sxs-lookup"><span data-stu-id="f6967-154">Format the XSLT output</span></span>

<span data-ttu-id="f6967-155">Po spuštění transformace se vytvoří výstupní soubor, který lze zobrazit v aplikaci Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f6967-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="f6967-156">Pomocí kombinace kláves Ctrl + A, Ctrl + K a Ctrl + D můžete výstupní soubor rychle formátovat.</span><span class="sxs-lookup"><span data-stu-id="f6967-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="f6967-157">Úprava transformace</span><span class="sxs-lookup"><span data-stu-id="f6967-157">Adjust the transformation</span></span>

<span data-ttu-id="f6967-158">Upravením transformace získejte příslušné pole nebo prvek v souboru s bankovním výpisem.</span><span class="sxs-lookup"><span data-stu-id="f6967-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="f6967-159">Toto pole či prvek pak namapujte na odpovídající prvek aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="f6967-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="f6967-160">Indikátor má dáti/dal</span><span class="sxs-lookup"><span data-stu-id="f6967-160">Debit/credit indicator</span></span>

<span data-ttu-id="f6967-161">V některých případech může být hodnota „má dáti“ importována jako hodnota „dal“ a obráceně.</span><span class="sxs-lookup"><span data-stu-id="f6967-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="f6967-162">K vyřešení tohoto problému je nutné změnit odpovídající soubor XSLT.</span><span class="sxs-lookup"><span data-stu-id="f6967-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="f6967-163">Pokud bankovní výpisy pocházejí z několika bank, ujistěte se, že všechny používají stejný přístup strany má dáti/dal nebo vytvořte samostatné transformace.</span><span class="sxs-lookup"><span data-stu-id="f6967-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="f6967-164">Šablona BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="f6967-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="f6967-165">Šablona ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="f6967-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="f6967-166">Šablona MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="f6967-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="f6967-167">Příklady formátů bankovních výpisů a technické rozložení</span><span class="sxs-lookup"><span data-stu-id="f6967-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="f6967-168">V následující tabulce jsou uvedeny příklady technických definic rozložení pro komplexní importní soubory s bankovním odsouhlasením a tři související vzorové soubory bankovních výpisů.</span><span class="sxs-lookup"><span data-stu-id="f6967-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="f6967-169">Zde můžete stáhnout vzorové soubory a technická rozvržení: [Import ukázkových souborů](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="f6967-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="f6967-170">Technická definice rozložení</span><span class="sxs-lookup"><span data-stu-id="f6967-170">Technical layout definition</span></span>                             | <span data-ttu-id="f6967-171">Vzorový soubor s bankovním výpisem</span><span class="sxs-lookup"><span data-stu-id="f6967-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="f6967-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="f6967-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="f6967-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="f6967-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="f6967-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="f6967-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="f6967-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="f6967-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="f6967-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="f6967-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="f6967-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="f6967-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
