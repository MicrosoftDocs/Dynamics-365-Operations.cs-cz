---
title: Stažení konfigurace elektronického vykazování ze služby Lifecycle Services
description: Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4cc14860bd969048c4378b40d97a7940a8710e89
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934647"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="c472e-103">Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c472e-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c472e-104">Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c472e-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c472e-105">Tento kurz vás provede stahováním nejnovější verze konfigurací elektronických sestav (ER) v rámci Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c472e-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="c472e-106">Přihlaste se k aplikaci použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="c472e-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="c472e-107">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="c472e-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="c472e-108">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="c472e-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="c472e-109">Správce systému</span><span class="sxs-lookup"><span data-stu-id="c472e-109">System administrator</span></span>

2. <span data-ttu-id="c472e-110">Přejděte do části **Správa organizace** &gt; **Pracovní prostory** &gt; **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="c472e-110">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="c472e-111">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="c472e-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="c472e-112">Na dlaždici **Microsoft** klepněte na tlačítko **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="c472e-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="c472e-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="c472e-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="c472e-114">Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="c472e-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="c472e-115">Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="c472e-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="c472e-116">Kliknutím na **Přidat** přidejte nové úložiště.</span><span class="sxs-lookup"><span data-stu-id="c472e-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="c472e-117">Vyberte možnost **LCS** jako typ úložiště.</span><span class="sxs-lookup"><span data-stu-id="c472e-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="c472e-118">Klikněte na **Vytvořit úložiště**.</span><span class="sxs-lookup"><span data-stu-id="c472e-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="c472e-119">Po výzvy postupujte podle pokynů k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="c472e-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="c472e-120">Zadejte název a popis úložiště.</span><span class="sxs-lookup"><span data-stu-id="c472e-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="c472e-121">Kliknutím na **OK** potvrďte nový záznam úložiště.</span><span class="sxs-lookup"><span data-stu-id="c472e-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="c472e-122">V mřížce vyberte nové úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="c472e-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="c472e-123">Klepněte na tlačítko **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.</span><span class="sxs-lookup"><span data-stu-id="c472e-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="c472e-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="c472e-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="c472e-125">Ve stromu konfigurací v levém podokně vyberte konfiguraci ER, kterou potřebujete.</span><span class="sxs-lookup"><span data-stu-id="c472e-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="c472e-126">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="c472e-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="c472e-127">Kliknutím na tlačítko **Importovat** stáhnete vybranou verzi ze LCS do aktuální instance.</span><span class="sxs-lookup"><span data-stu-id="c472e-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c472e-128">Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci přítomny.</span><span class="sxs-lookup"><span data-stu-id="c472e-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="c472e-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="c472e-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c472e-130">V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu.</span><span class="sxs-lookup"><span data-stu-id="c472e-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="c472e-131">Můžete být upozorněni na potíže se zjištěnou nekonzistencí.</span><span class="sxs-lookup"><span data-stu-id="c472e-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="c472e-132">Tyto potíže je nutné před importováním verze konfigurace odstranit.</span><span class="sxs-lookup"><span data-stu-id="c472e-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="c472e-133">Další informace naleznete v seznam souvisejících článků pro toto téma.</span><span class="sxs-lookup"><span data-stu-id="c472e-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c472e-134">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c472e-134">Additional resources</span></span>

[<span data-ttu-id="c472e-135">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="c472e-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
