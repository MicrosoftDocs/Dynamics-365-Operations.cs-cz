---
title: Podpora parametrizovaných volání zdrojů dat ER typu vypočítaného pole
description: Toto téma obsahuje informace o způsobu použití typu vypočítaného pole pro zdroje dat ER.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fb09e1ccd4b2be08e43784330adf4092ca25f5a6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349153"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Podpora parametrizovaných volání zdrojů dat ER typu vypočítaného pole

[!include [banner](../includes/banner.md)]

V tomto tématu je vysvětleno, jak můžete vytvořit zdroj dat Elektronického vykazování (ER) pomocí typu **Vypočítaného pole**. Tento zdroj dat může obsahovat výraz ER, který po spuštění může být řízen hodnotami argumentů parametrů, které jsou nakonfigurovány ve vazbě, která volá tento zdroj dat. Konfigurací parametrizovaných volání takového zdroje dat můžete znovu použít jeden zdroj dat v mnoha vazbách, čímž snížíte celkový počet datových zdrojů, které musí být nakonfigurovány v mapování modelu ER nebo ve formátech ER. Také zjednodušuje konfigurovanou komponentu ER, která snižuje náklady na údržbu a náklady na použití ostatních odběratelů.

## <a name="prerequisites"></a>Předpoklady
Pro dokončení příkladů v tomto tématu musíte mít následující přístup:

- Přístup k jedné z těchto rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Přístup k službám Regulatory Configuration Services (RCS), které byly zřízeny pro stejného klienta jako Finance and Operations, pro jednu z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

Je také nutné stáhnout a lokálně uložit následující soubory.

| **Obsah**                           | **Název souboru**                                        |
|---------------------------------------|------------------------------------------------------|
| Vzorová konfigurace datového modelu elektronického výkaznictví    | [Model pro informace o volání s parametry calls.version.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| Vzorová konfigurace metadat elektronického výkaznictví      | [Metadata pro informace o volání s parametry calls.version.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| Vzorová konfigurace mapování elektronického výkaznictví | [Mapování pro informace o volání s parametry calls.version.1.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| Vzorová konfigurace formátu elektronického výkaznictví        | [Formát pro informace o volání s parametry calls.version.1.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a>Přihlaste se k instanci RCS.
V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Nejprve musíte v RCS dokončit krok v proceduře [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Na výchozím řídicím panelu vyberte **Elektronické vykazování**.
2. Vyberte **Konfigurace vykazování**.
3. Import stažených konfigurací do RCS v následujícím pořadí: datový model, metadata, mapování modelu, formát. Pro každou konfiguraci ER proveďte následující kroky:

    1. Vyberte **Exchange**.
    2. Vyberte **Načíst ze souboru XML**.
    3. Zvolte **Procházet** a pak vyberte požadovanou konfiguraci elektronického výkaznictví ve formátu XML.
    4. Vyberte **OK**.

## <a name="review-the-provided-er-solution"></a>Zkontrolovat poskytnuté řešení ER

### <a name="review-model-mapping"></a>Kontrola mapování modelu

1. Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.
2. Vyberte **Mapování pro informace o voláních s parametry**.
3. Vyberte možnost **Návrhář**.
4. Vyberte možnost **Návrhář**.  
   
    Toto mapování modelu ER je navrženo k následujícím akcím:

    - Načtení seznamu daňových kódů (**Daňový** zdroj dat) nacházející se v tabulce **TaxTable**.
    - Načtení seznamu daňových transakcí (**Trans** zdroj dat) nacházející se v tabulce **TaxTrans**:
    
        - Seskupit seznam načtených transakcí (**Gr** zdroj dat) podle kódu daně
        - Vypočítat pro seskupené transakce po agregovaných hodnotách podle kódu daně:

            - Součet hodnot základu daně.
            - Součet hodnot daně.
            - Minimální hodnota uplatněné sazby daně.

    Mapování modelu v této konfiguraci implementuje základní datový model pro všechny formáty ER vytvořené pro tento model a prováděné ve Finance and Operations. V důsledku toho je obsah zdrojů dat **Daň** a **Gr** vystaven pro formáty ER, jako jsou například abstraktní zdroje dat.

    ![Stránka Návrhář mapování modelu zobrazující zdroje dat Daň a Gr.](media/er-calculated-field-type-01.png)

5.  Zavřete stránku **Návrhář mapování modelu**.
6.  Zavřete stránku **Mapování modelu**.

### <a name="review-format"></a>Zkontrolovat formát

1. Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.
2. Vyberte **Formát pro informace o voláních s parametry**.
3. Vyberte možnost **Návrhář**. Tento formát ER je navržen k následujícím akcím:

    - Generujte daňový výkaz ve formátu XML.
    - V daňovém výkazu prezentujte následující úrovně zdanění: normální, snížené a žádné.
    - Prezentujte více podrobností na každé úrovni zdanění, které mají různý počet podrobností na každé úrovni.

    ![Stránka návrháře formátu.](media/er-calculated-field-type-02.png)

4. Vyberte **Mapování**.
5. Rozbaltepoložky **Model**, **Data** a **Souhrnné** . 

    Vpočítané pole **Model.Data.Summary.Leve** obsahuje výraz vracející kód úrovně zdanění (**Pravidelný**, **Snížený**, **Žádný** nebo **Jiný**) jako textovou hodnotu pro libovolný kód daně, který lze načíst ze zdroje dat **Model.Data.Summary** za běhu.

    ![Stránka návrháře formátu s podrobnostmi o modelu datového modelu pro zjištění parametrizovaných hovorů.](media/er-calculated-field-type-03.png)

6. Rozbalte položku **Model**.**Data2**.
7. Rozbalte položku **Model**.**Data2.Summary2**.
   
    Datový zdroj **Model**.**Data2.Summary2** je konfigurováno pro seskupení podrobností transakcí datového zdroje **Model.Data.Summary** podle úrovně zdanění (vráceno vypočítaným polem **Model.Data.Summary.Level**) a výpočet agregací.

    ![Stránka návrháře formátu s podrobnostmi o zdroji dat Model.Data2.Summary2.](media/er-calculated-field-type-04.png)

8. Zkontrolujte vypočítaná pole **Model**.**Data2.Level1**, **Model**.**Data2.Level2** a **Model**.**Data2.Level3.** Tato vypočítaná pole slouží k filtrování seznamu záznamů **Model**.**Data2.Summary2** a vrátí pouze záznamy, které reprezentují určitou úroveň zdanění.
9. Zavřete stránku **Návrhář formátu**.

## <a name="create-a-derived-format"></a>Vytvoření odvozeného formátu
Poskytnutý formát lze zlepšit přidáním jednoho vypočítaného pole pro filtrování požadované úrovně zdanění namísto použití existujících tří polí: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** a **Model**.**Data2.Level3**. Požadovanou úroveň zdanění lze zadat v místě, kde bude voláno nové vypočtené pole.

1. Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.
2. Vyberte **Formát pro informace o voláních s parametry**.
3. Vyberte **Vytvořit konfiguraci**.
4. Vyberte možnost **Odvozeno od názvu: Formát pro informace o parametrizovaných volání, Microsoft**.
5. Do pole **Název** zadejte **Formát pro učení parametrizovaných volání (vlastní)**.
6. Vyberte **Vytvořit konfiguraci**.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Konfigurace parametrizovaného vypočítaného pole, které vrací seznam záznamů

### <a name="start-adding-a-new-calculated-field"></a>Začít přidávat nové počítané pole

1. Vyberte možnost **Návrhář**.
2. Vyberte **Rozbalit/sbalit** pro rozbalení všechn položek formátu.
3. Vyberte **Mapování**.
4. Rozbalte položku **Model**.
5. Vyberte položku **Model.Data2**.
6. Vyberte **přidat**.
7. Vyberte **Funkce\\vypočítané pole**.
8. Do pole **Název** zadejte **Úrovně**.
9. Vyberte možnost **Upravit vzorec**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definovat parametr pro přidání vypočítaného pole

1. Vyberte **Parametry**.
2. Zvolte **Nové**.
3. Do pole **Název** zadejte **Úroveň zdanění**.
4. V poli **Typ** vyberte **Řetězec**.

    K zadání typu argumentu parametru lze použít pouze primitivní datové typy. Proto nelze pro tento účel použít typy **Seznam záznamů**, **Záznam** a **Výčet**.

    Maximální počet parametrů, které lze zadat pro jedno vypočtené pole, je 8.

    ![Seznam zdroje dat parametrů.](media/er-calculated-field-type-05.png)

5. Vyberte **OK**.

Přidáte-li tento parametr, zadáte podmínku, která musí být na místě, aby bylo možné toto vypočtené pole volat. Při volání tohoto vypočítaného pole je nutné zadat argument parametru **Úroveň zdanění** jako hodnotu s formátem **Řetězec**.

   Ujistěte se, že definujete parametry pouze pro vypočítaná pole, která jsou uložena v kontejneru (**Seznam záznamů**, **Záznam** nebo **Kontejner**).

   Konfigurovaný parametr je k dispozici v seznamu zdrojů dat pro toto vypočtené pole. Chcete-li přidat parametr do konfigurovaného výrazu, vyberte možnost **Přidat zdroj dat**.

   ![Pole zdroje dat.](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definovat výraz pro přidání vypočítaného pole

1. Do pole **Vzorec** zdejte: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. V seznamu zdrojů dat vyberte parametr **Úroveň zdanění**.
3. Vyberte **Přidat zdroj dat**.
4. V poli **Vzorec** dokončete výraz jako:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**

5. Zvolte možnost **Uložit**.

    ![Informace o datových zdrojových polích.](media/er-calculated-field-type-07.png)

6. Zavřete stránku **Návrhář vzorce**.

### <a name="finish-adding-a-new-calculated-field"></a>Dokončete přidávávání nových počítaných polí

- Vyberte **OK**.

Na stránce **Návrhář formátu** je v konfigurovaných vypočítaných polích **Úrovně** vyžadován argument **Řetězec**.

![Rozbalený seznam úrovní vypočítaných polí.](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements&quot;></a>Použít nakonfigurované počítané pole pro prvky formátu vazby

1. Výběrem **Model.Data2.Levels** vyberte nakonfigurované počítané pole.
2. Vyberte prvek formátu **Statement.Taxation.Regular**.
3. Vyberte možnost **vazba**.
4. Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level1** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.

    Použitá vazba byla sestavena jako volání parametrizovaného počítaného pole. Standardně se název prvku vázaného formátu používá jako argument pro parametrizované počítané pole za následujících podmínek:

      - Vypočítané pole je nakonfigurováno pro použití jediného parametru.
      - Datový typ tohoto parametru je definován jako **Řetězec**.

    Je-li název prvku vázaného formátu prázdný, bude název zdroje dat tohoto prvku použit v použité vazbě.

5. Vyberte prvek formátu **Statement.Taxation.Reduced**.
6. Vyberte možnost **vazba**.
7. Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level2** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.
8. Vyberte prvek formátu **Statement.Taxation.None**.
9. Vyberte možnost **vazba**.
10. Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level3** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.

   Když zadáte argument parametrizovaného pole pro prvek XML představující úroveň zdanění (například **Model.Data2.Levels(&quot;Reduced")** jako textovou hodnotu), nemusíte provádět stejnou akci pro vnořené atributy XML – jejich vazby automaticky zdědí hodnotu argumentu definovaného na nadřazené úrovni (**Model.Data2.Levels.aggregated.Base**, nikoli **Model.Data2.Levels("Reduced").aggregated.Base**).

Opakující se volání jakéhokoliv parametrizovaného pole nejsou podporována.

Můžete vybrat možnost **Upravit vzorec** a změnit argument vyrovnáno podle výchozího pole ve vybrané vazbě. Pokud tento argument chybí, může způsobit chyby za běhu – uživatelé jsou informováni o takové situaci, když je aktuální formát ověřen.

![Upozornění na potvrzení ověření.](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record&quot;></a>Konfigurace parametrizovaného vypočítaného pole pro návrat záznamu
Pokud parametrizované pole vrací záznam, je nutné podporovat vazby jednotlivých polí tohoto záznamu k formátování prvků. V takovém případě nebude existovat žádná nadřazená vazba, která obsahuje hodnotu argumentu pro volání parametrizovaného počítaného pole - tato hodnota musí být definována ve vazbě pole jednoho záznamu.

### <a name=&quot;start-adding-a-new-calculated-field&quot;></a>Začít přidávat nové počítané pole

1. Vyberte položku **Model.Data2**.
2. Vyberte **přidat**.
3. Vyberte **Funkce\\vypočítané pole**.
4. Do pole **Název** zadejte **LevelRecord**.
5. Vyberte možnost **Upravit vzorec**.

### <a name=&quot;define-a-parameter-for-adding-a-calculated-field&quot;></a>Definovat parametr pro přidání vypočítaného pole

1. Vyberte **Parametry**.
2. Zvolte **Nové**.
3. Do pole **Název** zadejte **Úroveň zdanění**.
4. V poli **Typ** vyberte **Řetězec**.
5. Vyberte **OK**.

### <a name=&quot;define-an-expression-for-adding-a-calculated-field&quot;></a>Definovat výraz pro přidání vypočítaného pole

1. V poli **Vzorec** zadejte následující:  
    
    **FIRSTORNULL(\@.Levels(**

2. Vyberte parametr **Úroveň zdanění**.
3. Vyberte **Přidat zdroj dat**.
4. V poli **Vzorec** přidejte **&quot;Úroveň zdanění"))** do stavu, který jste zadali v kroku 1 a dokončete výraz na:  
    
    **FIRSTORNULL(\@.Levels('Taxation Level'))**

5. Zvolte **Uložit**.
6. Zavřete stránku **Návrhář vzorce**.

### <a name="finish-adding-a-new-calculated-field"></a>Dokončete přidávávání nových počítaných polí

-   Vyberte **OK**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Použít nakonfigurované počítané pole pro svázání prvků formátu

1. Rozbalením **Model.Data2.LevelRecord** vyberte nakonfigurované počítané pole.
2. Rozbalte kontejner **Model.Data2.LevelRecord.aggregated** nakonfigurovaného počítaného pole.
3. Vyberte pole **Model.Data2.LevelRecord.aggregated.Base**.
4. Vyberte prvek formátu **Statement.Taxation.None**.
5. Vyberte možnost **Zrušit vazbu**.
6. Vyberte prvek formátu **Statement.Taxation.None.Base**.
7. Vyberte možnost **vazba**.
8. Vyberte možnost **Upravit vzorec**.
9. Změňte výraz na **Model.Data2.LevelRecord("None").aggregated.Base**.

![Aktualizovaný výraz.](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Odebrat vypočtená pole, která nejsou použita

1. Vyberte **Model.Data2.Level1**.
2. Zvolte **Odstranit**.
3. Vyberte **Model.Data2.Level2**.
4. Zvolte **Odstranit**.
5. Vyberte **Model.Data2.Level3**.
6. Zvolte **Odstranit**.
7. Zvolte **Uložit**.

  > [!NOTE]
  > Znovu jste použili stejný model počítaného pole **Model.Data2.Levels** několikrát ve formátu vazeb. Je mnohem jednodušší použít a udržovat jedno vypočítané pole namísto více podobných polí.

8. Zavřete stránku **Návrhář formátu**.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Dokončete upravenou verzi odvozeného formátu

1. Na pevné záložce **Verze** vyberte možnost **Stav změny**.
2. Zvolte **Dokončit**.

## <a name="export-completed-version-of-a-derived-format"></a>Exportujte dokončenou verzi odvozeného formátu

1. Vyberte **Formát pro učení parametrizovaných volání (vlastní)** ve stromu konfigurací.
2. Na pevné záložce **Verze** vyberte dokončenou verzi 1.1.1.
3. Vyberte **Exchange**.
4. Vyberte **Exportovat jako soubor XML**.
5. Uloží staženou konfiguraci místně ve formátu XML.

## <a name="test-er-formats"></a>Testovat formáty ER 
Chcete-li se ujistit, že nakonfigurovaná počítaná pole fungují správně, můžete spustit počáteční a vylepšené formáty ER.

### <a name="import-er-configurations"></a>Import konfigurací ER
Revidované konfigurace lze importovat z RCS pomocí úložiště ER typu **RCS**. Pokud jste již provedli kroky v tématu, [Import konfigurací elektronického výkaznictví (ER) z Regulatory Configuration Services (RCS)](rcs-download-configurations.md), použijte nakonfigurované úložiště ER pro import konfigurací popsaných dříve v tomto tématu do vašeho prostředí. V opačném případě postupujte takto:

1. Vyberte společnost **DEMF** a na výchozím řídicím panelu vyberte možnost **Elektronické vykazování**.
2. Vyberte **Konfigurace vykazování**.
3. Import stažených konfigurací z Microsoft Download Center v následujícím pořadí: datový model, mapování modelu, formát. Pro každou konfiguraci ER proveďte následující kroky:

    1. Vyberte **Exchange**.
    2. Vyberte **Načíst ze souboru XML**.
    3. Zvolte **Procházet** a vyberte požadovanou konfiguraci elektronického výkaznictví ve formátu XML.
    4. Vyberte **OK**.

4. Importujte exportované z RCS dokončené verze 1.1.1 **Formát pro učení parametrizovaných volání (vlastní)**:

    1. Vyberte **Exchange**.
    2. Vyberte **Načíst ze souboru XML**.
    3. Vyberte **Procházet** a vyberte místně uložený soubor **Formát pro učení parametrizovaných volání (vlastní)** ve formátu XML.
    4. Vyberte **OK**.

### <a name="run-er-formats"></a>Spustit formáty ER

1. Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.
2. Vyberte **Formát pro informace o voláních s parametry**.
3. Vyberte **Spustit** na horním pásu.
4. Uložte místně generovaný výstup.
5. Vyberte položku **Formát pro učení parametrizovaných volání (vlastní)**.
6. Vyberte **Spustit** na horním pásu.
7. Uložte generovaný výstup místně. 
8. Porovnejte obsah generovaných výstupů.

## <a name="additional-resources"></a>Další prostředky

- [Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)
- [Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]