---
title: Začněte s doplňkem elektronické fakturace pro Itálii
description: Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Itálii v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 08d41244d3ec785127db8f69e37dd522a463c388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988533"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="ab97d-103">Začněte s doplňkem elektronické fakturace pro Itálii</span><span class="sxs-lookup"><span data-stu-id="ab97d-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="ab97d-104">Doplněk elektronické fakturace pro Itálii nemusí aktuálně podporovat všechny funkce, které jsou k dispozici pro elektronické faktury v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ab97d-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="ab97d-105">Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Itálii</span><span class="sxs-lookup"><span data-stu-id="ab97d-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="ab97d-106">Provede vás konfiguračními kroky, které jsou závislé na zemi v Regulatory Configuration Services (RCS) a Finance.</span><span class="sxs-lookup"><span data-stu-id="ab97d-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="ab97d-107">Rovněž vás provede procesem odesílání elektronických faktur, které jsou generovány ve formátu **FatturaPA** specifického pro Itálii prostřednictvím služby a vysvětluje, jak zkontrolovat výsledky zpracování.</span><span class="sxs-lookup"><span data-stu-id="ab97d-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ab97d-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="ab97d-108">Prerequisites</span></span>

<span data-ttu-id="ab97d-109">Než dokončíte kroky v tomto tématu, musíte provést kroky v [Začněte s doplňkem Elektronická fakturace](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="ab97d-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="ab97d-110">Nastavení RCS</span><span class="sxs-lookup"><span data-stu-id="ab97d-110">RCS setup</span></span>

<span data-ttu-id="ab97d-111">Během instalace RCS dokončíte tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="ab97d-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="ab97d-112">Naimportujte funkci elektronické fakturace pro export elektronických faktur zákazníků ve formátu **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="ab97d-113">Zkontrolujte konfigurace formátu, které jsou vyžadovány pro generování, odesílání a přijímání odpovědí o elektronických fakturách.</span><span class="sxs-lookup"><span data-stu-id="ab97d-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="ab97d-114">Nakonfigurujte události, které podporují scénáře odeslání elektronické faktury.</span><span class="sxs-lookup"><span data-stu-id="ab97d-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="ab97d-115">Publikování funkce elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ab97d-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="ab97d-116">„Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ab97d-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="ab97d-117">V tomto případě je export elektronických faktur zákazníků funkce elektronické fakturace, kterou nastavíte.</span><span class="sxs-lookup"><span data-stu-id="ab97d-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="ab97d-118">Import funkce elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="ab97d-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="ab97d-119">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="ab97d-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="ab97d-120">V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="ab97d-121">Na stránce **Funkce elektronické fakturace** vyberte **Import**, chcete-li importovat funkci elektronické fakturace z globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="ab97d-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ab97d-122">Pokud nevidíte seznam dostupných funkcí, vyberte **Synchronizovat**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="ab97d-123">Vyberte funkci **Export eletronických faktur (IT)** a vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Import funkce exportu elektronických faktur (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="ab97d-125">Při importu funkce **Export elektronických faktur (IT)** z globálního úložiště, importují se také všechna nastavení, která jsou popsána v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="ab97d-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="ab97d-126">Vytvořte novou verzi funkce Exportu eletronických faktur (IT)</span><span class="sxs-lookup"><span data-stu-id="ab97d-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="ab97d-127">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Přidání nové verze funkce elektronické fakturace](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="ab97d-129">Dále nakonfigurujete formáty elektronických zpráv (ER), které jsou spojeny s funkcí elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ab97d-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="ab97d-130">Na kartě **Konfigurace** vyberte **Přidat** ke správě verzí konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ab97d-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Správa verzí konfigurace funkcí elektronické fakturace](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="ab97d-132">V tomto kroku přidáváte a konfigurujete formáty ER různých souborů, které se používají k exportu italských elektronických faktur.</span><span class="sxs-lookup"><span data-stu-id="ab97d-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="ab97d-133">U italských elektronických faktur FatturaPA použijte buď následující standardní konfigurace, nebo skutečné přizpůsobené konfigurace, které používáte pro elektronickou fakturaci:</span><span class="sxs-lookup"><span data-stu-id="ab97d-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="ab97d-134">Prodejní faktura (IT)</span><span class="sxs-lookup"><span data-stu-id="ab97d-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="ab97d-135">Projektová faktura (IT)</span><span class="sxs-lookup"><span data-stu-id="ab97d-135">Project invoice (IT)</span></span>

    <span data-ttu-id="ab97d-136">Když vytvoříte funkci elektronické fakturace, která je odvozena z jiné funkce elektronické fakturace, všechny formáty ER se zdědí z původní funkce.</span><span class="sxs-lookup"><span data-stu-id="ab97d-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="ab97d-137">Vyberte konkrétní konfiguraci souboru formátu ER.</span><span class="sxs-lookup"><span data-stu-id="ab97d-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="ab97d-138">Vyberte **Upravit** nebo **Zobrazit** a otevřete stránku **Návrhář formátů**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Otevření stránky Návrhář formátu](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="ab97d-140">Použijte stránku **Návrhář formátů**, chcete-li upravovat a prohlížet konfigurace souborů ve formátu ER.</span><span class="sxs-lookup"><span data-stu-id="ab97d-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Stránka návrháře formátu](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="ab97d-142">Spravujte nastavení funkce elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="ab97d-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="ab97d-143">Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** vyberte **Přidat**, **Odebrat** nebo **Upravit** ke správě nastavení funkcí elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ab97d-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Správa nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="ab97d-145">V tomto kroku nakonfigurujete události, které se vztahují na elektronické faktury, včetně generování výstupních souborů XML ve formátu **FatturaPA** a digitální podepisování (je-li požadováno).</span><span class="sxs-lookup"><span data-stu-id="ab97d-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="ab97d-146">Nakonfigurujte nastavení funkce prodejní faktury</span><span class="sxs-lookup"><span data-stu-id="ab97d-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="ab97d-147">Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Prodejní faktura**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="ab97d-148">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-148">Select **Edit**.</span></span>
3. <span data-ttu-id="ab97d-149">Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí.</span><span class="sxs-lookup"><span data-stu-id="ab97d-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="ab97d-150">Akce definují seznam operací, které je nutné spustit v postupném pořadí, aby bylo možné provést úplné provedení události.</span><span class="sxs-lookup"><span data-stu-id="ab97d-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Karta Akce](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="ab97d-152">ID akce</span><span class="sxs-lookup"><span data-stu-id="ab97d-152">Action ID</span></span> | <span data-ttu-id="ab97d-153">Název akce</span><span class="sxs-lookup"><span data-stu-id="ab97d-153">Action name</span></span>        | <span data-ttu-id="ab97d-154">Popis akce</span><span class="sxs-lookup"><span data-stu-id="ab97d-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="ab97d-155">1</span><span class="sxs-lookup"><span data-stu-id="ab97d-155">1</span></span>         | <span data-ttu-id="ab97d-156">Převod dokumentu</span><span class="sxs-lookup"><span data-stu-id="ab97d-156">Transform document</span></span> | <span data-ttu-id="ab97d-157">Vytvořte soubor XML e-faktury ve formátu **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="ab97d-158">2</span><span class="sxs-lookup"><span data-stu-id="ab97d-158">2</span></span>         | <span data-ttu-id="ab97d-159">Podepsat dokument</span><span class="sxs-lookup"><span data-stu-id="ab97d-159">Sign document</span></span>      | <span data-ttu-id="ab97d-160">Aplikujte digitální podpis na soubor XML.</span><span class="sxs-lookup"><span data-stu-id="ab97d-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="ab97d-161">Vyberte kartu **Pravidla použitelnosti** pro zobrazení a udržování pravidel použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="ab97d-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="ab97d-162">Pravidla použitelnosti definují kontext, kde bude akce spuštěna.</span><span class="sxs-lookup"><span data-stu-id="ab97d-162">Applicability rules define the context where the action will be run.</span></span>

    ![Karta Pravidla použitelnosti](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="ab97d-164">Vyberte kartu **Proměnné** pro zobrazení a údržbu proměnných.</span><span class="sxs-lookup"><span data-stu-id="ab97d-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Karta Proměnné](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="ab97d-166">Definujte veřejné proměnné, které jsou nutné ke spuštění akcí.</span><span class="sxs-lookup"><span data-stu-id="ab97d-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="ab97d-167">Nakonfigurujte nastavení funkce projektové faktury</span><span class="sxs-lookup"><span data-stu-id="ab97d-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="ab97d-168">Kroky a nastavení, které jsou nutné ke konfiguraci nastavení funkce **Projektová faktura** je velmi podobné krokům a nastavením pro nastavení funkce **Prodejní faktura**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="ab97d-169">Když pracujete s projektovými fakturami, přečtěte si postupy pro prodejní faktury.</span><span class="sxs-lookup"><span data-stu-id="ab97d-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="ab97d-170">Přiřaďte funkci elektronické fakturace k prostředí</span><span class="sxs-lookup"><span data-stu-id="ab97d-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="ab97d-171">Na stránce **Funkce elektronické fakturace** na kartě **Prostředí** vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="ab97d-172">V poli **Prostředí** vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="ab97d-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="ab97d-173">V poli **Platí od** vyberte datum, kdy má začít platnost prostředí.</span><span class="sxs-lookup"><span data-stu-id="ab97d-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="ab97d-174">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-174">Select **Enable**.</span></span> 

![Povolení prostředí elektronické fakturace](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="ab97d-176">Publikování funkce elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="ab97d-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="ab97d-177">Funkci elektronické fakturace můžete publikovat změnou stavu verze na **Dokončeno** nebo **Publikováno**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="ab97d-178">Změna stavu verze na Dokončeno.</span><span class="sxs-lookup"><span data-stu-id="ab97d-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="ab97d-179">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="ab97d-180">Vyberte **Změnit stav \> Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="ab97d-181">Změna stavu verze na Publikováno.</span><span class="sxs-lookup"><span data-stu-id="ab97d-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="ab97d-182">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="ab97d-183">Vyberte **Změnit stav \> Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-183">Select **Change status \> Publish**.</span></span>

![Změna stavu funkce elektronické fakturace](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="ab97d-185">Nastavte integraci doplňku elektronické fakturace ve Finance</span><span class="sxs-lookup"><span data-stu-id="ab97d-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="ab97d-186">Během instalace Finance dokončíte tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="ab97d-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="ab97d-187">Importujte datový model ER, mapování datového modelu ER a kontextové konfigurace pro e-faktury FatturaPA.</span><span class="sxs-lookup"><span data-stu-id="ab97d-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="ab97d-188">Nakonfigurujte certifikát, který je vyžadován k digitálnímu podepisování italských elektronických faktur.</span><span class="sxs-lookup"><span data-stu-id="ab97d-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="ab97d-189">Importujte datový model ER, mapování datového modelu a formáty</span><span class="sxs-lookup"><span data-stu-id="ab97d-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="ab97d-190">V pracovním prostoru **Elektronické výkaznictví**, ověřte, že poskytovatel konfigurace **Služba obchodních dokumentů** je nastaven na **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="ab97d-191">Vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="ab97d-192">Vyberte **Globální prostředek \> Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="ab97d-193">Importujte **Model faktury**, **Mapování modelu faktury** a **Kontextový model faktury zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="ab97d-194">Zapněte funkci pro export elektronických faktur zákazníků pro Itálii</span><span class="sxs-lookup"><span data-stu-id="ab97d-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="ab97d-195">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="ab97d-196">Na kartě **Funkce** zaškrtněte políčko **Povoleno** v řádku pro odkaz na funkci **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![Zapnutí funkce FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="ab97d-198">Konfigurace elektronických dokumentů</span><span class="sxs-lookup"><span data-stu-id="ab97d-198">Configure electronic documents</span></span>

1. <span data-ttu-id="ab97d-199">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="ab97d-200">Na kartě **Elektronický dokument** vyberte **Přidat** a zadejte tabulky, které jsou nutné pro generování italských elektronických faktur:</span><span class="sxs-lookup"><span data-stu-id="ab97d-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="ab97d-201">**Název tabulky:** Deník faktury zákazníka</span><span class="sxs-lookup"><span data-stu-id="ab97d-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="ab97d-202">**Název tabulky:** Projektová faktura</span><span class="sxs-lookup"><span data-stu-id="ab97d-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="ab97d-203">Pro každou tabulku definujte související kontext dokumentu:</span><span class="sxs-lookup"><span data-stu-id="ab97d-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="ab97d-204">Pro **Deník faktury zákazníka** vyberte **Kontext faktury zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="ab97d-205">Pro **Faktura projektu** vyberte **Kontext faktury projektu**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Nastavení typů odpovědí](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="ab97d-207">Zpracování elektronických faktur</span><span class="sxs-lookup"><span data-stu-id="ab97d-207">Electronic invoice processing</span></span>

<span data-ttu-id="ab97d-208">Během zpracování ve Finance dokončíte tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="ab97d-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="ab97d-209">Generujte italské e-faktury prostřednictvím doplňku Elektronická fakturace</span><span class="sxs-lookup"><span data-stu-id="ab97d-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="ab97d-210">Zobrazte protokoly o provedení a zkontrolujte výsledky zpracování.</span><span class="sxs-lookup"><span data-stu-id="ab97d-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="ab97d-211">Generujte elektronické faktury</span><span class="sxs-lookup"><span data-stu-id="ab97d-211">Generate electronic invoices</span></span>

<span data-ttu-id="ab97d-212">Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** a aktivaci funkce **IT00036** starý proces pro generování italských elektronických faktur ve Finance již nelze použít.</span><span class="sxs-lookup"><span data-stu-id="ab97d-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="ab97d-213">Je nahrazen novým procesem, který je pojmenován **Odesílejte elektronické dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="ab97d-214">Dokumenty můžete odeslat ručně na základě vašeho požadavku na dokumenty elektronické faktury.</span><span class="sxs-lookup"><span data-stu-id="ab97d-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="ab97d-215">Než budete pokračovat, ověřte, že bylo dokončeno nastavení požadované pro italské elektronické faktury.</span><span class="sxs-lookup"><span data-stu-id="ab97d-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="ab97d-216">Další informace naleznete v tématu [Zákaznické elektronické faktury](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="ab97d-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="ab97d-217">Uvědomte si, že některé kroky nastavení popsané v tomto tématu nemusí být k dispozici z důvodu aktivace doplňku Elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="ab97d-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="ab97d-218">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Odesílejte elektronické dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="ab97d-219">Pro první odeslání jakéhokoli dokumentu nastavte možnost **Znovu odeslat dokumenty** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="ab97d-220">Pokud musíte znovu odeslat dokument prostřednictvím služby, nastavte tuto možnost na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="ab97d-221">Na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a otevřete dialogové okno **Dotaz**, kde můžete vytvořit dotaz pro výběr dokumentů k odeslání.</span><span class="sxs-lookup"><span data-stu-id="ab97d-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Dialogové okno Odeslat elektronické dokumenty](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="ab97d-223">Dotaz filtru</span><span class="sxs-lookup"><span data-stu-id="ab97d-223">Filter query</span></span>

1. <span data-ttu-id="ab97d-224">V dialogovém okně **Dotaz** nakonfigurujte podmínky filtrování prodejních faktur i projektových faktur nebo ponechte podmínky prázdné, aby zahrnovaly všechny neodeslané faktury.</span><span class="sxs-lookup"><span data-stu-id="ab97d-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Nastavení kritérií filtru odeslání](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="ab97d-226">Zvolte **OK** a zavřete dialogové okno **Dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="ab97d-227">Vyberte **OK** k odeslání vybraných dokumentů.</span><span class="sxs-lookup"><span data-stu-id="ab97d-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="ab97d-228">![POZNÁMKA] Během prvního pokusu o odeslání dokumentu prostřednictvím služby budete vyzváni k potvrzení spojení s doplňkem Elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="ab97d-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="ab97d-229">Vyberte **Klikněte zde pro připojení ke službě elektronického odesílání dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="ab97d-230">Zobrazit protokoly odeslání</span><span class="sxs-lookup"><span data-stu-id="ab97d-230">View submission logs</span></span>

<span data-ttu-id="ab97d-231">Můžete si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty.</span><span class="sxs-lookup"><span data-stu-id="ab97d-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="ab97d-232">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="ab97d-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="ab97d-233">V poli **Typ dokumentu** vyberte **Deník faktury zákazníka** nebo **Faktura projektu**, chcete-li filtrovat požadované elektronické dokumenty.</span><span class="sxs-lookup"><span data-stu-id="ab97d-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Výběr typu dokumentu pro zobrazení protokolů odeslání](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="ab97d-235">Hodnota, která je uvedena ve sloupci **Stav odeslání** představuje stav procesu odesílání.</span><span class="sxs-lookup"><span data-stu-id="ab97d-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="ab97d-236">Označuje, zda byl proces spuštěn tak, jak byl nakonfigurován, a zda je vyžadována další akce.</span><span class="sxs-lookup"><span data-stu-id="ab97d-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="ab97d-237">V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.</span><span class="sxs-lookup"><span data-stu-id="ab97d-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Zobrazení podrobností protokolu odeslání.](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="ab97d-239">Na pevné záložce **Zpracování akcí** můžete zobrazit protokol provádění akcí, které jsou konfigurovány ve verzi funkce, která byla nastavena v RCS.</span><span class="sxs-lookup"><span data-stu-id="ab97d-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="ab97d-240">Sloupec **Stav** ukazuje, zda byla akce úspěšně spuštěna.</span><span class="sxs-lookup"><span data-stu-id="ab97d-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="ab97d-241">Na pevné záložce **Soubory akcí** můžete zobrazit přechodné soubory, které byly vygenerovány během provádění akcí.</span><span class="sxs-lookup"><span data-stu-id="ab97d-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="ab97d-242">Můžete vybrat **Zobrazit** a stáhnout výstupní soubor XML ve formátu **FatturaPA** a zobrazit jeho obsah.</span><span class="sxs-lookup"><span data-stu-id="ab97d-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab97d-243">Související témata</span><span class="sxs-lookup"><span data-stu-id="ab97d-243">Related topics</span></span>

- [<span data-ttu-id="ab97d-244">Přehled doplňku Elektronická fakturace</span><span class="sxs-lookup"><span data-stu-id="ab97d-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="ab97d-245">Začněte s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="ab97d-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="ab97d-246">Nastavení doplňku Elektronická fakturace</span><span class="sxs-lookup"><span data-stu-id="ab97d-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
