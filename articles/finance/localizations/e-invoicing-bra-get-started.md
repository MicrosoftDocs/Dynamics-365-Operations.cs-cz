---
title: Začněte s doplňkem elektronické fakturace pro Brazílii
description: Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Brazílii v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/19/2020
ms.locfileid: "4441338"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="171d8-103">Začněte s doplňkem elektronické fakturace pro Brazílii</span><span class="sxs-lookup"><span data-stu-id="171d8-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="171d8-104">Doplněk elektronické fakturace pro Brazílii aktuálně nepodporuje všechny funkce, které jsou k dispozici v integraci fiskálních dokumentů zabudovaných do Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="171d8-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="171d8-105">Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Brazílii.</span><span class="sxs-lookup"><span data-stu-id="171d8-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="171d8-106">Provede vás konfiguračními kroky, které jsou závislé na zemi v Regulatory Configuration Services (RCS) a ve Finance a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="171d8-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="171d8-107">Také vás provede procesem odeslání fiskálního dokumentu NF-e (model elektronického fiskálního dokumentu 55) prostřednictvím služby a vysvětlí, jak zkontrolovat výsledky zpracování a stav fiskálních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="171d8-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="171d8-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="171d8-108">Prerequisites</span></span>

<span data-ttu-id="171d8-109">Než dokončíte kroky v tomto tématu, musíte provést kroky v [Začněte s doplňkem Elektronická fakturace](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="171d8-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="171d8-110">Nastavení RCS</span><span class="sxs-lookup"><span data-stu-id="171d8-110">RCS setup</span></span>

<span data-ttu-id="171d8-111">Během instalace RCS dokončíte tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="171d8-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="171d8-112">Importujte funkci elektronické fakturace pro fiskální dokumenty NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="171d8-113">Zkontrolujte formáty souborů, které jsou vyžadovány k odeslání fiskálních dokumentů NF-e k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="171d8-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="171d8-114">Zkontrolujte formáty souborů, které jsou požadovány pro zrušení schválené NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="171d8-115">Nakonfigurujte událost, která se vyžaduje k odeslání fiskálních dokumentů NF-e k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="171d8-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="171d8-116">Nakonfigurujte událost, která se vyžaduje pro zrušení schválené NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="171d8-117">Přiřaďte funkci elektronické fakturace do prostředí doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="171d8-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="171d8-118">Publikování funkce elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="171d8-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="171d8-119">„Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="171d8-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="171d8-120">Nastavení funkce elektronické fakturace mimo jiné kombinuje použití konfiguračních formátů elektronických zpráv (ER) k vytvoření konfigurovatelných souborů exportu a importu a použití akcí a toků akcí k umožnění vytváření konfigurovatelných pravidel pro odesílání požadavků, import odpovědi a analýzu obsahu odpovědí.</span><span class="sxs-lookup"><span data-stu-id="171d8-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="171d8-121">Import funkce elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="171d8-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="171d8-122">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="171d8-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="171d8-123">V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="171d8-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="171d8-124">Na stránce **Funkce elektronické fakturace** vyberte **Import**, chcete-li importovat funkci elektronické fakturace fiskálních dokumentů NF-e z globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="171d8-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![Tlačítko Importovat](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="171d8-126">Vyberte funkci fiskálního dokumentu NF-e a poté vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="171d8-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![Import funkce NF-e](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="171d8-128">Vytvořte novou verzi funkce fiskálního dokumentu NF-e</span><span class="sxs-lookup"><span data-stu-id="171d8-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="171d8-129">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="171d8-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Přidání nové verze funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="171d8-131">Aktualizujte verzi konfigurace</span><span class="sxs-lookup"><span data-stu-id="171d8-131">Update the configuration version</span></span>

1. <span data-ttu-id="171d8-132">Na stránce **Funkce elektronické fakturace** na kartě **Konfigurace** vyberte **Přidat** nebo **Odebrat** ke správě verzí konfigurace (konfigurace formátu souboru ER).</span><span class="sxs-lookup"><span data-stu-id="171d8-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Správa konfigurací funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="171d8-134">Když vytvoříte novou verzi funkce fiskálního dokumentu NF-e, všechny konfigurační verze (formáty souborů ER) se zdědí z nejnovější verze.</span><span class="sxs-lookup"><span data-stu-id="171d8-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="171d8-135">K odeslání fiskálního dokumentu NF-e k autorizaci jsou vyžadovány následující konfigurační verze:</span><span class="sxs-lookup"><span data-stu-id="171d8-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="171d8-136">formát exportu odeslání NFe</span><span class="sxs-lookup"><span data-stu-id="171d8-136">NFe submit export format</span></span>
        - <span data-ttu-id="171d8-137">Import zpráv odpovědi NFe</span><span class="sxs-lookup"><span data-stu-id="171d8-137">NFe response message import</span></span>
        - <span data-ttu-id="171d8-138">Import protokolu chyb NFe</span><span class="sxs-lookup"><span data-stu-id="171d8-138">NFe error log import</span></span>

    - <span data-ttu-id="171d8-139">K odeslání zrušení NF-e je nutná následující konfigurační verze:</span><span class="sxs-lookup"><span data-stu-id="171d8-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="171d8-140">formát exportu zrušení NFe</span><span class="sxs-lookup"><span data-stu-id="171d8-140">NFe cancel export format</span></span>

2. <span data-ttu-id="171d8-141">V seznamu vyberte verzi konfigurace a poté vyberte **Upravit** nebo **Zobrazit**, chcete-li otevřít stránku **Návrhář formátů**, kde můžete upravit nebo zobrazit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="171d8-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Otevření stránky Návrhář formátu](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="171d8-143">Použijte stránku **Návrhář formátů**, chcete-li upravovat nebo prohlížet konfigurace souborů ve formátu ER.</span><span class="sxs-lookup"><span data-stu-id="171d8-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="171d8-144">Další informace získáte v tématu [Vytvoření konfigurací elektronického dokumentu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span><span class="sxs-lookup"><span data-stu-id="171d8-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![Stránka návrháře formátu](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="171d8-146">Spravujte nastavení funkce elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="171d8-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="171d8-147">Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** vyberte **Přidat** nebo **Odebrat** ke správě nastavení funkcí elektronické fakturace (tj. událostí NF-e).</span><span class="sxs-lookup"><span data-stu-id="171d8-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![Správa nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="171d8-149">Když vytvoříte novou verzi funkce fiskálního dokumentu NF-e, která je odvozena z jiné funkce elektronické fakturace, všechna nastavení funkcí (události NF-e) se zdědí z nejnovější verze.</span><span class="sxs-lookup"><span data-stu-id="171d8-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="171d8-150">Chcete-li odeslat fiskální dokumenty NF-e k autorizaci, je vyžadováné nastavení funkce **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="171d8-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="171d8-151">Chcete-li odeslat zrušení NF-e, je vyžadováno nastavení funkce **Zrušení**.</span><span class="sxs-lookup"><span data-stu-id="171d8-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="171d8-152">Nakonfigurujte nastavení funkce Odeslat</span><span class="sxs-lookup"><span data-stu-id="171d8-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="171d8-153">Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="171d8-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="171d8-154">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="171d8-154">Select **Edit**.</span></span>

    ![Upravit nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="171d8-156">Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí.</span><span class="sxs-lookup"><span data-stu-id="171d8-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![Karta Akce](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="171d8-158">Zkontrolujte akce, které jsou vyžadovány k odeslání NF-e k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="171d8-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="171d8-159">ID akce</span><span class="sxs-lookup"><span data-stu-id="171d8-159">Action ID</span></span> | <span data-ttu-id="171d8-160">Název akce</span><span class="sxs-lookup"><span data-stu-id="171d8-160">Action name</span></span>                  | <span data-ttu-id="171d8-161">Popis akce</span><span class="sxs-lookup"><span data-stu-id="171d8-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="171d8-162">1</span><span class="sxs-lookup"><span data-stu-id="171d8-162">1</span></span>         | <span data-ttu-id="171d8-163">Převod dokumentu</span><span class="sxs-lookup"><span data-stu-id="171d8-163">Transform document</span></span>           | <span data-ttu-id="171d8-164">Vytvořte soubor NF-e XML pro odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="171d8-165">2</span><span class="sxs-lookup"><span data-stu-id="171d8-165">2</span></span>         | <span data-ttu-id="171d8-166">Podepsat dokument</span><span class="sxs-lookup"><span data-stu-id="171d8-166">Sign document</span></span>                | <span data-ttu-id="171d8-167">Aplikujte digitální certifikát na soubor XML.</span><span class="sxs-lookup"><span data-stu-id="171d8-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="171d8-168">3</span><span class="sxs-lookup"><span data-stu-id="171d8-168">3</span></span>         | <span data-ttu-id="171d8-169">Volejte brazilskou službu SEFAZ</span><span class="sxs-lookup"><span data-stu-id="171d8-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="171d8-170">Odešlete podepsaný soubor XML do webových služeb k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="171d8-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="171d8-171">4</span><span class="sxs-lookup"><span data-stu-id="171d8-171">4</span></span>         | <span data-ttu-id="171d8-172">Odezva procesu</span><span class="sxs-lookup"><span data-stu-id="171d8-172">Process response</span></span>             | <span data-ttu-id="171d8-173">Získejte odpověď webové služby.</span><span class="sxs-lookup"><span data-stu-id="171d8-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="171d8-174">5</span><span class="sxs-lookup"><span data-stu-id="171d8-174">5</span></span>         | <span data-ttu-id="171d8-175">Převod dokumentu</span><span class="sxs-lookup"><span data-stu-id="171d8-175">Transform document</span></span>           | <span data-ttu-id="171d8-176">Parsujte obsah souboru, který je přijat jako odpověď.</span><span class="sxs-lookup"><span data-stu-id="171d8-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="171d8-177">6</span><span class="sxs-lookup"><span data-stu-id="171d8-177">6</span></span>         | <span data-ttu-id="171d8-178">Převod dokumentu</span><span class="sxs-lookup"><span data-stu-id="171d8-178">Transform document</span></span>           | <span data-ttu-id="171d8-179">Vytvořte soubor XML a informujte se o stavu odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="171d8-180">7</span><span class="sxs-lookup"><span data-stu-id="171d8-180">7</span></span>         | <span data-ttu-id="171d8-181">Volejte brazilskou službu SEFAZ</span><span class="sxs-lookup"><span data-stu-id="171d8-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="171d8-182">Odešlete soubor XML, který požaduje stav odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="171d8-183">8</span><span class="sxs-lookup"><span data-stu-id="171d8-183">8</span></span>         | <span data-ttu-id="171d8-184">Odezva procesu</span><span class="sxs-lookup"><span data-stu-id="171d8-184">Process response</span></span>             | <span data-ttu-id="171d8-185">Získejte odpověď webové služby.</span><span class="sxs-lookup"><span data-stu-id="171d8-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="171d8-186">Nastavte adresu URL pro webové služby SEFAZ</span><span class="sxs-lookup"><span data-stu-id="171d8-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="171d8-187">Na stránce **Nastavení verze funkce** na kartě **Akce** na pevné záložce **Akce** vyberte **Volejte brazilskou službu SEFAZ** (ID akce **3**).</span><span class="sxs-lookup"><span data-stu-id="171d8-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="171d8-188">Na pevné záložce **Parametry** v poli **Parametr adresy URL** zadejte adresu URL webové služby SEFAZ pro odeslání NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="171d8-189">Na pevné záložce **Akce** vyberte **Volejte brazilskou službu SEFAZ** (ID akce **7**).</span><span class="sxs-lookup"><span data-stu-id="171d8-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7**).</span></span>
4. <span data-ttu-id="171d8-190">Na pevné záložce **Parametry** v poli **Parametr adresy URL** zadejte adresu URL webové služby SEFAZ pro odeslání NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="171d8-191">Nakonfigurujte nastavení funkce Zrušení</span><span class="sxs-lookup"><span data-stu-id="171d8-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="171d8-192">Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Zrušení**.</span><span class="sxs-lookup"><span data-stu-id="171d8-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="171d8-193">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="171d8-193">Select **Edit**.</span></span>
3. <span data-ttu-id="171d8-194">Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí.</span><span class="sxs-lookup"><span data-stu-id="171d8-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="171d8-195">Zkontrolujte akce, které jsou požadovány pro zrušení schválené NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="171d8-196">ID akce</span><span class="sxs-lookup"><span data-stu-id="171d8-196">Action ID</span></span> | <span data-ttu-id="171d8-197">Název akce</span><span class="sxs-lookup"><span data-stu-id="171d8-197">Action name</span></span>                  | <span data-ttu-id="171d8-198">Popis akce</span><span class="sxs-lookup"><span data-stu-id="171d8-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="171d8-199">1</span><span class="sxs-lookup"><span data-stu-id="171d8-199">1</span></span>         | <span data-ttu-id="171d8-200">Převod dokumentu</span><span class="sxs-lookup"><span data-stu-id="171d8-200">Transform document</span></span>           | <span data-ttu-id="171d8-201">Vytvořte soubor zrušení NF-e XML pro odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="171d8-202">2</span><span class="sxs-lookup"><span data-stu-id="171d8-202">2</span></span>         | <span data-ttu-id="171d8-203">Podepsat dokument</span><span class="sxs-lookup"><span data-stu-id="171d8-203">Sign document</span></span>                | <span data-ttu-id="171d8-204">Aplikujte digitální certifikát na soubor XML.</span><span class="sxs-lookup"><span data-stu-id="171d8-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="171d8-205">3</span><span class="sxs-lookup"><span data-stu-id="171d8-205">3</span></span>         | <span data-ttu-id="171d8-206">Volejte brazilskou službu SEFAZ</span><span class="sxs-lookup"><span data-stu-id="171d8-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="171d8-207">Odešlete podepsaný soubor XML do webových služeb ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="171d8-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="171d8-208">4</span><span class="sxs-lookup"><span data-stu-id="171d8-208">4</span></span>         | <span data-ttu-id="171d8-209">Odezva procesu</span><span class="sxs-lookup"><span data-stu-id="171d8-209">Process response</span></span>             | <span data-ttu-id="171d8-210">Získejte odpověď webové služby.</span><span class="sxs-lookup"><span data-stu-id="171d8-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="171d8-211">Nastavte adresu URL pro webové služby SEFAZ</span><span class="sxs-lookup"><span data-stu-id="171d8-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="171d8-212">Na stránce **Nastavení verze funkce** na kartě **Akce** na pevné záložce **Akce** vyberte **Volejte brazilskou službu SEFAZ** (ID akce **3**).</span><span class="sxs-lookup"><span data-stu-id="171d8-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="171d8-213">Na pevné záložce **Parametry** v poli **Parametr adresy URL** zadejte adresu URL webové služby SEFAZ pro zrušení schváleného NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="171d8-214">Zpřístupněte prostředí elektronické fakturace a přiřaďte verzi Koncept</span><span class="sxs-lookup"><span data-stu-id="171d8-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="171d8-215">Na stránce **Funkce elektronické fakturace** na kartě **Prostředí** vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="171d8-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="171d8-216">V poli **Prostředí** vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="171d8-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="171d8-217">V poli **Platí od** vyberte datum, kdy má začít platnost prostředí.</span><span class="sxs-lookup"><span data-stu-id="171d8-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="171d8-218">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="171d8-218">Select **Enable**.</span></span>

![Povolení prostředí elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="171d8-220">Změna stavu kursu na Dokončeno.</span><span class="sxs-lookup"><span data-stu-id="171d8-220">Change the status to Completed</span></span>

1. <span data-ttu-id="171d8-221">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="171d8-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="171d8-222">Vyberte **Změnit stav \> Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="171d8-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="171d8-223">Změna stavu kursu na Publikovat.</span><span class="sxs-lookup"><span data-stu-id="171d8-223">Change the status to Publish</span></span>

1. <span data-ttu-id="171d8-224">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="171d8-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="171d8-225">Vyberte **Změnit stav \> Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="171d8-225">Select **Change status \> Publish**.</span></span>

![Publikování funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="171d8-227">Nastavte integraci doplňku elektronické fakturace ve Finance nebo Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="171d8-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="171d8-228">Během instalace dokončíte tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="171d8-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="171d8-229">Zapněte funkci NF-e Federal pro Brazílii.</span><span class="sxs-lookup"><span data-stu-id="171d8-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="171d8-230">Importujte konkrétní datový model ER, mapování datového modelu a formáty, které jsou vyžadovány pro fiskální dokumenty NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="171d8-231">Importujte konfiguraci ER a nastavte typy odpovědí, které jsou nutné k aktualizaci stavu fiskálního dokumentu po vrácení procesu odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="171d8-232">Zapněte funkci NF-e Federal pro Brazílii</span><span class="sxs-lookup"><span data-stu-id="171d8-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="171d8-233">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="171d8-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="171d8-234">Na kartě **Funkce** zaškrtněte políčko **Povolit** v řádku pro odkaz na funkci **BR00053**.</span><span class="sxs-lookup"><span data-stu-id="171d8-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="171d8-235">Importujte mapování datového modelu ER vyžadované pro fiskální dokumenty NF-e</span><span class="sxs-lookup"><span data-stu-id="171d8-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="171d8-236">Přihlášení do aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="171d8-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="171d8-237">V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="171d8-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="171d8-238">Ujistěte se, že je tento poskytovatel konfigurace nastaven na **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="171d8-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="171d8-239">Další informace o tom, jak nastavit poskytovatele jako **Aktivní** naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="171d8-239">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="171d8-240">Vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="171d8-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="171d8-241">Vyberte **Globální prostředek \> Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="171d8-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="171d8-242">Importujte konfiguraci **Mapování fiskálních dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="171d8-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="171d8-243">Importujte konfiguraci ER a nastavte typy odpovědí pro fiskální dokumenty</span><span class="sxs-lookup"><span data-stu-id="171d8-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="171d8-244">V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="171d8-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="171d8-245">Vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="171d8-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="171d8-246">Vyberte **Globální prostředek \> Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="171d8-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="171d8-247">Importujte **Import protokolu chyb NF-e (BR)**, **Formát importu dat odpovědí NF-e (BR)** a **Import zpráv odpovědi NF-e (BR)**.</span><span class="sxs-lookup"><span data-stu-id="171d8-247">Import **NF-e error log import (BR)**, **NF-e response data import format (BR)**, and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="171d8-248">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="171d8-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="171d8-249">Na kartě **Elektronický dokument** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="171d8-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="171d8-250">V poli **Název tabulky** zadejte **Záhlaví fiskálního dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="171d8-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="171d8-251">V poli **Kontext dokumentu** vyberte **Kontextový model faktury zákazníka - kontext fiskálního dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="171d8-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="171d8-252">Vybrat **Typy odpovědí**.</span><span class="sxs-lookup"><span data-stu-id="171d8-252">Select **Response types**.</span></span>
9. <span data-ttu-id="171d8-253">Vyberte **Nový** a pak v poli **Typ odpovědí** vyberte **Odpověď**.</span><span class="sxs-lookup"><span data-stu-id="171d8-253">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="171d8-254">V poli **Stav odeslání** vyberte **Čeká na zpracování**.</span><span class="sxs-lookup"><span data-stu-id="171d8-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="171d8-255">V poli **Mapování modelů** vyberte **Formát importu zprávy odpovědi - mapování modelu ze zprávy odpovědi**.</span><span class="sxs-lookup"><span data-stu-id="171d8-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="171d8-256">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="171d8-256">Select **Save**.</span></span>
13. <span data-ttu-id="171d8-257">Vyberte **Nový** a pak v poli **Typ odpovědí** zadejte **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="171d8-257">Select **New**, and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="171d8-258">V poli **Stav odeslání** vyberte **Čeká na zpracování**.</span><span class="sxs-lookup"><span data-stu-id="171d8-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="171d8-259">V poli **Mapování modelů** vyberte **Formát importu dat odpovědí NFe - import dat odpovědí**.</span><span class="sxs-lookup"><span data-stu-id="171d8-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="171d8-260">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="171d8-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="171d8-261">Zpracování elektronických faktur</span><span class="sxs-lookup"><span data-stu-id="171d8-261">Electronic invoice processing</span></span>

<span data-ttu-id="171d8-262">Během zpracování ve Finance dokončíte tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="171d8-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="171d8-263">Odešlete fiskální dokument prostřednictvím doplňku Elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="171d8-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="171d8-264">Zobrazte protokoly o provedení odeslání a zkontrolujte výsledky zpracování.</span><span class="sxs-lookup"><span data-stu-id="171d8-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="171d8-265">Odešlete zrušení fiskálního dokumentu prostřednictvím doplňku Elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="171d8-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="171d8-266">Odešlete fiskální dokumenty NF-e k autorizaci SEFAZ</span><span class="sxs-lookup"><span data-stu-id="171d8-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="171d8-267">Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** již neluze používat starý postup pro odesílání fiskálních dokumentů NF-e k autorizaci (**Proces exportu / importu NF-e**).</span><span class="sxs-lookup"><span data-stu-id="171d8-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization (**Export/Import NF-e process**) can no longer be used.</span></span> <span data-ttu-id="171d8-268">Je nahrazen novým procesem, který je pojmenován **Odesílejte elektronické dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="171d8-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="171d8-269">Než budete pokračovat, ujistěte se, že máte jeden nebo více fiskálních dokumentů zákazníka model 55, které byly vystaveny fiskálním zřízením zákazníka.</span><span class="sxs-lookup"><span data-stu-id="171d8-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="171d8-270">Směr pro tyto fiskální dokumenty musí být nastaven na **Odchozí** a stav musí být **Vytvořeno**.</span><span class="sxs-lookup"><span data-stu-id="171d8-270">The direction for these fiscal documents must be set to **Outgoing**, and the status must be **Created**.</span></span> <span data-ttu-id="171d8-271">Další informace viz [Vydat fiskální dokument zákazníka (Brazílie)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span><span class="sxs-lookup"><span data-stu-id="171d8-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="171d8-272">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Odesílejte elektronické dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="171d8-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="171d8-273">Pro první odeslání jakéhokoli dokumentu vždy nastavte možnost **Znovu odeslat dokumenty** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="171d8-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="171d8-274">Pokud musíte znovu odeslat dokument prostřednictvím služby, nastavte tuto možnost na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="171d8-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="171d8-275">Na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a otevřete dialogové okno **Dotaz**, kde můžete vytvořit dotaz pro výběr dokumentů k odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="171d8-276">Na kartě **Rozsah** vyberte možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="171d8-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="171d8-277">V poli **Tabulka** vyberte **Záhlaví fiskálního dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="171d8-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="171d8-278">V poli **Odvozená tabulka** vyberte **Záhlaví fiskálního dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="171d8-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="171d8-279">V poli **Pole** zvolte **Číslo**.</span><span class="sxs-lookup"><span data-stu-id="171d8-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="171d8-280">V poli **Kritéria** zadejte číslo fiskálního dokladu, který má být odeslán.</span><span class="sxs-lookup"><span data-stu-id="171d8-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="171d8-281">Zvolte **OK** a zavřete dialogové okno **Dotaz**.</span><span class="sxs-lookup"><span data-stu-id="171d8-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="171d8-282">Vyberte **OK** k odeslání vybraných dokumentů.</span><span class="sxs-lookup"><span data-stu-id="171d8-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="171d8-283">Během prvního pokusu o odeslání dokumentu prostřednictvím služby budete vyzváni k potvrzení spojení s doplňkem Elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="171d8-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="171d8-284">Vyberte **Klikněte zde pro připojení ke službě elektronického odesílání dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="171d8-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="171d8-285">Zobrazit všechny protokoly odeslání</span><span class="sxs-lookup"><span data-stu-id="171d8-285">View all submission logs</span></span>

<span data-ttu-id="171d8-286">Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** je k dispozici nová stránka, která vám umožní sledovat proces odesílání dokumentů.</span><span class="sxs-lookup"><span data-stu-id="171d8-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="171d8-287">Můžete tuto stránku použít, chcete-li si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty.</span><span class="sxs-lookup"><span data-stu-id="171d8-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="171d8-288">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="171d8-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="171d8-289">V poli **Typ dokumentu** vyberte **Záhlaví fiskálního dokumentu** pro filtrování pouze fiskálních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="171d8-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="171d8-290">V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![Zobrazení podrobností protokolu odeslání.](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="171d8-292">U fiskálních dokumentů NF-e sloupec **Chybový kód** zobrazí návratový kód, který byl vrácen webovými službami SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="171d8-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="171d8-293">Prohlédněte si protokoly o odeslání prostřednictvím stránky fiskálních dokumentů</span><span class="sxs-lookup"><span data-stu-id="171d8-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="171d8-294">Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** můžete také zobrazit protokoly odeslání prostřednictvím stránky fiskálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="171d8-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="171d8-295">Přejděte na **Hlavní kniha \> Dotazy a sestavy \> Fiskální dokumenty \> Všechny fiskální dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="171d8-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="171d8-296">Vyberte fiskální dokument, který byl dříve odeslán prostřednictvím doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="171d8-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="171d8-297">V podokně akcí na kartě **NF-e federální** vyberte **Elektronický protokol dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="171d8-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![Prohlížení protokolů o odeslání ze stránky fiskálních dokumentů](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="171d8-299">Odešlete schválené fiskální dokumenty NF-e ke zrušení SEFAZ</span><span class="sxs-lookup"><span data-stu-id="171d8-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="171d8-300">Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** již nelze používat starý postup pro zrušení fiskálních dokumentů NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="171d8-301">Je nahrazen novým procesem zrušení, který je vložen do stránky **Elektronický protokol pro odesílání dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="171d8-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="171d8-302">Ujistěte se, že jste zrušili fiskální dokument zákazníka pro schválený fiskální dokument NF-e.</span><span class="sxs-lookup"><span data-stu-id="171d8-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="171d8-303">Další informace viz [Zrušit fiskální dokument zákazníka (Brazílie)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span><span class="sxs-lookup"><span data-stu-id="171d8-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="171d8-304">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="171d8-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="171d8-305">Vyberte fiskální dokument a poté vyberte **Funkce \> Odeslat související příspěvky**.</span><span class="sxs-lookup"><span data-stu-id="171d8-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="171d8-306">Zadejte popis souvisejícího příspěvku a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="171d8-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="171d8-307">Zobrazit protokoly zrušení</span><span class="sxs-lookup"><span data-stu-id="171d8-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="171d8-308">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="171d8-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="171d8-309">V poli **Typ dokumentu** vyberte **Záhlaví fiskálního dokumentu** pro filtrování pouze fiskálních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="171d8-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="171d8-310">Vyberte fiskální dokument a poté na stránce Akce vyberte **Dotazy \> Související příspěvky**.</span><span class="sxs-lookup"><span data-stu-id="171d8-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="171d8-311">Související odeslání jsou odeslání související s hlavním podáním, které bylo provedeno jako první.</span><span class="sxs-lookup"><span data-stu-id="171d8-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="171d8-312">Například odeslání, které autorizuje konkrétní NF-e, je hlavním odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="171d8-313">Odeslání, které požaduje zrušení stejného NF-e v SEFAZ, je souvisejícím odesdláním.</span><span class="sxs-lookup"><span data-stu-id="171d8-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="171d8-314">Existuje pouze proto, že požaduje zrušení úlohy, která byla provedena jiným odesláním.</span><span class="sxs-lookup"><span data-stu-id="171d8-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="171d8-315">Stránka **Související odeslání** zobrazuje všechna související odeslání a jejich stav odeslání pro daný fiskální dokument.</span><span class="sxs-lookup"><span data-stu-id="171d8-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="171d8-316">Na následujícím obrázku představuje první řádek odeslání, které požadovalo schválení fiskálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="171d8-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="171d8-317">Druhý řádek představuje odeslání, které zrušilo daný fiskální dokument.</span><span class="sxs-lookup"><span data-stu-id="171d8-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![Zobrazit protokoly odeslání zrušení](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="171d8-319">V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.</span><span class="sxs-lookup"><span data-stu-id="171d8-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Zobrazení podrobností protokolu odeslání zrušení](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="171d8-321">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="171d8-321">Privacy notice</span></span>
<span data-ttu-id="171d8-322">Povolení funkce BR-00053 (NF-e Federal) může vyžadovat odesílání omezených dat, která zahrnují daňové identifikační číslo organizace.</span><span class="sxs-lookup"><span data-stu-id="171d8-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="171d8-323">To bude předáno agenturám třetích stran oprávněným daňovým úřadem pro účely zasílání elektronických faktur tomuto daňovému úřadu v předdefinovaném formátu požadovaném pro integraci s webovými službami těchto vlád.</span><span class="sxs-lookup"><span data-stu-id="171d8-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="171d8-324">Správce může povolit a zakázat funkci BR-00053 (NF-e Federal) přechodem na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="171d8-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="171d8-325">Vyberte kartu **Funkce**, vyberte řádek obsahující funkci BR-00053 a poté proveďte příslušný výběr.</span><span class="sxs-lookup"><span data-stu-id="171d8-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="171d8-326">Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="171d8-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="171d8-327">Další informace najdete v oddílech Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země.</span><span class="sxs-lookup"><span data-stu-id="171d8-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="171d8-328">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="171d8-328">Additional resources</span></span>

- [<span data-ttu-id="171d8-329">Přehled doplňku Elektronická fakturace</span><span class="sxs-lookup"><span data-stu-id="171d8-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="171d8-330">Začněte s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="171d8-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="171d8-331">Nastavení doplňku Elektronická fakturace</span><span class="sxs-lookup"><span data-stu-id="171d8-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
