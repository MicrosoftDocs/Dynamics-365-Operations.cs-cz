---
title: Návrh konfigurace pro generování dokumentů ve formátu Excel
description: Toto téma popisuje, jak navrhnout formát elektronického výkaznictví tak, aby vyplnil šablonu Excel, a poté vygenerovat odchozí dokumenty ve formátu Excel.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8d6a18741d57829d1929fb8362dc4ba8e03a1bd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094022"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Návrh konfigurace pro generování dokumentů ve formátu Excel

[!include[banner](../includes/banner.md)]

Můžete navrhnout konfiguraci formátu [elektronického výkaznictví](general-electronic-reporting.md), která má [součást formátu](general-electronic-reporting.md#FormatComponentOutbound) elektronického výkaznictví, kterou můžete nakonfigurovat tak, aby generovala odchozí dokument ve formátu Microsoft Excel. K tomuto účelu musí být použity specifické komponenty formátu elektronického výkaznictví.

Chcete-li se o této funkci dozvědět více, postupujte podle kroků v tématu [Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Přidání nového formátu elektronického výkaznictví

Při přidání nové konfigurace formátu elektronického výkaznictví pro generování odchozího dokument ve formátu sešitu Excel musíte vybrat hodnotu **Excel** pro atribut formátu **Typ formátu** nebo ponechat atribut **Typ formátu** prázdný.

- Pokud vyberete **Excel**, můžete nakonfigurovat formát tak, aby generoval odchozí dokument pouze ve formátu Excel.
- Pokud atribut necháte prázdný, můžete nakonfigurovat formát tak, aby generoval odchozí dokument v libovolném formátu, který je podporován rámcem elektronického výkaznictví.

Chcete-li nakonfigurovat komponentu formátu elektronického výkaznictví, vyberte v podokně akcí možnost **Návrhář** a otevřete komponentu formátu elektronického výkaznictví pro úpravy v návrháři operací elektronického výkaznictví.

![Stránka Konfigurace](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Součást souboru Excel

### <a name="manual-entry"></a>Ruční zadání

Musíte přidat komponentu **Excel\\Soubor** do nakonfigurovaného formátu elektronického výkaznictví pro generování odchozího dokumentu ve formátu Excel.

![Součást Excel\Soubor](./media/er-excel-format-add-file-component.png)

Chcete-li určit rozvržení odchozího dokumentu, připojte sešit aplikace Excel, který má příponu .xlsx k součásti **Excel\\Soubor**, jako šablonu pro odchozí dokumenty.

> [!NOTE]
> Když ručně připojíte šablonu, musíte použít [typ dokumentu](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), který byl za tímto účelem nakonfigurován v [parametrech elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Přidání přílohy ke komponentě Excel\Soubor](./media/er-excel-format-add-file-component2.png)

Chcete-li určit, jak bude připojená šablona vyplněna při spuštění konfigurovaného formátu elektronického výkaznictví, musíte přidat vnořené komponenty **List**, **Rozsah** a **Buňka** k součásti **Excel\\Soubor**. Každá vnořená součást musí být přidružena l položce s názvem Excel.

### <a name="template-import"></a>Import šablony

Můžete vybrat možnost **Importovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat novou šablonu do prázdného formátu elektronického výkaznictví. V tomto příkladu bude součást **Excel\\Soubor** vytvořena automaticky a k ní bude připojena importovaná šablona. Všechny požadované komponenty elektronického výkaznictví budou také vytvořeny automaticky na základě nalezených položek s názvem Excel.

![Volba možnosti Importovat z Excelu](./media/er-excel-format-import-template.png)

> [!NOTE]
> Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.

## <a name="sheet-component"></a>Komponenta listu

Komponenta **List** označuje pracovní list přiloženého sešitu aplikace Excel, který musí být vyplněn. Název listu v šabloně Excel je definován ve vlastnosti **List** této komponenty.

> [!NOTE]
> Tato součást je volitelná pro sešity aplikace Excel, které obsahují jeden list.

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **List** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vložen příslušný list.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu, vygenerovaný dokument nebude obsahovat pracovní list.

![Příklad součásti listu](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Součást rozsahu

Součást **Rozsah** označuje rozsah Excelu, který musí být ovládán touto součástí elektronického výkaznictví. Název rozsahu je definován ve vlastnosti **Rozsah aplikace Excel** této komponenty.

Vlastnost **Směr replikace** určuje, zda a jak bude rozsah opakován v generovaném dokumentu:

- Pokud je vlastnost **Směr replikace** nastavena na **Žádná replikace**, příslušný rozsah aplikace Excel nebude ve vygenerovaném dokumentu opakován.
- Pokud je vlastnost **Směr replikace** nastavena na **Vertikální**, příslušný rozsah aplikace Excel bude ve vygenerovaném dokumentu opakován. Každý replikovaný rozsah je umístěn pod původní rozsah v šabloně Excel. Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.
- Pokud je vlastnost **Směr replikace** nastavena na **Horizontální**, příslušný rozsah aplikace Excel bude ve vygenerovaném dokumentu opakován. Každý replikovaný rozsah je umístěn napravo od původního rozsahu v šabloně Excel. Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.

Chcete-li se dozvědět více o horizontální replikaci, postupujte podle kroků v části [Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel](tasks/er-horizontal-1.md).

Součást **Rozsah** může mít další vnořené součásti elektronického výkaznictví, které se používají k zadávání hodnot do příslušných pojmenovaných rozsahů aplikace Excel.

- Pokud je některá součást skupiny **Text** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako textová hodnota.

    > [!NOTE]
    > Tento vzor použijte k formátování zadaných hodnot na základě národního prostředí, které je definováno v aplikaci.

- Pokud je součást **Buňka** skupiny **Excel** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako hodnota datového typu, který je definován vazbou součásti **Buňka** (například **Řetězec**, **Skutečný**, nebo **Celé číslo**).

    > [!NOTE]
    > Tento vzor použijte k povolení aplikace Excel pro formátování zadané hodnoty na základě národního prostředí místního počítače, které otevírá odchozí dokument.

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **Rozsah** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vyplněn příslušný rozsah.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah nepředstavuje celé řádky nebo sloupce, nebude do vygenerovaného dokumentu vyplněn příslušný rozsah.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah představuje celé řádky nebo sloupce, vygenerovaný dokument bude obsahovat tyto řádky a sloupce jako skryté.

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

## <a name="edit-an-added-er-format"></a>Úprava přidaného formátu elektronického výkaznictví

### <a name="update-a-template"></a>Aktualizace šablony

Můžete vybrat možnost **Aktualizovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat aktualizovanou šablonu do upravitelného formátu elektronického výkaznictví. Během tohoto procesu bude šablona vybrané součásti **Excel\\Soubor** nahrazena novou šablonou. Obsah upravitelného formátu elektronického výkaznictví bude synchronizován s obsahem aktualizované šablony elektronického výkaznictví.

- Nová komponenta formátu elektronického výkaznictví bude automaticky vytvořena pro každý název Excelu, pokud komponenta formátu elektronického výkaznictví není nalezena v upravitelném formátu.
- Každá součást formátu elektronického výkaznictví bude odstraněna z upravitelného formátu elektronického výkaznictví, pokud pro ni nebude nalezen příslušný název Excelu.

> [!NOTE]
> Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.
>
> Pokud upravitelný formát elektronického výkaznictví původně obsahoval prvky **List**, doporučujeme nastavit možnost **Vytvořit prvek formátu listu Excel** na **Ano** při importu aktualizované šablony. V opačném případě budou všechny vnořené prvky původního prvku **List** vytvořeny od začátku. Proto budou všechny vazby znovu vytvořených prvků formátu ztraceny v aktualizovaném formátu elektronického výkaznictví.

![Možnost Vytvořit prvek formátu listu Excel v dialogovém okně Aktualizovat z Excelu](./media/er-excel-format-update-template.png)

Chcete-li se o této funkci dozvědět více, postupujte podle pokynů v části [Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Ověření formátu elektronického výkaznictví

Při ověření formátu elektronického výkaznictví, který lze upravit, se provede kontrola konzistence, aby se zajistilo, že název Excel bude přítomen v aktuálně používané šabloně Excel. O jakýchkoli nesrovnalostech budete informováni. V případě některých nesrovnalostí bude nabídnuta možnost automaticky opravit problémy.

![Chybové zprávy ověření](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Řízení průběhu výpočtu vzorců aplikace Excel

Když je generován odchozí dokument ve formátu sešitu Microsoft Excel, některé buňky tohoto dokumentu mohou obsahovat vzorce aplikace Excel. Když je aktivována funkce **Povolit použití knihovny EPPlus v rámci elektronického výkaznictví**, můžete určit, kdy přesně se vzorce vypočítají, změnou hodnoty [parametru](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Možnosti výpočtu** v šabloně aplikace Excel, která se používá:

- Když vyberete hodnotu **Automaticky**, přepočítají se všechny závislé vzorce pokaždé, když je generovaný dokument připojen novými rozsahy, buňkami atd.
    >[!NOTE]
    > To může způsobit problém s výkonem šablon aplikace Excel, které obsahují více souvisejících vzorců.
- Když vyberete hodnotu **Ručně**, nebudou vzorce přepočítány při generování dokumentu.
    >[!NOTE]
    > Přepočet vzorce je vynucen ručně, když je generovaný dokument otevřen k náhledu v aplikaci Excel.
    > Tuto možnost nepoužívejte, pokud konfigurujete cíl ER, který předpokládá použití vygenerovaného dokumentu bez jeho náhledu v aplikaci Excel (pro převod PDF, odeslání e-mailem atd.), protože generovaný dokument nemusí obsahovat hodnoty v buňkách obsahujících vzorce.

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks\er-design-reports-openxml-2016-11.md)

[Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel](modify-electronic-reporting-format-reapply-excel-template.md)

[Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel](tasks/er-horizontal-1.md)

[Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md)

[Konfigurace elektronického výkaznictví pro doplňování dat do Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]