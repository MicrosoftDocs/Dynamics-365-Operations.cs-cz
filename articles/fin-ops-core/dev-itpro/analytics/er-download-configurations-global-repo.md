---
title: Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby
description: Toto téma vysvětluje, jak stahovat konfigurace elektronického vykazování (ER) z globálního úložiště konfigurační služby.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3a232cd319970e572580bc11f2dbaccbe208f127
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753377"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="8e3fa-103">Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby</span><span class="sxs-lookup"><span data-stu-id="8e3fa-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e3fa-104">Toto téma vysvětluje, jak stahovat [konfigurace elektronického vykazování (ER)](general-electronic-reporting.md#Configuration) z globálního úložiště konfigurační služby.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="8e3fa-105">Další informace viz [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, konfigurační služba](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="8e3fa-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="8e3fa-106">Otevřete úložiště konfigurací</span><span class="sxs-lookup"><span data-stu-id="8e3fa-106">Open configurations repository</span></span>

1. <span data-ttu-id="8e3fa-107">Přihlaste se k aplikaci Dynamics 365 Finance použitím některé z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="8e3fa-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="8e3fa-108">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8e3fa-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="8e3fa-109">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8e3fa-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="8e3fa-110">Správce systému</span><span class="sxs-lookup"><span data-stu-id="8e3fa-110">System administrator</span></span>

2. <span data-ttu-id="8e3fa-111">Přejděte do části **Správa organizace > Pracovní prostory > Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="8e3fa-112">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="8e3fa-113">Na dlaždici **Microsoft** vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Pracovní prostor elektronického vykazování](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="8e3fa-115">Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **Globální**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="8e3fa-116">Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="8e3fa-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="8e3fa-117">Vyberte **Přidat** a přidejte nové úložiště.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="8e3fa-118">Vyberte **Globální** jako typ úložiště a poté vyberte **Vytvořit úložiště**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="8e3fa-119">Po výzvy postupujte podle pokynů k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="8e3fa-120">Zadejte název a popis úložiště a poté vyberte **OK** k potvrzení nové položky úložiště.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="8e3fa-121">V mřížce vyberte nové úložiště typu **Globální**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="8e3fa-122">Vyberte **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Stránka úložišť konfigurace](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="8e3fa-124">Import jediné konfigurace</span><span class="sxs-lookup"><span data-stu-id="8e3fa-124">Import a single configuration</span></span>

1. <span data-ttu-id="8e3fa-125">Na stránce **Úložiště konfigurace**, ve stromu konfigurací, vyberte požadovanou konfiguraci ER.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="8e3fa-126">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="8e3fa-127">Vyberte **Importovat**, chcete-li stáhnout vybranou verzi z globálního úložiště do aktuální instance aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e3fa-128">Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci Finance přítomny.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Stránka úložiště konfigurace](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="8e3fa-130">Import filtrovaných konfigurací</span><span class="sxs-lookup"><span data-stu-id="8e3fa-130">Import filtered configurations</span></span>

1. <span data-ttu-id="8e3fa-131">Na stránce **Úložiště konfigurace**, ve stromu konfigurací, rozbalte pevnou záložku **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="8e3fa-132">V mřížce **Značky** přidejte všechny potřebné značky.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="8e3fa-133">V poli **Použitelnost země / regionu** vyberte příslušné kódy zemí / regionů a poté vyberte **Použít filtr**.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e3fa-134">Pevná záložka **Konfigurace** zobrazuje všechny konfigurace, které splňují zadané podmínky výběru.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="8e3fa-135">Na pevné záložce **Konfigurace** vyberte **Import**, chcete-li stáhnout filtrované konfigurace z globálního úložiště do aktuální instance.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="8e3fa-136">Na pevné záložce **Konfigurace** vyberte **Reset filtru** k vyčištění stanovených podmínek výběru.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Stránka úložiště konfigurace](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="8e3fa-138">V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="8e3fa-139">Můžete být upozorněni na potíže se zjištěnou nekonzistencí.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="8e3fa-140">Tyto potíže je nutné před importováním verze konfigurace odstranit.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="8e3fa-141">Další informace naleznete v seznam souvisejících zdrojů pro toto téma.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="8e3fa-142">Konfigurace ER lze konfigurovat jako závislé na jiných konfiguracích.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="8e3fa-143">Proto spolu s vybranou konfigurací mohou být automaticky importovány i další konfigurace.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="8e3fa-144">Další informace o závislostech konfigurací najdete v článku [Definujte závislost ER konfigurací na jiných komponentách](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="8e3fa-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e3fa-145">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="8e3fa-145">Additional resources</span></span>

[<span data-ttu-id="8e3fa-146">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8e3fa-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]