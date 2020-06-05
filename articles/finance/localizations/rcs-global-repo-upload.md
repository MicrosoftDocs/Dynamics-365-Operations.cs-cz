---
title: Vytvoření konfigurací elektronického výkaznictví v RCS a jejich odeslání do globálního úložiště
description: Toto téma vysvětluje, jak vytvořit konfiguraci elektronického vykazování (ER) ve službě Microsoft Regulatory Configuration Services (RCS) a odeslat ji do globálního úložiště.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371235"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="8c036-103">Vytvoření konfigurací v Regulatory Configuration Services (RCS) a jejich odeslání do globálního úložiště</span><span class="sxs-lookup"><span data-stu-id="8c036-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c036-104">Službu Microsoft Regulatory Configuration Services (RCS) můžete použít k navrhování konfigurací elektronického vykazování (ER) a jejich publikování, aby mohly být použity ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="8c036-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="8c036-105">Následující postupy vysvětlují, jak může uživatel v roli Správce systému nebo Návrháře elektronického výkaznictví vytvořit odvozenou verzi konfigurace ER, která byla nakonfigurována v instanci RCS, a poté odvozenou konfiguraci nahrát do globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="8c036-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="8c036-106">Než budete moci tyto kroky dokončit, je nutné nejprve splnit následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="8c036-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="8c036-107">Přistupte k RCS instanci.</span><span class="sxs-lookup"><span data-stu-id="8c036-107">Access an RCS instance.</span></span>
- <span data-ttu-id="8c036-108">Vytvořte aktivního poskytovatele konfigurace.</span><span class="sxs-lookup"><span data-stu-id="8c036-108">Create an active configuration provider.</span></span> <span data-ttu-id="8c036-109">Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8c036-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="8c036-110">Musíte se také ujistit, že je pro vaši společnost zajištěno prostředí RCS.</span><span class="sxs-lookup"><span data-stu-id="8c036-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="8c036-111">V aplikaci Finance and Operations přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="8c036-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="8c036-112">Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, pro její zřízení klikněte na externí odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů.</span><span class="sxs-lookup"><span data-stu-id="8c036-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="8c036-113">Pokud již bylo pro vaši společnost zřízeno prostředí RCS, přistupte k ní pomocí adresy URL výběrem možnosti přihlášení.</span><span class="sxs-lookup"><span data-stu-id="8c036-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="8c036-114">Vytvoření odvozenou verzi konfigurace v RCS</span><span class="sxs-lookup"><span data-stu-id="8c036-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="8c036-115">V pracovním prostoru **Elektronické výkaznictví** ověřte, zda máte aktivního poskytovatele konfigurace pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="8c036-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="8c036-116">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="8c036-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="8c036-117">Vyberte konfiguraci, ze které chcete odvodit novou verzi.</span><span class="sxs-lookup"><span data-stu-id="8c036-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="8c036-118">Pomocí pole filtru nad stromem můžete vyhledávání zúžit.</span><span class="sxs-lookup"><span data-stu-id="8c036-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="8c036-119">Vyberte **Vytvořit konfiguraci** \> **Odvodit z názvu**.</span><span class="sxs-lookup"><span data-stu-id="8c036-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="8c036-120">Zadejte jméno a popis a poté vyberte **Vytvořit konfiguraci** k vytvoření nové odvozené verze.</span><span class="sxs-lookup"><span data-stu-id="8c036-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="8c036-121">Vyberte nově odvozenou konfiguraci, přidejte popis verze a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c036-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="8c036-122">Stav konfigurace na se změní na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="8c036-122">The status of the configuration to is changed to **Completed**.</span></span>

![Nová verze konfigurace v RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="8c036-124">Při změně stavu konfigurace se může zobrazit chybová zpráva o ověření související s připojenými aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="8c036-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="8c036-125">Chcete-li validaci vypnout, v podokně Akce na kartě **Konfigurace** vyberte **Uživatelské parametry**, a poté nastavte **Přeskočit ověření při změně stavu konfigurace a přeskládat** možnost na **Ano**</span><span class="sxs-lookup"><span data-stu-id="8c036-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="8c036-126">Nahrajte konfiguraci do Globálního úložiště</span><span class="sxs-lookup"><span data-stu-id="8c036-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="8c036-127">Chcete-li s organizací sdílet novou nebo odvozenou konfiguraci, nahrajte ji do Globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="8c036-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="8c036-128">Vyberte dokončenou verzi konfigurace a poté vyberte **Nahrát do úložiště**.</span><span class="sxs-lookup"><span data-stu-id="8c036-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="8c036-129">Vyberte **Globální (Microsoft)** a poté vyberte **Nahrát**.</span><span class="sxs-lookup"><span data-stu-id="8c036-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Nahrání do možností úložiště](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="8c036-131">V dialogovém okně pro potvrzení vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8c036-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="8c036-132">Podle potřeby aktualizujte popis verze a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c036-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="8c036-133">Stav konfigurace je aktualizován na **Sdílení** a konfigurace se nahraje do globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="8c036-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="8c036-134">Odtud můžete s konfigurací pracovat následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="8c036-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="8c036-135">Importujte jej do instance Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8c036-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="8c036-136">Další informace získáte v tématu [(ER) Import konfigurací z RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="8c036-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="8c036-137">Pro sdílení s třetí stranou nebo externí organizací, viz [RCS sdílení konfigurací elektronického výkaznictví (ER) s externími organizacemi](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="8c036-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Odvozená verze konfigurace Intrastat Contoso v globálním úložišti](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
