---
title: Nastavení procesu importu rozšířené bankovního odsouhlasení
description: Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 Finance. Tento článek vysvětluje, jak nastavit funkci importu pro bankovní výpisy.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60195962e50817b4d85840a2464848db6e666f46
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716011"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Nastavení procesu importu rozšířené bankovního odsouhlasení

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tato funkce bude v září 2022 ukončena, noví uživatelé by měli používat elektronické hlášení. Další informace viz [Nastavení procesu importu rozšířené bankovního odsouhlasení pomocí elektronického výkaznictví](../accounts-payable/import-bai2-er.md).


Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Dynamics 365 Finance. Tento článek vysvětluje, jak nastavit funkci importu pro bankovní výpisy. 

Nastavení import bankovního výpisu závisí na formátu vašeho elektronického bankovního výpisu. Aplikace Finance standardně podporuje tři formáty bankovního příkazu: ISO20022, MT940 a BAI2.

## <a name="set-time-zone-preference"></a>Nastavení upřednostňovaného časového pásma
Při konfiguraci nastavení importu bankovního výpisu může být důležité zvážit časové pásmo v rámci souborů bankovních výpisů, které budou importovány. Ve výchozím nastavení se předpokládá, že hodnoty data a času jsou již v koordinovaném světovém čase (standard UTC) a při importu dat se nepoužije žádný převod časového pásma. 

K dispozici je možnost pro určení časového pásma, které se má použít pro import dat. Tato možnost je k dispozici v poli **předvolba časového pásma** na každé stránce **Podrobnosti o zdrojovém formátu data** (pevná záložka **Pracovní prostor > Správa dat data > Konfigurovat zdroje dat > Výběr formátu dat > Místní nastavení**). Tato předvolba časového pásma se použije pro všechny importy, které používají tento formát zdrojových dat. Chcete-li importovat data z více časových pásem, můžete vytvořit libovolný počet formátů zdroje dat.  

Toto časové pásmo nemusí být stejné jako časové pásmo uživatele nebo společnosti, proto je nutné vyjasnit, jaké časové pásmo aplikace data a času používá. Při nastavování předvoleb časového pásma doporučujeme zvážit následující body. 

 - Tato předvolba časového pásma se použije pro všechny importy, které používají tento formát zdrojových dat. Chcete-li importovat data z více časových pásem, můžete vytvořit libovolný počet formátů zdroje dat. 
 
 - Předvolbou časového pásma by mělo být místní časové pásmo data a času v souboru importu. 
 
 - Časové pásmo data a času nemusí být stejné jako časové pásmo uživatele nebo společnosti.
 
 - Uživatelé mohou pomocí svých **uživatelských možností** upravit vlastní časové pásmo.

Všimněte si, že následující akce mohou pomoci minimalizovat potenciální konflikty data a času při importu bankovních výpisů. 

 - Neměňte předvolby časových pásem pro bankovní účty, pro které již byly výpisy importovány. Změna přednastavení časového pásma může mít dopad na pořadí nových příkazů vzhledem ke stávajícím příkazům z důvodu úpravy časového pásma. 
 
 - Zkontrolujte všechny importy, které používají vybraný formát zdroje dat. Priorita časového pásma zadaná pro formát bude použita pro všechny importní projekty, které tento formát používají. Ověřte, zda je předvolba časového pásma vhodná pro všechny importní projekty, které tento formát používají.

## <a name="sample-files"></a>Vzorové soubory
Pro všechny tři formáty musíte mít soubory, které překládají elektronický bankovní výpis z původního formátu do formátu, který aplikace Finance může použít. Požadované soubory s prostředky můžete najít v uzlu **Prostředky** v průzkumníkovi aplikací v aplikaci Microsoft Visual Studio. Po nalezení souborů je zkopírujte na jedno známé umístění, ze kterého je můžete snadno odeslat během procesu instalace.

| Název prostředku                                           | Název souboru                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Příklady formátů bankovních výpisů a technické rozložení
Níže jsou uvedeny příklady technických definic rozložení pro komplexní importní soubory s bankovním odsouhlasením a tři související [vzorové soubory bankovních výpisů](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Technická definice rozložení                             | Vzorový soubor s bankovním výpisem          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Nastavení importu bankovních výpisů ISO20022
Nejprve je nutné definovat skupinu pro zpracování formátu bankovních výpisů pro bankovní výpisy ISO20022 pomocí rozhraní datové entity.

1.  Přejděte na **Pracovní prostory** &gt; **Správa dat**.
2.  Klepněte na tlačítko **Import**.
3.  Zadat název formátu, jako např. **ISO20022**.
4.  V poli **Formát dat zdroje** zadejte **Prvek XML**.
5.  V poli **Název entity** zadejte **Bankovní výpisy**.
6.  Pro odeslání souborů pro import klepněte na tlačítko **Odeslat** a potom vyhledejte a vyberte soubor **SampleBankCompositeEntity.xml**, který jste dříve uložili.
7.  Po odeslání entity bankovního výpisu a po dokončení mapování klepněte na akci **Zobrazit mapu** pro entitu.
8.  Entita bankovního výpisu je složená entita, která se skládá ze čtyř samostatných entit. V seznamu vyberte **BankStatementDocumentEntity** a potom klepněte na akci **Zobrazit mapu**.
9.  Na kartě **Transformace** klikněte na **Nový**.
10. Pro pořadové číslo 1 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **ISO20022XML-to-Reconciliation.xslt**, který jste dříve uložili. **Poznámka:** Transformační soubory Dynamics AX jsou vytvořeny pro standardní formát. Vzhledem k tomu, že banka se často odchyluje od tohoto formátu, bude možná nutné aktualizovat soubor transformace tak, aby mapoval váš formát bankovního výpisu. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Klepněte na možnost **Nový**.
12. Pro pořadové číslo 2 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BankReconciliation-to-Composite.xslt**, který jste dříve uložili.
13. Klikněte na **Použít transformace**.

Po nastavení skupiny zpracování formátu je dalším krokem definovat pravidla formátu bankovního výpisu pro bankovní výpisy ISO20022.

1.  Přejděte do nabídky **Pokladna a banka** &gt; **Nastavení** &gt; **Nastavení rozšířeného odsouhlasení banky** &gt; **Formát bankovního výpisu**.
2.  Klepněte na možnost **Nový**.
3.  Určete formát výpisu jako například **ISO20022**.
4.  Zadejte název formátu.
5.  Nastavte pole **Skupina zpracování** na skupinu, kterou jste definovali dříve, jako například **ISO20022**.
6.  Zaškrtněte políčko **XML file**.

Posledním krokem je povolení rozšířeného odsouhlasení banky a nastavení formátu výpisu u bankovního účtu.

1.  Přejděte do části **Pokladna a banka** &gt; **Bankovní účty**.
2.  Vyberte bankovní účet a jeho otevřením zobrazte jeho podrobnosti.
3.  Na kartě **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení banky** na **Ano**.
4.  Nastavte pole **Formát výpisu** na formát, který jste vytvořili dříve, jako například **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Nastavení importu bankovních výpisů MT940
Nejprve je nutné definovat skupinu pro zpracování formátu bankovních výpisů pro bankovní výpisy MT940 pomocí rozhraní datové entity.

1.  Přejděte na **Pracovní prostory** &gt; **Správa dat**.
2.  Klepněte na tlačítko **Import**.
3.  Zadat název formátu, jako např. **MT940**.
4.  V poli **Formát dat zdroje** zadejte **Prvek XML**.
5.  V poli **Název entity** zadejte **Bankovní výpisy**.
6.  Pro odeslání souborů pro import klepněte na tlačítko **Odeslat** a potom vyhledejte a vyberte soubor **SampleBankCompositeEntity.xml**, který jste dříve uložili.
7.  Po odeslání entity bankovního výpisu a po dokončení mapování klepněte na akci **Zobrazit mapu** pro entitu.
8.  Entita bankovního výpisu je složená entita, která se skládá ze čtyř samostatných entit. V seznamu vyberte **BankStatementDocumentEntity** a potom klepněte na akci **Zobrazit mapu**.
9.  Na kartě **Transformace** klikněte na **Nový**.
10. Pro pořadové číslo 1 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **MT940TXT-to-MT940XML.xslt**, který jste dříve uložili.
11. Klepněte na možnost **Nový**.
12. Pro pořadové číslo 2 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **MT940XML-to-Reconciliation.xslt**, který jste dříve uložili. **Poznámka:** Transformační soubory Dynamics AX jsou vytvořeny pro standardní formát. Vzhledem k tomu, že banka se často odchyluje od tohoto formátu, bude možná nutné aktualizovat soubor transformace tak, aby mapoval váš formát bankovního výpisu. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Klepněte na možnost **Nový**.
14. Pro pořadové číslo 3 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BankReconciliation-to-Composite.xslt**, který jste dříve uložili.
15. Klikněte na **Použít transformace**.

Po nastavení skupiny zpracování formátu je dalším krokem definovat pravidla formátu bankovního výpisu pro bankovní výpisy MT940.

1.  Přejděte do nabídky **Pokladna a banka** &gt; **Nastavení** &gt; **Nastavení rozšířeného odsouhlasení banky** &gt; **Formát bankovního výpisu**.
2.  Klepněte na možnost **Nový**.
3.  Určete formát výpisu jako například **MT940**.
4.  Zadejte název formátu.
5.  Nastavte pole **Skupina zpracování** na skupinu, kterou jste definovali dříve, jako například **MT940**.
6.  Nastavte pole **Typ souboru** na hodnotu **txt**.

Posledním krokem je povolení rozšířeného odsouhlasení banky a nastavení formátu výpisu u bankovního účtu.

1.  Přejděte do části **Pokladna a banka** &gt; **Bankovní účty**.
2.  Vyberte bankovní účet a jeho otevřením zobrazte jeho podrobnosti.
3.  Na kartě **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení banky** na **Ano**.
4.  Po zobrazení výzvy k potvrzení výběru a povolení rozšířeného odsouhlasení banky klepněte na tlačítko **OK**.
5.  Nastavte pole **Formát výpisu** na formát, který jste vytvořili dříve, jako například **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Nastavení importu bankovních výpisů BAI2
Nejprve je nutné definovat skupinu pro zpracování formátu bankovních výpisů pro bankovní výpisy BAI2 pomocí rozhraní datové entity.

1.  Přejděte na **Pracovní prostory** &gt; **Správa dat**.
2.  Klepněte na tlačítko **Import**.
3.  Zadat název formátu, jako např. **BAI2**.
4.  V poli **Formát dat zdroje** zadejte **Prvek XML**.
5.  V poli **Název entity** zadejte **Bankovní výpisy**.
6.  Pro odeslání souborů pro import klepněte na tlačítko **Odeslat** a potom vyhledejte a vyberte soubor **SampleBankCompositeEntity.xml**, který jste dříve uložili.
7.  Po odeslání entity bankovního výpisu a po dokončení mapování klepněte na akci **Zobrazit mapu** pro entitu.
8.  Entita bankovního výpisu je složená entita, která se skládá ze čtyř samostatných entit. V seznamu vyberte **BankStatementDocumentEntity** a potom klepněte na akci **Zobrazit mapu**.
9.  Na kartě **Transformace** klikněte na **Nový**.
10. Pro pořadové číslo 1 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BAI2CSV-to-BAI2XML.xslt**, který jste dříve uložili.
11. Klepněte na možnost **Nový**.
12. Pro pořadové číslo 2 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BAI2XML-to-Reconciliation.xslt**, který jste dříve uložili. **Poznámka:** Transformační soubory Dynamics AX jsou vytvořeny pro standardní formát. Vzhledem k tomu, že banka se často odchyluje od tohoto formátu, bude možná nutné aktualizovat soubor transformace tak, aby mapoval váš formát bankovního výpisu. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Klepněte na možnost **Nový**.
14. Pro pořadové číslo 3 klepněte na tlačítko **Odeslat soubor** a vyberte soubor **BankReconciliation-to-Composite.xslt**, který jste dříve uložili.
15. Klikněte na **Použít transformace**.

Po nastavení skupiny zpracování formátu je dalším krokem definovat pravidla formátu bankovního výpisu pro bankovní výpisy BAI2.

1.  Přejděte do nabídky **Pokladna a banka** &gt; **Nastavení** &gt; **Nastavení rozšířeného odsouhlasení banky** &gt; **Formát bankovního výpisu**.
2.  Klepněte na možnost **Nový**.
3.  Určete formát výpisu jako například **BAI2**.
4.  Zadejte název formátu.
5.  Nastavte pole **Skupina zpracování** na skupinu, kterou jste definovali dříve, jako například **BAI2**.
6.  Nastavte pole **Typ souboru** na hodnotu **txt**.

Posledním krokem je povolení rozšířeného odsouhlasení banky a nastavení formátu výpisu u bankovního účtu.

1.  Přejděte do části **Pokladna a banka** &gt; **Bankovní účty**.
2.  Vyberte bankovní účet a jeho otevřením zobrazte jeho podrobnosti.
3.  Na kartě **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení banky** na **Ano**.
4.  Po zobrazení výzvy k potvrzení výběru a povolení rozšířeného odsouhlasení banky klepněte na tlačítko **OK**.
5.  Nastavte pole **Formát výpisu** na formát, který jste vytvořili dříve, jako například **BAI2**.

## <a name="test-the-bank-statement-import"></a>Testování importu bankovního výpisu
Posledním krokem je testování toho, že můžete importovat bankovní výpis.

1.  Přejděte do části **Pokladna a banka** &gt; **Bankovní účty**.
2.  Vyberte bankovní účet, pro který je povolena funkce Rozšířené odsouhlasení banky.
3.  Na kartě **Odsouhlasit** klepněte na tlačítko **Bankovní výpisy**.
4.  Na stránce **Bankovní výpis** klepněte na tlačítko **Import výpisu**.
5.  Nastavte pole **Bankovní účet** na vybraný bankovní účet. Pole **Formát výpisu** bude nastaveno automaticky na základě nastavení v bankovním účtu.
6.  Klepněte na tlačítko **Procházet** a vyberte váš soubor elektronického bankovního výpisu.
7.  Klepněte na položku **Odeslat**.
8.  Klepněte na tlačítko **OK**.

Pokud import proběhne úspěšně, zobrazí se vám zpráva oznamující, že byl výkaz importován. Pokud import nebyl úspěšný, v pracovním prostoru **Správa dat** v části **Historie úlohy** vyhledejte úlohu. Kliknutím na tlačítko **Podrobnosti o spuštění** u úlohy otevřete stránku **Souhrn spuštění** a potom kliknutím na tlačítko **Zobrazit protokol provádění** zobrazte chyby importu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
