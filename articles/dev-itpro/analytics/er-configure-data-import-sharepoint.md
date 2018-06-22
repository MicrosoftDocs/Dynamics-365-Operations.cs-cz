---
title: Konfigurace importu dat z aplikace SharePoint
description: "Toto téma vysvětluje postup při importu dat z aplikace Microsoft SharePoint."
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Konfigurace importu dat z aplikace SharePoint

[!include[banner](../includes/banner.md)]

Při importu dat z příchozího souboru pomocí rozhraní elektronických sestav (ER) musíte konfigurovat formát ER, který podporuje import, a spustit mapování modelu typu **cíl**, který tento formát používá jako zdroj dat. Pokud chcete provést import dat, přejděte do souboru, který chcete importovat. Vstupní soubor může ručně vybrat uživatel. S novou možností ER podporovat import dat z aplikace Microsoft SharePoint tento proces lze konfigurovat jako bezobslužný. Konfigurace ER lze použít k provádění importu dat ze souborů, které jsou uloženy ve složkách Microsoft SharePoint. Toto téma vysvětluje, jak provedete import ze služby SharePoint do Microsoft Dynamics 365 for Finance and Operations. Tyto příklady používají transakcí dodavatele jako obchodní data.

## <a name="prerequisites"></a>Požadavky
Pro dokončení příkladů v tomto tématu musíte mít následující přístup:

- Přístup k aplikaci Finance and Operations pro některou z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Přístup k instanci serveru SharePoint, který je konfigurován k použití s aplikací Finance and Operations
- Konfigurace formátu a modelu ER pro platby 1099

### <a name="create-required-er-configurations"></a>Vytvoření požadovaných konfigurací ER
Přehrajte si průvodce záznamem úloh **ER Import dat ze souboru aplikace Microsoft Excel**, kteří jsou součástí obchodního procesu **7.5.4.3 Acquire/Develop IT service/solution components (10677)**. Tito průvodci záznamem úloh vás provedou procesem navrhování a použití konfigurací ER pro interaktivní import transakcí dodavatele z externích souborů aplikace Microsoft Excel. Další informace naleznete v tématu [analýza příchozích dokumentů do aplikace Microsoft Excel](parse-incoming-documents-excel.md). Nakonec budete mít:

- Konfigurace ER:

    - Konfigurace modelu ER, **model platby 1099**
    - Konfigurace formátu ER **formát pro import transakcí dodavatelů z aplikace Excel**

[![Konfigurace ER pro import dat ze služby SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Ukázka vstupního souboru pro import dat:

    - Soubor Excel **1099import data.xlsx**, s transakcemi dodavatele, které je nutné importovat do modulu Finance and Operations

[![Vzorový soubor aplikace Microsoft Excel pro import ze služby SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Formát pro import transakcí dodavatele je vybrán jako výchozí mapování modelu. Proto když spustíte mapování modelu **model platby 1099**, které je typu **Do cíle**, mapování modelu spustít tento formát pro import dat z externích souborů. Následně tato data použije k aktualizaci tabulek aplikace.

## <a name="configure-document-management-parameters"></a>Konfigurace parametrů správy dokumentů
1. Na stránce **Parametry správy dokumentů**, nakonfigurujte přístup k instanci serveru SharePoint, který bude používán ve společnosti, do které jste aktuálně přihlášení. V tomto příkladu je společnost USMF.
2. Zkontrolujte připojení k instanci serveru SharePoint, abyste se ujistili, že máte udělen přístup.

[![Nastavení správy dokumentů – server SharePoint](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Otevřete konfigurovaný web služby SharePoint a vytvořte následující složky, kde jsou uloženy příchozí soubory:

    - Zdroj importu souborů (hlavní)
    - Zdroj importu souborů (alternativní)

[![Nastavení správy dokumentů – server SharePoint](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Nastavení správy dokumentů – server SharePoint](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. V aplikaci Finance and Operations na stránce **Typy dokumentů** vytvořte následující typy dokumentu, které se použijí pro přístup ke složkám služby SharePoint, které jste právě vytvořili:

    - Hlavní SP
    - Alternativní SP

5. Pro vytvořené typy dokumentů v poli **Skupina** zadejte **Soubor** a do pole **Umístění** zadejte **SharePoint**. Pak zadejte adresu složky služby SharePoint:

    - Pro typ dokumentu **Hlavní SP**: zdroj importu souborů (hlavní)
    - Pro typ dokumentu **Alternativní SP**: zdroj importu souborů (alternativní)

[![Nastavení služby SharePoint - nový typ dokumentu](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Konfigurace zdrojů ER pro formát ER
1. Klikněte na **Správa organizace** > **Elektronická sestava** > **Úlohy elektronických sestav**.
2. Na stránce **Zdroj elektronického výkaznictví** nakonfigurujte zdrojové soubory pro import dat pomocí konfigurovaného ER formátu.
3. Definujte název masky souboru, aby byly importovány pouze soubory s příponou XLSX. Maska názvu souboru je volitelná a používá se pouze v případě, že byla definována. Můžete definovat pouze jednu masku pro každý formát ER.
4. Vyberte obě složky serveru SharePoint, které jste předtím vytvořili.

[![Nastavení zdroje souborů ER](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>*Zdroj* je definován individuálně pro každou společnost aplikace. Naopak *konfigurace* ER jsou sdíleny mezi společnostmi.

> [!NOTE]
> Když odstraníte nastavení zdroje ER zdroj pro formát ER, budou také odstraněny všechny připojené stavy souborů (viz níže).

## <a name="review-the-files-states-for-the-er-format"></a>Zkontrolujte stavy souborů ve formátu ER
1. Na stránce **Zdroj elektronického vykazování** vyberte **Stavy souboru pro zdroje** ke kontrole obsahu konfigurovaných zdrojů souboru pro aktuální formát ER.
2. V části **soubory** zkontrolujte seznam souborů. Tento seznam nabízí následující:

    - Zdrojové soubory, které jsou použitelné, jsou založené na masce názvu souboru (Pokud je maska souboru definovaná) a které jsou připraveny pro import dat. Pro tyto soubory je oddíl **zdroje protokolu formátu importu** prázdný.
    - Dříve importované soubory. Pro každý z těchto souborů v části **zdroje protokolu formátu importu** je možné zkontrolovat historii importu souboru.

Lze rovněž otevřít stránku **stavy souboru pro zdroje** výběrem možnosti **Správa organizace** \> **elektronické vykazování** \> **Stavy souboru pro zdroje**. V tomto případě stránka obsahuje informace o zdrojích souboru pro všechny formáty ER, pro které byly ve společnosti, do které jste aktuálně přihlášení, nakonfigurovány zdroje souborů.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Import dat ze souborů aplikace Excel, které jsou ve složce služby SharePoint
1. V rámci služby SharePoint, nahrajte soubor aplikace Microsoft Excel **1099import data.xlsx**, který obsahuje transakce dodavatele, do složky služby SharePoint **zdroj souborů importu (hlavní)**, kterou jste předtím vytvořili.

[![Obsah služby SharePoint - soubor aplikace Microsoft Excel pro import](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. V modulu Finance and Operations na stránce **Stavy souboru pro zdroje** vyberte **aktualizovat** k obnovení stránky. Všimněte si, že je soubor aplikace Excel, který byl nahrán do služby SharePoint, se zobrazil v tomto formuláři se stavem **Připraven**. Jsou podporovány následující stavy:

    - **Připraveno** – přiřazené automaticky pro každý nový soubor ve složce služby SharePoint. Tento stav znamená, že je soubor připraven k importu.
    - **Import** – přiřazené automaticky sestavou ER, když soubor bude uzamčen procesem importu, aby se zabránilo jeho použití jinými postupy (pokud je jich mnoho spuštěno současně).
    - **Importované** – přiřazené automaticky podle vyúčtování ER po úspěšném dokončení importu souboru. Tento stav znamená, že importovaný soubor byl odstraněn ze zdroje konfigurovaných souborů (složka SharePoint).
    - **Neúspěšné** – přiřazené automaticky podle vyúčtování ER po dokončení importu souboru s chybami nebo výjimkami.
    - **Blokování** – přiřazené ručně uživatelem v tomto formuláři. Tento stav znamená, že soubor nyní nebude importován. Tento stav slouží k odložení importu některých souborů.

[![Stránka stavů souboru ER pro vybrané zdroje](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Import dat ze souborů služby SharePoint
1. Otevřete strom konfigurace ER, vyberte **model platby 1099**a rozbalte seznam součástí modelu ER.
2. Vyberte název mapování modelu pro otevření seznamu mapování modelu vybrané konfigurace modelu ER.

[![Stránka stavů souboru ER pro vybrané zdroje](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Vyberte **spustit** ke spuštění mapování vybraného modelu. Vzhledem k tomu, že jste nakonfigurovali zdroje souboru pro formát ER, můžete změnit nastavení možnosti **zdroj souboru** podle potřeby. Ponecháte-li nastavení této možnosti, soubory XLSX jsou importovány z konfigurovaných zdrojů (složky serveru SharePoint, v tomto příkladu).

    V tomto příkladu importujete jen jeden soubor. Avšak pokud existuje více souborů, jsou vybrány pro import v pořadí, ve kterém byly přidány do složky služby SharePoint. Každé spuštění formátu ER importuje jeden vybraný soubor.

[![Spustit mapování modelu ER](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Mapování modelu lze spustit bezobslužně v dávkovém režimu. V takovém případě pokaždé, když je dávka spuštěna v tomto formátu ER, je importován jeden soubor ze zdrojů konfigurovaného souboru. K implementaci spuštění této dávky použijte následující kód.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Po úspěšném importu souboru ze složky SharePoint, je soubor z této složce odstraněn.

5. Zadejte ID dokladu, jako je například **V-00001**, a poté vyberte **OK**.

[![Spustit mapování modelu ER](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Na stránce **Stavy souboru pro zdroje** vyberte **aktualizovat** k obnovení stránky.

[![Stránka stavů souboru ER pro vybrané zdroje](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. V části **soubory** zkontrolujte seznam souborů. Oddíl **Zdroje protokolu formátu importu** obsahuje historii importu souboru aplikace Excel. Vzhledem k tomu, že tento soubor byl úspěšně importován, je označen jako **Odstraněn** ve složce služby SharePoint.
8. Zkontrolujte složku **Zdroj importu souborů (hlavní)** složky služby SharePoint. Soubory aplikace Excel, které byly úspěšně importovány, byly odstraněny z této složky.
9. V modulu Finance and Operations vyberte **Závazky** \> **Pravidelné úkoly** \> **Daň 1099** \> **Vyrovnávání dodavatele pro 1099**.
10. V poli **od data** a **do data** zadejte příslušné hodnoty. Pak vyberte **Ruční transakce 1099**.

    Transakce dodavatele importované ze souborů aplikace Excel na web služby SharePoint pro doklad **V-00001**, jsou uvedeny na stránce.

[![Stránka Transakce 1099 dodavatele](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Příprava souboru Excel k importu
1. Otevřete soubor aplikace Excel, který jste použili. Na řádek 3 sloupce 1 přidejte kód dodavatele, který neexistuje v aplikaci. Přidejte další falešné informace dodavatele do řádku.

[![Vzorový soubor aplikace Microsoft Excel pro import ze služby SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Nahrajte aktualizovaný soubor aplikace Excel obsahující transakce dodavatele do složky služby SharePoint **Zdroj importu souborů (hlavní)**.
3. V modulu Finance and Operations otevřete strom konfigurace ER, vyberte **model platby 1099**a rozbalte seznam součástí modelu ER.
4. Vyberte název mapování modelu k aktualizaci mapování modelu tak, aby nesprávný kód dodavatele byl považován za chybu během importu dat.
5. Vyberte možnost **Návrhář**.
6. Na kartě **Ověření** je nutné změnit akci po ověření pro pravidlo ověření, které bylo nakonfigurováno na posouzení, zda importovaný účet dodavatele v aplikaci existuje. Aktualizujte hodnotu pole **Akce po ověření** na **Zastavit provedení**, uložte změny a zavřete stránku.

[![Stránka Návrhář mapování modelu ER](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Uložte změny a zavřete návrhář ER mapování modelu.
8. Vyberte **spustit** ke spuštění modifikovaného mapování modelu ER.
9. Zadejte ID dokladu, jako je například **V-00002**, a poté vyberte **OK**.

    Všimněte si, že informační protokol obsahuje upozornění informující, že uložení v souboru složky SharePoint obsahuje nesprávný účet dodavatele a nedá se importovat.

[![Spustit mapování modelu ER](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Na stránce **Stavy souboru pro zdroje** vyberte **aktualizovat**a pak v části **soubory** zkontrolujte seznam souborů.

[![Stránka stavů souboru ER pro vybrané zdroje](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

Oddíl **Zdrojové protokoly pro formát importu** označuje, že při importu došlo k chybě a soubor je stále ve složce služby SharePoint (není zaškrtnuto políčko **Je odstran**). Pokud tento soubor opravíte ve službě SharePoint přidáním správného kódu dodavatele a následně změníte stav souboru ze **Selhání** na **Připraven** v oddílu **Protokol zdrojů pro formát importu**, můžete soubor znovu importovat.

11. Zkontrolujte složku **Zdroj importu souborů (hlavní)** složky služby SharePoint. Všimněte si, že soubor aplikace Excel, který nebyl importován, je stále v této složce.
12. V modulu Finance and Operations vyberte **Závazky** \> **Pravidelné úkoly** \> **Daň 1099** \> **Vyrovnání dodavatele pro 1099**, zadejte vhodné hodnoty do polí **Od data** a **Do data** a pak vyberte **Ruční transakce 1099**.

    Pouze transakce pro doklad V-00001 jsou k dispozici. Žádné transakce pro doklad V-00002 nejsou k dispozici, i když byla nalezena chyba poslední importované transakce v souboru aplikace Excel.

