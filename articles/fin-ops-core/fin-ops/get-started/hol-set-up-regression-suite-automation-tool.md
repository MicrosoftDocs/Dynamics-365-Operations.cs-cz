---
title: Nastavení a instalace kurzu pro nástroj Regression Suite Automation Tool
description: Toto téma je kurz, který ukazuje, jak nastavit a nainstalovat nástroj Regression suite automation tool (RSAT).
author: kfend
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 50450669387f4e2c9e81975d5345c525c7929c47
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180638"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="fb5d2-103">Nastavení a instalace kurzu pro nástroj Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="fb5d2-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="fb5d2-104">Toto téma je kurz, který vám pomůže získat instalační program a začít s nástrojem RSAT a nástroji spojenými s používáním nástroje RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="fb5d2-105">Pomocí nástrojů internetového prohlížeče můžete tuto stránku stáhnout a uložit ve formátu PDF.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="fb5d2-106">Klíčové koncepty</span><span class="sxs-lookup"><span data-stu-id="fb5d2-106">Key concepts</span></span>

- <span data-ttu-id="fb5d2-107">Vysvětlení instalace a nezbytných nastavení vyžadovaných pro různé aplikace podporující nástroj Regression Suite Automation Tool (RSAT).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="fb5d2-108">Vysvětlení, jak funkce Záznamník úloh spolu s funkcí Microsoft Dynamics Lifecycle Services (LCS) a Microsoft Azure DevOps umožňují vytvářet, konfigurovat, spouštět, zkoumat a vykazovat testovací případy.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="fb5d2-109">Pomocí záznamníku úkolů můžete funkčním uživatelům umožnit záznam obchodních úkolů a poté převést záznamy úkolů na sadu automatizovaných testů, aniž by bylo nutné vytvářet zdrojový kód.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="fb5d2-110">Než začnete</span><span class="sxs-lookup"><span data-stu-id="fb5d2-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fb5d2-111">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="fb5d2-111">Prerequisites</span></span>

- <span data-ttu-id="fb5d2-112">V tomto kurzu je vyžadováno prostředí s aplikací Microsoft Dynamics 365 for Finance and Operations verze 10.0 (duben 2019) nebo novější.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="fb5d2-113">Pro zákazníky, kteří používají Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3, je podporována také Platform update 20 (PU20) nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="fb5d2-114">Uživatel musí mít pro toto prostředí oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="fb5d2-115">Musíte mít přístup do LCS tenanta zákazníka a Azure DevOps (dříve známé jako Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="fb5d2-116">Uživatel, který vytváří a spravuje testy, musí mí licenci Azure DevOps Test Plans nebo Test Manager.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="fb5d2-117">Následující licence také umožní přístup k testovacím plánům:</span><span class="sxs-lookup"><span data-stu-id="fb5d2-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="fb5d2-118">Visual Studio Enterprise</span><span class="sxs-lookup"><span data-stu-id="fb5d2-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="fb5d2-119">Visual Studio Test Professional</span><span class="sxs-lookup"><span data-stu-id="fb5d2-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="fb5d2-120">Licence pro předplatitele Platforem MSDN</span><span class="sxs-lookup"><span data-stu-id="fb5d2-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="fb5d2-121">Nástroje RSAT musí mít přístup k testovacímu prostředí prostřednictvím webového prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="fb5d2-122">Chcete-li vygenerovat a upravit parametry testu, musíte mít nainstalovánu aplikaci Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="fb5d2-123">Konfigurace služby Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="fb5d2-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="fb5d2-124">Způsobilost uživatele</span><span class="sxs-lookup"><span data-stu-id="fb5d2-124">User eligibility</span></span>

<span data-ttu-id="fb5d2-125">Zkontrolujte, zda je uživatel vytvořen v aplikaci Azure DevOps a zda má úroveň předplatného, která poskytuje přístup k plánům testování Azure.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="fb5d2-126">Licence Azure DevOps Test Plans je vyžadována pouze v případě, že uživatel vytvoří a spravuje testovací případy (tj. ne všichni uživatelé RSAT musí tuto licenci vlastnit).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="fb5d2-127">Informace o licenčních požadavcích naleznete v tématu [Licenční požadavky](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="fb5d2-128">Vytvoření nového projektu Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="fb5d2-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="fb5d2-129">RSAT využívá Azure DevOps pro účely testování a správy testovacích sad, vytváření sestav a zkoumání výsledků testovacího běhu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="fb5d2-130">Můžete použít existující projekt Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="fb5d2-131">Pokud je však existující projekt Azure DevOps nastaven tak, že má vlastní šablonu, obdržíte při synchronizaci testovacích případů z modulu Modelování podnikových procesů (BPM) do Azure DevOps chybu synchronizace VSTS (viz část [testování synchronizace z BPM do Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="fb5d2-132">Pokud byly pro vlastní šablonu použity následující doporučené postupy, můžete testovací případy synchronizovat do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="fb5d2-133">(Tyto doporučené postupy jsou uvedeny v chybové zprávě.)</span><span class="sxs-lookup"><span data-stu-id="fb5d2-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="fb5d2-134">Neodstraňujte žádné typy pracovních položek nebo integrovaná pole.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="fb5d2-135">Neodstraňujte žádný stav typu pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="fb5d2-136">Nepřidávejte žádná požadovaná pole k typu pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-136">Do not add any required fields to a work item type.</span></span>

![Chybová zpráva se seznamem doporučených postupů](./media/setup_rsa_tool_02.png)

<span data-ttu-id="fb5d2-138">V opačném případě doporučujeme vytvořit nový projekt Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="fb5d2-139">Další informace naleznete v tématu [Problematika synchronizace s BPM pomocí vlastní šablony procesu Azure DevOps](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/) (VSTS).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="fb5d2-140">Otevřete Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="fb5d2-141">Vyberte **Vytvořit projekt** v pravém horním rohu stránky Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Tlačítko Vytvořit projekt](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="fb5d2-143">Vyplňte následující pole a poté vyberte možnost **Vytvořit**:</span><span class="sxs-lookup"><span data-stu-id="fb5d2-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="fb5d2-144">**Název projektu**</span><span class="sxs-lookup"><span data-stu-id="fb5d2-144">**Project name**</span></span>
    - <span data-ttu-id="fb5d2-145">**Kontrola verzí** – Vyberte **Kontrola verzí Team Foundation**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="fb5d2-146">Všimněte si, že výchozí možnost **Git**není podporována.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="fb5d2-147">**Proces položky práce**</span><span class="sxs-lookup"><span data-stu-id="fb5d2-147">**Work item process**</span></span>

    ![Dialogové okno Vytvořit nový projekt](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="fb5d2-149">Vytvoření osobního přístupového tokenu</span><span class="sxs-lookup"><span data-stu-id="fb5d2-149">Create a personal access token</span></span>

<span data-ttu-id="fb5d2-150">V tomto kurzu budete používat Modelování podnikových procesů (BPM) k vytvoření testovacích případů a synchronizaci testovacích případů pomocí Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="fb5d2-151">Chcete-li synchronizovat BPM s Azure DevOps, budete potřebovat osobní přístupový token.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="fb5d2-152">Vyberte ikonu profilu v pravém horním rohu stránky pro váš projekt Azure DevOps a pak vyberte **zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Příkaz Zabezpečení](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="fb5d2-154">V levém podokně v části **Zabezpečení** vyberte možnost **Osobní přístupové tokeny**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="fb5d2-155">Poté vyberte možnost **Nový token**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-155">Then select **New Token**.</span></span>

    ![Tlačítko Nový token na kartě Osobní přístupové tokeny v uživatelském nastavení](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="fb5d2-157">Vyplňte následující pole a poté vyberte možnost **Vytvořit**:</span><span class="sxs-lookup"><span data-stu-id="fb5d2-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="fb5d2-158">**Název**</span><span class="sxs-lookup"><span data-stu-id="fb5d2-158">**Name**</span></span>
    - <span data-ttu-id="fb5d2-159">**Vypršení platnosti (UTC)** – vyberte **vlastní definovaný** a poté použijte výběr data k výběru posledního dostupného data.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="fb5d2-160">**Rozsahy** – vyberte **úplný přístup**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Vytvoření dialogového okna Nový token pro osobní přístup](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="fb5d2-162">Poznamenejte si vytvořený osobní přístupový token.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="fb5d2-163">Budete jeh potřebovat později při nastavení konfigurace RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Osobní přístupový token](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="fb5d2-165">Konfigurace projektu LCS</span><span class="sxs-lookup"><span data-stu-id="fb5d2-165">Configure the LCS project</span></span>

<span data-ttu-id="fb5d2-166">Pro vaši hlavní testovací knihovnu potřebujete projekt služby Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="fb5d2-167">Jako hlavní knihovnu pro testovací případy se používá služba Modelování podnikových procesů (BPM).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="fb5d2-168">BPM slouží ke správě a distribuci testovacích knihoven v rámci projektů LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="fb5d2-169">Testovací případy ve formě kihoven BPM vydává například partner společnosti Microsoft nebo nezávislý dodavatel softwaru (ISV).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="fb5d2-170">V BPM jsou testovací případy uspořádány podle obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="fb5d2-171">V BPM není definována objednávka nebo frekvence provádění testovacího průchodu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="fb5d2-172">Tyto detaily jsou spravovány v Azure DevOps, jak je popsáno dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="fb5d2-173">Pro svůj projekt LCS můžete použít existující zákaznickou implementaci nebo projekt partnera.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="fb5d2-174">Aktualizace jazyka LCS</span><span class="sxs-lookup"><span data-stu-id="fb5d2-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="fb5d2-175">Chcete-li v uživatelském rozhraní správně zobrazit obchodní procesy, je nutné nastavit upřednostňovaný jazyk LCS na **Angličtina (Spojené státy)**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="fb5d2-176">Přejděte na projekt implementace LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="fb5d2-177">Zvolte tlačítko **Nastavení** tlačítko (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Jazyková předvolba**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Příkazy v nabídce nastavení](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="fb5d2-179">V poli **upřednostňovaný jazyk** vyberte **Angličtina (USA)** a pak vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Karta Jazykové předvolby v nastavení uživatele](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="fb5d2-181">Konfigurace LCS pro připojení k projektu Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="fb5d2-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="fb5d2-182">Pokud jste dříve vytvořili nový projekt Azure DevOps, nakonfigurujte pro připojení k němu projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="fb5d2-183">Jinak, pokud je projekt LCS již připojen k projektu Azure DevOps, můžete přejít k následující části.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="fb5d2-184">Přejděte na projekt implementace LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="fb5d2-185">Vyberte tlačítko **Nabídka** a poté vyberte **nastavení projektu**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Příkaz Nastavení projektu](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="fb5d2-187">V levém podokně vyberte **Visual Studio Team Services** a pak vyberte možnost **Nastavit Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Nastavení karty Visual Studio Team Services](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="fb5d2-189">V poli Adresa URL **Azure DevOps** zadejte adresu URL webu Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="fb5d2-190">V poli **Osobní přístupový token** zadejte osobní přístupový token, který byl vytvořen dříve.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-191">Ačkoli VSTS je nyní znám jako Azure DevOps, chcete-li připojit LCS Azure DevOps k projektu, použijte starou adresu URL.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="fb5d2-192">Například Azure DevOps URL používaná v tomto kurzu je `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="fb5d2-193">Na následujícím obrázku je však zadána možnost `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Krok 1 v nastavení služby Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="fb5d2-195">Vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-195">Select **Continue**.</span></span>
6. <span data-ttu-id="fb5d2-196">V poli Projekt **Visual Studio Team Services** vyberte projekt VST na vybraném webu pro odkazování na projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="fb5d2-197">Pole **Šablona procesu** je nastaveno ve výchozím nastavení na **Agilní**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="fb5d2-198">Pro vlastní šablonu si prohlédněte doporučené postupy v oddílu [Vytvoření nového projektu Azure DevOps](#create-a-new-azure-devops-project)</span><span class="sxs-lookup"><span data-stu-id="fb5d2-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="fb5d2-199">Pak vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-199">Then select **Continue**.</span></span>

    ![Krok 2 v nastavení služby Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="fb5d2-201">Zkontrolujte nastavení a pak vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-201">Review your settings, and then select **Save**.</span></span>

    ![Krok 3 v nastavení služby Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="fb5d2-203">Výběrem možnosti **Autorizovat** udělte skupině LCS přístup ke konfigurovanému webu Azure DevOps a zapněte funkce, které lze integrovat s VSTS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Tlačítko Autorizovat](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="fb5d2-205">Zobrazí se pole se zprávou "Budete přesměrováni na externí web pro autorizaci služby LCS, aby se mohla za vás připojovat k Visual Studio Team Services.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="fb5d2-206">Pokračovat?"</span><span class="sxs-lookup"><span data-stu-id="fb5d2-206">Proceed?"</span></span> <span data-ttu-id="fb5d2-207">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-207">Select **Yes**.</span></span>

    ![Okno se zprávou](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="fb5d2-209">Zvolte **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-209">Select **Accept**.</span></span>

    ![Autorizace přístupu](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="fb5d2-211">Pokud jste oprávněni jako uživatel, uživatelské rozhraní by se mělo vrátit na stránku nastavení projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Oprávněný uživatel](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="fb5d2-213">Vytvoření nové knihovny BPM</span><span class="sxs-lookup"><span data-stu-id="fb5d2-213">Create a new BPM library</span></span>

1. <span data-ttu-id="fb5d2-214">Přejděte na projekt implementace LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="fb5d2-215">Vyberte tlačítko **Nabídka** a poté vyberte **Modelování podnikových procesů**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Příkaz Modelování podnikových procesů](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="fb5d2-217">Vyberte **Nová knihovna**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-217">Select **New library**.</span></span>

    ![Tlačítko Nová knihovna](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="fb5d2-219">Do pole **Název knihovny** zadejte název a pak vyberte možnost **vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="fb5d2-220">V tomto výukovém kurzu pojmenujte knihovnu BPM **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Dialogové okno Vytvořit novou knihovnu](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="fb5d2-222">Otevřete novou **knihovnu BPM** RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="fb5d2-223">Vyberte **příklad základního obchodního procesu** a poté na pravé straně vyberte **režim úprav**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Tlačítko Režim úprav](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="fb5d2-225">Změňte hodnotu v poli **Název** a v poli **Popis** na **Vytvořit produkt**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="fb5d2-226">Pak vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-226">Then select **Save**.</span></span>

    ![Pole Název a Popis](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="fb5d2-228">Prostředí</span><span class="sxs-lookup"><span data-stu-id="fb5d2-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="fb5d2-229">Požadavek na verzi</span><span class="sxs-lookup"><span data-stu-id="fb5d2-229">Version requirement</span></span>

<span data-ttu-id="fb5d2-230">Je požadován test nebo prostředí sandbox, na kterém běží verze 10.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="fb5d2-231">Pro zákazníky, kteří používají verzi 7.3, je podporována také Platform update 20 nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="fb5d2-232">Nástroje RSAT musí mít přístup k vašemu testovacímu prostředí prostřednictvím webového prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="fb5d2-233">Kritéria uživatele</span><span class="sxs-lookup"><span data-stu-id="fb5d2-233">User criteria</span></span>

<span data-ttu-id="fb5d2-234">Uživatel musí mít pro toto prostředí oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="fb5d2-235">Nastavení nápovědy pro připojení s LCS</span><span class="sxs-lookup"><span data-stu-id="fb5d2-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="fb5d2-236">Tento krok je nutný pro připojení s LCS, aby bylo možné ukládat záznamy úkolů do příslušné knihovny BPM v systému LCS prostřednictvím klienta.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="fb5d2-237">Spusťte klienta.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-237">Open the client.</span></span>
2. <span data-ttu-id="fb5d2-238">Přejděte do nabídky **Správa systému \> Nastavení \> systémových parametrů**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="fb5d2-239">Na kartě **Nápověda** v poli konfigurace nápovědy služby **Lifecycle Services** vyberte příslušný projekt LCS (**RSAT** pro tento kurz).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Pole konfigurace nápovědy služby Lifecycle Services na kartě Nápověda](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="fb5d2-241">Knihovny BPM jsou vyplněny v příslušném projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="fb5d2-242">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-242">Select **Save**.</span></span>
5. <span data-ttu-id="fb5d2-243">Chcete-li zobrazit aktualizovaný obsah nápovědy, bude pravděpodobně nutné aktualizovat prohlížeč.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Oznámení o aktualizaci prohlížeče](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="fb5d2-245">Zaznamenání úkolů</span><span class="sxs-lookup"><span data-stu-id="fb5d2-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="fb5d2-246">Zkontrolujte, zda jsou všechny záznamy úkolů v hlavním řídicím panelu zahájeny.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="fb5d2-247">Jednotlivé nahrávky uchovávejte tak, aby byly krátké, a zaměřujte se na jeden obchodní úkol, jako je vytvoření prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="fb5d2-248">Vytvoření záznamu o úkolu a jeho uložení do knihovny BPM</span><span class="sxs-lookup"><span data-stu-id="fb5d2-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="fb5d2-249">Vytvořte odpovídající záznam úkolu, který můžete připojit k jednoduchému obchodnímu procesu, který byl vytvořen v nové knihovně BPM.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="fb5d2-250">Spusťte klienta.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-250">Open the client.</span></span>
2. <span data-ttu-id="fb5d2-251">V hlavním řídicím panelu vyberte tlačítko **Nastavení** (symbol ozubeného kola) a poté vyberte položku **Záznamník úloh**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Příkazy v nabídce nastavení](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="fb5d2-253">Vyberte **Vytvořit nahrávku**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-253">Select **Create recording**.</span></span>

    ![Tlačítko Vytvořit nahrávku](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="fb5d2-255">Vyplňte pole **Název nahrávky** a **Popis nahrávky** a pak vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Pole Název nahrávky a Popis nahrávky](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="fb5d2-257">Zaznamenejte kroky pro vytvoření produktu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-257">Record the steps for creating a product.</span></span> <span data-ttu-id="fb5d2-258">Po dokončení ukončete záznam výběrem tlačítka **Zastavit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Postup při vytváření produktu](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="fb5d2-260">Vyberte **Uložit ve službách Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-260">Select **Save to Lifecycle Services**.</span></span>

    ![Možnosti uložení](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="fb5d2-262">Informace o knihovně jsou načítány z LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-262">Library information is loaded from LCS.</span></span>

    ![Indikátor pokroku](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="fb5d2-264">Vyberte knihovnu BPM pro přidružení k záznamu úlohy.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="fb5d2-265">V tomto kurzu vyberte knihovnu **RSAT** BPM, která byla vytvořena dříve, a vytvořte v ní obchodní proces **Vytvořit produkt**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="fb5d2-266">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-266">Then select **OK**.</span></span>

    ![Přidružení záznamu o úkolu ke knihovně BPM a obchodnímu procesu](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="fb5d2-268">Zobrazí se zpráva Uložení do služeb Lifecycle Services proběhlo úspěšně.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Zpráva o úspěšném uložení na LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="fb5d2-270">Chcete-li záznam úkolu uložit místně a poté jej odeslat do seznamu BPM pomocí LCS, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="fb5d2-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="fb5d2-271">Po dokončení záznamu vyberte možnost **Uložit do tohoto počítače**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Možnosti uložení](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="fb5d2-273">V oznamovacím panelu prohlížeče vyberte **Uložit** nebo **Uložit jako** a uložte soubor do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Oznamovací panel](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="fb5d2-275">Přejděte do knihovny **BPM** pro RSAT a vyberte obchodní proces, do kterého chcete uložit záznam úloh.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="fb5d2-276">Na kartě **Přehled** vyberte možnost **odeslat**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Tlačítko Odeslat](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="fb5d2-278">Vyberte **Procházet** a vyberte soubor .axtr, který jste uložili dříve.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="fb5d2-279">Poté vyberte **odeslat**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-279">Then select **Upload**.</span></span>

        ![Výběr souboru .axtr k odeslání](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="fb5d2-281">Testování synchronizace z BPM do Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="fb5d2-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="fb5d2-282">Nyní, když je záznam úkolu připojen k obchodnímu procesu, je nutné ověřit, že obchodní proces a přidružený záznam úkolu mohou být synchronizovány s Azure DevOps jako funkce a testovací případ (v uvedeném pořadí) pomocí funkce synchronizace VSTS na LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="fb5d2-283">Odpovídající typ pracovní položky, který je vytvořen v aplikaci Azure DevOps, se bude lišit v závislosti na šabloně procesu, kterou jste vybrali při konfiguraci projektu LCS pomocí modulu Azure DevOps, jak je popsáno v tématu [vytvoření nového projektu Azure DevOps](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="fb5d2-284">Přejděte do knihovny BPM a otevřete knihovnu **RSAT**, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="fb5d2-285">Vyberte tlačítko se třemi tečkami (**...**) a vyberte **Synchronizace VSTS**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![Příkaz synchronizace VSTS v nabídce se třemi tečkami](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="fb5d2-287">Po dokončení synchronizace VSTS se na levé straně zobrazí karta **Požadavky** a bude obsahovat odpovídající pracovní položku Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-288">Pracovní položka vytvořená v aplikaci Azure DevOps bude mít jako předponu názvu název knihovny BPM.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Karta Požadavky](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="fb5d2-290">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-290">Refresh the page.</span></span>
4. <span data-ttu-id="fb5d2-291">Vyberte tlačítko se třemi tečkami (**...**). Zobrazí se další možnost, **Synchronizace testovacích případů.**</span><span class="sxs-lookup"><span data-stu-id="fb5d2-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="fb5d2-292">Vyberte tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-292">Select this option.</span></span>

    ![Příkaz synchronizace VSTS v nabídce se třemi tečkami](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="fb5d2-294">Pokud možnost **Synchronizace testovacích případů** není k dispozici po aktualizaci stránky, přejděte na hlavní stránku pro BPM a vyberte možnost **Synchronizovat testovací případy** pro celou knihovnu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="fb5d2-295">Tímto způsobem efektivně vynutíte synchronizaci pro celou knihovnu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![Výběr testovacích případů synchronizace pro celou knihovnu](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="fb5d2-297">Po dokončení testovacích případů synchronizace je na kartě **požadavky** vytvořen nový testovací případ.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Nový testovací případ na kartě požadavky](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="fb5d2-299">Přejděte k projektu Azure DevOps a vyberte **Vývěsky \> Pracovní položky**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Příkaz pracovní položky v části Vývěsky](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="fb5d2-301">Ověřte, zda existuje pracovní položka a testovací případ, který jste vytvořili prostřednictvím synchronizace BPM.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Pracovní položka a testovací případ](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="fb5d2-303">Instalace a konfigurace RSAT</span><span class="sxs-lookup"><span data-stu-id="fb5d2-303">Install and Configure RSAT</span></span>

<span data-ttu-id="fb5d2-304">RSAT lze nainstalovat do libovolného počítače se systémem Windows 10, který se může připojit k prostředí pomocí webového prohlížeče (Internet Explorer nebo webu Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="fb5d2-305">Před zahájením instalace nové verze nástroje doporučujeme předchozí verzi odinstalovat.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="fb5d2-306">Instalace ověřovacího certifikátu</span><span class="sxs-lookup"><span data-stu-id="fb5d2-306">Install an authentication certificate</span></span>

<span data-ttu-id="fb5d2-307">Chcete-li povolit ověřování, je nutné vygenerovat a nainstalovat certifikát do stejného počítače, ve kterém je spuštěna RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="fb5d2-308">Generování certifikátu</span><span class="sxs-lookup"><span data-stu-id="fb5d2-308">Generate a certificate</span></span>

1. <span data-ttu-id="fb5d2-309">Chcete-li vygenerovat soubor certifikátu, otevřete okno prostředí Microsoft Windows PowerShell jako správce a spusťte následující příkaz.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="fb5d2-310">Otevřete Správce certifikátů zadáním **certlm. msc** v dialogovém okně **Spustit** a potvrďte, že je certifikát **Automatický certifikát testování D365** vytvořen v části **Osobní \>Certifikáty**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-311">Nezapomeňte zadat **Certlm. msc**, nikoli **certmgr. msc**, protože certifikáty jsou uloženy v místním počítači.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Certifikát D365 automatického testování](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="fb5d2-313">Klikněte pravým tlačítkem na databázi a poté vyberte možnost **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="fb5d2-314">Přejděte na **Důvěryhodné kořenové certifikační autority \>** Certifikáty.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Složka certifikáty pod složkou důvěryhodné kořenové certifikační autority](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="fb5d2-316">Výběrem možnosti **vložit** v nabídce **Akce** zkopírujte certifikát do umístění **důvěryhodných kořenových certifikačních autorit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Příkaz Vložit v nabídce Akce](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="fb5d2-318">Chcete-li získat kryptografický otisk nainstalovaného certifikátu, ale bez mezer nebo zvláštních znaků, otevřete okno prostředí Windows PowerShell jako správce a spusťte následující příkazy.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="fb5d2-319">Uložte kryptografický otisk, protože jej budete potřebovat později při aktualizaci souborů WIF pro aplikační objektový server (AOS) a nastavení konfigurace RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="fb5d2-320">Konfigurace počítače AOS tak, aby důvěřoval připojení</span><span class="sxs-lookup"><span data-stu-id="fb5d2-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="fb5d2-321">Pokud je prostředí prostředím úrovně 2 +, kryptografický otisk certifikátu musí být aktualizován v souboru WIF. config pro **všechny** počítače AOS pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="fb5d2-322">Navažte spojení s protokolem RDP (Remote Desktop Protocol) k počítači se serverem AOS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="fb5d2-323">Podrobné informace o přihlášení jsou k dispozici na stránce Podrobnosti prostředí v systému LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="fb5d2-324">Otevřete službu Microsoft Internet Information Services (IIS) a v seznamu webů vyhledejte **AOSService**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService v seznamu webů](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="fb5d2-326">Klikněte pravým tlačítkem na **Prozkoumat** a otevřete složku **\<Drive\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="fb5d2-327">Vyhledejte soubor **wif. config**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-327">Find the **wif.config** file.</span></span>

    ![Soubor wif. config ve složce WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="fb5d2-329">Aktualizujte **soubor wif.config** přidáním nového záznamu autority pro váš certifikát a název úřadu, jak je uvedeno v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="fb5d2-330">Pokud více uživatelů používá stejnou aplikaci, musí každý uživatel generovat samostatné kryptografické otisky a každý z těchto kryptografických otisků musí být přidán v části **\<klíče\>**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="fb5d2-331">Pokud existuje více než jeden počítač se serverem AOS, zopakujte kroky 3 až 4 pro každý další počítač.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-332">Na rozdíl od prostředí starší úrovně 2 jsou nová prostředí s vrstvou 2 nasazena se dvěma instancemi AOS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="fb5d2-333">Spusťte příkaz **iisreset** ve všech počítačích AOS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-334">Pokud nemáte oprávnění správce ke spuštění příkazu **iisreset** v počítači s úrovní 1, vyberte na stránce Podrobnosti prostředí v nabídce LCS možnost udržovat > restartovat služby.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="fb5d2-335">Prostředí vrstvy 2+</span><span class="sxs-lookup"><span data-stu-id="fb5d2-335">Tier 2+ environment</span></span>

<span data-ttu-id="fb5d2-336">Pokud se používá vrstva 2 + (standardní prostředí sandbox pro příjem testů nebo vyšší) prostředí, ověřte nebo nastavte následující nastavení registru v počítači, ve kterém je nainstalována sada RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="fb5d2-337">Tento krok je požadován, protože pomáhá předcházet chybám ověřování a RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="fb5d2-338">Instalace RSAT</span><span class="sxs-lookup"><span data-stu-id="fb5d2-338">Install RSAT</span></span>

1. <span data-ttu-id="fb5d2-339">Přejděte na <https://www.microsoft.com/download/details.aspx?id=57357> a vyberte **Stáhnout**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="fb5d2-340">Vyberte všechny soubory a pak vyberte možnost **Další**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-340">Select all the files, and then select **Next**.</span></span>

    ![Výběr všech souborů](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="fb5d2-342">Poklepáním na balíček MSI spusťte instalační program.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="fb5d2-343">Po dokončení instalace vyberte možnost **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![Instalační soubor služby RSAT](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="fb5d2-345">Instalace ovladačů a prohlížeče Selenium</span><span class="sxs-lookup"><span data-stu-id="fb5d2-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="fb5d2-346">Ve starších verzích aplikace RSAT bylo nutné instalovat ovladač a prohlížeč Selenium.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="fb5d2-347">Již není nutné instalovat tyto ovladače, protože jsou instalovány automaticky.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="fb5d2-348">Při prvním spuštění aplikace RSAT se zobrazí výzva k automatickému stažení a instalaci programu Selenium.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="fb5d2-349">Další informace naleznete v tématu[Konfigurace RSAT](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="fb5d2-350">Před spuštěním testovacího případu budete vyzváni k automatickému stažení a instalaci ovladače prohlížeče, který odpovídá výchozímu prohlížeči, který je vybrán v konfiguraci nástroje RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="fb5d2-351">Další informace naleznete v části [Případy zavádění a spouštění testovacích případů](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="fb5d2-352">Začínáme s aplikací RSAT</span><span class="sxs-lookup"><span data-stu-id="fb5d2-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="fb5d2-353">Vytvoření testovacího plánu a sad testů</span><span class="sxs-lookup"><span data-stu-id="fb5d2-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="fb5d2-354">Přejděte k projektu Azure DevOps a vyberte možnost **testovací plány**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Příkaz Testovací plány](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="fb5d2-356">Vyberte **Nový testovací plán**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-356">Select **New Test Plan**.</span></span>

    ![Tlačítko Nový testovací plán](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="fb5d2-358">Zadejte hodnotu do pole **Název** a vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="fb5d2-359">V tomto výukovém kurzu pojmenujte testovací plán **Testovací plán testování RSAT**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Dialogové okno Nový testovací plán](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="fb5d2-361">Vyberte znak (**+**) a pak vyberte **Statická sada** k vytvoření statické sady v rámci nového testovacího plánu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="fb5d2-362">Pojmenujte novou sadu **T01 – Make to Stock**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-363">Můžete také vytvořit sadu založenou na dotazech, pokud chcete, aby nové testovací případy z BPM byly automaticky vyžádány v sadě pro RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Vytvoření statické sady](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="fb5d2-365">Připojení testovacích případů k testovacím sadám</span><span class="sxs-lookup"><span data-stu-id="fb5d2-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="fb5d2-366">Vyberte **Přidat existující** napravo pro přidání existujících testovacích případů do testovací sady.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Tlačítko Přidat existující aktivitu](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="fb5d2-368">Na stránce **Přidat testovací případy do sady** vyberte možnost **spustit dotaz** a pak vyberte testovací případ, který má být přidán do sady testů.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="fb5d2-369">V tomto kurzu vyberte testovací případ **Vytvořit nový případ**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="fb5d2-370">Poté vyberte možnost **Přidat testovací případy** v pravém dolním rohu stránky (toto tlačítko není zobrazeno na následujícím obrázku).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Tlačítko Spustit dotaz](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="fb5d2-372">Testovací případ se přidá do sady **T01-Make to Stock**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testovací případ přidaný do sady testů](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="fb5d2-374">Konfigurovat frontu RSAT</span><span class="sxs-lookup"><span data-stu-id="fb5d2-374">Configure RSAT</span></span>

1. <span data-ttu-id="fb5d2-375">Otevřete RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-375">Open RSAT.</span></span>

    ![Ikona RSAT](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="fb5d2-377">Zobrazí se varovná zpráva s informací: Regression Suite Automation Tool vyžaduje Selenium, chcete ji automaticky stáhnout a nainstalovat?</span><span class="sxs-lookup"><span data-stu-id="fb5d2-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="fb5d2-378">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-378">Select **Yes**.</span></span>

    ![Zpráva s upozorněním](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="fb5d2-380">Vyberte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu a potom v zobrazeném dialogovém okně vyplňte následující pole:</span><span class="sxs-lookup"><span data-stu-id="fb5d2-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="fb5d2-381">**Azure DevOps Url** – Zadejte adresu URL projektu Azure DevOps, například `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="fb5d2-382">**Přístupový token** – zadejte přístupový token, který umožňuje nástroji připojení k Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="fb5d2-383">Použijte osobní přístupový token, který jste vytvořili dříve v tomto kurzu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="fb5d2-384">Další informace naleznete v tématu [Ověření přístupu s osobními přístupovými tokeny](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="fb5d2-385">**Název projektu** – vyberte název projektu Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="fb5d2-386">**Testovací plán** – vyberte testovací plán Azure DevOps, který obsahuje vaše testovací případy.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="fb5d2-387">Další informace naleznete v tématu [Vytvoření testovacích plánů a sad testů](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="fb5d2-388">Po výběru testovacího plánu vyberte možnost **Testovat připojení** pro otestování připojení k aplikaci Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="fb5d2-389">**Název hostitele** – zadejte název hostitele testovacího prostředí, například **\<myaos\>. cloudax.dynamics.com.**</span><span class="sxs-lookup"><span data-stu-id="fb5d2-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="fb5d2-390">Nezahrnujte předponu **https://** nebo **http://**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="fb5d2-391">**Název hostitele SOAP** – zadejte název hostitele SOAP pro testovací prostředí.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="fb5d2-392">Název hostitele SOAP se obvykle shoduje s názvem hostitele, ale má příponu **SOAP**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="fb5d2-393">Zde je příklad: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="fb5d2-394">Nezahrnujte předponu **https://** nebo **http://**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fb5d2-395">Chcete-li najít název hostitele a název hostitele SOAP, spusťte Správce služby IIS, klikněte pravým tlačítkem na **Weby \> AOSService** a pak vyberte **Upravit vazby**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="fb5d2-396">Hodnoty ve sloupci **Název hostitele** poskytují název hostitele a název hostitele SOAP (název hostitele SOAP má v adrese URL příponu **soap**).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Název hostitele a název hostitele SOAP ve sloupci Název hostitele](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="fb5d2-398">**Uživatelské jméno správce** – zadejte e-mailovou adresu uživatele správce v testovacím prostředí.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="fb5d2-399">**Kryptografický otisk** – zadejte kryptografický otisk ověřovacího certifikátu, jak je popsáno výše v tomto výukovém kurzu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="fb5d2-400">**Pracovní adresář** – zadejte umístění složky pro ukládání souborů pro automatizaci testů, jako jsou například testovací datové soubory aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="fb5d2-401">Zadejte nebo vyberte například **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fb5d2-402">Obsahuje-li název složky mezery, spuštění se nezdaří, protože složku nelze najít.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="fb5d2-403">Jedná se o známý problém, který by měl být opraven v nejnovější verzi nástroje.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="fb5d2-404">**Výchozí prohlížeč** – Vyberte **Internet Explorer** nebo **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="fb5d2-405">Zkontrolujte, zda byly nainstalovány příslušné ovladače prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="fb5d2-406">**Časový limit testovacího běhu** – určuje časový limit (v minutách) pro testovací běh.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="fb5d2-407">Po uplynutí časového limitu budou všechna aktivní okna zavřena a nevyřízené testovací případy selžou.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="fb5d2-408">**Časový limit akce testu** – toto pole určuje časový limit (v minutách) pro požadavky serveru prostředí Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="fb5d2-409">Obvykle by měla být dostatečná výchozí hodnota (2 minuty).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="fb5d2-410">V případě pomalejšího prostředí však může být vhodné hodnotu zvýšit, pokud dojde k chybám, které souvisejí s časovým limitem.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="fb5d2-411">**Název společnosti** – zadejte název společnosti, který má být použit jako výchozí společnost při vytváření souborů parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="fb5d2-412">Společnost lze později změnit úpravou souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Dialogové okno Nastavení](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="fb5d2-414">Vyberte **Použít** k použití a uložení nastavení.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="fb5d2-415">Chcete-li uložit aktuální nastavení do konfiguračního souboru v počítači, vyberte možnost **Uložit jako**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="fb5d2-416">Chcete-li obnovit nastavení z konfiguračního souboru v počítači, vyberte možnost **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="fb5d2-417">Zvolte **Zavřít** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="fb5d2-418">Nahrání a spuštění testovacích případů</span><span class="sxs-lookup"><span data-stu-id="fb5d2-418">Load and run test cases</span></span>

1. <span data-ttu-id="fb5d2-419">Výběrem **Load** načtete **testovací plán RSAT** z projektu Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Tlačítko Odeslat](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="fb5d2-421">Vyberte testovací případ **Vytvořit nový produkt** z testovací sady a poté vyberte **Nový \> Generovat spuštění testu a soubory parametrů**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Příkaz Generovat spuštění testu a soubory parametrů v nabídce Nový](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="fb5d2-423">Soubor parametrů **aplikace Excel je vytvořen v místní složce, kterou jste zadali v konfiguraci RSAT (například C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Byl vytvořen soubor parametrů aplikace Excel.](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="fb5d2-425">Chcete-li uložit soubory parametrů, vyberte možnost **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="fb5d2-426">Soubory automatizace všech vybraných testovacích případů jsou odeslány do Azure DevOps aplikace pro budoucí použití.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="fb5d2-427">(Tyto soubory zahrnují testovací soubory parametrů aplikace Excel.)</span><span class="sxs-lookup"><span data-stu-id="fb5d2-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="fb5d2-428">Tímto způsobem můžete vybrat **Odeslat** pro načtení souborů parametrů (a automatizačních souborů) přímo z testovacího případu Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="fb5d2-429">Soubory parametrů není nutné znovu vygenerovat.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="fb5d2-430">Tento přístup bude důležitý později, když chcete zachovat změny v souboru parametrů a nechcete, aby byly přepsány.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="fb5d2-431">Chcete-li ověřit, zda jsou soubory automatizace a soubory parametrů uloženy do Azure DevOps, přejděte na projekt Azure DevOps, vyberte **Vývěsky \> Položky práce** a pak vyberte testovací případ **Vytvořit nový produkt**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="fb5d2-432">Na kartě **přílohy** se zobrazí čtyři soubory:</span><span class="sxs-lookup"><span data-stu-id="fb5d2-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="fb5d2-433">**.cs** – C\# soubor automatizace</span><span class="sxs-lookup"><span data-stu-id="fb5d2-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="fb5d2-434">**. dll** – kompilovaný soubor automatizace jako sestava</span><span class="sxs-lookup"><span data-stu-id="fb5d2-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="fb5d2-435">**.xlsx** – soubor parametrů Excel</span><span class="sxs-lookup"><span data-stu-id="fb5d2-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="fb5d2-436">**.xml** – soubor záznamů</span><span class="sxs-lookup"><span data-stu-id="fb5d2-436">**.xml** – Recording file</span></span>

    ![Soubory na kartě Přílohy](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="fb5d2-438">Vyberte testovací případ, který se má spustit, a pak vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-439">Před spuštěním testovacích případů v případě, že používáte prohlížeč Internet Explorer, zkontrolujte, zda je rozlišení plochy nastaveno na **100%** v **nastavení zobrazení systému Windows \> Měřítko a rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="fb5d2-440">Pokud toto nastavení nelze změnit u virtuálního počítače (VM), změňte jej na straně klienta (laptop), ze kterého se pokoušíte získat přístup k virtuálnímu počítači.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="fb5d2-441">Nastavení rozlišení pak zdědí nastavení zobrazení virtuálního počítače.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Rozlišení plochy je nastaveno na 100 %](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="fb5d2-443">Nejsou-li ovladače prohlížeče v systému nainstalovány, zobrazí se varovná zpráva s upozorněním, že tato operace vyžaduje ovladač \<browser name\>.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="fb5d2-444">Chcete ho nyní automaticky stáhnout a nainstalovat?</span><span class="sxs-lookup"><span data-stu-id="fb5d2-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="fb5d2-445">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-445">Select **Yes**.</span></span>

    ![Zpráva s upozorněním z aplikace Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Zpráva s upozorněním z aplikace Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="fb5d2-448">Pokud používáte prohlížeč Chrome a dostanete chybovou zprávu, že relace nebyla vytvořena, protože verze prohlížeče Chrome není správná, stáhněte si nejnovější ovladač Chrome ze stránek <http://chromedriver.chromium.org/downloads> do složky **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Chybová zpráva aplikace Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="fb5d2-450">Testovací případ je spuštěn a pole **Výsledek** je aktualizováno.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Indikátor pokroku](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="fb5d2-452">Pokud jste postupovali v tomto kurzu tak, jak je zapsán, testovací případ **Vytvořit nový produkt** se nezdaří, protože záznam úloh pro vytvoření produktu uložil název produktu jako pevně zakódovanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="fb5d2-453">Pokud znovu spustíte stejný testovací případ, měli byste obdržet chybovou zprávu, protože produkt již existuje.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Pole výsledku je nastaveno na nezdařilo se.](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="fb5d2-455">Zobrazení výsledků testu</span><span class="sxs-lookup"><span data-stu-id="fb5d2-455">View the test results</span></span>

1. <span data-ttu-id="fb5d2-456">Poklepejte na neúspěšný testovací případ.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="fb5d2-457">Dostanete chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-457">You receive an error message.</span></span>

    ![Chybová zpráva](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="fb5d2-459">Vyberte **Detaily** k zobrazení celé chybové zprávy.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-459">Select **Details** to view the whole error message.</span></span>

    ![Celá chybová zpráva](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="fb5d2-461">Chcete-li zobrazit podrobnou verzi chybové zprávy v Azure DevOps, vyberte **Otevřít v Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="fb5d2-462">V Azure DevOps můžete zobrazit stav testovacího případu a podrobnou chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Podrobná chybová zpráva v Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="fb5d2-464">Chcete-li zobrazit výsledky testu přímo v projektu Azure DevOps, přejděte na **Test Plans \> Test Plans \> Runs**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="fb5d2-465">Dvakrát klikněte na testovací běh, pro který chcete zobrazit podrobné informace.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-465">Double-click the test run that you want to see more details for.</span></span>

    ![Seznam testovacích běhů v Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="fb5d2-467">Na **Souhrn spuštění** je uvedeno, že testovací případ selhal, ale neposkytuje skutečnou chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="fb5d2-468">Chcete-li zobrazit podrobnou chybovou zprávu, vyberte kartu **Výsledky testu**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Karta Spustit souhrn](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="fb5d2-470">Na kartě **Výsledky testu** jsou uvedeny informace o testovacím případu spolu s výstupem a chybovou zprávou.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Karta Výsledky testu](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="fb5d2-472">Poklepáním na příslušný záznam zobrazíte podrobnou chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Podrobná chybová zpráva](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="fb5d2-474">Všechny chybové zprávy jsou k dispozici také místně ve složce **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="fb5d2-475">Výsledky testovacího běhu můžete exportovat také z úrovně plánu testování výběrem možnosti **Export**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Export testovacího plánu](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="fb5d2-477">Úprava souboru parametrů aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="fb5d2-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="fb5d2-478">Otevřete RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-478">Open RSAT.</span></span>
2. <span data-ttu-id="fb5d2-479">Vyberte testovací případ a poté výběrem možnosti **Upravit** otevřete soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="fb5d2-480">Na listu **EcoResProductCreate** si povšimněte, že hodnota pole **Číslo produktu** je pevně kódována.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="fb5d2-481">Chcete-li znovu spustit testovací případ, je nutné toto pole aktualizovat na nové číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="fb5d2-482">Chcete-li pro každý běh generovat jedinečné číslo produktu bez nutnosti znovu otevřít soubor parametrů aplikace Excel a ručně aktualizovat číslo produktu, použijte následující vzorec aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="fb5d2-483">Kromě karty **obecné** obsahuje soubor parametrů aplikace Excel kartu data pro každou stránku formuláře pro návštěvy testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Pole Číslo produktu](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="fb5d2-485">Zvolte **Uložit** a pak zavřete sešit aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="fb5d2-486">Výběrem možnosti **Nahrát** uložte soubor parametrů aplikace Excel do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Zpráva o úspěšném odeslání](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="fb5d2-488">Pokud chcete spustit testovací případy v určitém kontextu uživatele, zadejte do pole **Zkušební uživatel** na kartě **Obecné** souboru parametrů Excel ID e-mailu uživatele.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="fb5d2-489">V nejnovější verzi aplikace RSAT bylo aktualizováno rozložení polí v souboru parametrů aplikace Excel, ale koncept zůstává stejný.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Pole Testovací uživatel](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="fb5d2-491">Ověření výsledků</span><span class="sxs-lookup"><span data-stu-id="fb5d2-491">Validate the results</span></span>

- <span data-ttu-id="fb5d2-492">Výběrem **Spustit** znovu spusťte testovací případ a ověřte, zda byl testovací případ úspěšný.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="fb5d2-493">Výsledky testů můžete zobrazit způsobem popsaným v části [Zobrazení výsledků testu](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Pole výsledku je nastaveno na Úspěch](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="fb5d2-495">Zřetězení testovacích případů</span><span class="sxs-lookup"><span data-stu-id="fb5d2-495">Chaining of test cases</span></span>

<span data-ttu-id="fb5d2-496">Jedním klíčovým prvkem nástroje RSAT je zřetězení testovacích případů (tj. schopnost testu předat hodnoty jiným testům).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="fb5d2-497">Testovací případy se spouštějí podle jejich definovaného pořadí v testovacím plánu Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="fb5d2-498">(Tuto objednávku lze také aktualizovat samotným testovacím nástrojem.) Chcete-li tedy předávat proměnné z jednoho testovacího případu do jiného, je velmi důležité, aby testy byly ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="fb5d2-499">V tomto oddílu vytvoříte uloženou proměnnou v prvním testovacím případu, vytvoříte druhý testovací případ a předáte uloženou proměnnou z prvního testovacího případu do druhého testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="fb5d2-500">Testovací případy pak spustíte jako zřetězený testovací případ na kartě RSAT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="fb5d2-501">Úprava existujícího záznamu úlohy za účelem vytvoření uložené proměnné</span><span class="sxs-lookup"><span data-stu-id="fb5d2-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="fb5d2-502">Spusťte klienta.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-502">Open the client.</span></span>
2. <span data-ttu-id="fb5d2-503">Vyberte tlačítko **Nastavení** (symbol ozubeného kola) a poté vyberte položku **Záznamník úloh**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="fb5d2-504">Vyberte **Upravti záznam**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-504">Select **Edit Recording**.</span></span>

    ![Tlačítko Upravit záznam](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="fb5d2-506">Vyberte **Otevřít ze služeb Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="fb5d2-506">Select **Open from Lifecycle Services**.</span></span>

    ![Tlačítko Otevřít ze služeb Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="fb5d2-508">Vyberte **Vybrat knihovnu služeb Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Tlačítko Vybrat knihovnu služeb Lifecycle Services](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="fb5d2-510">Knihovny BPM jsou načítány z LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-510">BPM libraries are loaded from LCS.</span></span>

    ![Indikátor pokroku](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="fb5d2-512">Po načtení knihoven BPM z LCS vyberte knihovnu BPM **RSAT** a obchodní proces **Vytvořit nový produkt**, ke kterému byl záznam úkolu přidružen.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="fb5d2-513">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-513">Then select **OK**.</span></span>

    ![Výběr knihovny BPM a obchodního procesu](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="fb5d2-515">Název příslušného záznamu úkolu je zadán do pole název **název záznamu**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="fb5d2-516">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-516">Select **Start**.</span></span>

    ![Název záznamu úlohy v poli Název úlohy](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="fb5d2-518">Přejděte na **Správa informací o produktu \> Produkty** a vyberte **Nový** k otevření stránky, kde byla pořízena původní nahrávka úlohy **Vytvořit produkt**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="fb5d2-519">Vyberte **Vložit krok**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-520">Nový krok je vložen **za** krok, který jste vybrali v podokně.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Tlačítko Vložit krok](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="fb5d2-522">Klepněte pravým tlačítkem myši na pole **Číslo produktu** a vyberte **Záznamník úloh \> Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Příkaz Kopírovat](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="fb5d2-524">V podokně je přidán nový krok.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-524">A new step is added in the pane.</span></span> <span data-ttu-id="fb5d2-525">Poznamenejte si hodnotu v poli **Číslo produktu**, protože ji budete potřebovat později.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Přidán nový krok](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="fb5d2-527">Vyberte **Dokončeny úpravy**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="fb5d2-528">Vyberte **Uložit do Lifecycle Services** a přiřaďte nový záznam úkolu ke stejné knihovně BPM a obchodnímu procesu, k němuž byl záznam původního úkolu přidružen.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="fb5d2-529">Další informace naleznete v tématu [Vytvoření záznamu úlohy a jeho uložení do oddílu knihovny BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="fb5d2-530">Přejděte do knihovny BPM a vyberte **Synchronizovat testovací případy** pro přepis záznamu úloh připojenému k testovacímu případu v Azure DevOps, jak je popsáno v části [Testování synchronizace z BPM do Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="fb5d2-531">Otevřete RSAT a vyberte **Načíst**, chcete-li znovu načíst všechny testovací případy v sadě testů.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="fb5d2-532">Je nutné znovu vygenerovat soubory automatizace a parametrů pro příslušný testovací případ výběrem testovacího případu a následným výběrem **Nový \> Generovat soubory spuštění testu a parametry**, jak je popsáno v části [Načtení a spuštění testovacích případů](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-533">Pokud byl soubor parametrů aplikace Excel ponechán otevřený, obnovení se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="fb5d2-534">Proto se ujistěte, že soubor parametrů aplikace Excel pro testovací případ je uzavřen před tím, než vygenerujete nový soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="fb5d2-535">Vyberte **Upravit** k otevření nového souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="fb5d2-536">Bude zobrazena nová **uložená proměnná** položka na řádku 9.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="fb5d2-537">Tato proměnná **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, je uložena v souboru XML záznamu úkolu a lze ji použít v následných testech.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Záznam uložené proměnné](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="fb5d2-539">Vytvoření nového testovacího případu</span><span class="sxs-lookup"><span data-stu-id="fb5d2-539">Create a new test case</span></span>

1. <span data-ttu-id="fb5d2-540">Přejděte do knihovny **RSAT** BPM.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="fb5d2-541">Vyberte **příklad obchodního procesu podpory** a poté na pravé straně vyberte **režim úprav**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="fb5d2-542">Změňte hodnotu v poli **Název** a v poli **Popis** na **Vydat produkt**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="fb5d2-543">Pak vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-543">Then select **Save**.</span></span>

    ![Název a popis se změnil na Uvolnění produktu.](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="fb5d2-545">Vytvoření nového záznamu úlohy s funkcí ověření</span><span class="sxs-lookup"><span data-stu-id="fb5d2-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="fb5d2-546">Vytvořte záznam úloh pro uvolnění produktu, který byl vytvořen dříve, do právnické osoby USRT.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="fb5d2-547">Další informace naleznete v tématu [Vytvoření záznamu úlohy a jeho uložení do oddílu knihovny BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb5d2-548">U zřetězených testovacích případů doporučujeme, abyste vyhledali nebo vyfiltroval záznam, který požadujete, *ručním zadáním hodnoty pole*.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="fb5d2-549">Tímto způsobem může nástroj určit záznam, proti němuž je akce provedena v následném testovacím případu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Nový záznam úlohy s funkcí ověření](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="fb5d2-551">Jak ukazuje předchozí ilustrace, po nalezení produktu pomocí rychlého filtru, ale před tím, než vyberete **uvolněné produkty**, ověřte hodnotu pole **číslo produktu**, abyste se ujistili, že ID produktu je ID produktu, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="fb5d2-552">Chcete-li hodnotu ověřit, klepněte pravým tlačítkem myši na pole **Číslo produktu** a vyberte **Záznamník úloh \> Ověřit \> Aktuální hodnota**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Ověření aktuální hodnoty](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="fb5d2-554">Uložení záznamu úlohy do BPM</span><span class="sxs-lookup"><span data-stu-id="fb5d2-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="fb5d2-555">Po dokončení záznamu vyberte možnost **Uložit do Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Možnosti uložení](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="fb5d2-557">Informace o knihovně jsou načítány z LCS.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-557">Library information is loaded from LCS.</span></span>

    ![Indikátor pokroku](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="fb5d2-559">Vyberte knihovnu BPM pro přidružení k záznamu úlohy.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="fb5d2-560">V tomto kurzu vyberte knihovnu **RSAT** BPM, která byla vytvořena dříve, a vytvořte v ní obchodní proces **Uvolnit produkt**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="fb5d2-561">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="fb5d2-562">Synchronizace BPM v Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="fb5d2-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="fb5d2-563">Přejděte do knihovny BPM a otevřete knihovnu **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="fb5d2-564">Vyberte **Synchronizace VSTS** a **Synchronizovat testovací případy**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="fb5d2-565">Další informace naleznete v tématu [Testování synchronizace z BPM do Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="fb5d2-566">Po dokončení synchronizace se nová položka práce a odpovídající testovací případ pro obchodní proces **Uvolnit produkt** objeví v Azure DevOps v části **Vývěsky \> Položky práce**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="fb5d2-567">Přidání novéno testovacího případu do existující sady testů</span><span class="sxs-lookup"><span data-stu-id="fb5d2-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="fb5d2-568">Přejděte na **Testovací plány \> Testovací plány** a vyberte plán **RSAT Test Plan**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="fb5d2-569">Vyberte **Přidat existující**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="fb5d2-570">Na stránce **Přidat testovací případy do sady** vyberte možnost **spustit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="fb5d2-571">Vyberte nový testovací případ, který byl vytvořen pro **uvolnění produktu** a poté vyberte možnost **přidat testovací případy** v pravém dolním rohu stránky (toto tlačítko není zobrazeno na následujícím obrázku).</span><span class="sxs-lookup"><span data-stu-id="fb5d2-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Stránka Přidat testovací případy do sady](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="fb5d2-573">Sada testů nyní obsahuje dva testovací případy.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-573">The test suite now has two test cases.</span></span>

    ![Dva testovací případy v sadě testů](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="fb5d2-575">Nahrání testovacích případů do RSAT</span><span class="sxs-lookup"><span data-stu-id="fb5d2-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="fb5d2-576">Otevřete okno RSAT a vyberte **Načíst**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="fb5d2-577">Dojde k načtení testovacích případů a obdržíte upozornění, že tato akce přepíše soubory testovacích dat aplikace Excel, místní změny budou ztraceny.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="fb5d2-578">Chcete pokračovat?</span><span class="sxs-lookup"><span data-stu-id="fb5d2-578">Do you want to proceed?"</span></span> <span data-ttu-id="fb5d2-579">Výběrem **Ano** aktualizujete soubory parametrů aplikace Excel v místním systému, ale nepoužijete soubory parametrů aplikace Excel v Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Zpráva s upozorněním](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="fb5d2-581">Oba testovací případy se načítají spolu se souborem parametrů aplikace Excel pro první testovací případ.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="fb5d2-582">Protože jste vybrali **Odeslat** při posledním spuštění, budou soubory parametrů načteny z Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Testovací případy odeslány](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="fb5d2-584">Vyberte pouze druhý testovací případ a poté vyberte **Nový \> Generovat soubory parametrů spuštění testu a parametrů**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="fb5d2-585">Úprava souboru parametrů aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="fb5d2-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="fb5d2-586">Vyberte jenom druhý testovací případ a poté výběrem možnosti **Upravit** otevřete odpovídající soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="fb5d2-587">Zkopírujte uloženou proměnnou **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (viz [Modifikace existujícího záznamu úlohy k vytvoření uložené proměnné](#modify-an-existing-task-recording-to-create-a-saved-variable)) z prvního testovacího případu do všech polí, kde se používá číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="fb5d2-588">V takovém případě zkopírujte proměnnou do polí **Číslo produktu** a **Ověřit číslo produktu** v listu **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Pole Číslo produktu a Ověřit číslo produktu](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="fb5d2-590">Proměnné lze mezi testy přenášet pouze během jednoho testovacího běhu.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="fb5d2-591">Názvy proměnných se musí přesně shodovat.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="fb5d2-592">Zvolte **Uložit** a pak zavřete sešit aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="fb5d2-593">Vyberte **Nahrát** pro uložení provedených změn do souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="fb5d2-594">Spuštění zřetězených testovacích případů</span><span class="sxs-lookup"><span data-stu-id="fb5d2-594">Run the chained test cases</span></span>

1. <span data-ttu-id="fb5d2-595">Vyberte oba testovací případy a pak vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="fb5d2-596">Ověřte, zda oba testovací případy byly úspěšné.</span><span class="sxs-lookup"><span data-stu-id="fb5d2-596">Verify that both test cases have passed.</span></span>

    ![Pole výsledku nastavené na úspěch pro testovací případy](./media/setup_rsa_tool_105.png)
