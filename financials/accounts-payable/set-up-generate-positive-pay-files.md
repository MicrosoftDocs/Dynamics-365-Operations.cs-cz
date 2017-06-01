---
title: "Nastavení a vygenerování souborů kladných plateb"
description: "Tento článek vysvětluje postup při nastavení kladných plateb a generování souborů kladných plateb."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f82ed69aaaf4d3345ef4e74a338124465dcf2358
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-and-generate-positive-pay-files"></a>Nastavení a vygenerování souborů kladných plateb

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje postup při nastavení kladných plateb a generování souborů kladných plateb. 

Nastavte kladné platby pro generování elektronických seznamů šeků, které jsou dodávány bance. Poté při předložení šeku bance ho banka srovná se seznamem šeků. Pokud šek odpovídá tomu, co má banka má v záznamech v seznamu, banka jej zúčtuje. Pokud šek neodpovídá šeku v seznamu, banka předloží šek ke kontrole.

## <a name="security-for-positive-pay-files"></a>Zabezpečení pro soubory kladných plateb
Soubory kladných plateb mohou obsahovat citlivé informace o příjemcích plateb a šekových částkách. Nezapomeňte tedy použít dostatečná opatření od doby vytvoření souborů do jejich přijetí do banky. Soubory kladných plateb budou staženy do umístění, které je zadáno ve webovém prohlížeči. Vzhledem k tomu, že soubory kladných plateb mohou obsahovat důvěrné informace, je důležité, aby k vytváření a prohlížení těchto informací v aplikaci Microsoft Dynamics 365 for Operations měli přístup pouze oprávnění uživatelé. V následující tabulce naleznete postup, jak určit potřebná oprávnění.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Úkol</th>
<th>Oprávnění</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generování souborů kladných plateb na stránce se seznamem <strong>Bankovní účty</strong> nebo na stránce <strong>Bankovní účty</strong>.</td>
<td><ul>
<li><strong>Udržování informace o souborech kladných bankovních plateb</strong> (BankPositivePayProcess)</li>
<li><strong>NáhledSubjektuExportuKladnéBankovníPlatby</strong> (NáhledSubjektuExportuKladnéBankovníPlatby)</li>
</ul></td>
</tr>
<tr class="even">
<td>Generování souborů kladných plateb pro více právnických osob a bankovních účtů na stránce <strong>Vygenerovat soubor kladných plateb</strong>.</td>
<td><ul>
<li><strong>Udržování informace o souborech kladných bankovních plateb</strong> (BankPositivePayProcess)</li>
<li><strong>NáhledSubjektuExportuKladnéBankovníPlatby</strong> (NáhledSubjektuExportuKladnéBankovníPlatby)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zobrazení souborů kladných plateb na stránce <strong>Souhrnné informace o souboru kladných plateb</strong>.</td>
<td><strong>Zobrazit informace o bankovních souborech kladných plateb pro více právnických osob</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Potvrzení souboru kladných bankovních plateb na stránce <strong>Souhrnné informace o souboru kladných plateb</strong>.</td>
<td><strong>Potvrdit soubor kladných plateb</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Odvolání souboru kladných bankovních plateb na stránce <strong>Souhrnné informace o souboru kladných plateb</strong>.</td>
<td><strong>Odvolání souboru kladných plateb</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Nastavení formátu kladné platby
Soubory kladných plateb jsou vytvořeny pomocí datových entit. Aby bylo možné vygenerovat soubor kladných plateb, je nutné nastavit formát vstupní transformace, který se použije k převodu informací o šeku do formátu, ve kterém lze komunikovat s bankou. Na stránce **Formát kladné platby** můžete vytvořit identifikátor a popis formátu souboru. Vstupní formát transformace musí být soubor typu XML. Určitý formát závisí na transformačním souboru, který používáte. Například vzorový soubor v jazyce XSLT (Extensible Stylesheet Language Transformations ), který je vám k dispozici, používá formát **Prvek XML**. Pomocí akce **Nahrát soubor použitý k transformaci** určete umístění souboru transformace pro formát, který vyžaduje vaše banka.

## <a name="example-xslt-file-for-positive-pay-file"></a>Příklad: Soubor XSLT souborů kladných plateb
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
          <xsl:for-each select="Document/BankPositivePayExportEntity">
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Přiřazení formátu kladné platby k bankovnímu účtu
Pro každý bankovní účet, pro který chcete generovat informace o souborech kladných plateb, musíte přiřadit formát kladných plateb, který byl zadán v předchozím kroku. Na stránce **Bankovní účty** vyberte formát kladných plateb, který odpovídá bankovního účtu. V poli **Počáteční datum kladné platby** zadejte první datum generování souborů kladných plateb. Je důležité zadat datum do tohoto pole. V opačném případě první soubor kladných plateb, který vygenerujete, bude obsahovat všechny šeky, které kdy byly vytvořeny pro tento bankovní účet.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Přiřaďte číselnou řadu pro soubory kladných plateb
Každý soubor kladných plateb musí mít jedinečné číslo. Pomocí karty **Číselné řady** na stránce **Parametry řízení hotovosti a banky** vytvořte číselnou řadu pro soubory kladných plateb.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generování souborů kladných plateb pro jeden bankovní účet
Lze vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet. Ke generování souborů kladných plateb pro více právnických osob a bankovních účtů současně použijte informace v dalším kroku. Pokud chcete vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet, otevřete dialogové okno **Vygenerovat soubor kladných plateb** na stránce **Bankovní účty**. V poli **Datum přerušení** zadejte datum posledního šeku, který má být zahrnut do souboru kladných plateb. V souboru budou zahrnuty všechny šeky, které nebyly zahrnuty do souboru kladných plateb do tohoto data kontroly.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generování souborů kladných plateb pro více bankovních účtů
Pro vygenerování souboru kladných plateb pro bankovních účtů použijte periodickou úlohu **Vygenerovat soubor kladných plateb**. Vyberte formát souboru pro kladné platby a určete, zda chcete vygenerovat soubor pro všechny právnické osoby nebo pro vybranou právnickou osobu. Vyberte také, zda chcete vygenerovat soubor kladných plateb pro všechny bankovní účty, které používají zadaný formát kladné platby, nebo jen pro vybraný bankovní účet. V poli **Datum přerušení** zadejte datum posledního šeku, který má být zahrnut do souboru kladných plateb. V souboru budou zahrnuty všechny šeky, které nebyly zahrnuty do souboru kladných plateb do tohoto data kontroly.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Zobrazení výsledků generování souboru kladných plateb
Poté, co je soubor kladných plateb vygenerován, se výsledky zobrazí na stránce **Souhrnné informace o souboru kladných plateb**. Pokud chcete zobrazit podrobnosti o jednotlivých šecích, můžete použít stránku s podrobnostmi **Soubor kladných plateb**.

## <a name="confirm-a-positive-pay-file"></a>Potvrzení souboru kladných plateb
Po zaplacení šeků, které jsou uvedeny v souboru kladných plateb, obdržíte číslo potvrzení od banky. Poté můžete potvrdit soubor kladných plateb. Na stránce **Souhrnné informace o souboru kladných plateb** vyberte soubor kladných plateb, který má stav **Vytvořeno**, a poté vyberte akci **Zadání potvrzení**. Při potvrzením souboru kladných plateb se pořídí záznam čísla potvrzení od banky.

## <a name="recall-a-positive-pay-file"></a>Odvolat soubor kladných plateb
Pokud je nutné změnit soubor kladných plateb, můžete jej odvolat. Na stránce **Souhrnné informace o souboru kladných plateb** vyberte soubor kladných plateb, který má stav **Vytvořeno**, a poté vyberte akci **Odvolat**. Pro každý šek v souboru kladných plateb se resetuje pole, které označuje, zda byl šek zahrnut do souboru kladných plateb. Poté můžete vytvořit nový soubor kladných plateb, který obsahuje šeky, které byly odvolány.




