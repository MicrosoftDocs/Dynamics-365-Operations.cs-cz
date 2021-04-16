---
title: Začínáme s Elektronickou fakturací pro Mexiko
description: Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Mexiko.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2f5dd1d6bc520c9f5349c77dfcabdf2d538881ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840045"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="efc33-103">Začínáme s Elektronickou fakturací pro Mexiko</span><span class="sxs-lookup"><span data-stu-id="efc33-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="efc33-104">Elektronická fakturace pro Mexiko aktuálně nepodporuje všechny funkce, které jsou k dispozici v dokumentu Comprobante Fiscal Digital por Internet (CFDI) a v související integraci zabudované do Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="efc33-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="efc33-105">Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Mexiko.</span><span class="sxs-lookup"><span data-stu-id="efc33-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="efc33-106">Provede vás konfiguračními kroky, které jsou závislé na zemi v Regulatory Configuration Services (RCS) a Finance.</span><span class="sxs-lookup"><span data-stu-id="efc33-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="efc33-107">Také vás provede kroky, které musíte ve Finance dodržovat, abyste mohli prostřednictvím služby odesílat faktury CFDI, a vysvětlí, jak zkontrolovat výsledky zpracování a stav faktur CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="efc33-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="efc33-108">Prerequisites</span></span>

<span data-ttu-id="efc33-109">Než dokončíte kroky v tomto tématu, musíte provést kroky v [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="efc33-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="efc33-110">Nastavení RCS</span><span class="sxs-lookup"><span data-stu-id="efc33-110">RCS setup</span></span>

<span data-ttu-id="efc33-111">Během instalace RCS dokončíte tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="efc33-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="efc33-112">Importujte funkci elektronické fakturace pro zpracování faktur CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="efc33-113">Zkontrolujte konfigurace formátu, které jsou vyžadovány ke generování, odesílání a přijímání odpovědí o fakturách CFDI a k odesílání a přijímání odpovědí o zrušení.</span><span class="sxs-lookup"><span data-stu-id="efc33-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="efc33-114">Nakonfigurujte události, které podporují scénáře odeslání faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="efc33-115">Publikujte funkci elektronické fakturace pro faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="efc33-116">„Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server Elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="efc33-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="efc33-117">V tomto případě jsou faktury CFDI (MX) funkcí elektronické fakturace, kterou nastavíte.</span><span class="sxs-lookup"><span data-stu-id="efc33-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="efc33-118">Import funkce elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="efc33-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="efc33-119">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="efc33-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="efc33-120">V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="efc33-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="efc33-121">Na stránce **Funkce elektronické fakturace** vyberte **Import**, chcete-li importovat funkci **Faktury CFDI (MX)** z globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="efc33-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efc33-122">Pokud nevidíte funkci v seznamu, vyberte **Synchronizovat** a potom opakujte krok 3.</span><span class="sxs-lookup"><span data-stu-id="efc33-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![Funkce importu faktur CFDI (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="efc33-124">Při importu funkce **Faktury CFDI (MX)** z globálního úložiště importují se také všechna nastavení funkcí, včetně konfigurací a akcí.</span><span class="sxs-lookup"><span data-stu-id="efc33-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="efc33-125">Vytvořte novou verzi funkce faktur CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="efc33-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="efc33-126">Můžete vytvořit novou verzi, pokud je třeba například aktualizovat adresy URL.</span><span class="sxs-lookup"><span data-stu-id="efc33-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="efc33-127">Další informace viz [Elektronická fakturace CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="efc33-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="efc33-128">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="efc33-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Přidání nové verze funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="efc33-130">Aktualizujte verzi konfigurace</span><span class="sxs-lookup"><span data-stu-id="efc33-130">Update the configuration version</span></span>

1. <span data-ttu-id="efc33-131">Na stránce **Funkce elektronické fakturace** na kartě **Konfigurace** vyberte **Přidat** nebo **Odebrat** ke správě verzí konfigurace (konfigurace formátu souboru ER).</span><span class="sxs-lookup"><span data-stu-id="efc33-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Správa konfigurací funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="efc33-133">Když vytvoříte novou verzi, všechny konfigurace se zdědí z poslední publikované verze.</span><span class="sxs-lookup"><span data-stu-id="efc33-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="efc33-134">Ke zpracování faktur CFDI jsou vyžadovány následující konfigurace:</span><span class="sxs-lookup"><span data-stu-id="efc33-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="efc33-135">Faktura CFDI (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="efc33-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="efc33-136">Import zpráv odpovědi CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-136">CFDI response message import</span></span>
    - <span data-ttu-id="efc33-137">Import protokolu chyb CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-137">CFDI error log import</span></span>
    - <span data-ttu-id="efc33-138">Žádost o zrušení CFDI (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="efc33-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="efc33-139">Faktura CFDI (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="efc33-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="efc33-140">V seznamu vyberte verzi konfigurace a poté vyberte **Upravit** nebo **Zobrazit**, chcete-li otevřít stránku **Návrhář formátů**, kde můžete upravit nebo zobrazit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="efc33-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Otevření stránky Návrhář formátu](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="efc33-142">Použijte stránku **Návrhář formátů**, chcete-li upravovat a prohlížet konfigurace souborů ve formátu ER.</span><span class="sxs-lookup"><span data-stu-id="efc33-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="efc33-143">Další informace získáte v tématu [Vytvoření konfigurací elektronického dokumentu](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="efc33-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Stránka návrháře formátu](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="efc33-145">Spravujte nastavení funkce elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="efc33-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="efc33-146">Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** vyberte **Přidat**, **Odebrat** nebo **Upravit** ke správě nastavení funkcí elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="efc33-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Správa nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="efc33-148">Chcete-li odeslat faktury CFDI k autorizaci (vygenerovat soubor XML, odeslat soubor XML a zpracovat odpověď), je vyžadováno nastavení funkce **Prodejní faktura**.</span><span class="sxs-lookup"><span data-stu-id="efc33-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="efc33-149">Chcete-li odeslat zrušení faktury CFDI, jsou vyžadována nastavení funkcí **Zrušení** a **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="efc33-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="efc33-150">Nakonfigurujte nastavení funkce prodejní faktury</span><span class="sxs-lookup"><span data-stu-id="efc33-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="efc33-151">Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Prodejní faktura**.</span><span class="sxs-lookup"><span data-stu-id="efc33-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="efc33-152">Vyberte **Upravit**, chcete-li konfigurovat akce, pravidla použitelnosti a proměnné.</span><span class="sxs-lookup"><span data-stu-id="efc33-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![Úprava nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="efc33-154">Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí.</span><span class="sxs-lookup"><span data-stu-id="efc33-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="efc33-155">Akce definují seznam operací, které je nutné spustit v postupném pořadí, aby bylo možné provést úplné provedení události.</span><span class="sxs-lookup"><span data-stu-id="efc33-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Karta Akce](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="efc33-157">ID akce</span><span class="sxs-lookup"><span data-stu-id="efc33-157">Action ID</span></span> | <span data-ttu-id="efc33-158">Akce</span><span class="sxs-lookup"><span data-stu-id="efc33-158">Action</span></span>                   | <span data-ttu-id="efc33-159">Název akce</span><span class="sxs-lookup"><span data-stu-id="efc33-159">Action name</span></span>                                  | <span data-ttu-id="efc33-160">Popis akce</span><span class="sxs-lookup"><span data-stu-id="efc33-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="efc33-161">1</span><span class="sxs-lookup"><span data-stu-id="efc33-161">1</span></span>         | <span data-ttu-id="efc33-162">Převod dokumentu</span><span class="sxs-lookup"><span data-stu-id="efc33-162">Transform document</span></span>       | <span data-ttu-id="efc33-163">Generujte elektronickou fakturu CFDI bez digitální značky</span><span class="sxs-lookup"><span data-stu-id="efc33-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="efc33-164">Vygenerujte elektronickou fakturu CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="efc33-165">2</span><span class="sxs-lookup"><span data-stu-id="efc33-165">2</span></span>         | <span data-ttu-id="efc33-166">Podepsat dokument</span><span class="sxs-lookup"><span data-stu-id="efc33-166">Sign document</span></span>            | <span data-ttu-id="efc33-167">Digitální značka</span><span class="sxs-lookup"><span data-stu-id="efc33-167">Digital sign</span></span>                                 | <span data-ttu-id="efc33-168">Digitálně podepište e-fakturu k odeslání.</span><span class="sxs-lookup"><span data-stu-id="efc33-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="efc33-169">3</span><span class="sxs-lookup"><span data-stu-id="efc33-169">3</span></span>         | <span data-ttu-id="efc33-170">Volejte mexickou službu PAC</span><span class="sxs-lookup"><span data-stu-id="efc33-170">Call Mexican PAC service</span></span> | <span data-ttu-id="efc33-171">Odeslat elektronickou fakturu CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="efc33-172">Klient Windows Communication Foundation (WCF) odešle elektronickou fakturu CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="efc33-173">4</span><span class="sxs-lookup"><span data-stu-id="efc33-173">4</span></span>         | <span data-ttu-id="efc33-174">Odezva procesu</span><span class="sxs-lookup"><span data-stu-id="efc33-174">Process response</span></span>         | <span data-ttu-id="efc33-175">Analyzujte odpověď webové služby</span><span class="sxs-lookup"><span data-stu-id="efc33-175">Analyze web service response</span></span>                 | <span data-ttu-id="efc33-176">Analyzujte odezvu webové služby a vraťte protokol chyb.</span><span class="sxs-lookup"><span data-stu-id="efc33-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="efc33-177">Nastavte adresu URL pro webové Mexican PAZ</span><span class="sxs-lookup"><span data-stu-id="efc33-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="efc33-178">Na stránce **Nastavení verze funkce** na kartě **Akce** na pevné záložce **Akce** vyberte **Volejte mexickou službu PAC**.</span><span class="sxs-lookup"><span data-stu-id="efc33-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="efc33-179">Na pevné záložce **Parametry** v poli **Adresa URL** zadejte adresu URL webové služby pro odeslání faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="efc33-180">Stejným způsobem aktualizujte adresu URL pro akci **Volat mexickou službu PAC** pro nastavení funkcí **Zrušit** a **Žádost o zrušení**.</span><span class="sxs-lookup"><span data-stu-id="efc33-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="efc33-181">Přiřaďte verzi konceptu do prostředí elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="efc33-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="efc33-182">Na stránce **Funkce elektronické fakturace** na kartě **Prostředí** vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="efc33-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="efc33-183">V poli **Prostředí** vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="efc33-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="efc33-184">V poli **Platí od** vyberte datum, kdy má začít platnost prostředí.</span><span class="sxs-lookup"><span data-stu-id="efc33-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="efc33-185">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="efc33-185">Select **Enable**.</span></span>

![Povolení prostředí elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="efc33-187">Změna stavu verze na Dokončeno.</span><span class="sxs-lookup"><span data-stu-id="efc33-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="efc33-188">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="efc33-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="efc33-189">Vyberte **Změnit stav \> Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="efc33-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="efc33-190">Změna stavu verze na Publikováno.</span><span class="sxs-lookup"><span data-stu-id="efc33-190">Change the version status to Published</span></span>

- <span data-ttu-id="efc33-191">Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Změnit stav \> Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="efc33-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="efc33-192">Publikovat funkci elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="efc33-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="efc33-193">Na stránce **Funkce elektronické fakturace** vyberte kartu **Verze**, chcete-li spravovat stav funkce **Faktury CFDI (MX)**.</span><span class="sxs-lookup"><span data-stu-id="efc33-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="efc33-194">Vyberte **Změnit stav** ke změně stavu funkce.</span><span class="sxs-lookup"><span data-stu-id="efc33-194">Select **Change status** to change the status of the feature.</span></span>

![Změna stavu funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="efc33-196">Nastavení integrace Elektronické fakturace ve Finance</span><span class="sxs-lookup"><span data-stu-id="efc33-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="efc33-197">Chcete-li nastavit Elektronickou fakturaci v aplikaci Finance, proveďte tyto úkoly:</span><span class="sxs-lookup"><span data-stu-id="efc33-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="efc33-198">Importujte datový model ER, mapování datového modelu ER a formáte požadované pro faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="efc33-199">Nakonfigurujte typy odpovědí pro aktualizaci faktur CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="efc33-200">Tyto typy odpovědí se používají pro odpověď ze serveru autorizovaného poskytovatele certifikace (PAC).</span><span class="sxs-lookup"><span data-stu-id="efc33-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="efc33-201">Importujte datový model ER, mapování datového modelu ER a kontextové konfigurace pro e-faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="efc33-202">Přihlášení do aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="efc33-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="efc33-203">V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="efc33-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="efc33-204">Ujistěte se, že je tento poskytovatel konfigurace nastaven na **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="efc33-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="efc33-205">Další informace o tom, jak nastavit poskytovatele jako **Aktivní** naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="efc33-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="efc33-206">Vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="efc33-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="efc33-207">Vyberte **Globální prostředek \> Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="efc33-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="efc33-208">Importujte **Model faktury**, **Mapování modelu faktury**, **Formát faktury CFDI (MX)**, **Formát žádosti o zrušení faktury CFDI (MX)** a **Formát zrušení faktury CFDI (MX)**.</span><span class="sxs-lookup"><span data-stu-id="efc33-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="efc33-209">Zapněte funkci pro zpracování faktur CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="efc33-210">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="efc33-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="efc33-211">Na kartě **Funkce** zaškrtněte políčko **Povolit** v řádcích pro odkaz na funkci **MX-00010** and **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="efc33-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![Zapnutí funkcí pro zpracování faktur CFDI](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="efc33-213">Importujte konfiguraci ER a nastavte typy odpovědí pro aktualizaci faktur CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="efc33-214">Import konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="efc33-214">Import ER configurations</span></span>

1. <span data-ttu-id="efc33-215">V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="efc33-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="efc33-216">Vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="efc33-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="efc33-217">Vyberte **Globální prostředek \> Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="efc33-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="efc33-218">Importujte **Model zprávy s odpovědí**, **Import protokolu chyb CFDI (MX)** a **Import zpráv CFDI s odpovědí (MX)**.</span><span class="sxs-lookup"><span data-stu-id="efc33-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="efc33-219">Nastavte typy odpovědí</span><span class="sxs-lookup"><span data-stu-id="efc33-219">Set up the response types</span></span>

1. <span data-ttu-id="efc33-220">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="efc33-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="efc33-221">Na kartě **Elektronický dokument** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="efc33-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="efc33-222">Zadejte deník faktury zákazníka a poté v poli **Název tabulky** vyberte fakturu projektu.</span><span class="sxs-lookup"><span data-stu-id="efc33-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="efc33-223">Pro každou tabulku definujte související kontext dokumentu:</span><span class="sxs-lookup"><span data-stu-id="efc33-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="efc33-224">Pro **Deník faktury zákazníka** zadejte **Kontext faktury zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="efc33-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="efc33-225">Pro **Faktura projektu** zadejte **Kontext faktury projektu**.</span><span class="sxs-lookup"><span data-stu-id="efc33-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="efc33-226">Vyberte **Typy odpovědí**, chcete-li konfigurovat typy odpovědí, které lze vrátit z Elektronické fakturace a zahrnout do deníku faktury zákazníka nebo faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="efc33-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="efc33-227">Vyberte **Nový** a pak v poli **Typ odpovědí** vyberte **Odpověď**.</span><span class="sxs-lookup"><span data-stu-id="efc33-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="efc33-228">V poli **Stav odeslání** vyberte **Čeká na zpracování**.</span><span class="sxs-lookup"><span data-stu-id="efc33-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="efc33-229">V poli **Mapování modelů** vyberte **Formát importu zprávy odpovědi - mapování modelu ze zprávy odpovědi**.</span><span class="sxs-lookup"><span data-stu-id="efc33-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="efc33-230">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="efc33-230">Select **Save**.</span></span>
9. <span data-ttu-id="efc33-231">Vyberte **Nový** a pak v poli **Typ odpovědí** vyberte **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="efc33-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="efc33-232">V poli **Stav odeslání** vyberte **Čeká na zpracování**.</span><span class="sxs-lookup"><span data-stu-id="efc33-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="efc33-233">V poli **Mapování modelů** vyberte **Formát importu dat odpovědí CFDI (podrobnosti) - import dat odpovědí**.</span><span class="sxs-lookup"><span data-stu-id="efc33-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="efc33-234">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="efc33-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="efc33-235">Zpracovat elektronické faktury v aplikaci Finance</span><span class="sxs-lookup"><span data-stu-id="efc33-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="efc33-236">Během zpracování CFDI faktur ve Finance prostřednictvím Elektronické fakturace můžete provádět následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="efc33-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="efc33-237">Odesílat faktury CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="efc33-238">Zobrazit protokoly provádění podání.</span><span class="sxs-lookup"><span data-stu-id="efc33-238">View the submission execution logs.</span></span>
- <span data-ttu-id="efc33-239">Odesílat zrušení faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="efc33-240">Odesílat faktury CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-240">Submit CFDI invoices</span></span>

<span data-ttu-id="efc33-241">Po zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace** již nelze používat postup pro **Export/import elektronické faktury** pro odesílání faktur CFDI (**Pohledávky \> Faktury \> Elektronické faktury)**.</span><span class="sxs-lookup"><span data-stu-id="efc33-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="efc33-242">Je nahrazen novým procesem, který je pojmenován **Odesílejte elektronické dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="efc33-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="efc33-243">Před použitím nového procesu **Odeslat elektronické dokumenty** ověřte, že bylo dokončeno nastavení požadované pro mexické e-faktury.</span><span class="sxs-lookup"><span data-stu-id="efc33-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="efc33-244">Další informace naleznete v tématu [Rozložení CFDI verze 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="efc33-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="efc33-245">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Odesílejte elektronické dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="efc33-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="efc33-246">Pro první odeslání jakéhokoli dokumentu vždy nastavte možnost **Znovu odeslat dokumenty** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="efc33-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="efc33-247">Pokud musíte znovu odeslat dokument prostřednictvím služby, nastavte tuto možnost na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="efc33-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="efc33-248">Na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a otevřete dialogové okno **Dotaz**, kde můžete vytvořit dotaz pro výběr dokumentů k odeslání.</span><span class="sxs-lookup"><span data-stu-id="efc33-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Odeslání dokumentu CFDI](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="efc33-250">Během prvního pokusu o odeslání dokumentu prostřednictvím služby budete vyzváni k potvrzení spojení s Elektronickou fakturací.</span><span class="sxs-lookup"><span data-stu-id="efc33-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="efc33-251">Vyberte **Klikněte zde pro připojení ke službě elektronického odesílání dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="efc33-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="efc33-252">Zobrazit protokoly odeslání</span><span class="sxs-lookup"><span data-stu-id="efc33-252">View submission logs</span></span>

<span data-ttu-id="efc33-253">Můžete si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty nebo pouze pro jeden odeslaný dokument.</span><span class="sxs-lookup"><span data-stu-id="efc33-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="efc33-254">Zobrazit všechny protokoly odeslání</span><span class="sxs-lookup"><span data-stu-id="efc33-254">View all submission logs</span></span>

<span data-ttu-id="efc33-255">Po zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace** je k dispozici nová stránka, která vám umožní sledovat proces odesílání dokumentů.</span><span class="sxs-lookup"><span data-stu-id="efc33-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="efc33-256">Můžete tuto stránku použít, chcete-li si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty.</span><span class="sxs-lookup"><span data-stu-id="efc33-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="efc33-257">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="efc33-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="efc33-258">V poli **Typ dokumentu** vyberte **Deník faktury zákazníka**, chcete-li filtrovat požadované elektronické dokumenty.</span><span class="sxs-lookup"><span data-stu-id="efc33-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Výběr typu dokumentu pro zobrazení protokolů odeslání](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="efc33-260">V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.</span><span class="sxs-lookup"><span data-stu-id="efc33-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Zobrazení podrobností protokolu odeslání.](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="efc33-262">Informace v protokolech podání jsou rozděleny mezi tři pevné záložky:</span><span class="sxs-lookup"><span data-stu-id="efc33-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="efc33-263">**Zpracování akcí** - tato pevná záložka zobrazí protokol provádění akcí, které jsou konfigurovány ve verzi funkce, která byla nastavena v RCS.</span><span class="sxs-lookup"><span data-stu-id="efc33-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="efc33-264">Sloupec **Stav** ukazuje, zda byla akce úspěšně spuštěna.</span><span class="sxs-lookup"><span data-stu-id="efc33-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="efc33-265">**Soubory akcí** - tato pevná záložka zobrazí přechodné soubory, které byly vygenerovány během provádění akcí.</span><span class="sxs-lookup"><span data-stu-id="efc33-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="efc33-266">Můžete vybrat **Zobrazit** a stáhnout soubor a zobrazit jej.</span><span class="sxs-lookup"><span data-stu-id="efc33-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="efc33-267">**Zpracování protokolu akcí** - Tato pevná záložka zobrazuje výsledky komunikace mezi Elektronickou fakturací a cílovou webovou službou.</span><span class="sxs-lookup"><span data-stu-id="efc33-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="efc33-268">Ukazuje také, co bylo vráceno zpracováním z webové služby.</span><span class="sxs-lookup"><span data-stu-id="efc33-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="efc33-269">Sloupec **Chybový kód** zobrazí návratový kód, který byl vrácen autorizační webovou službou.</span><span class="sxs-lookup"><span data-stu-id="efc33-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="efc33-270">Po autorizaci odeslané faktury CFDI se její stav aktualizuje na **Schválený**.</span><span class="sxs-lookup"><span data-stu-id="efc33-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="efc33-271">Zobrazit protokoly o odeslání z faktur CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="efc33-272">Po zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace** můžete také zobrazit protokoly odeslání z faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="efc33-273">Přejděte na **Pohledávky \> Dotazy a sestavy \> CFDI (elektronické faktury)**.</span><span class="sxs-lookup"><span data-stu-id="efc33-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="efc33-274">Vyberte CFDI fakturu, která byla odeslána po zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="efc33-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="efc33-275">V podokně akcí na kartě **Historie** vyberte **Elektronický protokol dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="efc33-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Zobrazit protokoly o odeslání z faktur CFDI](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="efc33-277">U faktur CFDI, které byly odeslány před zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace**, je k dispozici tlačítko **Historie**.</span><span class="sxs-lookup"><span data-stu-id="efc33-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="efc33-278">U faktur CFDI, které byly odeslány po zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace**, tlačítko **Historie** není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="efc33-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="efc33-279">Zrušení odeslání faktury CFDI</span><span class="sxs-lookup"><span data-stu-id="efc33-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="efc33-280">Po zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace** již nelze používat starý postup pro zrušení faktur CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="efc33-281">Je nahrazen novým procesem zrušení, který je vložen do stránky **Elektronický protokol pro odesílání dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="efc33-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="efc33-282">Přejděte na **Pohledávky \> Dotazy a sestavy \> CFDI (elektronické faktury)**.</span><span class="sxs-lookup"><span data-stu-id="efc33-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="efc33-283">Pokud má faktura CFDI stav **Schváleno**, vyberte **Funkce \> Zrušit CFDI**.</span><span class="sxs-lookup"><span data-stu-id="efc33-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="efc33-284">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="efc33-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="efc33-285">Vyberte fakturu CFDI a poté vyberte **Funkce \> Odeslat související příspěvky**.</span><span class="sxs-lookup"><span data-stu-id="efc33-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="efc33-286">Zadejte popis souvisejícího příspěvku a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="efc33-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="efc33-287">Zobrazit protokoly zrušení</span><span class="sxs-lookup"><span data-stu-id="efc33-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="efc33-288">Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="efc33-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="efc33-289">V poli **Typ dokumentu** vyberte **Deník faktury zákazníka**, chcete-li filtrovat pouze dikumenty deníku zákaznických faktur.</span><span class="sxs-lookup"><span data-stu-id="efc33-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="efc33-290">Vyberte fakturu CFDI a poté na stránce Akce vyberte **Dotazy \> Související příspěvky**.</span><span class="sxs-lookup"><span data-stu-id="efc33-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="efc33-291">Stránka **Související odeslání** zobrazuje všechna související odeslání a jejich stav odeslání pro danou fakturu CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="efc33-292">Na následujícím obrázku představuje první řádek odeslání, které požadovalo schválení faktury CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="efc33-293">Druhý řádek představuje odeslání, které zrušilo danou fakturu CFDI.</span><span class="sxs-lookup"><span data-stu-id="efc33-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Zobrazit protokoly odeslání zrušení](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="efc33-295">V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.</span><span class="sxs-lookup"><span data-stu-id="efc33-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Zobrazení podrobností protokolu odeslání zrušení](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="efc33-297">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="efc33-297">Privacy notice</span></span>
<span data-ttu-id="efc33-298">Aktivace funkce **Mexická elektronická faktura CFDI (MX)** může vyžadovat odesílání omezených dat, která zahrnují daňové identifikační číslo organizace.</span><span class="sxs-lookup"><span data-stu-id="efc33-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="efc33-299">To bude předáno agenturám třetích stran oprávněným daňovým úřadem pro účely zasílání elektronických faktur tomuto daňovému úřadu v předdefinovaném formátu požadovaném pro integraci s webovými službami těchto vlád.</span><span class="sxs-lookup"><span data-stu-id="efc33-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="efc33-300">Správce může povolit a zakázat funkci **Mexická elektronická faktura CFDI (MX)** přechodem na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="efc33-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="efc33-301">Vyberte kartu **Funkce**, vyberte řádky, které obsahují funkci **Mexická elektronická faktura CFDI (MX)**, a poté proveďte příslušný výběr.</span><span class="sxs-lookup"><span data-stu-id="efc33-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="efc33-302">Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="efc33-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="efc33-303">Další informace najdete v oddílech Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země.</span><span class="sxs-lookup"><span data-stu-id="efc33-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efc33-304">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="efc33-304">Additional resources</span></span>

- [<span data-ttu-id="efc33-305">Přehled elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="efc33-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="efc33-306">Začínáme s Elektronickou fakturací</span><span class="sxs-lookup"><span data-stu-id="efc33-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="efc33-307">Nastavení Elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="efc33-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
