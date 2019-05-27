---
title: Připojení k systému nápovědy
description: Toto téma popisuje součástí systému nápovědy pro Microsoft Dynamics 365 for Finance and Operations a poskytuje přehled o způsobu jejich propojení a shrnutí postupu pro vytvoření vlastní nápovědy.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561968"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="09731-103">Připojení k systému nápovědy</span><span class="sxs-lookup"><span data-stu-id="09731-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09731-104">Toto téma popisuje součástí systému nápovědy pro Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09731-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="09731-105">Poskytuje přehled o tom, jak připojit tyto komponenty, a souhrnné informace o tom, jak vytvořit vlastní nápovědu.</span><span class="sxs-lookup"><span data-stu-id="09731-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="09731-106">Architektura nápovědy</span><span class="sxs-lookup"><span data-stu-id="09731-106">Help architecture</span></span>

<span data-ttu-id="09731-107">Následující obrázek znázorňuje části systému nápovědy aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09731-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="09731-108">Systém nápovědy v produktu přebírá články z webu aplikace Finance and Operations na adrese https://docs.microsoft.com a také z průvodců záznamem úloh uložených v modulu modelování podnikových procesů ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="09731-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="09731-109">Funkce označené v diagramu hvězdičkou (\*) jsou plánované, ale nejsou zatím k dispozici.</span><span class="sxs-lookup"><span data-stu-id="09731-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="09731-110">[![Architektura nápovědy](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="09731-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="09731-111">Připojení systému nápovědy</span><span class="sxs-lookup"><span data-stu-id="09731-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="09731-112">Karta **Průvodci záznamem úloh** není k dispozici v aplikacích Microsoft Dynamics 365 for Talent a Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="09731-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="09731-113">Funkci zpřístupníme v budoucí verzi.</span><span class="sxs-lookup"><span data-stu-id="09731-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="09731-114">Průvodci v prostředí Začínáme v aplikaci Talent jsou i nadále k dispozici a zabývají se základními funkcemi.</span><span class="sxs-lookup"><span data-stu-id="09731-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="09731-115">Na webu docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) jsou také k dispozici pokyny pro aplikaci Retail i Talent.</span><span class="sxs-lookup"><span data-stu-id="09731-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="09731-116">Pomocí stránky **Systémové parametry** správci systému připojí části systému nápovědy pro implementaci.</span><span class="sxs-lookup"><span data-stu-id="09731-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="09731-117">[![Formulář Systémové parametry s nastavením nápovědy](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="09731-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="09731-118">Na stránce **Systémové parametry** proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="09731-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09731-119">Při prvním otevření karty **Nápověda** je nutné se připojit k službě Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="09731-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="09731-120">Klikněte na odkaz uprostřed formuláře, počkejte na připojení, zavřete dialogové okno a kliknutím na tlačítko **OK** otevřete stránku **Parametry** systému.</span><span class="sxs-lookup"><span data-stu-id="09731-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="09731-121">[![Připojení k LCS](./media/connect-to-lcs-crop-1024x365.png "Připojení k LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="09731-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="09731-122">Vyberte projekt služby Lifecycle Services pro připojení.</span><span class="sxs-lookup"><span data-stu-id="09731-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="09731-123">Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.</span><span class="sxs-lookup"><span data-stu-id="09731-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="09731-124">U aplikace Finance and Operations vyberte pro obsah společnosti Microsoft nejnovější APQC Unified Library for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09731-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="09731-125">Pro modul Retail vydáme knihovnu v blízké době.</span><span class="sxs-lookup"><span data-stu-id="09731-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="09731-126">Pro aplikaci Talent není třeba knihovnu vybírat – připojení ke správné knihovně se nastaví automaticky.</span><span class="sxs-lookup"><span data-stu-id="09731-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="09731-127">Nastavte pořadí zobrazení knihoven BPM.</span><span class="sxs-lookup"><span data-stu-id="09731-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="09731-128">Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.</span><span class="sxs-lookup"><span data-stu-id="09731-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="09731-129">Po dokončení těchto kroků můžete otevřít podokno **Nápověda** a kliknutí na kartu **Průvodci záznamem úloh**. Zobrazí se vám nyní průvodci záznamem úloh, které se vztahují ke stránce, na které se momentálně v aplikaci Finance and Operations nacházíte.</span><span class="sxs-lookup"><span data-stu-id="09731-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="09731-130">Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.</span><span class="sxs-lookup"><span data-stu-id="09731-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="09731-131">Zobrazení přeložených průvodců úkoly</span><span class="sxs-lookup"><span data-stu-id="09731-131">Showing translated task guides</span></span>

<span data-ttu-id="09731-132">Přeložení průvodci úkolem byli poprvé vydání v knihovně APQC Unified Library pro květen 2016 a v knihovně Začínáme.</span><span class="sxs-lookup"><span data-stu-id="09731-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="09731-133">Chcete-li v aplikaci Finance and Operations zobrazit lokalizovanou nápovědu k průvodci záznamem úloh, zkontrolujte, zda máte připojenou knihovnu z května.</span><span class="sxs-lookup"><span data-stu-id="09731-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="09731-134">Jazyk, ve kterém se průvodce úkolem zobrazí, je řízen pro každého uživatele v jazykovém nastavení v části **Možnosti** &gt; **Předvolby**.</span><span class="sxs-lookup"><span data-stu-id="09731-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="09731-135">I když mnoho průvodců záznamem úloh již bylo přeloženo, klient aplikace Finance and Operations v současnosti nezobrazuje jejich přeložené názvy.</span><span class="sxs-lookup"><span data-stu-id="09731-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="09731-136">Stejně tak pouze průvodci úkolem vydaní v únoru jsou momentálně k dispozici v překladu v knihovně pro únor 2016.</span><span class="sxs-lookup"><span data-stu-id="09731-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="09731-137">Aktualizovanou knihovnou s další překlady zpřístupníme později.</span><span class="sxs-lookup"><span data-stu-id="09731-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="09731-138">Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.</span><span class="sxs-lookup"><span data-stu-id="09731-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="09731-139">Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).</span><span class="sxs-lookup"><span data-stu-id="09731-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="09731-140">Vytváření vlastních nápověd</span><span class="sxs-lookup"><span data-stu-id="09731-140">Creating custom help</span></span>

<span data-ttu-id="09731-141">Můžete použít průvodce záznamem úloh k vytvoření vlastní nápovědy, nebo připojit své webové stránky k panelu Nápověda.</span><span class="sxs-lookup"><span data-stu-id="09731-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="09731-142">Vytvoření vlastní nápovědy pomocí průvodců záznamem úloh</span><span class="sxs-lookup"><span data-stu-id="09731-142">Create custom help with task guides</span></span>

<span data-ttu-id="09731-143">Vlastní nápovědu pro aplikace Finance and Operations a Retail můžete vytvořit tak, že vytvoříte záznamy úloh, které odpovídají vaší implementaci, a uložíte je do knihovny obchodního procesu LCS.</span><span class="sxs-lookup"><span data-stu-id="09731-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="09731-144">Pro aplikaci Talent nelze vlastní průvodce záznamem úloh vytvořit.</span><span class="sxs-lookup"><span data-stu-id="09731-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="09731-145">Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům.</span><span class="sxs-lookup"><span data-stu-id="09731-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="09731-146">Můžete vytvořit také kopii sjednocené globální knihovny APQC a poté otevřít kopii z ní otevřít záznamy úloh, upravit je a uložit záznamy s provedenými změnami.</span><span class="sxs-lookup"><span data-stu-id="09731-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="09731-147">Další informace naleznete v tématu [Vytvoření záznamu úkolu jako dokumentace nebo školení](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="09731-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="09731-148">Připojení vlastního webu</span><span class="sxs-lookup"><span data-stu-id="09731-148">Connect a custom site</span></span>

<span data-ttu-id="09731-149">Společnost Microsoft poskytla dokument white paper a vzorový kód, které popisují způsob vytvoření a připojení vlastního webu nápovědy k panelu Nápověda.</span><span class="sxs-lookup"><span data-stu-id="09731-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="09731-150">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="09731-150">For more information, see:</span></span>

- [<span data-ttu-id="09731-151">Vytvoření vlastní nápovědy pro Finance and Operations (dokument white paper)</span><span class="sxs-lookup"><span data-stu-id="09731-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="09731-152">Úložiště GitHub vlastní nápovědy</span><span class="sxs-lookup"><span data-stu-id="09731-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="09731-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="09731-153">Additional resources</span></span>

[<span data-ttu-id="09731-154">Přehled nápovědy</span><span class="sxs-lookup"><span data-stu-id="09731-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="09731-155">Přehled záznamníku úloh</span><span class="sxs-lookup"><span data-stu-id="09731-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="09731-156">Postup vytvoření záznamu úloh pro použití jako dokumentace nebo školení</span><span class="sxs-lookup"><span data-stu-id="09731-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
