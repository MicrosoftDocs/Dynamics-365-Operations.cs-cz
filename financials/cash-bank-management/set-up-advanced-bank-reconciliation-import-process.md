---
title: "Nastavení procesu importu rozšířené bankovního odsouhlasení"
description: "Funkce rozšířeného odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 for Operations. Tento článek vysvětluje, jak nastavit funkci importu pro bankovní výpisy."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: acf7bacf6e95725024ff0a542a059349593d01a0
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Nastavení procesu importu rozšířené bankovního odsouhlasení

[!include[banner](../includes/banner.md)]


Funkce rozšířeného odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 for Operations. Tento článek vysvětluje, jak nastavit funkci importu pro bankovní výpisy. 

Nastavení import bankovního výpisu závisí na formátu vašeho elektronického bankovního výpisu. 365 Microsoft Dynamics pro operace podporuje tři formáty bankovních výpisů z pole: ISO20022 MT940 a BAI2.

## <a name="sample-files"></a>Vzorové soubory
Pro všechny tři formáty musí mít soubory, které překládají elektronický bankovní výpis z původního formátu do formátu, který můžete použít 365 Dynamics pro operace. Požadované soubory s prostředky můžete najít v uzlu **Prostředky** v průzkumníkovi aplikací v aplikaci Microsoft Visual Studio. Po nalezení souborů je zkopírujte na jedno známé umístění, ze kterého je můžete snadno odeslat během procesu instalace.

| Název prostředku                                           | Název souboru                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_k\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_k\_odsouhlasení\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_k\_složené\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_k\_odsouhlasení\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_k\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_k\_odsouhlasení\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Příklady formátů bankovních výpisů a technické rozložení
Následují příklady importu rozšířené bankovního odsouhlasení souboru definice technických rozložení a tři související soubory příkladu bankovních výpisů: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Technická definice rozložení                             | Vzorový soubor s bankovním výpisem          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Nastavení importu bankovních výpisů ISO20022
Nejprve je nutné definovat skupinu pro zpracování formátu bankovních výpisů pro bankovní výpisy ISO20022 pomocí rozhraní datové entity.

1.  Přejít na **prostorů**&gt;**Správa dat**.
2.  Click **Import**.
3.  Zadat název formátu, jako např. **ISO20022**.
4.  V poli **Formát dat zdroje **zadejte **Prvek XML**.
5.  V poli **Název entity** zadejte **Bankovní výpisy**.
6.  Pro odeslání souborů pro import klepněte na tlačítko **Odeslat** a potom vyhledejte a vyberte soubor **SampleBankCompositeEntity.xml**, který jste dříve uložili.
7.  Po odeslání entity bankovního výpisu a po dokončení mapování klepněte na akci **Zobrazit mapu** pro entitu.
8.  Entita bankovního výpisu je složená entita, která se skládá ze čtyř samostatných entit. V seznamu vyberte **BankStatementDocumentEntity** a potom klepněte na akci **Zobrazit mapu**.
9.  Na kartě **Transformace** klikněte na **Nový**.
10. Pro pořadové číslo 1 klepněte na tlačítko **Odeslat soubor** a vyberte soubor** ISO20022XML-to-Reconciliation.xslt**, který jste dříve uložili. **Poznámka:** Dynamics 365 pro operace transformační soubory jsou vytvořeny pro standardní formát. Vzhledem k tomu, že banky často odchýlit se od tohoto formátu, bude pravděpodobně nutné aktualizovat soubor transformace mapovat vaše formát bankovního výpisu. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Click **New**.
12. Pro pořadové číslo 2 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BankReconciliation-to-Composite.xslt**, který jste dříve uložili.
13. Klikněte na **Použít transformace**.

Po nastavení skupiny zpracování formátu je dalším krokem definovat pravidla formátu bankovního výpisu pro bankovní výpisy ISO20022.

1.  Přejít na **řízení hotovosti a banky**&gt;**nastavení**&gt;**rozšířené bankovního odsouhlasení nastavení**&gt;**formát bankovního výpisu**.
2.  Click **New**.
3.  Určete formát výpisu jako například **ISO20022**.
4.  Zadejte název formátu.
5.  Nastavte pole **Skupina zpracování** na skupinu, kterou jste definovali dříve, jako například **ISO20022**.
6.  Zaškrtněte políčko **XML file**.

Posledním krokem je povolení rozšířeného odsouhlasení banky a nastavení formátu výpisu u bankovního účtu.

1.  Přejít na **řízení hotovosti a banky**&gt;**bankovní účty**.
2.  Vyberte bankovní účet a jeho otevřením zobrazte jeho podrobnosti.
3.  Na kartě **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení banky **na **Ano**.
4.  Nastavte pole **Formát výpisu **na formát, který jste vytvořili dříve, jako například **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Nastavení importu bankovních výpisů MT940
Nejprve je nutné definovat skupinu pro zpracování formátu bankovních výpisů pro bankovní výpisy MT940 pomocí rozhraní datové entity.

1.  Přejít na **prostorů**&gt;**Správa dat**.
2.  Click **Import**.
3.  Zadat název formátu, jako např. **MT940**.
4.  V poli **Formát dat zdroje **zadejte **Prvek XML**.
5.  V poli **Název entity** zadejte **Bankovní výpisy**.
6.  Pro odeslání souborů pro import klepněte na tlačítko **Odeslat** a potom vyhledejte a vyberte soubor **SampleBankCompositeEntity.xml**, který jste dříve uložili.
7.  Po odeslání entity bankovního výpisu a po dokončení mapování klepněte na akci **Zobrazit mapu** pro entitu.
8.  Entita bankovního výpisu je složená entita, která se skládá ze čtyř samostatných entit. V seznamu vyberte **BankStatementDocumentEntity** a potom klepněte na akci **Zobrazit mapu**.
9.  Na kartě **Transformace** klikněte na **Nový**.
10. Pro pořadové číslo 1 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **MT940TXT-to-MT940XML.xslt**, který jste dříve uložili.
11. Klepněte na možnost **Nový**.
12. Pro pořadové číslo 2 klepněte na tlačítko **Odeslat soubor** a vyberte soubor** MT940XML-to-Reconciliation.xslt**, který jste dříve uložili. **Poznámka:** Dynamics 365 pro operace transformační soubory jsou vytvořeny pro standardní formát. Vzhledem k tomu, že banky často odchýlit se od tohoto formátu, bude pravděpodobně nutné aktualizovat soubor transformace mapovat vaše formát bankovního výpisu. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Click **New**.
14. Pro pořadové číslo 3 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BankReconciliation-to-Composite.xslt**, který jste dříve uložili.
15. Klikněte na **Použít transformace**.

Po nastavení skupiny zpracování formátu je dalším krokem definovat pravidla formátu bankovního výpisu pro bankovní výpisy MT940.

1.  Přejít na **řízení hotovosti a banky**&gt;**nastavení**&gt;**rozšířené bankovního odsouhlasení nastavení**&gt;**formát bankovního výpisu**.
2.  Click **New**.
3.  Určete formát výpisu jako například **MT940**.
4.  Zadejte název formátu.
5.  Nastavte pole **Skupina zpracování** na skupinu, kterou jste definovali dříve, jako například **MT940**.
6.  Nastavte pole **Typ souboru** na hodnotu **txt**.

Posledním krokem je povolení rozšířeného odsouhlasení banky a nastavení formátu výpisu u bankovního účtu.

1.  Přejít na **řízení hotovosti a banky**&gt;**bankovní účty**.
2.  Vyberte bankovní účet a jeho otevřením zobrazte jeho podrobnosti.
3.  Na kartě **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení banky **na **Ano**.
4.  Po zobrazení výzvy k potvrzení výběru a povolení rozšířeného odsouhlasení banky klepněte na tlačítko **OK**.
5.  Nastavte pole **Formát výpisu** na formát, který jste vytvořili dříve, jako například **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Nastavení importu bankovních výpisů BAI2
Nejprve je nutné definovat skupinu pro zpracování formátu bankovních výpisů pro bankovní výpisy BAI2 pomocí rozhraní datové entity.

1.  Přejít na **prostorů**&gt;**Správa dat**.
2.  Click **Import**.
3.  Zadat název formátu, jako např. **BAI2**.
4.  V poli **Formát dat zdroje **zadejte **Prvek XML**.
5.  V poli **Název entity** zadejte **Bankovní výpisy**.
6.  Pro odeslání souborů pro import klepněte na tlačítko **Odeslat** a potom vyhledejte a vyberte soubor **SampleBankCompositeEntity.xml**, který jste dříve uložili.
7.  Po odeslání entity bankovního výpisu a po dokončení mapování klepněte na akci **Zobrazit mapu** pro entitu.
8.  Entita bankovního výpisu je složená entita, která se skládá ze čtyř samostatných entit. V seznamu vyberte **BankStatementDocumentEntity** a potom klepněte na akci **Zobrazit mapu**.
9.  Na kartě **Transformace** klikněte na **Nový**.
10. Pro pořadové číslo 1 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BAI2CSV-to-BAI2XML.xslt**, který jste dříve uložili.
11. Klepněte na možnost **Nový**.
12. Pro pořadové číslo 2 klepněte na tlačítko **Odeslat soubor** a vyberte soubor** BAI2XML-to-Reconciliation.xslt**, který jste dříve uložili. **Poznámka:** Dynamics 365 pro operace transformační soubory jsou vytvořeny pro standardní formát. Protože banky často odchýlit se od tohoto formátu a bude pravděpodobně nutné aktualizovat soubor transformace mapovat vaše formát bankovního výpisu. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Click **New**.
14. Pro pořadové číslo 3 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BankReconciliation-to-Composite.xslt**, který jste dříve uložili.
15. Klikněte na **Použít transformace**.

Po nastavení skupiny zpracování formátu je dalším krokem definovat pravidla formátu bankovního výpisu pro bankovní výpisy BAI2.

1.  Přejít na **řízení hotovosti a banky**&gt;**nastavení**&gt;**rozšířené bankovního odsouhlasení nastavení**&gt;**formát bankovního výpisu**.
2.  Click **New**.
3.  Určete formát výpisu jako například **BAI2**.
4.  Zadejte název formátu.
5.  Nastavte pole **Skupina zpracování** na skupinu, kterou jste definovali dříve, jako například **BAI2**.
6.  Nastavte pole **Typ souboru** na hodnotu **txt**.

Posledním krokem je povolení rozšířeného odsouhlasení banky a nastavení formátu výpisu u bankovního účtu.

1.  Přejít na **řízení hotovosti a banky**&gt;**bankovní účty**.
2.  Vyberte bankovní účet a jeho otevřením zobrazte jeho podrobnosti.
3.  Na kartě **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení banky **na **Ano**.
4.  Po zobrazení výzvy k potvrzení výběru a povolení rozšířeného odsouhlasení banky klepněte na tlačítko **OK**.
5.  Nastavte pole **Formát výpisu** na formát, který jste vytvořili dříve, jako například **BAI2**.

## <a name="test-the-bank-statement-import"></a>Testování importu bankovního výpisu
Posledním krokem je testování toho, že můžete importovat bankovní výpis.

1.  Přejít na **řízení hotovosti a banky**&gt;**bankovní účty**.
2.  Vyberte bankovní účet, pro který je povolena funkce Rozšířené odsouhlasení banky.
3.  Na kartě **Odsouhlasit** klepněte na tlačítko **Bankovní výpisy**.
4.  Na stránce **Bankovní výpis** klepněte na tlačítko **Import výpisu**.
5.  Nastavte pole **Bankovní účet** na vybraný bankovní účet. Pole **Formát výpisu** bude nastaveno automaticky na základě nastavení v bankovním účtu.
6.  Klepněte na tlačítko **Procházet** a vyberte váš soubor elektronického bankovního výpisu.
7.  Klepněte na položku **Odeslat**.
8.  Klepněte na tlačítko **OK**.

Pokud import proběhne úspěšně, zobrazí se vám zpráva oznamující, že byl výkaz importován. Pokud import nebyl úspěšný, v pracovním prostoru **Správa dat** v části **Historie úlohy** vyhledejte úlohu. Kliknutím na tlačítko **Podrobnosti o spuštění** u úlohy otevřete stránku **Souhrn spuštění** a potom kliknutím na tlačítko **Zobrazit protokol provádění** zobrazte chyby importu.




