---
title: Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu
description: V tomto tématu je vysvětleno, jak lze konfigurovat formáty elektronického vykazování (ER) pro použití parametrů zadaných pro právnickou osobu.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9253191f9cd10e0b3c87d61991598f9b791c35d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570727"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

V mnoha formátech elektronického výkaznictví (ER), které budete navrhovat, je nutné filtrovat data pomocí sady hodnot, které jsou specifické pro jednotlivé právnické osoby vaší instance (například sada kódů daní k filtrování daňových transakcí). V současné době, když je filtrování tohoto typu konfigurováno ve formátu ER, jsou hodnoty, které jsou závislé na právnické osobě (například kódy daně), použity ve výrazech formátu ER pro určení pravidel filtrování dat. Proto je formát ER vytvořen tak, aby byl specifický pro právnickou osobu a aby generoval požadované sestavy, musíte vytvořit odvozené kopie původního formátu ER pro každou právnickou osobu, kde je nutné spustit formát ER. Každý odvozený formát ER je nutné upravit tak, aby do něj bylo možné převést specifické hodnoty právnické osoby, a to podle toho, zda byla aktualizována původní (základní) verze, exportována z testovacího prostředí a importována do provozního prostředí v okamžiku, kdy musí být nasazena k použití v produkci atd. Proto je údržba tohoto typu konfigurovaného řešení ER poměrně složitá a časově náročná z několika důvodů:

-   Čím více je právnických osob, tím více konfigurací ER je nutné spravovat.
-   Údržba konfigurací ER vyžaduje, aby měli uživatelé společnosti znalost elektronického výkaznictví.

Funkce pro specifické parametry aplikace ER umožňují uživatelům konfigurovat filtrování dat ve formátu ER tak, aby bylo založeno na sadě abstraktních pravidel. Tuto sadu pravidel lze nakonfigurovat tak, aby používala zdroje dat, které jsou k dispozici ve formátu ER. Obchodní uživatelé pak mohou specifikovat skutečná pravidla nad rámec ER pomocí uživatelského rozhraní (UI), které je generováno automaticky na základě nastavení odpovídajícího formátu ER a aktuálních dat právnické osoby, k nimž budou mít přístup zdroje dat formátu ER. Sadu pravidel specifikovanou pro formát ER lze exportovat z aktuální právnické osoby instance Dynamics 365 Finance (Finance). Poté ji lze importovat do jiné právnické osoby se stejnou nebo jinou instancí aplikace Finance jako sadu pravidel pro stejný formát ER.

## <a name="prerequisites"></a>Předpoklady

Pokud chcete dokončit příklady v tomto tématu, musíte mít přístup k instanci služeb Regulatory Configuration Services (RCS), který byl zřízen pro stejného klienta jako Finance and Operations, pro jednu z následujících rolí:

- Návrhář elektronického výkaznictví
- Funkční konzultant elektronického výkaznictví
- Správce systému

Doporučujeme dokončit kroky v tématu [Podpora parametrizovaných volání zdrojů dat ER typu VYPOčíTANé POLE](er-calculated-field-type.md). Pokud jste již tyto kroky splnili, můžete vynechat kroky v části **Import konfigurací ER do RCS**, který následuje.

## <a name="import-er-configurations-into-rcs"></a>Import konfigurací ER do RSC

Ze [služby Stažení softwaru](https://go.microsoft.com/fwlink/?linkid=851448) si můžete stáhnout soubor **Podpora parametrizovaných volání zdrojů dat ER typu VYPOčíTANéHO POLE**. Tento soubor zip obsahuje následující konfigurace ER, které je nutné extrahovat a uložit místně.

| **Popis obsahu**                        | **Název souboru**                                        |
|------------------------------------------------|------------------------------------------------------|
| Ukázkový soubor konfigurace **Model dat elektronického výkaznictví**    | Model pro informace o volání s parametry calls.version.1.xml     |
| Ukázkový soubor konfigurace **Metadata ER**      | Metadata pro informace o volání s parametry calls.version.1.xml  |
| Ukázkový soubor konfigurace **Mapování modelu ER** | Mapování pro informace o volání s parametry calls.version.1.1.xml |
| Ukázková konfigurace **Formát ER**             | Formát pro informace o volání s parametry calls.version.1.1.xml  |

Dále se přihlaste k instanci RCS.

V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. K provedení kroků v tomto postupu musíte nejprve dokončit postup [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md) v RCS.

1.  Na výchozím řídicím panelu vyberte **Elektronické vykazování**.
2.  Vyberte **Konfigurace vykazování**.
3.  Importujte konfigurace ER, které jste předtím stáhli do RCS, v následujícím pořadí: datový model, metadata, mapování modelu a formát. Pro každou konfiguraci ER postupujte takto:

    1.  Vyberte **Exchange**.
    2.  Vyberte **Načíst ze souboru XML**.
    3.  Zvolte **Procházet** a vyberte soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.
    4.  Vyberte **OK**.

## <a name="review-the-er-solution-that-is-provided"></a>Kontrola poskytnutého řešení ER

1.  Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.
2.  Vyberte položku **Formát pro učení parametrizovaných volání**.
3.  Vyberte možnost **Návrhář**.
4.  Vyberte **Rozbalit/sbalit**.

    Formát ER **Formát pro učení parametrizovaných volání** je navržen tak, aby vygeneroval daňový výkaz ve formátu XML, který představuje několik úrovní zdanění (pravidelná, redukovaná a žádná). Každá úroveň má různý počet podrobností.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Na kartě **Mapování** rozbalte položky **Model**, **Data** a **Souhrn**.

    Zdroj dat **Model.Data.Summary** vrátí seznam daňových transakcí. Tyto transakce jsou sumarizovány v seznamu podle kódu DPH. Pro tento zdroj dat bylo nakonfigurováno vypočítané pole **Model.Data.Summary.Level**, které vrací kód úrovně zdanění jednotlivých souhrnných záznamů. Pro jakýkoli kód zdanění, který lze načíst ze zdroje dat **Model.Data.Summary** v době běhu, vrátí vypočtené pole kód úrovně zdanění (**Běžný**, **Redukovaný**, **Žádný** nebo **Ostatní**) jako textovou hodnotu. Vypočtené pole **Model.Data.Summary.Level** se použije k filtrování záznamů zdroje dat **Model.Data.Summary** a zadání filtrovaných dat do každého prvku XML, který představuje úroveň zdanění pomocí polí **Model.Data2.Level1**, **Model.Data2.Level2** a **Model.Data2.Level3**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Vypočítané pole **Model.Data.Summary.Level** je nakonfigurováno tak, aby obsahovalo výraz ER. Všimněte si, že do této konfigurace jsou zakódovány kódy daní (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** a **InVAT0**). Tento formát ER je závislý na právnické osobě, kde byly tyto kódy daně nakonfigurovány.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Chcete-li podporovat jinou sadu kódů daní pro každou právnickou osobu, je nutné provést následující kroky:

    - Vytvoření odvozené verze formátu ER pro každou právnickou osobu.
    - Aktualizujte kódy DPH ve vypočteném poli **Model.Data.Summary.Level** na základě nastavení právnické osoby.

6.  Zavřete stránku **Návrhář formátu**.

## <a name="create-a-derived-format"></a>Vytvoření odvozeného formátu

Dále použijete funkci parametrů specifickou podle aplikace ER na podporu různých sad kódů daní pro každou právnickou osobu v jednoduchém formátu ER.

1.  Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.
2.  Vyberte položku **Formát pro učení parametrizovaných volání**.
3.  Vyberte **Vytvořit konfiguraci**.
4.  Vyberte možnost **Odvozeno od názvu: Formát pro informace o parametrizovaných volání, Microsoft**.
5.  Do pole **Název** zadejte **Formát pro učení vyhledání dat LE**.
6.  Vyberte **Vytvořit konfiguraci**.

## <a name="configure-a-derived-format"></a>Konfigurace odvozeného formátu

### <a name="add-a-format-enumeration"></a>Přidání výčtu formátu

Dále přidáte nový výčet formátu ER. Hodnoty tohoto formátu budou prezentovány obchodním uživatelům, kteří budou používat sady kódů daní, které jsou závislé na právnické osobě pro různé úrovně zdanění, které jsou použity ve formátu ER.

1.  Vyberte možnost **Návrhář**.
2.  Vyberte **Vyčíslení formátu**.
3.  Vyberte **přidat**.
4.  Do pole **Název** zadejte **Seznam úrovní zdanění**.
5.  Zvolte **Uložit**.
6.  Na kartě **Hodnoty vyčíslení formátu** vyberte možnost **Přidat**.
7.  Do pole **Název** zadejte **Běžné zdanění**.
8.  Znovu vyberte **Přidat**.
9.  Do pole **Název** zadejte **Redukované zdanění**.
10. Znovu vyberte **Přidat**.
11. Do pole **Název** zadejte **Žádné zdanění**.
12. Znovu vyberte **Přidat**.
13. Do pole **Název** zadejte **Jiné**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Vzhledem k tomu, že obchodní uživatelé mohou používat různé sady kódů daní závislé na právnické osobě, doporučujeme překládat hodnoty tohoto výčtu do jazyků konfigurovaných jako preferované jazyky pro tyto uživatele v modulu finance.

14. Vyberte záznam **žádné zdanění**.
15. Klikněte do pole **Popisek**.
16. Vyberte **Přeložit**.
17. V podokně **Překlad textu** do pole **ID popisku** zadejte **LBL_LEVELENUM_NO**.
18. Do pole **Text ve výchozím jazyce** zadejte **žádné zdanění**.
19. V poli **Jazyk** vyberte **DE**.
20. Do pole **přeložený text** napište **keine Besteuerung**.
21. Vyberte **Přeložit**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Zvolte **Uložit**.
23. Zavřete stránku **Vyčíslení formátu**.

### <a name="add-a-new-lookup-data-source"></a>Přidání nového zdroje dat vyhledávání

Dále přidáte nový zdroj dat, který určuje, jakým způsobem budou obchodní uživatelé určovat pravidla závislá na právnické osobě, aby byla pro jednotlivé souhrnné záznamy transakcí rozpoznána správná úroveň zdanění.

1.  Na kartě **Mapování** vyberte **Přidat**.
2.  Vyberte **Vyčíslení formátu\Lookup**.

    Právě jste zjistili, že každé pravidlo, které obchodní uživatelé zadá za účelem uznání úrovně zdanění, vrátí hodnotu výčtu formátu ER. Všimněte si, že k typu zdroje dat **Vyhledávání** lze přejít v části **Datový model** a z bloků **Dynamics 365 for Operations** navíc k bloku **Vyčíslení formátu**. Proto výčty datových modelů ER a výčty aplikací lze použít k určení typu hodnot, které jsou vraceny pro zdroje dat tohoto typu.
    
3.  Do pole **Název** zadejte **Selektor**.
4.  Do pole **Vyčíslení formátu** zadejte **Seznam úrovní zdanění**.

    Právě jste zadali, že pro každé pravidlo, které je zadáno v tomto zdroji dat, musí obchodní uživatel vybrat jednu z hodnot **seznamu výčtů formátu daňové úrovně** jako vrácenou hodnotu.
    
5.  Vyberte **upravit vyhledávání**.
6.  Vyberte **Sloupce**.
7.  Rozbalte položku **Model**.
8.  Rozbalte položku **Data**.
9.  Rozbalte položku **Daň**.
10. Vyberte položku **Model.Data.Tax.Code**.
11. Klepněte na tlačítko **přidat** (šipka vpravo).

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Právě jste zadali, že pro každé pravidlo, které je zadáno v tomto zdroji dat pro rozpoznání úrovně zdanění, musí obchodní uživatel vybrat jeden z daňových kódů jako podmínku. Seznam kódů daní, které může obchodní uživatel vybrat, bude vrácen zdrojem dat **Model.Data.Tax**. Vzhledem k tomu, že tento zdroj dat obsahuje pole **Název**, zobrazí se název kódu daně pro každou hodnotu kódu daně ve vyhledávání, které je prezentováno obchodnímu uživateli.
    
12. Vyberte **OK**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Obchodní uživatelé mohou přidat více pravidel jako záznamy tohoto datového zdroje. Každý záznam bude očíslován kódem řádku. Pravidla budou vyhodnocována v pořadí podle rostoucího čísla řádku.

    Protože jste vybrali pole **kód daně** jako podmínku pro pravidla v tomto vyhledávacím zdroji dat a protože **kód daně** je nastaven jako pole datového typu **řetězec**, bude každé pravidlo vyhodnoceno za běhu porovnáním kódu daně, který je předán zdroji dat s kódem daně, který je definován v tomto záznamu zdroje dat.

    Při nalezení pravidla, které splňuje konfigurovanou podmínku, vrátí tento zdroj dat vyhledávací hodnotu pravidla, které je definováno v poli **výsledek vyhledávání**. Pokud není nalezeno žádné pravidlo, je vyvolána výjimka pro upozornění uživatele, že aktuální zdroj dat nemůže vrátit správnou hodnotu.

13. Zvolte **Uložit**.
14. Zavřete stránku **Návrhář vyhledávání**.
15. Vyberte **OK**.

    Všimněte si, že jste přidali nový zdroj dat, který vrátí úroveň zdanění jako hodnotu **seznamu úrovní zdanění** pro jakýkoliv daňový kód, který je předán zdroji dat, jako argument parametru **kód** datového typu **řetězec**.
    
    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Všimněte si, že vyhodnocení konfigurovaných pravidel závisí na datovém typu polí, která byla vybrána pro definování podmínek těchto pravidel. Pokud vyberete pole, které je konfigurováno jako pole datového typu **Číselný** nebo **Datum**, kritéria se budou lišit od kritérií, která byla popsána dříve pro datový typ **řetězec**. U **číselného** a **datového** pole musí být pravidlo specifikováno jako rozsah hodnot. Pokud je hodnota předaná zdroji dat v nakonfigurovaném rozsahu, bude podmínka pravidla považována za splněnou.
    
    Následující obrázek znázorňuje příklad tohoto typu nastavení. Kromě pole **Model.Data.Tax.Code** datového typu **ŘEtězec** je použito pole **Model.Tax.Summary.Base** datového typu **Real** k určení podmínek pro zdroj dat vyhledávání.
    
    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Protože jsou pro tento zdroj dat vyhledávání vybraná pole **Model.Data.Tax.Code** a **Model.Tax.Summary.Base**, každé pravidlo tohoto zdroje dat bude konfigurováno následovně:
    
    -   V seznamu, který je zobrazen, musí být jako vrácená hodnota vybrané vyčíslení formátu **Seznam úrovní zdanění**.
    -   Kód daně musí být zadán jako podmínka tohoto pravidla. Jsou použitelné pouze kódy daní, které jsou poskytnuty zdrojem dat **Model.Data.Tax**.
    -   Minimální a maximální hodnoty částky základu daně musí být zadány jako podmínky tohoto pravidla.

    Zde je, jak bude každé pravidlo tohoto zdroje dat vyhodnoceno za běhu:
    -   Rovná se kód datového typu **řetězec**, který byl předán do tohoto zdroje dat, shodný s kódem daně pravidla?
    -   Spadá hodnota **skutečného** datového typu, který byl předán do tohoto zdroje dat, do rozmezí mezi specifickou minimální a maximální hodnotou?

    Pravidlo bude považováno za použitelné, pokud budou splněny obě podmínky.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Převést popisek pro vyhledávací zdroj dat, který byl přidán

Vzhledem k tomu, že obchodní uživatelé mohou používat různé sady kódů daní závislé na právnické osobě, doporučujeme překládat popisek jakéhokoli zdroje dat vyhledávání, který přidáte, aby byl prezentován v preferovaném jazyce každého uživatele na odpovídající stránce.

1.  Vyberte zdroj dat **Model.Data.Selector**.
2.  Vyberte možnost **Upravit**.
3.  Klikněte do pole **Popisek**.
4.  Vyberte **Přeložit**.
5.  V podokně **Překlad textu** do pole **ID popisku** zadejte **LBL_SELECTOR_DS**.
6.  Do pole **Text ve výchozím jazyce** zadejte volbu **Vybrat úroveň daně podle kódu daně**.
7.  V poli **Jazyk** vyberte **DE**.
8.  Do pole **přeložený text** zadejte **Steuerebene für Steuerkennzeichen auswählen**.
9.  Vyberte **Přeložit**.
10. Vyberte **OK**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Přidání nového pole ke spotřebování nakonfigurovaného vyhledávání

1.  Rozbalte položku **Model.Data**.
2.  Vyberte položku **Model.Data.Summary**.
3.  Vyberte **přidat**.
4.  Vyberte **Funkce/vypočítané pole**.
5.  Do pole **Název** zadejte **LevelByLookup**.
6.  Vyberte možnost **Upravit vzorec**.
7.  Do **pole Receptura** zadejte **Model.Selector(Model.Data.Summary.Code)**.
8.  Zvolte **Uložit**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Zavřete stránku **Editor vzorců**.
10. Vyberte **OK**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Všimněte si, že vypočtené pole **LevelByLookup**, které jste přidali, vrátí daňovou úroveň jako hodnotu **seznamu úrovní zdanění** pro každý záznam sumarizovaných daňových transakcí. Kód daně záznamu bude předán do zdroje dat vyhledávání **Model.Selector** a sada pravidel pro tento zdroj dat bude použita při výběru správné úrovně zdanění.

### <a name="add-a-new-format-enumeration-based-data-source"></a>Přidání nového zdroje dat na základě vyčíslení formátu

Dále přidáte nový zdroj dat, který odkazuje na vyčíslení formát, který jste přidali dříve. Hodnoty tohoto zdroje dat budou později použity ve výrazu formátu ER.

1.  Vyberte **Přidat kořen**.
2.  Vyberte **Vyčíslení formátu\Enumeration**.
3.  Do pole **Název** zadejte **TaxationLevel**.
4.  Do pole **Vyčíslení formátu** zadejte **Seznam úrovní zdanění**.
5.  Zvolte **Uložit**.

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>Úprava existujícího pole, aby bylo možné začít používat vyhledávání

Dále upravíte existující vypočtené pole tak, aby používalo konfigurovaný vyhledávací zdroj dat k vrácení správné hodnoty úrovně zdanění v závislosti na kódu daně.

1.  Vyberte položku **Model.Data.Summary.Level**.
2.  Vyberte možnost **Upravit**.
3.  Vyberte možnost **Upravit vzorec**.

    Všimněte si, že aktuální výraz pole **Model.Data.Summary.Level** obsahuje následující kódy pevně zakódovaných daní:
    
    CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")

4.  Do pole **Formula** Receptura zadejte **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.

    ![Stránka návrháře operace ER](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Všimněte si, že výraz v poli **Model.Data.Summary.Level** bude nyní vracet úroveň zdanění na základě kódu daně aktuálního záznamu a sady pravidel, které uživatel obchodního pravidla konfiguruje ve zdroji dat vyhledávání **Model.Data.Summary.Level**.
    
5.  Zvolte **Uložit**.
6.  Zavřete stránku **Návrhář vzorce**.
7.  Vyberte **OK**.
8.  Zvolte **Uložit**.
9.  Zavřete stránku **návrháře formátu**.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Dokončete koncept odvozeného formátu

1.  Na pevné záložce **Verze** vyberte možnost **Stav změny**.
2.  Zvolte **Dokončit**.
3.  Vyberte **OK**.

## <a name="export-completed-version-of-modified-format"></a>Exportujte dokončenou verzi modifikovaného formátu

1.  Ve stromu konfigurace vyberte položku **Formát pro ověření, jak vyhledat data LE**.
2.  Na pevné záložce **Verze** vyberte záznam se stavem **Dokončeno**.
3.  Vyberte **Exchange**.
4.  Vyberte **Exportovat jako soubor XML**.
5.  Vyberte **OK**.
6.  Webový prohlížeč stáhne soubor **Formát k zjištění, jak vyhledat data LE**. Tento soubor si uložte místně.

Chcete-li se dozvědět, jak vyhledat formát **Formát k zjištění, jak vyhledat data LE**, zopakujte kroky v tomto oddílu a uložte si místně následující soubory.

-   Format to learn parameterized calls.xml
-   Mapping to learn parameterized calls.xml
-   Model to learn parameterized calls.xml

Pokud chcete zjistit, jak používat konfigurovaný formát ER **Formát k zjištění, jak vyhledávat data LE** pro nastavení sad daňových kódů závislých na právnické osobě k filtrování daňových transakcí podle různých úrovní zdanění, dokončete kroky v tématu [Nastavení parametrů formátu ER podle právnické osoby](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Další zdroje

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Nastavení parametrů formátu ER podle právnické osoby](er-app-specific-parameters-set-up.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]