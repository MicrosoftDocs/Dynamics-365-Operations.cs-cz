---
title: Import aktualizovaných verzí konfigurací ER
description: Toto téma vysvětluje, jak importovat aktualizované verze konfigurací elektronického vykazování (ER) z globálního úložiště konfigurační služby.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679503"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="f3a6a-103">Import aktualizovaných verzí konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="f3a6a-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3a6a-104">[Úložiště](general-electronic-reporting.md#Repository) elektronického výkaznictví (ER) se používají ke sdílení [konfigurací ER](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="f3a6a-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="f3a6a-105">Můžete [importovat](download-electronic-reporting-configuration-lcs.md) konfigurace ER z různých úložišť do vaší instance Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="f3a6a-106">Při importu konfigurací ER mohou [poskytovatelé konfigurací](general-electronic-reporting.md#Provider) publikovat nové [verze](general-electronic-reporting.md#component-versioning) v úložištích, aby bylo možné je sdílet.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="f3a6a-107">Toto téma vysvětluje, jak importovat aktualizované verze konfigurací ER z globálního úložiště konfigurační služby.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="f3a6a-108">Další informace viz [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, konfigurační služba](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="f3a6a-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="f3a6a-109">Kontrola dostupných aktualizovaných verzí</span><span class="sxs-lookup"><span data-stu-id="f3a6a-109">Review the available updated versions</span></span>

1. <span data-ttu-id="f3a6a-110">Přihlaste se k aplikaci Finance použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="f3a6a-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="f3a6a-111">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f3a6a-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="f3a6a-112">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f3a6a-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f3a6a-113">Správce systému</span><span class="sxs-lookup"><span data-stu-id="f3a6a-113">System administrator</span></span>

2. <span data-ttu-id="f3a6a-114">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f3a6a-115">Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Import aktualizovaných verzí konfigurací**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Stránka konfigurací lokalizace](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="f3a6a-117">V dialogovém okně **Import aktualizovaných verzí konfigurací elektronického výkaznictví** vyberte v poli **Režim spouštění** možnost **Zobrazit pouze dostupné aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="f3a6a-118">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-118">Then select **OK**.</span></span> 

    ![Pole Režim spuštění s hodnotou Zobrazit pouze dostupné aktualizace](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="f3a6a-120">Zkontrolujte zprávy, které obdržíte.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-120">Review the messages that you receive.</span></span> <span data-ttu-id="f3a6a-121">Tyto zprávy uvádějí následující informace o konfiguracích ER v aktuální instanci systému Finance a o tom, jak srovnávají s obsahem globálního úložiště:</span><span class="sxs-lookup"><span data-stu-id="f3a6a-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="f3a6a-122">Celkový počet konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="f3a6a-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="f3a6a-123">Konfigurace ER, které nejsou přítomny v globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="f3a6a-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="f3a6a-124">Konfigurace ER, pro které je aktuální verze již k dispozici v aktuální instanci systému Finance (chcete-li zobrazit úplný seznam těchto konfigurací ER, klikněte na odkaz **Podrobnosti zprávy**)</span><span class="sxs-lookup"><span data-stu-id="f3a6a-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Zpráva „Nejnovější verze následujících konfigurací již byly importovány“ a podrobnosti zprávy](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="f3a6a-126">Konfigurace ER, pro které je aktuální verze již k dispozici v globálním úložišti a jež lze importovat do aktuální instance systému Finance (chcete-li zobrazit úplný seznam těchto konfigurací ER, klikněte na odkaz **Podrobnosti zprávy**)</span><span class="sxs-lookup"><span data-stu-id="f3a6a-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Zpráva „Dostupné aktualizace“ a podrobnosti zprávy](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="f3a6a-128">Import dostupných aktualizovaných verzí</span><span class="sxs-lookup"><span data-stu-id="f3a6a-128">Import available updated versions</span></span>

1. <span data-ttu-id="f3a6a-129">Přihlaste se k aplikaci Finance použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="f3a6a-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="f3a6a-130">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f3a6a-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="f3a6a-131">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f3a6a-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f3a6a-132">Správce systému</span><span class="sxs-lookup"><span data-stu-id="f3a6a-132">System administrator</span></span>

2. <span data-ttu-id="f3a6a-133">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f3a6a-134">Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Import aktualizovaných verzí konfigurací**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="f3a6a-135">V dialogovém okně **Import aktualizovaných verzí konfigurací elektronického výkaznictví** vyberte v poli **Režim spouštění** možnost **Importovat nejnovější aktualizace**. Provede se import nejnovějších verzí konfigurací ER z globálního úložiště do aktuální instance systému Finance.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="f3a6a-136">Chcete-li naplánovat dávkovou úlohu importu, nastavte na záložce s náhledem **Spustit na pozadí** u možnosti **Dávkové zpracování** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="f3a6a-137">Pokud chcete import opakovat pravidelně, nakonfigurujte požadované opakování.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Pole Režim spouštění nastavené na Import nejnovějších aktualizací](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="f3a6a-139">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-139">Select **OK**.</span></span>
7. <span data-ttu-id="f3a6a-140">Chcete-li zjistit, jaké verze konfigurací byly importovány, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="f3a6a-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="f3a6a-141">Pokud import spustíte interaktivně místo použití dávkové úlohy, zkontrolujte zprávy, které obdržíte.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Zprávy přijaté během interaktivního importování](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="f3a6a-143">Pokud spouštíte import v dávkovém režimu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="f3a6a-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="f3a6a-144">Přejděte na **Společné** \> **Dotazy** \> **Dávkové úlohy** \> **Moje dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="f3a6a-145">Vyhledejte a vyberte úlohu **Import aktualizací verzí konfigurací elektronického výkaznictví** a poté v podokně Akce vyberte na kartě **Dávková úloha** možnost **Historie dávkových úloh**. Zobrazí se historie úloh.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="f3a6a-146">Na stránce **Historie dávkových úloh** vyberte možnost **Protokol**.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="f3a6a-147">Poté v obdržené zprávě klikněte na odkaz **Podrobnosti zprávy**. Zobrazí se protokol úlohy.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Protokol úlohy](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="f3a6a-149">Nedoporučujeme plánovat opakovanou dávkovou úlohu tak, aby importovala aktualizované verze konfigurací ER přímo z globálního úložiště do produkčního prostředí, protože importované verze budou okamžitě k dispozici k použití.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="f3a6a-150">Místo toho tímto postupem přeneste verze konfigurací ER do prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="f3a6a-151">Poté je můžete vyhodnotit v prostředí sandbox a teprve následně nasadit do produkčního prostředí.</span><span class="sxs-lookup"><span data-stu-id="f3a6a-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3a6a-152">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f3a6a-152">Additional resources</span></span>

- [<span data-ttu-id="f3a6a-153">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f3a6a-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f3a6a-154">Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby</span><span class="sxs-lookup"><span data-stu-id="f3a6a-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
