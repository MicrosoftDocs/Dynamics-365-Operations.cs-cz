---
title: Návrhář receptur v elektronickém výkaznictví
description: Tento článek obsahuje obecné informace o použití návrháře receptur v elektronickém výkaznictví (ER).
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 3620fa886fd4b609a0f1f08b2338ab725065efe7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287921"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Návrhář receptur v elektronickém výkaznictví

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak lze používat návrháře receptur v elektronickém výkaznictví. Při vytváření formátu pro určitý elektronický dokument pro elektronické výkaznictví můžete použít vzorce k převodu dat za účelem plnění požadavků na plnění a formátování daného dokumentu. Tyto vzorce připomínají vzorce aplikace Microsoft Excel. V recepturách jsou podporovány různé typy funkcí: text, datum a čas, matematika, logika, informace a převod datových typů , stejně jako další funkce specifické pro danou obchodní doménu.

## <a name="formula-designer-overview"></a>Přehled návrháře vzorců

Elektronické výkaznictví podporuje návrháře receptur. Proto můžete během návrhu konfigurovat výrazy, které lze použít pro následující úkoly za běhu:

- Transformujte data přijatá z databáze aplikace, která by měla být zadána do datového modelu elektronického výkaznictví navrženého jako datový zdroj pro formáty elektronického výkaznictví. (Tyto transformace mohou například zahrnovat filtrování, seskupení a převod typů dat.)
- Formátování dat, která musí být odeslána do generovaného elektronické dokument v souladu s rozvržením a podmínkami konkrétního formátu elektronického výkaznictví. (Formátování může být například provedeno v souladu s požadovaným jazykem, jazykovou verzí nebo kódováním).
- Kontrola procesu vytváření elektronických dokumentů. (Například výrazy mohou povolit nebo zakázat výstup konkrétních prvků formátu, v závislosti na zpracování dat. Mohou rovněž přerušit proces vytváření dokumentu nebo odesílat zprávy uživateli.)

Můžete otevřít stránku **Návrhář receptur** po provedení některé z následujících akcí:

- vazba položek zdroje dat na součásti datového modelu,
- vazba položek zdroje dat na součásti formátu,
- kompletní údržba vypočtených polí, která jsou součástí datových zdrojů.
- Definování podmínek viditelnosti a upravitelnosti pro vstupní parametry uživatele.
- Definování výchozích hodnot pro vstupní parametry uživatele.
- návrh transformací formátu,
- definování povolení podmínek pro součásti formátu,
- definování názvů souborů pro součásti souboru formátu,
- definování podmínek pro ověření kontroly procesu,
- definování textu zpráv pro ověření kontroly procesu.

## <a name="data-binding"></a><a name="Binding"></a>Datová vazba

Návrháře receptur elektronického výkaznictví lze použít k definování výrazu, který převádí data přijatá ze zdrojů dat, aby tato data bylo možné zadat v příjemci dat za běhu následujícícmi způsoby:

- Ze zdrojů dat aplikace a parametrů spuštění do datového modelu elektronického výkaznictví,
- z datového modelu elektronického výkaznictví do formátu elektronického výkaznictví,
- Ze zdrojů dat aplikace a parametrů spuštění do formátu elektronického výkaznictví,

Následující obrázek znázorňuje návrh výraz tohoto typu. V tomto příkladu výraz zaokrouhluje hodnotu pole **Intrastat.AmountMST** v tabulce Intrastat na dvě desetinná místa a vrací zaokrouhlenou hodnotu.

[![Výraz datové vazby.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Je možné použít následující obrázek, který znázorňuje návrh výrazu tohoto typu. V tomto příkladu je výsledek navrženého výrazu zadán do komponenty **Transaction.InvoicedAmount** datového modelu **Vykazování daně**.

[![Používaný výraz datové vazby.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Navržená receptura `ROUND (Intrastat.AmountMST, 2)` zaokrouhluje za běhu hodnotu pole **AmountMST** pro každý záznam v tabulce Intrastat na dvě desetinná místa. Poté zadá zaokrouhlenou hodnotu do komponenty **Transaction.InvoicedAmount** datového modelu **Vykazování daně**.

## <a name="data-formatting"></a><a name="Transformation"></a>Formátování dat

Návrháře receptur elektronického výkaznictví lze použít k definování výrazu, který naformátuje data přijatá ze zdrojů dat, aby tato data bylo možné odeslat jako součást generovaného elektronického dokumentu: Můžete mít formátování, které je třeba použít jako typické pravidlo, které by mělo být znovu použito pro formát. V takovém případě můžete uvést toto formátování jednou v konfiguraci formátu jako pojmenovanou transformaci, která má výraz formátování. Tuto pojmenovanou transformaci lze potom propojit s mnoha komponentami formátu, kde výstup musí být formátován podle vytvořeného výrazu formátování.

Následující obrázek znázorňuje návrh transformace tohoto typu. V tomto příkladu ořeže transformace **TrimmedString** vstupní data typu dat *Řetězec* odstraněním počáteční a koncové mezery. Vrátí hodnotu oříznutého řetězce.

[![Transformace.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Je možné použít následující obrázek, který znázorňuje návrh transformace tohoto typu. V tomto příkladu více součástí formátu odesílá text jako výstup do generovaného elektrického dokumentu za běhu. Všechny tyto součásti formátu odkazují na transofmraci **TrimmedString** podle názvu.

[![Použitá transformace.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Když součásti formátu, jako je například součást **partyName** na předchozím obrázku, odkazují na transformaci **TrimmedString**, transformace odešle text jako výstup generovaného elektronického dokumentu. Tento text nezahrnuje počáteční a koncové mezery.

Pokud máte formátování, které je nutné použít jednotlivě, můžete toto formátování použít jako jednotlivý výraz vazby konkrétní součásti formátu. Následující obrázek znázorňuje výraz tohoto typu. V tomto příkladu je součást formátu **partyType** vázána na zdroj dat pomocí výrazu, který převede příchozí data z pole **Model.Company.RegistrationType** ve zdroji dat na text s velkými písmeny. Výraz pak odešle tento text jako výstup do elektronického dokumentu.

[![Použití formátování na jednotlivou součást.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Kontrola procesního toku

Návrháře receptur elektronického výkaznictví lze použít k definování výrazů, které se používají k řízení toku procesu generovaných elektronických dokumentů. K dispozici jsou tyto úlohy:

- Definujte podmínky určující, kdy musí být zastaven proces vytvoření dokumentu.
- Zadejte výrazy, které vytvoří zprávy pro uživatele o zastaveném procesu nebo vyvolají spuštění zpráv protokolu o pokračujícím procesu generování sestav.
- Zadejte názvy souborů generovaných elektronických dokumentů a řiďte podmínky jejich vytvoření.

Každé pravidlo procesu řízení toku je navržen jako jednotlivé ověření. Následující obrázek znázorňuje ověření tohoto typu. Zde je vysvětlení konfigurace v tomto příkladu:

- Ověření je vyhodnoceno, když je uzel **INSTAT** vytvořen během generování souboru XML.
- Pokud je seznam transakcí prázdný, ověření zastaví proces spouštění a vrátí hodnotu **FALSE**.
- Ověření vrátí chybovou zpráva, která obsahuje textu popisku 70894 v upřednostňovaném jazyce uživatele.

[![Ověření.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

Návrhář receptur elektronického výkaznictví lze také použít k vygenerování názvu souboru pro generovaný elektronický dokument a kontrolu procesu vytvoření souboru. Následující obrázek znázorňuje návrh kontroly procesního toku tohoto typu. Zde je vysvětlení konfigurace v tomto příkladu:

- Seznam záznamů z datového zdroje **model.Intrastat** je rozdělen do dávek. Každá dávka obsahuje až 1 000 záznamů.
- Výstup vytvoří soubor ZIP, který obsahuje jeden soubor ve formátu XML pro každou dávku, která byla vytvořena.
- Výraz vrátí název souboru pro generované elektronické dokumenty zřetězením názvu a přípony souboru. Pro druhou dávku a všechny následné dávky obsahuje název souboru ID dávky jako příponu.
- Výraz umožňuje (vrácením hodnoty **TRUE**) proces vytváření souborů pro dávky, které obsahují alespoň jeden záznam.

[![Kontrola procesního toku.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Řízení obsahu dokumentů

Návrhář receptur elektronického výkaznictví lze použít ke konfiguraci výrazů, které určují, která data budou vložena do generovaných elektronických dokumentů za běhu. Tyto výrazy mohou povolit nebo zakázat výstup konkrétních prvků formátu, v závislosti na zpracování dat a konfigurované logice. Tyto výrazy lze zadat pro jediný prvek formátu v poli **Povoleno** na kartě **Mapování** na stránce **Návrhář operací**. Výrazy můžete zadat jako logickou podmínku, která vrátí *logickou* hodnotu:

- Pokud podmínka vrátí hodnotu **True**, je spuštěn aktuální prvek formátu.
- Pokud podmínka vrátí hodnotu **False**, aktuální prvek formátu je přeskočen.

Následující obrázek znázorňuje výraz tohoto typu. (Jako příklad použijeme verzi 11.12.11 konfigurace formátu **ISO20022 Credit transfer (NO)**, která je poskytována společností Microsoft.) Součást formátu **XMLheader** je nakonfigurována tak, aby popisovala strukturu zprávy o peněžním převodu podle standardů zpráv ISO 20022 XML. Součást formátu **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** je konfigurována pro přidání prvku XML **Ustrd** do generované zprávy a vložení informací o úhradě v nestrukturovaném formátu jako textu následujících prvků XML:

- Součást **PaymentNotes** slouží ke generování textu poznámek k platbě.
- Součást **DelimitedSequence** generuje čísla faktur oddělená čárkou, která slouží k vyrovnání aktuálního peněžního převodu.

[![Součásti PaymentNotes a DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Součásti **PaymentNotes** a **DelimitedSequence** jsou označeny otazníkem. Otazník označuje, že použití součásti je podmíněné. V tomto případě je použití součástí založeno na následujících kritériích:
>
> - Výraz `@.PaymentsNotes <> ""` definovaný pro součást **PaymentNotes** umožňuje (vrácením hodnoty **TRUE**) naplnění prvku XML **Ustrd** textem poznámek k platbám, když tento text pro aktuální peněžní převod není prázdný.
>
>    [![Výraz pro součást PaymentNotes.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Výraz `@.PaymentsNotes = ""` definovaný pro součást **DelimitedSequence** umožňuje (vrácením hodnoty **TRUE**) naplnění prvku XML **Ustrd** seznamem čísel faktur oddělených čárkami, které jsou použity k účtování aktuálního peněžního převodu v případě, že text platby poznámek k platbám k tomuto peněžnímu převodu je prázdný.
>
>    [![Výraz pro součást DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> V závislosti na tomto nastavení bude generovaná zpráva pro každou platbu dlužníka – prvek XML **Ustrd** – obsahovat buď text poznámek k platbě, nebo, je-li tento text prázdný, seznam čárkami oddělených čísel faktur použitých k účtování této platby.

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Ověření konfigurovaných receptur

Na stránce **návrháře receptur** vyberte **Test** pro ověření, jak funguje nakonfigurovaná receptura.

[![Výběr testu pro ověření receptury.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Pokud jsou požadovány hodnoty argumentů receptury, můžete otevřít dialogové okno **Testovat výraz** ze stránky **návrháře receptur**. Ve většině případů je nutné tyto argumenty ručně definovat, protože nakonfigurované vazby nejsou spuštěny v době návrhu. Na kartě **Výsledek testu** na stránce **návrháře receptur** se zobrazí výsledek spuštění nakonfigurované receptury.

Následující příklad ukazuje, jak lze otestovat recepturu nakonfigurovanou pro doménu zahraničního obchodu, aby bylo jisté, že kód komodity Intrastat obsahuje pouze číslice.

Při testování této receptury můžete použít dialogové okno **Testovat výraz** k určení hodnoty kódu komodity Intrastat pro testování.

[![Určení kódu komodity Intrastat pro testování.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Po zadání kódu komodity Intrastat a výběru možnosti **OK** zobrazí karta **Výsledek testování** na stránce **návrháře receptur** výsledek provedení nakonfigurované receptury. Poté můžete vyhodnotit, zda je výsledek přijatelný. Pokud výsledek není přijatelný, můžete recepturu aktualizovat a znovu ji otestovat.

[![Výsledek testu.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Některé receptury nelze testovat v době návrhu. Receptura může například vrátit výsledek datového typu, který nelze zobrazit na kartě **Výsledek testu**. V tomto případě se zobrazí chybová zpráva oznamující, že recepturu nelze testovat.

[![Chybová zpráva.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
