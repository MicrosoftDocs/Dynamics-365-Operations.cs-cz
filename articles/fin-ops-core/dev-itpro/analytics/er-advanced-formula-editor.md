---
title: Rozšířený editor vzorců elektronického výkaznictví
description: V tomto článku je popsáno, jak lze pomocí rozšířeného editoru vzorců konfigurovat výrazy v mapování modelu a komponentách formátu elektronického výkaznictví.
author: kfend
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
ms.openlocfilehash: 269102028962cf1ebae599b9885f97871785a551
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286210"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Rozšířený editor vzorců elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Kromě [editoru vzorců](general-electronic-reporting.md) [elektronického výkaznictví](general-electronic-reporting-formula-designer.md) můžete použít rozšířený editoru vzorců elektronického výkaznictví ke zlepšení zkušenosti s konfigurací výrazů elektronického výkaznictví. Rozšířený editor je založen na prohlížeči a využívá [editor Monaco](https://microsoft.github.io/monaco-editor). V tomto článku jsou popsány nejčastěji používané funkce rozšířeného editoru:

- [Automatické formátování kódu](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Dokončení kódu](#CodeCompletion)
- [Navigace kódem](#CodeNavigation)
- [Strukturování kódu](#CodeStructuring)
- [Najít a nahradit](#FindAndReplace)
- [Vkládání dat](#DataPasting)
- [Obarvení syntaxe](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Aktivace rozšířeného editoru vzorců</a>

Chcete-li začít používat rozšířený editor vzorců v instanci aplikace Microsoft Dynamics 365 Finance, postupujte podle následujících kroků.

1.  Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2.  Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3.  V dialogovém okně **Parametry uživatele** v části **Sledování provádění** nastavte parametr **Povolit rozšířený editor vzorců** na **Ano**.

[![Dialogové okno Uživatelské parametry, zvýrazněný parametr Povolit rozšířený editor vzorců.](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Uvědomte si, že tento parametr je specifický pro uživatele a konkrétní společnost.

Počínaje verzí Microsoft Dynamics 365 Finance 10.0.19 můžete určovat, jaký editor vzorců ER je ve výchozím nastavení nabízen. Pomocí následujících kroků povolíte rozšířený editor vzorců pro všechny uživatele a společnosti aktuální instance Finance.

1.  Otevřete pracovní prostor **Správa funkcí**.
2.  Najděte a vyberte funkci **Nastavte rozšířený editor vzorců ER jako výchozí pro všechny uživatele** v seznamu a poté vyberte **Povolit hned**.
3.  Přejděte do části **Správa organizace** > **Elektronické výkaznictví** > **Konfigurace**.
4.  Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
5.  V dialogovém okně **Uživatelské parametry** vyhledejte parametr **Zakázat rozšířený editor vzorců** a ověřte, zda je nastaven na **Ne**.

[![Dialogové okno Uživatelské parametry, zvýrazněný parametr Zakázat rozšířený editor vzorců.](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> Hodnoty parametrů **Povolit rozšířený editor vzorců** a **Zakázat rozšířený editor vzorců** jsou uchovávány odděleně pro každého uživatele a jsou nabízeny v dialogovém okně **Uživatelské parametry** v závislosti na stavu funkce **Nastavit rozšířený editor vzorců ER jako výchozí pro všechny uživatele**.

## <a name=""></a><a name="Autoformatting">Automatické formátování kódu</a>

Při psaní složeného výrazu, který se skládá z více řádků kódu, bude odsazení nového řádku automaticky založeno na odsazení předchozího řádku. Můžete vybrat řádky a změnit jejich odsazení zadáním **tabulátoru** nebo **SHIFT+TAB**.

[![Gif editoru vzorců ER zobrazující výběr řádků a změnu odsazení.](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Automatické formátování umožňuje uchovat celý výraz správně naformátovaný, aby se usnadnila další údržba a aby se zjednodušilo pochopení konfigurované logiky.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Editor poskytuje dokončování slova, které usnadňuje psaní výrazu a zamezení překlepů. Když začnete přidávat nový text, editor automaticky nabídne seznam funkcí podporovaných ve funkcích elektronického výkaznictví, které obsahují zadané znaky. IntelliSense lze aktivovat také v jakémkoli místě nakonfigurovaného výrazu zadáním **CTRL+mezerník**.

[![Gif editoru vzorců ER zobrazující spouštění IntelliSense.](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Dokončení kódu</a>

Editor automaticky poskytuje dokončení kódu těmito způsoby:

- Vložení uzavírací závorky při zadání počáteční závorky, se zachováním kurzoru uvnitř závorek.
- Vložení symbolu druhé uvozovky při zadání první uvozovky, se zachováním kurzoru uvnitř uvozovek.
- Vložení symbolu druhé dvojité uvozovky při zadání první uvozovky, se zachováním kurzoru uvnitř uvozovek.

[![GIF editoru vzorců ER zobrazující editor automaticky poskytující doplnění kódu.](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Když namíříte na zadanou závorku, druhá závorka tohoto páru se automaticky zvýrazní, aby se zobrazila konstrukce, kterou podporují.

## <a name=""></a><a name="CodeNavigation">Navigace kódem</a>

Požadované symboly nebo řádky ve výrazu můžete vyhledat zadáním příkazu **Go to** pomocí palety příkazů nebo kontextové nabídky.

Chcete-li například přejít na řádek **8**, postupujte takto:

- Stiskněte **Ctrl+G**, zadejte hodnotu **8** a stiskněte **ENTER**.

  - nebo -

- Stiskněte **F1**, zadejte **G**, zvolte **Přejít na řádek**, zadejte hodnotu **8** a stiskněte **Enter**.

[![Gif editoru vzorců ER, který ukazuje, jak vyhledat části výrazu pomocí palety příkazů.](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Strukturování kódu</a>

Kód pro některé funkce, například [IF](er-functions-logical-if.md) nebo [CASE](er-functions-logical-case.md), je automaticky strukturován. Rozbalením a sbalením libovolných nebo všech rozkládacích oblastí tohoto kódu můžete omezit upravitelnou část výrazu, abyste se mohli zaměřit pouze na tu část kódu, která vyžaduje vaši pozornost. Pro tuto možnost lze použít příkazy přeložit/rozbalit.

Chcete-li například přeložit všechny oblasti, postupujte takto:

- Stiskněte **CTRL+K**

  - nebo -

- Stiskněte **F1**, stiskněte **FO**, vyberte **Přeložit vše** a poté stiskněte **Enter**

Chcete-li rozbalit všechny oblasti, postupujte takto:

- Stiskněte **CTRL+J**

  - nebo -
  
- Stiskněte **F1**, zadejte **UN**, vyberte **Rozbalit vše** a poté stiskněte **Enter**

[![Gif editoru vzorců ER zobrazující rozbalování kódu.](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Najít a nahradit</a>

Chcete-li vyhledat výskyty určitého textu, vyberte text ve výrazu a proveďte následující akce:

- Stisknutím **CTRL+F** a stiskněte **F3** pro vyhledání dalšího výskytu vybraného textu nebo stiskněte **Shift+F3** pro vyhledání předchozího výskytu.

  - nebo -
  
- Stiskněte **F1**, zadejte **F** a poté vyberte požadovanou možnost pro vyhledání vybraného textu.

Chcete-li nahradit výskyty určitého textu, vyberte text ve výrazu a proveďte následující akce:

- Stiskněte **CTRL+H**. Zadejte alternativní text a výběrem možnosti nahrazení nahraďte vybraný text nebo všechny výskyty tohoto textu v aktuálním výrazu.

  - nebo -
  
- Stiskněte **F1**, zadejte **R** a poté vyberte požadovanou možnost pro nahrazení vybraného textu. Zadejte alternativní text a výběrem možnosti nahrazení nahraďte vybraný text nebo všechny výskyty tohoto textu v aktuálním výrazu.

Chcete-li změnit všechny výskyty určitého textu, vyberte text ve výrazu a proveďte následující akce:

- Stiskněte **CTRL+ F2** a poté zadejte alternativní text.

  - nebo -
  
- Stiskněte **F1**, zadejte **C** a poté vyberte požadovanou možnost pro změnu vybraného textu. Zadejte alternativní text.

[![Gif editoru vzorců ER zobrazující najít a nahradit.](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Vkládání datových zdrojů a funkcí</a>

Můžete vybrat možnost **Přidat datový zdroj**, která vloží do aktuálního výrazu zdroj dat, který je aktuálně vybrán v levém panelu **zdroje dat**. Podobně můžete vybrat možnost **Přidat funkci**, která vloží do aktuálního výrazu funkci, která je aktuálně vybrána v pravém panelu **Funkce**. Pokud použijete editor vzorce elektronického výkaznictví, bude vybraná funkce nebo vybraný zdroj dat vždy vložen na konec konfigurovaného výrazu. Pokud použijete rozšířený editor vzorce elektronického výkaznictví, vybranou funkci nebo vybraný zdroj dat lze vložit do jakékoliv části konfigurovaného výrazu. Chcete-li určit, kam se mají data vložit, můžete použít kurzor.

[![Gif editoru vzorců ER zobrazující přidání zdroje dat a vložení funkce.](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Obarvení syntaxe</a>

V současné době se k zvýraznění následujících částí výrazů používají různé barvy:

- Text v dvojitých závorkách, který může představovat ID popisku textové konstanty.

[![Editor vzorce elektronického výkaznictví.](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Omezení

Editor je aktuálně podporován v následujících webových prohlížečích:

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)
- [Editor Monaco](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
