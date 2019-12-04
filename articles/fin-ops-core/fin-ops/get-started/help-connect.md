---
title: Připojení k systému nápovědy
description: Toto téma popisuje součástí systému nápovědy pro aplikace Finance and Operations a poskytuje přehled o způsobu jejich propojení a shrnutí postupu pro vytvoření vlastní nápovědy.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812573"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="4bb55-103">Připojení k systému nápovědy</span><span class="sxs-lookup"><span data-stu-id="4bb55-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bb55-104">V tomto tématu jsou popsány komponenty systému nápovědy pro aplikace Finance and Operations, jako je Dynamics 365 Finance, Supply Chain Management, Retail a Talent.</span><span class="sxs-lookup"><span data-stu-id="4bb55-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Retail, and Talent.</span></span> <span data-ttu-id="4bb55-105">Poskytuje přehled o tom, jak připojit tyto komponenty, a souhrnné informace o tom, jak vytvořit vlastní nápovědu.</span><span class="sxs-lookup"><span data-stu-id="4bb55-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="4bb55-106">Architektura nápovědy</span><span class="sxs-lookup"><span data-stu-id="4bb55-106">Help architecture</span></span>

<span data-ttu-id="4bb55-107">Následující obrázek znázorňuje části systému nápovědy.</span><span class="sxs-lookup"><span data-stu-id="4bb55-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="4bb55-108">Systém nápovědy v produktu přebírá články z webu https://docs.microsoft.com a také z průvodců záznamem úloh uložených v modulu Modelování podnikových procesů ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4bb55-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="4bb55-109">Funkce označené v diagramu hvězdičkou (\*) jsou plánované, ale nejsou zatím k dispozici.</span><span class="sxs-lookup"><span data-stu-id="4bb55-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="4bb55-110">[![Architektura nápovědy](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="4bb55-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="4bb55-111">Připojení systému nápovědy</span><span class="sxs-lookup"><span data-stu-id="4bb55-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="4bb55-112">Karta **Průvodci záznamem** úloh není k dispozici v aplikacích Dynamics 365 Talent či Retail.</span><span class="sxs-lookup"><span data-stu-id="4bb55-112">The **Task guides** tab is currently not available in Dynamics 365 Talent or Retail.</span></span> <span data-ttu-id="4bb55-113">Funkci zpřístupníme v budoucí verzi.</span><span class="sxs-lookup"><span data-stu-id="4bb55-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="4bb55-114">Průvodci v prostředí Začínáme v aplikaci Talent jsou i nadále k dispozici a zabývají se základními funkcemi.</span><span class="sxs-lookup"><span data-stu-id="4bb55-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="4bb55-115">Procesní nápověda je k dispozici také na webu docs.microsoft.com pro Retail a Talent.</span><span class="sxs-lookup"><span data-stu-id="4bb55-115">Procedural help is also available on the docs.microsoft.com site for both Retail and Talent.</span></span>

<span data-ttu-id="4bb55-116">Pomocí stránky **Systémové parametry** správci systému připojí části systému nápovědy pro implementaci.</span><span class="sxs-lookup"><span data-stu-id="4bb55-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="4bb55-117">[![Formulář Systémové parametry s nastavením nápovědy](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="4bb55-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="4bb55-118">Na stránce **Systémové parametry** proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="4bb55-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4bb55-119">Při prvním otevření karty **Nápověda** je nutné se připojit k službě Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="4bb55-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="4bb55-120">Klikněte na odkaz uprostřed formuláře, počkejte na připojení, zavřete dialogové okno a kliknutím na tlačítko **OK** otevřete stránku **Parametry** systému.</span><span class="sxs-lookup"><span data-stu-id="4bb55-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="4bb55-121">[![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png "Připojit k LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="4bb55-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="4bb55-122">Vyberte projekt služby Lifecycle Services pro připojení.</span><span class="sxs-lookup"><span data-stu-id="4bb55-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="4bb55-123">Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.</span><span class="sxs-lookup"><span data-stu-id="4bb55-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="4bb55-124">Nastavte pořadí zobrazení knihoven BPM.</span><span class="sxs-lookup"><span data-stu-id="4bb55-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="4bb55-125">Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.</span><span class="sxs-lookup"><span data-stu-id="4bb55-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="4bb55-126">Po dokončení těchto kroků můžete otevřít podokno **Nápověda** a kliknutí na kartu **Průvodci záznamem úloh**. Zobrazí se vám nyní průvodci záznamem úloh, které se vztahují ke stránce, na které se momentálně v aplikacích Finance and Operations nacházíte.</span><span class="sxs-lookup"><span data-stu-id="4bb55-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="4bb55-127">Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.</span><span class="sxs-lookup"><span data-stu-id="4bb55-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="4bb55-128">Zobrazení přeložených průvodců úkoly</span><span class="sxs-lookup"><span data-stu-id="4bb55-128">Showing translated task guides</span></span>

<span data-ttu-id="4bb55-129">Přeložení průvodci úkolem byli poprvé vydání v knihovně APQC Unified Library pro květen 2016 a v knihovně Začínáme.</span><span class="sxs-lookup"><span data-stu-id="4bb55-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="4bb55-130">Chcete-li v aplikacích Finance and Operations zobrazit lokalizovanou nápovědu k průvodci záznamem úloh, zkontrolujte, zda máte připojenou knihovnu z května.</span><span class="sxs-lookup"><span data-stu-id="4bb55-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="4bb55-131">Jazyk, ve kterém se průvodce úkolem zobrazí, je řízen pro každého uživatele v jazykovém nastavení v části **Možnosti** &gt; **Předvolby**.</span><span class="sxs-lookup"><span data-stu-id="4bb55-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="4bb55-132">I když mnoho průvodců úkolem již bylo přeloženy, klient aktuálně nezobrazuje názvy přeložených průvodců úkolem.</span><span class="sxs-lookup"><span data-stu-id="4bb55-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="4bb55-133">Stejně tak pouze průvodci úkolem vydaní v únoru jsou momentálně k dispozici v překladu v knihovně pro únor 2016.</span><span class="sxs-lookup"><span data-stu-id="4bb55-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="4bb55-134">Aktualizovanou knihovnou s další překlady zpřístupníme později.</span><span class="sxs-lookup"><span data-stu-id="4bb55-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="4bb55-135">Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.</span><span class="sxs-lookup"><span data-stu-id="4bb55-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="4bb55-136">Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).</span><span class="sxs-lookup"><span data-stu-id="4bb55-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="4bb55-137">Vytváření vlastních nápověd</span><span class="sxs-lookup"><span data-stu-id="4bb55-137">Creating custom help</span></span>

<span data-ttu-id="4bb55-138">Můžete použít průvodce záznamem úloh k vytvoření vlastní nápovědy, nebo připojit své webové stránky k panelu Nápověda.</span><span class="sxs-lookup"><span data-stu-id="4bb55-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="4bb55-139">Vytvoření vlastní nápovědy pomocí průvodců záznamem úloh</span><span class="sxs-lookup"><span data-stu-id="4bb55-139">Create custom help with task guides</span></span>

<span data-ttu-id="4bb55-140">Vlastní nápovědu pro aplikace Finance, Supply Chain Management a Retail můžete vytvořit tak, že vytvoříte záznamy úloh, které odpovídají vaší implementaci, a uložíte je do knihovny obchodního procesu LCS.</span><span class="sxs-lookup"><span data-stu-id="4bb55-140">You can create custom help for Finance, Supply Chain Management, and Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="4bb55-141">Pro aplikaci Talent nelze vlastní průvodce záznamem úloh vytvořit.</span><span class="sxs-lookup"><span data-stu-id="4bb55-141">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="4bb55-142">Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům.</span><span class="sxs-lookup"><span data-stu-id="4bb55-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="4bb55-143">Můžete vytvořit také kopii sjednocené globální knihovny APQC a poté otevřít kopii z ní otevřít záznamy úloh, upravit je a uložit záznamy s provedenými změnami.</span><span class="sxs-lookup"><span data-stu-id="4bb55-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="4bb55-144">Více informací viz [Zdroje záznamníku úloh](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="4bb55-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="4bb55-145">Připojení vlastního webu</span><span class="sxs-lookup"><span data-stu-id="4bb55-145">Connect a custom site</span></span>

<span data-ttu-id="4bb55-146">Společnost Microsoft poskytla dokument white paper a vzorový kód, které popisují způsob vytvoření a připojení vlastního webu nápovědy k panelu Nápověda.</span><span class="sxs-lookup"><span data-stu-id="4bb55-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="4bb55-147">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="4bb55-147">For more information, see:</span></span>

- [<span data-ttu-id="4bb55-148">Vytvoření vlastní nápovědy pro aplikace Finance and Operations (dokument white paper)</span><span class="sxs-lookup"><span data-stu-id="4bb55-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="4bb55-149">Úložiště GitHub vlastní nápovědy</span><span class="sxs-lookup"><span data-stu-id="4bb55-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="4bb55-150">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4bb55-150">Additional resources</span></span>

[<span data-ttu-id="4bb55-151">Systém nápovědy</span><span class="sxs-lookup"><span data-stu-id="4bb55-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="4bb55-152">Zdroje záznamníku úloh</span><span class="sxs-lookup"><span data-stu-id="4bb55-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="4bb55-153">Vytváření dokumentace nebo školení pomocí záznamníku úloh</span><span class="sxs-lookup"><span data-stu-id="4bb55-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
