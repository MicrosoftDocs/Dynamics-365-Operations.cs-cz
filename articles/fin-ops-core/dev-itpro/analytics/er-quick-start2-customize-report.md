---
title: Úprava formátu elektronického výkaznictví a vytvoření vlastního elektronického dokladu
description: Toto téma vysvětluje, jak upravit formát elektronického výkaznictví (ER) od společnosti Microsoft tak, aby generoval vlastní elektronické doklady.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60b318ab03bc1bb47517a206e8b2afd9c13cf273
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891712"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="9eb38-103">Úprava formátu elektronického výkaznictví a vytvoření vlastního elektronického dokladu</span><span class="sxs-lookup"><span data-stu-id="9eb38-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9eb38-104">Postupy v tomto tématu vysvětlují, jak může uživatel v roli administrátora systému nebo v role funkčního konzultanta elektronického výkaznictví provádět tyto úkoly:</span><span class="sxs-lookup"><span data-stu-id="9eb38-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="9eb38-105">Konfigurace parametrů pro [rámec elektronického výkaznictví (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9eb38-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="9eb38-106">Import konfigurace ER od společnosti Microsoft, jež se používají ke generování souboru platby, když je zpracovávána [platba dodavateli](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9eb38-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="9eb38-107">Vytvoření vlastní verze konfigurace standardního formátu ER od společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9eb38-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="9eb38-108">Úprava vlastní konfiguraci formátu ER tak, aby byly generovány soubory plateb, jež splňují požadavky konkrétní banky.</span><span class="sxs-lookup"><span data-stu-id="9eb38-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="9eb38-109">Převzetí změn provedených ve standardní konfiguraci formátu ER do vlastní konfiguraci formátu ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="9eb38-110">Všechny následující procedury lze provést ve společnosti **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="9eb38-111">Není nutné žádné kódování.</span><span class="sxs-lookup"><span data-stu-id="9eb38-111">No coding is required.</span></span>

- [<span data-ttu-id="9eb38-112">Konfigurace architektury ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="9eb38-113">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="9eb38-114">Aktivace poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="9eb38-115">Kontrola seznamu poskytovatelů konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="9eb38-116">Přidání nového poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="9eb38-117">Aktivace poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="9eb38-118">Import standardních konfigurací formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="9eb38-119">Import standardních konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="9eb38-120">Kontrola importovaných konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="9eb38-121">Příprava platby dodavateli ke zpracování</span><span class="sxs-lookup"><span data-stu-id="9eb38-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="9eb38-122">Přidejte údajů o bance k účtu dodavatele</span><span class="sxs-lookup"><span data-stu-id="9eb38-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="9eb38-123">Zadání platby dodavateli</span><span class="sxs-lookup"><span data-stu-id="9eb38-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="9eb38-124">Zpracování platby dodavateli pomocí standardního formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="9eb38-125">Nastavení způsobu elektronické platby</span><span class="sxs-lookup"><span data-stu-id="9eb38-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="9eb38-126">Zpracování platby dodavateli</span><span class="sxs-lookup"><span data-stu-id="9eb38-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="9eb38-127">Přizpůsobení standardního formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="9eb38-128">Vytvoření vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="9eb38-129">Úprava vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="9eb38-130">Označení vlastního formátu jako spustitelného</span><span class="sxs-lookup"><span data-stu-id="9eb38-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="9eb38-131">Zpracování platby dodavateli pomocí vlastního formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="9eb38-132">Nastavení způsobu elektronické platby</span><span class="sxs-lookup"><span data-stu-id="9eb38-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="9eb38-133">Zpracování platby dodavateli</span><span class="sxs-lookup"><span data-stu-id="9eb38-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="9eb38-134">Import nových verzí standardních konfigurací formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="9eb38-135">Import nových verzí standardních konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="9eb38-136">Kontrola importovaných konfigurací formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="9eb38-137">Převzetí změn z nové verze importovaného formátu do vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="9eb38-138">Dokončení aktuální verze konceptu vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="9eb38-139">Převedení vlastního formátu na novou základní verzi</span><span class="sxs-lookup"><span data-stu-id="9eb38-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="9eb38-140">Zpracování platby dodavateli pomocí nově podloženého formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="9eb38-141">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9eb38-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="9eb38-142">Konfigurace rámce ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-142">Configure the ER framework</span></span>

<span data-ttu-id="9eb38-143">Jako uživatel v roli funkčního konzultanta elektronického výkaznictví musíte nakonfigurovat minimální sadu parametrů ER, abyste mohli začít používat rámec ER k navrhování vlastních verzí standardního formátu ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="9eb38-144">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-144">Configure ER parameters</span></span>

1. <span data-ttu-id="9eb38-145">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-146">Na stránce **Konfigurace lokalizace** vyberte v části **Související odkazy** možnost **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="9eb38-147">Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="9eb38-148">Na kartě **Přílohy** natavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="9eb38-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="9eb38-149">V poli **Konfigurace** vyberte pro společnost **USMF** typ **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="9eb38-150">V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="9eb38-151">Další informace o parametrech elektronického výkaznictví najdete v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9eb38-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="9eb38-152">Aktivace poskytovatele konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9eb38-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="9eb38-153">U každé přidané konfigurace elektronického výkaznictví je vyznačen jako vlastník poskytovatel konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9eb38-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="9eb38-154">Pro tyto účely se používá poskytovatel konfigurace elektronického výkaznictví, který je aktivován v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="9eb38-155">Než začnete přidávat nebo upravovat konfigurace ER, musíte proto aktivovat poskytovatele konfigurace ER v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="9eb38-156">Pouze vlastník konfigurace ER může konfiguraci upravovat.</span><span class="sxs-lookup"><span data-stu-id="9eb38-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="9eb38-157">Konfiguraci ER proto můžete upravovat teprve poté, co je příslušná konfigurace ER aktivována v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="9eb38-158">Kontrola seznamu poskytovatelů konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9eb38-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="9eb38-159">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-160">Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="9eb38-161">Na stránce **Tabulka poskytovatelů konfigurací** má záznam každého poskytovatele jedinečný název a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="9eb38-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="9eb38-162">Zkontrolujte obsah této stránky.</span><span class="sxs-lookup"><span data-stu-id="9eb38-162">Review the contents of this page.</span></span> <span data-ttu-id="9eb38-163">Pokud již existuje záznam **Litware, Inc.** ( `https://www.litware.com`), další postup, [přidání nového poskytovatele konfigurace ER](#ActivateProvider), přeskočte.</span><span class="sxs-lookup"><span data-stu-id="9eb38-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="9eb38-164">Přidání nového poskytovatele konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9eb38-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="9eb38-165">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-166">Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="9eb38-167">Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="9eb38-168">Do pole **Název** zadejte **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="9eb38-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="9eb38-169">Do pole **Internetová adresa** zadejte `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="9eb38-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="9eb38-170">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="9eb38-171">Aktivace poskytovatele konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9eb38-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="9eb38-172">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-173">Na stránce **Konfigurace lokalizace** klikněte v části **Poskytovatelé konfigurací** na dlaždici **Litware, Inc.** a poté vyberte možnost **Nastavit jako aktivní**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="9eb38-174">Další informace o poskytovatelích konfigurací ER naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="9eb38-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="9eb38-175">Import standardních konfigurací formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="9eb38-176">Import standardních konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-176">Import the standard ER configurations</span></span>

<span data-ttu-id="9eb38-177">Chcete-li přidat standardní konfigurace ER do aktuální instance systému Microsoft Dynamics 365 Finance, musíte je importovat z [úložiště](general-electronic-reporting.md#Repository) ER, jež je pro tuto instanci nakonfigurováno.</span><span class="sxs-lookup"><span data-stu-id="9eb38-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="9eb38-178">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-179">Chcete-li zobrazit seznam úložišť pro poskytovatele Microsoft, klikněte na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurací** na dlaždici **Microsoft** a poté vyberte možnost **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="9eb38-180">Na stránce **Úložiště konfigurací** vyberte úložiště typu **Globální** a poté zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="9eb38-181">Pokud budete vyzváni k autorizaci pro připojení ke službě Regulatory Configuration Service, postupujte podle pokynů k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="9eb38-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="9eb38-182">Na stránce **Úložiště konfigurace** vyberte ve stromu konfigurací v levém podokně konfiguraci formátu **BACS (Velká Británie)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="9eb38-183">Na záložce s náhledem **Verze** vyberte jako požadovanou verzi formátu vybrané konfigurace ER **1.1**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="9eb38-184">Vyberte **Importovat**. Vybraná verze se stáhne z globálního úložiště do aktuální instance aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="9eb38-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Stránka úložiště konfigurace](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="9eb38-186">Pokud máte potíže s přístupem na [globální úložiště](er-download-configurations-global-repo.md), můžete si místo toho [stáhnout konfigurace](download-electronic-reporting-configuration-lcs.md) ze služby Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9eb38-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="9eb38-187">Kontrola importovaných konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="9eb38-188">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-189">Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="9eb38-190">Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte **Model platby**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="9eb38-191">Všimněte si, že kromě vybraného formátu ER **BACS (Velká Británie)** byly importovány další požadované konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="9eb38-192">Ujistěte se, že ve stromu konfigurací jsou k dispozici následující konfigurace ER:</span><span class="sxs-lookup"><span data-stu-id="9eb38-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="9eb38-193">**Model platby** – Tato konfigurace obsahuje komponentu ER [datový model](general-electronic-reporting.md#data-model-and-model-mapping-components), jež představuje datovou strukturu platební podnikové domény.</span><span class="sxs-lookup"><span data-stu-id="9eb38-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="9eb38-194">**Mapování modelu platby 1611** – Tato konfigurace obsahuje komponentu ER [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components), jež popisuje, jak se datový model vyplněn za chodu daty z aplikace.</span><span class="sxs-lookup"><span data-stu-id="9eb38-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="9eb38-195">**BACS (Velká Británie)** - Tato konfigurace obsahuje komponenty ER [formát](general-electronic-reporting.md#FormatComponentOutbound) a mapování formátu.</span><span class="sxs-lookup"><span data-stu-id="9eb38-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="9eb38-196">Komponenta formát určuje rozvržení sestavy.</span><span class="sxs-lookup"><span data-stu-id="9eb38-196">The format component specifies the report layout.</span></span> <span data-ttu-id="9eb38-197">Komponenta mapování formátu obsahuje zdroj dat modelu a určuje, jak se vyplněno rozvržení sestavy pomocí tohoto zdroje dat za chodu vyplňuje.</span><span class="sxs-lookup"><span data-stu-id="9eb38-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Stránka Konfigurace](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="9eb38-199">Příprava platby dodavateli ke zpracování</span><span class="sxs-lookup"><span data-stu-id="9eb38-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="9eb38-200">Přidejte údajů o bance k účtu dodavatele</span><span class="sxs-lookup"><span data-stu-id="9eb38-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="9eb38-201">Musíte zadat bankovní údaje pro účet dodavatele, na který bude později odkazovat registrovaná platba.</span><span class="sxs-lookup"><span data-stu-id="9eb38-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="9eb38-202">Přejděte do části **Pohledávky** \> **Dodavatelé** \> **Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="9eb38-203">Na **Všichni dodavatelé** vyberte účet dodavatele **GB_SI_000001** a poté v podokně Akce na kartě **Dodavatel** vyberte ve skupině **Nastavení** položku **Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="9eb38-204">Na stránce **Bankovní účty dodavatele** vyberte **Nový** a zadejte následující údaje:</span><span class="sxs-lookup"><span data-stu-id="9eb38-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="9eb38-205">Do pole **Bankovní účet** zadejte **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="9eb38-206">V poli **Bankovní skupiny** vyberte možnost **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="9eb38-207">Do pole **Číslo bankovního účtu** zadejte **202015**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="9eb38-208">Do pole **Kód SWIFT** zadejte hodnotu <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="9eb38-209">Do pole **IBAN** zadejte hodnotu **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="9eb38-210">V poli **Směrový kód banky** ponechte výchozí hodnotu <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Stránka Bankovní účty dodavatele](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="9eb38-212">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-212">Select **Save**.</span></span>
5. <span data-ttu-id="9eb38-213">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9eb38-213">Close the page.</span></span>
6. <span data-ttu-id="9eb38-214">Na stránce **Všichni dodavatelé** otevřete účet dodavatele **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="9eb38-215">Na stránce podrobností dodavatele vyberte možnost **Upravit**. Díky tomu bude stránka v případě potřeby editovatelná.</span><span class="sxs-lookup"><span data-stu-id="9eb38-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="9eb38-216">Na záložce s náhledem **Platba** vyberte v poli **Bankovní účet** možnost **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Stránka Podrobnosti dodavatele](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="9eb38-218">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-218">Select **Save**.</span></span>
10. <span data-ttu-id="9eb38-219">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9eb38-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="9eb38-220">Zadání platby dodavateli</span><span class="sxs-lookup"><span data-stu-id="9eb38-220">Enter a vendor payment</span></span>

<span data-ttu-id="9eb38-221">Novou platbu dodavateli musíte vytvořit pomocí [návrhu platby](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).</span><span class="sxs-lookup"><span data-stu-id="9eb38-221">You must enter a new vendor payment by using a [payment proposal](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).</span></span>

1. <span data-ttu-id="9eb38-222">Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9eb38-223">Na stránce **Platební deník dodavatelů** zvolte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="9eb38-224">Zvolte hodnotu **VendPay** v poli **Název**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="9eb38-225">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-225">Select **Lines**.</span></span>
5. <span data-ttu-id="9eb38-226">Vyberte **Návrh platby** \> **Vytvořit návrh platby**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="9eb38-227">V dialogovém okně **Návrh platby dodavateli** nakonfigurujte filtrování tak, aby se zobrazovaly pouze záznamy pro účet dodavatele **GB_SI_000001**, poté klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="9eb38-228">Vyberte řádek pro fakturu **00000007_Inv** a klikněte na **Vytvořit platbu**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Dialogové okno Návrh platby dodavateli](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="9eb38-230">Ověřte, že zadávaná platba je nakonfigurována k použití **Elektronického** způsobu platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Stránka Platby dodavatelů](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="9eb38-232">Zpracování platby dodavateli pomocí standardního formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="9eb38-233">Nastavení způsobu elektronické platby</span><span class="sxs-lookup"><span data-stu-id="9eb38-233">Set up the electronic payment method</span></span>

<span data-ttu-id="9eb38-234">Musíte nakonfigurovat elektronický způsob platby tak, aby využíval importovanou konfiguraci formátu ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="9eb38-235">Přejděte na **Pohledávky** \> **Nastavení platby** \> **Způsoby platby**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="9eb38-236">Na stránce **Způsoby platby – dodavatelé** vyberte v levém podokně **Elektronický** způsob platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="9eb38-237">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-237">Select **Edit**.</span></span>
4. <span data-ttu-id="9eb38-238">Na záložce s náhledem **Formáty souborů** nastavte u možnosti **Obecný formát elektronického exportu** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="9eb38-239">V poli **Exportovat konfiguraci formátu** vyberte konfiguraci formátu **BACS (Velká Británie)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Stránka Způsob platby – dodavatelé](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="9eb38-241">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="9eb38-242">Zpracování platby dodavateli</span><span class="sxs-lookup"><span data-stu-id="9eb38-242">Process a vendor payment</span></span>

1. <span data-ttu-id="9eb38-243">Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9eb38-244">Na stránce **Deník platby dodavateli** vyberte dříve přidaný deník platby a pak vyberte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="9eb38-245">Na stránce **Platby dodavateli** vyberte možnost **Generovat platby**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="9eb38-246">V dialogovém okně **Generovat platby** zadejte následující údaje:</span><span class="sxs-lookup"><span data-stu-id="9eb38-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9eb38-247">V poli **Způsob platby** vyberte **Elektronický**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="9eb38-248">V poli **Bankovní účet** vyberte **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="9eb38-249">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-249">Select **OK**.</span></span>
6. <span data-ttu-id="9eb38-250">V dialogovém okně **Parametry elektronického výkaznictví** nastavte u možnosti **Vytisknout kontrolní sestavu** hodnotu **Ano** a poté stiskněte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Stránka Parametry elektronického výkaznictví](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="9eb38-252">Kromě platebního souboru můžete nyní vygenerovat kontrolní sestavu.</span><span class="sxs-lookup"><span data-stu-id="9eb38-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="9eb38-253">Stáhněte soubor zip a z něj extrahujte následující soubory:</span><span class="sxs-lookup"><span data-stu-id="9eb38-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="9eb38-254">Kontrolní sestava ve formátu Excel</span><span class="sxs-lookup"><span data-stu-id="9eb38-254">The control report in Excel format</span></span>
    - <span data-ttu-id="9eb38-255">Platební soubor ve formátu TXT</span><span class="sxs-lookup"><span data-stu-id="9eb38-255">The payment file in TXT format</span></span>

        <span data-ttu-id="9eb38-256">Všimněte si, že v souladu se [strukturou](#PositionRoutingNumber) poskytovaného formátu ER začíná řádek platby ve vygenerovaném souboru směrovým kódem, který byl [definován](#DefineRoutingNumber) pro konfigurovaný bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="9eb38-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Platební soubor ve formátu TXT](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="9eb38-258">Přizpůsobení standardního formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-258">Customize the standard ER format</span></span>

<span data-ttu-id="9eb38-259">V příkladu, který je uveden v této části, chcete použít konfigurace ER poskytnuté společností Microsoft pro účely generování platebních souborů pro platby dodavatelům ve formátu BACS, musíte však přidat přizpůsobení, aby byly podporovány požadavky konkrétní banky.</span><span class="sxs-lookup"><span data-stu-id="9eb38-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="9eb38-260">Chcete také mít možnost vlastní formát upgradovat, když budou k dispozici nové verze konfigurací ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="9eb38-261">Upgrade však chcete provést s nejnižšími náklady.</span><span class="sxs-lookup"><span data-stu-id="9eb38-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="9eb38-262">V tomto případě musíte jako zástupce společnosti Litware, Inc. vytvořit (odvodit) novou konfiguraci formátu ER s tím, že jako základ použijete konfiguraci **BACS (Velká Británie)** od společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9eb38-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="9eb38-263">Vytvoření vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-263">Create a custom format</span></span>

1. <span data-ttu-id="9eb38-264">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9eb38-265">Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="9eb38-266">Společnost Litware, Inc. použije verzi 1.1 této konfigurace formátu ER jako základ pro vlastní verzi.</span><span class="sxs-lookup"><span data-stu-id="9eb38-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="9eb38-267">Výběrem možnosti **Vytvořit konfiguraci** otevřete rozbalovací dialogovou nabídku.</span><span class="sxs-lookup"><span data-stu-id="9eb38-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="9eb38-268">Tuto dialogovou nabídku můžete použít k vytvoření nové konfigurace pro vlastní formát platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="9eb38-269">Ve skupině polí **Nový** vyberte možnost **Odvodit z názvu: BACS (Velká Británie), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="9eb38-270">Do pole **Název** zadejte **BACS (Velká Británie – vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Dialogové okno Vytvořit konfiguraci – rozevírací seznam](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="9eb38-272">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-272">Select **Create configuration**.</span></span>

<span data-ttu-id="9eb38-273">Vytvoří se verze 1.1.1 **BACS (Velká Británie – vlastní)** konfigurace formátu ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="9eb38-274">Tato verze je ve [stavu](general-electronic-reporting.md#component-versioning) **Konceptu** a je editovatelná.</span><span class="sxs-lookup"><span data-stu-id="9eb38-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="9eb38-275">Aktuální obsah vašeho vlastního formátu ER odpovídá obsahu formátu poskytnutého společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9eb38-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Stránka Konfigurace](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="9eb38-277">Úprava vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-277">Edit a custom format</span></span>

<span data-ttu-id="9eb38-278">Vlastní formát musíte nakonfigurovat, aby splňoval konkrétní požadavky banky.</span><span class="sxs-lookup"><span data-stu-id="9eb38-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="9eb38-279">Banka může například vyžadovat, aby generované platební soubory obsahovaly kód SWIFT (Society for Worldwide Interbank Financial Telecommunication) banky, jíž je přiřazena role zprostředkovatele při zpracování platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="9eb38-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="9eb38-280">Kódy SWIFT jsou mezinárodní bankovní kódy a identifikují konkrétní banky na celém světě.</span><span class="sxs-lookup"><span data-stu-id="9eb38-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="9eb38-281">Někdy se též označují jako kódy BIC (Bank Identifier Code).</span><span class="sxs-lookup"><span data-stu-id="9eb38-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="9eb38-282">Kód SWIFT sestává z 11 znaků a musí být zadán na začátku každého platebního řádku ve vygenerovaném souboru platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="9eb38-283">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9eb38-284">Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie – vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="9eb38-285">Na záložce s náhledem **Verze** vyberte jako požadovanou verzi vybrané konfigurace **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="9eb38-286">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-286">Select **Designer**.</span></span>
5. <span data-ttu-id="9eb38-287">Na stránce **Návrhář formátu** vyberte možnost **Zobrazit podrobnosti**. Zobrazí se další informace o prvcích formátu.</span><span class="sxs-lookup"><span data-stu-id="9eb38-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="9eb38-288">Rozbalte a zkontrolujte následující prvky:</span><span class="sxs-lookup"><span data-stu-id="9eb38-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="9eb38-289">Prvek **BACSReportsFolder** typu **Složka**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="9eb38-290">Tento prvek se používá ke generování výstupu ve formátu ZIP.</span><span class="sxs-lookup"><span data-stu-id="9eb38-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="9eb38-291">Prvek **soubor** typu **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="9eb38-292">Tento prvek se používá ke generování souboru plateb ve formátu TXT.</span><span class="sxs-lookup"><span data-stu-id="9eb38-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="9eb38-293">Prvek **transakce** typu **Sekvence**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="9eb38-294">Tento prvek se používá ke generování jednoho řádku platby v souboru plateb.</span><span class="sxs-lookup"><span data-stu-id="9eb38-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="9eb38-295">Prvek **transakce** typu **Sekvence**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="9eb38-296">Tento prvek se používá ke generování jednotlivých polí jednoho řádku platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="9eb38-297">Vyberte prvek **transakce**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-297">Select the **transaction** element.</span></span>

    ![Prvek transakce v návrháři operací ER](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="9eb38-299">Poskytnutá sestava je nakonfigurována tak, aby <a id="PositionRoutingNumber"></a>každý řádek platby začínal směrovým kódem banky.</span><span class="sxs-lookup"><span data-stu-id="9eb38-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="9eb38-300">Pro tento účel se používá formátovací prvek **vendBankRouteNum**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="9eb38-301">Vyberte **Přidat** a poté vyberte typ formátu prvku, který přidáváte, jako **Text\\String**:</span><span class="sxs-lookup"><span data-stu-id="9eb38-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="9eb38-302">Do pole **Název** zadejte **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="9eb38-303">Do pole **Minimální délka** zadejte hodnotu **11**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="9eb38-304">Do pole **Maximální délka** zadejte hodnotu **11**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="9eb38-305">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9eb38-306">Prvek **vendBankSWIFT** se použije k zadání kódu SWIFT banky dodavatele do vygenerovaných souborů.</span><span class="sxs-lookup"><span data-stu-id="9eb38-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="9eb38-307">Ve stromu struktury formátu vyberte **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="9eb38-308">Chcete-li vybraný prvek formátu posunout o jednu úroveň výše, klikněte na **Přesunout nahoru**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="9eb38-309">Tento krok opakujte, kolikrát je třeba, aby prvek **vendBankSWIFT** byl <a id="PositionSWIFTCode"></a>prvním prvkem pod nadřazeným prvkem **transakce**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT jako první prvek pod prvkem transakce v návrháři operací ER](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="9eb38-311">Dokud máte ve stromové struktuře formátu vybraný prvek **vendBankSWIFT**, klikněte na kartu **Mapování** a poté rozbalte zdroj dat **Model**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="9eb38-312">Rozbalte **model.Payment** \> **model.Payment.CreditorAgent** a vyberte pole zdroje dat **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="9eb38-313">Toto pole zdroje dat obsahuje kód SWIFT banky dodavatele, jíž je při zpracování platby dodavateli přiřazena role zprostředkovatele.</span><span class="sxs-lookup"><span data-stu-id="9eb38-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="9eb38-314">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-314">Select **Bind**.</span></span> <span data-ttu-id="9eb38-315">Prvek formátu **vendBankSWIFT** je nyní propojen s polem zdroje dat **model.Payment.CreditorAgent.BICFI**, a proto budou kódy SWIFT vkládány do vygenerovaných platebních souborů.</span><span class="sxs-lookup"><span data-stu-id="9eb38-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![Prvek formátu vendBankSWIFT svázaný s polem zdroje dat model.Payment.CreditorAgent.BICFI v návrháři operací ER](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="9eb38-317">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-317">Select **Save**.</span></span>
15. <span data-ttu-id="9eb38-318">Zavřete stránku návrháře.</span><span class="sxs-lookup"><span data-stu-id="9eb38-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="9eb38-319">Označení vlastního formátu jako spustitelného</span><span class="sxs-lookup"><span data-stu-id="9eb38-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="9eb38-320">Nyní, když máte vytvořenou první verzi vlastního formátu a ten je ve stavu **Koncept**, můžete jej pro testovací účely spustit.</span><span class="sxs-lookup"><span data-stu-id="9eb38-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="9eb38-321">Chcete-li sestavu spustit, musíte zpracovat platbu dodavateli pomocí způsobu platby, která odkazuje na váš vlastní formát ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="9eb38-322">Ve výchozím nastavení jsou při volání formátu ER z aplikace [zvažovány](general-electronic-reporting.md#component-versioning) pouze verze se stavem **Dokončeno** nebo **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="9eb38-323">Toto chování pomáhá zabránit použití formátů ER s nedokončenými návrhy.</span><span class="sxs-lookup"><span data-stu-id="9eb38-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="9eb38-324">Pro zkušební účely však můžete aplikaci přinutit, aby použila verzi formátu ER ve stavu **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="9eb38-325">Pokud při testu zjistíte, že je třeba provést nějaké změny, můžete následně aktuální verzi formátu upravit.</span><span class="sxs-lookup"><span data-stu-id="9eb38-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="9eb38-326">Další informace naleznete v tématu [Použitelnost](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="9eb38-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="9eb38-327">Chcete-li použít koncept formátu ER, musíte příslušný formát ER explicitně označit.</span><span class="sxs-lookup"><span data-stu-id="9eb38-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="9eb38-328">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9eb38-329">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="9eb38-330">V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Spustit nastavení** hodnotu **Ano** a poté stiskněte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="9eb38-331">Je-li třeba vyberte možnost **Upravit**, má-li být aktuální stránka editovatelná.</span><span class="sxs-lookup"><span data-stu-id="9eb38-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="9eb38-332">Ve stromu konfigurace v levém podokně vyberte možnost **BACS (Velká Británie – vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="9eb38-333">U možnosti **Spustit koncept** nastavte hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Možnost Spustit koncept na stránce Konfigurace](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="9eb38-335">Zpracování platby dodavateli pomocí vlastního formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="9eb38-336">Nastavení způsobu elektronické platby</span><span class="sxs-lookup"><span data-stu-id="9eb38-336">Set up the electronic payment method</span></span>

<span data-ttu-id="9eb38-337">Elektronický způsob platby musíte nakonfigurovat tak, aby byl při zpracování plateb dodavateli použit váš vlastní formát ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="9eb38-338">Přejděte na **Pohledávky** \> **Nastavení platby** \> **Způsoby platby**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="9eb38-339">Na stránce **Způsoby platby – dodavatelé** vyberte v levém podokně **Elektronický** způsob platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="9eb38-340">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-340">Select **Edit**.</span></span>
4. <span data-ttu-id="9eb38-341">Na záložce s náhledem **Formát souboru** nastavte u možnosti **Obecný formát elektronického exportu** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="9eb38-342">V poli **Exportovat konfiguraci formátu** vyberte konfiguraci formátu **BACS (Velká Británie – vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Stránka Způsob platby – dodavatelé](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="9eb38-344">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="9eb38-345">Zpracování platby dodavateli</span><span class="sxs-lookup"><span data-stu-id="9eb38-345">Process a vendor payment</span></span>

1. <span data-ttu-id="9eb38-346">Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9eb38-347">Na stránce **Deník platby dodavateli** vyberte dříve vytvořený deník platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="9eb38-348">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-348">Select **Lines**.</span></span>
4. <span data-ttu-id="9eb38-349">Na stránce **Platby dodavateli** vyberte nad mřížkou **Stav platby** \> **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="9eb38-350">Vyberte **Generovat platbu**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="9eb38-351">V dialogovém okně **Generovat platby** zadejte následující údaje:</span><span class="sxs-lookup"><span data-stu-id="9eb38-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9eb38-352">V poli **Způsob platby** vyberte **Elektronický**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="9eb38-353">V poli **Bankovní účet** vyberte **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="9eb38-354">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-354">Select **OK**.</span></span>
8. <span data-ttu-id="9eb38-355">V dialogovém okně **Parametry elektronického výkaznictví** nastavte u možnosti **Vytisknout kontrolní sestavu** hodnotu **Ano** a poté stiskněte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9eb38-356">Kromě platebního souboru můžete vygenerovat pouze kontrolní sestavu.</span><span class="sxs-lookup"><span data-stu-id="9eb38-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="9eb38-357">Stáhněte soubor zip a z něj extrahujte následující soubory:</span><span class="sxs-lookup"><span data-stu-id="9eb38-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="9eb38-358">Kontrolní sestava ve formátu Excel</span><span class="sxs-lookup"><span data-stu-id="9eb38-358">The control report in Excel format</span></span>
    - <span data-ttu-id="9eb38-359">Platební soubor ve formátu TXT</span><span class="sxs-lookup"><span data-stu-id="9eb38-359">The payment file in TXT format</span></span>

        <span data-ttu-id="9eb38-360">Všimněte si, že v souladu se strukturou vlastního formátu ER platební řádek ve vygenerovaném souboru nyní [začíná](#PositionSWIFTCode) kódem SWIFT, který byl [zadán](#DefineSWIFTCode) pro bankovní účet dodavatele, jehož platba se zpracovává.</span><span class="sxs-lookup"><span data-stu-id="9eb38-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Platební soubor ve formátu TXT](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="9eb38-362">Import nových verzí standardních konfigurací formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="9eb38-363">V rámci příkladu uvedeného v této části se zobrazí upozornění na článek ze znalostní báze [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="9eb38-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="9eb38-364">Toto oznámení vás informuje o nové verzi formátu ER **BACS (Velká Británie)**, který publikovala společnost Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9eb38-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="9eb38-365">Kromě kontrolní sestavy umožňuje tato nová verze uživatelům generovat při zpracování plateb dodavatelům sestavu platebních avíz a sestavu průvodek.</span><span class="sxs-lookup"><span data-stu-id="9eb38-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="9eb38-366">Chcete začít používat tuto funkci.</span><span class="sxs-lookup"><span data-stu-id="9eb38-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="9eb38-367">Import nových verzí standardních konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="9eb38-368">Chcete-li přidat nové verze konfigurace ER do aktuální instance systému Finance, musíte je importovat z nakonfigurovaného [úložiště](general-electronic-reporting.md#Repository) ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="9eb38-369">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-370">Chcete-li zobrazit seznam úložišť pro poskytovatele Microsoft, klikněte na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurací** na dlaždici **Microsoft** a poté vyberte možnost **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="9eb38-371">Na stránce **Úložiště konfigurací** vyberte úložiště typu **Globální** a poté zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="9eb38-372">Pokud budete vyzváni k autorizaci pro připojení ke službě Regulatory Configuration Service, postupujte podle pokynů k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="9eb38-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="9eb38-373">Na stránce **Úložiště konfigurace** vyberte ve stromu konfigurací v levém podokně konfiguraci formátu **BACS (Velká Británie)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="9eb38-374">Na záložce s náhledem **Verze** vyberte jako požadovanou verzi formátu vybrané konfigurace ER **3.3**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="9eb38-375">Vyberte **Importovat**. Vybraná verze se stáhne z globálního úložiště do aktuální instance aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="9eb38-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Stránka úložiště konfigurace](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="9eb38-377">Pokud máte potíže s přístupem na [globální úložiště](er-download-configurations-global-repo.md), můžete si místo toho [stáhnout konfigurace](download-electronic-reporting-configuration-lcs.md) ze služby Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9eb38-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="9eb38-378">Kontrola importovaných konfigurací formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="9eb38-379">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-380">Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="9eb38-381">Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="9eb38-382">Na záložce s náhledem **Verze** vyberte verzi **3.3**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="9eb38-383">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-383">Select **Designer**.</span></span>
6. <span data-ttu-id="9eb38-384">Na stránce **Návrhář formátů** rozbalte prvek formátu **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="9eb38-385">Všimněte si, že verze 3.3 obsahuje prvek formátu **PaymentAdviceReport**, který se používá ke generování sestavy platebních avíz, když je zpracována platba dodavateli.</span><span class="sxs-lookup"><span data-stu-id="9eb38-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![Prvek formátu PaymentAdviceReport v návrháři operací ER](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="9eb38-387">Zavřete stránku návrháře.</span><span class="sxs-lookup"><span data-stu-id="9eb38-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="9eb38-388">Převzetí změn z nové verze importovaného formátu do vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="9eb38-389">Dokončení aktuální verze konceptu vlastního formátu</span><span class="sxs-lookup"><span data-stu-id="9eb38-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="9eb38-390">Pokud si přejete zachovat aktuální stav vlastního formátu, dokončíte koncept ve verzi 1.1.1 tak, že změníte jeho stav z **Koncept** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="9eb38-391">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9eb38-392">Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="9eb38-393">Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby**, rozbalte položku **BACS (Velká Británie)** a poté vyberte možnost **BACS (Velká Británie – vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="9eb38-394">Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="9eb38-395">Stav verze 1.1.1 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="9eb38-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="9eb38-396">Byla přidána nová editovatelná verze 1.1.2, která je nyní ve stavu **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="9eb38-397">Tuto verzi můžete použít k provedení dalších změn ve vlastním formátu ER.</span><span class="sxs-lookup"><span data-stu-id="9eb38-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="9eb38-398">Převedení vlastního formátu na novou základní verzi</span><span class="sxs-lookup"><span data-stu-id="9eb38-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="9eb38-399">Chcete-li začít používat novou funkčnost verze 3.3 formátu **BACS (Velká Británie)** v rámci přizpůsobování, musíte změnit základní verzi konfigurace na vlastní konfiguraci **BACS (Velká Británie – vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="9eb38-400">Pro tento proces je používáno označení [přeskladnění](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="9eb38-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="9eb38-401">Místo verze 1.1 **BACS (Velká Británie)** použijte novou verzi 3.3.</span><span class="sxs-lookup"><span data-stu-id="9eb38-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="9eb38-402">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9eb38-403">Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie – vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="9eb38-404">Na záložce s náhledem **Verze** vyberte verzi **1.1.2** a poté vyberte **Přeskládat**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="9eb38-405">V dialogovém okně **Přeskládat** vyberte v poli **Cílová verze** verzi **3.3** základní konfigurace. Tím se tato použije jako nová základní konfigurace a též k aktualizaci konfigurace.</span><span class="sxs-lookup"><span data-stu-id="9eb38-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Dialogové okno Přeskládat](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="9eb38-407">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-407">Select **OK**.</span></span>
6. <span data-ttu-id="9eb38-408">Všimněte si, že číslo konceptové verze se změnilo z **1.1.2** na **3.3.2**, což umožňuje reflektovat změnu základní verze.</span><span class="sxs-lookup"><span data-stu-id="9eb38-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="9eb38-409">Když dojde ke spojení vlastní verze a nové základní verze, mohou se objevit konflikty vyplývající ze změn formátu, které nelze sloučit automaticky.</span><span class="sxs-lookup"><span data-stu-id="9eb38-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Přestavěná konfigurace s konflikty na stránce Konfigurace](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="9eb38-411">Pokud jsou zjištěny konflikty, je nutné je vyřešit ručně v návrháři formátů.</span><span class="sxs-lookup"><span data-stu-id="9eb38-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="9eb38-412">Na záložce s náhledem **Verze** vyberte verzi **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="9eb38-413">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-413">Select **Designer**.</span></span>
9. <span data-ttu-id="9eb38-414">Na stránce **Návrhář formátů** vyberte na záložce s náhledem **Podrobnosti** záznam konfliktu z přestavby a poté vyberte možnost **Použít základní hodnotu**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Záznam konfliktu z přestavby v návrháři operací ER](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="9eb38-416">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-416">Select **Save**.</span></span>

    <span data-ttu-id="9eb38-417">Záznam konfliktu z přestavby by se již neměl na záložce s náhledem **Podrobnosti** objevovat.</span><span class="sxs-lookup"><span data-stu-id="9eb38-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Vyřešený konflikt v návrháři operací ER](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="9eb38-419">Konflikt jste vyřešili potvrzením, že je třeba v tomto formátu ER použít verzi 3 základního modelu.</span><span class="sxs-lookup"><span data-stu-id="9eb38-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="9eb38-420">Rozbalte **BACSReportsFolder** \> **soubor** \> **transakce** \> **transakce**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="9eb38-421">Na kartě **Mapování** si všimněte, že verze 3.3.2 vlastního formátu ER obsahuje vaše přizpůsobení (**vendBankSWIFT** a jeho vazby) a novou funkčnost verze 3.3 základního formátu ER od společnosti Microsoft (prvek formátu **PaymentAdviceReport** spolu s vnořenými prvky a nakonfigurovanými vazbami).</span><span class="sxs-lookup"><span data-stu-id="9eb38-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="9eb38-422">Pouhými několika kliknutími myši jste přijali změny nové základní verze sloučením s vlastním přizpůsobením.</span><span class="sxs-lookup"><span data-stu-id="9eb38-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Sloučený formát v návrháři operací ER](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="9eb38-424">Zavřete stránku návrháře.</span><span class="sxs-lookup"><span data-stu-id="9eb38-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="9eb38-425">Akce přestavby je vratná.</span><span class="sxs-lookup"><span data-stu-id="9eb38-425">The rebase action is reversible.</span></span> <span data-ttu-id="9eb38-426">Chcete-li tuto přestavbu zrušit, vyberte verzi **1.1.1** formátu **BACS (Velká Británie – vlastní)** na záložce s náhledem **Verze** a poté vyberte možnost **Získat tuto verzi**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="9eb38-427">Verze 3.3.2 se poté přečísluje na 1.1.2 a obsah konceptové verze 1.1.2 bude odpovídat obsahu verze 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="9eb38-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="9eb38-428">Zpracování platby dodavateli pomocí nově podloženého formátu ER</span><span class="sxs-lookup"><span data-stu-id="9eb38-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="9eb38-429">Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9eb38-430">Na stránce **Deník platby dodavateli** vyberte dříve vytvořený deník platby.</span><span class="sxs-lookup"><span data-stu-id="9eb38-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="9eb38-431">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-431">Select **Lines**.</span></span>
4. <span data-ttu-id="9eb38-432">Na stránce **Platby dodavateli** vyberte nad mřížkou **Stav platby** \> **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="9eb38-433">Vyberte **Generovat platbu**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="9eb38-434">V dialogovém okně **Generovat platby** zadejte následující údaje:</span><span class="sxs-lookup"><span data-stu-id="9eb38-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9eb38-435">V poli **Způsob platby** vyberte **Elektronický**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="9eb38-436">V poli **Bankovní účet** vyberte **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="9eb38-437">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-437">Select **OK**.</span></span>
8. <span data-ttu-id="9eb38-438">V dialogovém okně **Parametry elektronického výkaznictví** zadejte následující údaje:</span><span class="sxs-lookup"><span data-stu-id="9eb38-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9eb38-439">Nastavte možnost **Vytisknout kontrolní sestavu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="9eb38-440">Nastavte u položky **Tisknout platební avízo** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Dialogové okno parametrů elektronického výkaznictví](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="9eb38-442">Kromě platebního souboru můžete nyní vygenerovat kontrolní sestavu a sestavu platebních avíz.</span><span class="sxs-lookup"><span data-stu-id="9eb38-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="9eb38-443">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb38-443">Select **OK**.</span></span>
10. <span data-ttu-id="9eb38-444">Stáhněte soubor zip a z něj extrahujte následující soubory:</span><span class="sxs-lookup"><span data-stu-id="9eb38-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="9eb38-445">Kontrolní sestava ve formátu Excel</span><span class="sxs-lookup"><span data-stu-id="9eb38-445">The control report in Excel format</span></span>
    - <span data-ttu-id="9eb38-446">Sestava platebních avíz ve formátu Excel</span><span class="sxs-lookup"><span data-stu-id="9eb38-446">The payment advice report in Excel format</span></span>

        ![Sestava platebních avíz ve formátu Excel](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="9eb38-448">Platební soubor ve formátu TXT</span><span class="sxs-lookup"><span data-stu-id="9eb38-448">The payment file in TXT format</span></span>

        <span data-ttu-id="9eb38-449">Všimněte si, že platební řádek ve vygenerovaném souboru začíná kódem SWIFT, který byl zadán pro bankovní účet dodavatele, jehož platba se zpracovává.</span><span class="sxs-lookup"><span data-stu-id="9eb38-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Platební soubor ve formátu TXT](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="9eb38-451">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9eb38-451">Additional resources</span></span>

- [<span data-ttu-id="9eb38-452">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9eb38-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9eb38-453">Stažení konfigurací ER z Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="9eb38-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="9eb38-454">Stažení konfigurací ER z Globálního úložiště konfigurační služby</span><span class="sxs-lookup"><span data-stu-id="9eb38-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]