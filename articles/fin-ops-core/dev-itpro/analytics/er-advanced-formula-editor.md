---
title: Rozšířený editor vzorců elektronického výkaznictví
description: V tomto tématu je popsáno, jak lze pomocí rozšířeného editoru vzorců konfigurovat výrazy v mapování modelu a komponentách formátu elektronického výkaznictví.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270700"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="0d84a-103">Rozšířený editor vzorců elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0d84a-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d84a-104">Kromě [editoru vzorců](general-electronic-reporting.md) [elektronického výkaznictví](general-electronic-reporting-formula-designer.md) můžete použít rozšířený editoru vzorců elektronického výkaznictví ke zlepšení zkušenosti s konfigurací výrazů elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0d84a-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="0d84a-105">Rozšířený editor je založen na prohlížeči a využívá [editor Monaco](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="0d84a-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="0d84a-106">V tomto tématu jsou popsány nejčastěji používané funkce rozšířeného editoru:</span><span class="sxs-lookup"><span data-stu-id="0d84a-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="0d84a-107">Automatické formátování kódu</span><span class="sxs-lookup"><span data-stu-id="0d84a-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="0d84a-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="0d84a-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="0d84a-109">Dokončení kódu</span><span class="sxs-lookup"><span data-stu-id="0d84a-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="0d84a-110">Navigace kódem</span><span class="sxs-lookup"><span data-stu-id="0d84a-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="0d84a-111">Strukturování kódu</span><span class="sxs-lookup"><span data-stu-id="0d84a-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="0d84a-112">Najít a nahradit</span><span class="sxs-lookup"><span data-stu-id="0d84a-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="0d84a-113">Vkládání dat</span><span class="sxs-lookup"><span data-stu-id="0d84a-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="0d84a-114">Obarvení syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d84a-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="0d84a-115"><a name="ActivateAdvEditor">Aktivace rozšířeného editoru vzorců</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="0d84a-116">Chcete-li začít používat rozšířený editor vzorců v instanci aplikace Microsoft Dynamics 365 Finance, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="0d84a-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="0d84a-117">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="0d84a-118">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="0d84a-119">V dialogovém okně **Parametry uživatele** v části **Sledování provádění** nastavte parametr **Povolit rozšířený editor vzorců** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="0d84a-120">[![Dialogové okno Uživatelské parametry, zvýrazněný parametr Povolit rozšířený editor vzorců](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="0d84a-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="0d84a-121">Uvědomte si, že tento parametr je specifický pro uživatele a konkrétní společnost.</span><span class="sxs-lookup"><span data-stu-id="0d84a-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="0d84a-122">Počínaje verzí Microsoft Dynamics 365 Finance 10.0.19 můžete určovat, jaký editor vzorců ER je ve výchozím nastavení nabízen.</span><span class="sxs-lookup"><span data-stu-id="0d84a-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="0d84a-123">Pomocí následujících kroků povolíte rozšířený editor vzorců pro všechny uživatele a společnosti aktuální instance Finance.</span><span class="sxs-lookup"><span data-stu-id="0d84a-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="0d84a-124">Otevřete pracovní prostor **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="0d84a-125">Najděte a vyberte funkci **Nastavte rozšířený editor vzorců ER jako výchozí pro všechny uživatele** v seznamu a poté vyberte **Povolit hned**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="0d84a-126">Přejděte do části **Správa organizace** > **Elektronické výkaznictví** > **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="0d84a-127">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="0d84a-128">V dialogovém okně **Uživatelské parametry** vyhledejte parametr **Zakázat rozšířený editor vzorců** a ověřte, zda je nastaven na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="0d84a-129">[![Dialogové okno Uživatelské parametry, zvýrazněný parametr Zakázat rozšířený editor vzorců](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="0d84a-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="0d84a-130">Hodnoty parametrů **Povolit rozšířený editor vzorců** a **Zakázat rozšířený editor vzorců** jsou uchovávány odděleně pro každého uživatele a jsou nabízeny v dialogovém okně **Uživatelské parametry** v závislosti na stavu funkce **Nastavit rozšířený editor vzorců ER jako výchozí pro všechny uživatele**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="0d84a-131"><a name="Autoformatting">Automatické formátování kódu</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="0d84a-132">Při psaní složeného výrazu, který se skládá z více řádků kódu, bude odsazení nového řádku automaticky založeno na odsazení předchozího řádku.</span><span class="sxs-lookup"><span data-stu-id="0d84a-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="0d84a-133">Můžete vybrat řádky a změnit jejich odsazení zadáním **tabulátoru** nebo **SHIFT+TAB**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="0d84a-134">[![Gif editoru vzorců ER zobrazující výběr řádků a změnu odsazení](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="0d84a-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="0d84a-135">Automatické formátování umožňuje uchovat celý výraz správně naformátovaný, aby se usnadnila další údržba a aby se zjednodušilo pochopení konfigurované logiky.</span><span class="sxs-lookup"><span data-stu-id="0d84a-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="0d84a-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="0d84a-137">Editor poskytuje dokončování slova, které usnadňuje psaní výrazu a zamezení překlepů.</span><span class="sxs-lookup"><span data-stu-id="0d84a-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="0d84a-138">Když začnete přidávat nový text, editor automaticky nabídne seznam funkcí podporovaných ve funkcích elektronického výkaznictví, které obsahují zadané znaky.</span><span class="sxs-lookup"><span data-stu-id="0d84a-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="0d84a-139">IntelliSense lze aktivovat také v jakémkoli místě nakonfigurovaného výrazu zadáním **CTRL+mezerník**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="0d84a-140">[![Gif editoru vzorců ER zobrazující spouštění IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="0d84a-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="0d84a-141"><a name="CodeCompletion">Dokončení kódu</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="0d84a-142">Editor automaticky poskytuje dokončení kódu těmito způsoby:</span><span class="sxs-lookup"><span data-stu-id="0d84a-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="0d84a-143">Vložení uzavírací závorky při zadání počáteční závorky, se zachováním kurzoru uvnitř závorek.</span><span class="sxs-lookup"><span data-stu-id="0d84a-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="0d84a-144">Vložení symbolu druhé uvozovky při zadání první uvozovky, se zachováním kurzoru uvnitř uvozovek.</span><span class="sxs-lookup"><span data-stu-id="0d84a-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="0d84a-145">Vložení symbolu druhé dvojité uvozovky při zadání první uvozovky, se zachováním kurzoru uvnitř uvozovek.</span><span class="sxs-lookup"><span data-stu-id="0d84a-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="0d84a-146">[![GIF editoru vzorců ER zobrazující editor automaticky poskytující doplnění kódu](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="0d84a-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="0d84a-147">Když namíříte na zadanou závorku, druhá závorka tohoto páru se automaticky zvýrazní, aby se zobrazila konstrukce, kterou podporují.</span><span class="sxs-lookup"><span data-stu-id="0d84a-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="0d84a-148"><a name="CodeNavigation">Navigace kódem</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="0d84a-149">Požadované symboly nebo řádky ve výrazu můžete vyhledat zadáním příkazu **Go to** pomocí palety příkazů nebo kontextové nabídky.</span><span class="sxs-lookup"><span data-stu-id="0d84a-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="0d84a-150">Chcete-li například přejít na řádek **8**, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0d84a-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="0d84a-151">Stiskněte **Ctrl+G**, zadejte hodnotu **8** a stiskněte **ENTER**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="0d84a-152">- nebo -</span><span class="sxs-lookup"><span data-stu-id="0d84a-152">-or-</span></span>

- <span data-ttu-id="0d84a-153">Stiskněte **F1**, zadejte **G**, zvolte **Přejít na řádek**, zadejte hodnotu **8** a stiskněte **Enter**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="0d84a-154">[![Gif editoru vzorců ER, který ukazuje, jak vyhledat části výrazu pomocí palety příkazů](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="0d84a-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="0d84a-155"><a name="CodeStructuring">Strukturování kódu</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="0d84a-156">Kód pro některé funkce, například [IF](er-functions-logical-if.md) nebo [CASE](er-functions-logical-case.md), je automaticky strukturován.</span><span class="sxs-lookup"><span data-stu-id="0d84a-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="0d84a-157">Rozbalením a sbalením libovolných nebo všech rozkládacích oblastí tohoto kódu můžete omezit upravitelnou část výrazu, abyste se mohli zaměřit pouze na tu část kódu, která vyžaduje vaši pozornost.</span><span class="sxs-lookup"><span data-stu-id="0d84a-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="0d84a-158">Pro tuto možnost lze použít příkazy přeložit/rozbalit.</span><span class="sxs-lookup"><span data-stu-id="0d84a-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="0d84a-159">Chcete-li například přeložit všechny oblasti, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0d84a-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="0d84a-160">Stiskněte **CTRL+K**</span><span class="sxs-lookup"><span data-stu-id="0d84a-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="0d84a-161">- nebo -</span><span class="sxs-lookup"><span data-stu-id="0d84a-161">-or-</span></span>

- <span data-ttu-id="0d84a-162">Stiskněte **F1**, stiskněte **FO**, vyberte **Přeložit vše** a poté stiskněte **Enter**</span><span class="sxs-lookup"><span data-stu-id="0d84a-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="0d84a-163">Chcete-li rozbalit všechny oblasti, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0d84a-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="0d84a-164">Stiskněte **CTRL+J**</span><span class="sxs-lookup"><span data-stu-id="0d84a-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="0d84a-165">- nebo -</span><span class="sxs-lookup"><span data-stu-id="0d84a-165">-or-</span></span>
  
- <span data-ttu-id="0d84a-166">Stiskněte **F1**, zadejte **UN**, vyberte **Rozbalit vše** a poté stiskněte **Enter**</span><span class="sxs-lookup"><span data-stu-id="0d84a-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="0d84a-167">[![Gif editoru vzorců ER zobrazující rozbalování kódu](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="0d84a-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="0d84a-168"><a name="FindAndReplace">Najít a nahradit</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="0d84a-169">Chcete-li vyhledat výskyty určitého textu, vyberte text ve výrazu a proveďte následující akce:</span><span class="sxs-lookup"><span data-stu-id="0d84a-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="0d84a-170">Stisknutím **CTRL+F** a stiskněte **F3** pro vyhledání dalšího výskytu vybraného textu nebo stiskněte **Shift+F3** pro vyhledání předchozího výskytu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="0d84a-171">- nebo -</span><span class="sxs-lookup"><span data-stu-id="0d84a-171">-or-</span></span>
  
- <span data-ttu-id="0d84a-172">Stiskněte **F1**, zadejte **F** a poté vyberte požadovanou možnost pro vyhledání vybraného textu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="0d84a-173">Chcete-li nahradit výskyty určitého textu, vyberte text ve výrazu a proveďte následující akce:</span><span class="sxs-lookup"><span data-stu-id="0d84a-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="0d84a-174">Stiskněte **CTRL+H**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="0d84a-175">Zadejte alternativní text a výběrem možnosti nahrazení nahraďte vybraný text nebo všechny výskyty tohoto textu v aktuálním výrazu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="0d84a-176">- nebo -</span><span class="sxs-lookup"><span data-stu-id="0d84a-176">-or-</span></span>
  
- <span data-ttu-id="0d84a-177">Stiskněte **F1**, zadejte **R** a poté vyberte požadovanou možnost pro nahrazení vybraného textu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="0d84a-178">Zadejte alternativní text a výběrem možnosti nahrazení nahraďte vybraný text nebo všechny výskyty tohoto textu v aktuálním výrazu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="0d84a-179">Chcete-li změnit všechny výskyty určitého textu, vyberte text ve výrazu a proveďte následující akce:</span><span class="sxs-lookup"><span data-stu-id="0d84a-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="0d84a-180">Stiskněte **CTRL+ F2** a poté zadejte alternativní text.</span><span class="sxs-lookup"><span data-stu-id="0d84a-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="0d84a-181">- nebo -</span><span class="sxs-lookup"><span data-stu-id="0d84a-181">-or-</span></span>
  
- <span data-ttu-id="0d84a-182">Stiskněte **F1**, zadejte **C** a poté vyberte požadovanou možnost pro změnu vybraného textu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="0d84a-183">Zadejte alternativní text.</span><span class="sxs-lookup"><span data-stu-id="0d84a-183">Enter the alternative text.</span></span>

<span data-ttu-id="0d84a-184">[![Gif editoru vzorců ER zobrazující najít a nahradit](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="0d84a-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="0d84a-185"><a name="DataPasting">Vkládání datových zdrojů a funkcí</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="0d84a-186">Můžete vybrat možnost **Přidat datový zdroj**, která vloží do aktuálního výrazu zdroj dat, který je aktuálně vybrán v levém panelu **zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="0d84a-187">Podobně můžete vybrat možnost **Přidat funkci**, která vloží do aktuálního výrazu funkci, která je aktuálně vybrána v pravém panelu **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="0d84a-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="0d84a-188">Pokud použijete editor vzorce elektronického výkaznictví, bude vybraná funkce nebo vybraný zdroj dat vždy vložen na konec konfigurovaného výrazu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="0d84a-189">Pokud použijete rozšířený editor vzorce elektronického výkaznictví, vybranou funkci nebo vybraný zdroj dat lze vložit do jakékoliv části konfigurovaného výrazu.</span><span class="sxs-lookup"><span data-stu-id="0d84a-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="0d84a-190">Chcete-li určit, kam se mají data vložit, můžete použít kurzor.</span><span class="sxs-lookup"><span data-stu-id="0d84a-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="0d84a-191">[![Gif editoru vzorců ER zobrazující přidání zdroje dat a vložení funkce](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="0d84a-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="0d84a-192"><a name="SyntaxColorization">Obarvení syntaxe</a></span><span class="sxs-lookup"><span data-stu-id="0d84a-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="0d84a-193">V současné době se k zvýraznění následujících částí výrazů používají různé barvy:</span><span class="sxs-lookup"><span data-stu-id="0d84a-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="0d84a-194">Text v dvojitých závorkách, který může představovat ID popisku textové konstanty.</span><span class="sxs-lookup"><span data-stu-id="0d84a-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="0d84a-195">[![Editor vzorce elektronického výkaznictví](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="0d84a-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="0d84a-196">Omezení</span><span class="sxs-lookup"><span data-stu-id="0d84a-196">Limitations</span></span>

<span data-ttu-id="0d84a-197">Editor je aktuálně podporován v následujících webových prohlížečích:</span><span class="sxs-lookup"><span data-stu-id="0d84a-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="0d84a-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="0d84a-198">Chrome</span></span>
- <span data-ttu-id="0d84a-199">Edge</span><span class="sxs-lookup"><span data-stu-id="0d84a-199">Edge</span></span>
- <span data-ttu-id="0d84a-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="0d84a-200">Firefox</span></span>
- <span data-ttu-id="0d84a-201">Opera</span><span class="sxs-lookup"><span data-stu-id="0d84a-201">Opera</span></span>
- <span data-ttu-id="0d84a-202">Safari</span><span class="sxs-lookup"><span data-stu-id="0d84a-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d84a-203">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0d84a-203">Additional resources</span></span>

- [<span data-ttu-id="0d84a-204">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0d84a-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0d84a-205">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0d84a-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="0d84a-206">Editor Monaco</span><span class="sxs-lookup"><span data-stu-id="0d84a-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
