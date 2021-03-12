---
title: Sdílení konfigurací ER v RCS/globálním úložišti s externími organizacemi
description: Toto téma vysvětluje, jak sdílet konfigurace elektronického vykazování (ER) ve službě Microsoft Regulatory Configuration Services (RCS)/globálním úložišti přímo s externími organizacemi.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0973d36a8fddd16d02776ac6567d424ac6ebc3ae
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994293"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="ca72e-103">Sdílejte konfigurace elektronického vykazování (ER) v globálním úložišti služby Microsoft Regulatory Configuration Services (RCS) s externími organizacemi</span><span class="sxs-lookup"><span data-stu-id="ca72e-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca72e-104">Službu Microsoft Regulatory Configuration Services (RCS) můžete použít ke sdílení konfigurací elektronického vykazování (ER) a jejich publikování do externích organizací.</span><span class="sxs-lookup"><span data-stu-id="ca72e-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="ca72e-105">Následující postupy vysvětlují, jak uživatel RCS může sdílet verzi konfigurace ER, která byla nakonfigurována v instanci RCS, s externí organizací.</span><span class="sxs-lookup"><span data-stu-id="ca72e-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="ca72e-106">Než budete moci tyto kroky dokončit, je nutné nejprve splnit následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="ca72e-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="ca72e-107">Přistupte k RCS instanci.</span><span class="sxs-lookup"><span data-stu-id="ca72e-107">Access an RCS instance.</span></span>
- <span data-ttu-id="ca72e-108">Vytvořte aktivního poskytovatele konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ca72e-108">Create an active configuration provider.</span></span> <span data-ttu-id="ca72e-109">Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ca72e-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="ca72e-110">Vytvořte a nahrajte novou verzi konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="ca72e-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="ca72e-111">Pro další informace viz [Vytvoření a nahrání nových verzí konfigurace elektronického hlášení (ER)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="ca72e-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="ca72e-112">Musíte se také ujistit, že je pro vaši společnost zajištěno prostředí RCS.</span><span class="sxs-lookup"><span data-stu-id="ca72e-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="ca72e-113">V aplikaci Finance and Operations přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="ca72e-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ca72e-114">Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, pro její zřízení klikněte na externí odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů.</span><span class="sxs-lookup"><span data-stu-id="ca72e-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="ca72e-115">Pokud již bylo pro vaši společnost zřízeno prostředí RCS, přistupte k ní pomocí adresy URL výběrem možnosti přihlášení.</span><span class="sxs-lookup"><span data-stu-id="ca72e-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="ca72e-116">Ověřte konfiguraci, kterou chcete sdílet</span><span class="sxs-lookup"><span data-stu-id="ca72e-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="ca72e-117">Postupujte podle těchto kroků a ověřte, že konfigurace, kterou chcete sdílet, již byla nahrána do globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="ca72e-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="ca72e-118">V **Elektronickém výkaznictí** vyberte pracovní prostor **Úložiště** pro vašeho poskytovatele konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ca72e-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Poskytovatelé konfigurace](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="ca72e-120">Vyberte **Globální úložiště** \> **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="ca72e-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="ca72e-121">Vyhledejte konfiguraci, kterou chcete sdílet.</span><span class="sxs-lookup"><span data-stu-id="ca72e-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="ca72e-122">Pomocí pole filtru můžete vyhledávání zúžit.</span><span class="sxs-lookup"><span data-stu-id="ca72e-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="ca72e-123">Pokud nemůžete najít konfiguraci v globálním úložišti, postupujte podle těchto kroků: [Vytvořte a nahrajte novou verzi konfigurace elektronického výkaznictví (ER)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="ca72e-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="ca72e-124">Sdílení konfigurací elektronického výkaznictví s externími organizacemi</span><span class="sxs-lookup"><span data-stu-id="ca72e-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="ca72e-125">Po vytvoření konfigurace u vašeho poskytovatele konfigurace ji můžete sdílet přímo s externími organizacemi pomocí pevné záložky **Sdíleno s** na stránce **Globální úložiště konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="ca72e-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="ca72e-126">V **Elektronickém výkaznictí** vyberte pracovní prostor **Úložiště** pro vašeho poskytovatele konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ca72e-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="ca72e-127">Vyberte **Globální úložiště** \> **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="ca72e-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="ca72e-128">Vyberte konfiguraci, kterou chcete sdílet.</span><span class="sxs-lookup"><span data-stu-id="ca72e-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="ca72e-129">Na pevné kartě **Sdíleno s** vyberte **Organizace**.</span><span class="sxs-lookup"><span data-stu-id="ca72e-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Sdíleno pomocí pevné záložky](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="ca72e-131">V dialogovém okně zadejte název domény pro externí organizaci a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca72e-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Sdílejte konfigurační verzi pomocí dialogového okna externí organizace](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="ca72e-133">Konfigurace je sdílena s externí organizací a je k dispozici této organizaci v globálním úložišti.</span><span class="sxs-lookup"><span data-stu-id="ca72e-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="ca72e-134">Odtud ji lze importovat do instance RCS organizace nebo do jejích instancí aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca72e-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="ca72e-135">Chcete-li zrušit sdílení konfigurace, která byla dříve sdílena s externí organizací, vyberte konfiguraci a klikněte na **Zrušit sdílení** a poté vyberte **OK**</span><span class="sxs-lookup"><span data-stu-id="ca72e-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
