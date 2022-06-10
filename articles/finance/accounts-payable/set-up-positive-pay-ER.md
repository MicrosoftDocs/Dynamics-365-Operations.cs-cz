---
title: Nastavte a vygenerujte soubory kladných plateb pomocí elektronického výkaznictví
description: Toto téma vysvětluje postup při nastavení kladných plateb pomocí elektronického výkaznictví.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: bc2f17d62b429b599d5ac5f2a521819275d36b64
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770240"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Nastavte soubory kladných plateb pomocí elektronického výkaznictví

Toto téma vysvětluje postup při nastavení kladných plateb a generování souborů kladných plateb s využitím Elektronického výkaznictví.

> [!NOTE] 
> Před použitím funkce **Generování souborů kladných plateb banky** budete muset nejprve aktualizovat seznam entit.
> Přejděte na **Správa dat > Import / Export > Parametry architektury** 
> pevná záložka **Nastavení entity** a vyberte **Aktualizovat seznam entit**.


Nastavte kladné platby pro generování elektronických seznamů šeků, které jsou dodávány bance. Při předložení šeku bance ho banka srovná se seznamem šeků. Pokud šek odpovídá tomu, co má banka má v záznamech v seznamu, banka jej zúčtuje. Pokud šek neodpovídá šeku v seznamu, banka předloží šek ke kontrole.

## <a name="security-for-positive-pay-files"></a>Zabezpečení pro soubory kladných plateb
Soubory kladných plateb mohou obsahovat citlivé informace o příjemcích plateb a šekových částkách. Nezapomeňte tedy použít dostatečná opatření od doby vytvoření souborů do jejich přijetí do banky. Soubory kladných plateb budou staženy do umístění, které je zadáno ve webovém prohlížeči. Vzhledem k tomu, že soubory kladných plateb mohou obsahovat důvěrné informace, je důležité, aby k vytváření a prohlížení těchto informací v aplikaci Microsoft Dynamics 365 Finance měli přístup pouze oprávnění uživatelé. V následující tabulce naleznete postup, jak určit potřebná oprávnění.

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

## <a name="set-up-the-electronic-reporting-configuration"></a>Nastavte konfiguraci elektronického výkaznictví

1. Přejděte na **Pracovní prostory \> Elektronické sestavy**.
2. Na dlaždici pro poskytovatele konfigurace **Microsoft** vyberte **Úložiště**.
3. Vyberte **Globální** a potom vyberte **Otevřít**.
4. Pokud je nutné vytvořit připojení k úložišti, vyberte v dialogovém okně modrý odkaz.
5. V seznamu konfigurace vyhledejte a vyberte **Model kladných plateb \> Formát kladných plateb**.
6. Na pevné záložce **Verze** zvolte nejnovější verzi a poté zvolte **Importovat**.

## <a name="set-up-a-positive-pay-format"></a>Nastavení formátu kladné platby

1. Přejděte do **Pokladna a banka \> Nastavení \> Formáty kladných plateb**.
2. Zvolte **Nové**.
3. Nastavte pole **Formát plateb** a **Popis**.
4. Vyberte zaškrtávací políčko **Obecný formát elektronického exportu**.
5. Nastavte pole **Konfigurace formátu exportu** na **Formát kladných plateb**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Přiřazení formátu kladné platby k bankovnímu účtu
Pro každý bankovní účet, pro který chcete generovat informace o souborech kladných plateb, musíte přiřadit formát kladných plateb, který byl zadán v předchozím kroku. Na stránce Bankovní účty vyberte formát kladných plateb, který odpovídá bankovního účtu. V poli **Počáteční datum kladné platby** zadejte první datum generování souborů kladných plateb. 

>[!Important]
> Zadejte datum v poli **Počáteční datum kladných plateb**. Pokud ho necháte prázdné, první soubor kladných plateb, který vygenerujete, bude obsahovat všechny šeky, které byly vytvořeny pro tento bankovní účet.

1. Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Otevřete bankovní účet.
3. Na pevné záložce **Všeobecné** nastavte pole **Formát kladných plateb** na formát, který byl vytvořen dříve.
4. Nastavte pole **Počáteční datum kladných plateb** na aktuální datum.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Přiřaďte číselnou řadu pro soubory kladných plateb
Každý soubor kladných plateb musí mít jedinečné číslo. Na stránce **Parametry řízení hotovosti a banky** vytvořte číselnou řadu pro soubory kladných plateb na kartě **Číselné řady**.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generování souborů kladných plateb pro jeden bankovní účet
Lze vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet. Ke generování souborů kladných plateb pro více právnických osob a bankovních účtů současně použijte informace v dalším kroku. Pokud chcete vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet, otevřete dialogové okno **Vygenerovat soubor kladných plateb** na stránce **Bankovní účty**. V poli **Datum přerušení** zadejte datum posledního šeku, který má být zahrnut do souboru kladných plateb. V souboru budou zahrnuty všechny šeky, které nebyly zahrnuty do souboru kladných plateb do tohoto data kontroly.

1. Přejděte na **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Otevřete bankovní účet, pro který je nastavena kladná platba.
3. Vyberte **Spravujte platby \> Kladná platba \> Soubor kladných plateb**.
4. Nastavte pole **Datum přerušení**. Kontroly generované před tímto datem budou zahrnuty.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generování souborů kladných plateb pro více bankovních účtů
Pro vygenerování souboru kladných plateb pro bankovních účtů použijte periodickou úlohu **Soubor kladných plateb**. Vyberte formát souboru pro kladné platby a určete, zda chcete vygenerovat soubor pro všechny právnické osoby nebo pro vybranou právnickou osobu. Vyberte také, zda chcete vygenerovat soubor kladných plateb pro všechny bankovní účty, které používají zadaný formát kladné platby, nebo jen pro vybraný bankovní účet. V poli **Datum přerušení** zadejte datum posledního šeku, který má být zahrnut do souboru kladných plateb. V souboru budou zahrnuty všechny šeky, které nebyly zahrnuty do souboru kladných plateb do tohoto data kontroly.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Zobrazení výsledků generování souboru kladných plateb
Poté, co je soubor kladných plateb vygenerován, se výsledky zobrazí na stránce **Souhrnné informace o souboru kladných plateb**. Pokud chcete zobrazit podrobnosti o jednotlivých šecích, přejděte na stránku **Podrobnosti souboru kladných plateb**.

## <a name="confirm-a-positive-pay-file"></a>Potvrzení souboru kladných plateb
Po zaplacení šeků, které jsou uvedeny v souboru kladných plateb, obdržíte číslo potvrzení od banky. Poté můžete potvrdit soubor kladných plateb. Na stránce **Souhrnné informace o souboru kladných plateb** vyberte soubor kladných plateb, který má stav **Vytvořeno**, a poté vyberte akci **Zadání potvrzení**. Při potvrzením souboru kladných plateb se pořídí záznam čísla potvrzení od banky.

## <a name="recall-a-positive-pay-file"></a>Odvolat soubor kladných plateb
Pokud je nutné změnit soubor kladných plateb, můžete jej odvolat. Na stránce **Souhrnné informace o souboru kladných plateb** vyberte soubor kladných plateb, který má stav **Vytvořeno**, a poté vyberte akci **Odvolat**. Pro každý šek v souboru kladných plateb se resetuje pole, které označuje, zda byl šek zahrnut do souboru kladných plateb. Poté můžete vytvořit nový soubor kladných plateb, který obsahuje šeky, které byly odvolány.


Výsledný soubor XML bude stažen.
