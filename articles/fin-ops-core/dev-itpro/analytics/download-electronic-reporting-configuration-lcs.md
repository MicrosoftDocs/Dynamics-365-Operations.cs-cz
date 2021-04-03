---
title: Stažení konfigurace elektronického vykazování ze služby Lifecycle Services
description: Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 8aaa3be426c0321da7e72d6acc18918d8b0ecee2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570363"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="91464-103">Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="91464-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91464-104">Tohle téma popisuje, jak stáhnout nejnovější verzi [konfigurací elektronického výkaznictví](general-electronic-reporting.md#Configuration) z [knihovny sdíleného majetku](../lifecycle-services/asset-library.md) v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="91464-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="91464-105">Přihlaste se k aplikaci použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="91464-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="91464-106">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="91464-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="91464-107">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="91464-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="91464-108">Správce systému</span><span class="sxs-lookup"><span data-stu-id="91464-108">System administrator</span></span>

2. <span data-ttu-id="91464-109">Přejděte do části **Správa organizace** &gt; **Pracovní prostory** &gt; **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="91464-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="91464-110">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="91464-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="91464-111">Na dlaždici **Microsoft** vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="91464-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="91464-112">[![Dlaždice Microsoft na stránce Konfigurace lokalizace](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="91464-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="91464-113">Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="91464-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="91464-114">Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="91464-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="91464-115">Volbou **Přidat** přidejte úložiště.</span><span class="sxs-lookup"><span data-stu-id="91464-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="91464-116">Vyberte možnost **LCS** jako typ úložiště.</span><span class="sxs-lookup"><span data-stu-id="91464-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="91464-117">Zvolte **Vytvořit úložiště**.</span><span class="sxs-lookup"><span data-stu-id="91464-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="91464-118">Pokud se zobrazí výzva k autorizaci, postupujte podle pokynů na obrazovce.</span><span class="sxs-lookup"><span data-stu-id="91464-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="91464-119">Zadejte název a popis úložiště.</span><span class="sxs-lookup"><span data-stu-id="91464-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="91464-120">Volbou **OK** potvrďte nový záznam úložiště.</span><span class="sxs-lookup"><span data-stu-id="91464-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="91464-121">V mřížce vyberte nové úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="91464-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="91464-122">Vyberte **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.</span><span class="sxs-lookup"><span data-stu-id="91464-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="91464-123">[![Stránka úložišť konfigurace](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="91464-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="91464-124">Pokud máte potíže s přístupem do úložiště LCS ke stažení konfigurací ze sdílené knihovny majetku v LCS, můžete si konfigurace stánout také z [globálního úložiště](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="91464-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="91464-125">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="91464-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="91464-126">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="91464-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="91464-127">Volbou **Importovat** stáhnete vybranou verzi ze LCS do aktuální instance.</span><span class="sxs-lookup"><span data-stu-id="91464-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="91464-128">Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci přítomny.</span><span class="sxs-lookup"><span data-stu-id="91464-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="91464-129">[![Stránka úložiště konfigurace](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="91464-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="91464-130">V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu.</span><span class="sxs-lookup"><span data-stu-id="91464-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="91464-131">Můžete být upozorněni na potíže se zjištěnou nekonzistencí.</span><span class="sxs-lookup"><span data-stu-id="91464-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="91464-132">Tyto potíže je nutné před importováním verze konfigurace odstranit.</span><span class="sxs-lookup"><span data-stu-id="91464-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="91464-133">Další informace naleznete v seznam souvisejících témat pro toto téma.</span><span class="sxs-lookup"><span data-stu-id="91464-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91464-134">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="91464-134">Additional resources</span></span>

[<span data-ttu-id="91464-135">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="91464-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="91464-136">Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby</span><span class="sxs-lookup"><span data-stu-id="91464-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]