---
title: Návrh konfigurace pro generování dokumentů ve formátu Excel
description: Tento článek popisuje, jak navrhnout formát elektronického výkaznictví tak, aby vyplnil šablonu Excel, a poté vygenerovat odchozí dokumenty ve formátu Excel.
author: kfend
ms.date: 05/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 2feadf8e196936220cf557989cae40b742447d99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280917"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Návrh konfigurace pro generování dokumentů ve formátu Excel

[!include[banner](../includes/banner.md)]

Můžete navrhnout konfiguraci formátu [elektronického výkaznictví](general-electronic-reporting.md) s komponentou formátu elektronického výkaznictví, kterou můžete nakonfigurovat tak, aby generovala odchozí dokument ve formátu sešitu Microsoft Excel. K tomuto účelu musí být použity specifické komponenty formátu elektronického výkaznictví.

Chcete-li se o této funkci dozvědět více, postupujte podle kroků v článku [Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Přidání nového formátu elektronického výkaznictví

Při přidání nové konfigurace formátu elektronického výkaznictví pro generování odchozího dokument ve formátu sešitu Excel musíte vybrat hodnotu **Excel** pro atribut formátu **Typ formátu** nebo ponechat atribut **Typ formátu** prázdný.

- Pokud vyberete **Excel**, můžete nakonfigurovat formát tak, aby generoval odchozí dokument pouze ve formátu Excel.
- Pokud atribut necháte prázdný, můžete nakonfigurovat formát tak, aby generoval odchozí dokument v libovolném formátu, který je podporován rámcem elektronického výkaznictví.

Chcete-li nakonfigurovat komponentu formátu elektronického výkaznictví, vyberte v podokně akcí možnost **Návrhář** a otevřete komponentu formátu elektronického výkaznictví pro úpravy v návrháři operací elektronického výkaznictví.

![Stránka konfigurace.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Součást souboru Excel

### <a name="manual-entry"></a>Ruční zadání

Musíte přidat komponentu **Excel\\Soubor** do nakonfigurovaného formátu elektronického výkaznictví pro generování odchozího dokumentu ve formátu Excel.

![Součást Excel\Soubor.](./media/er-excel-format-add-file-component.png)

Chcete-li určit rozvržení odchozího dokumentu, připojte sešit aplikace Excel, který má příponu .xlsx k součásti **Excel\\Soubor**, jako šablonu pro odchozí dokumenty.

> [!NOTE]
> Když ručně připojíte šablonu, musíte použít [typ dokumentu](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types), který byl za tímto účelem nakonfigurován v [parametrech elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Přidání přílohy ke komponentě Excel\Soubor.](./media/er-excel-format-add-file-component2.png)

Chcete-li určit, jak bude připojená šablona vyplněna při spuštění konfigurovaného formátu elektronického výkaznictví, musíte přidat vnořené komponenty **List**, **Rozsah** a **Buňka** k součásti **Excel\\Soubor**. Každá vnořená součást musí být přidružena l položce s názvem Excel.

### <a name="template-import"></a>Import šablony

Můžete vybrat možnost **Importovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat novou šablonu do prázdného formátu elektronického výkaznictví. V tomto příkladu bude součást **Excel\\Soubor** vytvořena automaticky a k ní bude připojena importovaná šablona. Všechny požadované komponenty elektronického výkaznictví budou také vytvořeny automaticky na základě nalezených položek s názvem Excel.

![Volba možnosti Importovat z Excelu.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.

## <a name="sheet-component"></a>Komponenta listu

Komponenta **List** označuje pracovní list přiloženého sešitu aplikace Excel, který musí být vyplněn. Název listu v šabloně Excel je definován ve vlastnosti **List** této komponenty.

> [!NOTE]
> Tato součást je volitelná pro sešity aplikace Excel, které obsahují jeden list.

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **List** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vložen příslušný list.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu, vygenerovaný dokument nebude obsahovat pracovní list.

![Příklad součásti listu.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Součást rozsahu

### <a name="nested-components"></a>Vnořené komponenty

#### <a name="data-typing"></a>Typování dat

Součást **Rozsah** může mít další vnořené součásti elektronického výkaznictví, které se používají k zadávání hodnot do příslušných rozsahů.

- Pokud je některá součást skupiny **Text** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako textová hodnota.

    > [!NOTE]
    > Tento vzor použijte k formátování zadaných hodnot na základě národního prostředí, které je definováno v aplikaci.

- Pokud je součást **Buňka** skupiny **Excel** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako hodnota datového typu, který je definován vazbou součásti **Buňka**. Datový typ může být například **Řetězec**, **Reálné číslo** nebo **Celé číslo**.

    > [!NOTE]
    > Tento vzor použijte k povolení aplikace Excel pro formátování zadané hodnoty na základě národního prostředí místního počítače, které otevírá odchozí dokument.

#### <a name="row-handling"></a>Manipulace s řádky

Komponentu **Rozsah** lze nakonfigurovat jako vertikálně replikovanou, takže v listu aplikace Excel je generováno více řádků. Řádky může generovat nadřazená komponenta **Rozsah** nebo vnořená komponenta **Rozsah**.

Ve verzi 10.0.26 a novější můžete vynutit, aby vygenerovaný list ponechal vygenerované řádky na stejné stránce. V návrháři formátu ER nastavte možnost **Udržovat řádky pohromadě** na **Ano** pro nadřazenou komponentu **Rozsah** v editovatelném formátu ER. ER se pak pokusí ponechat veškerý obsah, který je generován tímto rozsahem, na stejné stránce. Pokud výška obsahu překročí zbývající prostor na aktuální stránce, bude přidán konec stránky a obsah začne v horní části další nové stránky.

> [!NOTE]
> Doporučujeme vám nakonfigurovat možnost **Udržovat řádky pohromadě** pouze pro rozsahy, které pokrývají celou šířku generovaného dokumentu.
>
> Možnost **Udržovat řádky pohromadě** se vztahuje pouze na komponenty **Excel \> Soubor**, které jsou nakonfigurovány pro použití šablony sešitu aplikace Excel.
>
> Možnost **Udržovat řádky pohromadě** se dá použít pouze tehdy, když je povolena možnost **Povolit používání knihovny EPPlus v rámci elektronického vykazování**.
>
> Tuto funkci lze použít pro komponenty **Rozsah**, které jsou umístěny pod komponentou **Stránka**. Neexistuje však žádná záruka, že [součty zápatí stránky](er-paginate-excel-reports.md#add-data-sources-to-calculate-page-footer-totals) se správně vypočítají pomocí zdrojů dat [Sběr dat](er-data-collection-data-sources.md).

Chcete-li se dozvědět, jak tuto možnost používat, postupujte podle příkladů v [Návrh formátu ER k udržení řádků pohromadě na stejné stránce aplikace Excel](er-keep-excel-rows-together.md).

### <a name="replication"></a>Replikace

Vlastnost **Směr replikace** určuje, zda a jak bude rozsah opakován v generovaném dokumentu:

- **Žádná replikace** – Příslušný rozsah Excelu se ve vygenerovaném dokumentu nebude opakovat.
- **Vertikální** – Příslušný rozsah Excelu se ve vygenerovaném dokumentu bude opakovat vertikálně. Každý replikovaný rozsah je umístěn pod původní rozsah v šabloně Excel. Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.
- **Horizontální** – Příslušný rozsah Excelu se ve vygenerovaném dokumentu bude opakovat horizontálně. Každý replikovaný rozsah je umístěn napravo od původního rozsahu v šabloně Excel. Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.

    Chcete-li se dozvědět více o horizontální replikaci, postupujte podle kroků v části [Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel](tasks/er-horizontal-1.md).

### <a name="enabling"></a>Povoluje se

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **Rozsah** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vyplněn příslušný rozsah.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah nepředstavuje celé řádky nebo sloupce, nebude do vygenerovaného dokumentu vyplněn příslušný rozsah.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah představuje celé řádky nebo sloupce, vygenerovaný dokument bude obsahovat tyto řádky a sloupce jako skryté.

### <a name="resizing"></a>Změna velikosti

Šablonu aplikace Excel můžete nakonfigurovat tak, aby používala buňky k prezentaci textových dat. Chcete-li zajistit, aby byl ve vygenerovaném dokumentu viditelný celý text v buňce, můžete tuto buňku nakonfigurovat tak, aby do ní text automaticky zalamovala. Můžete také nakonfigurovat řádek obsahující tuto buňku tak, aby automaticky upravil svou výšku, pokud není zalomený text zcela viditelný. Další informace naleznete v části „Zalamování textu v buňce“ v [Opravte data, která jsou v buňkách oříznutá](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e).

> [!NOTE]
> Kvůli známému [Omezení Excelu](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353), i když nakonfigurujete buňky pro zalamování textu a nakonfigurujete řádky obsahující tyto buňky tak, aby automaticky upravovaly svou výšku tak, aby odpovídaly zalamovanému textu, možná nebudete moci použít funkce aplikace Excel **Automatické přizpůsobení** a **Obtékání textu** pro sloučené buňky a řádky, které je obsahují. 

Od verze 10.0.23 aplikace Dynamics 365 Finance můžete při práci v generovaném dokumentu přinutit elektronické výkaznictví, aby vypočítalo výšku každého řádku, který byl konfigurován tak, aby se jeho výška automaticky přizpůsobila obsahu vnořených buněk, kdykoli tento řádek obsahuje alespoň jednu sloučenou buňku, která byla konfigurována tak, aby obtékala text uvnitř. Vypočítaná výška se pak použije ke změně velikosti řádku, aby bylo zajištěno, že ve vygenerovaném dokumentu budou viditelné všechny buňky v řádku.

> [!NOTE]
> Poznámka: tato funkce nemusí fungovat podle očekávání, když se k formátování sloučené buňky použije vlastní písmo. Protože Excel nevkládá vlastní písma, neposkytuje informace o vlastní velikosti písma. Velikost sloučené buňky proto může být nesprávně odhadnuta.

Chcete-li začít používat tuto funkci při spuštění jakýchkoli formátů elektronického výkaznictví, které byly nakonfigurovány pro použití šablon aplikace Excel ke generování odchozích dokumentů, postupujte takto.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** vyberte v části **Související odkazy** možnost **Parametry elektronického výkaznictví**.
3. Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Modul runtime** u možnosti **Zalamovat text v buňce** hodnotu **Ano**.

Pokud chcete změnit toto pravidlo pro jeden formát elektronického výkaznictví, aktualizujte verzi konceptu tohoto formátu podle následujících kroků.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte konfiguraci elektronického výkaznictví, která je navržena pro použití šablony Excel pro generování odchozích dokumentů.
4. Na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.
5. V podokně akcí zvolte **Návrhář**.
6. Na stránce **Návrhář formátu** ve stromu formátu v levém podokně vyberte komponentu Excel, která je propojena s šablonou Excel.
7. Na kartě **Formát** v poli **Upravte výšku řádku** vyberte hodnotu, která určí, zda má být elektronické výkaznictví vynuceno za běhu změnit výšku řádků v odchozím dokumentu, který je generován upraveným formátem elektronického výkaznictví:

    - **Výchozí** – Použijte obecné nastavení, které je nakonfigurováno v poli **Automaticky přizpůsobit výšku řádku** na stránce **Parametry elektronického výkaznictví**.
    - **Ano** – Přepište obecné nastavení a změňte výšku řádku za běhu.
    - **Ne** – Přepište obecné nastavení a neměňte výšku řádku za běhu.

## <a name="cell-component"></a>Součást buňky

Součást **Buňka** se používá k vyplnění pojmenovaných buněk, tvarů a obrázků Excelu. Chcete-li označit objekt pojmenovaný Excel, který musí být vyplněn součástí elektronické výkaznictví **Buňka**, musíte zadat název tohoto objektu ve vlastnosti **Rozsah aplikace Excel** součásti **Buňka**.

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **Buňka** k určení, zda ve vygenerovaném dokumentu musí být vyplněn objekt:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vyplněn příslušný objekt. Vazba této součásti **Buňka** určuje hodnotu vloženou do příslušného objektu.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu, příslušný objekt nebude vyplněn ve vygenerovaném dokumentu.

Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do buňky, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu (například **Řetězec**, **Skutečný**, nebo **Celé číslo**). V tomto případě je hodnota zadána do buňky jako hodnota stejného typu dat.

Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do tvaru Excel, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu (například **Řetězec**, **Skutečný**, nebo **Celé číslo**). V tomto případě je hodnota zadána do tvaru Excel jako text tohoto tvaru. Pro hodnoty typů dat, které nejsou **řetězcem**, převod na text se provádí automaticky.

> [!NOTE]
> Můžete nakonfigurovat součást **Buňka** pro vyplnění tvaru pouze v případech, kdy je podporována vlastnost textu tvaru.

Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do obrázku Excelu, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu **Kontejner**, který představuje obrázek v binárním formátu. V tomto případě je hodnota zadána do obrázku Excelu jako obrázek.

> [!NOTE]
> Každý obrázek a tvar Excelu je považován za ukotvený svým levým horním rohem ke konkrétní buňce nebo rozsahu Excelu. Pokud chcete replikovat obrázek nebo tvar aplikace Excel, musíte nakonfigurovat buňku nebo rozsah, do kterých jsou ukotveny, jako replikovanou buňku nebo rozsah.

Chcete-li se dozvědět více o tom, jak vkládat obrázky a tvary, nahlédněte do části [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Součást konce stránky

Součást **Konec stránky** vynutí, aby Excel začal na nové stránce. Tato součást není vyžadována, pokud chcete použít výchozí stránkování aplikace Excel, ale měli byste ji použít, pokud chcete, aby aplikace Excel postupovala podle formátu elektronického výkaznictví pro vytvoření stránkování.

## <a name="page-component"></a><a name="page-component"></a>Komponenta Strana

### <a name="overview"></a>Přehled

Komponentu **Strana** použijte, když chcete, aby Excel ve vygenerovaném odchozím dokumentu dodržoval formát elektronického výkaznictví a stránkování struktury. Když formát elektronického výkaznictví spouští komponenty, které jsou podřazeny komponentě **Strana**, automaticky se přidají požadované konce stránek. Během tohoto procesu se bere do úvahy velikost generovaného obsahu, nastavení stránky šablony aplikace Excel a velikost papíru vybraná v šabloně aplikace Excel.

Pokud musíte vygenerovaný dokument rozdělit do různých sekcí, z nichž každá má jiné stránkování, můžete konfigurovat několik komponent **Strana** v každé komponentě [List](er-fillable-excel.md#sheet-component).

### <a name="structure"></a><a name="page-component-structure"></a>Struktura

Pokud je první komponentou podřazenou komponentě **Strana** komponenta typu [Rozsah](er-fillable-excel.md#range-component), která má **Směr replikace** nastaven na **Žádná replikace**, tento rozsah je považován za záhlaví stránky pro stránkování založené na nastavení aktuální komponenty **Strana**. Rozsah aplikace Excel, který je přidružen k této komponentě formátu, se opakuje v horní části každé stránky, která je generována pomocí nastavení aktuální komponenty **Strana**.

> [!NOTE]
> Aby bylo zajištěno správné stránkování, když je ve vaší šabloně aplikace Excel konfigurován rozsah [Řádky, které se mají nahoře opakovat](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409), musí se adresa tohoto rozsahu aplikace Excel rovnat adrese rozsahu, který je přidružen k dříve popsané komponentě **Rozsah**.

Pokud je poslední komponentou podřazenou komponentě **Strana** komponenta typu **Rozsah**, která má **Směr replikace** nastaven na **Žádná replikace**, tento rozsah je považován za zápatí stránky pro stránkování založené na nastavení aktuální komponenty **Strana**. Rozsah aplikace Excel, který je přidružen k této komponentě formátu, se opakuje v dolní části každé stránky, která je generována pomocí nastavení aktuální komponenty **Strana**.

> [!NOTE]
> Aby bylo zajištěno správné stránkování, neměly by se rozsahy aplikace Excel, které jsou přidruženy ke komponentě **Rozsah**, za běhu měnit. Nedoporučujeme formátovat buňky tohoto rozsahu pomocí [možností](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84) **Zalamovat text v buňce** a **Přizpůsobit výšku řádků** aplikace Excel.

Můžete přidat několik dalších komponent **Rozsah** mezi volitelné komponenty **Rozsah**, které určí způsob vyplňování generovaného dokumentu.

Pokud sada vnořených komponent **Rozsah** podřazených komponentě **Strana** nevyhovuje dříve popsané struktuře, dojde k [chybě](er-components-inspections.md#i17) ověření v režimu návrhu v návrháři formátu elektronického výkaznictví. Chybová zpráva vás informuje, že problém může způsobit problémy za běhu.

> [!NOTE]
> Chcete-li generovat správný výstup, nezadávejte vazbu pro žádnou komponentu **Rozsah** podřazenou komponentě **Strana**, pokud je vlastnost **Směr replikace** pro tuto komponentu **Rozsah** nastavena na **Žádná replikace** a rozsah je konfigurován tak, aby generoval záhlaví stránky nebo zápatí stránky.

Pokud chcete, aby počítání a sčítání související se stránkováním vypočítalo průběžné součty a součty za stránku, doporučujeme konfigurovat požadované zdroje dat pro [shromažďování dat](er-data-collection-data-sources.md). Chcete-li se naučit používat komponentu **Strana** ke stránkování generovaného sešitu aplikace Excel, dokončete postupy uvedené v článku [Návrh formátu elektronického výkaznictví pro stránkování generovaného dokumentu ve formátu aplikace Excel](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Omezení

Když použijete komponentu **Strana** ke stránkování v Excelu, nebudete znát konečný počet stránek ve vygenerovaném dokumentu, dokud nebude stránkování dokončeno. Proto nemůžete vypočítat celkový počet stránek pomocí vzorců elektronického výkaznictví a vytisknout správný počet stránek generovaného dokumentu na libovolnou stránku před poslední stránkou.

> [!TIP]
> Chcete-li tato čísla uvést v záhlaví nebo zápatí aplikace Excel, použijte speciální [formátování](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) Excelu pro záhlaví a zápatí.

Konfigurované komponenty **Strana** nejsou brány do úvahy při aktualizaci šablony aplikace Excel v upravitelném formátu v Dynamics 365 Finance verze 10.0.22. Tato funkce je zvažována pro další vydání aplikace Finance.

Pokud konfigurujete šablonu aplikace Excel tak, aby používala [podmíněné formátování](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting), v některých případech toto nemusí fungovat podle očekávání.

### <a name="applicability"></a>Použitelnost

Komponenta **Strana** funguje u komponenty formátu [souboru aplikace Excel](er-fillable-excel.md#excel-file-component) pouze v případě, že je tato komponenta nakonfigurována pro použití šablony v aplikaci Excel. Jestliže [nahradíte](tasks/er-design-configuration-word-2016-11.md) šablonu aplikace Excel šablonou aplikace Word a poté spustíte upravitelný formát elektronického výkaznictví, komponenta **Strana** bude ignorována.

Komponenta **Strana** funguje pouze tehdy, když je povolena možnost **Povolit používání knihovny EPPlus v rámci elektronického vykazování**. Je vyvolána výjimka za běhu, pokud se elektronické výkaznictví pokusí zpracovat komponentu **Strana**, když je tato funkce deaktivována.

> [!NOTE]
> Je vyvolána výjimka za běhu, pokud formát elektronického výkaznictví zpracovává komponentu **Strana** šablony aplikace Excel, která obsahuje alespoň jeden vzorec, který odkazuje na neplatnou buňku. Chcete-li zabránit chybám za běhu, opravte šablonu aplikace Excel podle popisu v článku [Jak opravit chybu #ODKAZ!](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Komponenta zápatí

Komponenta **Zápatí** se používá k vyplnění zápatí v dolní části vygenerovaného listu v sešitu aplikace Excel.

> [!NOTE]
> Tuto komponentu můžete přidat pro všechny komponenty **List** k určení různých zápatí pro různé listy ve vygenerovaném sešitu aplikace Excel.

Když konfigurujete jednotlivou komponentu **Zápatí**, můžete použít vlastnost **Vzhled záhlaví/zápatí** k určení stránek, pro které se komponenta používá. K dispozici jsou následující hodnoty:

- **Všechny** – Spustit nakonfigurovanou komponentu **Zápatí** pro všechny stránky nadřazeného listu aplikace Excel.
- **První** – Spustit nakonfigurovanou komponentu **Zápatí** pouze pro první stránku nadřazeného listu aplikace Excel.
- **Sudá** – Spustit nakonfigurovanou komponentu **Zápatí** pouze pro sudé stránky nadřazeného listu aplikace Excel.
- **Lichá** – Spustit nakonfigurovanou komponentu **Zápatí** pouze pro liché stránky nadřazeného listu aplikace Excel.

Pro jednu komponentu **List** můžete přidat několik komponent **Zápatí**, z nichž každá má pro vlastnost **Vzhled záhlaví/zápatí** jinou hodnotu. Tímto způsobem můžete vygenerovat různá zápatí pro různé typy stránek v listu aplikace Excel.

> [!NOTE]
> Zajistěte, aby každá komponenta **Zápatí**, kterou přidáte do jednoho **Listu**, měla pro vlastnost **Vzhled záhlaví/zápatí** jinou hodnotu. Jinak dojde k [chybě ověření](er-components-inspections.md#i16). Chybová zpráva, kterou obdržíte, vás upozorní na nekonzistenci.

Pod přidanou komponentu **Zápatí** přidejte požadované vnořené komponenty **Text\\Řetězec**, **Text\\DateTime** nebo jiný typ. Nakonfigurujte vazby pro tyto komponenty a určete, jak je vyplněno vaše zápatí stránky.

Můžete také použít speciální [formátovací kódy](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) ke správnému formátování obsahu vygenerovaného zápatí. Chcete-li se naučit používat tento přístup, postupujte podle pokynů v [příkladu 1](#example-1) dále v tomto článku.

> [!NOTE]
> Při konfiguraci formátů elektronického výkaznictví nezapomeňte vzít v úvahu [limit](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) Excel a maximální počet znaků pro jedno záhlaví nebo zápatí.

## <a name="header-component"></a>Komponenta záhlaví

Komponenta **Záhlaví** se používá k vyplnění záhlaví v horní části vygenerovaného listu v sešitu aplikace Excel. Používá se stejně jako komponenta **Zápatí**.

## <a name="edit-an-added-er-format"></a>Úprava přidaného formátu elektronického výkaznictví

### <a name="update-a-template"></a>Aktualizace šablony

Můžete vybrat možnost **Aktualizovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat aktualizovanou šablonu do upravitelného formátu elektronického výkaznictví. Během tohoto procesu bude šablona vybrané součásti **Excel\\Soubor** nahrazena novou šablonou. Obsah upravitelného formátu elektronického výkaznictví bude synchronizován s obsahem aktualizované šablony elektronického výkaznictví.

- Nová komponenta formátu elektronického výkaznictví bude automaticky vytvořena pro každý název Excelu, pokud komponenta formátu elektronického výkaznictví není nalezena v upravitelném formátu.
- Každá součást formátu elektronického výkaznictví bude odstraněna z upravitelného formátu elektronického výkaznictví, pokud pro ni nebude nalezen příslušný název Excelu.

> [!NOTE]
> Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.
>
> Pokud upravitelný formát elektronického výkaznictví původně obsahoval prvky **List**, doporučujeme nastavit možnost **Vytvořit prvek formátu listu Excel** na **Ano** při importu aktualizované šablony. V opačném případě budou všechny vnořené prvky původního prvku **List** vytvořeny od začátku. Proto budou všechny vazby znovu vytvořených prvků formátu ztraceny v aktualizovaném formátu elektronického výkaznictví.

![Možnost Vytvořit prvek formátu listu Excel v dialogovém okně Aktualizovat z Excelu.](./media/er-excel-format-update-template.png)

Ve verzi 10.0.28 a novějších můžete použít volbu **Aktualizujte prvky formátu záhlaví a zápatí aplikace Excel**.

- Když nastavíte tuto možnost na **Ne**, prvky formátu Excel Header a Excel Footer zůstanou nezměněny, i když byla odpovídající záhlaví nebo zápatí aktualizována v listech importované šablony ve formátu sešitu Excel.
- Když nastavíte tuto možnost na **Ano**, prvky formátu Excel Header a Excel Footer se změní, když byla odpovídající záhlaví nebo zápatí aktualizována v listech importované šablony ve formátu sešitu Excel.

    - Pokud se struktura záhlaví nebo zápatí listu nezměnila nebo pokud byla pouze připojena, aktualizuje se struktura odpovídajícího prvku formátu Excel Header nebo Excel Footer. Vazby prvků formátu, které jsou vnořeny pod tímto prvkem formátu Excel Header nebo Excel Footer, budou zachovány.
    - Pokud se struktura záhlaví nebo zápatí listu změnila, odpovídající prvek formátu Excel Header nebo Excel Footer se opět vytvoří. Vazby prvků formátu, které jsou vnořeny pod tímto prvkem formátu Excel Header nebo Excel Footer, budou odebrány.

![Možnost Aktualizovat prvky formátu záhlaví a zápatí Excel v dialogovém okně Aktualizovat z Excelu.](./media/er-excel-format-update-template2.png)

Chcete-li se o této funkci dozvědět více, postupujte podle pokynů v části [Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Ověření formátu elektronického výkaznictví

Při ověření formátu elektronického výkaznictví, který lze upravit, se provede kontrola konzistence, aby se zajistilo, že název Excel bude přítomen v aktuálně používané šabloně Excel. O jakýchkoli nesrovnalostech budete informováni. V případě některých nesrovnalostí bude nabídnuta možnost automaticky opravit problémy.

![Chybové zprávy ověření.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Řízení průběhu výpočtu vzorců aplikace Excel

Když je generován odchozí dokument ve formátu sešitu Microsoft Excel, některé buňky tohoto dokumentu mohou obsahovat vzorce aplikace Excel. Když je aktivována funkce **Povolit použití knihovny EPPlus v rámci elektronického výkaznictví**, můžete určit, kdy přesně se vzorce vypočítají, změnou hodnoty [parametru](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Možnosti výpočtu** v šabloně aplikace Excel, která se používá:

- Když vyberete hodnotu **Automaticky**, přepočítají se všechny závislé vzorce pokaždé, když je generovaný dokument připojen novými rozsahy, buňkami atd.

    > [!NOTE]
    > To může způsobit problém s výkonem šablon aplikace Excel, které obsahují více souvisejících vzorců.

- Když vyberete hodnotu **Ručně**, nebudou vzorce přepočítány při generování dokumentu.

    > [!NOTE]
    > Přepočet vzorce je vynucen ručně, když je generovaný dokument otevřen k náhledu v aplikaci Excel.
    > Tuto možnost nepoužívejte, pokud konfigurujete cíl elektronického výkaznictví, který předpokládá použití vygenerovaného dokumentu bez jeho náhledu v aplikaci Excel (pro převod PDF, odeslání e-mailem atd.), protože generovaný dokument nemusí obsahovat hodnoty v buňkách obsahujících vzorce.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Příklad 1: Formátování obsahu zápatí

1. Použijte poskytnuté konfigurace elektronického výkaznictví ke [generování](er-generate-printable-fti-forms.md) dokumentu s volnou textovou fakturou (FTI), který lze tisknout.
2. Zkontrolujte zápatí vygenerovaného dokumentu. Všimněte si, že obsahuje informace o aktuálním čísle stránky a celkovém počtu stránek v dokumentu.

    ![Zkontrolujte zápatí vygenerovaného dokumentu ve formátu Excel.](./media/er-fillable-excel-footer-1.gif)

3. V návrháři formátu elektronického výkaznictví [otevřete](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) ukázkový formát elektronického výkaznictví pro kontrolu.

    Zápatí listu **faktury** je generováno na základě nastavení dvou komponent **Řetězec**, které jsou umístěny pod komponentou **Zápatí**.

    - První komponenta **Řetězec** vyplní následující speciální kódy formátování, aby donutila aplikaci Excel použít konkrétní formátování:

        - **&C** – Zarovnat text zápatí do středu.
        - **&"Segoe UI,Regular"&8** – Vložit text zápatí v písmu "Segoe UI Regular" písmo o velikosti 8 bodů.

    - Druhý komponent **Řetězec** vyplní text, který obsahuje aktuální číslo stránky a celkový počet stránek v aktuálním dokumentu.

    ![Zkontrolujte formát elektronického výkaznictví zápatí na stránce Návrhář formátů.](./media/er-fillable-excel-footer-2.png)

4. Přizpůsobte ukázkový formát elektronického výkaznictví a upravte aktuální zápatí stránky:

    1. [Vytvořit](er-quick-start2-customize-report.md#DeriveProvidedFormat) odvozený formát **Faktura s volným textem (Excel) vlastní**, který je založen na vzorovém formátu elektronického výkaznictví.
    2. Přidejte první nový pár komponent **Řetězec** pro komponentu **Zápatí** listu **Faktura**:

        1. Přidejte komponentu **Řetězec**, která zarovná název společnosti vlevo a zobrazí jej v 8bodovém písmu "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**).
        2. Přidejte komponentu **Řetězec** komponenta, která vyplňuje název společnosti (**model.InvoiceBase.CompanyInfo.Name**).

    3. Přidejte druhý nový pár komponent **Řetězec** pro komponentu **Zápatí** listu **Faktura**:

        1. Přidejte komponentu **Řetězec**, která zarovná datum zpracování vpravo a zobrazí jej v 8bodovém písmu "Segoe UI Regular" (**"&R&"Segoe UI,Regular"&8"**).
        2. Přidejte komponentu **Řetězec**, která vyplní datum zpracování ve vlastním formátu (**"&nbsp;&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Kontrola formátu elektronického výkaznictví zápatí na stránce Návrhář formátů.](./media/er-fillable-excel-footer-3.png)

    4. [Vyplňte](er-quick-start2-customize-report.md#CompleteDerivedFormat) verzi konceptu odvozeného formátu elektronického výkaznictví **Faktura s volným textem (Excel) vlastní**.

5. [Nakonfigurujte](er-generate-printable-fti-forms.md#configure-print-management) správu tisku pro použití odvozeného formátu elektronického výkaznictví **Faktura s volným textem (Excel) vlastní** namísto ukázkového formátu elektronického výkaznictví.
6. Vygenerujte tisknutelný dokument FTI a zkontrolujte zápatí vygenerovaného dokumentu.

    ![Kontrola zápatí vygenerovaného dokumentu ve formátu Excel.](./media/er-fillable-excel-footer-4.gif)

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a>Příklad 2: Oprava problému EPPlus se sloučenými buňkami

Můžete spustit formát elektronického výkaznictví a tím vygenerovat odchozí dokument ve formátu sešitu aplikace Excel. Když je povolena funkce **Povolit používání knihovny EPPlus v rámci elektronického vykazování** v pracovním prostoru **Správa funkcí**, [knihovna EPPlus](https://www.nuget.org/packages/epplus/4.5.2.1) se použije k vytvoření výstupu ve formátu sešitu Excel. Nicméně kvůli známému [chování aplikace Excel](https://answers.microsoft.com/en-us/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9) a omezení knihovny EPPlus se můžete setkat s následující výjimkou: „Nelze odstranit/přepsat sloučené buňky. Rozsah je částečně sloučen s jiným sloučeným rozsahem.“ Chcete-li zjistit, jaké šablony aplikace Excel mohou způsobit tuto výjimku a jak můžete problém vyřešit, postupujte dle následujícího příkladu.

1. V desktopové aplikaci Excel vytvořte nový sešit Excel.
2. V listu **List1** přidejte název **ReportTitle** pro buňku **A2**.
3. Slučte buňky **A1** a **A2**.

    ![Kontrola výsledků sloučení buněk A1 a A2 v navrženém sešitu Excel v desktopové aplikaci Excel.](./media/er-fillable-excel-example2-1.png)

3. Na stránce **Konfigurace** [přidejte nový formát elektronického výkaznictví](er-fillable-excel.md#add-a-new-er-format), abyste vygenerovali odchozí dokument ve formátu sešitu Excel.
4. Na stránce **Návrhář formátů** [importujte](er-fillable-excel.md#template-import) navržený sešit Excel do přidaného formátu elektronického výkaznictví jako novou šablonu pro odchozí dokumenty.
5. Na kartě **Mapování** nakonfigurujte vazbu pro komponentu **ReportTitle** typu [Buňka](er-fillable-excel.md#cell-component).
6. Spusťte konfigurovaný formát elektronického výkaznictví. Všimněte si, že je vyvolána následující výjimka: „Nelze odstranit/přepsat sloučené buňky. Rozsah je částečně sloučen s jiným sloučeným rozsahem.“

    ![Kontrola výsledků spuštění nakonfigurovaného formátu elektronického výkaznictví na stránce Návrhář formátů.](./media/er-fillable-excel-example2-2.png)

Problém opravíte některým z následujících způsobů:

- **Jednodušší, ale nedoporučuje se:** V pracovním prostoru **Správa funkcí** vypněte funkci **Povolit používání knihovny EPPlus v rámci elektronického vykazování**. Ačkoli je tento přístup snazší, můžete se při jeho použití setkat s jinými problémy, protože některé funkce elektronického vykazování jsou podporovány pouze v případě, že je povolena funkce **Povolit používání knihovny EPPlus v rámci elektronického vykazování**.
- **Doporučeno:** Postupujte následovně:

    1. V desktopové aplikaci Excel upravte sešit aplikace Excel jedním z následujících způsobů:

        - Na listu **List1** zrušte sloučení buněk **A1** a **A2**.
        - Změňte odkaz pro název **ReportTitle** z **=List1!$A$2** na **=List1!$A$1**.

        ![Kontrola výsledků změny odkazu v navrženém sešitu Excel v desktopové aplikaci Excel.](./media/er-fillable-excel-example2-3.png)

    2. Na stránce **Návrhář formátů** [importujte](er-fillable-excel.md#template-import) upravený sešit aplikace Excel do upravitelného formátu elektronického výkaznictví, aby se aktualizovala stávající šablona.
    3. Spusťte upravený formát elektronického výkaznictví.

        ![Kontrola vygenerovaného dokumentu v desktopové aplikaci Excel.](./media/er-fillable-excel-example2-4.png)

## <a name="limitations"></a>Omezení

### <a name="known-epplus-library-limitations"></a>Známá omezení knihovny EPPlus

#### <a name="external-data-sources"></a>Externí zdroje dat

Pokud jedna z vašich šablon obsahuje kontingenční tabulku, která je založena na modelu PowerPivot, který odkazuje na [externí zdroj dat](https://support.microsoft.com/office/create-a-pivottable-with-an-external-data-source-db50d01d-2e1c-43bd-bfb5-b76a818a927b), a je povolena funkce **Povolit použití knihovny EPPlus v rámci elektronického vykazování**, při spuštění formátu elektronického výkaznictví, který používá tuto šablonu ke generování odchozího dokumentu ve formátu Excel, se zobrazí následující chybová zpráva: „Zdroj mezipaměti není list.“ Chcete-li problém opravit, máte následující možnosti:

- **Doporučeno:** Přepracujte řešení Excel, které používáte:

    1. Izolujte část, která obsahuje kontingeční body, v samostatném sešitu aplikace Excel (sešit A). 
    2. Pomocí elektronického výkaznictví vygenerujte druhý sešit aplikace Excel (sešit B) z Finance, který obsahuje požadované podrobnosti. 
    3. V sešitu A se odkažte na sešit B, jakmile se sešit B vygeneruje.

- Vypněte funkci **Povolit použití knihovny EPPlus v elektronickém reportovacím rámci** k použití možnosti jiné než EPPlus. 

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks\er-design-reports-openxml-2016-11.md)

[Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel](modify-electronic-reporting-format-reapply-excel-template.md)

[Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel](tasks/er-horizontal-1.md)

[Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md)

[Konfigurace elektronického výkaznictví pro doplňování dat do Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
