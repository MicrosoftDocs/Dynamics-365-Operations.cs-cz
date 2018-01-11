---
title: "Poradce při potížích s importem souboru bankovního výpisu"
description: "Je důležité, aby se rozvržení souboru s bankovním výpisem od banky shodovalo s rozvržením podporovaným v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně. Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky. Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem. V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 263bfe858f2ca5f7fe2f7426565938899d98130f
ms.openlocfilehash: 14ec157ee822ffc5e3a6bc2012d8ec36bb09f0b7
ms.contentlocale: cs-cz
ms.lasthandoff: 01/11/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="ebeef-107">Poradce při potížích s importem souboru bankovního výpisu</span><span class="sxs-lookup"><span data-stu-id="ebeef-107">Bank statement file import troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ebeef-108">Je důležité, aby se rozvržení souboru s bankovním výpisem od banky shodovalo s rozvržením podporovaným v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="ebeef-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports.</span></span> <span data-ttu-id="ebeef-109">Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně.</span><span class="sxs-lookup"><span data-stu-id="ebeef-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="ebeef-110">Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky.</span><span class="sxs-lookup"><span data-stu-id="ebeef-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="ebeef-111">Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem.</span><span class="sxs-lookup"><span data-stu-id="ebeef-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="ebeef-112">V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží.</span><span class="sxs-lookup"><span data-stu-id="ebeef-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="ebeef-113">Kde se stala chyba?</span><span class="sxs-lookup"><span data-stu-id="ebeef-113">What is the error?</span></span>
------------------

<span data-ttu-id="ebeef-114">Při pokusu o import souboru s bankovním výpisem přejděte při hledání chyby k historii úlohy řízení dat a podrobnostem o jejím provedení.</span><span class="sxs-lookup"><span data-stu-id="ebeef-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="ebeef-115">Chyba může pomoci tím, že bude ukazovat na řádek výkazu, rozvahy nebo výpisu.</span><span class="sxs-lookup"><span data-stu-id="ebeef-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="ebeef-116">Obvykle však neposkytuje dostatek informací k identifikaci pole nebo prvku, který problém způsobil.</span><span class="sxs-lookup"><span data-stu-id="ebeef-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="ebeef-117">Jaký je rozdíl?</span><span class="sxs-lookup"><span data-stu-id="ebeef-117">What are the differences?</span></span>
<span data-ttu-id="ebeef-118">Srovnejte definici rozvržení bankovního souboru s definicí importu v aplikaci Finance and Operations a poznamenejte si všechny rozdíly v polích a prvcích.</span><span class="sxs-lookup"><span data-stu-id="ebeef-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="ebeef-119">Porovnejte soubor bankovního výpisu s příslušným vzorovým souborem aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ebeef-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="ebeef-120">V souborech ISO20022 by mělo být možné snadno zjistit rozdíly.</span><span class="sxs-lookup"><span data-stu-id="ebeef-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="ebeef-121">Transformace</span><span class="sxs-lookup"><span data-stu-id="ebeef-121">Transformations</span></span>
<span data-ttu-id="ebeef-122">Obvykle je nutné provést změny v jedné ze tří transformací.</span><span class="sxs-lookup"><span data-stu-id="ebeef-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="ebeef-123">Každá transformace je sestavena pro konkrétní standard.</span><span class="sxs-lookup"><span data-stu-id="ebeef-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="ebeef-124">Název prostředku</span><span class="sxs-lookup"><span data-stu-id="ebeef-124">Resource name</span></span>                                         | <span data-ttu-id="ebeef-125">Název souboru</span><span class="sxs-lookup"><span data-stu-id="ebeef-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="ebeef-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="ebeef-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="ebeef-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="ebeef-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="ebeef-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="ebeef-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="ebeef-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="ebeef-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="ebeef-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="ebeef-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="ebeef-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="ebeef-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="ebeef-132">Ladění transformací</span><span class="sxs-lookup"><span data-stu-id="ebeef-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="ebeef-133">Úprava souboru BAI2 a MT940</span><span class="sxs-lookup"><span data-stu-id="ebeef-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="ebeef-134">BAI2 a MT940 jsou textové soubory a vyžadují provedení úprav, než bude možné použít ladění dokumentů XSLT (Extensible Stylesheet Language Transformations).</span><span class="sxs-lookup"><span data-stu-id="ebeef-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="ebeef-135">Program tyto úpravy provede při importu souboru.</span><span class="sxs-lookup"><span data-stu-id="ebeef-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="ebeef-136">Vytvořit soubor XML a zkopírujte do něj následující text.</span><span class="sxs-lookup"><span data-stu-id="ebeef-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="ebeef-137">Zkopírujte obsah souboru s bankovním výpisem a vložte jej do souboru XML tak, aby nahradil text **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="ebeef-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="ebeef-138">Ladění souboru XSLT</span><span class="sxs-lookup"><span data-stu-id="ebeef-138">Debug the XSLT</span></span>

<span data-ttu-id="ebeef-139">Další informace naleznete v tématu <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="ebeef-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="ebeef-140">Spusťte Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ebeef-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="ebeef-141">Vytvořte aplikační konzoli.</span><span class="sxs-lookup"><span data-stu-id="ebeef-141">Create a console application.</span></span>
3.  <span data-ttu-id="ebeef-142">Otevřete odpovídající soubor XSLT.</span><span class="sxs-lookup"><span data-stu-id="ebeef-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="ebeef-143">Klepněte na XLST a na stránku s jeho vlastnostmi.</span><span class="sxs-lookup"><span data-stu-id="ebeef-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="ebeef-144">jako vstup nastavte umístění souboru s bankovním výpisem.</span><span class="sxs-lookup"><span data-stu-id="ebeef-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="ebeef-145">Zadejte název souboru a jeho umístění pro výstup.</span><span class="sxs-lookup"><span data-stu-id="ebeef-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="ebeef-146">Nastavte požadované zlomové body.</span><span class="sxs-lookup"><span data-stu-id="ebeef-146">Set the required break points.</span></span>
8.  <span data-ttu-id="ebeef-147">V nabídce klepněte na **XML** &gt; **Spustit ladění XSLT**.</span><span class="sxs-lookup"><span data-stu-id="ebeef-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="ebeef-148">Formátování výstupu XSLT</span><span class="sxs-lookup"><span data-stu-id="ebeef-148">Format the XSLT output</span></span>

<span data-ttu-id="ebeef-149">Po spuštění transformace se vytvoří výstupní soubor, který lze zobrazit v aplikaci Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ebeef-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="ebeef-150">Pomocí kombinace kláves Ctrl + A, Ctrl + K a Ctrl + D můžete výstupní soubor rychle formátovat.</span><span class="sxs-lookup"><span data-stu-id="ebeef-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="ebeef-151">Úprava transformace</span><span class="sxs-lookup"><span data-stu-id="ebeef-151">Adjust the transformation</span></span>

<span data-ttu-id="ebeef-152">Upravením transformace získejte příslušné pole nebo prvek v souboru s bankovním výpisem.</span><span class="sxs-lookup"><span data-stu-id="ebeef-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="ebeef-153">Toto pole či prvek pak namapujte na odpovídající prvek aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ebeef-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="ebeef-154">Indikátor má dáti/dal</span><span class="sxs-lookup"><span data-stu-id="ebeef-154">Debit/credit indicator</span></span>

<span data-ttu-id="ebeef-155">V některých případech může být hodnota „má dáti“ importována jako hodnota „dal“ a obráceně.</span><span class="sxs-lookup"><span data-stu-id="ebeef-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="ebeef-156">K vyřešení tohoto problému je nutné změnit odpovídající soubor XSLT.</span><span class="sxs-lookup"><span data-stu-id="ebeef-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="ebeef-157">Pokud bankovní výpisy pocházejí z několika bank, ujistěte se, že všechny používají stejný přístup strany má dáti/dal nebo vytvořte samostatné transformace.</span><span class="sxs-lookup"><span data-stu-id="ebeef-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="ebeef-158">Šablona BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="ebeef-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="ebeef-159">Šablona ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="ebeef-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="ebeef-160">Šablona MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="ebeef-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="ebeef-161">Příklady formátů bankovních výpisů a technické rozložení</span><span class="sxs-lookup"><span data-stu-id="ebeef-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="ebeef-162">V následující tabulce jsou uvedeny příklady technických definic rozložení pro komplexní importní soubory s bankovním odsouhlasením a tři související vzorové soubory bankovních výpisů.</span><span class="sxs-lookup"><span data-stu-id="ebeef-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="ebeef-163">Můžete stáhnout soubory příkladu a technické rozložení zde: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="ebeef-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="ebeef-164">Technická definice rozložení</span><span class="sxs-lookup"><span data-stu-id="ebeef-164">Technical layout definition</span></span>                             | <span data-ttu-id="ebeef-165">Vzorový soubor s bankovním výpisem</span><span class="sxs-lookup"><span data-stu-id="ebeef-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="ebeef-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="ebeef-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="ebeef-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="ebeef-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="ebeef-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="ebeef-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="ebeef-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="ebeef-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="ebeef-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="ebeef-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="ebeef-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="ebeef-171">BAI2StatementExample</span></span>                 |






