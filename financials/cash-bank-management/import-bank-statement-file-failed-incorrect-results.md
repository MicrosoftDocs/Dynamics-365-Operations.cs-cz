---
title: "Bankovní výpis souboru importu Poradce při potížích"
description: "Je důležité, že banky soubor výpisu z banky odpovídají rozložení, které podporuje Microsoft Dynamics 365 pro operace. Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně. Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky. Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem. V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: 9717cf2f36033efe8465906324966242977c6eb2
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-file-import-troubleshooting"></a>Bankovní výpis souboru importu Poradce při potížích

[!include[banner](../includes/banner.md)]


Je důležité, že banky soubor výpisu z banky odpovídají rozložení, které podporuje Microsoft Dynamics 365 pro operace. Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně. Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky. Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem. V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží.

<a name="what-is-the-error"></a>Kde se stala chyba?
------------------

Při pokusu o import souboru s bankovním výpisem přejděte při hledání chyby k historii úlohy řízení dat a podrobnostem o jejím provedení. Chyba může pomoci tím, že bude ukazovat na řádek výkazu, rozvahy nebo výpisu. Obvykle však neposkytuje dostatek informací k identifikaci pole nebo prvku, který problém způsobil.

## <a name="what-are-the-differences"></a>Jaký je rozdíl?
Definice rozložení bankovního souboru, který chcete 365 Microsoft Dynamics pro definici importu operace porovnání a zaznamenejte rozdíly v polích a prvky. Porovnejte soubor výpisu bankovního související ukázku Dynamics 365 pro operace soubor. V souborech ISO20022 by měl být snadno zjistit rozdíly.

## <a name="transformations"></a>Transformace
Obvykle je nutné provést změny v jedné ze tří transformací. Každá transformace je sestavena pro konkrétní standard.

| Název prostředku                                         | Název souboru                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_k\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_k\_odsouhlasení\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_k\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

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
8.  V nabídce klepněte na příkaz **XML**&gt;**spustit ladění XSLT**.

### <a name="format-the-xslt-output"></a>Formátování výstupu XSLT

Po spuštění transformace se vytvoří výstupní soubor, který lze zobrazit v aplikaci Visual Studio. Pomocí kombinace kláves Ctrl + A, Ctrl + K a Ctrl + D můžete výstupní soubor rychle formátovat.

### <a name="adjust-the-transformation"></a>Úprava transformace

Upravením transformace získejte příslušné pole nebo prvek v souboru s bankovním výpisem. Pak odpovídající 365 Dynamics operací prvku mapování tohoto pole nebo prvek.

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






