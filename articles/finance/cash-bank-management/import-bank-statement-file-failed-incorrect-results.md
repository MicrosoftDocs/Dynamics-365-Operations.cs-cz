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
ms.openlocfilehash: dc5b9cf3449b48767a27891a019f8fe8df2a900559898e3cb1849d25bec7c987
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757114"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Poradce při potížích s importem souboru bankovního výpisu

[!include [banner](../includes/banner.md)]

Je důležité, aby se soubor s bankovním výpisem z banky shodoval s rozvržením podporovaným v aplikaci Microsoft Dynamics 365 Finance. Díky přísným standardům pro bankovní výpisy bude většina integrací fungovat správně. Někdy však soubor s prohlášením nemusí být možné importovat, nebo bude obsahovat nesprávné výsledky. Tyto problémy jsou obvykle způsobeny drobnými rozdíly v souboru s bankovním výpisem. V tomto článku je popsán postup pro vyřešení těchto rozdílů a potíží.

## <a name="what-is-the-error"></a>Kde se stala chyba?

Při pokusu o import souboru s bankovním výpisem přejděte při hledání chyby k historii úlohy řízení dat a podrobnostem o jejím provedení. Chyba může pomoci tím, že bude ukazovat na řádek výkazu, rozvahy nebo výpisu. Obvykle však neposkytuje dostatek informací k identifikaci pole nebo prvku, který problém způsobil.

> [!NOTE]
> Importované bankovní výpisy se mohou překrývat pouze pro jeden bod v čase.  Například pokud výpis končí 1. ledna 2021 v 0:00, počáteční datum dalšího výpisu může být 1. ledna 2021 v 0:00.

## <a name="what-are-the-differences"></a>Jaký je rozdíl?
Srovnejte definici rozvržení bankovního souboru s definicí importu v aplikaci Finance a poznamenejte si všechny rozdíly v polích a prvcích. Porovnejte soubor bankovního výpisu s příslušným vzorovým souborem aplikace Finance. V souborech ISO20022 by mělo být možné snadno zjistit rozdíly.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Rozdíly v časových pásmech u importovaných bankovních výpisů
Hodnoty data a času v importním souboru se mohou lišit od hodnot data a času zobrazených ve Finance and Operations. Chcete-li zabránit této nesrovnalosti, zadejte prioritu časového pásma na stránce **Konfigurovat zdroje dat**. Informace o zadání předvoleb pro časové pásmo najdete v tématu [Nastavení procesu importu pokročilého odsouhlasení banky](set-up-advanced-bank-reconciliation-import-process.md).

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

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Zkopírujte obsah souboru s bankovním výpisem a vložte jej do souboru XML tak, aby nahradil text **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Ladění souboru XSLT

Další informace naleznete v tématu <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Spusťte aplikaci Microsoft Visual Studio.
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

Upravením transformace získejte příslušné pole nebo prvek v souboru s bankovním výpisem. Toto pole či prvek pak namapujte na odpovídající prvek aplikace Finance.

### <a name="debitcredit-indicator"></a>Indikátor má dáti/dal

V některých případech může být hodnota „má dáti“ importována jako hodnota „dal“ a obráceně. K vyřešení tohoto problému je nutné změnit odpovídající soubor XSLT. Pokud bankovní výpisy pocházejí z několika bank, ujistěte se, že všechny používají stejný přístup strany má dáti/dal nebo vytvořte samostatné transformace.

-   Šablona BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator
-   Šablona ISO20022XML-to-Reconcilation.xslt GetCreditDebit
-   Šablona MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Příklady formátů bankovních výpisů a technické rozložení
V následující tabulce jsou uvedeny příklady technických definic rozložení pro komplexní importní soubory s bankovním odsouhlasením a tři související vzorové soubory bankovních výpisů. Zde můžete stáhnout vzorové soubory a technická rozvržení: [Import ukázkových souborů](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Technická definice rozložení                             | Vzorový soubor s bankovním výpisem          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
