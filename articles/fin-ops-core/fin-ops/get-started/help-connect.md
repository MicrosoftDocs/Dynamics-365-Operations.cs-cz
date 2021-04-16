---
title: Konfigurace prostředí nápovědy pro aplikace Finance and Operations
description: Toto téma poskytuje informace o součástech systému nápovědy pro některé aplikace Microsoft Dynamics 365.
author: margoc
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82bb9a09e6d302b0d453ceb5131da039769b58fb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745682"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="07b0d-103">Konfigurace prostředí nápovědy pro aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="07b0d-103">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07b0d-104">V tomto tématu najdete přehled součástí systému nápovědy pro aplikace Finance and Operations, jako je Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce a Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="07b0d-104">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="07b0d-105">Toto téma také vysvětluje, jak tyto komponenty propojit, a poskytuje shrnutí procesu vytváření vlastní nápovědy.</span><span class="sxs-lookup"><span data-stu-id="07b0d-105">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="07b0d-106">Architektura nápovědy</span><span class="sxs-lookup"><span data-stu-id="07b0d-106">Help architecture</span></span>

<span data-ttu-id="07b0d-107">Aplikace Finance and Operations zahrnují koncepční přehledy a další témata, která jsou publikována na web internetu [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="07b0d-107">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="07b0d-108">K tomuto obsahu lze poté přistupovat z podokna **Nápověda** v produktu.</span><span class="sxs-lookup"><span data-stu-id="07b0d-108">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="07b0d-109">Následující obrázek znázorňuje části systému nápovědy.</span><span class="sxs-lookup"><span data-stu-id="07b0d-109">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="07b0d-110">[![Architektura nápovědy](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="07b0d-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="07b0d-111">Systém nápovědy v produktu stahuje články z docs.microsoft.com a dalších připojených webů.</span><span class="sxs-lookup"><span data-stu-id="07b0d-111">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="07b0d-112">Načítá také průvodce záznamem úloh, které jsou uloženy v modelování podnikových procesů v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="07b0d-112">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="07b0d-113">Přidání průvodců záznamem úloh</span><span class="sxs-lookup"><span data-stu-id="07b0d-113">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="07b0d-114">Karta **Průvodci záznamem úloh** není k dispozici v aplikacích Human Resources či Commerce.</span><span class="sxs-lookup"><span data-stu-id="07b0d-114">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="07b0d-115">Nicméně průvodci záznamem úloh v prostředí Začínáme v aplikaci Human Resources jsou i nadále k dispozici a zabývají se základními funkcemi.</span><span class="sxs-lookup"><span data-stu-id="07b0d-115">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="07b0d-116">Procesní nápověda je k dispozici také na webu [https://docs.microsoft.com/dynamics365](/dynamics365/) pro Human Resources a Commerce.</span><span class="sxs-lookup"><span data-stu-id="07b0d-116">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="07b0d-117">Na stránce **Parametry systému** mohou správci systému nakonfigurovat přístup k příslušným knihovnám průvodců záznamem úloh pro implementaci.</span><span class="sxs-lookup"><span data-stu-id="07b0d-117">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="07b0d-118">Chcete-li nakonfigurovat nápovědu, musíte se přihlásit pomocí účtu u stejného klienta jako je klient, ve kterém je aplikace umístěna.</span><span class="sxs-lookup"><span data-stu-id="07b0d-118">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="07b0d-119">Knihovnu LCS nelze připojit z instance aplikace spuštěné na místním virtuálním pevném disku (VHD).</span><span class="sxs-lookup"><span data-stu-id="07b0d-119">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="07b0d-120">[![Formulář Systémové parametry s nastavením nápovědy](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="07b0d-120">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="07b0d-121&quot;>Chcete-li nakonfigurovat průvodce záznamem úloh pro řešení, postupujte podle těchto kroků na stránce **Parametry systému**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;07b0d-121&quot;>To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id=&quot;07b0d-122&quot;>Při prvním otevření karty **Nápověda** je nutné se připojit k službě Lifecycle Services.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;07b0d-122&quot;>The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id=&quot;07b0d-123&quot;>Zvolte odkaz uprostřed formuláře, počkejte na připojení, zavřete dialogové okno a volbou tlačítka **OK** otevřete stránku **Parametry systému**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;07b0d-123&quot;>Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id=&quot;07b0d-124&quot;>[![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png &quot;Připojit k LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="07b0d-124">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="07b0d-125">Vyberte projekt služby Lifecycle Services pro připojení.</span><span class="sxs-lookup"><span data-stu-id="07b0d-125">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="07b0d-126">Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.</span><span class="sxs-lookup"><span data-stu-id="07b0d-126">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="07b0d-127">Nastavte pořadí zobrazení knihoven BPM.</span><span class="sxs-lookup"><span data-stu-id="07b0d-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="07b0d-128">Toto pořadí zobrazení určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.</span><span class="sxs-lookup"><span data-stu-id="07b0d-128">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="07b0d-129">Po dokončení těchto kroků můžete otevřít podokno **Nápověda** a zvolit kartu **Průvodci záznamem úloh**. Zobrazí se vám nyní průvodci záznamem úloh, které se vztahují ke stránce, na které se momentálně v aplikacích Finance and Operations nacházíte.</span><span class="sxs-lookup"><span data-stu-id="07b0d-129">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="07b0d-130">Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.</span><span class="sxs-lookup"><span data-stu-id="07b0d-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="07b0d-131">Zobrazení přeložených průvodců úkoly</span><span class="sxs-lookup"><span data-stu-id="07b0d-131">Showing translated task guides</span></span>

<span data-ttu-id="07b0d-132">Přeložení průvodci záznamem úloh byli poprvé vydáni v knihovně APQC Unified Library pro květen 2016 a v knihovně Začínáme.</span><span class="sxs-lookup"><span data-stu-id="07b0d-132">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="07b0d-133">Chcete-li zobrazit lokalizovanou nápovědu pro průvodce záznamem úloh, ujistěte se, že je vaše řešení Dynamics 365 připojeno ke knihovně z května 2016.</span><span class="sxs-lookup"><span data-stu-id="07b0d-133">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="07b0d-134">Uživatelé mohou změnit jazyk, ve kterém se průvodce úkolem zobrazí, změnou jazykového nastavení v části **Možnosti** &gt; **Preference**.</span><span class="sxs-lookup"><span data-stu-id="07b0d-134">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="07b0d-135">I když mnoho průvodců záznamem úloh již bylo přeloženo, klient aktuálně nezobrazuje názvy přeložených průvodců záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="07b0d-135">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="07b0d-136">Kromě toho jsou v knihovně z května 2016 k dispozici překlady pouze pro průvodce úloh, které byly vydány v únoru 2016.</span><span class="sxs-lookup"><span data-stu-id="07b0d-136">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="07b0d-137">Aktualizovanou knihovnu s další překlady zpřístupní Microsoft později.</span><span class="sxs-lookup"><span data-stu-id="07b0d-137">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="07b0d-138">Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.</span><span class="sxs-lookup"><span data-stu-id="07b0d-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="07b0d-139">Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).</span><span class="sxs-lookup"><span data-stu-id="07b0d-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="07b0d-140">Přidání vlastní nápovědy</span><span class="sxs-lookup"><span data-stu-id="07b0d-140">Adding custom Help</span></span>

<span data-ttu-id="07b0d-141">Můžete použít průvodce záznamem úloh k vytvoření vlastní nápovědy, nebo připojit vlastní webové stránky k podoknu **Nápověda**.</span><span class="sxs-lookup"><span data-stu-id="07b0d-141">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="07b0d-142">Vytvoření vlastní nápovědy pomocí průvodců záznamem úloh</span><span class="sxs-lookup"><span data-stu-id="07b0d-142">Create custom Help by using task guides</span></span>

<span data-ttu-id="07b0d-143">Můžete si vytvořit vlastní nápovědu pro podporované aplikace vytvořením záznamů úloh, které odrážejí vaši implementaci, a poté je uložit do knihovny obchodních procesů v LCS.</span><span class="sxs-lookup"><span data-stu-id="07b0d-143">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="07b0d-144">V aplikaci Human Resources nelze vytvářet vlastní průvodce záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="07b0d-144">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="07b0d-145">Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům.</span><span class="sxs-lookup"><span data-stu-id="07b0d-145">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="07b0d-146">Můžete vytvořit také kopii sjednocené knihovny APQC a poté otevřít záznamy úloh v kopii, upravit je a uložit záznamy s provedenými změnami.</span><span class="sxs-lookup"><span data-stu-id="07b0d-146">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="07b0d-147">Více informací viz [Zdroje záznamníku úloh](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="07b0d-147">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="07b0d-148">Připojení vlastního webu nápovědy</span><span class="sxs-lookup"><span data-stu-id="07b0d-148">Connect a custom Help site</span></span>

<span data-ttu-id="07b0d-149">Aplikace Finance and Operations se používají jen zřídka ve své výchozí formě.</span><span class="sxs-lookup"><span data-stu-id="07b0d-149">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="07b0d-150">Místo toho je řešení přizpůsobeno a rozšířeno podle potřeb organizace.</span><span class="sxs-lookup"><span data-stu-id="07b0d-150">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="07b0d-151">Můžete také přizpůsobit a rozšířit prostředí nápovědy.</span><span class="sxs-lookup"><span data-stu-id="07b0d-151">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="07b0d-152">Například můžete přidat vlastní nápovědu do podokna **Nápověda** v produktu.</span><span class="sxs-lookup"><span data-stu-id="07b0d-152">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="07b0d-153">Společnost Microsoft poskytla sadu nástrojů, která vám pomůže při nasazení a připojení vlastní nápovědy k podoknu **Nápověda**.</span><span class="sxs-lookup"><span data-stu-id="07b0d-153">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="07b0d-154">Informace o tom, jak můžete nastavit vlastní řešení nápovědy připojené k podoknu **Nápověda** najdete v části [Přehled vlastní nápovědy](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="07b0d-154">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="07b0d-155">Pokud chcete spolupracovat se společností Microsoft na nástrojích a procesech přizpůsobení nápovědy, vyplňte formulář na adrese [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="07b0d-155">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="07b0d-156">Viz také</span><span class="sxs-lookup"><span data-stu-id="07b0d-156">See also</span></span>

[<span data-ttu-id="07b0d-157">Systém nápovědy</span><span class="sxs-lookup"><span data-stu-id="07b0d-157">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="07b0d-158">Přehled vlastní nápovědy</span><span class="sxs-lookup"><span data-stu-id="07b0d-158">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="07b0d-159">Zdroje záznamníku úloh</span><span class="sxs-lookup"><span data-stu-id="07b0d-159">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="07b0d-160">Vytváření dokumentace nebo školení pomocí záznamníku úloh</span><span class="sxs-lookup"><span data-stu-id="07b0d-160">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="07b0d-161">Úložiště GitHub vlastní nápovědy</span><span class="sxs-lookup"><span data-stu-id="07b0d-161">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]