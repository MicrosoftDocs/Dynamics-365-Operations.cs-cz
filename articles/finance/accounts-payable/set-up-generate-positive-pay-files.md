---
title: Nastavení a generování souborů kladné platby
description: Toto téma vysvětluje postup při nastavení kladných plateb a generování souborů kladných plateb.
author: panolte
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 82f7c8947bcc2dab394ea24e28a3631cc8682e5a
ms.sourcegitcommit: 1b00e21faf89de8b3450936253a4c02cb4d12a3d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295239"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="03ed1-103">Nastavení a generování souborů kladné platby</span><span class="sxs-lookup"><span data-stu-id="03ed1-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03ed1-104">Toto téma vysvětluje postup při nastavení kladných plateb a generování souborů kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="03ed1-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="03ed1-105">Nastavte kladné platby pro generování elektronických seznamů šeků, které jsou dodávány bance.</span><span class="sxs-lookup"><span data-stu-id="03ed1-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="03ed1-106">Poté při předložení šeku bance ho banka srovná se seznamem šeků.</span><span class="sxs-lookup"><span data-stu-id="03ed1-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="03ed1-107">Pokud šek odpovídá tomu, co má banka má v záznamech v seznamu, banka jej zúčtuje.</span><span class="sxs-lookup"><span data-stu-id="03ed1-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="03ed1-108">Pokud šek neodpovídá šeku v seznamu, banka předloží šek ke kontrole.</span><span class="sxs-lookup"><span data-stu-id="03ed1-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="03ed1-109">Zabezpečení pro soubory kladných plateb</span><span class="sxs-lookup"><span data-stu-id="03ed1-109">Security for positive pay files</span></span>
<span data-ttu-id="03ed1-110">Soubory kladných plateb mohou obsahovat citlivé informace o příjemcích plateb a šekových částkách.</span><span class="sxs-lookup"><span data-stu-id="03ed1-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="03ed1-111">Nezapomeňte tedy použít dostatečná opatření od doby vytvoření souborů do jejich přijetí do banky.</span><span class="sxs-lookup"><span data-stu-id="03ed1-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="03ed1-112">Soubory kladných plateb budou staženy do umístění, které je zadáno ve webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="03ed1-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="03ed1-113">Vzhledem k tomu, že soubory kladných plateb mohou obsahovat důvěrné informace, je důležité, aby k vytváření a prohlížení těchto informací v aplikaci Microsoft Dynamics 365 Finance měli přístup pouze oprávnění uživatelé.</span><span class="sxs-lookup"><span data-stu-id="03ed1-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="03ed1-114">V následující tabulce naleznete postup, jak určit potřebná oprávnění.</span><span class="sxs-lookup"><span data-stu-id="03ed1-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03ed1-115">Úkol</span><span class="sxs-lookup"><span data-stu-id="03ed1-115">Task</span></span></th>
<th><span data-ttu-id="03ed1-116">Oprávnění</span><span class="sxs-lookup"><span data-stu-id="03ed1-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03ed1-117">Generování souborů kladných plateb na stránce se seznamem <strong>Bankovní účty</strong> nebo na stránce <strong>Bankovní účty</strong>.</span><span class="sxs-lookup"><span data-stu-id="03ed1-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="03ed1-118"><strong>Udržování informace o souborech kladných bankovních plateb</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="03ed1-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="03ed1-119"><strong>NáhledSubjektuExportuKladnéBankovníPlatby</strong> (NáhledSubjektuExportuKladnéBankovníPlatby)</span><span class="sxs-lookup"><span data-stu-id="03ed1-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ed1-120">Generování souborů kladných plateb pro více právnických osob a bankovních účtů na stránce <strong>Vygenerovat soubor kladných plateb</strong>.</span><span class="sxs-lookup"><span data-stu-id="03ed1-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="03ed1-121"><strong>Udržování informace o souborech kladných bankovních plateb</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="03ed1-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="03ed1-122"><strong>NáhledSubjektuExportuKladnéBankovníPlatby</strong> (NáhledSubjektuExportuKladnéBankovníPlatby)</span><span class="sxs-lookup"><span data-stu-id="03ed1-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ed1-123">Zobrazení souborů kladných plateb na stránce <strong>Souhrnné informace o souboru kladných plateb</strong>.</span><span class="sxs-lookup"><span data-stu-id="03ed1-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="03ed1-124"><strong>Zobrazit informace o bankovních souborech kladných plateb pro více právnických osob</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="03ed1-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ed1-125">Potvrzení souboru kladných bankovních plateb na stránce <strong>Souhrnné informace o souboru kladných plateb</strong>.</span><span class="sxs-lookup"><span data-stu-id="03ed1-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="03ed1-126"><strong>Potvrdit soubor kladných plateb</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="03ed1-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ed1-127">Odvolání souboru kladných bankovních plateb na stránce <strong>Souhrnné informace o souboru kladných plateb</strong>.</span><span class="sxs-lookup"><span data-stu-id="03ed1-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="03ed1-128"><strong>Odvolání souboru kladných plateb</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="03ed1-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="03ed1-129">Nastavení formátu kladné platby</span><span class="sxs-lookup"><span data-stu-id="03ed1-129">Set up a positive pay format</span></span>
<span data-ttu-id="03ed1-130">Soubory kladných plateb jsou vytvořeny pomocí datových entit.</span><span class="sxs-lookup"><span data-stu-id="03ed1-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="03ed1-131">Aby bylo možné vygenerovat soubor kladných plateb, je nutné nastavit formát vstupní transformace, který se použije k převodu informací o šeku do formátu, ve kterém lze komunikovat s bankou.</span><span class="sxs-lookup"><span data-stu-id="03ed1-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="03ed1-132">Na stránce **Formát kladné platby** můžete vytvořit identifikátor a popis formátu souboru.</span><span class="sxs-lookup"><span data-stu-id="03ed1-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="03ed1-133">Vstupní formát transformace musí být soubor typu XML.</span><span class="sxs-lookup"><span data-stu-id="03ed1-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="03ed1-134">Určitý formát závisí na transformačním souboru, který používáte.</span><span class="sxs-lookup"><span data-stu-id="03ed1-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="03ed1-135">Například vzorový soubor v jazyce XSLT (Extensible Stylesheet Language Transformations ), který je vám k dispozici, používá formát **Prvek XML**.</span><span class="sxs-lookup"><span data-stu-id="03ed1-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="03ed1-136">Pomocí akce **Nahrát soubor použitý k transformaci** určete umístění souboru transformace pro formát, který vyžaduje vaše banka.</span><span class="sxs-lookup"><span data-stu-id="03ed1-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="03ed1-137">Příklad: Soubor XSLT souborů kladných plateb</span><span class="sxs-lookup"><span data-stu-id="03ed1-137">Example: XSLT file for positive pay file</span></span>

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="03ed1-138">Přiřazení formátu kladné platby k bankovnímu účtu</span><span class="sxs-lookup"><span data-stu-id="03ed1-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="03ed1-139">Pro každý bankovní účet, pro který chcete generovat informace o souborech kladných plateb, musíte přiřadit formát kladných plateb, který byl zadán v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="03ed1-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="03ed1-140">Na stránce **Bankovní účty** vyberte formát kladných plateb, který odpovídá bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="03ed1-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="03ed1-141">V poli **Počáteční datum kladné platby** zadejte první datum generování souborů kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="03ed1-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="03ed1-142">Je důležité zadat datum do tohoto pole.</span><span class="sxs-lookup"><span data-stu-id="03ed1-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="03ed1-143">V opačném případě první soubor kladných plateb, který vygenerujete, bude obsahovat všechny šeky, které kdy byly vytvořeny pro tento bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="03ed1-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="03ed1-144">Přiřaďte číselnou řadu pro soubory kladných plateb</span><span class="sxs-lookup"><span data-stu-id="03ed1-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="03ed1-145">Každý soubor kladných plateb musí mít jedinečné číslo.</span><span class="sxs-lookup"><span data-stu-id="03ed1-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="03ed1-146">Pomocí karty **Číselné řady** na stránce **Parametry řízení hotovosti a banky** vytvořte číselnou řadu pro soubory kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="03ed1-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="03ed1-147">Generování souborů kladných plateb pro jeden bankovní účet</span><span class="sxs-lookup"><span data-stu-id="03ed1-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="03ed1-148">Lze vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="03ed1-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="03ed1-149">Ke generování souborů kladných plateb pro více právnických osob a bankovních účtů současně použijte informace v dalším kroku.</span><span class="sxs-lookup"><span data-stu-id="03ed1-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="03ed1-150">Pokud chcete vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet, otevřete dialogové okno **Vygenerovat soubor kladných plateb** na stránce **Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="03ed1-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="03ed1-151">V poli **Datum přerušení** zadejte datum posledního šeku, který má být zahrnut do souboru kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="03ed1-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="03ed1-152">V souboru budou zahrnuty všechny šeky, které nebyly zahrnuty do souboru kladných plateb do tohoto data kontroly.</span><span class="sxs-lookup"><span data-stu-id="03ed1-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="03ed1-153">Generování souborů kladných plateb pro více bankovních účtů</span><span class="sxs-lookup"><span data-stu-id="03ed1-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="03ed1-154">Pro vygenerování souboru kladných plateb pro bankovních účtů použijte periodickou úlohu **Vygenerovat soubor kladných plateb**.</span><span class="sxs-lookup"><span data-stu-id="03ed1-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="03ed1-155">Vyberte formát souboru pro kladné platby a určete, zda chcete vygenerovat soubor pro všechny právnické osoby nebo pro vybranou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="03ed1-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="03ed1-156">Vyberte také, zda chcete vygenerovat soubor kladných plateb pro všechny bankovní účty, které používají zadaný formát kladné platby, nebo jen pro vybraný bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="03ed1-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="03ed1-157">V poli **Datum přerušení** zadejte datum posledního šeku, který má být zahrnut do souboru kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="03ed1-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="03ed1-158">V souboru budou zahrnuty všechny šeky, které nebyly zahrnuty do souboru kladných plateb do tohoto data kontroly.</span><span class="sxs-lookup"><span data-stu-id="03ed1-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="03ed1-159">Zobrazení výsledků generování souboru kladných plateb</span><span class="sxs-lookup"><span data-stu-id="03ed1-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="03ed1-160">Poté, co je soubor kladných plateb vygenerován, se výsledky zobrazí na stránce **Souhrnné informace o souboru kladných plateb**.</span><span class="sxs-lookup"><span data-stu-id="03ed1-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="03ed1-161">Pokud chcete zobrazit podrobnosti o jednotlivých šecích, můžete použít stránku s podrobnostmi **Soubor kladných plateb**.</span><span class="sxs-lookup"><span data-stu-id="03ed1-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="03ed1-162">Potvrzení souboru kladných plateb</span><span class="sxs-lookup"><span data-stu-id="03ed1-162">Confirm a positive pay file</span></span>
<span data-ttu-id="03ed1-163">Po zaplacení šeků, které jsou uvedeny v souboru kladných plateb, obdržíte číslo potvrzení od banky.</span><span class="sxs-lookup"><span data-stu-id="03ed1-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="03ed1-164">Poté můžete potvrdit soubor kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="03ed1-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="03ed1-165">Na stránce **Souhrnné informace o souboru kladných plateb** vyberte soubor kladných plateb, který má stav **Vytvořeno**, a poté vyberte akci **Zadání potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="03ed1-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="03ed1-166">Při potvrzením souboru kladných plateb se pořídí záznam čísla potvrzení od banky.</span><span class="sxs-lookup"><span data-stu-id="03ed1-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="03ed1-167">Odvolat soubor kladných plateb</span><span class="sxs-lookup"><span data-stu-id="03ed1-167">Recall a positive pay file</span></span>
<span data-ttu-id="03ed1-168">Pokud je nutné změnit soubor kladných plateb, můžete jej odvolat.</span><span class="sxs-lookup"><span data-stu-id="03ed1-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="03ed1-169">Na stránce **Souhrnné informace o souboru kladných plateb** vyberte soubor kladných plateb, který má stav **Vytvořeno**, a poté vyberte akci **Odvolat**.</span><span class="sxs-lookup"><span data-stu-id="03ed1-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="03ed1-170">Pro každý šek v souboru kladných plateb se resetuje pole, které označuje, zda byl šek zahrnut do souboru kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="03ed1-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="03ed1-171">Poté můžete vytvořit nový soubor kladných plateb, který obsahuje šeky, které byly odvolány.</span><span class="sxs-lookup"><span data-stu-id="03ed1-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



