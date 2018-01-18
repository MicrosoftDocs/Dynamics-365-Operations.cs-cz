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
ms.search.form: BankStatementFormat
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4feb77bf0031494dfd456c23c632a264c96f0e43
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a>Poradce při potížích s importem souboru bankovního výpisu

[!include[banner](../includes/banner.md)]


Je důležité, aby se rozvržení souboru s bankovním výpisem od banky shodovalo s rozvržením podporovaným v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně. Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky. Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem. V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží.

<a name="what-is-the-error"></a>Kde se stala chyba?
------------------

Při pokusu o import souboru s bankovním výpisem přejděte při hledání chyby k historii úlohy řízení dat a podrobnostem o jejím provedení. Chyba může pomoci tím, že bude ukazovat na řádek výkazu, rozvahy nebo výpisu. Obvykle však neposkytuje dostatek informací k identifikaci pole nebo prvku, který problém způsobil.

## <a name="what-are-the-differences"></a>Jaký je rozdíl?
Srovnejte definici rozvržení bankovního souboru s definicí importu v aplikaci Finance and Operations a poznamenejte si všechny rozdíly v polích a prvcích. Porovnejte soubor bankovního výpisu s příslušným vzorovým souborem aplikace Finance and Operations. V souborech ISO20022 by mělo být možné snadno zjistit rozdíly.

## <a name="transformations"></a>Transformace
Obvykle je nutné provést změny v jedné ze tří transformací. Každá transformace je sestavena pro konkrétní standard.

| Název prostředku                                         | Název souboru                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Ladění transformací
### <a name="adjust-the-bai2-and-mt940-files"></a>Úprava souboru BAI2 a MT940

BAI2 a MT940 jsou textové soubory a vyžadují provedení úprav, než bude možné použít ladění dokumentů XSLT (Extensible Stylesheet Language Transformations). Program tyto úpravy provede při importu souboru.

1.  Vytvořit soubor XML a zkopírujte do něj následující text.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Zkopírujte obsah souboru s bankovním výpisem a vložte jej do souboru XML tak, aby nahradil text **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Ladění souboru XSLT

Další informace naleznete v tématu <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Spusťte Microsoft Visual Studio.
2.  Vytvořte aplikační konzoli.
3.  Otevřete odpovídající soubor XSLT.
4.  Klepněte na XLST a na stránku s jeho vlastnostmi.
5.  jako vstup nastavte umístění souboru s bankovním výpisem.
6.  Zadejte název souboru a jeho umístění pro výstup.
7.  Nastavte požadované zlomové body.
8.  V nabídce klepněte na **XML** &gt; **Spustit ladění XSLT**.

### <a name="format-the-xslt-output"></a>Formátování výstupu XSLT

Po spuštění transformace se vytvoří výstupní soubor, který lze zobrazit v aplikaci Visual Studio. Pomocí kombinace kláves Ctrl + A, Ctrl + K a Ctrl + D můžete výstupní soubor rychle formátovat.

### <a name="adjust-the-transformation"></a>Úprava transformace

Upravením transformace získejte příslušné pole nebo prvek v souboru s bankovním výpisem. Toto pole či prvek pak namapujte na odpovídající prvek aplikace Finance and Operations.

### <a name="debitcredit-indicator"></a>Indikátor má dáti/dal

V některých případech může být hodnota „má dáti“ importována jako hodnota „dal“ a obráceně. K vyřešení tohoto problému je nutné změnit odpovídající soubor XSLT. Pokud bankovní výpisy pocházejí z několika bank, ujistěte se, že všechny používají stejný přístup strany má dáti/dal nebo vytvořte samostatné transformace.

-   Šablona BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator
-   Šablona ISO20022XML-to-Reconcilation.xslt GetCreditDebit
-   Šablona MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Příklady formátů bankovních výpisů a technické rozložení
V následující tabulce jsou uvedeny příklady technických definic rozložení pro komplexní importní soubory s bankovním odsouhlasením a tři související vzorové soubory bankovních výpisů. Můžete stáhnout soubory příkladu a technické rozložení zde: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Technická definice rozložení                             | Vzorový soubor s bankovním výpisem          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |






