---
title: Konfigurace importu dat z aplikace SharePoint
description: Toto téma vysvětluje postup při importu dat z aplikace Microsoft SharePoint.
author: NickSelin
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 9ac328e660c7a8a3b4a4f34a650062a0fa974771
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074759"
---
# <a name="configure-data-import-from-sharepoint"></a>Konfigurace importu dat z aplikace SharePoint

[!include[banner](../includes/banner.md)]

Při importu dat z příchozího souboru pomocí rozhraní elektronických sestav (ER) musíte konfigurovat formát ER, který podporuje import, a spustit mapování modelu typu **cíl**, který tento formát používá jako zdroj dat. Pokud chcete provést import dat, přejděte do souboru, který chcete importovat. Vstupní soubor může ručně vybrat uživatel. S novou možností ER podporovat import dat z aplikace Microsoft SharePoint lze tento proces konfigurovat jako bezobslužný. Konfigurace ER lze použít k provádění importu dat ze souborů, které jsou uloženy ve složkách Microsoft SharePoint. Toto téma vysvětluje, jak dokončit import ze služby do SharePoint. Tyto příklady používají transakcí dodavatele jako obchodní data.

## <a name="prerequisites"></a>Předpoklady
Pro dokončení příkladů v tomto tématu musíte mít následující přístup:

- Přístup k některé z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Přístup k instanci serveru Microsoft SharePoint, který je konfigurován k použití s aplikací.
- Konfigurace formátu a modelu ER pro platby 1099.

### <a name="create-required-er-configurations"></a>Vytvoření požadovaných konfigurací ER
Přehrajte si průvodce záznamem úloh **ER Import dat ze souboru aplikace Microsoft Excel**, které jsou součástí obchodního procesu **7.5.4.3 Acquire/Develop IT service/solution components (10677)**. Tito průvodci záznamem úloh vás provedou procesem navrhování a použití konfigurací ER pro interaktivní import transakcí dodavatele z externích souborů aplikace Microsoft Excel. Další informace naleznete v tématu [analýza příchozích dokumentů do formátu Excel](parse-incoming-documents-excel.md). Po dokončení průvodců záznamem úloh, bude mít následující nastavení.

#### <a name="er-configurations"></a>Konfigurace ER

- Konfigurace modelu ER, **model platby 1099**
- Konfigurace formátu ER **formát pro import transakcí dodavatelů z aplikace Excel**

![Konfigurace ER pro import dat ze služby SharePoint.](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Ukázka vstupního souboru pro import dat:

- Soubor Excel **1099import data.xlsx**, s transakcemi dodavatele, které je nutné importovat.

![Vzorový soubor aplikace Excel pro import ze služby SharePoint.](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Formát pro import transakcí dodavatele je vybrán jako výchozí mapování modelu. Proto když spustíte mapování modelu **model platby 1099**, které je typu **Do cíle**, mapování modelu spustít tento formát pro import dat z externích souborů. Následně tato data použije k aktualizaci tabulek aplikace.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>Konfigurace přístupu na web služby SharePoint pro uložení souboru
Pokud chcete uložit elektronické soubory s výkazy do umístění ve službě SharePoint, musíte nakonfigurovat přístup k instanci serveru SharePoint, kterou bude používat aktuální společnost. V tomto příkladu je společnost USMF. Pokyny naleznete v tématu [Konfigurace úložiště služby SharePoint](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Dokončete jednotlivé kroky v části [Konfigurovat úložiště služby SharePoint](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).
2. Otevřete konfigurovanou stránku SharePoint.
3. Vytvořte následující složky, do kterých lze uložit příchozí soubory elektronického vykazování:

     - Zdroj importu souborů (hlavní) (Příklad ukazuje následující snímek obrazovky)
     - Zdroj importu souborů (alternativní)

    ![Zdroj importu souborů (hlavní).](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Volitelné) Vytvořte následující složky, do kterých lze uložit příchozí soubory po importu: 

    - Složka archivu souborů - tato složka je určená pro úspěšně importované soubory.
    - Složka s upozorněním na soubory - tato složka je určena pro soubory, které byly importovány s varováním.
    - Složka chyb souborů - tato složka je určená pro neúspěšně importované soubory.

4. Přejděte na **Správa dokumentů > Správa dokumentů > Typy dokumentů**.
5. Vytvořte následující typy dokumentů, které budou použity pro přístup k složkám služby SharePoint, které jste vytvořili. Pokyny naleznete v tématu [Konfigurovat typy dokumentů](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Typ dokumentu        | Seskupit              | Místo konání      | Složka SharePoint      |
|--------------------|--------------------|---------------|------------------------|
|Hlavní SP             |Soubor                |SharePoint     |Zdroj importu souborů (hlavní)|
|Alternativní SP             |Soubor                |SharePoint     |Zdroj importu souborů (alternativní)|
|Archiv SP             |Soubor                |SharePoint     |Složka archivu souborů|
|Upozornění SP             |Soubor                |SharePoint     |Složka k upozornění na soubory|
|Chyba SP             |Soubor                |SharePoint     |Složka chyb souborů|

![Nastavení služby SharePoint – nový typ dokumentu.](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Konfigurace zdrojů ER pro formát ER
1. Klikněte na **Správa organizace** \> **Elektronická sestava** \> **Úlohy elektronických sestav**.
2. Na stránce **Zdroj elektronického výkaznictví** nakonfigurujte zdrojové soubory pro import dat pomocí konfigurovaného ER formátu.
3. Definujte název masky souboru, aby byly importovány pouze soubory s příponou XLSX. Maska názvu souboru je volitelná a používá se pouze v případě, že byla definována. Můžete definovat pouze jednu masku pro každý formát ER.
4. Pokud existuje několik souborů k importu a není důležité pořadí při importu, změňte možnost **Seřadit soubory před importem** na **Neseřazovat**.
5. Vyberte všechny složky SharePoint, které jste předtím vytvořili.

    [![Nastavení zdroje souborů ER.](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - *Zdroj* je definován individuálně pro každou společnost aplikace. Naopak *konfigurace* ER jsou sdíleny mezi společnostmi.
> - Když odstraníte nastavení zdroje ER zdroj pro formát ER, budou také odstraněny všechny připojené stavy souborů (viz níže).

## <a name="review-the-files-states-for-the-er-format"></a>Zkontrolujte stavy souborů ve formátu ER
1. Na stránce **Zdroj elektronického vykazování** vyberte **Stavy souboru pro zdroje** ke kontrole obsahu konfigurovaných zdrojů souboru pro aktuální formát ER.
2. V části **soubory** zkontrolujte seznam souborů. Tento seznam nabízí následující:

    - Zdrojové soubory, které jsou použitelné, jsou založené na masce názvu souboru (Pokud je maska souboru definovaná) a které jsou připraveny pro import dat. Pro tyto soubory je oddíl **zdroje protokolu formátu importu** prázdný.
    - Dříve importované soubory. Pro každý z těchto souborů v části **zdroje protokolu formátu importu** je možné zkontrolovat historii importu souboru.

Lze rovněž otevřít stránku **stavy souboru pro zdroje** výběrem možnosti **Správa organizace** \> **elektronické vykazování** \> **Stavy souboru pro zdroje**. V tomto případě stránka obsahuje informace o zdrojích souboru pro všechny formáty ER, pro které byly ve společnosti, do které jste aktuálně přihlášení, nakonfigurovány zdroje souborů.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Import dat ze souborů aplikace Excel, které jsou ve složce služby SharePoint
1. V rámci služby SharePoint nahrajte soubor aplikace Microsoft Excel **1099import-data.xlsx**, který obsahuje transakce dodavatele, do složky služby SharePoint **zdroj souborů importu (hlavní)**, kterou jste předtím vytvořili.

    [![Obsah SharePoint – Soubor Microsoft Excel pro import.](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Na stránce **Stavy souboru pro zdroje** vyberte **aktualizovat** k obnovení stránky. Soubor aplikace Excel, který byl nahrán do služby SharePoint, se zobrazil na této stránce se stavem **Připraven**. Jsou podporovány následující stavy:

    - **Připraveno** – přiřazené automaticky pro každý nový soubor ve složce služby SharePoint. Tento stav znamená, že je soubor připraven k importu.
    - **Import** – přiřazené automaticky sestavou ER, když soubor bude uzamčen procesem importu, aby se zabránilo jeho použití jinými postupy (pokud je jich mnoho spuštěno současně).
    - **Importované** – přiřazené automaticky podle vyúčtování ER po úspěšném dokončení importu souboru. Tento stav znamená, že importovaný soubor byl odstraněn ze zdroje konfigurovaných souborů (složka SharePoint).
    - **Neúspěšné** – přiřazené automaticky podle vyúčtování ER po dokončení importu souboru s chybami nebo výjimkami.
    - **Blokování** – přiřazené ručně uživatelem na této stránce. Tento stav znamená, že soubor nyní nebude importován. Tento stav slouží k odložení importu některých souborů.

    [![Aktualizovaná stránka stavů souboru ER pro vybrané zdroje.](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Import dat ze souborů SharePoint
1. Otevřete strom konfigurace ER, vyberte **model platby 1099** a rozbalte seznam součástí modelu ER.
2. Vyberte název mapování modelu pro otevření seznamu mapování modelu vybrané konfigurace modelu ER.

    [![Stránka konfigurace.](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Vyberte **spustit** ke spuštění mapování vybraného modelu. Vzhledem k tomu, že jste nakonfigurovali zdroje souboru pro formát ER, můžete změnit nastavení možnosti **zdroj souboru** podle potřeby. Ponecháte-li nastavení této možnosti, soubory XLSX jsou importovány z konfigurovaných zdrojů (složky SharePoint, v tomto příkladu).

    V tomto příkladu importujete jen jeden soubor. Avšak pokud existuje více souborů, jsou vybrány pro import v pořadí, ve kterém byly přidány do složky služby SharePoint. Každé spuštění formátu ER importuje jeden vybraný soubor.

    [![Import ze služby SharePoint a spuštění mapování modelu ER.](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Mapování modelu lze spustit [bezobslužně](#limitations) v dávkovém režimu. V takovém případě pokaždé, když je dávka spuštěna v tomto formátu ER, je importován jeden soubor ze zdrojů konfigurovaného souboru.

    Po úspěšném importování souboru ze složky SharePoint je soubor odstraněn z této složky a přesune se do složky pro úspěšně importované soubory nebo do složky pro importované soubory s upozorněními. V opačném případě se přesune do složky neúspěšných souborů nebo zůstává v této složce, pokud není složka pro neúspěšné soubory nastavená. 

5. Zadejte ID dokladu, jako je například **V-00001**, a poté vyberte **OK**.

    [![Spustit mapování modelu ER.](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Na stránce **Stavy souboru pro zdroje** vyberte **aktualizovat** k obnovení stránky.

    [![Stavy souboru ER pro stránku zdroje.](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. V části **soubory** zkontrolujte seznam souborů. Oddíl **Zdroje protokolu formátu importu** obsahuje historii importu souboru aplikace Excel. Vzhledem k tomu, že tento soubor byl úspěšně importován, je označen jako **Odstraněn** ve složce služby SharePoint.
8. Zkontrolujte složku **Zdroj importu souborů (hlavní)** složky služby SharePoint. Soubory aplikace Excel, které byly úspěšně importovány, byly odstraněny z této složky.
9. Vyberte **Závazky** \> **Pravidelné úlohy** \> **Daň 1099** \> **Vyrovnání dodavatele pro sestavy 1099**.
10. V poli **od data** a **do data** zadejte příslušné hodnoty. Pak vyberte **Ruční transakce 1099**.

    Transakce dodavatele importované ze souborů aplikace Excel na web služby SharePoint pro doklad **V-00001**, jsou uvedeny na stránce.

    [![Stránka Transakce 1099 dodavatele.](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Příprava souboru Excel k importu
1. Otevřete soubor aplikace Excel, který jste použili. Na řádek 3 sloupce 1 přidejte kód dodavatele, který neexistuje v aplikaci. Přidejte další falešné informace dodavatele do řádku.

    [![Vzorový soubor aplikace Microsoft Excel pro import ze služby SharePoint.](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Nahrajte aktualizovaný soubor aplikace Excel obsahující transakce dodavatele do složky služby SharePoint **Zdroj importu souborů (hlavní)**.
3. Otevřete strom konfigurace ER, vyberte **model platby 1099** a rozbalte seznam součástí modelu ER.
4. Vyberte název mapování modelu k aktualizaci mapování modelu tak, aby nesprávný kód dodavatele byl považován za chybu během importu dat.
5. Vyberte možnost **Návrhář**.
6. Na kartě **Ověření** je nutné změnit akci po ověření pro pravidlo ověření, které bylo nakonfigurováno na posouzení, zda importovaný účet dodavatele v aplikaci existuje. Aktualizujte hodnotu pole **Akce po ověření** na **Zastavit provedení**, uložte změny a zavřete stránku.

    [![Stránka Návrhář mapování modelu ER.](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Uložte změny a zavřete návrhář ER mapování modelu.
8. Vyberte **spustit** ke spuštění modifikovaného mapování modelu ER.
9. Zadejte ID dokladu, jako je například **V-00002**, a poté vyberte **OK**.

    Informační protokol obsahuje upozornění, že uložení v souboru složky SharePoint obsahuje nesprávný účet dodavatele a nedá se importovat.

    [![Dokončené spuštění mapování modelu ER.](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Na stránce **Stavy souboru pro zdroje** vyberte **aktualizovat** a pak v části **soubory** zkontrolujte seznam souborů.

    [![Stránka stavů souboru ER pro vybrané zdroje.](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   Oddíl **Zdrojové protokoly pro formát importu** označuje, že při procesu importu došlo k chybě a soubor je stále ve složce Chybné soubory SharePoint (není zaškrtnuto políčko **Je odstraněn**). Pokud tento soubor opravíte ve službě SharePoint přidáním správného kódu dodavatele a následně ho přesunete do složky Zdroj importu souborů (hlavní) SharePoint, můžete soubor znovu importovat.

11. Vyberte **Závazky** \> **Pravidelné úkoly** \> **Daň 1099** \> **Vyrovnání dodavatele pro 1099**, zadejte vhodné hodnoty do polí **Od data** a **Do data** a pak vyberte **Ruční transakce 1099**.

    Pouze transakce pro doklad V-00001 jsou k dispozici. Žádné transakce pro doklad V-00002 nejsou k dispozici, i když byla nalezena chyba poslední importované transakce v souboru aplikace Excel.

## <a name=""></a><a name="limitations">Omezení</a>

Ve verzích Dynamics 365 Finance před verzí 10.0.25 uživatelské rozhraní architektury ER nenabízí schopnost iniciovat novou dávkovou úlohu, která provede mapování modelu v bezobslužném režimu pro import dat. Musíte sestavit novou logiku, aby bylo možné volat konfigurované mapování modelu ER z uživatelského rozhraní aplikace a importovat data z příchozích souborů. K vývoji této logiky je nutná určitá inženýrská práce. 

Další informace o příslušném rozhraní API ER najdete v části [Kód ke spuštění mapování formátu pro import dat](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) v tématu [Změny rozhraní API architektury ER pro aktualizaci aplikace 7.3](er-apis-app73.md). Prostudujte kód ve třídě `BankImport_RU` modelu `Application Suite` a podívejte se, jak lze implementovat vaši vlastní logiku. Třída `BankImport_RU` rozšiřuje třídu `RunBaseBatch`. Zejména prostudujte metodu `runER()`, kde je vytvořen objekt `ERIModelMappingDestinationRun` jako provádění modul mapování modelu ER.

Ve verzi Finance 10.0.25 a pozdější uživatelské rozhraní architektury ER nenabízí schopnost iniciovat novou dávkovou úlohu, která provede mapování modelu v bezobslužném režimu pro import dat. Další informace o tomto procesu viz [Import dat v dávkovém režimu z ručně vybraných souborů](er-configure-data-import-batch.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Změny rozhraní API architektury ER pro aktualizaci aplikace 7.3](er-apis-app73.md)

[Změny rozhraní API architektury ER pro aktualizaci aplikace 10.0.23](er-apis-app10-0-23.md)

[Změny rozhraní API architektury ER pro aktualizaci aplikace 10.0.25](er-apis-app10-0-25.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
