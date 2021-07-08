---
title: Stažení konfigurace elektronického vykazování ze služby Lifecycle Services
description: Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271176"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="d4386-103">Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d4386-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4386-104">Tohle téma popisuje, jak stáhnout nejnovější verzi [konfigurací elektronického výkaznictví](general-electronic-reporting.md#Configuration) z [knihovny sdíleného majetku](../lifecycle-services/asset-library.md) v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d4386-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4386-105">Používání služby LCS jako úložiště pro konfigurace elektronického výkaznictví (ER) je označeno jako [zastaralé](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="d4386-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="d4386-106">Další informace viz [Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="d4386-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="d4386-107">Přihlaste se k aplikaci použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="d4386-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="d4386-108">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d4386-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="d4386-109">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d4386-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d4386-110">Správce systému</span><span class="sxs-lookup"><span data-stu-id="d4386-110">System administrator</span></span>

2. <span data-ttu-id="d4386-111">Přejděte do části **Správa organizace** &gt; **Pracovní prostory** &gt; **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="d4386-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="d4386-112">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="d4386-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="d4386-113">Na dlaždici **Microsoft** vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="d4386-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="d4386-114">[![Dlaždice Microsoft na stránce Konfigurace lokalizace](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="d4386-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="d4386-115">Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="d4386-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="d4386-116">Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="d4386-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="d4386-117">Volbou **Přidat** přidejte úložiště.</span><span class="sxs-lookup"><span data-stu-id="d4386-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="d4386-118">Vyberte možnost **LCS** jako typ úložiště.</span><span class="sxs-lookup"><span data-stu-id="d4386-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="d4386-119">Zvolte **Vytvořit úložiště**.</span><span class="sxs-lookup"><span data-stu-id="d4386-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="d4386-120">Pokud se zobrazí výzva k autorizaci, postupujte podle pokynů na obrazovce.</span><span class="sxs-lookup"><span data-stu-id="d4386-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="d4386-121">Zadejte název a popis úložiště.</span><span class="sxs-lookup"><span data-stu-id="d4386-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="d4386-122">Volbou **OK** potvrďte nový záznam úložiště.</span><span class="sxs-lookup"><span data-stu-id="d4386-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="d4386-123">V mřížce vyberte nové úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="d4386-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="d4386-124">Vyberte **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.</span><span class="sxs-lookup"><span data-stu-id="d4386-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="d4386-125">[![Stránka úložišť konfigurace](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="d4386-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="d4386-126">Pokud máte potíže s přístupem do úložiště LCS ke stažení konfigurací ze sdílené knihovny majetku v LCS, můžete si konfigurace stánout také z [globálního úložiště](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="d4386-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="d4386-127">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="d4386-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="d4386-128">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="d4386-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="d4386-129">Volbou **Importovat** stáhnete vybranou verzi ze LCS do aktuální instance.</span><span class="sxs-lookup"><span data-stu-id="d4386-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4386-130">Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci přítomny.</span><span class="sxs-lookup"><span data-stu-id="d4386-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="d4386-131">[![Stránka úložiště konfigurace](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="d4386-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d4386-132">V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu.</span><span class="sxs-lookup"><span data-stu-id="d4386-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="d4386-133">Můžete být upozorněni na potíže se zjištěnou nekonzistencí.</span><span class="sxs-lookup"><span data-stu-id="d4386-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="d4386-134">Tyto potíže je nutné před importováním verze konfigurace odstranit.</span><span class="sxs-lookup"><span data-stu-id="d4386-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="d4386-135">Další informace naleznete v seznam souvisejících témat pro toto téma.</span><span class="sxs-lookup"><span data-stu-id="d4386-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4386-136">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d4386-136">Additional resources</span></span>

[<span data-ttu-id="d4386-137">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d4386-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="d4386-138">Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby</span><span class="sxs-lookup"><span data-stu-id="d4386-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
