---
title: Záznamník úloh a nápověda pro Retail Modern POS (MPOS) a Cloud POS
description: Toto téma popisuje, jak používat záznamník úloh v aplikacích Retail Modern POS (MPOS) a Cloud POS.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: aa892f4335d9b1aeee62f5571ee36601cab031cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220406"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="18a56-103">Záznamník úloh a nápověda pro Retail Modern POS (MPOS) a Cloud POS</span><span class="sxs-lookup"><span data-stu-id="18a56-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18a56-104">Toto téma popisuje, jak používat záznamník úloh v aplikacích Retail Modern POS (MPOS) a Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="18a56-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="18a56-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="18a56-105">Overview</span></span>

<span data-ttu-id="18a56-106">Záznamník úloh v Retail Modern POS nebo Cloud POS je nové řešení, které nabízí vysokou míru odezvy.</span><span class="sxs-lookup"><span data-stu-id="18a56-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="18a56-107">Poskytuje flexibilní aplikační programovací rozhraní (API) pro rozšíření a plynulou integraci se spotřebiteli záznamů obchodních procesů.</span><span class="sxs-lookup"><span data-stu-id="18a56-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="18a56-108">Integrace Záznamníku úloh s nástrojem Modelování podnikových procesů (BPM) ve službě Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) se posunula kupředu.</span><span class="sxs-lookup"><span data-stu-id="18a56-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="18a56-109">Proto mohou uživatelé dále vytvářet diagramy pro bohaté obchodní procesy ze záznamů pro analýzu a návrh aplikací.</span><span class="sxs-lookup"><span data-stu-id="18a56-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="18a56-110">Architektura</span><span class="sxs-lookup"><span data-stu-id="18a56-110">Architecture</span></span>

<span data-ttu-id="18a56-111">Záznamník úkolů může zaznamenávat akce uživatele v klientovi s přesnou věrností.</span><span class="sxs-lookup"><span data-stu-id="18a56-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="18a56-112">Každý ovládací prvek je laděný tak, aby upozornil Záznamník úloh o provedení akce uživatele.</span><span class="sxs-lookup"><span data-stu-id="18a56-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="18a56-113">Ovládací prvek oznámí Záznamníku úloh, že došlo k události, a předá všechny příslušné informace o odpovídající akci uživatele v reálném čase.</span><span class="sxs-lookup"><span data-stu-id="18a56-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="18a56-114">Z těchto informací může Záznamník úloh zaznamenat typ akce uživatele (například kliknutí na tlačítko, zadání hodnoty nebo navigace) a veškerá data, která souvisí s akcí uživatele (například hodnota a typ vstupních dat, kontext formuláře nebo kontext záznamu).</span><span class="sxs-lookup"><span data-stu-id="18a56-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="18a56-115">Záznamník úloh zachovává informace s dostatkem detailů k zajištění, že přehrávání nahrávky může provést nahrané akce přímo v pořadí, v jakém je uživatel provedl.</span><span class="sxs-lookup"><span data-stu-id="18a56-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="18a56-116">(Přehrávání funkce není dosud implementováno v Retail modern POS nebo Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="18a56-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="18a56-117">Základní konfigurace</span><span class="sxs-lookup"><span data-stu-id="18a56-117">Basic configuration</span></span>

<span data-ttu-id="18a56-118">Pokud chcete zapnout nahrávání úloh v systému POS, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="18a56-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="18a56-119">Klikněte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Registry**.</span><span class="sxs-lookup"><span data-stu-id="18a56-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="18a56-120">Klepněte na registr, pokud chcete povolit záznam úlohy.</span><span class="sxs-lookup"><span data-stu-id="18a56-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="18a56-121">Na kartě **Registr** na pevné záložce **Obecné** nastavte možnost **Povolit záznam úloh** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="18a56-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="18a56-122">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="18a56-122">Click **Save**.</span></span>
5. <span data-ttu-id="18a56-123">Přejděte na **Retail and Commerce** &gt; **IT pro Retail and Commerce** &gt; **Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="18a56-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="18a56-124">Vyberte úlohu **Registry (1090)** a klikněte na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="18a56-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="18a56-125">Vytvoření záznamu</span><span class="sxs-lookup"><span data-stu-id="18a56-125">Create a recording</span></span>

<span data-ttu-id="18a56-126">Tento postup slouží k vytvoření nového záznamu pomocí Záznamníku úloh.</span><span class="sxs-lookup"><span data-stu-id="18a56-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="18a56-127">Spusťte Retail Modern POS nebo Cloud POS a přihlaste se.</span><span class="sxs-lookup"><span data-stu-id="18a56-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="18a56-128">Na stránce **Nastavení** v části **Záznamník úloh** klikněte na **Otevřít záznamník úloh**.</span><span class="sxs-lookup"><span data-stu-id="18a56-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="18a56-129">Otevře se podokno **Záznamníku úloh**.</span><span class="sxs-lookup"><span data-stu-id="18a56-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="18a56-130">Můžete kliknout na tlačítko **Zavřít** (**X**) v pravém horním rohu pro zavření podokna **Záznamník úkolů** před zahájením nového záznamu.</span><span class="sxs-lookup"><span data-stu-id="18a56-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="18a56-131">K opětovnému otevření podokna zopakujte krok 2.</span><span class="sxs-lookup"><span data-stu-id="18a56-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="18a56-132">[![Podokno Záznamník úloh](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="18a56-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="18a56-133">Zadejte jméno a popis pro nahrávky a poté klepněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="18a56-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="18a56-134">Relace záznamu začne hned po klepnutí na tlačítko **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="18a56-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="18a56-135">Pokud kliknete na tlačítko **Zavřít** (**X**) v pravém horním rohu v době, kdy probíhá nahrávání, podokno **Záznamník úloh** se zavře, ale relace nahrávání se neukončí.</span><span class="sxs-lookup"><span data-stu-id="18a56-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="18a56-136">K opětovnému otevření podokna Záznamník úkolů klepněte na tlačítko **Nápověda** (otazník) v horní části obrazovky.</span><span class="sxs-lookup"><span data-stu-id="18a56-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="18a56-137">[![Otazník](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="18a56-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="18a56-138">Po kliknutí na tlačítko **Spustit** záznamník úloh přejde do režimu nahrávání.</span><span class="sxs-lookup"><span data-stu-id="18a56-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="18a56-139">V podokně **Záznamník úloh** se zobrazují informace a ovládací prvky, které se vztahují k procesu záznamu.</span><span class="sxs-lookup"><span data-stu-id="18a56-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="18a56-140">Proveďte akce, které chcete provést v uživatelském rozhraní Retail Modern POS nebo Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="18a56-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="18a56-141">Pokud chcete záznam zastavit, klikněte na **Stop**.</span><span class="sxs-lookup"><span data-stu-id="18a56-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="18a56-142">Možnosti stahování</span><span class="sxs-lookup"><span data-stu-id="18a56-142">Download options</span></span>

<span data-ttu-id="18a56-143">Po ukončení relace záznamu se zobrazuje několik možností tak, abyste si mohli stáhnout záznam.</span><span class="sxs-lookup"><span data-stu-id="18a56-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="18a56-144">[![Možnosti stahování](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="18a56-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="18a56-145">Uložit do tohoto počítače</span><span class="sxs-lookup"><span data-stu-id="18a56-145">Save to this PC</span></span>

<span data-ttu-id="18a56-146">K přehrání Průvodce záznamem úloh, správě nahrávky nebo úpravě anotací v nahrávce můžete použít balíček nahrávky.</span><span class="sxs-lookup"><span data-stu-id="18a56-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="18a56-147">(Tato funkce není dosud implementována v Retail Modern POS nebo Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="18a56-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="18a56-148">Exportovat jako dokument aplikace Word</span><span class="sxs-lookup"><span data-stu-id="18a56-148">Export as Word document</span></span>

<span data-ttu-id="18a56-149">Nahrávku můžete uložit jako dokument Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="18a56-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="18a56-150">Dokument bude obsahovat zaznamenané kroky a snímky obrazovky, které byly zaznamenány.</span><span class="sxs-lookup"><span data-stu-id="18a56-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="18a56-151">Uložit jako vývojářský záznam</span><span class="sxs-lookup"><span data-stu-id="18a56-151">Save as developer recording</span></span>

<span data-ttu-id="18a56-152">Nezpracovaný soubor záznamu je užitečný pro scénáře vývojářů, jako je generování testovacího kódu.</span><span class="sxs-lookup"><span data-stu-id="18a56-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="18a56-153">(Tato funkce není dosud implementována.)</span><span class="sxs-lookup"><span data-stu-id="18a56-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="18a56-154">Ovládací prvky pro záznam</span><span class="sxs-lookup"><span data-stu-id="18a56-154">Recording controls</span></span>

<span data-ttu-id="18a56-155">[![Ovládací prvky pro záznam](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="18a56-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="18a56-156">Zastavit</span><span class="sxs-lookup"><span data-stu-id="18a56-156">Stop</span></span>

<span data-ttu-id="18a56-157">Pokud chcete relaci záznamu zastavit, klikněte na **Stop**.</span><span class="sxs-lookup"><span data-stu-id="18a56-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="18a56-158">Poznámka: Relaci po dokončení nelze restartovat.</span><span class="sxs-lookup"><span data-stu-id="18a56-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="18a56-159">Proto ověřte, že záznam bude dokončen před ukončením.</span><span class="sxs-lookup"><span data-stu-id="18a56-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="18a56-160">Pozastavit</span><span class="sxs-lookup"><span data-stu-id="18a56-160">Pause</span></span>

<span data-ttu-id="18a56-161">Klepněte na tlačítko **Pozastavit** pro dočasné ukončení relace záznamu a pokračování v operaci.</span><span class="sxs-lookup"><span data-stu-id="18a56-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="18a56-162">Kroky provedené po kliknutí na **Pozastavit** se nezaznamenají.</span><span class="sxs-lookup"><span data-stu-id="18a56-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="18a56-163">Pokračovat</span><span class="sxs-lookup"><span data-stu-id="18a56-163">Continue</span></span>

<span data-ttu-id="18a56-164">Pokud chcete záznam po pozastavení obnovit, klikněte na **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="18a56-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="18a56-165">Pořídit snímky obrazovky</span><span class="sxs-lookup"><span data-stu-id="18a56-165">Capture screenshots</span></span>

<span data-ttu-id="18a56-166">Záznamník úkolů může zaznamenat snímky obrazovky uživatelského rozhraní Retail Modern POS při zaznamenávání obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="18a56-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="18a56-167">Chcete-li aktivovat funkci pořízení snímku obrazovky, nastavte možnost **Zachytit obrazovku** na **Ano** a poté proveďte záznam.</span><span class="sxs-lookup"><span data-stu-id="18a56-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="18a56-168">Po ukončení záznamu klikněte na tlačítko **Zastavit** a stáhněte dokument aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="18a56-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="18a56-169">Dokument bude obsahovat kroky s příslušnými snímky obrazovky.</span><span class="sxs-lookup"><span data-stu-id="18a56-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="18a56-170">Funkce zachycení obrazovky není podporována v prostředí Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="18a56-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="18a56-171">Počáteční a koncový úkol</span><span class="sxs-lookup"><span data-stu-id="18a56-171">Start task and End task</span></span>

<span data-ttu-id="18a56-172">Začátek a konec sady seskupených kroků můžete určit pomocí tlačítka **Počáteční úkol** a **Koncový** **úkol**.</span><span class="sxs-lookup"><span data-stu-id="18a56-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="18a56-173">Kliknutím na **Počáteční úkol** přidáte krok Počáteční úkol. Potom proveďte kroky, které mají být zahrnuty ve skupině.</span><span class="sxs-lookup"><span data-stu-id="18a56-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="18a56-174">Po dokončení kroků skupiny klepněte na tlačítko **Koncový úkol**.</span><span class="sxs-lookup"><span data-stu-id="18a56-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="18a56-175">Úlohy pomáhají uspořádat vaše postupy.</span><span class="sxs-lookup"><span data-stu-id="18a56-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="18a56-176">Mohou být vnořeny v jiných úkolech.</span><span class="sxs-lookup"><span data-stu-id="18a56-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="18a56-177">Tímto způsobem můžete lépe uspořádat příliš dlouhé a složité obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="18a56-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="18a56-178">Přidání poznámek</span><span class="sxs-lookup"><span data-stu-id="18a56-178">Adding annotations</span></span>

<span data-ttu-id="18a56-179">Poznámka je doplňkový text, který přidáváte do kroku v záznamu.</span><span class="sxs-lookup"><span data-stu-id="18a56-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="18a56-180">Můžete například použít poznámky k poskytnutí uživateli dalšího kontextu nebo pokynů.</span><span class="sxs-lookup"><span data-stu-id="18a56-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="18a56-181">Můžete přidat poznámky před nebo za krok.</span><span class="sxs-lookup"><span data-stu-id="18a56-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="18a56-182">Můžete přidat poznámky k jakémkoli kroku klepnutím na tlačítko **Upravit** (symbol tužky) napravo od kroku.</span><span class="sxs-lookup"><span data-stu-id="18a56-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="18a56-183">[![Tlačítko Upravit u kroku](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="18a56-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="18a56-184">Texty a poznámky</span><span class="sxs-lookup"><span data-stu-id="18a56-184">Texts and notes</span></span>

<span data-ttu-id="18a56-185">V polích **Texty** a **Poznámky** můžete přidat text, který by měl být přidružený ke kroku v Průvodci záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="18a56-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="18a56-186">[![Pole Text a Poznámky](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="18a56-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="18a56-187">Text</span><span class="sxs-lookup"><span data-stu-id="18a56-187">Text</span></span>

<span data-ttu-id="18a56-188">Text, který zadáte do pole **Text**, se zobrazí *nad* krokem v Průvodci záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="18a56-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="18a56-189">Toto místo je vhodné pro text, který si má uživatel přečíst před dokončením kroku.</span><span class="sxs-lookup"><span data-stu-id="18a56-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="18a56-190">Poznámky</span><span class="sxs-lookup"><span data-stu-id="18a56-190">Notes</span></span>

<span data-ttu-id="18a56-191">Text, který zadáte do pole **Poznámky**, se zobrazí *pod* krokem v Průvodci záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="18a56-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="18a56-192">Aby si uživatel mohl přečíst text poznámky, musí rozbalit text kroku v místním okně.</span><span class="sxs-lookup"><span data-stu-id="18a56-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="18a56-193">Toto umístění je vhodné pro volitelný materiál ke čtení nebo další informace, které mohou být pro uživatele užitečné, ale uživatel je nevyžaduje pro dokončení akce.</span><span class="sxs-lookup"><span data-stu-id="18a56-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="18a56-194">Nápověda v Retail Modern POS a Cloud POS</span><span class="sxs-lookup"><span data-stu-id="18a56-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="18a56-195">Chcete-li zobrazovat vlastní záznamy úkolů v podokně nápovědy pro Retail Modern POS a Cloud POS, aby je bylo možné přehrát jako průvodce úkolem nebo zobrazit jako text, je třeba záznamy úkolů uložit do vlastní knihovny BPM a poté aktualizovat systémové parametry nápovědy tak, aby odkazovaly na knihovnu BPM.</span><span class="sxs-lookup"><span data-stu-id="18a56-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="18a56-196">Další informace naleznete v tématu [Připojení systému nápovědy](../fin-and-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="18a56-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="18a56-197">Nápověda pro Retail Modern POS a Cloud POS prohlledává LCS v reálném čase.</span><span class="sxs-lookup"><span data-stu-id="18a56-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="18a56-198">Vyhledává ve všech knihovnách BPM, které jsou vybrány v parametrech systému nápovědy aplikace Commerce, a zobrazí příslušné výsledky.</span><span class="sxs-lookup"><span data-stu-id="18a56-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="18a56-199">Pro přístup do nabídky **Nápověda** klikněte na tlačítko **Nápověda** (otazník) v horní části obrazovky a do vyhledávacího pole napište název procesu. Potom klikněte na tlačítko pro vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="18a56-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="18a56-200">[![Tlačítko Nápověda](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="18a56-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="18a56-201">Po kliknutí na Průvodce záznamem úloh ve výsledcích vyhledávání můžete zobrazit kroky jako téma nápovědy nebo kroky exportovat do wordového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="18a56-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="18a56-202">V nápovědě pro Retail Retail Modern POS a Cloud POS se nezobrazují průvodci záznamem úloh v závislosti na tom, v jakém jste formuláři nebo jakou provádíte operaci.</span><span class="sxs-lookup"><span data-stu-id="18a56-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="18a56-203">Je nutné v poli pro vyhledávání zadat název procesu a poté kliknout na **Hledat**.</span><span class="sxs-lookup"><span data-stu-id="18a56-203">You have to type the process name in the search box and then click **Search**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]