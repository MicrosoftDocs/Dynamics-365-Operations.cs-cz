---
title: "Stažení konfigurace elektronického vykazování ze služby Lifecycle Services"
description: "Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 116142ed7c1e48fa90d95b7a6f65a75568d4b0d2
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="6ea91-103">Stažení konfigurace elektronického vykazování ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6ea91-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6ea91-104">Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6ea91-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="6ea91-105">Tento kurz vás provede stahováním nejnovější verze konfigurací elektronických sestav (ER) v rámci Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6ea91-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1.  <span data-ttu-id="6ea91-106">Přihlaste se k aplikaci Finance and Operations použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="6ea91-106">Sign in to Finance and Operations by using one of the following roles:</span></span>
    -   <span data-ttu-id="6ea91-107">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="6ea91-107">Electronic reporting developer</span></span>
    -   <span data-ttu-id="6ea91-108">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="6ea91-108">Electronic reporting functional consultant</span></span>
    -   <span data-ttu-id="6ea91-109">Správce systému</span><span class="sxs-lookup"><span data-stu-id="6ea91-109">System administrator</span></span>

2.  <span data-ttu-id="6ea91-110">Přejděte do části **Správa organizace** &gt; **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="6ea91-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3.  <span data-ttu-id="6ea91-111">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="6ea91-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4.  <span data-ttu-id="6ea91-112">Na dlaždici **Microsoft** klepněte na tlačítko **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="6ea91-112">On the **Microsoft** tile, click **Repositories**.</span></span> <span data-ttu-id="6ea91-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="6ea91-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>
5.  <span data-ttu-id="6ea91-114">Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="6ea91-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="6ea91-115">Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="6ea91-115">If this repository doesn't appear in the grid, follow these steps:</span></span>
    1.  <span data-ttu-id="6ea91-116">Kliknutím na **Přidat** přidejte nové úložiště.</span><span class="sxs-lookup"><span data-stu-id="6ea91-116">Click **Add** to add a new repository.</span></span>
    2.  <span data-ttu-id="6ea91-117">Vyberte možnost **LCS** jako typ úložiště.</span><span class="sxs-lookup"><span data-stu-id="6ea91-117">Select **LCS** as the repository type.</span></span>
    3.  <span data-ttu-id="6ea91-118">Klikněte na **Vytvořit úložiště**.</span><span class="sxs-lookup"><span data-stu-id="6ea91-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="6ea91-119">Po výzvy postupujte podle pokynů k autorizaci.</span><span class="sxs-lookup"><span data-stu-id="6ea91-119">If prompted, follow the authorization instructions.</span></span>
    5.  <span data-ttu-id="6ea91-120">Zadejte název a popis úložiště.</span><span class="sxs-lookup"><span data-stu-id="6ea91-120">Enter a name and description for the repository.</span></span>
    6.  <span data-ttu-id="6ea91-121">Kliknutím na **OK** potvrďte nový záznam úložiště.</span><span class="sxs-lookup"><span data-stu-id="6ea91-121">Click **OK** to confirm the new repository entry.</span></span>
    7.  <span data-ttu-id="6ea91-122">V mřížce vyberte nové úložiště typu **LCS**.</span><span class="sxs-lookup"><span data-stu-id="6ea91-122">In the grid, select the new repository of the **LCS** type.</span></span>

6.  <span data-ttu-id="6ea91-123">Klepněte na tlačítko **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.</span><span class="sxs-lookup"><span data-stu-id="6ea91-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span> <span data-ttu-id="6ea91-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="6ea91-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>
7.  <span data-ttu-id="6ea91-125">Ve stromu konfigurací v levém podokně vyberte konfiguraci ER, kterou potřebujete.</span><span class="sxs-lookup"><span data-stu-id="6ea91-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8.  <span data-ttu-id="6ea91-126">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="6ea91-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9.  <span data-ttu-id="6ea91-127">Kliknutím na tlačítko **Importovat** stáhnete vybranou verzi ze LCS do aktuální instance aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ea91-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span> <span data-ttu-id="6ea91-128">**Poznámka:** Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci aplikace Finance and Operations přítomny.</span><span class="sxs-lookup"><span data-stu-id="6ea91-128">**Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span> <span data-ttu-id="6ea91-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="6ea91-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

<span data-ttu-id="6ea91-130">**Poznámka:** V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-130">**Note:** Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="6ea91-131">Můžete být upozorněni na potíže se zjištěnou nekonzistencí.</span><span class="sxs-lookup"><span data-stu-id="6ea91-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="6ea91-132">Tyto potíže je nutné před importováním verze konfigurace odstranit.</span><span class="sxs-lookup"><span data-stu-id="6ea91-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="6ea91-133">Další informace naleznete v seznam souvisejících článků pro toto téma.</span><span class="sxs-lookup"><span data-stu-id="6ea91-133">For more information, see the list of related articles for this topic.</span></span>

<a name="see-also"></a><span data-ttu-id="6ea91-134">Viz také</span><span class="sxs-lookup"><span data-stu-id="6ea91-134">See also</span></span>
--------

[<span data-ttu-id="6ea91-135">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="6ea91-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)




